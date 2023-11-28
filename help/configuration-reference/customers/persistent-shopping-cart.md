---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart]'
description: Granska konfigurationsinställningarna på [!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart] sidan för Commerce Admin.
exl-id: d6c5ae46-32ed-4fcd-bcd6-ee3a07d7db5f
feature: Configuration, Shopping Cart
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Persistent Shopping Cart]

{{config}}

>[!NOTE]
>
>A [Beständig kundvagn](../../stores-purchase/cart-persistent.md) tillåter lagring av oköpta artiklar som finns kvar i vagnen och sparar dem under en period som konfigurerats i _Varaktighet, livstid_. Cookies bör tillåtas i kundens webbläsare att använda beständig kundvagn.

## [!UICONTROL General Options]

![Allmänna alternativ](./assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Persistence] | Webbplats | Avgör om persistence är aktiverat. |
| [!UICONTROL Persistence Lifetime (seconds)] | Webbplats | Definierar livstiden för den beständiga cookien i sekunder. Högsta tillåtna värde är 3153600000 sekunder (100 år). |
| [!UICONTROL Enable "Remember Me"] | Webbplats | Definierar om _Kom ihåg mig_ kryssrutan visas på inloggnings- och registreringssidorna för butiken. Alternativ: <br/>**`Yes`**- Visar _Kom ihåg mig_ kryssrutan.<br/>**`No`** - Visar inte _Kom ihåg mig_ och den beständiga cookien används bara för kunder som redan har den. |
| [!UICONTROL "Remember Me" Default Value] | Webbplats | Definierar standardläget för _Kom ihåg mig_ kryssrutan. |
| [!UICONTROL Clear Persistence on Log Out] | Webbplats | Definierar om den beständiga cookien ska tas bort när en butikskund loggar ut. Oavsett hur detta är konfigurerat används den beständiga cookien fortfarande om en kund inte loggar ut, men sessionscookien upphör att gälla. |
| [!UICONTROL Persist Shopping Cart] | Webbplats | Definierar om den beständiga cookien ger åtkomst till kundvagnsdata för korrespondentkontot. Alternativ: <br/>**`Yes`**- Kundvagnens innehåll sparas när sessionen är slut.<br/>**`No`** - Kundvagnens innehåll sparas inte när sessionen är slut. |
| [!UICONTROL Persist Wish List] | Webbplats | ![Adobe Commerce](../../assets/adobe-logo.svg) (Endast Adobe Commerce) Anger om tillståndet för kundens önskelistor behålls när sessionen avslutas. Alternativ: <br/>**`Yes`**- Innehållet i önskelistan sparas när sessionen avslutas.<br/>**`No`** - Önsterlistan sparas inte när sessionen avslutas. |
| [!UICONTROL Persist Recently Ordered Items] | Webbplats | ![Adobe Commerce](../../assets/adobe-logo.svg) (Endast Adobe Commerce) Anger om tillståndet för nyligen beställda objekt behålls när sessionen avslutas. Alternativ: <br/>**`Yes`**- Tillståndet för nyligen beställda objekt sparas när sessionen avslutas.<br/>**`No`** - Tillståndet för nyligen beställda objekt sparas inte när sessionen avslutas. |
| [!UICONTROL Persist Currently Compared Products] | Webbplats | ![Adobe Commerce](../../assets/adobe-logo.svg) (Endast Adobe Commerce) Anger om statusen för jämförda produkter behålls när sessionen avslutas. Alternativ: <br/>**`Yes`**- De produkter som jämförs sparas när sessionen avslutas.<br/>**`No`** - De produkter som för närvarande jämförs sparas inte när sessionen avslutas. |
| [!UICONTROL Persist Comparison History] | Webbplats | ![Adobe Commerce](../../assets/adobe-logo.svg) (Endast Adobe Commerce) Anger om jämförelsehistoriken ska behållas när sessionen avslutas. Alternativ: <br/>**`Yes`**- Status för jämförelsehistorik sparas när sessionen avslutas.<br/>**`No`** - Jämförelsehistoriken sparas inte när sessionen avslutas. |
| [!UICONTROL Persist Recently Viewed Products] | Webbplats | ![Adobe Commerce](../../assets/adobe-logo.svg) (Endast Adobe Commerce) Anger om tillståndet för nyligen visade produkter behålls när sessionen avslutas. Alternativ: <br/>**`Yes`**- Tillståndet för nyligen visade produkter sparas när sessionen avslutas.<br/>**`No`** - Tillståndet för nyligen visade produkter sparas inte när sessionen avslutas. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | Webbplats | ![Adobe Commerce](../../assets/adobe-logo.svg) (Endast Adobe Commerce) Anger om statusen för kundens gruppmedlemskap och segmenteringskriterier behålls när sessionen avslutas. Alternativ: <br/>**`Yes`**- Status för kundens gruppmedlemskap och segmenteringsdata sparas när sessionen avslutas.<br/>**`No`** - Tillståndet för kundens gruppmedlemskap och segmenteringsdata sparas inte när sessionen avslutas. |

{:style=&quot;table-layout:auto&quot;}
