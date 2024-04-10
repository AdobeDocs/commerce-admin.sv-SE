---
title: Cachehantering
description: Lär dig hur du använder verktygen för cachehantering, som är ett enkelt sätt att förbättra prestanda för din plats.
exl-id: c87f85ca-81b9-4cbf-9817-3d779397eefd
feature: Cache, System
source-git-commit: add2259bf326d7812999e3e7d4724af10f7497c0
workflow-type: tm+mt
source-wordcount: '1845'
ht-degree: 0%

---

# Cachehantering

Cachehanteringssystemet Adobe Commerce och Magento Open Source är ett enkelt sätt att förbättra webbplatsens prestanda. När ett cacheminne kräver en uppdatering visas ett meddelande längst upp på arbetsytan med en länk till [!UICONTROL Cache Management] sida där du kan visa och uppdatera cacheminnen.

![Spara produktattribut - uppdatera cachemeddelande](./assets/product-attribute-save-msg-update-cache.png){width="500"}

The _[!UICONTROL Cache Management]_visas status för varje primärt cacheminne och tillhörande tagg. De stora knapparna i det övre högra hörnet kan användas för att tömma cacheminnet, eller den kompletta cachelagringen. Längst ned på sidan kan du med ytterligare knappar tömma katalogproduktbildernas cache och JavaScript/CSS-cache.

>[!IMPORTANT]
>
>När katalogenheter ändras kan det påverka andra sidor och göra flera cacher ogiltiga samtidigt. När du granskar sidan för cachehantering kan du se ogiltiga objekt som behöver uppdateras när de var _**inte redigerad direkt**_. Den här ogiltigförklaringen inträffar t.ex. när du redigerar en produkt i katalogen som är tilldelad en kategori eller när du ändrar en relaterad produktregel.

När du har rensat ett cacheminne bör du alltid uppdatera webbläsaren så att du ser de senaste filerna. Webbläsarcachen rensas inte när du rensar Commerce-cachen. Du kan behöva rensa webbläsarens cache för att se uppdaterat innehåll.

Mer teknisk information om Adobe Commerce cachning finns på [Cacheöversikt](https://developer.adobe.com/commerce/frontend-core/guide/caching/){:target=&quot;_blank&quot;} i _Utvecklingshandbok för Commerce Frontend_.

Öppna _[!UICONTROL Cache Management]_gör något av följande:

- Klicka på **[!UICONTROL Cache Management]** i meddelandet ovanför arbetsytan.
- På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

![Cachehantering](./assets/cache-management-invalid.png){width="700" zoomable="yes"}

## Metodtips för cachelagring

Omindexering och cachelagring har olika syften i Commerce. [Index](index-management.md) spåra databasinformation för bättre sökprestanda, snabbare datahämtning för butiker med mera. Caches save loaded data, images, formats, and the like for enhanced performance loading and accessing the storefront.

- Töm alltid cacheminnet efter installation av tillägg/moduler. Du kan installera ett eller flera tillägg och sedan tömma cachen.
- Rensa cachen efter installation av Commerce. För nya installationer bör du även indexera om.
- Töm cacheminnet när du har uppgraderat från en version av Open Source eller Commerce till en annan.
- När du tömmer cacheminnen bör du tänka på vilken typ av cacheminne det är och schemalägga tömningen under icke-topptider. Välj till exempel en tid då få kunder får tillgång till webbplatsen, som sen natt eller tidig morgon. Om du rensar vissa cachetyper under högbelastningstider blir Admin mycket belastad och kan resultera i en nedladdad plats tills den är slutförd.
- När [omindexering](index-management.md)behöver du inte också utföra en tömningscache.

## Rollresurser för cachehantering

Användarna kan tilldelas åtkomst till specifika cacheunderhållsåtgärder per roll, inklusive alternativ för att visa, växla och tömma cacheminnen. Adobe rekommenderar att du bara aktiverar rensningsåtgärder för användare på administratörsnivå. Om du får tillgång till alla funktioner för cachehantering kan det påverka butikens prestanda.

![Rollresurser - cachehantering](./assets/permissions-role-resources-cache-management.png){width="600" zoomable="yes"}

Mer information om hur du tilldelar resurser för att bevilja åtkomst för administratörsanvändarkonton finns i [Rollresurser](permissions-user-roles.md#role-resources). Följande resurser styr åtkomsten till verktygen för cachehantering:

- [!UICONTROL Clean Cache Actions]

   - [!UICONTROL Flush Cache Storage]
   - [!UICONTROL Flush Magento Cache]

- [!UICONTROL Cache Type Management]

   - [!UICONTROL Toggle Cache Type]
   - [!UICONTROL Refresh Cache Type]

- [!UICONTROL Additional Cache Management]

   - [!UICONTROL Catalog Images Cache]
   - [!UICONTROL Flush Js/Css]
   - [!UICONTROL Flush Static Files]

## Uppdatera specifika cacheminnen

1. För varje cache som ska uppdateras markerar du kryssrutan i början av raden.

1. Ange **[!UICONTROL Actions]** till `Refresh` och klicka **[!UICONTROL Submit]**.

## Uppdatera massåtgärd

1. Om du vill välja en grupp cacheminnen anger du **[!UICONTROL Mass Actions]** till något av följande:

   - `Select All`
   - `Select Visible`

1. Markera kryssrutan för varje cache som åtgärden ska rikta sig till.

1. Ange **[!UICONTROL Actions]** till `Refresh` och klicka **[!UICONTROL Submit]**.

## Rensa produktbildcachen

1. Under _[!UICONTROL Additional Cache Management]_, klicka **[!UICONTROL Flush Catalog Images Cache]**för att rensa förgenererade produktbildfiler.

   The `Image cache was cleaned` visas högst upp på arbetsytan.

1. Rensa cacheminnet i webbläsaren.

## Töm JavaScript-/CSS-cachen

1. Under _[!UICONTROL Additional Cache Management]_, klicka **[!UICONTROL Flush JavaScript/CSS Cache]**för att rensa alla JavaScript- och CSS-filer som har slagits samman till en enda fil.

   The `The JavaScript/CSS cache has been cleaned` visas högst upp på arbetsytan.

1. Rensa cacheminnet i webbläsaren.

## Töm med kommandoraden

Systemadministratörer och utvecklare med tillgång till Commerce-programservern kan också hantera cache- och cachekonfigurationen från kommandoraden med Commerce CLI. Se [Hantera cachen](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-cache#:~:text=You%20can%20also%20clean%20and,bin%2Fmagento%20cache%3Aclean%20.) i _Konfigurationshandbok_.{:target=&quot;_blank&quot;}.

## Kontroller

| Kontroll | Beskrivning |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Mass Actions] | Markerar kryssrutan för flera cacher. Alternativ: <br/>**[!UICONTROL Select All]**— Markerar kryssrutan för alla cacheminnen.<br/>** Avmarkera alla **— Rensar kryssrutan för alla cacher.<br/>**[!UICONTROL Select Visible]** — Markerar kryssrutan för alla synliga cacheminnen. <br/>**[!UICONTROL Unselect Visible]**— Rensar kryssrutan för alla synliga cacher. |
| [!UICONTROL Actions] | Anger vilken åtgärd som ska tillämpas på alla markerade cacheminnen. Alternativ: <br/>**[!UICONTROL Enable]**— Aktiverar alla markerade cacheminnen.<br/>**[!UICONTROL Disable]** — Inaktiverar alla markerade cacher. <br/>**[!UICONTROL Refresh]**— Uppdaterar alla markerade cacheminnen. |
| [!UICONTROL Submit] | Tillämpar åtgärden på alla markerade cacheminnen. |

{style="table-layout:auto"}

### Knappar

| Knapp | Beskrivning |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Flush Magento Cache] | Tar bort alla objekt i standardcachen för Commerce (`var/cache`), enligt deras associerade Commerce-taggar. |
| [!UICONTROL Flush Cache Storage] | Tar bort alla objekt från cachen, oavsett Commerce-tagg. Om systemet använder en alternativ cacheplats tas alla cachelagrade filer som används av andra program bort. |
| [!UICONTROL Flush Catalog Images Cache] | Tar bort alla automatiskt storleksändrade och vattenstämplade katalogbilder som lagras i `media/catalog/product/cache`. Om nyligen överförda bilder inte visas i katalogen kan du försöka tömma katalogen och uppdatera webbläsaren. |
| [!UICONTROL Flush JavaScript/CSS Cache] | Tar bort den sammanfogade kopian av JavaScript- och CSS-filer från cachen. Om de senaste ändringarna av formatmallen eller JavaScript inte återspeglas i arkivet kan du försöka tömma JavaScript/CSS-cachen och uppdatera webbläsaren. |
| [!UICONTROL Flush Static Files Cache] | Tar bort förbearbetade visningsfiler och statiska filer. |

{style="table-layout:auto"}

### Cacher

The [!UICONTROL Cache Management] På sidan visas de cachetyper som du kan hantera från administratören med deras aktuella status. I det här avsnittet beskrivs de standardcachetyper som stöds av Adobe Commerce. The _Cache-tagg_ och _Cache-id_ kolumner beskriver värden som används i Commerce-programkoden:

- `cache_type_id` definierar den unika identifieraren för en cachetyp.

- `%CACHE_TYPE_TAG%` definierar den unika tagg som ska användas i cachetypsomfång.

Utvecklare och systemintegratörer använder dessa värden för att konfigurera och hantera cachning när de anpassar eller integrerar med Adobe Commerce, till exempel för att utveckla integreringar med GraphQL API:er. The `cache type id` används även för cachehantering från programserverns kommandorad med Commerce CLI, till exempel ` bin/magento cache:status config` visar aktuell status för konfigurationscachen.

>[!NOTE]
>
>Utvecklare och systemintegratörer kan anpassa och utöka Cachehanteringssystemet i Commerce för att stödja anpassade moduler och integreringar. Mer information finns i [Konfigurera cachelagring](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cache/caching-overview) i _Konfigurationshandbok för Adobe Commerce_.

<!-- prettier-ignore -->

#### Information om cachelista

| Cache | Beskrivning | Cache-tagg | Cache-id |
|-------|------------|----------|----------|
| [!UICONTROL Configuration] | Commerce samlar in XML-konfiguration från alla moduler, sammanfogar den och sparar det sammanfogade resultatet i cachen.<br>**[!UICONTROL System]**-  `config.xml`,`local.xml`<br>**[!UICONTROL Module]** - `config.xml`<br><br>Cachen innehåller även lagringsinställningar som lagras i filsystemet och databasen. Rensa eller tömma den här cachetypen efter att konfigurationsfilerna har ändrats. | `CONFIG` | `config` |
| [!UICONTROL Layouts] | Kompilerade sidlayouter, det vill säga layoutkomponenter från alla komponenter. Rensa eller tömma den här cachetypen efter att du har ändrat layoutfiler. | `LAYOUT_GENERAL_CACHE_TAG` | `layout` |
| [!UICONTROL Blocks HTML output] | HTML sidfragment per block. Rengör eller tömma den här cachetypen efter att du har ändrat visningslagret. | `BLOCK_HTML` | `block_html` |
| [!UICONTROL Collections Data] | Samla in datafiler som lagrar resultatet av databasfrågor. Om det behövs rensar Commerce cachen automatiskt, men tredjepartsutvecklare kan placera alla data i valfritt segment i cachen. Rensa eller tömma den här cachetypen om den anpassade modulen använder logik som resulterar i cacheposter som inte kan rensas. | `COLLECTION_DATA` | `collections` |
| [!UICONTROL Reflections] | Rensar API-gränssnittets reflektionsdata, som vanligtvis genereras under körning. | `REFLECTION` | `reflection` |
| `Database DDL operations` | Databasschema. Om det behövs rensar Commerce cachen automatiskt, men tredjepartsutvecklare kan placera alla data i valfritt segment i cachen. Rensa eller tömma den här cachetypen efter att du har gjort anpassade ändringar i databasschemat. (Detta är med andra ord uppdateringar som Commerce inte gör sig själv.) Ett sätt att uppdatera databasschemat automatiskt är att använda magentainställningarna:db-schema:uppgraderingskommando. | `DB_DDL` | `db_ddl` |
| [!UICONTROL Compiled Config] | Resultat av kodkompilering. | `COMPILED_CONFIG` | `compiled_config` |
| [!UICONTROL Webhooks Response Cache] | Cachelagrar svar på webkrok-begäranden. Mer information finns i [Webhooks Guide](https://developer.adobe.com/commerce/extensibility/webhooks/release-notes/#enhancements-2) i dokumentationen för Commerce-utvecklare. | `WEBHOOKS_RESPONSE` | `webhooks_response` |
| [!UICONTROL EAV types and attributes] | Deklarationscache för entitetstyper för metadata relaterade till EAV-attribut (t.ex. butiksetiketter, länkar till relaterad PHP-kod, attributåtergivning, sökinställningar osv.). Du behöver vanligtvis inte rensa eller tömma den här cachetypen. | `EAV` | `eav` |
| [!UICONTROL Customer Notification] | Tillfälliga meddelanden som visas i användargränssnittet. | `CUSTOMER_NOTIFICATION` | `customer_notification` |
| [!UICONTROL GraphQL Query Resolver Results] | Caches the results from GraphQL query resolvers for customer, CMS page, CMS block, and product media gallery entities. Låt cachen vara aktiverad för att förbättra GraphQL prestanda. | `GRAPHQL_QUERY_RESOLVER_RESULT` | `graphql_query_resolver_result` |
| [!UICONTROL Integrations Configuration] | Konfigurationsfil för integrering. Rensa eller tömma det här cacheminnet när du har ändrat eller lagt till integreringar. | `INTEGRATION` | `config_integration` |
| [!UICONTROL Integrations API Configuration] | Kompilerade API:er för integrering av butiker. | `INTEGRATION_API_CONFIG` | `config_integration_api` |
| [!UICONTROL Admin UI SDK Cache] | Cachelagrar anpassningar av administratören. Se [Administratörskonfiguration och -testning](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/configuration/) i _Handbok för administratörsgränssnitt för SDK_. | `ADMIN_UI_SDK` | `admin_ui_sdk` |
| [!UICONTROL Page Cache] | Cachelagring av hela sidor. | `FPC` | `full_page` |
| [!UICONTROL Target Rule] | Index för målregel | `TARGET_RULE` | `target_rule` |
| [!UICONTROL Web Services Configuration] | Cachelagrar webb-API-strukturen. | `WEBSERVICE` | `config_webservice` |
| [!UICONTROL Translations] | Översättningsfiler. | `TRANSLATE` | `translate` |

{style="table-layout:auto"}

## Cachelagring

Adobe Commerce och Magento Open Source använder helsidescachning på servern för att snabbt visa kategori-, produkt- och CMS-sidor. Helsidescachning förbättrar svarstiden och minskar belastningen på servern. Utan cachelagring kan varje sida behöva köra kodblock och hämta information från databasen. Om cachelagring av hela sidor är aktiverad kan en helt genererad sida dock läsas direkt från cacheminnet.

>[!NOTE]
>
>Vi rekommenderar att [Finska cache](https://varnish-cache.org/){:target=&quot;_blank&quot;} får endast användas i en produktionsmiljö.

Cachelagrat innehåll kan användas för att behandla begäranden från liknande typer av besök. Detta kan leda till att de sidor som visas för en besökare av en viss person skiljer sig från dem som visas för kunden. Vid cachelagring är varje besök en av tre typer:

- `Non-sessioned` - Vid ett icke-sessionerat besök visar kunderna sidor, men interagerar inte med butiken. Systemet cachelagrar innehållet på varje sida som visas och skickar dem till andra kunder som inte sitter bredvid varandra.
- `Sessioned` - Vid ett besök som hålls på plats tilldelas de kunder som interagerar med butiken - genom aktiviteter som att jämföra produkter eller lägga till produkter i kundvagnen - ett sessions-ID. Cachelagrade sidor som genereras under sessionen används endast av den användaren under sessionen.
- `Customer` - Kundsessioner skapas för dem som har registrerat sig för ett konto hos din butik och butik medan de är inloggade på sina konton. Under sessionen kan kunderna få specialerbjudanden, kampanjer och priser som baseras på deras tilldelade kundgrupp.

Teknisk information finns på [Konfigurera och använda lack](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/varnish/config-varnish.html){:target=&quot;_blank&quot;} och [Använd Redis för Commerce-sidan och standardcachen](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-pg-cache.html){:target=&quot;_blank&quot;} i _Konfigurationshandbok_.

**_Så här konfigurerar du helsidescachen:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL System]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Full Page Cache]** -avsnitt.

   ![Avancerad konfiguration - helsidescache](../configuration-reference/advanced/assets/system-full-page-cache.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Caching Application]** till något av följande:

   - `Built-in Application`
   - `Varnish Caching`

1. Om du vill ange timeout för sidcachen anger du **[!UICONTROL TTL for public content]**. (Standardvärdet är `86400`)

1. Ange maximalt antal [layouthandtag](https://developer.adobe.com/commerce/frontend-core/guide/layouts/#layout-handles) för att bearbeta [`{BASE-URL}/page_cache/block/esi`](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/use-varnish-esi.html) HTTP-slutpunkt, ange **[!UICONTROL Handles param size]**. Genom att begränsa storleken kan du förbättra säkerheten och prestandan. (Standardvärdet är `100`)

1. Om du använder lack fyller du i **[!UICONTROL Varnish Configuration]** enligt följande:

   - **[!UICONTROL Access list]** - Ange de IP-adresser som kan rensa lack-konfigurationen för att generera en config-fil. Avgränsa flera poster med komma. Standardvärdet är `localhost`.

   - **[!UICONTROL Backend host]** - Ange IP-adressen för den backend-värd som genererar konfigurationsfiler. Standardvärdet är `localhost`.

   - **[!UICONTROL Backend port]** - Identifiera den serverdelsport som används för att generera konfigurationsfiler. Standardvärdet är: `8080`.

   - **[!UICONTROL Grace period]** - Ange hur många sekunder som ska användas som respitperiod för att generera konfigurationsfiler. Se [Avancerad lack-konfiguration](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/config-varnish-advanced.html) i _Konfigurationshandbok_.

   - Exportera konfigurationen som en `varnish.vcl` klickar du på knappen för den version av lack som du använder.

   ![Avancerad konfiguration - helsidescache](../configuration-reference/advanced/assets/system-full-page-cache-varnish.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
