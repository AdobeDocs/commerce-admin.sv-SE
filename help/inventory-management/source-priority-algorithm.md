---
title: Konfigurera algoritmen för källprioritet
description: Lär dig hur du konfigurerar källprioriteten som används för att sortera tilldelade källor i din Stock och gör rekommendationer.
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Konfigurera algoritmen för källprioritet

Anpassade lager innehåller en lista över källor att sälja och leverera tillgängligt produktlager via din butik. Den här algoritmen använder ordningen för tilldelade källor i ditt lager för att göra rekommendationer.

Vid körning, algoritmen:

- Fungerar genom den konfigurerade källordningen på lagernivå med början överst

- Rekommenderar en kvantitet att leverera och källa per produkt baserat på beställningsordningen, tillgänglig kvantitet och beställd kvantitet

- Fortsätter nedåt i listan tills orderleveransen har fyllts i

- Hoppar över inaktiverade källor om de hittas i listan

Ordna källorna uppifrån och ned i prioritetsordning för att utföra beställningarna när du vill konfigurera dem. Källvalsalgoritmen (SSA) ger en algoritmprioritet som använder den här ordningen när leverans- och lageravdrag bestäms. Se [Prioritera källor för en Stock](stocks-prioritize-sources.md).

## Konfigurera källornas prioritet

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**.

1. Öppna en resurs i redigeringsläge och navigera till _[!UICONTROL Sources]_område.

1. Klicka på **[!UICONTROL Assign Sources]**.

1. I _[!UICONTROL Assign Sources]_markera kryssrutan för den önskade källan och klicka sedan på&#x200B;**[!UICONTROL Done]**om du vill tilldela en källa till lagret.

>[!NOTE]
>
>När du använder [Avståndsprioritet](distance-priority-algorithm.md) Leveransalgoritm, om vägar och data inte returneras för den valda [Beräkningsläge](distance-priority-algorithm.md) (vid körning, cykling eller gång) för en leverans används som standard källprioritet för SSA.

![Källorder efter prioritering](assets/inventory-stock-priority-after.png)

| Ikoner | Beskrivning |
|----------------------------------------------|----------------------------------------------------------------|
| ![dra och släpp ikonen för att ange prioritet](assets/icon-drag-and-drop-action.png) | Använd för att dra och släppa källor efter prioritet. |
| ![klicka på ikonen för att ta bort tilldelning av en källa](assets/icon-delete-action.png) | Ta bort tilldelning av en källa till ett lager. |
