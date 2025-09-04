---
title: Lägg till innehåll - blockera
description: Lär dig mer om blockinnehållstypen som används för att lägga till ett återanvändbart block på  [!DNL Page Builder] scenen.
exl-id: fcedb125-e0c8-4b59-bd26-7f3912e0db2a
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Lägg till innehåll - blockera

Använd innehållstypen _Block_ för att lägga till ett befintligt, aktivt [block](../content-design/blocks.md) på [[!DNL Page Builder] scenen](workspace.md#stage). I följande exempel innehåller den första kolumnen blocket med en sidmeny för sidan. Den andra kolumnen innehåller en bild.

![Blockera med en sidmeny](./assets/pb-add-content-block-example.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Blockera verktygslåda

| Verktyg | Ikon | Beskrivning |
| --------- | -------- | ------------- |
| Flytta | ![Ikonen Flytta](./assets/pb-icon-move.png) | Flyttar blockbehållaren och dess innehåll till en annan plats på scenen. |
| Inställningar | ![Ikon för inställningar](./assets/pb-icon-settings.png) | Öppnar sidan Redigera block, där du kan välja blocket och ändra egenskaperna för behållaren. |
| Dölj | ![Dölj ikon](./assets/pb-icon-hide.png) | Döljer den aktuella blockbehållaren och dess innehåll. |
| Visa | ![Visa ikon](./assets/pb-icon-show.png) | Visar den dolda blockbehållaren och dess innehåll. |
| Duplicera | ![Duplicera ikon](./assets/pb-icon-duplicate.png) | Skapar en kopia av blockbehållaren och dess innehåll. |
| Ta bort | ![Ikonen Ta bort](./assets/pb-icon-remove.png) | Tar bort blockbehållaren och dess innehåll från scenen. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Lägg till ett befintligt block

1. Navigera till arbetsytan [!DNL Page Builder] på målsidan, blocket, det dynamiska blocket, produkten eller kategorin.

1. Expandera [!DNL Page Builder] på panelen **[!UICONTROL Add Content]** och dra en **[!UICONTROL Block]** platshållare till scenen.

   ![Dra ett block till scenen](./assets/pb-add-content-block-drag.png){width="600" zoomable="yes"}

1. Håll pekaren över den tomma blockbehållaren för att visa verktygslådan och välj ikonen _Inställningar_ ( ![Inställningar-ikon](./assets/pb-icon-settings.png){width="25"} ).

1. Klicka på **[!UICONTROL Select Block]**.

   ![Markera ett block](./assets/pb-add-content-block-select.png){width="200"}

1. Klicka på **[!UICONTROL Select]** i den sista kolumnen i det block som du vill lägga till.

   ![Markerat block](./assets/pb-add-content-block-selected.png){width="600" zoomable="yes"}

   Namnet på det markerade blocket visas på sidan.

   ![Blocknamn](./assets/pb-add-content-block-name.png){width="200"}

1. Fyll i återstående inställningar efter behov och använd fältbeskrivningarna i slutet av den här sidan som referens.

1. När du är klar klickar du på **[!UICONTROL Save]** för att tillämpa inställningarna och återgå till arbetsytan i [!DNL Page Builder].

### Avancerade inställningar

1. Om du vill styra blockets placering i den överordnade behållaren väljer du en **[!UICONTROL Alignment]**:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | `Default` | Använder den standardinställning för justering som anges i formatmallen för det aktuella temat. |
   | `Left` | Justerar listan längs den vänstra kanten på den överordnade behållaren, med hänsyn till eventuell utfyllnad som har angetts. |
   | `Center` | Justerar listan i mitten av den överordnade behållaren, med hänsyn till eventuell utfyllnad som har angetts. |
   | `Right` | Justerar blocket längs den högra kanten på den överordnade behållaren, med hänsyn till eventuell utfyllnad som har angetts. |

   {style="table-layout:auto"}

1. Ange ett **[!UICONTROL Border]**-format som ska användas på alla fyra sidor i blockbehållaren:

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

1. Om du anger ett annat kantlinjeformat än `None` fyller du i visningsalternativen för kantlinjen:

   | Alternativ | Beskrivning |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Ange färgen genom att välja en färgruta, klicka på färgväljaren eller genom att ange ett giltigt färgnamn eller motsvarande hexadecimalt värde. |
   | [!UICONTROL Border Width] | Ange antalet pixlar för kantlinjens bredd. |
   | [!UICONTROL Border Radius] | Ange antalet pixlar för att definiera radiens storlek som används för att runda varje hörn av kanten. |

   {style="table-layout:auto"}

1. (Valfritt) Ange namnen på **[!UICONTROL CSS classes]** från den aktuella formatmallen som ska användas för behållaren.

   Avgränsa flera klassnamn med blanksteg.

1. Ange värden, i pixlar, för **[!UICONTROL Margins and Padding]** för att fastställa blockbehållarens yttre marginaler och inre utfyllnad.

   Ange motsvarande värden i diagrammet.

   | Behållarområde | Beskrivning |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | Mängden tomt utrymme som används på ytterkanten på behållarens alla sidor. Alternativ: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Mängden tomt utrymme som används på behållarens inre kant på alla sidor. Alternativ: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

## Redigera blockinställningar

1. Håll pekaren över blockbehållaren och välj ikonen _Inställningar_ ( ![Inställningsikonen](./assets/pb-icon-settings.png){width="25"} ) i verktygslådan.

   ![Blockera verktygslåda](./assets/pb-add-content-block-toolbox.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Select Block]** om du vill välja ett annat block.

   - Klicka på **[!UICONTROL Select]** i listan med aktiva block på det block som du vill lägga till.
   - Klicka på **[!UICONTROL Add Selected]**.

1. Uppdatera de återstående inställningarna efter behov och använd fältbeskrivningarna i slutet av den här sidan som referens.

1. När du är klar klickar du på **[!UICONTROL Save]** för att tillämpa inställningarna och återgå till arbetsytan i [!DNL Page Builder].

## Duplicera ett block

1. Håll pekaren över blockbehållaren för att visa verktygslådan och välj ikonen _Duplicera_ (![Duplicera ikon](./assets/pb-icon-duplicate.png)).

   Dupliceringen visas precis nedanför originalet.

1. Om du vill flytta det nya blocket till en ny plats håller du pekaren över behållaren och klickar sedan på _Flytta_ (![ikonen Flytta](./assets/pb-icon-move.png)) i verktygslådan.

1. Markera och dra blocket tills den röda stödlinjen visas på den nya positionen.

   De övre och nedre kantlinjerna i varje behållare visas som streckade linjer när blocket flyttas.

## Ta bort ett block från scenen

1. Håll pekaren över blockbehållaren för att visa verktygslådan och välj ikonen _Ta bort_ (![Ta bort ikon](./assets/pb-icon-remove.png)).

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
