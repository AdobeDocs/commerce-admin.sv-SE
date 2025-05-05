---
title: Produktinställningar - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]
description: För en produkt definierar inställningarna för [!UICONTROL Related Products, Up-Sells, and Cross-Sells] enkla marknadsföringsblock på produktsidan som markerar ett urval av ytterligare produkter.
exl-id: 5bd65fad-4e55-40db-8702-10c366261565
feature: Catalog Management, Products, Page Content
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 0%

---

# Produktinställningar - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]

Använd avsnittet _[!UICONTROL Related Products, Up-Sells, and Cross-Sells]_&#x200B;för att skapa enkla marknadsföringsblock som visar ett urval av ytterligare produkter som kan vara av intresse för kunden. Mer information finns i [Produktrelationer](../merchandising-promotions/product-relationships.md).

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
>![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) **Produktrekommendationer från Adobe Sensei** förenklar processen att definiera produktrelationer genom att använda artificiell intelligens och maskininlärningsalgoritmer för att göra en djupanalys av samlade besöksdata. Dessa data kombineras med er Adobe Commerce-katalog och ger en engagerande, relevant och personaliserad upplevelse för kunderna.
><br/>
>Mer information om hur du använder det här Adobe-utvecklade tillägget som ett alternativ till manuellt konfigurerade produktrekommendationer och merförsäljning finns i _[produktrekommendationsguiden](https://experienceleague.adobe.com/docs/commerce/product-recommendations/guide-overview.html?lang=sv-SE)_.

## Samhörande produkter

Relaterade produkter ska köpas utöver den artikel som kunden visar. Kunden kan placera artikeln i kundvagnen genom att klicka i kryssrutan. Placeringen av blocket _Relaterade produkter_ varierar beroende på definierat tema och sidlayout. I exemplet nedan visas blocket _Relaterade produkter_ längst ned på sidan _Produktvy_. Med en layout med två kolumner visas ofta blocket _Relaterade produkter_ i det högra sidofältet.

![Relaterade produkter](./assets/storefront-product-related-products.png){width="600" zoomable="yes"}

Så här ställer du in relaterade produkter:

1. Öppna produkten i redigeringsläge.

1. Bläddra nedåt och utöka ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]**.

1. Klicka på **[!UICONTROL Add Related Products]**.

1. Använd [filterkontrollerna](../getting-started/admin-grid-controls.md) för att hitta de produkter du vill ha.

1. I listan markerar du kryssrutan för alla produkter som du vill använda som en relaterad produkt.

   ![Relaterade produkter](./assets/products-related-add.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Add Selected Products]** när du är klar.

## Merförsäljning

Merförsäljningsprodukter är artiklar som kunden kanske föredrar istället för den produkt som är aktuell. En artikel som erbjuds som merförsäljning kan vara av högre kvalitet, mer populär eller ha bättre vinstmarginal. Merförsäljningsprodukter visas på produktsidan under en rubrik som _Du kan också vara intresserad av följande produkter_.

![Merförsäljning](./assets/storefront-product-upsell.png){width="600" zoomable="yes"}

Så här väljer du merförsäljningsprodukter:

1. Öppna produkten i redigeringsläge.

1. Bläddra nedåt och utöka ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]**.

1. Klicka på **[!UICONTROL Add Up-Sell Products]**.

1. Använd [filterkontrollerna](../getting-started/admin-grid-controls.md) för att hitta de produkter du vill ha.

1. I listan markerar du kryssrutan för den produkt du vill använda som merförsäljningsprodukt.

   ![Merförsäljning](./assets/product-up-sell-add.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Add Selected Products]** när du är klar.

>[!NOTE]
>
>Överordnad paketprodukt visas alltid automatiskt som en merförsäljningsprodukt för alla dess underordnade produkter.

## Korsförsäljning

Korsförsäljningsartiklar liknar impulsköp som placerats bredvid kassaregistret i kassan. Produkter som erbjuds som korsförsäljning visas på kundvagnssidan, precis innan kunden påbörjar utcheckningsprocessen.

>[!NOTE]
>
>Om du vill visa eller dölja korsförsäljningsobjekt per butiksvy läser du alternativet [Kassa > Kundvagn](../configuration-reference/sales/checkout.md) med namnet _[!UICONTROL Show Cross-sell Items]_&#x200B;i kundvagnen. Du kanske vill dölja korsförsäljning under en viss försäljning eller för A/B-testning i en butiksvy.

![Korsförsäljning i kundvagn](./assets/storefront-cart-cross-sells.png){width="600" zoomable="yes"}

**_Så här väljer du korsförsäljningsprodukter:_**

1. Öppna produkten i redigeringsläge.

1. Bläddra nedåt och utöka ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]**.

1. Klicka på **[!UICONTROL Add Cross-Sell Products]**.

1. Använd [filterkontrollerna](../getting-started/admin-grid-controls.md) för att hitta de produkter du vill ha.

1. I listan markerar du kryssrutan för den produkt du vill använda som korsförsäljningsprodukt.

   ![Cross-sell Products](./assets/product-cross-sell-add.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Add Selected Products]** när du är klar.
