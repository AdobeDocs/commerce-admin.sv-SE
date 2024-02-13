---
title: Katalog- och produkt-URL:er
description: Lär dig mer om URL-formattyperna för dina katalogprodukter och hur du konfigurerar dem.
exl-id: 47405dc6-9b5e-4ca8-87eb-5a222de40793
feature: Catalog Management, Products, Search, Categories
source-git-commit: 11d78b7d7b548c373cfe0ec398814994c3e99e7a
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 0%

---

# Katalog- och produkt-URL:er

De URL:er du tilldelar till produkter och kategorier spelar en viktig roll när det gäller att avgöra hur bra webbplatsen indexeras av sökmotorer. Innan du börjar skapa katalogen bör du överväga de tillgängliga alternativen. Om du vill visa det aktuella URL-formatet går du till butiken och navigerar till valfri produkt i katalogen. URL-adressens format beror på de aktuella konfigurationsinställningarna och den metod som du använder för att hitta sidan.

## URL-format

### Dynamisk URL

En dynamisk URL skapas _i farten_ och kan innehålla en frågesträng med variabler för produkt-ID:t, sorteringsordningen och sidan där förfrågan gjordes. När en kund söker efter en produkt i din butik kan den resulterande URL:en se ut ungefär så här:

- `http://mystore.com/catalogsearch/result/?q=racer+back`
- `http://mystore.com/women/tops-women.html?style_general=135`

### Statisk URL

En statisk URL är en fast adress för en viss sida. En statisk URL kan visas i ett sökmotorvänligt format eller en som refererar produkter och kategorier efter ID. Dessa URL:er innehåller ord som andra kan använda för att söka efter en produkt och som kräver att omskrivningar av webbservern är aktiverade. Filer med statiska URL:er används ofta för produkt- och kategorisidor, innehållssidor och [temaresurser](../content-design/theme-assets.md).

- `http://mystore.com/antonia-racer-tank.html`

## URL-komponenter

### URL-nyckel

URL-nyckeln är en del av en statisk URL som beskriver produkten eller kategorin. När du skapar en produkt eller kategori genereras en inledande URL-nyckel automatiskt baserat på namnet. Information om hur du ändrar URL-nyckeln finns i [Sökmotoroptimering](product-search-engine-optimization.md) i produktinformationen.

>[!NOTE]
>
>Som standard ersätts specialtecken med accent automatiskt med sina vanliga versioner utan accent i URL-tangenten. Till exempel: `ñ` ersätts automatiskt av `n`. Det här beteendet kan inaktiveras genom att ställa in _[!UICONTROL Search Engine Optimization: Apply transliteration for product URL]_konfigurationsalternativ till `No`. Se [Konfigurera katalog-URL](#configure-catalog-urls).

URL-nyckeln ska bestå av gemener med bindestreck som inte är avslutande mellan dessa tecken för att avgränsa ord. Bindestreck tillåts inte i början eller slutet av URL-nyckeln. En väldesignad, &quot;sökmotorvänlig&quot; URL-nyckel kan innehålla produktnamn och nyckelord för att förbättra det sätt på vilket den indexeras av sökmotorer. URL-nyckeln kan konfigureras för att skapa en automatisk omdirigering om URL-nyckeln ändras.

>[!NOTE]
>
>Information om hur du utökar URL-anpassningar, t.ex. lokaliserade URL-adresser, finns i [URL-omskrivning](../merchandising-promotions/url-rewrite.md) för mer information.

### HTML suffix

Katalogen kan konfigureras så att suffixet antingen inkluderas eller exkluderas som en del av kategori- och produkt-URL:er. Det finns olika anledningar till att folk kan välja att använda eller utelämna suffixet. Vissa anser att suffixet inte längre har något användbart syfte och att sidor utan suffix indexeras mer effektivt av sökmotorer. Företaget kan dock ha ett standardiserat format för URL:er som kräver ett suffix.

Eftersom suffixet styrs av systemkonfigurationen bör du aldrig skriva det direkt i URL-nyckeln för en kategori eller produkt. (Om du gör det får du ett dubbelt suffix i slutet av URL:en.) Oavsett om du bestämmer dig för att använda suffixet eller inte bör du vara konsekvent och använda samma inställning för alla produkt- och kategorisidor. Här är exempel på URL:er med - och utan - ett suffix.

#### URL med suffix för HTML

- `http://mystore.com/helena-hooded-fleece.html`
- `http://mystore.com/helena-hooded-fleece.htm`

#### URL utan HTML-suffix

- `http://mystore.com/helena-hooded-fleece`

### Kategorisökväg

Du kan konfigurera URL:en så att den antingen inkluderar eller exkluderar kategorins sökväg. Som standard inkluderas kategorisökvägen i alla kategorier och produktsidor. I följande exempel visas samma produkt-URL med, och utan, kategorisökväg.

#### URL med kategorisökväg

- `http://mystore.com/women/tops-women/hoodies-and-sweatshirts-women/helena-hooded-fleece.html`

#### URL utan kategorisökväg

- `http://mystore.com/helena-hooded-fleece.html`

Om du inte vill att sökmotorer ska kunna indexera flera URL:er som leder till samma innehåll, kan du utesluta kategorisökvägen från URL:en. En annan metod är att använda en kanonisk meta-tagg för att låta sökmotorer veta vilka URL:er som ska indexeras och vilka som ska ignoreras. Som standard inkluderar Commerce inte kategorisökvägen i produkt-URL:er.

## Konfigurera katalog-URL

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Search Engine Optimizations]** och ange alternativ:

   - Ange **[!UICONTROL Product URL Suffix]** till `html` eller `htm`. Ange suffixet utan punkt eftersom det tillämpas automatiskt.

   - Ange **[!UICONTROL Category URL Suffix]** till `html` eller `htm`. Ange suffixet utan punkt eftersom det tillämpas automatiskt.

   - Ange **[!UICONTROL Use Categories Path for Product URLs]** efter dina önskemål.

   ![Sökmotoroptimering](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   En detaljerad lista över dessa alternativ finns på [Sökmotoroptimering](../configuration-reference/catalog/catalog.md#search-engine-optimization) i _Konfigurationsreferens_.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

1. När du uppmanas till det klickar du på **[!UICONTROL Cache Management]** i systemmeddelandet och uppdatera den ogiltiga cachen.

   ![Uppdatera cache](./assets/msg-cache-management.png){width="450" zoomable="yes"}

   Mer information om de här alternativen finns i [Uppdatera cacher](../systems/cache-management.md#refresh-specific-caches).

## Konfigurera katalogmediets URL-format

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL General]** och välja **[!UICONTROL Web]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Url Options]** och ange alternativ:

![Webb > Allmänna alternativ](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

| Fält | [Omfång](../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Add Store Code to URLs] | Global | Om återskrivningar av webbservrar är aktiverade, infogar den här inställningen Store-koden för den aktuella vyn i URL:en. Alternativ: `Yes` / `No` |
| [!UICONTROL Auto-redirect to Base URL] | Global | (För inställningar för en enskild butik) Om det finns en trasig länk på din webbplats dirigeras trafiken till bas-URL:en i stället för till en sida med meddelandet&quot;Hittar inte 404 sida&quot;. Alternativ: `No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br /><br />**_Viktigt!_**Använd inte automatisk omdirigering till bas-URL för inställningar för flera lager. |
| [!UICONTROL Catalog media URL format] | Global | Definierar det URL-format som tilldelats produkter och kategorier. Alternativ: <br />**[!UICONTROL Unique hash per image variant (Legacy mode)]**- Definierar det konverterade filnamnet som ett unikt hash-värde.<br />**[!UICONTROL Image optimization based on query parameters]** - Definierar [bildoptimering](../content-design/media-gallery-image-optimization.md) process beroende på frågeparametrar. |

{style="table-layout:auto"}
