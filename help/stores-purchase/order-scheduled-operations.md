---
title: Schemalagda orderåtgärder
description: Lär dig mer om schemalagda beställningsåtgärder och beställningar av cron-inställningar som stöder den här funktionen.
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: db859c40cd6f052a8f1153e245c23d9f1ea97d33
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Schemalagda orderåtgärder

Använd [Cron](../systems/cron.md) jobb för att schemalägga följande sorteringsåtgärder:

![Ordningsrutnät](./assets/orders-grid.png){width="700" zoomable="yes"}

## Ange livslängd för väntande betalningsorder

Löptiden för order med väntande betalningar bestäms av _Kroniinställningar för order_ konfiguration. Standardvärdet är 480 minuter, vilket är åtta timmar.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Sales]** och välja **[!UICONTROL Sales]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Orders Cron Settings]** -avsnitt.

   ![Kroniinställningar för order](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. För **[!UICONTROL Pending Payment Order Lifetime (minutes)]** anger du antalet minuter innan en väntande betalning förfaller.

1. Klicka på **[!UICONTROL Save Config]**.

## Aktivera schemalagda stödrasteruppdateringar och omindexering

Konfigurationen av stödrasterinställningar schemalägger uppdateringar av följande orderhanteringsrutnät och indexerar om data enligt schemat av [Cron](../systems/cron.md):

- [Beställningar](orders.md#orders-workspace)
- [Fakturor](invoices.md)
- [Leveranser](shipments.md)
- [Kreditnotor](credit-memos.md)

Genom att schemalägga dessa uppgifter kan du undvika de lås som uppstår när data sparas och minska bearbetningstiden. När det här alternativet är aktiverat utförs uppdateringar endast under det schemalagda kron-jobbet. För bästa resultat bör Cron konfigureras att köras en gång i minuten.

**_Så här aktiverar du uppdateringar och omindexering:_**

När [Produktionsläge](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode) (standardläget som används i Adobe Commerce i molninfrastruktur) är aktiverat, kör följande kommando:

``bin/magento config:set dev/grid/async_indexing 1``

När [Standardläge](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode) är aktiverat utför du följande steg:

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Advanced]** och välja **[!UICONTROL Developer]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Grid Settings]** -avsnitt.

1. Ange **[!UICONTROL Asynchronous Indexing]** till `Enable`.

   ![Stödrasterinställningar](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]**.
