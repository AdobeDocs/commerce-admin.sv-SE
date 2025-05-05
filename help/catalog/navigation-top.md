---
title: Övre navigering
description: Lär dig hur du definierar huvudmenyn för en butik, som fungerar som en katalog för olika avdelningar.
exl-id: 8b71fe73-2716-4820-9e57-4cb1e6888132
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 0%

---

# Övre navigering

Huvudmenyn i din butik är som en katalog till de olika avdelningarna i din butik. Varje alternativ representerar en annan produktkategori. Placeringen och presentationen av den översta navigeringen kan variera beroende på tema, men hur den fungerar är i stort sett detsamma.

![Övre navigering](./assets/storefront-top-navigation.png){width="700" zoomable="yes"}

Katalogens kategoristruktur kan påverka hur bra webbplatsen indexeras av sökmotorer. Ju djupare inkapslad en kategori är, desto mindre sannolikt är det att den indexeras grundligt. I allmänhet är det mest effektiva att använda mellan en och tre synliga nivåer. Rotkategorin [&#128279;](category-root.md) räknas som den första nivån, men visas inte på menyn. Det maximala antalet nivåer som är tillgängliga i den översta navigeringen bestäms av konfigurationen. Dessutom kan det finnas en gräns för hur många menynivåer som stöds av ditt butikstema. Exempeltemat Luma har stöd för upp till fem nivåer, inklusive roten.

## Numrera menynivåer

| Objekt | Beskrivning |
|--- |--- |
| Nivå 1 | Den första nivån är rotkategorin, som i exempeldata heter &quot;Standardkategori&quot;. Roten är en behållare för menyn och dess namn visas inte som ett alternativ på menyn. |
| Nivå 2 | På en skrivbordsskärm är den översta navigeringen huvudmenyn som visas längst upp på sidan. På en mobil enhet visas huvudmenyn vanligtvis som en utfällbar meny med alternativ. Alternativen på andra nivån i Luma-butiken är _Nyheter_, _Kvinnor_, _Män_, _Kugghjul_, _Utbildning_ och _Försäljning_. |
| Nivå 3 | Den tredje nivån visas under varje alternativ på huvudmenyn. Under _Kvinnor_ är till exempel alternativen på den tredje nivån _Tops_ och _Bottoms_. |
| Nivå 4 | Alternativen på den fjärde nivån är underkategorier som utgår från ett alternativ på den tredje nivån. Under _Tops_ är till exempel alternativen på den fjärde nivån _Jackets_, _Hoodies &amp; Sweatshirts_, _Tees_ och _Bras &amp; Tank_. |

{style="table-layout:auto"}

## Ange den övre navigeringen

Om du vill att en kategori ska visas i den översta navigeringen i en butik utför du följande steg:

### Steg 1: Skapa en kategori

1. Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Categories]** på sidofältet _Admin_.

1. Ange en **[!UICONTROL Store View]** för att bestämma var den nya kategorin ska vara tillgänglig.

1. Välj den överordnade kategorin för den nya kategorin i kategoriträdet.

   Om du börjar från början utan data kan det bara finnas två kategorier i listan: _Standardkategori_, som är roten, och en _exempelkategori_.

1. Klicka på **[!UICONTROL Add Subcategory]**.

1. Fyll i den grundläggande informationen med följande inställningar:

   - **[!UICONTROL Enable Category]** inställd på `Yes`
   - **[!UICONTROL Include in Menu]** inställd på `Yes`

1. I visningsinställningen har **[!UICONTROL Anchor]** värdet `Yes`.

1. Slutför eventuella andra nödvändiga [kategoriinställningar](category-create.md).

1. Klicka på **[!UICONTROL Save]** när du är klar.

För en multibutiksinstallation kan en annan huvudmeny tilldelas som [rotkategori ](category-root.md) för varje [butik](../stores-purchase/stores.md#add-stores).

### Steg 2: Ange djupet för den översta navigeringen

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Catalog]** under.

1. Expandera avsnittet **[!UICONTROL Category Top Navigation]**.

   ![Övre kategorinavigering](../configuration-reference/catalog/assets/catalog-category-top-navigation.png){width="600" zoomable="yes"}

   Eftersom den översta navigeringens djup har ett globalt [konfigurationsomfång](../getting-started/websites-stores-views.md#scope-settings) gäller inställningen alla webbplatser, butiker och butiksvyer i Commerce-installationen. Konfigurationsavsnittet _[!UICONTROL Category Top Navigation]_&#x200B;är bara tillgängligt när&#x200B;_[!UICONTROL Store View]_ i det övre vänstra hörnet är inställt på `Default Config`.

   En detaljerad lista över dessa alternativ finns i [Övre navigering för kategori](../configuration-reference/catalog/catalog.md#layered-navigation) i _Konfigurationsreferens_.

1. Om du vill begränsa antalet underkategorier som visas i den övre navigeringen anger du numret för **[!UICONTROL Maximal Depth]**.

   Standardvärdet är `0`, vilket inte sätter någon gräns för antalet underkategorinivåer.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
