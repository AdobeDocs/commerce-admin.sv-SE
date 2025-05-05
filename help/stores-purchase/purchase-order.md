---
title: Inköpsorder
description: Lär dig hur du ställer in inköpsorder som en offlinebetalningsmetod i din butik.
exl-id: 493c1b59-2155-449f-a08a-eb1aa2af9b3e
feature: Purchase Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Inköpsorder

En _inköpsorder_ (PO) tillåter företagskunder att betala för auktoriserade inköp genom att referera till inköpsordernumret. Inköpsordern auktoriseras och utfärdas i förväg av det företag som gör köpet. Vid utcheckning väljer kunden Inköpsorder som betalningsmetod. När vi tagit emot din faktura behandlar företaget betalningen i leverantörsreskontratsystemet och betalar för köpet.

Innan du godkänner betalning med inköpsorder måste du alltid fastställa den kommersiella kundens kreditvärdighet.

**_Så här konfigurerar du betalning med inköpsorder:_**

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Payment Methods]**.

1. Under _[!UICONTROL Other Payment Methods]_&#x200B;expanderar du ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Purchase Order]**.

   ![Inköpsorder](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   En detaljerad beskrivning av de här konfigurationsinställningarna finns i [Inköpsorder](../configuration-reference/sales/payment-methods.md#purchase-order) i _referenshandboken för konfiguration_.

   >[!NOTE]
   >
   >Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för att ändra de här inställningarna.

1. Om du vill aktivera betalningsmetoden anger du **[!UICONTROL Enabled]** till `Yes`.

1. För **[!UICONTROL Title]** anger du en titel som identifierar betalningsmetoden vid utcheckning.

1. Ange **[!UICONTROL New Order Status]** till `Pending` tills betalningen har auktoriserats.

1. Ange **[!UICONTROL Payment from Applicable Countries]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här betalningsmetoden.
   - `Specific Countries` - När du har valt det här alternativet visas listan _[!UICONTROL Payment from Specific Countries]_. Om du vill markera flera länder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

1. Ange **[!UICONTROL Minimum Order Total]** och **[!UICONTROL Maximum Order Total]** till de belopp som krävs för att kvalificera dig för den här betalningsmetoden.

   >[!NOTE]
   >
   >En order kvalificerar om summan faller mellan, eller exakt matchar, minimi- eller maximivärdena för totalvärdet.

1. För **[!UICONTROL Sort Order]** anger du ett tal som bestämmer positionen för det här objektet i listan över betalningsmetoder som visas vid utcheckning.

   Det här talet är relativt till de andra betalningsmetoderna. (`0` = först, `1` = sekund, `2` = tredje o.s.v.)

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
