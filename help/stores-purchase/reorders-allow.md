---
title: Tillåt ombeställningar
description: Lär dig hur ni kan erbjuda kunderna möjlighet att ändra beställning.
exl-id: 9fe4c4fb-8596-4fd0-a93b-927ebdfc0c94
feature: Orders, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Tillåt ombeställningar

När det här alternativet är aktiverat kan ombeställningar göras direkt från kundkontot eller från den ursprungliga ordern i _Administratör_. Ordna om är aktiverat som standard.

![Länk för kundombeställning i administratören](./assets/customer-reorder.png){width="700" zoomable="yes"}

## Villkor för att ändra ordning ska aktiveras för en order

- The _Tillåt ombeställning_ konfigurationsalternativet måste vara aktiverat.

- Om ordern är i `Hold` eller in `Payment Review` status är alternativet för att ändra ordning inaktiverat.

- Om något av objekten i ordningen inte är tillgängligt, inte finns i lager eller är inaktiverat, är alternativet för omsortering inaktiverat i butiken.

- An _Administratör_ kan ändra ordningen även om något av objekten är utanför lagret eller inaktiverat.

## Konfigurera för att tillåta kundombeställningar

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Sales]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Reorder]** -avsnitt.

   ![Alternativ för omsortering](../configuration-reference/sales/assets/sales-reorder.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Allow Reorder]** till `Yes`.

   Den här inställningen aktiverar funktionen för omsortering från kundkontot i listan över butiker eller order i Admin.

1. Klicka på **[!UICONTROL Save Config]**.

## Sortera om från butiken

Kunden kan initiera omsorteringsfunktionen för en viss order från två sidor:

- _Mina beställningar_ page

- _Ordervy_ page

### Mina beställningar

The _Ändra ordning_ visas alltid i listan med beställningar (även om alla produkter i beställningen inte är tillgängliga för ombeställning).

![Exempel på butiker - sidan Mina beställningar](./assets/my-order-page-view.png){width="700" zoomable="yes"}

**Fall 1.** Alla produkter i beställningen är **tillgänglig** för ombeställning

Användaren dirigeras om till kundvagnen och alla produkter läggs till i kundvagnen

![Kundvagn](./assets/shopping-cart-page.png){width="700" zoomable="yes"}

**Fall 2.** Vissa produkter från beställningen är **inte tillgängligt** för ombeställning

>[!NOTE]
>
>Det går att ändra ordning `Not Visible Individually` produkter.

The _Ändra ordning_ knappen visas inte på _Mina beställningar_ och _Visa order_ sidor.

![Mina beställningar, sida 1](./assets/my-orders-view-page1.png){width="700" zoomable="yes"}

### Sidan Ordervy

**Fall 1.** Alla produkter från ordern är tillgängliga för ombeställning

Användaren dirigeras om till kundvagnen och alla produkter läggs till i kundvagnen

**Fall 2.** Vissa produkter från beställningen är **inte tillgängligt** för ombeställning

>[!NOTE]
>
>Det går att ändra ordning `Not Visible Individually` produkter.

The _Ändra ordning_ knappen visas inte på _Mina beställningar_ och _Visa order_ sidor.

![Sidan med orderinformation](./assets/order-view-page.png){width="700" zoomable="yes"}

### Kundvagnen är inte tom

Om kundvagnen inte är tom och användaren klickar **[!UICONTROL Reorder]** (från _Mina beställningar_  eller _Ordervy_ sida) finns produkterna kvar i varukorgen med de nya beställningsprodukterna.

![Ordna om artiklar](./assets/shopping-cart-view1.png){width="700" zoomable="yes"}

## Ändra ordning från administratören

1. På _Administratör_ sidebar, gå till **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Leta reda på beställningen och öppna i **[!UICONTROL View]** läge.

1. Klicka **[!UICONTROL Reorder]** som visas i det övre knappfältet.

   ![Beställningsinformation i administratören](./assets/order-view-admin.png){width="600" zoomable="yes"}

   När du klickat **[!UICONTROL Reorder]**, _Skapa ny order_ sidan öppnas med produkterna i omordning.

   ![Skapa omordning](./assets/create-reorder-page.png){width="600" zoomable="yes"}

1. Fyll i alla obligatoriska fält efter behov.

1. Klicka för att skicka ordern **[!UICONTROL Submit Order]**.
