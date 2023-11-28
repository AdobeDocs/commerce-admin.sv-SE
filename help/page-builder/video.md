---
title: Media - video
description: Läs mer om videoinnehållstypen som används för att lägga till en video som finns på YouTube eller Vimeo i [!DNL Page Builder] stage.
exl-id: 9cd075e7-c10d-4c34-8932-c1ccb32bf198
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '935'
ht-degree: 0%

---

# Media - video

Använd _Video_ innehållstyp för att lägga till en video som finns på [YouTube][1] eller [Vimeo][2] till [[!DNL Page Builder] stage](workspace.md#stage). Det är enkelt att bädda in video på en sida eller i ett block eller i beskrivningar av produkter och kategorier.

![Video på butikens startsida](./assets/pb-storefront-video.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Videoverktygslåda

![Videoverktygslåda](./assets/pb-media-video-toolbox.png){width="600" zoomable="yes"}

| Verktyg | Ikon | Beskrivning |
|--- |--- |--- |
| Flytta | ![Ikonen Flytta](./assets/pb-icon-move.png){width="25"} | Flyttar videon till en annan plats på scenen. |
| (etikett) | [!UICONTROL Video] | Identifierar den aktuella innehållsbehållaren som en video. Håll pekaren över bildbehållaren för att visa verktygslådan. |
| Inställningar | ![Ikonen Inställningar](./assets/pb-icon-settings.png){width="25"} | Öppnar _[!UICONTROL Edit Video]_sidan där du kan ändra egenskaperna för videon och behållaren. |
| Dölj | ![Dölj ikon](./assets/pb-icon-hide.png){width="25"} | Döljer den aktuella videon. |
| Visa | ![Visa ikon](./assets/pb-icon-show.png){width="25"} | Visar den dolda videon. |
| Duplicera | ![Duplicera, ikon](./assets/pb-icon-duplicate.png){width="25"} | Skapar en kopia av videon. |
| Ta bort | ![Ikonen Ta bort](./assets/pb-icon-remove.png){width="25"} | Tar bort videon från scenen. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Lägga till en video

1. Navigera till [YouTube][1] eller [Vimeo][2] video som du vill bädda in och kopiera länken.

   Du kan också kopiera en direktlänk till en giltig videofil. Se [Grundläggande videoinställningar](#basic-video-settings) för giltiga länkar.

1. I [!DNL Commerce] Admin, gå tillbaka till [!DNL Page Builder] på arbetsytan där du vill lägga till videon.

1. I [!DNL Page Builder] panel, expandera **[!UICONTROL Media]** och dra en **[!UICONTROL Video]** platshållare till scenen.

   ![Dra en videoplatshållare till scenen](./assets/pb-media-video-drag.png){width="600" zoomable="yes"}

1. Håll pekaren över videobehållaren för att visa verktygslådan och välj _Inställningar_ ( ![Ikonen Inställningar](./assets/pb-icon-settings.png){width="20"} ).

1. För **[!UICONTROL Video URL]** klistrar du in URL-adressen till videon som du kopierade.

   URL:en för [!DNL Page Builder] videon som används i det här exemplet är: `https://www.youtube.com/watch?v=Y0KNS7C5dZA`.

1. Begränsa **[!UICONTROL Maximum Width]** för videon anger du den maximala bredden i pixlar.

   Om det är tomt är videon så bred som behållaren tillåter, vilket ger marginaler och utfyllnad.

1. Klicka på i det övre högra hörnet **[!UICONTROL Save]** för att använda inställningarna och gå tillbaka till [!DNL Page Builder] arbetsyta.

## Ändra videoinställningar

1. Håll pekaren över videobehållaren för att visa verktygslådan och välj _Inställningar_ ( ![Ikonen Inställningar](./assets/pb-icon-settings.png){width="20"} ).

1. Ändra inställningarna enligt följande avsnitt:

   - [Grundläggande](#basic-video-settings)
   - [Avancerat](#advanced)

1. Klicka på i det övre högra hörnet **[!UICONTROL Save]** för att använda inställningarna och gå tillbaka till [!DNL Page Builder] arbetsyta.

### Grundläggande videoinställningar

1. Om du vill ändra aktuell video uppdaterar du **[!UICONTROL Video URL]**.

   Ange en giltig video-URL. Giltiga video-URL:er kan vara länkar till:

   - YouTube videofilmer: `https://youtu.be/CoDhMRUUjeI`
   - Vimeo-videor: `https://vimeo.com/190156113`
   - Giltiga videofiler (`.mp4` rekommenderas): `https://myvideos.com/spiral.mp4`

1. Om du vill ändra bredden som tillåts för videon i butiken anger du den nya **[!UICONTROL Maximum Width]** i pixlar.

   Om det är tomt utökas behållarens hela bredd med mindre utrymme för marginaler och utfyllnad.

1. Om du vill starta videon automatiskt när sidan har lästs in anger du **[!UICONTROL Autoplay]** till `Yes`.

   Om Autoplay är inställt på `Yes`, stängs videon av vid uppspelning enligt en princip. Men även med den här inställningen kan mobila enheter inte spela upp videoklipp automatiskt. Mer information om dessa principer finns i följande utvecklarresurser:

   - [Spela upp automatiskt från Vimeo](https://vimeo.zendesk.com/hc/en-us/articles/115004485728-Autoplaying-and-looping-embedded-videos)
   - [Princip för automatisk uppspelning från Google (Chrome/YouTube)](https://developer.chrome.com/blog/autoplay/)
   - [Princip för automatisk uppspelning av lokala videor](https://developer.mozilla.org/en-US/docs/Web/Media/Autoplay_guide)

   Om Autoplay är inställt på `No`spelas videon endast upp på användarens begäran.

### [!UICONTROL Advanced]

1. Om du vill styra videofilens vågräta placering i behållaren väljer du en **[!UICONTROL Alignment]**:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | `Default` | Använder den standardinställning för justering som anges i formatmallen för det aktuella temat. |
   | `Left` | Justerar innehållet längs videobehållarens vänstra kant, med hänsyn tagen till eventuell utfyllnad som har angetts. |
   | `Center` | Justerar innehållet i mitten av videobehållaren, med hänsyn till eventuell utfyllnad som har angetts. |
   | `Right` | Justerar innehållet längs videobehållarens högra kant, med hänsyn tagen till eventuell utfyllnad som har angetts. |

   {style="table-layout:auto"}

- Ange **[!UICONTROL Border]** format som används på videobehållarens alla fyra sidor:

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

- Om du anger ett annat kantlinjeformat än `None`slutför du visningsalternativen för kantlinjer:

  ![Kantfärg](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

  | Alternativ | Beskrivning |
  | ------ |------------ |
  | [!UICONTROL Border Color] | Ange färgen genom att välja en färgruta, klicka på färgväljaren eller genom att ange ett giltigt färgnamn eller motsvarande hexadecimalt värde. |
  | [!UICONTROL Border Width] | Ange antalet pixlar för kantlinjens bredd. |
  | [!UICONTROL Border Radius] | Ange antalet pixlar för att definiera radiens storlek som används för att runda varje hörn av kanten. |

  {style="table-layout:auto"}

- (Valfritt) Ange namnen på **[!UICONTROL CSS classes]** från den aktuella formatmallen som ska användas för videobehållaren.

  Avgränsa flera klassnamn med blanksteg.

- Ange värden i pixlar för **[!UICONTROL Margins and Padding]** för att ange de yttre marginalerna och den inre utfyllnaden för videobehållaren.

  Ange varje motsvarande värde i videobehållardiagrammet.

  | Behållarområde | Beskrivning |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | Mängden tomt utrymme som används på ytterkanten på behållarens alla sidor. |
  | [!UICONTROL Padding] | Mängden tomt utrymme som används på behållarens inre kant på alla sidor. |

  {style="table-layout:auto"}

## Flytta en video

1. Håll pekaren över videobehållaren för att visa verktygslådan och välj _Flytta_ ( ![Ikonen Flytta](./assets/pb-icon-move.png){width="20"} ).

   ![Flytta en video](./assets/pb-media-video-toolbox-move-col1.png){width="500" zoomable="yes"}

1. Markera och dra videon till den nya positionen, precis nedanför den röda stödlinjen.

   ![Placera videon med den röda stödlinjen](./assets/pb-media-video-toolbox-move-col2.png){width="500" zoomable="yes"}

## Ta bort en video från scenen

1. Håll pekaren över videobehållaren för att visa verktygslådan och välj _Ta bort_ (![Ikonen Ta bort](./assets/pb-icon-remove.png)).

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

[1]: https://www.youtube.com/
[2]: https://vimeo.com/
