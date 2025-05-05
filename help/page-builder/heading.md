---
title: Element - rubrik
description: Lär dig mer om innehållstypen Rubrik, som används för att lägga till en textbehållare med en rubriknivå från H1 till H6 på  [!DNL Page Builder] scenen.
exl-id: dc51e7f6-a235-49dc-a978-1419a63fa33e
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# Element - rubrik

Rubriknivåer skapar en hierarki som organiserar innehåll och hjälper sökmotorer att indexera varje sida. Använd innehållstypen _Rubrik_ i [[!DNL Page Builder] scenen](workspace.md#stage) för att lägga till en textbehållare med rubriknivå från H1 till H6 på scenen. Rubriker formateras enligt den formatmall som är kopplad till det aktuella temat.

Fältet [Innehållsrubrik](workspace.md) i avsnittet _[!UICONTROL Content]_&#x200B;kan användas för att lägga till en H1-rubrik högst upp på sidan. Fältet är dock äldre än tidigare [!DNL Commerce] versioner och har stöd för äldre innehåll. Det här fältet utnyttjar inte de avancerade funktionerna i [!DNL Page Builder]. Vi rekommenderar att du lämnar fältet Innehållsrubrik tomt och använder innehållstypen [!DNL Page Builder] Rubrik för att lägga till rubriker på alla nivåer på sidan.

Följande exempel visar hur innehållstypen Innehållsrubrik och Rubrik visas när de formateras med Luma-temat.

![Innehållsrubrik och rubriknivåer på butiken](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

Du kan dra en rubrik från avsnittet _Element_ på panelen [!DNL Page Builder] till en rad, kolumn eller tabbuppsättning på scenen. Rubriknivån och justeringen kan styras från redigeringsverktygsfältet på scenen eller med kontrollen _Inställningar_ ( ![Inställningsikonen](./assets/pb-icon-settings.png){width="20"} ).

{{$include /help/_includes/page-builder-save-timeout.md}}

## Rubrikredigerare

![Rubrikredigeraren med verktygsfältet](./assets/pb-elements-heading-toolbar.png){width="500" zoomable="yes"}

## Verktygslåda för rubrikbehållare

Precis som för alla innehållsbehållare visas verktygslådan när du för muspekaren över behållaren.

![Verktygslådan Rubrikbehållare](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

| Verktyg | Ikon | Beskrivning |
| --------- | ----------------- | ---------------------- |
| Flytta | ![Ikonen Flytta](./assets/pb-icon-move.png){width="25"} | Flyttar rubrikbehållaren till en annan giltig plats på sidan. |
| (etikett) | Rubrik | Identifierar den aktuella behållaren som en rubrik. |
| Inställningar | ![Ikon för inställningar](./assets/pb-icon-settings.png){width="25"} | Öppnar sidan Redigera rubrik, där du kan ändra egenskaperna för behållaren. |
| Dölj | ![Dölj ikon](./assets/pb-icon-hide.png){width="25"} | Döljer rubrikbehållaren. |
| Visa | ![Visa ikon](./assets/pb-icon-show.png){width="25"} | Visar den dolda rubrikbehållaren. |
| Duplicera | ![Duplicera ikon](./assets/pb-icon-duplicate.png){width="25"} | Skapar en kopia av rubrikbehållaren. |
| Ta bort | ![Ikonen Ta bort](./assets/pb-icon-remove.png){width="25"} | Tar bort rubrikbehållaren och dess innehåll från scenen. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Lägg till en rubrik

1. Expandera **[!UICONTROL Elements]** på panelen [!DNL Page Builder] och dra en **[!UICONTROL Heading]** platshållare till en rad, kolumn eller tabb på scenen.

   ![Dra en rubrik till scenen](./assets/pb-elements-heading-drag.png){width="600" zoomable="yes"}

1. Skriv rubriktexten över platshållaren `Edit Heading Text` i redigeraren.

   Som standard tilldelas rubriktexten en rubriktyp på nivå två (H2).

   ![Platshållare i rubrikredigeraren](./assets/pb-elements-header-editor-placeholder.png){width="500" zoomable="yes"}

1. Välj önskad rubriktyp mellan H1 och H6 i verktygsfältet.

1. Ändra justeringen om det behövs.

## Redigera rubrikinställningar

1. Håll pekaren över rubrikbehållaren för att visa verktygslådan och välj ikonen _Inställningar_ ( ![Inställningar-ikon](./assets/pb-icon-settings.png){width="20"} ).

   ![Verktygslådan Rubrik](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

1. Uppdatera rubrikinnehållet (**[!UICONTROL Heading Type]** och **[!UICONTROL Heading Text]**) om det behövs.

   Du kan även uppdatera innehållet i rubrikredigeraren.

1. Uppdatera inställningarna för _[!UICONTROL Advanced]_&#x200B;efter behov.

   - Om du vill styra rubrikens placering i den överordnade behållaren väljer du en **[!UICONTROL Alignment]**:

     | Alternativ | Beskrivning |
     | ------ | ----------- |
     | `Default` | Använder den standardinställning för justering som anges i formatmallen för det aktuella temat. |
     | `Left` | Justerar listan längs den vänstra kanten på den överordnade behållaren, med hänsyn till eventuell utfyllnad som har angetts. |
     | `Center` | Justerar listan i mitten av den överordnade behållaren, med hänsyn till eventuell utfyllnad som har angetts. |
     | `Right` | Justerar blocket längs den högra kanten på den överordnade behållaren, med hänsyn till eventuell utfyllnad som har angetts. |

     {style="table-layout:auto"}

   - Ange formatet **[!UICONTROL Border]** som ska användas på alla fyra sidorna i rubrikbehållaren:

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

   - Om du anger ett annat kantlinjeformat än `None` fyller du i visningsalternativen för kantlinjen:

     | Alternativ | Beskrivning |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Ange färgen genom att välja en färgruta, klicka på färgväljaren eller genom att ange ett giltigt färgnamn eller motsvarande hexadecimalt värde. |
     | [!UICONTROL Border Width] | Ange antalet pixlar för kantlinjens bredd. |
     | [!UICONTROL Border Radius] | Ange antalet pixlar för att definiera radiens storlek som används för att runda varje hörn av kanten. |

     {style="table-layout:auto"}

   - (Valfritt) Ange namnen på **[!UICONTROL CSS classes]** från den aktuella formatmallen som ska användas för behållaren.

     Avgränsa flera klassnamn med blanksteg.

   - Ange värden, i pixlar, för **[!UICONTROL Margins and Padding]** för att bestämma de yttre marginalerna och den inre utfyllnaden för rubrikbehållaren.

     Ange motsvarande värden i diagrammet.

     | Behållarområde | Beskrivning |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Mängden tomt utrymme som används på ytterkanten på behållarens alla sidor. Alternativ: `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | Mängden tomt utrymme som används på behållarens inre kant på alla sidor. Alternativ: `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. När du är klar klickar du på **[!UICONTROL Save]** för att tillämpa inställningarna och återgå till arbetsytan i [!DNL Page Builder].

## Duplicera en rubrik

För en formaterad rubrik med specifika inställningar är det effektivare att duplicera rubriken i stället för att börja om med en ny platshållare.

1. Håll pekaren över rubrikbehållaren för att visa verktygslådan och välj ikonen _Duplicera_ ( ![Duplicera ikon](./assets/pb-icon-duplicate.png){width="20"} ).

   Dupliceringen visas precis nedanför originalet.

   ![Duplicera en rubrikbehållare](./assets/pb-elements-heading-duplicate.png){width="500" zoomable="yes"}

1. Håll pekaren över den nya rubrikbehållaren för att visa verktygslådan och välj ikonen _Flytta_ ( ![Flytta ](./assets/pb-icon-move.png){width="20"} ).

   ![Flytta en rubrik](./assets/pb-elements-heading-move.png){width="500" zoomable="yes"}

1. Markera och dra rubriken tills den röda stödlinjen markerar den nya positionen.

   De övre och nedre kantlinjerna i varje behållare visas som streckade linjer när rubriken flyttas.

   ![Flyttar den duplicerade rubriken till position](./assets/pb-elements-heading-move-guideline.png){width="500" zoomable="yes"}

1. Om du vill ändra rubriknivån klickar du på rubriktexten och väljer den nya nivån i redigeringsverktygsfältet.

   ![Välj en ny rubriknivå](./assets/pb-elements-heading-change-heading-level.png){width="500" zoomable="yes"}
