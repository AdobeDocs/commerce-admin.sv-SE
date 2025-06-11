---
title: Konfigurera AEM Assets Integration för Commerce
description: Lär dig hur du konfigurerar och konfigurerar din Experience Manager Assets-miljö för att hantera Commerce-resurser för din butik.
feature: CMS, Media, Configuration
exl-id: 699f517e-1545-4c22-aa8d-9c8d60d352af
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# Konfigurera AEM Assets Integration för Commerce

För att kunna konfigurera Adobe Experience Manager Assets-integrationen för Commerce måste du ha administratörsbehörighet för att kunna anpassa program- och miljökonfigurationen.

- Administrativ åtkomst till det Cloud Manager-program där AEM Assets as a Cloud Service-miljöerna etableras.

- Administrativ åtkomst till Adobe Commerce-miljön och möjlighet att hämta eller generera de API-nycklar som krävs för autentisering.

## Krav för att använda integreringen

För att utnyttja integreringen måste företagen uppfylla följande krav:

- Aktiva licenser för Adobe Commerce, Adobe Experience Manager Assets och [AEM Dynamic Media](https://experienceleague.adobe.com/sv/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media).

- Adobe Commerce 2.4.5+

- Adobe Experience Manager etableras med [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/sv/docs/experience-manager-cloud-service/content/assets/overview)

- Den Adobe Commerce-användare som konfigurerar integreringen måste ha tillgång till den [IMS-organisation](https://experienceleague.adobe.com/sv/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) där AEM Assets-projektet etableras.

## Viktiga fördelar

- **Ingen extra kostnad** - Den här integreringen tillhandahålls kostnadsfritt för handlare som uppfyller licensieringskraven.

- **officiell Adobe-lösning** - Utvecklad, underhållen och stöds fullt ut av Adobe, vilket garanterar stabilitet och anpassning till framtida plattformsförbättringar.

- **Adobe Managed Support Model** - Adobe hanterar hjälp och felsökning, vilket ger sinnesro och smidig problemlösning.

## Nästa steg

Att möjliggöra Commerce-integrering med Experience Manager Assets är en trestegsprocess:

1. [Installera AEM Assets-paketet](aem-assets-configure-aem.md).

1. [Installera Adobe Commerce-paket](aem-assets-configure-aem.md).

1. [Konfigurera integrationsresursen](aem-assets-setup-synchronization.md).
