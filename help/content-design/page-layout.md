---
title: Sidlayouter
description: Lär dig mer om sidlayoutsektionerna och hur du konfigurerar standardlayouter.
exl-id: 397a92cf-6f20-4729-8d7c-c5f672fc1c9a
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 0%

---

# Sidlayouter

Layouten för varje sida i din butik består av distinkta avsnitt, eller behållare, som definierar sidhuvud, sidfot och innehållsområden för sidan. Beroende på layouten kan varje sida ha en, två, tre kolumner eller mer. Du kan tänka dig layouten som sidans _golvplan_ och tilldela en viss layout som ska användas som standard för CMS-, produkt- och kategorisidor.

På sidan flyter innehållsblocken så att det tillgängliga utrymmet fylls, enligt det avsnitt i [sidlayouten](layout-updates.md) där de har tilldelats. Observera att om du ändrar layouten från en layout med tre kolumner till en layout med två kolumner, så utökas huvudområdets innehåll så att det tillgängliga utrymmet fylls. Observera också att alla block som är kopplade till den oanvända sidofältet verkar försvinna. Om du återställer layouten med tre kolumner visas dock blocken igen. Den här flytande metoden, eller _flytande layout_, gör det möjligt att ändra sidlayouten utan att behöva omarbeta innehållet. Om du är van vid att arbeta med enskilda HTML-sidor kräver den här modulära metoden _byggblock_ ett annat sätt att tänka.

![Två kolumner med sidlayout för vänster stapel som standard](./assets/storefront-2-column-ee.png){width="700" zoomable="yes"}

## Konfigurera standardlayouter

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Välj **[!UICONTROL Web]** i den vänstra panelen under _[!UICONTROL General]_.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Default Layouts]**.

   ![Standardlayouter](./assets/web-default-layouts.png){width="600" zoomable="yes"}

1. Välj den **[!UICONTROL Default Product Layout]** som du vill använda för produktsidor.

   Den här inställningen avgör vilken layout som används som standard för produktsidor.

   - `No layout updates` - Det finns inga layoutuppdateringar tillgängliga för produktsidor.
   - `Empty` - En tom layout används för produktsidor.
   - `1 column` - Använder en enda kolumnlayout för produktsidor.
   - `2 columns with left bar` - Använder en layout med två kolumner och sidofältet till vänster för produktsidor.
   - `2 columns with right bar` - Använder en layout med två kolumner och sidofältet till höger för produktsidor.
   - `3 columns` - Använder en layout med tre kolumner och sidofält till vänster och höger för produktsidor.

   När [Page Builder](../page-builder/introduction.md) är aktiverat finns det ytterligare alternativ för full bredd. Du kan sedan använda Page Builder-innehållsverktygen för att utforma layouten för dina produktsidor.

   - `Page -- Full Width` - Använder layouten _Sida - full bredd_ för produktsidor.
   - `Category -- Full Width` - Använder layouten _Kategori - full bredd_ för produktsidor.
   - `Product -- Full Width` - (rekommenderas) Använder layouten _Produkt - full bredd_ för produktsidor.

1. Välj den **[!UICONTROL Default Category Layout]** som du vill använda för kategorisidor.

   Den här inställningen avgör vilken layout som används som standard för kategorisidor.

   - `No layout updates` - Layoutuppdateringar är inte tillgängliga för kategorisidor.
   - `Empty` - En tom layout används för kategorisidor.
   - `1 column` - Använder en enda kolumnlayout för kategorisidor.
   - `2 columns with left bar` - Använder en layout med två kolumner och sidofältet till vänster för kategorisidor.
   - `2 columns with right bar` - Använder en layout med två kolumner och sidofältet till höger för kategorisidor.
   - `3 columns` - Använder en layout med tre kolumner och sidofält till vänster och höger för kategorisidor.

   När [Page Builder](../page-builder/introduction.md) är aktiverat finns det ytterligare alternativ för full bredd. Du kan sedan använda Page Builder-innehållsverktygen för att utforma layouten för dina kategorisidor.

   - `Page -- Full Width` - Använder layouten _Sida - full bredd_ för kategorisidor.
   - `Category -- Full Width` - (rekommenderas) Använder layouten _Kategori - full bredd_ för kategorisidor.
   - `Product -- Full Width` - Använder layouten _Produkt - full bredd_ för kategorisidor.

1. Välj den **[!UICONTROL Default Page Layout]** som du vill använda för CMS-sidor.

   Den här inställningen avgör vilken layout som används som standard för CMS-sidor.

   - `No layout updates` - Det finns inga layoutuppdateringar för CMS-sidor.
   - `Empty` - Använder en tom layout för CMS-sidor.
   - `1 column` - Använder en enda kolumnlayout för CMS-sidor.
   - `2 columns with left bar` - Använder en layout med två kolumner och sidofältet till vänster för CMS-sidor.
   - `2 columns with right bar` - Använder en layout med två kolumner och sidofältet till höger för CMS-sidor.
   - `3 columns` - Använder en layout med tre kolumner och sidofält till vänster och höger för CMS-sidor.

   När [Page Builder](../page-builder/introduction.md) är aktiverat finns det ytterligare alternativ för full bredd. Du kan sedan använda Page Builder-innehållsverktygen för att utforma layouten för dina CMS-sidor.

   - `Page -- Full Width` - (rekommenderas) Använder layouten _Sida - full bredd_ för CMS-sidor.
   - `Category - Full Width` - Använder layouten _Kategori - full bredd_ för CMS-sidor.
   - `Product - Full Width` - Använder layouten _Produkt - full bredd_ för CMS-sidor.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Standardsidlayout

### En kolumn

![Diagram - layout med en kolumn](./assets/layout-1-col-th.png){zoomable="yes"}

Layouten _[!UICONTROL 1 Column]_kan användas för att skapa en dramatisk startsida med en stor bild eller fokalpunkt. Det är också ett bra val för en landningssida eller en annan sida som har en kombination av text, bilder och video.

### Två kolumner med vänster fält

![Diagram - layout med två kolumner och vänster fält](./assets/layout-2-col-lft-bar-th.png){zoomable="yes"}

Layouten _[!UICONTROL 2 Columns with Left Bar]_används ofta för sidor med navigering till vänster, till exempel en katalog eller sökresultatsidor med navigering i flera lager. Det är också ett utmärkt val för hemsidor som behöver ytterligare navigering eller block med stöd för innehåll till vänster.

### Två kolumner med höger fält

![Diagram - layout med två kolumner och höger fält](./assets/layout-2-col-rt-bar-th.png){zoomable="yes"}

Med layouten _[!UICONTROL 2 Columns with Right Bar]_är huvudinnehållsområdet tillräckligt stort för en iögonfallande bild eller banderoll. Den här layouten används ofta för produktsidor med block med stödinnehåll till höger.

### Tre kolumner

![Diagram - layout med tre kolumner](./assets/layout-3-col-th.png){zoomable="yes"}

Layouten _[!UICONTROL 3 Column]_har en mittkolumn som är tillräckligt bred för sidans huvudtext, med utrymme på varje sida för ytterligare navigering och block med stöd för innehåll.

### Tom

![Diagram - tom layout](./assets/layout-blank-th.png){zoomable="yes"}

Layouten _[!UICONTROL Empty]_kan användas för att definiera anpassade sidlayouter.
