---
title: Importera nedladdningsbara produkter
description: Granska ett exempel på hur du importerar produktdata för en nedladdningsbar produkt.
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---

# Importera nedladdningsbara produkter

Flödet för import av hämtningsbara produkter är detsamma som för [paketprodukter](data-transfer-bundle-products.md) eller [konfigurerbara produkter](data-transfer-configurable-products.md). Skillnaden är att en nedladdningsbar produkt har [hämtningsbara länkar](../catalog/product-create-downloadable.md) och [hämtningsbara exempel](../catalog/product-create-downloadable.md) med sina bilder.

Standardrotkatalogen för hämtningsbara länkar och exempel är `<Magento-root-folder>/pub/media/import`. Om fjärrlagringsmodulen är aktiverad är standardrotkatalogen för hämtningsbara länkar och exempel katalogen `<remote-storage-root-folder>/media/import`.

CSV-filen har separata kolumner för `downloadable_links` och `downloadable_samples`.

- **Hämtningsbara länkbilder** - I följande exempel finns hämtningsbara länkbilder (`red.jpg` och `black.jpg`) i mappen `<Magento-root-folder>/pub/media/import/test`. Om fjärrlagring är aktiverat finns dessa bilder i mappen `<remote-storage-root-folder>/media/import/test`.

  ![Exempeldata - hämtningsbar produkt med hämtningsbara länkar](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **Hämtningsbara exempelbilder** - I följande exempel finns den hämtningsbara exempelbilden (`white.jpg`) i mappen `<Magento-root-folder>/pub/media/import/test`. Om fjärrlagring är aktiverat finns bilden i mappen `<remote-storage-root-folder>/media/import/test`.

  ![Exempeldata - hämtningsbar produkt med hämtningsbara exempel](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

Mer information om hur du aktiverar och hanterar fjärrlagringsmodulen finns i [Konfigurera fjärrlagring](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html?lang=sv-SE) i _konfigurationsguiden_.
