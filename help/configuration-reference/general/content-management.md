---
title: '[!UICONTROL General] &gt; [!UICONTROL Content Management]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL General] &gt; [!UICONTROL Content Management] i Commerce Admin.
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 5929a2ff26dadda40ecfa9e435a73343caef3cde
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Content Management]

{{config}}

## [!UICONTROL WYSIWYG Options]

![WYSIWYG-alternativ](./assets/content-management-wysiwyg-options.png)<!-- zoom -->

<!-- [WYSIWYG Options](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/wysiwyg/editor) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable WYSIWYG Editor] | Butiksvy | Anger om redigeraren är aktiverad för butiken. Alternativ: Aktiverat som standard/inaktiverat som standard/inaktiverat helt |
| [!UICONTROL WYSIWYG Editor] | Webbplats | Anger vilken version av TinyMCE-redigeraren som används för WYSIWYG-redigeraren. Alternativ: <br/>**`TinyMCE 5`**- (Standard) Använder TinyMCE version 5 som WYSIWYG standardredigerare.<br><br>_ **&#x200B; Obs!**&#x200B;_En uppdatering av TinyMCE 5.10-biblioteket i Adobe Commerce och Magento Open Source 2.4.5 åtgärdar en sårbarhet som tillåter godtycklig JavaScript-körning vid uppdatering av en bild eller länk med vissa typer av URL:er. TinyMCE 3 togs bort i version 2.4.0 och togs bort i version 2.4.3. TinyMCE 4 togs bort i version 2.4.4. |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | Global | Avgör om [statiska URL:er](../../content-design/catalog-urls-dynamic-media.md) används för mediainnehåll som refereras från WYSIWYG-redigeraren. Inställningen gäller alla platser där WYSIWYG-redigeraren är tillgänglig, inklusive produkter, kategorier, sidor och block. Alternativ: <br/>**`Yes`**- Använder statiska URL:er för mediainnehåll som infogas med WYSIWYG Editor. Statiska URL:er är absoluta och bryts om butikens [bas-URL](../../stores-purchase/store-urls.md) ändras.<br/>**`No`** (Standard) - Använder dynamiska URL:er för mediainnehåll som infogas med WYSIWYG-redigeraren, baserat på direktivet `{{media url="..."}}`. Dynamiska URL:er är relativa och bryts inte om bas-URL:en för butiken ändras. |

{style="table-layout:auto"}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

![CMS-sidhierarki](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/pages/page-hierarchy) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | Global | Aktiverar användning av sidhierarki för innehållssidor. Alternativ: `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | Global | Ger dig möjlighet att associera metadata med sidor i hierarkin. Alternativ: `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | Global | Anger standardmenyformatet. Alternativ: `Content` / `Left Column` / `Right Column` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Content Tools]

![Avancerade innehållsverktyg](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://experienceleague.adobe.com/en/docs/commerce-admin/page-builder/walkthrough/3-catalog-content) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | Global | Avgör om de [!DNL Page Builder] avancerade innehållsverktygen är tillgängliga. Alternativ: <br/>**`Yes`**- Arbetsytan [!DNL Page Builder] visas i innehållsavsnittet för sidor, block, produkter och kategorier.<br/>**`No`** - CMS standardverktyg för redigering visas i avsnittet _[!UICONTROL Content]_&#x200B;av sidor, block, produkter och kategorier. |
| [!UICONTROL Enable Page Builder Content Preview] | Global | Avgör om [!DNL Page Builder]-innehållsförhandsvisningar är aktiverade för produkter och kategorier. Alternativ: `Yes` / `No` <br/>**_Obs!:_** Det här är inställt på `Yes` som standard, men om du stänger av förhandsgranskningen kan du förhindra prestandaproblem som uppstår när förhandsgranskningar läses in i ett produkt- eller kategoriformulär. |
| [!UICONTROL Google Maps API Key] | Global | API-nyckeln [!DNL Google Maps] från ditt Google-konto. |
| [!UICONTROL Test Key] |  | Verifierar API-nyckeln för [!DNL Google Maps]. |
| [!UICONTROL Google Maps Style] | Global | Klistra in JSON-koden för formatet [!DNL Google Maps] här om du vill ändra utseendet och känslan för innehållstypen för kartan. |
| [!UICONTROL Default Column Grid Size] | Global | Anger standardantalet kolumner i rutnätet [!DNL Page Builder]. |
| [!UICONTROL Maximum Column Grid Size] | Global | Anger det maximala antalet kolumner i rutnätet [!DNL Page Builder]. |

{style="table-layout:auto"}

>[!TIP]
>
>Med Page Builder är det enkelt att skapa innehållsrika sidor med anpassade layouter som förbättrar ert visuella berättande och som ökar kundernas engagemang och lojalitet. Funktionerna är utformade för att förbättra kvaliteten och minska tiden och kostnaden för att skapa anpassade sidor. Mer information om de här funktionerna och hur du kan använda dem för att skapa engagerande innehåll för din Adobe Commerce- eller Magento Open Source-butik finns i [_användarhandboken för Page Builder_](../../page-builder/guide-overview.md).
