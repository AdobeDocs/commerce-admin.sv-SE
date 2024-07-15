---
title: Media - bild
description: Lär dig mer om bildinnehållstypen som används för att lägga till en JPG, GIF eller PNG-bild på  [!DNL Page Builder] scenen.
exl-id: 1b8d906e-7570-4c1f-87a0-992400faf55c
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1550'
ht-degree: 0%

---

# Media - bild

Använd innehållstypen _Bild_ om du vill lägga till en JPG, GIF eller PNG-bild på [[!DNL Page Builder] scenen](workspace.md#stage). Förutom standardskrivbordsbilden kan du ange en sekundär bild för mobila enheter. Du kan också lägga till en bildtext som visas under bilden och länka bilden till en URL-adress, produkt, kategori eller sida.

>[!TIP]
>
>Du kan använda [Adobe Stock Integration](../content-design/adobe-stock.md) för att hitta och spara en lämplig resurs bland de miljontals som tillhandahålls av [Adobe Stock](https://stock.adobe.com). Mer information om hur du söker efter, finjusterar och sparar Adobe Stock-resurser i ditt galleri finns i [Använda Adobe Stock-bilder](../content-design/adobe-stock-manage.md) .

{{$include /help/_includes/page-builder-save-timeout.md}}

## Verktygslådan Bild

Verktygslådan för bilden visas när du hovrar över bildbehållaren.

![Verktygslådan Bild](./assets/pb-media-image-giftcard-column-toolbox.png){width="500" zoomable="yes"}

| Verktyg | Ikon | Beskrivning |
|--- |--- |--- |
| Flytta | ![Ikonen Flytta](./assets/pb-icon-move.png){width="25"} | Flyttar bilden till en annan plats på scenen. |
| (etikett) | Bild | Identifierar den aktuella innehållsbehållaren som en bild. Håll pekaren över bildbehållaren för att visa verktygslådan. |
| Inställningar | ![Ikon för inställningar](./assets/pb-icon-settings.png){width="25"} | Öppnar sidan _Redigera bild_ där du kan ändra egenskaperna för bilden och behållaren. |
| Dölj | ![Dölj ikon](./assets/pb-icon-hide.png){width="25"} | Döljer den aktuella bilden. |
| Visa | ![Visa ikon](./assets/pb-icon-show.png){width="25"} | Visar den dolda bilden. |
| Duplicera | ![Duplicera ikon](./assets/pb-icon-duplicate.png){width="25"} | Skapar en kopia av bilden. |
| Ta bort | ![Ikonen Ta bort](./assets/pb-icon-remove.png){width="25"} | Tar bort bilden från scenen. |
| Överför ny bild |  | Överför en bild från det lokala filsystemet till galleriet. |
| Välj från galleri |  | Väljer en befintlig bild från galleriet. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Lägga till en bild

1. Expandera **[!UICONTROL Media]** på panelen [!DNL Page Builder] och dra en **[!UICONTROL Image]** platshållare till målbehållaren.

   Du kan lägga till en bild till en rad, kolumn eller tabb. I följande exempel dras bilden till en tom kolumn.

   ![Dra en bildinnehållstyp till scenen](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

1. Använd någon av följande metoder för att lägga till bildresursen:

   ![Överför bild eller Välj från galleriverktyg på scenen](./assets/pb-media-image-upload-select.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >Den största filstorleken är 4 MB. Filtyper som stöds är JPG, GIF och PNG.

   - _**Överför en ny bild**_: Använd den här metoden om du vill överföra en ny bildfil från datorn.

      - Klicka på **[!UICONTROL Upload Image]**.

      - Leta upp och välj bilden som du vill lägga till i galleriet och målbehållaren.

     Du kan också dra en bildfil från datorn och släppa den på ikonen _Kamera_ ( ![Kameraikon](./assets/pb-icon-camera.png){width="20"} ).

   - _**Välj en befintlig resurs**_: Använd den här metoden om du vill välja en befintlig bildresurs från medielagring/galleri.

      - Klicka på **[!UICONTROL Select from Gallery]**.

      - Använd trädet för att navigera till bilden.

      - Klicka på miniatyrbilden och klicka på **[!UICONTROL Add Selected]**.

        ![Lägger till en markerad bild](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - _**Sök efter och markera en Adobe Stock-bild**_: Använd den här metoden om du vill söka efter en bild från Adobe Stock.

     >[!NOTE]
     >
     >Den här metoden kräver en [Adobe Stock-integrering](../content-design/adobe-stock.md) konfigurerad för din administratör.

      - Klicka på **[!UICONTROL Search Adobe Stock]** och sök efter en bild.

      - Spara förhandsvisningen eller den licensierade bilden i galleriet.

        Mer information om hur du arbetar med Adobe Stock-resurser finns i [Använda Adobe Stock-bilder](../content-design/adobe-stock-manage.md).

      - Välj miniatyrbilden för resursen i galleriet och klicka på **[!UICONTROL Add Selected]**.

   Bilden visas i målbehållaren på platshållarplatsen. Till skillnad från en bakgrundsbild kan du flytta bilden till en annan plats i den aktuella behållaren eller till en annan behållare.

   >[!NOTE]
   >
   >Innehållstyperna [Banner](banner.md) och [Slider](slider.md) innehåller även alternativen _Överför bild_ och _Välj från galleri_ för att lägga till bilder.

   ![Bild i en kolumn](./assets/pb-media-image-column1-giftcard.png){width="500" zoomable="yes"}

## Ändra bildinställningar

1. Håll pekaren över bildbehållaren för att visa verktygslådan och välj ikonen _Inställningar_ (![Inställningar-ikon](./assets/pb-icon-settings.png){width="20"} ).
Filnamnet, dimensionerna och filstorleken visas under den aktuella bilden.

   ![Aktuell bild](./assets/pb-media-image-settings-image.png){width="600" zoomable="yes"}

1. Gör något av följande om du vill ändra aktuell **[!UICONTROL Image]**:

   - _**Överför en ny bild**_: Använd den här metoden om du vill överföra en ny bildfil från datorn.

      - Klicka på **[!UICONTROL Upload Image]**.

      - Leta upp och välj bilden som du vill lägga till i galleriet och målbehållaren.

   - _**Välj en befintlig resurs**_: Använd den här metoden om du vill välja en befintlig bildresurs från medielagring/galleri.

      - Klicka på **[!UICONTROL Select from Gallery]**.

      - Använd trädet för att navigera till bilden.

      - Klicka på miniatyrbilden och klicka på **[!UICONTROL Add Selected]**.

        ![Lägger till en markerad bild](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - **Sök efter och markera en Adobe Stock-bild**: Använd den här metoden om du vill söka efter en bild från Adobe Stock.

     >[!NOTE]
     >
     >Den här metoden kräver en [Adobe Stock-integrering](../content-design/adobe-stock.md) konfigurerad för din administratör.

      - Klicka på **[!UICONTROL Search Adobe Stock]** och sök efter en bild.

      - Spara förhandsvisningen eller den licensierade bilden i galleriet.

        Mer information om hur du arbetar med Adobe Stock-resurser finns i [Använda Adobe Stock-bilder](../content-design/adobe-stock-manage.md).

      - Välj miniatyrbilden för resursen i galleriet och klicka på **[!UICONTROL Add Selected]**.

1. Om du vill lägga till en **[!UICONTROL Mobile Image]** använder du samma metoder som beskrivs i föregående steg för att välja en bild som ska användas för visning på mobila enheter.

   ![Mobilbild](./assets/pb-media-image-settings-mobile-image.png){width="600" zoomable="yes"}

1. Ange vid behov en **[!UICONTROL Link]** för bilden.

   Länken är den målsida som visas när kunden klickar på bilden. Du kan använda en av tre länktyper:

   - **[!UICONTROL URL]** - Länkar till en relativ eller fullständig URL.

   - **[!UICONTROL Product]** - Identifierar målsidan baserat på produktnamnet eller SKU:n. Sök efter produkten efter namn baserat på antingen ett partiellt eller fullständigt namn. Välj produkten i sökresultatlistan.

     ![Välja en produkt som ska länkas](./assets/pb-media-image-settings-image-link-product-results.png){width="600" zoomable="yes"}

   - **[!UICONTROL Category]** - Identifierar målsidan som en specifik kategori eller underkategori i kategoriträdet. Sök efter kategorin utifrån antingen ett helt eller delvis namn. Välj kategori i det utökade avsnittet i det visade trädet.

     ![Välj en kategori att länka](./assets/pb-media-image-settings-image-link-category-tree.png){width="600" zoomable="yes"}

   - **[!UICONTROL Page]** - Identifierar målsidan som en specifik innehållssida. Sök efter sidan baserat på ett helt eller delvis namn. Välj sidan i sökresultatlistan.

     ![Välja en sida som ska länkas](./assets/pb-media-image-settings-image-link-page-results.png){width="600" zoomable="yes"}

   Markera kryssrutan **[!UICONTROL Open in new tab]** om du inte vill att besökaren ska kunna navigera bort från din butik. När kryssrutan är avmarkerad öppnas det länkade målet på samma webbläsarflik, som kan navigera besökaren bort från din butik.

1. Om du vill lägga till en **[!UICONTROL Image Caption]** anger du texten som du vill ska visas under bilden.

   Bildtextens format bestäms av den formatmall som är kopplad till det aktuella temat.

   Bildtexten visas vanligtvis under bilden och ger information om bilden för besökare och sökmotorer. Om webbplatsen finns på flera språk kan du använda samma bild, men översätta bildtexten. I HTML är taggen `<figcaption>` en delmängd av taggen `<figure>`. `<figcaption>This is the image caption</figcaption>`

1. Uppdatera övriga inställningar efter behov:

   - [Sökmotoroptimering](#search-engine-optimization)
   - [Avancerat](#advanced)

1. När du är klar klickar du på **[!UICONTROL Save]** för att tillämpa inställningarna och återgå till arbetsytan i [!DNL Page Builder].

## Flytta en bild

1. Håll pekaren över bildbehållaren för att visa verktygslådan och välj ikonen _Flytta_ (![Flytta ](./assets/pb-icon-move.png){width="20"} ).

   ![Flytta en bild](./assets/pb-media-image-column1-move-giftcard.png){width="500" zoomable="yes"}

1. Markera och dra bilden till den nya positionen, precis nedanför den röda stödlinjen.

   ![Använda den röda stödlinjen för att placera bilden](./assets/pb-media-image-column2-move-giftcard-red-guideline.png){width="500" zoomable="yes"}

## Ta bort en bild

1. Håll pekaren över bildbehållaren för att visa verktygslådan och välj ikonen _Ta bort_ ( ![Ta bort ikon](./assets/pb-icon-remove.png){width="20"} ).

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

## Sökmotoroptimering

Texten för de här inställningarna visas för sökmotorer och förbättrar indexeringen av sidan.

- För **[!UICONTROL Alternative Text]** anger du en _alt_-textbeskrivning för de digitala tillgänglighetsverktygen som ska visas.

  Alternativtext är en god hjälpmedelspraxis och krävs enligt lag i vissa språkområden. I HTML är attributet `alt` en delmängd av taggen `image`: `<image title="tooltip" alt="description" src="image.jpg">`.

- För **[!UICONTROL Title Attribute]** anger du den text som ska visas som ett verktygstips vid muspekaren.

  Det bästa sättet är att välja en beskrivande, nyckelordsrik titel som förbättrar hur bilden indexeras av sökmotorer. I HTML är attributet `title` en delmängd av taggen `image`: `<image title="tooltip" alt="description" src="image.jpg">`.

## [!UICONTROL Advanced]

- Om du vill styra den vågräta placeringen av bilderna som läggs till i behållaren väljer du **[!UICONTROL Alignment]**.

  | Alternativ | Beskrivning |
  | ------ | ----------- |
  | `Default` | Använder den standardinställning för justering som anges i formatmallen för det aktuella temat. |
  | `Left` | Justerar bildinnehållet längs den vänstra kanten av bildbehållaren, med hänsyn till eventuell utfyllnad som har angetts. |
  | `Center` | Justerar bildinnehållet i mitten av bildbehållaren, med hänsyn till eventuell utfyllnad som har angetts. |
  | `Right` | Justerar bildinnehållet längs den högra kanten av bildbehållaren, med hänsyn till eventuell utfyllnad som har angetts. |

  {style="table-layout:auto"}

- Ange det **[!UICONTROL Border]**-format som ska användas på alla fyra sidorna i bildbehållaren:

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

  ![Kantfärg](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

  | Alternativ | Beskrivning |
  | ------ |------------ |
  | [!UICONTROL Border Color] | Ange färgen genom att välja en färgruta, klicka på färgväljaren eller genom att ange ett giltigt färgnamn eller motsvarande hexadecimalt värde. |
  | [!UICONTROL Border Width] | Ange antalet pixlar för kantlinjens bredd. |
  | [!UICONTROL Border Radius] | Ange antalet pixlar för att definiera radiens storlek som används för att runda varje hörn av kanten. |

  {style="table-layout:auto"}

- (Valfritt) Ange namnen på **[!UICONTROL CSS classes]** från den aktuella formatmallen som ska användas i bildbehållaren.

  Avgränsa flera klassnamn med blanksteg.

- Ange värden (i pixlar) för **[!UICONTROL Margins and Padding]** för att ange de yttre marginalerna och den inre utfyllnaden för bildbehållaren.

  Ange varje motsvarande värde i bildbehållardiagrammet.

  | Behållarområde | Beskrivning |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | Mängden tomt utrymme som används på ytterkanten på behållarens alla sidor. |
  | [!UICONTROL Padding] | Mängden tomt utrymme som används på behållarens inre kant på alla sidor. |

  {style="table-layout:auto"}
