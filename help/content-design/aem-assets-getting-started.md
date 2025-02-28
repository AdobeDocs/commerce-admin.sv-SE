---
title: Konfigurera AEM Assets Integration för Commerce
description: Lär dig hur du kan introducera Experience Manager Assets med din [!DNL Commerce] instans för att få tillgång till ett oändligt antal mediefiler som kan användas i din butik.
feature: CMS, Media, Configuration
source-git-commit: c109edc9d9277baafd61da1df0f1917f07089353
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# Konfigurera AEM Assets Integration för Commerce

För att kunna konfigurera AEM Assets-integreringen måste du ha administratörsbehörighet för att kunna anpassa program- och miljökonfigurationen.

- Administrativ åtkomst till det Cloud Manager-program där AEM Assets as a Cloud Service-miljöerna etableras.

- Administrativ åtkomst till Adobe Commerce-miljön och möjlighet att hämta eller generera API-nycklar som krävs för autentisering.

## Krav för att använda integreringen

För att utnyttja integreringen måste företagen uppfylla följande krav:

- Aktiva licenser för Adobe Commerce, AEM Assets och [AEM Dynamic Media](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media).

- Adobe Commerce 2.4.5+

   - PHP 8.1, 8.2, 8.3
   - Disposition: 2.x

- Adobe Experience Manager etableras med [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/overview)

- Den Adobe Commerce-användare som konfigurerar integreringen måste ha tillgång till den [IMS-organisation](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) där AEM Assets-projektet etableras.

## Viktiga fördelar

- **Ingen extra kostnad** - Den här integreringen tillhandahålls kostnadsfritt för handlare som uppfyller licensieringskraven.

- **officiell Adobe-lösning** - Utvecklad, underhållen och stöds fullt ut av Adobe, vilket garanterar stabilitet och anpassning till framtida plattformsförbättringar.

- **Adobe Managed Support Model** - Hjälp och felsökning hanteras direkt av Adobe, vilket ger sinnesro och smidig problemlösning.

## Nästa steg

Att möjliggöra Commerce-integrering med Experience Manager Assets är en trestegsprocess:

1. [Konfigurera ditt AEM-resursprojekt för att hantera Adobe Commerce-resurser](aem-assets-configure-aem.md).

1. [Installera AEM-filnamnsintegreringstillägget och konfigurera Adobe Commerce](aem-assets-configure-aem.md).

1. [Aktivera resurssynkronisering](aem-assets-setup-synchronization.md).
