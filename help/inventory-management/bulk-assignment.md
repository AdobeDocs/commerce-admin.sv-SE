---
title: Grupptilldelning av lagerkälla och avtilldelning
description: Lär dig hur du använder verktyget Tilldela källor för att hantera källtilldelningar för produkter.
exl-id: 1f1e81a5-fb06-46b7-84ca-7feea4942093
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# Grupptilldelning och borttagning av tilldelning av källa

Använd _Tilldela källor_ verktyg för att lägga till en eller flera källor till dina produkter. Verktyget är till hjälp när du skapar och tilldelar anpassade källor till ditt standardlager eller anpassade lager och förbereder nya platser och lager.

När du har lagt till nya anpassade källor kan du lägga till [lagerkvantiteter per produkt](quantities-assign-per-product.md) eller för flera produkter via administratören eller med [importfunktion](inventory-import-export.md).

![Lägg till lagerkällor för valda produkter](assets/inventory-bulk-assign-sources.gif)

## Tilldela källor och kvantiteter

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Välj de produkter som du vill ändra källorna för.

   Bläddra eller sök efter produkterna och markera kryssrutorna.

1. Klicka på **[!UICONTROL Actions]** överst och välj **[!UICONTROL Assign Inventory Source]**.

1. Klicka **[!UICONTROL OK]** i bekräftelsedialogrutan.

1. Markera kryssrutorna för alla källor som du vill lägga till i produkterna.

1. Klicka på **[!UICONTROL Assign Sources]**.

   ![Välj produkter för att lägga till källor](assets/inventory-bulk-assign-sources-summary.png){width="600" zoomable="yes"}

Källorna läggs till produkterna med lagerkvantiteten 0. Du kan lägga till [lagerkvantiteter](quantities-assign-per-product.md) per källa.

## Ta bort tilldelning av källor och kvantiteter

När du frigör en källa från en produkt anger du att produkten inte längre finns i lager på den platsen. Denna process rensar helt alla lagerdata för den källa som för närvarande är tilldelad produkten. Om du vill flytta det befintliga lagret till en ny plats bör du använda _Överför lager_ alternativ.

{{$include /help/_includes/unassign-source.md}}

Vi rekommenderar att du slutför alla beställningar och leveranser för dessa produkter innan du tar bort källan.

![Ta bort tilldelning av källor för valda produkter](assets/inventory-bulk-unassign-sources.gif)

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Välj de produkter som du vill ändra källor för.

   Bläddra eller sök efter produkterna och markera kryssrutorna.

1. Klicka på **[!UICONTROL Actions]** överst och välj **[!UICONTROL Unassign Inventory Source]**.

1. Klicka **[!UICONTROL OK]** i bekräftelsedialogrutan.

1. Välj den källa som du vill ta bort från produkterna.

   På sidan visas ett varningsmeddelande som tar bort tilldelning av alla specifika käll- och kvantitetsdata från produkten.

1. Klicka på **[!UICONTROL Unassign Sources]**.

   ![Ta bort källor från valda produkter](assets/inventory-bulk-unassign-sources-summary.png){width="600" zoomable="yes"}
