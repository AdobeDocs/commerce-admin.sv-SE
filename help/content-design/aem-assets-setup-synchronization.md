---
title: Aktivera resurssynkronisering
description: Lär dig hur du kopplar ihop dina Adobe Commerce- och Experience Manager Assets-projekt för att möjliggöra resurssynkronisering mellan dessa två system.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: d8e255259e4a8b87c63a4d1c013b4c1feb2b29cb
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# Aktivera resurssynkronisering

Aktivera resurssynkronisering genom att uppdatera Commerce-miljökonfigurationen för att ansluta Commerce till AEM Assets-instansen. Integreringen möjliggör synkronisering av resurser mellan Commerce och AEM Assets, vilket säkerställer att produktbilder och andra resurser alltid är uppdaterade.

När du har identifierat AEM-resursprojektet väljer du matchningsregeln för att synkronisera resurser mellan Adobe Commerce och AEM Assets.

- **[!UICONTROL Match by product SKU]** - Standardregel som matchar SKU:n i resursmetadata med [Commerce-produktens SKU](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/glossary#sku) för att se till att resurserna är kopplade till rätt produkter.

- **[!UICONTROL Custom match]** - Matchningsregel för mer komplexa scenarier eller specifika affärskrav som kräver anpassad matchningslogik. Implementering av anpassad matchning kräver utveckling av anpassad kod i Adobe Developer App Builder för att definiera hur resurser matchas med produkter. Mer information kommer snart...

Använd standardregeln *Matcha efter produktsku* för inledande introduktion.

## Förutsättningar

- [Konfigurera AEM Assets för hantering av Commerce-resurser](aem-assets-configure-aem.md)

- [Installera och konfigurera AEM Assets-integreringen för Commerce](aem-assets-configure-commerce.md) för att lägga till tillägget och generera nödvändiga autentiseringsuppgifter och anslutningar för att använda tillägget.

- Skapa en supportanmälan för att begära aktivering av AEM Assets Integration. Du måste ange **[!UICONTROL Program ID]**, **[!UICONTROL Environment ID]** och **[!UICONTROL IMS Org ID]** för den AEM Assets-redigeringsmiljö som du vill ansluta till Commerce.

  >[!TIP]
  >
  > (Valfritt) Ange **[!UICONTROL Asset Selector IMS Client ID]** om det är tillgängligt. Se [ImsAuthProps](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app) i dokumentationen för *AEM Assets Selector* .

## Konfigurera anslutningen

1. Hämta projekt- och miljö-ID:t för [AEM Assets Authoring Environment](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start).

   1. Öppna AEM Sites-konsolen och välj **[!UICONTROL Assets]**.

   1. Kopiera och spara projekt- och miljö-ID:n från URL:en:<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`
1. Öppna AEM Assets Integration-konfigurationen i Commerce Admin.

   1. Gå till **[!UICONTROL Store]** > Konfiguration > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**.

      ![AEM Assets-integrering aktiverar integreringen](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. Ange AEM Assets-miljön **[!UICONTROL Program ID]** och **[!UICONTROL Environment ID]**.

   Redigera konfigurationsvärdena genom att ta bort markeringen från *[!UICONTROL Use system value]*.

1. Ange **[!UICONTROL Asset Selector IMS Client ID]**, om tillgängligt.

   [Klient-ID:t för IMS-klient ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app#ims-auth-props) för resursväljaren krävs av [!UICONTROL Assets Selector], en AEM Assets-funktion som gör att användare kan bädda in visuella resurser direkt på Commerce produktsidor.

1. Välj [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment) för autentisering av begäranden mellan Commerce och tjänsten för tillgångsmatchning.

1. Ange **[!UICONTROL Integration enabled]** till `Yes` om du vill tillåta att Commerce accepterar inkommande uppdateringar från AEM Assets.

   När integreringen har aktiverats finns det ytterligare konfigurationsalternativ som du kan använda för att ange matchningsvillkor för resurser.

1. Definiera matchningsregeln för resurssynkronisering.

   1. Välj **[!UICONTROL Match by product SKU]** eller **[!UICONTROL Custom match (Requires App Builder)]**.

   1. Lägg till [AEM Assets-metadatafältnamnet ](aem-assets-configure-aem.md#configure-metadata) som definierats för Commerce produkt-SKU:er i fältet **[!UICONTROL Match by product SKU attribute name]**, till exempel `commerce:skus`.

1. Välj **[!UICONTROL Save Config]** om du vill använda uppdateringar och initiera resurssynkronisering.

   Konfigurationsuppdateringen utlöser den inledande synkroniseringsprocessen, vilket gör att Commerce kan acceptera inkommande uppdateringar från AEM Assets. Den tid som krävs för synkronisering beror på mängden resurser och specifika konfigurationer. Integreringen utnyttjar automatiserade processer för att minimera den tid som krävs för synkronisering.

## Nästa steg

[Använd AEM Assets med Commerce](aem-assets-manage.md)
