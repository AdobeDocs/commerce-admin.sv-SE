---
title: Infoga en widget i redigeraren
description: Lägg till olika innehållselement på en sida med widgetverktyget i WYSIWYG Editor.
exl-id: bbc5e059-06d8-4dda-89a7-6c9826b73fd3
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# Infoga en widget i redigeraren

Verktyget [widget](widget-create.md) kan användas för att lägga till olika innehållselement på sidan, bland annat länkar till en Commerce-innehållssida eller -nod, produkt eller kategori. Länkarna kan placeras på sidan i ett blockformat, eller infogas direkt i innehållet. Du kan använda widgetverktyget för att skapa länkar till följande typer av innehåll:

- [Innehållssidor](pages.md)
- [Katalogkategorier](../catalog/categories.md)
- [Katalogprodukter](../catalog/product-create.md)

Som standard ärver länkar sin stil från temats formatmall.

{{$include /help/_includes/directives-caution.md}}

1. Öppna en sida, ett block eller ett dynamiskt block i redigeringsläge.

1. Gå till avsnittet _[!UICONTROL Content]_och klicka på ett element som stöder redigeraren.

1. Placera markören där du vill att widgeten ska visas och klicka på ikonen _Infoga widget_ .

   ![Verktygsfältet för redigeraren - Infoga widget](./assets/editor-toolbar-widget-button.png){width="700" zoomable="yes"}

   Om du inte har Page Builder aktiverat och föredrar att arbeta med koden klickar du på **[!UICONTROL Show / Hide Editor]**. Placera insättningspunkten i texten där du vill att widgeten ska visas. Klicka sedan på **[!UICONTROL Insert Widget]**.

1. Välj **[!UICONTROL Widget Type]**.

   Mer information om de här alternativen finns i [Widgettyper](widgets.md#widget-types). I följande steg används ett exempel för att infoga en länk till en produkt.

1. Om du vill använda produktnamnet lämnar du fältet **[!UICONTROL Anchor Custom Text]** tomt.

1. Ange en **[!UICONTROL Anchor Custom Title]** för bästa SEO-praxis.

   Den här titeln visas inte på sidan.

1. Ange **[!UICONTROL Template]** till något av följande:

   - Om du vill infoga länken i texten väljer du `Product Link Inline Template`.

   - Om du vill placera länken på en separat rad väljer du `Product Link Block Template`.

1. Klicka på **[!UICONTROL Select Product]** och gör följande:

   - Gå till önskad kategori i trädet.

   - Välj den länkade produkten i listan.

1. Klicka på **[!UICONTROL Insert Widget]** för att placera länken på sidan.

   Om du arbetar med HTML-kod visas en [markup-tagg](../systems/markup-tags.md) för länken överst på sidan, omsluten av dubbla klammerparenteser. Använd vid behov _Klipp ut och Klistra in_ för att placera taggen i koden där du vill att länken ska visas.

1. När dina innehållsredigeringar är klara klickar du på **[!UICONTROL Save]**.

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
