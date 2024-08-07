---
title: Aktivera resurssynkronisering
description: Lär dig hur du kopplar ihop dina Adobe Commerce- och Experience Manager Assets-projekt för att möjliggöra resurssynkronisering mellan dessa två system.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: 508e9e1d23a4b6e70ada22e2a22c0dcd401393a9
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Aktivera resurssynkronisering

>[!BEGINSHADEBOX]

**Förutsättningar**

- [Konfigurera AEM Experience Manager Assets för att hantera Commerce-resurser](#aem-assets-configure-aem)
- [Installera och konfigurera AEM Assets-integreringen för Commerce](#aem-assets-configure-commerce.md) för att lägga till tillägget och generera nödvändiga autentiseringsuppgifter och anslutningar för att använda tillägget.

>[!ENDSHADEBOX]

Under den här aktiveringsprocessen registrerar du ditt klient-ID genom att ange program- och miljö-ID för din AEM utvecklingsmiljö. Dessa ID:n identifierar det AEM Assets-projekt som du ansluter till och tillhandahåller autentiseringsuppgifter för kommunikation och arbetsflöden mellan Commerce och AEM Assets.

När du har identifierat AEM resurser väljer du den matchande regel som ska användas för att synkronisera resurser mellan Adobe Commerce och AEM Assets.

AEM Assets Integration för Commerce har stöd för två matchande regler för att synkronisera resurser mellan Adobe Commerce och AEM Assets.

- **Matcha efter produkt-SKU** - Det här är standardmatchningsregeln som matchar resurser baserat på lagerinställningarna (SKU) för produkten. SKU:n är en unik identifierare för varje produkt. Den här regeln matchar SKU:n i resursmetadata med Commerce-produktens SKU för att säkerställa att resurserna är kopplade till rätt produkter.

- **Anpassad matchning** - Den här matchningsregeln gäller för mer komplexa scenarier eller specifika affärskrav som kräver anpassad matchningslogik. Om du vill använda den här regeln måste du ha implementerad anpassad kod i Adobe Developer App Builder som definierar hur resurser matchas med produkter. Mer information kommer snart...

Använd standardregeln `Match by product sku` för inledande introduktion. Om det behövs kan du ändra matchningsregeln senare.

## Aktivera integreringen

1. Hämta projekt- och miljö-ID:t för din [AEM Assets-redigeringsmiljö](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start).

   1. Öppna AEM Sites-konsolen och välj **[!UICONTROL Assets]**.

   1. Kopiera och spara projekt- och miljö-ID:n från URL:en:<br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`|

1. Öppna AEM Assets Integration-konfigurationen i Commerce Admin.

   1. Välj **[!UICONTROL Store]** > Konfiguration > **[!UICONTROL CATALOG]** > **[!UICONTROL Catalog]**.

   1. Expandera **[!UICONTROL Experience Manager Assets integration]**.

      ![AEM Assets-integrering aktiverar integreringen](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. Identifiera det Experience Manager Assets-projekt som du vill ansluta till genom att ange **[!UICONTROL Program ID]** och **[!UICONTROL Environment ID]**.

1. Lägg till OAUTH-autentiseringsuppgifterna för att autentisera API-begäranden mellan Adobe Commerce och ARES-tjänsten genom att välja **[[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)**, till exempel `Assets integration`.

1. Tillåt att Commerce accepterar inkommande uppdateringar från AEM Assets genom att ange **[!UICONTROL Enable integration]** till `Yes`.

   När du har aktiverat integreringen kan du konfigurera resursmatchningsregeln.

   ![AEM Assets Integration - välj resursmatchningsregel](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. Definiera matchningsregeln för resurssynkronisering.

   1. Välj **[!UICONTROL Match by product SKU]**.

   1. Lägg till [AEM Assets-metadatafältnamnet ](aem-assets-configure-aem.md#configure-metadata) som definierats för Commerce produkt-SKU:er i fältet **[!UICONTROL Match by product SKU attribute name]**, till exempel `commerce:skus`.

1. Använd konfigurationen och initiera synkroniseringsprocessen genom att välja **[!UICONTROL Save Config]**.
