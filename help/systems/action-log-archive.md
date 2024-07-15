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

Administratörens [åtgärder](action-log.md)-arkiv visar CSV-loggfiler som lagras på servern. I konfigurationen kan du ange hur länge loggposterna ska lagras och hur ofta de ska arkiveras. Som standard innehåller filnamnet aktuellt datum i ISO-format:  `yyyyMMddHH`

>[!NOTE]
>
>Loggarkivering kräver att ett [cron-jobb](cron.md) har konfigurerats.

## Konfigurera loggarkivet

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Advanced]** i den vänstra panelen och välj **[!UICONTROL System]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Admin Actions Log Archiving]** och ange följande alternativ:

   - **[!UICONTROL Log Entry Lifetime, Days]** - Ange det antal dagar som du vill behålla loggposterna i databasen innan de tas bort.
   - **[!UICONTROL Log Archiving Frequency]** - Ange som `Daily`, `Weekly` eller `Monthly`.

   ![Avancerad konfiguration - arkivering av administratörsåtgärdslogg](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   En detaljerad lista över konfigurationsinställningarna finns i [Arkivering av administratörsåtgärdslogg](../configuration-reference/advanced/system.md) i _Konfigurationsreferens_.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Visa arkivet

Gå till **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**på sidofältet_ Admin _.

![Åtgärdsloggarkiv](./assets/action-log-archive.png){width="600" zoomable="yes"}
