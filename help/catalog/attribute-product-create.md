---
title: Skapa och ta bort produktattribut
description: Lär dig hur du skapar och tar bort produktattribut, som används för att beskriva specifika egenskaper för produkterna i din katalog.
exl-id: fd0e5d5b-a917-4e55-8ec2-7ebb040d3d06
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1159'
ht-degree: 0%

---

# Skapa och ta bort produktattribut

Du kan skapa attribut när du arbetar med en produkt eller från _[!UICONTROL Product Attributes]_sida. Följande steg visar hur du skapar attribut från_[!UICONTROL Stores]_ -menyn.

## Steg 1: Beskriv de grundläggande attributegenskaperna

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Klicka på **[!UICONTROL Add New Attribute]**.

   ![Nya attributegenskaper](./assets/attribute-properties.png){width="600" zoomable="yes"}

1. För **[!UICONTROL Default Label]** anger du en etikett som identifierar attributet.

1. Ange vilken typ av indatakontroll som ska användas för datainmatning **[!UICONTROL Catalog Input Type for Store Owner]** till något av följande:

   | Egenskap | Beskrivning |
   |--- |--- |
   | `Text Field` | Ett enradigt inmatningsfält för text. |
   | `Text Area` | Ett inmatningsfält med flera rader för att skriva textstycken, som en produktbeskrivning. Du kan använda WYSIWYG-redigeraren för att formatera texten med HTML-taggar, eller ange taggarna direkt i texten. |
   | `Text Editor` | En fullt fungerande textredigerare på attributplatsen. |
   | Datum | Visar ett datumvärde i [format](attributes-input-types.md#date-and-time-options) och [tidszon](../getting-started/store-details.md#locale-options). Datumvärden kan väljas från en lista eller en kalender ( ![Kalenderikon](../assets/icon-calendar.png) ). <br/><br/>**_Obs!_**Beroende på systemkonfigurationen,_Administratör _-användare kan ange datum direkt i ett fält eller välja ett datum i kalendern eller listan. Mer information om hur du anger datum- och tidsvärden finns i [Alternativ för datum och tid](attributes-input-types.md#date-and-time-options). |
   | `Yes/No` | Visar en nedrullningsbar lista med fördefinierade alternativ för `Yes` och `No`. |
   | `Dropdown` | Visar en nedrullningsbar lista med värden som endast accepterar ett val. Indatatypen för listrutan är en nyckelkomponent i [konfigurerbara produkter](product-create-configurable.md). |
   | `Multiple Select` | Visar en nedrullningsbar lista med värden som accepterar flera val. |
   | `Price` | Den här indatatypen används för att skapa prisfält utöver de fördefinierade attributen: Price, Special Price, Tier Price och Cost. Valutan som används avgörs av systemkonfigurationen. |
   | `Media Image` | Kopplar en extra bild till en produkt, t.ex. en produktlogotyp, anvisningar för omvårdnad eller ingredienser från en livsmedelsetikett. När du lägger till ett mediabildsattribut i en produkts attributuppsättning blir det en extra bildtyp tillsammans med Base, Small och Thumbnail. Mediebildattributet kan uteslutas från [storefront media browser](catalog-images-video.md#storefront-media-browser). |
   | `Fixed Product Tax` | Här kan du definiera [FPT-räntor](../stores-purchase/fixed-product-tax.md) baserat på kraven för ditt språkområde. |
   | `Visual Swatch` | Visar en färgruta som visar färg, struktur eller mönster för en konfigurerbar produkt. A [visuell färgruta](swatches.md) kan fyllas med ett hexadecimalt färgvärde eller visas en överförd bild som representerar färg, material, struktur eller mönster för alternativet. |
   | `Text Swatch` | En textbaserad representation av ett konfigurerbart produktalternativ som ofta används för storlek. [Textfärgrutor](swatches.md#text-based-swatches) kan även innehålla hexadecimala färgvärden. |
   | `Page Builder` | En fullt fungerande [Page Builder](../page-builder/introduction.md) på den plats där attributet är placerat, vilket gör det enkelt att lägga till engagerande innehåll på produktsidan. |

   {style="table-layout:auto"}

1. Om du vill välja ett alternativ innan kunden kan köpa produkten anger du **[!UICONTROL Values Required]** till `Yes`.

1. För [!UICONTROL Dropdown] och [!UICONTROL Multiple Select] indatatyper, gör följande:

   - Under _[!UICONTROL Manage Options]_, klicka **[!UICONTROL Add Option]**.

   - Ange det första värdet som du vill ska visas i listan.

     Du kan ange ett värde för Admin och en översättning av värdet för varje butiksvy. Om du bara har en butiksvy kan du bara ange Admin-värdet och det används även för butiken.

   - Klicka **[!UICONTROL Add Option]** och upprepa föregående steg för varje alternativ som du vill ta med i listan.

   - Välj **[!UICONTROL Is Default]** om du vill använda alternativet som standardvärde.

   ![Produktattribut - alternativ för hantering](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

## Steg 2: Beskriv de avancerade egenskaperna (om det behövs)

1. Ange ett unikt **[!UICONTROL Attribute Code]** i gemener och utan blanksteg.

   ![Produktattribut - avancerade egenskaper](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

   Vilka alternativ som är tillgängliga beror på _[!UICONTROL Catalog Input Type for Store Owner]_inställning.

1. Ange **[!UICONTROL Scope]** för att ange var i [butikshierarki](../getting-started/websites-stores-views.md) att attributet kan användas.

1. Om du vill förhindra en dubblettvärdespost anger du **[!UICONTROL Unique Value]** till `Yes`.

1. För indatatyper som anges med värden kör du ett giltighetstest för alla data som anges i ett textfält genom att ange **[!UICONTROL Input Validation for Store Owner]** till den typ av data som fältet ska innehålla.

   Det här fältet är inte tillgängligt för indatatyper med valda värden. Testet kan validera något av följande:

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Indatavalidering](./assets/product-attribute-input-validation.png){width="400"}

1. Lägg till attributet i [Produktlista](products-list.md)anger du följande alternativ till `Yes`.

   - **Alternativ för Lägg till i kolumn** - Inkluderar attributet som en kolumn i _[!UICONTROL Products]_lista.
   - **Använd i filteralternativ** - Lägger till en filterkontroll i kolumnrubriken i _[!UICONTROL Products]_lista.

## Steg 3: Ange fältetiketten

1. I navigeringen till vänster väljer du **[!UICONTROL Manage Labels]**.

1. Ange en **[!UICONTROL Title]** som ska användas som etikett för fältet.

   Om din butik finns på olika språk kan du ange en översatt titel för varje vy.

   ![Produktattribut - hantera titlar](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## Steg 4: Beskriv egenskaperna för butiken

1. I navigeringen till vänster väljer du **[!UICONTROL Storefront Properties]**.

   ![Produktattribut - butiksegenskaper](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

   Vilka alternativ som är tillgängliga beror på _[!UICONTROL Catalog Input Type for Store Owner]_inställning.

1. Om attributet ska vara tillgängligt för sökning anger du **[!UICONTROL Use in Search]** till `Yes`.

   - Ange **[!UICONTROL Search Weight]** för att styra var objektet visas i sökresultatet: 1 (lägsta vikt) till 10 (högsta vikt).

   - Ange **[!UICONTROL Visible in Advanced Search]** efter behov. Läs mer i [Avancerad sökning](search.md#advanced-search).

1. Om du vill inkludera attributet i Produktjämförelse anger du **[!UICONTROL Comparable on Storefront]** till `Yes`.

1. Gör följande för listrutor, flera val och prisfält:

   - Om du vill använda attributet som ett filter vid navigering i lager anger du **[!UICONTROL Use in Layered Navigation]** till `Yes`.

   - Om du vill använda attributet i navigering i lager på sökresultatsidor anger du **[!UICONTROL Use in Search Results Layered Navigation]** till `Yes`.

   - För **[!UICONTROL Position]** anger du ett tal som anger attributets relativa position i navigeringsblocket med lager.

1. Om du vill använda attributet i prisregler anger du **[!UICONTROL Use for Promo Rule Conditions]** till `Yes`.

1. Om du vill att texten ska kunna formateras med HTML anger du **[!UICONTROL Allow HTML Tags on Frontend]** till `Yes`.

   Den här inställningen gör WYSIWYG-redigeraren tillgänglig för fältet.

1. Om du vill ta med attributet på produktsidan anger du **[!UICONTROL Visible on Catalog Pages on Storefront]** till `Yes`.

1. Ange följande inställningar om de stöds av ditt tema:

   - Om du vill inkludera attributet i produktlistor anger du **[!UICONTROL Used in Product Listing]** till `Yes`.

   - Om du vill använda attribut som en sorteringsparameter för produktlistor anger du **[!UICONTROL Used for Sorting in Product Listing]** till `Yes`.

1. När du är klar klickar du på **[!UICONTROL Save Attribute]**.

## Steg 5: Tilldela det skapade attributet till attributuppsättningen

För att ett attribut ska vara synligt på sidan för att skapa produkten lägger du till det i en specifik attributuppsättning.

1. När du har slutfört föregående steg går du till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Markera den attributuppsättning du behöver i listan och öppna den i redigeringsläge.

1. Dra det skapade attributet från **[!UICONTROL Unassigned Attributes]** till lämplig mapp i **Grupper** kolumn.

1. När du är klar klickar du på **[!UICONTROL Save]**.

## Attribut för konfigurerbara produkter

Alla attribut som används som en nedrullningsbar lista med alternativ för en [konfigurerbar produkt](product-create-configurable.md) måste ha följande egenskaper:

| Egenskap | Värde |
|----------|------ |
| Katalogindatatyp för butiksägare | Listruta |
| Omfång | Global |

{style="table-layout:auto"}

## Ta bort ett attribut

När ett attribut tas bort tas det bort från alla relaterade produkter och attributuppsättningar. Systemattribut ingår i butikens kärnfunktioner och kan inte tas bort.

Innan du tar bort ett attribut bör du kontrollera att det inte används av någon produkt i katalogen. Ett enkelt sätt att avgöra om ett attribut används är att använda [Exportera](../systems/data-export.md) för att kontrollera listan med produktentitetsattribut. Om attributet inte finns med i listan används det inte av några produkter i katalogen.

**_Ta bort ett attribut:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Leta reda på attributet i listan och öppna i redigeringsläge.

1. Klicka på **[!UICONTROL Delete Attribute]**.

   ![Ta bort attribut](./assets/attribute-delete.png){width="600" zoomable="yes"}

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.
