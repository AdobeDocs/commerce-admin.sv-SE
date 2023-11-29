---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Wish List]'
description: Granska konfigurationsinställningarna på [!UICONTROL Customers] &gt; [!UICONTROL Wish List] sidan för Commerce Admin.
exl-id: 33ff428c-03e3-4698-a01e-f007b4e1688e
feature: Configuration, Customers, Storefront
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Wish List]

{{config}}

>[!NOTE]
>
>Med en önskelista kan registrerade kunder skapa egna produktsamlingar som de vill köpa i framtiden. Önsklistorna kan delas mellan kunder.

## [!UICONTROL General Options]

![Allmänna alternativ](./assets/wishlist-general-options.png)<!-- zoom -->

<!--[General Options](https://docs.magento.com/user-guide/marketing/wishlist-configuration.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Butiksvy | Aktiverar önskelistemodulen för din butik. Alternativ: `Yes` / `No` |
| [!UICONTROL Show in Sidebar] | Butiksvy | Anger synlighet för önskelistorna i sidofältet. <br/>Alternativ: `Yes` / `No` |
| [!UICONTROL Enable Multiple Wish Lists] | Butiksvy | ![Adobe Commerce](../../assets/adobe-logo.svg) (Endast Adobe Commerce) När inställt på `Yes`, gör det möjligt för kunderna att skapa och underhålla flera önskelistor. Alternativ: `Yes` / `No` |
| [!UICONTROL Number of Multiple Wish Lists] | Butiksvy | ![Adobe Commerce](../../assets/adobe-logo.svg) (Endast Adobe Commerce) Om flera önskelistor är aktiverade, bestämmer du det maximala antalet önskelistor som kunder kan ha associerat med sitt konto. |

{style="table-layout:auto"}

## [!UICONTROL Share Options]

![Delningsalternativ](./assets/wishlist-share-options.png)<!-- zoom -->

<!-- [Share Options](https://docs.magento.com/user-guide/marketing/wishlist-configuration.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Email Sender] | Butiksvy | Anger den butikskontakt som visas som avsändare av det meddelande som skickas när en önskelista delas. Standardkontakt: `General Contact` |
| [!UICONTROL Email Template] | Butiksvy | Bestämmer e-postmallen som används för meddelandet som skickas när en önskelista delas. Standardmall: `Share Wishlist` |
| [!UICONTROL Max Emails Allowed to be Sent] | Butiksvy | Anger det maximala antalet e-postmeddelanden som kan skickas i en batch. Om du anger en maxgräns kan belastningen på servern minskas. Högsta tillåtna antal är 10 000. Standardvärde: `10` |
| [!UICONTROL Email Text Length Limit] | Butiksvy | Anger det maximala antalet tecken som kan inkluderas i meddelandet. Högsta tillåtna antal är 10 000. Standardvärde: `255` |

{style="table-layout:auto"}

## [!UICONTROL My Wish List Link]

![Länk till Min önskelista](./assets/wishlist-my-wishlist-link.png)<!-- zoom -->

<!--[My Wish List Link](https://docs.magento.com/user-guide/marketing/wishlist-configuration.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Display Wish List Summary] | Webbplats | Konfigurerar visningen av Önsklistesammanfattning på kundkontouppsättningen. Alternativ: `Display number of items in wish list` / `Display item quantities` |

{style="table-layout:auto"}
