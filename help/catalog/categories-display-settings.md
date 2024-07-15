---
title: Kategorier - Visningsinställningar
description: Lär dig hur du använder inställningarna för [!UICONTROL Display] för att definiera vilka innehållselement som ska visas på en kategorisida och i vilken ordning produkterna ska visas.
exl-id: bb3a1b00-ba56-4113-8208-860963612333
feature: Catalog Management, Categories, Page Content
source-git-commit: a47e744cf4cc5163ca2ba0718ccb78eb65a7d404
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# Kategorier - Visningsinställningar

Visningsinställningarna avgör vilka innehållselement som visas på en kategorisida och i vilken ordning produkterna visas. Du kan aktivera CMS-block, ange kategoriens ankarstatus och hantera sorteringsalternativ på fliken _[!UICONTROL Display Settings]_. Exempel på hur kategorier visas i butiken finns i [Katalognavigering](navigation.md).

![Visningsinställningar för kategorier](./assets/category-display-settings.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Display Mode] | Bestämmer vilka innehållselement som visas på kategorisidan. Alternativ: `Products Only` / `Static Block Only` / `Static Block and Products` |
| [!UICONTROL Anchor] | När värdet är `Yes` visas produkter från underkategorierna i kategorin, även om de inte uttryckligen har lagts till i kategorin, och _[!UICONTROL filter by attribute]_-avsnittet visas i lagernavigeringen. Alternativ: `Yes` / `No` |
| [!UICONTROL Available Product Listing Sort By] | (Obligatoriskt) Standardvärdena är `Position`, `Name` och `Price`. Om du vill anpassa sorteringsalternativet avmarkerar du kryssrutan **[!UICONTROL Use All Available Attributes]** och markerar de attribut du vill använda. Du kan definiera och lägga till attribut efter behov. Den här inställningen gäller inte för [!DNL Live Search] [Sidwidgeten Produktlista](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Default Product Listing Sort By] | (Obligatoriskt) Om du vill definiera standardalternativet _[!UICONTROL Sort By]_avmarkerar du kryssrutan **[!UICONTROL Use Config Settings]**och markerar ett attribut. Den här inställningen gäller inte för [!DNL Live Search] [Sidwidgeten Produktlista](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Layered Navigation Price Step] | Som standard visar Commerce prisintervallet i steg om 10, 100 och 1000, beroende på vilka produkter som finns i listan. Om du vill ändra intervallet för prissteg avmarkerar du kryssrutan **[!UICONTROL Use Config Settings]**. |

{style="table-layout:auto"}
