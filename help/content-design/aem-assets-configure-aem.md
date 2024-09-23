---
title: Konfigurera Experience Manager Assets
description: Lägg till de metadata som krävs för att aktivera AEM Assets Integration för Commerce för att synkronisera resurser mellan Adobe Commerce- och Experience Manager Assets-projekt.
feature: CMS, Media, Integration
exl-id: deb7c12c-5951-4491-a2bc-542e993f1f84
source-git-commit: 8a150c79c2e15ce5bd2cb2037f94c94f90b7a1df
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 0%

---

# Konfigurera Experience Manager Assets

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Förbered AEM as a Cloud Service-miljön för att hantera Commerce-resurser genom att uppdatera systemkonfigurationen och konfigurera Assets-metadata för att identifiera och hantera Commerce-resurser.

Integreringen kräver att du lägger till ett anpassat `Commerce`-namnområde och ytterligare [profilmetadata](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-profiles) och [schemadata](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-schemas).

Adobe tillhandahåller en AEM projektmall för att lägga till namnutrymmet och metadataresurserna i AEM Assets as a Cloud Service miljökonfiguration. I mallen läggs följande till:

- Ett [anpassat namnområde](https://github.com/ankumalh/assets-commerce/blob/main/ui.config/jcr_root/apps/commerce/config/org.apache.sling.jcr.repoinit.RepositoryInitializer~commerce-namespaces.cfg.json), `Commerce` som identifierar Commerce-relaterade egenskaper.

- En anpassad metadatatyp `commerce:isCommerce` med etiketten `Does it exist in Commerce?` som taggar Commerce-resurser som är associerade med ett Adobe Commerce-projekt.

- En anpassad metadatatyp `commerce:productmetadata` och en motsvarande UI-komponent som lägger till en *[!UICONTROL Product Data]*-egenskap. Produktdata innehåller metadataegenskaper för att associera en Commerce-resurs med produkt-SKU:er och för att ange bild `role` och `position`-attribut för resursen.

  ![Användargränssnittskontroll för anpassade produktdata](./assets/aem-commerce-sku-metadata-fields-from-template.png){width="600" zoomable="yes"}

- Ett metadatamatchemaformulär med en Commerce-flik som innehåller fälten `Does it exist in Adobe Commerce?` och `Product Data` för taggning av Commerce-resurser. Formuläret innehåller även alternativ för att visa eller dölja fälten `roles` och `order` (position) från AEM Assets-gränssnittet.

  ![Commerce-flik för AEM Assets metadatamatchformulär](./assets/assets-configure-metadata-schema-form-editor.png){width="600" zoomable="yes"}

- Ett [exempel på taggad och godkänd Commerce-resurs](https://github.com/ankumalh/assets-commerce/blob/main/ui.content/src/main/content/jcr_root/content/dam/wknd/en/activities/hiking/equipment_6.jpg/.content.xml) `equipment_6.jpg` som har stöd för inledande resurssynkronisering. Endast godkända Commerce-resurser kan synkroniseras från AEM Assets till Adobe Commerce.

Mer information om AEM Commerce-Assets finns i [Viktigt](https://github.com/ankumalh/assets-commerce).

## Anpassa AEM Assets-miljökonfigurationen

>[!BEGINSHADEBOX]

**Förutsättningar**

- [Åtkomst till AEM Assets Cloud Manager program och miljöer](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/cloud-manager#access-sysadmin-bo) med rollerna Program och Distributionshanteraren.

- En [lokal AEM ](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview)-utvecklingsmiljö och bekanta dig med den AEM lokala utvecklingsprocessen.

- Förstå [AEM projektstruktur](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) och hur du distribuerar anpassade innehållspaket med Cloud Manager.

>[!ENDSHADEBOX]

### Distribuera Commerce-Assets AEM till AEM Assets redigeringsmiljö

1. Från Cloud Manager kan du vid behov skapa produktions- och stagingmiljöer för ditt AEM Assets-projekt.

1. Konfigurera vid behov en distributionspipeline.

1. Hämta standardkoden från GitHub från [Commerce-Assets-AEM](https://github.com/ankumalh/assets-commerce).

1. Installera den anpassade koden i din [lokala AEM utvecklingsmiljö](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview) i AEM Assets-miljökonfigurationen som ett Maven-paket, eller genom att manuellt kopiera koden till den befintliga projektkonfigurationen.

1. Verkställ ändringarna och överför din lokala utvecklingsgren till Cloud Manager Git-databasen.

1. [Distribuera din kod från Cloud Manager för att uppdatera AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deploying-code-with-cloud-manager).

## Konfigurera en metadataprofil

Ange standardvärden för metadata för Commerce-resurser genom att skapa en metadataprofil. När du väl har konfigurerat den här profilen kan du använda den för AEM Resursmappar så att standardvärdena används automatiskt. Den här valfria installationen hjälper till att effektivisera hanteringen av tillgångar genom att minska antalet manuella steg.

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

1. Lägg till fältet `Does it exist in Commerce?` i formuläret och ställ in standardvärdet på `yes`.

   ![AEM Författaradministratör lägger till metadatafält i profilen](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

1. Spara uppdateringen.

1. Använd metadataprofilen `Commerce integration` i den mapp där Commerce-resurser lagras.

   1. På sidan [!UICONTROL  Metadata Profiles] väljer du Commerce integreringsprofil.

   1. Välj **[!UICONTROL Apply Metadata Profiles to Folder(s)]** på åtgärdsmenyn.

   1. Markera den mapp som innehåller Commerce-resurser.

      Skapa en Commerce-mapp om den inte finns.

   1. Klicka på **[!UICONTROL Apply]**.

>[!TIP]
>
>Du kan synkronisera Commerce-resurser automatiskt när de överförs till AEM Assets-miljön genom att uppdatera metadataprofilen och ange standardvärdet `Approved` för fältet _[!UICONTROL Review Status]_. Egenskapstypen för fältet `Review Status` är `./jcr:content/metadata/dam:status`.


## Nästa steg

Konfigurera Adobe Commerce när du har uppdaterat AEM:

1. [Installera och konfigurera AEM Assets Integration för Commerce](aem-assets-configure-commerce.md)
2. [Aktivera resurssynkronisering för att överföra resurser mellan Adobe Commerce projektmiljö och AEM Assets projektmiljö](aem-assets-setup-synchronization.md)
