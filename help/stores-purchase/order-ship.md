---
title: Leverera en beställning
description: Lär dig hur du fyller i leveransinformationen för en bearbetningsorder och visar leveransinformation och spårningsinformation.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: abd125cc6e61850db55fb31dbcbd9dc38ac0fca5
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Leverera en beställning

En beställning som har betalats, men väntar på leverans, har statusen `Processing`. Leveransposten innehåller en detaljerad historik över leveransprocessen som är kopplad till ordern. Delvisa leveranser kan göras tills ordern är slutförd.

1. Välj **[!UICONTROL Sales]** > **[!UICONTROL Orders]** på sidofältet _Admin_.

1. I listan _[!UICONTROL Orders]_letar du reda på den order som ska skickas och klickar för att öppna den.

1. Klicka på knappen **[!UICONTROL Ship]** i det övre högra hörnet.

1. Om du vill uppdatera fakturerings- eller leveransadressen klickar du på länken **[!UICONTROL Edit]** i det övre högra hörnet av avsnittet.

   Gör nödvändiga ändringar och klicka på **[!UICONTROL Save Order Address]**.

1. Om du vill att transportören ska generera en leveransetikett markerar du kryssrutan **[!UICONTROL Create Shipping Label]** och anger alternativen:

   - Om du vill lägga till ett spårningsnummer bläddrar du nedåt till avsnittet _[!UICONTROL Shipping Information]_och klickar på&#x200B;**[!UICONTROL Add Tracking Number]**.

   - Gör något av följande:

      - Markera **[!UICONTROL Carrier]** och ange spårning **[!UICONTROL Number]**.

      - Ange **[!UICONTROL Carrier]** till `Custom Value`, ange **[!UICONTROL Title]** för den anpassade bäraren och ange spårning **[!UICONTROL Number]**.

      - [Visa spårningsinformation](#track-the-shipment).

1. Om du vill göra en delleverans bläddrar du nedåt till avsnittet Artiklar till leverans och anger **[!UICONTROL Qty to Ship]** för varje objekt.

1. Så här meddelar du kunder via e-post om leveransen:

   - Ange eventuella kommentarer som du vill ta med i rutan **[!UICONTROL Shipment Comments]**.

   - Om du vill inkludera kommentarerna i det e-postmeddelande som skickas till kunden markerar du kryssrutan **[!UICONTROL Append Comments]**.

   - Om du vill skicka en kopia av e-postmeddelandet till dig själv markerar du kryssrutan **[!UICONTROL Email Copy of Shipment]**.

     Statusen för ett fakturameddelande visas bredvid fakturanumret för den ifyllda fakturan som skickad eller inte skickad.

1. Klicka på **[!UICONTROL Submit Shipment]** när du är klar.

   Orderns status ändras från `Processing` till `Complete`.

>[!NOTE]
>
>Om en beställning läggs som &quot;leverans i butik&quot; är leveransalternativen inte tillgängliga. Klicka på **[!UICONTROL Notify Order is Ready for Pickup]** om du vill utlösa ett e-postmeddelande till kunden. Orderns status ändras sedan till `Complete`.

## Visa leveransinformation

1. Gå till **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** på sidofältet _Admin_.

1. Leta reda på leveransen i listan och klicka för att öppna posten.

1. Om du vill lägga till en kommentar i ordningen rullar du nedåt till avsnittet _[!UICONTROL Comments History]_och anger kommentaren i rutan.

   - Markera kryssrutan **[!UICONTROL Notify Customer by Email]** om du vill skicka kommentaren till kunden via e-post.

   - Om du vill publicera kommentaren på kundens konto markerar du kryssrutan **[!UICONTROL Visible on Frontend]**.

1. Klicka på **[!UICONTROL Update]**.

## Spåra leveransen

**Metod 1:** Fliken Orderinformation

1. Gå till **[!UICONTROL Sales]** > **[!UICONTROL Orders]** på sidofältet _Admin_.

1. Hitta leveransordern i rutnätet och klicka på **[!UICONTROL View]**.

1. Bläddra ned till avsnittet _[!UICONTROL Shipping & Handling Information]_och klicka på&#x200B;**[!UICONTROL Track Order]**.

   All tillgänglig spårningsinformation visas i ett popup-fönster.

1. Klicka på **[!UICONTROL Close Window]** när du är klar.

**Metod 2:** Fliken Från orderleverans

1. Gå till **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** på sidofältet _Admin_.

1. Leta reda på leveransen i listan och klicka för att öppna posten.

1. Klicka på **[!UICONTROL Track this Shipment]**.

   All tillgänglig spårningsinformation visas i ett popup-fönster.

1. Klicka på **[!UICONTROL Close Window]** när du är klar.
