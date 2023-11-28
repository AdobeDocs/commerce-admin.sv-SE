---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL Developer]'
description: Granska konfigurationsinställningarna på [!UICONTROL Advanced] &gt; [!UICONTROL Developer] sidan för Commerce Admin.
exl-id: 2ef4ba6a-b5a5-419d-8d61-e535e3366370
role: Admin, Developer
feature: Site Management, Configuration, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# [!UICONTROL Advanced] > [!UICONTROL Developer]

{{config}}

>[!NOTE]
>
>Dessa konfigurationsinställningar är tillgängliga i [utvecklarläge](../../systems/developer-tools.md#operation-modes) endast.

## [!UICONTROL Frontend Development Workflow]

![Frontend Development Workflow](./assets/developer-frontend-development-workflow.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Utvecklingsarbetsflöde](../../systems/developer-tools.md#frontend-development-workflow) i _Handbok för adminsystem_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Workflow Type] | Global | Avgör om mindre kompilering sker på klient- eller serversidan under utvecklingen. Alternativ: <br/>**`Client side less compilation`**- Kompileringen görs i webbläsaren med hjälp av det inbyggda biblioteket less.js.<br/>**`Server side less compilation`** - Kompilering görs på servern med hjälp av Less PHP-biblioteket. Det här är standardläget för produktion. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Developer Client Restrictions]

![Begränsningar för utvecklarklienter](./assets/developer-developer-client-restrictions.png)<!-- zoom -->

Mer information om hur du ändrar den här inställningen finns i [Klientbegränsningar](../../systems/developer-tools.md#client-restrictions) i _Handbok för adminsystem_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Allow IPs (comma separated)] | Butiksvy | Skapar en tillåtelselista IP-adresser som kan använda utvecklarverktyg på en aktiv webbplats, utan att störa kunderna i butiken. Ändringar av webbplatsen när du använder ett utvecklarverktyg som _Textbunden översättning_, visas bara från IP-adresserna till tillåtelselista. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Template Settings]

![Mallinställningar](./assets/developer-template-settings.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Optimera resursfiler](../../systems/developer-tools.md#optimizing-resource-files) i _Handbok för adminsystem_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Allow Symlinks] | Butiksvy | Aktivering [symboliska länkar](https://en.wikipedia.org/wiki/Symbolic_link) kan utsätta sajten för säkerhetsrisker och rekommenderas inte för ett produktionslager. |
| [!UICONTROL Minify Html] | Butiksvy | Anger om HTML för butiksmallar är minimerad. Alternativ: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Debug]

![Felsök](./assets/developer-debug.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Tips för mallsökväg](../../systems/developer-tools.md#template-path-hints) i _Handbok för adminsystem_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Template Path Hints for Storefront] | Butiksvy | Lägger till en notation i storefront som anger sökvägen till varje mall som används på sidan. Alternativ: `Yes` / `No` |
| [!UICONTROL Enable Template Path Hints for Admin] | Global | Lägger till en anteckning i administratören som anger sökvägen till varje mall som används på sidan. Alternativ: `Yes` / `No` |
| [!UICONTROL Add Block Class Type to Hints] | Butiksvy | Inkluderar namnen på blocken i mallsökvägstipsen. Alternativ: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Translate Inline]

![Översätt textbundet](./assets/developer-translate-inline.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Översätt textbundet](../../systems/developer-tools.md#translate-inline) i _Handbok för adminsystem_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable for Storefront] | Butiksvy | Aktiverar den textbundna översättaren för butiken. Gränssnittstexten kan redigeras för varje butiksvy. Om du vill använda den infogade översättaren utan att störa livebutiken lägger du till din IP-adress i tillåtelselista Developer Client Restrictions. |
| [!UICONTROL Enable for Admin] | Global | Aktiverar den infogade översättaren för administratören. Till skillnad från butiken kan administratören inte översättas till flera språk. Fältetiketterna och annan text i gränssnittet kan dock ändras. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL JavaScript Settings]

![JavaScript-inställningar](./assets/developer-javascript-settings.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Optimera resursfiler](../../systems/developer-tools.md#optimizing-resource-files) i _Handbok för adminsystem_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Merge JavaScript Files] | Butiksvy | Sammanfogar flera JavaScript-filer till en enda fil för att förbättra sidinläsningstiden. |
| [!UICONTROL Enable JavaScript Bundling] | Butiksvy | Avgör om flera JavaScript-filer kan paketeras i en fil. Alternativ: `Yes` / `No` |
| [!UICONTROL Minify JavaScript Files] | Butiksvy | Onödiga tecken, blanksteg och indrag tas bort för att minska storleken på koden. |
| [!UICONTROL Move JS code to the bottom of the page] | Global | Om det här alternativet är aktiverat flyttas JS-koden längst ned på sidan. Alternativ: `Yes` / `No` |
| [!UICONTROL Translation Strategy] | Global | Bestämmer översättningsmetoden som används av systemet. Alternativ: <br/>**`Dictionary`**- Translation on storefront side.<br/>**`Embedded`** - Översättning på adminsidan. |
| [!UICONTROL Log JS Errors to Session Storage] | Global | Om det här alternativet är aktiverat kan användas i funktionstester för rapportering. Alternativ: `Yes` / `No` |
| [!UICONTROL Log JS Errors to Session Storage Key] | Global | Identifierar nyckeln som används för att hämta insamlade js-fel. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL CSS Settings]

![CSS-inställningar](./assets/developer-css-settings.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Optimera resursfiler](../../systems/developer-tools.md#optimizing-resource-files) i _Handbok för adminsystem_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Merge CSS Files] | Butiksvy | Sammanfogar flera CSS-filer till en enda fil för att förbättra sidinläsningstiden. Alternativ: `Yes` / `No` |
| [!UICONTROL Minify CSS Files] | Butiksvy | Onödiga tecken, blanksteg och indrag tas bort för att minska storleken på koden. Alternativ: `Yes` / `No` |
| [!UICONTROL Use CSS critical path] | Global | The _CSS-kritisk sökväg_ levererar minierad kritisk CSS inline i `<head>` och definierar alla icke-kritiska format som läses in asynkront. Alternativ: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Image Processing Settings]

![Inställningar för bildbearbetning](./assets/developer-image-processing-settings.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Image Adapter] | Global | Anger det kort som används för att återge bilder. När du har ändrat adapterinställningen tömmer du cachen för katalogbilder. Alternativ: `PHP GD2` / `ImageMagick` <br/><br/>**_Obs!_**ICO-filtypen stöds bara av ImageMagik-adaptern. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Caching Settings]

![Inställningar för cachelagring](./assets/developer-cache-settings.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Cache User Defined Attributes] | Global | När det här alternativet är aktiverat cachelagras användardefinierade attribut och EAV-attribut (System Entity Attribute Value). Det här alternativet kan öka prestandan men kräver även mer utrymme för cachelagring. Alternativ: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Static Files Settings]

![Inställningar för statiska filer](./assets/developer-static-files-settings.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Sign Static Files] | Global | När det här alternativet är aktiverat läggs en digital signatur till i URL:en för statiska filer så att webbläsarna kan identifiera när en nyare version av filen är tillgänglig. Om en fils signatur skiljer sig från vad som lagras i webbläsarens cache, används den nyare versionen av filen. Statiska filer som kan signeras är JavaScript, CSS, bilder och teckensnitt. Alternativ: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Grid Settings]

![Stödrasterinställningar](./assets/developer-grid-settings.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Asynchronous Indexing|Global] | Avgör när enheter i orderhanteringssystemet, t.ex. order, fakturor, leveranser och kreditnotor, läggs till i rutnätet och indexeras om. Asynkron indexering kan användas för att undvika lås på data under sparåtgärder och för att minska bearbetningstiden. Alternativ: <br/>**`Disable`**- (Standard) Orderrelaterade enheter läggs till i rutnätet vid olika tillfällen. när de sparas.<br/>**`Enable`** - Orderrelaterade entiteter läggs bara till i rutnätet under ett schemalagt cron-jobb. Cron ska konfigureras att köras en gång i minuten. |

{:style=&quot;table-layout:auto&quot;}
