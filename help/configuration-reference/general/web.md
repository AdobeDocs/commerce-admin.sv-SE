---
title: '[!UICONTROL General] &gt; [!UICONTROL Web]'
description: Granska konfigurationsinställningarna på [!UICONTROL General] &gt; [!UICONTROL Web] sidan för Commerce Admin.
exl-id: 1809b03a-a55c-41b4-947b-f66f4bd290a1
feature: Site Management, Configuration
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1795'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Web]

{{config}}

## [!UICONTROL URL Options]

![Webb > Allmänna alternativ](./assets/web-url-options.png)<!-- zoom -->

<!-- [URL Options configuration settings](https://docs.magento.com/user-guide/stores/store-urls.html) -->

| Fält | Omfång | Beskrivning |
|  ---  |  ---  |  ---  |
| [!UICONTROL Add Store Code to URLs] | Global | Om Rewrites för webbserver är aktiverat infogar Store-koden för den aktuella vyn i URL:en. Alternativ: `Yes` / `No`. <br />När det här fältet är inställt på `Yes`måste du inkludera butikskoder i webbläsarens URL:er för att säkerställa att URL-omskrivningar mappas korrekt och att alla sidor öppnas korrekt. Det här undviker du _404 Sidan hittades inte_ fel. |
| [!UICONTROL Auto-redirect to Base URL] | Butiksvy | (För inställningar för en enskild butik) Om det finns en bruten länk på din webbplats dirigerar om trafiken till bas-URL:en i stället för till en sida med meddelandet&quot;Hittar inte 404 sida&quot;. Alternativ:` No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br />**_Viktigt:_**Använd inte automatisk omdirigering till bas-URL för inställningar för flera lager. |
| [!UICONTROL Catalog media URL format] | Global | Definierar [URL-format](../../catalog/catalog-urls.md) som tilldelats produkter och kategorier. Alternativ: Unik hash per bildvariant (äldre läge) definierar det konverterade filnamnet som ett unikt hash-värde. Bildoptimering baserad på frågeparametrar definierar [bildoptimering](../../content-design/media-gallery-image-optimization.md) process beroende på frågeparametrar. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![Webb > Sökmotoroptimering](./assets/web-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization configuration settings](https://docs.magento.com/user-guide/marketing/url-rewrite.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Use Web Server Rewrites] | Butiksvy | PHP-baserade system innehåller vanligtvis en fil som kallas `index.php` i rotmappen. Som standard visas filnamnet i URL:en precis efter namnet på rotmappen. När detta är aktiverat utelämnas systemet `index.php` från webbadressen. Denna användbarhet gör varje URL mer koncis och påverkar inte prestanda eller rangordning. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Base URLs]

![Webb > Bas-URL](./assets/web-base-urls.png)<!-- zoom -->

<!-- [Base URLS configuration settings](https://docs.magento.com/user-guide/stores/store-urls.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Base URL] | Butiksvy | Den fullständiga adressen till Commerce-rotmappen som inte körs över en krypterad kanal (SSL). URL:en måste avslutas med ett snedstreck. |
| [!UICONTROL Base Link URL] | Butiksvy | En tagg som används som platshållare för bas-URL:en. |
| [!UICONTROL Base URL for Static View Files] | Butiksvy | En sökväg som pekar på platsen för statiska filer som används av temat, t.ex. CSS, teckensnitt, bilder och JavaScript. En platshållare används för att representera bas-URL. Om din Commerce-installation har flera platser med samma mappstruktur kan du ha olika mappar för varje plats. Ställ in konfigurationsomfånget på rätt plats innan du anger bas-URL:en för statiska vyfiler. Du kan även ange en mapp utanför din Commerce-installation. |
| [!UICONTROL Base URL for User Media Files] | Butiksvy | En sökväg som pekar på platsen för katalogbilder och andra mediefiler. En platshållare används för att representera bas-URL. Om din Commerce-installation har flera webbplatser med samma mappstruktur kan du ha olika mediamappar för var och en av dem. Detta ger dig möjlighet att säkerhetskopiera och återställa varje mediemapp separat. Du kan även ange en mediamapp utanför din Commerce-installation. |

{style="table-layout:auto"}

## [!UICONTROL Base URLs (Secure)]

![Webb > Bas-URL:er (säkra)](./assets/web-base-urls-secure.png)<!-- zoom -->

<!-- [Base URLs (Secure) configuration settings](https://docs.magento.com/user-guide/stores/store-urls.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Secure Base URL] | Butiksvy | Den fullständiga adressen till Commerce-rotmappen som levereras med krypterat SSL-/TLS-protokoll. URL:en måste avslutas med ett snedstreck. |
| [!UICONTROL Secure Base Link URL] | Butiksvy | En tagg som används som platshållare för bas-URL:en som körs över en säker kanal. |
| [!UICONTROL Secure Base URL for Static View Files] | Butiksvy | En tagg som pekar på platsen för statiska filer som CSS, teckensnitt, bilder och JavaScript som används av temat. Filerna kan finnas på en osäker eller säker kanal. Om din Commerce-installation har flera platser med samma mappstruktur kan du ha olika mappar för varje plats. Ställ in konfigurationsomfånget på rätt plats innan du anger bas-URL:en för statiska vyfiler. Du kan även ange en mapp utanför din Commerce-installation. |
| [!UICONTROL Secure Base URL for User Media Files] | Butiksvy | En sökväg som pekar på platsen för katalogbilder och andra mediefiler. Filerna kan finnas på en osäker eller säker kanal. En platshållare används för att representera bas-URL. Om din Commerce-installation har flera webbplatser med samma mappstruktur kan du ha olika mediamappar för var och en av dem. Detta ger dig möjlighet att säkerhetskopiera och återställa varje mediemapp separat. Du kan även ange en mediamapp utanför din Commerce-installation. |
| [!UICONTROL Use Secure URLs on Storefront] | Butiksvy | Om din domän har ett säkerhetscertifikat kan du välja att köra butiken med eller utan SSL-kryptering. Alternativ:<br />**`Yes`**- Lagra URL:er börjar med `https` för att ange att sidan levereras med krypterat, säkert protokoll.<br />**`No`** - Lagra URL:er börjar med `http` för att ange att sidan levereras utan säkert protokoll. |
| [!UICONTROL Use Secure URLs in Admin] | Global | Om din domän har ett säkerhetscertifikat kan du välja att köra arkivadministratören, med eller utan SSL-kryptering. Alternativ: <br />**`Yes`**- Admin-URL:er börjar med `https` för att ange att sidan levereras med krypterat, säkert protokoll.<br />**`No`** - Admin-URL:er börjar med `http` för att ange att sidan levereras utan säkert protokoll.<br /> När säkra URL:er är aktiverade för både butiken och administratören visas ytterligare två fält för att aktivera och konfigurera `HSTS`. |
| [!UICONTROL Enable HTTP Strict Transport Security (HSTS)] | Butiksvy | När det är aktiverat [`HSTS`][1] tillhandahåller ett mått på säkerheten mot &quot;man in the middle&quot;-attacker och förhindrar användare från att åsidosätta meddelandet &quot;invalid certificate&quot;. Alternativ: `Yes` / `No` |
| [!UICONTROL Upgrade Insecure Requests] | Butiksvy | När det här alternativet är aktiverat konverteras osäkra (`HTTP`) begäranden som tas emot från webbläsaren till den säkra (`HTTPS`). Alternativ: `Yes` / `No` |
| [!UICONTROL Offloader Header] | Global | Anger `offloader_header` i serverkonfigurationen för att identifiera protokollet mellan klienten och belastningsutjämnaren. De flesta Commerce-installationer använder standardvärdet, `X-Forwarded-Proto` (XFP) för att identifiera protokollet som antingen `HTTP` eller `HTTPS`. |

{style="table-layout:auto"}

## [!UICONTROL Default Pages]

![Webb > Standardsidor](./assets/web-default-pages.png)<!-- zoom -->

<!-- [Default Pages configuration settings](https://docs.magento.com/user-guide/cms/pages-default.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Default Web URL] | Butiksvy | Anger landningssidan som är associerad med bas-URL:en. Detta anges som standard till &quot;cms&quot; för att ange en sida från Commerce Content Management System (CMS). Du kan också använda en annan typ av landningssida, till exempel en blogg. Om till exempel en blogg är installerad på servern på `magento/blog`kan du ange namnet på bloggmappen som en relativ sökväg till urvalet av sidor. |
| [!UICONTROL CMS Home Page] | Butiksvy | Om du vill välja butikens hemsida väljer du bara CMS-sidan i listan. Som standard visas hela urvalet av CMS-sidor som är tillgängliga för din butik på CMS-startsidan. |
| [!UICONTROL Default No-route URL] | Butiksvy | Innehåller URL-adressen till den standardsida som du vill ska visas när en `404 Page not Found` ett fel inträffar. Standardvärdet är `cms/noroute/index`. |
| [!UICONTROL CMS No Route Page] | Butiksvy | Identifierar en specifik CMS-sida som du vill ska visas när ett fel av typen 404 Sidan hittades inte inträffar. Standardsidan är 404 Hittades inte. |
| [!UICONTROL CMS No Cookies Page] | Butiksvy | Identifierar en specifik CMS-sida som visas när cookies inte är aktiverade för webbläsaren. På sidan förklaras varför cookies används och hur du aktiverar dem för varje webbläsare. Standardsidan är Aktivera cookies. |
| [!UICONTROL Show Breadcrumbs for CMS Pages] | Butiksvy | Avgör om ett spårningsspår visas på alla CMS-sidor i katalogen. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Default Layouts]

![Standardlayouter](./assets/web-default-layouts.png)<!-- zoom -->

<!--[Default Layouts](https://docs.magento.com/user-guide/design/page-layout.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Default Product Layout] | Global | Bestämmer [layout](../../content-design/page-layout.md) som används som standard för produktsidor. Alternativ: <br/>**`No layout updates`**- Som standard är layoutuppdateringar inte tillgängliga för produktsidor.<br/>**`Empty`** - I används som standard en tom layout för produktsidor. <br/>**`1 column`**- I används som standard en enda kolumnlayout för produktsidor.<br/>**`2 columns with left bar`** - I används som standard en layout med två kolumner och sidofältet till vänster för produktsidor. <br/>**`2 columns with right bar`**- I används som standard en layout med två kolumner och sidofältet till höger för produktsidor.<br/>**`3 columns`** - I används som standard en layout med tre kolumner och sidofält till vänster och höger för produktsidor.<br/>**`Page -- Full Width`**- (Kräver [!DNL Page Builder]) Som standard används layouten Sida - Full bredd för produktsidor i .<br/>**`Category - Full Width`** - (Kräver [!DNL Page Builder]) I används som standard layouten Kategori - hel bredd för produktsidor. <br/>**`Product - Full Width`**- (Kräver [!DNL Page Builder]) I används som standard layouten Produkt - hel bredd för produktsidor. |
| [!UICONTROL Default Category Layout] | Global | Bestämmer [layout](../../content-design/page-layout.md) som används som standard för kategorisidor. Alternativ: <br/>**`No layout updates`**- Som standard är layoutuppdateringar inte tillgängliga för kategorisidor.<br/>**`Empty`** - I används som standard en tom layout för kategorisidor. <br/>**`1 column`**- I används som standard en enda kolumnlayout för kategorisidor.<br/>**`2 columns with left bar`** - I används som standard en layout med två kolumner och sidofältet till vänster för kategorisidor. <br/>**`2 columns with right bar`**- I används som standard en layout med två kolumner och sidofältet till höger för kategorisidor.<br/>**`3 columns`** - I används som standard en layout med tre kolumner och sidofält till vänster och höger för kategorisidor.<br/>**`Page - Full Width`**- (Kräver [!DNL Page Builder]) Som standard används layouten Sida - Full bredd för kategorisidor i .<br/>**`Category - Full Width`** - (Kräver [!DNL Page Builder]) I används som standard layouten Kategori - hel bredd för kategorisidor. <br/>**`Product - Full Width`**- (Kräver [!DNL Page Builder]) I används som standard layouten Produkt - hel bredd för kategorisidor. |
| Standardsidlayout | Global | Bestämmer [layout](../../content-design/page-layout.md) som används som standard för CMS-sidor. Alternativ: <br/>**`No layout updates`**- Som standard är layoutuppdateringar inte tillgängliga för CMS-sidor.<br/>**`Empty`** - I används som standard en tom layout för CMS-sidor. <br/>**`1 column`**- I används som standard en enda kolumnlayout för CMS-sidor.<br/>**`2 columns with left bar`** - I används som standard en layout med två kolumner och sidofältet till vänster för CMS-sidor.<br/>**`2 columns with right bar`**- I används som standard en layout med två kolumner och sidofältet till höger för CMS-sidor.<br/>**`3 columns`** - I används som standard en layout med tre kolumner och sidofält till vänster och höger för CMS-sidor.<br/>**`Page - Full Width`**- (Kräver [!UICONTROL Page Builder]) Som standard används layouten Sida - Full bredd för CMS-sidor i .<br/>**`Category - Full Width`** - (Kräver [!UICONTROL Page Builder]) I används som standard layouten Kategori - hel bredd för CMS-sidor. <br/>**`Product - Full Width`**- (Kräver [!DNL Page Builder]) I används som standard layouten Produkt - Full bredd för CMS-sidor. |

{style="table-layout:auto"}

## [!UICONTROL Default Cookie Settings]

![Webb > Standardinställningar för cookie](./assets/web-default-cookie-settings.png)<!-- zoom -->

<!-- [Default Cookie configuration settings](https://docs.magento.com/user-guide/stores/compliance-cookie-law.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Cookie Lifetime] | Butiksvy | Anger hur länge en cookie kan finnas innan den tas bort automatiskt. Standardvärdet är 3 600 sekunder (1 timme) |
| [!UICONTROL Cookie Path] | Butiksvy | Anger de mappar på servern där Commerce-cookies kan användas. Om du vill göra Commerce-cookies tillgängliga överallt i installationen anger du Cookie-sökvägen till ett enda snedstreck: `/`. Detta värde får endast innehålla cookie-sökvägen, och **_inte_** innehåller andra cookie-parametrar. |
| [!UICONTROL Cookie Domain] | Butiksvy | Avgör om Commerce-cookies är tillgängliga för underdomäner. För att t.ex. stödja `mysubdomain`.domain.com anger du namnet på din domän med en punkt i början, som `.domain.com`. Det här värdet får endast innehålla cookie-domänen, och **_inte_** innehåller andra cookie-parametrar. |
| [!UICONTROL Use HTTP Only] | Butiksvy | Avgör om Commerce Cookies bara kan användas över en osäker kanal (http), eller också kan användas över en krypterad kanal (https). Alternativ: `Yes` / `No` |
| [!UICONTROL Cookie Restriction Mode] | Webbplats | Avgör om läget för begränsning av cookie är aktiverat. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Session Validation Settings]

![Webb > Sessionsvalidering](./assets/web-session-validation-settings.png)<!-- zoom -->

<!-- [Session Validation configuration settings](https://docs.magento.com/user-guide/stores/security-session-validation.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Validate REMOTE_ADDR] | Global | Verifierar att IP-adressen för en begäran matchar `$_SESSION` data. Sessionen avslutas om en annan IP-adress upptäcks. Alternativ: `Yes` / `No` |
| [!UICONTROL Validate HTTP_VIA] | Global | Verifierar inkommande proxydata och kontrollerar att proxyadressen för en begäran matchar `$_SESSION` data. Sessionen avslutas om en annan proxyadress upptäcks. Alternativ: `Yes` / `No` |
| [!UICONTROL Validate HTTP_x_FORWARDED_FOR] | Global | Verifierar utgående proxydata och kontrollerar att den vidarebefordrade adressen för en begäran matchar  `$_SESSION` data. Sessionen avslutas om en annan adress för vidarebefordrad har identifierats. Alternativ: `Yes` / `No` |
| [!UICONTROL Validate HTTP_USER_AGENT] | Global | `USER_AGENT` hänvisar till den webbläsare eller enhet som används för att komma åt webbplatsen. Den verifierar att namnet och versionen på webbläsaren och operativsystemet matchar `$_SESSION` data. Sessionen avslutas om en annan användaragent identifieras från en begäran till en annan i samma session. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Browser Capabilities Detection]

![Webb > Identifiering av webbläsarfunktioner](./assets/web-browser-capabilities-detection.png)<!-- zoom -->

<!-- [Browser Capabilities Detection configuration settings](https://docs.magento.com/user-guide/stores/security-browser-capabilities-detection.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Redirect to CMS-page if Cookies are Disabled] | Butiksvy | Om cookies är inaktiverade i webbläsaren dirigeras de automatiskt om till CMS-sidan Inga cookies. Alternativ: `Yes` / `No` |
| [!UICONTROL Show Notice if JavaScript is Disabled] | Butiksvy | Om JavaScript är inaktiverat i webbläsaren visas ett meddelande som uppmanar användaren att aktivera JavaScript-alternativ: `Yes` / `No` (inaktiveras) |
| [!UICONTROL Show Notice if Local Storage is Disabled] | Butiksvy | Visar ett meddelande om den lokala cachen är inaktiverad. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

[1]: https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
