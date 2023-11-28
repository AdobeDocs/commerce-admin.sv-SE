---
title: Lägga till ett roterande dynamiskt block
description: Visa ett bildspel med interaktivt innehåll på butiken genom att lägga till flera dynamiska block i en roterare.
exl-id: 3d338014-cf26-4171-b48b-d37b3d7b0e81
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 0%

---

# Lägga till ett roterande dynamiskt block

{{ee-feature}}

Om du vill visa ett bildspel med interaktivt innehåll kan du lägga till flera [dynamiska block](dynamic-blocks.md) till en rotator. The [widget](widgets.md) används för att placera roteraren på en viss plats på en sida eller på flera sidor i butiken.

![Dynamisk blockrotering](./assets/widget-dynamic-block-rotator.png){width="700" zoomable="yes"}

## Steg 1: Skapa enskilda dynamiska block

Till [skapa dynamiska block](dynamic-blocks.md) som du vill placera i rotatorn, följ dessa instruktioner:

## Steg 2: Lägg till en widget för dynamisk blockrotering

1. På _Administratör_ sidebar, gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicka på i det övre högra hörnet **[!UICONTROL Add Widget]**.

1. Under _Inställningar_, ange **[!UICONTROL Type]** till `Dynamic Blocks Rotator`.

1. Välj aktuell **[!UICONTROL Design Theme]** i butiken.

   Den här inställningen identifierar det aktuella paketet eller [tema](themes.md) som bestämmer butikens sidlayout.

1. Klicka på **[!UICONTROL Continue]**.

   ![Inställningar för dynamisk blockrotering](./assets/widget-dynamic-block-rotator-settings.png){width="600" zoomable="yes"}

## Steg 3: Slutför alternativen

1. Under _Egenskaper för Storefront_, ange alternativ:

   - Ange en **[!UICONTROL Title]** för rotatorn.

   - I **[!UICONTROL Assign to Store Views]** väljer du [butiksvyer](../getting-started/websites-stores-views.md) där rotatorn är tillgänglig.

   - (Valfritt) Ange en **[!UICONTROL Sort Order]** tal för att bestämma roterarens position i målbehållaren. Den är relativ till andra widgetar som kan tilldelas till samma behållare.

   ![Egenskaper för rotationsbutiker](./assets/widget-dynamic-block-rotator-storefront-properties.png){width="600" zoomable="yes"}

1. Under _Layoutalternativ_, klicka **[!UICONTROL Add Layout Update]** och gör följande:

   - Ange **[!UICONTROL Display on]** till den sida, eller den typ av sida, där roteraren ska visas.

      - `Categories` - Visar roteringen på endera [ankare](../catalog/navigation-layered.md) eller sidor utan ankarpunkt. Alternativ: Ankarkategorier / Kategorier utan ankarpunkt
      - `Products` - Visar roteraren på en viss typ av produktsida eller på alla produktsidor. Alternativ: Alla produkttyper / [Enkel produkt](../catalog/product-create-simple.md) /  [Virtuell produkt](../catalog/product-create-virtual.md) / [Paketprodukt](../catalog/product-create-bundle.md) / [Nedladdningsbar produkt](../catalog/product-create-downloadable.md) / [Presentkort](../catalog/product-gift-card-create.md) / [Konfigurerbar produkt](../catalog/product-create-configurable.md) / [Grupperad produkt](../catalog/product-create-grouped.md)
      - `Generic Pages` - Visar rotationen på alla sidor, på en viss sida eller endast på sidor med en viss layout. Alternativ: `All Pages` / `Specified Page` / `Page Layouts`

     I exemplet ska roteraren placeras på en `Specified Page`.

   - Välj den specifika **[!UICONTROL Page]** där rotatorn ska visas.

   - Ange **[!UICONTROL Container]** till den del av [sidlayout](page-layout.md#standard-page-layouts) där rotatorn ska visas.

     Om andra widgetar tilldelas till samma behållare visas de i sekvens enligt sorteringsordningen.

   - Acceptera `Dynamic Block Template` som standard **[!UICONTROL Template]**.

     Den här inställningen avgör vilken mall som används för att formatera roteraren, baserat på om roteraren ska vara fristående eller placeras inuti befintlig text.

     ![Uppdateringar av rotationslayout](./assets/widget-dynamic-block-rotator-layout-updates.png){width="600" zoomable="yes"}

   - Klicka på **[!UICONTROL Save and Continue Edit]**.

1. Välj **[!UICONTROL Widget Options]**.

1. För **[!UICONTROL Dynamic Blocks to Display]**, acceptera `Specified Dynamic Blocks`.

   Den här inställningen avgör vilken typ av dynamiska block som finns i rotatorn.

   - `Specified Dynamic Blocks` - Innehåller endast specifika dynamiska block.
   - `Cart Price Rule Related` - Inkluderar endast dynamiska block som är kopplade till en kundprisregel.
   - `Catalog Price Rule Related` - Inkluderar endast dynamiska block som är kopplade till en katalogprisregel.

1. Till **[!UICONTROL Restrict the Dynamic Block Types]** som kan användas med widgeten väljer du `Content Area`.

   Den här inställningen begränsar banderollen till en viss del av sidlayouten.

   - `Content Area` - Placerar det dynamiska blocket i sidans huvudinnehållsområde.
   - `Footer` - Placerar det dynamiska blocket i sidfoten.
   - `Header` - Placerar det dynamiska blocket i sidhuvudet.
   - `Left Column` - Placerar det dynamiska blocket i den vänstra kolumnen i sidlayouten, om det är tillgängligt.
   - `Right Column` - Placerar det dynamiska blocket i den högra kolumnen i sidlayouten, om det är tillgängligt.

1. Ange **[!UICONTROL Rotation Mode]** till något av följande:

   - `Display all instead of rotating` - Visar en stapel med dynamiska block, där alla är synliga.
   - `One at a time, Random` - Visar de angivna dynamiska blocken i slumpmässig ordning. När sidan uppdateras visas ett annat (och slumpmässigt) dynamiskt block.
   - `One at the time, Series` - Visar de angivna dynamiska blocken i den sekvens som de lades till. När sidan uppdateras visas nästa dynamiska block i sekvensen.
   - `One at the time, Shuffle` - Visar ett dynamiskt block i taget i blandad ordning. Det här alternativet liknar `One at a time, Random` förutom att samma dynamiska block inte upprepas.

     ![Alternativ för rotationswidget](./assets/widget-dynamic-block-rotator-widget-options.png){width="600" zoomable="yes"}

1. I **[!UICONTROL Specify Dynamic Blocks]** markerar du kryssrutan för varje dynamiskt block som du vill ta med i rotatorn.

1. När du är klar klickar du på **[!UICONTROL Save]**.
