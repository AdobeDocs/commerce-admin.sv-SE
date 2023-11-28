---
title: Leverera en beställning
description: Lär dig hur du fyller i leveransinformationen för en bearbetningsorder och visar leveransinformation och spårningsinformation.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# Leverera en beställning

En beställning som har betalats men väntar på leverans har `Processing` status. Leveransposten innehåller en detaljerad historik över leveransprocessen som är kopplad till ordern. Delvisa leveranser kan göras tills ordern är slutförd.

1. På _Administratör_ sidlist, välj **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. I _[!UICONTROL Orders]_söker du efter den order som ska skickas och klickar för att öppna den.

1. Klicka i det övre högra hörnet på **[!UICONTROL Ship]** -knappen.

1. Om du vill uppdatera fakturerings- eller leveransadressen klickar du på **[!UICONTROL Edit]** i det övre högra hörnet av avsnittet.

   Gör nödvändiga ändringar och klicka på **[!UICONTROL Save Order Address]**.

1. Om du vill att transportören ska generera en leveransetikett väljer du **[!UICONTROL Create Shipping Label]** och ange alternativ:

   - Om du vill lägga till ett spårningsnummer bläddrar du nedåt till _[!UICONTROL Shipping Information]_och klicka **[!UICONTROL Add Tracking Number]**.

   - Gör något av följande:

      - Välj **[!UICONTROL Carrier]** och ange spårning **[!UICONTROL Number]**.

      - Ange **[!UICONTROL Carrier]** till `Custom Value`, ange **[!UICONTROL Title]** för den anpassade bäraren och ange spårning **[!UICONTROL Number]**.

      - [Visa spårningsinformation](#track-the-shipment).

1. Om du vill göra en delleverans bläddrar du nedåt till avsnittet Artiklar till leverans och anger **[!UICONTROL Qty to Ship]** för varje objekt.

1. Så här meddelar du kunder via e-post om leveransen:

   - Ange eventuella kommentarer som du vill inkludera i **[!UICONTROL Shipment Comments]** box.

   - Om du vill inkludera kommentarerna i det e-postmeddelande som skickas till kunden väljer du **[!UICONTROL Append Comments]** kryssrutan.

   - Om du vill skicka en kopia av e-postmeddelandet till dig själv väljer du **[!UICONTROL Email Copy of Shipment]** kryssrutan.

     Statusen för ett fakturameddelande visas bredvid fakturanumret för den ifyllda fakturan som skickad eller inte skickad.

1. När du är klar klickar du på **[!UICONTROL Submit Shipment]**.

   Orderns status ändras från `Processing` till `Complete`.

>[!NOTE]
>
>Om en beställning läggs som &quot;leverans i butik&quot; är leveransalternativen inte tillgängliga. Klicka **[!UICONTROL Notify Order is Ready for Pickup]** för att utlösa ett e-postmeddelande till kunden. Orderns status ändras sedan till `Complete`.

## Visa leveransinformation

1. På _Administratör_ sidebar, gå till **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Leta reda på leveransen i listan och klicka för att öppna posten.

1. Om du vill lägga till en kommentar i ordningen rullar du nedåt till _[!UICONTROL Comments History]_och ange kommentaren i rutan.

   - Om du vill skicka kommentaren till kunden via e-post väljer du **[!UICONTROL Notify Customer by Email]** kryssrutan.

   - Om du vill bokföra kommentaren på kundens konto väljer du **[!UICONTROL Visible on Frontend]** kryssrutan.

1. Klicka på **[!UICONTROL Submit Comment]**.

## Spåra leveransen

**Metod 1:** Fliken Orderinformation

1. På _Administratör_ sidebar, gå till **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Hitta leveransordern i rutnätet och klicka på **[!UICONTROL View]**.

1. Bläddra nedåt till _[!UICONTROL Shipping & Handling Information]_och klicka **[!UICONTROL Track Order]**.

   All tillgänglig spårningsinformation visas i ett popup-fönster.

1. När du är klar klickar du **[!UICONTROL Close Window]**.

**Metod 2:** Fliken Från orderleverans

1. På _Administratör_ sidebar, gå till **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Leta reda på leveransen i listan och klicka för att öppna posten.

1. Klicka på **[!UICONTROL Track this Shipment]**.

   All tillgänglig spårningsinformation visas i ett popup-fönster.

1. När du är klar klickar du **[!UICONTROL Close Window]**.
