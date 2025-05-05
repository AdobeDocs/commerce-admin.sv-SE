---
title: Skapa leveranser med flera källor
description: Lär dig hur flerkällvaruförsäljare kan skapa och skicka leveranser.
exl-id: d2995139-0fc3-4379-a4ec-b0d38ed566bb
feature: Inventory, Shipping/Delivery
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Skapa leveranser med flera källor

Med [!DNL Inventory Management] skickar du en eller flera leveranser samtidigt som du har lager. Om du vill generera ytterligare leveranser efter behov upprepar du dessa instruktioner med rekommenderade eller manuellt angivna kvantiteter och källor. Instruktionerna beskriver hur flerkällvaruförsäljare skickar leveranser. Handlare med en enda källa skickar leveranser utan dessa ytterligare steg (se [Skapa en leverans](../stores-purchase/shipments.md#create-a-shipment){target="_blank"} i huvudanvändarhandboken).

När du skapar leveranser använder du algoritmen Source Selection för beräknade rekommendationer. Följ och använd dessa rekommendationer eller ange beloppen per källa och generera anpassade leveranser. Du kontrollerar ditt utgående lager för varje order och anger vilka belopp som ska dras av, skickar en eller flera leveranser och levererar i lager och restorder när lagret är tillgängligt. Ange ett belopp som ska dras av från källkvantiteten för varje radartikel i ordern.

Du kanske vill skicka delförsändelser till:

- Fyll i restorder när lagret anländer

- Balansera lageravdrag mellan källor

När du anger leveranser dras de inmatade beloppen av lagerbehållningen av. Reservationer konverteras alltså till faktiska kvantitetsavdrag.

## Skapa en leverans

1. Gå till **[!UICONTROL Sales]** > **[!UICONTROL Orders]** på sidofältet _Admin_.

1. Leta reda på ordningen och öppna i visningsläge.

1. Om ordern har betalats och fakturerats och är klar att skickas klickar du på **[!UICONTROL Ship]**.

1. Slutför Source Selection för att skicka produkter per källa:

   - Om du vill visa leveransrekommendationer klickar du på **[!UICONTROL Source Selection Algorithm]** och väljer en algoritm.

     | Algoritm | Beskrivning |
     |--|--|
     | [Source-prioritet](source-priority-algorithm.md) | Rekommenderar leveranser från källor enligt beställningarna för källor som tilldelats till lagret. |
     | [Avståndsprioritet](distance-priority-algorithm.md) | Rekommenderar försändelser från källor närmast leveransadressen baserat på fysiskt avstånd eller kortast leveranstid. |

     >[!IMPORTANT]
     >
     >När du använder algoritmen Distance Priority för leverans och vägar och data inte returneras för det valda [Computation Mode ](distance-priority-algorithm.md) (som kör, cyklar eller går) för en leverans, används som standard Source Priority för SSA. Vi rekommenderar att du även anger [prioritet för källor per lager](stocks-prioritize-sources.md).


   - För **[!UICONTROL Select a Source to Ship from]** väljer du en källa att skicka en leverans från.

   - Behåll det rekommenderade beloppet för varje radobjekt eller ange ett specifikt belopp i **[!UICONTROL Qty to Deduct]**. Det här värdet anger det belopp som dras av från lagret för den valda källan.

   - Klicka på **[!UICONTROL Proceed to Shipment]**.

     ![Välj en Source och ange en kvantitet](assets/shipment-adobe-shipping-sources.png){width="350" zoomable="yes"}

1. Granska sidan _[!UICONTROL New Shipment]_&#x200B;och ange eventuella ytterligare ändringar efter behov.

   Avsnittet _[!UICONTROL Inventory]_&#x200B;visar källa, produktleverans, total beställd kvantitet och kvantitet som ska levereras.

   ![Lagerinformation för leveransen, till exempel partiell leverans](assets/inventory-shipment-details.png){width="350" zoomable="yes"}

1. Klicka på **[!UICONTROL Submit Shipment]** för att slutföra.
