---
title: Sidlayouter
description: Lär dig mer om sidlayoutsektionerna och hur du konfigurerar standardlayouter.
exl-id: 397a92cf-6f20-4729-8d7c-c5f672fc1c9a
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# Sidlayouter

Layouten för varje sida i din butik består av distinkta avsnitt, eller behållare, som definierar sidhuvud, sidfot och innehållsområden för sidan. Beroende på layouten kan varje sida ha en, två, tre kolumner eller mer. Du kan tänka dig layouten som _planritning_ på sidan och tilldela en särskild layout som ska användas som standard för CMS-, produkt- och kategorisidor.

På sidan är innehållsblocken flytande för att fylla det tillgängliga utrymmet, enligt avsnittet på sidan [sidlayout](layout-updates.md) där de är tilldelade att visas. Observera att om du ändrar layouten från en layout med tre kolumner till en layout med två kolumner, så utökas huvudområdets innehåll så att det tillgängliga utrymmet fylls. Observera också att alla block som är kopplade till den oanvända sidofältet verkar försvinna. Om du återställer layouten med tre kolumner visas dock blocken igen. denna smidiga metod, eller _flytande layout_ gör det möjligt att ändra sidlayouten utan att behöva ändra innehållet. Om du är van vid att arbeta med enskilda HTML-sidor är detta modulära _byggsten_ Strategin kräver ett annat sätt att tänka.

![Standardlayout med två spalter och vänsterstreck](./assets/storefront-2-column-ee.png){width="700" zoomable="yes"}

## Konfigurera standardlayouter

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I den vänstra panelen under _[!UICONTROL General]_, välja **[!UICONTROL Web]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Default Layouts]** -avsnitt.

   ![Standardlayouter](./assets/web-default-layouts.png){width="600" zoomable="yes"}

1. Välj **[!UICONTROL Default Product Layout]** som du vill använda för produktsidor.

   Den här inställningen avgör vilken layout som används som standard för produktsidor.

   - `No layout updates` - Det finns inga layoutuppdateringar för produktsidor.
   - `Empty` - Använder en tom layout för produktsidor.
   - `1 column` - Använder en enda kolumnlayout för produktsidor.
   - `2 columns with left bar` - Använder en layout med två kolumner och sidofältet till vänster för produktsidor.
   - `2 columns with right bar` - Använder en layout med två kolumner och sidofältet till höger för produktsidor.
   - `3 columns` - Använder en layout med tre kolumner och sidofält till vänster och höger för produktsidor.

   När [Page Builder](../page-builder/introduction.md) är aktiverat finns det ytterligare alternativ för full bredd. Du kan sedan använda Page Builder-innehållsverktygen för att utforma layouten för dina produktsidor.

   - `Page -- Full Width` - Använder _Sida - full bredd_  layout för produktsidor.
   - `Category -- Full Width` - Använder _Kategori - full bredd_ layout för produktsidor.
   - `Product -- Full Width` - (Rekommenderas) Använder _Produkt - full bredd_ layout för produktsidor.

1. Välj **[!UICONTROL Default Category Layout]** som du vill använda för kategorisidor.

   Den här inställningen avgör vilken layout som används som standard för kategorisidor.

   - `No layout updates` - Det finns inga layoutuppdateringar för kategorisidor.
   - `Empty` - Använder en tom layout för kategorisidor.
   - `1 column` - Använder en enda kolumnlayout för kategorisidor.
   - `2 columns with left bar` - Använder en layout med två kolumner och sidofältet till vänster för kategorisidor.
   - `2 columns with right bar` - Använder en layout med två kolumner och sidofältet till höger för kategorisidor.
   - `3 columns` - Använder en layout med tre kolumner och sidofält till vänster och höger för kategorisidor.

   När [Page Builder](../page-builder/introduction.md) är aktiverat finns det ytterligare alternativ för full bredd. Du kan sedan använda Page Builder-innehållsverktygen för att utforma layouten för dina kategorisidor.

   - `Page -- Full Width` - Använder _Sida - full bredd_ layout för kategorisidor.
   - `Category -- Full Width` - (Rekommenderas) Använder _Kategori - full bredd_ layout för kategorisidor.
   - `Product -- Full Width` - Använder _Produkt - full bredd_ layout för kategorisidor.

1. Välj **[!UICONTROL Default Page Layout]** som du vill använda för CMS-sidor.

   Den här inställningen avgör vilken layout som används som standard för CMS-sidor.

   - `No layout updates` - Det finns inga layoutuppdateringar tillgängliga för CMS-sidor.
   - `Empty` - Använder en tom layout för CMS-sidor.
   - `1 column` - Använder en enda kolumnlayout för CMS-sidor.
   - `2 columns with left bar` - Använder en layout med två kolumner och sidofältet till vänster för CMS-sidor.
   - `2 columns with right bar` - Använder en layout med två kolumner och sidofältet till höger för CMS-sidor.
   - `3 columns` - Använder en layout med tre kolumner och sidofält till vänster och höger för CMS-sidor.

   När [Page Builder](../page-builder/introduction.md) är aktiverat finns det ytterligare alternativ för full bredd. Du kan sedan använda Page Builder-innehållsverktygen för att utforma layouten för dina CMS-sidor.

   - `Page -- Full Width` - (Rekommenderas) Använder _Sida - full bredd_ layout för CMS-sidor.
   - `Category - Full Width` - Använder _Kategori - full bredd_ layout för CMS-sidor.
   - `Product - Full Width` - Använder _Produkt - full bredd_ layout för CMS-sidor.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Standardsidlayout

### En kolumn

![Diagram - layout med en kolumn](./assets/layout-1-col-th.png){zoomable=&quot;yes&quot;}

The _[!UICONTROL 1 Column]_kan användas för att skapa en dramatisk startsida med stor bild eller fokalpunkt. Det är också ett bra val för en landningssida eller en annan sida som har en kombination av text, bilder och video.

### Två kolumner med vänster fält

![Diagram - layout med två kolumner och vänster streck](./assets/layout-2-col-lft-bar-th.png){zoomable=&quot;yes&quot;}

The _[!UICONTROL 2 Columns with Left Bar]_layout används ofta för sidor med navigering till vänster, till exempel en katalog eller sökresultatsidor med navigering i lager. Det är också ett utmärkt val för hemsidor som behöver ytterligare navigering eller block med stöd för innehåll till vänster.

### Två kolumner med höger fält

![Diagram - layout med två kolumner och höger stapel](./assets/layout-2-col-rt-bar-th.png){zoomable=&quot;yes&quot;}

Med _[!UICONTROL 2 Columns with Right Bar]_layout, är huvudinnehållsområdet stort nog för en iögonfallande bild eller banderoll. Den här layouten används ofta för produktsidor med block med stödinnehåll till höger.

### Tre kolumner

![Diagram - layout med tre kolumner](./assets/layout-3-col-th.png){zoomable=&quot;yes&quot;}

The _[!UICONTROL 3 Column]_layout har en mittkolumn som är tillräckligt bred för sidans huvudtext, med utrymme på varje sida för ytterligare navigering och block med stödinnehåll.

### Tom

![Diagram - tom layout](./assets/layout-blank-th.png){zoomable=&quot;yes&quot;}

The _[!UICONTROL Empty]_layout kan användas för att definiera anpassade sidlayouter.
