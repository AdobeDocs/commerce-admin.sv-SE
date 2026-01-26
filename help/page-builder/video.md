---
title: Media - video
description: Lär dig mer om videoinnehållstypen som används för att lägga till en video som finns på YouTube eller Vimeo på  [!DNL Page Builder] scenen.
exl-id: 9cd075e7-c10d-4c34-8932-c1ccb32bf198
feature: Page Builder, Page Content
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# Media - video

Använd innehållstypen _Video_ för att lägga till en video som finns på [YouTube](https://www.youtube.com/) eller [Vimeo](https://vimeo.com/) på [[!DNL Page Builder] scenen](workspace.md#stage). Det är enkelt att bädda in video på en sida eller i ett block eller i beskrivningar av produkter och kategorier.

![Video på butikens startsida](./assets/pb-storefront-video.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Videoverktygslåda

![Verktygslådan Video](./assets/pb-media-video-toolbox.png){width="600" zoomable="yes"}

| Verktyg | Ikon | Beskrivning |
|--- |--- |--- |
| Flytta | ![Ikonen Flytta](./assets/pb-icon-move.png){width="25"} | Flyttar videon till en annan plats på scenen. |
| (etikett) | [!UICONTROL Video] | Identifierar den aktuella innehållsbehållaren som en video. Håll pekaren över bildbehållaren för att visa verktygslådan. |
| Inställningar | ![Ikon för inställningar](./assets/pb-icon-settings.png){width="25"} | Öppnar sidan _[!UICONTROL Edit Video]_, där du kan ändra egenskaperna för videon och behållaren. |
| Dölj | ![Dölj ikon](./assets/pb-icon-hide.png){width="25"} | Döljer den aktuella videon. |
| Visa | ![Visa ikon](./assets/pb-icon-show.png){width="25"} | Visar den dolda videon. |
| Duplicera | ![Duplicera ikon](./assets/pb-icon-duplicate.png){width="25"} | Skapar en kopia av videon. |
| Ta bort | ![Ikonen Ta bort](./assets/pb-icon-remove.png){width="25"} | Tar bort videon från scenen. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Lägga till en video

1. Navigera till [YouTube](https://www.youtube.com/) - eller [Vimeo](https://vimeo.com/) -videon som du vill bädda in och kopiera länken innan du börjar.

   Du kan också kopiera en direktlänk till en giltig videofil. Mer information om giltiga länkar finns i [Grundläggande videoinställningar](#basic-video-settings).

1. Gå tillbaka till arbetsytan [!DNL Commerce] i [!DNL Page Builder]-administratören där du vill lägga till videon.

1. Expandera [!DNL Page Builder] på panelen **[!UICONTROL Media]** och dra en **[!UICONTROL Video]** platshållare till scenen.

   ![Dra en videoplatshållare till scenen](./assets/pb-media-video-drag.png){width="600" zoomable="yes"}

1. Håll pekaren över videobehållaren för att visa verktygslådan och välj ikonen _Inställningar_ ( ![Inställningar-ikon](./assets/pb-icon-settings.png){width="20"} ).

1. För **[!UICONTROL Video URL]** klistrar du in URL-adressen för videon som du kopierade.

   URL:en för videon [!DNL Page Builder] som används i det här exemplet är: `https://www.youtube.com/watch?v=Y0KNS7C5dZA`.

1. Om du vill begränsa **[!UICONTROL Maximum Width]** för videon anger du den maximala bredden i pixlar.

   Om det är tomt är videon så bred som behållaren tillåter, vilket ger marginaler och utfyllnad.

1. Klicka på **[!UICONTROL Save]** i det övre högra hörnet för att tillämpa inställningarna och återgå till arbetsytan i [!DNL Page Builder].

## Ändra videoinställningar

1. Håll pekaren över videobehållaren för att visa verktygslådan och välj ikonen _Inställningar_ ( ![Inställningar-ikon](./assets/pb-icon-settings.png){width="20"} ).

1. Ändra inställningarna enligt följande avsnitt:

   - [Grundläggande](#basic-video-settings)
   - [Avancerat](#advanced)

1. Klicka på **[!UICONTROL Save]** i det övre högra hörnet för att tillämpa inställningarna och återgå till arbetsytan i [!DNL Page Builder].

### Grundläggande videoinställningar

1. Uppdatera **[!UICONTROL Video URL]** om du vill ändra den aktuella videon.

   Ange en giltig video-URL. Giltiga video-URL:er kan vara länkar till:

   - YouTube-videofilmer: `https://youtu.be/CoDhMRUUjeI`
   - Vimeo-videofilmer: `https://vimeo.com/190156113`
   - Giltiga videofiler (`.mp4` rekommenderas): `https://myvideos.com/spiral.mp4`

1. Om du vill ändra bredden som tillåts för videon i butiken anger du den nya **[!UICONTROL Maximum Width]** i pixlar.

   Om det är tomt utökas behållarens hela bredd med mindre utrymme för marginaler och utfyllnad.

1. Om du vill starta videon automatiskt när sidan har lästs in anger du **[!UICONTROL Autoplay]** till `Yes`.

   Om Autoplay är inställt på `Yes` stängs videon av vid uppspelning enligt principen. Men även med den här inställningen kan mobila enheter inte spela upp videoklipp automatiskt. Mer information om dessa principer finns i följande utvecklarresurser:

   - [Princip för automatisk uppspelning från Vimeo](https://vimeo.zendesk.com/hc/en-us/articles/115004485728-Autoplaying-and-looping-embedded-videos)
   - [Princip för automatisk uppspelning från Google (Chrome/YouTube)](https://developer.chrome.com/blog/autoplay/)
   - [Princip för automatisk uppspelning av lokala videor](https://developer.mozilla.org/en-US/docs/Web/Media/Autoplay_guide)

   Om Autoplay är inställt på `No` spelas videon endast upp på användarens begäran.

### [!UICONTROL Advanced]

1. Om du vill styra den vågräta placeringen av videon i behållaren väljer du en **[!UICONTROL Alignment]**:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | `Default` | Använder den standardinställning för justering som anges i formatmallen för det aktuella temat. |
   | `Left` | Justerar innehållet längs videobehållarens vänstra kant, med hänsyn tagen till eventuell utfyllnad som har angetts. |
   | `Center` | Justerar innehållet i mitten av videobehållaren, med hänsyn till eventuell utfyllnad som har angetts. |
   | `Right` | Justerar innehållet längs videobehållarens högra kant, med hänsyn tagen till eventuell utfyllnad som har angetts. |

   {style="table-layout:auto"}

- Ange formatet **[!UICONTROL Border]** som ska användas på alla fyra sidor i videobehållaren:

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

- (Valfritt) Ange namnen på **[!UICONTROL CSS classes]** från den aktuella formatmallen som ska användas för videobehållaren.

  Avgränsa flera klassnamn med blanksteg.

- Ange värden (i pixlar) för **[!UICONTROL Margins and Padding]** för att ange de yttre marginalerna och den inre utfyllnaden för videobehållaren.

  Ange varje motsvarande värde i videobehållardiagrammet.

  | Behållarområde | Beskrivning |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | Mängden tomt utrymme som används på ytterkanten på behållarens alla sidor. |
  | [!UICONTROL Padding] | Mängden tomt utrymme som används på behållarens inre kant på alla sidor. |

  {style="table-layout:auto"}

## Flytta en video

1. Håll pekaren över videobehållaren för att visa verktygslådan och välj ikonen _Flytta_ ( ![Flytta ](./assets/pb-icon-move.png){width="20"} ).

   ![Flytta en video](./assets/pb-media-video-toolbox-move-col1.png){width="500" zoomable="yes"}

1. Markera och dra videon till den nya positionen, precis nedanför den röda stödlinjen.

   ![Använda den röda stödlinjen för att placera videon](./assets/pb-media-video-toolbox-move-col2.png){width="500" zoomable="yes"}

## Ta bort en video från scenen

1. Håll pekaren över videobehållaren för att visa verktygslådan och välj ikonen _Ta bort_ (![Ta bort ikon](./assets/pb-icon-remove.png)).

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.


<!-- Last updated from includes: 2023-09-11 14:30:19 -->
