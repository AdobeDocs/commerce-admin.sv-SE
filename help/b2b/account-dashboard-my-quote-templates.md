---
title: '[!UICONTROL My Quote Templates]'
description: Lär dig mer om kundupplevelsen av offertmallar, som finns på kontrollpanelen för butikskonton.
feature: B2B, Companies, Quotes
exl-id: 3d95a44e-b874-442b-af96-0dc6b589d0f7
source-git-commit: 71b9326aa5a8c3d7656b3c0f166cf25291b2abba
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# [!UICONTROL My Quote Templates]

Om offerter är aktiverade visas alla offertmallar som är associerade med kundkontot i avsnittet _[!UICONTROL My Quotes Template]_på kontrollpanelen för kundkonton. Beroende på deras tillstånd kan bara köpare som gör inköp för ett företags räkning begära en offertmall och förhandla om offertpriser och villkor för återkommande order.

![Mina offertmallar](./assets/account-dashboard-quote-templates-list.png){width="700" zoomable="yes"}

I offertmallslistan ordnas mallarna efter status.

- **[!UICONTROL Active Quote Templates]** listar mallar som har förhandlats och godkänts för användning. Informationen omfattar minsta offertsumma och beställningar som gjorts om dessa alternativ konfigurerades under förhandlingsprocessen. Köpare kan generera en länkad offert från mallen för att skicka en order baserat på offertvillkor.

- **[!UICONTROL In Review]** listar mallar i förhandlingsprocessen som visar aktuell status och tillhandahåller en länk för att öppna mallen.

- **[!UICONTROL Inactive]** listar mallar som har gått ut, annullerats eller som inte längre är giltiga eftersom en köpare har utnyttjat det tillåtna antalet allokerade order.

För köparen är sidan *[!UICONTROL My Quotes Templates]* fokuspunkt för all kommunikation mellan köpare och säljare under förhandlingsprocessen.

En köpare som accepterar de förhandlade villkor som säljaren erbjuder kan acceptera mallen och sedan använda den för att generera på förhand godkända länkade offerter som kan användas för att göra beställningar.

- Åtgärder som rör hantering av offertmallen:

   - Avbryt en mall
   - Skicka till säljaren för granskning
   - Acceptera offertmallen
   - Ändra offertmallens förfallodatum
   - Lägg till en leveransadress

- Åtgärder för att uppdatera offertmallsinformation under förhandlingsprocessen:

   - Granska priser och uppdateringar.
   - Om kvantitetströsklar har konfigurerats för offertmallen justerar du minimum- och maxvärdena.
   - Spåra förhandlingsprocessen från [!UICONTROL Comments] och [!UICONTROL History] avsnitt.
   - För mallar som fortfarande granskas kan köparen ändra offertmallen genom att ta bort artiklar.
   - Kommunicera och förhandla med säljaren genom att lägga till anteckningar på radobjekt- och offertnivå.

  När köparen har gjort ändringar returnerar han mallen till säljaren för granskning.

- Allmänna åtgärder under förhandling:

   - Skicka offertmall till säljare för granskning
   - Acceptera offertmallen
   - Avbryt om du vill avsluta förhandlingen och stänga offerten

I följande exempel visas en offertmall som har uppdaterats av köparen och skickats tillbaka till säljaren för granskning.

![Köparvy för offertmall](./assets/account-dashboard-my-quote-template-detailed.png){width="700" zoomable="yes"}

Mallar med statusen `Submitted` är låsta tills säljaren granskar och uppdaterar mallen och returnerar den till köparen.

## Skapa en offertmall

Köparen kan påbörja offertmallsförhandlingen med någon av följande metoder:

- Skapa en mall från en befintlig offert genom att klicka på åtgärden **[!UICONTROL Create quote template]**.

- Skicka en offertförfrågan från butiken och lägg till kommentarer som ber säljaren att skapa en offertmall utifrån offertförfrågan.

## Visa en offertmall

1. Köparen loggar in på sitt konto.

1. Välj **[!UICONTROL My Quote Templates]** i den vänstra panelen.

1. Söker efter offertmallen i listan och klickar på **[!UICONTROL View]** i kolumnen _[!UICONTROL Action]_.

## Lägg till en leveransadress

Köparen kan inte acceptera en offertmall förrän den har en leveransadress.

1. Köparen loggar in på sitt konto.

1. Välj **[!UICONTROL My Quote Templates]** i den vänstra panelen.

1. Väljer önskad offertmall.

1. Klicka på **[!UICONTROL Add New Address]** i avsnittet **[!UICONTROL Shipping Information]**.

1. Fyller i detaljer för den nya adressen.

1. Klicka på **[!UICONTROL Save Address]**.

När köparen har lagt till adressen skickar de tillbaka mallen till säljaren för granskning. Säljaren tillhandahåller alternativ för frakt och leverans. Dessa uppdateringar kan påverka det förhandlade offertpriset. Leveransalternativen är låsta vid utcheckning.

## Generera en länkad offert

När köparen har godkänt en offertmall kan de använda den för att generera förgodkända, länkade citattecken från *[!UICONTROL My Quote Templates dashboard]* eller från offertmallen med hjälp av åtgärden **[!UICONTROL Generate a quote]**.

Den länkade offerten innehåller ett meddelande som anger att den är godkänd och klar för utcheckning. Den innehåller även en länk till offertmallen i rubrikinformationen.

![Länkad offert genererad från en offertmall](./assets/quote-templates-linked-quote.png){width="700" zoomable="yes"}

Om offertmallen har konfigurerats med ett ordertröskelvärde ökas antalet när den länkade offerten genereras.

Köpare kan utföra följande åtgärder från en länkad offert:

- Om offerten har konfigurerats med kvantitetströsklar justerar du orderkvantiteten för radartiklar.
- Gå till kassan för att skicka en order.
- Ta bort eller skriv ut offerten.
- Öppna offertmallen som används för att generera offerten.

## Avbryt en offertmall

Klicka på **[!UICONTROL Cancel Quote Template]** på mallsidan för offerter.

Offertmallen avbryts och offertstatusen ändras till `Closed`. Det stängda citattecknet finns kvar i listan med *[!UICONTROL Inactive]* citattecken och finns kvar i listan i rutnätet _[!UICONTROL Quote Templates]_i Admin.
