---
title: ' [!DNL Media Gallery]'
description: Använd Mediegalleriet för att ordna och hantera dina mediefiler på servern.
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# [!DNL Media Gallery]

Med Adobe Commerce eller Magento Open Source 2.4 kan handlare använda den nya _förbättrade_ [!DNL Media Gallery] för att ordna och hantera sina mediefiler på servern. Den nya [!DNL Media Gallery] innehåller samma funktioner som den befintliga medielagringen, men innehåller ett förbättrat användargränssnitt och en närmare integrering med [Adobe Stock][adobe-stock].

![Bilder som visas i stödrastret för mediegalleriet](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Produktbilder som lagts till i [_[!UICONTROL Images and Videos]_-produktavsnittet ](../catalog/product-image.md#upload-an-image) hanteras inte av [!DNL Media Gallery]. Endast bilder som används i produktavsnittsfälten för_[!UICONTROL Content]_ visas och filtreras i den nya [!DNL Media Gallery].

## Aktivera nya [!DNL Media Gallery]

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Advanced]** i den vänstra panelen och välj **[!UICONTROL System]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**.

   ![Avancerad konfiguration - [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enable Old Media Gallery]** till `No`.

1. Klicka på **[!UICONTROL Save Config]**.

1. När du uppmanas till det klickar du på länken **[!UICONTROL Cache Management]** i systemmeddelandet och uppdaterar den ogiltiga cachen.

   [[!UICONTROL Content]-menyn ](/help/content-design/content-menu.md) visar nu det nya _[!UICONTROL Media Gallery]_-alternativet.

>[!NOTE]
>
>Fullständig funktionalitet för nya [!DNL Media Gallery] kräver att `media.gallery.synchronization`- och `media.content.synchronization`-kökonsumenter startas för inledande synkronisering. Mer information finns i [Hantera meddelandeköer](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) i _Konfigurationshandboken_.

## Åtkomst till nya [!DNL Media Gallery]

Den nya [!DNL Media Gallery] är tillgänglig på menyn Innehåll eller när du [lägger till eller redigerar en sida](/help/content-design/page-add.md). Du kan även komma åt den när du [skapar eller redigerar en kategori](/help/catalog/category-create.md) eller när du [infogar bilder med Innehållsredigeraren](/help/content-design/editor-insert-image.md).

Så här kommer du åt den nya [!UICONTROL Media Gallery] via menyn [!UICONTROL Content]:

- Gå till **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**på sidofältet_ Admin _.

Så här kommer du åt det nya mediegalleriet när du lägger till eller redigerar en sida:

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add a New Page]**.

   Om du vill redigera en befintlig sida kan du använda kolumnen _[!UICONTROL Action]_för att klicka på&#x200B;**[!UICONTROL Select]**och välja **[!UICONTROL Edit]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Content]** och gör följande:

   - Om du har [Page Builder aktiverat](../page-builder/setup.md) expanderar du panelen **[!UICONTROL Media]** och drar en **[!UICONTROL Image]** platshållare till målbehållaren. Klicka sedan på **[!UICONTROL Select from Gallery]**.

     ![Dra bilden till scenen](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - Om [WYSIWYG-redigeraren är aktiverad](/help/content-design/editor.md) klickar du på **[!UICONTROL Show/Hide Editor]** och sedan på **[!UICONTROL Insert Image]**.

## [!DNL Media Gallery] demo

Titta på den här videon om du vill veta mer om [!DNL Media Gallery]:

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12&learn=on)

[adobe-stock]: https://stock.adobe.com

