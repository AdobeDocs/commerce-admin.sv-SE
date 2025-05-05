---
title: Importera nivåpriser
description: Lär dig hur du exporterar nivåprissättningsdata och importerar uppdaterade data.
exl-id: b19d0208-68b3-45ba-9896-318e12ff4131
feature: Products, Data Import/Export
source-git-commit: 55b0672984ce8cdb853daf024299919beaf7ce0b
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---

# Importera nivåpriser

I stället för att ange [nivåpriser](../catalog/product-price-tier.md) manuellt för varje produkt kan det vara mer effektivt att [importera](data-import.md) prisdata. Innan du börjar skapar du en exempelfil med exporterade nivåprisdata som du kan använda som mall.

![Exempelbutiker - nivåpriser](./assets/storefront-tier-pricing-water-bottle.png){width="700" zoomable="yes"}

## Steg 1: Exportera skiktprisdata

I följande exempel exporteras data om nivåpriser för en enskild produkt. Sedan kan du använda exporterade data som en mall för bulkimport av skiktprisdata. Mer information om hur du exporterar avancerade prisdata finns i [Avancerade prissättningsdata](data-attributes-product.md#advanced-pricing-attributes).

![Priser på produktnivå](./assets/price-tier-customer-group-discount.png){width="600" zoomable="yes"}

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**&#x200B;på sidofältet_ Admin _.

1. Under _[!UICONTROL Export Settings]_&#x200B;anger du **[!UICONTROL Entity Type]**&#x200B;till `Advanced Pricing`.

1. Bläddra nedåt till SKU-attributen i rutnätet **[!UICONTROL Entity Attributes]** och gör följande:

   - För nivåpriser som baseras på en rabattprocent anger du SKU för varje produkt som ska exporteras, åtskilda med kommatecken.

     ![Dataexport - produkt-SKU](./assets/price-tier-export-sku.png){width="600" zoomable="yes"}

   - För nivåpriser som baseras på ett fast belopp anger du SKU för varje produkt.

   - Rulla ned och klicka på **[!UICONTROL Continue]**.

1. Leta upp exportfilen på nedladdningsplatsen för webbläsaren och öppna filen.

   ![Exempel - exporterade prisdata för kundgruppsrabatt](./assets/price-tier-customer-group-discount-export.png){width="600" zoomable="yes"}

**_Exporterade nivåprisdata_**

Följande kolumner inkluderas i exporterade data:

- `sku`
- `tier_price_website`
- `tier_price_customer_group`
- `tier_price_qty`
- `tier_price`
- `tier_price_value_type`

Du använder exporterade data som en mall för import av skiktprisdata.

## Steg 2: Uppdatera data

1. Uppdatera skiktprisdata för varje produkt efter behov.

   Alla produkter utan nivåprisuppdateringar kan tas bort från CSV-filen. Du behöver inte importera om produkter som inte har ändrats.

1. **[!UICONTROL Save]** den uppdaterade CSV-filen.

>[!NOTE]
>
>Importfilens storlek får inte vara större än 2 MB.

## Steg 3: Importera uppdaterade data

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**&#x200B;på sidofältet_ Admin _.

1. Under _Importinställningar_ anger du **[!UICONTROL Entity Type]** till `Advanced Pricing`.

1. Ange **[!UICONTROL Import Behavior]** till `Add/Update`.

1. Under **[!UICONTROL File to Import]** klickar du på **[!UICONTROL Choose File]** och väljer den fil som du förberedde för import från din katalog.

1. Klicka på **[!UICONTROL Check Data]** i det övre högra hörnet.

1. Om filen är giltig klickar du på **[!UICONTROL Import]**.

   I annat fall åtgärdar du alla problem med de data som visas i meddelandet och försöker importera filen igen.
