---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Quotes]'
description: Granska konfigurationsinställningarna på [!UICONTROL Sales] &gt; [!UICONTROL Quotes] sidan för Commerce Admin.
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>Med installation och aktivering av Adobe Commerce B2B kan köpupplevelsen personaliseras med företagsspecifika funktioner. Adobe Commerce B2B är en integrerad lösning som stöder både B2B- och B2C-modeller. Mer information om B2B-funktionerna finns i [Användarhandbok för Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

{{config}}

<!-- [Quotes](https://docs.magento.com/user-guide/sales/quotes.html) -->

## [!UICONTROL General]

![Allmänt](./assets/quotes-general.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Minimum Amount] | Webbplats | Den minsta delsumman för kundvagnen, efter eventuella rabatter, som krävs innan en kund kan skicka in en anbudsförfrågan. Standardvärde: `0` |
| [!UICONTROL Minimum Amount Message] | Butiksvy | Meddelandet som visas i kundvagnen när en kund försöker skicka en anbudsförfrågan, men minimibeloppet som krävs uppfylls inte. |
| [!UICONTROL Default Expiration Period] | Webbplats | Bestämmer standardlivslängden för en [citat](../../b2b/quote-price-negotiation.md) som tidsperiod från det datum då anbudsförfrågan ingavs. Alternativ: `Days` / `Weeks` / `Months` |

{style="table-layout:auto"}

## [!UICONTROL Attached Files]

![Bifogade filer](./assets/quotes-attached-files.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL File formats for upload] | Global | Bestämmer vilka filformat som kan bifogas till en offert. Standardvärden som stöds: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png`och `jpeg` |
| [!UICONTROL Maximum file size] | Global | Anger den maximala storleken för en fil som är kopplad till en offert. Den här inställningen kan åsidosättas av serverkonfigurationen. |

{style="table-layout:auto"}
