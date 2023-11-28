---
title: Metadata
description: Lär dig mer om hur du kan ange nyckelordsrika metadata för att förbättra det sätt på vilket sökmotorer indexerar din Commerce-webbplats.
exl-id: 2acc1523-9da6-4e6f-8e4f-607603a61559
feature: Merchandising, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 0%

---

# Metadata

Din butik innehåller platser där du kan ange metadata med sökord för att förbättra sökmotorernas indexering av webbplatsen. När du konfigurerar din butik kan du ange preliminära metadata för att slutföra den senare. Med tiden kan ni finjustera metadata för att inrikta er på kundernas köpmönster och önskemål.

![Produktinställningar - sökmotoroptimering](./assets/product-basic-settings-search-engine-optimization-yoga-strap.png){width="700" zoomable="yes"}

## Meta title

Meta-titeln visas i namnlisten och på fliken i webbläsaren och i sökresultatlistorna. Meta-titeln ska vara unik för sidan och ha färre än 70 tecken.

![Exempel på storefront - metatitel](./assets/storefront-home-page-meta-title.png){width="600"}

## Meta-nyckelord

Även om vissa sökmotorer ignorerar metatangentord används de fortfarande av andra. Det bästa sättet är att lägga in nyckelord med högt värde i metatiteln och metabeskrivningen.

![Webbläsarsökning - metannyckelord](./assets/storefront-meta-description.png){width="500"}

## Meta description

Metabeskrivningar ger en kort översikt över sidan för sökresultatlistor. I idealfallet bör en metabeskrivning innehålla mellan 150 och 160 tecken, men fältet får innehålla upp till 255 tecken.

## Omfattande textutdrag

Detaljerade kodavsnitt innehåller detaljerad information om sökresultatlistor och andra program. Som standard är strukturerad datamarkering som baseras på [schema.org][1] standard läggs till i butikens produktmall. Därför finns det mer information för sökmotorer som ska inkluderas som _rich snippets_ i produktlistor.

## Kanonisk meta-tagg

Vissa sökmotorer straffar webbplatser som har flera URL:er som pekar på samma innehåll. Den kanoniska meta-taggen anger för sökmotorer vilken sida som ska indexeras när flera URL-adresser har identiskt eller liknande innehåll. Om du använder den kanoniska meta-taggen kan du förbättra webbplatsens rankning och sammanställning av sidvyer. Den kanoniska meta-taggen placeras i `<head>` block för en produkt- eller kategorisida. Den ger en länk till den URL du föredrar, så sökmotorer ger den en bättre vikt.

### Exempel 1: Kategorisökvägen skapar dubblerade URL:er

Om din katalog till exempel är konfigurerad att inkludera kategorinavigeringssökvägen i produkt-URL:er, genererar din butik flera URL:er som pekar på samma produktsida.

    http://mystore.com/gear/bags/driven-backpack.html
    http://mystore.com/driven-backpack.html

### Exempel 2: Kategorisidans fullständiga URL

När kanoniska metataggar för kategorier är aktiverade innehåller kategorisidan i din butik en kanonisk URL till den fullständiga kategorins URL:

    http://mystore.com/gear/bags/

### Exempel 3: Produktsidans fullständiga URL

När kanoniska metataggar för produkter är aktiverade innehåller produktsidan en kanonisk URL till nyckeln domain-name/product-url eftersom produkt-URL-nycklarna är globalt unika.

    http://mystore.com/driven-backpack.html

Om du även inkluderar kategorisökvägen i produkt-URL:er förblir den kanoniska URL:en domän-namn/product-url-key. Du kan dock även komma åt produkten via den fullständiga URL:en, som innehåller kategorin. Om produkt-URL-nyckeln till exempel är `driven-backpack` och som är tilldelad kategorin Kugghjulet > Bags, kan du få åtkomst till produkten via någon av URL:erna.

Du kan undvika att straffas av sökmotorer genom att utelämna kategorin från URL-adressen, eller genom att använda den kanoniska meta-taggen för att dirigera sökmotorer till indexering antingen efter produkt eller kategori. Vi rekommenderar att du aktiverar kanoniska metataggar för både kategorier och produkter.

### Aktivera den kanoniska meta-taggen

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **Sökmotoroptimering** -avsnitt.

   Om du vill ändra några fältvärden måste du först rensa **Använd systemvärde** efter varje fält.

   ![Katalogkonfiguration - sökmotoroptimering](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Om du vill att sökmotorer bara ska indexera kategorisidor med den fullständiga kategorisökvägen gör du följande:

   - Ange **Använd metataggen för kanonisk länk för kategorier** till `Yes`.

   - Ange **Använd metataggen för kanoniska länkar för produkter** till `No`.

1. Om du vill att sökmotorer bara ska indexera produktsidor med formatet domän-namn/produkt-url-nyckel gör du följande:

   - Ange **Använd metataggen för kanoniska länkar för produkter** till `Yes`.

   - Ange **Använd metataggen för kanonisk länk för kategorier** till `No`.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Demo av metadata

I den här videon får du lära dig mer om hur du hanterar SEO-metadata:

>[!VIDEO](https://video.tv.adobe.com/v/343750?quality=12)

[1]: https://schema.org/
