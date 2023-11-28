---
title: Returnerar butiksupplevelsen
description: Läs om hur kunderna kan hantera sina produktreturer från sina konton i butiken.
exl-id: c276ca2c-3d8b-4019-a9aa-e7631080f331
feature: Returns, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# Returnerar butiksupplevelsen

{{ee-feature}}

Kunder kan använda något av följande för att begära en RMA från butiken:

- [Widget för beställningar och returer](../content-design/widget-orders-returns.md) i sidlisten
- _Beställningar och returer_ länk i sidfot

Det bästa är att du tar med en beskrivning av dina RMA-krav och RMA-processer i kundtjänstens policy.

>[!NOTE]
>
>Om du vill samla in ytterligare information om returer kan du lägga till egen, anpassad information [returnerar attribut](attributes-returns.md).

All kundens RMA-information visas på **[!UICONTROL My Returns]** på kundkontots kontrollpanel.

![Mina returer](./assets/my-returns-page.png){width="700" zoomable="yes"}

## Begär en RMA

Kunden utför följande steg i butiken för att skicka in en RMA:

1. Klicka i sidfoten **[!UICONTROL Orders and Returns]**.

1. Anger orderinformationen:

   - Order-ID
   - Efternamn för fakturering
   - E-post

1. Klickningar **[!UICONTROL Continue]**.

   ![Beställningar och returer](./assets/storefront-orders-and-returns.png){width="700" zoomable="yes"}

1. Under orderdatumet klickar du **[!UICONTROL Return]**.

   ![Beställningsinformation](./assets/storefront-orders-and-returns-order-information.png){width="700" zoomable="yes"}

1. Väljer vilket objekt som ska returneras och anges **[!UICONTROL Quantity to Return]**.

1. Uppsättningar **[!UICONTROL Resolution]** till något av följande:

   - Exchange
   - [Återbetalning](../customers/refunds-customer-account.md)
   - [Butikskrediter](../customers/store-credit-using.md)

1. Uppsättningar **[!UICONTROL Item Condition]** till något av följande:

   - `Unopened`
   - `Opened`
   - `Damaged`

1. Uppsättningar **[!UICONTROL Reason to Return]** till något av följande:

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   ![Skapa ny retur](./assets/storefront-orders-and-returns-create-new-return.png){width="700" zoomable="yes"}

1. Vid behov, uppsättningar **[!UICONTROL Contact Email Address]** och **[!UICONTROL Comments]**.

   >[!NOTE]
   >
   >Om ordern innehåller flera artiklar och kunden vill returnera en annan artikel kan de klicka på **[!UICONTROL Add Item To Return]** markerar du objektet och anger sedan alla angivna alternativ.

1. Klickningar **[!UICONTROL Submit]**.
