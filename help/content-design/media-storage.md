---
title: Medielagring
description: Lär dig hur medielagring hjälper dig att ordna och få tillgång till Commerce mediefiler som lagras på servern.
exl-id: 5cf1bb20-d747-4a12-8558-e167c229efe8
feature: Page Content, Media
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# Medielagring

Med medielagring kan du ordna och få tillgång till mediefiler som lagras på servern. Sökvägen till filernas plats bestäms av konfigurationen för [bas-URL](../stores-purchase/store-urls.md) . Filer i medielagring kan nås från redigeraren när du arbetar med sidor och statiska block. Vanligtvis finns medielagring i filsystemet på samma server som programfilerna för [!DNL Commerce].

Alternativt kan mediefiler hanteras i en [databas](media-storage-database.md), på en separat server eller i ett [leveransnätverk](media-storage-content-delivery-network.md). Fördelen med att använda alternativ lagring är att det minimerar den arbetsinsats som krävs för att synkronisera media. Synkroniseringsprestanda påverkas särskilt när flera instanser av systemet distribueras på olika servrar som behöver åtkomst till samma bilder, CSS-filer och andra mediefiler.

Redigeraren kan konfigureras att använda statiska eller [dynamiska medie-URL:er](../catalog/catalog-urls.md#configure-catalog-media-url-format) för kataloginnehåll i kategori- eller produktbeskrivningar.

![[!DNL Commerce] medielagring](./assets/media-storage.png){width="650" zoomable="yes"}

## Lägg till filer i medielagringen

De första två stegen är samma som om du infogar en bild.

1. Klicka på ikonen _Infoga bild_ i verktygsfältet [redigerare](editor.md) .

   ![Ikonen Infoga bild](./assets/editor-toolbar-image-button.png){width="700" zoomable="yes"}

   Den här åtgärden öppnar dialogrutan _[!UICONTROL Insert/edit image]_.

1. Efter _[!UICONTROL Source]_&#x200B;klickar du på ikonen_ Sök _(![ikonen Sök](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

1. Gör något av följande i katalogträdet till vänster:

   - Navigera till mappen där du vill spara den överförda bilden.

   - Navigera till den plats där du vill skapa en mapp och klicka på **Skapa mapp**.

     Om du vill lägga till en mapp anger du mappnamnet och klickar på **[!UICONTROL OK]**.

1. Om du vill lägga till en eller flera filer i medielagringen kan du antingen överföra filerna från datorn eller använda [Adobe Stock Integration](adobe-stock.md):

   Om du vill överföra filer från datorn klickar du på **[!UICONTROL Choose Files]** och gör följande:

   - Gå till bildens plats i den lokala datorns katalog.

   - Markera varje bild som ska överföras.

   - Klicka på **[!UICONTROL Open]**.

   Så här använder du resurser från Adobe Stock med [integreringen](adobe-stock.md):

   - Klicka på **[!UICONTROL Search Adobe Stock]**.

   - Lägg till en förhandsvisning eller licensierad bild från Adobe Stock (se [Använda Adobe Stock-bilder](adobe-stock-manage.md)).

Bilderna överförs till den aktuella medielagringsmappen på servern.

![[!DNL Commerce] medielagring](./assets/media-storage.png){width="650" zoomable="yes"}

## Infoga en bild från medielagring

Öppna sidan eller blocket som ska redigeras. Använd sedan någon av följande metoder för att infoga en bild från medielagring:

### Metod 1: WYSIWYG

1. Klicka på ikonen _Infoga bild_ i verktygsfältet [redigerare](editor.md) .

1. Efter _[!UICONTROL Source]_&#x200B;klickar du på ikonen_ Sök _(![ikonen Sök](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

   ![Markera sökikonen](./assets/editor-dialog-insert-image.png){width="250" zoomable="yes"}

1. Navigera i katalogträdet till vänster till mappen där bilden finns.

1. Markera bildrutan i bilden och klicka på **[!UICONTROL Add Selected]**.

### Metod 2: HTML

1. Placera markören i koden där taggen `<img>` ska infogas.

1. Klicka på **[!UICONTROL Insert Image]**.

   ![Infoga bild (HTML-läge)](./assets/editor-html-mode-insert-image.png){width="600" zoomable="yes"}
