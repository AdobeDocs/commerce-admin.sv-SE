---
title: Google reCAPTCHA
description: Lär dig konfigurera Google reCAPTCHA för administratörsåtkomst och olika butiksåtgärder som initierats av registrerade kunder.
exl-id: c3b53702-0882-4ac4-9cf5-39fefc90005e
role: Admin
feature: Configuration, Security
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '1061'
ht-degree: 0%

---

# Google reCAPTCHA

[Google reCAPTCHA](https://developers.google.com/recaptcha) ser till att en människa interagerar med webbplatsen i stället för en dator (eller robot). Till skillnad från Adobe Commerce och Magento Open Source [CAPTCHA](security-captcha.md) har Google reCAPTCHA förbättrat säkerheten med ett urval av olika visningsalternativ och visningsmetoder. Ytterligare trafikinformation finns på kontrollpanelen för ditt Google reCAPTCHA-konto.

Google reCAPTCHA konfigureras separat för Admin och storefront.

- För Admin kan Google reCAPTCHA användas på [inloggningssidan](../getting-started/admin-signin.md) och när en användare begär en lösenordsåterställning. Om Commerce [CAPTCHA](security-captcha.md) också är aktiverat kan Google reCAPTCHA användas samtidigt utan problem.

- För butiken kan Google reCAPTCHA användas för att logga in på ett [kundkonto](../customers/customer-sign-in.md), skicka ett meddelande från sidan [Kontakta oss](../getting-started/store-details.md#contact-us-form) och på flera andra platser i butiken.

  ![Google reCAPTCHA - kundinloggning](./assets/customer-account-login-recaptcha.png){width="700" zoomable="yes"}

Google reCAPTCHA kan implementeras på flera sätt:

- _reCAPTCHA v3 Osynlig_ - Använder en algoritm för att klassificera användarinteraktioner och avgör sannolikheten för att användaren är mänsklig baserat på ett poängvärde.

- _reCAPTCHA v2 Osynlig_ - Utför bakgrundsverifiering utan användarinteraktion. Användare och kunder verifieras automatiskt, men de kan behöva välja ut specifika bilder för att klara en utmaning.

- _reCAPTCHA v2 (&quot;Jag är inte en robot&quot;)_ - Validerar begäranden med kryssrutan _&quot;Jag är inte en robot&quot;_.

>[!IMPORTANT]
>
>Innan du kan konfigurera Google reCAPTCHA kontrollerar du att filen `PHP.ini` innehåller följande inställning: `allow_url_fopen = 1`. Detta kan kräva hjälp av utvecklare. Se [Nödvändiga PHP-inställningar](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html?lang=sv-SE){:target="_blank"} i installationshandboken.

## Steg 1: Generera Google reCAPTCHA-nycklar

Google reCAPTCHA kräver ett par API-nycklar för att kunna aktiveras. Du kan få dessa nycklar kostnadsfritt via reCAPTCHA-webbplatsen. Innan du genererar nycklarna måste du känna till vilken typ av reCAPTCHA du vill använda.

1. Öppna Google reCAPTCHA-sidan och logga in på ditt konto.

1. För **[!UICONTROL Label]** anger du ett namn som identifierar nycklarna för intern referens.

   Du behöver en uppsättning nycklar för varje reCAPTCHA-typ som används i din Adobe Commerce- eller Magento Open Source-installation. Till exempel: `Commerce Invisible`

1. För **[!UICONTROL reCAPTCHA type]** väljer du den metod som du vill använda.

   - _reCAPTCHA v3 osynlig_
   - _reCAPTCHA v2 Osynlig_
   - _reCAPTCHA v2 (&quot;Jag är inte en robot&quot;)_

1. Ange din butiks domän för **[!UICONTROL Domain]**. Till exempel: mystore.com

   Om du har flera arkiv med olika domäner anger du varje domän på en separat rad.

   - Lägg till din butiksdomän och eventuella underdomäner.
   - Du kan lägga till `localhost`, andra lokala VM-domäner och mellanlagringsdomäner efter behov för testning.

1. Markera kryssrutan till **[!UICONTROL Accept the reCAPTCHA Terms of Service]**.

1. (Valfritt) Markera kryssrutan **[!UICONTROL Send alerts to owners]** för att skicka meddelanden om Google upptäcker problem eller misstänkt trafik.

1. Klicka på **[!UICONTROL Submit]** för att slutföra registreringen och ta emot nycklar.

   >[!IMPORTANT]
   >
   >Alla nycklar gäller inte för alla typer av reCAPTCHA, och om du använder dem fel kan det leda till oväntat beteende. Google reCAPTCHA-nycklar som genererats för reCAPTCHA v2 &quot;Jag är inte en robot&quot; fungerar inte med _reCAPTCHA v2 Invisible_ och kan blockera funktioner där reCAPTCHA är aktiverat.

## Steg 2: Konfigurera Google reCAPTCHA för administratören

[!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."}

1. Logga in på ditt Admin-konto.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidlisten Admin.

1. I det övre högra hörnet anger du **[!UICONTROL Store View]** till `Default Config`.

1. Expandera **[!UICONTROL Security]** i den vänstra panelen och klicka på **[!UICONTROL Google reCAPTCHA Admin Panel]**.

   >[!NOTE]
   >
   >Avmarkera kryssrutan **[!UICONTROL Use system value]** för varje fält som du vill konfigurera.

1. Om du vill använda _[!DNL reCAPTCHA v2 ("I am not a robot")]_&#x200B;expanderar du avsnittet **[!UICONTROL reCAPTCHA v2 ("I am not a robot")]**&#x200B;och gör följande:

   - För **[!UICONTROL Google API Website Key]** anger du webbplatsnyckeln som skapades för den här reCAPTCHA-typen när du registrerade ditt Google reCAPTCHA-konto.

   - För **[!UICONTROL Google API Secret Key]** anger du den hemliga nyckel som är kopplad till ditt Google reCAPTCHA-konto.

   - För **[!UICONTROL Size]** väljer du storleken på den Google reCAPTCHA-ruta som du vill ska visas. Alternativ: `Normal (default)` / `Compact`

   - För **[!UICONTROL Theme]** väljer du det tema som du vill använda för att formatera rutan Google reCAPTCHA. Alternativ: `Light Theme (default)` / `Dark Theme`

   - För **[!UICONTROL Language Code]** anger du koden med två tecken för att ange [språket som används för Google reCAPTCHA-text och -meddelanden](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 -&quot;Jag är inte en robot&quot;](../configuration-reference/security/assets/recaptcha-admin-v2-not-robot.png){width="600" zoomable="yes"}

1. Om du vill använda _[!DNL reCAPTCHA v2 Invisible]_&#x200B;expanderar du avsnittet **[!UICONTROL reCAPTCHA v2 Invisible]**&#x200B;och gör följande:

   - För **[!UICONTROL Google API Website Key]** anger du webbplatsnyckeln som skapades för den här reCAPTCHA-typen när du registrerade ditt Google reCAPTCHA-konto.

   - För **[!UICONTROL Google API Secret Key]** anger du den hemliga nyckel som är kopplad till ditt Google reCAPTCHA-konto.

   - För **[!UICONTROL Invisible Badge Position]** väljer du den märkordsposition som ska användas på varje sida. Alternativ: `Inline` / `Bottom Right` / `Bottom Left`

   - För **[!UICONTROL Theme]** väljer du det tema som ska användas för att formatera rutan Google reCAPTCHA. Alternativ: `Light Theme (default)` / `Dark Theme`

   - För **[!UICONTROL Language Code]** anger du en kod med två tecken som anger [språket som används för Google reCAPTCHA-text och -meddelanden](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 Osynlig](../configuration-reference/security/assets/recaptcha-admin-v2-invisible.png){width="600" zoomable="yes"}

1. Om du vill använda _[!DNL reCAPTCHA v3 Invisible]_&#x200B;expanderar du avsnittet **[!UICONTROL reCAPTCHA v3 Invisible]**&#x200B;och gör följande:

   - För **[!UICONTROL Google API Website Key]** anger du webbplatsnyckeln som skapades för den här reCAPTCHA-typen när du registrerade ditt Google reCAPTCHA-konto.

   - För **[!UICONTROL Google API Secret Key]** anger du den hemliga nyckel som är kopplad till ditt Google reCAPTCHA-konto.

   - Ange **[!UICONTROL Minimum Score Threshold]** för att identifiera när en användarinteraktion flaggas som en potentiell risk, där 1.0 är en typisk användarinteraktion och 0.0 troligtvis är en robot. Standard: `0.5`

   - För **[!UICONTROL Invisible Badge Position]** väljer du den position som ska användas på varje sida. Alternativ: `Inline` / `Bottom Right` / `Bottom Left`

   - För **[!UICONTROL Theme]** väljer du det tema som ska användas för att formatera rutan Google reCAPTCHA. Alternativ: `Light Theme (default)` / `Dark Theme`

   - För **[!UICONTROL Language Code]** anger du en kod med två tecken som anger [språket som används för Google reCAPTCHA-text och -meddelanden](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v3 osynlig](../configuration-reference/security/assets/recaptcha-admin-v3-invisible.png){width="600" zoomable="yes"}

1. Expandera **[!UICONTROL reCAPTCHA Validation Failure Messages]** och ange de meddelanden som visas i administratören om valideringen misslyckas eller inte kan slutföras.

   ![reCAPTCHA-felmeddelanden](../configuration-reference/security/assets/recaptcha-admin-failure-messages.png){width="600" zoomable="yes"}

1. Expandera avsnittet **[!UICONTROL Admin Panel]** och konfigurera följande efter behov:

   - Ange **[!UICONTROL Enable for Login]** till den reCAPTCHA-typ som du vill använda för inloggningssidan för Admin.

   - Ange **[!UICONTROL Enable for Forgot Password]** till den reCAPTCHA-typ som du vill använda för begäranden om återställning av lösenord.

   Administrationsalternativ för ![reCAPTCHA](../configuration-reference/security/assets/recaptcha-admin-panel.png){width="600" zoomable="yes"}

## Steg 3: Konfigurera Google reCAPTCHA för butiken

1. Välj **[!UICONTROL Google reCAPTCHA Storefront]** i den vänstra panelen under _[!UICONTROL Security]_.

1. Fyll i avsnittet för varje reCAPTCHA-typ som du vill använda i butiken.

   Mer information om alternativen för varje reCAPTCHA-typ finns i _Steg 2: Konfigurera Google reCAPTCHA för Admin_.

1. Expandera **[!UICONTROL reCAPTCHA Validation Failure Messages]** och ange de meddelanden som visas i butiken om valideringen misslyckas eller inte kan slutföras.

1. Expandera avsnittet **[!UICONTROL Storefront]**.

   >[!NOTE]
   >
   >Avmarkera kryssrutan **[!UICONTROL Use system value]** för varje fält som du vill konfigurera.

1. Ställ in varje butiksplatsfält på den typ av reCAPTCHA som du har konfigurerat att använda.

   - [!UICONTROL Enable for Customer Login]
   - [!UICONTROL Enable for Forgot Password]
   - [!UICONTROL Enable for Create New Customer Account]
   - [!UICONTROL Enable for Edit Customer Account]
   - [!UICONTROL Enable for Create New Company Account] ![Adobe Commerce B2B](../assets/b2b.svg) (endast tillgängligt med Adobe Commerce B2B)
   - [!UICONTROL Enable for Contact Us]
   - [!UICONTROL Enable for Product Review]
   - [!UICONTROL Enable for Newsletter Subscription]
   - [!UICONTROL Enable for Gift Card] ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)
   - [!UICONTROL Enable for Invitation Create Account]
   - [!UICONTROL Enable for Send To Friend]
   - [!UICONTROL Enable for Checkout/Placing Order]
   - [!UICONTROL Enable for Wishlist Sharing]
   - [!UICONTROL Enable for Coupon Codes]
   - [!UICONTROL Enable for PayPal PayflowPro payment form]

   ![Alternativ för Storefront-konfiguration](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## Steg 4: Spara konfigurationen

1. När konfigurationsinställningarna är klara klickar du på **[!UICONTROL Save Config]**.

1. Klicka på **[!UICONTROL Cache Management]** i meddelandet längst upp på arbetsytan och uppdatera varje ogiltig cache.
