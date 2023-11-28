---
title: Webbplatskartor
description: Lär dig hur du konfigurerar en webbplatskarta för att indexera alla sidor och bilder på dina Commerce-webbplatser.
exl-id: 48c975ae-b088-4e52-80cf-cb19c2b9b00f
feature: Merchandising, Storefront, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1207'
ht-degree: 0%

---

# Webbplatskartor

En webbplatskarta förbättrar det sätt på vilket din butik indexeras av sökmotorer och är utformad för att hitta sidor som kan förbises av webbcrawler. En platskarta kan konfigureras för indexering av alla sidor och bilder.

När det här alternativet är aktiverat skapas en fil med namnet `sitemap.xml` som sparas på den plats som du anger. Med konfigurationen kan du ange uppdateringsfrekvens och prioritet för varje typ av innehåll. Din webbplatskarta bör uppdateras så ofta som innehållet på din webbplats ändras, vilket kan vara varje dag, varje vecka eller varje månad.

När webbplatsen är under utveckling kan du inkludera instruktioner i `robots.txt` för webbcrawler för att undvika att indexera webbplatsen. Innan du startar programmet kan du ändra instruktionerna så att webbplatsen kan indexeras.

Teknisk information finns på [Lägg till platskarta och robots.txt][1] i _Handbok för Commerce on Cloud Infrastructure_.

![Webbplatskarta](./assets/marketing-sitemap-grid-generated.png){width="700" zoomable="yes"}

## Steg 1. Konfigurera webbplatskartan

Slutför [Konfiguration av XML-webbplatskarta](#site-map-configuration) för att avgöra vad som ingår och hur ofta platskartan uppdateras.

## Steg 2. Generera webbplatskartan

1. På _Administratör_ meny, gå till **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**.

1. Klicka på **[!UICONTROL Add Site Map]**.

   ![Rutnät för webbplatskartor](./assets/marketing-sitemap.png){width="700" zoomable="yes"}

1. Ange webbplatskartan **[!UICONTROL Filename]**. Exempel: `sitemap.xml`

1. Ange **[!UICONTROL Path]** för att avgöra var platskartan ska placeras på servern. Kontrollera att sökvägen är skrivskyddad.

   - `/sitemap/` - Placerar platskartefilen i en katalog med namnet _sitemap_.

   - `/` - Placerar platskartfilen på grundsökvägen eller roten för din Commerce-installation.

   ![Ny webbplatskarta](./assets/marketing-sitemap-new.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save & Generate]**.

   Det kan ta några minuter innan webbplatskartan visas i rutnätet.

## Steg 3. Konfigurera och aktivera robots.txt (valfritt)

Slutför [sökrobotar](seo-overview.md#search-engine-robots) konfiguration med instruktioner som instruerar sökmotorer att crawla de delar av webbplatsen som du vill indexera.

## Steg 4. Skicka din webbplatskarta till sökmotorer

Du kan skicka webbplatskartan till olika sökmotorer genom att ge dem länken till `sitemap.xml` i din Commerce-installation. Så här kopierar du länken:

1. I _Webbplatskarta_ högerklicka på URL-adressen i listan **[!UICONTROL Link for Google]** kolumn.

1. Välj **[!UICONTROL Copy Link Address]**.

Mer information finns i instruktionerna för den specifika sökmotorn. Här följer länkar till instruktioner för två sökmotorer:

- [Google][2]
- [Microsoft® Bing][3]

## Steg 5: Återställ tidigare instruktioner för robot (valfritt)

Du kan nu återställa de ursprungliga (standardinställningen) begränsningarna.

## Hantera webbplatskartor och robots.txt för flera webbplatser

Om du har flera webbplatser kan du förenkla processen att skapa och skicka in webbplatskartor. Bara [skapa](#site-map-configuration) en eller flera platskartor som innehåller URL:er för alla verifierade arkiv och sparar platskartorna på en enda plats. Alla platser måste verifieras i [Google Search Console](https://support.google.com/webmasters/answer/7451001).

Så här skapar du platskartor för en multistore-instans:

1. Skapa en mapp med namnet `sitemaps` på webbplatsens rot och skapa sedan undermappar för varje domän:

       /sitemaps/domain_1/
       /sitemaps/domain_2/
   
1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**.

1. Skapa eller redigera platskartelistorna för varje butik och ange **[!UICONTROL Path]** till den som du skapade för butiken:

   `/sitemaps/domain_1/`
   `/sitemaps/domain_2/`

1. Uppdatera filen robots.txt om det behövs.

   Om du vill vara säker på att sökmotorspindlarna är korrekt dirigerade till de nya webbplatskartorna kan du uppdatera eller skapa filen robots.txt. Lägg till följande rader högst upp.

       Webbplatskarta
       Webbplatskarta: https://www.domain_1.com/sitemaps/domain_1/sitemap.xml
       Webbplatskarta: https://www.domain_2.com/sitemaps/domain_2/sitemap.xml
   
>[!NOTE]
>
>Om webbplatsen använder [Apache](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/web-server/apache.html) webbservermotorn bör du uppdatera [`.htaccess`](https://httpd.apache.org/docs/current/howto/htaccess.html) i webbplatsens rot för att dirigera andra platskarteförfrågningar till rätt plats.

## Kolumnbeskrivningar

| Kolumn | Beskrivning |
|------|-----------|
| [!UICONTROL ID] | Det sekventiella postnumret för den aktuella webbplatskartan. |
| [!UICONTROL Filename] | Filnamnet på webbplatskartan. |
| [!UICONTROL Path] | Platsen där platskartan finns på servern. Till exempel: <br/>`/sitemap/` - Placerar platskartefilen i en katalog med namnet _sitemap_, en nivå under roten i Commerce-installationen. <br/>`/` - Placerar platskartfilen på grundsökvägen eller roten för Commerce-installationen. |
| [!UICONTROL Link for Google] | URL-adressen till webbplatskartan som ska skickas till Google och andra sökmotorer. |
| [!UICONTROL Last Generated] | Anger det datum och den tidpunkt då webbplatskartan senast genererades. |
| [!UICONTROL Store View] | Butiksvyn där platskartan tillämpas. |
| [!UICONTROL Generate] | Återskapar platskartan. |

{style="table-layout:auto"}

## Konfiguration av platskarta

Din webbplatskarta bör uppdateras så ofta som innehållet på din webbplats ändras, vilket kan vara på en daglig, veckovis eller månadsbasis. Med konfigurationen kan du ange frekvens och prioritet för varje typ av innehåll.

### Steg 1. Ange frekvens och prioritet för innehållsuppdateringar

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL XML Sitemap]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Categories Options]** och gör följande:

   >[!NOTE]
   >
   >Rensa **[!UICONTROL Use system value]** om du vill ändra inställningarna.

   - Ange **[!UICONTROL Frequency]** till något av följande:

      - `Always`
      - `Hourly`
      - `Daily`
      - `Weekly`
      - `Monthly`
      - `Yearly`
      - `Never`

   - För **[!UICONTROL Priority]**, ange ett värde mellan `0.0` och `1.0`. Noll har lägst prioritet.

   ![XML-webbplatskarta - Kategorialternativ](../configuration-reference/catalog/assets/xml-sitemap-categories-options.png){width="600" zoomable="yes"}

   En detaljerad lista över dessa alternativ finns på [Kategorialternativ](../configuration-reference/catalog/xml-sitemap.md#categories-options) i _Konfigurationsreferens_.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Products Options]** och fylla i **[!UICONTROL Frequency]** och **[!UICONTROL Priority]** inställningar efter behov.

   En detaljerad lista över dessa alternativ finns på [Produktalternativ](../configuration-reference/catalog/xml-sitemap.md#products-options) i _Konfigurationsreferens_.

1. Ange hur mycket bilder ska inkluderas i platskartan **[!UICONTROL Add Images into Sitemap]** till något av följande:

   - `None`
   - `Base Only`
   - `All`

   ![Katalogkonfiguration - XML-produkter för platskarta](../configuration-reference/catalog/assets/xml-sitemap-products-options.png){width="600" zoomable="yes"}

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL CMS Pages Options]** och fylla i **[!UICONTROL Frequency]** och **[!UICONTROL Priority]** inställningar efter behov.

   ![Katalogkonfiguration - CMS-sidor för XML-platskarta](../configuration-reference/catalog/assets/xml-sitemap-cms-pages-options.png){width="600" zoomable="yes"}

   En detaljerad lista över dessa alternativ finns på [Alternativ för CMS-sidor](../configuration-reference/catalog/xml-sitemap.md#cms-pages-options) i _Konfigurationsreferens_.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Store Url Options]** och fylla i **[!UICONTROL Frequency]** och **[!UICONTROL Priority]** inställningar efter behov.

   ![Katalogkonfiguration - URL för XML-platskarta](./assets/xml-sitemap.png){width="600" zoomable="yes"}

   En detaljerad lista över dessa alternativ finns på [Lagra URL-alternativ](../configuration-reference/catalog/xml-sitemap.md#store-url-options) i _Konfigurationsreferens_.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

### Steg 2. Slutför genereringsinställningarna

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Generation Settings]** -avsnitt.

   Rensa **Använd systemvärde** om du vill ändra inställningarna.

   ![Katalogkonfiguration - Genereringsinställningar för XML-platskarta](../configuration-reference/catalog/assets/xml-sitemap-generation-settings.png){width="600" zoomable="yes"}

   En detaljerad lista över dessa alternativ finns på [Genereringsinställningar](../configuration-reference/catalog/xml-sitemap.md#generation-settings) i _Konfigurationsreferens_.

1. Skapa en platskarta genom att ange **[!UICONTROL Enabled]** till `Yes` och gör följande:

   - Ange **[!UICONTROL Start Time]** till timmen, minuten och sekunden där du vill att platskartan ska uppdateras.

   - Ange **[!UICONTROL Frequency]** till något av följande:

      - `Daily`
      - `Weekly`
      - `Monthly`

   - För **[!UICONTROL Error Email Recipient]** anger du e-postadressen till den person som ska få ett meddelande om ett fel inträffar under en platskartuppdatering.

   - Ange **[!UICONTROL Error Email Sender]** till butikskontakten som visas som avsändare av felmeddelandet.

   - Ange **[!UICONTROL Error Email Template]** till mallen som används för felmeddelandet.

### Steg 3. Ange begränsningar för webbplatskartan

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Sitemap File Limits]** -avsnitt.

   ![Katalogkonfiguration - XML-filbegränsningar för platskarta](../configuration-reference/catalog/assets/xml-sitemap-sitemap-file-limits.png){width="600" zoomable="yes"}

   En detaljerad lista över dessa alternativ finns på [Filbegränsningar för platskarta](../configuration-reference/catalog/xml-sitemap.md#sitemap-file-limits) i _Konfigurationsreferens_.

1. För **[!UICONTROL Maximum No of URLs per File]** anger du det maximala antalet URL:er som kan inkluderas i platskartan.

   Som standard är gränsen 50 000.

1. För **[!UICONTROL Maximum File Size]** anger du den största storleken i byte som tilldelas platskartan.

   Standardstorleken är 10 485 760 byte.

### Steg 4. Ange inställningar för att skicka sökmotorer

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Search Engine Submission Settings]** -avsnitt.

   ![Katalogkonfiguration - Skicka inställningar för XML-sökmotor för webbplatskartor](../configuration-reference/catalog/assets/xml-sitemap-search-engine-submission-settings.png){width="600" zoomable="yes"}

1. Om du använder `robots.txt` för att ge instruktioner till sökmotorer som crawlar webbplatsen, ange **[!UICONTROL Enable Submission to Robots.txt]** till `Yes`.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/robots-sitemap.html
[2]: https://support.google.com/webmasters/answer/183669?hl=en
[3]: https://www.bing.com/webmasters/help/Sitemaps-3b5cf6ed
