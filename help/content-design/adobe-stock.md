---
title: Adobe Stock Integration
description: Integrera Adobe Stock med  [!DNL Commerce] -instansen för att få tillgång till ett oändligt antal mediefiler som kan användas i din butik.
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 9aec049cfaa12f342d66f45a75af0ce50a23c2c8
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Adobe Stock Integration

Integrera [Adobe Stock](https://stock.adobe.com) med [!UICONTROL Commerce] om du vill få tillgång till ett oändligt antal medieresurser som du kan använda i din butik.

![Adobe Stock sökresultat](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

Adobe Stock ger företag tillgång till miljontals utvalda och royaltyfria foton, vektorer, illustrationer, videor, mallar och 3D-resurser av hög kvalitet för alla kreativa projekt. [!DNL Commerce] användare kan snabbt hitta, förhandsgranska och licensiera Adobe Stock-resurser. Användarna kan också spara dem i [medielagringsplatsen](./media-storage.md), utan att lämna arbetsytan Admin.

## Förutsättningar

Den här integreringen kräver:

- Ett [Adobe Developer](https://developer.adobe.com/console/home)-konto
- Adobe Commerce eller Magento Open Source, 2.3.4 eller senare

För licensiering av Adobe Stock-bilder krävs:

- Ett [Adobe-konto](https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html)
- En betald [Adobe Stock](https://stock.adobe.com)-plan som är kopplad till kontot

## Integrera [!DNL Commerce] och Adobe Stock

Att konfigurera Adobe Stock-integrationen för Adobe Commerce är en tvåstegsprocess:

1. [Skapa en adobe.developer-integration](#create-an-adobe-developer-integration) för att generera en API-nyckel
1. [Konfigurera Adobe Stock-integreringen i Commerce Admin](#configure-the-adobe-stock-integration)

### Integrera Adobe Developer

1. Gå till [Adobe Developer Console](https://developer.adobe.com/console/home).

1. Klicka på _[!UICONTROL Quick Start]_&#x200B;under **[!UICONTROL Create new project]**.

1. Klicka på _[!UICONTROL Project overview]_&#x200B;i blocket **[!UICONTROL Add API]**.

1. Välj **[!UICONTROL Adobe Stock]** i integreringslistan och klicka på **[!UICONTROL Next]**.

1. Välj OAuth 2.0 **[!UICONTROL Web App]**.

1. Ange **[!UICONTROL redirect URI]**.

   Standardomdirigerings-URI:n har formatet `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`, till exempel `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`, där:

   - `${HOST}` är ditt [!DNL Commerce] fullständiga kvalificerade domännamn (till exempel `https://store.myshop.com`).
   - `${ADMIN_URI}` är din [!DNL Commerce] Admin URI (till exempel `admin_hgkq1l`), som kan hämtas genom att köra `magento info:adminuri`.

1. Ange **[!UICONTROL Redirect URI pattern]**, som är samma som din omdirigerings-URI med två skillnader:

   - Alla punkter (`.`) måste föregås av två omvända snedstreck (`\\`).
   - Lägg till `.*` i slutet av mönstret.

   Om du använder exemplet från föregående standard-URI för omdirigering blir mönstret `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`

1. Klicka på **[!UICONTROL Next]**.

1. Granska tillgängliga omfattningar och klicka på **[!UICONTROL Save configured API]**.

1. Kopiera **[!UICONTROL Client ID]** (API-nyckel) och **[!UICONTROL Client secret]** på den följande sidan.

   Den här informationen används i steg i nästa avsnitt.

### Konfigurera Adobe Stock-integrering

Om du vill ange systemkonfigurationen i din [!DNL Commerce]-administratör använder du _API-nyckeln_ och _klienthemligheten_ som genererats i [föregående avsnitt](#create-an-adobeio-integration).

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_&#x200B;Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Advanced]** i den vänstra panelen och välj **[!UICONTROL System]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** och gör följande:

   - Ange **[!UICONTROL Enabled Adobe Stock]** till `Yes`.

   - Ange din **[!UICONTROL API Key (Client ID)]**.

   - Ange din **[!UICONTROL Client Secret]**.

   - Klicka på **[!UICONTROL Test Connection]** för att validera dina nycklar.

   ![Avancerad konfiguration - Adobe Stock-integrering](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   Ge valideringen några sekunder. Om dina autentiseringsuppgifter är giltiga bör du se en grön _anslutning klar!_ meddelande.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
