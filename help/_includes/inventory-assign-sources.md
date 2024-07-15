---
title: Lager - tilldela källor och kvantiteter
description: Återanvänt avsnitt om tilldelning av källor och kvantiteter när katalogprodukter skapas.
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# Lager - tilldela källor och kvantiteter

Om du använder [[!DNL Inventory Management]](../inventory-management/introduction.md) för flera källor rullar du nedåt till avsnittet **Källor** och tilldelar källor och kvantiteter:

1. Klicka på **[!UICONTROL Assign Sources]** om du vill lägga till en källa.

1. Bläddra bland eller sök efter källor och markera kryssrutan bredvid de källor som du vill lägga till för produkten.

   ![Tilldela källor till produkten](../catalog/assets/inventory-product-assign-sources.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Done]** för att lägga till källorna.

1. Om du vill hantera källans kvantitet och status klickar du på **[!UICONTROL Advanced Inventory]** och anger **[!UICONTROL Manage Stock]** till `Yes`.

1. Ange **[!UICONTROL Source Item Status]** till `In Stock`.

1. Ange en beloppsuppdatering av **[!UICONTROL Qty]** för lagerbehållning.

1. Gör något av följande om du vill ange ett meddelande för lagerkvantiteter:

   - _Anpassad meddelandekvantitet_ - Avmarkera kryssrutan **[!UICONTROL Notify Quantity Use Default]** och ange ett belopp i **[!UICONTROL Notify Quantity]**.

   - _Standardkvantitet för meddelande_ - Markera kryssrutan **[!UICONTROL Notify Quantity Use Default]**. Commerce kontrollerar och använder inställningen i [!UICONTROL Advanced Inventory] eller den globala lagringskonfigurationen.

   ![Uppdatera produktkvantiteter per Source](../catalog/assets/inventory-product-quantity.png){width="600" zoomable="yes"}
