---
title: Konfigurerbar produkt
description: Lär dig hur du skapar en konfigurerbar produkt som ger kunderna olika valmöjligheter.
exl-id: 2066fd20-5227-41e9-b213-31825a58ebd9
feature: Catalog Management, Products
source-git-commit: f6140fda2769e109d2b38c2f9c458f67097dff0a
workflow-type: tm+mt
source-wordcount: '2483'
ht-degree: 0%

---

# Konfigurerbar produkt

En konfigurerbar produkt ser ut som en enskild produkt med en listruta över varje variant. Varje listartikel är i själva verket en separat enkel produkt med en unik SKU, som gör det möjligt att spåra lager för varje produktvariation. Du kan uppnå en liknande effekt genom att använda en enkel produkt med anpassade alternativ, men utan möjlighet att spåra lager för varje variation.

I följande instruktioner visas hur du skapar en konfigurerbar produkt med en [produktmall](attribute-sets.md), obligatoriska fält och grundläggande inställningar. Varje obligatoriskt fält markeras med en röd asterisk (`*`). När du är klar med grunderna kan du slutföra de andra produktinställningarna efter behov.

![Konfigurerbar produkt](./assets/product-configurable.png){width="700" zoomable="yes"}

## Del 1: Skapa en konfigurerbar produkt

Även om en konfigurerbar produkt använder fler SKU:er och till att börja med tar lite längre tid att konfigurera, kan det spara tid i slutänden. Om du planerar att utöka din verksamhet är den konfigurerbara produkttypen ett bra val för produkter med flera alternativ.

Förbered en [attributuppsättning](attribute-sets.md) som innehåller ett attribut som är inställt på en av de tillåtna indatatyperna för varje produktvariation. Attributuppsättningen kan till exempel innehålla listruteattribut för färg och storlek.

Egenskaperna för varje attribut som används för en konfigurerbar produktvariation måste ha följande inställningar:

### Krav för produktvariantattribut

| Egenskap | Inställning |
|--- |--- |
| [!UICONTROL Scope] | `Global` |
| [!UICONTROL Catalog Input Type for Store Owner] | Indatatypen för alla attribut som används för en produktvariation måste vara något av följande: `Dropdown`, `Visual Swatch`, eller `Text Swatch`. |
| [!UICONTROL Values Required] | `Yes` |

{style="table-layout:auto"}

### Steg 1: Välj produkttyp

1. På _Administratör_ sidebar, gå till  **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. På _[!UICONTROL Add Product]_( ![Menypil](../assets/icon-menu-down-arrow-red.png){width="25"} ) i det övre högra hörnet väljer du **[!UICONTROL Configurable Product]**.

   ![Lägg till konfigurerbar produkt](./assets/product-add-configurable.png){width="700" zoomable="yes"}

### Steg 2: Välj attributuppsättning

The [attributuppsättning](attribute-sets.md) bestämmer valet av fält som används i produkten. Attributuppsättningen som används i följande exempel har attribut för färg och storlek. Attributuppsättningens namn anges längst upp på sidan och ställs från början in på `Default`.

1. Om du vill välja attributuppsättning för produkten klickar du på fältet överst på sidan och gör något av följande:

   - För **[!UICONTROL Search]** anger du namnet på attributuppsättningen.
   - I listan väljer du den attributuppsättning som du vill använda.

   Formuläret uppdateras för att återspegla ändringen.

1. Om du vill lägga till ytterligare ett attribut i attributuppsättningen klickar du på **[!UICONTROL Add Attribute]** och följ instruktionerna i [Lägga till ett attribut](product-attributes-add.md).

   ![Välj mall](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

### Steg 3: Slutför de obligatoriska inställningarna

1. Ange produkten **[!UICONTROL Product Name]**.

1. Acceptera standardinställningen **[!UICONTROL SKU]** som baseras på produktnamnet eller anger ett annat.

1. Ange produkten **[!UICONTROL Price]**.

1. Eftersom produkten ännu inte är klar att publiceras kan du ange **[!UICONTROL Enable Product]** till `No`.

1. klicka **[!UICONTROL Save]** och fortsätta.

   När produkten sparas kan du [Butiksvy](introduction.md#product-scope) Väljaren visas i det övre vänstra hörnet.

1. Välj **[!UICONTROL Store View]** där produkten ska finnas tillgänglig.

   ![Välj butiksvyn](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Steg 4: Slutför de grundläggande inställningarna

1. Ange **[!UICONTROL Tax Class]** till något av följande:

   - `None`
   - `Taxable Goods`

1. The **[!UICONTROL Quantity]** bestäms av produktvariationerna så att du kan lämna det tomt.

1. Lämna **[!UICONTROL Stock Status]** som angivet.

   Lagerstatus för en konfigurerbar produkt bestäms av varje associerad konfiguration. Eftersom produkten sparades utan att någon kvantitet angavs har **[!UICONTROL Stock Status]** är inställd på `Out of Stock`.

   >[!NOTE]
   >
   >The **Stock-status** av den konfigurerbara produkten är en **_halvmanuell_** styrd inställning. Den kontrolleras delvis av statusen Stock för dess underordnade produkter. Det ingår i en **_multivillkor_** beräkning av lagerstatus, som beskrivs i [Konfigurera Stock-status](#configure-the-stock-status) -avsnitt.

1. Ange produkten **[!UICONTROL Weight]**.

>[!NOTE]
>
>En konfigurerbar produkt måste alltid ha en vikt. Om du väljer **[!UICONTROL This item has no weight]** från listrutan ändras den automatiskt till **[!UICONTROL This item has weight]** när du har sparat produkten.

1. Acceptera standardinställningen **[!UICONTROL Visibility]** inställning för `Catalog, Search`.

1. Så här visar du produkten i listan över [nya produkter](../content-design/widget-new-products-list.md)väljer du **[!UICONTROL Set Product as New]** kryssrutan.

1. Om du vill tilldela produktkategorier klickar du på **[!UICONTROL Select…]** och gör något av följande:

   **Välj en befintlig kategori**:

   - Börja skriva i rutan tills du hittar en matchning.

   - Markera kryssrutan för den kategori som ska tilldelas.

   ![Välj en eller flera kategorier för paketprodukten](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **Skapa en kategori**:

   - Klicka på **[!UICONTROL New Category]**.

   - Ange **[!UICONTROL Category Name]** och väljer **[!UICONTROL Parent Category]** som bestämmer dess placering i menystrukturen.

   s- klicka **[!UICONTROL Create Category]**.

1. Välj **[!UICONTROL Country of Manufacture]**.

   Det kan finnas ytterligare attribut som används för att beskriva produkten. Markeringen varierar efter attributuppsättning och du kan slutföra dem senare.

### Steg 5: Spara och fortsätt

Nu är ett bra tillfälle att spara ditt arbete. Klicka på i det övre högra hörnet **[!UICONTROL Save]**. I nästa serie steg ställer du in konfigurationerna för varje produktvariant.

## Del 2: Lägga till konfigurationer

I följande exempel visas hur du lägger till konfigurationer för tre färger och tre storlekar. Sammantaget skapas nio enkla produkter med unika SKU:er som täcker alla möjliga kombinationer av variationer. Som standard baseras produktnamnet och SKU:n för varje variation på attributvärdet och antingen det överordnade produktnamnet eller SKU:n.

Förloppsindikatorn högst upp på sidan visar var du befinner dig i processen och guidar dig genom varje steg.

### Steg 1: Välj attribut

1. Fortsätt uppifrån och ned, rulla nedåt till _[!UICONTROL Configurations]_och klicka **[!UICONTROL Create Configurations]**.

   ![Konfigurationer](./assets/product-configurable-create-configurations.png){width="600" zoomable="yes"}

1. Markera kryssrutan för alla attribut som du vill inkludera som en konfiguration.

   I detta exempel `color` och `size` är markerade.

   ![Välj attribut](./assets/product-create-configurable-step1.png){width="600" zoomable="yes"}

   Listan innehåller alla attribut från attributuppsättningen som kan användas i en konfigurerbar produkt.

1. Om du vill lägga till ett attribut klickar du på **[!UICONTROL Create New Attribute]** och gör följande:

   - Fyll i attributegenskaperna.

   - Klicka på **[!UICONTROL Save Attribute]**.

   - Markera kryssrutan för attributet.

1. Klicka på i det övre högra hörnet **[!UICONTROL Next]**.

### Steg 2: Ange attributvärden

1. För varje attribut markerar du kryssrutan för de värden som gäller för produkten.

   ![Attributvärden](./assets/product-create-configurable-step2.png){width="600" zoomable="yes"}

1. Om du vill ordna om attributen klickar du på knappen _Ändra ordning_ ( ![Ikon för sorteringsordning](../assets/icon-sort-order.png) ) och flytta avsnittet till en ny plats.

   Ordningen bestämmer positionen för listrutorna på produktsidan.

1. Klicka på i förloppsindikatorn **[!UICONTROL Next]**.

### Steg 3: Konfigurera bilder, pris och kvantitet

I det här steget fastställs bilder, priser och kvantitet för varje konfiguration. De tillgängliga alternativen är desamma för alla, och du kan bara välja ett. Du kan använda samma inställning för alla SKU:er, använda en unik inställning för varje SKU:er eller hoppa över inställningarna för tillfället.

Välj de konfigurationsalternativ som gäller.

Använd någon av följande metoder för att konfigurera **[!UICONTROL images]**:

**Metod 1:** Använda en enda uppsättning bilder på alla SKU:er

1. Välj **[!UICONTROL Apply single set of images to all SKUs]**.

1. Bläddra till varje bild som du vill ta med i produktgalleriet eller dra dem till rutan.

![Använd samma bilder för alla SKU:er](./assets/product-configurations-images-apply-single-set.png){width="600" zoomable="yes"}

**Metod 2:** Använd unika bilder för varje SKU

Eftersom bilden för den överordnade produkten redan har överförts kan du använda det här alternativet för att överföra en bild av varje färg. Du kan lägga till en annan bild som visas i kundvagnen när någon köper artikeln i en viss färg.

1. Välj **[!UICONTROL Apply unique images by attribute to each SKU]**.

1. Välj **[!UICONTROL Attribute]** som bilderna illustrerar, till exempel `color`.

1. För varje attributvärde bläddrar du till de bilder du vill använda för den konfigurationen eller drar dem till rutan.

   Om du drar bilden till en värderuta visas den även i avsnitten för de andra värdena. Om du vill ta bort en bild klickar du på _Papperskorgen_ (![Papperskorgsikon](../assets/icon-delete-trashcan-solid.png)).

   ![Unika bilder per SKU](./assets/product-configurable-create-configurations-add-images-unique.png){width="600" zoomable="yes"}

Använd någon av följande metoder för att konfigurera **[!UICONTROL prices]**:

>[!NOTE]
>
>En konfigurerbar produkt har inte ett eget pris i katalogen. Det konfigurerbara produktpriset härleds från dess [!UICONTROL In Stock] underordnade produkter.

**Metod 1:** Använd samma pris på alla SKU:er

1. Om priset är detsamma för alla variationer väljer du **[!UICONTROL Apply single price to all SKUs]**.

1. Ange **[!UICONTROL Price]**.

   ![Samma pris per SKU](./assets/product-configurable-create-configurations-price-all-skus.png){width="600" zoomable="yes"}

**Metod 2:** Använd olika pris för varje SKU

1. Om priset skiljer sig för var och en eller för vissa variationer av produkten väljer du **[!UICONTROL Apply unique prices by attribute to each SKU]**.

1. Välj **[!UICONTROL Attribute]** detta är grunden för prisskillnaden.

1. Ange **[!UICONTROL Price]** för varje attributvärde.

   I det här exemplet kostar XL-storleken mer.

   ![Unikt pris per SKU](./assets/product-configurable-create-configurations-price-unique.png){width="600" zoomable="yes"}

Använd någon av följande metoder för att konfigurera **[!UICONTROL Quantity]**:

**Metod 1:** Använd samma kvantitet för alla SKU:er

Om kvantiteten är densamma för alla SKU:er väljer du **[!UICONTROL Apply single quantity to each SKU]** och ange kvantiteten.

_Handlare med en enda källa_ - Ange **[!UICONTROL Quantity]**.

_Handlare med flera källor som använder [Inventory management](../inventory-management/introduction.md)_ - Tilldela källor och lägg till kvantiteter för alla genererade produktvarianter:

1. Välj **[!UICONTROL Apply single quantity to each SKU]** alternativ.

1. Om du vill lägga till en källa klickar du **[!UICONTROL Assign Sources]**.

1. Bläddra eller sök efter en källa som du vill lägga till. Markera kryssrutan bredvid de källor som du vill lägga till för produkten.

1. Ange ett lagerbehållningsbelopp per källa.

   ![En kvantitet för alla SKU:er, tilldela källa](./assets/inventory-configure-product-quantity.png){width="600" zoomable="yes"}

**Metod 2:** Använd annan kvantitet efter attribut

_Handlare med en enda källa_ - Ange **[!UICONTROL Quantity]**.

_Handlare med flera källor som använder [Inventory management](../inventory-management/introduction.md)_ - Tilldela källor och lägg till kvantiteter för alla genererade produktvarianter:

1. Om kvantiteten är olika för varje SKU väljer du **[!UICONTROL Apply unique quantity by attribute to each SKU]**.

1. Ange **[!UICONTROL Quantity]** for each.

   ![Olika kvantiteter per attribut](./assets/product-configurations-quantity-different.png){width="600" zoomable="yes"}

När konfigurationen för bilder, pris och kvantitet är klar klickar du på **[!UICONTROL Next]** längst upp till höger.

### Steg 4: Generera produktkonfigurationer

Vänta en stund tills produktlistan visas och gör något av följande:

- Om du är nöjd med konfigurationen klickar du på **[!UICONTROL Generate Products]**.

- Om du vill korrigera klickar du på **[!UICONTROL Back]**.

![Granska sammanfattningen innan du genererar produktvariationer](./assets/product-create-configurable-summary.png){width="600" zoomable="yes"}

De aktuella produktvariationerna visas längst ned i _Konfiguration_ -avsnitt.

![Aktuella konfigurationer](./assets/product-create-configurable-generated.png){width="600" zoomable="yes"}

### Steg 5: Lägg till produktbilder

1. Rulla ned och expandera ![Expansionsväljare](../assets/icon-display-expand.png) den _[!UICONTROL Images and Videos]_-avsnitt.

1. Klicka på _Kamera_ och bläddra till huvudbilden som du vill använda för den konfigurerbara produkten.

Mer information finns i [Bilder och video](product-images-and-video.md).

### Steg 6: Fyll i produktinformationen

Bläddra nedåt och fyll i informationen i följande avsnitt efter behov:

- [Innehåll](product-content.md)

- [Samhörande produkter, merförsäljning och korsförsäljning](related-products-up-sells-cross-sells.md)

- [Sökmotoroptimering](product-search-engine-optimization.md)

- [Anpassningsbara alternativ](settings-advanced-custom-options.md)

- [Produkter på webbplatser](settings-basic-websites.md)

- [Design](settings-advanced-design.md)

- [Presentalternativ](product-gift-options.md)

### Steg 7: Publicera produkten

1. Om du är redo att publicera produkten i katalogen anger du **[!UICONTROL Enable Product]** till `Yes` och gör något av följande:

   - **Metod 1:** Spara och förhandsgranska

      - Klicka på i det övre högra hörnet **[!UICONTROL Save]**.

      - Om du vill visa produkten i din butik väljer du **[!UICONTROL Customer View]** på _Administratör_ ( ![Menypil](../assets/icon-menu-down-arrow-black.png) ).

     Butiken öppnas på en ny flik i webbläsaren.

     ![Kundvy](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Metod 2:** Spara och stäng

     På _[!UICONTROL Save]_( ![Menypil](../assets/icon-menu-down-arrow-red.png){width="25"} ) väljer du **[!UICONTROL Save & Close]**.

### Steg 8: Konfigurera kundvagnsminiatyrerna

Om du har en annan bild för varje variant kan du ställa in konfigurationen så att rätt bild används för kundvagnsminiatyrbilden.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Checkout]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den _[!UICONTROL Shopping Cart]_-avsnitt.

1. Ange **[!UICONTROL Configurable Product Image]** till `Product Thumbnail Itself`.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

   ![Kundvagn - konfigurerbar produktbild](./assets/config-checkout-configurable-product.png){width="600" zoomable="yes"}

## Konfigurera Stock-status

Konfigurerbar produktlagerstatus skiljer sig från den enkla produktens lagerstatus, där det är en direkt representation av produktens tillgänglighet. För en konfigurerbar produkt är lagerstatusen en del av en **_multivillkor_** beräkning av lagerstatus.

### Ökning

De viktigaste principerna för Stock-statusrelationer är följande:

- När du ändrar **[!UICONTROL Stock Status]** av den konfigurerbara produkten som `Out of Stock` och klicka **[!UICONTROL Save]**, det är **_inte kontrollerad_** efter lagerstatus för sina underordnade produkter. Den visas alltid som `Out of Stock` i Admin och på Storefront.

- När du anger **[!UICONTROL Stock Status]** av den konfigurerbara produkten som `In Stock` och klicka **[!UICONTROL Save]**, det är **_endast delvis kontrollerad_** baserat på lagerstatus för dess underordnade produkter, som återspeglas i Admin och på Storefront.

### Detaljbeskrivning

The _Stock-status_ av den konfigurerbara produkten styrs delvis av Stock-statusen för dess underordnade produkter och enligt följande **_multivillkor_** beräkning av lagerstatus:

#### Endast med standardkälla/standardlager:

- Om den konfigurerbara produktStock-statusen är **_manuellt_** ange till `Out of Stock` av en administratörsanvändare, filimport eller API-anrop kvarstår som `Out of Stock` på båda **_Administratör_** och **_Storefront_** tills det är  **_manuellt_** ändrat till `In stock` av en administratörsanvändare, filimport eller API-anrop. Den kan inte styras av lagerstatusen för dess underordnade produkter.

- Om den konfigurerbara produktStock-statusen är **_manuellt_** ange till `In Stock` av en administratörsanvändare, filimport eller API-anrop, är dess arkivstatus **_automatiskt_** kontrolleras av Stock-statusen för dess underordnade produkter på båda **_Administratör_** och **_Storefront_**.

>[!NOTE]
>
>Anpassade lager och källor ingår i [Inventory management](../inventory-management/sources-stocks.md) och vi rekommenderar att du använder verktyget exklusivt för att hantera lager och källfiler. Standardfunktionerna för källa och lager är en del av `CatalogInventory` som nu är inaktuellt.

#### Med minst en anpassad källa/aktie:

- Om det konfigurerbara värdet för produktStock-status är **_manuellt_** ange till `Out of Stock` av en administratörsanvändare, filimport eller API-anrop kvarstår som `Out of Stock` på båda **_Administratör_** och **_Storefront_** tills det är **_manuellt_** ändrat till `In Stock` av en administratörsanvändare, filimport eller API-anrop. Den **_inte_** kontrolleras med avseende på deras underordnade produkters Stock-status.

- Om det konfigurerbara värdet för produktStock-status är **_manuellt_** ange till `In Stock` av en administratörsanvändare, filimport eller API-anrop, är dess arkivstatus **_automatiskt_** styrs av Stock-status för dess underordnade produkter på **_Storefront_** endast.

- Om det konfigurerbara värdet för produktStock-status är **_manuellt_** ange till `In Stock` av en administratörsanvändare, filimport eller API-anrop kvarstår som `In Stock` i **_Administratör_** tills det är **_manuellt_** ändrat till `Out of Stock` av en administratörsanvändare, filimport eller API-anrop. Den **_inte_** kontrolleras med avseende på deras underordnade produkters Stock-status.

## Saker att komma ihåg

- En konfigurerbar produkt låter kunden välja mellan olika indatatyper: listrutor, flera markeringar, visuella färgrutor och textrutor. Varje alternativ är en separat, enkel produkt.

- [Stock-status](../inventory-management/sources-stocks.md) för en konfigurerbar produkt är en inställning som styrs halvmanuellt. Den skiljer sig från den enkla produktens lagerstatus, där den utgör en direkt representation av produktens tillgänglighet. För en konfigurerbar produkt är lagerstatusen en del av en lagerstatusberäkning med flera kriterier.

- Konfigurerbara underordnade produkter kan vara enkla eller virtuella produkter **utan anpassade alternativ**. Om du vill göra anpassade underordnade produkter virtuella måste du välja `Тhis item has no weight` för **[!UICONTROL Weight]** för var och en av dem.

- En konfigurerbar produkt har inte ett eget pris i katalogen. Det konfigurerbara produktpriset härleds från dess [!UICONTROL In Stock] underordnade produkter.

- De attribut som används för produktvariationer måste ha ett globalt omfång och kunden måste vara skyldig att välja ett värde. Produktvariantattributen måste inkluderas i den attributuppsättning som används som mall för den konfigurerbara produkten.

- Attributuppsättningen som används som mall för en konfigurerbar produkt måste innehålla de attribut som innehåller de värden som behövs för varje produktvariation.

- Miniatyrbilden i kundvagnen kan ställas in så att bilden visas från den konfigurerbara produktposten eller från produktvariationen.

- [Attribut för färgrutor](swatches.md#create-swatches-for-products) kan konfigureras så att inte motsvarande enkla produktbilder visas när du väljer färgrutan genom att ställa in **[!UICONTROL Update Product Preview Image]** alternativvärde till `No` på sidan för redigering av attribut i Admin.

- Temat styr hur bildgalleriet fungerar när en användare växlar mellan produktkonfigurationer. Standardbeteendet för _Tom_ temat är att åsidosätta de överordnade konfigurerbara produktbilderna med den valda produktvarianten. För Luma-temat är standardbeteendet att lägga till de valda produktvariationsbilderna i de överordnade konfigurerbara produktbilderna.
