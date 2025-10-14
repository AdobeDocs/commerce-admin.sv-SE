---
title: Enkel produkt
description: Lär dig hur du skapar en enkel produkt som kan säljas individuellt eller som en del av en grupperad, konfigurerbar eller paketerad produkt.
exl-id: 3ac9b28d-3929-4fd6-97ca-145ea6d6897c
feature: Catalog Management, Products
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Enkel produkt

En av nycklarna till att utnyttja kraften i olika produkttyper är att lära sig när man ska använda en enkel, fristående produkt. En enkel produkt kan säljas individuellt eller som en del av en grupperad produkt, konfigurerbar produkt eller paketprodukt. En enkel produkt med anpassade alternativ kallas ibland för en _sammansatt produkt_.

I följande instruktioner visas hur du skapar en enkel produkt med en [produktmall](attribute-sets.md), obligatoriska fält och grundläggande inställningar. Alla obligatoriska fält är markerade med en röd asterisk (`*`). När du är klar med grunderna kan du slutföra de andra produktinställningarna efter behov.

![Enkel produkt](./assets/product-simple.png){width="700" zoomable="yes"}

## Steg 1: Välj produkttyp

1. Gå till _>_ på sidofältet **[!UICONTROL Catalog]** Admin **[!UICONTROL Products]**.

1. Välj _[!UICONTROL Add Product]_&#x200B;på menyn ![&#x200B; ( &#x200B;](../assets/icon-menu-down-arrow-red.png){width="25"}menypil **[!UICONTROL Simple Product]**) i det övre högra hörnet.

   ![Lägg till enkel produkt](./assets/product-add-simple.png){width="700" zoomable="yes"}

## Steg 2: Välj attributuppsättning

Så här väljer du den [attributuppsättning](attribute-sets.md) som används som mall för produkten:

- Klicka i fältet **[!UICONTROL Attribute Set]** och ange hela eller en del av attributuppsättningens namn.

- Välj den attributuppsättning som du vill använda i listan som visas.

Formuläret uppdateras för att återspegla ändringen.

![Välj attributuppsättning](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Steg 3: Slutför de obligatoriska inställningarna

1. Ange **[!UICONTROL Product Name]**.

1. Acceptera standardvärdet **[!UICONTROL SKU]** som baseras på produktnamnet eller ange ett annat.

1. Ange produkten **[!UICONTROL Price]**.

1. Eftersom produkten ännu inte är klar att publiceras anger du alternativet **[!UICONTROL Enable Product]** till `No`.

1. klicka på **[!UICONTROL Save]** och fortsätt.

   När produkten sparas visas väljaren [Store View](introduction.md#product-scope) i det övre vänstra hörnet.

1. Välj den **[!UICONTROL Store View]** där produkten ska vara tillgänglig.

   ![Välj butiksvy](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Steg 4: Slutför de grundläggande inställningarna

1. Ange **[!UICONTROL Tax Class]** till något av följande:

   - `None`
   - `Taxable Goods`
   - `Refund Adjustments`
   - `Gift Options`
   - `Order Gift Wrapping`
   - `Item Gift Wrapping`
   - `Printed Gift Card`
   - `Reward Points`
   - `VAT Reduced`
   - `VAT Standard`

1. Ange **[!UICONTROL Quantity]** för produkten som finns i lager.

   Som standard är **[!UICONTROL Stock Status]** inställd på `In Stock`.

   >[!NOTE]
   >
   >Om du aktiverar [Inventory management](../inventory-management/introduction.md) anger handlare med en enda Source kvantiteten i det här avsnittet. Flera Source-handlare lägger till källor och kvantiteter i avsnittet Källor. Se följande avsnitt _Tilldela källor och kvantiteter (Inventory management)_.

1. Ange **[!UICONTROL Weight]** för produkten.

1. Acceptera standardinställningen **[!UICONTROL Visibility]** för `Catalog, Search`.

1. Om du vill tilldela _[!UICONTROL Categories]_&#x200B;till produkten klickar du på rutan **[!UICONTROL Select…]**&#x200B;och gör något av följande:

   **Välj en befintlig kategori**:

   - Börja skriva i rutan tills du hittar en matchning.

   - Markera kryssrutan för varje kategori som ska tilldelas.

   **Skapa en kategori**:

   - Klicka på **[!UICONTROL New Category]**.

   - Ange **[!UICONTROL Category Name]** och välj **[!UICONTROL Parent Category]** som avgör dess position i menystrukturen.

   - Klicka på **[!UICONTROL Create Category]**.

1. Markera kryssrutan [&#x200B; om du vill visa produkten i listan över &#x200B;](../content-design/widget-new-products-list.md)nya produkter **[!UICONTROL Set Product as New]**.

1. Välj **[!UICONTROL Country of Manufacture]**.

Det kan finnas ytterligare enskilda attribut som beskriver produkten. Markeringen varierar efter attributuppsättning och du kan slutföra dem senare.

### Tilldela källor och kvantiteter ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## Steg 5: Fyll i produktinformationen

Bläddra nedåt och fyll i informationen i följande avsnitt efter behov:

- [Innehåll](product-content.md)
- [Bilder och video](product-images-and-video.md)
- [Samhörande produkter, merförsäljning och korsförsäljning](related-products-up-sells-cross-sells.md)
- [Sökmotoroptimering](product-search-engine-optimization.md)
- [Anpassningsbara alternativ](settings-advanced-custom-options.md)
- [Produkter på webbplatser](settings-basic-websites.md)
- [Design](settings-advanced-design.md)
- [Presentalternativ](product-gift-options.md)

## Steg 6: Publicera produkten

1. Om du är redo att publicera produkten i katalogen anger du **[!UICONTROL Enable Product]**-växeln till `Yes`.

1. Gör något av följande:

   - **Metod 1:** Spara och förhandsgranska

      - Klicka på **[!UICONTROL Save]** i det övre högra hörnet.

      - Om du vill visa produkten i din butik väljer du **[!UICONTROL Customer View]** på menyn _Admin_ (![Menypil](../assets/icon-menu-down-arrow-black.png)).

     Butiken öppnas på en ny flik i webbläsaren.

     ![Kundvy](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Metod 2:** Spara och stäng

     Välj _[!UICONTROL Save]_&#x200B;på menyn ![&#x200B; ( &#x200B;](../assets/icon-menu-down-arrow-red.png){width="25"}Menypil **[!UICONTROL Save & Close]**).

## Saker att komma ihåg

- Enkla produkter kan inkluderas i konfigurerbara, paketerade och grupperade produkttyper.

- Enkel produktkonfiguration åsidosätter konfigurerbara produktkonfigurationer för en viss produkt.

- En enkel produkt kan ha anpassade alternativ med olika typer av indata, vilket gör det möjligt att sälja många produktvariationer från en enda SKU.

<!-- Last updated from includes: 2023-05-19 17:14:58 -->
