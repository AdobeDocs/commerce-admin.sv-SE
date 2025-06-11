---
title: Optimera bilder i Mediegalleriet
description: Lär dig hur du använder bildoptimering för dina  [!DNL Commerce] medieresurser.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# Optimera bilder i Mediegalleriet

Den nya funktionen [Mediegalleriet](media-gallery.md) har en _bildoptimeringsfunktion_ som förbättrar prestanda och minskar storleken på mediefiler i butiken. Den här optimeringen är aktiverad som standard och kan ändras i lagringskonfigurationsinställningarna.

## Konfigurera bildoptimering

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Advanced]** i den vänstra panelen och välj **[!UICONTROL System]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** och gör följande:

   - Ange **[!UICONTROL Enable Image Optimization]** till `Yes`.
   - Ange värdena **[!UICONTROL Maximum Width]** och **[!UICONTROL Maximum Height]** (i pixlar) efter dina behov.

## Beteende

När funktionen för bildoptimering i Mediegalleriet är aktiverad infogas en optimerad kopia av en bild automatiskt i innehållet från [Mediegalleriet](media-gallery.md) i stället för i originalfilen.

När värdena _Maximal bredd_ och _Maximal höjd_ ändras i konfigurationen uppdateras alla befintliga optimerade bilder som infogats tidigare.

Mediegalleriets bildoptimering kräver att `media.gallery.renditions.update`-kökonsumenterna kör för att återskapa optimerade bilder när konfigurationen ändras. Mer information finns i [Hantera meddelandeköer](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) i _Konfigurationshandboken_.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
