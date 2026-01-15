---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Shipping Settings]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Sales] &gt; [!UICONTROL Shipping Settings] i Commerce Admin.
exl-id: d7d46946-f8c9-4714-96c3-2173e28f7bfa
feature: Configuration, Shipping/Delivery
source-git-commit: 528e57df775b53b6137e1542ad0583c60d2f47ff
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Shipping Settings]

{{config}}

Mer information om hur du ändrar de här inställningarna finns i [Leveransinställningar](../../stores-purchase/shipping-settings.md) i _butiker och inköpsupplevelseguiden_.

## [!UICONTROL Origin]

![Ursprung](./assets/shipping-settings-origin.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Country] | Webbplats | Ursprungslandet. |
| [!UICONTROL Region/State] | Webbplats | Ursprungsregionen eller ursprungsstaten. |
| [!UICONTROL ZIP/Postal Code] | Webbplats | Postnummer eller postnummer för ursprungsorten. |
| [!UICONTROL City] | Webbplats | Ort till ursprungsplatsen. |
| [!UICONTROL Street Address] | Webbplats | Gatuadress till ursprungsplatsen. |
| [!UICONTROL Street Address Line 2] | Webbplats | En extra rad för gatuadressen till ursprungsplatsen, om det behövs. |

{style="table-layout:auto"}

## [!UICONTROL Shipping Policy Parameters]

![Parametrar för leveransprincip](./assets/shipping-settings-shipping-policy-parameters.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Apply Custom Shipping Policy] | Webbplats | Anger om din leveransprofil visas under utcheckningen. Alternativ: `Yes` / `No` |
| [!UICONTROL Shipping Policy] | Butiksvy | Innehåller din leveranspolicy som text. |

{style="table-layout:auto"}

## [!UICONTROL Shipment Tracking URLs]

[!BADGE Endast SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce as a Cloud Service-projekt (SaaS-infrastruktur som hanteras av Adobe)."}

[!BADGE Sandbox]{type=Caution tooltip="Objekten i listan är för närvarande bara tillgängliga i sandlådemiljöer. Adobe gör nya releaser tillgängliga i sandlådemiljöer först för att ge dig tid att testa kommande ändringar innan releasen är tillgänglig i produktionsmiljöer."}

![Parametrar för leveransprincip](./assets/shipping-settings-shipment-tracking-urls.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Custom Tracking URLs] | Butiksvy | Avgör om leveransspårningsnummer som skickas i kundmeddelanden är länkar eller oformaterad text. Standardvärdet `No` anger att siffrorna är oformaterad text. Alternativ: `Yes` / `No` |
| [!UICONTROL USPS Tracking URL] | Butiksvy | URL-mallen för försändelser från United States Postal Service. |
| [!UICONTROL UPS Tracking URL] | Butiksvy | URL-mallen för försändelser från United Parcel Service. |
| [!UICONTROL FedEx Tracking URL] | Butiksvy | URL-mallen för Federal Express-leveranser. |
| [!UICONTROL DHL Tracking URL] | Butiksvy | URL-mallen för DHL Express-leveranser. |

{style="table-layout:auto"}
