---
title: URL-omskrivningar
description: Lär dig mer om att skriva om URL-adresser och att använda Commerce URL-omskrivningsverktyg för att ändra URL-adresser som är kopplade till en produkt, kategori eller CMS-sida.
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# URL-omskrivningar

>[!TIP]
>
>Information om Adobe Commerce as a Cloud Service finns i [SEO-riktlinjerna](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/?lang=sv-SE) i dokumentationen för Commerce Storefront

Med URL-omskrivningsverktyget kan du ändra alla URL-adresser som är kopplade till en produkt, kategori eller CMS-sida. När omskrivningen börjar gälla omdirigeras alla länkar som pekar på den tidigare URL:en till den nya adressen.

>[!NOTE]
>
>Om du vill uppdatera URL-omskrivningar för flera eller alla produkter samtidigt läser du [Flera URL-omskrivningar](url-rewrite-product.md#multiple-url-rewrites).

Termerna _rewrite_ och _redirect_ används ofta på samma sätt, men refererar till något annorlunda processer. En URL-omskrivning ändrar det sätt som en URL visas i webbläsaren. En URL-omdirigering uppdaterar URL:en som lagras på servern. En URL-omdirigering kan vara tillfällig eller permanent. Butiken använder URL-omskrivningar och omdirigeringar för att göra det enkelt för dig att ändra URL-nyckeln för en produkt, kategori eller sida och bevara befintliga länkar.

Som standard är [automatiska URL-omdirigeringar](url-redirect-product-automatic.md) aktiverade för din butik och kryssrutan **Skapa permanent omdirigering för gammal URL** markeras under URL-nyckelfältet för varje produkt.

{{url-rewrite-skip}}

{{url-rewrite-params}}

![Sökmotoroptimering - skapa permanent URL-omdirigering](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

## Kanoniska URL:er

För SEO-syften är det en bra idé att var och en av dina webbsidor bara har en, tydlig URL-adress.

Om du har en sida som kan nås av flera URL-adresser, eller olika sidor med liknande innehåll, ser Google dem som dubblettversioner av samma sida. Google väljer en URL som den kanoniska versionen och crawlningen som, och alla andra URL:er betraktas som dubblerade URL:er och crawlas mindre ofta.

Om du inte uttryckligen talar om för Google vilken URL som är kanonisk, kan det vara ett val för dig, eller också kan båda ha samma vikt. Detta kan leda till oönskat beteende och kan leda till en ineffektiv crawlningsbudget och låg distribuerad backlänkar.

Beroende på hur du konfigurerar webbplatsen kan det finnas flera versioner av din webbplats i indexet, bland annat:

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

Mer information om hur du anger en kanonisk sida finns i [Google Search Central-dokumentationen](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).

## Konfigurera URL-omskrivningar

Möjligheten att aktivera återskrivningar av webbserverns Apache ingår i den första Commerce-installationen. Commerce använder ofta URL-omskrivningar för att ta bort filnamnet `index.php` som normalt visas i URL:en precis efter rotmappen. När Rewrites för webbserver är aktiverat skriver systemet om alla URL:er för att utelämna `index.php`. Omskrivningen tar bort ord som inte förmedlar något till sökmotorer eller kunder och som inte påverkar prestanda eller webbplatsens rangordning.

URL utan omskrivning av webbserver

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

URL med omskrivning av webbserver

    http://www.yourdomain.com/magento/storeview/url-identifier

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Välj **[!UICONTROL Web]** i den vänstra panelen där **[!UICONTROL General]** är expanderat.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Search Engine Optimization]**.

   ![Allmän konfiguration - optimering av webbsökmotor](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Use Web Server Rewrites]** som din inställning.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Skapa URL-omskrivningar

Du kan använda URL-omskrivningsverktyget för att skapa produkt- och kategoriomskrivningar och anpassade omskrivningar för alla sidor i din butik. När omskrivningen börjar gälla omdirigeras alla befintliga länkar som pekar på den tidigare URL:en till den nya adressen.

URL-omskrivningar kan användas för att lägga till nyckelord med högt värde för att förbättra det sätt på vilket produkten indexeras av sökmotorer. Du kan också använda omskrivningar för att skapa ytterligare URL:er för en tillfällig säsongsändring eller permanent ändring. Återskrivningar kan skapas för alla giltiga sökvägar, inklusive CMS innehållssidor. Internt refererar systemet alltid produkter och kategorier efter deras ID. Oavsett hur ofta URL:en ändras, ändras inte ID:t. Här är några sätt som du kan använda en URL-omskrivning:

System-URL

    http://www.example.com/catalog/category/id/6

Ursprunglig URL

    http://www.example.com/peripherals/keyboard.html

Omdirigerad produkt-URL

    http://www.example.com/ergonomic-keyboard.html

Ytterligare kategori-URL

    http://www.example.com/all-on-sale.html
    http://www.example.com/save-now/spring-sale

![URL skriver om stödraster](./assets/url-rewrites.png){width="700" zoomable="yes"}

Commerce erbjuder följande typer av URL-omskrivning:

* [Återskrivningar av produkter](url-rewrite-product.md)
* [Kategoriåterskrivningar](url-rewrite-category.md)
* [CMS Page Rewrites](url-rewrite-cms-page.md)
* [Anpassade omskrivningar](url-rewrite-custom.md)

## Demo om återskrivningar av URL

I den här videon får du lära dig mer om hur du hanterar URL-omskrivningar:

>[!VIDEO](https://video.tv.adobe.com/v/343751?quality=12&learn=on)
