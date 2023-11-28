---
title: '[!UICONTROL My Quotes]'
description: Lär dig mer om kundupplevelsen för offerter, som finns på deras kontouppsättning.
exl-id: 137f0a99-8f24-4838-b54b-b0ef2c39a32a
feature: B2B, Companies, Quotes
source-git-commit: 27b0c43f72faa2c2e8717fd5929f36d12f9e1b08
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---


# [!UICONTROL My Quotes]

Om citattecken är aktiverade visas _[!UICONTROL My Quotes]_i kundkontots kontrollpanel listas alla offerter som kunden har skickat in. Beroende på deras tillstånd kan bara köpare som gör inköp för ett företags räkning skicka in begäranden om att förhandla om priset på ett köp.

![Mina offerter](./assets/account-dashboard-my-quotes.png){width="700" zoomable="yes"}

Köparen påbörjar processen av [skicka en förfrågan](quote-request.md) till en offert från kundvagnen. E-post utbyts mellan köparen och säljaren under [förhandlingsprocess](quote-price-negotiation.md). För köparen gäller följande: [!UICONTROL My Quotes] sidan är fokuspunkten för all kommunikation mellan köpare och säljare under förhandlingsprocessen. En köpare som accepterar det förhandlade pris som säljaren erbjuder kan gå direkt till utcheckningssidan från offerten. Det går inte att lägga till ytterligare rabatter i det förhandlade offerten.

En köpare kan slutföra följande åtgärder när han eller hon förhandlar om en offert:

* Granska artikelpriser och uppdateringar
* Spåra förhandlingsprocessen från [!UICONTROL Comments] och [!UICONTROL History] avsnitt
* Ändra offerten för att ta bort objekt
* Kommunicera och förhandla med säljaren genom att lägga till anteckningar på radobjektsnivå och offertnivå
* Skicka offert till säljare för granskning
* Konvertera offerten till en order om villkoren är godtagbara
* Stäng citattecknet
* Ta bort offerten
* [!BADGE Funktioner för 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Endast tillgängligt för betaprogramdeltagare"}

I följande exempel visas en offert som har uppdaterats av köparen och skickats tillbaka till säljaren för granskning.


![Köparvy över offert](./assets/account-dashboard-my-quote-detail.png){width="700" zoomable="yes"}

Citat med `Updated` status är låst tills säljaren returnerar offerten.

## Visa citattecken

Med de [behörigheter för deras roll](account-company-roles-permissions.md), kunder som är kopplade till ett företagskonto kan se offerter som begärts av [underordnade användare](account-company-structure.md). Företagsadministratörer kan se alla offerter för företagskontot.

1. Kunden loggar in på sitt konto i butiken.

1. Klickningar **[!UICONTROL My Quotes]** i den vänstra navigeringen.

1. Om du vill se alla citattecken de har skapat klickar du på **[!UICONTROL Show My Quotes]** länk (visas endast för företagsadministratören eller kontot med underordnade användare).

1. Om du vill se alla citat från alla företagsanvändare klickar du på **[!UICONTROL Show All Quotes]**.

## Visa en offert

1. Kunden loggar in på sitt konto.

1. I den vänstra panelen väljer **[!UICONTROL My Quotes]**.

1. Söker efter offerten i listan och klickar **[!UICONTROL View]** i _[!UICONTROL Action]_kolumn.

## Skriva ut en offert

1. I det öppna citattecknet till höger om _[!UICONTROL Items Quoted]_-avsnittet, kunden klickar **[!UICONTROL Print]**.

1. Verifierar **[!UICONTROL Destination]** som antingen skrivare eller PDF.

1. Klickningar **[!UICONTROL Print]**.

## Avbryta en offertförfrågan

1. Klicka på i den öppna citattecknet precis ovanför avsnittet Objekt som citerats **[!UICONTROL Close quote]**.

   Begäran avbryts och offertstatusen ändras till `Closed`. Det stängda citattecknet finns kvar i din lista över citattecken och finns kvar i listan i _[!UICONTROL Quotes]_från Admin.

1. Om du vill ta bort det annullerade citattecknet från listan med citattecken klickar du på **[!UICONTROL Delete]**.

1. När du uppmanas att bekräfta klickar du **[!UICONTROL OK]**.

   Det avslutande citattecknet tas bort från deras lista med citattecken. Den finns dock kvar på listan _[!UICONTROL Quotes]_i Admin, med `Closed` status.

## Offertåtgärder

| Åtgärd | Beskrivning |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Byt namn | [!BADGE Funktioner för 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Endast tillgängligt för betaprogramdeltagare"} |
| Skapa en kopia | [!BADGE Funktioner för 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Endast tillgängligt för betaprogramdeltagare"} |
| Stäng citat | När en köpare stänger en offert kan den inte öppnas igen. Vid behov kan köparen återskapa den med hjälp av [!UICONTROL Create Copy] åtgärd. Det här alternativet är inte tillgängligt om offertstatusen är `Draft`. |
| Ta bort citat | När en köpare tar bort en offert tas den bort från systemet och är inte längre tillgänglig. |
| Skriv ut | Öppnar ett utskriftsformulär där du kan spara offerten som PDF, fil eller skriva ut den på en konfigurerad skrivare. |

## Kolumnbeskrivningar

| Kolumn | Beskrivning |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Quote Name] | Namnet som köparen tilldelat offertförfrågan. |
| [!UICONTROL Created] | Datumet då offertförfrågan skickades för första gången. |
| [!UICONTROL Created By] | Förnamn och efternamn på den köpare som skickade offertförfrågan. |
| [!UICONTROL Status] | Anger offertens status. Status för en offert kan bara ändras genom åtgärder från antingen köparen eller säljaren. <br/>**[!UICONTROL Submitted]**- Köparens anbudsförfrågan har ännu inte öppnats av säljaren. I det här läget kan köparen fortfarande ändra anbudsförfrågan. Tillgängliga åtgärder: `View` / `Close` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Pending]** - Säljaren har öppnat förfrågan och håller på att granska den och förbereda ett svar. Tillgängliga åtgärder: `View` / `Close` <br/>**[!UICONTROL Updated]**- Säljaren har skickat ett svar till köparen och _[!UICONTROL Proceed to Checkout]_knappen är aktiverad. I det här läget kan köparen fortsätta att ändra offerten. Tillgängliga åtgärder: `View` / `Send for Review` / `Proceed to Checkout` / `Delete Quote` / `Close` / `Edit Quantity` / `Delete SKU` / `Add comments` / `Edit Shipping Address`<br/>**[!UICONTROL Open]**- Köparen uppdaterar fortfarande offerten och_[!UICONTROL Proceed to Checkout]_ knappen är inaktiverad. Tillgängliga åtgärder: `View` / `Send for Review` / `Delete Quote` / `Edit quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` <br/>**[!UICONTROL Ordered]**- Köparen har lämnat in en beställning baserad på det framförhandlade offerten. Offerten är låst och kan inte redigeras. Tillgänglig åtgärd: Visa<br/>**[!UICONTROL Closed]** - Köparen har avslutat förhandlingen och avbryter offerten. Offerten är låst och kan inte redigeras av vare sig köpare eller säljare. Tillgängliga åtgärder: `View` / `Delete` <br/>**[!UICONTROL Declined]**- Säljaren har avböjt anbudsförfrågan eller att göra en föreslagen ändring under förhandlingsprocessen. En offert kan avvisas när som helst i arbetsflödet. Alla anpassade priser tas bort från offerten. Köparen kan fortsätta redigera offerten och skicka in den på nytt eller göra köpet med standardpriser för katalog. Tillgängliga åtgärder: `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Expired]** - Offertens livstid har gått ut. Alla föreslagna priser återställs. Köparen kan antingen slutföra köpet baserat på standardpriser för kataloger eller inleda en ny förhandlingsrunda. Tillgängliga åtgärder: `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` |

{style="table-layout:auto"}
