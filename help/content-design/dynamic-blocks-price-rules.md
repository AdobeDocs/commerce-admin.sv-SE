---
title: Dynamiska block i prisregler
description: Associera ett dynamiskt block med en kampanjprisregel.
exl-id: e1564df2-1c06-4d11-a32d-6f5c0be974e3
feature: Page Content, Price Rules
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Dynamiska block i prisregler

{{ee-feature}}

Alla [dynamiskt block](dynamic-blocks.md) som du skapar kan kopplas till en kampanj. Om du vill skapa associationen måste du först skapa både det dynamiska blocket och [katalogprisregel](../merchandising-promotions/price-rules-catalog.md) eller [kundprisregel](../merchandising-promotions/price-rules-cart.md). Kopplingen kan skapas när du arbetar med en prisregel eller när du arbetar med ett dynamiskt block.

>[!IMPORTANT]
>
>När du har skapat associationen visas det dynamiska blocket **endast** när regeln startar. Om kampanjen är avsedd för segment A visas blocket för segment A. Om erbjudandet inte är aktivt visas inte blocket.

## Associera ett dynamiskt block med en prisregel

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_och välj något av följande:

   - **[!UICONTROL Catalog Price Rules]**
   - **[!UICONTROL Cart Price Rules]**

1. Leta reda på regeln som du vill associera med det dynamiska blocket i stödrastret och öppna i redigeringsläge.

1. Rulla ned och expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Related Dynamic Blocks]**.

1. I den första kolumnen ställer du in filtret på `Any` och klicka **[!UICONTROL Reset Filter]**.

   Rutnätet visar nu alla tillgängliga dynamiska block.

1. Markera kryssrutan för varje dynamiskt block som du vill koppla till regeln.

   ![Lägga till markerade dynamiska block](./assets/price-rule-cart-related-dynamic-blocks-any.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save]**.

## Associera en prisregel med ett dynamiskt block

1. På _Administratör_ sidebar, gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. Hitta det dynamiska blocket i rutnätet och öppna i redigeringsläge.

1. Rulla ned och expandera **[!UICONTROL Related Promotions]**.

   Eventuella aktuella prisregler visas i rutnätet.

1. Lägg till en ny associerad regel eller ta bort en aktuell association.

   - Om du vill associera en kundvagnsbefordran klickar du på **[!UICONTROL Add Cart Price Rules]**.

   - Om du vill associera en produktrelaterad kampanj klickar du på **[!UICONTROL Add Catalog Price Rules]**.

1. Markera kryssrutan för varje regel som du vill koppla till det dynamiska blocket i rutnätet.

1. Klicka på **[!UICONTROL Add Selected]**.

   ![Lägga till valda prisregler i ett dynamiskt block](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save]**.
