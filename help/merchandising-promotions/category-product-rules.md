---
title: Kategoriregler för försäljning
description: Lär dig hur du skapar en regel som dynamiskt ändrar produktval enligt en uppsättning villkor.
exl-id: 765b863a-bb83-418b-9fca-ef0a148b09eb
feature: Categories, Merchandising
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 0%

---

# Kategoriregler för försäljning

{{ee-feature}}

Kategorireglerna ändrar dynamiskt produkturvalet enligt en uppsättning villkor. Varje kategori kan bara ha en kategoriregel, även om den enskilda regeln kan ha flera villkor. Du kan till exempel skapa en kategoriregel för ett visst varumärke. Produkter av samma varumärke läggs automatiskt till i listan, även om de inte tillhör samma kategori. Du kan lägga till så många villkor i uttrycket som behövs för att beskriva de produkter som du vill inkludera.

>[!TIP]
>
>Under konfigurationen av kategoriregler sorteras produkterna __, _matchas_, _tilldelas_ och _inte tilldelade_ enligt den regeln **_endast_** när den här kategorin sparas. Om du till exempel lägger till en produkt i katalogen och vill tilldela den enligt regeln, måste du **spara om varje kategori** som är inställd på att matcha produkter enligt regel. Om någon produktStock-status ändras till `In Stock` eller `Out of Stock` och produkterna i kategorin ska vara _sorterade_ enligt regeln **[!UICONTROL Automatic Sorting]** måste du klicka på **[!UICONTROL Save Category]**.

Varje villkor består av en attribut-, value- och logisk operator. Endast attribut med egenskapen _[[!UICONTROL Use in Product Listing]](../catalog/attribute-product-create.md)_inställd på `Yes` kan användas i kategoriregler. Du måste ange den här egenskapen för attributet om du vill använda ett attribut som inte finns med i produktlistor. Även om datumattribut inte stöds kan du använda attributen Skapad den eller Ändrad den för att definiera ett datum eller datumintervall. Om du till exempel bara vill inkludera produkter som har skapats under den senaste veckan anger du värdet `<7` för Skapad den.

>[!NOTE]
>
>Se till att konfigurera varje attribut som används i regeln som ett [_smart_-attribut](smart-attributes-configure.md).

![Kategoriproduktregel](../catalog/assets/category-product-rule-with-stock.png){width="600" zoomable="yes"}

Regler för kategoriprodukter kan snabba upp processen att tilldela specifika produkter till kategorier, baserat på villkor som bestämmer vilka produkter som visas i kategorin. De&quot;smarta&quot; attribut som kan användas med kategoriproduktregler anges i [Visual Merchandiser](visual-merchandiser.md) -konfigurationen.

>[!NOTE]
>
>Var försiktig när du tillämpar en kategoriproduktregel eftersom produkter som inte uppfyller villkoret tas bort från kategorin. Om du t.ex. skapar en regel som endast innehåller lila tanktoppar tas alla andra tanktoppar bort från kategorin.

## Steg 1: Konfigurera attributen _smart_

1. Kontrollera att egenskapen [[!UICONTROL Use in Product Listing]](../catalog/product-attributes.md) storefront är inställd på `Yes` för varje attribut som ska användas i regeln.

   >[!NOTE]
   >
   >Se till att attributet som du väljer INTE är en multiselect _[!UICONTROL Input Type]_.

1. Slutför [konfigurationen](smart-attributes-configure.md) för att identifiera varje _smart_-attribut som ska användas med Visual Merchandiser.

## Steg 2: Skapa kategoriregeln

1. Öppna kategorin som ska redigeras i kategoriträdet.

1. I avsnittet **[!UICONTROL Products in Category]** anger du **[!UICONTROL Match products by rule]** till `Yes`.

   Alternativen för automatisk sortering och villkor visas.

1. Klicka på **[!UICONTROL Add Condition]**.

1. Välj den **[!UICONTROL Attribute]** som utgör grunden för villkoret.

1. Ange **[!UICONTROL Operator]** till något av följande:

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. Ange **[!UICONTROL Value]** som ska matchas.

   ![Lägg till villkor i kategoriregel](../catalog/assets/category-rule-create.png){width="500"}

1. Upprepa den här processen för varje attribut som behövs för att beskriva de villkor som ska uppfyllas.

   Om du till exempel vill matcha produkter som skapades för mellan sju och 30 dagar sedan gör du följande:

   - Ange **[!UICONTROL Date Created]** till `Less than 30`.

   - Ange **[!UICONTROL Logic]** till `AND`.

     >[!NOTE]
     >
     >När du väljer `AND` gäller regeln produkter där alla villkor är uppfyllda. När du väljer `OR` gäller det för produkter där minst ett villkor är uppfyllt.

   - Ange **[!UICONTROL Date Modified]** till `Greater than 7`.

1. Om du vill använda en sorteringsordning automatiskt på den dynamiskt genererade produktlistan anger du **[!UICONTROL Automatic Sorting]**.

   ![Automatisk sortering](./assets/automatic-sorting-field.png){width="600" zoomable="yes"}

   Alternativ för sorteringsordning definieras globalt och används baserat på aktuella villkor. Du kan inte ange en annan sorteringsordning för vynivå för webbplatsen, butiken eller butiken.

   | Sorteringsalternativ | Beskrivning |
   |-----------| -----------|
   | [!UICONTROL Stock quantity] | Sortera baserat på lager, uppifrån eller ned: `Move low stock to top` eller `Move out of stock to bottom` |
   | [!UICONTROL Special price] | Sortera baserat på pris, uppifrån eller ned: `Special price to top` eller `Special price to bottom` |
   | [!UICONTROL New Products] | Visa de senaste produkterna: `Newest products first` |
   | [!UICONTROL Color] | Sortera i bokstavsordning efter färg: `Sort by color` |
   | [!UICONTROL Product Names] | Sortera efter namn i stigande eller fallande ordning: `Name A - Z` eller `Name Z -A` |
   | [!UICONTROL SKU] | Sortera efter SKU i stigande eller fallande ordning: `SKU: Ascending` eller `SKU: Descending` |
   | [!UICONTROL Price] | Sortera efter pris i stigande eller fallande ordning: `Price: High to low` eller `Price: Low to high` |

   {style="table-layout:auto"}

1. Klicka på **[!UICONTROL Save Category]** när du är klar.

>[!NOTE]
>
>När du ställer in en kategoriregel matchas produkterna och tilldelas till regeln när kategorin sparas. Om du lägger till en produkt i katalogen och vill inkludera den i regeln, måste du spara om varje kategori som är inställd på att matcha produkter enligt regel. Detta säkerställer att den nya produkten ingår.

### Menyalternativ

- **[!UICONTROL Match products by rule]** - Anger om listan med produkter i kategorin dynamiskt genereras av en kategoriregel. Alternativ: `Yes` / `No`

- **[!UICONTROL Automatic Sorting]** - Använder automatiskt en sorteringsordning i listan med kategoriprodukter. Alternativ: `None`, `Move low stock to top`, `Move low stock to bottom`, `Special price to top`, `Special price to bottom`, `Newest products first`, `Sort by color`, `Name: A - Z`, `Name: Z - A`, `SKU: Ascending`, `SKU: Descending`, `Price: High to Low` och `Price: Low to High`

  >[!NOTE]
  >
  >Om du har en konfigurerbar produkt med underordnade produkter, beräknas den överordnade produkten baserat på den kombinerade summan av underordnade produktlager. Tänk dig ett exempel där du har konfigurerbar produkt _Proteus Fitness Shirt_ med orange, röd och gul underordnade produkter med olika lagerkvantiteter. Det överordnade produktlagret beräknas baserat på den sammanlagda summan av lager av orangea, röda och gula underordnade produkter. Med alternativet `Move low stock to top` beräknas beståndet av överordnade produkter genom att alla dess säljbara underordnade produkter kombineras och sorteras därefter.

- **[!UICONTROL Add Condition]** - Lägger till ett annat villkor i regeln.

- **[!UICONTROL Attribute]** - Bestämmer vilket attribut som används som grund för villkoret. Alternativ:

  | Alternativ | Beskrivning |
  | ------ | ----------- |
  | `Clone Category ID(s)` | Klonar dynamiskt produkter, utan sortering och ordning, från flera kategorier baserade på kategori-ID. |
  | `Color` | Inkluderar produkter baserade på färg. |
  | `Date Created (days ago)` | Inkluderar produkter baserat på antalet dagar sedan produkterna lades till i katalogen. |
  | `Date Modified (days ago)` | Inkluderar produkter baserat på antalet dagar sedan produkterna senast ändrades. |
  | `Name` | Inkluderar produkter baserat på produktnamnet. |
  | `Price` | Inkluderar produkter baserade på pris. Det här attributet gäller inte för konfigurerbara produkter eftersom de inte har ett eget pris. |
  | `Quantity` | Inkluderar produkter baserat på lagerkvantiteten. |
  | `SKU` | Innehåller produkter baserade på SKU. |

  {style="table-layout:auto"}

  >[!NOTE]
  >
  >Kvantiteten för en konfigurerbar produkt med underordnade alternativ beräknas genom att kombinera alla säljbara underordnade produktkvantiteter. Tänk dig ett exempel där du har en konfigurerbar produkt, _Grundläggande träningstank_, med färgalternativen lila, rött och gult och olika mängder av varje. I det här fallet är kvantiteten för den överordnade produkten (Basic Fitness Tank) den sammanlagda säljbara kvantiteten för de lila, röda och gula underordnade färgprodukterna.

- **[!UICONTROL Operator]** - Anger den operator som används i attributvärdet för att uppfylla villkoret. Om ingen operator anges används `Equal` som standard. Alternativ: `Equal`, `Not equal`, `Greater than`, `Greater than or equal to`, `Less than`, `Less than or equal to` och `Contains`

- **[!UICONTROL Value]** - Anger det värde som attributet måste ha för att uppfylla villkoret.

- **[!UICONTROL Logic]** - Logikkolumnen används för att definiera flera villkor och visas bara när ett annat villkor läggs till. Operatorerna följer reglerna för prioritet för MySQL [booleska operatorer](https://dev.mysql.com/doc/refman/8.0/en/operator-precedence.html). Alternativ: `AND` / `OR`
