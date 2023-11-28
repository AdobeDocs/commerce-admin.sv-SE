---
title: Ingen deltotal utcheckning
description: Lär dig hur du ställer in en noll-delsumma som en offlinemetod för betalning i din butik.
exl-id: c14ce289-8292-41d9-a448-f493c784f35c
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Ingen deltotal utcheckning

_Ingen deltotal utcheckning_ kan användas för order med delsumman noll som beskattas efter att en rabatt har tillämpats. Exempelvis kan noll delsummeutcheckning användas i följande situationer:

- Rabatten täcker hela inköpspriset utan extra fraktkostnad.

- Kunden lägger till en [nedladdningsbar](../catalog/product-create-downloadable.md) eller [virtuell](../catalog/product-create-virtual.md) produkten i kundvagnen och priset är lika med noll.

- Priset för en [enkel](../catalog/product-create-simple.md) produkten är noll, och [fri frakt](shipping-free.md) är en tillgänglig metod.

- A [kupong](../merchandising-promotions/price-rules-cart-coupon.md) täcker produktens fullpris och frakt.

För att spara tid kan noll deltotalorder anges till automatisk fakturering.

**_Så här konfigurerar du utcheckning av delsumma noll:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Payment Methods]**.

1. Under _[!UICONTROL Other Payment Methods]_, expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Zero Subtotal Checkout]**-avsnitt.

   ![Noll delsumma, utcheckning](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Rensa vid behov först **[!UICONTROL Use system value]** om du vill ändra inställningarna.

1. Aktivera utcheckning av delsumma noll genom att ange **[!UICONTROL Enabled]** till `Yes`.

1. För **[!UICONTROL Title]**, anger du en titel som identifierar metoden Delsumma noll vid utcheckning.

1. Om beställningarna vanligtvis väntar på godkännande, acceptera standardinställningen **[!UICONTROL New Order Status]** as `Pending"` tills ordern är godkänd.

   Om du vill kan du använda `Processing` eller `Suspected Fraud` status för nya order med denna betalningsmetod.

1. Ange **[!UICONTROL Automatically Invoice All Items]** till `Yes` om du automatiskt vill fakturera alla artiklar som har nollsaldo.

   Det här alternativet är bara tillgängligt om **[!UICONTROL New Order Status]** option is set to `Processing`.

   >[!NOTE]
   >
   >If _[!UICONTROL New Order Status]_är inställd på `Processing` och_[!UICONTROL Automatically Invoice All Items]_ är inställd på `No`måste du också tilldela **[!UICONTROL Order Status]** = `Processing` för **[!UICONTROL Order State]** = `Pending` och **[!UICONTROL Default Status]** = `No` mappning på [Orderstatus](order-status.md#custom-order-status) sida.

1. Ange **[!UICONTROL Payment from Applicable Countries]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här betalningsmetoden.
   - `Specific Countries` - När du har valt det här alternativet visas _[!UICONTROL Payment from Specific Countries]_visas. Om du vill markera flera länder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

1. För **[!UICONTROL Sort Order]** anger du ett tal som bestämmer positionen för det här objektet i listan över betalningsmetoder som visas vid utcheckning.

   Det här talet är relativt till de andra betalningsmetoderna. (`0` = first, `1` = sekund, `2` = tredje och så vidare.)

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
