---
title: Automatiska omdirigeringar
description: Lär dig hur du konfigurerar automatiska omdirigeringar som ska genereras när URL-nyckeln för en produkt eller kategori ändras i din Commerce Store.
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

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Search Engine Optimization]** -avsnitt.

   ![Katalogkonfiguration - sökmotoroptimering](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** till `Yes`.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Omdirigera produkt-URL:er automatiskt

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Hitta produkten i listan och klicka för att öppna posten.

1. Expandera ![Expansionsväljare ](../assets/icon-display-expand.png) den **[!UICONTROL Search Engine Optimization]** -avsnitt.

   ![Optimering av produktsökmotor - permanent omdirigering](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. För **[!UICONTROL URL Key]** gör du följande:

   - Se till att **[!UICONTROL Create Permanent Redirect for old URL]** är markerad. Om inte, följ instruktionerna för att [aktivera automatiska omdirigeringar](url-rewrite.md#configure-url-rewrites).

   - Uppdatera **[!UICONTROL URL Key]** vid behov, använda alla gemener och icke-avslutande bindestreck mellan dessa tecken i stället för mellanslag.

1. När du är klar klickar du på **[!UICONTROL Save]**.

1. När du uppmanas att uppdatera cachen följer du länkarna i meddelandet längst upp på arbetsytan.

   Den permanenta omdirigeringen gäller nu för produkten och alla tillhörande kategori-URL:er.

## Omdirigera kategoriadresser automatiskt

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Leta reda på kategorin i trädet och klicka för att öppna posten.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Search Engine Optimization]** -avsnitt.

1. För **[!UICONTROL URL Key]** gör du följande:

   - Se till att **[!UICONTROL Create Permanent Redirect for old URL]** är markerad. Om inte, följ instruktionerna för att [aktivera automatiska omdirigeringar](url-rewrite.md#configure-url-rewrites).

   - Uppdatera **[!UICONTROL URL Key]** vid behov, använda alla gemener och icke-avslutande bindestreck mellan dessa tecken i stället för mellanslag.

1. När du är klar klickar du på **[!UICONTROL Save]**.

1. När du uppmanas att uppdatera cachen följer du länkarna i meddelandet längst upp på arbetsytan.

   Den permanenta omdirigeringen gäller nu för kategorin och alla tillhörande produkt-URL:er.

## Hoppa över generering av produkt-URL-omskrivningar för att spara kategori {#skip-rewrite}

>[!WARNING]
>
>Om du stänger av den automatiska genereringen av URL:er för kategorier/produkter tas alla befintliga URL-skrivningar för kategori/produkttyp bort permanent, vilket inte kan återställas. Detta kan potentiellt orsaka olösta konflikter mellan kategori-/produkttypens URL-adress som kräver en manuell uppdatering av URL-nyckeln för att kunna lösas.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Search Engine Optimization]** -avsnitt.

1. Ange **[!UICONTROL Generate "category/product" URL Rewrites]** till `No`.

1. Klicka på **[!UICONTROL OK]** för att bekräfta ändringen och borttagningen av befintliga URL-omskrivningar.

   ![Inaktivera omskrivning av kategori-/produkt-URL - bekräfta](./assets/seo-rewrite-off.png){width="350"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
