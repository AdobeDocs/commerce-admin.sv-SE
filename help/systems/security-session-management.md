---
title: Sessionshantering
description: Lär dig hur du konfigurerar sessionshantering för att skydda administratören och butiken.
exl-id: ad954218-aa3e-44e6-b23f-008de7fc7543
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Sessionshantering

[Sessionshantering](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html) är en bästa praxis för att förhindra denial of service (DoS) för API-säkerhet. En session representerar den tid en besökare tillbringar på din webbplats och är inte relaterad till hur länge administratörsanvändare eller -kunder är inloggade på sina konton.

En session är en sekvens av nätverks-HTTP-begäran och svarstransaktioner som är associerade med samma användare. Det är ett sätt att associera en klient (Admin) med deras data när de ansluter till servern. Sessioner används för att skapa variabler, t.ex. åtkomsträttigheter och lokaliseringsinställningar, som gäller för varje interaktion en användare har med ett webbprogram under sessionen.

## Sessionsstorlek

Använd följande konfigurationsinställningar för att begränsa den maximala sessionsstorleken för administratörer och butiksbesökare:

- **[!UICONTROL Max Session Size in Admin]**—Begränsa den maximala sessionsstorleken i byte. Använd `0` för att inaktivera.
- **[!UICONTROL Max Session Size in Storefront]**—Begränsa den maximala sessionsstorleken i byte. Använd `0` för att inaktivera.

>[!TIP]
>
>Båda inställningarna mäts i byte och är som standard `256000` byte (eller 256 kB).

**_Så här konfigurerar du maximal sessionsstorlek:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]**  > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL System]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Security]** för att komma åt sessionsinställningarna.

   ![Sessionsinställningar](../configuration-reference/advanced/assets/system-security.png){width="600" zoomable="yes"}

1. Ange nya sessionsstorlekar i byte.

   >[!WARNING]
   >
   >Om värdet är för lågt kan det orsaka problem. Om du anger något av alternativen under standardvärdet 256000 byte visas ett varningsmeddelande. Klicka **[!UICONTROL No]**&#x200B;ändrar systemet värdet till `256000`.

1. Klicka på **[!UICONTROL Save Config]**.

### Administratörssessioner

Om du överskrider den maximala sessionsstorleken visas ett felmeddelande och sessionsstorleksbegränsningen loggas till `var/log` katalog.

Om du förlorar åtkomsten till administratören efter att du har angett sessionsstorleken för låg kan du återställa konfigurationen med CLI:

```bash
bin/magento config:set system/security/max_session_size_admin 256000
```

### Sessioner i butiker

Om du överskrider den maximala sessionsstorleken visas inget fel, men systemet loggar begränsningar för sessionsstorlek till `var/log` katalog.

## Sessionsvalidering

Med Adobe Commerce och Magento Open Source kan du validera sessionsvariabler som en skyddsåtgärd mot eventuella sessionsfixeringsattacker eller försök att förgifta eller kapa användarsessioner. Inställningarna för sessionsvalidering avgör hur sessionsvariabler valideras under varje butiksbesök och om sessions-ID inkluderas i butikens URL.

Teknisk information finns på [Använd Redis för sessionslagring](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-session.html) i _Konfigurationshandbok_.

![Allmän konfiguration - validering av webbsession](../configuration-reference/general/assets/web-session-validation-settings.png){width="600" zoomable="yes"}

Valideringen kontrollerar att besökarna är de som de säger att de är genom att jämföra värdet i valideringsvariablerna med sessionsdata som lagras i `$_SESSION` data för användaren. Valideringen misslyckas om informationen inte överförs som förväntat och motsvarande variabel är tom. Beroende på inställningarna för sessionsvalidering avslutas klientsessionen omedelbart om en sessionsvariabel misslyckas i valideringsprocessen.

Om du aktiverar alla valideringsvariabler kan du förhindra attacker, men det kan även påverka serverns prestanda. Som standard är all sessionsvariabelvalidering inaktiverad. Vi rekommenderar att du experimenterar med inställningarna för att hitta den bästa kombinationen för din Adobe Commerce- eller Magento Open Source-installation. Att aktivera alla valideringsvariabler kan visa sig vara onödigt begränsande och kan förhindra åtkomst till kunder som har internetanslutningar som passerar genom en proxyserver eller som kommer bakom en brandvägg. Mer information om sessionsvariabler och hur de används finns i systemadministrationsdokumentationen för ditt Linux®-system.

**_Så här konfigurerar du sessionsvalideringen:_**

1. På _Administratör_ sidebar, gå till  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen _[!UICONTROL General]_och välja **[!UICONTROL Web]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Session Validation Settings]** -avsnitt.

1. Ange vart och ett av konfigurationsalternativen:

   - **[!UICONTROL Validate REMOTE_ADDR]** — Ställ in på `Yes` för att verifiera att IP-adressen för en begäran matchar det som lagras i `$_SESSION` variabel.

   - **[!UICONTROL Validate HTTP_VIA]** — Ställ in på `Yes` för att verifiera att proxyadressen för en inkommande begäran matchar det som lagras i `$_SESSION` variabel.

   - **[!UICONTROL Validate HTTP_X_FORWARDED_FOR]** — Ställ in på `Yes` verifiera att den vidarebefordrade adressen för en begäran matchar det som lagras i `$_SESSION` variabel.

   - **[!UICONTROL Validate HTTP_USER_AGENT]** — Ställ in på `Yes` för att verifiera att webbläsaren eller enheten som används för att få åtkomst till butiken under en session matchar det som lagras i `$_SESSION` variabel.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Administratörssessionens livstid

Som en säkerhetsåtgärd _Administratör_ är inställt på timeout efter 900 sekunders (15 minuter) tangentbordsinaktivitet. Du kan justera sessionens livstid så att den passar din arbetsstil.

**_Så här justerar du administratörssessionens livstid:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Rulla ned och expandera **[!UICONTROL Advanced]** i den vänstra panelen.

1. Klicka på **[!UICONTROL Admin]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den _[!UICONTROL Security]_-avsnitt.

1. För **[!UICONTROL Admin Session Lifetime (seconds)]** anger du antalet sekunder som en session förblir aktiv innan timeout inträffar.

   ![Avancerad konfiguration - Säkerhetsinställningar för administratör](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.## Administratörssessionslivstid

Som en säkerhetsåtgärd _Administratör_ är inställt på timeout efter 900 sekunders (15 minuter) tangentbordsinaktivitet. Du kan justera sessionens livstid så att den passar din arbetsstil.

**_Så här justerar du administratörssessionens livstid:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Rulla ned och expandera **[!UICONTROL Advanced]** i den vänstra panelen.

1. Klicka på **[!UICONTROL Admin]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den _Säkerhet_ -avsnitt.

1. För **[!UICONTROL Admin Session Lifetime (seconds)]** anger du antalet sekunder som en session förblir aktiv innan timeout inträffar.

   ![Avancerad konfiguration - Säkerhetsinställningar för administratör](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
