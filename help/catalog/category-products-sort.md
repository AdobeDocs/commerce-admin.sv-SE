---
title: Sortera kategoriprodukter
description: Lär dig hur du definierar placeringen av produkter i en kategori manuellt eller genom att använda en fördefinierad sorteringsordning.
exl-id: 09c66a5d-57d4-4e78-a8d8-e3047c1bd35a
feature: Catalog Management, Categories, Products
source-git-commit: 14c3eb7d54776382bfa196efdac446d42c8dc940
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# Sortera kategoriprodukter

{{ee-feature}}

Positionen för produkter i en kategori kan anges manuellt genom att dra och släppa produkter på plats eller genom att använda en fördefinierad sorteringsordning. Som standard kan produkterna sorteras efter lagernivå, ålder, färg, namn, SKU och pris. Automatisk sortering åsidosätter den aktuella sorteringsordningen och återställer eventuella dra och släpp-positioner som angetts manuellt. Sorteringsordningen för färger och den miniminivå som kan krävas för produkter som ska tas med i listan anges i [Visual Merchandiser](../configuration-reference/catalog/visual-merchandiser.md) konfiguration.

>[!NOTE]
>
>På kategorisidorna `Out of stock` produkter alltid visas **_efter_** `In Stock` produkter i produktlistan med alla sorteringstyper.

Du kan ställa in kategorialternativen separat för varje [butiksvy](../stores-purchase/stores.md#add-stores) för att bestämma vilka produkter som ska väljas, deras relativa position i listan och vilka attribut som är tillgängliga för kategoriregler. Det finns dock en enda **_global_** sorteringsordning och produktposition i katalogen och de delas i alla [butiksvyer](../stores-purchase/store-views.md), butiker och webbplatser.

## Steg 1: Ange omfattningen för konfigurationen

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Välj **[!UICONTROL Store View]** där inställningarna gäller.

   För en installation i flera butiker finns _[!UICONTROL Store View]_När du anger det här alternativet används sorteringsordningen för alla tillgängliga vyer i butiken.

1. Välj den kategori som du vill redigera i kategoriträdet till vänster.

   ![Kategoriträd](./assets/category-selected.png){width="700" zoomable="yes"}

## Steg 2: Sortera produkterna

>[!NOTE]
>
>När du sorterar en kategori efter ett produktattribut sorteras även produkter med samma attributvärden efter deras _[!UICONTROL Product ID]_i stigande ordning.

I _[!UICONTROL Products in Category]_klickar du på plattorna ( ![Visa paneler](../assets/icon-view-tiles.png) ) för att visa produktrutorna i ett rutnät. Använd antingen den manuella eller automatiska metoden för att sortera produkterna.

![Produktpaneler](./assets/category-products-tiles.png){width="600" zoomable="yes"}

### Metod 1: Manuell sortering

1. Ange **[!UICONTROL Sort Order]** efter dina önskemål.

   ![Sorteringsordning](./assets/category-edit-sort-order.png){width="600" zoomable="yes"}

1. Om du vill använda den nya sorteringsordningen klickar du på **[!UICONTROL Sort]**.

1. Spara sorteringsordningen genom att klicka på **[!UICONTROL Save Category]**.

1. Uppdatera ogiltiga indexerare när du uppmanas till detta.

### Metod 2: Automatisk sortering

1. Ange **[!UICONTROL Match products by rule]** (![Växla ja](../assets/toggle-yes.png)) till `Yes`.


1. Ange **[!UICONTROL Automatic Sorting]** efter dina önskemål.

1. Följ instruktionerna i nästa steg för att skapa en kategoriregel.

## Steg 3: Skapa en kategoriregel

1. Ange **[!UICONTROL Match products by rule]** (![Växla ja](../assets/toggle-yes.png)) till `Yes`.

1. Klicka på **[!UICONTROL Add Condition]**.

1. Välj **[!UICONTROL Attribute]** detta är grunden för villkoret.

1. Ange **[!UICONTROL Operator]** till något av följande:

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. Ange lämplig **[!UICONTROL Value]**.

   ![Kategorivillkor](./assets/category-rule-create.png){width="600" zoomable="yes"}

1. Om du vill lägga till ytterligare ett villkor klickar du på **[!UICONTROL Add Condition]** och upprepa processen.

## Steg 4: Spara, uppdatera och verifiera

1. När du är klar klickar du på **[!UICONTROL Save Category]**.

1. När du uppmanas att uppdatera cachen klickar du på **[!UICONTROL Cache Management]** och uppdatera varje ogiltig cache.

1. Kontrollera att reglerna för produkturval, sortering och kategori fungerar som de ska i butiken.

   Om du måste göra justeringar ändrar du inställningarna och försöker igen.
