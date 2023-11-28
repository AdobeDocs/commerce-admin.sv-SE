---
title: Lagringsplats
description: Lär dig hur du lokaliserar en butik eller butiksvy.
exl-id: 64e1b431-f599-444c-9d39-207bb95f0400
topic: Commerce, Localization
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Lagringsplats

Den mesta texten som verkar vara hårdkodad på sidor i butiken kan omedelbart ändras till ett annat språk genom att vyns språkområde ändras. När du ändrar språkområdet översätts inte ordet för ord, utan bara en annan översättningstabell som innehåller gränssnittstexten som används i hela butiken. Den text som kan ändras är navigeringsrubriker, etiketter, knappar och länkar som _Min kundvagn_ och _Mitt konto_. Du kan också använda [Textbunden översättning](../configuration-reference/advanced/developer.md) för att redigera text i gränssnittet.

Språkpaket finns under [Översättningar och lokalisering][1]{:target=&quot;_blank&quot;} på Commerce Marketplace. Nya tillägg läggs kontinuerligt till på Marketplace, så kom tillbaka ofta.

## Steg 1: Installera ett språkpaket

Följ standardinstruktionerna för att installera språkpakettillägget. Mer information om hur du installerar ett tillägg finns i [Allmän CLI-installation][2] i _Handbok för tillägg_.

## Steg 2: Skapa en butiksvy för språket

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Klicka på **[!UICONTROL Create Store View]**.

1. Ange alternativ för den nya butiksvyn:

   - **[!UICONTROL Store]** — Välj den butik som är överordnad vyn.

   - **[!UICONTROL Name]** — Ange ett namn för butiksvyn. Till exempel: Portugisiska.

     I butikens sidhuvud visas namnet i _språkväljare_.

   - **[!UICONTROL Code]** — Ange en kod med gemener för att identifiera vyn. Exempel: `portuguese`.

   - **[!UICONTROL Status]** — Aktivera vyn genom att ange att `Enabled`.

   - **[!UICONTROL Sort Order]** — (Valfritt) Ange ett nummer som avgör i vilken ordning den här vyn visas tillsammans med andra vyer.

1. När du är klar klickar du på **[!UICONTROL Save Store View]**.

## Steg 3: Ändra språkinställningen för butiksvyn

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I det övre vänstra hörnet anger du **[!UICONTROL Store View]** till den specifika vy där konfigurationen ska användas.

1. När du uppmanas att bekräfta omfångsväxling klickar du på **[!UICONTROL OK]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Locale Options]** -avsnitt.

1. Rensa **[!UICONTROL Use Website]** kryssruta och ange **[!UICONTROL Locale]** till det språk som du vill tilldela vyn.

   Om det finns flera varianter av det tillgängliga språket måste du välja det för den specifika regionen eller dialekten.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

   När du har ändrat språk för språkområdet är det återstående innehållet som du har skapat, inklusive produktnamn och beskrivningar, kategorier, [CMS](../content-design/page-translate.md) sidor och block måste översättas separat för varje butiksvy.

## Lokalisera produkter

Om din butik har flera vyer på olika språk är samma produkter tillgängliga i respektive butiksvy. Du kan använda samma grundläggande produktinformation, som SKU, pris och lagernivå, oavsett språk. Översätt sedan bara produktnamn, beskrivningsfält och metadata efter behov för varje språk.

### Steg 1: Översätt produktfält

1. På _Administratör_ sidebar, gå till  **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Leta reda på produkten som ska översättas i rutnätet och öppna den i redigeringsläge.

1. I det övre vänstra hörnet anger du **[!UICONTROL Store View]** till vyn för översättningen och klicka på **[!UICONTROL OK]** när du uppmanas att bekräfta.

1. Gör följande för varje fält som ska redigeras:

   - Avmarkera **[!UICONTROL Use Default Value]** till höger om fältet.

   - Klistra in eller skriv den översatta texten i fältet.

   Se till att översätta alla textfält, inklusive [image](../catalog/catalog-images-video.md) etiketter och Alt-text, [Sökmotoroptimering](../catalog/product-search-engine-optimization.md) fält och alla [Anpassade alternativ](../catalog/settings-advanced-custom-options.md) information.

1. När du är klar klickar du på **[!UICONTROL Save]**.

### Steg 2: Översätt fältetiketter

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. I listan hittar du attributet som ska översättas och öppnas i redigeringsläge.

1. Välj **[!UICONTROL Manage Labels]**.

1. I _[!UICONTROL Manage Titles]_anger du en översatt etikett för varje butiksvy.

   ![Ange översatta etiketter](./assets/product-attribute-labels-translate.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Attribute]**.

### Steg 3: Översätt alla kategorier

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **Kategorier**.

1. I det övre vänstra hörnet anger du **[!UICONTROL Store View]** till vyn för översättningen och klicka på **[!UICONTROL OK]** när du uppmanas att bekräfta.

1. Leta reda på kategorin som ska översättas i trädet och öppna den i redigeringsläge.

1. För _Grundläggande information_, översätta **[!UICONTROL Category Name]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den _[!UICONTROL Content]_och översätta **[!UICONTROL Description]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Search Engine Optimization Settings]** och översätt följande fält:

   - **[!UICONTROL Meta Title]**
   - **[!UICONTROL Meta Keywords]**
   - **[!UICONTROL Meta Description]**

1. Under _[!UICONTROL Search Engine Optimization Settings]_gör du följande för att översätta **[!UICONTROL URL Key]**:

   - Rensa **[!UICONTROL Use Default Value]** till höger om fältet.

   - Ange den översatta texten.

   - Se till att **[!UICONTROL Create Permanent Redirect for old URL]** är markerad.

   ![Översätt URL-nyckeln](./assets/category-translate-url-key.png)

1. När du är klar klickar du på **[!UICONTROL Save Category]**.

1. Upprepa processen för alla kategorier som används i butiken.

### Steg 4: Översätt produktattribut och attributalternativ

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Välj det attribut som ska översättas.

1. Välj **[!UICONTROL Manage Labels]** till vänster och ange **[!UICONTROL Managed Titles]** alternativ för att definiera översättningar av attributtitel.

1. Välj **[!UICONTROL Properties]** till vänster och ange de översatta attributalternativen i dialogrutan **[!UICONTROL Manage Options]** -avsnitt.

   ![Hantera alternativ](./assets/manage-option-tab.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Attribute]**.


[1]: https://marketplace.magento.com/extensions/content-customizations/translations-localization.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html
