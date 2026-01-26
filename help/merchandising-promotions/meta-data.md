---
title: Meta data
description: Läs om hur du kan ange metadata med nyckelord för att förbättra det sätt på vilket sökmotorer indexerar din Commerce-webbplats.
exl-id: 2acc1523-9da6-4e6f-8e4f-607603a61559
feature: Merchandising, Search
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 0%

---

# Meta data

>[!TIP]
>
>Information om Adobe Commerce as a Cloud Service finns i [metadatariktlinjerna](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/metadata/) i dokumentationen för Commerce Storefront

Din butik innehåller platser där du kan ange metadata med sökord för att förbättra sökmotorernas indexering av webbplatsen. När du konfigurerar din butik kan du ange preliminära metadata för att slutföra den senare. Med tiden kan ni finjustera metadata för att inrikta er på kundernas köpmönster och önskemål.

![Produktinställningar - sökmotoroptimering](./assets/product-basic-settings-search-engine-optimization-yoga-strap.png){width="700" zoomable="yes"}

## Meta title

Meta-titeln visas i namnlisten och på fliken i webbläsaren och i sökresultatlistorna. Meta-titeln ska vara unik för sidan och ha färre än 70 tecken.

![Exempelarkiv - metarubrik](./assets/storefront-home-page-meta-title.png){width="600"}

## Meta nyckelord

Även om vissa sökmotorer ignorerar metatangentord används de fortfarande av andra. Det bästa sättet är att lägga in nyckelord med högt värde i metatiteln och metabeskrivningen.

![Webbläsarsökning - metannyckelord](./assets/storefront-meta-description.png){width="500"}

## Beskrivning av Meta

Meta beskrivningar ger en kort översikt över sidan med sökresultatlistor. I idealfallet bör en metabeskrivning innehålla mellan 150 och 160 tecken, men fältet får innehålla upp till 255 tecken.

## Omfattande textutdrag

Detaljerade kodavsnitt innehåller detaljerad information om sökresultatlistor och andra program. Som standard läggs strukturerad datakod som är baserad på standarden [schema.org](https://schema.org/) till i butikens produktmall. Därför finns det mer information för sökmotorer som ska inkluderas som _avancerade fragment_ i produktlistor.

## Kanonisk meta-tagg

Vissa sökmotorer straffar webbplatser som har flera URL:er som pekar på samma innehåll. Den kanoniska meta-taggen anger för sökmotorer vilken sida som ska indexeras när flera URL-adresser har identiskt eller liknande innehåll. Om du använder den kanoniska meta-taggen kan du förbättra webbplatsens rankning och sammanställning av sidvyer. Den kanoniska meta-taggen placeras i `<head>`-blocket på en produkt- eller kategorisida. Den ger en länk till den URL du föredrar, så sökmotorer ger den en bättre vikt.

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

Om du även inkluderar kategorisökvägen i produkt-URL:er förblir den kanoniska URL:en domän-namn/product-url-key. Du kan dock även komma åt produkten via den fullständiga URL:en, som innehåller kategorin. Om produkt-URL-nyckeln till exempel är `driven-backpack` och är tilldelad kategorin Kugghjul > Sväskor, kan produkten nås via någon av URL:erna.

Du kan undvika att straffas av sökmotorer genom att utelämna kategorin från URL-adressen, eller genom att använda den kanoniska meta-taggen för att dirigera sökmotorer till indexering antingen efter produkt eller kategori. Vi rekommenderar att du aktiverar kanoniska metataggar för både kategorier och produkter.

### Aktivera den kanoniska meta-taggen

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **Optimering av sökmotor**.

   Om du vill ändra några fältvärden måste du först avmarkera kryssrutan **Använd systemvärde** efter varje fält.

   ![Katalogkonfiguration - sökmotoroptimering](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Om du vill att sökmotorer bara ska indexera kategorisidor med den fullständiga kategorisökvägen gör du följande:

   - Ange **Använd Meta-taggen för kanoniska länkar för kategorierna** till `Yes`.

   - Ange **Använd Meta-taggen för kanoniska länkar för produkterna** till `No`.

1. Om du vill att sökmotorer bara ska indexera produktsidor med formatet domän-namn/produkt-url-nyckel gör du följande:

   - Ange **Använd Meta-taggen för kanoniska länkar för produkterna** till `Yes`.

   - Ange **Använd Meta-taggen för kanoniska länkar för kategorierna** till `No`.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Meta Data Demo

I den här videon får du lära dig mer om hur du hanterar SEO-metadata:

>[!VIDEO](https://video.tv.adobe.com/v/343750?quality=12&learn=on)
