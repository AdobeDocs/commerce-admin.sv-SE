---
title: Konfigurationsreferens för beständig varukorg
description: Återanvändbart innehåll för konfigurationsreferensen i kundvagnen.
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# [!UICONTROL General Options]

![Allmänna alternativ](/help/configuration-reference/customers/assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://experienceleague.adobe.com/sv/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-persistent#configure-a-persistent-cart) -->

| Fält | [Omfång](/help/getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |------------------------------------------------------------------------|--- |
| [!UICONTROL Enable Persistence] | Webbplats | Avgör om beständighetsfunktionen är aktiverad. |
| [!UICONTROL Persistence Lifetime (seconds)] | Webbplats | Definierar livstiden för den beständiga cookien i sekunder. Det högsta tillåtna värdet är 34560000 sekunder (400 dagar). Detta är en begränsning av den maximala rekommenderade kaklivstiden. |
| [!UICONTROL Enable "Remember Me"] | Webbplats | Anger om kryssrutan _Kom ihåg mig_ visas på inloggnings- och registreringssidorna för butiken. Alternativ: <br/>**`Yes`**- Visar kryssrutan _Kom ihåg mig_.<br/>**`No`** - Visar inte kryssrutan _Kom ihåg mig_ och den beständiga cookien används bara för kunder som redan har den. |
| [!UICONTROL "Remember Me" Default Value] | Webbplats | Definierar standardläget för kryssrutan _Kom ihåg mig_. |
| [!UICONTROL Clear Persistence on Log Out] | Webbplats | Definierar om den beständiga cookien ska tas bort när en butikskund loggar ut. Oavsett hur det här alternativet är konfigurerat används den beständiga cookien fortfarande om en kund inte loggar ut, men sessionscookien upphör att gälla. |
| [!UICONTROL Persist Shopping Cart] | Webbplats | Definierar om den beständiga cookien ger åtkomst till kundvagnsdata för motsvarande konto. Alternativ: <br/>**`Yes`**&#x200B;eller **`No`**. |
| [!UICONTROL Persist Wish List] | Webbplats | ![Adobe Commerce](/help/assets/adobe-logo.svg) (endast Adobe Commerce) Anger om tillståndet för kundens önskelistor behålls när sessionen avslutas. Alternativ: <br/>**`Yes`**- Innehållet i önskelistan sparas när sessionen avslutas.<br/>**`No`** - önskelistan sparas inte när sessionen avslutas. |
| [!UICONTROL Persist Recently Ordered Items] | Webbplats | ![Adobe Commerce](/help/assets/adobe-logo.svg) (endast Adobe Commerce) Anger om tillståndet för nyligen beställda objekt sparas när sessionen avslutas. Alternativ: <br/>**`Yes`**&#x200B;eller **`No`**. |
| [!UICONTROL Persist Currently Compared Products] | Webbplats | ![Adobe Commerce](/help/assets/adobe-logo.svg) (endast Adobe Commerce) Anger om statusen för produkter som jämförs behålls när sessionen avslutas. Alternativ: <br/>**`Yes`**&#x200B;eller **`No`**. |
| [!UICONTROL Persist Comparison History] | Webbplats | ![Adobe Commerce](/help/assets/adobe-logo.svg) (endast Adobe Commerce) Anger om jämförelsehistoriken ska behållas när sessionen avslutas. Alternativ: <br/>**`Yes`**&#x200B;eller **`No`**. |
| [!UICONTROL Persist Recently Viewed Products] | Webbplats | ![Adobe Commerce](/help/assets/adobe-logo.svg) (endast Adobe Commerce) Anger om tillståndet för nyligen visade produkter behålls när sessionen avslutas. Alternativ: <br/>**`Yes`**&#x200B;eller **`No`**. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Webbplats | ![Adobe Commerce](/help/assets/adobe-logo.svg) (endast Adobe Commerce) Anger om statusen för kundens gruppmedlemskap och segmenteringskriterier behålls när sessionen avslutas. Alternativ: <br/>**`Yes`**- Tillståndet för kundens gruppmedlemskap och segmenteringsdata sparas när sessionen avslutas.<br/>**`No`** - Tillståndet för kundens gruppmedlemskap och segmenteringsdata sparas inte när sessionen avslutas. |

{style="table-layout:auto"}
