---
title: Import av produktbilder
description: Lär dig hur du importerar produktbilder med sökvägen och filnamnet för varje bild.
exl-id: 991550e6-9ce2-4472-becb-3492bd4c9582
feature: Products, Data Import/Export, Media
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# Import av produktbilder

Flera produktbilder av varje typ kan importeras till Adobe Commerce och Magento Open Source och kopplas till en viss produkt. Sökvägen och filnamnet för varje produktavbildning anges i CSV-filen och bildfilerna som ska importeras överförs till motsvarande sökväg på Commerce-servern eller den externa servern.

Commerce skapar en egen katalogstruktur för produktbilder som är ordnade i bokstavsordning. När du exporterar produktdata med befintliga bilder till en CSV-fil kan du se den alfabetiska sökvägen före filnamnet för varje bild. När du importerar nya bilder behöver du dock inte ange en sökväg eftersom katalogstrukturen hanteras automatiskt i Commerce. Men se till att ange den relativa sökvägen till importkatalogen före filnamnet för varje bild som ska importeras.

Om du vill överföra bilder måste du ha inloggningsuppgifter och korrekta behörigheter för att få tillgång till Commerce-mappen på servern. Med rätt autentiseringsuppgifter kan du använda valfritt SFTP-verktyg för att överföra filerna från din stationära dator till servern.

Innan du försöker importera många bilder ska du granska stegen i den importmetod som du vill använda och köra igenom processen med några produkter. När du har förstått hur det fungerar kommer du att känna dig säker på att importera stora mängder bilder.

>[!IMPORTANT]
>
>Vi rekommenderar att du använder ett program som har stöd för UTF-8-kodning för att redigera CSV-filer, till exempel Anteckningar++. Microsoft® Excel infogar ytterligare tecken i kolumnrubriken i CSV-filen, vilket kan förhindra att data importeras tillbaka till Commerce.

## Metod 1: Importera bilder från den lokala servern

1. På Commerce-servern överför du bildfilerna till `var/import/images` mapp eller undermapp, till exempel `var/import/images/product_images`. Det här är standardrotmappen för import av produktbilder.

   ```terminal
   <Magento root folder>/var/import/images
   ```

   >[!NOTE]
   >
   Från Adobe Commerce och Magento Open Source `2.3.2` release, den sökväg som anges i **[!UICONTROL Images File Directory]** sammanfogningar för import till bildens baskatalog - `<Magento-root-folder>/var/import/images`. I tidigare versioner av Adobe Commerce och Magento Open Source kan du använda en annan mapp på Commerce-servern, förutsatt att sökvägen till mappen anges under importen.

1. I CSV-data anger du namnet på varje bildfil som ska importeras på rätt rad av `sku`och i rätt kolumn enligt bildtyp (`base_image`, `small_image`, `thumbnail_image`, eller `additional_images`).

   >[!NOTE]
   >
   För bilder i standardimportmappen (`var/import/images`) ska du inte ta med sökvägen före filnamnet i CSV-data.

   CSV-filen får bara innehålla `sku` -kolumn och relaterade bildkolumner.

   ![Exempel - Import av CSV-bilddata](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. Följ instruktionerna för att [import](data-import.md) data.

1. Ange den relativa sökvägen efter när du har valt vilken fil som ska importeras **[!UICONTROL Images File Directory]**.

   ```terminal
   var/import/images
   ```

   ![Filkatalog för import av data-bilder](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   Lämna _[!UICONTROL Images File Directory]_tom för att använda `<Magento-root-folder>/var/import/images` katalog. Från och med Adobe Commerce och Magento Open Source version 2.3.2 är detta standardkatalogen för importbilder.

   Om du importerar flera bilder för en enda `sku`infogar du bilderna i en kolumn med namnet `additional_images` (lägg till kolumnen om den inte redan har lagts till), avgränsade med kommatecken. Exempel: `image02.jpg,image03.jpg`

## Metod 2: Importera bilder från extern server

1. Överför bilderna som ska importeras till den angivna mappen på den externa servern.

1. I CSV-data anger du den fullständiga URL:en för varje bildfil i rätt kolumn efter bildtyp (`base_image`, `small_image`, `thumbnail_image`, eller `additional_images`).

   ```terminal
   https://example.com/images/image.jpg
   ```

1. Följ instruktionerna för att [import](data-import.md) data.

## Metod 3: Importera bilder med fjärrlagring

1. Överför bildfilerna till modulen Fjärrlagring `var/import/images` mapp eller undermapp, till exempel `var/import/images/product_images`. Det här är standardrotmappen för import av produktbilder.

   ```terminal
   <remote-storage-root-folder>/var/import/images
   ```

   >[!NOTE]
   >
   Från Adobe Commerce och Magento Open Source `2.3.2` release, den sökväg som anges i _[!UICONTROL Images File Directory]_sammanfogar för import till bildens baskatalog: `<remote-storage-root-folder>/var/import/images`. I tidigare versioner av Adobe Commerce och Magento Open Source kan du använda en annan mapp på Commerce-servern så länge sökvägen till mappen anges under importen.

1. I CSV-data anger du namnet på varje bildfil som ska importeras på rätt rad av `sku`och i rätt kolumn enligt bildtyp (`base_image`, `small_image`, `thumbnail_image`, eller `additional_images`).

   >[!NOTE]
   >
   För bilder i standardimportmappen (`var/import/images`) ska du inte ta med sökvägen före filnamnet i CSV-data.

   CSV-filen får bara innehålla `sku` -kolumn och relaterade bildkolumner.

   ![Exempel - Import av CSV-bilddata](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. Följ instruktionerna för att [import](data-import.md) data.

1. Ange den relativa sökvägen efter när du har valt vilken fil som ska importeras **[!UICONTROL Images File Directory]**.

   ```terminal
   var/import/images/product_images
   ```

   >[!TIP]
   >
   Lämna _[!UICONTROL Images File Directory]_tom för att använda `<Magento-root-folder>/var/import/images` katalog. Från och med Adobe Commerce och Magento Open Source version 2.3.2 är detta standardkatalogen för importbilder.

   Om du importerar flera bilder för en enda `sku`infogar du bilderna i en kolumn med namnet `additional_images` (lägg till kolumnen om den inte redan har lagts till), avgränsat med kommatecken: `image02.jpg,image03.jpg`

Mer information om hur du aktiverar och hanterar modulen för fjärrlagring finns i [Konfigurera fjärrlagring](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) i _Konfigurationsguide_.

>[!NOTE]
>
Bildens storlek ändras inte när du importerar produktbilder. Storleken på produktbilderna ändras i förgrunden av `pub/get.php`. Se till att `pub/get.php` fungerar som det ska, annars kanske inte bildens storlek ändras.
