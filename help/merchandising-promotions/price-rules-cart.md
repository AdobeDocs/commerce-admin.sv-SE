---
title: Kundprisregler
description: Lär dig mer om kundprisregler som tillämpar rabatter på artiklar i kundvagnen baserat på en uppsättning villkor.
exl-id: f3038f2a-9d34-4696-a39e-f87fbb1294a2
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# Kundprisregler

Kundprisreglerna tillämpar rabatter på artiklar i kundvagnen, baserat på en uppsättning villkor. Rabatten kan tillämpas automatiskt när villkoren är uppfyllda eller när kunden anger en giltig kupongkod. När rabatten används visas den i kundvagnen under delsumman. En kundprisregel kan användas efter behov för en säsong eller en befordran genom att ändra dess status och datumintervall.

>[!NOTE]
>
>Om kupongregeln innehåller villkor som anger utcheckningsalternativ, t.ex. vissa leverans- eller betalningsmetoder, uppfylls villkoren endast i utcheckning när de specifika leverans-/betalningsmetoderna har valts. I så fall kan kupongen användas vid utcheckning i det sista steget.

![Exempel på butiksskylt - kundvagnskupong](./assets/storefront-cart-apply-coupon.png){width="600" zoomable="yes"}

## Få tillgång till kundvagnsprisregler

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**på sidofältet_ Admin _.

   ![Kundprisregel](./assets/price-rule-cart.png){width="700" zoomable="yes"}

1. Om du har många regler använder du filteralternativen längst upp i varje kolumn för att effektivisera listan och klickar på **[!UICONTROL Search]** för att tillämpa filtren.

1. Om du vill rensa alla filteralternativ och visa hela listan klickar du på **[!UICONTROL Reset Filter]**.

1. Uppdatera egenskaper för en regel:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Klicka på **[!UICONTROL Edit]** för att visa sidan Regelinformation.

   - ![Magento Open Source](../assets/open-source.svg) (endast Magento Open Source) Klicka på regeln i listan för att visa sidan Regelinformation.

   Där kan du ändra inställningarna för linjen (ungefär som när du skapar en regel).

## Filteralternativ efter kolumn

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL ID] | Ange text för att filtrera listan efter ett visst regel-ID-nummer. |
| [!UICONTROL Rule] | Ange text för att filtrera listan baserat på det regelnamn som definierades när regeln skapades. |
| [!UICONTROL Coupon Code] | Ange text för att filtrera listan baserat på det kodnamn som definierades när regeln skapades. |
| [!UICONTROL Priority] | Fritextfält som filtrerar listan baserat på den prioritet som har definierats för en regel. |
| [!UICONTROL Status] | Använd det här alternativet om du vill filtrera listan baserat på regelstatus (`Active` eller `Inactive`). |
| [!UICONTROL Web Site] | Använd det här alternativet om du vill filtrera listan baserat på webbplatser som definierats för en regel. |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Klicka på **[!UICONTROL Edit]** för att visa sidan _[!UICONTROL Rule Information]_och uppdatera regelinställningarna (ungefär som att skapa en regel). |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) (endast Magento Open Source) Använd de dynamiska kalenderfälten (_[!UICONTROL To:]_och_[!UICONTROL From:]_) för att filtrera listan baserat på regelns startdatum så som det definierades när regeln skapades. |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) (endast Magento Open Source) Använd de dynamiska kalenderfälten (_[!UICONTROL To:]_och_[!UICONTROL From:]_) för att filtrera listan baserat på slutdatumet för regeln som definierades när regeln skapades. |

{style="table-layout:auto"}

## Använd Real-Time CDP målgrupper för att informera om kundvagnsregler

Lär dig hur du [aktiverar](../customers/audience-activation.md) Real-Time CDP-målgrupper i din Adobe Commerce-instans för att informera om kundprisregler.
