---
title: Exempel på kundprisregel - rabatt med lägsta produktpris
description: Se ett exempel på hur du kan använda en kundprisregel för att erbjuda en rabatt med ett lägsta produktpris.
exl-id: dc06cd12-d23b-4836-9ad2-93ca60dac927
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 6bc76c76bc7a17e115696911cc2499075d35c541
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Exempel på kundprisregel - rabatt med minimiköp

Kundprisregler kan användas för att erbjuda en procentuell rabatt som baseras på ett minimiproduktpris i kundvagnen. I följande exempel tillämpas en rabatt på 10 % på alla produkter i hela varukorgen när minst en produkt med ett pris över 30,00 USD från en angiven kategori läggs till i kundvagnen. Rabattformatet är följande:

X % rabatt på hela kundvagnen när minst en produkt kommer från Y-kategorin och priset är över SEK.

## Steg 1. Skapa en kundvagnsregel

Följ de grundläggande [instruktionerna](price-rules-cart.md) för att skapa en kundvagnsregel.

## Steg 2. Definiera villkoren

1. Bläddra nedåt och utöka ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Conditions]**.

1. Klicka på _Lägg till_ (![Lägg till ikon](../assets/icon-add-green-circle.png)) och välj **[!UICONTROL Product Attribute Combination]**.

   ![Villkor för kundprisregel - kombination av produktattribut](./assets/condition1.png){width="500" zoomable="yes"}

1. Klicka på _Lägg till_ (![Lägg till ikon](../assets/icon-add-green-circle.png)) i början av nästa rad och välj **[!UICONTROL Category]** i listan under **[!UICONTROL Product Attribute]**.

   - Klicka på länken (**..**) _mer_ om du vill visa ytterligare alternativ.

     ![Villkor för kundprisregel - kategorialternativ](./assets/condition3.png){width="600" zoomable="yes"}

   - Klicka på ikonen _Väljare_ (![Lista-ikon](../assets/icon-list-chooser.png)) för att visa de tillgängliga kategorierna. Markera kryssrutan för varje kategori som du vill ta med i kategoriträdet. Klicka på bockikonen för att godkänna kategorivalen.

     ![Villkor för kundprisregel - kategori](./assets/condition4.png){width="600" zoomable="yes"}

1. Klicka på _Lägg till_ (![Lägg till ikon](../assets/icon-add-green-circle.png)) i början av nästa rad och gör följande:

   - Välj **[!UICONTROL Price in cart]** i listan under **[!UICONTROL Cart Item Attribute]**.

     ![Villkor för kundprisregel - kundvagnsartikelattribut](./assets/condition5.png){width="500"}

   - Klicka på **är** och välj `equals or greater than`.

   - Klicka på **..** och ange beloppet som priset i kundvagnen måste vara för att uppfylla villkoret. Ange till exempel `30`.

     ![Villkor för kundprisregel - pris i kundvagn](./assets/condition6.png){width="500"}

1. Klicka på **[!UICONTROL Save and Continue Edit]**.

## Steg 3. Definiera åtgärderna

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Actions]** och gör följande:

   ![Åtgärder för kundprisregel](./assets/minimum-discount-actions.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL Apply]** till `Percent of product price discount`.

   - Ange **[!UICONTROL Discount Amount]**. Ange till exempel `10` som 10 % rabatt.

   - Ange **[!UICONTROL Discard subsequent rules]** till `Yes` om du vill förhindra att fler kampanjer tillämpas på köpet.

1. Klicka på **[!UICONTROL Save and Continue Edit]** och fyll i regeln efter behov.

## Steg 4. Fyll i etiketterna

Fyll i [Steg 4](price-rules-cart.md) i instruktionerna för kundprisregeln för att ange etiketter som visas vid utcheckningen.

## Steg 5: Spara och testa regeln

{{new-price-rule}}

1. När regeln är klar klickar du på **[!UICONTROL Save Rule]**.

1. Testa regeln för att kontrollera att den fungerar som den ska.
