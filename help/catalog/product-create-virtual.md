---
title: Virtuell produkt
description: Lär dig hur du skapar en virtuell produkt som representerar en icke-materiell artikel, till exempel ett medlemskap, en tjänst, en garanti eller en prenumeration.
exl-id: 8788ba04-e911-429e-9e48-ce589f0c9fa1
feature: Catalog Management, Products
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Virtuell produkt

Virtuella produkter, eller digitala varor, representerar icke-materiella tillgångar som medlemskap, tjänster, garantier eller prenumerationer samt digitala nedladdningar av böcker, musik, videor eller andra produkter. Virtuella produkter kan säljas individuellt eller inkluderas som en del av produkttyperna [Grupperad produkt](product-create-grouped.md), [Konfigurerbar produkt](product-create-configurable.md) eller [Paketprodukt](product-create-bundle.md).

Förutom att fältet _[!UICONTROL Weight]_&#x200B;saknas är processen att skapa en virtuell produkt och en enkel produkt densamma. I följande instruktioner visas hur du skapar en virtuell produkt med hjälp av en [produktmall](attribute-sets.md), obligatoriska fält och grundläggande inställningar. När du är klar med grunderna kan du slutföra de andra produktinställningarna efter behov.

>[!NOTE]
>
>PayPal har ersatt stödet för försäljning av digitala varor via PayPal Express Checkout. De rekommenderar att du antingen använder [PayPal Payments Standard](../stores-purchase/paypal-payments-standard.md) eller någon annan PayPal-betalningsgateway för att bearbeta alla order som innehåller virtuella produkter.

![Virtuell produkt](./assets/product-virtual-membership.png){width="700" zoomable="yes"}

## Steg 1: Välj produkttyp

1. Gå till _>_ på sidofältet **[!UICONTROL Catalog]** Admin **[!UICONTROL Products]**.

1. Välj _[!UICONTROL Add Product]_&#x200B;på menyn ![&#x200B; ( &#x200B;](../assets/icon-menu-down-arrow-red.png){width="25"}menypil **[!UICONTROL Virtual Product]**) i det övre högra hörnet.

   ![Lägg till virtuell produkt](./assets/product-add-virtual.png){width="700" zoomable="yes"}

## Steg 2: Välj attributuppsättning

Gör något av följande om du vill välja den [attributuppsättning](attribute-sets.md) som används som mall för produkten:

- Klicka i fältet **[!UICONTROL Attribute Set]** och ange hela eller en del av attributuppsättningens namn.

- Välj den attributuppsättning som du vill använda i listan som visas.

Formuläret uppdateras för att återspegla ändringen.

![Välj attributuppsättning](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Steg 3: Slutför de obligatoriska inställningarna

1. Ange **[!UICONTROL Product Name]**.

1. Acceptera standardvärdet **[!UICONTROL SKU]** som baseras på produktnamnet eller ange ett annat.

1. Ange produkten **[!UICONTROL Price]**.

1. Eftersom produkten ännu inte är klar att publiceras anger du **[!UICONTROL Enable Product]** till `No`.

1. Klicka på **[!UICONTROL Save]** och fortsätt.

   När produkten sparas visas väljaren [Store View](introduction.md#product-scope) i det övre vänstra hörnet.

1. Välj den **[!UICONTROL Store View]** där produkten ska vara tillgänglig.

   ![Välj butiksvy](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Steg 4: Slutför de grundläggande inställningarna

1. Ange **[!UICONTROL Tax Class]** till något av följande:

   - `None`
   - `Taxable Goods`

1. Ange **[!UICONTROL Quantity]** för produkten som finns i lager och gör följande:

   - Acceptera standardinställningen **[!UICONTROL Stock Status]** för `In Stock`.

     Eftersom ingen virtuell produkt har levererats används inte fältet **[!UICONTROL Weight]**.

   - Acceptera standardinställningen **[!UICONTROL Visibility]** för `Catalog, Search`.

   >[!NOTE]
   >
   >Om du aktiverar [Inventory management](../inventory-management/introduction.md) anger handlare med en enda källa kvantiteten i det här avsnittet. Flera källhandlare lägger till källor och kvantiteter i avsnittet Källor. Se följande avsnitt _Tilldela källor och kvantiteter (Inventory management)_.

1. Om du vill tilldela **[!UICONTROL Categories]** till produkten klickar du på rutan **[!UICONTROL Select…]** och gör något av följande:

   **Välj en befintlig kategori**:

   - Börja skriva i rutan tills du hittar en matchning.

   - Markera kryssrutan för den kategori som ska tilldelas.

   **Skapa en kategori**:

   - Klicka på **[!UICONTROL New Category]**.

   - Ange **[!UICONTROL Category Name]** och välj **[!UICONTROL Parent Category]** som avgör dess position i menystrukturen.

   - Klicka på **[!UICONTROL Create Category]**.

   Det kan finnas ytterligare enskilda attribut som beskriver produkten. Markeringen varierar beroende på attributuppsättning och du kan slutföra dem senare.

### Tilldela källor och kvantiteter ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## Steg 5: Fyll i produktinformationen

Fyll i informationen i följande avsnitt efter behov:

- [Innehåll](product-content.md)
- [Bilder och video](product-images-and-video.md)
- [Sökmotoroptimering](product-search-engine-optimization.md)
- [Samhörande produkter, merförsäljning och korsförsäljning](related-products-up-sells-cross-sells.md)
- [Anpassningsbara alternativ](settings-advanced-custom-options.md)
- [Produkter på webbplatser](settings-basic-websites.md)
- [Design](settings-advanced-design.md)
- [Presentalternativ](product-gift-options.md)

>[!NOTE]
>
>Alternativet _[!UICONTROL Is this downloadable product?]_&#x200B;är inaktiverat som standard. Om du aktiverar den här funktionen för en virtuell produkt blir produkten [nedladdningsbar](product-create-downloadable.md#downloadable-product).

## Steg 6: Publicera produkten

1. Om du är redo att publicera produkten i katalogen anger du **[!UICONTROL Enable Product]** till `Yes`.

1. Gör något av följande:

   - **Metod 1:** Spara och förhandsgranska

      - Klicka på **[!UICONTROL Save]** i det övre högra hörnet.

      - Om du vill visa produkten i din butik väljer du **[!UICONTROL Customer View]** på menyn _Admin_ ( ![Menypil &#x200B;](../assets/icon-menu-down-arrow-black.png) ).

     Butiken öppnas på en ny flik i webbläsaren.

     ![Kundvy](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Metod 2:** Spara och stäng

     Välj _[!UICONTROL Save]_&#x200B;på menyn ![&#x200B; (](../assets/icon-menu-down-arrow-red.png){width="25"}Menypil **[!UICONTROL Save & Close]**).

## Saker att komma ihåg

- Virtuella produkter används för icke-materiella produkter som tjänster, prenumerationer och garantier.

- Virtuella produkter är som enkla produkter, men utan vikt.

- Leveransalternativen visas inte vid utcheckning om det inte finns en faktisk produkt i kundvagnen.

<!-- Last updated from includes: 2023-05-19 17:14:58 -->
