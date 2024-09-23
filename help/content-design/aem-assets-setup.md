---
title: Konfigurera AEM Assets Integration
description: Läs mer om kraven och stegen för att konfigurera integreringen mellan Adobe Commerce och AEM Assets as a Cloud Service.
feature: CMS, Media, Configuration, Integration
source-git-commit: df21ea9a797a4f11d0104cf34134ced3bbabbdf4
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# Konfigurera AEM Assets Integration

Aktivera avancerade funktioner för resurshantering genom att konfigurera AEM Assets-miljön och installera och konfigurera AEM Assets-integreringen för Commerce.

När integreringen är aktiv kan administratörer använda Experience Manager Assets as a Cloud Service som en enda källa till sanning för att skapa och hantera resurser och som ett centralt digitalt resurshanteringsverktyg (DAM) för att skapa, hantera, organisera och distribuera material för Commerce-projekt.

## Krav

- Adobe Commerce 2.4.5+
   - PHP 8.1, 8.2, 8.3
   - Disposition: 2.x
- Adobe Experience Manager har etablerats med [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/overview)
- Den Adobe Commerce-användare som konfigurerar integreringen måste ha tillgång till den [IMS-organisation](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) där AEM Assets-projektet etableras.

## Konfigurera integreringen

>[!BEGINSHADEBOX]

**Förutsättningar**

För att kunna konfigurera AEM Assets-integreringen måste du ha administratörsbehörighet för att kunna anpassa program- och miljökonfigurationen.

- Administrativ åtkomst till Cloud Manager där AEM Assets as a Cloud Service miljöer etableras.
- Administrativ åtkomst till Adobe Commerce-miljön och möjlighet att hämta eller generera API-nycklar som krävs för autentisering.

>[!ENDSHADEBOX]

Att möjliggöra Commerce-integrering med Experience Manager Assets är en trestegsprocess:

1. [Konfigurera ditt Experience Manager Assets-projekt för att hantera Commerce-resurser](aem-assets-configure-aem.md).

1. [Installera Experience Manager Assets Integration-tillägget och konfigurera Adobe Commerce](aem-assets-configure-aem.md).

1. [Aktivera resurssynkronisering](aem-assets-setup-synchronization.md).
