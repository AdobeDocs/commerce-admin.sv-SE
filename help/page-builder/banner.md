---
title: Media - banderoll
description: Lär dig mer om Banner-innehållstypen som används för att lägga till en illustrerad, interaktiv komponent i [!DNL Page Builder] stage.
exl-id: 287d866c-8a63-4531-8c1b-40d560a07947
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '2300'
ht-degree: 0%

---

# Media - banderoll

Använd _Banderoll_ innehållstyp för att lägga till en illustrerad, interaktiv komponent som engagerar användarna med en uppmaning till åtgärd och knapp i [[!DNL Page Builder] stage](workspace.md#stage).

>[!NOTE]
>
>Vad som tidigare var _Banderoll_ på menyn Innehåll, är nu [Dynamiskt block](../content-design/dynamic-blocks.md).

![Banderoll på startsidan för butiken](./assets/pb-banner-homepage.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Banderollverktygslåda

Banderollverktygslådan visas när du hovrar över banderollbehållaren.

![Banderollverktygslåda](./assets/pb-tutorial1-banner-toolbox.png){width="600" zoomable="yes"}

| Verktyg | Ikon | Beskrivning |
|--- |--- |--- |
| Flytta | ![Ikonen Flytta](./assets/pb-icon-move.png){width="25"} | Flyttar banderollen till en annan plats på scenen. |
| (etikett) | Banderoll | Identifierar den aktuella innehållsbehållaren som en banner. Håll pekaren över behållaren för att visa verktygslådan. |
| Inställningar | ![Ikonen Inställningar](./assets/pb-icon-settings.png){width="25"} | Öppnar sidan Redigera banderoll där du kan ändra egenskaperna för banderollen och behållaren. |
| Dölj | ![Dölj ikon](./assets/pb-icon-hide.png){width="25"} | Döljer den aktuella bannern. |
| Visa | ![Visa ikon](./assets/pb-icon-show.png){width="25"} | Visar den dolda banderollen. |
| Duplicera | ![Duplicera, ikon](./assets/pb-icon-duplicate.png){width="25"} | Skapar en kopia av banderollen. |
| Ta bort | ![Ikonen Ta bort](./assets/pb-icon-remove.png){width="25"} | Tar bort bannern från scenen. |
| [!UICONTROL Upload New Image] |  | Överför en bild från det lokala filsystemet till galleriet för banderollbakgrunden. |
| [!UICONTROL Select from Gallery] |  | Använder en befintlig bild från galleriet som bannerbakgrund. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Lägg till en banderoll

1. I [!DNL Page Builder] panel, expandera **[!UICONTROL Media]** och dra en **[!UICONTROL Banner]** platshållare till scenen.

   ![Dra en bannerinnehållstyp till scenen](./assets/pb-tutorial1-banner-drag-to-stage.png){width="600" zoomable="yes"}

   The _[!UICONTROL Upload Image]_och_[!UICONTROL Select from Gallery]_ -knappar inkluderas så att du snabbt kan ändra banderollinnehållet direkt från scenen. Du kan också ändra innehållet på _[!UICONTROL Edit Banner]_sida.

1. Klicka på banderollplatshållaren för att visa [textredigerare](../content-design/editor.md) och ange innehåll för banderollen.

   Du kan även inkludera mer komplext banderollinnehåll med [Innehåll](#content) inställningar.

## Ändra bannerinställningar

1. Håll pekaren över banderollbehållaren för att visa verktygslådan och välj _Inställningar_ (![Ikonen Inställningar](./assets/pb-icon-settings.png)).

1. Använd följande avsnitt för detaljerad information om hur du uppdaterar de tillgängliga inställningarna:

   - [[!UICONTROL Appearance]](#appearance)
   - [[!UICONTROL Content]](#content)
   - [[!UICONTROL Background]](#background)
   - [[!UICONTROL Advanced]](#advanced)

1. När du är klar klickar du på **[!UICONTROL Save]** i det övre högra hörnet för att stänga _[!UICONTROL Edit Banner]_sida.

1. Klicka på i det övre högra hörnet **[!UICONTROL Save]** för att använda inställningarna och gå tillbaka till [!DNL Page Builder] arbetsyta.

## [!UICONTROL Appearance]

Banderoller är enkla att installera och underhålla eftersom de är baserade på en av fyra fördefinierade mallar.

- Välj någon av följande banderollplaceringstyper:

  | Placement | Beskrivning |
  | --------- | ----------- |
  | [!UICONTROL Poster] | Centrerar innehållet och knappen på banderollen. Om övertäckningen används, utökas banderollens hela bredd. |
  | [!UICONTROL Collage Left] | Placerar innehåll och knapp i ett definierat område till vänster om banderollen. Om övertäckningen används, täcker den bara det definierade området. |
  | [!UICONTROL Collage Center] | Placerar innehåll och knapp i ett definierat område som är centrerat på banderollen. Om övertäckningen används, täcker den bara det definierade området. |
  | [!UICONTROL Collage Right] | Placerar innehåll och knapp i ett definierat område till höger om banderollen. Om övertäckningen används, täcker den bara det definierade området. |

  {style="table-layout:auto"}

  ![Utseende - collage höger](./assets/pb-tutorial1-row-banner-settings-appearance-collage-right.png){width="600" zoomable="yes"}

- (Valfritt) Ange **[!UICONTROL Minimum Height]** för raden.

  Den minsta höjden kan vara ett tal med valfri giltig CSS-enhet (till exempel `100px`, `50%`, `50em`, `100vh`) eller en beräkning (som `100vh - 237px`).

  Du kan till exempel ange den minsta höjden för en banderoll så att hela sidhöjden sträcks ut, vilket ger dig tilltalande alternativ för helsidesbakgrundsbilder och -videor.

## [!UICONTROL Background]

Det finns många alternativ för att definiera en banners bakgrundsvisning. Du kan använda en enkel färg- eller bakgrundsbild och hantera mer avancerade effekter.

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

![Ange opacitet](./assets/pb-settings-background-color.png){width="600" zoomable="yes"}

>[!NOTE]
>
>[!DNL Page Builder] har även stöd för genomskinliga lager, eller _alfakanal_, i bakgrundsbilder som kan användas för att skapa bakgrunder med varierande grad av opacitet.

### [!UICONTROL Background Type]

En bakgrundstyp kan vara en bild eller en video. [!DNL Page Builder] standardvärdet är `Image` och visar olika bildinställningar. Om du väljer `Video`, [!DNL Page Builder] byter ut bildinställningarna mot videoinställningarna. Båda bakgrundstypsinställningarna beskrivs i följande avsnitt.

![Bakgrundstyp](./assets/pb-background-type.png){width="200"}

### Inställningar för bildtyp

Om du anger _Bakgrundstyp_ till `Image`använder du följande inställningar för att definiera hur bakgrundsbilden ska visas.

![Banderoll med bakgrundsbild](./assets/pb-tutorial1-banner-background.png){width="600" zoomable="yes"}

- **[!UICONTROL Background Image]** - Använd vid behov de medföljande verktygen för att välja en bakgrundsbild som ska användas på banderollen:

  | Verktyg | Beskrivning |
  | ---- | ----------- |
  | [!UICONTROL Upload] | Överför en bildfil från den lokala datorn till galleriet och använder den sedan som bakgrundsbild för banderollen. |
  | [!UICONTROL Select from Gallery] | Uppmanar dig att välja en befintlig bild från galleriet som bakgrundsbild för banderollen. |
  | ![Kameraikon](./assets/pb-icon-camera.png){width="25"} | Gör att du kan dra bilden till kamerapanelen eller bläddra till bilden i det lokala filsystemet. |

  {style="table-layout:auto"}

- **[!UICONTROL Background Mobile Image]** - Använd vid behov samma verktyg för att välja en annan bakgrundsbild som ska användas för visning på mobila enheter.

- **[!UICONTROL Background Size]** - Ange det här alternativet för att bestämma hur bakgrundsbilden ska skalförändras i förhållande till banderollens bredd:

  | Alternativ | Beskrivning |
  | ------ | ----------- |
  | `Cover` | Bakgrundsbilden täcker banderollens hela bredd. |
  | `Contain` | Bakgrundsbilden är begränsad till innehållsområdets bredd. |
  | `Auto` | Använder storleken från den aktuella formatmallen. |

  {style="table-layout:auto"}

  ![Bakgrundsstorlek](./assets/pb-layout-row-settings-background-size-cover.png){width="200"}

- **[!UICONTROL Background Position]** - Ange det här alternativet för att bestämma hur bakgrundsbilden är förankrad i förhållande till banderollen:

  | Ankarpunkt | Positioner |
  | ------ | ----------- |
  | `Top` | Vänster / Mitten / Höger |
  | `Center` | Vänster / Mitten / Höger |
  | `Bottom` | Vänster / Mitten / Höger |

  {style="table-layout:auto"}

  Fästpunkten är som ett push-stift som fäster bilden vid banderollen vid den angivna bakgrundspositionen.

- **[!UICONTROL Background Attachment]** - Ange bilagetypen för att bestämma hur bakgrundsbilden flyttas i relation till rullningssidan:

  | Alternativ | Beskrivning |
  | ------ | ----------- |
  | `Scroll` | Den bifogade bakgrundsbilden synkroniseras så att den flyttas nedåt när sidan rullas. |
  | `Fixed` | (Inte tillgängligt för mobiler) Bakgrundsbilden flyttas inte när behållaren rullas över bilden och är fast vid den angivna bakgrundspositionen. |

  {style="table-layout:auto"}

- **[!UICONTROL Background Repeat]** - Om du vill upprepa bakgrundsbilden för att fylla utrymmet ändrar du den här inställningen `Yes`.

### Inställningar för videotyp

Om du anger _[!UICONTROL Background Type]_till `Video`använder du följande inställningar för att definiera hur bakgrundsbilden ska visas.

- **[!UICONTROL Video URL]** - Ange en giltig video-URL. Giltiga video-URL:er kan vara länkar till:

   - YouTube videofilmer: `https://youtu.be/CoDhMRUUjeI`
   - Vimeo-videor: `https://vimeo.com/190156113`
   - Giltiga videofiler (`.mp4` rekommenderas): `https://myvideos.com/spiral.mp4`

  ![URL för bakgrundsvideo](./assets/pb-video-url.png){width="200"}

- **[!UICONTROL Overlay Color]** - Välj en färg som du vill använda en genomskinlig färgton på videon.

- **[!UICONTROL Infinite Loop]** - Ange som `No` för att få videon att spelas upp en gång och stoppa. När den är inställd på `Yes` (standard) upprepas videon i en oändlig slinga.

- **[!UICONTROL Lazy Load]** - Ange som `No` för att göra så att videon läses in med sidan, även när den inte syns. När den är inställd på `Yes` (standard) läses videon bara in från källan när den visas på skärmen.

- **[!UICONTROL Play Only When Visible]** - Ange som `No` för att få videon att börja spelas upp omedelbart efter att den har lästs in, oavsett om den är synlig eller inte. När den är inställd på `Yes` (standard) spelas videon bara upp när den är synlig.

- **[!UICONTROL Fallback Image]** - Om det behövs anger du en bild som ska visas på skärmen innan videon läses in och om videon inte läses in av någon anledning.

## [!UICONTROL Content]

Du kan ändra banderollinnehållet direkt på scenen eller när du ändrar inställningarna. Inställningarna innehåller mer komplexa innehållsfunktioner, som bannerlänkar, knappar och övertäckningar. Innehållets position återspeglar [Utseende](#appearance) placeringsinställning.

### Enkelt innehåll på scenen

1. Klicka på platshållartexten och ange den text som du vill ska visas på banderollen.

   Redigeringsverktygsfältet visas ovanför textrutan.

   ![Redigera innehåll på scenen](./assets/pb-tutorial1-banner-stage-text.png){width="600" zoomable="yes"}

1. Använd redigerarens verktygsfält för att ange och formatera text samt infoga element som länkar, bilder och widgetar.

   ![Scen med formaterad text](./assets/pb-tutorial1-banner-stage-text-format-line2.png){width="600" zoomable="yes"}

### Komplext innehåll i inställningarna

1. Håll pekaren över banderollbehållaren för att visa verktygslådan och välj _Inställningar_ ( ![Ikonen Inställningar](./assets/pb-icon-settings.png){width="25"} ).

1. Bläddra nedåt till _[!UICONTROL Content]_-avsnittet och använd **[!UICONTROL Message Text]**för att ange och formatera bannertext.

   Du kan också infoga element, till exempel textlänkar, bilder och widgetar.

   ![Meddelandetextredigerare](./assets/pb-tutorial1-banner-settings-content-message-text.png){width="600" zoomable="yes"}

1. Ange vid behov en **[!UICONTROL Link]** för bannern.

   Länken är den målsida som visas när kunden klickar på banderollknappen eller området. Du kan använda en av tre länktyper:

   - **[!UICONTROL URL]** - Länkar till en relativ eller fullständig URL-adress.
   - **[!UICONTROL Product]** - Identifierar målsidan baserat på produktnamnet eller SKU:n. Sök efter produkten efter namn baserat på antingen ett partiellt eller fullständigt namn. Välj produkten i sökresultatlistan.
   - **[!UICONTROL Category]** - Identifierar målsidan som en specifik kategori eller underkategori i kategoriträdet. Sök efter kategorin utifrån antingen ett helt eller delvis namn. Välj kategori i det utökade avsnittet i det visade trädet.
   - **[!UICONTROL Page]** - Identifierar målsidan som en specifik innehållssida. Sök efter sidan baserat på ett helt eller delvis namn. Välj sidan i sökresultatlistan.

   >[!NOTE]
   >
   >Från och med version 2.4.1, [!DNL Page Builder] stöder inte längre länkning av banderollen och länkar i den kapslade texten på grund av problem med visningen i butiken. Om du använder en länk i _[!UICONTROL Message Text]_kan du inte konfigurera_[!UICONTROL Link]_ alternativ. Om du föredrar att använda en enda länk för hela banderollen kan du ta bort alla länkar från texten.<br/>
   >
   >![Länkkonfigurationen har blockerats](./assets/pb-nested-link-blocked.png){width="200"}


1. Om det behövs lägger du till en knapp som uppmanar kunderna att följa länken.

   Inställningen för banderollutseende placerar en enda länk eller knapp under texten. Fyll i egenskaperna för länken eller knappen som du vill lägga till.

   ![Utseende med text och knapp (eller länk)](./assets/pb-tutorial1-row-banner-settings-appearance-collage-right.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Du kan också använda flera knappar eller länkar genom att lägga till en [block](block.md) till bannern. För att undvika konflikter ska du behålla alla länkar eller knappar i det separata blocket och inte lägga till en länk eller knapp direkt i banderollen.

   - Ange **[!UICONTROL Show Button]** till något av följande:

     | Alternativ | Beskrivning |
     | ------ | ----------- |
     | `Always` | En knapp visas alltid på banderollen. |
     | `On Hover` | En knapp visas bara på banderollen när du hovrar. |
     | `Never Show` | En knapp visas aldrig på banderollen. |

     {style="table-layout:auto"}

   - Ange **[!UICONTROL Button Text]** för att visas på knappen.

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

   Du kan använda en övertäckning för att använda en bakgrundsfärg på det aktiva innehållsområdet som definieras av [!UICONTROL Appearance] inställning. Banderollens bakgrundsbild är fortfarande synlig för banderollens hela bredd.

   Om du väljer att visa en övertäckning anger du **[!UICONTROL Overlay Color]**:

   - Klicka på **Ingen färg** och välj en färgruta.
   - I **Ingen färg** anger du ett giltigt färgnamn eller ett hexadecimalt värde.

   ![Övertäckningsfärg](./assets/pb-tutorial1-banner-settings-overlay-color.png){width="600" zoomable="yes"}

1. Klicka på i det övre högra hörnet **[!UICONTROL Save]** för att använda inställningarna och gå tillbaka till [!DNL Page Builder] arbetsyta.

   ![Banderoll med textmeddelande och knapp](./assets/pb-tutorial1-banner-stage-background-color.png){width="600" zoomable="yes"}


## [!UICONTROL Search Engine Optimization] {#seo}

Texten för de här inställningarna visas för sökmotorer och förbättrar indexeringen av sidan.

- För **[!UICONTROL Alternative Text]**, ange en _alt_ textbeskrivning för de digitala tillgänglighetsverktygen som ska visas.

  Alternativtext är en god hjälpmedelspraxis och krävs enligt lag i vissa språkområden. I HTML `alt` är en delmängd av `image` tagg: `<image title="tooltip" alt="description" src="image.jpg">`.

- För **[!UICONTROL Title Attribute]** anger du den text som ska visas som ett verktygstips när du för musen över.

  Det bästa sättet är att välja en beskrivande, nyckelordsrik titel som förbättrar hur bilden indexeras av sökmotorer. I HTML `title` är en delmängd av `image` tagg: `<image title="tooltip" alt="description" src="image.jpg">`.

## [!UICONTROL Advanced]

1. Om du vill styra den vågräta placeringen av innehållsbehållare som läggs till i banderollen väljer du en **[!UICONTROL Alignment]**:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | `Default` | Använder den standardinställning för justering som anges i formatmallen för det aktuella temat. |
   | `Left` | Justerar innehållsbehållarna längs den vänstra kanten av banderollbehållaren, med hänsyn till eventuell utfyllnad som har angetts. |
   | `Center` | Justerar innehållsbehållaren i mitten av banderollbehållaren, med hänsyn till eventuell utfyllnad som har angetts. |
   | `Right` | Justerar innehållsbehållaren längs banderollbehållarens högra kant, med hänsyn tagen till eventuell utfyllnad som har angetts. |

   {style="table-layout:auto"}

1. Ange **[!UICONTROL Border]** format som används på alla fyra sidorna av banderollbehållaren:

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

   - **[!UICONTROL Border Color]** - Ange färgen genom att välja en färgruta, klicka på färgväljaren eller genom att ange ett giltigt färgnamn eller motsvarande hexadecimalt värde.

     ![Kantfärg](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

   - **[!UICONTROL Border Width]** - Ange antalet pixlar för kantlinjens bredd.

   - **[!UICONTROL Border Radius]** - Ange antalet pixlar för att definiera radiens storlek som används för att runda varje hörn av kanten.

1. (Valfritt) Ange namnen på **[!UICONTROL CSS classes]** från den aktuella formatmallen som ska användas för banderollbehållaren.

   Avgränsa flera klassnamn med blanksteg.

1. Ange värden i pixlar för **[!UICONTROL Margins and Padding]** om du vill ange banderollens yttre marginaler och inre utfyllnad.

   Ange varje motsvarande värde i bannerbehållardiagrammet.

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | [!UICONTROL Margins] | Mängden tomt utrymme som används på ytterkanten på behållarens alla sidor. |
   | [!UICONTROL Padding] | Mängden tomt utrymme som används på behållarens inre kant på alla sidor. |

   {style="table-layout:auto"}
