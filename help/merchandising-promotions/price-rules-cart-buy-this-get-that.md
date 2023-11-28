---
title: Exempel på kundprisregel - köp den här produkten
description: Se ett exempel på hur du kan använda en kundprisregel för att erbjuda en köp-this-get-that-kampanj.
exl-id: 49e4f9d1-bc60-4861-baca-a23fe148d1c4
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 0%

---

# Exempel på kundprisregel - köp den här produkten

I det här exemplet visas hur du ställer in en [kundprisregel](price-rules-cart.md) för _Köp den här, få den kostnadsfritt_ kampanj. Rabattformatet är följande:

_Köp X-kvantitet av produkt, få Y-kvantitet utan kostnad_

## Steg 1. Skapa en kundvagnsprisregel

Complete [Steg 1](price-rules-cart.md) av kundprisregelns instruktioner för att slutföra regelinformationen.

## Steg 2. Definiera villkoren

Complete [Steg 2](price-rules-cart.md) av kundvagnsinstruktionerna för att definiera villkoren för prisregeln. Detta är det första av två villkor som kan läggas till i regeln och som avgör när regeln aktiveras. Den kan baseras på en kombination av följande:

- Produktattribut
- Produkter
- Cart-attribut
- ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Kundsegment

Om inget anges aktiveras regeln för varje kundvagn.

![Kundprisregel - villkor](./assets/buy-x-get-y-condition-default.png){width="600" zoomable="yes"}

## Steg 3. Definiera åtgärderna

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Actions]** och gör följande:

   - Ange **[!UICONTROL Apply]** till `Buy X get Y free (_[!UICONTROL _[!UICONTROL Discount Amount]_]_ is Y)`.

   - Ange **[!UICONTROL Discount Amount]** till `1`. Detta är den kvantitet som kunden får utan kostnad.

   - Om du vill begränsa antalet rabatter som kan användas när villkoret är uppfyllt anger du numret i dialogrutan **[!UICONTROL Maximum Qty Discount is Applied To]** fält. Detta beräknas med detta [formel](#maximum-quantity-discount).

   - För **[!UICONTROL Discount Qty Step (Buy X)]**, ange den kvantitet kunden måste köpa för att vara berättigad till rabatten. I det här exemplet måste kunden köpa tre.

   - Om du vill förhindra att andra rabatter tillämpas på köpet anger du **[!UICONTROL Discard subsequent rules]** till `Yes`.

   ![Kundprisregel - köp 3 få 1 utan kostnad](./assets/buy-3-get-1-actions.png){width="600" zoomable="yes"}

1. Om du bara vill tillämpa regeln på vissa artiklar i kundvagnen, fyll i villkoret för att beskriva varukorgsartiklarna och/eller produktattributen som krävs för kampanjen.

   I följande exempel används SKU:n för att tillämpa regeln på alla associerade variationer av en konfigurerbar produkt.

   ![Kundprisregel - villkor för varukorgsartiklar](./assets/buy-3-get-1-actions-condition.png){width="600" zoomable="yes"}

1. Inkludera **[!UICONTROL Free Shipping]**, välja `For matching items only`.

1. Klicka **[!UICONTROL Save and Continue Edit]** och slutför resten av regeln efter behov.

## Steg 4. Fyll i etiketten

Complete [Steg 4](price-rules-cart.md) av instruktionerna om kundprisregel för att ange etiketten som visas vid utcheckningen.

## Steg 5: Spara och testa regeln

{{new-price-rule}}

1. När regeln är klar klickar du på **[!UICONTROL Save Rule]**.

1. Testa regeln för att kontrollera att den fungerar som den ska.

## Variationer

Köp X Get Y Free behandlas som en enda åtgärd med en _radsumma_ beroende. Alla artiklar måste komma från samma SKU för att kvalificera sig för kampanjen. Exempel:

Köp X-kvantitet av produkt från kategori A, få Y-kvantitet av samma produkt utan kostnad.

För att begränsa den kostnadsfria produkten till kategorierna A, B och C ska åtgärden vara följande:

Om ALLA dessa villkor är TRUE: Kategorin är en av A, B, C

Om du vill begränsa de kostnadsfria objekten från någon kategori (A, B eller C) och få Y från SKU:er (D123, E123 eller F123) anger du åtgärden enligt följande:

Om ALLA dessa villkor är TRUE: SKU är något av D123, E123, F123

## Maximal kvantitetsrabatt

Använd följande formel för att fastställa rätt värde för maximal mängdrabatt:

Formel = `(X+Y) * (M/Y)`
Plats
`X` = antal köpta artiklar
`Y` = antal kostnadsfria artiklar
`M` = Maximalt antal kostnadsfria artiklar

Exempel:

Köp fem och få två utan kostnad med högst fyra kostnadsfria artiklar tillåtna.

    Plats
    X = 5
    Y = 2
    M = 4
    Maximal mängdrabatt = (5+2)*(4/2)=(7)*(2)=14

Köp fem och få tre utan kostnad med högst nio kostnadsfria artiklar tillåtna.

    Plats
    X = 5
    Y = 3
    M = 9
    Maximal mängdrabatt = (5+3)*(9/3)=24

Köp 20 och få två utan kostnad med högst 20 kostnadsfria artiklar tillåtna.

    Plats
    X = 20
    Y = 2
    M = 20
    Maximal rabatt = (20+2)*(20/2)=(22)*(10)=220
