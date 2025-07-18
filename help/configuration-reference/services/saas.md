---
title: '[!UICONTROL Services] &gt; [!UICONTROL Commerce Services Connector]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Services] &gt; [!UICONTROL Commerce Services Connector] i Commerce Admin.
exl-id: 3570e846-c8ab-4a36-b020-1b536bbd377d
feature: Configuration, Saas
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 0020db425032254fb7661701533d1e700d98260c
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---

# [!UICONTROL Services] > [!UICONTROL Commerce Services Connector]

Mer information om hur du ansluter din butik till Adobe Commerce tjänster finns i [Commerce Services](https://experienceleague.adobe.com/docs/commerce/user-guides/integration-services/saas.html?lang=sv-SE).

{{config}}

## [!UICONTROL Sandbox API Keys]

![API-nyckel för sandlåda](./assets/sandbox-key-saas-configuration.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Sandbox public API key] | Global | API-nyckel som identifierar författaren och deras rättigheter, om sådana finns. |
| [!UICONTROL Sandbox private API key] | Global | En privat nyckel som är associerad med API-nyckeln. |

{style="table-layout:auto"}

## [!UICONTROL Production Keys]

![API-nyckel för produktion](./assets/prod-key-saas-configuration.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Production public API key] | Global | API-nyckel som identifierar författaren och deras rättigheter, om sådana finns. |
| [!UICONTROL Production private API key] | Global | En privat nyckel som är associerad med API-nyckeln. |

{style="table-layout:auto"}

## [!UICONTROL SaaS Identifier]

![SaaS-identifierare](./assets/saas-identifier.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Project] | Global | Namnet på det SaaS-projekt som grupperar alla dina SaaS-datamallar. En _Skapa projekt_-knapp visas om det inte finns några SaaS-projekt. |
| [!UICONTROL Data Space] | Global | Visar en lista över SaaS-datautrymmen i det angivna SaaS-projektet. Antalet SaaS-datamallar beror på din [Commerce-licens](https://experienceleague.adobe.com/docs/commerce/user-guides/integration-services/saas.html?lang=sv-SE):<br />Adobe Commerce - ett produktionsdatautrymme; två testdatamallar;<br />Magento Open Source - ett produktionsdatautrymme; inga testdatamallar |

{style="table-layout:auto"}

## [!UICONTROL IMS Organization]

![IMS-organisation](./assets/ims-organization.png)<!-- zoom -->

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Sign in using Adobe ID] | Din Adobe ID är vanligtvis den e-postadress du använde när du startade ditt medlemskap eller köpte ett program eller en tjänst från Adobe. Din Adobe ID är nyckeln du behöver för att komma åt ditt Adobe-konto. |

{style="table-layout:auto"}
