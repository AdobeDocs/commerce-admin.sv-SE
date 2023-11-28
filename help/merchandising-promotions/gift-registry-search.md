---
title: Lägg till sökning i presentregistret
description: Lär dig hur du placerar en sökruta i presentregistret för att hjälpa besökare att köpa produkter från kundregister.
exl-id: 8c5558d6-3641-4769-987e-8b217603d9fc
feature: Gift, Storefront, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# Lägg till sökning i presentregistret

{{ee-feature}}

The [Widget](../content-design/widgets.md) kan du använda för att placera en sökruta i presentregistret var som helst i din butik. Du kan ange vilka sökalternativ som ska vara tillgängliga för kunder, till exempel namn, e-postadress och presentregister-ID. När kunden klickar på knappen Sök visas resultatet på söksidan i presentregistret. Om sökningen inte ger några resultat kan kunden försöka igen med andra parametrar.

![Exempel på storefront - sökning i presentregistret](./assets/storefront-gift-registry-search.png){width="700" zoomable="yes"}

## Konfigurera sökning i presentregistret

1. På _Administratör_ sidebar, gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicka på i det övre högra hörnet **[!UICONTROL Add Widget]**.

1. Välj **[!UICONTROL Settings]** och gör följande:

   - Ange **[!UICONTROL Type]** till `Gift Registry Search`.

   - Ange **[!UICONTROL Design Theme]** till temat som används av butiken.

   - Klicka på **[!UICONTROL Continue]**.

   ![Presentregister - sökinställningar](./assets/widget-gift-registry-search-settings.png){width="700" zoomable="yes"}

1. I _[!UICONTROL Storefront Properties]_gör du följande:

   - Ange en **[!UICONTROL Widget Title]** för intern referens.

   - Ange **[!UICONTROL Assign to Store Views]** till de butiksvyer där Gift Registry Search ska vara tillgängligt.

   - Ange **[!UICONTROL Sort Order]** för att bestämma i vilken ordning som sökblocket i presentregistret ska visas när det finns andra block tilldelade till samma plats på sidan.

   ![Presentregister - butiksegenskaper](./assets/widget-gift-registry-search-storefront-properties.png){width="700" zoomable="yes"}

1. I **[!UICONTROL Layout Updates]** avsnitt, klicka **[!UICONTROL Add Layout Update]**.

1. Så här avgör du var presentregistersökningen ska visas i arkivet:

   - Ange **[!UICONTROL Display On]** till de sidor i butiken där du vill att sökblocket i presentregistret ska visas.

   - Välj **[!UICONTROL Categories]** där du vill att den ska visas.

   - Ange **[!UICONTROL Container]** till den plats på sidan där sökblocket i presentregistret ska placeras.

   ![Presentregister - layoutuppdateringar](./assets/widget-gift-registry-search-layout-updates.png){width="500" zoomable="yes"}

1. Välj **[!UICONTROL Widget Options]**.

1. Om du vill se hur besökare på din webbplats kan söka efter presentregister väljer du så många av följande som gäller:

   - [!UICONTROL All Forms]
   - [!UICONTROL Registrant Name Search]
   - [!UICONTROL Registrant Email Search]
   - [!UICONTROL Gift Registry ID Search]

   ![Presentregister - widgetalternativ](./assets/widget-gift-registry-search-widget-options.png){width="700" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save]**.

1. När du uppmanas att uppdatera sidcachen klickar du på länken i meddelandet längst upp på arbetsytan och följer instruktionerna.

## Fältbeskrivningar

### [!UICONTROL Settings]

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Type] | Identifierar `Gift Registry Search` som typen av widget. |
| [!UICONTROL Design Theme] | Temat som används av arkivet där Presentregistersökningen ska visas. |

{style="table-layout:auto"}

### [!UICONTROL Storefront Properties]

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Widget Title] | Ett namn för intern referens. |
| [!UICONTROL Assign to Store Views] | Identifierar de butiksvyer där presentregistersökningen ska vara tillgänglig. |
| [!UICONTROL Sort Order] | Anger i vilken ordning Gift Registry Search-blocket ska visas om det finns andra block tilldelade till samma plats. |

{style="table-layout:auto"}

### [!UICONTROL Layout Updates]

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Display On] | Ange de sidor eller typer av sidor där sökblocket i presentregistret visas. |
| [!UICONTROL Categories] | Identifierar, om tillämpligt, kategorisidorna där Gift Registry Search visas. |
| [!UICONTROL Container] | Anger det sidlayoutblock där Gift Registry Search placeras. Alternativen varierar beroende på mall och tema. |

{style="table-layout:auto"}

### [!UICONTROL Widget Options]

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Quick Search Form Types] | Bestämmer vilka typer av sökningar som kan utföras med Gift Registry Search. Alternativ: `All Forms` / `Registrant Name Search` /` Registrant Email Search` / `Gift Registry ID Search` |

{style="table-layout:auto"}
