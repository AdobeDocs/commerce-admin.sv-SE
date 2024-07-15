---
title: Produkttyper
description: Läs om hur  [!DNL Inventory Management] har stöd för lager- och orderhantering för alla Adobe Commerce- och Magento Open Source-produkttyper.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# Produkttyper

[!DNL Inventory Management] har stöd för lager- och orderhantering för alla produkttyper i Adobe Commerce och Magento Open Source: enkel, konfigurerbar, virtuell, hämtningsbar, paketerad och grupperad. Alternativen och kraven kan variera mellan olika produkttyper för källor, lager och leveranser.

- [Försäljare med en enda källa](merchant-sourcing.md#single-source-merchants) kan skapa och uppdatera produktinställningar och kvantiteter utan att behöva utföra ytterligare uppdateringar. Alla skapade och nyligen importerade produkter tilldelas automatiskt till standardversionen av Source och standardversionen av Stock, som är omedelbart tillgänglig för kunder om den är aktiverad och i lager.

- [Återförsäljare med flera källor](merchant-sourcing.md#multi-source-merchants) tilldelar källor, kvantiteter per källa och inställningar under eller efter det att produkten skapats. [!DNL Commerce] tilldelar alla nyimporterade produkter till standardprodukten (Source), vilket kräver ytterligare redigeringar för att tilldela källor och kvantiteter.

| Produkttyp | Leveransalgoritm och Source Selection |
|--|--|
| [[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"} | Stöder SSA-rekommendationer och åsidosättningar vid leverans. |
| [[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"} | Stöder SSA-rekommendationer och åsidosättningar vid leverans. |
| [[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"} | Använder alltid SSA-rekommendationen. Algoritmen körs implicit när den skapar fakturor och de föreslagna resultaten används alltid.<br/>Du kan inte justera dessa resultat. |
| [[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"} | Använder alltid SSA-rekommendationen. Algoritmen körs implicit när den skapar fakturor och de föreslagna resultaten används alltid. <br/>Du kan inte justera dessa resultat. |
| [[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"} | Stöder SSA-rekommendationer och åsidosättningar vid leverans. |
| [[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"} | Stöder SSA-rekommendationer och åsidosättningar vid leverans. |
