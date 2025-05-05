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

Med Adobe Commerce och Magento Open Source kan du acceptera _kontantbetalningar vid leverans_ (COD) för inköp. Du kan bara acceptera postförskott från vissa länder och du kan finjustera konfigurationen med minimi- och maximumgränser för ordersumman.

Fraktbolaget får betalning från kunden vid leveranstillfället, som sedan överförs till dig. Du kan göra en justering för de avgifter som fraktfirman tar ut för frakt- och expeditionsavgifter.

**_Så här ställer du in kontanter på leveransbetalningar:_**

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Payment Methods]**.

1. Under _Andra betalningsmetoder_ expanderar du ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Cash On Delivery Payment]**.

   ![Kontant vid betalning](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   En detaljerad beskrivning av de här konfigurationsinställningarna finns i [Kontant vid leverans](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment) i _referenshandboken för konfiguration_.

   >[!NOTE]
   >
   >Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för att ändra de här inställningarna.

1. Om du vill aktivera kontanter vid leverans anger du **[!UICONTROL Enabled]** till `Yes`.

1. För **[!UICONTROL Title]** anger du en titel som identifierar postförskott vid utcheckning.

1. Ange **[!UICONTROL New Order Status]** till `Pending` tills inleveransen av betalningen har bekräftats.

   Om du vill kan du använda statusen `Processing` eller `Suspected Fraud` för nya order med den här betalningsmetoden.

1. Ange **[!UICONTROL Payment from Applicable Countries]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här betalningsmetoden.
   - `Specific Countries` - När du har valt det här alternativet visas listan _[!UICONTROL Payment from Specific Countries]_. Om du vill markera flera länder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

1. Ange **[!UICONTROL Instructions]** för att acceptera leverans av en postförskott.

1. Ange **[!UICONTROL Minimum Order Total]** och **[!UICONTROL Maximum Order Total]** till de orderbelopp som krävs för att kvalificera sig för postförskott.

   >[!NOTE]
   >
   >En order kvalificerar om summan är mellan, eller matchar, minsta eller högsta ordersumma.

1. För **[!UICONTROL Sort Order]** anger du ett tal som bestämmer positionen för det här objektet i listan över betalningsmetoder som visas vid utcheckning.

   Det här talet är relativt till de andra betalningsmetoderna. (`0` = först, `1` = sekund, `2` = tredje o.s.v.)

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
