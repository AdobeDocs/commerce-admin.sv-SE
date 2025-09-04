---
title: Media - Karta
description: Lär dig mer om innehållstypen för kartan, som används för att lägga till en karta från  [!DNL Google Maps] Plattform på  [!DNL Page Builder] scenen.
exl-id: 91fea8f8-d48a-43f1-ba2a-212c7130cee9
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1571'
ht-degree: 0%

---

# Media - Karta

Använd innehållstypen _Karta_ om du vill lägga till en karta från [[!DNL Google Maps] Plattform][1] på [[!DNL Page Builder] scenen](workspace.md#stage). Du kan till exempel lägga till en karta till ett block och sedan lägga till blocket på sidorna [Om oss](../content-design/pages.md#about-us) och [Kontakta oss](../getting-started/store-details.md#contact-us-form).

Om du vill få ut det mesta av [!DNL Google Maps]-plattformen kan du anpassa kartan, markera dina butiksplatser och använda Google [Platser][2] för att lägga till omfattande information om din butik i alla [!DNL Google Maps] .

## Fördelar med att bädda in en Google-karta

1. Förser köpare med en fullständig mängd information om ditt företag (telefonnummer, webbplats, recensioner, stjärngraderingar och så vidare) direkt på din webbplats.

1. En Google-karta visar oftast närliggande attraktioner, parker, restauranger och så vidare. Den här informationen hjälper dina kunder att fastställa din fysiska plats och planera sin resa.

1. Gör det enkelt för kunderna att hitta adressen till din fysiska butik utan att behöva öppna ett nytt webbläsarfönster och lämna sajten.

1. Om du har en kedja av fysiska butiker kan du genom att lägga till en Google Map på din webbplats öka varumärkeskännedomen och trovärdigheten i form av markerade objekt.

![Exempelarkiv - mappa med plats](./assets/pb-media-maps-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Kartverktygslåda

Kartverktygslådan visas när du hovrar över kartbehållaren.

| Verktyg | Ikon | Beskrivning |
|--- |--- |--- |
| Flytta | ![Ikonen Flytta](./assets/pb-icon-move.png){width="25"} | Flyttar kartan till en annan plats på scenen. |
| (etikett) | [!UICONTROL Map] | Identifierar den aktuella innehållsbehållaren som en karta. Håll pekaren över kartbehållaren för att visa verktygslådan. |
| Inställningar | ![Ikon för inställningar](./assets/pb-icon-settings.png){width="25"} | Öppnar sidan Redigera karta, där du kan ändra egenskaperna för kartan och behållaren. |
| Dölj | ![Dölj ikon](./assets/pb-icon-hide.png){width="25"} | Döljer den aktuella kartan. |
| Visa | ![Visa ikon](./assets/pb-icon-show.png){width="25"} | Visar den dolda kartan. |
| Duplicera | ![Duplicera ikon](./assets/pb-icon-duplicate.png){width="25"} | Skapar en kopia av kartan. |
| Ta bort | ![Ikonen Ta bort](./assets/pb-icon-remove.png){width="25"} | Tar bort kartan från scenen. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Konfigurera [!DNL Google Maps] för din administratör

Innan du lägger till en karta måste du först öppna ett [konto][3] för en kostnadsfri testversion av [!DNL Google Maps] Platform. Den kostnadsfria provperioden varar i 12 månader och inkluderar en kredit på 300 dollar. Om du använder din kredit debiterar Google inte ditt konto utan ditt tillstånd.

### Steg 1: Hämta [!DNL Google Maps] API-nyckeln

Beroende på om du redan har en [!DNL Google Maps]-nyckel kan du använda någon av följande procedurer för att hämta den API-nyckel som krävs för konfigurationen. Om du vill konfigurera en [!DNL Google Maps]-nyckel måste du vara webbplatsadministratör som är behörig att aktivera fakturering för ditt konto. Om du inte är redo att konfigurera ett [!DNL Google Maps]-plattformskonto kan du hoppa över det här steget och använda platshållarkartan för tillfället.

1. Gå till [Google Cloud Platform Console](https://cloud.google.com/console/google/maps-apis/overview).

1. Klicka på listrutan för projektet och välj eller skapa det projekt som du vill lägga till en API-nyckel för.

1. Om du vill konfigurera dina API-autentiseringsuppgifter följer du [instruktionerna][4] i [!DNL Google Maps] -dokumentationen.

1. Kopiera API-nyckeln till Urklipp.

### Steg 2: Konfigurera [!DNL Google Maps] i [!DNL Commerce]

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_&#x200B;Admin **[!UICONTROL Configuration]**.

1. Välj _[!UICONTROL General]_&#x200B;i den vänstra panelen under **[!UICONTROL Content Management]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

   ![Avancerade innehållsverktyg](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   Mer information om konfigurationsalternativen för det avancerade verktyget för innehållshantering finns i [referenshandboken för konfiguration](../configuration-reference/general/content-management.md).

1. För **[!UICONTROL Google Maps API Key]** klistrar du in nyckeln som du kopierade i steg 1.

1. Klicka på **[!UICONTROL Test Key]**.

   Om det är problem med nyckeln går du tillbaka till [!DNL Google Maps]-plattformen för att lösa problemet. Försök sedan igen.

1. När nyckeln har verifierats klickar du på **[!UICONTROL Save Config]**.

## Lägga till en karta på scenen

1. Öppna sidan, blocket eller det dynamiska blocket på arbetsytan för [!DNL Page Builder].

1. Expandera [!DNL Page Builder] på panelen **[!UICONTROL Media]** och dra en **[!UICONTROL Map]** platshållare till scenen.

   ![Dra en karta till scenen](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   Om [!DNL Google Maps]-plattformen är konfigurerad för din butik visas en karta för din butiksplats.

   ![[!DNL Google Maps]](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   Om [!DNL Google Maps]-plattformen ännu inte har konfigurerats för din butik visas en platshållarkarta i stället.

   ![[!DNL Google Maps] Platshållare ](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

## Lägg till en anpassad mappningsplats

1. Håll pekaren över kartbehållaren för att visa verktygslådan och välj ikonen _Inställningar_ ( ![Inställningsikonen](./assets/pb-icon-settings.png){width="20"} ).

1. Klicka på _[!UICONTROL Edit Map]_&#x200B;i det övre högra hörnet på sidan **[!UICONTROL Add Location]**.

1. Ange **[!UICONTROL Location Name]** som du vill ska kopplas till stiftet på kartan.

1. Samla de platskoordinater som du vill använda för den anpassade platsen.

   I rutan **[!UICONTROL Position]** kan du också dra stiftet på den visade kartan.

   Om det behövs går du till [[!DNL Google Maps]][5] i ett nytt webbläsarfönster och använder någon av följande metoder för att hämta koordinaterna:

   ![Mappningskoordinater](./assets/pb-media-maps-settings-add-location-coordinates.png){width="600" zoomable="yes"}

   **Metod 1:** Kopiera från URL

   - I det övre vänstra hörnet anger du adressen i rutan **[!UICONTROL Search]** och klickar på ikonen _Sök_ ( ![ikonen Sök](../assets/icon-magnify-search.png){width="20"} ).

   - Kopiera koordinaterna i URL:en och klistra in dem i en anteckningsruta.

   **Metod 2:** Kopiera från &quot;Vad finns här?&quot;

   - Högerklicka på det röda stiftet som markerar platsen på kartan och välj **[!UICONTROL What's here?]** på menyn.

   - I den visade etiketten kopierar du texten, inklusive koordinaterna, och klistrar in texten i en anteckningsruta.

1. Ange siffrorna, utan kommatecken, i var och en av **[!UICONTROL Coordinates]**-rutorna.

   Du kan också ange så mycket av den återstående informationen som du vill ska vara tillgänglig på kartan.

1. Komprimera all annan information som du vill associera med kartplatsen:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | [!UICONTROL Phone Number] | Telefonnumret till platsen. |
   | [!UICONTROL Street Address] | Platsens gatuadress. |
   | [!UICONTROL City] | Platsens stad. |
   | [!UICONTROL Region/State] | Platsens region eller tillstånd. |
   | [!UICONTROL Zip/Postal Code] | Platsens postnummer. |
   | [!UICONTROL Country] | Landet där platsen finns. |
   | [!UICONTROL Comment] | Alla kommentarer som du vill ta med. |

   {style="table-layout:auto"}

1. Klicka på **[!UICONTROL Save]** när du är klar.

   Den nya platsen visas på kartan och i kartpositionens rutnät på sidan _[!UICONTROL Edit Map]_.

   ![[!DNL Page Builder] - mappar platsens rutnät ](./assets/pb-media-maps-settings-add-location-grid.png){width="600" zoomable="yes"}

## Formatera kartan {#styling}

Använd guiden [!DNL Google Maps] för plattformsformat för att tillämpa ett av sex fördefinierade teman eller för att skapa ett anpassat tema. Du kan generera en JSON-fil med mappningsformategenskaperna eller en länk till den formaterade kartan.

### Ändra kartformatet

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_&#x200B;Admin **[!UICONTROL Configuration]**.

1. Välj _[!UICONTROL General]_&#x200B;i den vänstra panelen under **[!UICONTROL Content Management]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. Klicka på **[!UICONTROL Google Maps Style]** Skapa kartformat[ i textrutan ][6].

   Den här åtgärden öppnar guiden [[!DNL Google Maps] Plattformsformat][6] på en separat flik, där du kan definiera en stil för [!DNL Google Maps]-plattformsprojektet.

1. Klicka på **[!UICONTROL Create a Style]** och följ instruktionerna.

   Klicka på **[!UICONTROL Finish]** när du är klar.

1. Exportera det färdiga formatet som JSON-kod eller som en URL så att du kan lägga till det i konfigurationen [!DNL Commerce].

   - **JSON**: Klicka **[!UICONTROL Copy JSON]** nedanför rutan med den genererade JSON-koden.

   - **[!UICONTROL URL]**: Klicka **[!UICONTROL Copy URL]** nedanför rutan med den genererade URL:en.

1. Gå tillbaka till webbläsarfliken för din administratör och klistra in den genererade koden eller URL:en i rutan **Google Maps Style** .

   Om du använder en URL ersätter du platshållaren `YOUR_API_KEY` med API-nyckeln för [!DNL Google Maps]. Den här URL:en länkar till din formaterade Google Map.

1. Klicka på **[!UICONTROL Save Config]** i det övre högra hörnet.

### Ändra kartinställningar

1. Hovra över kartbehållaren för att visa verktygslådan och välj ikonen _Inställningar_ ( ![Inställningsikonen](./assets/pb-icon-settings.png){width="20"} ).

1. Ändra de grundläggande inställningarna efter behov:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | [!UICONTROL Height] | Anger höjden på det visade schemat i pixlar. |
   | [!UICONTROL Show Controls] | Anger om standardkontrollerna för Google Map visas. |

   {style="table-layout:auto"}

1. Ändra inställningarna för _[!UICONTROL Advanced]_&#x200B;efter behov:

   - Om du vill styra den vågräta placeringen av kartinnehållet som har lagts till i behållaren väljer du en **[!UICONTROL Alignment]**:

     | Alternativ | Beskrivning |
     | ------ | ----------- |
     | `Default` | Använder den standardinställning för justering som anges i formatmallen för det aktuella temat. |
     | `Left` | Justerar innehållet längs kartbehållarens vänstra kant, med hänsyn till eventuell utfyllnad som har angetts. |
     | `Center` | Justerar innehållet i mitten av kartbehållaren, med hänsyn till eventuell utfyllnad som har angetts. |
     | `Right` | Justerar innehållet längs kartbehållarens högra kant, med hänsyn till eventuell utfyllnad som har angetts. |

     {style="table-layout:auto"}

   - Ange det **[!UICONTROL Border]**-format som ska användas på alla fyra sidor i kartbehållaren:

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

   - (Valfritt) Ange namnen på **[!UICONTROL CSS classes]** från den aktuella formatmallen som ska användas för kartbehållaren.

     Avgränsa flera klassnamn med blanksteg.

   - Ange värden (i pixlar) för **[!UICONTROL Margins and Padding]** för att ange kartbehållarens yttre marginaler och inre utfyllnad.

     Ange varje motsvarande värde i kartbehållardiagrammet.

     | Behållarområde | Beskrivning |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Mängden tomt utrymme som används på ytterkanten på behållarens alla sidor. |
     | [!UICONTROL Padding] | Mängden tomt utrymme som används på behållarens inre kant på alla sidor. |

     {style="table-layout:auto"}

     >[!NOTE]
     >
     >Utfyllnad är inte tillgängligt för innehållstypen Karta.

1. När du är klar klickar du på **[!UICONTROL Save]** för att tillämpa inställningarna och återgå till arbetsytan i [!DNL Page Builder].

### Ändra stödrastrets storlek

Stödrasterstorleken avgör storleken på kartan som hör till en [kolumn](column.md) på scenen [!DNL Page Builder]. Som standard är kartan 12 kolumner bred, med högst 16 kolumner.

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_&#x200B;Admin **[!UICONTROL Configuration]**.

1. Välj _[!UICONTROL General]_&#x200B;i den vänstra panelen under **[!UICONTROL Content Management]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. Uppdatera stödrasteralternativen efter behov:

   >[!NOTE]
   >
   >Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för att ändra de här inställningarna.

   - För **[!UICONTROL Default Column Grid Size]** anger du ett nytt värde för stödrastrets standardstorlek.

   - För **[!UICONTROL Maximum Column Grid Size]** anger du ett nytt värde för den maximala standardstödrasterstorleken.

   ![Inställningar för kolumnstödrasterstorlek](./assets/pb-configure-advanced-content-tools-grid-size.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

[1]: https://cloud.google.com/maps-platform/
[2]: https://cloud.google.com/maps-platform/places/
[3]: https://cloud.google.com/maps-platform/user-guide/
[4]: https://developers.google.com/maps/documentation/javascript/get-api-key
[5]: https://www.google.com/maps
[6]: https://mapstyle.withgoogle.com/

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
