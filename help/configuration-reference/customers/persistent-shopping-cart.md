---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart] i Commerce Admin.
exl-id: d6c5ae46-32ed-4fcd-bcd6-ee3a07d7db5f
feature: Configuration, Shopping Cart
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Persistent Shopping Cart]

{{config}}

>[!NOTE]
>
>En [beständig kundvagn](../../stores-purchase/cart-persistent.md) tillåter kvarhållande av oköpta artiklar som finns kvar i kundvagnen och sparar dem under en period som konfigurerats i _Varaktighet_. Cookies bör tillåtas i kundens webbläsare att använda beständig kundvagn.

## [!UICONTROL General Options]

![Allmänna alternativ](./assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Persistence] | Webbplats | Avgör om persistence är aktiverat. |
| [!UICONTROL Persistence Lifetime (seconds)] | Webbplats | Definierar livstiden för den beständiga cookien i sekunder. Högsta tillåtna värde är 3153600000 sekunder (100 år). |
| [!UICONTROL Enable "Remember Me"] | Webbplats | Definierar om kryssrutan _Kom ihåg mig_ ska visas på inloggnings- och registreringssidorna för butiken. Alternativ: <br/>**`Yes`**- Visar kryssrutan _Kom ihåg mig_.<br/>**`No`** - Visar inte kryssrutan _Kom ihåg mig_ och den beständiga cookien används bara för kunder som redan har den. |
| [!UICONTROL "Remember Me" Default Value] | Webbplats | Definierar standardläget för kryssrutan _Kom ihåg mig_. |
| [!UICONTROL Clear Persistence on Log Out] | Webbplats | Definierar om den beständiga cookien ska tas bort när en butikskund loggar ut. Oavsett hur detta är konfigurerat används den beständiga cookien fortfarande om en kund inte loggar ut, men sessionscookien upphör att gälla. |
| [!UICONTROL Persist Shopping Cart] | Webbplats | Definierar om den beständiga cookien ger åtkomst till kundvagnsdata för korrespondentkontot. Alternativ: <br/>**`Yes`**- innehållet i kundvagnen sparas när sessionen avslutas.<br/>**`No`** - Innehållet i kundvagnen sparas inte när sessionen avslutas. |
| [!UICONTROL Persist Wish List] | Webbplats | ![Adobe Commerce](../../assets/adobe-logo.svg) (endast Adobe Commerce) Anger om tillståndet för kundens önskelistor behålls när sessionen avslutas. Alternativ: <br/>**`Yes`**- Innehållet i önskelistan sparas när sessionen avslutas.<br/>**`No`** - önskelistan sparas inte när sessionen avslutas. |
| [!UICONTROL Persist Recently Ordered Items] | Webbplats | ![Adobe Commerce](../../assets/adobe-logo.svg) (endast Adobe Commerce) Anger om tillståndet för nyligen beställda objekt behålls när sessionen avslutas. Alternativ: <br/>**`Yes`**- Tillståndet för nyligen beställda objekt sparas när sessionen avslutas.<br/>**`No`** - Tillståndet för nyligen sorterade objekt sparas inte när sessionen avslutas. |
| [!UICONTROL Persist Currently Compared Products] | Webbplats | ![Adobe Commerce](../../assets/adobe-logo.svg) (endast Adobe Commerce) Anger om statusen för de produkter som jämförs behålls när sessionen avslutas. Alternativ: <br/>**`Yes`**- Tillståndet för jämförda produkter sparas när sessionen avslutas.<br/>**`No`** - Tillståndet för produkter som jämförs sparas inte när sessionen avslutas. |
| [!UICONTROL Persist Comparison History] | Webbplats | ![Adobe Commerce](../../assets/adobe-logo.svg) (endast Adobe Commerce) Anger om jämförelsehistoriken behålls när sessionen avslutas. Alternativ: <br/>**`Yes`**- Jämförelsehistoriken sparas när sessionen avslutas.<br/>**`No`** - Jämförelsehistoriken sparas inte när sessionen avslutas. |
| [!UICONTROL Persist Recently Viewed Products] | Webbplats | ![Adobe Commerce](../../assets/adobe-logo.svg) (endast Adobe Commerce) Anger om tillståndet för nyligen visade produkter behålls när sessionen avslutas. Alternativ: <br/>**`Yes`**- Tillståndet för nyligen visade produkter sparas när sessionen avslutas.<br/>**`No`** - Tillståndet för nyligen visade produkter sparas inte när sessionen avslutas. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Webbplats | ![Adobe Commerce](../../assets/adobe-logo.svg) (endast Adobe Commerce) Anger om statusen för kundens gruppmedlemskap och segmenteringskriterier behålls när sessionen avslutas. Alternativ: <br/>**`Yes`**- Tillståndet för kundens gruppmedlemskap och segmenteringsdata sparas när sessionen avslutas.<br/>**`No`** - Tillståndet för kundens gruppmedlemskap och segmenteringsdata sparas inte när sessionen avslutas. |

{style="table-layout:auto"}
