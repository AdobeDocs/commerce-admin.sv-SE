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

- [Beställningar och returwidget](../content-design/widget-orders-returns.md) i sidofältet
- Länken _Beställningar och returnering_ i sidfoten

Det bästa är att du tar med en beskrivning av dina RMA-krav och RMA-processer i kundtjänstens policy.

>[!NOTE]
>
>Om du vill samla in ytterligare information om returer kan du lägga till egna [returer](attributes-returns.md)-attribut.

All kundens RMA-information visas på sidan **[!UICONTROL My Returns]** på kontrollpanelen för kundkonton.

![Mina returer](./assets/my-returns-page.png){width="700" zoomable="yes"}

## Begär en RMA

Kunden utför följande steg i butiken för att skicka in en RMA:

1. Klicka på **[!UICONTROL Orders and Returns]** i sidfoten.

1. Anger orderinformationen:

   - Order-ID
   - Efternamn för fakturering
   - E-post

1. Klicka på **[!UICONTROL Continue]**.

   ![Beställningar och returer](./assets/storefront-orders-and-returns.png){width="700" zoomable="yes"}

1. Under orderdatumet klickar du på **[!UICONTROL Return]**.

   ![Beställningsinformation](./assets/storefront-orders-and-returns-order-information.png){width="700" zoomable="yes"}

1. Väljer vilket objekt som ska returneras och anges i **[!UICONTROL Quantity to Return]**.

1. Anger **[!UICONTROL Resolution]** till något av följande:

   - Exchange
   - [Återbetalning](../customers/refunds-customer-account.md)
   - [Butikskrediter](../customers/store-credit-using.md)

1. Anger **[!UICONTROL Item Condition]** till något av följande:

   - `Unopened`
   - `Opened`
   - `Damaged`

1. Anger **[!UICONTROL Reason to Return]** till något av följande:

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   ![Skapa nytt returvärde](./assets/storefront-orders-and-returns-create-new-return.png){width="700" zoomable="yes"}

1. Anger **[!UICONTROL Contact Email Address]** och **[!UICONTROL Comments]** om det behövs.

   >[!NOTE]
   >
   >Om ordern innehåller flera artiklar och kunden vill returnera ett till objekt, kan de klicka på **[!UICONTROL Add Item To Return]**, markera objektet och sedan ange alla angivna alternativ.

1. Klicka på **[!UICONTROL Submit]**.
