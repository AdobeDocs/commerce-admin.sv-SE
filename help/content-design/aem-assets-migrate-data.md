---
title: Migrera mediefiler till AEM
description: Migrera mediefilerna från Adobe Commerce eller en extern källa till AEM Assets DAM.
feature: CMS, Media, Integration
source-git-commit: 094c585b335e5751a1387989d5ba33332c351c57
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# Migrera mediefiler till AEM Assets DAM

Både Adobe Commerce och Adobe Experience Manager (AEM) har inbyggda funktioner för att effektivisera migreringen av mediefiler från Commerce till AEM Assets digitala resurshanteringssystem (DAM). Du kan också migrera mediefiler från andra källor.

## Förutsättningar

| Kategori | Krav |
|----------|-------------|
| **Systemkrav** | <ul><li>AEM as a Cloud Service-miljö etablerad med AEM Assets</li><li>Tillräcklig lagringskapacitet</li><li>Nätverksbandbredd för stora filöverföringar</li></ul> |
| **Nödvändig åtkomst och behörigheter** | <ul><li>Administratörsåtkomst till AEM Assets as a Cloud Service</li><li>Tillgång till källsystemet där mediefiler lagras (Adobe Commerce eller externt system)</li><li>Lämpliga behörigheter för att få åtkomst till molnlagringstjänster</li></ul> |
| **Konto för molnlagring** | <ul><li>AWS S3 eller Azure Blob Storage-konto</li><li>Privat behållare/bucket-konfiguration</li><li>Autentiseringsuppgifter</li></ul> |
| **Källinnehåll** | <ul><li>Organiserade mediefiler redo för migrering</li><li>Bild- och videofiler i <a href="https://experienceleague.adobe.com/sv/docs/experience-manager-cloud-service/content/assets/file-format-support#image-formats">format som stöds av AEM Assets</a>.</li><li>Rena, deduplicerade tillgångar</li></li> |
| **Förberedelse av metadata** | <ul><li><a href="https://experienceleague.adobe.com/sv/docs/commerce-admin/content-design/aem-asset-management/getting-started/aem-assets-configure-aem">AEM Assets metadataprofil har konfigurerats för Commerce-resurser</a></li><li>Mappade metadatavärden för varje resurs</li><li>CSV-filredigerare (t.ex. Microsoft Excel)</li></ul> |

## Bästa praxis för migrering

1. Kuratera resurser före migrering genom att ta bort oanvänt och duplicerat innehåll.
1. Ordna materialet logiskt efter storlek, format eller skiftläge.
1. Överväg att dela upp stora migreringar i mindre grupper.
1. Schemalägg resurskrävande import under tider med låg belastning.
1. Validera metadatamappning före fullständig import.

## Arbetsflöde för migrering

Följ migreringsarbetsflödet för att exportera mediefiler från Adobe Commerce eller ett annat externt system och importera dem till AEM Assets DAM.

### Steg 1: Exportera innehåll från den befintliga datakällan

För Adobe Commerce-handlare är modulen Fjärrlagring ett smidigt sätt att exportera mediefiler från Commerce och importera dem till AEM Assets. Med den här modulen kan du lagra och hantera mediefiler på fjärrlagringstjänster som AWS S3, vilket gör migreringsprocessen mer effektiv. Mer information om hur du konfigurerar fjärrlagring för din Commerce-instans finns i [Konfigurera fjärrlagring](https://experienceleague.adobe.com/sv/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage-aws-s3) i *Konfigurationshandboken för Commerce*.

Om du har mediefiler lagrade utanför Adobe Commerce kan du överföra dem direkt till någon av de [datakällor](https://experienceleague.adobe.com/sv/docs/experience-manager-cloud-service/content/assets/assets-view/bulk-import-assets-view#prerequisites) som stöds av AEM as a Cloud Service.

### Steg 2: Skapa en CSV-fil för metadatamappning

Skapa en metadatamappningsfil i CSV-format och överför den till källmappen som innehåller dina mediefiler. Den här filen mappar viktiga metadata till varje resurs till:

- Ordna och kategorisera resurser i DAM för enkel identifiering
- Aktivera korrekt synkronisering mellan Adobe Commerce och AEM Assets
- Underhåll relationer mellan resurser och produkter efter migrering

Ange värden för metadatafälten som ingår i [AEM Assets-metadataprofilen för Commerce-resurser](aem-assets-configure-aem.md) för varje mediefil som du vill migrera enligt följande tabell.

| Metadata | Beskrivning | Värde |
|-------|-------------|--------|
| assetPath (på engelska) | Den fullständiga sökvägen där resursen ska lagras i AEM Assets-databasen.<br><br>Använd sökvägen för att skapa undermappar för att organisera Commerce-resurser, till exempel `content/dam/commerce/<brand>/<type>`. | `/content/dam/commerce/<sub-folder>/..<filename>` |
| dc:titel | Visningsrubriken för resursen i AEM Assets | Strängvärde (till exempel `Sample 1`) |
| dam:status | Godkännandestatus för resursen i AEM Assets | `approved` |
| handel:positioner | Tillgångens position/ordning i produktgallerier | Numeriskt värde (t.ex. &quot;1&quot;) |
| handel:isCommerce | Flagga som anger om tillgången används i handeln | `Yes` |
| handel:skus | SKU:er för den här resursen | Strängvärde (till exempel `sample1`) |
| handel:roller | Roller eller typer av bilder för resursen (till exempel `thumbnail`, `main image`, `swatch`) | Flera värden avgränsade med semikolon (t.ex.&quot;miniatyrbild; bild; färgrutebild; liten_bild&quot;) |

+++CSV-kod

Använd det här exemplet på CSV-kod för att skapa filen i en kodredigerare eller ett kalkylbladsprogram som Microsoft Excel.

```csv
assetPath,dc:title{{String}},dam:status{{String}},commerce:positions{{String: multi}},commerce:isCommerce{{String}},commerce:skus{{String: multi}},commerce:roles{{String: multi}}
/content/dam/commerce/sample1.jpg,Sample 1,approved,1,Yes,sample1,thumbnail; image; swatch_image; small_image
/content/dam/commerce/sample2.jpg,Sample 2,approved,1,Yes,sample2,thumbnail; image; swatch_image; small_image
/content/dam/commerce/sample3.jpg,Sample 3,approved,1,Yes,sample3,thumbnail; image; swatch_image; small_image
```

+++

### Steg 3: Importera Assets satsvis till AEM Assets

När du har skapat metadatamappningsfilen kan du använda verktyget för massimport i AEM Assets för att importera dina resurser.

Här följer en översikt på hög nivå över hur du använder verktyget.

1. [Logga in på din AEM Assets as a Cloud Service författarmiljö](https://experienceleague.adobe.com/sv/docs/experience-manager-cloud-service/content/onboarding/journey/aem-users#login-aem).

1. I Experience Manager-verktygsvyn väljer du **[!UICONTROL Assets]** > **[!UICONTROL Bulk Import]**.

   ![AEM Assets-redigering](./assets/aem-assets-bulk-import-selection.png){width="600" zoomable="yes"}

1. Välj **[!UICONTROL Create]** i konfigurationerna för massimport för att öppna konfigurationsformuläret.

   ![AEM Assets-redigering](./assets/aem-assets-bulk-import-configuration.png){width="600" zoomable="yes"}

1. Konfigurera och spara konfigurationen.

   Du behöver:

   - Autentiseringsuppgifter för din datakälla
   - Målmappen i AEM Assets där importerade filer ska lagras
   - Information om MIME-typer, filstorlek och andra parametrar för att anpassa importkonfigurationen (valfritt)
   - Sökvägen till CSV-filen för metadatamappning som du laddade upp till molnlagringsinstansen.

   Mer information finns i [Konfigurera verktyget Massimport](https://experienceleague.adobe.com/sv/docs/experience-manager-cloud-service/content/assets/manage/add-assets#configure-bulk-ingestor-tool) i *AEM Assets as a Cloud Service-användarhandboken*.

1. När du har sparat konfigurationen använder du verktygen för massimport för att testa och köra importåtgärden.

>[!MORELIKETHIS]
>
>[Videodemo om verktyget Importera satsvis](https://experienceleague.adobe.com/sv/docs/experience-manager-cloud-service/content/assets/manage/add-assets#asset-bulk-ingestor)
>[Tips, bästa praxis och begränsningar](https://experienceleague.adobe.com/sv/docs/experience-manager-cloud-service/content/assets/manage/add-assets#tips-limitations)
>[Överför eller importera resurser med API:er ](https://experienceleague.adobe.com/sv/docs/experience-manager-cloud-service/content/assets/admin/developer-reference-material-apis#asset-upload)

