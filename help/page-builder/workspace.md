---
title: '''[!DNL Page Builder] Arbetsyta'
description: Läs mer om verktygen i [!DNL Page Builder] när du skapar bassidor, produkt- och katalogsidor, block och dynamiska block.
exl-id: 1cd7b300-0a18-490f-bc11-36de3fec13dc
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '1413'
ht-degree: 0%

---

# [!DNL Page Builder] Arbetsyta

När [[!DNL Page Builder] är aktiverat](setup.md), _[!UICONTROL Content]_att skapa och redigera innehåll för att dra nytta av den avancerade [!DNL Page Builder] verktyg för CMS [sidor](../content-design/page-add.md), [produkt](../catalog/product-content.md) och [kategori](../catalog/categories-content-settings.md) sidor, [block](../content-design/block-add.md)och [dynamiska block](../content-design/dynamic-blocks.md). Det här avsnittet innehåller en_ Innehållsrubrik _fält, en förhandsgranskning av innehållet och enkel åtkomst till helskärmsläget [!DNL Page Builder] arbetsyta.

![Innehållsavsnitt med [!DNL Page Builder] förhandsgranska](./assets/pb-content-preview.png){width="700" zoomable="yes"}

## Innehållsrubrik

Eftersom sökmotorer söker efter rubriker på nivå ett (H1) är det enkelt att lägga till en rubrik på nivå ett för att säkerställa att sidan indexeras korrekt.

>[!NOTE]
>
>The _[!UICONTROL Content Heading]_fältet som visas högst upp på sidan är ett äldre fält som stöder innehåll som skapades med tidigare [!DNL Commerce] releaser. Det är dock inte en del av [!DNL Page Builder]. The [!UICONTROL Content Heading] formateras som en H1-rubrik enligt den formatmall som är kopplad till det aktuella temat. Den placeras precis ovanför det aktiva innehållsområdet som definieras av [!DNL Page Builder] stage.

Du bör lämna alternativet _[!UICONTROL Content Heading]_fältet är tomt och använder [!DNL Page Builder] [Rubrik](heading.md) innehållstyp.

![Content Heading and other heading](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

## Förhandsgranska

När du expanderar _[!UICONTROL Content]_och det finns befintligt innehåll som skapats med [!DNL Page Builder]visas en förhandsgranskning av innehållet så som det skulle visas på en sida. Klicka **[!UICONTROL Edit with Page Builder]**eller inuti förhandsvisningsområdet för innehållet för att öppna [!DNL Page Builder] arbetsyta där du kan göra nödvändiga uppdateringar.

![Förhandsgranskning av produktbeskrivning](./assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

>[!NOTE]
>
>För produkt- och kategoriformulären är den här förhandsvisningen aktiverad som standard, men kan inaktiveras. Om prestandan försämras på grund av inläsning av förhandsvisningen kan du inaktivera förhandsvisningen i [Konfiguration för innehållshantering](../configuration-reference/general/content-management.md#advanced-content-tools) inställningar.

## Scen

När du öppnar [!DNL Page Builder] arbetsytan i förhandsgranskningen är den primära arbetsytan där du kan skapa och formatera innehåll, och till och med göra snabba redigeringar av direktinnehåll. Inledningsvis är scenen tom, vilket ger den designyta där du kan dra rader, kolumner och tabbar från den vänstra panelen.

>[!NOTE]
>
>Från och med version 2.4.1 är redigering av innehåll nu helskärmsläge endast för alla områden som styrs av [!DNL Page Builder]- CMS-sidor, produkt- och kategorisidor, block och dynamiska block. Vid helskärmsredigering fokuseras ditt innehåll och ger en vy som bättre matchar användarupplevelsen i butiken.

![Scen med sidinnehåll](./assets/pb-workspace-simple-page.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Vieports

A _visningsruta_ är det synliga området på en webbsida som en användare ser. I helskärmsläge visas visningsruteknapparna ovanför [!DNL Page Builder] -scenen för att visa innehållet när webbplatsanvändaren ser det i butiken.

![Knappar för visningsruta](./assets/pb-workspace-viewport-buttons.png){width="500" zoomable="yes"}

[!DNL Page Builder] definierar också brytpunkter för visningsrutor. Brytpunkter definierar den minsta och största bredden som vissa format används i. The [!DNL Page Builder] visningsrutor har följande innehållsbrytpunkter:

- **Skrivbordsbrytpunkt**—`min-width: 1024px`. Den här brytpunkten tillämpar format som har definierats för visningsrutebredder som mäter 1 024 pixlar och bredare.
- **Mobila brytpunkter**—`max-width: 768px, min-width: 640px`. Dessa brytpunkter tillämpar format som är definierade för visningsrutans bredd mellan 768 pixlar och 640 pixlar.

[!DNL Page Builder] visningsrutor har två funktioner: **_förhandsgranskning av innehåll_** och **_brytpunktsinställningar_**.

### Förhandsgranskning av innehåll

Som standard [!DNL Page Builder] har två förhandsgranskningar av visningsrutan:

- **Skrivbord** — Visar förhandsgranskning av innehåll utan fördefinierad bredd. Skrivbordsdefinierade format (med en minsta brytpunktsbredd på 1 024 pixlar) används fortfarande på sidan. Bredden på skrivbordsvyn definieras av inställningarna för behållarinnehållstyper, som rader. När du väljer skrivbordsvyn visas hur innehållet är formaterat på butiken när webbläsarens sidbredd är 1 024 pixlar och bredare.

  ![Förhandsgranskning av skrivbordsvy med en minsta bredd på 1 024 pixlar](./assets/pb-workspace-viewport-desktop.png){width="500" zoomable="yes"}

- **Mobil** — Visar förhandsgranskningen av innehållet med en fördefinierad bredd på 768 pixlar. Till skillnad från skrivbordsvyn visar visningsrutan Mobilt sidinnehåll vid en bredd på 768 pixlar, tillsammans med de format som är definierade för brytpunktsbredderna 768 pixlar (maximalt) och 640 pixlar (minst).

  ![Förhandsgranskning av mobilvisningsruta med en minsta bredd på 768 pixlar](./assets/pb-workspace-viewport-mobile.png){width="500" zoomable="yes"}

### Brytpunktsinställningar

Visningsknapparna har också möjlighet att tillämpa olika brytpunktsformat på innehållstyper baserat på den valda visningsrutan. Som standard [!DNL Page Builder] innehåller brytpunktsinställningar för _[!UICONTROL Minimum Height]_fält med rader, kolumner, flikar, flikar, banderoller, reglage och bilder. När du väljer visningsrutan för mobila enheter och sedan öppnar du redigeraren för någon av dessa innehållstyper kan du ange fältvärden som är specifika för brytpunkterna för visningsrutan för mobila enheter. I innehållstypfält som tillåter särskilda brytpunktsinställningar visas en ikon till höger om fältet, som i följande exempel för en rad:

![Ikonindikator för brytpunktsinställning](./assets/pb-workspace-viewport-field-breakpoint.png){width="400"}

## Panel

The [!DNL Page Builder] Panelen finns till vänster om scenen och innehåller innehållstyper som kan dras till scenen. En behållare som är specifik för innehållstypen visas sedan med en verktygslåda med alternativ. Innehållstyperna är ordnade på panelen enligt följande:

### Layout

The _[!UICONTROL Layout]_i [!DNL Page Builder] används för att lägga till rader, kolumner eller tabbar på scenen. När du drar en innehållstyp från panelen till scenen visas en behållare med en verktygslåda med alternativ som är specifika för innehållstypen.

Som standard är [!DNL Page Builder] scenen är tom. När du drar layoutinnehållstyper från panelen till scenen kan du placera dem ovanför, under eller inuti andra layoutbehållare på sidan. Rader kan bara läggas till direkt på scenen.

![[!DNL Page Builder] panel med layoutinnehållstyper och scen](./assets/pb-stage-toolbox.png){width="600" zoomable="yes"}

| Innehållstyp för layout | Beskrivning |
| ------------------- |------------ |
| [Rad](row.md) | En ny rad kan bara dras från panelen till scenen och placeras antingen ovanför eller under en annan rad, flik eller kolumngrupp. Du kan också använda alternativet Duplicera för att skapa en kopia av en befintlig rad. |
| [Kolumn](column.md) | En kolumn kan dras från panelen till scenen eller till rader och flikar. Det maximala antalet kolumner som kan läggas till bestäms av antalet rutnätsindelningar som anges i [konfiguration](setup.md). |
| [Tabbar](tabs.md) | En enskild tabb kan dras från panelen till scenen eller till rader och kolumner. Du kan lägga till fler flikar från verktygslådan. |

{style="table-layout:auto"}

### Element

Använd _[!UICONTROL Elements]_i [!DNL Page Builder] för att lägga till text, rubriker, knappar, avgränsare och HTML-kod i en layoutbehållare på [[!DNL Page Builder] stage](workspace.md#stage). När du drar en innehållstyp från panelen till en rad eller kolumn, eller till en tabbuppsättning på scenen, visas en behållare. Använd verktygslådan för innehållstyp för att komma åt inställningar som är specifika för typen.

![[!DNL Page Builder] panel med elementinnehållstyper](./assets/pb-elements.png){width="600" zoomable="yes"}

| Elementinnehållstyp | Beskrivning |
| -------------------- | ----------- |
| [Text](text.md) | Lägger till en textbehållare och redigerare på scenen. |
| [Rubrik](heading.md) | Lägger till en rubrikbehållare på scenen. |
| [Knappar](buttons.md) | Lägger till en behållare för antingen en enskild knapp eller en uppsättning knappar på scenen. |
| [Delare](divider.md) | Lägger till en behållare för en avgränsare på scenen. |
| [HTML Code](html-code.md) | Lägger till en behållare för HTML-kod på scenen. |

{style="table-layout:auto"}

### Media

Använd _[!UICONTROL Media]_i [!DNL Page Builder] för att lägga till bilder, video, banners, reglage och [!DNL Google Maps] till valfri layoutbehållare på [[!DNL Page Builder] stage](workspace.md#stage). När en mediainnehållstyp dras från panelen till scenen, visas en behållare med en verktygslåda med alternativ som är specifika för innehållstypen.

![[!DNL Page Builder] panel med mediainnehållstyper](./assets/pb-media-content-types.png){width="600" zoomable="yes"}

| Medieinnehållstyp | Beskrivning |
| ------------------- | ------------------------------------------ |
| [Bild](image.md) | Lägger till en bildbehållare på scenen. |
| [Video](video.md) | Lägger till en videobehållare på scenen. |
| [Banderoll](banner.md) | Lägger till en banderollbehållare på scenen. |
| [Skjutreglage](slider.md) | Lägger till en skjutreglagebehållare på scenen. |
| [Karta](map.md) | Lägger till en [!DNL Google Maps] behållare till scenen. |

{style="table-layout:auto"}

### Lägg till innehåll

Använd _[!UICONTROL Add Content]_i [!DNL Page Builder] för att lägga till befintligt innehåll i [[!DNL Page Builder] stage](workspace.md#stage). När du drar en mediainnehållstyp från panelen till scenen visas en behållare. Använd verktygslådan för innehållstyp för att komma åt_ Inställningar _som är specifika för typen.

![[!DNL Page Builder] panel med Lägg till innehållstyper](./assets/pb-add-content.png){width="600" zoomable="yes"}

| Innehållstyp | Beskrivning |
| ---------------------------------------------------------------- | -------------------------------------------- |
| [Blockera](block.md) | Lägger till ett befintligt block på scenen. |
| [Dynamiskt block](dynamic-block.md) | Lägger till ett befintligt dynamiskt block på scenen. |
| [Produkter](products.md) | Lägger till en lista med produkter på scenen. |
| ![Endast Adobe Commerce](../assets/adobe-logo.svg) [Recommendations](recommendations.md) | Lägger till en rekommendationsenhet på scenen. |

{style="table-layout:auto"}

## Toolbox

Varje innehållsbehållare på scenen har en verktygslåda med alternativ. Alternativen varierar beroende på innehållstyp, men omfattar vanligtvis Flytta, Inställningar, Dölj/Visa, Duplicera och Ta bort.

### Visa verktygslådan

Håll pekaren över behållaren för att visa verktygslådan och välja ett alternativ.

![Alternativ för verktygslådan Rader](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

### Alternativ för verktygslådan

| Alternativ | Ikon | Beskrivning |
| --------- | ---------------------------------------- | ------------ |
| Flytta | ![Ikonen Flytta](./assets/pb-icon-move.png){width="25"} | Flyttar den aktuella innehållsbehållaren till en annan plats på scenen. |
| Lägg till | ![Ikonen Lägg till](./assets/pb-icon-add.png){width="25"} | Lägger till underordnade element som en knapp, bildruta eller tabb. |
| (etikett) |           | Identifierar behållarinnehållstypen. |
| Inställningar | ![Ikonen Inställningar](./assets/pb-icon-settings.png){width="25"} | Öppnar egenskaperna för innehållsbehållaren i redigeringsläge. |
| Dölj | ![Dölj ikon](./assets/pb-icon-hide.png){width="25"} | Döljer den aktuella innehållsbehållaren. |
| Visa | ![Visa ikon](./assets/pb-icon-show.png){width="25"} | Visar aktuell innehållsbehållare. |
| Duplicera | ![Duplicera, ikon](./assets/pb-icon-duplicate.png){width="25"} | Skapar en kopia av den aktuella innehållsbehållaren. |
| Ta bort | ![Ta bort](./assets/pb-icon-remove.png){width="25"} | Tar bort aktuell innehållsbehållare från scenen. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}
