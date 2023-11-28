---
title: Lägga till attribut i en produkt
description: Lär dig hur du lägger till attribut till produkter i din katalog.
exl-id: 1f92807a-2362-48a2-8d3a-4aef90a5671f
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# Lägga till attribut i en produkt

Även om attribut i första hand hanteras från [Lager](../stores-purchase/stores-menu.md) kan du också lägga till nya attribut _i farten_ när du arbetar med en produkt. Du kan välja i listan över befintliga attribut eller skapa ett attribut. Det nya attributet läggs till i [attributuppsättning](../catalog/attribute-sets.md) som produkten baseras på.

## Steg 1: Lägg till ett attribut

1. Öppna produkten i redigeringsläge.

1. Klicka på i det övre högra hörnet **[!UICONTROL Add Attribute]**.

   ![Ny produkt med standardattributuppsättning](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. Använd alternativet [filterkontroller](../getting-started/admin-grid-controls.md) om du vill hitta attributet i rutnätet och göra följande:

   - Markera kryssrutan i den första kolumnen i varje attribut som ska läggas till.

   - Klicka på **[!UICONTROL Add Selected]**.

   ![Välj ett attribut](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. Om du vill definiera ett nytt attribut klickar du **[!UICONTROL Create New Attribute]** och slutför objekten i steg 2.

## Steg 2: Beskriv de grundläggande attributegenskaperna

![Attributegenskaper](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. Under _[!UICONTROL Attribute Properties]_, ange en **[!UICONTROL Attribute Label]**för att identifiera attributet.

1. Ange **[!UICONTROL Catalog Input Type for Store Owner]** till typen av [indatakontroll](attributes-input-types.md) som ska användas för datainmatning.

   Om attributet används för en [konfigurerbar produkt](product-create-configurable.md), välja `Dropdown`. Sedan anger du **[!UICONTROL Required]** till `Yes`.

1. För `Dropdown` och `Multiple Select` indatatyper, gör följande:

   - Under **[!UICONTROL Values]**, klicka **[!UICONTROL Add Value]**.

   - Ange det första värdet som du vill ska visas i listan.

     Du kan ange ett värde för Admin och en översättning av värdet för varje butiksvy. Om du bara har en butiksvy kan du bara ange Admin-värdet, och det används även för butiken.

   - Klicka **[!UICONTROL Add Value]** och upprepa föregående steg för varje alternativ som du vill ta med i listan.

   - Välj **[!UICONTROL Is Default]** om du vill använda alternativet som standardvärde.

   ![Värden](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. Om du vill att kunden ska välja ett alternativ innan produkten kan köpas anger du **[!UICONTROL Required]** till `Yes`.

## Steg 3: Beskriv de avancerade egenskaperna (valfritt)

![Avancerade attributegenskaper](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. Ange ett unikt **[!UICONTROL Attribute Code]** i gemener och utan blanksteg.

1. Ange **[!UICONTROL Scope]** för att ange var i butikshierarkin attributet kan användas.

   Om attributet används för en [konfigurerbar produkt](product-create-configurable.md), välja `Global`.

1. Om det här attributet bara gäller för den här produkten anger du **[!UICONTROL Unique Value]** till `Yes`.

1. Om du vill köra ett giltighetstest av data som anges i ett textfält anger du **[!UICONTROL Input Validation for Store Owner]** till den typ av data som fältet ska innehålla.

   Det här fältet är inte tillgängligt för indatatyper med valda värden. Indatavalidering kan användas för något av följande:

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Indatavalidering](./assets/product-attribute-input-validation.png){width="500"}

1. Om du vill kunna ta med attributet som en kolumn i rutnätet Produkter anger du **[!UICONTROL Add to Column Options]** till `Yes`.

1. Om du vill kunna filtrera _[!UICONTROL Products]_stödraster efter den här kolumnen, ange **[!UICONTROL Use in Filter Options]**till `Yes`.

## Steg 4: Ange fältetiketten

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Manage titles]** -avsnitt.

1. Ange en **[!UICONTROL Title]** som ska användas som etikett för fältet.

   Om din butik finns på olika språk kan du ange en översatt titel för varje vy.

   ![Hantera titlar](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## Steg 5: Beskriv egenskaperna för butiken

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Storefront Properties]** -avsnitt.

   ![Egenskaper för Storefront](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. Om du vill göra attributet tillgängligt för sökning anger du **[!UICONTROL Use in Search]** till `Yes`.

1. Om du vill inkludera attributet i Produktjämförelse anger du **[!UICONTROL Comparable on Storefront]** till `Yes`.

1. Om du vill ta med listrutor, flera val eller prisattribut i navigeringen i lager anger du **[!UICONTROL Use in Search Results Layered Navigation]** till något av följande:

   - `Filterable (with results)` - Navigering i flera lager innehåller endast de filter för vilka matchande produkter kan hittas. Attributvärden som redan gäller för alla produkter som visas i listan visas inte som tillgängliga filter. Attributvärden med antalet noll (0) produktmatchningar utelämnas också från listan över tillgängliga filter.<br/><br/>Den filtrerade produktlistan innehåller bara de produkter som matchar filtret. Produktlistan uppdateras bara om de valda filtren ändrar vad som visas.

   - `Filterable (no results)` - Navigering i flera lager innehåller filter för alla tillgängliga attributvärden och deras produktantal, inklusive produkter med noll (0) produktmatchningar. Om attributvärdet är en färgruta visas värdet som ett filter, men stryks över.

1. Om du vill använda lagerstyrd navigering på sökresultatsidor anger du **[!UICONTROL Use in Search Results Navigation]** till `Yes` och ange ett tal i **[!UICONTROL Position]** fält.

   Positionsnumret anger den relativa positionen för attributet i det lageruppbyggda navigeringsblocket.

1. Om du vill använda attributet i prisregler anger du **[!UICONTROL Use for Promo Rule Conditions]** till `Yes`.

1. Om du vill att texten ska kunna formateras med HTML anger du **[!UICONTROL Allow HTML Tags on Storefront]** till `Yes`.

   Den här inställningen gör WYSIWYG-redigeraren tillgänglig när du redigerar fältet.

1. Om du vill ta med attributet på produktsidan anger du **[!UICONTROL Visible on Catalog Pages on Storefront]** till `Yes`.

1. Ange följande inställningar enligt temat:

   - Om du vill inkludera attributet i produktlistor anger du **[!UICONTROL Used in Product Listing]** till `Yes`.

   - Om du vill använda attribut som en sorteringsparameter för produktlistor anger du **[!UICONTROL Used for Sorting in Product Listing]** till `Yes`.

1. När du är klar klickar du på **[!UICONTROL Save Attribute]**.
