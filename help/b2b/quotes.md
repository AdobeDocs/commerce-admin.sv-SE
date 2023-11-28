---
title: Förhandlingsbara offerter
description: Lär dig mer om arbetsflöden för offerter och hur du kan tillhandahålla den här tjänsten till dina företagskonton.
exl-id: c278818b-fa5a-4e7a-8ca2-c4b757da4f05
feature: B2B, Quotes
source-git-commit: 27b0c43f72faa2c2e8717fd5929f36d12f9e1b08
workflow-type: tm+mt
source-wordcount: '1601'
ht-degree: 0%

---

# Förhandlingsbara offerter

Köpare och säljare använder offerter för att hantera förhandlingsprocessen för att lägga till beställningar, uppdatera kvantiteter, begära och tillämpa rabatter och så vidare - tills de når en överenskommelse. Offertförhandlingen kan initieras av en auktoriserad företagsköpare eller av en företagssäljare.

Offerter kan initieras av en auktoriserad företagsköpare eller en säljare. När offerten har skapats börjar förhandlingsprocessen när köparen eller säljaren skickar offerten för granskning. The _Citat_ rutnät som visar varje mottagen offert och som bevarar en historik över kommunikationen mellan köpare och säljare. Använd standarden [arbetsplatskontroller](../getting-started/admin-workspace.md) om du vill filtrera listan, ändra kolumnlayouten, spara vyer och exportera data.

- I butiken skickar köparna offerten som [Begäran om förhandling](quote-price-negotiation.md) priset från kundvagnen. När en köpare skapar en offertförfrågan kan han eller hon spara offerten som ett utkast eller skicka den direkt till säljaren.

- I Admin kan säljare skapa offerter för företagsköparens räkning. När en säljare skapar offerten kan han eller hon spara offerten som ett utkast eller skicka den direkt till köparen för att inleda förhandlingsprocessen.

Under förhandlingsprocessen kan offerten bara uppdateras av personen som granskar och föreslår villkor för vidare förhandling.

## Förutsättningar

Förhandlingsbara offerter är bara tillgängliga om Adobe Commerce har följande konfigurationsinställningar:

- [Tillägget B2B för Adobe Commerce är installerat](install.md)
- [Konfigurerade B2B-funktioner](enable-basic-features.md)
   - Aktivera företagskonton
   - Aktivera B2B-citat

## Arbetsflöde för offert

Offerter kan initieras av köparen eller säljaren.

**Steg 1: Skapa offert**

- **Köparens anbudsförfrågan** - köparen [begär en offert](quote-request.md) från kundvagnen. Förfrågan visas i _Mina offerter_ listan i köparens kontonamall och e-postmeddelandet skickas till säljaren som är tilldelad företagskontot. I Admin visas begäran i _Citat_ rutnät, med statusen `New`. Köparen kan ändra en anbudsförfrågan tills den öppnas av säljaren.

  ![Citat](./assets/quote-request-from-shopping-cart.png){width="700" zoomable="yes"}


- **Säljare** — En säljare kan [skapa en offert](sales-rep-initiates-quote.md) från Admin för en specifik företagsköpare. Säljaren måste uppdatera offerten för att kunna lägga till produkter och annan information som rabatter och anteckningar till köparen. Försäljningsrepresentationen kan spara offerten som en `draft` eller skicka det till köparen för att påbörja förhandlingen. I utkastläge är offerten bara synlig för säljaren. När offerten har skickats är statusen `Submitted`. Den kan inte ändras av säljaren förrän köparen skickar tillbaka den.

  ![Säljare som initierar en köpoffert från rastret Offerter i administratören](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}


**Steg 2: Offertgranskning och förhandling**

**Säljaren visar förfrågan och skickar svar** - I administratören ser säljaren anbudsförfrågan. Offertens status ändras till `Pending`och köparen inte kan göra några ändringar. The [säljarsvar](quote-price-negotiation.md) genom att erbjuda rabatterade priser för produkterna i offerten, anger en kommentar och skickar tillbaka offerten till köparen. Köparen och säljaren meddelas via e-post att säljaren har svarat.

**Köparens vycitat från säljaren och skickar svar** - Köparen klickar på länken i e-postmeddelandet för att öppna offerten eller öppnar offerten från _Mina offerter_ sidan på kontouppsättningen. Köparen kan lämna noteringar till säljaren på radobjekt- eller offertnivå och ta bort artiklar.

Köparen och säljaren kan fortsätta förhandlingsprocessen tills ett avtal nås eller säljaren avvisar offerten. Om köparen gör ändringar i offerten - lägger till eller tar bort produkter eller ändrar produktkvantiteter - måste offerten skickas tillbaka till säljaren för granskning.

**Steg 4: Köparen accepterar offerter** - Köparen godtar det föreslagna priset och fortsätter att handla. Det går inte att lägga till ytterligare rabatter i det förhandlade offerten.

## B2B-rollresurser för butiksofferter

Konfigurationsalternativen för citattecken styrs med [rollresurser](../systems/permissions-user-roles.md#role-resources). Dessa rollresurser måste anges för den administratörsanvändarroll som tilldelas butiksadministratören.

Om du vill ge åtkomst till offertfunktioner i administratören går du till **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, väljer rollen och navigerar till [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] i_ Rollresurser _träd.

## Använda en åtgärd

I Admin kan B2B-administratörer och säljare hantera offerter från offertstödrastret med hjälp av [!UICONTROL Actions] -menyn.

![Citat](./assets/quotes-grid.png){width="700" zoomable="yes"}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Sales]** > **[!UICONTROL Quotes]**.

1. I stödrastrets första kolumn markerar du kryssrutan för varje post som du vill använda åtgärden på.

1. I **[!UICONTROL Actions]** välj den åtgärd som ska användas.

### Visa en offert

1. I **[!UICONTROL Actions]** kolumn för en post klickar du på **[!UICONTROL View]**.

1. Följ instruktionerna och börja med [prisförhandling](quote-price-negotiation.md) -processen.

### Visa offertaktivitet

Visa förhandlingens tidslinje, kommunikation och annan offertaktivitet från [!UICONTROL Comments] och [!UICONTROL History Log]—information innehåller statusändringar, uppdateringar av kund- och leveransinformation, artikel- och prisuppdateringar samt annan viktig information.

1. Öppna en offert.

1. Visa offertförhandlingskommentarer och historik genom att bläddra till **[!UICONTROL Negotiation]** och markera **[!UICONTROL Comments]** och **[!UICONTROL History Log]**.

   ![Visa historik](./assets/quote-view-history.png){width="400"}

1. Händelser spåras också på radobjektnivå.

   ![Visa radartikelhistorik](./assets/quote-view-line-item-history.png){width="400"}


### Avslå en anbudsförfrågan

Endast offertförfrågningar med `Open` status kan avvisas.

1. Markera varje öppen offertförfrågan som du vill avvisa.

1. Ange _[!UICONTROL Actions]_styra till `Declined`.

1. Ange anledningen till att offerten avvisades och klicka på **[!UICONTROL Confirm]**.

   ![Vill du avböja offert?](./assets/quote-decline-confirm.png){width="400"}


## Kolumnbeskrivningar

| Kolumn | Beskrivning |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Select] | Markera kryssrutan eller använd markeringskontrollen i kolumnrubriken för att välja de citattecken som ska bli en åtgärd. Alternativ: Markera allt/Avmarkera allt |
| [!UICONTROL ID] | En unik numerisk identifierare som tilldelas när en anbudsförfrågan skickas från en köpares kundvagn. När du visar offertinformationen visas ID:t högst upp på sidan i stället för offertnamnet. |
| [!UICONTROL Name] | Namnet som tilldelats en offertförfrågan av köparen. |
| [!UICONTROL Created Date] | Datum och tid då köparen först skickade anbudsförfrågan. |
| [!UICONTROL Company] | Namnet på det företag för vilket en köpare lämnar en anbudsförfrågan. |
| [!UICONTROL Submitted By] | Förnamn och efternamn på den företagsköpare som skickar en anbudsförfrågan. |
| [!UICONTROL Last Updated] | Datum och tid för den senaste kommunikationen mellan köpare och säljare om offerten. |
| [!UICONTROL Sales Rep] | Förnamn och efternamn på säljaren som hanterar köparens konto. |
| [!UICONTROL Quote Total (Base)] | Det totala priset på produkter som ska köpas baserat på den ursprungliga offerten. Det totala beloppet visas i webbplatsens basvaluta och i butikens valuta. |
| [!UICONTROL Quote Total (Negotiated)] | Det totala priset på produkter som ska köpas baserat på den förhandlade offerten. Summan beräknas automatiskt av systemet och inkluderar alla radobjekt- eller offertnivårabatter som säljaren tillämpar. Det totala beloppet visas i webbplatsens basvaluta och i butikens valuta. |
| [!UICONTROL Status] | Anger det aktuella tillståndet för en offertförfrågan. Status för en offert kan bara ändras genom åtgärder från antingen köparen eller säljaren. Se även statusinställningarna i [köparkonto](account-dashboard-my-quotes.md).<ul><li>**[!UICONTROL New]** - Köparen har lämnat in en anbudsförfrågan, men den har inte visats av säljaren. Förfrågan kan uppdateras av köparen tills den öppnas av säljaren.</li><li>**[!UICONTROL Draft]** - Säljaren skapar ett utkast till offert för en köpare. Offerten visas inte för köparen förrän säljaren lägger till erbjudandeinformationen (artiklar, kvantitet, rabatt och så vidare) och skickar offerten till köparen.</li> <li>**[!UICONTROL Open]** - Säljaren öppnade förfrågan och håller på att granska den och förbereda ett svar. </li><li>**[!UICONTROL Submitted]** - Säljaren skickade ett svar till köparen. Det går inte att redigera offertposten under förhandlingsprocessen.</li><li>**[!UICONTROL Client Reviewed]** - Köparen såg säljarens svar och håller på att förbereda ett svar.</li><li>**[!UICONTROL Updated]** - Köparen lämnade ett svar, men det har inte visats av säljaren.</li><li>**[!UICONTROL Ordered]** - Köparen lämnade in beställningen baserat på det framförhandlade offerten.</li><li>**[!UICONTROL Closed]** - Köparen avbröt offertförfrågan.</li><li>**[!UICONTROL Declined]** - Säljaren avböjde anbudsförfrågan. Alla anpassade priser tas bort från offerten och posten låses för ytterligare redigeringar.</li><li>**[!UICONTROL Expired]** - Köparen svarade inte på säljarens svar inom den angivna tidsperioden och offerten är inte längre giltig.</li></ul> |
| [!UICONTROL Actions] | **[!UICONTROL View]** - Öppnar anbudsförfrågan och sparar en post för förhandlingen mellan köpare och säljare. |

{style="table-layout:auto"}

## Knappfält

| Knapp | Beskrivning |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Send] | Skickar den uppdaterade offerten som ett svar på köparens fråga. Den här knappen är inaktiverad om säljaren väntar på ett svar från köparen. |
| [!UICONTROL Back] | Återgår till _Citat_ utan att spara ändringarna. |
| [!UICONTROL Create Copy] | [!BADGE Funktioner för 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Endast tillgängligt för betaprogramdeltagare"}`<original quote name> (copy)`. Ändra namnet genom att redigera värdet i [!UICONTROL Name] och spara offerten som ett utkast. |
| [!UICONTROL Print] | Skickar offerten till en skrivare eller sparar den som en PDF-fil. |
| [!UICONTROL Create a copy] | Skapar en kopia av offerten med namnet `<original quote name> (copy)` och öppnar den. Byt namn på och uppdatera den nya offerten efter behov innan du sparar den som ett utkast eller skickar den till köparen. |
| [!UICONTROL Save as Draft] | Sparar ändringar som gjorts i offerten, men skickar den inte tillbaka till köparen. |
| [!UICONTROL Decline] | Avböjer begäran om att förhandla om priser, antingen på den inledande undersökningen eller under pågående förhandlingar. När en offert avvisas bör säljaren lägga till en kommentar som förklarar beslutet. När en offert avvisas återställs alla förhandlade priser till ursprungsvärdena. Den här knappen är inaktiverad medan säljaren väntar på ett svar från köparen. |

{style="table-layout:auto"}

## Exempel på citat

I följande bild visas ett exempel på offertdetaljvyn i Admin med vissa inställningar konfigurerade.

![Exempel på citat](./assets/quote-full.png){width="700" zoomable="yes"}


>[!NOTE]
>
>[!BADGE Funktioner för 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Endast tillgängligt för betaprogramdeltagare"}
