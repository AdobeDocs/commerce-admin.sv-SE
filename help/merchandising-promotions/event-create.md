---
title: Skapa och uppdatera händelser
description: Lär dig hur du skapar en händelse som är kopplad till en kategori i din katalog.
exl-id: 6c9f6a33-6785-4c3a-add6-dc2a6b16ed88
feature: Marketing Tools, Promotions/Events
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 0%

---

# Skapa och uppdatera händelser

{{ee-feature}}

Varje händelse är associerad med en kategori i din katalog och endast en händelse kan associeras med en viss kategori i taget. Om du vill visa en lista över kommande evenemang i din butik måste du också konfigurera en [Catalog Events Carousel](../content-design/widget-event-carousel.md) widget.

![Händelselista](./assets/category-events.png){width="700" zoomable="yes"}

## Skapa en händelse

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. Klicka på i det övre högra hörnet **[!UICONTROL Add Catalog Event]**.

1. Välj den kategori som du vill associera med händelsen i kategoriträdet.

   Eftersom varje kategori bara kan ha en händelse i taget inaktiveras alla kategorier som redan har en händelse.

   ![Ny händelse - kategoriträd](./assets/catalog-events-category-tree.png){width="500" zoomable="yes"}

1. Definiera **[!UICONTROL Catalog Event Information]**:

   ![Kataloghändelseinformation](./assets/catalog-event-information.png){width="700" zoomable="yes"}

   - För **[!UICONTROL Start Date]** använder du kalendern (![Kalenderikon](../assets/icon-calendar.png)) för att välja datumet. Använd **[!UICONTROL Hour]** och **[!UICONTROL Minute]** skjutreglage som anger när händelsen börjar.

   - För **[!UICONTROL End Date]** använder du kalendern (![Kalenderikon](../assets/icon-calendar.png)) för att välja datumet. Använd **[!UICONTROL Hour]** och **[!UICONTROL Minute]** skjutreglage för att ange den tid som händelsen slutar.

   - Så här överför du en **[!UICONTROL Image]** för händelsewidgeten klickar du på **[!UICONTROL Choose File]** och välj bildfilen i katalogen.

   - I **[!UICONTROL Sort Order]** anger du en siffra som anger i vilken ordning händelsen visas när den listas med andra händelser.

   - Markera kryssrutan för varje sidtyp där du vill att nedräkningsfilmen ska visas.

1. När du är klar klickar du på **[!UICONTROL Save]**.

## Uppdatera händelser

Händelser kan redigeras antingen från sidan Händelser eller från den kategori som är associerad med händelsen. När en kategori har en associerad händelse visas knappen Redigera händelse i det övre högra hörnet.

### Metod 1: Redigera en händelse från sidan Händelser

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. Leta reda på händelsen i listan och öppna den i redigeringsläge.

1. Gör nödvändiga ändringar i händelsen.

1. När du är klar klickar du på **[!UICONTROL Save]**.

### Metod 2: Redigera en händelse från en kategori

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Välj den kategori som är associerad med händelsen i kategoriträdet till vänster.

1. Klicka på i det övre högra hörnet **[!UICONTROL Edit Even]t**.

1. Gör nödvändiga ändringar i händelsen.

1. När du är klar klickar du på **[!UICONTROL Save]**.

## Ta bort en händelse

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. Leta reda på händelsen i listan och öppna den i redigeringsläge.

1. Klicka på i det övre högra hörnet **[!UICONTROL Delete]**.

1. Bekräfta åtgärden genom att klicka **[!UICONTROL OK]**.

## Fältbeskrivningar

| Fält | [Omfång](../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Category] | Global | När du skapar en händelse länkas det här fältet tillbaka till kategoriträdet. När du redigerar en händelse länkas den till kategorisidan för händelsen. |
| [!UICONTROL Start Date] | Global | Startdatum och starttid för händelsen i `MMDDYYYY HH;MM` format. Klicka på kalenderikonen för att välja datumet. |
| [!DNL End Date] | Global | Slutdatum och sluttid för händelsen i `MMDDYYYY HH;MM` format. Klicka på kalenderikonen för att välja datumet. |
| [!UICONTROL Image] | Butiksvy | Överför en bild som visas i [Carousel-widgeten Kataloghändelser](../content-design/widget-event-carousel.md). |
| [!UICONTROL Sort Order] | Global | Anger i vilken ordning den här händelsen ska visas när den listas med andra händelser. |
| [!UICONTROL Display Countdown Ticker On] | Global | Visar nedräkningsfilmen i sidhuvudet på varje angiven sida. Alternativ: `Category Page` / `Product Page` |
| [!UICONTROL Status] | Global | Anger händelsens status baserat på intervallet för startdatum och slutdatum. Status är ett skrivskyddat värde. Värden: `Open` / `Closed` / `Upcoming` |

{style="table-layout:auto"}

## Knappfält

| Knapp | Beskrivning |
|--- |--- |
| **[!UICONTROL Back]** | Återgår till sidan Händelser utan att spara den nya händelsen eller ändringarna i en befintlig händelse. |
| **[!UICONTROL Delete]** | Tar bort händelsen. |
| **[!UICONTROL Reset]** | Rensar formen på ändringar som inte har sparats och återställer den ursprungliga händelseinformationen. |
| **[!UICONTROL Save and Continue Edit]** | Sparar alla ändringar och låter formuläret vara öppet i redigeringsläge. |
| **[!UICONTROL Save]** | Sparar ändringar, stänger formuläret och återgår till sidan Händelser. |

{style="table-layout:auto"}
