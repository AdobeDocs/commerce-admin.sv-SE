---
title: Konfigurera loggrotation
description: Konfigurera loggrotation för AEM Assets-integrering för Commerce.
feature: CMS, Media, Integration
source-git-commit: 9e1f80d24eed078b5b28ae2d102c3f3df457081d
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# Konfigurera Experience Manager Assets

AEM Assets Integration för Commerce innehåller följande loggfiler:

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

Be systemadministratören att kontrollera loggfilens rotationsschema för dessa loggar för att förhindra att de blir för stora. I vissa miljöer roteras loggfilerna automatiskt, men i andra miljöer måste du konfigurera loggrotation manuellt. Mer information finns i följande avsnitt:

- Be systemadministratören att konfigurera [loggrotation](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html?lang=sv-SE#server-settings) för lokala Adobe Commerce-installationer.
- Information om projekt för molninfrastruktur finns i [Visa och hantera loggar](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/test/log-locations.html?lang=sv-SE).


