---
title: Förhandla om en offert
description: Lär dig mer om arbetsflöden för offertförhandlingar och hur du arbetar med köpare.
exl-id: 93efbc9d-da4d-4ff8-95c1-13848b68bc38
feature: B2B, Quotes
source-git-commit: 734290b9d609a173186325b418cd92cbf41b0efb
workflow-type: tm+mt
source-wordcount: '2040'
ht-degree: 0%

---

# Förhandla om en offert

Om [B2B-offerter är aktiverade](configure-quotes.md) i konfigurationen kan prisförhandling initieras av en auktoriserad köpare från ett företag eller en säljare.

Köparna initierar prisförhandlingsprocessen genom att [begära en offert](quote-request.md) från kundvagnen. Försäljningsrepresentanter kan initiera förhandlingar genom att [skapa ett utkast till offert för en köpare](sales-rep-initiates-quote.md), uppdatera offerten med de ursprungliga orderartiklarna och -priserna och skicka den till köparen.

När prisförhandlingen börjar visas citattecken i rutnätet [Offerter](quotes.md). Alla förhandlingar mellan köparen och säljaren äger rum via e-post och inleds och spåras utifrån offertens detaljvy.

Under förhandlingsprocessen kan säljaren göra följande från administratören:

- Lägg till eller ta bort produkter
- Ändra kvantiteten
- Använd en rabatt på radobjekt eller det totala priset
- Lägg till eller ändra leveranssätt
- Lägg till kommentarer
- Skicka den uppdaterade offerten till köparen eller spara som ett utkast

Köpare hanterar offertförhandlingsprocessen från butiken med [[!UICONTROL My Quotes]](account-dashboard-my-quotes.md). Medan offerten är öppen för granskning är dess status på köparens konto inställd på `Pending`. Köparen kan ändra och skicka offerten på nytt även om den har avvisats eller gått ut.

## Steg 1: Visa förfrågan

1. Gå till **[!UICONTROL Sales]** > **[!UICONTROL Quotes]** på sidlisten Admin.

   Den nya begäran visas i rutnätet _[!UICONTROL Quotes]_.

1. Klicka på **[!UICONTROL View]** i kolumnen _Åtgärder_.

   ![Ny offert](./assets/quote-grid-new.png){width="700" zoomable="yes"}

## Steg 2: Ändra offerten

1. Klicka på ikonen _Kalender_ (![Kalender-ikon](../assets/icon-calendar.png)) under _[!UICONTROL Quote & Account Information]_.

   ![Citat- och kontoinformation](./assets/quote-details-account-information.png){width="575" zoomable="yes"}

1. Välj en **[!UICONTROL Expiration Date]** som offert.

1. Bläddra ned till avsnittet _[!UICONTROL Quote Totals]_och uppdatera **[!UICONTROL Negotiated Price]**efter behov.

   ![Uppdatera förhandlat pris](./assets/quote-change-update-negotiated-price.png){width="600" zoomable="yes"}

   Om köparen ändrar kvantiteten för artiklar i offerten visas ett meddelande högst upp i offerten, som anger att listan över artiklar har ändrats och att det förhandlade priset måste uppdateras.

   ![Meddelande om ändring av offert](./assets/quote-change-notice.png){width="600" zoomable="yes"}

### Lägg till nya produkter i offerten

1. Klicka på **[!UICONTROL Add Products by SKU]**.

1. Ange **[!UICONTROL SKU]** och **[!UICONTROL Qty]** som ska läggas till.

   ![Lägg till i offert av SKU](./assets/quote-details-add-by-sku.png){width="600" zoomable="yes"}

### Tillämpa uppdateringar av radobjekt

Använd radobjektsändringar i avsnittet _[!UICONTROL Items Quoted]_om det behövs.

![Använd uppdateringar av radobjekt](./assets/quote-apply-line-item-operations.png){width="600" zoomable="yes"}

- Ändra **[!UICONTROL Quantity]** som måste köpas till föreslaget pris.

- Välj **[!UICONTROL Configure]** och ändra produktalternativen.

  Alternativet [!UICONTROL Configure] är bara tillgängligt på ett radobjekt för en konfigurerbar produkt

- Välj en åtgärd för att uppdatera objektet på menyn **[!UICONTROL Action]**:
   - **Rabattartikel** om du vill tillämpa en rabatt som en procentandel, ett fast belopp eller ett föredraget pris.
Du kan även låsa rabattbeloppet för att förhindra ytterligare rabatter. Om rabatten inte är låst
både radrabatt och rabatt på offertnivå tillämpas på produktpriset.
   - **Lämna en anteckning till köparen** för att ge köparen ytterligare information om ett objekt
   - **Ta bort** om du vill ta bort ett objekt från offerten.

### Tillämpa ändringar och uppdatera

- Klicka på **[!UICONTROL Add to Quote]** om du vill använda ändringarna.

- Klicka på **[!UICONTROL Recalculate the Quote]** om du vill uppdatera offerten.

- Om du vill tillämpa ändringarna och uppdatera offerten till den delade katalogen och prisreglerna klickar du på **[!UICONTROL Update Prices]** och sedan på **[!UICONTROL Proceed]** för att bekräfta uppdateringen.

  ![Objekt som citerats](./assets/quote-detail-items-quoted.png){width="600" zoomable="yes"}

### Uppdatera leveransinformation

1. Om köparen inkluderar en _leveransadress_ i offerten klickar du på **[!UICONTROL Get shipping methods and rates]**.

1. Välj leveranssätt bland de tillgängliga alternativen.

1. Ange **[!UICONTROL Proposed Shipping Price]**.

   _[!UICONTROL Quote Totals]_har uppdaterats för att återspegla det föreslagna leveranspriset.

### Bifoga ett stöddokument

1. Klicka på **[!UICONTROL Attach file]** under rutan _Lägg till din kommentar_.

   Som standard kan [bifogade filer](../configuration-reference/sales/quotes.md) vara upp till 2 MB i något av följande filformat: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG eller JPEG, PNG.

1. Välj filen i katalogen.

## Steg 3: Uppdatera offertnivåinformation och skicka ditt svar

1. I avsnittet _[!UICONTROL Negotiation]_på fliken_[!UICONTROL Comments]_ anger du ditt svar i avsnittet **[!UICONTROL Add your comment]**.

1. Om du vill inkludera ett stöddokument klickar du på **[!UICONTROL Attach file]** och väljer filen i din katalog.

   Den största tillåtna filstorleken för bilagor är 2 MB.

1. Så här tillämpar du en rabatt på hela offerten:

   - Välj någon av följande rabattyper under _[!UICONTROL Quote Totals]_i avsnittet_[!UICONTROL Negotiated Price]_:

      - `Percentage Discount`
      - `Amount Discount`
      - `Proposed Price`

   - Ange beloppet som en procentandel eller ett fast pris.

     ![Förhandlingskommentarer](./assets/quote-detail-negotiation-comments.png){width="600" zoomable="yes"}

1. Skicka eller spara offerten:

   - Om offerten är klar att skickas tillbaka till köparen klickar du på **[!UICONTROL Send]**.

   - Klicka på **[!UICONTROL Save as Draft]** om du vill fortsätta arbeta med offerten senare.

## Steg 4: Följ upp en offert

När du skickar en offert meddelas både köparen och säljaren som hanterar företagskontot. E-postmeddelandet innehåller en länk till offerten på köparens konto och offertens förfallodatum. Köparen kan när som helst under förhandlingarna göra något av följande:

- Godkänn offerten och slutför köpet.
- Skicka ett svar med ett räknarerbjudande och fortsätt förhandlingen.
- Avsluta förhandlingen.

Om du vill övervaka offertens position i arbetsflödet kontrollerar du din e-postadress och offertens status i rutnätet. Du kan fortsätta med förhandlingsprocessen så länge som det behövs.

## Knappfält

| Knapp | Beskrivning |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Back] | Återgår till sidan _[!UICONTROL Quotes]_utan att spara ändringarna. |
| [!UICONTROL Print] | Skickar offerten till en skrivare eller sparar den som en PDF-fil. |
| [!UICONTROL Create Copy] | [!BADGE 1.5.0-beta-funktioner]{type=Informative url=&quot;/help/b2b/release-notes.md&quot; tooltip=&quot;Tillgängligt endast för Beta-programdeltagare&quot;} Skapar och öppnar en kopia av det aktuella citattecknet med `(copy)` som tillägg till det ursprungliga namnet. Byt namn på den nya offerten genom att redigera fältet [!UICONTROL Name]. Bearbeta den nya offerten genom att spara den som ett utkast eller skicka den till kunden. |
| [!UICONTROL Save as Draft] | Spara ändringar som gjorts i offerten, men skicka inte tillbaka den till köparen. |
| [!UICONTROL Decline] | Avböjer begäran om att förhandla om priser, antingen på den inledande undersökningen eller under pågående förhandlingar. När en offert avvisas bör säljaren lägga till en kommentar som förklarar beslutet. När en offert avvisas återställs alla förhandlade priser till ursprungsvärdena. Den här knappen är inaktiverad medan säljaren väntar på ett svar från köparen. |
| [!UICONTROL Send] | Skickar den uppdaterade offerten som ett svar på köparens fråga. Den här knappen är inaktiverad om säljaren väntar på ett svar från köparen. |

{style="table-layout:auto"}

## Fältbeskrivningar

Citatinformation och funktioner i Admin är ordnade i följande avsnitt.

### [!UICONTROL Quote & Account Information]

| Fält | Beskrivning |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Name] | Namnet som tilldelats en offertförfrågan av [köparen](account-company-roles-permissions.md). |
| [!UICONTROL Status] | Anger offertens aktuella tillstånd. Status för en offert kan bara ändras genom åtgärder från antingen köparen eller säljaren. Se även [statusinställningarna](quotes.md) från administratören och [köparens konto](account-dashboard-my-quotes.md). |
| [!UICONTROL Created] | Datum och tid då köparen först skickade anbudsförfrågan. |
| [!UICONTROL Created By] | Förnamn och efternamn på den företagsköpare som skickade anbudsförfrågan. |
| [!UICONTROL Expiration Date] | Anger den sista dagen som den aktuella offerten är giltig. Standardförfallodatumet anges i konfigurationen till 30 dagar efter att en köpare har skickat in en anbudsförfrågan. <br/><br/>Säljaren kan åsidosätta standardförfallodatumet genom att ange ett annat datum (MMM DD YYYY) eller välja datumet i kalendern. Offerten upphör aldrig att gälla om fältet lämnas tomt. <br/><br/>För öppna offerter får säljaren ett [e-postmeddelande](../systems/email-templates.md) 48 timmar innan offerten är schemalagd att förfalla. Köpare meddelas 24 timmar före utgångsdatumet. <br/><br/>Statusen för offerten ändras till _Förfallen_ och köparen kan inte göra fler ändringar i offerten. De föreslagna priserna i offerten återgår till de ursprungliga värdena från katalogen. <br/><br/>Om en offert är öppen för granskning av säljaren när offerten är inställd på att förfalla, återställs förfallodatumet enligt det intervall som är inställt i konfigurationen. <br/><br/>Förfallodatumet är det enda fältet i avsnittet _Citat och konto_ som kan redigeras under granskningsprocessen. |
| [!UICONTROL Company] | Det juridiska namnet för det [företag](account-companies.md) som köparen representerar. |
| [!UICONTROL Company Admin Email] | E-postadressen till [företagets administratör](account-company-admin.md). |
| [!UICONTROL Sales Rep] | [säljaren](account-company-manage.md) som arbetar för säljaren och är den primära kontakten som tilldelats företagskontot. |
| [!UICONTROL Shared Catalog (or Customer Group)] | Den [delade katalogen](catalog-shared.md) eller [kundgruppen](account-company-customer-group.md) som företaget är tilldelat. Offerten kan innehålla anpassade priser från den delade katalogen som är tilldelad företaget. |

{style="table-layout:auto"}

### [!UICONTROL Add to Quote by SKU]

| Fält | Beskrivning |
|---------------------------|-----------------------------------------------------------|
| [!UICONTROL Enter SKU] | SKU:n för den produkt som ska läggas till i offerten. |
| [!UICONTROL Qty] | Antalet objekt i denna SKU som ska läggas till i offerten. |
| [!UICONTROL Add to Quote] | Lägger till den angivna produktkvantiteten i offerten. |

{style="table-layout:auto"}

### [!UICONTROL Items Quoted]

| Fält | Beskrivning |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Name & SKU] | Länkat produktnamn och lagerställeenhet. |
| [!UICONTROL Stock] | Antalet produkter under denna SKU som är tillgängliga för försäljning. |
| [!UICONTROL Cost] | Det belopp som säljaren betalade för att köpa produkten. |
| [!UICONTROL Catalog Price] | Priset på produkten i köparens katalog, baserat på kundgruppen eller den delade katalogen som är tilldelad köparens företag. |
| [!UICONTROL Cart Price] | Det ursprungliga priset för artikeln i vagnen, minus eventuella rabatter som tillämpas från vagnen. Kundvagnspriset kan skilja sig från katalogpriset om det finns rabatter eller kundvagnsregler som gäller för köparens kundgrupp. |
| [!UICONTROL Discount] | Radartikelrabatten som tillämpas på artikeln. Värdet kan vara en procentandel, ett fast belopp eller ett föreslaget pris. |
| [!UICONTROL Qty] | Antalet enheter i SKU:n som utgör basen för det angivna priset. Endast ett positivt tal större än noll kan anges. Om du vill ändra kvantiteten till noll tar du bort radobjektet från offerten. |
| [!UICONTROL Subtotal] | Det föreslagna priset multiplicerat med antalet beställda artiklar. |
| [!UICONTROL Estimated Tax] | Momsbeloppet som beräknas för den här radartikeln enligt konfigurationen. Beroende på inställningarna för momsberäkning kan den uppskattade momsen baseras på något av följande: Pris per enhet / Summa för rad / Summa |
| [!UICONTROL Subtotal (Incl./Excl. Tax)] | Beroende på konfigurationen kan den här kolumnen visa delsumman med eller utan uppskattad moms. |
| [!UICONTROL Action] | Markeringsmenyn för åtgärder som kan tillämpas på ett radobjekt:<ul><li>**[!UICONTROL Discount item]**</li><li>**[!UICONTROL Leave a note to Buyer]**</li><li>**[!UICONTROL Remove an item from the quote]**</li></ul>. |
| [!UICONTROL Configure] | Gör att du kan ändra produktalternativen för en konfigurerbar produkt. |
| [!UICONTROL Update Prices] | Uppdaterar offerten med de senaste ändringarna från den delade katalogen och prisreglerna. |
| [!UICONTROL Recalculate Quote] | Beräknar om alla offertpriser, kundvagnsprisregler och moms för att återspegla ändringar i offerten. |

{style="table-layout:auto"}

### [!UICONTROL Shipping Information]

| Fält | Beskrivning |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Shipping Address] | Visar den leveransadress som anges i köparens konto. Leveransadressen är tom om köparen inte angav någon adress innan begäran skickades. |
| [!UICONTROL Shipping Method & Price] | Länken Hämta leveransmetoder och fraktsatser visas om köparen inkluderar en _leveransadress_ i offerten. |

{style="table-layout:auto"}

### [!UICONTROL Negotiation]

| Fält | Beskrivning |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Comments] | Fliken Kommentarer i förhandlingsavsnittet används för att ange ett meddelande till köparen om offerten. <br/>**[!UICONTROL Add your comment]**- Kommentarerna används för att kommunicera med köparen under förhandlingsprocessen. Använd kommentarerna för att förklara eventuella rabatter som ges i offerten eller orsaken till att en offertförfrågan avvisas.<br/>**[!UICONTROL Attach file]** - Den maximala filstorleken och de filtyper som stöds för [bifogade filer](configure-quotes.md) bestäms av konfigurationen. Som standard kan en bifogad fil vara upp till 2 MB och av någon av följande filtyper: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG eller JPEG, PNG. |
| [!UICONTROL History Log] | På den här fliken visas en komplett historik över offerten med datum, offertstatus och kommentarer. |

{style="table-layout:auto"}

### [!UICONTROL Quote Totals]

| Fält | Beskrivning |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Total Cost] | Den totala kostnaden för säljaren av de artiklar som ingår i offerten. |
| [!UICONTROL Catalog Total Price  (Incl./Excl. Tax)] | Det totala priset för artiklarna i offerten utan moms, enligt priserna i den delade katalogen eller den primära katalogen som används som bas för offerten. Expandera avsnittet för att visa de värden som används i beräkningen, beroende på inställningen [Visa delsumma](../configuration-reference/sales/tax.md) i konfigurationen. Alternativ: <br/>**[!UICONTROL Subtotal (Excl. Tax)]**- Katalogens totala pris utan uppskattad moms.<br/>**[!UICONTROL Subtotal (Incl. Tax)]** - Katalogens totala pris utan uppskattad moms. <br/>**[!UICONTROL Estimated Tax]**- Momsbeloppet som beräknas gälla för katalogens totalpris. |
| Förhandlat pris | Rabatten som erbjuds köparen kan baseras på något av följande: <br/>**[!UICONTROL Percentage Discount]**- Rabatten i procent.<br/>**[!UICONTROL Amount Discount]** - Rabatten som ett fast belopp. <br/>**[!UICONTROL Proposed Price]**- Det pris som säljaren föreslår.<p>Om alla artiklar i offerten har en låst artikelrabatt inaktiveras avsnittet [!UICONTROL Negotiated Price] eftersom ingen ytterligare rabatt kan tillämpas.</p><p>Om en produkt har en rabatt på radobjekt som inte är låst tillämpas både rabatten på radobjektet och rabatten på offertnivån på produktpriset.</p> |
| [!UICONTROL Quote Subtotal (Incl./Excl. Tax)] | Det totala föreslagna priset för varje radartikel i offerten, antingen med eller utan moms, beroende på inställningarna för [momsberäkning](../configuration-reference/sales/tax.md) i konfigurationen. |
| [!UICONTROL Shipping & Handling] | Det belopp som säljaren angett i fältet Föreslaget leveranspris i avsnittet Leveransinformation i offerten. Om fältet är tomt baseras beloppet på den valda leveransmetoden. |
| [!UICONTROL Estimated Tax] | Momsbeloppet som beräknas förfalla enligt inställningarna i [visningsinställningarna](../configuration-reference/sales/tax.md). |
| [!UICONTROL Quote Grand Total (Incl. Tax)] | Slutsumman längst ned i offerten som innehåller förhandlat pris, uppskattad moms samt föreslagen frakt och hantering. |

{style="table-layout:auto"}
