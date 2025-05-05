---
title: Webbplatskartor
description: Lär dig hur du konfigurerar en webbplatskarta för att indexera alla sidor och bilder på dina Commerce-webbplatser.
exl-id: 48c975ae-b088-4e52-80cf-cb19c2b9b00f
feature: Merchandising, Storefront, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1175'
ht-degree: 0%

---

# Webbplatskartor

En webbplatskarta förbättrar det sätt på vilket din butik indexeras av sökmotorer och är utformad för att hitta sidor som kan förbises av webbcrawler. En platskarta kan konfigureras för indexering av alla sidor och bilder.

När det här alternativet är aktiverat skapar Commerce en fil med namnet `sitemap.xml` som sparas i din installation på den plats som du anger. Med konfigurationen kan du ange uppdateringsfrekvens och prioritet för varje typ av innehåll. Din webbplatskarta bör uppdateras så ofta som innehållet på din webbplats ändras, vilket kan vara varje dag, varje vecka eller varje månad.

När din webbplats är under utveckling kan du inkludera instruktioner i filen `robots.txt` för webbcrawlningar för att undvika att indexera webbplatsen. Innan du startar programmet kan du ändra instruktionerna så att webbplatsen kan indexeras.

Mer teknisk information finns i [Lägg till platskarta och robots.txt][1] i _Commerce on Cloud Infrastructure Guide_.

![Rutnät för platskartor](./assets/marketing-sitemap-grid-generated.png){width="700" zoomable="yes"}

## Steg 1. Konfigurera webbplatskartan

Slutför konfigurationen [XML-platskarta](#site-map-configuration) för att fastställa vad som ingår och hur ofta platskartan uppdateras.

## Steg 2. Generera webbplatskartan

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**&#x200B;på menyn_ Admin _.

1. Klicka på **[!UICONTROL Add Site Map]**.

   ![Rutnät för webbplatskarta](./assets/marketing-sitemap.png){width="700" zoomable="yes"}

1. Ange webbplatskartan **[!UICONTROL Filename]**. Till exempel: `sitemap.xml`

1. Ange **[!UICONTROL Path]** för att avgöra var platskartefilen ska finnas på servern. Kontrollera att sökvägen är skrivskyddad.

   - `/sitemap/` - Placerar platskartefilen i en katalog med namnet _sitemap_.

   - `/` - Placerar platskartefilen i grundsökvägen eller roten för din Commerce-installation.

   ![Ny webbplatskarta](./assets/marketing-sitemap-new.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save & Generate]** när du är klar.

   Det kan ta några minuter innan webbplatskartan visas i rutnätet.

## Steg 3. Konfigurera och aktivera robots.txt (valfritt)

Slutför konfigurationen av [sökrobotar](seo-overview.md#search-engine-robots) med instruktioner som instruerar sökmotorer att crawla de delar av webbplatsen som du vill indexera.

## Steg 4. Skicka din webbplatskarta till sökmotorer

Du kan skicka webbplatskartan till olika sökmotorer genom att ge dem länken till filen `sitemap.xml` i din Commerce-installation. Så här kopierar du länken:

1. Högerklicka på URL:en i kolumnen **[!UICONTROL Link for Google]** i listan _Platskarta_.

1. Välj **[!UICONTROL Copy Link Address]** på menyn.

Mer information finns i instruktionerna för den specifika sökmotorn. Här följer länkar till instruktioner för två sökmotorer:

- [Google][2]
- [Microsoft® Bing][3]

## Steg 5: Återställ tidigare instruktioner för robot (valfritt)

Du kan nu återställa de ursprungliga (standardinställningen) begränsningarna.

## Hantera webbplatskartor och robots.txt för flera webbplatser

Om du har flera webbplatser kan du förenkla processen att skapa och skicka in webbplatskartor. [Skapa](#site-map-configuration) en eller flera webbplatskartor som innehåller URL:er för alla verifierade butiker och spara platskartorna på en enda plats. Alla webbplatser måste verifieras i [Google Search Console](https://support.google.com/webmasters/answer/7451001).

Så här skapar du platskartor för en multistore-instans:

1. Skapa en mapp med namnet `sitemaps` i webbplatsens rot och skapa sedan undermappar för varje domän:

       /sitemaps/domain_1/
       /sitemaps/domain_2/
   
1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**&#x200B;på sidofältet_ Admin _.

1. Skapa eller redigera platskartlistor för varje butik och ställ in **[!UICONTROL Path]** på den som du skapade för butiken:

   `/sitemaps/domain_1/`
   `/sitemaps/domain_2/`

1. Uppdatera filen robots.txt om det behövs.

   Om du vill vara säker på att sökmotorspindlarna är korrekt dirigerade till de nya webbplatskartorna kan du uppdatera eller skapa filen robots.txt. Lägg till följande rader högst upp.

       Webbplatskarta
       Webbplatskarta: https://www.domain_1.com/sitemaps/domain_1/sitemap.xml
       Webbplatskarta: https://www.domain_2.com/sitemaps/domain_2/sitemap.xml
   
>[!NOTE]
>
>Om din webbplats använder webbservermotorn [Apache](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/web-server/apache.html) bör du uppdatera filen [`.htaccess`](https://httpd.apache.org/docs/current/howto/htaccess.html) i webbplatsens rot för att dirigera eventuella andra platskarteförfrågningar till rätt plats.

## Kolumnbeskrivningar

| Kolumn | Beskrivning |
|------|-----------|
| [!UICONTROL ID] | Det sekventiella postnumret för den aktuella webbplatskartan. |
| [!UICONTROL Filename] | Filnamnet på webbplatskartan. |
| [!UICONTROL Path] | Platsen där platskartan finns på servern. Till exempel: <br/>`/sitemap/` - Placerar platskartefilen i en katalog med namnet _sitemap_, en nivå under roten för Commerce-installationen. <br/>`/` - Placerar platskartefilen på grundsökvägen eller roten för Commerce-installationen. |
| [!UICONTROL Link for Google] | URL-adressen till webbplatskartan som ska skickas till Google och andra sökmotorer. |
| [!UICONTROL Last Generated] | Anger det datum och den tidpunkt då webbplatskartan senast genererades. |
| [!UICONTROL Store View] | Butiksvyn där platskartan tillämpas. |
| [!UICONTROL Generate] | Återskapar platskartan. |

{style="table-layout:auto"}

## Konfiguration av platskarta

Din webbplatskarta bör uppdateras så ofta som innehållet på din webbplats ändras, vilket kan vara på en daglig, veckovis eller månadsbasis. Med konfigurationen kan du ange frekvens och prioritet för varje typ av innehåll.

### Steg 1. Ange frekvens och prioritet för innehållsuppdateringar

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL XML Sitemap]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Categories Options]** och gör följande:

   >[!NOTE]
   >
   >Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för att ändra de här inställningarna.

   - Ange **[!UICONTROL Frequency]** till något av följande:

      - `Always`
      - `Hourly`
      - `Daily`
      - `Weekly`
      - `Monthly`
      - `Yearly`
      - `Never`

   - Ange ett värde mellan `0.0` och `1.0` för **[!UICONTROL Priority]**. Noll har lägst prioritet.

   ![XML-webbplatskarta - Kategorialternativ](../configuration-reference/catalog/assets/xml-sitemap-categories-options.png){width="600" zoomable="yes"}

   En detaljerad lista över dessa alternativ finns i [Kategorialternativ](../configuration-reference/catalog/xml-sitemap.md#categories-options) i _Konfigurationsreferens_.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Products Options]** och fyll i inställningarna för **[!UICONTROL Frequency]** och **[!UICONTROL Priority]** efter behov.

   En detaljerad lista över dessa alternativ finns i [Produktalternativ](../configuration-reference/catalog/xml-sitemap.md#products-options) i _Konfigurationsreferens_.

1. Ange **[!UICONTROL Add Images into Sitemap]** till något av följande för att avgöra i vilken utsträckning bilder ska inkluderas i platskartan:

   - `None`
   - `Base Only`
   - `All`

   ![Katalogkonfiguration - XML-produkter för platskarta](../configuration-reference/catalog/assets/xml-sitemap-products-options.png){width="600" zoomable="yes"}

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL CMS Pages Options]** och fyll i inställningarna för **[!UICONTROL Frequency]** och **[!UICONTROL Priority]** efter behov.

   ![Katalogkonfiguration - CMS-sidor för XML-platskarta](../configuration-reference/catalog/assets/xml-sitemap-cms-pages-options.png){width="600" zoomable="yes"}

   En detaljerad lista över dessa alternativ finns i [Alternativ för CMS-sidor](../configuration-reference/catalog/xml-sitemap.md#cms-pages-options) i _Konfigurationsreferens_.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Store Url Options]** och fyll i inställningarna för **[!UICONTROL Frequency]** och **[!UICONTROL Priority]** efter behov.

   ![Katalogkonfiguration - URL för XML-platskarta](./assets/xml-sitemap.png){width="600" zoomable="yes"}

   En detaljerad lista över dessa alternativ finns i [Lagra URL-alternativ](../configuration-reference/catalog/xml-sitemap.md#store-url-options) i _Konfigurationsreferens_.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

### Steg 2. Slutför genereringsinställningarna

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Generation Settings]**.

   Om det behövs avmarkerar du kryssrutan **Använd systemvärde** för att ändra de här inställningarna.

   ![Katalogkonfiguration - Genereringsinställningar för XML-platskarta](../configuration-reference/catalog/assets/xml-sitemap-generation-settings.png){width="600" zoomable="yes"}

   En detaljerad lista över dessa alternativ finns i [Genereringsinställningar](../configuration-reference/catalog/xml-sitemap.md#generation-settings) i _Konfigurationsreferens_.

1. Om du vill generera en platskarta anger du **[!UICONTROL Enabled]** till `Yes` och gör följande:

   - Ange **[!UICONTROL Start Time]** till timmen, minuten och sekunden som du vill att platskartan ska uppdateras.

   - Ange **[!UICONTROL Frequency]** till något av följande:

      - `Daily`
      - `Weekly`
      - `Monthly`

   - För **[!UICONTROL Error Email Recipient]** anger du e-postadressen till den person som ska få ett meddelande om ett fel inträffar under en platskartuppdatering.

   - Ange **[!UICONTROL Error Email Sender]** till butikskontakten som visas som avsändare av felmeddelandet.

   - Ange **[!UICONTROL Error Email Template]** till mallen som används för felmeddelandet.

### Steg 3. Ange begränsningar för webbplatskartan

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Sitemap File Limits]**.

   ![Katalogkonfiguration - XML-begränsningar för webbplatskartor](../configuration-reference/catalog/assets/xml-sitemap-sitemap-file-limits.png){width="600" zoomable="yes"}

   En detaljerad lista med de här alternativen finns i [Filbegränsningar för platskarta](../configuration-reference/catalog/xml-sitemap.md#sitemap-file-limits) i _Konfigurationsreferens_.

1. För **[!UICONTROL Maximum No of URLs per File]** anger du det maximala antalet URL:er som kan inkluderas i platskartan.

   Som standard är gränsen 50 000.

1. För **[!UICONTROL Maximum File Size]** anger du den största storleken i byte som har allokerats för platskartan.

   Standardstorleken är 10 485 760 byte.

### Steg 4. Ange inställningar för att skicka sökmotorer

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Search Engine Submission Settings]**.

   ![Katalogkonfiguration - Skicka inställningar för XML-sökmotor för webbplatskartor](../configuration-reference/catalog/assets/xml-sitemap-search-engine-submission-settings.png){width="600" zoomable="yes"}

1. Om du använder en `robots.txt`-fil för att ge instruktioner till sökmotorer som crawlar din webbplats, anger du **[!UICONTROL Enable Submission to Robots.txt]** till `Yes`.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

[1]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/robots-sitemap.html
[2]: https://support.google.com/webmasters/answer/183669?hl=en
[3]: https://www.bing.com/webmasters/help/Sitemaps-3b5cf6ed
