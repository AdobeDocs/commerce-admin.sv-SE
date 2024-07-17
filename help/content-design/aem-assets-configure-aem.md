---
title: Konfigurera Experience Manager Assets
description: Lägg till de metadata som krävs för att aktivera AEM Assets Integration för Commerce för att synkronisera resurser mellan Adobe Commerce- och Experience Manager Assets-projekt.
feature: CMS, Media, Integration
source-git-commit: d91ba86b77ef91e849d1737628b575f2309376b8
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# Konfigurera Experience Manager Assets

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Om du vill hantera medieresurser för din butik med hjälp av AEM Assets-integreringen för Commerce måste du lägga till vissa metadata för att vara säker på att du enkelt kan söka efter och hantera Commerce-resurser. Dessa metadata underlättar också synkroniseringen av resurser mellan Adobe Commerce och Experience Manager Assets. När du har definierat metadatafälten mappas dessa fält automatiskt första gången en Commerce-resurs delas med Experience Manager Assets.

För integreringen konfigurerar du två typer av metadata:

- Med **[metadataprofilen](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-profiles)** kan du använda standardmetadata för resurser i en mapp. Alla resurser i mappen ärver standardmetadata som konfigurerats i profilen.

- **[Metadataschemat](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-schemas)** definierar layouten för egenskapssidan och den uppsättning fält som kan användas som metadataegenskaper för en AEM.

## Konfigurera metadata

För den första introduktionen lägger du till följande Commerce-metadata i både en AEM Assets-metadataprofil och ett metadataschema.

| Fälttyp | Etikett | Egenskap | Standardvärde |
|------ | ------- | ---------- | ------------- |
| Text | **Finns den i Adobe Commerce?** | `./jcr:content/metadata/commerce:isCommerce` | ja |
| Flervärdestext | **SKU:er** | `./jcr:content/metadata/commerce:skus` | ingen |
| Flervärdestext | **Positioner** | `./jcr:content/metadata/commerce:positions` | ingen |
| Flervärdestext | **Roller** | `./jcr:content/metadata/commerce:roles` | ingen |


### Lägga till Commerce-fält i en metadataprofil

1. Gå till arbetsytan för administrering av författarinnehåll för AEM Assets på arbetsytan i Adobe Experience Manager genom att klicka på ikonen Adobe Experience Manager.

   ![AEM Assets-redigering](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}

1. Öppna administratörsverktygen genom att välja hammikonen.

   ![AEM Författaradministratör hanterar metadataprofiler](./assets/aem-manage-metadata-profiles.png){width="600" zoomable="yes"}

1. Öppna profilkonfigurationssidan genom att klicka på **[!UICONTROL Metadata Profiles]**.

1. **[!UICONTROL Create]** en metadataprofil för Commerce-integreringen.

   ![AEM Författaradministratör lägger till metadataprofiler ](./assets/aem-create-metadata-profile.png){width="600" zoomable="yes"}

1. Lägg till en flik för Commerce-metadata.

   1. Klicka på **[!UICONTROL Settings]** till vänster.

   1. Klicka på **[!UICONTROL +]** i flikavsnittet och ange sedan **[!UICONTROL Tab Name]**, `Commerce`.

1. Lägg till [metadatafälten](#configure-metadata) i formuläret.

   ![AEM Författaradministratör lägger till metadatafält i profilen](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

1. Spara uppdateringen.

1. Använd metadataprofilen `Commerce integration` i den mapp där Commerce-resurser lagras.

   1. På sidan [!UICONTROL  Metadata Profiles] väljer du Commerce integreringsprofil.

   1. Välj **[!UICONTROL Apply Metadata Profiles to Folder(s)]** på åtgärdsmenyn.

   1. Markera den mapp som innehåller Commerce-resurser.

      Skapa en Commerce-mapp om den inte finns.

   1. Klicka på **[!UICONTROL Apply]**.

### Lägga till Commerce-fält i ett metadataschemaformulär

1. Öppna **[!UICONTROL Metadata Schemas]** ([!UICONTROL Manage metadata schema forms]) på AEM författarinnehållets administrationspanel för Assets.

   ![AEM för uppdatering av metadataram för författaradministratör](./assets/aem-assets-manage-metadata-schema.png){width="600" zoomable="yes"}

1. **[!UICONTROL Create]** ett metadataschema för Commerce.

   ![AEM för uppdatering av metadataram för författaradministratör](./assets/aem-assets-create-metadata-schema.png){width="600" zoomable="yes"}

1. Skapa fälten `Does Commerce exist?` och `Commerce mappings` på [!UICONTROL Metadata Schema Form] och mappa egenskaperna.

1. Klicka på **[!UICONTROL Save]**.


## Publish en mediefil

När du har konfigurerat AEM metadata och schemaprofil för Commerce-resurser skapar du den första Commerce-resursen som mappar Commerce metadatafälten.

1. Gå till [!UICONTROL Assets > Files] och markera mappen **Commerce** från Experience Manager.

1. Överför en bild för ett Commerce-projekt genom att dra filen till mappen eller genom att klicka på **[!UICONTROL Add Assets]**.

1. Kontrollera att metadatakonfigurationen **isCommerce** är inställd på `true` och att egenskapen `commerce:skus` är inställd på SKU för den Commerce-produkt som är associerad med bilden.

1. Godkänn resursen.


## Lägga till en resurs i Commerce-mappen

Skapa minst en resurs i AEM Assets Commerce-mappen som har Commerce-metadataattribut tilldelade.

Den här resursen krävs för att konfigurera synkronisering mellan din Commerce-instans och AEM Assets.

## Mappa metadata för resurser

Metadata mappas när en Commerce-resurs publiceras för första gången.  från Commerce för första gången. Medieresurser som har inbyggda eller anpassade fält mappas automatiskt till de angivna fälten första gången en resurs skickas till Experience Manager Assets.

Innan du kan börja mappa resurser ska du utföra följande uppgifter:

- [Installera och konfigurera AEM Assets Integration för Commerce](aem-assets-configure-commerce.md)
- [Aktivera resurssynkronisering för att överföra resurser mellan Adobe Commerce projektmiljö och AEM Assets projektmiljö](aem-assets-setup-synchronization.md)
