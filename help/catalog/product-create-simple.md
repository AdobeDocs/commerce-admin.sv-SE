---
title: Enkel produkt
description: Lär dig hur du skapar en enkel produkt som kan säljas individuellt eller som en del av en grupperad, konfigurerbar eller paketerad produkt.
exl-id: 3ac9b28d-3929-4fd6-97ca-145ea6d6897c
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---

# Enkel produkt

En av nycklarna till att utnyttja kraften i olika produkttyper är att lära sig när man ska använda en enkel, fristående produkt. En enkel produkt kan säljas individuellt eller som en del av en grupperad produkt, konfigurerbar produkt eller paketprodukt. En enkel produkt med anpassade alternativ kallas ibland för _sammansatt produkt_.

I följande instruktioner visas hur du skapar en enkel produkt med en [produktmall](attribute-sets.md), obligatoriska fält och grundläggande inställningar. Varje obligatoriskt fält markeras med en röd asterisk (`*`). När du är klar med grunderna kan du slutföra de andra produktinställningarna efter behov.

![Enkel produkt](./assets/product-simple.png){width="700" zoomable="yes"}

## Steg 1: Välj produkttyp

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. På _[!UICONTROL Add Product]_( ![Menypil](../assets/icon-menu-down-arrow-red.png){width="25"} ) längst upp till höger väljer du **[!UICONTROL Simple Product]**.

   ![Lägg till enkel produkt](./assets/product-add-simple.png){width="700" zoomable="yes"}

## Steg 2: Välj attributuppsättning

Välj [attributuppsättning](attribute-sets.md) som används som mall för produkten:

- Klicka på **[!UICONTROL Attribute Set]** och ange hela eller delar av attributuppsättningens namn.

- Välj den attributuppsättning som du vill använda i listan som visas.

Formuläret uppdateras för att återspegla ändringen.

![Välj attributuppsättning](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Steg 3: Slutför de obligatoriska inställningarna

1. Ange **[!UICONTROL Product Name]**.

1. Acceptera standardinställningen **[!UICONTROL SKU]** som baseras på produktnamnet eller anger ett annat.

1. Ange produkten **[!UICONTROL Price]**.

1. Eftersom produkten ännu inte är klar att publiceras ställer du in **[!UICONTROL Enable Product]** alternativ till `No`.

1. klicka **[!UICONTROL Save]** och fortsätta.

   När produkten sparas kan du [Butiksvy](introduction.md#product-scope) Väljaren visas i det övre vänstra hörnet.

1. Välj **[!UICONTROL Store View]** där produkten ska finnas tillgänglig.

   ![Välj butiksvyn](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

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

1. Ange **[!UICONTROL Quantity]** av den produkt som finns i lager.

   Som standard **[!UICONTROL Stock Status]** är inställd på `In Stock`.

   >[!NOTE]
   >
   >Om du aktiverar [Inventory management](../inventory-management/introduction.md), försäljare med en källa anger kvantiteten i det här avsnittet. Flera källhandlare lägger till källor och kvantiteter i avsnittet Källor. Se följande _Tilldela källor och kvantiteter (Inventory management)_ -avsnitt.

1. Ange **[!UICONTROL Weight]** av produkten.

1. Acceptera standardinställningen **[!UICONTROL Visibility]** inställning för `Catalog, Search`.

1. Tilldela _[!UICONTROL Categories]_till produkten klickar du på&#x200B;**[!UICONTROL Select…]**och gör något av följande:

   **Välj en befintlig kategori**:

   - Börja skriva i rutan tills du hittar en matchning.

   - Markera kryssrutan för varje kategori som ska tilldelas.

   **Skapa en kategori**:

   - Klicka på **[!UICONTROL New Category]**.

   - Ange **[!UICONTROL Category Name]** och väljer **[!UICONTROL Parent Category]** som bestämmer dess placering i menystrukturen.

   - Klicka på **[!UICONTROL Create Category]**.

1. Så här visar du produkten i listan över [nya produkter](../content-design/widget-new-products-list.md)väljer du **[!UICONTROL Set Product as New]** kryssrutan.

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

1. Om du vill publicera produkten i katalogen anger du **[!UICONTROL Enable Product]** växla till `Yes`.

1. Gör något av följande:

   - **Metod 1:** Spara och förhandsgranska

      - Klicka på i det övre högra hörnet **[!UICONTROL Save]**.

      - Om du vill visa produkten i din butik väljer du **[!UICONTROL Customer View]** på _Administratör_ (![Menypil](../assets/icon-menu-down-arrow-black.png)).

     Butiken öppnas på en ny flik i webbläsaren.

     ![Kundvy](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Metod 2:** Spara och stäng

     På _[!UICONTROL Save]_ ( ![Menypil](../assets/icon-menu-down-arrow-red.png){width="25"} ) väljer du **[!UICONTROL Save & Close]**.

## Saker att komma ihåg

- Enkla produkter kan inkluderas i konfigurerbara, paketerade och grupperade produkttyper.

- Enkel produktkonfiguration åsidosätter konfigurerbara produktkonfigurationer för en viss produkt.

- En enkel produkt kan ha anpassade alternativ med olika typer av indata, vilket gör det möjligt att sälja många produktvariationer från en enda SKU.
