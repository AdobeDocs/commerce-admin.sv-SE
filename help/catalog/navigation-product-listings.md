---
title: Produktlistor
description: Lär dig hur du ändrar produktlistekonfigurationen, som avgör hur många produkter som visas per sida och vilket attribut som används för att sortera listan.
exl-id: 3779d9db-4adb-473b-b9c9-ad066f50b549
feature: Catalog Management, Products, Page Content
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Produktlistor

Produktlistor kan ställas in så att de visas som standard som antingen en lista eller ett rutnät. Du kan också bestämma hur många produkter som ska visas per sida och vilket attribut som ska användas för att sortera listan. Produktlistan innehåller en uppsättning kontroller som kan användas för att sortera produkterna, ändra listformatet, sortera efter attribut och gå från en sida till nästa.

>[!NOTE]
>
>När en kategori sorteras efter ett produktattribut sorteras produkter med samma attributvärden också efter deras _[!UICONTROL Product ID]_&#x200B;i stigande ordning.

![Produkter som visas som ett rutnät](./assets/storefront-catalog-page.png){width="700" zoomable="yes"}

## Konfigurera produktlistor

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Storefront]**.

   ![Konfigurationsalternativ för Storefront](../configuration-reference/catalog/assets/catalog-storefront.png){width="600" zoomable="yes"}

   En detaljerad lista över dessa alternativ finns i [Storefront](../configuration-reference/catalog/catalog.md#storefront) i _Konfigurationsreferens_.

   >[!NOTE]
   >
   >Om du vill visa produkter och deras priser på rätt sätt enligt _produktsortering efter pris_ kontrollerar du att inställningarna för prisvisningen i [Momskonfiguration](../configuration-reference/sales/tax.md) har samma värde (`Excluding Tax` **eller** `Including Tax`). Kontrollera värdet **[!UICONTROL Catalog Prices]** för _[!UICONTROL Calculation Settings]_. Och för&#x200B;_[!UICONTROL Price Display Settings]_, kontrollera värdet **[!UICONTROL Display Product Prices in Catalog]**. Om de har olika värden kan prisfiltren i lagernavigeringen eventuellt inte filtrera och sortera produkter efter pris.

1. Ange standardvärdet **[!UICONTROL List Mode]** till något av följande:

   - `Grid Only`
   - `List Only`
   - `Grid (default) / List`
   - `List (default / Grid`

1. För **[!UICONTROL Products per Page on Grid Allowed Values]** anger du antalet produkter som du vill ska visas per sida när den visas i stödrasterformat.

   Om du vill ange ett urval av värden avgränsar du varje tal med ett kommatecken.

1. För **[!UICONTROL Products per Page on Grid Default Value]** anger du standardantalet produkter som ska visas i rutnätet per sida.

1. För **[!UICONTROL Products per Page on List Allowed Values]** anger du antalet produkter som du vill ska visas per sida när de visas i listformat.

   Om du vill ange ett urval av värden avgränsar du varje tal med ett kommatecken.

1. För **[!UICONTROL Products per page on List Default Value]** anger du standardantalet produkter som visas i listan, per sida.

1. Ange **[!UICONTROL Product Listing Sorted by]** till standardattributet som ursprungligen används för att sortera listan.

1. Om du vill ge kunderna möjlighet att lista alla produkter anger du **[!UICONTROL Allow All Products on Page]** till `Yes`.

1. Om du vill behålla alla sidnumreringsinställningar när kunderna bläddrar genom kataloglistor anger du **[!UICONTROL Remember Category Pagination]** till `Yes`.

   Om du aktiverar den här inställningen behålls antalet produkter som visas i en lista eller rutnät när kunderna bläddrar från en kategori till en annan. Som standard är det här fältet inställt på `No` eftersom det använder mer cache-lagring och kan påverka hur sidor indexeras av sökmotorer.

1. Gör följande om du använder en [platt katalog](catalog-flat.md) (**rekommenderas inte**):

   - Om du vill visa en platt kategorilista med produkter anger du **[!UICONTROL Use Flat Catalog Category]** till `Yes`.

   - Om du vill visa en platt produktlista anger du **[!UICONTROL Use Flat Catalog Product]** till `Yes`.

1. Om du vill tillåta dynamiska referenser för medieresurser i kategori- och produkt-URL:er anger du **[!UICONTROL Allow Dynamic Media URLs in Products and Categories]** till `Yes`.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Sidkontroller

| Kontroll | Beskrivning |
|--- |--- |
| [!UICONTROL View As] | Visar produkterna i antingen rutnät- eller listformat. |
| [!UICONTROL Sort By] | Ändrar sorteringsordningen för listan. |
| [!UICONTROL Show Per Page] | Avgör hur många produkter som visas per sida. |
| Sidnumreringslänkar | Navigering länkar till andra sidor. |

{style="table-layout:auto"}

## Sidnumreringskontroller

Sidnumreringsinställningarna visas högst upp och längst ned i listan och styr formatet på sidnumreringslänkarna för produktlistor. Du kan ange antalet länkar som ska visas i kontrollen och konfigurera länkarna Nästa och Föregående. För att sidnumreringslänkarna ska visas måste det finnas fler produkter i listan än vad som tillåts per sida i produktlistkonfigurationen.

![Sidnumreringskontroller](./assets/storefront-pagination-controls.png){width="700" zoomable="yes"}

### Sidnumreringskontroller i Storefront

| Kontroll | Beskrivning |
|--- |--- |
| ![Visa stödraster](./assets/controls-pagination-list-grid.png) | [!UICONTROL View As] - Visar listan i antingen rutnät- eller listformat. |
| ![Sortera efter](./assets/control-pagination-sort-by.png) | [!UICONTROL Sort By] - Ändrar sorteringsordningen för listan. Egenskapen _[!UICONTROL Used for Sorting in Product Listing]_&#x200B;storefront avgör vilka [produktattribut](../catalog/product-attributes.md) som kan användas för att sortera listan. |
| ![Visa per sida](./assets/control-pagination-show-per-page.png) | [!UICONTROL Show Per Page] - Anger hur många produkter som visas per sida. |
| ![Sidnumreringslänkar](./assets/control-pagination.png) | Sidnumreringslänkar - Navigeringslänkar till andra sidor. |

{style="table-layout:auto"}

### Konfigurera sidnumreringskontrollerna

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Leta reda på den butiksvy som du vill konfigurera och klicka på **[!UICONTROL Edit]** i kolumnen **[!UICONTROL Action]**.

1. Under **[!UICONTROL Other Settings]** expanderar du ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Pagination]**.

   ![Sidnumrering](./assets/config-design-pagination.png){width="600" zoomable="yes"}

   Mer information om de här inställningarna finns i [Designkonfiguration](../content-design/configuration.md).

1. I **[!UICONTROL Pagination Frame]** anger du antalet länkar som du vill ska visas i sidnumreringskontrollen.

1. För **[!UICONTROL Pagination Frame Skip]** anger du antalet länkar som du vill hoppa över innan nästa uppsättning länkar visas i sidnumreringskontrollen.

   Om sidnumreringsramen t.ex. har fem länkar och du vill hoppa till de kommande fem länkarna, hur många länkar vill du hoppa över? Om du anger värdet till fyra (`4`) är den sista länken från föregående uppsättning den första länken i nästa uppsättning.

1. För **[!UICONTROL Anchor Text for Previous]** anger du den text som du vill ska visas för länken Föregående.

   Lämna tomt om du vill använda standardpilen.

1. För **[!UICONTROL Anchor Text for Next]** anger du den text som du vill ska visas för länken Nästa. Lämna tomt om du vill använda standardpilen.

1. Klicka på **[!UICONTROL Save Configuration]** när du är klar.
