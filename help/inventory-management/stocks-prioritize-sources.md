---
title: Prioritera lagerkällor för ett lager
description: Lär dig hur du ordnar källor uppifrån och ned i prioritetsordning, vilket används när du fastställer utleverans- och lageravdrag.
exl-id: 16db3ee3-ce99-40dd-b1a3-fcb145b1298f
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Prioritera källor för en aktie

Efter tillägg [källor](sources-manage.md) till [stock](stocks-manage.md), ordna källorna uppifrån och ned i prioritetsordning. Källvalsalgoritmen (SSA) ger en algoritmprioritet som använder den här ordningen när leverans- och lageravdrag bestäms.

Källprioriteten för lager påverkar inte tilldelade källor när produktlager redigeras.

I det här exemplet har UK Stock oordnade källor för en butik och två lagerställen i London och ett lagerställe i Berlin.

![Källorder före prioritering](assets/inventory-priority-before.png){width="350" zoomable="yes"}

Handlaren föredrar att få leveranser prioriterade från större lager i Berlin, sedan London-lagerstället, London-lagerplatsen och slutligen butiken i London. Om du vill ändra ordningen drar och släpper du posterna i önskad ordning.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stocks]**.

1. Öppna aktien i _Redigera_ läge.

1. Expandera _[!UICONTROL Sources]_vid behov.

1. Använd ![Sorteringsikon](assets/icon-sort.png) om du vill dra och släppa källorna i en prioritet från överkanten (första) till nederkanten (sista).

   Ordern är viktig vid leveransorder. SSA rekommenderar leveranser baserat på källordningen

1. Klicka **[!UICONTROL Save & Continue]** för att spara ändringarna.

![Källorder efter prioritering](assets/inventory-stock-priority-after.png){width="350" zoomable="yes"}
