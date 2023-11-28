---
title: Checkar och betalningsorder
description: Lär dig hur du ställer in check- och betalningsorder som en offlinebetalningsmetod i din butik.
exl-id: e004f0c3-f659-4b08-a41a-88bfc05acaab
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Checkar och betalningsorder

Med Adobe Commerce och Magento Open Source kan du godkänna betalningar med check eller penningorder. The _Check/penningorder_ betalningsmetod är aktiverad som standard för din butik. Du kan endast acceptera checkar och betalningsorder från vissa länder, och du kan finjustera konfigurationen med minimi- och maximumgränser för ordersumman.

**_Så här konfigurerar du betalning med check eller penningorder:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Payment Methods]**.

1. Under _[!UICONTROL Other Payment Methods]_, expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Check / Money Order]**-avsnitt.

   ![Check/penningorder](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   En detaljerad beskrivning av de här konfigurationsinställningarna finns i [Check/penningorder](../configuration-reference/sales/payment-methods.md#check--money-order) i _Referenshandbok för konfiguration_.

   >[!NOTE]
   >
   >Rensa vid behov först **[!UICONTROL Use system value]** om du vill ändra inställningarna.

1. Om du vill acceptera betalning med check eller penningorder anger du **[!UICONTROL Enabled]** till `Yes`.

1. För **[!UICONTROL Title]**, anger du en titel som identifierar betalningsmetoden för check/penningorder under utcheckningen.

1. Om beställningarna vanligtvis väntar på godkännande, acceptera standardinställningen **[!UICONTROL New Order Status]** as `Pending"` tills det har godkänts.

   Om du vill kan du använda `Processing` eller `Suspected Fraud` status för nya order med denna betalningsmetod.

1. Ange **[!UICONTROL Payment from Applicable Countries]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här betalningsmetoden.
   - `Specific Countries` - När du har valt det här alternativet visas _[!UICONTROL Payment from Specific Countries]_visas. Om du vill markera flera länder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

1. För **[!UICONTROL Make Check Payable To]** Ange namnet på den part som checken ska betalas till.

1. För **[!UICONTROL Send Check To]** Ange gatuadress eller PO Box där kontrollerna skickas.

1. Ange **[!UICONTROL Minimum Order Total]** och **[!UICONTROL Maximum Order Total]** till de orderbelopp som krävs för att få utnyttja denna betalningsmetod.

   >[!NOTE]
   >
   >En order kvalificerar om summan faller mellan, eller exakt matchar, minimi- eller maximivärdena för totalvärdet.

1. För **[!UICONTROL Sort Order]** anger du ett tal som bestämmer positionen för det här objektet i listan över betalningsmetoder som visas vid utcheckning.

   Det här talet är relativt till de andra betalningsmetoderna. (`0` = first, `1` = sekund, `2` = tredje och så vidare.)

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
