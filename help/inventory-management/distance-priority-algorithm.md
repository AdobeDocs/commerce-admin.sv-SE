---
title: Konfigurera algoritmen för avståndsprioritet
description: Ange konfigurationen för att jämföra platsen för leveransdestinationsadressen med källplatserna för att fastställa den närmaste källan för att slutföra leveranser.
exl-id: 4dec179a-25ac-48db-a84b-4974798272b0
feature: Inventory, Configuration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---

# Konfigurera algoritmen för avståndsprioritet

Algoritmen Avståndsprioritet jämför platsen för leveransdestinationsadressen med källplatserna för att fastställa den närmaste källan för leverans av försändelser. Avståndet kan bestämmas genom fysisk sträcka eller tid som tillbringas med att resa från en plats till en annan, med hjälp av databasdata eller körning, gång eller cyklingsanvisningar. Använd den här [Source-algoritmen](selection-reservations.md) för att rekommendera närmaste källa till leveransmåladresserna.

>[!NOTE]
>
>Om du använder algoritmen för avståndsprioritet bör du ange den fullständiga gatuadressen och GPS-koordinaterna för dina [källor](sources-add.md).

Du har två alternativ för att beräkna avståndet och tiden för att hitta den närmaste källan för leverans:

- **Google MAP** - Använder [Google Maps Platform](https://cloud.google.com/maps-platform/)-tjänster för att beräkna avståndet och tiden mellan leveransdestinationsadressen och källplatserna. Det här alternativet använder källans latitud- och longitudkoordinater (GPS-koordinater) och kan använda gatuadressen beroende på beräkningsläget. En Google API-nyckel krävs med [API för geokodning](https://developers.google.com/maps/documentation/geocoding/start) och [API:t för distansmatris](https://developers.google.com/maps/documentation/distance-matrix/start) aktiverat, och du kan debiteras via Google.

- **Offlineberäkning** - Beräknar avståndet med nedladdade och importerade geokoddata med hjälp av postkoder och GPS-koordinater för att fastställa den närmaste källan till leveransens måladress. Om du vill konfigurera det här alternativet kan du behöva utvecklarhjälp för att initialt hämta och importera geokoder med kommandoradsinstruktioner.

>[!NOTE]
>
>Konfigurera [standardskattemålet](../stores-purchase/tax-class.md#default-tax-destination){target="_blank"} för varje land för en webbplats med flera länder.

## Använd Google Maps

Du behöver inget Google-konto för att komma igång. Processen innefattar vid behov att skapa Google-konton och projekt. Det här alternativet kräver ett faktureringskonto och en betalningsmetod som läggs till i ditt Google-konto för att slutföra konfigurationer och använda algoritmen.
Avståndsbaserad algoritm för Google MAP rekommenderas som mer avancerad och exakt jämfört med offlineberäkning.

### Steg 1: Skapa Google API-nyckeln

Nyckeln är från [Google Maps Platform](https://cloud.google.com/maps-platform/) och ska ha [API för geokodning](https://developers.google.com/maps/documentation/geocoding/start) och [API för distansmatris](https://developers.google.com/maps/documentation/distance-matrix/start) aktiverat. Mer information finns i [Konfigurera algoritmen för avståndsprioritet](distance-priority-algorithm.md).

1. Gå till [Google Maps Platform](https://cloud.google.com/maps-platform/) och klicka på **[!UICONTROL Get Started]**.

1. Om du vill aktivera plattformen väljer du **[!UICONTROL Maps, Routes, and Places]** och klickar på **[!UICONTROL Continue]**.

   ![Google Maps Platform för din nyckel](assets/inventory-google-key1.png){width="350" zoomable="yes"}

1. Logga in med ett Google-konto eller skapa ett konto.

1. Konfigurera ett projekt:

   - Välj ett projekt eller ange ett nytt projektnamn.

   - Om du vill acceptera villkoren väljer du `Yes`.

   - Klicka på **[!UICONTROL Next]**.

1. Ange ett faktureringskonto eller skapa ett. Du kan hoppa över och lägga till ett faktureringskonto senare.

   Det krävs ett faktureringskonto för att använda den här tjänsten.

1. Klicka på **[!UICONTROL Console]** om du vill öppna och konfigurera dina alternativ för Google Cloud-plattformen.

   - Öppna projektet.

   - Expandera menyn och klicka på **[!UICONTROL APIs & Services]** > **[!UICONTROL Library]**.

     ![Google API Services](assets/inventory-google-key2.png){width="350" zoomable="yes"}

   - Sök efter [API för geokodning](https://developers.google.com/maps/documentation/geocoding/start) och [API för avståndsmatris](https://developers.google.com/maps/documentation/distance-matrix/start). Välj och aktivera varje tjänst.

1. Expandera menyn, klicka på **[!UICONTROL APIs & Services]** > **[!UICONTROL Credentials]** och kopiera Google API-nyckeln.

   ![Google API Key Copy](assets/inventory-google-key3.png){width="350" zoomable="yes"}

### Steg 2: Konfigurera Google MAP Provider

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Inventory]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet _[!UICONTROL Distance Provider for Distance Based SSA]_och ange **[!UICONTROL Provider]**till `Google MAP`.

   ![Providers för distansbaserad SSA](assets/config-catalog-inventory-distance-provider.png){width="350" zoomable="yes"}

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet _[!UICONTROL Google Distance Provider]_och konfigurera inställningarna:

   - För **[!UICONTROL Google API Key]** anger du nyckeln som kopierats från ditt Google-konto.

   - Välj en konfiguration för **[!UICONTROL Computation mode]**.

     >[!NOTE]
     >
     >Om rutter och data inte returneras för det valda beräkningsläget (körning, cykling eller gång) för en leverans när den här algoritmen används för leverans, används som standard Source-prioritet. Du bör ange [prioritet för källor per lager](stocks-prioritize-sources.md).

     | Alternativ | Beskrivning |
     | ----- | ----- |
     | `Driving` | (Standard) Begär standardvägbeskrivningar för körning i vägnätet. |
     | `Walking` | Begär vägbeskrivningar där man kan gå med hjälp av fotgängarbanor och sidewalks (där sådana finns). |
     | `Bicycling` | Begär cykelväggar med cykliska banor och önskade gator (om sådana finns). [Distance Matrix Service](https://developers.google.com/maps/documentation/javascript/distancematrix#travel_modes) är bara tillgänglig i USA och vissa kanadensiska städer. |

   - Välj en värdetyp för **[!UICONTROL Value]**:

     | Alternativ | Beskrivning |
     | ----- | ----- |
     | `Distance` | (Standard) Returnerar avståndet mellan punkter i mätvärden (kilometer och meter) eller i imperium (engelska mil och fot). |
     | `Time to Destination` | Returnerar den tid som krävs för att resa från källplatserna till leveransadressen i timmar och minuter. |

   ![Google Distance Provider](assets/config-catalog-inventory-distance-provider-settings.png){width="350" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Använd offlineberäkning

Vid offlineberäkningar används landskoder för att fastställa avståndet mellan leveransdestinationen och källadresserna. Det här alternativet kan kräva utvecklarhjälp för att konfigurera. Använd ett [!DNL Inventory Management] CLI-kommando för att hämta och importera data från [geonames.org](https://www.geonames.org/).

>[!NOTE]
>
>Importerade geokoder från [geonames.org](https://www.geonames.org/) har begränsningar för vissa länder, till exempel Kanada och Irland. Mer information finns i [GeoNames-postkodfiler](https://download.geonames.org/export/zip/readme.txt).

### Steg 1: Hämta och importera geokoder

Komplett kommandoradskonfiguration för att hämta och importera geokodländer som ska levereras till och ha källplatser i. Det här steget kan kräva utvecklarhjälp för att få hjälp med kommandoradsuppgifter. Se [Importera geokoder](cli.md#import-geocodes).

Slutför dessa kommandon när du vill lägga till fler geokoder.

### Steg 2: Ange beräkningen

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Inventory]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet _[!UICONTROL Distance Provider for Distance Based SSA]_.

1. Avmarkera kryssrutan **[!UICONTROL Use system value]** och ange **[!UICONTROL Provider]** till `Offline Calculation`.

   ![Avståndsproviders för avståndsbaserad SSA](assets/inventory-distance-offline.png){width="350" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
