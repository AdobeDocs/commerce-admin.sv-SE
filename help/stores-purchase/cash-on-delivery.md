---
title: Kontant vid leverans (COD)
description: Lär dig hur du ställer in kontanter vid leverans som en offlinebetalningsmetod i din butik.
exl-id: dcf94734-a66e-4d32-b389-b47c979ceaa9
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Kontant vid leverans (COD)

Med Adobe Commerce och Magento Open Source kan du godkänna _kontanter_ (COD) betalningar för inköp. Du kan bara acceptera postförskott från vissa länder och du kan finjustera konfigurationen med minimi- och maximumgränser för ordersumman.

Fraktbolaget får betalning från kunden vid leveranstillfället, som sedan överförs till dig. Du kan göra en justering för de avgifter som fraktfirman tar ut för frakt- och expeditionsavgifter.

**_Så här ställer du in kontanter på leveransbetalningar:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Payment Methods]**.

1. Under _Andra betalningsmetoder_, expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Cash On Delivery Payment]** -avsnitt.

   ![Kontant vid betalning](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   En detaljerad beskrivning av de här konfigurationsinställningarna finns i [Kontant vid leverans](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment) i _Referenshandbok för konfiguration_.

   >[!NOTE]
   >
   >Rensa vid behov först **[!UICONTROL Use system value]** om du vill ändra inställningarna.

1. Aktivera kontanter vid leverans, ange **[!UICONTROL Enabled]** till `Yes`.

1. För **[!UICONTROL Title]**, anger du en titel som identifierar betalningsmetoden för postförskott vid utcheckningen.

1. Ange **[!UICONTROL New Order Status]** till `Pending` tills mottagandet av betalningen har bekräftats.

   Om du vill kan du använda `Processing` eller `Suspected Fraud` status för nya order med denna betalningsmetod.

1. Ange **[!UICONTROL Payment from Applicable Countries]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här betalningsmetoden.
   - `Specific Countries` - När du har valt det här alternativet visas _[!UICONTROL Payment from Specific Countries]_visas. Om du vill markera flera länder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

1. Ange **[!UICONTROL Instructions]** för att ta emot leverans av en postförskott.

1. Ange **[!UICONTROL Minimum Order Total]** och **[!UICONTROL Maximum Order Total]** på de orderbelopp som krävs för att kunna erhålla postförskott.

   >[!NOTE]
   >
   >En order kvalificerar om summan är mellan, eller matchar, minsta eller högsta ordersumma.

1. För **[!UICONTROL Sort Order]** anger du ett tal som bestämmer positionen för det här objektet i listan över betalningsmetoder som visas vid utcheckning.

   Det här talet är relativt till de andra betalningsmetoderna. (`0` = first, `1` = sekund, `2` = tredje och så vidare.)

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
