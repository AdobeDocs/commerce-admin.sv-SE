---
title: Exempel på kundprisregel - köp den här produkten
description: Se ett exempel på hur du kan använda en kundprisregel för att erbjuda en köp-this-get-that-kampanj.
exl-id: 49e4f9d1-bc60-4861-baca-a23fe148d1c4
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# Exempel på kundprisregel - köp den här produkten

I det här exemplet visas hur du ställer in en [kundvagnsprisregel](price-rules-cart.md) för en _Köp den här, få den kostnadsfria_ kampanjen. Rabattformatet är följande:

_Köp X-kvantitet av produkt, hämta Y-kvantitet kostnadsfritt_

## Steg 1. Skapa en kundvagnsprisregel

Slutför [steg 1](price-rules-cart.md) av instruktionerna för kundprisregeln för att slutföra regelinformationen.

## Steg 2. Definiera villkoren

Slutför [steg 2](price-rules-cart.md) av kundvagnsinstruktionerna för att definiera villkoren för prisregeln. Detta är det första av två villkor som kan läggas till i regeln och som avgör när regeln aktiveras. Den kan baseras på en kombination av följande:

- Produktattribut
- Produkter
- Cart-attribut
- ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) kundsegment

Om inget anges aktiveras regeln för varje kundvagn.

![Kundprisregel - villkor](./assets/buy-x-get-y-condition-default.png){width="600" zoomable="yes"}

## Steg 3. Definiera åtgärderna

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Actions]** och gör följande:

   - Ange **[!UICONTROL Apply]** till `Buy X get Y free (_[!UICONTROL _[!UICONTROL Discount Amount]_]_ is Y)`.

   - Ange **[!UICONTROL Discount Amount]** till `1`. Detta är den kvantitet som kunden får utan kostnad.

   - Om du vill begränsa antalet rabatter som kan användas när villkoret är uppfyllt anger du numret i fältet **[!UICONTROL Maximum Qty Discount is Applied To]**. Detta beräknas med den här [formeln](#maximum-quantity-discount).

   - För **[!UICONTROL Discount Qty Step (Buy X)]** anger du den kvantitet kunden måste köpa för att vara berättigad till rabatten. I det här exemplet måste kunden köpa tre.

   - Om du vill förhindra att andra rabatter tillämpas på köpet anger du **[!UICONTROL Discard subsequent rules]** till `Yes`.

   ![Kundprisregel - köp 3 få 1 utan kostnad](./assets/buy-3-get-1-actions.png){width="600" zoomable="yes"}

1. Om du bara vill tillämpa regeln på vissa artiklar i kundvagnen, fyll i villkoret för att beskriva varukorgsartiklarna och/eller produktattributen som krävs för kampanjen.

   I följande exempel används SKU:n för att tillämpa regeln på alla associerade variationer av en konfigurerbar produkt.

   ![Kundprisregel - villkor för varukorgsartiklar](./assets/buy-3-get-1-actions-condition.png){width="600" zoomable="yes"}

1. Om du vill ta med **[!UICONTROL Free Shipping]** väljer du `For matching items only`.

1. Klicka på **[!UICONTROL Save and Continue Edit]** och fyll i resten av regeln efter behov.

## Steg 4. Fyll i etiketten

Fyll i [Steg 4](price-rules-cart.md) i instruktionerna för kundprisregeln för att ange etiketten som visas vid utcheckningen.

## Steg 5: Spara och testa regeln

{{new-price-rule}}

1. När regeln är klar klickar du på **[!UICONTROL Save Rule]**.

1. Testa regeln för att kontrollera att den fungerar som den ska.

## Variationer

Köp X Get Y Free bearbetas som en enskild åtgärd med ett _radtotal_-beroende. Alla artiklar måste komma från samma SKU för att kvalificera sig för kampanjen. Exempel:

Köp X-kvantitet av produkt från kategori A, få Y-kvantitet av samma produkt utan kostnad.

För att begränsa den kostnadsfria produkten till kategorierna A, B och C ska åtgärden vara följande:

Om ALLA dessa villkor är TRUE:
Kategorin är en av A, B, C

Om du vill begränsa de kostnadsfria objekten från någon kategori (A, B eller C) och få Y från SKU:er (D123, E123 eller F123) anger du åtgärden enligt följande:

Om ALLA dessa villkor är TRUE:
SKU är en av D123, E123, F123

## Maximal kvantitetsrabatt

Använd följande formel för att fastställa rätt värde för maximal mängdrabatt:

Formel = `(X+Y) * (M/Y)`
Plats
`X` = antal köpta artiklar
`Y` = antal kostnadsfria objekt
`M` = Maximalt antal kostnadsfria objekt

Exempel:

Köp fem och få två utan kostnad med högst fyra kostnadsfria artiklar tillåtna.

    Där
    X = 5
    Y = 2
    M = 4
    Maximal mängdrabatt = (5+2)*(4/2)=(7)*(2)=14

Köp fem och få tre utan kostnad med högst nio kostnadsfria artiklar tillåtna.

    Där
    X = 5
    Y = 3
    M = 9
    Högsta mängdrabatt = (5+3)*(9/3)=24

Köp 20 och få två utan kostnad med högst 20 kostnadsfria artiklar tillåtna.

    Där
    X = 20
    Y = 2
    M = 20
    Maximal mängdrabatt = (20+2)*(20/2)=(22)*(10)=220
