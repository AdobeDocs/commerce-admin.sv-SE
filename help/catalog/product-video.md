---
title: Lägg till produktvideor
description: Lär dig hur du konfigurerar produktvideor för din butik, vilket kräver en API-nyckel från YouTube från ett Google-konto, och lägger till en videolänk för en produkt.
exl-id: 0cfcee67-a2e2-41cb-ac70-304452f5db6d
feature: Catalog Management, Products, Media
source-git-commit: e439c1082834cbc81f6ccc7ca99e240d649c8b81
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# Lägg till produktvideor

Om du vill lägga till en produktvideo måste du först skaffa en API-nyckel från ditt Google-konto och ange den i butikens konfiguration. Sedan kan du länka till videon från produkten.

## Steg 1: Hämta YouTube API-nyckeln

1. Logga in på ditt Google-konto på [Google Developers Console][1].

1. I sökfältet högst upp anger du `YouTube Data API v3` och klicka på sökikonen.

1. Kontrollera att API-sidan är aktiverad när den visas.

1. Välj **[!UICONTROL Credentials]**.

1. Beroende på om du har inloggningsuppgifter eller inte gör du något av följande:

   - Om du redan har de nödvändiga inloggningsuppgifterna kopierar du nyckeln i _API-nycklar_ tabell.

   - Om du inte redan har autentiseringsuppgifter för detta API klickar du på **[!UICONTROL Create Credentials]**  överst och följ instruktionerna för att skapa de inloggningsuppgifter som behövs. Under _Hämta dina autentiseringsuppgifter_, kopiera API-nyckeln och klicka på **[!UICONTROL Done]**.

1. Kopiera API-nyckeln till Urklipp.

1. Klicka på ikonen Redigera till höger och ange begränsningar för att se till att API-nyckeln är begränsad till rätt referenter.

1. Vänta en stund medan nyckeln skapas och kopiera sedan nyckeln till Urklipp.

   I nästa steg klistrar du in nyckeln i butikens konfiguration.

## Steg 2: Konfigurera nyckeln i Commerce

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den _[!UICONTROL Product Video]_och klistra in **[!UICONTROL YouTube API key]**.

   ![Product Video configuration](../configuration-reference/catalog/assets/catalog-product-video.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

1. Uppdatera cacheminnet när du uppmanas till detta.

## Steg 3: Länka till videon

1. Öppna en produkt i redigeringsläge.

1. Rulla till och expandera _[!UICONTROL Images and Videos]_-avsnitt.

   ![Bilder och video](./assets/product-simple-images-videos.png){width="600" zoomable="yes"}

1. klicka **[!UICONTROL Add Video]**.

   Om du inte har konfigurerat YouTube API-nyckeln än klickar du på **[!UICONTROL OK]** för att fortsätta. Du kan inte länka till en YouTube-video, men du kan gå igenom processen.

1. För **[!UICONTROL Url]** anger du webbadressen till YouTube- eller Vimeo-videon.

   ![Ny video för produkten](./assets/product-video-add.png){width="600" zoomable="yes"}

1. Klicka utanför fältet och vänta på feedback på API-nyckeln eller videon.

   Om allt är klart kan YouTube ge grundläggande information om videon

1. Ange **[!UICONTROL Title]** och **[!UICONTROL Description]** av videon.

1. Så här överför du **[!UICONTROL Preview Image]**, bläddra till bilden och markera filen.

   >[!NOTE]
   >
   >Efter överföring genereras den förhandsvisningsbild som visas automatiskt av en extern videotjänstleverantör. Du kan inte redigera bilden från Adobe Commerce Admin.

1. Om du föredrar att använda videometadata klickar du på **[!UICONTROL Get Video Information]**.

1. Markera kryssrutan för varje videoklipp om du vill se hur videon används i butiken **[!UICONTROL Role]** som gäller:

   - `Base Image`
   - `Small Image`
   - `Swatch Image`
   - `Thumbnail`
   - `Hide from Product Page`

1. När du är klar klickar du på **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Om _[!UICONTROL Autostart base video]_konfigurationsalternativet är inställt på `Yes` men videon börjar inte spelas upp automatiskt, det kan bero på de automatiska uppspelningsprinciper som används av webbläsaren och som inte kan styras av Adobe Commerce. Alla webbläsare som stöds har sina egna automatiska uppspelningsprinciper som kan ändras över tid och videon kanske inte spelas upp automatiskt i framtiden. Som en rekommenderad metod bör du inte förlita dig på automatisk uppspelning för affärskritisk funktionalitet och bör testa beteendet för automatisk uppspelning av video i din butik med varje webbläsare som stöds.

## Underhåll API-åtkomst

Enligt Google utvecklare [Villkor]kan YouTube inaktivera API-åtkomst för konton som har varit inaktiva i mer än 90 dagar. Den här förekomsten kan leda till att dina videoklipp inte visas. Om du vill att API-åtkomsten ska vara aktuell använder du ett cron-jobb för att pinga API:t med regelbundna intervall:

```code
30 10 1 * * curl -i -G -e https://yourdomain.com/ -d "part=snippet&maxResults=1&q=test&key=YOUTUBEAPIKEY" https://www.googleapis.com/youtube/v3/search >/dev/null 2>&1
```

## Fältreferens

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL URL] | Den associerade videons URL. |
| [!UICONTROL Title] | Videons titel. |
| [!UICONTROL Description] | Videobeskrivningen. |
| [!UICONTROL Preview Image] | En överförd bild som används som förhandsgranskning av videon i din butik. |
| [!UICONTROL Get Video Information] | Hämtar videometadata som lagras på värdservern. Du kan använda originaldata eller uppdatera dem efter behov. |
| [!UICONTROL Role] | Anger hur förhandsvisningsbilden används i din butik. Du kan välja valfri kombination av alternativ: `Base Image`, `Small Image`, `Thumbnail`, `Swatch Image`, `Hide from Product Page` |

{style="table-layout:auto"}

[1]: https://console.developers.google.com/
[Villkor]: https://developers.google.com/youtube/terms/developer-policies#d.-accessing-youtube-api-services
