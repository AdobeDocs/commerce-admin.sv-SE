---
title: Konfigurera loggrotation
description: Konfigurera loggrotation för AEM Assets-integrering för Commerce.
feature: CMS, Media, Integration
exl-id: f735d086-048c-4555-bc58-ac6736c281b0
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# Konfigurera Experience Manager Assets

AEM Assets Integration för Commerce innehåller följande loggfiler i din Commerce-instans:

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

Be systemadministratören att kontrollera loggfilens rotationsschema för dessa loggar för att förhindra att de blir för stora. I vissa miljöer roteras loggfilerna automatiskt, men i andra miljöer måste du konfigurera loggrotation manuellt. Mer information finns i följande avsnitt:

- Be systemadministratören att konfigurera [loggrotation](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html#server-settings) för lokala Adobe Commerce-installationer.
- Information om projekt för molninfrastruktur finns i [Visa och hantera loggar](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/test/log-locations.html).
