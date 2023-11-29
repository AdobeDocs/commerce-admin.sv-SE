---
title: '[!UICONTROL General] &gt; [!UICONTROL Content Management]'
description: Granska konfigurationsinställningarna på [!UICONTROL General] &gt; [!UICONTROL Content Management] sidan för Commerce Admin.
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
source-git-commit: 5eef49c10680a47574afe3d3ecfa430dca7ad9ff
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Content Management]

{{config}}

## [!UICONTROL WYSIWYG Options]

![WYSIWYG-alternativ](./assets/content-management-wysiwyg-options.png)<!-- zoom -->

<!-- [WYSIWYG Options](https://docs.magento.com/user-guide/cms/editor.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable WYSIWYG Editor] | Butiksvy | Anger om redigeraren är aktiverad för butiken. Alternativ: Aktiverat som standard/inaktiverat som standard/inaktiverat helt |
| [!UICONTROL WYSIWYG Editor] | Webbplats | Anger vilken version av TinyMCE-redigeraren som används för WYSIWYG-redigeraren. Alternativ: <br/>**`TinyMCE 5`**- (Standard) Använder TinyMCE version 5 som WYSIWYG-standardredigerare.<br><br>_** Obs!**_En uppdatering av TinyMCE 5.10-biblioteket i Adobe Commerce och Magento Open Source 2.4.5 åtgärdar en sårbarhet som tillåter godtycklig JavaScript-körning vid uppdatering av en bild eller länk med vissa typer av URL:er. TinyMCE 3 togs bort i version 2.4.0 och togs bort i version 2.4.3. TinyMCE 4 togs bort i version 2.4.4. |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | Global | Bestämmer om [statiska URL:er](../../content-design/catalog-urls-dynamic-media.md) används för mediainnehåll som refereras från WYSIWYG-redigeraren. Inställningen gäller alla platser där WYSIWYG-redigeraren är tillgänglig, inklusive produkter, kategorier, sidor och block. Alternativ: <br/>**`Yes`**- Använder statiska URL:er för mediainnehåll som infogas med WYSIWYG-redigeraren. Statiska URL:er är absoluta och bryts om [bas-URL](../../stores-purchase/store-urls.md) av butiksändringarna.<br/>**`No`** (Standard) - Använder dynamiska URL:er för mediainnehåll som infogas med WYSIWYG-redigeraren, baserat på  `{{media url="..."}}` -direktivet. Dynamiska URL:er är relativa och bryts inte om bas-URL:en för butiken ändras. |

{style="table-layout:auto"}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

![CMS-sidhierarki](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://docs.magento.com/user-guide/cms/page-hierarchy.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | Global | Aktiverar användning av sidhierarki för innehållssidor. Alternativ: `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | Global | Ger dig möjlighet att associera metadata med sidor i hierarkin. Alternativ: `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | Global | Anger standardmenyformatet. Alternativ: `Content` / `Left Column` / `Right Column` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Content Tools]

![Avancerade innehållsverktyg](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://docs.magento.com/user-guide/cms/page-builder-workspace.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | Global | Anger om [!DNL Page Builder] avancerade verktyg finns tillgängliga. Alternativ: <br/>**`Yes`**- [!DNL Page Builder] -arbetsytan visas i innehållsavsnittet för sidor, block, produkter och kategorier.<br/>**`No`** - Standardverktygen för CMS-redigering visas i _[!UICONTROL Content]_av sidor, block, produkter och kategorier. |
| [!UICONTROL Enable Page Builder Content Preview] | Global | Anger om [!DNL Page Builder] förhandsgranskning av innehåll är aktiverat för produkter och kategorier. Alternativ: `Yes` / `No` <br/>**_Obs!_**Detta är inställt på `Yes` som standard, men om du stänger av förhandsgranskningen kan du förhindra prestandaproblem som uppstår när du läser in förhandsgranskningar i ett produkt- eller kategoriformulär. |
| [!UICONTROL Google Maps API Key] | Global | The [!DNL Google Maps] API-nyckel från ditt Google-konto. |
| [!UICONTROL Test Key] |  | Validerar [!DNL Google Maps] API-nyckel. |
| [!UICONTROL Google Maps Style] | Global | Klistra in [!DNL Google Maps] formatera JSON-kod här om du vill ändra utseendet och känslan för Map-innehållstypen. |
| [!UICONTROL Default Column Grid Size] | Global | Anger standardantalet kolumner i [!DNL Page Builder] rutnät. |
| [!UICONTROL Maximum Column Grid Size] | Global | Anger det maximala antalet kolumner i [!DNL Page Builder] rutnät. |

{style="table-layout:auto"}

>[!TIP]
>
>Med Page Builder är det enkelt att skapa innehållsrika sidor med anpassade layouter som förbättrar ert visuella berättande och som ökar kundernas engagemang och lojalitet. Funktionerna är utformade för att förbättra kvaliteten och minska tiden och kostnaden för att skapa anpassade sidor. Mer information om de här funktionerna och hur du kan använda dem för att skapa engagerande innehåll för din Adobe Commerce eller Magento Open Source Store finns i [_Användarhandbok för Page Builder_](../../page-builder/guide-overview.md).
