---
title: Aktivera resurssynkronisering
description: Lär dig hur du kopplar ihop dina Adobe Commerce- och Experience Manager Assets-projekt för att möjliggöra resurssynkronisering mellan dessa två system.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: e069f0a99ed9289b22cafe06fe2f787912cbba23
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Aktivera resurssynkronisering

Under aktiveringsprocessen registrerar du innehavar-ID:t för projektet med program- och miljö-ID:t för din AEM redigeringsmiljö. Dessa ID:n identifierar det AEM Assets-projekt som du ansluter till och anger autentiseringsuppgifter för att möjliggöra kommunikation mellan Commerce- och AEM Assets-miljöerna.

När du har identifierat AEM resurser väljer du matchningsregel för att synkronisera resurser mellan Adobe Commerce och AEM Assets.

- **[!UICONTROL Match by product SKU]** - Standardregel som matchar SKU:n i resursmetadata med [Commerce-produktens SKU](https://experienceleague.adobe.com/en/docs/commerce-operations/operational-playbook/glossary#sku) för att se till att resurserna är kopplade till rätt produkter.

- **[!UICONTROL Custom match]** - Matchningsregel för mer komplexa scenarier eller specifika affärskrav som kräver anpassad matchningslogik. Implementering av anpassad matchning kräver utveckling av anpassad kod i Adobe Developer App Builder för att definiera hur resurser matchas med produkter. Mer information kommer snart...

Använd standardregeln *Matcha efter produktsku* för inledande introduktion.

## Förutsättningar

- [Konfigurera AEM Experience Manager Assets för att hantera Commerce-resurser](#aem-assets-configure-aem)
- [Installera och konfigurera AEM Assets-integreringen för Commerce](#aem-assets-configure-commerce.md) för att lägga till tillägget och generera nödvändiga autentiseringsuppgifter och anslutningar för att använda tillägget.

## Konfigurera anslutningen

1. Hämta projekt- och miljö-ID:t för [AEM Assets Authoring Environment](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start).

   1. Öppna AEM Sites-konsolen och välj **[!UICONTROL Assets]**.

   1. Kopiera och spara projekt- och miljö-ID:n från URL:en:<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|

1. Öppna AEM Assets Integration-konfigurationen i Commerce Admin.

   1. Gå till **[!UICONTROL Store]** > Konfiguration > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**.

      ![AEM Assets-integrering aktiverar integreringen](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. Ange AEM Assets-miljön **[!UICONTROL Program ID]** och **[!UICONTROL Environment ID]**.

1. Ange **[!UICONTROL Asset Selector IMS Client ID].

   Med [IMS-ID](../getting-started/adobe-ims-config.md) kan du integrera AEM Assets med Page Builder.

1. Välj [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)** för att autentisera begäranden mellan Commerce och tjänsten för tillgångsmatchning.

1. Tillåt att Commerce accepterar inkommande uppdateringar från AEM Assets genom att ange **[!UICONTROL Integration enabled]** till `Yes`.

   När du har aktiverat integreringen konfigurerar du resursmatchningsregeln.

   ![AEM Assets Integration - välj resursmatchningsregel](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Definiera matchningsregeln för resurssynkronisering.

   1. Välj **[!UICONTROL Match by product SKU]**.

   1. Lägg till [AEM Assets-metadatafältnamnet ](aem-assets-configure-aem.md#configure-metadata) som definierats för Commerce produkt-SKU:er i fältet **[!UICONTROL Match by product SKU attribute name]**, till exempel `commerce:skus`.

   ![AEM Assets Integration - välj resursmatchningsregel](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Välj **[!UICONTROL Save Config]** om du vill använda uppdateringar och initiera resurssynkronisering
