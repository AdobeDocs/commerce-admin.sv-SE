---
title: Media - Karta
description: Lär dig mer om innehållstypen för kartan, som används för att lägga till en karta från [!DNL Google Maps] Plattform för [!DNL Page Builder] stage.
exl-id: 91fea8f8-d48a-43f1-ba2a-212c7130cee9
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1583'
ht-degree: 0%

---

# Media - Karta

Använd _Karta_ innehållstyp för att lägga till en karta från [[!DNL Google Maps] Plattform][1] till [[!DNL Page Builder] stage](workspace.md#stage). Du kan till exempel lägga till en karta till ett block och sedan lägga till blocket i [Om oss](../content-design/pages.md#about-us) och [Kontakta oss](../getting-started/store-details.md#contact-us-form) sidor.

Få ut det mesta av [!DNL Google Maps] På plattformen kan du anpassa kartan, markera var du befinner dig och använda Google [Platser][2] för att lägga till omfattande information om din butik i alla [!DNL Google Maps].

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
| Inställningar | ![Ikonen Inställningar](./assets/pb-icon-settings.png){width="25"} | Öppnar sidan Redigera karta, där du kan ändra egenskaperna för kartan och behållaren. |
| Dölj | ![Dölj ikon](./assets/pb-icon-hide.png){width="25"} | Döljer den aktuella kartan. |
| Visa | ![Visa ikon](./assets/pb-icon-show.png){width="25"} | Visar den dolda kartan. |
| Duplicera | ![Duplicera, ikon](./assets/pb-icon-duplicate.png){width="25"} | Skapar en kopia av kartan. |
| Ta bort | ![Ikonen Ta bort](./assets/pb-icon-remove.png){width="25"} | Tar bort kartan från scenen. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Konfigurera [!DNL Google Maps] för din administratör

Innan du lägger till en karta måste du först öppna en [konto][3] för en kostnadsfri testversion av [!DNL Google Maps] Platform. Den kostnadsfria provperioden varar i 12 månader och inkluderar en kredit på 300 dollar. Om du använder din kredit debiterar Google inte ditt konto utan ditt tillstånd.

### Steg 1: Skaffa [!DNL Google Maps] API-nyckel

Beroende på om du redan har en [!DNL Google Maps] använder du någon av följande procedurer för att hämta den API-nyckel som krävs för konfigurationen. Så här konfigurerar du en [!DNL Google Maps] måste du vara webbplatsadministratör för att kunna aktivera fakturering för ditt konto. Om du inte är redo att konfigurera en [!DNL Google Maps] Du kan hoppa över det här steget och använda platshållarkartan för tillfället.

1. Gå till [Google Cloud Platform Console](https://cloud.google.com/console/google/maps-apis/overview).

1. Klicka på listrutan för projektet och välj eller skapa det projekt som du vill lägga till en API-nyckel för.

1. Om du vill konfigurera dina API-autentiseringsuppgifter följer du [instruktioner][4] i [!DNL Google Maps] dokument.

1. Kopiera API-nyckeln till Urklipp.

### Steg 2: Konfigurera [!DNL Google Maps] in [!DNL Commerce]

1. I _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I den vänstra panelen under _[!UICONTROL General]_, välja **[!UICONTROL Content Management]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

   ![Avancerade innehållsverktyg](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   Mer information om konfigurationsalternativen för det avancerade verktyget för innehållshantering finns i [Referenshandbok för konfiguration](../configuration-reference/general/content-management.md).

1. För **[!UICONTROL Google Maps API Key]** klistrar du in den nyckel du kopierade i steg 1.

1. Klicka på **[!UICONTROL Test Key]**.

   Om det är något problem med nyckeln går du tillbaka till [!DNL Google Maps] Plattformswebbplats som löser problemet. Försök sedan igen.

1. När nyckeln har verifierats klickar du på **[!UICONTROL Save Config]**.

## Lägga till en karta på scenen

1. Öppna sidan, blocket eller det dynamiska blocket på sidan [!DNL Page Builder] arbetsyta.

1. I [!DNL Page Builder] panel, expandera **[!UICONTROL Media]** och dra en **[!UICONTROL Map]** platshållare till scenen.

   ![Dra en karta till scenen](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   If [!DNL Google Maps] Plattformen har konfigurerats för din butik. En karta visas för din butiksplats.

   ![[!DNL Google Maps]](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   If [!DNL Google Maps] Plattformen har inte konfigurerats för din butik än. En platshållarkarta visas i stället.

   ![[!DNL Google Maps] Platshållare](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

## Lägg till en anpassad mappningsplats

1. Hovra över kartbehållaren för att visa verktygslådan och välj _Inställningar_ ( ![Ikonen Inställningar](./assets/pb-icon-settings.png){width="20"} ).

1. I det övre högra hörnet av _[!UICONTROL Edit Map]_sida, klicka **[!UICONTROL Add Location]**.

1. Ange **[!UICONTROL Location Name]** som du vill ska kopplas till stiftet på kartan.

1. Samla de platskoordinater som du vill använda för den anpassade platsen.

   Alternativt kan du **[!UICONTROL Position]** kan du dra stiftet på den visade kartan.

   Om det behövs går du till [[!DNL Google Maps]][5] i ett nytt webbläsarfönster och använd någon av följande metoder för att hämta koordinaterna:

   ![Kartkoordinater](./assets/pb-media-maps-settings-add-location-coordinates.png){width="600" zoomable="yes"}

   **Metod 1:** Kopiera från URL

   - Ange adressen i det övre vänstra hörnet **[!UICONTROL Search]** och klicka på _Sök_ ( ![Ikonen Sök](../assets/icon-magnify-search.png){width="20"} ).

   - Kopiera koordinaterna i URL:en och klistra in dem i en anteckningsruta.

   **Metod 2:** Copy from &quot;What&#39;s here?&quot;

   - Högerklicka på det röda stiftet som markerar platsen på kartan och välj **[!UICONTROL What's here?]** på menyn.

   - I den visade etiketten kopierar du texten, inklusive koordinaterna, och klistrar in texten i en anteckningsruta.

1. Ange siffrorna, utan kommatecken, i varje **[!UICONTROL Coordinates]** rutor.

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

1. När du är klar klickar du på **[!UICONTROL Save]**.

   Den nya platsen visas på kartan och i kartpositionens rutnät på _[!UICONTROL Edit Map]_sida.

   ![[!DNL Page Builder] - kartor, platsrutnät](./assets/pb-media-maps-settings-add-location-grid.png){width="600" zoomable="yes"}

## Formatera kartan {#styling}

Använd [!DNL Google Maps] Guiden Formatera plattform när du vill använda ett av sex fördefinierade teman eller skapa ett anpassat tema. Du kan generera en JSON-fil med mappningsformategenskaperna eller en länk till den formaterade kartan.

### Ändra kartformatet

1. I _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I den vänstra panelen under _[!UICONTROL General]_, välja **[!UICONTROL Content Management]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. Under **[!UICONTROL Google Maps Style]** textruta, klicka [Skapa kartformat][6].

   Åtgärden öppnar [[!DNL Google Maps] Guiden Plattformsformat][6] på en separat flik där du kan definiera ett format för [!DNL Google Maps] Plattformsprojekt

1. Klicka **[!UICONTROL Create a Style]** och följ instruktionerna.

   När du är klar klickar du på **[!UICONTROL Finish]**.

1. Exportera det färdiga formatet som JSON-kod eller som en URL-adress så att du kan lägga till det i [!DNL Commerce] konfiguration.

   - **JSON**: Under rutan med den genererade JSON-koden klickar du på **[!UICONTROL Copy JSON]**.

   - **[!UICONTROL URL]**: Under rutan med den genererade URL:en klickar du på **[!UICONTROL Copy URL]**.

1. Gå tillbaka till webbläsarfliken för Admin och klistra in den genererade koden eller URL:en i **Google Maps Style** box.

   Om du använder en URL-adress ersätter du `YOUR_API_KEY` platshållare med [!DNL Google Maps] API-nyckel. Den här URL:en länkar till din formaterade Google Map.

1. Klicka på i det övre högra hörnet **[!UICONTROL Save Config]**.

### Ändra kartinställningar

1. Hovra över kartbehållaren för att visa verktygslådan och välj _Inställningar_ ( ![Ikonen Inställningar](./assets/pb-icon-settings.png){width="20"} ).

1. Ändra de grundläggande inställningarna efter behov:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | [!UICONTROL Height] | Anger höjden på det visade schemat i pixlar. |
   | [!UICONTROL Show Controls] | Anger om standardkontrollerna för Google Map visas. |

   {style="table-layout:auto"}

1. Ändra _[!UICONTROL Advanced]_inställningar efter behov:

   - Om du vill styra den vågräta placeringen av kartinnehållet som lagts till i behållaren väljer du en **[!UICONTROL Alignment]**:

     | Alternativ | Beskrivning |
     | ------ | ----------- |
     | `Default` | Använder den standardinställning för justering som anges i formatmallen för det aktuella temat. |
     | `Left` | Justerar innehållet längs kartbehållarens vänstra kant, med hänsyn till eventuell utfyllnad som har angetts. |
     | `Center` | Justerar innehållet i mitten av kartbehållaren, med hänsyn till eventuell utfyllnad som har angetts. |
     | `Right` | Justerar innehållet längs kartbehållarens högra kant, med hänsyn till eventuell utfyllnad som har angetts. |

     {style="table-layout:auto"}

   - Ange **[!UICONTROL Border]** format som används på alla fyra sidorna i kartbehållaren:

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

   - (Valfritt) Ange namnen på **[!UICONTROL CSS classes]** från den aktuella formatmallen som ska användas för mappningsbehållaren.

     Avgränsa flera klassnamn med blanksteg.

   - Ange värden i pixlar för **[!UICONTROL Margins and Padding]** för att ange kartbehållarens yttre och inre utfyllnad.

     Ange varje motsvarande värde i kartbehållardiagrammet.

     | Behållarområde | Beskrivning |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Mängden tomt utrymme som används på ytterkanten på behållarens alla sidor. |
     | [!UICONTROL Padding] | Mängden tomt utrymme som används på behållarens inre kant på alla sidor. |

     {style="table-layout:auto"}

     >[!NOTE]
     >
     >Utfyllnad är inte tillgängligt för innehållstypen Karta.

1. När du är klar klickar du på **[!UICONTROL Save]** för att använda inställningarna och gå tillbaka till [!DNL Page Builder] arbetsyta.

### Ändra stödrastrets storlek

Rutnätets storlek avgör storleken på kartan i förhållande till en [kolumn](column.md) på [!DNL Page Builder] stage. Som standard är kartan 12 kolumner bred, med högst 16 kolumner.

1. I _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I den vänstra panelen under _[!UICONTROL General]_, välja **[!UICONTROL Content Management]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. Uppdatera stödrasteralternativen efter behov:

   >[!NOTE]
   >
   >Rensa **[!UICONTROL Use system value]** om du vill ändra inställningarna.

   - För **[!UICONTROL Default Column Grid Size]** anger du ett nytt värde för stödrastrets standardstorlek.

   - För **[!UICONTROL Maximum Column Grid Size]** anger du ett nytt värde för den maximala standardstödrasterstorleken.

   ![Inställningar för kolumnstödrasterstorlek](./assets/pb-configure-advanced-content-tools-grid-size.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

[1]: https://cloud.google.com/maps-platform/
[2]: https://cloud.google.com/maps-platform/places/
[3]: https://cloud.google.com/maps-platform/user-guide/
[4]: https://developers.google.com/maps/documentation/javascript/get-api-key
[5]: https://www.google.com/maps
[6]: https://mapstyle.withgoogle.com/
