---
title: Beställningar
description: Lär dig mer om arbetsytan Beställningar och de sökfunktioner som används för att hitta beställningar i Admin.
exl-id: 6ec8b8c7-97c4-446e-9420-e36e72e90237
feature: Orders, Admin Workspace
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1202'
ht-degree: 0%

---

# Beställningar

Rutnätet _Beställningar_ visar alla aktuella order och spårar deras förlopp och [orderstatus](order-status.md) via [arbetsflödet](order-processing.md). Ett enkelt sätt att förstå den grundläggande processen är att en order blir en [faktura](invoices.md) och en faktura blir en [leverans](shipments.md). Rutnätet representerar det första steget i processen och det är där du kan [uppdatera](order-update.md) befintliga order och skapa order.

Vanligtvis skapas order när kunderna slutför utcheckningsprocessen från butiken. Om en kund behöver hjälp kan du även få åtkomst till kundens [kundvagn](shopping-assisted-cart-manage.md) eller [skapa en beställning](customer-account-create-order.md) antingen från rutnätet _Beställningar_ eller direkt från kundkontot.

## Arbetsytan Beställningar

På arbetsytan Beställningar visas alla aktuella beställningar, och du kan redigera befintliga beställningar och [skapa](customer-account-create-order.md) beställningar. Varje rad i rutnätet representerar en kundorder och varje kolumn representerar ett attribut eller datafält. Använd [kontrollerna](../getting-started/admin-grid-controls.md) som standard för att sortera och filtrera listan, söka efter order och tillämpa [åtgärder](../getting-started/admin-actions-control.md) på valda order. Använd flikarna ovanför sidnumreringskontrollerna för att filtrera listan, ändra standardvyn, ändra och ordna om kolumner samt exportera data.

![Ordningsrutnät](./assets/orders-grid.png){width="700" zoomable="yes"}

### Rutnätslayout

Markeringen av kolumner och deras ordning i rutnätet kan ändras enligt dina önskemål. Den nya layouten kan sparas som ett stödraster _vy_. Som standard inkluderas bara nio av 20 tillgängliga kolumner i rutnätet.

![Ordna kolumner för stödraster](./assets/order-grid-columns.png){width="600" zoomable="yes"}

#### Ändra kolumnmarkeringen

Klicka på kontrollen _Kolumner_ ( ![Kolumninställningar](../assets/icon-columns.png) ) i det övre högra hörnet och gör följande:

- Markera kryssrutan för den kolumn som du vill lägga till i rutnätet.
- Avmarkera kryssrutan för de kolumner som du vill ta bort från stödrastret.

#### Återställ kolumnmarkeringen

1. Klicka på kontrollen _Kolumner_ ( ![Kolumninställningar](../assets/icon-columns.png) ).

1. Klicka på **[!UICONTROL Reset]** om du vill återställa stödrasterkolumnerna.

   Rutnätslayouten ändras så att endast [standardkolumner](#column-descriptions) visas.

#### Flytta en kolumn

1. Klicka och håll ned kolumnrubriken.

1. Dra kolumnen till den nya positionen och släpp den.

#### Spara en stödrastervy

1. Klicka på kontrollen **[!UICONTROL View]** ( ![Ögon-ikon](../assets/icon-view-eye.png) ).

1. Klicka på **[!UICONTROL Save Current View]**.

1. Ange **[!UICONTROL name]** som vy.

1. Om du vill spara alla ändringar klickar du på pilen ( ![pilikonen](../assets/icon-arrow-save.png) ).

   Namnet på vyn visas nu som den aktuella vyn.

#### Ändra vyn

Klicka på kontrollen **[!UICONTROL View]** ( ![Ögon-ikon](../assets/icon-view-eye.png) ). Gör sedan något av följande:

- Om du vill använda en annan vy klickar du på vyns namn.

- Om du vill ändra namnet på en vy klickar du på ikonen _Redigera_ ( ![Penna ](../assets/icon-edit-pencil.png) ) och uppdaterar namnet.

### Workspace

| Kontroll | Beskrivning |
|--- |--- |
| [!UICONTROL Create New Order] | Skapar en order. Mer information finns i [Skapa en beställning](customer-account-create-order.md). |
| [!UICONTROL Go to Archive] | Visar en lista med arkiverade order. |
| [!UICONTROL Search] | Startar en sökning efter order baserat på de aktuella filtren. |
| [!UICONTROL Filters] | Definierar en uppsättning sökparametrar som används för att filtrera posterna som visas i rutnätet. |
| [!UICONTROL Default View] | Anger stödrastrets standardkolumnlayout. |
| [!UICONTROL Columns] | Anger markeringen av kolumner och deras ordning i rutnätet. Kolumnlayouten kan ändras och sparas som en _vy_. Som standard inkluderas bara vissa av kolumnerna i rutnätet. |
| [!UICONTROL Export] | Exporterar de markerade posterna som en CSV- eller Excel XML-fil. |

{style="table-layout:auto"}

### Åtgärder

Om du vill utföra en åtgärd på en viss order markerar du kryssrutan i den första kolumnen i varje order. Om du vill markera eller avmarkera alla order använder du kontrollen längst upp i kolumnen.

![Beställa åtgärder](./assets/orders-action.png){width="600" zoomable="yes"}

| Kontroll | Beskrivning |
|--- |--- |
| [!UICONTROL Actions] | Visar alla åtgärder som kan tillämpas på valda order. Om du vill tillämpa en åtgärd på en order eller en grupp av order markerar du kryssrutan i den första kolumnen i varje order. <br/>Beställa åtgärder: `Cancel` / `Hold` / `Unhold` / `Print Invoices` / `Print Packing Slips` / `Print Credit Memos` / `Print All` / `Print Shipping Labels` / `Move to Archive` ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) |
| [!UICONTROL Mass Actions] | Kan användas för att markera flera poster som mål för åtgärden. Markera kryssrutan i den första kolumnen i varje post som är föremål för åtgärden. Alternativ: `Select All` / `Unselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL Submit] | Tillämpar den aktuella åtgärden på de markerade orderposterna. |
| [!UICONTROL Edit] | Öppnar ordningen i redigeringsläge. |

{style="table-layout:auto"}

### Kolumnbeskrivningar

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Select] | Markera kryssrutorna för de citattecken som ska bli föremål för en åtgärd, eller använd markeringskontrollen i kolumnrubriken. Alternativ: Markera allt/Avmarkera allt |
| [!UICONTROL ID] | Ett unikt sekventiellt nummer som tilldelas när en ny order sparas för första gången. |
| [!UICONTROL Purchase Point] | Identifierar butiksvyn där ordern placerades. |
| [!UICONTROL Purchase Date] | Datum och tid då ordern placerades. Den visas alltid enligt standardtidszonen. |
| [!UICONTROL Bill-to Name] | Namnet på den person som är ansvarig för att betala för ordern. |
| [!UICONTROL Ship-to Name] | Namnet på den person som ordern ska skickas till. |
| [!UICONTROL Grand Total (Base)] | Orderns totalsumma. |
| [!UICONTROL Grand Total (Purchased)] | Summan av inköpta produkter i ordern. |
| [!UICONTROL Status] | Aktuell orderstatus. |
| [!UICONTROL Action] | _[!UICONTROL View]_öppnar ordningen i redigeringsläge. |
| [!UICONTROL Allocated sources] | Källor som tilldelats den specifika ordern. |

{style="table-layout:auto"}

Ytterligare kolumner är tillgängliga:

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Billing Address] | Faktureringsadressen till den kund som beställde. |
| [!UICONTROL Shipping Address] | Den adress dit ordern ska skickas. |
| [!UICONTROL Shipping Information] | Den metod som ska användas för att skicka ordern. |
| [!UICONTROL Customer Email] | E-postadressen till den person som gjorde beställningen. |
| [!UICONTROL Customer Group] | Den kundgrupp som den person som lade ordern är tilldelad till. |
| [!UICONTROL Subtotal] | Delsumman för beställningen, utan frakt och expeditionsavgift. |
| [!UICONTROL Shipping and Handling] | Belopp som debiteras för frakt och hantering. |
| [!UICONTROL Customer Name] | Förnamn och efternamn på den kund som lade ordern. |
| [!UICONTROL Payment Method] | Betalningsmetoden som ska användas för ordern. |
| [!UICONTROL Total Refunded] | Alla belopp från ordern som ska återbetalas till kunden. |
| [!UICONTROL Refunded to Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Alla belopp i ordern som ska återbetalas till kundens butikskrediter. |
| [!UICONTROL Company Name] | ![Adobe Commerce B2B](../assets/b2b.svg) (tillgänglig med Adobe Commerce B2B) Namnet på det [företag](../b2b/account-companies.md) som gjorde beställningen. |

{style="table-layout:auto"}

## Ordersökning

Du kan använda sökrutan längst upp till vänster i stödrastret Beställningar till att söka efter särskilda order efter nyckelord eller till att filtrera ordningsposterna i stödrastret.

![Sökresultat](./assets/order-search.png){width="600" zoomable="yes"}

### Sök efter en matchning

1. Ange en sökterm i sökrutan.

1. Om du vill visa resultatet klickar du på _Sök_ ( ![Förstoringsglaset ](../assets/icon-magnify-search.png) ).

### Filtrera sökningen

1. Om du vill visa urvalet av sökfilter klickar du på fliken _Filter_ ( ![Tratt icon](../assets/icon-filter-search.png) ).

   ![Beställa filter](./assets/order-search-filter.png){width="600" zoomable="yes"}

1. Fyll i så många av filtren du vill för att beskriva de order du vill hitta.

1. Klicka på **[!UICONTROL Apply Filters]** för att visa resultatet.

### Sökfilter

| Filter | Beskrivning |
|--- |--- |
| [!UICONTROL Purchase Date] | Filtrerar sökningen baserat på köpdatum. Om du vill söka efter order inom ett datumintervall anger du både **[!UICONTROL from]**- och **[!UICONTROL to]**-datumen. |
| [!UICONTROL ID] | Filtrerar sökningen baserat på order-ID. |
| [!UICONTROL Grand Total (Base)] | Filtrerar sökningen baserat på totalsumman för varje order, vilket inkluderar alla krediter som har tillämpats på ordern. |
| [!UICONTROL Grand Total (Purchased)] | Filtrerar sökningen baserat på totalsumman för inköpta objekt i varje order. |
| [!UICONTROL Bill-to Name] | Filtrerar sökningen efter namnet på den person som är ansvarig för att betala ordern. |
| [!UICONTROL Ship-to Name] | Filtrerar sökningen efter namnet på den person som varje order skickas till. |
| [!UICONTROL Purchase Point] | Filtrerar sökningen efter webbplats, butik eller butiksvy där ordern placerades. |
| [!UICONTROL Status] | Filtrerar sökningen baserat på orderstatus. Alternativ: `Canceled` / `Closed` / `Complete` / `Suspected Fraud` / `On Hold` / `Payment Review` / `PayPal Canceled Reversal` /` PayPal Reversed` /` Pending` / `Pending Payment` / `Pending PayPal` / `Processing` |
| [!UICONTROL Braintree Transaction Source] | Filtrerar sökningen baserat på transaktionskälla. |

{style="table-layout:auto"}

### Sökverktyg

| Verktyg | Beskrivning |
|--- |--- |
| [!UICONTROL Apply Filters] | Tillämpar alla filter på sökresultaten. |
| [!UICONTROL Cancel] | Avbryter aktuell sökning. |
| [!UICONTROL Clear All] | Tar bort alla sökfilter. |

{style="table-layout:auto"}

## Felsökningsresurser

Hjälp om felsökning av orderproblem finns i följande artiklar i Commerce Support Knowledge Base:

- [Visningsfel för beställningar](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/magento-2.4.0-known-issue-orders-display-error.html)
- [PayPal-dubblettorder 10415-fel](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-6/mdva-31006-magento-patch-paypal-duplicate-orders-10415-error.html)
- [Nya order skickas till arkivet](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/new-orders-are-sent-to-archive.html)
- [Beställningar visas inte i rutnätet för beställningar i Admin](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/orders-not-displayed-in-the-orders-grid-in-the-admin.html)
- [Beställningsstatus - felaktig leverans skapad via REST API](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-7/mdva-30972-magento-patch-order-status-incorrect-shipment-created-via-rest-api.html)
