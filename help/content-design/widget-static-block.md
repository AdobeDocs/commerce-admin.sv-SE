---
title: Placera ett block med en widget
description: Lär dig hur du använder en statisk blockwidget för att placera ett befintligt innehåll nästan var som helst i din butik.
exl-id: 174deef2-33c4-4f1a-8ca8-4969be209bc7
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# Placera ett block med en widget

Med _CMS Static Block_ [widget](widgets.md) kan du placera ett befintligt [innehållsblock](blocks.md) nästan var som helst i din butik.

![Widgets](./assets/widgets.png){width="700" zoomable="yes"}

## Steg 1: Välj typ av widget

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add Widget]** i det övre högra hörnet.

1. I avsnittet _Inställningar_ anger du **[!UICONTROL Type]** till `CMS Static Block` och klickar på **[!UICONTROL Continue]**.

1. Kontrollera att **[!UICONTROL Design Theme]** är inställt på det aktuella temat och klicka på **[!UICONTROL Continue]**.

   ![Widget-inställningar](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Gör följande i avsnittet _[!UICONTROL Storefront Properties]_:

   - För **[!UICONTROL Widget Title]** anger du en beskrivande titel för widgeten.

     Den här titeln visas bara från _Admin_.

   - För **[!UICONTROL Assign to Store Views]** väljer du de butiksvyer där widgeten visas.

     Du kan välja en viss butiksvy eller `All Store Views`. Om du vill markera flera vyer håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

   - (Valfritt) Ange ett nummer för **[!UICONTROL Sort Order]** för att avgöra i vilken ordning det här objektet visas med andra på samma del av sidan. (`0` = först, `1` = sekund, `3` = tredje o.s.v.)

     ![Storefront-egenskaper](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

## Steg 2: Slutför uppdateringarna av widgetlayouten

1. Klicka på **[!UICONTROL Add Layout Update]** i avsnittet _[!UICONTROL Layout Updates]_.

1. Ange **[!UICONTROL Display On]** till den kategori, produkt eller sida där du vill att blocket ska visas.

1. Så här placerar du blocket på en viss sida:

   - Välj den **[!UICONTROL Page]** där du vill att blocket ska visas.

   - Välj den **[!UICONTROL Block Reference]** som identifierar platsen där blocket visas på sidan.

   - Acceptera standardinställningen för **[!UICONTROL Template]**, som är inställd på `CMS Static Block Default Template`.

     ![Layoutuppdateringar](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

### Uppdateringsalternativ för layout

| Fält | Beskrivning |
|--- |--- |
| **_[!UICONTROL Categories]_** |  |
| [!UICONTROL Anchor Categories] | Visar widgeten på sidan för ankarkategori.<br/>**[!UICONTROL Categories]**- Kategorier där ankaret visas. Alternativ: `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - Ange behållaren för den del av sidlayouten där du vill visa widgeten.<br/>**[!UICONTROL Template]**- Bestämmer temat för layouten. |
| [!UICONTROL Non-Anchor Categories] | Visar widgeten på sidan som inte är ankarpunkt.<br/>**[!UICONTROL Categories]**- Kategorier där ankaret visas. Alternativ: `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - Ange behållaren för den del av sidlayouten där du vill visa widgeten.<br/>**[!UICONTROL Template]**- Bestämmer temat för layouten. |
| **_[!UICONTROL Products]_** |  |
| Alla produkttyper | Visar widgeten antingen på en viss typ av produktsida eller på alla produktsidor. <br/>**[!UICONTROL Products]**- Produkter som widgeten visas för. Alternativ: `All` /` Specific Products`<br/>**[!UICONTROL Container]** - Ange behållaren för den del av sidlayouten där du vill visa widgeten.<br/>**[!UICONTROL Template]**- Bestämmer temat för layouten. |
| **_[!UICONTROL Generic Pages]_** |  |
| [!UICONTROL All Pages] | Visar widgeten på alla sidor. <br/>**[!UICONTROL Container]**- Ställ in behållaren på den del av sidlayouten där du vill visa widgeten.<br/>**[!UICONTROL Template]** - Bestämmer temat för layouten. |
| [!UICONTROL Specified Page] | Visar widgeten på en viss sida. Alternativ:<br/>**[!UICONTROL Page]**- Sidor som widgeten visas för.<br/>**[!UICONTROL Container]** - Ställ in behållaren på den del av sidlayouten där du vill visa widgeten.<br/>**Mall** - Anger layoutens tema. |
| [!UICONTROL Page Layouts] | Visar widgeten på sidor med en viss layout. <br/>**[!UICONTROL Page]**- Sidor som widgeten visas för.<br/>**[!UICONTROL Container]** - Ställ in behållaren på den del av sidlayouten där du vill visa widgeten.<br/>**[!UICONTROL Template]**- Bestämmer temat för layouten. |

{style="table-layout:auto"}

## Steg 3: Placera blocket

1. Välj **[!UICONTROL Widget Options]** i den vänstra panelen.

1. Klicka på **[!UICONTROL Select Block…]** och välj det block som du vill montera i listan.

1. Klicka på **[!UICONTROL Save]** när du är klar.

   Appen visas nu i listan.

1. Följ instruktionerna högst upp på sidan för att uppdatera indexet och sidcachen när du uppmanas till detta.

1. Gå tillbaka till butiken för att bekräfta att blocket visas på rätt plats.

   Om du vill flytta blocket kan du öppna widgeten igen eller prova med en annan sida eller blockreferens.
