---
title: Returnerar
description: Lär dig mer om arbetsflödet för returer och att utfärda en returnerad varuauktorisering.
exl-id: 9dde0360-aa99-4fc4-92ff-976d9874ffec
feature: Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# Returnerar

A _returnerad varuauktorisering_ (RMA) kan beviljas kunder som begär att få returnera en artikel för ersättning eller återbetalning. Normalt kontaktar kunden handlaren för att begära en återbetalning. Om det godkänns tilldelas det ett unikt RMA-nummer som identifierar den returnerade produkten. I konfigurationen kan du antingen aktivera RMA för alla produkter eller bara tillåta RMA för vissa produkter. The _[!UICONTROL Returns]_rutnätet visar de aktuella returnerade varuförfrågningarna (RMA) och används för att ange nya returförfrågningar.

![Returnerar rutnät](./assets/return.png){width="600" zoomable="yes"}

RMA-nummer kan utfärdas för enkla, grupperade, konfigurerbara och paketerade produkttyper. RMA-nummer är dock inte tillgängliga för virtuella produkter, hämtningsbara produkter och presentkort.

## Kolumnbeskrivningar

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Select] | Markera kryssrutorna för returer som ska bli föremål för en åtgärd, eller använd markeringskontrollen i kolumnrubriken. Alternativ: `Select All` / `Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL RMA] | En unik numerisk identifierare som tilldelas varje retur |
| [!UICONTROL Requested] | Datum och tid då returen placerades |
| [!UICONTROL Order] | Ett unikt nummer för den ursprungliga ordern |
| [!UICONTROL Ordered] | Datum och tid då ordern lades |
| [!UICONTROL Customer] | Namnet på den kund eller köpare som lade ordern |
| [!UICONTROL Status] | Returstatus. Alternativ: `Pending` / `Authorized` / `Partially Authorized` / `Approved` / `Rejected` / `Processed and Closed` / `Closed` |
| [!UICONTROL Action] | **[!UICONTROL View]** öppnar returen i redigeringsläge. |

{style="table-layout:auto"}

## Arbetsflöde för RMA och retur

1. **Ta emot begäran** - Om [aktiverad](rma-configure.md#enable-rmas-for-your-store) för butiken kan både registrerade kunder och gäster begära en RMA. Du kan också [skicka en RMA-begäran i administratören](#create-a-return-request-in-the-admin).

2. **RMA utfärdad** - När du har övervägt begäran kan du auktorisera den delvis, helt eller avbryta den. Om du godkänner returen och godkänner att betala för returleveransen, kan du skapa en leveransorder från administratören med en leverantör som stöds.

3. **Mottagen varuexponering och produktretur har bearbetats** - Följande flödesschema beskriver den operativa ordern för att slutföra returprocessen:

   ![Arbetsflöde för produktretur](./assets/workflow-customer-returns.png){width="500"}

## RMA-status

Under livscykeln kan en returnerad varuauktorisering (RMA) ha många tilldelade statusvärden (till exempel Väntande eller Auktoriserat). RMA-statusen anger förloppet för en RMA-begäran som tagits upp av användaren eller handlaren.

| Status | Beskrivning |
|--- |--- |
| [!UICONTROL Pending] | Den ursprungliga status som tilldelats en RMA-begäran när den hämtas av en användare i butiken eller av handlaren i administratören. |
| [!UICONTROL Authorized] | Denna status tilldelas RMA när alla begärda artiklar har auktoriserats av handlaren i administratören för returer. |
| [!UICONTROL Partially Authorized] | Denna status tilldelas RMA om någon av de begärda artiklarna har nekats och andra produkter har auktoriserats. |
| [!UICONTROL Denied] | Denna status tilldelas RMA om alla begärda artiklar avvisas av handlaren i administratören för returer. |
| [!UICONTROL Return Received] | Den här statusen tilldelas RMA av handlaren när de begärda artiklarna tas emot från användaren. |
| [!UICONTROL Return Partially Received] | Den här statusen tilldelas RMA av handlaren när de begärda objekten delvis returneras och vissa av objekten nekas att bearbetas. |
| [!UICONTROL Approved] | Den här statusen tilldelas RMA av handlaren när de begärda artiklarna har godkänts för vidare bearbetning. |
| [!UICONTROL Rejected] | Den här statusen tilldelas RMA av handlaren när de begärda artiklarna avvisas för vidare bearbetning. |
| [!UICONTROL Processed and Closed] | Denna status tilldelas av handlaren till RMA när alla begärda artiklar har godkänts för vidare bearbetning. |
| [!UICONTROL Closed] | Den här statusen tilldelas RMA av handlaren när de begärda artiklarna nekas att bearbetas för retur. |

{style="table-layout:auto"}

## Skapa en returbegäran i administratören

En handlare kan skapa en returbegäran för kundens räkning från administratören. Kunderna kan [skapa en returbegäran](rma-customer-experience.md) i butiken för en Adobe Commerce-butik.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Sales]** > **[!UICONTROL Returns]**.

1. Klicka på **[!UICONTROL New Return Request]**.

1. Om du vill skapa en returbegäran klickar du på en order med en `Complete` status.

1. Under _[!UICONTROL Return Information]_väljer du **[!UICONTROL Return Items]**-fliken.

1. Om du vill lägga till objekt som ska returneras klickar du på **[!UICONTROL Add Items]**.

1. Markera kryssrutan för den önskade produkten och klicka på **[!UICONTROL Add Selected Product to returns]**.

1. För **[!UICONTROL Requested]** anger du antalet artiklar som ska returneras.

1. Ange **[!UICONTROL Return Reason]** till något av följande:

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   Om orsaken till returen skiljer sig från alternativen i listan kan du ange en egen om du väljer `Other` alternativ.

1. Ange **[!UICONTROL Item Condition]** till något av följande:

   - `Unopened`
   - `Opened`
   - `Damaged`

1. Ange **[!UICONTROL Resolution]** till något av följande:

   - `Exchange`
   - `Refund`
   - `Store Credit`

1. Om du vill skapa en retur klickar du **[!UICONTROL Submit Returns]**.

   ![Begärda RMA-objekt](./assets/return-item-request.png){width="600" zoomable="yes"}

   Den nyligen skickade RMA-begäran visas på **[!UICONTROL Returns]** sida med en `Pending` status.
