---
title: Installera [!DNL Adobe Commerce B2B] extension
description: Lär dig hur du installerar [!DNL Adobe Commerce B2B] metapackage.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: be36742aa1214e7e8e7f343051336cd3635099f4
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---


# Installera [!DNL Adobe Commerce B2B] extension

Adobe Commerce B2B-tillägget `magento/extension-b2b` finns för alla versioner av Adobe Commerce som stöds. Den installeras när du har installerat Adobe Commerce.


## Krav

- [Adobe Commerce](https://business.adobe.com/products/magento/magento-commerce.html), alla versioner som stöds
- PHP 8.1 / 8.2 / 8.3
- [!DNL Composer]

## Plattformar som stöds

- Adobe Commerce om molninfrastruktur (ECE)
- Adobe Commerce lokal (EE)

## Installationssteg

>[!BEGINSHADEBOX]

**Förutsättningar**

- Åtkomst till [repo.magento.com](https://repo.magento.com/) för att hämta tillägget. För nyckelgenerering och för att erhålla nödvändiga rättigheter, se [Hämta dina autentiseringsnycklar](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

  Spara autentiseringsnycklar för installation genom att definiera dem globalt i [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) katalog. Eller spara dem i en [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) i Adobe Commerce programrotkatalog.

- [Version som stöds av B2B-tillägget](https://experienceleague.adobe.com/en/docs/commerce-operations/release/product-availability)-Bestäm den senaste versionen av B2B-tillägget som stöds i den distribuerade Adobe Commerce-versionen.

- I versionsinformationen finns den senaste informationen om versionskompatibilitet, uppdateringar eller ändringar som kan påverka installations- eller uppgraderingskrav.

   - [Versionsinformation för B2B](release-notes.md)
   - [Versionsinformation för Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

Installera B2B-tillägget (`magento/b2b-extension`) med Composer. Tillägget är ett Composer-metapaket som innehåller en samling moduler som aktiverar B2B-funktionerna för en Adobe Commerce-instans. En lista med inkluderade moduler finns på [B2B-paket](packages.md).

>[!BEGINTABS]

>[!TAB Molninfrastruktur]

>[!TIP]
>
>När du installerar Adobe Commerce B2B i molninfrastrukturen rekommenderar Adobe att du distribuerar Adobe Commerce-programmet till en integrerings- eller mellanlagringsmiljö innan du börjar.

Adobe rekommenderar att du arbetar i en utvecklingsgren när du lägger till B2B-tillägget i ditt projekt. Om du inte har någon gren kan du läsa [Skapa en gren för utveckling](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches). När du installerar B2B-tillägget `Magento_B2b` tilläggsnamnet infogas automatiskt i `app/etc/config.php` -fil. Du behöver inte redigera filen direkt.

**Installera B2B-tillägget**:

1. Byt till din projektkatalog på din lokala arbetsstation.

1. Skapa eller checka ut en utvecklingsgren.

1. Lägg till B2B-tillägget i `require` i `composer.json` -fil.

   ```bash
   composer require magento/extension-b2b --no-update
   ```

1. Uppdatera projektberoenden.

   ```bash
   composer update
   ```

1. Lägg till, implementera och push-ändra kod.

   ```bash
   git add -A
   ```

   ```bash
   git commit -m "Install the B2B extension."
   ```

   ```bash
   git push origin <branch-name>
   ```

   >[!NOTE]
   >
   >När du publicerar uppdateringar till molnmiljön initieras Commerce molndistributionsprocess för att ändringarna ska börja gälla. Kontrollera distributionsstatusen på [distributionslogg](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process). Om du råkar ut för distributionsfel finns mer information i [Återställning efter komponentfel](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment).

1. När bygget och distributionen är klar använder du SSH för att logga in på fjärrmiljön och verifiera att B2B-tillägget är installerat och aktiverat.

   ```bash
   bin/magento module:status Magento_B2b
   ```

   Ett tilläggsnamn har formatet: `<VendorName>_<ComponentName>`.

   Exempelsvar:

   ```terminal
   Magento_B2b : Module is enabled
   ```

>[!TAB Lokalt]

1. Uppdatera Adobe Commerce rotkatalog `composer.json` så här lägger du till beroenden för B2B-tillägget:

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Om ett fel inträffar, till exempel:

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Kontrollera att paketet är rättstavat, att det har en version och att paketet är tillgängligt och att det uppfyller kraven på minsta stabilitet (stabil).

1. Ange [autentiseringsnycklar](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

   Dina _publik nyckel_ är ditt användarnamn; din _privat nyckel_ är ditt lösenord. Om du har sparat dina offentliga och privata nycklar i `auth.json`, uppmanas du inte att autentisera.

1. Kör följande kommandon när Composer har slutfört uppdateringen av moduler:

   ```bash
   bin/magento setup:upgrade
   ```

   ```bash
   bin/magento setup:di:compile
   ```

   ```bash
   bin/magento setup:static-content:deploy -f
   ```

   ```bash
   bin/magento cache:clean
   ```

   >[!NOTE]
   >
   >I produktionsläget kan du få ett meddelande till `Please rerun Magento compile command`. Ange kommandona för att slutföra installationen. Adobe Commerce uppmanar dig inte att köra kompileringskommandot i utvecklarläge.

>[!ENDTABS]

När installationen är klar konfigurerar och startar du meddelandekonsument.

## Meddelandekunder

Adobe Commerce B2B-tillägget använder MySQL för meddelandeköhantering. I följande tabell visas de meddelandekunder som stöder B2B-funktioner. När du har installerat tillägget startar du meddelandekunderna för de B2B-funktioner som krävs för din Commerce Store.

| Konsument | Beskrivning |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | Uppdaterar priset för varje produkt i en delad katalog. Krävs när [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) alternativet är aktiverat i konfigurationsinställningarna för Admin System. |
| `sharedCatalogUpdateCategoryPermissions` | Uppdaterar kategorier som tilldelats en delad katalogkategori. Krävs när [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) alternativet är aktiverat i konfigurationsinställningarna för Admin System. |
| `negotiableQuotePriceUpdate` | Uppdaterar priser för överlåtbara offerter. Krävs när [**[!UICONTROL Quotes]**](quotes.md) alternativet är aktiverat i konfigurationsinställningarna för Admin System. |
| `purchaseorder.toorder` | Konverterar inköpsorder till order. Krävs när [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) alternativet är aktiverat i konfigurationsinställningarna för Admin System. |
| `purchaseorder.transactional.email` | Skicka e-post med inköpsorder. Krävs när [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) alternativet är aktiverat i konfigurationsinställningarna för Admin System. |
| `purchaseorder.validation` | Validerar inköpsorder mot relevant [regler för godkännande](account-dashboard-approval-rules.md). Krävs när [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) alternativet är aktiverat i konfigurationsinställningarna för Admin System. |
| `quoteItemCleaner` | Tar bort ogiltiga eller inaktiva prisnoteringar när en produkt tas bort från katalogen eller tas bort från kundvagnen. Krävs när [**[!UICONTROL Quotes]**](quotes.md) alternativet är aktiverat i konfigurationsinställningarna för Admin System. |
| `inventoryQtyCounter` | Asynkront korrigerar aktieindexet efter att en order har placerats eller en produkt har tagits bort. Krävs när [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) är aktiverat för Inventory management i inställningarna för Admin-konfigurationen. Se [Bästa praxis för prestanda](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update). |
| `async.operations.all` | Skapar meddelanden för varje enskild åtgärd i en [gruppåtgärd](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/) till exempel importera eller exportera artiklar, ändra priser i massskala och tilldela produkter till ett lagerställe. Krävs när [**Gruppåtgärder för administratörer**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) alternativ för [!DNL Inventory Management] är inställd på **Kör asynkront** i konfigurationsinställningarna för Admin System. |

{style="table-layout:auto"}

>[!NOTE]
>
>En lista över alla Adobe Commerce-kunder finns på [Konsumenter i meddelandekön](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/consumers) i _Konfigurationshandbok_.

### Konfigurera meddelandeanvändare

Förhindra eventuella bearbetningsproblem eller förseningar genom att lägga till följande parametrar när du [skapa budskap till konsumenterna](#start-message-consumers) för B2B-funktioner.

- `--max-messages <value>`— Anger det maximala antalet meddelanden som varje konsument måste behandla innan de avslutar (standard = 10000). Även om Adobe inte rekommenderar det kan du använda 0 för att hindra konsumenten från att säga upp sig. Det bästa sättet för ett PHP-program är att starta om långvariga processer för att förhindra eventuella minnesläckor.

- `--batch-size <value>`- Gör att du kan begränsa de systemresurser som förbrukas av konsumenterna (CPU, minne). Om du använder mindre grupper minskar resursanvändningen och det leder därmed till långsammare bearbetning.  Om det anges används meddelanden i en kö i grupper om `<value>` var. Det här alternativet gäller endast för batchkonsumenten. If `--batch-size` är inte definierad, tar batchkonsumenten emot alla tillgängliga meddelanden i en kö.

Mer information om ytterligare konfigurationsalternativ finns i [Specifik konfiguration](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#specific-configuration).

### Börjar skicka meddelanden till konsumenter

Om du vill aktivera asynkrona åtgärder för B2B-funktioner måste du starta flera meddelandekonsument.

1. Visa en lista över tillgängliga meddelandekunder:

   ```bash
   bin/magento queue:consumers:list
   ```

   Kommandot returnerar tillgängliga meddelandekunder inklusive alla [B2B-meddelandekunder](#message-consumers).

1. Starta varje kund separat:

   ```bash
   bin/magento queue:consumers:start [--max-messages=<value>] [--batch-size=<value>] <consumer_name>
   ```

   Exempel:

   ```bash
   bin/magento queue:consumers:start quoteItemCleaner
   ```

>[!TIP]
>
>Om du vill köra den i bakgrunden lägger du till `&` till kommandot, återgå till en uppmaning och fortsätta köra kommandon. Till exempel: `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

Mer information finns i [Hantera meddelandeköer](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues) i _Konfigurationshandbok_.

### Lägg till meddelandekonsument i cron

Du kan automatisera körningsschemat för `SharedCatalogUpdateCategoryPermissions` och `SharedCatalogUpdatePrice` meddelandekonsument genom att lägga till schemat i kundkonfigurationsfilen [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

Du kan också konfigurera scheman för meddelandekunder från [Lagra konfigurationsinställningar](../systems/cron.md) i Admin.

## Aktivera B2B-funktioner i administratören

När du har installerat Adobe Commerce B2B-tillägget och startat för meddelandeanvändarna måste du också [aktivera B2B-funktioner i administratören](enable-basic-features.md).

