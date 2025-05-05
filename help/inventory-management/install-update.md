---
title: Installera, uppdatera och ta bort [!DNL Inventory Management]
description: Lär dig hur du hanterar  [!DNL Inventory Management] metapaketet.
exl-id: d088ff35-c0e1-41c8-89fb-78180eaefbf7
level: Experienced
feature: Inventory, Install
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---

# Installera, uppdatera och ta bort [!DNL Inventory Management]

[!DNL Inventory Management]-moduler innehåller alla lagerfunktioner och alternativ för handlare med en och flera källor för att hantera produktkvantiteter och lager för försäljningskanaler. Dessa funktioner finns i version 2.4.x av Adobe Commerce och Magento Open Source.

De här funktionerna och tilläggen utvecklades som en del av [lagerprojektet](https://github.com/magento/inventory) via Magento Open Source Community Engineering Program.

[!DNL Inventory Management] installeras i version 2.3.x och 2.4.x av Adobe Commerce och Magento Open Source, med alla funktioner aktiverade som standard. Inga ytterligare steg krävs för att aktivera dessa lagerfunktioner. Uppgraderingar från v2.1.x eller 2.2.x kan kräva ytterligare steg. Se [Uppgradera Inventory management](#upgrade-inventory-management).

Installation enligt [Snabbstart av lokal installation](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html?lang=sv-SE){target="_blank"} rekommenderas. Installera med ett metapaket om du vill ta emot alla [!DNL Inventory Management] moduler.

Följande rad i `composer.json`-metapaketet installerar [!DNL Inventory Management]:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

En lista över [!DNL Inventory Management] metapaketversioner finns i [versionsinformationen](release-notes.md).

Installationsprocessen [!DNL Inventory Management] lägger till alla moduler i filen `<Magento_installation_directory>/app/etc/config.php`. Ett `1`-värde anger att motsvarande modul är aktiverad. Följande lista med moduler ska läggas till:

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

## Aktivera [!DNL Inventory Management]-funktioner

Vid installation, uppgradering eller uppdatering är alternativet _[!UICONTROL Manage Stock]_&#x200B;i Admin aktiverat som standard. Det här alternativet aktiverar lagerspårning och lagerhantering, men påverkar inte modulens status. Mer information om hur du inaktiverar moduler finns i nästa avsnitt.

Mer information om konfigurationer finns i [Konfigurera Inventory management](configuration.md).

## Inaktivera Inventory management

>[!IMPORTANT]
>
>Vi rekommenderar att du använder [!DNL Inventory Management]-standardmoduler. Den alternativa modulen [!DNL CatalogInventory], som används för system med inaktiverade [!DNL Inventory Management]-moduler, är nu föråldrad. Inaktivering av modulerna [!DNL Inventory Management] kan orsaka ett instabilt system och leda till olika problem.

Du kan inaktivera [!DNL Inventory Management] moduler till:

* Snabba upp uppgraderingsprocessen för handlare som migrerar från 2.0.x, 2.1.x, 2.2.x eller 2.3.x till 2.4.x.
* Använd anpassade eller externa lagerhanterings- och orderhanteringssystemmoduler.

Gå till sidan [Aktivera eller inaktivera moduler](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=sv-SE) i _installationshandboken_ för mer information om hur du inaktiverar de tillämpliga modulerna.

När det är klart visas en lista med moduler och värden i `<Magento_installation_directory>/app/etc/config.php`, med början:

```php
   'Magento_Inventory' => 0,
   'Magento_InventoryAdminUi' => 0,
   'Magento_InventoryAdvancedCheckout' => 0,
   ...
```

>[!IMPORTANT]
>
>Om du har OMS Connector-modulerna installerade kontrollerar du att du inte inaktiverar modulen `Magento_InventoryMessageBus`, som är en anslutningsmodul. Du måste använda Connector med OMS.

## Ta bort Inventory management

>[!IMPORTANT]
>
>Vi rekommenderar att du använder [!DNL Inventory Management]-standardmoduler. Den alternativa modulen [!DNL CatalogInventory], som används för system med borttagna [!DNL Inventory Management]-moduler, är nu föråldrad. Om du tar bort modulerna [!DNL Inventory Management] kan det orsaka ett instabilt system och leda till olika problem.

Om du väljer att inte använda funktionen [!DNL Inventory Management] kan du ta bort (avinstallera) de här modulerna. Om du vill ta bort alla moduler genom kompositfilen lägger du till följande i `composer.json`:

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

### Tidigare [!DNL Commerce] versioner

När du uppgraderar eller uppdaterar en befintlig 2.1.x-, 2.2.x- eller 2.3.x-installation till Adobe Commerce eller Magento Open Source 2.4.x är [!DNL Inventory Management]-moduler inaktiverade som standard. Den här standardinställningen är en försiktighetsåtgärd för att förhindra bakåtkompatibla uppgraderingar och för att ge bättre stöd för Order Management (OMS).

>[!NOTE]
>
>Order Management stöder inte [!DNL Inventory Management]. Vid uppgradering inaktiveras [!DNL Inventory Management] moduler så att OMS och [!DNL Commerce] 2.3.x kan fungera utan problem.


Så här aktiverar du [!DNL Inventory Management] moduler:

1. Redigera filen `<Commerce_installation_directory>/app/etc/config.php`.
1. Aktivera genom att ändra alla lagermoduler från `0` till `1`.
1. Uppdatera databasen:

   ```bash
   bin/magento setup:upgrade
   ```

1. Rensa cachen:

   ```bash
   bin/magento cache:clean
   ```

Vi rekommenderar att du använder kommandona [inkonsekvenser i reservationen](cli.md) efter uppgraderingen. När du uppgraderar läggs alla dina produkter till i standardlagret. Om du har väntande order uppdaterar kommandona din försäljningsbara kvantitet och reservationer korrekt för försäljning och orderhantering.

### Tidigare [!DNL Inventory Management] versioner

När du uppgraderar från tidigare versioner av [!DNL Inventory Management] till den senaste versionen följer du normala uppgraderingssteg för tillägg.

Den senaste versionen av ditt metapaket:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Mer information om Commerce uppgraderingar finns i följande handböcker:

* [Commerce Update Guide](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/overview.html?lang=sv-SE){target="_blank"}
* [Aktivera eller inaktivera moduler](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=sv-SE){target="_blank"}
