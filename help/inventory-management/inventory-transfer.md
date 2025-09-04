---
title: Överför lager till källa
description: Lär dig hur flerkällvaruhandlare kan överföra produktlager från en källplats till en annan.
exl-id: 30438412-bc93-4e65-8b6a-5ddb50afa7ff
feature: Inventory, Configuration
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Överför lager till källa

Beroende på verksamhetens behov och status för lokalisering överför handlare med flera källor ofta produktlager från en källplats till en annan. Du kanske till exempel stänger en lagerplats eller inte längre levererar specifika produkter från en plats, vilket flyttar alla operationer för dessa produkter till en ny plats.

Med det här alternativet kan du välja en eller flera produkter, ursprungskällan som ska överföras till lagret och destinationskällan som ska ta emot kvantiteter:

- Lagerkvantiteter, status för Source-artikel (i lager/utlager) och Meddela kvantitet för den valda källan flyttas per produkt.

- Om en produkt inte har den källan hoppas den över.

- Allt produktlager för källan flyttas. Du kan inte överföra en delkvantitet.

>[!NOTE]
>
>Om ursprungs- och destinationskällorna finns i olika lager påverkar detta den aggregerade säljbara kvantiteten och reservationerna för pågående order.

Du kan också ta bort tilldelningen av källan när du överför lagerkvantiteter.

{{$include /help/_includes/unassign-source.md}}

![Överför lager till en annan källa](assets/inventory-bulk-transfer-source.gif)

1. Gå till _>_ på sidofältet **[!UICONTROL Catalog]** Admin **[!UICONTROL Products]**.

1. Välj de produkter som du vill ändra källor för.

   Bläddra eller sök efter produkter och markera kryssrutor för överföring.

1. Klicka på menyn **[!UICONTROL Actions]** överst och välj **[!UICONTROL Transfer Inventory to Source]**.

1. Klicka på **[!UICONTROL OK]** i bekräftelsedialogrutan.

1. Om du vill överföra produkter till en ny destination väljer du ursprungskällan (_[!UICONTROL from]_).

1. Om du vill överföra produkter till ett nytt mål väljer du målkällan (_[!UICONTROL to]_).

1. Om du vill ta bort källan från produkterna markerar du den valfria kryssrutan **[!UICONTROL Unassign from origin source after transfer]**.

   ![Välj ursprung och mål för överföring](assets/inventory-bulk-transfer-summary.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Transfer Inventory]**.

   Alla produktkvantiteter dras av från ursprungskällan och läggs till i destinationskällan. Kvantitet och säljbart antal uppdateras automatiskt.

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
