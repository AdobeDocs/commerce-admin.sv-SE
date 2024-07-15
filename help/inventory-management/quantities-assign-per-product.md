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

När du har lagt till [källor](sources-assign-per-product.md) uppdaterar du lagerkvantiteterna för din produkt. Dessa värden spårar tillgängliga lagerbehållningsbelopp.

Om du vill dölja en källas lager från leveranser utan att ta bort källan anger du _[!UICONTROL Source Item Status]_till `Out of Stock`. SSA- och leveransalternativen har bara åtkomst till källor som listas som `In Stock` med tillgänglig lagerkvantitet.

Alla uppdaterade kvantiteter och källor visas i produktrutnätet.

## Uppdatera kvantiteter

1. Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]** på sidofältet _Admin_.

1. Leta upp och öppna en produkt i redigeringsläge.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Sources]**.

1. Ange **[!UICONTROL Source Item Status]** till `In Stock`.

1. Om du vill uppdatera kvantiteten för lagerbehållning anger du ett belopp för **[!UICONTROL Qty]**.

1. Gör något av följande om du vill ange ett meddelande för lagerkvantiteter:

   - Anpassad meddelandekvantitet - Avmarkera kryssrutan **[!UICONTROL Use Default]** och ange ett belopp i **[!UICONTROL Notify Qty]**.
   - Standardkvantitet för meddelande - Markera kryssrutan **[!UICONTROL Use Default]**. [!DNL Commerce] kontrollerar och använder inställningen i _[!UICONTROL Advanced Inventory]_eller den globala lagringskonfigurationen.

   ![Uppdatera produktkvantiteter per Source](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Spara genom att göra något av följande:

   - Klicka på **[!UICONTROL Save]**.

   - Välj **[!UICONTROL Save & Close]** på menyn **[!UICONTROL Save]** (![Menypil](../assets/icon-menu-down-arrow-red.png)).


Produktstödrastret uppdateras med en lista över alla källor och relaterade kvantiteter. För produkter med fler än fem tilldelade källor håller du pekaren över kolumnen _[!UICONTROL Quantity per Source]_för att se den fullständiga listan.

![Produktkvantiteter per källa](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
