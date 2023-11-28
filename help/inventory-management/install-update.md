---
title: "Installera, uppdatera och ta bort [!DNL Inventory Management]"
description: Lär dig hantera [!DNL Inventory Management] metapackage.
exl-id: d088ff35-c0e1-41c8-89fb-78180eaefbf7
level: Experienced
feature: Inventory, Install
source-git-commit: d6c81da4b4e0674d6699e9781921ccb2160b9983
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# Installera, uppdatera och ta bort [!DNL Inventory Management]

[!DNL Inventory Management] moduler innehåller alla lagerfunktioner och alternativ för handlare med en och flera källor för att hantera produktkvantiteter och lager för försäljningskanaler. Dessa funktioner finns i version 2.4.x av Adobe Commerce och Magento Open Source.

Dessa funktioner och tillägg utvecklades som en del av [Lagerprojekt](https://github.com/magento/inventory) genom Magento Open Source Community Engineering-programmet.

[!DNL Inventory Management] installeras i version 2.3.x och 2.4.x av Adobe Commerce och Magento Open Source, med alla funktioner aktiverade som standard. Inga ytterligare steg krävs för att aktivera dessa lagerfunktioner. Uppgraderingar från v2.1.x eller 2.2.x kan kräva ytterligare steg. Se [Uppgradera Inventory management](#upgrade-inventory-management).

Installation enligt [Snabbstart av lokal installation](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html){target="_blank"} rekommenderas. Installera med ett metapaket för att få alla [!DNL Inventory Management] moduler.

Följande rad i `composer.json` installationer av metapackage [!DNL Inventory Management]:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

För en lista med [!DNL Inventory Management] metapackage-versioner, se [versionsinformation](release-notes.md).

The [!DNL Inventory Management] installationsprocessen lägger till alla moduler i `<Magento_installation_directory>/app/etc/config.php` -fil. A `1` anger att motsvarande modul är aktiverad. Följande lista med moduler ska läggas till:

```php
        'Magento_Inventory' => 1,
        'Magento_InventoryAdminUi' => 1,
        'Magento_InventoryAdvancedCheckout' => 1,
        'Magento_InventoryApi' => 1,
        'Magento_InventoryBundleProduct' => 1,
        'Magento_InventoryBundleProductAdminUi' => 1,
        'Magento_InventoryCatalog' => 1,
        'Magento_InventorySales' => 1,
        'Magento_InventoryCatalogAdminUi' => 1,
        'Magento_InventoryCatalogApi' => 1,
        'Magento_InventoryCatalogSearch' => 1,
        'Magento_InventoryConfigurableProduct' => 1,
        'Magento_InventoryConfigurableProductAdminUi' => 1,
        'Magento_InventoryConfigurableProductIndexer' => 1,
        'Magento_InventoryConfiguration' => 1,
        'Magento_InventoryConfigurationApi' => 1,
        'Magento_InventoryDistanceBasedSourceSelection' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionAdminUi' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionApi' => 1,
        'Magento_InventoryElasticsearch' => 1,
        'Magento_InventoryExportStockApi' => 1,
        'Magento_InventoryIndexer' => 1,
        'Magento_InventorySalesApi' => 1,
        'Magento_InventoryGroupedProduct' => 1,
        'Magento_InventoryGroupedProductAdminUi' => 1,
        'Magento_InventoryGroupedProductIndexer' => 1,
        'Magento_InventoryImportExport' => 1,
        'Magento_InventoryCache' => 1,
        'Magento_InventoryLowQuantityNotification' => 1,
        'Magento_InventoryLowQuantityNotificationApi' => 1,
        'Magento_InventoryMultiDimensionalIndexerApi' => 1,
        'Magento_InventoryProductAlert' => 1,
        'Magento_InventoryRequisitionList' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryExportStock' => 1,
        'Magento_InventorySalesAdminUi' => 1,
        'Magento_InventorySalesFrontendUi' => 1,
        'Magento_InventorySetupFixtureGenerator' => 1,
        'Magento_InventoryShipping' => 1,
        'Magento_InventorySourceDeductionApi' => 1,
        'Magento_InventorySourceSelection' => 1,
        'Magento_InventorySourceSelectionApi' => 1,
        'Magento_InventoryLowQuantityNotificationAdminUi' => 1,
        'Magento_InventoryShippingAdminUi' => 1,
        'Magento_InventoryGraphQl' => 1,
```

## Aktivera [!DNL Inventory Management] funktioner

Vid installation, uppgradering eller uppdatering av _[!UICONTROL Manage Stock]_som standard är alternativet i Admin aktiverat. Det här alternativet aktiverar lagerspårning och lagerhantering, men påverkar inte modulens status. Mer information om hur du inaktiverar moduler finns i nästa avsnitt.

Mer information om konfigurationer finns i [Konfigurera Inventory management](configuration.md).

## Inaktivera Inventory management

>[!IMPORTANT]
>
>Använda standardinställningen [!DNL Inventory Management] rekommenderas. Alternativet [!DNL CatalogInventory] -modul, som används för system med inaktiverat [!DNL Inventory Management] är nu föråldrat. Inaktiverar [!DNL Inventory Management] moduler kan orsaka ett instabilt system och leda till olika problem.

Du kanske vill inaktivera [!DNL Inventory Management] moduler till:

* Snabba upp uppgraderingsprocessen för handlare som migrerar från 2.0.x, 2.1.x, 2.2.x eller 2.3.x till 2.4.x.
* Använd anpassade eller externa lagerhanterings- och orderhanteringssystemmoduler.

Se [Aktivera eller inaktivera moduler](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html) sidan i _Installationshandbok_ om du vill ha information om hur du inaktiverar de tillämpliga modulerna.

När det är klart visas en lista med moduler och värden i `<Magento_installation_directory>/app/etc/config.php`, som börjar med:

```php
   'Magento_Inventory' => 0,
   'Magento_InventoryAdminUi' => 0,
   'Magento_InventoryAdvancedCheckout' => 0,
   ...
```

>[!IMPORTANT]
>
>Om du har OMS Connector-modulerna installerade kontrollerar du att du inte inaktiverar `Magento_InventoryMessageBus` -modul, som är en kopplingsmodul. Du måste använda Connector med OMS.

## Ta bort Inventory management

>[!IMPORTANT]
>
>Använda standardinställningen [!DNL Inventory Management] rekommenderas. Alternativet [!DNL CatalogInventory] modul, som används för system som tagits bort [!DNL Inventory Management] är nu föråldrat. Tar bort [!DNL Inventory Management] moduler kan orsaka ett instabilt system och leda till olika problem.

Om du inte använder [!DNL Inventory Management] kan du ta bort (avinstallera) dessa moduler. Om du vill ta bort alla moduler genom kompositfilen lägger du till följande i `composer.json`:

```
"replace": {
        "magento/module-inventory": "*",
        "magento/module-inventory-admin-ui": "*",
        "magento/module-inventory-advanced-checkout": "*",
        "magento/module-inventory-api": "*",
        "magento/module-inventory-bundle-product": "*",
        "magento/module-inventory-bundle-product-admin-ui": "*",
        "magento/module-inventory-cache": "*",
        "magento/module-inventory-catalog": "*",
        "magento/module-inventory-catalog-admin-ui": "*",
        "magento/module-inventory-catalog-api": "*",
        "magento/module-inventory-catalog-search": "*",
        "magento/module-inventory-configurable-product": "*",
        "magento/module-inventory-configurable-product-admin-ui": "*",
        "magento/module-inventory-configurable-product-indexer": "*",
        "magento/module-inventory-configuration": "*",
        "magento/module-inventory-configuration-api": "*",
        "magento/module-inventory-distance-based-source-selection": "*",
        "magento/module-inventory-distance-based-source-selection-admin-ui": "*",
        "magento/module-inventory-distance-based-source-selection-api": "*",
        "magento/module-inventory-export-stock": "*",
        "magento/module-inventory-export-stock-api": "*",
        "magento/module-inventory-elasticsearch": "*",
        "magento/module-inventory-graph-ql": "*",
        "magento/module-inventory-grouped-product": "*",
        "magento/module-inventory-grouped-product-admin-ui": "*",
        "magento/module-inventory-grouped-product-indexer": "*",
        "magento/module-inventory-import-export": "*",
        "magento/module-inventory-indexer": "*",
        "magento/module-inventory-low-quantity-notification": "*",
        "magento/module-inventory-low-quantity-notification-admin-ui": "*",
        "magento/module-inventory-low-quantity-notification-api": "*",
        "magento/module-inventory-multi-dimensional-indexer-api": "*",
        "magento/module-inventory-product-alert": "*",
        "magento/module-inventory-requisition-list": "*",
        "magento/module-inventory-reservations": "*",
        "magento/module-inventory-reservations-api": "*",
        "magento/module-inventory-reservation-cli": "*",
        "magento/module-inventory-sales": "*",
        "magento/module-inventory-sales-admin-ui": "*",
        "magento/module-inventory-sales-api": "*",
        "magento/module-inventory-sales-frontend-ui": "*",
        "magento/module-inventory-setup-fixture-generator": "*",
        "magento/module-inventory-shipping": "*",
        "magento/module-inventory-shipping-admin-ui": "*",
        "magento/module-inventory-source-deduction-api": "*",
        "magento/module-inventory-source-selection": "*",
        "magento/module-inventory-source-selection-api": "*",
        "magento/module-inventory-visual-merchandiser": "*",
        "magento/module-inventory-swatches-frontend-ui": "*",
        "magento/module-inventory-quote-graph-ql": "*",
        "magento/module-inventory-in-store-pickup": "*",
        "magento/module-inventory-in-store-pickup-sales": "*",
        "magento/module-inventory-in-store-pickup-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-sales-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-api": "*",
        "magento/module-inventory-in-store-pickup-sales-api": "*",
        "magento/module-inventory-in-store-pickup-frontend": "*",
        "magento/module-inventory-in-store-pickup-shipping": "*",
        "magento/module-inventory-in-store-pickup-graph-ql": "*",
        "magento/module-inventory-in-store-pickup-shipping-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-multishipping": "*",
        "magento/module-inventory-in-store-pickup-shipping-api": "*",
        "magento/module-inventory-in-store-pickup-quote": "*",
        "magento/module-inventory-in-store-pickup-webapi-extension": "*",
        "magento/module-inventory-in-store-pickup-quote-graph-ql": "*",
        "magento/module-inventory-configurable-product-frontend-ui": "*",
        "magento/module-inventory-catalog-search-configurable-product": "*",
        "magento/module-inventory-catalog-search-bundle-product": "*",
        "magento/module-inventory-catalog-frontend-ui": "*",
        "magento/module-inventory-bundle-import-export": "*",
        "magento/module-inventory-bundle-product-indexer": "*"
    }
```

När den här ändringen är klar kör du en dispositionsinstallation och tar automatiskt bort dessa Inventory management-moduler.

## Uppgradera Inventory management

### Föregående [!DNL Commerce] versioner

Vid uppgradering eller uppdatering av en befintlig installation av 2.1.x, 2.2.x eller 2.3.x till Adobe Commerce eller Magento Open Source 2.4.x, [!DNL Inventory Management] moduler är inaktiverade som standard. Den här standardinställningen är en försiktighetsåtgärd för att förhindra bakåtkompatibla uppgraderingar och för att ge bättre stöd för orderhantering (OMS).

>[!NOTE]
>
>Orderhantering stöder inte [!DNL Inventory Management]. Vid uppgradering, [!DNL Inventory Management] moduler inaktiveras för att tillåta OMS och [!DNL Commerce] 2.3.x för smidigt arbete.


Aktivera [!DNL Inventory Management] moduler:

1. Redigera `<Commerce_installation_directory>/app/etc/config.php` -fil.
1. Ändra alla lagermoduler från `0` till `1` för att aktivera.
1. Uppdatera databasen:

   ```bash
   bin/magento setup:upgrade
   ```

1. Rensa cachen:

   ```bash
   bin/magento cache:clean
   ```

Du bör använda [inkonsekvenser i bokningen, kommandon](cli.md) efter uppgradering. När du uppgraderar läggs alla dina produkter till i standardlagret. Om du har väntande order uppdaterar kommandona din försäljningsbara kvantitet och reservationer korrekt för försäljning och orderhantering.

### Föregående [!DNL Inventory Management] versioner

Vid uppgradering från tidigare versioner av [!DNL Inventory Management] till den senaste versionen, följ normala uppgraderingssteg för tillägg.

Den senaste versionen av ditt metapaket:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Mer information om uppgraderingar i Commerce finns i följande handböcker:

* [Handbok för Commerce Update](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/overview.html){target="_blank"}
* [Aktivera eller inaktivera moduler](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html){target="_blank"}
