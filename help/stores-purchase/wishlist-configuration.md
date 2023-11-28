---
title: Konfigurera önskelistor
description: Lär dig hur du konfigurerar önskelistefunktioner för dina butikskunder.
exl-id: 479455f1-282f-4277-b132-45c5867fb21c
feature: Customers, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# Konfigurera önskelistor

Konfiguration av önskelista aktiverar önskelistor och fastställer e-postmallen och avsändaren av e-postmeddelanden som används när en önskelista delas.

## Aktivera önskelistefunktioner

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Customers]** och välja **[!UICONTROL Wish List]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL General Options]** och gör följande:

   ![Kundkonfiguration - allmänna inställningar för önskelista](../configuration-reference/customers/assets/wishlist-general-options.png){width="600" zoomable="yes"}

   - Växla **[!UICONTROL Enabled]** till `Yes`, som aktiverar önskelistemodulen för butiken.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Växla **[!UICONTROL Enable Multiple Wish Lists]** till `Yes`, som gör det möjligt för kunderna att skapa och underhålla flera önskelistor.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Ange ett värde för **[!UICONTROL Number of Multiple Wish Lists]**.

   - Växla **[!UICONTROL Show in Sidebar]** till `Yes`, som visar önskelistorna i sidofältet.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Share Options]** och gör följande:

   ![Kundkonfiguration - alternativ för önskelista](../configuration-reference/customers/assets/wishlist-share-options.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL Email Sender]** till butikskontakten som ska visas som avsändare av meddelandet. Alternativ: Allmän kontakt, Säljare, Kundsupport, Anpassad e-post.

   - Ange **[!UICONTROL Email Template]** som ska användas när en kund delar en önskelista.

   - Om du vill begränsa det totala antalet e-postmeddelanden som en kund kan skicka anger du en **[!UICONTROL Max Emails Allowed to be Sent]** värde. Standardvärdet är 10 och maxvärdet är 10 000.

   - Om du vill begränsa meddelandets storlek anger du ett värde för **[!UICONTROL Email Text Length Limit]**. Standardvärdet är 255.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL My Wish List Link]** avsnitt och ange **[!UICONTROL Display Wish List Summary]** till något av följande:

   - `Display number of items in wish list`
   - `Display item quantities`

   ![Kundkonfiguration - önskelista](../configuration-reference/customers/assets/wishlist-my-wishlist-link.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Lägg till sökning i önskelista

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)

Alla offentliga önskelistor kan hittas med hjälp av sökningen i önskelistan [widget](../content-design/widgets.md). Med widgeten kan kunden söka efter önskelistans namn eller e-postadress. Butikskunder kan hitta önskelistor som tillhör andra kunder, visa dem och beställa produkter från dem eller lägga till produkterna i sina egna önskelistor. Om en artikel köpts från en allmän önskelista av en annan kund tas den inte bort från den ursprungliga önskelistan. The _Önsklistesökning_ widgeten kan läggas till på vilken sida som helst i din butik så att kunderna enkelt kan hitta önskelistor för vänner och familjemedlemmar.

![Exempelarkiv - sökning i önskelista](./assets/storefront-wishlist-search.png){width="700" zoomable="yes"}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicka på i det övre högra hörnet **[!UICONTROL Add Widget]**.

1. I _[!UICONTROL Settings]_gör du så här:

   - Ange **[!UICONTROL Type]** till `Wish List Search`.

   - Ange **[!UICONTROL Design Theme]** till temat för butiken där önskelistan läggs till.

   - Klicka på **[!UICONTROL Continue]**.

1. Slutför _[!UICONTROL Storefront Properties]_:

   - Ange **[!UICONTROL Widget Title]**.

   - Ange **[!UICONTROL Assign to Store Views]** till den vy eller webbplats där widgeten ska användas.

   - För **[!UICONTROL Sort Order]** anger du ett nummer som bestämmer placeringen av widgeten i dess behållare.

     `0` = först (standard), `1` = sekund, `2` = tredje och så vidare.

1. I _[!UICONTROL Layout Updates]_avsnitt, klicka **[!UICONTROL Add Layout Update]**och ange **[!UICONTROL Display on]**till något av följande:

   - _[!UICONTROL Categories]_

      - `Anchor Categories`
      - `Non-Anchor Categories`

   - _[!UICONTROL Products]_

      - `All Product Type`
      - `Simple Product`
      - `Virtual Product`
      - `Bundle Product`
      - `Configurable Product`
      - `Downloadable Product`
      - `Gift Card`
      - `Grouped Product`

   - _[!UICONTROL Generic Page]_

      - `All Pages`
      - `Specified Page`
      - `Page Layouts`

1. I **[!UICONTROL Container]** väljer du det område i sidlayouten där den ska placeras.

   ![Sökwidget för önskelista - layout](./assets/widget-wishlist-search-storefront.png){width="700" zoomable="yes"}

1. Välj **[!UICONTROL Widget Options]**.

1. Ange **[!UICONTROL Quick Search Form Types]** till något av följande:

   - `All Forms` - Kunderna kan söka efter alla tillgängliga parametrar.
   - `Owner Name` - Kunder kan söka efter önskelistor efter ägarnamn.
   - `Owner Email` - Kunder kan söka efter önskelistor efter ägarens e-postadress.

   >[!NOTE]
   >
   >Leveransadresser ingår inte i önskelistor.

1. Konfigurera återstående widgegenskaper efter behov, enligt standarden [instruktioner](../content-design/widget-create.md).

1. När du är klar klickar du på **[!UICONTROL Save]**.

1. Uppdatera alla ogiltiga cacheminnen när du uppmanas till detta.
