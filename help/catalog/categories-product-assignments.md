---
title: Kategoriprodukttilldelningar
description: Läs mer om hur du använder [!UICONTROL Products in Category] inställningar som styr vilka produkter som för närvarande är tilldelade kategorin.
exl-id: e7ab11c0-2d55-4824-a397-a1c858344d4f
feature: Catalog Management, Categories, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---

# Kategoriprodukttilldelningar

Använd _[!UICONTROL Products in Category]_för att granska de produkter som för närvarande är tilldelade kategorin. Sökfiltren högst upp i varje kolumn används för att lägga till och ta bort produkter från kategorin. Du kan också använda [kategoriregler](../merchandising-promotions/category-product-rules.md) ( ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce) för att dynamiskt ändra produktvalet när en uppsättning villkor uppfylls. Mer information finns på [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md)).

>[!TIP]
>
>Vid inställning av kategoriregel är produkterna _sorterad_, _matchad_, _tilldelad_ och _ej tilldelad_ enligt den regeln **_endast_** när den här kategorin sparas. Om du vill vara säker på att en ny produkt tilldelas enligt regeln när du lägger till den i katalogen **måste spara om varje kategori** som är inställt på att matcha produkter enligt regel. Om någon produktlagerstatus ändras till `In Stock` eller `Out of Stock` och produkterna i kategorin är _sorterad_ enligt **Automatisk sortering** regel måste du klicka **[!UICONTROL Save Category]**.

![Kategoriprodukter](./assets/category-products-in-category.png){width="600" zoomable="yes"}

>[!NOTE]
>
>På kategorisidorna `Out of stock` produkter alltid visas **_efter_** `In Stock` produkter i produktlistan med alla sorteringstyper.

>[!NOTE]
>
>The _Stock_ kolumn visar säljbar produktkvantitet för _**valt kategoriomfång**_ endast. När flera lager hanteras för produkter bör du växla mellan motsvarande omfång för att visa andra _Stock_ kolumnvärden i _Kategoriprodukter_ rutnät.

## Använd en kategoriregel

{{ee-feature}}

1. Ange **[!UICONTROL Match products by rule]** till `Yes`.

   Alternativen för automatisk sortering och villkor visas.

   ![Matcha produkter efter regel](./assets/category-match-products-by-rule.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Automatic Sorting]** beställa.

   Den här automatiska sorteringen baseras på aktuella förhållanden.

   - `Stock level` - Flytta uppåt eller nedåt.
   - `Special price` - Flytta uppåt eller nedåt.
   - `New Products` - Visa de nyaste produkterna först.
   - `Color` - Sortera i bokstavsordning efter färg.
   - `Name` - Sortera i stigande eller fallande ordning efter namn.
   - `SKU` - Sortera i stigande eller fallande ordning efter SKU
   - `Price` - Sortera i stigande eller fallande ordning efter pris.

1. Klicka **[!UICONTROL Add Condition]** och gör följande:

   - Välj **[!UICONTROL Attribute]** detta är grunden för villkoret.
   - Välj **[!UICONTROL Operator]** krävs för att bilda uttrycket.
   - Ange **[!UICONTROL Value]** som ska matchas.

   ![Lägg till villkor i kategoriregel](./assets/category-rule-create.png){width="600" zoomable="yes"}

   Upprepa den här processen för varje attribut som ska användas för att beskriva de villkor som ska uppfyllas. Om du till exempel vill matcha produkter som skapades för 7 till 30 dagar sedan gör du följande:

   - Ange **[!UICONTROL Date Created]** till `Less than 30`.
   - Ange **[!UICONTROL Logic]** till `AND`.
   - Ange **[!UICONTROL Date Modified]** till `Greater than 7`.

1. När du är klar klickar du på **[!UICONTROL Save Category]**.

### Sidalternativ

| Alternativ | Beskrivning |
|--- |--- |
| [!UICONTROL Match products by rule] | Avgör om listan med produkter i kategorin genereras dynamiskt av en kategoriregel. Alternativ: `Yes` / `No` |
| [!UICONTROL Automatic Sorting] | Använder automatiskt en sorteringsordning i listan med kategoriprodukter. Alternativ: <br/>`None`<br/>`Move low stock to top`<br/>`Move low stock to bottom`<br/>`Special price to top`<br/>`Special price to bottom`<br/>`Newest products first`<br/>`Sort by color`<br/>`Name: A - Z`<br/>`Name: Z - A`<br/>`SKU: Ascending`<br/>`SKU: Descending`<br/>`Price: High to Low`<br/>`Price: Low to High` |
| [!UICONTROL Add Condition] | Lägger till ett annat villkor till regeln. |

{style="table-layout:auto"}

### Sidvillkor

| Alternativ | Beskrivning |
|--- |--- |
| [!UICONTROL Attribute] | Anger det attribut som används som bas för villkoret. Alternativ: <br/>**[!UICONTROL Clone Category ID(s)]**- Klonar dynamiskt produkter, utan sortering och ordning, från flera kategorier baserade på kategori-ID.<br/>**[!UICONTROL Color]** - Innehåller produkter baserade på färg. <br/>**[!UICONTROL Date Created (days ago)]**- Inkluderar produkter baserat på antalet dagar sedan produkterna lades till i katalogen.<br/>**[!UICONTROL Date Modified (days ago)]** - Inkluderar produkter baserat på antalet dagar sedan produkterna senast ändrades. <br/>**[!UICONTROL Name]**- Inkluderar produkter baserat på produktnamnet.<br/>**[!UICONTROL Price]** - Inkluderar produkter baserade på pris. <br/>**[!UICONTROL Quantity]**- Inkluderar produkter baserat på lagerkvantiteten.<br/>** SKU **- Innehåller produkter baserade på SKU. |
| [!UICONTROL Operator] | Anger den operator som används i attributvärdet för att uppfylla villkoret. Om inte en operator anges, `Equal` används som standard. Alternativ: `Equal` / `Not equal` / `Greater than` / `Greater than or equal to` / `Less than` / `Less than or equal to` / `Contains` |
| [!UICONTROL Value] | Anger det värde som attributet måste ha för att uppfylla villkoret. |
| [!UICONTROL Logic] | Används för att definiera flera villkor och visas bara när ett annat villkor läggs till. Alternativ: `OR` / `AND` |

{style="table-layout:auto"}

>[!NOTE]
>
>Kvantiteten för en konfigurerbar produkt med underordnade alternativ beräknas genom att kombinera alla säljbara underordnade produktkvantiteter. Ta ett exempel på en konfigurerbar produkt _Tank för uthållighetsträning_ med färgalternativen lila, rött och gult och olika mängder av varje färg. I det här scenariot är den överordnade produktkvantiteten den sammanlagda försäljningsbara kvantiteten för de lila, röda och gula underordnade produkterna.

## Kontroller


## Sidkontroller

{{ee-feature}}

| Kontroll | Beskrivning |
|----------|--------------|
| ![Visa som lista](../assets/icon-view-list.png) | Visa som lista |
| ![Visa som rutor](../assets/icon-view-tiles.png) | Visa som rutor |
| ![Växla inte](../assets/toggle-no.png) | Matcha enligt regel - Nej |
| ![Växla ja](../assets/toggle-yes.png) | Matcha enligt regel - Ja |
| ![Flytta kontrollenhet](../assets/icon-move.png) | Med dra-och-släpp-kontrollen kan du ta tag i en produkt och flytta den till en annan plats på stödrastrets aktuella sida. Mer information finns på [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md). |
| ![Positionskontroll](../assets/control-position.png) | Bestämmer produktens position i listan. |

{style="table-layout:auto"}

## Sidkontroller

{{ce-feature}}

| Kontroll | Beskrivning |
|----------|--------------|
| ![Markerad kryssruta](../assets/checkbox-selected.png) | Använd kryssrutan i rubriken för den första kolumnen när du ska välja alla produkter eller ta bort alla val. Kontrollen i den första raden avgör typen av sökning och kan ställas in så att den inkluderar alla poster eller bara de poster som antingen är tilldelade kategorin eller inte. Kryssrutan i den första kolumnen på varje rad identifierar produkter som ska läggas till i kategorin. Alternativ: `Yes` / `No` / `Any` |
| [!UICONTROL Search Filters] | Filterkontrollerna högst upp i varje kolumn kan användas för att ange specifika värden som du vill ta med eller utelämna från listan, beroende på inställningen Markera alla. |
| [!UICONTROL Reset Filter] | Tar bort alla sökfilter. |
| [!UICONTROL Search] | Söker i katalogen baserat på filtervillkoren och visar resultatet. |

{style="table-layout:auto"}
