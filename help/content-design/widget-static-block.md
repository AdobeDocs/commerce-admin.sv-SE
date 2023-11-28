---
title: Placera ett block med en widget
description: Lär dig hur du använder en statisk blockwidget för att placera ett befintligt innehåll nästan var som helst i din butik.
exl-id: 174deef2-33c4-4f1a-8ca8-4969be209bc7
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Placera ett block med en widget

The _Statiskt CMS-block_ [widget](widgets.md) ger dig möjlighet att placera ut en befintlig [innehållsblock](blocks.md) nästan var som helst i din butik.

![Widgetar](./assets/widgets.png){width="700" zoomable="yes"}

## Steg 1: Välj typ av widget

1. På _Administratör_ sidebar, gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicka på i det övre högra hörnet **[!UICONTROL Add Widget]**.

1. I _Inställningar_ avsnitt, ange **[!UICONTROL Type]** till `CMS Static Block` och klicka **[!UICONTROL Continue]**.

1. Verifiera att **[!UICONTROL Design Theme]** är inställt på det aktuella temat och klickar på **[!UICONTROL Continue]**.

   ![Widget-inställningar](./assets/widget-settings.png){width="600" zoomable="yes"}

1. I _[!UICONTROL Storefront Properties]_gör du följande:

   - För **[!UICONTROL Widget Title]** anger du en beskrivande titel för widgeten.

     Den här titeln visas bara från _Administratör_.

   - För **[!UICONTROL Assign to Store Views]** markerar du de butiksvyer där widgeten visas.

     Du kan välja en viss butiksvy eller `All Store Views`. Om du vill markera flera vyer håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

   - (valfritt) för **[!UICONTROL Sort Order]** anger du en siffra som bestämmer i vilken ordning det här objektet visas med andra på samma del av sidan. (`0` = first, `1` = sekund, `3` = tredje och så vidare.)

     ![Storefront-egenskaper](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

## Steg 2: Slutför uppdateringarna av widgetlayouten

1. I _[!UICONTROL Layout Updates]_avsnitt, klicka **[!UICONTROL Add Layout Update]**.

1. Ange **[!UICONTROL Display On]** till den kategori, produkt eller sida där du vill att blocket ska visas.

1. Så här placerar du blocket på en viss sida:

   - Välj **[!UICONTROL Page]** där du vill att blocket ska visas.

   - Välj **[!UICONTROL Block Reference]** som identifierar platsen där blocket visas på sidan.

   - Acceptera standardinställningen för **[!UICONTROL Template]**, som är inställd på `CMS Static Block Default Template`.

     ![Layoutuppdateringar](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

### Uppdateringsalternativ för layout

| Fält | Beskrivning |
|--- |--- |
| **_[!UICONTROL Categories]_** |  |
| [!UICONTROL Anchor Categories] | Visar widgeten på sidan för ankarkategori.<br/>**[!UICONTROL Categories]**- Kategorier där ankaret visas. Alternativ: `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - Ställ in behållaren på den del av sidlayouten där du vill visa widgeten.<br/>**[!UICONTROL Template]**- Anger layoutens tema. |
| [!UICONTROL Non-Anchor Categories] | Visar widgeten på sidan som inte är ankarpunkt.<br/>**[!UICONTROL Categories]**- Kategorier där ankaret visas. Alternativ: `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - Ställ in behållaren på den del av sidlayouten där du vill visa widgeten.<br/>**[!UICONTROL Template]**- Anger layoutens tema. |
| **_[!UICONTROL Products]_** |  |
| Alla produkttyper | Visar widgeten antingen på en viss typ av produktsida eller på alla produktsidor. <br/>**[!UICONTROL Products]**- Produkter som widgeten visas för. Alternativ: `All` /` Specific Products`<br/>**[!UICONTROL Container]** - Ställ in behållaren på den del av sidlayouten där du vill visa widgeten.<br/>**[!UICONTROL Template]**- Anger layoutens tema. |
| **_[!UICONTROL Generic Pages]_** |  |
| [!UICONTROL All Pages] | Visar widgeten på alla sidor. <br/>**[!UICONTROL Container]**- Ställ in behållaren på den del av sidlayouten där du vill visa widgeten.<br/>**[!UICONTROL Template]** - Anger layoutens tema. |
| [!UICONTROL Specified Page] | Visar widgeten på en viss sida. Alternativ:<br/>**[!UICONTROL Page]**- Sidor som widgeten visas för.<br/>**[!UICONTROL Container]** - Ställ in behållaren på den del av sidlayouten där du vill visa widgeten.<br/>**Mall** - Anger layoutens tema. |
| [!UICONTROL Page Layouts] | Visar widgeten på sidor med en viss layout. <br/>**[!UICONTROL Page]**- Sidor som widgeten visas för.<br/>**[!UICONTROL Container]** - Ställ in behållaren på den del av sidlayouten där du vill visa widgeten.<br/>**[!UICONTROL Template]**- Anger layoutens tema. |

{style="table-layout:auto"}

## Steg 3: Placera blocket

1. I den vänstra panelen väljer du **[!UICONTROL Widget Options]**.

1. Klicka **[!UICONTROL Select Block…]** och välj det block som du vill montera i listan.

1. När du är klar klickar du på **[!UICONTROL Save]**.

   Appen visas nu i listan.

1. Följ instruktionerna högst upp på sidan för att uppdatera indexet och sidcachen när du uppmanas till detta.

1. Gå tillbaka till butiken för att bekräfta att blocket visas på rätt plats.

   Om du vill flytta blocket kan du öppna widgeten igen eller prova med en annan sida eller blockreferens.
