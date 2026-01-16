---
title: Google reCAPTCHA Enterprise
description: Lär dig hur du konfigurerar Google CAPTCHA Enterprise för att skydda din Adobe Commerce as a Cloud Service-butik från stötar och bedrägliga aktiviteter.
role: Admin
feature: Configuration, Security
badgeSaas: label="Endast SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce as a Cloud Service-projekt (SaaS-infrastruktur som hanteras av Adobe)."
source-git-commit: dde1d634a1c6c7435668a8ad6084b926cc0d6193
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---

# Google reCAPTCHA Enterprise

[!BADGE Sandbox]{type=Caution tooltip="Objekten i listan är för närvarande bara tillgängliga i sandlådemiljöer. Adobe släpper först uppdateringar i Sandbox så att du kan testa kommande ändringar innan de börjar i Production."}

[Google reCAPTCHA Enterprise](https://cloud.google.com/security/products/recaptcha#protect-against-fraud-and-abuse-with-modern-bot-protection-and-fraud-prevention-platform) ger avancerat robotskydd för din Adobe Commerce as a Cloud Service-butik genom att använda adaptiv riskanalys och maskininlärning för att skilja mellan människor och botar. Detta bidrar till att förhindra bedrägliga aktiviteter, skräppost och missbruk på din webbplats.

>[!NOTE]
>
>Den här funktionen har INTE stöd för reCAPTCHA för administratören.

Se [Google reCAPTCHA V3 och V2](security-google-recaptcha.md) för information om hur du konfigurerar andra versioner av Google reCAPTCHA.

## Funktioner

Google reCAPTCHA Enterprise har följande funktioner:

- **Avancerad robotidentifiering**: Använder Google Clouds maskininlärningsmodeller för överlägsen robotidentifiering
- **Riskanalys**: Innehåller detaljerade riskpoäng (0,0-1,0) för varje interaktion
- **Konfigurerbara tröskelvärden**: Ange minimala godtagbara riskpoäng per klientorganisation
- **Stöd för flera innehavare**: Konfiguration per innehavare med isolerade Google Cloud-projekt
- **Krypterade autentiseringsuppgifter**: Tjänstkontots autentiseringsuppgifter lagras krypterade i en databas
- **Formulärskydd**: Skyddar alla Commerce-standardformulär, inklusive inloggning, utcheckning, produktrecensioner med mera.

## Förutsättningar

Du behöver följande resurser innan du kan konfigurera Google reCAPTCHA Enterprise för din Adobe Commerce as a Cloud Service-butik:

- Ett aktivt Google Cloud-konto med reCAPTCHA Enterprise aktiverat.
- Tillgång till Google Cloud Console för att skapa och hantera reCAPTCHA Enterprise-nycklar.

På multi-tenant-installationer av Adobe Commerce as a Cloud Service måste varje klientorganisation ha ett eget Google Cloud-projekt och reCAPTCHA Enterprise-nycklar.

## Steg 1: Konfigurera Google reCAPTCHA Enterprise

Följ de här allmänna stegen för att konfigurera Google reCAPTCHA Enterprise för din butik. Detaljerade instruktioner finns i [Google reCAPTCHA Enterprise-dokumentationen](https://docs.cloud.google.com/recaptcha/docs/overview).

1. [Skapa ett Google Cloud-projekt](https://developers.google.com/workspace/guides/create-project) för din reCAPTCHA Enterprise-implementering.

1. Aktivera [reCAPTCHA Enterprise API](https://docs.cloud.google.com/recaptcha/docs/prepare-environment).

1. Skapa en poängbaserad reCAPTCHA Enterprise [webbplatsnyckel](https://docs.cloud.google.com/recaptcha/docs/choose-key-type).

1. Skapa ett tjänstkonto med IAM-rollen `roles/recaptchaenterprise.admin`.

1. Ladda ned JSON-nyckelfilen för tjänstkontot, som innehåller de inloggningsuppgifter som krävs för att autentisera din Adobe Commerce as a Cloud Service-butik med Google reCAPTCHA Enterprise.

## Steg 2: Konfigurera Google reCAPTCHA för butiken

1. Välj _[!UICONTROL Security]_&#x200B;i den vänstra panelen under **[!UICONTROL Google reCAPTCHA Storefront]**.

1. Fyll i avsnittet **[!UICONTROL reCAPTCHA Enterprise]** enligt följande.

   - För **[!UICONTROL Site Key]** kopierar och klistrar du in din reCAPTCHA Enterprise-webbplatsnyckel från din Google Cloud-konsol.

   - För **[!UICONTROL Google Cloud Project ID]** kopierar och klistrar du in projekt-ID:t från ditt Google Cloud-projekt.

   - För **[!UICONTROL Service Account JSON]** kopierar du innehållet i JSON-nyckelfilen för tjänstkontot som du hämtade i [Steg 1: Konfigurera Google reCAPTCHA Enterprise](#step-1-set-up-google-recaptcha-enterprise).

   - För **[!UICONTROL Minimum Score Threshold]** anger du det lägsta poängvärdet (0,0-1,0) för att identifiera när en användarinteraktion har flaggats som en potentiell risk. Poängen 1.0 är en typisk användarinteraktion och 0.0 är troligen en robot.

   - För **[!UICONTROL Badge Position]** väljer du positionen för det osynliga reCAPTCHA-märket på varje sida. Alternativ: `Inline` / `Bottom Right` / `Bottom Left`.

   - För **[!UICONTROL Theme]** väljer du antingen `Light Theme` (standard) eller `Dark Theme` för att fastställa formatet för rutan Google reCAPTCHA.

   - För **[!UICONTROL Language Code]** anger du en [tvåteckenskod](https://developers.google.com/recaptcha/docs/language) som anger vilket språk som används för Google reCAPTCHA-text och -meddelanden.

   - För **[!UICONTROL Validation Failure Message]** kan du ändra meddelandet som visas i butiken när valideringen inte lyckas.


1. Expandera avsnittet **[!UICONTROL Storefront]** och ange varje butiksformulär som du vill skydda till **[!UICONTROL reCAPTCHA Enterprise]**.

   {{recaptcha-forms-list}}

   ![Alternativ för Storefront-konfiguration](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## Steg 3: Spara konfigurationen

1. När konfigurationsinställningarna är klara klickar du på **[!UICONTROL Save Config]**.

1. Klicka på **[!UICONTROL Cache Management]** i meddelandet längst upp på arbetsytan och uppdatera varje ogiltig cache.
