---
title: Automatiska omdirigeringar
description: Lär dig hur du konfigurerar automatiska omdirigeringar som ska genereras när URL-nyckeln för en produkt eller kategori ändras i din Commerce-butik.
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# Automatiska omdirigeringar

Din butik kan konfigureras så att den automatiskt genererar en permanent omdirigering när URL-nyckeln för en produkt eller kategori ändras. I avsnittet Sökmotoroptimering visas om permanenta omdirigeringar är aktiverade i kryssrutan under URL-nyckeln. Om din butik redan är konfigurerad att automatiskt omdirigera katalog-URL:er är en omdirigering en enkel uppdatering av URL-nyckeln. Processen att skapa en automatisk omdirigering är densamma för både produkter och kategorier.

>[!NOTE]
>
>När automatiska omdirigeringar är aktiverade och du sparar en kategori, genereras alla produkt- och kategoriomskrivningar i realtid och lagras som standard i databastabeller. Detta kan leda till betydande prestandaproblem för kategorier med många tilldelade produkter. Lösningen är att ändra den här standardinställningen och hoppa över generering av URL-omskrivningar för kategori/produkter för produkter när en kategori sparas. I det här fallet genereras produktomskrivningar endast för den kanoniska produkt-URL:en.

## Konfigurera automatiska omdirigeringar

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Search Engine Optimization]**.

   ![Katalogkonfiguration - sökmotoroptimering](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** till `Yes`.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Omdirigera produkt-URL:er automatiskt

1. Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]** på sidofältet _Admin_.

1. Hitta produkten i listan och klicka för att öppna posten.

1. Expandera ![Expansionsväljaren ](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Search Engine Optimization]**.

   ![Optimering av produktsökmotor - permanent omdirigering](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. Gör följande för **[!UICONTROL URL Key]**:

   - Kontrollera att kryssrutan **[!UICONTROL Create Permanent Redirect for old URL]** är markerad. Om inte, följ instruktionerna för att [aktivera automatiska omdirigeringar](url-rewrite.md#configure-url-rewrites).

   - Uppdatera **[!UICONTROL URL Key]** efter behov med alla gemener och bindestreck som inte är avslutande mellan dessa tecken i stället för mellanslag.

1. Klicka på **[!UICONTROL Save]** när du är klar.

1. När du uppmanas att uppdatera cachen följer du länkarna i meddelandet längst upp på arbetsytan.

   Den permanenta omdirigeringen gäller nu för produkten och alla tillhörande kategori-URL:er.

## Omdirigera kategoriadresser automatiskt

1. Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Categories]** på sidofältet _Admin_.

1. Leta reda på kategorin i trädet och klicka för att öppna posten.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Search Engine Optimization]**.

1. Gör följande för **[!UICONTROL URL Key]**:

   - Kontrollera att kryssrutan **[!UICONTROL Create Permanent Redirect for old URL]** är markerad. Om inte, följ instruktionerna för att [aktivera automatiska omdirigeringar](url-rewrite.md#configure-url-rewrites).

   - Uppdatera **[!UICONTROL URL Key]** efter behov med alla gemener och bindestreck som inte är avslutande mellan dessa tecken i stället för mellanslag.

1. Klicka på **[!UICONTROL Save]** när du är klar.

1. När du uppmanas att uppdatera cachen följer du länkarna i meddelandet längst upp på arbetsytan.

   Den permanenta omdirigeringen gäller nu för kategorin och alla tillhörande produkt-URL:er.

## Hoppa över generering av produkt-URL-omskrivningar för att spara kategori {#skip-rewrite}

>[!WARNING]
>
>Om du stänger av den automatiska genereringen av URL:er för kategorier/produkter tas alla befintliga URL-skrivningar för kategori/produkttyp bort permanent, vilket inte kan återställas. Detta kan potentiellt orsaka olösta konflikter mellan kategori-/produkttypens URL-adress som kräver en manuell uppdatering av URL-nyckeln för att kunna lösas.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Search Engine Optimization]**.

1. Ange **[!UICONTROL Generate "category/product" URL Rewrites]** till `No`.

1. Klicka på **[!UICONTROL OK]** i bekräftelsedialogrutan för att bekräfta ändringen och borttagningen av befintliga URL-skrivningar.

   ![Inaktivera omskrivning av kategori-/produkt-URL - bekräfta](./assets/seo-rewrite-off.png){width="350"}

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
