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

_Ingen delsummeutcheckning_ kan användas för order med delsumman noll som beskattas efter en rabatt. Exempelvis kan noll delsummeutcheckning användas i följande situationer:

- Rabatten täcker hela inköpspriset utan extra fraktkostnad.

- Kunden lägger till en [nedladdningsbar](../catalog/product-create-downloadable.md)- eller [virtuell](../catalog/product-create-virtual.md)-produkt i kundvagnen och priset är lika med noll.

- Priset för en [enkel](../catalog/product-create-simple.md)-produkt är noll och metoden [fri frakt](shipping-free.md) är tillgänglig.

- En [kupongkod](../merchandising-promotions/price-rules-cart-coupon.md) täcker produktens fulla pris och frakt.

För att spara tid kan noll deltotalorder anges till automatisk fakturering.

**_Så här konfigurerar du utcheckning av delsumma noll:_**

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Payment Methods]**.

1. Under _[!UICONTROL Other Payment Methods]_&#x200B;expanderar du ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Zero Subtotal Checkout]**.

   ![Ingen deltotal utcheckning](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för att ändra de här inställningarna.

1. Om du vill aktivera utcheckning av noll delsummor anger du **[!UICONTROL Enabled]** till `Yes`.

1. För **[!UICONTROL Title]** anger du en titel som identifierar metoden noll delsumma vid utcheckning.

1. Om order vanligtvis väntar på godkännande ska du godkänna standardinställningen **[!UICONTROL New Order Status]** som `Pending"` tills ordern har godkänts.

   Om du vill kan du använda statusen `Processing` eller `Suspected Fraud` för nya order med den här betalningsmetoden.

1. Ange **[!UICONTROL Automatically Invoice All Items]** till `Yes` om du vill fakturera alla artiklar som har nollsaldo automatiskt.

   Det här alternativet är bara tillgängligt om alternativet **[!UICONTROL New Order Status]** är inställt på `Processing`.

   >[!NOTE]
   >
   >Om _[!UICONTROL New Order Status]_&#x200B;är inställt på `Processing` och&#x200B;_[!UICONTROL Automatically Invoice All Items]_ är inställt på `No` måste du även tilldela **[!UICONTROL Order Status]** = `Processing` för mappningen **[!UICONTROL Order State]** = `Pending` och **[!UICONTROL Default Status]** = `No` på sidan [Beställningsstatus](order-status.md#custom-order-status).

1. Ange **[!UICONTROL Payment from Applicable Countries]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här betalningsmetoden.
   - `Specific Countries` - När du har valt det här alternativet visas listan _[!UICONTROL Payment from Specific Countries]_. Om du vill markera flera länder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

1. För **[!UICONTROL Sort Order]** anger du ett tal som bestämmer positionen för det här objektet i listan över betalningsmetoder som visas vid utcheckning.

   Det här talet är relativt till de andra betalningsmetoderna. (`0` = först, `1` = sekund, `2` = tredje o.s.v.)

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
