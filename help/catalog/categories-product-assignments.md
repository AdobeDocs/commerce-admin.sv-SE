---
title: Kategoriprodukttilldelningar
description: Läs om hur du använder inställningarna för [!UICONTROL Products in Category] för att kontrollera vilka produkter som för närvarande är tilldelade till kategorin.
exl-id: e7ab11c0-2d55-4824-a397-a1c858344d4f
feature: Catalog Management, Categories, Products
source-git-commit: 5aea3aa13ab0eb74866fc0cbcbfe08b5099abe95
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# Kategoriprodukttilldelningar

För en kategori använder du avsnittet _[!UICONTROL Products in Category]_för att granska de produkter som för närvarande är tilldelade till kategorin. Sökfiltren högst upp i varje kolumn används för att lägga till och ta bort produkter från kategorin. Du kan också använda [kategoriregler](../merchandising-promotions/category-product-rules.md) ( ![endast Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce) för att dynamiskt ändra produktvalet när en uppsättning villkor uppfylls. Mer information finns i [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md)).

>[!TIP]
>
>Under konfigurationen av kategoriregler sorteras produkterna __, _matchas_, _tilldelas_ och _inte tilldelade_ enligt den regeln **_endast_** när den här kategorin sparas. För att säkerställa att en ny produkt tilldelas enligt regeln när du lägger till den i katalogen måste du **spara om varje kategori** som är inställd på att matcha produkter enligt regel. Om någon produktStock-status ändras till `In Stock` eller `Out of Stock` och produkterna i kategorin _sorteras_ enligt regeln **Automatisk sortering** måste du klicka på **[!UICONTROL Save Category]**.

![Kategoriprodukter](./assets/category-products-in-category.png){width="600" zoomable="yes"}

>[!NOTE]
>
>I kolumnen _Stock_ visas endast tillgänglig produktkvantitet för _**det valda kategoriomfånget**_. När flera lager hanteras för produkter bör du växla mellan motsvarande omfång för att visa andra _Stock_-kolumnvärden i rutnätet _Kategoriprodukter_.

## Använd en kategoriregel

{{ee-feature}}

1. Ange **[!UICONTROL Match products by rule]** till `Yes`.

   Alternativen för automatisk sortering och villkor visas.

   ![Matcha produkter efter regel](./assets/category-match-products-by-rule.png){width="600" zoomable="yes"}

1. Ange ordningen **[!UICONTROL Automatic Sorting]**.

   Den här automatiska sorteringen baseras på aktuella förhållanden.

   - `Stock level` - Flytta uppåt eller nedåt.
   - `Special price` - Flytta uppåt eller nedåt.
   - `New Products` - Visa de senaste produkterna först.
   - `Color` - Sortera i bokstavsordning efter färg.
   - `Name` - Sortera i stigande eller fallande ordning efter namn.
   - `SKU` - Sortera i stigande eller fallande ordning efter SKU
   - `Price` - Sortera i stigande eller fallande ordning efter pris.

1. Klicka på **[!UICONTROL Add Condition]** och gör följande:

   - Välj den **[!UICONTROL Attribute]** som utgör grunden för villkoret.
   - Välj **[!UICONTROL Operator]** som krävs för att bilda uttrycket.
   - Ange **[!UICONTROL Value]** som ska matchas.

   ![Lägg till villkor i kategoriregel](./assets/category-rule-create.png){width="600" zoomable="yes"}

   Upprepa den här processen för varje attribut som ska användas för att beskriva de villkor som ska uppfyllas. Om du till exempel vill matcha produkter som skapades för 7 till 30 dagar sedan gör du följande:

   - Ange **[!UICONTROL Date Created]** till `Less than 30`.
   - Ange **[!UICONTROL Logic]** till `AND`.
   - Ange **[!UICONTROL Date Modified]** till `Greater than 7`.

1. Klicka på **[!UICONTROL Save Category]** när du är klar.

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
| [!UICONTROL Attribute] | Anger det attribut som används som bas för villkoret. Alternativ: <br/>**[!UICONTROL Clone Category ID(s)]**- Klonar produkter dynamiskt, utan sortering och ordning, från flera kategorier baserat på kategori-ID.<br/>**[!UICONTROL Color]** - Inkluderar produkter baserade på färg. <br/>**[!UICONTROL Date Created (days ago)]**- Inkluderar produkter baserat på antalet dagar sedan produkterna lades till i katalogen.<br/>**[!UICONTROL Date Modified (days ago)]** - Inkluderar produkter baserat på antalet dagar sedan produkterna senast ändrades. <br/>**[!UICONTROL Name]**- Inkluderar produkter baserat på produktnamnet.<br/>**[!UICONTROL Price]** - Inkluderar produkter baserat på pris. <br/>**[!UICONTROL Quantity]**- Inkluderar produkter baserat på lagerkvantiteten.<br/>** SKU **- Innehåller produkter baserade på SKU. |
| [!UICONTROL Operator] | Anger den operator som används i attributvärdet för att uppfylla villkoret. Om ingen operator anges används `Equal` som standard. Alternativ: `Equal` / `Not equal` / `Greater than` / `Greater than or equal to` / `Less than` / `Less than or equal to` / `Contains` |
| [!UICONTROL Value] | Anger det värde som attributet måste ha för att uppfylla villkoret. |
| [!UICONTROL Logic] | Används för att definiera flera villkor och visas bara när ett annat villkor läggs till. Alternativ: `OR` / `AND` |

{style="table-layout:auto"}

>[!NOTE]
>
>Kvantiteten för en konfigurerbar produkt med underordnade alternativ beräknas genom att kombinera alla underordnade produktkvantiteter. Ta ett exempel på en konfigurerbar produkt _Endurance Fitness Tank_ med färgalternativen lila, röd och gul och olika mängder av varje. I det här scenariot är den överordnade produktkvantiteten den kombinerade kvantiteten för de lila, röda och gula underordnade produkterna.

## Kontroller


## Sidkontroller

{{ee-feature}}

| Kontroll | Beskrivning |
|----------|--------------|
| ![Visa som lista](../assets/icon-view-list.png) | Visa som lista |
| ![Visa som rutor](../assets/icon-view-tiles.png) | Visa som rutor |
| ![Växla inte](../assets/toggle-no.png) | Matcha enligt regel - Nej |
| ![Växla ja](../assets/toggle-yes.png) | Matcha enligt regel - Ja |
| ![Flytta kontrollenhet](../assets/icon-move.png) | Med dra-och-släpp-kontrollen kan du ta tag i en produkt och flytta den till en annan plats på stödrastrets aktuella sida. Mer information finns i [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md). |
| ![Positionskontrollen](../assets/control-position.png) | Bestämmer produktens position i listan. |

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
