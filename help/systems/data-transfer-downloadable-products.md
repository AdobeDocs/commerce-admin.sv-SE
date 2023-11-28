---
title: Importera nedladdningsbara produkter
description: Granska ett exempel på hur du importerar produktdata för en nedladdningsbar produkt.
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# Importera nedladdningsbara produkter

Flödet för import av nedladdningsbara produkter är detsamma som för [Paketprodukter](data-transfer-bundle-products.md) eller [Konfigurerbara produkter](data-transfer-configurable-products.md). Skillnaden är att en nedladdningsbar produkt har [nedladdningsbara länkar](../catalog/product-create-downloadable.md) och [nedladdningsbara exempel](../catalog/product-create-downloadable.md) med bilderna.

Standardrotkatalogen för hämtningsbara länkar och exempel är `<Magento-root-folder>/pub/media/import`. Om fjärrlagringsmodulen är aktiverad är standardrotkatalogen för hämtningsbara länkar och exempel `<remote-storage-root-folder>/media/import` katalog.

CSV-filen har separata kolumner för `downloadable_links` och `downloadable_samples`.

- **Länkbilder som kan hämtas** — I följande exempel kan du hämta länkbilder (`red.jpg` och `black.jpg`) finns i `<Magento-root-folder>/pub/media/import/test` mapp. Om fjärrlagring är aktiverat finns dessa bilder i `<remote-storage-root-folder>/media/import/test` mapp.

  ![Exempeldata - nedladdningsbar produkt med nedladdningsbara länkar](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **Nedladdningsbara exempelbilder** — I följande exempel är den hämtningsbara exempelbilden (`white.jpg`) finns i `<Magento-root-folder>/pub/media/import/test` mapp. Om fjärrlagring är aktiverat finns den här bilden i `<remote-storage-root-folder>/media/import/test` mapp.

  ![Exempeldata - nedladdningsbar produkt med nedladdningsbara exempel](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

Mer information om att aktivera och hantera fjärrlagringsmodulen finns i [Konfigurera fjärrlagring](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) i _Konfigurationsguide_.
