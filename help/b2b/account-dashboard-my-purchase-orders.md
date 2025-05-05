---
title: '[!UICONTROL My Purchase Orders]'
description: Läs mer om inköpsorder och hur företag kan använda dem för att hantera sina inköp.
exl-id: b7348bc8-b874-4642-a372-530883d9d94c
feature: B2B, Companies, Purchase Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# [!UICONTROL My Purchase Orders]

När inköpsorder är [aktiverade för ett företag](purchase-order-flow.md) skapas automatiskt alla order för en kund som är inloggad på ett företagsanvändarkonto som en inköpsorder (PO). Företagsanvändare med nödvändig behörighet kan skapa, redigera och ta bort inköpsordrar som de skapar, tillsammans med de inköpsordrar som skapas av underordnade användare.

![Mina inköpsorder](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Inköpsorder skapar en _ögonblicksbild_ av artikelpriser, rabatter och leveranspriser när ordern skapades. Om priset på en artikel ändras efter att inköpsordern har skapats, används det ursprungliga priset.

## Hantera inköpsorder

Från sidan _Visa inköpsorder_ kan kunden hantera inköpsordern beroende på deras [rollbehörigheter](account-company-roles-permissions.md).

- Klicka på **[!UICONTROL View]** om du vill visa PO:n.
- Klicka på fliken **[!UICONTROL Comments]** om du vill se kommentarer om PO:n.
- Klicka på fliken **[!UICONTROL History Log]** om du vill se en fullständig orderhistorik.

>[!IMPORTANT]
>
>Om en artikel i en inköpsorder inte finns i lager, eller har otillräckligt antal tillgängliga, uppstår ett fel när inköpsordern konverteras till en faktisk order. Om restorder är aktiverade bearbetas ordern normalt.

## Ny inköpsorder från befintlig inköpsorder

Om kunden har en befintlig inköpsorder och vill lägga till nya artiklar kan de generera en dubblettinköpsorder med nya produkter som läggs till i den nya inköpsordern. Kunden utför följande steg:

1. På sidan _Min inköpsorder_ hittar kunden inköpsordern och klickar på länken **[!UICONTROL View]**.

1. Kunden klickar på **[!UICONTROL Add Items to Shopping Cart]**.

   Sidan Kundvagn öppnas med alla artiklar listade.

1. Gör tillägg eller ändringar.

1. (Valfritt) Använder **[!UICONTROL Custom Reference Number]** för att lägga till ett internt faktura-/inköpsordernummer i ordern.

1. Följer det normala arbetsflödet för utcheckning och klickar på **[!UICONTROL Place Purchase Order]**.

Om de har artiklar i kundvagnen när de klickar på _[!UICONTROL Add Items to Shopping Cart]_&#x200B;visas en dialogruta. I den här dialogrutan kan de välja mellan att sammanfoga varukorgen med de nya artiklarna eller att ersätta artiklarna i kundvagnen med artiklarna i inköpsordern.

Den ursprungliga inköpsordern kan stängas om den inte längre behövs.

## Godkännanden av inköpsorder

För en kund som har utsetts till godkännare baserat på företagsstruktur eller tilldelad företagsroll visas fliken **[!UICONTROL Requires My Approval]** på kontrollpanelen _[!UICONTROL My Purchase Orders]_. Kunden klickar på den här fliken för att granska inköpsordrar som väntar på godkännande. Räknaren visar hur många order som väntar på godkännande.

När du har klickat på **[!UICONTROL View]** för en inköpsorder och granskat informationen kan godkännaren klicka på **[!UICONTROL Approve]** eller **[!UICONTROL Reject]**.

### Massgodkännande/avvisning

Från och med Adobe Commerce 2.4.1 kan godkännarna godkänna eller avvisa flera inköpsorder samtidigt.

1. Klicka på fliken **[!UICONTROL Requires My Approval]** på sidan _[!UICONTROL My Purchase Order]_.

1. Markera kryssrutan för varje inköpsorder som ska godkännas eller avvisas.

1. Klicka på **[!UICONTROL Approve Selected]** eller **[!UICONTROL Reject Selected]**.

En kund kan bara välja inköpsorder med en status som tillåter en åtgärd. Företagsadministratörer kan göra bulkgodkännanden eller avslag för aktiva inköpsorder i företaget.
