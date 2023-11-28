---
title: Visual Merchandiser - översikt
description: Läs mer om Visual Merchandiser-verktygen som gör att du kan positionera produkter och avgöra vilka produkter som visas i kategorilistan.
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Visual Merchandiser

{{ee-feature}}

The _Visual Merchandiser_ är en uppsättning avancerade verktyg som gör att du kan positionera produkter och använda villkor som bestämmer vilka produkter som visas i kategorilistan. Resultatet kan vara ett dynamiskt urval produkter som justeras efter ändringar i katalogen. Du kan arbeta i _visuellt läge_, som visar varje produkt som en platta i ett rutnät, eller att arbeta från en lista med produkter i kategorin. Samma verktyg är tillgängliga i varje läge och du kan använda knapparna i det övre högra hörnet för att växla mellan olika typer av visning.

![Kategoriprodukter i vyn Sida vid sida](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## Öppna Visual Merchandiser

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Gå igenom kategoriträdet och klicka på den kategori som du vill redigera.

1. Rulla ned och expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Products in Category]** -avsnitt.

1. Klicka på _Visa som rutor_ ( ![Visa som rutor](../assets/icon-view-tiles.png) ) för att visa produkterna som ett rutnät.

1. När du är klar klickar du på **[!UICONTROL Save Category]**.

## Ändra en produkts position

1. Använd [sorteringsordning](../catalog/navigation-product-listings.md) för att visa den produkt du vill flytta.

   - **Metod 1: Dra och släpp**

     Ta tag i _Dra_ (![Dra ikonen](../assets/icon-move.png)) i det övre högra hörnet av produktrutan och släpp produkten på rätt plats. Antalet produkter justeras för att återspegla den nya positionen.

   - **Metod 2: Ange positionsvärde**

     I _Position_ styrenhet (![Positionsfält](../assets/control-position.png)) på produktrutan anger du numret där du vill att produkten ska visas. Retur `0` om du vill placera produkten högst upp i listan.

1. När du är klar klickar du på **[!UICONTROL Save Category]**.

>[!NOTE]
>
>I en ren installation reserverar Adobe Commerce kategori-ID:t `2` för rotkatalogen för standardarkivet. Visual Merchandiser kan bara använda kategorier med ID-nummer `3` eller större.

## Arbetsytekontroller

| Kontroll | Beskrivning |
|--- |--- |
| ![Ikon för visningslista](../assets/icon-view-list.png) | Visa som lista |
| ![Visa som rutor, ikon](../assets/icon-view-tiles.png) | Visa som rutor |
| ![Matcha enligt regel - växla - nej](../assets/toggle-no.png) | Matcha enligt regel - nej |
| ![Matcha enligt regel - ja](../assets/toggle-yes.png) | Matcha enligt regel - ja |
| ![Ikonen Flytta](../assets/icon-move.png) | Dra |
| ![Positionskontroll](../assets/control-position.png) | Position |
| ![Ikonen Ta bort från kategori](../assets/icon-delete-x.png) | Ta bort från kategori |
| ![Objekt per sidkontroll](../assets/control-items-per-page.png) | Visa per sida |
| ![Ändra sidvisning](../assets/control-page-display.png) | Gå till nästa/föregående |

{style="table-layout:auto"}
