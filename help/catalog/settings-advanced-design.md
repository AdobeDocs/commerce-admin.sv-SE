---
title: Produktinställningar - [!UICONTROL Design]
description: För en produkt är [!UICONTROL Design] kan du använda ett annat tema på en produktsida och ändra layouten.
exl-id: 8606ddc7-ca81-4503-94e5-a8276506c0a1
feature: Catalog Management, Products, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Produktinställningar - [!UICONTROL Design]

The _[!UICONTROL Design]_kan du använda ett annat tema på produktsidan, ändra kolumnlayouten, bestämma var produktalternativen ska visas och ange egen XML-kod.

![Design](./assets/product-design-ee.png){width="600" zoomable="yes"}

>[!NOTE]
>
>När samma produkt har tilldelats flera kategorier med olika designinställningar för varje kategori bör du ange **[!UICONTROL Use Categories Path for Product URLs]** = `Yes` i [Konfigurationsalternativ för sökmotoroptimering](../configuration-reference/catalog/catalog.md#search-engine-optimization). Om du vill komma åt den här inställningen går du till  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, expandera **[!UICONTROL Catalog]**och välja **[!UICONTROL Catalog]**under den vänstra panelen och expandera sedan **[!UICONTROL Search Engine Optimization]**på sidan.

| Fält | [Omfång](../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|---|---|----|
| [!UICONTROL Theme] | Butiksvy | ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Du kan använda ett annat tema för produkten. Alternativ: (Alla tillgängliga teman) |
| [!UICONTROL Layout] | Butiksvy | Ger dig möjlighet att använda en annan [layout](../content-design/page-layout.md) till produktsidan. Alternativ: <br/>**[!UICONTROL No layout updates]**- Som standard är layoutuppdateringar inte tillgängliga för produktsidan.<br/>**[!UICONTROL Empty]** - Här kan du definiera en egen layout, t.ex. en sida med fyra kolumner. (Kräver förståelse för XML.) <br/>**[!UICONTROL 1 column]**- Använder en layout med en kolumn på produktsidan.<br/>**[!UICONTROL 2 columns with left bar]** - En layout med två kolumner och vänster sidospalt används på produktsidan. <br/>**[!UICONTROL 2 columns with right bar]**- Använder en layout med två kolumner och höger sidospalt på produktsidan.<br/>**[!UICONTROL 3 columns]** - Använder en layout med tre kolumner på produktsidan. <br/>**[!UICONTROL Page -- Full Width]**- (Kräver [[!DNL Page Builder]](../page-builder/introduction.md)) Använder helbreddslayouten för CMS-sidor på produktsidan.<br/>**[!UICONTROL Category -- Full Width]** - (Kräver [!DNL Page Builder]) Använder helbreddslayouten för kategorisidor på produktsidan. <br/>**[!UICONTROL Product -- Full Width]**- (Kräver [!UICONTROL Page Builder]) Använder helbreddslayouten för produktsidor på produktsidan. |
| [!UICONTROL Display Product Options In] | Butiksvy | Avgör var produktalternativen visas på produktsidan. Alternativ: `Product Info Column` / `Block after Info Column` |
| [!UICONTROL Custom Layout Update] | Butiksvy | Används för att komma åt alternativ för att uppdatera en anpassad layout på produktsidan. |

{style="table-layout:auto"}
