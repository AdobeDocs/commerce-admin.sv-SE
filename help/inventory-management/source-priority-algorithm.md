---
title: Konfigurera Source-prioritetsalgoritmen
description: Lär dig hur du konfigurerar källprioriteten som används för att sortera tilldelade källor i din Stock och gör rekommendationer.
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Konfigurera Source-prioritetsalgoritmen

Anpassade lager innehåller en lista över källor att sälja och leverera tillgängligt produktlager via din butik. Den här algoritmen använder ordningen för tilldelade källor i ditt lager för att göra rekommendationer.

Vid körning, algoritmen:

- Fungerar genom den konfigurerade källordningen på lagernivå med början överst

- Rekommenderar en kvantitet att leverera och källa per produkt baserat på beställningsordningen, tillgänglig kvantitet och beställd kvantitet

- Fortsätter nedåt i listan tills orderleveransen har fyllts i

- Hoppar över inaktiverade källor om de hittas i listan

Ordna källorna uppifrån och ned i prioritetsordning för att utföra beställningarna när du vill konfigurera dem. Source Selection Algorithm (SSA) ger en algoritmprioritet som använder den här ordningen för att fastställa leverans- och lageravdrag. Se [Prioritera källor för en Stock](stocks-prioritize-sources.md).

## Konfigurera källornas prioritet

1. Gå till **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]** på sidofältet _Admin_.

1. Öppna ett lager i redigeringsläge och navigera till området _[!UICONTROL Sources]_.

1. Klicka på **[!UICONTROL Assign Sources]**.

1. I vyn _[!UICONTROL Assign Sources]_&#x200B;markerar du kryssrutan för den önskade källan och klickar sedan på&#x200B;**[!UICONTROL Done]**&#x200B;för att tilldela en källa till lagret.

>[!NOTE]
>
>När algoritmen [Distansprioritet](distance-priority-algorithm.md) används för leverans, och om vägar och data inte returneras för det valda [beräkningsläget](distance-priority-algorithm.md) (kör, cyklar eller går) för en leverans, används som standard Source-prioritet.

![Source-order efter prioritering](assets/inventory-stock-priority-after.png)

| Ikoner | Beskrivning |
|----------------------------------------------|----------------------------------------------------------------|
| ![dra och släpp ikonen för att ange prioritet](assets/icon-drag-and-drop-action.png) | Använd för att dra och släppa källor efter prioritet. |
| ![klicka på ikonen för att ta bort tilldelning av en källa](assets/icon-delete-action.png) | Ta bort tilldelning av en källa till ett lager. |
