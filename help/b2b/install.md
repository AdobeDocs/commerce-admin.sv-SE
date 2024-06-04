---
title: Installera [!DNL Adobe Commerce B2B] extension
description: Lär dig hur du installerar [!DNL Adobe Commerce B2B] metapackage.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---


# Installera [!DNL Adobe Commerce B2B] extension

Adobe Commerce B2B-tillägget är bara tillgängligt för Adobe Commerce v2.2.0 eller senare. Den installeras när du har installerat Adobe Commerce.

Installera den senaste versionen av B2B-tillägget som stöds i den distribuerade Adobe Commerce-versionen.

>[!NOTE]
>
>Dessa installationsanvisningar gäller för Adobe Commerce som driftsätts lokalt. Information om hur du installerar B2B-tillägget för Commerce-projekt som distribueras i molninfrastrukturen finns i [Commerce Cloud Infrastructure Guide](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/b2b-module.html).

## Krav

- Adobe Commerce version 2.3.x eller senare
- [Version som stöds av B2B-tillägget](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html#compatibility)
- Giltig [autentiseringsnycklar](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) för att hämta Adobe Commerce-tillägg.

  Spara autentiseringsnycklar för installation genom att definiera dem globalt i [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) katalog. Eller spara dem i en [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) i Adobe Commerce programrotkatalog.

Innan du installerar eller uppgraderar B2B-tillägget bör du kontrollera i versionsinformationen den senaste informationen om versionskompatibilitet, uppdateringar eller ändringar som kan påverka installations- eller uppgraderingskraven.

- [Versionsinformation för B2B](release-notes.md)
- [Versionsinformation för Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html?lang=en)

## Installationssteg

1. Uppdatera Adobe Commerce rotkatalog `composer.json` så här lägger du till beroenden för B2B-tillägget:

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Om ett fel inträffar, till exempel:

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Kontrollera att paketet är rättstavat, att det har en version och att paketet är tillgängligt och att det uppfyller kraven på minsta stabilitet (stabil).

1. Ange [autentiseringsnycklar](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

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

När installationen är klar konfigurerar och startar du meddelandekonsument, inklusive [ange parametrar för meddelandekunder](#configure-message-consumers).

## Meddelandekunder

Adobe Commerce B2B-tillägget använder MySQL för meddelandeköhantering. I följande tabell visas de meddelandekunder som stöder B2B-funktioner. När du har installerat tillägget startar du meddelandekunderna för de B2B-funktioner som krävs för din Commerce Store.

| Konsument | Beskrivning |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | Uppdateringspris för varje produkt i en delad katalog. Krävs när [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) alternativet är aktiverat i inställningarna för Admin-systemkonfigurationen. |
| `sharedCatalogUpdateCategoryPermissions` | Uppdaterar kategorier som tilldelats en delad katalogkategori. Krävs när [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) alternativet är aktiverat i inställningarna för Admin-systemkonfigurationen. |
| `negotiableQuotePriceUpdate` | Uppdaterar priser för överlåtbara offerter. Krävs när [**[!UICONTROL Quotes]**](quotes.md) alternativet är aktiverat i inställningarna för Admin-systemkonfigurationen. |
| `purchaseorder.toorder` | Konverterar inköpsorder till order. Krävs när [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) alternativet är aktiverat i inställningarna för Admin-systemkonfigurationen. |
| `purchaseorder.transactional.email` | Skicka e-post med inköpsorder. Krävs när [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) alternativet är aktiverat i inställningarna för Admin-systemkonfigurationen. |
| `purchaseorder.validation` | Validerar inköpsorder mot relevant [regler för godkännande](account-dashboard-approval-rules.md). Krävs när [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) alternativet är aktiverat i inställningarna för Admin-systemkonfigurationen. |
| `quoteItemCleaner` | Tar bort ogiltiga eller inaktiva prisnoteringar när en produkt tas bort från katalogen eller tas bort från kundvagnen. Krävs när [**[!UICONTROL Quotes]**](quotes.md) alternativet är aktiverat i inställningarna för Admin-systemkonfigurationen. |
| `inventoryQtyCounter` | Asynkront korrigerar aktieindexet efter att en order har placerats eller en produkt har tagits bort. Krävs när [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) är aktiverat för Inventory management i inställningarna för Admin-konfigurationen. Se [Bästa praxis för prestanda](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/configuration.html#deferred-stock-update). |
| `async.operations.all` | Skapar meddelanden för varje enskild åtgärd i en [gruppåtgärd](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/), till exempel importera eller exportera artiklar, ändra priser i massskala och tilldela produkter till ett lager. Krävs när [**Gruppåtgärder för administratörer**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) alternativ för [!DNL Inventory Management] är inställd på **Kör asynkront** i konfigurationsinställningarna för administratörssystemet. |

{style="table-layout:auto"}

>[!NOTE]
>
>En lista över alla Adobe Commerce-kunder finns på [Konsumenter i meddelandekön](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/consumers.html) i _Konfigurationshandbok_.

### Konfigurera meddelandeanvändare

Förhindra eventuella bearbetningsproblem eller förseningar genom att lägga till följande parametrar när du [skapa budskap till konsumenterna](#start-message-consumers) för B2B-funktioner.

- `--max-messages <value>`— Anger det maximala antalet meddelanden som varje konsument måste behandla innan de avslutar (standard = 10000). Även om vi inte rekommenderar det kan du använda 0 för att hindra konsumenten från att säga upp sig. Det bästa sättet för ett PHP-program är att starta om långvariga processer för att förhindra eventuella minnesläckor.

- `--batch-size <value>`- Gör att du kan begränsa de systemresurser som förbrukas av konsumenterna (CPU, minne). Om du använder mindre grupper minskar resursanvändningen och det leder därmed till långsammare bearbetning.  Om det anges används meddelanden i en kö i grupper om `<value>` var. Det här alternativet gäller endast för batchkonsumenten. If `--batch-size` är inte definierad, tar batchkonsumenten emot alla tillgängliga meddelanden i en kö.

Mer information om ytterligare konfigurationsalternativ finns i [Specifik konfiguration](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#specific-configuration).

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

Mer information finns i [Hantera meddelandeköer](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) i _Konfigurationshandbok_.

### Lägg till meddelandekonsument i cron

Du kan automatisera körningsschemat för `SharedCatalogUpdateCategoryPermissions` och `SharedCatalogUpdatePrice` meddelandekonsument genom att lägga till schemat i kundkonfigurationsfilen [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

Du kan också konfigurera scheman för meddelandekunder från [Lagra konfigurationsinställningar](../systems/cron.md) i Admin.

## Aktivera B2B-funktioner i administratören

När du har installerat Adobe Commerce B2B-tillägget och startat för meddelandeanvändarna måste du också [aktivera B2B-funktioner i administratören](enable-basic-features.md).
