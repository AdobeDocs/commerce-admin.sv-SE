---
title: URL för dynamiska media
description: Lär dig hur du använder en dynamisk medie-URL som en relativ referens till en bild eller en annan medieresurs.
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# URL för dynamiska media

En dynamisk medie-URL är en relativ referens till en bild eller en annan medieresurs. När det här alternativet är aktiverat kan dynamiska medie-URL:er användas för att länka direkt till resurser på servern eller till filer som lagras i ett [innehållsleveransnätverk](media-storage-content-delivery-network.md). Användning av dynamiska medie-URL:er kan påverka katalogens prestanda och [redigeraren](editor.md#configure-the-editor) kan konfigureras att använda antingen statiska eller dynamiska medie-URL:er.

Precis som med alla [taggar](../systems/markup-tags.md) är direktivet omgivet av dubbla klammerparenteser. Formatet på en dynamisk medie-URL ser ut så här:

`\{\{media url="path/to/image.jpg"}}`

Dynamiska URL-direktiv bearbetas från sparat HTML-innehåll när sidan återges i butiken. Varje gång sidan återges skannas innehållet efter `\{\{media url="..."}}` och varje direktiv ersätts med motsvarande medie-URL.

{{$include /help/_includes/directives-caution.md}}

## Konfigurera statiska medie-URL:er

Som standard har bilder som infogats i katalogen från WYSIWYG Editor relativa, dynamiska URL:er. Om du föredrar att använda en statisk URL kan du ändra konfigurationsinställningen.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Välj **[!UICONTROL Content Management]** i den vänstra panelen under _[!UICONTROL General]_.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL WYSIWYG Options]**.

   ![WYSIWYG-alternativ](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** till något av följande:

   - `Yes` - Använder statiska URL:er för mediainnehåll som infogas med WYSIWYG Editor. Statiska URL:er är absoluta och bryts om butikens [bas-URL](../stores-purchase/store-urls.md) ändras.

   - `No` - (Standard) Använder dynamiska URL:er för mediainnehåll som infogas med WYSIWYG-redigeraren, baserat på direktivet `\{\{media url="..."}}`. Dynamiska URL:er är relativa och bryts inte om bas-URL:en för butiken ändras.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
