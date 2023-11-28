---
title: Konfigurera administratörssäkerhet
description: Lär dig konfigurera säkerhet för din butiksadministratör.
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
source-git-commit: e301cfaeec3a8427fff6138ba041bdbd7433c137
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%

---

# Konfigurera administratörssäkerhet

Vi rekommenderar att du använder ett mångfacetterat tillvägagångssätt för att skydda din butik. Du kan börja med en [anpassad administratörs-URL](../stores-purchase/store-urls.md#use-a-custom-admin-url) det är inte lätt att gissa sig till, snarare än den självklara &quot;Admin&quot; eller &quot;Backend&quot;. Som standard används lösenord för [logga in](../getting-started/admin-signin.md) Admin måste innehålla minst sju tecken och innehålla både bokstäver och siffror. Som en [bästa praxis](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html)använder du bara starka administratörslösenord som innehåller en kombination av bokstäver, siffror och symboler. Adobe Commerce och Magento Open Source tillåter inte återanvändning av de fyra sista lösenorden som tilldelats kontot.

Administratörens säkerhetskonfiguration ger dig möjlighet att:

- Lägg till en hemlig nyckel till URL-adresser
- Kräv att lösenord är skiftlägeskänsliga
- Begränsa längden på administratörssessioner
- Begränsa lösenordens livslängd
- Begränsa antalet inloggningsförsök som kan göras innan administratörens användarkonto är [låst](permissions-users-all.md#locked-users).

För ökad säkerhet kan du konfigurera längden på tangentbordsinaktivitet innan den aktuella sessionen förfaller och kräva att användarnamnet och lösenordet är skiftlägeskänsliga.

Förutom säkerhetsinställningarna i det här avsnittet [tvåfaktorsautentisering](security-two-factor-authentication.md) (2FA) krävs för att verifiera användarens identitet med ett engångslösenord som genereras av en app eller enhet. Du uppmanas att konfigurera 2FA första gången du loggar in i Admin. För ytterligare säkerhet kan administratörsinloggningen även konfigureras så att en [CAPTCHA](security-captcha.md).

>[!NOTE]
>
>Lager som har aktiverats [!DNL Adobe Identity Management Services] (IMS)-autentisering har inbyggda Adobe Commerce och Magento Open Source 2FA inaktiverat. Administratörsanvändare som är inloggade på sin Commerce-instans med sina inloggningsuppgifter för Adobe behöver inte autentisera igen för många administratörsuppgifter. Autentisering hanteras av Adobe IMS när administratörsanvändaren loggar in på sin aktuella session. Se [[!DNL Adobe Identity Management Service] (IMS) Integreringsöversikt](../getting-started/adobe-ims-integration-overview.md).

Teknisk information finns på [Säkerhet - översikt](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target=&quot;_blank&quot;} i utvecklardokumentationen.

![Administratörssäkerhet](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## Konfigurera administratörssäkerhet

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I den vänstra panelen under _[!UICONTROL Advanced]_, välja **[!UICONTROL Admin]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Security]** -avsnitt.

1. Om du vill förhindra att administratörsanvändare loggar in från samma konto på olika enheter anger du **[!UICONTROL Admin Account Sharing]** till `No`.

1. Ange vilken metod som ska användas för att hantera begäranden om återställning av lösenord **[!UICONTROL Password Reset Protection Type]** till något av följande:

   - `By IP and Email` — Lösenordet kan återställas online när ett svar har tagits emot från meddelandet skickas till den e-postadress som är kopplad till administratörskontot.
   - `By IP` — Lösenordet kan återställas online utan ytterligare bekräftelse.
   - `By Email` — Lösenordet kan endast återställas genom att du svarar via e-post på meddelandet som skickas till den e-postadress som är kopplad till administratörskontot.
   - `None` — Lösenordet kan bara återställas av butiksadministratören.

1. Ange säkerhetsalternativ för inloggning:

   - För **[!UICONTROL Recovery Link Expiration Period (hours)]** anger du antalet timmar som en länk för lösenordsåterställning är giltig.

   - Om du vill bestämma det maximala antalet lösenordsbegäranden som kan skickas per timme anger du numret för **[!UICONTROL Max Number of Password Reset Requests]**.

   - För **[!UICONTROL Min Time Between Password Reset Requests]** anger du det minsta antal minuter som måste gå mellan begäranden om återställning av lösenord.

   - Om du vill lägga till en hemlig nyckel till Admin URL som en försiktighetsåtgärd mot explosioner anger du **[!UICONTROL Add Secret Key to URLs]** till `Yes`. Den här inställningen är aktiverad som standard.

   - Om du vill kräva att gemener och versaler i inloggningsuppgifterna som anges matchar det som lagras i systemet anger du **[!UICONTROL Login is Case Sensitive]** till `Yes`.

   - Om du vill bestämma längden på en administratörssession innan timeout inträffar anger du sessionens längd i sekunder för **[!UICONTROL Admin Session Lifetime (seconds)]** fält. Värdet måste vara minst 60 sekunder.

   - För **[!UICONTROL Maximum Login Failures to Lockout Account]** anger du hur många gånger en användare kan försöka logga in på administratören innan kontot är låst. Som standard tillåts sex försök. Lämna fältet tomt för obegränsat antal inloggningsförsök.

   - För **[!UICONTROL Lockout Time (minutes)]** anger du antalet minuter som ett administratörskonto låses när det maximala antalet försök uppfylls.

1. Ange alternativ för lösenord:

   - Om du vill begränsa längden på administratörslösenord anger du antalet dagar som ett lösenord gäller för **[!UICONTROL Password Lifetime (days)]**. Under en obegränsad livstid lämnar du fältet tomt.

   - Ange **[!UICONTROL Password Change]** till något av följande:

      - `Forced` — Kräver att administratörsanvändare ändrar sina lösenord efter kontoinställningarna.
      - `Recommended` — Rekommenderar att administratörsanvändare ändrar sina lösenord efter kontoinställningarna.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Krav för administratörslösenord

Som standard måste ett administratörslösenord innehålla minst sju tecken och innehålla både bokstäver och siffror.
