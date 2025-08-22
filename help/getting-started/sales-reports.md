---
title: Försäljningsrapporter
description: Med  [!DNL Commerce] försäljningsrapporterna kan du spåra order, skatter, fakturor, frakt, återbetalningar, kuponger och PayPal-kvittning.
exl-id: 928a407f-cbed-4114-ad0b-ee227383bf36
feature: Reporting, Orders
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: c406add80981387305755221f21624dad475e63f
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 1%

---

# Försäljningsrapporter

I urvalet av försäljningsrapporter ingår beställningar, moms, fakturerad, leverans, återbetalningar, kuponger och PayPal-kvittning.

## Rapportfilter

Du kan generera en försäljningsrapport för en hel webbplats eller för en butik. Försäljningsrapporterna kan filtreras efter tidsintervall, datum och status.

![Filter för försäljningsrapport](./assets/tax-report.png){width="600"}

Om du vill filtrera en försäljningsrapport anger du följande alternativ:

| Alternativ | Beskrivning |
|--- |--- |
| [!UICONTROL Date Used] | Anger vilka data som ska användas för rapporten. |
| [!UICONTROL Period] | Den period för vilken data används: Dag/månad/år. |
| [!UICONTROL From/To] | Används för att definiera sökdata efter start- och slutdatum. |
| [!UICONTROL Order Status] | Anger orderstatus |
| [!UICONTROL Empty Rows] | Anger om tomma rader ska läggas till i rapporten. |

## [!UICONTROL Orders Report]

[!UICONTROL Orders Report] innehåller antalet beställningar som har gjorts och annullerats, med totalsummor för försäljning, fakturerade belopp, återbetalt, inkasserad moms, fraktavgifter och rabatter.

1. Gå till _>_ > **[!UICONTROL Reports]** på sidofältet _[!UICONTROL Sales]_Admin **[!UICONTROL Orders]**.

1. I avsnittet **[!UICONTROL Filter]** väljer du alternativ för rapporteringsperiod och orderstatus som används för att fylla i rapporten.

1. Klicka på **[!UICONTROL Show Report]**.

![Beställningsrapportposter](./assets/order-report-records.png){width="600"}

## [!UICONTROL Tax Report]

[!UICONTROL Tax Report] innehåller den momsregel som används, momssats, antal order och momsbelopp.

1. Gå till _>_ > **[!UICONTROL Reports]** på sidofältet _[!UICONTROL Sales]_Admin **[!UICONTROL Tax]**.

1. I avsnittet **[!UICONTROL Filter]** väljer du alternativ för rapporteringsperiod och orderstatus som används för att fylla i rapporten.


1. Klicka på **[!UICONTROL Show Report]**.

![Skatterapport](./assets/tax-report-records.png){width="600"}

## [!UICONTROL Invoice Report]

[!UICONTROL Invoice Report] innehåller antalet order och fakturor under tidsperioden, med fakturerade, betalda och obetalda belopp.

1. Gå till _>_ > **[!UICONTROL Reports]** på sidofältet _[!UICONTROL Sales]_Admin **[!UICONTROL Invoiced]**.

1. I avsnittet **[!UICONTROL Filter]** väljer du alternativ för rapporteringsperiod och orderstatus som används för att fylla i rapporten.

1. Klicka på **[!UICONTROL Show Report]**.

![Fakturarapport](./assets/sales-invoiced.png){width="600"}

## [!UICONTROL Shipping Report]

[!UICONTROL Shipping Report] innehåller antalet beställningar för transportföretaget eller leveransmetoden, inklusive belopp för total försäljning och total frakt.

1. Gå till _>_ > **[!UICONTROL Reports]** på sidofältet _[!UICONTROL Sales]_Admin **[!UICONTROL Shipping]**.

1. I avsnittet **[!UICONTROL Filter]** väljer du alternativ för rapporteringsperiod och orderstatus som används för att fylla i rapporten.

1. Klicka på **[!UICONTROL Show Report]**.

![Leveransrapport](./assets/shipping.png){width="600"}

## [!UICONTROL Refunds Report]

[!UICONTROL Refunds Report] innehåller antalet återbetalningsorder och det totala beloppet som återbetalas online och offline.

1. Gå till _>_ > **[!UICONTROL Reports]** på sidofältet _[!UICONTROL Sales]_Admin **[!UICONTROL Refunds]**.

1. I avsnittet **[!UICONTROL Filter]** väljer du alternativ för rapporteringsperiod och orderstatus som används för att fylla i rapporten.

1. Klicka på **[!UICONTROL Show Report]**.

![Återbetalningsrapport](./assets/sales-refunds.png){width="600"}

## [!UICONTROL Coupons Report]

[!UICONTROL Coupons Report] innehåller varje kupongkod som används under angivet tidsintervall, relaterad prisregel och antal gånger som används, med summor och delsummor för försäljning och rabatter.

1. Gå till _>_ > **[!UICONTROL Reports]** på sidofältet _[!UICONTROL Sales]_Admin **[!UICONTROL Coupons]**.

1. I avsnittet **[!UICONTROL Filter]** väljer du alternativ för rapporteringsperiod och orderstatus som används för att fylla i rapporten.

1. Klicka på **[!UICONTROL Show Report]**.

Mer information om hur du använder [!UICONTROL Coupons Report] för att samla in data för dina kampanjer finns i [Kuponderrapportering](../merchandising-promotions/price-rules-cart-coupon.md#coupons-report) i _Handboken för marknadsföring och kampanjer_.

<!--- ![Coupons Report](./assets/sales-coupons.png) need coupon data  -->

## [!UICONTROL PayPal Settlement Reports]

Sidan [PayPal-kvittningsrapporter] innehåller händelsetypen, till exempel en debetkortstransaktion, start- och slutdatum, bruttobelopp och relaterade avgifter. Rapporten kan uppdateras automatiskt med de senaste data från PayPal. Det finns filtreringsalternativ för datumintervall, handelskonto, transaktions-ID, faktura-ID eller PayPal-referens-ID.

Gå till _>_ > **[!UICONTROL Reports]** på sidofältet _[!UICONTROL Sales]_Admin **[!UICONTROL PayPal Settlement]**.

![PayPal-kvittningsrapport](./assets/reports-sales-paypal-settlement.png){width="600"}

Mer information om hur du använder [!UICONTROL PayPal Settlement Reports] för att hämta information om varje PayPal-transaktion som påverkar kvittningen av medel finns i [PayPal-kvittningsrapporter](../stores-purchase/paypal-settlement-reports.md) i _butiks- och inköpsupplevelseguiden_.

## [!UICONTROL Braintree Settlement Report]

Kvittningsrapporten [Braintree](../stores-purchase/braintree.md) kan filtreras efter skapandedatum, belopp, status, transaktionstyp, betalningstyp, transaktions-ID, order-ID, PayPal-betalnings-ID, typ, handelskonto-ID eller kvittningsbatch-ID. Rapporten innehåller transaktions-ID, beställnings-ID, PayPal-betalnings-ID, typ, skapandedatum, belopp, kvittningskod, status, kvittningssvarstext, återbetalning-ID, handlarkonto-ID, kvittningsbatch-ID och valuta.

Gå till _>_ > **[!UICONTROL Reports]** på sidofältet _[!UICONTROL Sales]_Admin **[!UICONTROL Braintree Settlement]**.

<!--- ![Braintree Settlement Report](./assets/braintree-settlement.png) need a Braintree connection to update report screen -->

## Exportera rapporter

1. Om du vill exportera rapporten väljer du filtyp: `Excel XML` eller `CSV`

1. Klicka på **[!UICONTROL Export]**.

## Uppdatera statistik

Om du vill minska prestandapåverkan av att generera försäljningsrapporter, beräknar och lagrar [!DNL Commerce] den statistik som krävs för varje rapport. I stället för att räkna om statistiken varje gång en rapport genereras används den lagrade statistiken, såvida du inte uppdaterar statistiken. Om du vill inkludera de senaste uppgifterna måste rapportstatistiken uppdateras innan en försäljningsrapport genereras.

![Uppdatera statistik](./assets/refresh-stats.png){width="700"}

1. Gå till _>_ > **[!UICONTROL Reports]** på sidofältet _[!UICONTROL Statistics]_Admin **[!UICONTROL Refresh Statistics]**.

1. Markera kryssrutan för varje rapport som ska uppdateras i listan.

1. Ställ in kontrollen **[!UICONTROL Actions]** på något av följande:

   - `Refresh Lifetime Statistics`
   - `Refresh Statistics for the Last Day`

1. Klicka på **[!UICONTROL Submit]**.
