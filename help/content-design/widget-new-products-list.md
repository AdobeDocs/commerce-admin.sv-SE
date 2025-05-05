---
title: Ny widget för produktlista
description: Lär dig hur du använder den nya produktlistwidgeten för att visa en lista över de senast tillagda produkterna.
exl-id: bdff3655-cd14-4a19-a51f-4cabeb274d2a
feature: Page Content, Products
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 0%

---

# Ny widget för produktlista

Listan med nya produkter är ett exempel på dynamiskt innehåll och består av livedata som hämtas från produktkatalogen. Som standard innehåller listan _Nya produkter_ de första åtta av de senast tillagda produkterna. Den kan dock även konfigureras så att den endast innehåller produkter inom ett angivet datumintervall.

![Ny produktlista på butikens startsida](./assets/storefront-home-page-new-products.png){width="700" zoomable="yes"}

## Steg 1: Ange varje produkt som ny

![Magento Open Source](../assets/open-source.svg) Det här steget gäller endast Magento Open Source.

![Adobe Commerce](../assets/adobe-logo.svg) För Adobe Commerce-butiker, se [Schemalägga en uppdatering](content-staging-scheduled-update.md) och fortsätt sedan till steg 2 på den här sidan.

Datumintervallinställningen _[!UICONTROL Set Product as New]_&#x200B;kan bara konfigureras i schemalagda uppdateringar.

Om du anger en produkt som ny läggs produkten till i listan _Nya produkter_. Du kan när som helst ändra inställningen igen när du inte längre vill ta med den i listan.

1. Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]** på sidofältet _Admin_.

1. Hitta de produkter du vill ha och öppna i redigeringsläge.

1. För **[!UICONTROL Set Product as New]** växlar du alternativet att ange produkten som en ny produkt eller inte.

   ![Anger produkten som ny](./assets/product-set-as-new.png){width="400" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]** när du är klar.

1. När du uppmanas att indexera om och uppdatera sidcachen klickar du på länkarna högst upp på sidan och följer instruktionerna.

## Steg 2: Skapa widgeten

Koden som avgör innehållet i listan Nya produkter och dess placering i din butik genereras av widgetverktyget.

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add Widget]** i det övre högra hörnet.

1. Gör följande i avsnittet _[!UICONTROL Settings]_:

   - Ange **[!UICONTROL Type]** till `Catalog New Products List`.

   - Välj den **[!UICONTROL Design Theme]** som används av butiken.

1. Klicka på **[!UICONTROL Continue]**.

   ![Nya inställningar för widgeten Produktlista](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Gör följande i avsnittet _[!UICONTROL Storefront Properties]_:

   - För **[!UICONTROL Widget Title]** anger du en beskrivande titel för widgeten. (Den här titeln visas bara från _administratören_.)

   - För **[!UICONTROL Assign to Store Views]** väljer du de butiksvyer där widgeten visas.

     Du kan välja en viss butiksvy eller `All Store Views`. Om du vill markera flera vyer håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

   - (Valfritt) Ange ett nummer för **[!UICONTROL Sort Order]** för att avgöra i vilken ordning det här objektet visas med andra på samma del av sidan. (`0` = först, `1` = sekund, `3` = tredje o.s.v.)

   ![Layoutuppdateringar](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

## Steg 3: Välj plats

1. Klicka på **[!UICONTROL Add Layout Update]** i avsnittet _[!UICONTROL Layout Updates]_.

1. Ange **[!UICONTROL Display On]** till `Specified Page.`

1. Ange **[!UICONTROL Page]** till `CMS Home Page`.

1. Ange **[!UICONTROL Block Reference]** till `Main Content Area`.

1. Ange **[!UICONTROL Template]** till något av följande:

   - `New Product List Template`
   - `New Products Grid Template`

     ![Layoutuppdateringar](./assets/widget-layout-update-new-products-list.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save and Continue Edit]**.

   För tillfället kan du ignorera meddelandet för att uppdatera cachen.

## Steg 4: Konfigurera listan

1. Välj **[!UICONTROL Widget Options]** på den vänstra panelen.

1. Ange **[!UICONTROL Display Products]** till något av följande:

   - `All Products` - Visar produkter i sekvens och börjar med den senast tillagda produkten.
   - `New Products` - Visar endast de produkter som identifieras som _new_. En produkt anses vara ny under det datumintervall som anges i _[!UICONTROL Set Product As New From/To]_. Listan är tom om datumintervallet förfaller utan att några nya produkter har definierats.

1. Om du vill ha navigeringskontroll för listor med flera sidor anger du **[!UICONTROL Display Page Control]** till `Yes`.

   För **[!UICONTROL Number of Products per Page]** anger du antalet produkter som du vill ska visas på varje sida.

1. Ange alternativet **[!UICONTROL Number of Products to Display]** till antalet nya produkter som du vill ta med i listan.

   Standardinställningen är `10`.

1. För **[!UICONTROL Cache Lifetime (Seconds)]** väljer du hur ofta du vill uppdatera listan över nya produkter.

   Som standard är cachen inställd på 86 400 sekunder (24 timmar).

   ![Widget-alternativ](./assets/widget-options-new-product-list.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]** när du är klar.

1. När du uppmanas att uppdatera cacheminnet klickar du på länken i meddelandet längst upp på sidan och följer instruktionerna.

## Steg 5: Förhandsgranska ditt arbete

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**&#x200B;på sidofältet_ Admin _.

1. Hitta sidan i rutnätet där listan _Nya produkter_ ska visas och klicka på länken **[!UICONTROL Preview]** i kolumnen _[!UICONTROL Action]_.
