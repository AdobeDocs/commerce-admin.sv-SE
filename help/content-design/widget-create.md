---
title: Skapa och hantera widgetar
description: Lär dig hur du skapar och hanterar widgetar som automatiskt uppdaterar innehåll i din butik.
exl-id: 680f2f41-ec51-4ac6-9e92-2817591af3e6
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# Skapa och hantera widgetar

Widgetar är återanvändbara komponenter. Du kan enkelt skapa widgetar och ändra befintliga så att innehållet uppdateras automatiskt i hela butiken. Du kan också ta bort widgetar som inte längre används.

![Widgets](./assets/widgets.png){width="700" zoomable="yes"}

## Skapa en widget

Processen med att skapa en widget är nästan densamma för varje [widgettyp](widgets.md#widget-types). Du kan följa den första delen av instruktionerna och sedan slutföra den sista delen för den typ av widget du vill använda.

### Steg 1: Välj typ

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add Widget]**.

1. I avsnittet _[!UICONTROL Settings]_:

   - Ange **[!UICONTROL Type]** till den widgettyp som du vill skapa.

   - Kontrollera att **[!UICONTROL Design Theme]** är inställt på det aktuella temat.

     ![Widget-inställningar](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Continue]**.

### Steg 2: Ange egenskaper och layout för butiken

1. I avsnittet _[!UICONTROL Storefront Properties]_:

   - För **[!UICONTROL Widget Title]** anger du en beskrivande titel för widgeten.

     Den här titeln visas bara från administratören.

   - För **[!UICONTROL Assign to Store Views]** väljer du de butiksvyer där du vill att widgeten ska vara synlig.

     Du kan välja en viss butiksvy eller `All Store Views`. Om du vill markera flera vyer håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

   - (Valfritt) Ange ett nummer för **[!UICONTROL Sort Order]** för att avgöra i vilken ordning det här objektet visas med andra på samma del av sidan. (`0` = först, `1` = sekund, `3` = tredje o.s.v.)

     ![Storefront-egenskaper](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Add Layout Update]** i avsnittet _[!UICONTROL Layout Updates]_.

1. Ange **[!UICONTROL Display On]** till den typ av sida där den ska visas.

1. I listan **[!UICONTROL Container]** väljer du det område i sidlayouten där den ska placeras.

   ![Layoutuppdateringar](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

1. Om widgeten är en länk anger du **[!UICONTROL Template]** till något av följande:

   - `Block Template` - Formaterar innehållet så att det kan placeras som en fristående enhet på sidan.
   - `Inline Template` - Formaterar innehållet så att det kan placeras i annat innehåll. Till exempel en länk som finns inuti ett textstycke.

### Steg 3: Slutför widgetalternativen

Alternativen för varje widgettyp varierar något, men processen är i stort sett densamma. I följande exempel visas produktlistan för en viss kategori med sidnumreringskontroller.

1. Välj **[!UICONTROL Widget Options]** på den vänstra panelen.

1. Klicka på **[!UICONTROL Select Block]**.

1. Ange en **[!UICONTROL Title]** som ska visas ovanför listan, till exempel `Featured Products`.

1. Ange **[!UICONTROL Display Page Control]** till `Yes` för sidnumreringskontroller och gör följande:

   - Ange **[!UICONTROL Number of Products per Page]**.

   - Ange totalsumman **[!UICONTROL Number of Products to Display]**.

   - Ange **[!UICONTROL Condition]** till den produktkategori som ska visas.

     Processen är samma som att ställa in ett villkor för en [prisregel](../merchandising-promotions/price-rules-catalog.md).

### Steg 4: Spara och kontrollera resultatet

1. Klicka på **[!UICONTROL Save]** när du är klar.

1. Följ instruktionerna högst upp på arbetsytan för att uppdatera cachen efter behov.

1. Gå tillbaka till butiken för att kontrollera att widgeten fungerar som den ska.

   Om du vill flytta den till en annan plats kan du öppna widgeten igen och prova med en annan sid- eller blockreferens.

## Demo om att skapa widget

Titta på den här videon om du vill veta mer om hur du skapar widgetar:

>[!VIDEO](https://video.tv.adobe.com/v/343786?quality=12&learn=on)

## Redigera en widget

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**&#x200B;på sidofältet_ Admin _.

1. Leta upp widgeten med hjälp av filtren ovanför stödrastret och klicka sedan på widgetens namn.

1. Gör nödvändiga ändringar.

   Gå igenom stegen för att skapa en widget för information om widgetalternativen.

1. Klicka på **[!UICONTROL Save]**.

## Ta bort en widget

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**&#x200B;på sidofältet_ Admin _.

1. Leta upp widgetarna med hjälp av filtren ovanför stödrastret och markera sedan kryssrutan för de widgetar som ska tas bort.

1. I listans övre vänstra hörn anger du **[!UICONTROL Actions]** till `Delete`.

1. Klicka på **[!UICONTROL Submit]** när du är klar.

1. Bekräfta åtgärden genom att klicka på **[!UICONTROL OK]**.
