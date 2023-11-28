---
title: Media - Skjutreglage
description: Lär dig mer om Slider-innehållstypen som används för att lägga till ett bildspel med bilder i [!DNL Page Builder] stage.
exl-id: 757dbdc3-b146-4ef8-a17d-59f8da62626f
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '3799'
ht-degree: 0%

---

# Media - Skjutreglage

Använd _Skjutreglage_ innehållstyp för att lägga till ett bildspel med bilder i [[!DNL Page Builder] stage](workspace.md#stage). Du kan överföra nya bilder eller välja befintliga bilder från galleriet eller produktkatalogen. Ett reglage kan ställas in så att det spelas upp automatiskt eller styras manuellt med navigeringsknappar. Information om hur du associerar skjutreglaget med en viss befordran finns i [Dynamiskt block](dynamic-block.md).

![Mediereglaget i butiken](./assets/pb-media-slider-buy3-get1free-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Verktygslådor

När du arbetar med Slider-innehållstypen lägger du till och redigerar enskilda bildrutor och den skjutreglagebehållare som innehåller en eller flera bildrutor. Varje bild har en egen verktygslåda som du använder för att utforma bilder på [!DNL Page Builder] stage.

## Verktygslåda för enskilda bilder

![Verktygslåda för enskilda bilder](./assets/pb-media-slider-toolbox-slide-row.png){width="500" zoomable="yes"}

| Verktyg | Ikon | Beskrivning |
|--- |--- |--- |
| Flytta | ![Ikonen Flytta](./assets/pb-icon-move.png){width="25"} | Flyttar bildrutan till en annan plats på skjutreglaget. |
| (etikett) | Bild # | Identifierar numret på den aktuella bilden. |
| Inställningar | ![Ikonen Inställningar](./assets/pb-icon-settings.png){width="25"} | Öppnar _[!UICONTROL Edit Slide]_där du kan ändra den aktuella bildens egenskaper. |
| Duplicera | ![Duplicera, ikon](./assets/pb-icon-duplicate.png){width="25"} | Skapar en kopia av den aktuella bildrutan. |
| Ta bort | ![Ikonen Ta bort](./assets/pb-icon-remove.png){width="25"} | Tar bort den aktuella bildrutan från skjutreglaget. |

{style="table-layout:auto"}

## Verktygslådan Skjutreglage

| Verktyg | Ikon | Beskrivning |
|--- |--- |--- |
| Flytta | ![Ikonen Flytta](./assets/pb-icon-move.png){width="25"} | Flyttar reglaget till en annan plats på scenen. |
| (etikett) | [!UICONTROL Slider] | Anger skjutreglagebehållaren. |
| Inställningar | ![Ikonen Inställningar](./assets/pb-icon-settings.png){width="25"} | Öppnar _[!UICONTROL Edit Slider]_sidan där du kan ändra egenskaperna för videon och behållaren. |
| Dölj | ![Dölj ikon](./assets/pb-icon-hide.png){width="25"} | Döljer det aktuella skjutreglaget. |
| Visa | ![Visa ikon](./assets/pb-icon-show.png){width="25"} | Visar det dolda skjutreglaget. |
| Duplicera | ![Duplicera, ikon](./assets/pb-icon-duplicate.png){width="25"} | Skapar en kopia av skjutreglaget. |
| Ta bort | ![Ikonen Ta bort](./assets/pb-icon-remove.png){width="25"} | Tar bort skjutreglaget från scenen. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Lägga till en enskild bildruta

1. Öppna sidan, blocket eller det dynamiska blocket där du vill placera reglaget och expandera **[!UICONTROL Content]** -avsnitt.

1. I [!DNL Page Builder] panel, expandera **[!UICONTROL Media]** och dra en **[!UICONTROL Slider]** platshållare till en rad, kolumn eller tabb på scenen.

   I följande exempel är radens bakgrundsfärg gul (`#fffd16`).

   ![Dra skjutreglaget till scenen](./assets/pb-media-slider-drag-row.png){width="600" zoomable="yes"}

   Skjutreglagebehållaren visas på scenen med en enda tom bildruta.

1. Klicka i skjutreglagebehållaren för att visa [textredigerare](../content-design/editor.md) och ange innehåll för den första bilden.

   Du kan även inkludera mer komplext banderollinnehåll med [Innehåll](#content) inställningar.

1. Klicka på navigeringspunkten längst ned i skjutreglaget för att visa verktygslådan för den enskilda bildrutan och välj _Inställningar_ ( ![Ikonen Inställningar](./assets/pb-icon-settings.png){width="20"} ).

   Skjutreglage har två verktygslådor. Se till att du använder bildverktygslådan längst ned.

1. Slutför inställningarna efter behov enligt följande avsnitt:

   - [[!UICONTROL Appearance]](#appearance)
   - [[!UICONTROL Background]](#background)
   - [[!UICONTROL Content]](#content)
   - [[!UICONTROL Search Engine Optimization]](#seo)
   - [[!UICONTROL Advanced]](#advanced)

1. När du är klar klickar du på **[!UICONTROL Save]** för att använda inställningarna och gå tillbaka till [!DNL Page Builder] arbetsyta.

## Lägg till fler bilder

I följande avsnitt beskrivs en serie steg som du kan använda för att börja med en enskild bildruta och skapa ett responsivt reglage med funktioner och länkar till specifika produkter. Om du inte redan har en enskild bildruta följer du instruktionerna ovan för att lägga till en enskild bildruta på scenen.

Om du vill lägga till bildrutor använder du en eller flera av följande metoder:

### Metod 1: Duplicera en befintlig bildruta

Du kan spara tid genom att duplicera en bildruta som redan har konfigurerats med de nödvändiga inställningarna.

1. Klicka på navigeringspunkten under bildrutan för att visa verktygslådan och välj _Duplicera_ ( ![Duplicera, ikon](./assets/pb-icon-duplicate.png){width="20"} ).

   ![Duplicera en bildruta](./assets/pb-media-slider-duplicate-slide.png){width="500" zoomable="yes"}

1. Klicka på navigeringspunkten för den nya bildrutan och visa verktygslådan och välj _Inställningar_ ( ![Ikonen Inställningar](./assets/pb-icon-settings.png){width="20"} ).

1. Ändra inställningarna efter behov enligt följande avsnitt:

   - [[!UICONTROL Appearance]](#appearance)
   - [[!UICONTROL Background]](#background)
   - [[!UICONTROL Content]](#content)
   - [[!UICONTROL Advanced]](#advanced)

1. När du är klar klickar du på **[!UICONTROL Save]** för att använda inställningarna och gå tillbaka till [!DNL Page Builder] arbetsyta.

### Metod 2: Lägg till en ny tom bildruta

1. Hovra över skjutreglagebehållaren längst upp för att visa verktygslådan och välj _Lägg till_ ( ![Ikonen Lägg till](./assets/pb-icon-add.png){width="20"} ).

   ![Lägga till en tom bildruta](./assets/pb-media-slider-toolbox-add.png){width="500" zoomable="yes"}

   En ny tom bildruta med en egen navigeringspunkt och verktygslåda läggs till i skjutreglaget och visas på scenen.

   ![Ny bild med verktygslåda](./assets/pb-media-slider-slide2-toolbox.png){width="500" zoomable="yes"}

1. Klicka på navigeringspunkten för den nya bildrutan och visa verktygslådan och välj _Inställningar_ ( ![Ikonen Inställningar](./assets/pb-icon-settings.png){width="20"} ).

1. Ändra inställningarna efter behov enligt följande avsnitt:

   - [[!UICONTROL Appearance]](#appearance)
   - [[!UICONTROL Background]](#background)
   - [[!UICONTROL Content]](#content)
   - [[!UICONTROL Advanced]](#advanced)

1. När du är klar klickar du på **[!UICONTROL Save]** i det övre högra hörnet för att stänga _[!UICONTROL Edit Slide]_sida.

### Lägga till widget i en bildruta

Du kan lägga till valfritt [widgettyp](../content-design/widgets.md#widget-types) till din bild i en [!DNL Page Builder] scenen med följande steg:

1. [Skapa widgeten](../content-design/widget-create.md) som du vill se på en bildruta.

1. Öppna sidan, blocket eller det dynamiska blocket där du vill placera reglaget och expandera **[!UICONTROL Content]** -avsnitt.

1. I [!DNL Page Builder] panel, expandera **[!UICONTROL Media]** och dra en **[!UICONTROL Slider]** platshållare till en rad, kolumn eller tabb på scenen.

1. Klicka i skjutreglagebehållaren för att visa [textredigerare](../content-design/editor.md) och klickar på _Infoga widget_ ( ![Ikon för att infoga widget](./assets/editor-btn-insert-widget.png){width="20"} ).

1. Välj **[!UICONTROL Widget Type]** du behöver.

1. Ange inställningarna, som är olika beroende på typen av widget

   ![Exempel på hur du infogar en widget i bildrutan](./assets/insert-widget-to-slide-page.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Insert Widget]** längst upp till höger.

1. Ändra övriga inställningar efter behov.

1. När du är klar klickar du på **[!UICONTROL Save]** längst upp till höger.

   ![Exempel på infogad widget i bildrutan](./assets/inserting-widget-on-slide.png){width="600" zoomable="yes"}

### Visa varje bild

Om du vill visa varje bildruta på scenen klickar du på nästa punkt under den bildruta som visas.

![Färdigt reglage](./assets/pb-media-slider-slide2.png){width="500" zoomable="yes"}

Bilden i föregående exempel har en bakgrundsbild, en genomskinlig mobilbild och en textbunden bild som har lagts till från textredigeraren. Den här tekniken fungerar bra på mobila enheter genom att stänga av bakgrundsbilden och bara visa den mindre textbundna bilden. Produktbilden i det här exemplet har följande ytterligare inställningar:

| Alternativ | Exempelinställning |
|--- |--- |
| [!UICONTROL Appearance] | `Collage Right` |
| [!UICONTROL Background Color] | `#ffffff` (Vit) |
| [!UICONTROL Background Image] | Bilden på den här bilden sparades från produktsidan och överfördes till galleriet. |
| [!UICONTROL Mobile Background Image] | Den mobila bakgrundsbilden är en genomskinlig bild som är 10 pixlar fyrkantig. Om du använder en tom bild för mobilen ersätts standardbakgrundsbilden med en osynlig bild. |
| [!UICONTROL Background Size] | `Auto` |
| [!UICONTROL Message Text] | `Minerva LumaTech&trade; V-Tee` (Centrera) med infogad bild skalad till 40 % (Centrera) |
| [!UICONTROL Link] | `Product` |
| [!UICONTROL Show Button] | `Always` |
| [!UICONTROL Button Text] | `Buy Now` |
| [!UICONTROL Show Overlay] | `Never Show` |
| [!UICONTROL Alignment] | `Center` (för att justera knappen) |
| [!UICONTROL Border] | `Solid` |
| [!UICONTROL Border Color] | `#000000` (Svart) |
| [!UICONTROL Border Width] | `1 px` |

{style="table-layout:auto"}

## Ändra inställningar för enskilda bildrutor

1. Ändra skjutreglaget på scenen och visa den bildruta som du vill ändra.

1. I verktygslådan för enskilda bildrutor väljer du _Inställningar_ ( ![Ikonen Inställningar](./assets/pb-icon-settings.png){width="20"} ) och slutför inställningarna efter behov enligt följande avsnitt.

1. Klicka på i det övre högra hörnet **[!UICONTROL Save]** för att använda inställningarna och gå tillbaka till [!DNL Page Builder] arbetsyta.

### [!UICONTROL Appearance]

1. Välj någon av följande bildplaceringstyper:

   | Typ | Beskrivning |
   | ---- | ----------- |
   | `Poster` | Centrerar bildruteinnehållet i skjutreglagebehållaren. Om övertäckningen används utökas reglagets hela bredd. |
   | `Collage Left` | Placerar bildinnehållet i ett definierat område på vänster sida av skjutreglagebehållaren. Om övertäckningen används, täcker den bara det definierade området. |
   | `Collage Center` | Placerar bildinnehållet i ett definierat område centrerat i skjutreglagebehållaren. Om övertäckningen används, täcker den bara det definierade området. |
   | `Collage Right` | Placerar bildinnehållet i ett definierat område på den högra sidan av skjutreglagebehållaren. Om övertäckningen används, täcker den bara det definierade området. |

   {style="table-layout:auto"}

   ![Bildplacering](./assets/pb-slide-appearance-collage-right.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Slide Name]**.

   När du arbetar i redigeringsläge visas bildrutenamnet som ett verktygstips ovanför navigeringspunkten. Bildrutenamnet visas inte från butiken.

   ![Bildnamn i navigeringen](./assets/pb-media-slider-name-buy3-get1free.png){width="500" zoomable="yes"}

1. Ange **[!UICONTROL Minimum Height]** för bilden.

   Den minsta höjden kan vara ett tal med valfri giltig CSS-enhet (till exempel `100px`, `50%`, `50em`, `100vh`) eller en beräkning (som `100vh - 237px`).

   Du kan till exempel ställa in bildspelets minsta höjd så att den täcker hela sidans höjd och sedan använda bakgrundsbilder och -videor för att skapa snygga designalternativ.

   >[!NOTE]
   >
   >När bildrutan är inställd på hela sidhöjden (100vh) sträcks även reglaget som innehåller bildrutan ut hela sidhöjden så att den passar bildrutans höjd.

## [!UICONTROL Background]

Det finns många alternativ för att definiera bakgrundsvisningen för en bildruta. Du kan använda en enkel färg- eller bakgrundsbild och hantera mer avancerade effekter.

### [!UICONTROL Background Color]

Ange bakgrundsfärgen genom att välja en färgruta, klicka på färgväljaren eller genom att ange ett giltigt färgnamn eller motsvarande hexadecimalt värde. Den här inställningen bestämmer radens bakgrundsfärg. Du kan också justera färgens opacitet.

![Ingen färg (standard)](./assets/pb-settings-background-color-no-color.png){width="200"}

Du kan ange värdet på ett av tre sätt:

- Ett fördefinierat färgnamn, till exempel `White`
- Det hexadecimala färgvärdet för färgen, till exempel `#ffffff`
- rgba-värdet för färgen, med opacitetsprocent, till exempel `rgba(255, 255, 255, 0.75)`

Om du vill välja en färg klickar du på färgrutan till vänster om _Ingen färg_ box.

![Välja en färgruta](./assets/pb-settings-background-color-picker-swatch.png){width="600" zoomable="yes"}

Om du klickar på färgrutan för att öppna färgväljaren igen visar rutan under reglaget de aktuella värdena för rött, grönt, blått och alfa (rgba). Det sista talet anger den aktuella opaciteten i procent som decimal. Du kan justera opaciteten med hjälp av skjutreglaget eller ange ett decimalvärde.

![Ange opacitet för bakgrundsfärg](./assets/pb-settings-background-color.png){width="600" zoomable="yes"}

>[!NOTE]
>
>[!DNL Page Builder] har även stöd för genomskinliga lager, eller _alfakanal_, i bakgrundsbilder som kan användas för att skapa bakgrunder med varierande grad av opacitet.

### [!UICONTROL Background Type]

En bakgrundstyp kan vara en bild eller en video. [!DNL Page Builder] standardvärdet är `Image` och visar olika bildinställningar. Om du väljer `Video`, [!DNL Page Builder] byter ut bildinställningarna mot videoinställningarna. Båda bakgrundstypsinställningarna beskrivs i följande avsnitt.

![Bakgrundstyp](./assets/pb-background-type.png){width="400"}

### Inställningar för bildtyp

Om du anger _[!UICONTROL Background Type]_till `Image`använder du följande inställningar för att definiera hur bakgrundsbilden ska visas.

![Banderoll med bakgrundsbild](./assets/pb-tutorial1-banner-background.png){width="600" zoomable="yes"}

- **[!UICONTROL Background Image]** - Använd vid behov de medföljande verktygen för att välja en bakgrundsbild som ska användas på banderollen:

  | Verktyg | Beskrivning |
  | ---- | ----------- |
  | [!UICONTROL Upload] | Överför en bildfil från den lokala datorn till galleriet och använder den sedan som bakgrundsbild för banderollen. |
  | [!UICONTROL Select from Gallery] | Uppmanar dig att välja en befintlig bild från galleriet som bakgrundsbild för banderollen. |
  | ![Kameraikon](./assets/pb-icon-camera.png){width="25"} | Gör att du kan dra bilden till kamerapanelen eller bläddra till bilden i det lokala filsystemet. |

  {style="table-layout:auto"}

- **[!UICONTROL Background Mobile Image]** - Använd vid behov samma verktyg för att välja en annan bakgrundsbild som ska användas för visning på mobila enheter.

- **[!UICONTROL Background Size]** - Välj hur bakgrundsbilden ska skalförändras i förhållande till banderollens bredd:

  | Alternativ | Beskrivning |
  | ------ | ----------- |
  | `Cover` | Bakgrundsbilden täcker banderollens hela bredd. |
  | `Contain` | Bakgrundsbilden är begränsad till innehållsområdets bredd. |
  | `Auto` | Använder storleken från den aktuella formatmallen. |

  {style="table-layout:auto"}

  ![Bakgrundsstorlek](./assets/pb-layout-row-settings-background-size-cover.png){width="400"}

- **[!UICONTROL Background Position]** - Välj hur bakgrundsbilden ska förankras i förhållande till banderollen:

  | Ankarpunkt | Position |
  | ------------ | -------- |
  | `Top` | Vänster / Mitten / Höger |
  | `Center` | Vänster / Mitten / Höger |
  | `Bottom` | Vänster / Mitten / Höger |

  {style="table-layout:auto"}

  Fästpunkten är som ett push-stift som fäster bilden vid banderollen vid den angivna bakgrundspositionen.

- **[!UICONTROL Background Repeat]** - Om du vill upprepa bakgrundsbilden för att fylla utrymmet ändrar du den här inställningen `Yes`.

### Inställningar för videotyp

Om du anger _Bakgrundstyp_ till `Video`använder du följande inställningar för att definiera hur bakgrundsbilden ska visas.

- **[!UICONTROL Video URL]** - Ange en giltig video-URL. Giltiga video-URL:er kan vara länkar till:

   - YouTube videofilmer: `https://youtu.be/CoDhMRUUjeI`
   - Vimeo-videor: `https://vimeo.com/190156113`
   - Giltiga videofiler (`.mp4` rekommenderas): `https://myvideos.com/spiral.mp4`

  ![URL för bakgrundsvideo](./assets/pb-video-url.png){width="500"}

- **[!UICONTROL Overlay Color]** - Välj en färg som du vill använda en genomskinlig färgton på videon.

- **[!UICONTROL Infinite Loop]** - Ange som `No` för att få videon att spelas upp en gång och stoppa. När det här alternativet är inställt på `Yes` (standard) upprepas videon i en oändlig slinga.

- **[!UICONTROL Lazy Load]** - Ange som `No` för att göra så att videon läses in med sidan, även när den inte syns. När det här alternativet är inställt på `Yes` (standard) läses videon bara in från källan när den visas på skärmen.

- **[!UICONTROL Play Only When Visible]** - Ange som `No` för att få videon att börja spelas upp omedelbart efter att den har lästs in, oavsett om den är synlig eller inte. När det här alternativet är inställt på `Yes` (standard) spelas videon bara upp när den är synlig.

- **[!UICONTROL Fallback Image]** - Om det behövs anger du en bild som ska visas på skärmen innan videon läses in och om videon inte läses in av någon anledning.

## [!UICONTROL Content]

Du kan ändra bildinnehållet direkt på scenen eller när du ändrar inställningarna. Inställningarna innehåller mer komplexa innehållsfunktioner, som bildlänkar, knappar och övertäckningar. Innehållets position återspeglar [Utseende](#appearance) placeringsinställning.

### Enkelt innehåll på scenen

1. Klicka på platshållaren eller den befintliga texten och ange den nya texten som du vill ska visas på bildrutan.

   Redigeringsverktygsfältet visas ovanför textrutan.

1. Använd redigerarens verktygsfält för att ange och formatera text samt infoga element som länkar, bilder och widgetar.

   ![Scen med formaterad text](./assets/pb-tutorial1-banner-stage-text-format-line2.png){width="500" zoomable="yes"}

### Komplext innehåll i inställningarna

1. Klicka på navigeringspunkten längst ned i skjutreglaget för att visa verktygslådan för den enskilda bildrutan och välj _Inställningar_ ( ![Ikonen Inställningar](./assets/pb-icon-settings.png){width="20"} ).

1. I _[!UICONTROL Content]_anger du **[!UICONTROL Message Text]**som du vill ska visas med bildrutan.

1. Bläddra nedåt till _[!UICONTROL Content]_-avsnittet och använd **[!UICONTROL Message Text]**för att ange och formatera bannertext.

   Du kan också infoga element, till exempel textlänkar, bilder och widgetar.

1. Formatera texten efter behov med redigeringsverktygsfältet.

   Den första bilden i det här exemplet har en bakgrundsbild, men ingen meddelandetext. The `Buy 3 Get 1 Free` text ovanför skjutreglaget finns i en textbehållare (läggs till senare).

1. Ange vid behov en **[!UICONTROL Link]** för bilden.

   Länken är den målsida som visas när kunden klickar på bildruteområdet. Du kan använda en av tre länktyper:

   - **[!UICONTROL URL]** - Länkar till en relativ eller fullständig URL-adress.

   - **[!UICONTROL Product]** - Identifierar målsidan baserat på produktnamnet eller SKU:n. Sök efter produkten efter namn baserat på antingen ett partiellt eller fullständigt namn. Välj produkten i sökresultatlistan.

     ![Välja en produkt att länka](./assets/pb-media-image-settings-image-link-product-results.png){width="600" zoomable="yes"}

   - **[!UICONTROL Category]** - Identifierar målsidan som en specifik kategori eller underkategori i kategoriträdet. Sök efter kategorin utifrån antingen ett helt eller delvis namn. Välj kategori i det utökade avsnittet i det visade trädet.

     ![Välja en kategori att länka till](./assets/pb-settings-link-category-womens-tees.png){width="600" zoomable="yes"}

   - **[!UICONTROL Page]** - Identifierar målsidan som en specifik innehållssida. Sök efter sidan baserat på ett helt eller delvis namn. Välj sidan i sökresultatlistan.

     ![Välja en sida att länka till](./assets/pb-media-image-settings-image-link-page-results.png){width="600" zoomable="yes"}

   <div class="bs-callout-info" markdown="1">
   Från och med version 2.4.1, [!DNL Page Builder] stöder inte längre länkning av bildrutan och länkar i den kapslade texten på grund av problem med visningen i butiken. Om du använder en länk i _[!UICONTROL Message Text]_ kan du inte konfigurera _[!UICONTROL Link]_. Om du föredrar att använda en enda länk för hela bilden kan du ta bort alla länkar från texten.

   ![Länkkonfigurationen har blockerats](./assets/pb-nested-link-blocked.png){width="300"}
   </div>

   Om du vill hindra besökaren från att navigera utanför din butik väljer du **[!UICONTROL Open in new tab]** kryssrutan. När kryssrutan är avmarkerad öppnas det länkade målet på samma webbläsarflik, som kan navigera besökaren bort från din butik.

1. Om det behövs lägger du till en knapp som uppmanar kunderna att följa länken.

   Bilden _Utseende_ placerar en enskild länk eller knapp under texten. Fyll i egenskaperna för länken eller knappen som du vill lägga till.

   ![Bildutseende - collage höger](./assets/pb-slide-appearance-collage-right.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Du kan också använda flera knappar eller länkar genom att lägga till en [block](block.md) till bannern. För att undvika konflikter ska du behålla alla länkar eller knappar i det separata blocket och inte lägga till en länk eller knapp direkt i banderollen.

   - Ange **[!UICONTROL Show Button]** till något av följande:

     | Alternativ | Beskrivning |
     | ------ | ----------- |
     | `Always` | En knapp visas alltid på bildrutan. |
     | `On Hover` | En knapp visas bara på bildrutan när du hovrar. |
     | `Never Show` | En knapp visas aldrig på bilden. |

     {style="table-layout:auto"}

   - Ange **[!UICONTROL Button Text]** som ska visas på knappen.

   - Ange **[!UICONTROL Button Type]** till något av följande:

     | Alternativ | Beskrivning |
     | ------ | ----------- |
     | `Primary` | Använder det primära knappformatet från den aktuella formatmallen. |
     | `Secondary` | Använder det sekundära knappformatet från den aktuella formatmallen, om tillämpligt. |
     | `Link` | Skapar en hyperlänk i stället för en knapp. |

     {style="table-layout:auto"}

     Knappformatet från det aktuella temat avgör knappformatet. Vanligtvis har en primärknapp en mer framträdande bakgrundsfärg än en sekundär knapp.

1. Ange **[!UICONTROL Show Overlay]** till något av följande:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | `Always` | Övertäckningen är alltid synlig. |
   | `On Hover` | Övertäckningen visas bara vid hovring. |
   | `Never Show` | Övertäckningen är inte synlig. |

   {style="table-layout:auto"}

   Du kan använda en övertäckning för att använda en bakgrundsfärg på det aktiva innehållsområdet som definieras av inställningen Utseende. Bakgrundsbilden för bildrutan förblir synlig för bildrutans hela bredd.

   ![Inställningar för bildövertäckning](./assets/pb-media-slider-overlay-settings.png){width="600" zoomable="yes"}

   Om du väljer att visa en övertäckning anger du **[!UICONTROL Overlay Color]**:

   - Klicka på _Ingen färg_ och välj en färgruta.
   - I **[!UICONTROL Color]** anger du ett giltigt färgnamn eller ett hexadecimalt värde.

   ![Övertäckningsfärg för bild](./assets/pb-tutorial1-banner-settings-overlay-color.png){width="600" zoomable="yes"}


## [!UICONTROL Search Engine Optimization] {#seo}

Texten för de här inställningarna visas för sökmotorer och förbättrar indexeringen av sidan.

- För **[!UICONTROL Alternative Text]**, ange en _alt_ textbeskrivning för de digitala tillgänglighetsverktygen som ska visas.

  Alternativtext är en god hjälpmedelspraxis och krävs enligt lag i vissa språkområden. I HTML `alt` är en delmängd av `image` tagg: `<image title="tooltip" alt="description" src="image.jpg">`.

- För **[!UICONTROL Title Attribute]** anger du den text som ska visas som ett verktygstips när du för musen över.

  Det bästa sättet är att välja en beskrivande, nyckelordsrik titel som förbättrar hur bilden indexeras av sökmotorer. I HTML `title` är en delmängd av `image` tagg: `<image title="tooltip" alt="description" src="image.jpg">`.

## [!UICONTROL Advanced]

1. Om du vill styra den vågräta placeringen av innehåll som läggs till i bildrutan väljer du **[!UICONTROL Alignment]**:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | `Default` | Använder den standardinställning för justering som anges i formatmallen för det aktuella temat. |
   | `Left` | Justerar innehållet längs bildens vänstra kant, med hänsyn tagen till eventuell utfyllnad som har angetts. |
   | `Center` | Justerar innehållet i bildens mitt, med hänsyn till eventuell utfyllnad som har angetts. |
   | `Right` | Justerar innehållet längs bildrutans högra kant, med hänsyn tagen till eventuell utfyllnad. |

   {style="table-layout:auto"}

1. Ange **[!UICONTROL Border]** format som används på alla fyra sidorna av bildrutan:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | `Default` | Använder det standardkantlinjeformat som anges av den associerade formatmallen. |
   | `None` | Visar ingen synlig indikation på bildrutekanten. |
   | `Dotted` | Behållarramen visas som en prickad linje. |
   | `Dashed` | Behållarramen visas som en streckad linje. |
   | `Solid` | Behållarramen visas som en heldragen linje. |
   | `Double` | Behållarramen visas som en dubbel linje. |
   | `Groove` | Behållarkanten visas som en utdragen linje. |
   | `Ridge` | Behållarkanten visas som en rak linje. |
   | `Inset` | Behållarramen visas som en indragen linje. |
   | `Outset` | Behållarramen visas som en startrad. |

   {style="table-layout:auto"}

1. Om du anger ett annat kantlinjeformat än `None`slutför du visningsalternativen för kantlinjer:

   ![Kantfärg](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

   | Alternativ | Beskrivning |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Ange färgen genom att välja en färgruta, klicka på färgväljaren eller genom att ange ett giltigt färgnamn eller motsvarande hexadecimalt värde. |
   | [!UICONTROL Border Width] | Ange antalet pixlar för kantlinjens bredd. |
   | [!UICONTROL Border Radius] | Ange antalet pixlar för att definiera radiens storlek som används för att runda varje hörn av kanten. |

   {style="table-layout:auto"}

1. (Valfritt) Ange namnen på **[!UICONTROL CSS classes]** från den aktuella formatmallen som ska användas på bildrutan.

   Avgränsa flera klassnamn med blanksteg.

1. Ange värden i pixlar för **[!UICONTROL Margins and Padding]** för att ange bildrutans yttre marginaler och inre utfyllnad.

   Ange varje motsvarande värde i bildspelet.

   | Behållarområde | Beskrivning |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | Mängden tomt utrymme som används på utsidan av alla sidor av bildrutan. |
   | [!UICONTROL Padding] | Mängden tomt utrymme som används på insidan av alla sidor av bildrutan. |

   {style="table-layout:auto"}

## Lägga till en skjutreglagetitel

Om du vill ha en titel ovanför skjutreglaget lägger du bara till en [Textinnehållstyp] ovanför skjutreglaget. Formatera sedan texten efter behov.

1. I [!DNL Page Builder] panel, expandera **[!UICONTROL Elements]** och dra en **Text** platshållare för en rad, kolumn eller tabb som anges på scenen.

   När du drar markerar en röd stödlinje insättningspunkten ovanför skjutreglaget.

   ![Dra en textplatshållare ovanför ett reglage](./assets/pb-media-slider-elements-text-drag.png){width="600" zoomable="yes"}

1. Använd redigeraren för att formatera texten efter behov.

   ![Redigera skjutreglagets titeltext](./assets/pb-media-slider-elements-text-editor.png){width="500" zoomable="yes"}

## Ändra skjutreglageinställningar

1. Håll pekaren över skjutreglaget för att visa verktygslådan och välj _Inställningar_ ( ![Ikonen Inställningar](./assets/pb-icon-settings.png){width="20"} ).

   ![Verktygslådan Skjutreglage](./assets/pb-media-slider-tee-shirts-main-toolbox.png){width="500" zoomable="yes"}

1. Ange **[!UICONTROL Minimum Height]** för bilden.

   Den minsta höjden kan vara ett tal med valfri giltig CSS-enhet (till exempel `100px`, `50%`, `50em`, `100vh`) eller en beräkning (som `100vh - 237px`).

   Du kan till exempel ange den minsta höjden för ett reglage så att hela sidhöjden sträcks ut, vilket ger dig tilltalande alternativ för helsidesbakgrundsbilder och -videor.

   ![Lägsta höjd för skjutreglage](./assets/pb-media-slider-settings-minimum-height.png){width="400"}

1. Om du vill att skjutreglaget ska börja när sidan läses in anger du **[!UICONTROL Autoplay]** till `Yes` och ange **[!UICONTROL Autoplay Speed]** till antalet millisekunder i fördröjningen mellan bildrutorna.

   Som standard är hastigheten inställd på 4 000 ms, vilket är fyra sekunder. Om du ställer in automatisk uppspelning på `No`visas den första bilden som standard och kunden måste klicka på bildnavigeringen (punkter eller pilar) för att visa nästa bild i sekvens.

   ![Inställningar för automatisk uppspelning av skjutreglage](./assets/pb-media-slider-settings-autoplay.png){width="600" zoomable="yes"}

1. Om du vill jämna ut övergången från en bildruta till nästa anger du **[!UICONTROL Fade]** till `Yes`.

   När du tonar verkar bilderna vara på plats, men innehållet ändras jämnt från en till nästa. Utan att tona visas den vågräta rörelsen från en bildruta till nästa.

   ![Inställningar för Slider-toning och oändlig slinga](./assets/pb-media-slider-settings-fade-infinite-loop.png){width="600" zoomable="yes"}

1. Om du vill att bildspelet ska upprepas oavbrutet när sidan är öppen anger du **[!UICONTROL Infinite Loop]** till `Yes`.

1. Så här väljer du typ av navigeringskontroller för skjutreglaget:

   - Inkludera _Nästa_ och _Föregående_ pilar till vänster och höger om varje bildruta, ange **[!UICONTROL Show Arrows]** till `Yes`.

   - Om du vill inkludera en uppsättning navigeringspunkter under skjutreglaget anger du **[!UICONTROL Show Dots]** till `Yes`.

   ![Skjutreglaget visar pilar och punkter](./assets/pb-media-slider-settings-show-arrows-dots.png){width="600" zoomable="yes"}

1. Slutför [Avancerat](#slider-advanced) skjutreglagen efter behov.

1. När du är klar klickar du på **[!UICONTROL Save]** för att använda inställningarna och gå tillbaka till [!DNL Page Builder] arbetsyta.

### Avancerat - reglage {#slider-advanced}

1. Om du vill styra placeringen av bildrutorna i den överordnade skjutreglagebehållaren väljer du **[!UICONTROL Alignment]**:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | `Default` | Använder den standardinställning för justering som anges i formatmallen för det aktuella temat. |
   | `Left` | Justerar bildrutorna längs skjutreglagebehållarens vänstra kant, med hänsyn tagen till eventuell utfyllnad. |
   | `Center` | Justerar bildrutorna i mitten av skjutreglagebehållaren, med hänsyn till eventuell utfyllnad som har angetts. |
   | `Right` | Justerar bildrutorna längs skjutreglagebehållarens högra kant, med hänsyn tagen till eventuell utfyllnad. |

   {style="table-layout:auto"}

1. Ange **[!UICONTROL Border]** format som används på alla fyra sidorna i skjutreglagebehållaren:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | `Default` | Använder det standardkantlinjeformat som anges av den associerade formatmallen. |
   | `None` | Visar inte någon synlig indikation för behållarkanterna. |
   | `Dotted` | Behållarramen visas som en prickad linje. |
   | `Dashed` | Behållarramen visas som en streckad linje. |
   | `Solid` | Behållarramen visas som en heldragen linje. |
   | `Double` | Behållarramen visas som en dubbel linje. |
   | `Groove` | Behållarkanten visas som en utdragen linje. |
   | `Ridge` | Behållarkanten visas som en rak linje. |
   | `Inset` | Behållarramen visas som en indragen linje. |
   | `Outset` | Behållarramen visas som en startrad. |

   {style="table-layout:auto"}

1. Om du anger ett annat kantlinjeformat än `None`slutför du visningsalternativen för kantlinjer:

   | Alternativ | Beskrivning |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Ange färgen genom att välja en färgruta, klicka på färgväljaren eller genom att ange ett giltigt färgnamn eller motsvarande hexadecimalt värde. |
   | [!UICONTROL Border Width] | Ange antalet pixlar för kantlinjens bredd. |
   | [!UICONTROL Border Radius] | Ange antalet pixlar för att definiera radiens storlek som används för att runda varje hörn av kanten. |

   {style="table-layout:auto"}

1. (Valfritt) Ange namnen på **[!UICONTROL CSS classes]** från den aktuella formatmallen som ska användas för skjutreglagebehållaren.

   Avgränsa flera klassnamn med blanksteg.

1. Ange värden i pixlar för **[!UICONTROL Margins and Padding]** för att bestämma de yttre marginalerna och den inre utfyllnaden för skjutreglagebehållaren.

   Ange motsvarande värden i diagrammet.

   | Behållarområde | Beskrivning |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | Mängden tomt utrymme som används på ytterkanten på behållarens alla sidor. |
   | [!UICONTROL Padding] | Mängden tomt utrymme som används på behållarens inre kant på alla sidor. |

   {style="table-layout:auto"}

## Testa skjutreglaget

1. Öppna sidan där du har inkluderat reglaget, ange **[!UICONTROL Enable Page]** till `Yes`.

1. Klicka i det övre högra hörnet på **[!UICONTROL Save]** pil och välj **[!UICONTROL Save & Close]**.

1. Hitta sidan i _Sidor_ stödraster och markera **[!UICONTROL View]** i _[!UICONTROL Action]_kolumn.

   ![Förhandsgranskning av reglage - standardvy](./assets/pb-media-slider-desktop-view.png){width="600" zoomable="yes"}

   När du förhandsgranskar skjutreglaget ändrar du storlek på fönstret så att du kan se hur det ser ut på en mobil enhet.

   ![Förhandsgranskning av reglage - mobilvy](./assets/pb-media-slider-mobile-view.png){width="400" zoomable="yes"}
