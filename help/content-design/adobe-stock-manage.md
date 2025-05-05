---
title: Använda Adobe Stock-bilder
description: Förbättra dina butikssidor med bilder från Adobe Stock.
exl-id: 8f7d6f0a-511f-4f4b-821d-10a06e18041e
feature: CMS, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 1%

---

# Använda Adobe Stock-bilder

[Adobe Stock](https://stock.adobe.com)-bilder kan användas i stället för att överföra ditt eget bildinnehåll. Ett vanligt användningssätt är att överföra och montera bildinnehåll när du skapar en sida.

[[!DNL Media Gallery]](media-gallery.md) har en direkt integrering med Adobe Stock, vilket gör det enkelt att licensiera dina bilder direkt från gallerisidan.

## Åtkomst till Adobe Stock sökstödraster

Adobe Stock sökpanel är tillgänglig när du [lägger till eller redigerar en sida](page-add.md), när du [skapar eller redigerar en kategori](../catalog/category-create.md) eller när du [infogar bilder via Innehållsredigeraren](editor-insert-image.md).

**_Så här söker du efter Adobe Stock-resurser och lägger till en stockbild på en sida:_**

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add a New Page]**.

   Om du vill redigera en befintlig sida kan du använda kolumnen _[!UICONTROL Action]_&#x200B;för att klicka på&#x200B;**[!UICONTROL Select]**&#x200B;och välja **[!UICONTROL Edit]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Content]** och gör följande:

   - Om [WYSIWYG-redigeraren är aktiverad](editor.md) klickar du på **[!UICONTROL Show/Hide Editor]** och sedan på **[!UICONTROL Insert Image]**.

   - Om du har [Page Builder aktiverat](../page-builder/setup.md) expanderar du panelen **[!UICONTROL Media]** och drar en **[!UICONTROL Image]** platshållare till målbehållaren. Klicka sedan på **[!UICONTROL Select from Gallery]**.

     ![Dra en bild till Page Builder-scenen](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Search Adobe Stock]**.

**_Så här söker du efter Adobe Stock-resurser och lägger till en stockbild i en kategori:_**

1. Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Categories]** på sidofältet _Admin_.

1. Klicka på **[!UICONTROL Add Root Category]** eller **[!UICONTROL Add Subcategory]**.

   Om du vill lägga till bilden i en befintlig kategori klickar du på kategorinamnet i listan till vänster.

1. Expandera avsnittet **[!UICONTROL Content]** och klicka **[!UICONTROL Select from Gallery]** under _[!UICONTROL Category Image]_.

1. Klicka på **[!UICONTROL Search Adobe Stock]**.

Så här söker du efter Adobe Stock-resurser och lägger till en stockbild från WYSIWYG-redigeraren:

1. klicka på **[!UICONTROL Show/Hide Editor]**.

1. Klicka på **[!UICONTROL Insert Image]**.

1. Klicka på **[!UICONTROL Search Adobe Stock]**.

   ![Adobe Stock sökresultat](./assets/adobe-stock-search-grid.png){width="600" zoomable="yes"}

## Filtrera och söka efter Adobe Stock-resurser

[Adobe Stock sökstödraster](#access-the-adobe-stock-search-grid) innehåller funktioner för frågor och filtrering som hjälper dig att hitta den perfekta bilden för dina [!DNL Commerce]-butiker.

Som standard kommer sökresultaten från ett galleri med några hundra resultat från Adobe Stock. När du gör en egen nyckelordssökning söker du efter de miljontals mediefiler som är tillgängliga via Adobe Stock.

### Söka efter Adobe Stock-resurser med nyckelord

1. [Öppna Adobe Stock Search-rutnätet](#access-the-adobe-stock-search-grid).

1. Ange din nyckelordssökning i indatafältet **[!UICONTROL Search by keyword]** i det övre vänstra hörnet och klicka på förstoringsglaset eller tryck på **Retur**.

   ![Adobe Stock sökresultat för nyckelordet mango](./assets/adobe-stock-search-keyword.png){width="600" zoomable="yes"}

### Filtrera Adobe Stock-resurser

1. [Kör en nyckelordssökning för Adobe Stock-resurser](#search-for-adobe-stock-assets-by-keywords).

1. Klicka på **[!UICONTROL Filters]**.

   Det finns flera filter för att förfina sökresultaten:

   | Filter | Beskrivning |
   |---|---|
   | [!UICONTROL Subcategory] | Filter för bilder som är **foton** eller **illustrationer** |
   | [!UICONTROL Orientation] | Filtrera bilder efter storlek, form och proportioner |
   | [!UICONTROL Color] | Använda en färgpalett för att filtrera bilder efter färg |
   | [!UICONTROL Price] | Filtrera efter bilder baserat på deras kostnad |
   | [!UICONTROL Safe search] | Aktivera eller inaktivera säker sökning |
   | [!UICONTROL Isolated Assets] | Begränsa visningen till endast _isolerade resurser_, som har objekt som visas fristående på en solid bakgrund |

   {style="table-layout:auto"}

   ![Adobe Stock sökfilter](./assets/adobe-stock-filters.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Apply Filters]**.

   Sökresultatstödrastret uppdateras med den förfinade sökningen.

## Visa bildinformation

Varje bild har information som kan visas. Ytterligare bildspecifika åtgärder, som att [spara förhandsvisningar](adobe-stock-save-preview.md) eller [spara (och eventuellt licensiera) bilder](adobe-stock-license-image.md), är tillgängliga via den här detaljerade vyn.

1. [Öppna Adobe Stock sökrutnät](#access-the-adobe-stock-search-grid).

1. Klicka på en bild i sökresultatet.

   Ytterligare bildinformation visas, till exempel:

   - En större version av bilden
   - Metadata för bilder, som _[!UICONTROL Dimensions]_,_[!UICONTROL File type]_, _[!UICONTROL Category]_,_[!UICONTROL File]_ och _nyckelord_
   - Relaterade bilder, till exempel bilder från samma _serie_ eller _modell_
   - Åtgärdsknappar, som [[!UICONTROL Save Preview]](adobe-stock-save-preview.md) och [[!UICONTROL Save (and optionally license) Image]](adobe-stock-license-image.md)

     ![Information om Adobe Stock-bilder](./assets/adobe-stock-image-details.png){width="600" zoomable="yes"}

## Logga in på ditt Adobe-konto

Om du vill få fullständig åtkomst till en bild och ta bort Adobe Stock-vattenstämpeln måste du [logga in med ett Adobe-konto](https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html) och köpa krediter för att licensiera rättigheterna att använda en bild.

1. [Öppna Adobe Stock Search-rutnätet](#access-the-adobe-stock-search-grid).

1. Klicka på **[!UICONTROL Sign In]** överst till höger.

   Ett nytt webbläsarfönster guidar dig genom inloggningsprocessen [Adobe](https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html).

   När du har slutfört inloggningsprocessen visas det licensierade läget för bilder i sökresultaten som en etikett.

   ![Adobe-inloggning](./assets/adobe-stock-account-login.png){width="600" zoomable="yes"}

### Visa det licensierade läget för sökresultat

[Logga in på ditt Adobe-konto](#log-in-to-your-adobe-account).

Alla licensierade bilder som är kopplade till ditt Adobe-konto har en etikett som visar vilka bilder du har licensierat.

![Adobe Stock sökresultat med licensierade bilder](./assets/adobe-stock-licensed-images.png){width="600" zoomable="yes"}

### Spara bilder i medielagringen

Bilder som söks igenom med Adobe Stock-integrering kan sparas i [!DNL Commerce] [medielagringen](media-storage.md) för enkel återanvändning i din [!DNL Commerce]-butik.

Du kan spara två typer av bilder: en [bildförhandsvisning](adobe-stock-save-preview.md) eller en [licensierad bild](adobe-stock-license-image.md).

#### Spara en bildförhandsvisning

En förhandsvisning är en vattenstämplad version av en Adobe Stock-resurs. Förhandsgranskning av bilder är kostnadsfria och ett bra sätt att experimentera med olika bilder innan du bestämmer dig för att köpa en licens för specifika bilder och använda dem i produktionsbutikerna.

1. [Öppna Adobe Stock sökrutnät](#access-the-adobe-stock-search-grid).

1. Om du vill [visa bildinformationen](#view-image-details) klickar du på en bild i sökstödrastret.

1. Klicka på **[!UICONTROL Save Preview]**.

   Den här åtgärden visar en uppmaning om att ange ett filnamn som används för att spara bilden i medielagringen. Ett standardfilnamn anges, men du kan anpassa namnet efter dina inställningar.

   ![Spara Adobe Stock-förhandsvisningsbild](./assets/adobe-stock-save-preview.png){width="500" zoomable="yes"}

1. Klicka på **[!UICONTROL Confirm]**.

   Sidan dirigeras om till medielagringen och den sparade förhandsvisningen visas.

#### Spara en licensierad bild

Adobe Stock-resurser som du vill använda för din produktion [!DNL Commerce]-butiker måste licensieras. Licensen säkerställer att du har laglig åtkomst till bilden och att du tar bort den Adobe Stock-vattenstämpel som finns i alla [bildförhandsvisningar](adobe-stock-save-preview.md). Om du vill licensiera bilder eller spara redan licensierade bilder måste du vara inloggad på ditt Adobe-konto.

1. [Logga in på ditt Adobe-konto](#log-in-to-your-adobe-account).

1. Om du vill [visa bildinformationen](#view-image-details) klickar du på en bild i sökstödrastret.

1. Beroende på den aktuella licensstatusen för bilden gör du något av följande:

   - Om bilden redan är licensierad klickar du på **[!UICONTROL Save]**.

   - Om bilden är _inte_ licensierad klickar du på **[!UICONTROL License and Save]**.

     >[!NOTE]
     >
     >Du måste ha [Adobe Stock-krediter](https://helpx.adobe.com/stock/help/credit-packs.html) tillgängliga på ditt konto för att licensiera bilden.

   Den här åtgärden visar en uppmaning om att ange ett filnamn som används för att spara bilden i [medielagringen](media-storage.md). Ett standardfilnamn anges, men du kan anpassa namnet efter dina inställningar.

1. Klicka på **[!UICONTROL Confirm]**.

   Sidan dirigeras om till medielagringen och den sparade förhandsvisningen visas.
