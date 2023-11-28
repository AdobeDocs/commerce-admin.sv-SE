---
title: URL för dynamiska media
description: Lär dig hur du använder en dynamisk medie-URL som en relativ referens till en bild eller en annan medieresurs.
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
source-git-commit: d3b9b4cd0d12f8d5feb2bad0bf601970f9ee1a36
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# URL för dynamiska media

En dynamisk medie-URL är en relativ referens till en bild eller en annan medieresurs. När det här alternativet är aktiverat kan dynamiska medie-URL:er användas för att länka direkt till resurser på servern eller till filer som lagras på en [innehållsleveransnätverk](media-storage-content-delivery-network.md). Användning av dynamiska medie-URL:er kan påverka katalogens prestanda och [redigerare](editor.md#configure-the-editor) kan konfigureras att använda antingen statiska eller dynamiska medie-URL:er.

Som med alla [taggar](../systems/markup-tags.md), är direktivet omgivet av dubbla klammerparenteser. Formatet på en dynamisk medie-URL ser ut så här:

`\{\{media url="path/to/image.jpg"}}`

Dynamiska URL-direktiv bearbetas från sparat HTML-innehåll när sidan återges i butiken. Varje gång sidan återges skannas innehållet `\{\{media url="..."}}` och varje direktiv ersätts med motsvarande medie-URL.

{{$include /help/_includes/directives-caution.md}}

## Konfigurera statiska medie-URL:er

Som standard har bilder som infogats i katalogen från WYSIWYG-redigeraren relativa, dynamiska URL:er. Om du föredrar att använda en statisk URL kan du ändra konfigurationsinställningen.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I den vänstra panelen under _[!UICONTROL General]_, välja **[!UICONTROL Content Management]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL WYSIWYG Options]** -avsnitt.

   ![WYSIWYG-alternativ](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** till något av följande:

   - `Yes` - Använder statiska URL:er för mediainnehåll som infogas med WYSIWYG-redigeraren. Statiska URL:er är absoluta och bryts om [bas-URL](../stores-purchase/store-urls.md) av butiksändringarna.

   - `No` - (Standard) Använder dynamiska URL:er för mediainnehåll som infogas med WYSIWYG-redigeraren, baserat på `\{\{media url="..."}}` -direktivet. Dynamiska URL:er är relativa och bryts inte om bas-URL:en för butiken ändras.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
