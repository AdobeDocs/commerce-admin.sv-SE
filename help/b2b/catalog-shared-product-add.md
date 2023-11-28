---
title: Lägga till produkter i en delad katalog
description: Lär dig hur du lägger till produkter i en delad katalog, antingen individuellt eller i grupper per kategori.
exl-id: c88b46b4-cea8-4f65-b7e4-6681bab64d41
feature: B2B, Companies, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Lägga till produkter i en delad katalog

Produkter kan läggas till i en delad katalog antingen individuellt eller i grupper med flera produkter per kategori.

Följande krav måste vara uppfyllda för att en komplex produkt (till exempel bundle, grouped eller configurable) ska vara synlig från butiken i en delad katalog:

- Alla [tillhörande produkter](../catalog/product-configurations.md) och alternativen måste tilldelas samma delade katalog och aktiveras i den primära katalogen.
- För [konfigurerbar](../catalog/product-create-configurable.md) och [grupperad](../catalog/product-create-grouped.md) -produkter visas bara de aktiverade tillhörande produkterna.
- För [paket](../catalog/product-create-bundle.md) måste alla alternativ inkluderas i den delade katalogen.

  ![Välj produkter för katalog](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## Metod 1: Lägg till en enskild produkt

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. För produkten i rutnätet som du vill lägga till går du till _[!UICONTROL Action]_kolumn och klicka **[!UICONTROL Edit]**.

1. Bläddra nedåt, expandera ![Expansionsväljare](../assets/icon-display-expand.png) den _[!UICONTROL Product in Shared Catalogs]_och gör följande:

   - Markera kryssrutan för varje delad katalog där produkten ska visas. Om du vill välja alla kataloger klickar du på **[!UICONTROL Select all]**.

     ![Produkt i delade kataloger](./assets/shared-catalog-assign-from-product.png){width="600" zoomable="yes"}

     Namnet på varje markerad katalog visas i dialogrutan _[!UICONTROL Shared Catalogs]_fält.

     ![Delade kataloger tilldelade](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

   - Klicka **[!UICONTROL Done]** för att spara inställningarna.

1. När du är klar klickar du på **[!UICONTROL Save]**.

## Metod 2: Lägg till flera produkter

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. För den delade katalogen i rutnätet går du till _[!UICONTROL Action]_kolumn och markera **[!UICONTROL Set Pricing and Structure]**.

1. Gör något av följande i kategoriträdet:

   - Om du vill inkludera alla produkter klickar du **[!UICONTROL Select all]** eller markera kryssrutan för den överordnade kategorin.
   - Om du vill ta med specifika produktkategorier markerar du kryssrutan för varje kategori som du vill ta med.
   - Om du vill inkludera eller exkludera en enskild produkt markerar eller avmarkerar du produktkryssrutan.

   Kommentaren under varje kategori i trädet visar antalet produkter i kategorin som för närvarande ingår i den delade katalogen. Kommentaren under [rotkategori](../catalog/category-root.md) visar det totala antalet produkter från alla kategorier som är markerade för den delade katalogen.

1. Om du vill visa kategoriprodukter i rutnätet klickar du på namnet på kategorin i trädet.

   När en kategori är markerad händer följande:

   - Växlingsknappen i stödrastrets första kolumn är inställd på `On` för varje vald produkt.
   - Om en produkt har tilldelats flera kategorier och utelämnats i någon av dem, är den tillgänglig genom de andra kategorierna och genom [katalogsökning](../catalog/search.md).
   - Systemet ställer in automatiskt [Kategoribehörigheter](../catalog/category-permissions.md) till `Allow` för de valda produkterna.
