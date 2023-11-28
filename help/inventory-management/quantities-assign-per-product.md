---
title: Tilldela lagerkvantiteter per produkt
description: Lär dig hur du uppdaterar lagerkvantiteter för din produkt och spårar tillgängliga lagerbelopp.
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Tilldela kvantiteter per produkt

Efter tillägg [källor](sources-assign-per-product.md), uppdaterar lagerkvantiteterna för din produkt. Dessa värden spårar tillgängliga lagerbehållningsbelopp.

Om du vill dölja en källas lager från leveranser utan att ta bort källan anger du _[!UICONTROL Source Item Status]_till `Out of Stock`. SSA- och leveransalternativen har endast åtkomst till källor som listas som `In Stock` med tillgänglig lagerkvantitet.

Alla uppdaterade kvantiteter och källor visas i produktrutnätet.

## Uppdatera kvantiteter

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Leta upp och öppna en produkt i redigeringsläge.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Sources]** -avsnitt.

1. Ange **[!UICONTROL Source Item Status]** till `In Stock`.

1. om du vill uppdatera lagerbehållningen anger du ett belopp för **[!UICONTROL Qty]**.

1. Gör något av följande om du vill ange ett meddelande för lagerkvantiteter:

   - Anpassad meddelandekvantitet - Avmarkera alternativet **[!UICONTROL Use Default]** kryssrutan och ange ett belopp i **[!UICONTROL Notify Qty]**.
   - Standardkvantitet för meddelanden - Välj **[!UICONTROL Use Default]** kryssrutan. [!DNL Commerce] kontrollerar och använder inställningen i _[!UICONTROL Advanced Inventory]_eller global lagringskonfiguration.

   ![Uppdatera produktkvantiteter per källa](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Spara genom att göra något av följande:

   - Klicka på **[!UICONTROL Save]**.

   - På **[!UICONTROL Save]** (![Menypil](../assets/icon-menu-down-arrow-red.png)) väljer du **[!UICONTROL Save & Close]**.


Produktstödrastret uppdateras med en lista över alla källor och relaterade kvantiteter. För produkter med fler än fem tilldelade källor håller du muspekaren över _[!UICONTROL Quantity per Source]_för att se hela listan.

![Produktkvantiteter per källa](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
