---
title: Grupperad produkt
description: Lär dig skapa en grupperad produkt som består av enkla fristående produkter som presenteras som en grupp.
exl-id: af42b7fc-27f2-4c5a-b504-a70a324fae76
feature: Catalog Management, Products
source-git-commit: 140930df515d1e0604b18a4ebf689254b9487b53
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 0%

---

# Grupperad produkt

En grupperad produkt består av enkla fristående produkter som presenteras som en grupp. Du kan erbjuda varianter av en enskild produkt eller gruppera dem efter årstid eller tema. Att presentera en grupperad produkt kan vara ett incitament för kunderna att köpa ytterligare artiklar. En grupperad produkt är ett enkelt sätt att erbjuda olika varianter av en produkt och visa alla på samma sida.

Du kan till exempel sälja öppna lageruppbyggda program och lista alla typer av utskrifter som används på en formell plats. Vissa kan beställa flera salladsgafflar, fiskgafflar, middagsknivar, fiskknivar, smörknivar, soppskedar och dessertskedar. Andra kunder kan beställa en enkel gaffel, kniv och sked. Kunderna kan beställa valfritt antal av varje artikel som de vill.

Även om de presenteras som en grupp, köps varje produkt i gruppen som en separat artikel. I kundvagnen visas varje artikel och inköpskvantiteten som en separat radartikel.

I följande instruktioner visas hur du skapar en grupperad produkt med en [produktmall](attribute-sets.md), obligatoriska fält och grundläggande inställningar. Varje obligatoriskt fält markeras med en röd asterisk (`*`). När du är klar med grunderna kan du slutföra de andra produktinställningarna efter behov.

![Grupperad produkt](./assets/product-grouped.png){width="700" zoomable="yes"}

## Steg 1: Välj produkttyp

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. På _[!UICONTROL Add Product]_( ![Menypil](../assets/icon-menu-down-arrow-red.png){width="25"} ) i det övre högra hörnet väljer du **[!UICONTROL Grouped Product]**.

   ![Lägg till grupperad produkt](./assets/product-add-grouped.png){width="700" zoomable="yes"}

## Steg 2: Välj attributuppsättning

Välj [attributuppsättning](attribute-sets.md) som används som mall för produkten gör du något av följande:

- Om du vill söka anger du namnet på **[!UICONTROL Attribute Set]**.
- I listan väljer du den attributuppsättning som du vill använda.

Formuläret uppdateras för att återspegla ändringen.

![Välj mall](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

Om de attribut som behövs inte finns kan du lägga till nya attribut när du skapar en produkt:

- Klicka på i det övre högra hörnet **[!UICONTROL Add Attribute]**.
- Definiera ett nytt attribut (se [Lägga till ett attribut i en produkt](product-attributes-add.md)).

  ![Nytt attribut](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

Använd alternativet [filterkontroller](../getting-started/admin-grid-controls.md) om du vill hitta attributet i rutnätet och göra följande:

- Markera kryssrutan i den första kolumnen i varje attribut som ska läggas till.
- Klicka på **[!UICONTROL Add Selected]**.

## Steg 3: Slutför de obligatoriska inställningarna

1. Ange **[!UICONTROL Product Name]**.

1. Acceptera standardinställningen **[!UICONTROL SKU]** som baseras på produktnamnet eller anger ett annat.

   Observera att **[!UICONTROL Quantity]** fältet är inte tillgängligt eftersom värdet härleds från de enskilda produkter som utgör gruppen.

   En grupperad produkt har inte ett eget pris i katalogen. Det grupperade produktpriset härleds från priset för de enskilda produkter som ingår i gruppen.

1. Eftersom produkten ännu inte är klar att publiceras kan du ange **[!UICONTROL Enable Product]** till `No` ( ![Växla inte](../assets/toggle-no.png) ).

1. Klicka **[!UICONTROL Save]** och fortsätta.

   När produkten sparas visas produktnamnet högst upp på sidan och [Butiksvy](introduction.md#product-scope) Väljaren visas i det övre vänstra hörnet.

1. Välj **[!UICONTROL Store View]** där produkten ska finnas tillgänglig.

   ![Välj butiksvy](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Steg 4: Slutför de grundläggande inställningarna

1. Acceptera **[!UICONTROL Stock Status]** inställning för `In Stock`.

1. Tilldela **[!UICONTROL Categories]** till produkten klickar du på **[!UICONTROL Select…]** och gör något av följande:

   **Välj en befintlig kategori:**

   - Börja skriva i rutan tills du hittar en matchning.

   - Markera kryssrutan för den kategori som ska tilldelas.

   **Skapa en kategori:**

   - Klicka på **[!UICONTROL New Category]**.

   - Ange **[!UICONTROL Category Name]** och väljer **[!UICONTROL Parent Category]** som bestämmer dess placering i menystrukturen.

   - Klicka på **[!UICONTROL Create Category]**.

1. Acceptera **[!UICONTROL Visibility]** inställningar för `Catalog, Search`.

1. Så här fungerar produkten i [lista över nya produkter](../content-design/widget-new-products-list.md)väljer du **[!UICONTROL Set Product as New]** **[!UICONTROL from]** och **[!UICONTROL to]** datum i kalendern.

1. Välj **[!UICONTROL Country of Manufacture]**.

   Det kan finnas ytterligare enskilda attribut som beskriver produkten. Markeringen varierar attributuppsättningen och du kan slutföra dem senare.

## Steg 5: Lägg till produkter i gruppen

1. Bläddra nedåt till **[!UICONTROL Grouped Products]** och klicka **[!UICONTROL Add Products to Group]**.

   ![Grupperade produkter](./assets/product-grouped-products.png){width="600" zoomable="yes"}

1. Om det behövs kan du använda [filter](../getting-started/admin-grid-controls.md) för att hitta de produkter som du vill inkludera i gruppen.

1. Markera kryssrutan för varje objekt som du vill ta med i gruppen i listan.

   >[!NOTE]
   >
   >Endast enkla, nedladdningsbara och virtuella produkter utan konfigurerbara alternativ kan grupperas i underordnade produkter. Andra produkttyper visas inte i urvalslistan.

   ![Lägg till valda produkter](./assets/product-grouped-add-products.png){width="600" zoomable="yes"}

1. Om du vill lägga till dem i produktgruppen klickar du på **[!UICONTROL Add Selected Products]**.

   De valda produkterna visas i _[!UICONTROL Grouped Products]_-avsnitt.

   För flerkällshandel med [Inventory management](../inventory-management/sources-stocks.md), innehåller rutnätet en **[!UICONTROL Quantity per Source]** kolumn med varje tilldelat käll- och lagerbelopp.

   ![Produkter i grupp](./assets/product-grouped-grouped-products-section.png){width="600" zoomable="yes"}

1. Ange en **[!UICONTROL Default Quantity]** för något av objekten.

1. Om du vill ändra ordningen på produkterna klickar du på _Ändra ordning_ ikon ( ![Positionskontroll](../assets/icon-sort-order.png) ) i den första kolumnen och dra produkten till den nya positionen i listan.

1. Om du vill ta bort en produkt från gruppen klickar du **[!UICONTROL Remove]**.

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

## Steg 6: Publicera produkten

1. Om du är redo att publicera produkten i katalogen anger du **[!UICONTROL Enable Product]** till `Yes`.

1. Gör något av följande:

   **Metod 1:** Spara och förhandsgranska

   - Klicka på i det övre högra hörnet **[!UICONTROL Save]**.

   - Om du vill visa produkten i din butik väljer du **[!UICONTROL Customer View]** på _Administratör_ ( ![Menypil](../assets/icon-menu-down-arrow-black.png) ).

     Butiken öppnas på en ny flik i webbläsaren.

     ![Kundvy](./assets/product-admin-customer-view.png){width="700" zoomable="yes"}

   **Metod 2:** Spara och stäng

   - På _[!UICONTROL Save]_( ![Menypil](../assets/icon-menu-down-arrow-red.png){width="25"} ) väljer du **[!UICONTROL Save & Close]**.

## Steg 7: Konfigurera kundvagnsminiatyrerna (valfritt)

Om du har en annan bild för varje produkt i gruppen kan du ställa in konfigurationen så att rätt bild används för kundvagnsminiatyrbilden.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Checkout]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Shopping Cart]**.

   En detaljerad lista över dessa konfigurationsalternativ finns i [Kundvagn](../configuration-reference/sales/checkout.md#shopping-cart) i _Konfigurationsreferens_.

1. Ange **[!UICONTROL Grouped Product Image]** till `Product Thumbnail Itself`.

   ![Kundvagn](./assets/config-sales-cart-grouped-product.png){width="600" zoomable="yes"}

   Avmarkera vid behov **[!UICONTROL Use system value]** om du vill ange det här alternativet.

1. Klicka på **[!UICONTROL Save Config]**.

## Saker att komma ihåg

- En grupperad produkt är en samling enkla tillhörande produkter.

- Grupperade underordnade produkter kan vara enkla, nedladdningsbara eller virtuella produkter **[!UICONTROL without custom options]**.

- Varje inköpt artikel visas separat i kundvagnen i stället för som en del av gruppen.

- En grupperad produkt har inte ett eget pris i katalogen. Det grupperade produktpriset härleds från priset för de enskilda produkter som ingår i gruppen.

- Miniatyrbilden i kundvagnen kan ställas in så att den visar bilden från den grupperade överordnade produkten eller tillhörande produkt.
