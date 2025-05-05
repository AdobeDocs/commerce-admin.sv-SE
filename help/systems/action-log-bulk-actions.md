---
title: Massåtgärder
description: Lär dig hur du konfigurerar och visar massåtgärdsloggen.
exl-id: 3907d9ef-3592-4dbb-805f-97b79bafd8ab
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# Massåtgärder

{{ee-feature}}

Massåtgärdsloggen registrerar information om asynkrona massåtgärder som körs i bakgrunden, till exempel import/export eller tilldelning av [anpassade priser](../b2b/catalog-shared-manage.md#update-custom-pricing) till flera produkter i en [delad katalog](../b2b/catalog-shared.md).

![Logg för massåtgärder](./assets/bulk-actions-log.png){width="600" zoomable="yes"}

## Konfigurera massåtgärder

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Advanced]** i den vänstra panelen och välj **[!UICONTROL System]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Bulk Actions]** och ange alternativet för att spara loggen:

   **[!UICONTROL Days Saved in Log]** - Ange antalet dagar som massåtgärder sparas i en logg.

   ![Avancerad konfiguration - massåtgärder](../configuration-reference/advanced/assets/system-bulk-actions.png){width="600" zoomable="yes"}

   En detaljerad lista över konfigurationsinställningarna finns i [_Massåtgärder_](../configuration-reference/advanced/system.md) i _Konfigurationsreferens_.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Visa massåtgärder

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Bulk Actions]**&#x200B;på sidofältet_ Admin _.

1. Sök efter önskad åtgärd i loggen.

1. Klicka på **[!UICONTROL Details]** i kolumnen _[!UICONTROL Action]_.
