---
title: Installera AEM Assets Package för Commerce
description: Lägg till de metadata som krävs för att aktivera AEM Assets Integration för Commerce för att synkronisera resurser mellan Adobe Commerce- och Experience Manager Assets-projekt.
feature: CMS, Media, Integration
exl-id: deb7c12c-5951-4491-a2bc-542e993f1f84
source-git-commit: 3522c3d3d772be5278206c10d8e699c2c4cc31af
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 0%

---

# Installera AEM Assets-paketet

Adobe tillhandahåller en projektmall, `commerce-assets`, för att lägga till Commerce namnområde och metadataresurser i Experience Manager Assets as a Cloud Service-miljökonfigurationen. Distribuera den här mallen i din miljö som ett Maven-paket. Konfigurera sedan Commerce-metadata i AEM Assets redigeringsmiljö för att slutföra installationen.

Mallen lägger till följande resurser i AEM Assets redigeringsmiljö.

- Ett [anpassat namnområde](https://github.com/ankumalh/assets-commerce/blob/main/ui.config/jcr_root/apps/commerce/config/org.apache.sling.jcr.repoinit.RepositoryInitializer~commerce-namespaces.cfg.json), `Commerce` som identifierar Commerce-relaterade egenskaper.

- En anpassad metadatatyp `commerce:isCommerce` med etiketten `Eligible for Commerce` som taggar Commerce-resurser som är associerade med ett Adobe Commerce-projekt.

- En anpassad metadatatyp `commerce:productmetadata` och en motsvarande UI-komponent som lägger till en *[!UICONTROL Product Data]*-egenskap. Produktdata innehåller metadataegenskaper för att associera en Commerce-resurs med produkt-SKU:er och för att ange bild `role` och `position`-attribut för resursen.

  ![Användargränssnittskontroll för anpassade produktdata](./assets/aem-commerce-sku-metadata-fields-from-template.png){width="600" zoomable="yes"}

- Ett metadatamatchemaformulär med en Commerce-flik som innehåller fälten `Does it exist in Adobe Commerce?` och `Product Data` för taggning av Commerce-resurser. Formuläret innehåller även alternativ för att visa eller dölja fälten `roles` och `order` (position) från AEM Assets-gränssnittet.

  ![Commerce-flik för AEM Assets metadatamatchformulär](./assets/assets-configure-metadata-schema-form-editor.png){width="600" zoomable="yes"}

- Ett [exempel på taggad och godkänd Commerce-resurs](https://github.com/ankumalh/assets-commerce/blob/main/ui.content/src/main/content/jcr_root/content/dam/wknd/en/activities/hiking/equipment_6.jpg/.content.xml) `equipment_6.jpg` som har stöd för inledande resurssynkronisering. Endast godkända Commerce-resurser kan synkroniseras från AEM Assets till Adobe Commerce.

>[!NOTE]
>Mer information om projektmallen `commerce-assets` för AEM finns i [Viktigt](https://github.com/ankumalh/assets-commerce).

Du behöver följande resurser och behörigheter för att kunna använda det här AEM-projektet för att uppdatera miljökonfigurationen:

- [Åtkomst till AEM Assets Cloud Manager program och miljöer](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/cloud-manager#access-sysadmin-bo) med rollerna Program och Distributionshanteraren.

- En [lokal AEM-utvecklingsmiljö](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview) som är bekant med AEM lokala utvecklingsprocess.

- Förstå [AEM projektstruktur](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) och hur du distribuerar anpassade innehållspaket med Cloud Manager.

## Installera paketet `commerce-assets`

1. Från Cloud Manager kan du vid behov skapa produktions- och stagingmiljöer för ditt AEM Assets-projekt.

1. Konfigurera vid behov en distributionspipeline.

1. Hämta standardkoden från GitHub från [Commerce-Assets AEM-projektet](https://github.com/ankumalh/assets-commerce).

1. Från din [lokala AEM-utvecklingsmiljö](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview) installerar du den anpassade koden i din AEM Assets-miljökonfiguration som ett Maven-paket, eller genom att manuellt kopiera koden till den befintliga projektkonfigurationen.

1. Genomför ändringarna och skicka din lokala utvecklingsgren till Cloud Manager Git-databasen.

1. [Distribuera din kod från Cloud Manager för att uppdatera AEM-miljön](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deploying-code-with-cloud-manager).

## Konfigurera en metadataprofil

I AEM Assets-redigeringsmiljö anger du standardvärden för Commerce-objektmetadata genom att skapa en metadataprofil. Använd sedan den nya profilen i AEM Resursmappar för att använda dessa standardvärden automatiskt. Den här konfigurationen effektiviserar tillgångsbearbetning genom att minska antalet manuella steg.

1. Gå till arbetsytan för innehållsadministration för AEM Assets på Adobe Experience Manager-arbetsytan genom att klicka på ikonen Adobe Experience Manager.

   ![AEM Assets-redigering](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}

1. Öppna administratörsverktygen genom att välja hammikonen.

   ![AEM Author Admin hanterar metadataprofiler](./assets/aem-manage-metadata-profiles.png){width="600" zoomable="yes"}

1. Öppna profilkonfigurationssidan genom att klicka på **[!UICONTROL Metadata Profiles]**.

1. **[!UICONTROL Create]** en metadataprofil för Commerce-integreringen.

   ![AEM Author Admin lägger till metadataprofiler ](./assets/aem-create-metadata-profile.png){width="600" zoomable="yes"}

1. Lägg till en flik för Commerce-metadata.

   1. Klicka på **[!UICONTROL Settings]** till vänster.

   1. Klicka på **[!UICONTROL +]** i flikavsnittet och ange sedan **[!UICONTROL Tab Name]**, `Commerce`.

1. Lägg till fältet `Does it exist in Commerce?` i formuläret och ställ in standardvärdet på `yes`.

   ![AEM Author Admin lägger till metadatafält i profilen](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

1. Spara uppdateringen.

1. Använd metadataprofilen `Commerce integration` i den mapp där Commerce-resurser lagras.

   1. På sidan [!UICONTROL  Metadata Profiles] väljer du Commerce integreringsprofil.

   1. Välj **[!UICONTROL Apply Metadata Profiles to Folders]** på åtgärdsmenyn.

   1. Markera den mapp som innehåller Commerce-resurser.

      Skapa en Commerce-mapp om den inte finns.

   1. Klicka på **[!UICONTROL Apply]**.

>[!TIP]
>
>Du kan synkronisera Commerce-resurser automatiskt när de överförs till AEM Assets-miljön genom att uppdatera metadataprofilen och ange standardvärdet `Approved` för fältet _[!UICONTROL Review Status]_. Egenskapstypen för fältet `Review Status` är `./jcr:content/metadata/dam:status`.

## Nästa steg

[Installera Adobe Commerce-paket](aem-assets-configure-commerce.md)
