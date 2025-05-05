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

Med Adobe Commerce och Magento Open Source kan du godkänna betalningar med check eller penningorder. Betalningsmetoden _Check/Money Order_ är aktiverad som standard för din butik. Du kan endast acceptera checkar och betalningsorder från vissa länder, och du kan finjustera konfigurationen med minimi- och maximumgränser för ordersumman.

**_Så här konfigurerar du betalning med check eller betalningsorder:_**

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Payment Methods]**.

1. Under _[!UICONTROL Other Payment Methods]_&#x200B;expanderar du ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Check / Money Order]**.

   ![Kontrollera/Pengar beställ](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   En detaljerad beskrivning av de här konfigurationsinställningarna finns i [Kontrollera/Pengar Order](../configuration-reference/sales/payment-methods.md#check--money-order) i _Konfigurationsreferenshandboken_.

   >[!NOTE]
   >
   >Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för att ändra de här inställningarna.

1. Om du vill acceptera betalning med check eller penningorder anger du **[!UICONTROL Enabled]** till `Yes`.

1. För **[!UICONTROL Title]** anger du en titel som identifierar betalningsmetoden för check/betalningsorder under utcheckningen.

1. Om beställningarna vanligtvis väntar på godkännande ska du godkänna standardvärdet **[!UICONTROL New Order Status]** som `Pending"` tills det godkänns.

   Om du vill kan du använda statusen `Processing` eller `Suspected Fraud` för nya order med den här betalningsmetoden.

1. Ange **[!UICONTROL Payment from Applicable Countries]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här betalningsmetoden.
   - `Specific Countries` - När du har valt det här alternativet visas listan _[!UICONTROL Payment from Specific Countries]_. Om du vill markera flera länder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

1. För **[!UICONTROL Make Check Payable To]** anger du namnet på den part som checken måste betalas till.

1. För **[!UICONTROL Send Check To]** anger du gatuadressen eller PO-lådan där kontrollerna skickas.

1. Ange **[!UICONTROL Minimum Order Total]** och **[!UICONTROL Maximum Order Total]** till de orderbelopp som krävs för att kvalificera dig för den här betalningsmetoden.

   >[!NOTE]
   >
   >En order kvalificerar om summan faller mellan, eller exakt matchar, minimi- eller maximivärdena för totalvärdet.

1. För **[!UICONTROL Sort Order]** anger du ett tal som bestämmer positionen för det här objektet i listan över betalningsmetoder som visas vid utcheckning.

   Det här talet är relativt till de andra betalningsmetoderna. (`0` = först, `1` = sekund, `2` = tredje o.s.v.)

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
