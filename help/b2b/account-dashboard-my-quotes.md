---
title: '[!UICONTROL My Quotes]'
description: Lär dig mer om kundupplevelsen för offerter, som finns på deras kontouppsättning.
exl-id: 137f0a99-8f24-4838-b54b-b0ef2c39a32a
feature: B2B, Companies, Quotes
source-git-commit: 6cf53c7caf37c24be473afecfba829595c14cb8c
workflow-type: tm+mt
source-wordcount: '1220'
ht-degree: 0%

---


# [!UICONTROL My Quotes]

Om offerter är aktiverade visas alla offerter som skickats av kunden i avsnittet _[!UICONTROL My Quotes]_&#x200B;på kontrollpanelen för kundkonton. Beroende på deras tillstånd kan bara köpare som gör inköp för ett företags räkning skicka in begäranden om att förhandla om priset på ett köp.

![Mina citattecken](./assets/account-dashboard-my-quotes.png){width="700" zoomable="yes"}

Köparen påbörjar processen genom att [skicka en anbudsförfrågan](quote-request.md) från kundvagnen. E-post utbyts mellan köparen och säljaren under [förhandlingsprocessen](quote-price-negotiation.md). För köparen är sidan [!UICONTROL My Quotes] fokuspunkt för all kommunikation mellan köpare och säljare under förhandlingsprocessen. En köpare som accepterar det förhandlade pris som säljaren erbjuder kan gå direkt till utcheckningssidan från offerten. Det går inte att lägga till ytterligare rabatter i det förhandlade offerten.

När en köpare förhandlar om en offert finns det flera alternativ för att antingen hantera offerten eller uppdatera offertinformationen.

* Åtgärder som rör hantering av offerten:

   * Skapa en kopia av offerten
   * Stäng citattecknet
   * Ta bort offerten
   * Byt namn på citattecknet
   * Skriv ut offerten
   * Skapa en mall

* Åtgärder för att uppdatera offertinformation:

   * Granska artikelpriser och uppdateringar
   * Spåra förhandlingsprocessen från [!UICONTROL Comments] och [!UICONTROL History] avsnitt
   * Ändra offerten för att ta bort objekt
   * Kommunicera och förhandla med säljaren genom att lägga till anteckningar på radobjektsnivå och offertnivå
   * Lägg till en leveransadress
   * Flytta radartiklar till en rekvisitionslista
   * Konvertera offerten till en order om villkoren är godtagbara

* Allmänna åtgärder under förhandling:

   * Skicka offert till säljare för granskning
   * Gå till kassan

I följande exempel visas en offert som har uppdaterats av köparen och skickats tillbaka till säljaren för granskning.


![Köparvy för offert](./assets/account-dashboard-my-quote-detailed.png){width="700" zoomable="yes"}

Kurser med statusen `Updated` är låsta tills säljaren returnerar offerten.

## Visa citattecken

Med de nödvändiga [behörigheterna för rollen](account-company-roles-permissions.md) kan köpare som är kopplade till ett företagskonto se offerter som har begärts av [underordnade användare](account-company-structure.md). Företagsadministratörer kan se alla offerter för företagskontot.

1. Köparen loggar in på sitt konto i butiken.

1. Klicka på **[!UICONTROL My Quotes]** i den vänstra navigeringen.

1. Om du vill visa alla offerter som de har skapat klickar du på länken **[!UICONTROL Show My Quotes]** (visas endast för företagsadministratören eller kontot med underordnade användare).

1. Klicka på **[!UICONTROL Show All Quotes]** om du vill se alla citat från alla företagsanvändare.

## Visa en offert

1. Köparen loggar in på sitt konto.

1. Välj **[!UICONTROL My Quotes]** i den vänstra panelen.

1. Söker efter citattecknet i listan och klickar på **[!UICONTROL View]** i kolumnen _[!UICONTROL Action]_.

## Kopiera en offert

1. Köparen loggar in på sitt företagskonto i butiken.

1. Välj **[!UICONTROL My Quotes]** i den vänstra panelen.

1. Hitta och få tillgång till den önskade offerten i listan och klicka på **[!UICONTROL Create Copy]** i den ursprungliga offerten.

## Skapa mall

1. Köparen loggar in på sitt konto.

1. Välj **[!UICONTROL My Quote Templates]** i den vänstra panelen.

1. Söker efter citattecknet i listan **[!UICONTROL My Quotes]** och klickar på **[!UICONTROL Create Quote Template]** i kolumnen _[!UICONTROL Action]_.

## Flytta radobjekt från en offert till en rekvisitionslista

1. Köparen loggar in på sitt konto.

1. Välj **[!UICONTROL My Quotes]** i den vänstra panelen.

1. Hitta och öppna den önskade citattecknen i listan.

1. Markera radobjekten.

1. Klicka på **[!UICONTROL Move to Requisition list]** i listrutan _[!UICONTROL Actions]_.

1. Välj en befintlig rekvisitionslista om du vill flytta de markerade objekten.

1. Klicka på **[!UICONTROL Move item]**.

Mer information om den här processen finns i [Lägg till produkter i en rekvisitionslista](requisition-lists.md).

>[!NOTE]
>
> Du kan inte skapa en ny rekvisitionslista när du flyttar artiklar. Det går bara att flytta artiklar till en befintlig rekvisitionslista.

## Flytta radobjekt till en ny offert

1. Köparen loggar in på sitt konto.

1. Välj **[!UICONTROL My Quotes]** i den vänstra panelen.

1. Hitta och öppna den önskade citattecknen i listan.

1. Markera radobjekten.

1. Klicka på **[!UICONTROL Move item to new quote]** i listrutan _[!UICONTROL Actions]_.

1. Ge den nya offerten ett namn i modal.

1. Välj **[!UICONTROL Move to quote]** om du vill flytta det markerade objektet till den nya offerten.

>[!NOTE]
>
> När du markerar flera objekt visas spärrning som **[!UICONTROL Move selected items to new quote]**.

## Lägga till en leveransadress

1. Köparen loggar in på sitt konto.

1. Välj **[!UICONTROL My Quotes]** i den vänstra panelen.

1. Markerar det önskade citattecknet.

1. Klicka på **[!UICONTROL Add New Address]** i avsnittet **[!UICONTROL Shipping Information]**.

1. Fyller i detaljer för den nya adressen.

1. Klicka på **[!UICONTROL Save Address]**.

När köparen lägger till adressen tillhandahåller säljaren alternativ för frakt och leverans. Dessa uppdateringar kan påverka det förhandlade offertpriset. Leveransalternativen är låsta vid utcheckning.

## Skriva ut en offert

1. I den öppna citattecknet till höger om avsnittet _[!UICONTROL Items Quoted]_&#x200B;klickar köparen på&#x200B;**[!UICONTROL Print]**.

1. Verifierar **[!UICONTROL Destination]** som skrivare eller PDF.

1. Klicka på **[!UICONTROL Print]**.

## Avbryta en offertförfrågan

1. Klicka på **[!UICONTROL Close quote]** i den öppna citattecknet precis ovanför avsnittet Objekt som citerats.

   Begäran avbryts och offertstatusen ändras till `Closed`. Den stängda offerten finns kvar i din lista med offerter och finns kvar i listan i rutnätet _[!UICONTROL Quotes]_&#x200B;från administratören.

1. Om du vill ta bort det annullerade citattecknet från listan med citattecken klickar du på **[!UICONTROL Delete]**.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

   Det avslutande citattecknet tas bort från deras lista med citattecken. Den visas dock fortfarande i rutnätet _[!UICONTROL Quotes]_&#x200B;i Admin, med statusen `Closed`.

## Offertåtgärder

| Åtgärd | Beskrivning |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Byt namn | Ändra namnet på citattecknet |
| Skapa kopia | En köpare kan skapa en offert från den aktuella offerten genom att kopiera och byta namn på den. |
| Stäng citat | När en köpare stänger en offert kan den inte öppnas igen. Vid behov kan köparen återskapa den genom att använda åtgärden [!UICONTROL Create Copy]. Det här alternativet är inte tillgängligt om offertstatusen är `Draft`. |
| Skapa mall | Skapa en offertmall baserad på aktuell offert. Offertmallar effektiviserar offertförhandlingen genom att låta köpare och säljare komma överens om kontrakt och prisvillkor som kan tillämpas på flera offerter.  Vid avtal kan köparen generera en i förväg godkänd, länkad offert från mallen för efterföljande order i stället för att starta om anbudsförfrågningsprocessen. |
| Ta bort citat | När en köpare tar bort en offert tas den bort från systemet och är inte längre tillgänglig. |
| Skriv ut | Öppnar ett utskriftsformulär där du kan spara offerten som PDF, fil eller skriva ut den på en konfigurerad skrivare. |

## Kolumnbeskrivningar

| Kolumn | Beskrivning |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Quote Name] | Namnet som köparen tilldelat offertförfrågan. |
| [!UICONTROL Created] | Datumet då offertförfrågan skickades för första gången. |
| [!UICONTROL Created By] | Förnamn och efternamn på den köpare som skickade offertförfrågan. |
| [!UICONTROL Status] | Anger offertens status. Status för en offert kan bara ändras genom åtgärder från antingen köparen eller säljaren. <br/>**[!UICONTROL Submitted]**- Köparens anbudsförfrågan har inte öppnats av säljaren än. I det här läget kan köparen fortfarande ändra anbudsförfrågan. Tillgängliga åtgärder: `View` / `Close` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Pending]** - Säljaren har öppnat förfrågan och håller på att granska den och förbereda ett svar. Tillgängliga åtgärder: `View` / `Close` <br/>**[!UICONTROL Updated]**- säljaren har skickat ett svar till köparen och knappen _[!UICONTROL Proceed to Checkout]_&#x200B;är aktiverad. I det här läget kan köparen fortsätta att ändra offerten. Tillgängliga åtgärder: `View` / `Send for Review` / `Proceed to Checkout` / `Delete Quote` / `Close` / `Edit Quantity` / `Delete SKU` / `Add comments` / `Edit Shipping Address`<br/>**[!UICONTROL Open]**- Köparen uppdaterar fortfarande offerten och knappen&#x200B;_[!UICONTROL Proceed to Checkout]_ är inaktiverad. Tillgängliga åtgärder: `View` / `Send for Review` / `Delete Quote` / `Edit quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` <br/>**[!UICONTROL Ordered]**- Köparen har skickat en order baserat på det förhandlade offerten. Offerten är låst och kan inte redigeras. Tillgänglig åtgärd: Visa<br/>**[!UICONTROL Closed]** - Köparen har avslutat förhandlingen och avbryter offerten. Offerten är låst och kan inte redigeras av vare sig köpare eller säljare. Tillgängliga åtgärder: `View` / `Delete` <br/>**[!UICONTROL Declined]**- säljaren har avböjt anbudsförfrågan eller för att göra en föreslagen ändring under förhandlingsprocessen. En offert kan avvisas när som helst i arbetsflödet. Alla anpassade priser tas bort från offerten. Köparen kan fortsätta redigera offerten och skicka in den på nytt eller göra köpet med standardpriser för katalog. Tillgängliga åtgärder: `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Expired]** - Offertens livstid har gått ut. Alla föreslagna priser återställs. Köparen kan antingen slutföra köpet baserat på standardpriser för kataloger eller inleda en ny förhandlingsrunda. Tillgängliga åtgärder: `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` |

{style="table-layout:auto"}
