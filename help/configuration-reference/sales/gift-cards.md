---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Gift Cards]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Sales] &gt; [!UICONTROL Gift Cards] i Commerce Admin.
exl-id: 95bfdbde-633e-44d0-9d43-00dde671ab6d
feature: Configuration, Gift
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Gift Cards]

{{ee-feature}}

{{config}}

## [!UICONTROL Gift Card Email Settings]

![Inställningar för e-post med presentkort](./assets/gift-cards-gift-card-email-settings.png)<!-- zoom -->

<!-- [Gift Card Email Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Gift Card Notification Email Sender] | Butiksvy | Identifierar den [butikskontakt](../../getting-started/store-details.md#store-email-addresses) som visas som avsändare av presentkortsmeddelandet. Standardvärde: `General Contact` |
| [!UICONTROL Gift Card Notification Email Template] | Butiksvy | Bestämmer [mallen](../../systems/email-templates.md) som används för presentkortets e-postmeddelande. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card General Settings]

![Allmänna inställningar för presentkort](./assets/gift-cards-gift-card-general-settings.png)<!-- zoom -->

<!-- [Gift Card General Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Redeemable] | Global | Avgör om innehavaren av presentkortet kan lösa in sitt kontantvärde. Alternativ: `Yes` / `No`. |
| [!UICONTROL Lifetime (days)] | Global | Anger antalet dagar som kortet är giltigt. Om kortet lämnas tomt upphör det inte att gälla. <br/><br/>**_Viktigt!_**På vissa platser är det inte tillåtet att ange förfallodata för presentkort. Kontrollera de lokala lagarna innan du anger en livstid för dina presentkort. |
| [!UICONTROL Allow Gift Message] | Butiksvy | Avgör om möjligheten att inkludera ett presentmeddelande är tillgängligt för kunder som köper ett presentkort. Alternativ: `Yes` / `No`. |
| [!UICONTROL Gift Message Maximum Length] | Butiksvy | Anger det maximala antalet tecken som tillåts i ett presentkortsmeddelande. Standardvärde: 255 |
| [!UICONTROL Generate Gift Card Account when Order Item is] | Global | Avgör om ett presentkortskonto genereras när en kund gör en beställning eller när ordern faktureras. Alternativ: `Ordered` / `Invoiced` |

{style="table-layout:auto"}

## [!UICONTROL Email Sent from Gift Card Account Management]

![E-post skickad från presentkortskontohantering](./assets/gift-cards-email-sent-from-account.png)<!-- zoom -->

<!-- [Email Sent from Gift Card Account Management](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Gift Card Email Sender] | Butiksvy | Identifierar den [butikskontakt](../../getting-started/store-details.md#store-email-addresses) som visas som avsändare av presentkortets e-postmeddelande. Standardvärde: `General Contact` |
| [!UICONTROL Gift Card Template] | Butiksvy | Bestämmer [mallen](../../systems/email-templates.md) som används för presentkortets e-postadress. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card Account General Settings]

![Allmänna inställningar för presentkortskonto](./assets/gift-cards-gift-card-account-general-settings.png)<!-- zoom -->

<!-- [Gift Card Account General Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Code Length] | Global | Anger längden på presentkortskoden. |
| [!UICONTROL Code Format] | Global | Bestämmer formatet för presentkortskoden. Alternativ: `Alphanumeric` / `Numeric` |
| [!UICONTROL Code Prefix] | Global | Definierar alla prefix som har lagts till i början av koden. |
| [!UICONTROL Code Suffix] | Global | Definierar alla suffix som har lagts till i slutet av koden. |
| [!UICONTROL Dash Every X Characters] | Global | Om du vill ta med streck i koden bestämmer du antalet tecken mellan varje streck. |
| [!UICONTROL New Pool Size] | Global | Anger storleken på den nya kodpoolen som ska genereras. |
| [!UICONTROL Low Code Pool Threshold] | Global | Fastställer antalet poster i kodpoolen som utlöser en varning om att poolen måste fyllas på. |
| [!UICONTROL Generate] | Global | Klicka för att generera en lista med presentkortskoder. |

{style="table-layout:auto"}
