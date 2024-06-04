---
title: Skapa en produkt
description: Lär dig mer om de typer av produkter som du kan skapa för din katalog.
exl-id: ff90bf8a-a64d-403f-bd09-5c8167a36f0b
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# Skapa en produkt

Att välja en produkttyp är en av de första sakerna du måste göra för att skapa en produkt. Om du just har börjat skapa en produktkatalog kan du skapa några exempelprodukter och experimentera med varje produkttyp. Förutom de grundläggande produkttyperna gäller termen _komplex produkt_ används ibland för att hänvisa till produkter med flera alternativ, t.ex. en konfigurerbar produkt som är tillgänglig i olika färger och storlekar.

>[!NOTE]
>
>Mer information finns i katalogen [navigering](navigation.md), konfigurera [kategorier](categories.md) och [attributes](product-attributes.md)och katalogen [URL-alternativ](catalog-urls.md) som finns tillgängliga. När du har förstått dessa koncept är det mest effektiva sättet att lägga till många produkter i katalogen att [import](../systems/data-import.md) de från en CSV-fil.

![Produktsida i butiken](./assets/storefront-product-page.png){width="700" zoomable="yes"}

## Produkttyper

**[Enkel produkt](product-create-simple.md)** - En enkel produkt är en fysisk artikel med en enda SKU. Enkla produkter har olika prissättning och olika indatakontroller, vilket gör det möjligt att sälja varianter av produkten. Enkla produkter kan användas tillsammans med grupperade, paketerade och konfigurerbara produkter.

**[Konfigurerbar produkt](product-create-configurable.md)** - En konfigurerbar produkt ser ut att vara en enda produkt med listor över alternativ för varje ändring. Varje alternativ representerar dock en separat, enkel produkt med en distinkt SKU, som gör det möjligt att spåra lager för varje variation.

**[Grupperad produkt](product-create-grouped.md)** - En grupperad produkt består av flera fristående produkter i grupp. Du kan erbjuda varianter av en enstaka produkt eller gruppera dem för en kampanj. Produkterna kan köpas separat eller i grupp.

**[Virtuella produkter](product-create-virtual.md)** - En virtuell produkt är inte en påtaglig produkt och används vanligtvis för produkter som tjänster, medlemskap, garantier och prenumerationer. Virtuella produkter kan användas tillsammans med grupperade produkter och paketprodukter.

**[Paketprodukt](product-create-bundle.md)**  - Med en paketprodukt kan kunderna&quot;bygga sina egna&quot; utifrån en mängd olika alternativ. Paketet kan vara en presentkorg, en dator eller något annat som kan anpassas. Varje artikel i paketet är en separat, fristående produkt.

**[Nedladdningsbar produkt](product-create-downloadable.md)** - En digitalt nedladdningsbar produkt består av en eller flera filer som har laddats ned. Filerna kan finnas på servern eller tillhandahållas som URL-adresser till andra servrar.

**[Presentkort](product-gift-card-create.md)** - ([Adobe Commerce](../landing/home.md#product-editions) (endast) Det finns tre typer av presentkort. _Virtuell_ presentkort skickas med e-post. _Fysisk_ presentkort skickas till mottagaren. _Kombinerad_ presentkort som är en kombination av virtuella och fysiska. Varje kod har en unik kod som löses in vid utcheckning. Presentkort kan också ingå i en grupperad produkt.

## Produktinställningar

De vanligaste produktinställningarna och attributen visas överst på sidan, följt av anpassade attribut. Alla andra produktinställningar finns i expanderbara avsnitt längst ned på sidan.

![Produktinställningar](./assets/product-settings.png){width="600" zoomable="yes"}

| Inställning | Beskrivning |
|--- |--- |
| [[!UICONTROL Sources]](../inventory-management/sources-assign-per-product.md) | (När [[!DNL Inventory Management]](../inventory-management/introduction.md) är aktiverat) Visar de källor som produkten kan distribueras från. |
| [[!UICONTROL Content]](product-content.md) | Används för att ange och redigera produktbeskrivningen som visas på butikens produktsida. |
| [[!UICONTROL Configurations]](product-configurations.md) | Visar en lista över eventuella befintliga variationer av produkten och kan användas för att generera variationer som kan användas med den konfigurerbara produkttypen. |
| [[!UICONTROL Product Reviews]](settings-advanced-product-reviews.md) | Visar alla recensioner som kunder har skickat in för produkten. |
| [[!UICONTROL Search Engine Optimization]](product-search-engine-optimization.md) | Anger de URL-nyckelfält och metadatafält som används av sökmotorer för att indexera produkten. |
| [[!UICONTROL Related Products, Up-Sells, and Cross-Sells]](related-products-up-sells-cross-sells.md) | Används för att skapa enkla marknadsföringsblock i butiken som presenterar ett urval av ytterligare produkter som kan vara av intresse för kunden. |
| [[!UICONTROL Customizable Options]](settings-advanced-custom-options.md) | Lägger till anpassningsbara alternativ till en produkt. |
| [[!UICONTROL Product in Websites]](settings-basic-websites.md) | Identifierar varje webbplats där produkten är tillgänglig, enligt butikshierarkin. |
| [[!UICONTROL Design]](settings-advanced-design.md) | Används för att tillämpa ett annat tema på produktsidan, ändra kolumnlayouten, bestämma var produktalternativen ska visas och ange anpassad XML-kod. |
| [[!UICONTROL Gift options]](product-gift-options.md) | Används för att aktivera eller inaktivera ett presentalternativ vid utcheckning på produktnivå. |
| [[!UICONTROL Product In Shared Catalogs]](../b2b/catalog-shared.md) | ![Adobe Commerce B2B](../assets/b2b.svg) (Tillgängligt med [Adobe Commerce B2B](../b2b/introduction.md) endast) Möjliggör underhåll av delade kataloger med anpassade priser för olika företag. |
| [[!UICONTROL Downloadable Information]](product-create-downloadable.md#step-5-complete-the-downloadable-information) | Används för att definiera parametrar för produkthämtning. |

{style="table-layout:auto"}

## Avancerade priser och lager

Klicka på länken nedan för att få tillgång till de avancerade prissättnings- och lagerinställningarna **[!UICONTROL Price]** och **[!UICONTROL Quantity]**. Mer information finns i [Hantera priser](pricing-advanced.md) och [Inventory management](../inventory-management/introduction.md).
