---
title: Kategorier - Designinställningar
description: Lär dig hur du använder inställningarna för [!UICONTROL Design] för att definiera utseendet och känslan för en kategori, alla tillhörande produktsidor och sidlayout.
exl-id: 6dc216ac-1c52-4196-9c93-e5cad19901b5
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Kategorier - Designinställningar

Avsnittet _[!UICONTROL Design]_ger dig kontroll över utseendet och känslan för en kategori, alla tillhörande produktsidor och sidlayout. Du kan anpassa en kategorisida och tillhörande produkter för en kampanj, eller för att skilja kategorin åt. Du kan till exempel utveckla en distinkt design för ett varumärke eller en specialproduktlinje, eller tillämpa en uppdatering för en viss tidsperiod.

![Designinställningar för en kategori](./assets/category-design.png){width="600" zoomable="yes"}

>[!NOTE]
>
>När samma produkt tilldelas till flera kategorier med olika designinställningar för varje kategori bör du ange **Använd kategorisökväg för produkt-URL:er** = `Yes` i [konfigurationsalternativen för sökmotoroptimering](../configuration-reference/catalog/catalog.md#search-engine-optimization). Om du vill komma åt den här inställningen går du till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, expanderar **[!UICONTROL Catalog]**och väljer **Katalog**under den vänstra panelen och expanderar sedan avsnittet **Sökmotoroptimering**på sidan.

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Use Parent Category Settings] | Tillåter den aktuella kategorin att ärva designinställningarna från den överordnade kategorin. Om det används blir alla andra fält i designavsnittet otillgängliga. Alternativ: `Yes` / ` No` |
| [!UICONTROL Theme] | Använder ett anpassat tema i kategorin. |
| [!UICONTROL Layout] | Använder en annan layout på kategorisidan. Alternativ: <br/>**[!UICONTROL No layout updates]**- Som standard är layoutuppdateringar inte tillgängliga för kategorisidor.<br/>**[!UICONTROL Empty]** - Använd för att definiera din egen sidlayout. (Kräver förståelse för XML.) <br/>**[!UICONTROL 1 column]**- Använder en layout med en kolumn på kategorisidan.<br/>**[!UICONTROL 2 columns with left bar]** - Använder en layout med två kolumner och vänster sidospalt på kategorisidan. <br/>**[!UICONTROL 2 columns with right bar]**- Använder en layout med två kolumner och höger sidospalt på kategorisidan.<br/>**[!UICONTROL 3 columns]** - Använder en layout med tre kolumner på kategorisidan.<br/>**[!UICONTROL Page -- Full Width]**- (Kräver [Page Builder](../page-builder/introduction.md)) Använder helbreddslayouten för CMS-sidor på kategorisidan.<br/>**[!UICONTROL Category -- Full Width]** - (Kräver Page Builder) Använder helbreddslayouten för kategorisidor på kategorisidan. <br/>**[!UICONTROL Product -- Full Width]**- (Kräver Page Builder) Tillämpar helbreddslayouten för produktsidor på kategorisidan. |
| [!UICONTROL Custom Layout Update] | Visar tillgängliga anpassade layoutuppdateringsfiler på servern. Välj den anpassade layoutuppdatering som du vill använda för kategorin. |
| [!UICONTROL Apply Design to Products] | När du väljer det här alternativet används anpassade inställningar för alla produkter i kategorin. |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Design Update]

{{ce-feature}}

Avsnittet _[!UICONTROL Scheduled Design Update]_avgör datumintervallet när en anpassad design används på kategorisidor.

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | Anger datumintervallet när en anpassad layout används för kategorin. |

![Schemalagd designuppdatering](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}
