---
title: Produktlista
description: Lär dig mer om sidan _[!UICONTROL Products]_ i Admin, där du kan skapa produkter och redigera befintliga.
exl-id: 47e14f72-017f-456a-8904-6d32ef47e6f1
feature: Catalog Management, Products, Admin Workspace
source-git-commit: 8bb91b80f8ba957676c654e984deb5704b777612
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---

# Produktlista

Alla produkter i katalogen är tillgängliga från sidan _[!UICONTROL Products]_&#x200B;i Admin, där du kan skapa produkter och redigera befintliga. Vid installation på flera platser kan varje webbplats erbjuda olika produkter som ska säljas från samma katalog.

Listan _[!UICONTROL Products]_&#x200B;innehåller alla produkter i katalogen, visar de webbplatser där de är tillgängliga och om de är aktiverade för försäljning. I Adobe Commerce B2B-installationer där [delade kataloger](../b2b/catalog-shared.md) är aktiverade innehåller rutnätet en kolumn som anger vilka produkter som har alternativa rabattpriser i en delad katalog.

Du kan bläddra igenom listsidan efter sida eller söka efter specifika produkter. Använd [standardkontrollerna](../getting-started/admin-grid-controls.md) för att sortera och filtrera listan och tillämpa [åtgärder](../getting-started/admin-actions-control.md) på valda produkter.

![Rutnät för produkter](./assets/products-grid.png){width="700" zoomable="yes"}

## Begränsa produktvisning

För att förbättra prestanda för stora kataloger rekommenderar vi att du begränsar antalet produkter som visas i rutnätet. Du kan begränsa vilka produktrutnät som visas för:

- Produkter
- Lägg till relaterade produkter/merförsäljning/korsförsäljning
- Lägg till produkter i programpaketet
- Lägg till produkter i gruppprodukt
- Skapa order (administratör)

Den här konfigurationsinställningen för produktvisningsbegränsning är inaktiverad som standard. Genom att aktivera det kan du begränsa antalet produkter i rutnätet till ett visst värde. Om den är aktiverad och antalet matchande produkter för rutnätsvisningen är större än postgränsen, returneras en begränsad postmängd. När gränsen nås visas inte totalt antal poster, antal markerade poster och sidnumreringselement i rutnätets rubrik.

>[!NOTE]
>
>Om du inte vill att produktrutnätet ska begränsas använder du filter mer exakt för att skapa en samling som har färre objekt än det antal som anges i fältet _[!UICONTROL Records Limit]_.

**_Så här konfigurerar du produktvisningsbegränsningen:_**

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Advanced]** och välj **[!UICONTROL Admin]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Admin Grids]** och gör följande:

   - Ange **[!UICONTROL Limit Number of Products in Grid]** till `Yes`.

   - (Valfritt) Ange ett värde i fältet **[!UICONTROL Records Limit]** för att begränsa antalet produkter i rutnätet till ett visst värde. Standardminimivärdet är `20000`.

   ![Konfigurationsinställningar för administratörsstödraster](../configuration-reference/advanced/assets/admin-admin-grids.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Sidkontroller

| Kontroll | Beskrivning |
|--- |--- |
| [!UICONTROL Add Product] | Startar processen att skapa en ny enkel produkt. Klicka på nedpilen om du vill välja en viss produkttyp. Alternativ: [[!UICONTROL Simple Product]](product-create-simple.md) / [[!UICONTROL Configurable Product]](product-create-configurable.md) / [[!UICONTROL Grouped Product]](product-create-grouped.md) / [[!UICONTROL Virtual Product]](product-create-virtual.md) / [[!UICONTROL Bundle Product]](product-create-bundle.md) / [[!UICONTROL Downloadable Product]](product-create-downloadable.md) / [[!UICONTROL Gift Card]](product-gift-card-create.md) |
| [!UICONTROL Actions] | Visar alla åtgärder som kan tillämpas på valda produkter i listan. Om du vill utföra en åtgärd på en produkt eller produktgrupp markerar du kryssrutan i den första kolumnen i varje produkt. Alternativ: `Delete` / `Change Status` / `Update Attributes` / `Assign Inventory Source` / `Unassign Inventory Source` / `Transfer Inventory To Source` |
| [!UICONTROL Filters] | Startar en katalogsökning baserat på de aktuella filtren. |
| [!UICONTROL Default View] | Anger den aktuella stödrasterkolumnlayouten. Om det finns sparade stödrasterkolumnvyer kan du välja en annan. |
| [!UICONTROL Columns] | Visar alla åtgärder som kan tillämpas på valda produkter i listan. Om du vill utföra en åtgärd på en produkt eller produktgrupp markerar du kryssrutan i den första kolumnen i varje produkt. |
| [!UICONTROL Search by keyword] | Sökrutan i det övre vänstra hörnet används för att hitta produkter efter nyckelord. |
| [!UICONTROL Edit] | Öppnar produkten i redigeringsläge. Du kan åstadkomma samma sak genom att klicka var som helst på raden. |

{style="table-layout:auto"}

## Standardkolumner

| Kolumn | Beskrivning |
|--- |--- |
| (Kryssruta) | Väljer att flera poster ska bli föremål för en åtgärd. Kryssrutan i den första kolumnen i varje vald post är markerad. Alternativ: <br/>**[!UICONTROL Select All]**- Markerar alla poster som hittats och som matchar de aktuella filterinställningarna.<br/>**[!UICONTROL Select All on This Page]** - Markerar bara de poster som finns på den aktuella sidan och som matchar filterinställningarna. |
| [!UICONTROL ID] | Ett unikt sekventiellt nummer som tilldelas när en ny produkt sparas för första gången. |
| [!UICONTROL Thumbnail] | Visar en miniatyrbild av huvudproduktbilden. |
| [!UICONTROL Name] | Produktnamnet. |
| [!UICONTROL Type] | Produkttypen. |
| [!UICONTROL Attribute Set] | Namnet på den attributuppsättning som används som mall för produkten. |
| [!UICONTROL SKU] | Den unika lagringsenhet som är tilldelad produkten. |
| [!UICONTROL Price] | Enhetspriset för produkten. |
| [!UICONTROL Quantity] | Den kvantitet som finns i lager. |
| [!UICONTROL Salable Quantity] | Summan av alla tillgängliga enheter för denna produkt. |
| [!UICONTROL Visibility] | Anger var produkten visas i katalogen. Alternativ: `Not Visible Individually` / `Catalog` / `Search` / `Catalog, Search` |
| [!UICONTROL Status] | Anger produktens status. Alternativ: `Enabled` och `Disabled` |
| [!UICONTROL Websites] | Anger de webbplatser där produkten finns tillgänglig. |
| [!UICONTROL Action] | Öppnar produkten i redigeringsläge. |
| [!UICONTROL Shared Catalog] | ![Adobe Commerce B2B](../assets/b2b.svg) (endast tillgängligt med [Adobe Commerce B2B](./b2b/../introduction.md)) Anger de delade kataloger som innehåller anpassade priser för produkten. |

{style="table-layout:auto"}

## Andra kolumner

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Short Description] | Kort beskrivning av produkten. |
| [!UICONTROL Special Price From Date] | Det första datumet för specialpriskampanjen. |
| [!UICONTROL Special Price To Date] | Sista datumet för specialpriskampanjen. |
| [!UICONTROL Cost] | Artikelns faktiska kostnad. |
| [!UICONTROL Manufacturer] | Produkttillverkaren. |
| [!UICONTROL Meta Keywords] | Meta keywords for the product. |
| [!UICONTROL Color] | Produktfärgen. |
| [!UICONTROL Set Product as New from Date] | Det första datumet för den angivna produkten som en ny kampanj. |
| [!UICONTROL Set Product as New to Date] | Det sista datumet för den angivna produkten som en ny kampanj. |
| [!UICONTROL Active From / To] | Startdatum och slutdatum för produkten. |
| [!UICONTROL Layout] | Produktlayouten. |
| [!UICONTROL Minimum Advertised Price] | Det lägsta annonserade priset för produkten. |
| [!UICONTROL Allow Gift Message] | Presentkort till kunder som köper ett presentkort. |
| [!UICONTROL Special Price] | Specialpris för produkten. |
| [!UICONTROL Weight] | Produktens vikt. |
| [!UICONTROL Meta Title] | Produktens metanamn. |
| [!UICONTROL Meta Description] | Beskrivning av produktmetadata. |
| [!UICONTROL Country of Manufacture] | Tillverkningslandet. |
| [!UICONTROL New Theme] | Anpassat tema har använts på produkten. |
| [!UICONTROL URL Key] | Produktens URL-nyckel. |
| [!UICONTROL Tax Class] | Produktmomsklassen. |
| [!UICONTROL Allow Gift Message] | Visar tillgängligheten för presentmeddelandealternativet för produkten. |

{style="table-layout:auto"}
