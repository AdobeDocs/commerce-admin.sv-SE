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

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Payment Methods]**.

1. Under _Andra betalningsmetoder_, expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Bank Transfer Payment]** -avsnitt.

   ![Betalning av banköverföring](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Rensa vid behov först **[!UICONTROL Use system value]** om du vill ändra inställningarna.

1. Aktivera banköverföringar genom att ange **[!UICONTROL Enabled]** till `Yes`.

1. För **[!UICONTROL Title]**, anger du en titel som identifierar betalningsmetoden för banköverföring vid utcheckning.

1. Ange **[!UICONTROL New Order Status]** till `Pending` tills betalningen är godkänd.

1. Ange **[!UICONTROL Payment from Applicable Countries]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här betalningsmetoden.

   - `Specific Countries` - När du har valt det här alternativet visas _[!UICONTROL Payment from Specific Countries]_visas. Om du vill markera flera länder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

1. Ange **[!UICONTROL Instructions]** som kunderna måste följa för att göra en banköverföring.

   Beroende på i vilket land banken är belägen och bankens behov kan du inkludera följande information:

   - Bankkontonamn
   - Bankkontonummer
   - Bankroutningskod
   - Bankens namn
   - Bankadress

1. Ange **[!UICONTROL Minimum Order Total]** och **[!UICONTROL Maximum Order Total]** till de belopp som krävs för att få använda betalningsmetoden.

   >[!NOTE]
   >
   >En order kvalificerar om summan faller mellan, eller exakt matchar, minimi- eller maximivärdena för totalvärdet.

1. För **[!UICONTROL Sort Order]** anger du ett tal som bestämmer positionen för det här objektet i listan över betalningsmetoder som visas vid utcheckning.

   Det här talet är relativt till de andra betalningsmetoderna. (`0` = first, `1` = sekund, `2` = tredje och så vidare.)

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
