---
title: Rotkategori och hierarki
description: Lär dig mer om kategorihierarkin och rotkategorin, som fungerar som behållare för huvudmenyn i kategoriträdet.
exl-id: b419cb45-4fe5-42c4-be20-667c7e1e4354
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# Rotkategori och hierarki

Produkterna på huvudmenyn avgörs av rotkategorin som är tilldelad till [store](../stores-purchase/stores.md#add-stores). Rotkategorin är i princip en behållare för huvudmenyn i kategoriträdet. Du kan skapa en rotkategori med en helt ny uppsättning produkter eller kopiera produkter från en befintlig rotkategori. Rotkategorin kan tilldelas den aktuella butiken eller en annan butik på samma webbplats.

![Kataloghierarkidiagram](./assets/catalog-hierarchy-scope.svg){width="550"}

Från Admin fungerar kategoristrukturen som ett upp-och-ned-träd med roten överst. Roten har ett namn, men ingen URL-nyckel, och visas inte i [navigering överst](navigation-top.md) i butiken. Alla andra kategorier på menyn är kapslade under roten. Eftersom rotkategorin är den högsta nivån i katalogen, kan det bara finnas en rotkategori i taget. Du kan dock skapa ytterligare rotkategorier för alternativa katalogstrukturer och olika arkiv.

I följande exempel visas hur du skapar en rotkategori och tilldelar den till en annan butik.

## Steg 1: Skapa en rotkategori

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Till vänster klickar du på **[!UICONTROL Add Root Category]**.

   ![Ny rotkategori](./assets/category-root-ee.png){width="600" zoomable="yes"}

1. Ange en **[!UICONTROL Category Name]**.

   Det namn du väljer tilldelas från början till alla butiksvyer.

1. Om du vill lägga till produkter i katalogen från den aktuella katalogen gör du följande:

   - Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den _Produkter i kategori_ -avsnitt.

   - Använd [sökfilter](../getting-started/admin-grid-controls.md) för att hitta de produkter du vill ha och markera kryssrutan för varje produkt som du vill kopiera till den nya katalogen.

1. När du är klar klickar du på **[!UICONTROL Save]**.

## Steg 2: Skapa huvudmenyn

1. Till vänster väljer du den nya rotkategorin som du skapade i föregående steg.

1. Skapa [kategoristruktur](category-create.md) för huvudmenyn klickar du på **[!UICONTROL Add Subcategory]** och följ instruktionerna.

## Steg 3: Tilldela rotkategorin till arkivet

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. I _Lager_ i rutnätskolumnen klickar du på den butik som du vill tilldela den nya katalogen.

1. Ange **[!UICONTROL Root Category]** till den nya rotkategorin som du skapade.

1. Se till att butiken har en **[!UICONTROL Default Store View]** tilldelad.

   Butiken måste ha minst en [butiksvy](../stores-purchase/store-views.md).

1. När du är klar klickar du på **[!UICONTROL Save Store]**.

1. Så här kontrollerar du att butiken har en ny katalog:

   - På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

     Alla produkter som kopierades till den nya katalogen visas i rutnätet.

   - Kontrollera att den nya katalogen och huvudmenyn fungerar som de ska genom att gå till butiken.
