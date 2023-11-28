---
title: Åtgärdsloggarkiv
description: Lär dig hur du konfigurerar och visar administratörens åtgärdsloggarkiv.
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Åtgärdsloggarkiv

{{ee-feature}}

Administratören [funktionsmakron](action-log.md) arkiv listar de CSV-loggfiler som lagras på servern. I konfigurationen kan du ange hur länge loggposterna ska lagras och hur ofta de ska arkiveras. Som standard innehåller filnamnet aktuellt datum i ISO-format:  `yyyyMMddHH`

>[!NOTE]
>
>Loggarkivering kräver en [cron](cron.md) som ska konfigureras.

## Konfigurera loggarkivet

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL System]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Admin Actions Log Archiving]** och ange följande alternativ:

   - **[!UICONTROL Log Entry Lifetime, Days]** — Ange det antal dagar som du vill behålla loggposterna i databasen innan de tas bort.
   - **[!UICONTROL Log Archiving Frequency]** — Ställ in på `Daily`, `Weekly`, eller `Monthly`.

   ![Avancerad konfiguration - arkivering av administratörsåtgärdslogg](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   En detaljerad lista över konfigurationsinställningarna finns i [Loggarkivering för administratörsåtgärder](../configuration-reference/advanced/system.md) i _Konfigurationsreferens_.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Visa arkivet

På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**.

![Åtgärdsloggarkiv](./assets/action-log-archive.png){width="600" zoomable="yes"}
