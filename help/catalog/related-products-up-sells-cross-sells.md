---
title: Produktinställningar - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]
description: För en produkt är [!UICONTROL Related Products, Up-Sells, and Cross-Sells] -inställningarna definierar enkla marknadsföringsblock på produktsidan som markerar ett urval av ytterligare produkter.
exl-id: 5bd65fad-4e55-40db-8702-10c366261565
feature: Catalog Management, Products, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# Produktinställningar - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]

Använd _[!UICONTROL Related Products, Up-Sells, and Cross-Sells]_för att skapa enkla reklamblock som innehåller ett urval av ytterligare produkter som kan vara av intresse för kunden. Mer information finns i [Produktrelationer](../merchandising-promotions/product-relationships.md).

![Samhörande produkter, merförsäljning och korsförsäljning](./assets/product-related-up-sell-cross-sell.png){width="600" zoomable="yes"}

Varje block består av en lista över produkter som tillhör ett visst alternativ.

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL ID] | En unik numerisk identifierare som tilldelas till produktentiteten. |
| [!UICONTROL Thumbnail] | Produktminiatyrbild. |
| [!UICONTROL Name] | Produktens namn. |
| [!UICONTROL Status] | Anger produktstatus. Alternativ: `Enabled` / `Disabled`. Inaktiverade produkter visas inte i blocken på frontend. |
| [!UICONTROL Attribute Set] | Namnet på den attributuppsättning som används som mall för produkten. |
| [!UICONTROL SKU] | Den unika lagringsenhet som är tilldelad produkten. |
| [!UICONTROL Price] | Enhetspriset för produkten. |
| [!UICONTROL Action] | Alternativ: `Remove`. Tar bort en produkt från blocket. |

{style="table-layout:auto"}

>[!TIP]
>
>![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) **Product Recommendations powered by Adobe Sensei** förenklar processen att definiera produktrelationer genom att använda artificiell intelligens och maskininlärningsalgoritmer för att göra en djupgående analys av samlade besökardata. Dessa data kombineras med er Adobe Commerce-katalog och ger en engagerande, relevant och personaliserad upplevelse för kunderna.
><br/>
>Mer information om hur du använder det här tillägget som utvecklats av Adobe som ett alternativ till manuellt konfigurerade produktrekommendationer och merförsäljning finns i _[Product Recommendations Guide](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html)_.

## Samhörande produkter

Relaterade produkter ska köpas utöver den artikel som kunden visar. Kunden kan placera artikeln i kundvagnen genom att klicka i kryssrutan. Placeringen av _Samhörande produkter_ -block varierar beroende på definierat tema och sidlayout. I exemplet nedan är _Samhörande produkter_ -blocket visas längst ned i _Produktvy_ sida. Med en layout med två kolumner _Samhörande produkter_ visas ofta i den högra sidlisten.

![Samhörande produkter](./assets/storefront-product-related-products.png){width="600" zoomable="yes"}

Så här ställer du in relaterade produkter:

1. Öppna produkten i redigeringsläge.

1. Rulla ned och expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** -avsnitt.

1. Klicka på **[!UICONTROL Add Related Products]**.

1. Använd [filterkontroller](../getting-started/admin-grid-controls.md) för att hitta de produkter du vill ha.

1. I listan markerar du kryssrutan för alla produkter som du vill använda som en relaterad produkt.

   ![Samhörande produkter](./assets/products-related-add.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Add Selected Products]**.

## Merförsäljning

Merförsäljningsprodukter är artiklar som kunden kanske föredrar istället för den produkt som är aktuell. En artikel som erbjuds som merförsäljning kan vara av högre kvalitet, mer populär eller ha bättre vinstmarginal. Merförsäljning visas på produktsidan under en rubrik som _Du kan också vara intresserad av följande produkter_.

![Merförsäljning](./assets/storefront-product-upsell.png){width="600" zoomable="yes"}

Så här väljer du merförsäljningsprodukter:

1. Öppna produkten i redigeringsläge.

1. Rulla ned och expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** -avsnitt.

1. Klicka på **[!UICONTROL Add Up-Sell Products]**.

1. Använd [filterkontroller](../getting-started/admin-grid-controls.md) för att hitta de produkter du vill ha.

1. I listan markerar du kryssrutan för den produkt du vill använda som merförsäljningsprodukt.

   ![Merförsäljning](./assets/product-up-sell-add.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Add Selected Products]**.

## Korsförsäljning

Korsförsäljningsartiklar liknar impulsköp som placerats bredvid kassaregistret i kassan. Produkter som erbjuds som korsförsäljning visas på kundvagnssidan, precis innan kunden påbörjar utcheckningsprocessen.

>[!NOTE]
>
>Om du vill visa eller dölja korsförsäljningsartiklar per butiksvy läser du [Kassa > Kundvagn](../configuration-reference/sales/checkout.md) option called _[!UICONTROL Show Cross-sell Items]_i kundvagnen. Du kanske vill dölja korsförsäljning under en viss försäljning eller för A/B-testning i en butiksvy.

![Korsförsäljning i kundvagn](./assets/storefront-cart-cross-sells.png){width="600" zoomable="yes"}

**_Så här väljer du korsförsäljningsprodukter:_**

1. Öppna produkten i redigeringsläge.

1. Rulla ned och expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** -avsnitt.

1. Klicka på **[!UICONTROL Add Cross-Sell Products]**.

1. Använd [filterkontroller](../getting-started/admin-grid-controls.md) för att hitta de produkter du vill ha.

1. I listan markerar du kryssrutan för den produkt du vill använda som korsförsäljningsprodukt.

   ![Korsförsäljning](./assets/product-cross-sell-add.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Add Selected Products]**.
