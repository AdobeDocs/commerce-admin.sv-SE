---
title: Tilldela lagerkällor per produkt
description: Lär dig hur du tilldelar en lagerkälla till en produkt.
exl-id: 7e47be25-633e-4f5d-bb61-0d9e79b6dbad
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# Tilldela källor per produkt

Innan du ändrar kvantiteter och inställningar måste du tilldela [källor](sources-manage.md) till produkterna.

{{$include /help/_includes/unassign-source.md}}

## Tilldela källor till en produkt

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Öppna en produkt i _Redigera_ läge.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Sources]** -avsnitt.

   I det här avsnittet kan du ändra källan, uppdatera lagerkvantiteter och mycket mer.

   >[!NOTE]
   >
   >För närvarande stöder endast enkla, konfigurerbara, virtuella, nedladdningsbara och grupperade produkter flera källor. Paketprodukter kan skapas och hanteras med enbart standardkällan och Stock.

   ![Avsnittet Produktkällor](assets/inventory-product-sources-before.png){width="600" zoomable="yes"}

1. Om du vill lägga till en källa klickar du **[!UICONTROL Assign Sources]**.

1. På _[!UICONTROL Assign Sources]_markerar du kryssrutan bredvid varje källa som du vill tilldela produkten.

   ![Produkt - tilldela källor](assets/inventory-product-assign-sources.png){width="600" zoomable="yes"}

1. Klicka **[!UICONTROL Done]** för att lägga till källorna.

1. Spara genom att göra något av följande:

   - Klicka på **[!UICONTROL Save]**.
   - På _[!UICONTROL Save]_ (![menypil](../assets/icon-menu-down-arrow-red.png)) väljer du **[!UICONTROL Save & Close]**.

När du har tilldelat källor uppdaterar du [lagerkvantitet](quantities-assign-per-product.md) för varje produktkälla.
