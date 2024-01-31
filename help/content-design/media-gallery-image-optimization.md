---
title: Optimera bilder i Mediegalleriet
description: Lär dig använda bildoptimering för [!DNL Commerce] medieresurser.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Optimera bilder i Mediegalleriet

Den nya [Mediegalleri](media-gallery.md) ger en _bildoptimering_ som förbättrar prestanda och minskar storleken på mediefiler i butiken. Den här optimeringen är aktiverad som standard och kan ändras i lagringskonfigurationsinställningarna.

## Konfigurera bildoptimering

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL System]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** och gör följande:

   - Ange **[!UICONTROL Enable Image Optimization]** till `Yes`.
   - Ange **[!UICONTROL Maximum Width]** och **[!UICONTROL Maximum Height]** värden (i pixlar) efter behov.

## Beteende

När funktionen för bildoptimering i Mediegalleriet är aktiverad infogas en optimerad kopia av en bild automatiskt i innehållet från [Mediegalleri](media-gallery.md) i stället för den ursprungliga filen.

När _Maximal bredd_ och _Maximal höjd_ om du ändrar värden i konfigurationen uppdateras alla befintliga optimerade bilder som infogats tidigare.

Bildoptimering i Mediegalleriet kräver att `media.gallery.renditions.update` köanvändare körs för att återskapa optimerade bilder när konfigurationen ändras. Se [Hantera meddelandeköer](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) i _Konfigurationshandbok_ för mer information.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
