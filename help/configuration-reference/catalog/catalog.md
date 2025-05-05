---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Catalog]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Catalog] &gt; [!UICONTROL Catalog] i Commerce Admin.
exl-id: fc25ae80-aaa7-42c4-bba2-f03d3caa7970
feature: Configuration, Catalog Management
source-git-commit: 20f97d6ab391b7f5675d6790ab2ec5d24e9dda21
workflow-type: tm+mt
source-wordcount: '3261'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Catalog]

{{config}}

## [!UICONTROL Product Fields Auto-Generation]

![Automatisk generering av produktfält](./assets/catalog-product-fields-auto-generation.png)<!-- zoom -->

<!-- [Product Fields Auto-Generation](https://experienceleague.adobe.com/sv/docs/commerce-admin/catalog/products/product-workspace#default-field-values) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Mask for SKU] | Global | Bestämmer SKU-fältets standardvärde baserat på platshållarvärden från andra fält och eventuell ytterligare text som anges. Standardplatshållare: <br/>Produktnamn - `{{name}}` |
| [!UICONTROL Mask for Meta Title] | Global | Bestämmer standardvärdet för fältet Meta Title baserat på platshållarvärden från andra fält och eventuell ytterligare text som anges. Standardplatshållare: <br/>Produktnamn - `{{name}}` |
| [!UICONTROL Mask for Meta Keywords] | Global | Bestämmer standardvärdet för fältet _Meta Keywords_ baserat på platshållarvärden från andra fält och eventuell ytterligare text som anges. Standardplatshållare: <br/>Produktnamn - `{{name}}` |
| [!UICONTROL Mask for Meta Description] | Global | Bestämmer standardvärdet för fältet Metabeskrivning baserat på platshållarvärden från andra fält och eventuell ytterligare text som anges. Standardplatshållare: <br/>Produktnamn - `{{name}}` <br/>Beskrivning - `{{description}}` |

{style="table-layout:auto"}

## [!UICONTROL Product Reviews]

![Produktrecensioner](./assets/catalog-product-reviews.png)<!-- zoom -->

<!-- [Product Reviews](https://experienceleague.adobe.com/sv/docs/commerce-admin/marketing/merchandising/product-reviews/product-reviews) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Butiksvy | Aktiverar produktrecensioner. Alternativ: `Yes` / `No` |
| [!UICONTROL Allow Guests to Write Reviews] | Webbplats | Avgör om kunderna måste öppna ett konto hos din butik för att kunna skriva produktrecensioner. |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![Storefront](./assets/catalog-storefront.png)<!-- zoom -->

<!-- [Storefront](https://experienceleague.adobe.com/sv/docs/commerce-admin/catalog/catalog/navigation/navigation-product-listings) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL List Mode] | Butiksvy | Bestämmer formatet för sökresultatlistan. Alternativ: <br/>**`Grid Only`**- Formaterar listan som ett rutnät med rader och kolumner. Varje produkt visas i en enda cell i rutnätet.<br/>**`List Only`** - Formaterar listan med varje produkt på en separat rad. <br/>**`Grid (default / List)`**- Produkterna visas som standard i stödrastervyn och kan växlas till listvyn.<br/>**`List (default / Grid)`** - Produkterna visas som standard i listvyn och kan växlas till stödrastervyn. |
| [!UICONTROL Products per Page on Grid Allowed Values] | Butiksvy | Anger hur många produkter som visas i stödrastervyn. Ange flera värden avgränsade med kommatecken om du vill välja alternativ. |
| [!UICONTROL Products per Page on Grid Default Value] | Butiksvy | Anger hur många produkter som visas per sida som standard i stödrastervyn. |
| [!UICONTROL Products per Page on List Allowed Values] | Butiksvy | Bestämmer antalet produkter som visas i listvyn. Ange flera värden avgränsade med kommatecken om du vill välja alternativ. |
| [!UICONTROL Products per Page on List Default Value] | Butiksvy | Anger antalet produkter som visas per sida som standard i listvyn. |
| Produktlista sortera efter | Butiksvy | Bestämmer sorteringsordningen i sökresultatlistan. Valet av alternativ avgörs av kategorins visningsinställningar och de tillgängliga attribut som är inställda på `Used for Sorting in Product Listing`. Standardvärdet är `Use All Available Attributes` och innehåller vanligtvis Bästa värde, Namn, Pris. Den här inställningen gäller inte för [!DNL Live Search] [Sidwidgeten Produktlista](https://experienceleague.adobe.com/sv/docs/commerce/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Allow All Products per Page] | Butiksvy | Om värdet är `Yes` inkluderas alternativet `ALL` i kontrollen &quot;Visa per sida&quot;. |
| [!UICONTROL Remember Category Pagination] | Global | Om värdet är `Yes` sparas de aktuella kategorisidbrytningsvärdena när kunderna bläddrar från en kategori till en annan i [produktlistor](../../catalog/navigation-product-listings.md). När du sparar värdet används mer lagringsutrymme och det kan påverka hur sidor indexeras av sökmotorer. Alternativ: `Yes` / `No` (standard) |
| [!UICONTROL Use Flat Catalog Category] | Global | Aktiverar den [platta kategoristrukturen](../../catalog/catalog-flat.md) (rekommenderas inte). Alternativ: `Yes` / `No` |
| [!UICONTROL Use Flat Catalog Product] | Global | Aktiverar plattproduktstrukturen. (rekommenderas inte) Alternativ: `Yes` / `No` |
| [!UICONTROL Swatches per Product] | Butiksvy | Anger antalet tillgängliga färgrutor för varje produkt. Standard: `16` |
| [!UICONTROL Show Swatches in Product List] | Butiksvy | Anger om färgrutorna visas i produktlistan. Alternativ: `Yes` / `No` |
| [!UICONTROL Show Swatch Tooltip] | Butiksvy | Anger om verktygstipset för färgrutan visas. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Alerts]

![Produktaviseringar](./assets/catalog-product-alerts.png)<!-- zoom -->

<!-- [Product Alerts](https://experienceleague.adobe.com/sv/docs/commerce-admin/inventory/configuration/product-alerts/alert-setup) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Allow Alerts When Product Price Changes] | Butiksvy | Avgör om det finns e-postaviseringar tillgängliga för produktprisändringar. Alternativ: `Yes` / `No` |
| [!UICONTROL Price Alert Email Template] | Butiksvy | Identifierar mallen som används för e-postaviseringar om produktprisändringar. Standardmall: `Product price alert` |
| [!UICONTROL Allow Alert When Product Comes Back in Stock] | Webbplats | Avgör om kunderna kan välja att få en avisering när produkten kommer tillbaka i lager. Alternativ: `Yes` / `No` |
| [!UICONTROL Stock Alert Email Template] | Butiksvy | Identifierar mallen som används för e-postmeddelanden om lagervarningar. Standardmall: `Product stock alert` |
| [!UICONTROL Alert Email Sender] | Butiksvy | Bestämmer butikskontakten som visas som avsändare av produktvarningsmeddelandet. Alternativ: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email` |

{style="table-layout:auto"}

## [!UICONTROL Product Alerts Run Settings]

![Körningsinställningar för produktaviseringar](./assets/catalog-product-alerts-run-settings.png)<!-- zoom -->

<!-- [Product Alerts Run Settings](https://experienceleague.adobe.com/sv/docs/commerce-admin/inventory/configuration/product-alerts/alert-setup) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Frequency] | Global | Välj hur ofta produktvarningar skickas ut. Alternativ: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Start Time] | Global | Välj vilken tid på dagen som produktaviseringsprocessen ska starta. Den här tiden ska vara efter att pris- eller lageruppdateringar har utförts. |
| [!UICONTROL Error Email Recipient] | Global | Identifiera e-postadressen till den person (vanligtvis en butiksadministratör) som ska få ett e-postmeddelande när ett fel uppstår i produktaviseringsprocessen. |
| [!UICONTROL Error Email Sender] | Global | Välj rollen som e-postmeddelandet är `from`. |
| [!UICONTROL Error Email Template] | Global | Välj den e-postmall som ska användas för felmeddelanden för produktaviseringar. |

{style="table-layout:auto"}

## [!UICONTROL Product Image Placeholders]

![Platshållare för produktbilder](./assets/catalog-product-image-placeholders.png)<!-- zoom -->

<!-- [Product Image Placeholders](https://experienceleague.adobe.com/sv/docs/commerce-admin/catalog/products/digital-assets/product-image-config#image-placeholders) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Base Image] | Butiksvy | Identifierar platshållarfilen som valts för basbilden. |
| [!UICONTROL Small Image] | Butiksvy | Identifierar platshållarfilen som valts för den lilla bilden. |
| [!UICONTROL Swatch] | Butiksvy | Identifierar platshållarfilen som valts för färgrutan. |
| [!UICONTROL Thumbnail] | Butiksvy | Identifierar platshållarfilen som valts för miniatyrbilden. |
| [!UICONTROL Choose File] |  | Navigerar till filen och överför den som platshållarbild för typen. |

{style="table-layout:auto"}

## [!UICONTROL Recently Viewed/Compared Products]

![Nyligen visade/jämförda produkter](./assets/catalog-recently-viewed-and-compared-products.png)<!-- zoom -->

<!-- Recently Viewed/Compared Products](https://experienceleague.adobe.com/sv/docs/commerce-admin/stores-sales/shopper-tools/products-viewed-compared) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Synchronize widget products with backend storage] | Global | Anger synkroniseringen av produktwidgetinformation, t.ex. produkt-ID, med databasen. På så sätt kan information återanvändas på andra enheter. |
| [!UICONTROL Show for Current] | Webbplats | Begränsar de produkter som visas till den aktuella webbplatsen. Alternativ: `Website` / `Store` / `Store View` |
| [!UICONTROL Default Recently Viewed Products Count] | Butiksvy | Anger det maximala antalet nyligen visade produkter som visas i listan. |
| [!UICONTROL Default Recently Compared Products Count] | Butiksvy | Anger det maximala antalet nyligen jämförda produkter som visas i listan. |
| [!UICONTROL Lifetime of products in Recently Viewed Widget] | Global | Avgör hur länge i sekunder som visade produkter visas i listan över senast visade. |
| [!UICONTROL Lifetime of products in Recently Compared Widget] | Global | Avgör hur länge jämförda produkter visas i listan över senast jämförda produkter i sekunder. |

{style="table-layout:auto"}

## [!UICONTROL Product Video]

![Produktvideor](./assets/catalog-product-video.png)<!-- zoom -->

<!-- [Product Videos](https://experienceleague.adobe.com/sv/docs/commerce-admin/catalog/products/digital-assets/product-video) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL YouTube API key] | Butiksvy | Anger den API-nyckel som krävs för att ansluta till YouTube-servern. |
| [!UICONTROL Autostart base video] | Butiksvy | Om du vill starta videon automatiskt när sidan har lästs in, anger du värdet `Yes`. |
| [!UICONTROL Show related video] | Butiksvy | Om du vill visa relaterade videoklipp anger du `Yes`. |
| [!UICONTROL Auto restart video] | Butiksvy | Ange `Yes` om du vill aktivera automatisk uppspelning av video. |

{style="table-layout:auto"}

## [!UICONTROL Price]

![Pris](./assets/catalog-price.png)<!-- zoom -->

<!--Price](https://experienceleague.adobe.com/sv/docs/commerce-admin/catalog/products/pricing/catalog-price-scope) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Catalog Price Scope] | Global | Bestämmer omfattningen för basvalutan. Alternativ: `Global` / `Website` |
| [!UICONTROL Default Product Price] | Global | ![Adobe Commerce](../../assets/adobe-logo.svg) (endast Adobe Commerce) Definierar standardproduktpriset, om tillämpligt. |

{style="table-layout:auto"}

## [!UICONTROL Layered Navigation]

>[!NOTE]
>
>Standardsökkonfigurationen som beskrivs i det här avsnittet skiljer sig åt för [Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=sv-SE).

<!-- [Layered Navigation - Automatic (equalize price ranges)](https://experienceleague.adobe.com/sv/docs/commerce-admin/catalog/catalog/navigation/navigation-layered#configure-layered-navigation) -->

![Navigering i lager - Automatisk (jämför prisintervall)](./assets/layered-navigation-equalize-price-range.png)<!-- zoom -->

![Navigering i lager - Automatisk (jämför produktantal)](./assets/layered-navigation-equalize-product-counts.png)<!-- zoom -->

![Navigering i lager - Manuell](./assets/layered-navigation-manual.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Display Product Count] | Butiksvy | Avgör om produktantalet visas efter varje attribut, prisintervall och kategori. Alternativ: `Yes` / `No` |
| [!UICONTROL Price Navigation Step Calculation] | Butiksvy | Bestämmer metoden som används för att fastställa [prisnavigeringssteget](../../catalog/navigation-layered.md#configure-price-navigation)). Alternativ: <br/>`Automatic (equalize price ranges)` - Baserar beräkningen på prisintervallet för produkter i gruppen. <br/>`Automatic (equalize product counts)` - Baserar beräkningen på antalet produkter i gruppen. Fastställer ett tröskelvärde för minsta antal produkter i gruppen, för att förhindra att de delas upp i mindre grupper. <br/>`Manual` - Använder divisionsgränsen som du anger för prisintervall. |
| [!UICONTROL Default Price Navigation Step] | Butiksvy | Anger antalet produkter som ingår i varje steg. |
| [!UICONTROL Maximum Number of Price Intervals] | Butiksvy | Fastställer en gräns för antalet prisintervall som visas i lagerstyrd navigering. |

{style="table-layout:auto"}

## [!UICONTROL Category Permissions]

{{ee-feature}}

![Kategoribehörigheter](./assets/catalog-category-permissions.png)<!-- zoom -->

<!-- [Category Permissions](https://experienceleague.adobe.com/sv/docs/commerce-admin/catalog/categories/category-permissions) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable] | Global | Aktiverar kategoribegränsningar. Som standard begränsas alla kategorier när du använder den här funktionen. Alternativ: `Yes` / `No` |
| [!UICONTROL Allow Browsing Category] | Webbplats | Bestämmer vem som får bläddra igenom kategorier. Alternativ: <br/>`Yes, for Everyone` - Gör att alla besökare och kunder kan bläddra i kategorin. <br/>`Yes, for Specified Customer Groups` - Tillåter endast medlemmar i valda kundgrupper att bläddra i kategorin. <br/>`No, Redirect to Landing Page` - Nekar åtkomst till kategorin och dirigerar om till den valda sidan. |
| [!UICONTROL Display Product Prices] | Webbplats | Kontrollerar visningen av produktpriser för kategorin. Alternativ: <br/>`Yes, for Everyone` - Alla kan se priset på produkter i kategorin. <br/>`Yes, for Specified Customer Groups` - Endast medlemmar i valda kundgrupper kan se priset på produkter i kategorin. <br/>`No` - Stänger av visningen av produktpriser för kategorin. |
| [!UICONTROL Allow Adding to Cart] | Webbplats | Bestämmer vem som kan köpa produkter från kategorin. Alternativ: <br/>`Yes, for Everyone` - Alla kan placera produkter från kategorin i sina kundvagnar. <br/>`Yes, for Specified Customer Groups` - Tillåter endast medlemmar i valda kundgrupper att placera produkter från kategorin i sina kundvagnar. <br/>`No` - Ingen får placera produkter från kategorin i sina kundvagnar. |
| [!UICONTROL Disallow Catalog Search by] | Webbplats | Identifierar de kundgrupper som inte tillåts söka efter produkter i kategorin. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![Sökmotoroptimering](./assets/catalog-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization](https://experienceleague.adobe.com/sv/docs/commerce-admin/catalog/products/settings/product-search-engine-optimization) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Popular Search Terms] | Butiksvy | Avgör om _Populära sökvillkor_ har implementerats i arkivet. Den här inställningen gäller inte för butiker som använder [Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=sv-SE). Alternativ: `Enable` / `Disable` |
| [!UICONTROL Product URL Suffix] | Butiksvy | Avgör om ett suffix, till exempel html eller htm, används på produkt-URL:er. Om det används ska du inte ange någon punkt före suffixet, eftersom det tillämpas automatiskt. |
| [!UICONTROL Category URL Suffix] | Butiksvy | Avgör om ett suffix, till exempel html eller htm, används på kategorins URL:er. Om det används ska du inte ange någon punkt före suffixet, eftersom det tillämpas automatiskt. |
| [!UICONTROL Use Categories Path for Product URLs] | Butiksvy | Avgör om kategorisökvägar inkluderas i produkt-URL:er på butiken. Om du gör det kan flera URL-adresser peka på samma sida, vilket kan påverka sökordningen. Mer information finns i [Kanonisk meta-tagg](../../merchandising-promotions/meta-data.md#canonical-meta-tag). |
| [!UICONTROL Create Permanent Redirect for URLs if URL Key Changed] | Butiksvy | Avgör om en permanent omdirigering skapas automatiskt när en URL-nyckel ändras. När det är implementerat är kryssrutan Skapa anpassad omdirigering för gammal URL under fältet för produkt-URL-nyckel markerad som standard. Alternativ: `Yes` / `No` |
| [!UICONTROL Generate "category/product" URL Rewrites] | Global | Avgör om Adobe Commerce genererar data och sparar dem i omskrivningstabeller när en användare sparar en kategori som innehåller många tilldelade produkter.  <br/><br/>Om du ändrar det här alternativet påverkas inte hur produkt-URL:er hanteras i Adobe Commerce, eftersom systemet automatiskt löser produkt-URL:er oavsett den här inställningen. <br/><br/>Alternativ: `Yes` / `No` <br/><br/>**_Viktigt!_**&#x200B;Om du sparar genererade data i en URL-omskrivningstabell kan prestandan försämras. Mer information finns i [Automatiska produktomdirigeringar](../../merchandising-promotions/url-redirect-product-automatic.md). |
| [!UICONTROL Apply transliteration for product URL] | Butiksvy | Avgör om translitterering används när produkt-URL:er skapas eller uppdateras. Alternativ: `Yes` / `No`. Standardvärdet är `Yes`. <br/><br/>I vissa fall bör du inaktivera transkribering. Om du till exempel har en webbutik på kinesiska rekommenderar SEO att URL:er för produkten matchar produktnamnet. Om du anger alternativet till `No` kan kinesiska tecken användas i produkt-URL:er i stället för ASCII-motsvarigheter. |
| [!UICONTROL Page Title Separator] | Butiksvy | Identifierar tecknet som skiljer kategorinamnet och underkategorin åt i webbläsarens namnlist. |
| [!UICONTROL Use Canonical Link Meta Tag for Categories] | Butiksvy | Om det finns flera URL:er som pekar på samma kategorisida använder det här alternativet en kanonisk meta-tagg för att identifiera den kategori-URL som sökmotorer ska indexera. URL:en innehåller ett fullständigt namn till kategorin med meta-taggen. Detta minskar dubblettinnehållet och förbättrar SEO. Alternativ: `Yes` / `No` |
| [!UICONTROL Use Canonical Link Meta Tag for Products] | Butiksvy | Om det finns flera URL:er som pekar på samma produktsida använder det här alternativet en kanonisk meta-tagg för att identifiera den produkt-URL som sökmotorer ska indexera. URL:en innehåller ett fullständigt namn till produkten med meta-taggen. Detta minskar dubblettinnehållet och förbättrar SEO. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Category Top Navigation]

![Övre kategorinavigering](./assets/catalog-category-top-navigation.png)<!-- zoom -->

<!-- Category Top Navigation](https://experienceleague.adobe.com/sv/docs/commerce-admin/catalog/catalog/navigation/navigation-top) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Maximal Depth] | Global | Anger antalet underkategorinivåer i den övre navigeringen. Standardvärdet `0` har ingen gräns för antalet nivåer. |

{style="table-layout:auto"}

## [!UICONTROL Catalog Search]

Du kan konfigurera katalogsökning med [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=sv-SE) eller tredjepartstjänster som stöds av Adobe Commerce. Följ instruktionerna för installationen.

### Adobe Commerce med [!DNL Live Search]

När Live Search är installerat innehåller katalogsökningen följande konfigurationsinställningar:

![Katalogsökning för Live-sökning](./assets/catalog-search-live-search.png)<!-- zoom -->

<!-- [Catalog Search for Live Search](https://experienceleague.adobe.com/sv/docs/commerce-admin/catalog/catalog/search/search-configuration) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Minimal Query Length] | Butiksvy | Det minsta antalet tecken som tillåts i en katalogsökning. Värdet som anges för det här alternativet måste vara kompatibelt med motsvarande intervall som anges i dina Elasticsearch sökmotorkonfigurationer. Om du till exempel anger värdet `2` i Adobe Commerce, uppdaterar du värdet i sökmotorn. |
| [!UICONTROL Maximum Query Length] | Butiksvy | Det maximala antalet tecken som tillåts i en katalogsökning. Värdet som anges för det här alternativet måste vara kompatibelt med motsvarande intervall som anges i dina Elasticsearch sökmotorkonfigurationer. Om du till exempel anger värdet 300 i Adobe Commerce, uppdaterar du värdet i sökmotorn. |
| [!UICONTROL Number of top search results to cache] | Butiksvy | Antalet populära söktermer och sökresultat som ska cachelagras för snabbare svar. Om du anger värdet `0` cachelagras alla söktermer och sökresultat när de anges en andra gång. Standardvärde: `100` |
| [!UICONTROL Autocomplete Limit] | Butiksvy | Avgör det maximala antalet rader som är tillgängliga på sidan [storefront pover]. Standardvärdet kan ändras när Live Search installeras och uppdateras senare genom att den här konfigurationsinställningen ändras. Standardvärde: `8` |

{style="table-layout:auto"}

### Sökmotorer från tredje part

Adobe Commerce stöder OpenSearch och Elasticsearch. Adobe Commerce version 2.3.7-p3, 2.4.3-p2 och 2.4.4 och senare stöder OpenSearch-tjänsten. Elasticsearch 7.11 och senare stöds inte i Adobe Commerce för molninfrastrukturprojekt. Elasticsearch stöds fortfarande för lokala installationer.

>[!IMPORTANT]
>
>- På grund av att supporten för Elasticsearch 7 upphör i augusti 2023 rekommenderar Adobe att alla Adobe Commerce-kunder migrerar till sökmotorn OpenSearch 2.x. Mer information om hur du migrerar sökmotorn under en uppgradering finns i [Migrera till OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html?lang=sv-SE) i _uppgraderingshandboken_.
>- I version 2.4.4 och 2.4.3-p2 gäller alla fält med etiketten Elasticsearch även OpenSearch. När stöd för Elasticsearch 8.x introducerades i version 2.4.6 skapades nya etiketter för att skilja mellan Elasticsearch- och OpenSearch-konfigurationer. Konfigurationsalternativen för båda är dock desamma.

![Konfigurationsalternativ för katalogsökning](./assets/catalog-search-opensearch.png){zoomable="yes"}

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Minimal Query Length] | Butiksvy | Det minsta antalet tecken som tillåts i en katalogsökning. Värdet som anges för det här alternativet måste vara kompatibelt med motsvarande intervall som anges i OpenSearch- eller Elasticsearch-konfigurationen. Om du till exempel anger värdet `2` i Adobe Commerce måste du även uppdatera värdet i sökmotorkonfigurationen. Standardvärde: `3` |
| [!UICONTROL Maximum Query Length] | Butiksvy | Det maximala antalet tecken som tillåts i en katalogsökning. Värdet som anges för det här alternativet måste vara kompatibelt med motsvarande intervall som anges i OpenSearch- eller Elasticsearch-konfigurationen. Om du till exempel anger värdet `300` i Adobe Commerce måste du uppdatera värdet i sökmotorkonfigurationen. Standardvärde: `128` |
| [!UICONTROL Number of top search results to cache] | Butiksvy | Antalet populära söktermer och sökresultat som ska cachelagras för snabbare svar. Om du anger värdet `0` cachelagras alla söktermer och sökresultat när de anges en andra gång. Standardvärde: `100` |
| [!UICONTROL Enable EAV Indexer] | Global | Avgör om produktindexeraren ska aktiveras eller inaktiveras. Den här funktionen förbättrar indexeringshastigheten och begränsar indexeraren från att användas av tillägg från tredje part. Standardalternativ: `Yes` för aktiverad |
| [!UICONTROL Autocomplete Limit] | Butiksvy | Det maximala antalet sökfrågor som ska visas under sökfältet för automatisk ifyllning av sökning. Om du begränsar den här mängden ökar sökningens prestanda och storleken på den visade listan minskar. Standardvärde: `8` |
| Sökmotor | Global | Identifierar den sökmotor som krävs för att bearbeta begäranden om katalogdata. Konfigurationsalternativen för sökmotorn är desamma för både OpenSearch och Elasticsearch. Alternativ: `OpenSearch` eller `Elasticsearch` |
| [!UICONTROL OpenSearch Server Hostname] | Global | Anger namnet på OpenSearch- eller Elasticsearch-värdservern. |
| [!UICONTROL OpenSearch Server Port] | Global | Anger antalet serverportar som används av OpenSearch eller Elasticsearch. Standardvärde: `9200` |
| [!UICONTROL OpenSearch Index Prefix] | Global | Tilldelar ett prefix som identifierar OpenSearch- eller Elasticsearch-indexet. Standardvärde: `magento2` |
| [!UICONTROL Enable OpenSearch HTTP Auth] | Global | Om det här alternativet är aktiverat används HTTP-autentisering för att fråga efter användarnamn och lösenord innan OpenSearch- eller Elasticsearch-servern används. Alternativ: `Yes` / `No` |
| [!UICONTROL OpenSearch HTTP Username] | Global | När _Aktivera Elasticsearch HTTP-autentisering_ är `Yes` anges användarnamnet för OpenSearch eller Elasticsearch HTTP-autentisering. |
| [!UICONTROL OpenSearch HTTP Password] | Global | När _Aktivera Elasticsearch HTTP-autentisering_ är inställt på `Yes` anger lösenordet för OpenSearch eller Elasticsearch HTTP-autentisering. |
| [!UICONTROL OpenSearch Server Timeout] | Global | Anger antalet sekunder innan en begäran till OpenSearch- eller Elasticsearch-servern tar slut. Standardvärde: `15` |
| [!UICONTROL Test Connection] |  | Validerar OpenSearch- eller Elasticsearch-anslutningen. |
| [!UICONTROL Enable Search Recommendations] | Butiksvy | Avgör om sökrekommendationer erbjuds när en sökning inte ger några resultat och visas under avsnittet `Related search terms` på sökresultatsidan. Alternativ: `Yes` / `No` <br/> Om värdet är Ja visas ytterligare alternativ för _[!UICONTROL Search Recommendations Count]_&#x200B;och&#x200B;_[!UICONTROL Shows Results Count for Each Recommendation]_. |
| [!UICONTROL Search Recommendations Count] | Butiksvy | Anger antalet söktermer som erbjuds som rekommendationer. Som standard visas inte fler än fem. |
| [!UICONTROL Show Results Count for Each Recommendation] | Butiksvy | När värdet är `Yes` visas antalet produkter som hittats för den föreslagna sökrekommendationen inom hakparenteser. Alternativ: `Yes` / `No` |
| [!UICONTROL Enable Search Suggestions] | Butiksvy | Avgör om sökförslag visas för vanliga felstavningar. När det här alternativet är aktiverat visas sökförslag för alla förfrågningar som inte ger några resultat och som visas under avsnittet `Did you mean` på sidan **Sökresultat**. Sökförslag kan påverka sökresultatet. Om värdet är `Yes` visas ytterligare alternativ för Aktivera sökrekommendationer och associerade fält. Alternativ: `Yes` / `No` |
| [!UICONTROL Search Suggestions Count] | Butiksvy | Anger antalet sökförslag som erbjuds. Till exempel: `2` |
| [!UICONTROL Show Results Count for Each Suggestion] | Butiksvy | Anger om antalet sökresultat visas för varje förslag. Beroende på temat visas numret oftast inom hakparenteser efter förslaget. Alternativ: `Yes` / `No` |
| [!UICONTROL Minimum Terms to Match] | Butiksvy | Anger ett värde som motsvarar antalet termer i frågan som sökresultaten ska matcha för att returneras. Detta ger optimala resultat och relevans för kunderna. Procentvärden motsvarar ett tal och vid behov avrundas nedåt och används som minsta antal termer som ska matchas i frågan. Värdet kan vara ett negativt eller positivt heltal, ett negativt eller ett positivt tal, en kombination av de två eller flera kombinationerna. Mer information finns i [minimum_should_match-parametern](https://opensearch.org/docs/latest/query-dsl/minimum-should-match/) i OpenSearch-dokumentationen. |

## [!UICONTROL Downloadable Product Options]

![Hämtningsbara produktalternativ](./assets/catalog-downloadable-product-options.png)<!-- zoom -->

<!-- [Downloadable Product Options](https://experienceleague.adobe.com/sv/docs/commerce-admin/catalog/products/types/product-create-downloadable#configure-the-download-options) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Order Item Status to Enable Downloads] | Webbplats | Anger den status som en order måste ha innan hämtningar blir tillgängliga. Alternativ: `Pending` / `Invoiced` |
| [!UICONTROL Default Maximum Number of Downloads] | Webbplats | Fastställer standardantalet nedladdningar som är tillgängliga för en kund. |
| [!UICONTROL Shareable] | Webbplats | Avgör om kunderna måste logga in på sina konton för att komma åt nedladdningslänken. Alternativ: <br/>**Ja** - Tillåter att länken skickas via e-post, som sedan kan delas med andra. <br/>**Nej** - Kunder måste logga in på sina konton för att få åtkomst till nedladdningslänken. |
| [!UICONTROL Default Sample Title] | Butiksvy | Standardtiteln för alla exempelfiler. |
| [!UICONTROL Default Link Title] | Butiksvy | Standardlänken för alla nedladdningsbara titlar. |
| [!UICONTROL Opens Links in New Window] | Webbplats | Avgör om nedladdningslänken öppnas i ett nytt webbläsarfönster. Alternativ: `Yes` / `No` |
| [!UICONTROL Use Content Disposition] | Butiksvy | Avgör hur länken till det hämtningsbara innehållet levereras, som en e-postbilaga eller som en infogad länk i ett webbläsarfönster. Alternativ: <br/>**`Attachment`**- Hämtningslänken levereras som en e-postbilaga.<br/>**`Inline`** - Hämtningslänken levereras som en intern länk på en webbsida. |
| [!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items] | Webbplats | Avgör om gäster som köper hämtningsbara produkter måste registrera sig för ett konto och logga in för att slutföra utcheckningsprocessen. Alternativ: <br/>**`Yes`**- Om kundvagnen innehåller hämtningsbara produkter måste gästen antingen registrera sig för ett konto eller logga in på ett befintligt konto för att slutföra köpet.<br/>**`No`** - Hämtningslänken levereras som en intern länk i e-postmeddelandets brödtext.  <br/> _&#x200B;**Obs!**&#x200B;_ Gästutcheckning är bara tillgänglig för hämtningsprodukter om Delningsbar är inställt på `Yes`. |

{style="table-layout:auto"}

## [!UICONTROL Date & Time Custom Options]

![Anpassade alternativ för datum och tid](./assets/catalog-date-time-custom-options.png)<!-- zoom -->

<!-- Date & Time Custom Options](https://experienceleague.adobe.com/sv/docs/commerce-admin/catalog/product-attributes/attributes-input-types#date-and-time-options) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Use JavaScript Calendar] | Butiksvy | Avgör om JavaScript-kalendern används som indatakontroll för datumfält. Alternativ: `Yes` / `No` <br/>Om värdet är `No` visas en separat listruta för varje del av datumfältet. |
| [!UICONTROL Date Fields Order] | Butiksvy | Fastställer ordningen för de tre datumfälten. Alternativ: `Day` / `Month` / `Year` |
| [!UICONTROL Time Format] | Butiksvy | Anger tidsformatet till antingen 12 eller 24 timmar. Alternativ: `12h AM/PM` / `24h` |
| [!UICONTROL Year Range] | Butiksvy | Definierar start- och slutintervallet för år som visas i fältet _År_. Värdet måste anges i YYYY-format. |

{style="table-layout:auto"}

## [!UICONTROL Catalog Events]

{{ee-feature}}

![Kataloghändelser](./assets/catalog-events.png)<!-- zoom -->

<!-- [Catalog Events](https://experienceleague.adobe.com/sv/docs/commerce-admin/marketing/promotions/events/events-private-sales) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Catalog Events Functionality] | Webbplats | Avgör om händelsemodulen är aktiverad. |
| [!UICONTROL Enable Catalog Event Widget on Frontend] | Butiksvy | Avgör om händelsewidgeten är tillgänglig i butiken. Detta är ett statiskt block med information om händelser på din plats. |
| [!UICONTROL Number of Events to be Displayed in the Event Slider Widget] | Butiksvy | Anger antalet händelser som visas i widgeten för händelseglaget på kategorisidorna. Om du vill åsidosätta använder du variabeln `limit="x"`. |
| [!UICONTROL Events to Scroll per Click in Event Slider Widget] | Butiksvy | Anger antalet händelser som ska visas i händelseglagwidgeten på CMS-sidor, t.ex. hemsidan. Om du vill åsidosätta använder du variabeln `scroll="x"`. |

{style="table-layout:auto"}

## [!UICONTROL Rule-Based Product Relations]

{{ee-feature}}

![Regelbaserade produktrelationer](./assets/catalog-rule-based-product-relations.png)<!-- zoom -->

<!-- [Rule-Based Product Relations](https://experienceleague.adobe.com/sv/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Maximum Number of Products in Related Products List] | Global | Avgör det maximala antalet produkter som kan visas i listan _Relaterade produkter_. |
| [!UICONTROL Show Related Products] | Global | Avgör vilken lista över relaterade produkter som visas i butiken. Det kan vara antingen den lista som väljs manuellt i produktinformationen, den lista som skapas som svar på en produktrelationsregel eller en kombination av de två. Alternativ: `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Related Products List] | Global | Anger i vilken ordning produkterna i listan _Relaterade produkter_ visas. Alternativ: `Do not rotate` / `Shuffle` |
| [!UICONTROL Maximum Number of Products in Cross-Sell Product List] | Global | Anger det maximala antalet produkter som kan visas i korsförsäljningslistan. |
| [!UICONTROL Show Cross-Sell Products] | Global | Avgör vilken lista över korsförsäljningsprodukter som visas i butiken. Det kan vara antingen den lista som väljs manuellt i produktinformationen, den lista som skapas som svar på en produktrelationsregel eller en kombination av de två. Alternativ: `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Cross-Sell Products List] | Global | Bestämmer i vilken ordning produkterna i korsförsäljningslistan visas. Alternativ: Rotera inte/Blanda inte |
| [!UICONTROL Maximum Number of Products in Upsell Product List] | Global | Avgör det maximala antalet produkter som kan visas i listan _Merförsäljning_. |
| [!UICONTROL Show Upsell Products] | Global | Avgör vilken lista över merförsäljningsprodukter som visas i butiken. Det kan vara antingen den lista som väljs manuellt i produktinformationen, den lista som skapas som svar på en produktrelationsregel eller en kombination av de två. Alternativ: `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Upsell Product List] | Global | Anger i vilken ordning produkterna i Upsell Product list visas. Alternativ: `Do not rotate` / `Shuffle` |

{style="table-layout:auto"}
