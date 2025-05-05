---
title: Banköverföringar
description: Lär dig hur du ställer in banköverföringar som en offlinebetalningsmetod i din butik.
exl-id: 34b2163c-2edd-4741-b002-3d8fb561fc78
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# Banköverföringar

Adobe Commerce och Magento Open Source tillåter att du godkänner betalning som överförs från ett kundbankkonto och som sätts in på ditt handlarbankkonto.

**_Så här konfigurerar du banköverföringsbetalningar:_**

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Payment Methods]**.

1. Under _Andra betalningsmetoder_ expanderar du ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Bank Transfer Payment]**.

   ![Banköverföringsbetalning](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för att ändra de här inställningarna.

1. Om du vill aktivera banköverföringar anger du **[!UICONTROL Enabled]** till `Yes`.

1. För **[!UICONTROL Title]** anger du en titel som identifierar banköverföringsbetalningsmetoden vid utcheckning.

1. Ange **[!UICONTROL New Order Status]** till `Pending` tills betalningen har auktoriserats.

1. Ange **[!UICONTROL Payment from Applicable Countries]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här betalningsmetoden.

   - `Specific Countries` - När du har valt det här alternativet visas listan _[!UICONTROL Payment from Specific Countries]_. Om du vill markera flera länder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

1. Ange **[!UICONTROL Instructions]** som dina kunder måste följa för att kunna ställa in en banköverföring.

   Beroende på i vilket land banken är belägen och bankens behov kan du inkludera följande information:

   - Bankkontonamn
   - Bankkontonummer
   - Bankroutningskod
   - Bankens namn
   - Bankadress

1. Ange **[!UICONTROL Minimum Order Total]** och **[!UICONTROL Maximum Order Total]** till de belopp som krävs för att kvalificera dig för den här betalningsmetoden.

   >[!NOTE]
   >
   >En order kvalificerar om summan faller mellan, eller exakt matchar, minimi- eller maximivärdena för totalvärdet.

1. För **[!UICONTROL Sort Order]** anger du ett tal som bestämmer positionen för det här objektet i listan över betalningsmetoder som visas vid utcheckning.

   Det här talet är relativt till de andra betalningsmetoderna. (`0` = först, `1` = sekund, `2` = tredje o.s.v.)

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
