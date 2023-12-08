---
title: '[!UICONTROL General] &gt; [!UICONTROL New Relic Reporting]'
description: Granska konfigurationsinställningarna på [!UICONTROL General] &gt; [!UICONTROL New Relic Reporting] sidan för Commerce Admin.
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: 1aec5c618d1f3f7f083523956d2aee62b777faca
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

>[!NOTE]
>Dessa konfigurationsalternativ gäller inte för Adobe Commerce i molninfrastrukturen.
>
>Om du har ett Pro-avtal är New Relic redan [förkonfigurerad och aktiverad som standard](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). Om du deltar i Starter-planen måste du fylla i [Konfigurationssteg för New Relic](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) som ingår i installationsprocessen.

## [!UICONTROL General]

![Allmänt](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/reports/new-relic-reporting.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | Butiksvy | Bestämmer om din butik kan användas med [!DNL New Relic] Rapportering. Alternativ: `Yes` / `No` |
| [!UICONTROL New Relic API URL] | Butiksvy | URL:en där New Relic API:er distribueras. Till exempel: `https://api.newrelic.com/deployments.xml` |
| API-URL för insikter | Butiksvy | URL:en där API:er för Insights distribueras. Använd procentsymbolen (%) för att representera ditt konto-ID. Till exempel: `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | Butiksvy | Konto-ID som tilldelats din [!DNL New Relic] konto. |
| [!UICONTROL New Relic Application ID] | Butiksvy | Program-ID som tilldelats din [!DNL New Relic] konto för Commerce-integrering. |
| [!UICONTROL New Relic API Key] | Butiksvy | Nyckeln som du har tilldelats för att få åtkomst till [!DNL New Relic] API. |
| [!UICONTROL Insights API Key] | Butiksvy | Nyckeln som tilldelas dig för att få tillgång till insikter. |
| [!UICONTROL New Relic Application Name] | Butiksvy | Namnet som du har tilldelat din [!DNL New Relic] integrering. |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | Butiksvy | Ett alternativ för att skicka rapportdata som samlats in för butiken och administratören som separata appar till New Relic. Det här alternativet kräver ett namn för [!UICONTROL New Relic Application Name]. Funktionen lägger till programnamnet med ett understreck till insamlade programdata. Till exempel: `MyStore_Adminhtml`, `MyStore_frontend` |

{style="table-layout:auto"}

## [!UICONTROL Cron]

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://docs.magento.com/user-guide/system/cron.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | Butiksvy | Bestämmer om [!DNL New Relic] kan köras enligt schema med [Cron](../../systems/cron.md). Alternativ: `Yes` / `No` |

{style="table-layout:auto"}
