---
title: Kontroller för administratörsstödraster
description: Lär dig hur du arbetar på administratörssidor som hanterar data för att visa en samling med poster i ett rutnät.
exl-id: a4a9531d-eb2f-41d6-bb36-dc6d8811ee95
source-git-commit: a3fb702d0b6e08c3aaaa0d6b5e07aa825026ef76
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# Kontroller för administratörsstödraster

Administratörssidor som hanterar data visar en samling med poster i ett rutnät. Kontrollerna högst upp i varje kolumn kan användas för att sortera data. Den aktuella sorteringsordningen anges med en stigande eller fallande pil i kolumnrubriken. Du kan ange vilka kolumner som ska visas i stödrastret och dra dem till olika positioner. Du kan också spara olika kolumnupplägg som vyer som kan användas senare. Kolumnen **[!UICONTROL Action]** visar åtgärder som kan tillämpas på en enskild post. Dessutom kan datum från den aktuella vyn med de flesta stödraster exporteras till en [CSV](../systems/data-csv.md) - eller XML-fil.

![Sidan Beställningar - stödrastervisning](./assets/admin-workspace-grid.png){width="700" zoomable="yes"}

## Sortera listan

1. Klicka på en kolumnrubrik.

   Pilen anger att den aktuella ordningen är antingen stigande eller fallande.

1. Använd sidnumreringskontrollerna för att visa ytterligare sidor i samlingen.

   ![Stödrastervisning - sidkontroller](./assets/pagination-controls.png){width="300"}

## Sidindela listan

1. Ställ in kontrollen **[!UICONTROL Pagination]** på det antal poster som du vill visa per sida.

1. Klicka på **[!UICONTROL Next]** och **[!UICONTROL Previous]** om du vill bläddra igenom listan eller ange en specifik **[!UICONTROL Page Number]**.

## Filtrera listan

1. Klicka på **[!UICONTROL Filters]**.

1. Fyll i så många filter som behövs för att beskriva den post du vill hitta.

1. Klicka på **[!UICONTROL Apply Filters]**.

   ![Orderlista - filterkontroller](./assets/admin-workspace-filters.png){width="700" zoomable="yes"}

## Exportera data

1. Markera de poster som du vill exportera.

   >[!NOTE]
   >
   >Produktdata kan inte exporteras från rutnätet. Mer information finns i [Exportera](../systems/data-export.md).

1. Välj något av följande filformat på menyn _Exportera_ (![Menyväljare](../assets/icon-export.png)) i det övre högra hörnet:

   - `CSV`
   - `Excel XML`

   ![Listan Beställningar - exportalternativ](./assets/customers-grid-export.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Export]**.

1. Leta efter den hämtade filen med exporterade data på den plats som webbläsaren använder för nedladdning.

## Stödrasterlayout

Markeringen av kolumner och deras ordning i rutnätet kan ändras enligt dina önskemål och sparas som en _vy_. Du kan styra vilka attribut som visas i rutnätet under den enskilda attributkonfigurationen. Många attribut som visas i produktrutnätet kan påverka administratörens inläsningstid och prestanda.

![Ordna kolumner för stödraster](./assets/admin-grid-columns.png){width="700" zoomable="yes"}

### Ändra markeringen av kolumner

1. Klicka på kontrollen _Kolumner_ (![Kolumner-kontroll](../assets/icon-columns.png)) i det övre högra hörnet.

1. Ändra kolumnmarkeringar:

   - Markera kryssrutan för den kolumn som du vill lägga till i rutnätet.
   - Avmarkera kryssrutan för de kolumner som du vill ta bort från stödrastret.
   - Om du vill returnera standardstödrastervyn klickar du på **[!UICONTROL Reset]**.

Se till att rulla nedåt för att se alla tillgängliga kolumner.

### Flytta en kolumn

1. Klicka på kolumnrubriken och håll ned.

1. Dra kolumnen till den nya positionen och släpp den.

### Spara en stödrastervy

1. Klicka på kontrollen _Visa_ (![Visa kontroll](../assets/icon-view-eye.png)).

1. Klicka på **[!UICONTROL Save Current View]**.

1. Ange **[!UICONTROL name]** som vy.

1. Om du vill spara alla ändringar klickar du på _pilen_ (![Spara alla ändringar](../assets/icon-arrow-save.png)).

   Namnet på vyn visas nu som den aktuella vyn.

### Ändra stödrastervyn

1. Klicka på kontrollen _Visa_ (![Visa ikon](../assets/icon-view-eye.png)).

1. Gör något av följande:

   - Om du vill använda en annan vy klickar du på vyns namn.
   - Om du vill ändra namnet på en vy klickar du på ikonen _Redigera_ (![Redigera ikon](../assets/icon-edit-pencil.png)) och uppdaterar namnet.
   - Om du vill ta bort en vy klickar du på ikonen _Redigera_ (![Redigera ](../assets/icon-edit-pencil.png)) och sedan på ikonen _Ta bort_ (![Ta bort](../assets/icon-delete-trashcan-solid.png)).
