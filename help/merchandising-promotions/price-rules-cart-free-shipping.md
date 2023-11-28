---
title: Exempel på kundprisregel - fri frakt
description: Se ett exempel på hur man kan få fri frakt med en kundvagnsregel.
exl-id: f7652254-ff01-44ff-a207-2d7cf2017517
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Exempel på kundprisregel - fri frakt

Fri frakt kan erbjudas som en kampanj, antingen med eller utan [kupong](price-rules-cart-coupon.md). En kostnadsfri leveranskupong, eller verifikation, kan också användas för kundens plockningsorder, så att ordern kan faktureras och skickas för att slutföra ordern [arbetsflöde](../stores-purchase/order-processing.md#order-workflow-and-processing).

Vissa transportföretagskonfigurationer ger dig möjlighet att erbjuda fri frakt baserat på en minimiorder. Om du vill utöka den här grundfunktionen kan du använda kundvagnsprisregler för att skapa komplexa villkor som baseras på flera produktattribut, kundvagnsinnehåll och kundgrupper.

## Steg 1. Aktivera fri frakt

1. Aktivera [fri frakt](../stores-purchase/shipping-free.md) i din butikskonfiguration.

1. Slutför inställningarna för fri frakt för [bärartjänst](../stores-purchase/carriers.md) som du vill använda för fri frakt.

## Steg 2. Skapa en kundvagnsprisregel

På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

Följ stegen nedan för att ange vilken typ av kostnadsfri frakthöjning du vill erbjuda.

### Exempel 1: Fri frakt för alla beställningar

1. Slutför **[!UICONTROL Rule Information]** enligt följande:

   - Ange en **[!UICONTROL Rule Name]** för intern referens.
   - Ange en kort beskrivning **[!UICONTROL Description]** för att beskriva regeln.
   - Ange **[!UICONTROL Active]** till `Yes`.
   - I **[!UICONTROL Websites]** väljer du var den kostnadsfria leveranskupongen ska vara tillgänglig.
   - Välj **[!UICONTROL Customer Groups]** som regeln gäller.
   - Ange **[!UICONTROL Coupon]** till något av följande:
      - Acceptera standardinställningen (`No Coupon`).
      - Om du vill använda en kupong med prisregeln väljer du `Specific Coupon`. Fyll i instruktionerna för att konfigurera en [kupong](price-rules-cart-coupon.md).

1. Rulla ned och expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Actions]** och gör följande:

   - Ange **[!UICONTROL Apply]** till `Percent of product price discount`.
   - Ange **[!UICONTROL Apply to Shipping Amount]** till `Yes`.
   - Ange **[!UICONTROL Free Shipping]** till `For matching items only`.

   ![Kundprisregel - åtgärder för fri frakt](./assets/free-shipping-actions.png){width="600" zoomable="yes"}

### Exempel 2: Fri frakt för beställningar över $

1. Slutför **[!UICONTROL General Information]** inställningar enligt beskrivningen i föregående exempel.

1. Rulla ned och expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Conditions]** -avsnitt.

1. Klicka _Lägg till_ (![Ikonen Lägg till](../assets/icon-add-green-circle.png)) för att infoga ett villkor och göra följande:

   - I listan under **[!UICONTROL Cart Attribute]**, välja `Subtotal`.
   - Klicka **[!UICONTROL is]** och välja `equals or greater than`.
   - Klicka **...** och ange ett tröskelvärde för delsumman, till exempel `100`, för att slutföra villkoret.

   ![Kundprisregel - villkor](./assets/free-shipping-condition1.png){width="600" zoomable="yes"}

1. Expandera vid behov ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Actions]** och gör följande:

   - Ange **[!UICONTROL Apply]** till `Percent of product price discount`.
   - Ange **[!UICONTROL Apply to Shipping Amount]** till `Yes`.
   - Ange **[!UICONTROL Free Shipping]** till `For matching items only`.

## Steg 3. Fyll i etiketterna

Complete [Steg 4](price-rules-cart.md) av kundprisregelns instruktioner om att ange etiketter som visas vid utcheckningen.

## Steg 4. Spara och testa regeln

{{new-price-rule}}

1. När regeln är klar klickar du på **[!UICONTROL Save Rule]**.

1. Testa regeln för att kontrollera att den fungerar som den ska.
