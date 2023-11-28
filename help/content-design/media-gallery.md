---
title: The [!DNL Media Gallery]
description: Använd Mediegalleriet för att ordna och hantera dina mediefiler på servern.
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# The [!DNL Media Gallery]

Med Adobe Commerce eller Magento Open Source 2.4 kan handlarna använda nya _förbättrad_ [!DNL Media Gallery] för att ordna och hantera sina mediefiler på servern. Den här nya [!DNL Media Gallery] innehåller samma funktioner som den befintliga medielagringen, men har ett förbättrat användargränssnitt och en närmare integrering med [Adobe Stock][adobe-stock].

![Bilder som visas i stödrastret i mediegalleriet](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Produktbilder som lagts till i [_[!UICONTROL Images and Videos]_produktsektion](../catalog/product-image.md#upload-an-image) hanteras inte av [!DNL Media Gallery]. Endast bilder som används i_[!UICONTROL Content]_ produktavsnittsfält visas och filtreras i nya [!DNL Media Gallery].

## Aktivera nya [!DNL Media Gallery]

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL System]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**.

   ![Avancerad konfiguration - [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enable Old Media Gallery]** till `No`.

1. Klicka på **[!UICONTROL Save Config]**.

1. När du uppmanas till det klickar du på **[!UICONTROL Cache Management]** i systemmeddelandet och uppdatera den ogiltiga cachen.

   The [[!UICONTROL Content] meny](/help/content-design/content-menu.md) visar nu det nya _[!UICONTROL Media Gallery]_alternativ.

>[!NOTE]
>
>Fullständig funktionalitet för nya [!DNL Media Gallery] kräver `media.gallery.synchronization` och `media.content.synchronization` köanvändare ska startas för inledande synkronisering. Se [Hantera meddelandeköer](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) i _Konfigurationshandbok_ för mer information.

## Få tillgång till nya [!DNL Media Gallery]

Den nya [!DNL Media Gallery] går att komma åt från menyn Innehåll eller när du [lägga till eller redigera en sida](/help/content-design/page-add.md). Du kan även komma åt den när du [skapa eller redigera en kategori](/help/catalog/category-create.md)eller när du [infoga bilder med Innehållsredigeraren](/help/content-design/editor-insert-image.md).

Så här kommer du åt den nya [!UICONTROL Media Gallery] via [!UICONTROL Content] meny:

- På _Administratör_ sidebar, gå till **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

Så här kommer du åt det nya mediegalleriet när du lägger till eller redigerar en sida:

1. På _Administratör_ sidebar, gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Klicka på **[!UICONTROL Add a New Page]**.

   Om du vill redigera en befintlig sida kan du använda _[!UICONTROL Action]_kolumn att klicka på&#x200B;**[!UICONTROL Select]**och välja **[!UICONTROL Edit]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Content]** och gör följande:

   - Om du har [Page Builder aktiverat](../page-builder/setup.md), expandera **[!UICONTROL Media]** och dra en **[!UICONTROL Image]** platshållare till målbehållaren. Klicka sedan på **[!UICONTROL Select from Gallery]**.

     ![Dra bilden till scenen](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - Om du har [WYSIWYG-redigeraren är aktiverad](/help/content-design/editor.md), klicka **[!UICONTROL Show/Hide Editor]** och sedan klicka **[!UICONTROL Insert Image]**.

## [!DNL Media Gallery] demo

Läs mer om [!DNL Media Gallery], se den här videon:

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12)

[adobe-stock]: https://stock.adobe.com

