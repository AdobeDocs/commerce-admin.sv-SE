---
title: Översätta en innehållssida
description: Lär dig hur du skapar en översatt version av varje sida som är tillgänglig från den specifika butiksvyn.
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# Översätta en innehållssida

Om din butik har flera vyer på olika [språk](../stores-purchase/store-localize.md) och du har angett språket för varje vy till ett annat språk blir resultatet en delvis översatt webbplats. Nästa steg är att skapa en översatt version av varje sida som är tillgänglig från butiksvyn. Kolumnen [!UICONTROL Store View] i listan _[!UICONTROL Manage Pages]_visar varje vy som har en översatt version av sidan.

Om du vill översätta en innehållssida måste du skapa en annan sida som har samma URL-nyckel som originalet, men som är tilldelad den specifika butiksvyn. Uppdatera sedan sidan för den specifika vyn med den översatta texten. I följande exempel visas hur du skapar en översatt version av sidan _Om oss_ för den spanska butiksvyn.

## Steg 1: Kopiera URL-nyckeln för sidan som ska översättas

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**på sidofältet_ Admin _.

1. I rutnätet söker du efter sidan som ska översättas och öppnar den i _redigeringsläget_.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Search Engine Optimization]** och kopiera **[!UICONTROL URL Key]** till Urklipp.

1. Om du vill gå tillbaka till stödrastret _[!UICONTROL Pages]_klickar du på&#x200B;**[!UICONTROL Back]**i det övre knappfältet.

## Steg 2: Lägg till en sida för det översatta innehållet

1. Klicka på **[!UICONTROL Add New Page]**.

1. Ange den översatta **[!UICONTROL Page Title]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Content]** och slutför den översatta texten för sidan.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Search Engine Optimization]** och gör följande:

   - Klistra in **[!UICONTROL URL Key]** som du kopierade från originalsidan.

   - Ange den översatta texten för **[!UICONTROL Meta Title]**, **[!UICONTROL Meta Keywords]** och **[!UICONTROL Meta Description]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Page in Websites]** och ange **[!UICONTROL Store View]** till den butiksvy där sidan ska vara tillgänglig.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Design]** och ange sidans kolumn **[!UICONTROL Layout]**.

1. Klicka på **[!UICONTROL Save]**.

1. Uppdatera alla ogiltiga [caches](../systems/cache-management.md) när du uppmanas till detta.

## Steg 3: Verifiera översättningen

Verifiera översättningen genom att gå till butiken och använda språkväljaren för att ändra butiksvyn.

Observera att det fortfarande finns vissa element på sidan som ska översättas, inklusive företagets sidfotslänkar [block](block-add.md), [välkomstmeddelandet](../getting-started/storefront-branding.md#change-the-welcome-message) och [produktinformation](../stores-purchase/store-localize.md#localize-products).
