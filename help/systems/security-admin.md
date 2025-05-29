---
title: Konfigurera administratörssäkerhet
description: Lär dig konfigurera säkerhet för din butiksadministratör.
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Konfigurera administratörssäkerhet

Vi rekommenderar att du använder ett mångfacetterat tillvägagångssätt för att skydda din butik. Du kan börja med att använda en [anpassad administratörs-URL](../stores-purchase/store-urls.md#use-a-custom-admin-url) som inte är enkel att gissa sig till, i stället för den självklara &quot;Admin&quot; eller &quot;Backend&quot;. Som standard måste lösenord som används för att [logga in](../getting-started/admin-signin.md) i Admin vara minst sju tecken långa och innehålla både bokstäver och siffror. Som [bästa praxis](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html) bör du bara använda starka administratörslösenord som innehåller en kombination av bokstäver, siffror och symboler. Adobe Commerce och Magento Open Source tillåter inte återanvändning av de fyra sista lösenorden som tilldelats kontot.

Administratörens säkerhetskonfiguration ger dig möjlighet att:

- Lägg till en hemlig nyckel till URL-adresser
- Kräv att lösenord är skiftlägeskänsliga
- Begränsa längden på administratörssessioner
- Begränsa lösenordens livslängd
- Begränsa antalet inloggningsförsök som kan göras innan administratörens användarkonto är [låst](permissions-users-all.md#locked-users).

För ökad säkerhet kan du konfigurera längden på tangentbordsinaktivitet innan den aktuella sessionen förfaller och kräva att användarnamnet och lösenordet är skiftlägeskänsliga.

Utöver säkerhetsinställningarna i det här avsnittet krävs [tvåfaktorautentisering](security-two-factor-authentication.md) (2FA) för att verifiera användarens identitet med ett engångslösenord som skapas av en app eller enhet. Du uppmanas att konfigurera 2FA första gången du loggar in i Admin. För ytterligare säkerhet kan administratörsinloggningen också konfigureras så att en [CAPTCHA](security-captcha.md) krävs.

>[!NOTE]
>
>Lager som har aktiverat [!DNL Adobe Identity Management Services] (IMS)-autentisering har inbyggda Adobe Commerce och Magento Open Source 2FA inaktiverade. Administratörsanvändare som är inloggade på sin Commerce-instans med sina Adobe-inloggningsuppgifter behöver inte autentisera igen för många administratörsuppgifter. Autentisering hanteras av Adobe IMS när administratörsanvändaren loggar in på sin aktuella session. Se [[!DNL Adobe Identity Management Service] (IMS)-integreringsöversikt](../getting-started/adobe-ims-integration-overview.md).

Mer teknisk information finns i [Säkerhetsöversikt](https://developer.adobe.com/commerce/php/architecture/basics/security/){:target="_blank"} i utvecklardokumentationen.

![Administratörssäkerhet](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## Konfigurera administratörssäkerhet

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Välj **[!UICONTROL Admin]** i den vänstra panelen under _[!UICONTROL Advanced]_.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Security]**.

1. Om du vill förhindra att administratörsanvändare loggar in från samma konto på olika enheter anger du **[!UICONTROL Admin Account Sharing]** till `No`.

1. Om du vill fastställa vilken metod som används för att hantera begäranden om återställning av lösenord anger du **[!UICONTROL Password Reset Protection Type]** till något av följande:

   - `By IP and Email` - Lösenordet kan återställas online när ett svar har tagits emot från meddelandet skickas till den e-postadress som är kopplad till administratörskontot.
   - `By IP` - Lösenordet kan återställas online utan ytterligare bekräftelse.
   - `By Email` - Lösenordet kan bara återställas genom att svara via e-post på meddelandet som skickas till den e-postadress som är kopplad till administratörskontot.
   - `None` - Lösenordet kan bara återställas av butiksadministratören.

1. Ange säkerhetsalternativ för inloggning:

   - För **[!UICONTROL Recovery Link Expiration Period (hours)]** anger du det antal timmar en länk för lösenordsåterställning fortfarande är giltig.

   - Om du vill fastställa det maximala antalet lösenordsbegäranden som kan skickas per timme anger du numret för **[!UICONTROL Max Number of Password Reset Requests]**.

   - För **[!UICONTROL Min Time Between Password Reset Requests]** anger du det minsta antal minuter som måste gå mellan begäranden om återställning av lösenord.

   - Ange **[!UICONTROL Add Secret Key to URLs]** till `Yes` om du vill lägga till en hemlig nyckel till Admin URL som en försiktighetsåtgärd mot attacker. Den här inställningen är aktiverad som standard.

   - Om du vill kräva att användningen av gemener och versaler i de inloggningsuppgifter som anges matchar det som lagras i systemet anger du **[!UICONTROL Login is Case Sensitive]** till `Yes`.

   - Om du vill fastställa längden på en administratörssession innan den timeout uppstår anger du sessionens varaktighet i sekunder för fältet **[!UICONTROL Admin Session Lifetime (seconds)]**. Värdet måste vara minst 60 sekunder.

   - För **[!UICONTROL Maximum Login Failures to Lockout Account]** anger du det antal gånger en användare kan försöka logga in på administratören innan kontot är låst. Som standard tillåts sex försök. Lämna fältet tomt för obegränsat antal inloggningsförsök.

   - För **[!UICONTROL Lockout Time (minutes)]** anger du det antal minuter som ett administratörskonto är låst när det maximala antalet försök uppfylls.

1. Ange alternativ för lösenord:

   - Om du vill begränsa livslängden för administratörslösenord anger du antalet dagar som ett lösenord är giltigt för **[!UICONTROL Password Lifetime (days)]**. Under en obegränsad livstid lämnar du fältet tomt.

   - Ange **[!UICONTROL Password Change]** till något av följande:

      - `Forced` - Kräver att administratörsanvändare ändrar sina lösenord efter kontoinställningarna.
      - `Recommended` - Rekommenderar att administratörsanvändare ändrar sina lösenord efter kontokonfigurationen.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Krav för administratörslösenord

Som standard måste ett administratörslösenord innehålla minst sju tecken och innehålla både bokstäver och siffror.
