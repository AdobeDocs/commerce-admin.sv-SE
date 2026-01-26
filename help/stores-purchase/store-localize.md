---
title: Lagringsplats
description: Lär dig hur du lokaliserar en butik eller butiksvy.
exl-id: 64e1b431-f599-444c-9d39-207bb95f0400
topic: Commerce, Localization
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 0%

---

# Lagringsplats

Den mesta texten som verkar vara hårdkodad på sidor i butiken kan omedelbart ändras till ett annat språk genom att vyns språkområde ändras. När du ändrar språkområdet översätts inte ordet för ord, utan bara en annan översättningstabell som innehåller gränssnittstexten som används i hela butiken. Den text som kan ändras är navigeringsrubriker, etiketter, knappar och länkar som _Min kundvagn_ och _Mitt konto_. Du kan också använda verktyget [Textbunden översättning](../configuration-reference/advanced/developer.md) för att redigera text i gränssnittet.

Språkpaket finns under [Översättningar och lokalisering](https://marketplace.magento.com/extensions/content-customizations/translations-localization.html){:target="_blank"} på Commerce Marketplace. Nya tillägg läggs kontinuerligt till på Marketplace, så kom tillbaka ofta.

## Steg 1: Installera ett språkpaket

Följ standardinstruktionerna för att installera språkpakettillägget. Mer information om hur du installerar ett tillägg finns i [Allmän CLI-installation](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) i _Tilläggsguiden_.

## Steg 2: Skapa en butiksvy för språket

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_Admin **[!UICONTROL All Stores]**.

1. Klicka på **[!UICONTROL Create Store View]**.

1. Ange alternativ för den nya butiksvyn:

   - **[!UICONTROL Store]** - Välj den butik som är överordnad vyn.

   - **[!UICONTROL Name]** - Ange ett namn för butiksvyn. Till exempel: Portugisiska.

     I butikens huvud visas namnet i _språkväljaren_.

   - **[!UICONTROL Code]** - Ange en kod med gemener för att identifiera vyn. Till exempel: `portuguese`.

   - **[!UICONTROL Status]** - Aktivera vyn genom att ange `Enabled`.

   - **[!UICONTROL Sort Order]** — (Valfritt) Ange ett nummer för att avgöra i vilken ordning den här vyn visas tillsammans med andra vyer.

1. Klicka på **[!UICONTROL Save Store View]** när du är klar.

## Steg 3: Ändra språkinställningen för butiksvyn

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_Admin **[!UICONTROL Configuration]**.

1. I listrutan **[!UICONTROL Scope]** väljer du den butiksvy som ska konfigureras och klickar på **[!UICONTROL OK]** när du uppmanas till detta.

1. Expandera *[!UICONTROL General]* Expansionsväljaren![ i avsnittet ](../assets/icon-display-expand.png) på konfigurationssidan **[!UICONTROL Locale Options]**.

1. Avmarkera kryssrutan **[!UICONTROL Use Website]** och ställ in **[!UICONTROL Locale]** på det språk som du vill tilldela vyn.

   Om det finns flera varianter av det tillgängliga språket måste du välja det för den specifika regionen eller dialekten.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

   När du har ändrat språk för språkområdet måste det återstående innehållet som du har skapat, inklusive produktnamn och beskrivningar, kategorier, [CMS](../content-design/page-translate.md) -sidor och block, översättas separat för varje butiksvy.

## Lokalisera produkter

Om din butik har flera vyer på olika språk är samma produkter tillgängliga i respektive butiksvy. Du kan använda samma grundläggande produktinformation, som SKU, pris och lagernivå, oavsett språk. Översätt sedan bara produktnamn, beskrivningsfält och metadata efter behov för varje språk.

### Steg 1: Översätt produktfält

1. Gå till _>_ på sidofältet **[!UICONTROL Catalog]** Admin **[!UICONTROL Products]**.

1. Leta reda på produkten som ska översättas i rutnätet och öppna den i redigeringsläge.

1. I det övre vänstra hörnet anger du **[!UICONTROL Store View]** till vyn för översättningen och klickar på **[!UICONTROL OK]** när du uppmanas att bekräfta.

1. Gör följande för varje fält som ska redigeras:

   - Avmarkera kryssrutan **[!UICONTROL Use Default Value]** till höger om fältet.

   - Klistra in eller skriv den översatta texten i fältet.

   Se till att översätta alla textfält, inklusive [bild](../catalog/catalog-images-video.md) -etiketter och Alt-text, [sökmotoroptimeringsfält](../catalog/product-search-engine-optimization.md) och eventuell [anpassad alternativinformation](../catalog/settings-advanced-custom-options.md) -information.

1. Klicka på **[!UICONTROL Save]** när du är klar.

### Steg 2: Översätt fältetiketter

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Attributes]_Admin **[!UICONTROL Product]**.

1. I listan hittar du attributet som ska översättas och öppnas i redigeringsläge.

1. Välj **[!UICONTROL Manage Labels]** på den vänstra panelen.

1. I avsnittet _[!UICONTROL Manage Titles]_anger du en översatt etikett för varje butiksvy.

   ![Ange översatta etiketter](./assets/product-attribute-labels-translate.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Attribute]** när du är klar.

### Steg 3: Översätt alla kategorier

1. Gå till _>_ Kategorier **[!UICONTROL Catalog]** på sidofältet **Admin**.

1. I det övre vänstra hörnet anger du **[!UICONTROL Store View]** till vyn för översättningen och klickar på **[!UICONTROL OK]** när du uppmanas att bekräfta.

1. Leta reda på kategorin som ska översättas i trädet och öppna den i redigeringsläge.

1. För _grundläggande information_, översätt **[!UICONTROL Category Name]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet _[!UICONTROL Content]_och översätt **[!UICONTROL Description]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Search Engine Optimization Settings]** och översätt följande fält:

   - **[!UICONTROL Meta Title]**
   - **[!UICONTROL Meta Keywords]**
   - **[!UICONTROL Meta Description]**

1. Gör följande under avsnittet _[!UICONTROL Search Engine Optimization Settings]_för att översätta **[!UICONTROL URL Key]**:

   - Avmarkera kryssrutan **[!UICONTROL Use Default Value]** till höger om fältet.

   - Ange den översatta texten.

   - Kontrollera att kryssrutan **[!UICONTROL Create Permanent Redirect for old URL]** är markerad.

   ![Översätt URL-nyckeln](./assets/category-translate-url-key.png)

1. Klicka på **[!UICONTROL Save Category]** när du är klar.

1. Upprepa processen för alla kategorier som används i butiken.

### Steg 4: Översätt produktattribut och attributalternativ

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Attributes]_Admin **[!UICONTROL Product]**.

1. Välj det attribut som ska översättas.

1. Välj **[!UICONTROL Manage Labels]** till vänster och ange **[!UICONTROL Managed Titles]**-alternativen för att definiera attributets rubriköversättningar.

1. Välj **[!UICONTROL Properties]** till vänster och ange alternativen för översatta attribut i avsnittet **[!UICONTROL Manage Options]**.

   ![Hantera alternativ](./assets/manage-option-tab.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Attribute]** när du är klar.
