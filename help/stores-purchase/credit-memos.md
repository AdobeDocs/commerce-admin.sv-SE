---
title: Kreditnotor
description: Lär dig mer om kreditnotor och hur de används för att utfärda en partiell eller fullständig återbetalning.
exl-id: dc2faf86-0182-4661-9543-bc6e00e06dbf
feature: Orders, Invoices, Returns
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# Kreditnotor

A _kreditnota_ är ett dokument som visar det belopp som ska betalas av kunden för en fullständig eller partiell återbetalning. Beloppet kan tillämpas på ett köp eller återbetalas till kunden. Du kan skriva ut en kreditnota för en enstaka order eller för flera order som en batch. Innan en kreditnota kan skrivas ut måste den skapas för ordern. The _Kreditnotor_ På sidan visas de kreditnotor som har utfärdats till kunder.

![Kreditnotor](./assets/credit-memos.png){width="700" zoomable="yes"}

## Återbetalningsmetod

The [betalningsmetod](payments.md) för ordern avgör i viss utsträckning vilken metod som används för att återbetala en order.

Du kan återbetala beställningar på tre sätt:

- Kontokredit - Beställningar som betalas med ett kreditkonto kan återbetalas som kontokredit:
   - ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) [Butikskrediter](../customers/store-credit-using.md)
   - ![Adobe Commerce B2B](../assets/b2b.svg) (Finns med Adobe Commerce B2B) [Betalning à conto](../b2b/enable-basic-features.md#configure-payment-on-account) (offline-metod)
   - ![Adobe Commerce B2B](../assets/b2b.svg) (Finns med Adobe Commerce B2B) [Företagskrediter](../b2b/credit-company.md)
- [Online-återbetalning](payments.md#online-payment-methods)- Beställningar som betalas med kreditkort via en betalningstjänst, som PayPal eller Braintree, återbetalas online via betalningsfunktionen.
- [Offlineåterbetalning](payments.md#offline-payment-methods)—Beställningar som betalas med kontanter vid leverans ([COD](cash-on-delivery.md)) eller av [check eller penningorder](check-money-order.md) återbetalas offline.

Du kan utfärda en offlineåterbetalning eller kontokredit (om den är aktiverad) för alla betalningsmetoder.

En order som har betalats av kontanter vid leverans ([COD](cash-on-delivery.md)) eller av [check eller penningorder](check-money-order.md) återbetalas offline.

## Återbetalningsarbetsflöde

1. **Betalningsåtgärd** - Om [Betalningsåtgärd](credit-memo-create.md#payment-action-setting) konfigurationen är inställd på `Authorize`måste du generera en faktura innan du skapar en kreditnota - fortsätt till steg 2. Om inställt på `Authorize and Capture`har en faktura redan skapats - fortsätt till steg 3.

1. **Generera faktura** - [Skapa en faktura](invoices.md#create-an-invoice) för ordern, så att du kan skicka en återbetalning till kunden via kreditnota.

1. **Skapa kreditnota** - [Utfärda en kreditnota](credit-memo-create.md) i Admin för en [kreditköp](credit-memo-create.md#issue-a-refund-for-a-credit-purchase), eller en [check eller penningorder](credit-memo-create.md#issue-an-offline-refund-for-check-or-money-order).

## Kolumnbeskrivningar

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Select] | Markera kryssrutorna för de kreditnotobjekt som ska bli föremål för en åtgärd, eller använd markeringskontrollen i kolumnrubriken. Alternativ: `Select All` / `Deselect All` |
| [!UICONTROL Credit Memo] | En unik numerisk identifierare som tilldelas när en begäran om en kreditnota skickas. |
| [!UICONTROL Created] | Datum och tid då köparen först lämnade in en begäran om kreditnota. |
| [!UICONTROL Order#] | Order-ID för den order vars produkter returneras. |
| [!UICONTROL Order Date] | Datum och tid då köparen lade en order. |
| [!UICONTROL Bill-to Name] | Namnet på den person som är ansvarig för att betala för ordern. |
| [!UICONTROL Status] | Anger det aktuella tillståndet för en kreditnotsbegäran. |
| [!UICONTROL Refunded] | Det totala beloppet som återbetalas från ordern. |
| [!UICONTROL Actions] | **[!UICONTROL View]** - Öppnar begäran om en kreditnota och upprätthåller ett register över förhandlingen mellan köpare och säljare. |
| [!UICONTROL Order Status] | Anger orderstatus. |
| [!UICONTROL Purchased From] | Anger webbplatsen, butiken och butiksvyn där beställningen placerades. |
| [!UICONTROL Billing Address] | Faktureringsadressen till den kund som beställde. |
| [!UICONTROL Shipping Address] | Den adress dit ordern ska skickas. |
| [!UICONTROL Customer Name] | Förnamn och efternamn på den kund som lade ordern. |
| [!UICONTROL Email] | E-postadressen till den person som gjorde beställningen. |
| [!UICONTROL Customer Group] | Kundgruppen som kunden är tilldelad till. |
| [!UICONTROL Payment Method] | Betalningsmetoden som ska användas för betalningen. |
| [!UICONTROL Shipping Information] | Den metod som ska användas för att skicka ordern. |
| [!UICONTROL Subtotal] | Delsumman för beställningen, utan frakt och expeditionsavgift. |
| [!UICONTROL Shipping & Handling] | Belopp som debiteras för frakt och hantering. |
| [!UICONTROL Adjustment Refund] | Det belopp som läggs till det totala belopp som återbetalas som en extra återbetalning. |
| [!UICONTROL Adjustment Fee] | Det belopp som subtraheras från det totala beloppet som återbetalas. |
| [!UICONTROL Grand Total] | Ordersumman. |

{style="table-layout:auto"}
