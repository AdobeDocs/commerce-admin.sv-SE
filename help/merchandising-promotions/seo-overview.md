---
title: Sökmotoroptimering
description: Läs mer om SEO-verktyg (sökmotoroptimering) för Commerce-webbplatser och metodtips för optimal SEO.
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# SEO - översikt

_Sökmotoroptimering_ (SEO) är praxis att finjustera innehållet och presentationen av en webbplats för att förbättra det sätt på vilket sidorna indexeras av sökmotorer. Handeln innehåller olika funktioner som stöder er pågående SEO-insats.

## Metadata

Läs mer om hur du lägger till och förbättrar nyckelordsinnehåll [metadata](meta-data.md) för er webbplats och butik.

## Använda en platskarta

A [webbplatskarta](sitemap-xml.md) förbättrar det sätt på vilket din butik indexeras av sökmotorer och är utformad för att hitta sidor som kan förbises av webbcrawler. En platskarta kan konfigureras för indexering av alla sidor och bilder.

## URL-omskrivningar

The [URL-omskrivning](url-rewrite.md) kan du ändra alla URL:er som är kopplade till en produkt, kategori eller CMS-sida.

## Sökrobotar

Commerce-konfigurationen innehåller inställningar för att generera och hantera instruktioner för webbcrawlningar och botar som indexerar din webbplats. Om begäran om `robots.txt` når Commerce (och inte en fysisk fil), dirigeras den dynamiskt till robotstyrningen. Instruktionerna är direktiv som känns igen och följs av de flesta sökmotorer.

Som standard innehåller filen robots.txt som genereras av Commerce instruktioner för web crawler för att undvika att indexera vissa delar av webbplatsen som innehåller filer som används internt av systemet. Du kan använda standardinställningarna eller definiera egna instruktioner för alla eller för specifika sökmotorer. Det finns många artiklar online som utforskar ämnet i detalj.

### Exempel på anpassade instruktioner

**Tillåter fullständig åtkomst**

    Användaragent:*
    Tillåt inte:

**Tillåter inte åtkomst till alla mappar**

    Användaragent:*
    Tillåt inte: /

**Standardinstruktioner**

    Användaragent: *
    Tillåt inte: /index.php/
    Tillåt inte: /*?
    Tillåt inte: /checkout/
    Tillåt inte: /app/
    Tillåt inte: /lib/
    Tillåt inte: /*.php$
    Tillåt inte: /pkginfo/
    Tillåt inte: /report/
    Tillåt inte: /var/
    Tillåt inte: /katalog/
    Tillåt inte: /kund/
    Tillåt inte: /sendvän/
    Tillåt inte: /review/
    Tillåt inte: /*SID=

### Konfigurera `robots.txt`

1. På _Administratör_ sidebar, gå till **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Hitta **[!UICONTROL Global]** -konfigurationen i stödrastrets första rad och klicka på **[!UICONTROL Edit]**.

   ![Global designkonfiguration](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. Rulla ned och expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Search Engine Robots]** och gör följande:

   ![Designkonfiguration - sökrobotar](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL Default Robots]** till något av följande:

     | Alternativ | Beskrivning |
     |------|------------|
     | `INDEX, FOLLOW` | Instruerar webbcrawlningar att indexera platsen och att checka tillbaka senare för att se ändringar. |
     | `NOINDEX, FOLLOW` | Instruerar webbcrawlningar att undvika att indexera platsen, men att senare göra ändringar. |
     | `INDEX, NOFOLLOW` | Instruerar webbcrawlningar att indexera platsen en gång, men att inte checka tillbaka senare för ändringar. |
     | `NOINDEX, NOFOLLOW` | Instruerar webbcrawlningar att undvika att indexera webbplatsen och att inte checka tillbaka senare för att se ändringar. |

     {style="table-layout:auto"}

   - Om det behövs kan du ange egna instruktioner i **[!UICONTROL Edit Custom instruction of robots.txt file]** box. När en plats håller på att utvecklas kanske du vill neka åtkomst till alla mappar.

   - Om du vill återställa standardinstruktionerna klickar du på **[!UICONTROL Reset to Default]**.

1. När du är klar klickar du på **[!UICONTROL Save Configuration]**.
