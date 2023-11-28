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

Med [!DNL Inventory Management], skicka en eller flera leveranser när du har lager. Om du vill generera ytterligare leveranser efter behov upprepar du dessa instruktioner med rekommenderade eller manuellt angivna kvantiteter och källor. Instruktionerna beskriver hur flerkällvaruförsäljare skickar leveranser. Handlare med en enda källa skickar leveranser utan dessa ytterligare steg (se [Skapa en leverans](../stores-purchase/shipments.md#create-a-shipment){target="_blank"} i användarhandboken).

När du skapar leveranser använder du algoritmen för källval för beräknade rekommendationer. Följ och använd dessa rekommendationer eller ange beloppen per källa och generera anpassade leveranser. Du kontrollerar ditt utgående lager för varje order och anger vilka belopp som ska dras av, skickar en eller flera leveranser och levererar i lager och restorder när lagret är tillgängligt. Ange ett belopp som ska dras av från källkvantiteten för varje radartikel i ordern.

Du kanske vill skicka delförsändelser till:

- Fyll i restorder när lagret anländer

- Balansera lageravdrag mellan källor

När du anger leveranser dras de inmatade beloppen av lagerbehållningen av. Reservationer konverteras alltså till faktiska kvantitetsavdrag.

## Skapa en leverans

1. På _Administratör_ sidebar, gå till **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Leta reda på ordningen och öppna i visningsläge.

1. Om ordern är betald och fakturerad och är klar att skickas klickar du på **[!UICONTROL Ship]**.

1. Slutför källvalet för att skicka produkter per källa:

   - Om du vill visa leveransrekommendationer klickar du **[!UICONTROL Source Selection Algorithm]** och välja en algoritm.

     | Algoritm | Beskrivning |
     |--|--|
     | [Källprioritet](source-priority-algorithm.md) | Rekommenderar leveranser från källor enligt beställningarna för källor som tilldelats till lagret. |
     | [Avståndsprioritet](distance-priority-algorithm.md) | Rekommenderar försändelser från källor närmast leveransadressen baserat på fysiskt avstånd eller kortast leveranstid. |

     >[!IMPORTANT]
     >
     >När algoritmen Distance Priority (Avståndsprioritet) används för leverans och vägar och data inte returneras för den valda [Beräkningsläge](distance-priority-algorithm.md) (körning, cykling eller gång) för en transport är standardvärdet för SSA källprioritet. Vi rekommenderar att du även ställer in [prioritet för källor per lager](stocks-prioritize-sources.md).


   - För  **[!UICONTROL Select a Source to Ship from]** väljer du en källa att skicka en leverans från.

   - För varje radobjekt ska du behålla det rekommenderade beloppet eller ange ett specifikt belopp i **[!UICONTROL Qty to Deduct]**. Det här värdet anger det belopp som dras av från lagret för den valda källan.

   - Klicka på **[!UICONTROL Proceed to Shipment]**.

     ![Välj en källa och ange en kvantitet](assets/shipment-adobe-shipping-sources.png){width="350" zoomable="yes"}

1. Granska _[!UICONTROL New Shipment]_och ange eventuella ytterligare ändringar.

   The _[!UICONTROL Inventory]_I visas källa, produktleverans, total beställd kvantitet och kvantitet att leverera.

   ![Lagerinformation för leveransen, exempel partiell leverans](assets/inventory-shipment-details.png){width="350" zoomable="yes"}

1. Klicka **[!UICONTROL Submit Shipment]** för att slutföra.
