---
title: Sökmotoroptimering
description: Läs om SEO-verktyg (sökmotoroptimering) för Commerce webbplatser och de bästa sätten att optimera SEO.
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
source-git-commit: c8649d9107a92b15a1c9af8ae5d2ad0e8e34e64e
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# SEO - översikt

_Sökmotoroptimering_ (SEO) är ett sätt att finjustera innehållet och presentationen för en webbplats för att förbättra det sätt på vilket sidorna indexeras av sökmotorer. Commerce har olika funktioner som stöder er pågående SEO-insats.

>[!TIP]
>
>Information om Adobe Commerce as a Cloud Service finns i [SEO-riktlinjerna](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/) i dokumentationen för Commerce Storefront

## Metadata

[!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."}

Lär dig mer om att lägga till och förbättra [metadata](meta-data.md) med nyckelord för din webbplats och butik.

## Använda en platskarta

[!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."}

En [webbplatskarta](sitemap-xml.md) förbättrar det sätt på vilket din butik indexeras av sökmotorer och är utformad för att hitta sidor som kan förbises av webbcrawler. En platskarta kan konfigureras för indexering av alla sidor och bilder.

## URL-omskrivningar

[!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."}

Med verktyget [URL-omskrivning](url-rewrite.md) kan du ändra alla URL-adresser som är kopplade till en produkt, kategori eller CMS-sida.

## Sökrobotar

Commerce-konfigurationen innehåller inställningar för att generera och hantera instruktioner för webbcrawlningar och botar som indexerar din webbplats. Om begäran för `robots.txt` når Commerce (i stället för en fysisk fil) dirigeras den dynamiskt till robotstyrenheten. Instruktionerna är direktiv som känns igen och följs av de flesta sökmotorer.

Som standard innehåller filen robots.txt som genereras av Commerce instruktioner för web crawler för att undvika att indexera vissa delar av webbplatsen som innehåller filer som används internt av systemet. Du kan använda standardinställningarna eller definiera egna instruktioner för alla eller för specifika sökmotorer. Det finns många artiklar online som utforskar ämnet i detalj.

### Exempel på anpassade instruktioner

**Tillåter fullständig åtkomst**

    Användaragent:*
    Tillåt inte:

**Tillåt inte åtkomst till alla mappar**

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
    Tillåt inte: /sendent vän/
    Tillåt inte: /review/
    Tillåt inte: /*SID=

### Konfigurera `robots.txt`

1. Gå till _>_ > **[!UICONTROL Content]** på sidofältet _[!UICONTROL Design]_&#x200B;Admin **[!UICONTROL Configuration]**.

1. Leta reda på konfigurationen **[!UICONTROL Global]** i den första raden i rutnätet och klicka på **[!UICONTROL Edit]**.

   ![Global designkonfiguration](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. Bläddra nedåt och expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Search Engine Robots]** och gör följande:

   ![Designkonfiguration - sökrobotar](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL Default Robots]** till något av följande:

     | Alternativ | Beskrivning |
     |------|------------|
     | `INDEX, FOLLOW` | Instruerar webbcrawlningar att indexera platsen och att checka tillbaka senare för att se ändringar. |
     | `NOINDEX, FOLLOW` | Instruerar webbcrawlningar att undvika att indexera platsen, men att senare göra ändringar. |
     | `INDEX, NOFOLLOW` | Instruerar webbcrawlningar att indexera platsen en gång, men inte följa några länkar på sidan. |
     | `NOINDEX, NOFOLLOW` | Instruerar webbcrawlningar att undvika att indexera platsen och att inte följa några länkar på sidan. |

     {style="table-layout:auto"}

   - Ange anpassade instruktioner i rutan **[!UICONTROL Edit Custom instruction of robots.txt file]** om det behövs. När en plats håller på att utvecklas kanske du vill neka åtkomst till alla mappar.

   - Om du vill återställa standardinstruktionerna klickar du på **[!UICONTROL Reset to Default]**.

1. Klicka på **[!UICONTROL Save Configuration]** när du är klar.
