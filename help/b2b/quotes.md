---
title: Förhandlingsbara offerter
description: Lär dig mer om arbetsflöden för offerter och hur du kan tillhandahålla den här tjänsten till dina företagskonton.
exl-id: c278818b-fa5a-4e7a-8ca2-c4b757da4f05
feature: B2B, Quotes
source-git-commit: 7f4993ff8b16beda2a371737fb5a8ecb5f9c9396
workflow-type: tm+mt
source-wordcount: '1269'
ht-degree: 0%

---

# Förhandlingsbara offerter

Köpare och säljare använder offerter för att hantera förhandlingsprocessen för att lägga till beställningar, uppdatera kvantiteter, begära och tillämpa rabatter och så vidare - tills de når en överenskommelse. Offertförhandlingen kan initieras av en auktoriserad företagsköpare eller av en företagssäljare.

![Listvy för citattecken i Admin](./assets/quotes-admin-list-view-intro.png){width="700" zoomable="yes"}

När offerten har skapats börjar förhandlingsprocessen när köparen eller säljaren skickar offerten för granskning. Rutnätet _Offerter_ som listar varje mottagen offert och underhåller en historik över kommunikationen mellan köpare och säljare. Använd standardkontrollerna för [arbetsplats](../getting-started/admin-workspace.md) för att filtrera listan, ändra kolumnlayouten, spara vyer och exportera data.

- I butiken skickar köparna offerten som en [förfrågan om att förhandla](quote-price-negotiation.md) om priset från kundvagnen. När en köpare skapar en offertförfrågan kan han eller hon spara offerten som ett utkast eller skicka den direkt till säljaren.

- I Admin kan säljare skapa offerter för företagsköparens räkning. När en säljare skapar offerten kan han eller hon spara offerten som ett utkast eller skicka den direkt till köparen för att inleda förhandlingsprocessen.

Under förhandlingsprocessen kan offerten bara uppdateras av personen som granskar och föreslår villkor för vidare förhandling.

## Förutsättningar

Förhandlingsbara offerter är bara tillgängliga om Adobe Commerce har följande konfigurationsinställningar:

- [Adobe Commerce B2B-tillägget är installerat](install.md)
- [Konfigurerade B2B-funktioner](enable-basic-features.md)
   - Aktivera företagskonton
   - Aktivera B2B-citat

## Arbetsflöde för offert

Offerter kan initieras av köparen eller säljaren.

I det här diagrammet visas offertstatus för en köpare och säljare (Admin) i de olika stegen när du initierar en offert.

![Offerter, statusarbetsflöde](./assets/quote-status-workflow.svg){width="700" zoomable="yes"}

**Steg 1: Skapa offert (ny)**

- **Köparen begär offert** - Köparen [begär en offert](quote-request.md) från kundvagnen. Begäran visas i listan _Mina offerter_ på kontouppsättningen för köparen och e-postmeddelanden skickas till säljaren som är tilldelad företagskontot. I Admin visas begäran i rutnätet _Quotes_ med statusen `New`. Köparen kan ändra en anbudsförfrågan tills den öppnas av säljaren.

  ![Citattecken](./assets/quote-request-from-shopping-cart.png){width="700" zoomable="yes"}

- **Försäljningsrepresentant** - En säljare kan [skapa en offert](sales-rep-initiates-quote.md) från administratören för en specifik företagsköpare. Säljaren måste uppdatera offerten för att kunna lägga till produkter och annan information som rabatter och anteckningar till köparen. Försäljningsrepresentationen kan spara offerten som `draft` eller skicka den till köparen för att påbörja förhandlingen. I utkastläge är offerten bara synlig för säljaren. När offerten har skickats är statusen `Submitted`. Den kan inte ändras av säljaren förrän köparen skickar tillbaka den.

  ![Säljare som initierar en inköpsoffert från rastret Offerter i administratören](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}

**Steg 2: Offertgranskning och förhandling (granskning)**

Granskning eller förhandling av en offert kan omfatta ändrade kvantiteter, borttagning av artiklar, tillägg av radartikelkommentarer, användning av radobjekt- eller offertrabatter (säljare) och tillägg av en leveransadress (köpare).

- **Säljaren visar förfrågan och skickar svar** - I administratören ser säljaren anbudsförfrågan. I butiken ändras offertens status till `Pending` och köparen kan inte göra några ändringar. [säljaren svarar](quote-price-negotiation.md) genom att erbjuda prisrabatter och justera kvantiteter och artiklar efter behov, anger en kommentar och skickar offerten tillbaka till köparen. Köparen och säljaren meddelas via e-post att säljaren har svarat.

- **Köparen visar offert från säljaren och skickar svar** - Köparen klickar på länken i e-postmeddelandet för att öppna offerten eller öppnar offerten från sidan _Mina offerter_ på kontonamanelen. Köparen kan lämna noteringar till säljaren på rad- eller offertnivå, ändra kvantiteter och ta bort artiklar.

Köparen och säljaren kan fortsätta förhandlingsprocessen tills ett avtal nås eller säljaren avvisar offerten. Om köparen gör ändringar i offerten - lägger till eller tar bort produkter eller ändrar produktkvantiteter - måste offerten skickas tillbaka till säljaren för granskning.

- **Köparen lägger till en leveransadress** - Köparen kan lägga till en leveransadress i offerten. När köparen har lagt till adressen kan säljaren tillhandahålla alternativ för frakt och leverans. Vilka leveransmetoder som visas beror på konfigurationen för Storefront.

Om köparen lägger till en leveransadress, måste förhandlingsavtalet granskas och säljaren kan fortsätta förhandlingsprocessen tills ett avtal nås eller säljaren avvisar offerten.

**Steg 3: Köparen accepterar offert (utcheckning)**

Köparen godtar det föreslagna priset och fortsätter till kassan. Det går inte att lägga till ytterligare rabatter i det förhandlade offerten.

Leveransalternativen är låsta vid utcheckning.

## Offertstatus

Offertstatus ger information om det aktuella läget för offerten i offertarbetsflödet. Statusen för en offert ändras bara när en köpare eller säljare utför en åtgärd på offerten. Statusen ändras till exempel till en beställning om en köpare väljer [!UICONTROL Proceed to Checkout] för en aktiv offert.

- *[!UICONTROL New]** - Köparen skickade en anbudsförfrågan, men den har inte visats av säljaren. Förfrågan kan uppdateras av köparen tills den öppnas av säljaren.

- **[!UICONTROL Draft]** - Säljaren skapar ett utkast till offert för en köpare. Offerten visas inte för köparen förrän säljaren lägger till erbjudandeinformationen (artiklar, kvantitet, rabatt och så vidare) och skickar offerten till köparen.

- **[!UICONTROL Open]** - Säljaren öppnade förfrågan och håller på att granska den och förbereda ett svar

- **[!UICONTROL Submitted]** - Säljaren skickade ett svar till köparen. Det går inte att redigera offertposten under förhandlingsprocessen.

- **[!UICONTROL Client Reviewed]** - Köparen visade säljarens svar och håller på att förbereda ett svar.

- **[!UICONTROL Updated]** - Köparen skickade ett svar, men den har inte visats av säljaren.

- **[!UICONTROL Ordered]** - Köparen skickade ordern baserat på det förhandlade offerten.

- **[!UICONTROL Closed]** - Köparen avbröt offertförfrågan.

- **[!UICONTROL Declined]** - Säljaren avvisade anbudsförfrågan. Alla anpassade priser tas bort från offerten och posten låses för ytterligare redigeringar.

- **[!UICONTROL Expired]** - Köparen svarade inte på säljarens svar inom den angivna tidsperioden och offerten är inte längre giltig.

## B2B-rollresurser för butiksofferter

Konfigurationsalternativen för offerter styrs med [rollresurserna](../systems/permissions-user-roles.md#role-resources). Dessa rollresurser måste anges för den administratörsanvändarroll som tilldelas butiksadministratören.

Om du vill ge åtkomst till offertfunktioner i Admin går du till **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, markerar rollen och navigerar till [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] i trädet_ Rollresurser _.

![Offertar roller och behörigheter](./assets/roles-permissions-quotes.png){width="700" zoomable="yes"}

## Använda en åtgärd

I Admin kan B2B-administratörer och säljare hantera offerter från offertstödrastret via menyn [!UICONTROL Actions].

![Citattecken](./assets/quotes-grid.png){width="700" zoomable="yes"}

1. Gå till **[!UICONTROL Sales]** > **[!UICONTROL Quotes]** på sidofältet _Admin_.

1. I stödrastrets första kolumn markerar du kryssrutan för varje post som du vill använda åtgärden på.

1. I **[!UICONTROL Actions]** väljer du den åtgärd som ska användas.

### Visa en offert

1. Klicka på **[!UICONTROL View]** i kolumnen **[!UICONTROL Actions]** för en post.

1. Om du vill svara på kundens begäran följer du instruktionerna och påbörjar [prisförhandlingen](quote-price-negotiation.md).

### Visa offertaktivitet

Visa förhandlingens tidslinje, kommunikation och annan offertaktivitet från [!UICONTROL Comments] och [!UICONTROL History Log] - informationen innehåller statusändringar, uppdateringar av kund- och leveransinformation, artikel- och prisuppdateringar och annan viktig information.

1. Öppna en offert.

1. Visa kommentarer och historik för offertförhandling genom att bläddra till **[!UICONTROL Negotiation]** och välja **[!UICONTROL Comments]** och **[!UICONTROL History Log]**.

   ![Visa historik](./assets/quote-view-history.png){width="400"}

1. Händelser spåras också på radobjektnivå.

   ![Visa historik för radobjekt](./assets/quote-view-line-item-history.png){width="400"}


### Avslå en anbudsförfrågan

Endast offertförfrågningar med statusen `Open` kan avvisas.

1. Markera varje öppen offertförfrågan som du vill avvisa.

1. Ställ in kontrollen _[!UICONTROL Actions]_på `Declined`.

1. Ange anledningen till att offerten avvisades när du uppmanas till detta och klicka på **[!UICONTROL Confirm]**.

   ![Avböj offert?](./assets/quote-decline-confirm.png){width="400"}
