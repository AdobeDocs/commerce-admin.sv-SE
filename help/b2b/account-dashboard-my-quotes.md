---
title: '[!UICONTROL My Quotes]'
description: Lär dig mer om kundupplevelsen för offerter, som finns på deras kontouppsättning.
exl-id: 137f0a99-8f24-4838-b54b-b0ef2c39a32a
feature: B2B, Companies, Quotes
source-git-commit: 27b0c43f72faa2c2e8717fd5929f36d12f9e1b08
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 0%

---


# [!UICONTROL My Quotes]

Om offerter är aktiverade visas alla offerter som skickats av kunden i avsnittet _[!UICONTROL My Quotes]_på kontrollpanelen för kundkonton. Beroende på deras tillstånd kan bara köpare som gör inköp för ett företags räkning skicka in begäranden om att förhandla om priset på ett köp.

![Mina citattecken](./assets/account-dashboard-my-quotes.png){width="700" zoomable="yes"}

Köparen påbörjar processen genom att [skicka en anbudsförfrågan](quote-request.md) från kundvagnen. E-post utbyts mellan köparen och säljaren under [förhandlingsprocessen](quote-price-negotiation.md). För köparen är sidan [!UICONTROL My Quotes] fokuspunkt för all kommunikation mellan köpare och säljare under förhandlingsprocessen. En köpare som accepterar det förhandlade pris som säljaren erbjuder kan gå direkt till utcheckningssidan från offerten. Det går inte att lägga till ytterligare rabatter i det förhandlade offerten.

En köpare kan slutföra följande åtgärder när han eller hon förhandlar om en offert:

* Granska artikelpriser och uppdateringar
* Spåra förhandlingsprocessen från [!UICONTROL Comments] och [!UICONTROL History] avsnitt
* Ändra offerten för att ta bort objekt
* Kommunicera och förhandla med säljaren genom att lägga till anteckningar på radobjektsnivå och offertnivå
* Skicka offert till säljare för granskning
* Konvertera offerten till en order om villkoren är godtagbara
* Stäng citattecknet
* Ta bort offerten
* [!BADGE 1.5.0-beta-funktioner]{type=Informative url="/help/b2b/release-notes.md" tooltip="Endast tillgängligt för Beta programdeltagare"}

I följande exempel visas en offert som har uppdaterats av köparen och skickats tillbaka till säljaren för granskning.


![Köparvy för offert](./assets/account-dashboard-my-quote-detail.png){width="700" zoomable="yes"}

Kurser med statusen `Updated` är låsta tills säljaren returnerar offerten.

## Visa citattecken

Med de [behörigheter som krävs för rollen](account-company-roles-permissions.md) kan kunder som är kopplade till ett företagskonto se offerter som begärts av [underordnade användare](account-company-structure.md). Företagsadministratörer kan se alla offerter för företagskontot.

1. Kunden loggar in på sitt konto i butiken.

1. Klicka på **[!UICONTROL My Quotes]** i den vänstra navigeringen.

1. Om du vill visa alla offerter som de har skapat klickar du på länken **[!UICONTROL Show My Quotes]** (visas endast för företagsadministratören eller kontot med underordnade användare).

1. Klicka på **[!UICONTROL Show All Quotes]** om du vill se alla citat från alla företagsanvändare.

## Visa en offert

1. Kunden loggar in på sitt konto.

1. Välj **[!UICONTROL My Quotes]** i den vänstra panelen.

1. Söker efter citattecknet i listan och klickar på **[!UICONTROL View]** i kolumnen _[!UICONTROL Action]_.

## Skriva ut en offert

1. I den öppna offerten till höger om avsnittet _[!UICONTROL Items Quoted]_klickar kunden på&#x200B;**[!UICONTROL Print]**.

1. Verifierar **[!UICONTROL Destination]** som skrivare eller PDF.

1. Klicka på **[!UICONTROL Print]**.

## Avbryta en offertförfrågan

1. Klicka på **[!UICONTROL Close quote]** i den öppna citattecknet precis ovanför avsnittet Objekt som citerats.

   Begäran avbryts och offertstatusen ändras till `Closed`. Den stängda offerten finns kvar i din lista med offerter och finns kvar i listan i rutnätet _[!UICONTROL Quotes]_från administratören.

1. Om du vill ta bort det annullerade citattecknet från listan med citattecken klickar du på **[!UICONTROL Delete]**.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

   Det avslutande citattecknet tas bort från deras lista med citattecken. Den visas dock fortfarande i rutnätet _[!UICONTROL Quotes]_i Admin, med statusen `Closed`.

## Offertåtgärder

| Åtgärd | Beskrivning |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Byt namn | [!BADGE 1.5.0-beta-funktioner]{type=Informative url=&quot;/help/b2b/release-notes.md&quot; tooltip=&quot;Endast tillgängligt för Beta-programdeltagare&quot;} Ändra offertens namn |
| Skapa en kopia | [!BADGE 1.5.0-beta-funktioner]{type=Informative url=&quot;/help/b2b/release-notes.md&quot; tooltip=&quot;Endast tillgängligt för Beta-programdeltagare&quot;} En köpare kan skapa en ny offert från den aktuella offerten genom att kopiera och byta namn på den. |
| Stäng citat | När en köpare stänger en offert kan den inte öppnas igen. Vid behov kan köparen återskapa den genom att använda åtgärden [!UICONTROL Create Copy]. Det här alternativet är inte tillgängligt om offertstatusen är `Draft`. |
| Ta bort citat | När en köpare tar bort en offert tas den bort från systemet och är inte längre tillgänglig. |
| Skriv ut | Öppnar ett utskriftsformulär där du kan spara offerten som PDF, fil eller skriva ut den på en konfigurerad skrivare. |

## Kolumnbeskrivningar

| Kolumn | Beskrivning |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Quote Name] | Namnet som köparen tilldelat offertförfrågan. |
| [!UICONTROL Created] | Datumet då offertförfrågan skickades för första gången. |
| [!UICONTROL Created By] | Förnamn och efternamn på den köpare som skickade offertförfrågan. |
| [!UICONTROL Status] | Anger offertens status. Status för en offert kan bara ändras genom åtgärder från antingen köparen eller säljaren. <br/>**[!UICONTROL Submitted]**- Köparens anbudsförfrågan har inte öppnats av säljaren än. I det här läget kan köparen fortfarande ändra anbudsförfrågan. Tillgängliga åtgärder: `View` / `Close` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Pending]** - Säljaren har öppnat förfrågan och håller på att granska den och förbereda ett svar. Tillgängliga åtgärder: `View` / `Close` <br/>**[!UICONTROL Updated]**- säljaren har skickat ett svar till köparen och knappen _[!UICONTROL Proceed to Checkout]_är aktiverad. I det här läget kan köparen fortsätta att ändra offerten. Tillgängliga åtgärder: `View` / `Send for Review` / `Proceed to Checkout` / `Delete Quote` / `Close` / `Edit Quantity` / `Delete SKU` / `Add comments` / `Edit Shipping Address`<br/>**[!UICONTROL Open]**- Köparen uppdaterar fortfarande offerten och knappen_[!UICONTROL Proceed to Checkout]_ är inaktiverad. Tillgängliga åtgärder: `View` / `Send for Review` / `Delete Quote` / `Edit quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` <br/>**[!UICONTROL Ordered]**- Köparen har skickat en order baserat på det förhandlade offerten. Offerten är låst och kan inte redigeras. Tillgänglig åtgärd: Visa<br/>**[!UICONTROL Closed]** - Köparen har avslutat förhandlingen och avbryter offerten. Offerten är låst och kan inte redigeras av vare sig köpare eller säljare. Tillgängliga åtgärder: `View` / `Delete` <br/>**[!UICONTROL Declined]**- säljaren har avböjt anbudsförfrågan eller för att göra en föreslagen ändring under förhandlingsprocessen. En offert kan avvisas när som helst i arbetsflödet. Alla anpassade priser tas bort från offerten. Köparen kan fortsätta redigera offerten och skicka in den på nytt eller göra köpet med standardpriser för katalog. Tillgängliga åtgärder: `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Expired]** - Offertens livstid har gått ut. Alla föreslagna priser återställs. Köparen kan antingen slutföra köpet baserat på standardpriser för kataloger eller inleda en ny förhandlingsrunda. Tillgängliga åtgärder: `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` |

{style="table-layout:auto"}
