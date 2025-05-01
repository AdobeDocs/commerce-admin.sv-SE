---
title: Visual Merchandiser - översikt
description: Läs mer om Visual Merchandiser-verktygen som gör att du kan positionera produkter och avgöra vilka produkter som visas i kategorilistan.
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Visual Merchandiser

{{ee-feature}}

_Visual Merchandiser_ är en uppsättning avancerade verktyg som gör att du kan placera produkter och använda villkor som avgör vilka produkter som visas i kategorilistan. Resultatet kan vara ett dynamiskt urval produkter som justeras efter ändringar i katalogen. Du kan arbeta i _visuellt läge_, som visar varje produkt som en platta i ett rutnät, eller arbeta från en lista med produkter i kategorin. Samma verktyg är tillgängliga i varje läge och du kan använda knapparna i det övre högra hörnet för att växla mellan olika typer av visning.

![Kategoriprodukter i panelvyn](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## Öppna Visual Merchandiser

1. Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Categories]** på sidofältet _Admin_.

1. Gå igenom kategoriträdet och klicka på den kategori som du vill redigera.

1. Bläddra nedåt och utöka ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Products in Category]**.

1. Klicka på knappen _Visa som rutor_ ( ![Visa som rutor](../assets/icon-view-tiles.png) ) för att visa produkterna som ett rutnät.

1. Klicka på **[!UICONTROL Save Category]** när du är klar.

## Ändra en produkts position

1. Använd [sorteringsordningen](../catalog/navigation-product-listings.md) för att visa produkten som du vill flytta.

   - **Metod 1: Dra och släpp**

     Ta kontrollen _Dra_ (![Dra ikon](../assets/icon-move.png)) i det övre högra hörnet av produktrutan och släpp produkten på rätt plats. Antalet produkter justeras för att återspegla den nya positionen.

   - **Metod 2: Ange positionsvärde**

     Ange numret där du vill att produkten ska visas i _Positionskontrollen_ (![Positionsfältet](../assets/control-position.png)) på produktplattan. Ange `0` om du vill placera produkten överst i listan.

1. Klicka på **[!UICONTROL Save Category]** när du är klar.

>[!NOTE]
>
>I en rensad installation reserverar Adobe Commerce kategori-ID:t `2` för rotkatalogen för standardbutiken. Visual Merchandiser kan bara använda kategorier med ID-nummer `3` eller högre.

## Workspace

| Kontroll | Beskrivning |
|--- |--- |
| ![Ikon för visningslista](../assets/icon-view-list.png) | Visa som lista |
| ![Visa som plattor, ikon](../assets/icon-view-tiles.png) | Visa som rutor |
| ![Växla matchning efter regel - nej](../assets/toggle-no.png) | Matcha enligt regel - nej |
| ![Växla matchning efter regel - ja](../assets/toggle-yes.png) | Matcha enligt regel - ja |
| ![Ikonen Flytta](../assets/icon-move.png) | Dra |
| ![Positionskontrollen](../assets/control-position.png) | Position |
| ![Ta bort från kategoriikon](../assets/icon-delete-x.png) | Ta bort från kategori |
| ![Objekt per sidkontroll](../assets/control-items-per-page.png) | Visa per sida |
| ![Ändra sidvisning](../assets/control-page-display.png) | Gå till nästa/föregående |

{style="table-layout:auto"}
