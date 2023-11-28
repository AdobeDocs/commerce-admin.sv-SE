---
title: Adobe Stock Integration
description: Integrera Adobe Stock med [!DNL Commerce] -instans för att få tillgång till ett oändligt antal mediefiler som kan användas i din butik.
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Adobe Stock Integration

För att få tillgång till ett oändligt antal mediefiler som kan användas i din butik måste du integrera [Adobe Stock][adobe-stock] med [!UICONTROL Commerce].

![Adobe Stock sökresultat](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

Adobe Stock ger företag tillgång till miljontals utvalda och royaltyfria foton, vektorer, illustrationer, videor, mallar och 3D-resurser av hög kvalitet för alla kreativa projekt. [!DNL Commerce] -användare snabbt kan hitta, förhandsgranska och licensiera Adobe Stock-mediefiler. Användarna kan också spara dem i [medielagring][media-storage], utan att lämna arbetsytan Admin.

## Förutsättningar

Den här integreringen kräver:

- An [Adobe Developer][dev-console] konto
- Adobe Commerce eller Magento Open Source, 2.3.4 eller senare

För licensiering av Adobe Stock-bilder krävs:

- An [Adobe][adobe-signin]
- En betald [Adobe Stock][adobe-stock] plan som är associerad med kontot

## Integrera [!DNL Commerce] och Adobe Stock

Att konfigurera Adobe Stock-integrationen för Adobe Commerce är en tvåstegsprocess:

1. [Skapa integration med adobe.developer](#create-an-adobe-developer-integration) för att generera en API-nyckel
1. [Konfigurera Adobe Stock-integreringen i Commerce Admin](#configure-the-adobe-stock-integration)

### Integrera Adobe Developer

1. Navigera till [Adobe Developer Console][dev-console].

1. Under _[!UICONTROL Quick Start]_, klicka **[!UICONTROL Create new project]**.

1. I _[!UICONTROL Project overview]_block, klicka **[!UICONTROL Add API]**.

1. Välj **[!UICONTROL Adobe Stock]** från listan och klicka på **[!UICONTROL Next]**.

1. Välj OAuth 2.0 **[!UICONTROL Web App]**.

1. Ange **[!UICONTROL redirect URI]**.

   Standardomdirigerings-URI:n finns i formuläret `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`, till exempel `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`, där:

   - `${HOST}` är din [!DNL Commerce] fullständigt kvalificerat domännamn (till exempel `https://store.myshop.com`).
   - `${ADMIN_URI}` är din [!DNL Commerce] Admin-URI (till exempel `admin_hgkq1l`), som kan hämtas genom att köra `magento info:adminuri`.

1. Ange **[!UICONTROL Redirect URI pattern]**, vilket är samma som din omdirigerings-URI med två skillnader:

   - Alla punkter (`.`) måste föregås av två omvända snedstreck (`\\`).
   - Lägg till `.*` till slutet av mönstret.

   Med hjälp av exemplet från den tidigare omdirigerings-URI:n blir det `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`.

1. Klicka på **[!UICONTROL Next]**.

1. Granska tillgängliga omfattningar och klicka på **[!UICONTROL Save configured API]**.

1. Kopiera **[!UICONTROL Client ID]** (API-nyckel) och **[!UICONTROL Client secret]**.

   Den här informationen används i steg i nästa avsnitt.

### Konfigurera Adobe Stock-integrering

Så här anger du systemkonfigurationen i din [!DNL Commerce] Admin, använd _API-nyckel_ och _Klienthemlighet_ genereras i [föregående avsnitt][create-integration].

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL System]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** och gör följande:

   - Ange **[!UICONTROL Enabled Adobe Stock]** till `Yes`.

   - Ange **[!UICONTROL API Key (Client ID)]**.

   - Ange **[!UICONTROL Client Secret]**.

   - Klicka **[!UICONTROL Test Connection]** för att validera dina nycklar.

   ![Avancerad konfiguration - integrering med Adobe Stock](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   Ge valideringen några sekunder. Om inloggningsuppgifterna är giltiga bör du se en grön _Anslutningen lyckades!_ meddelande.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
[media-storage]: media-storage.md
[dev-console]: https://developer.adobe.com/console/home
[create-integration]: #create-an-adobeio-integration
