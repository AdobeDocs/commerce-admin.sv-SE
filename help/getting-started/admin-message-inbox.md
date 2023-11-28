---
title: Inkorg för administratörsmeddelande
description: Lär dig mer om administratörens inkorg med viktiga och användbara meddelanden från Adobe och från [!DNL Commerce] system.
exl-id: c53bb0e4-9f18-4d40-8cc4-8c3b485f8d68
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Inkorg för administratörsmeddelande

Din butik får meddelanden från Adobe regelbundet. Meddelandena klassas som viktiga och kan gälla systemuppdateringar, korrigeringar, nya versioner, schemalagt underhåll eller kommande evenemang. Klockikonen i sidhuvudet anger antalet olästa meddelanden i inkorgen.

![Administratör - inkommande meddelanden](./assets/admin-inbox-summary.png){width="700" zoomable="yes"}

The _[!UICONTROL Notifications]_På sidan visas alla meddelanden ordnade efter datum. The_[!UICONTROL Action]_ kan användas för att markera enskilda meddelanden som lästa, visa mer detaljerad information eller för att ta bort meddelandet från inkorgen.

Konfigurationen avgör hur ofta inkorgen uppdateras och hur meddelandena levereras. Om din butiksadministratör har en säker URL måste meddelanden levereras via HTTPS.

## Visa nya inkommande meddelanden

1. Klicka på **[!UICONTROL Notification]** i sidhuvudet och läs sammanfattningen.

1. Gör något av följande:

   - Om det behövs klickar du på meddelandet för att visa den fullständiga texten.
   - Om du vill ta bort meddelandet klickar du på borttagningsikonen till höger om meddelandet.
   - Om du vill visa den fullständiga meddelandelistan klickar du på **[!UICONTROL See All]**.

## Åtgärda ett kritiskt meddelande

Gör något av följande om du vill få ett meddelande av avgörande betydelse:

- Klicka på **[!UICONTROL Read Details]**.
- Om du vill stänga varningsrutan men låta meddelandet vara aktivt klickar du på **[!UICONTROL Close]**.

## Administrera aviseringar

1. Öppna meddelandesidan genom att göra något av följande:

   - Klicka på **[!UICONTROL Notification]** i sidhuvudet. Om ett eller flera nya meddelanden visas klickar du på **[!UICONTROL See All]**.

   - På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Notifications]**.

1. I **[!UICONTROL Action]** gör du något av följande:

   - Mer information får du genom att klicka **[!UICONTROL Read Details]** om du vill öppna den länkade sidan i ett nytt fönster.

   - Behåll meddelandet i inkorgen genom att klicka **[!UICONTROL Mark As Read]**.

     ![Admin - Markera valda meddelanden som lästa](./assets/admin-notifications-mark-as-read.png){width="700" zoomable="yes"}

   - Klicka på om du vill ta bort meddelandet **[!UICONTROL Remove]**.

1. Gör något av följande om du vill använda en åtgärd på flera meddelanden:

   - Markera kryssrutan i den första kolumnen för varje meddelande som ska hanteras.
   - Om du vill markera flera meddelanden anger du **[!UICONTROL Mass Actions]** kontroll efter behov.

1. Ange **[!UICONTROL Actions]** kontrollera något av följande:

   - `Mark as Read`
   - `Remove`

1. Klicka **[!UICONTROL Submit]** för att slutföra processen.

## Konfigurera meddelanden

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera i den vänstra navigeringspanelen **[!UICONTROL Advanced]** och välja **[!UICONTROL System]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png)den **[!UICONTROL Notifications]** -avsnitt.

   ![Meddelandekonfiguration](./assets/system-notifications.png){width="600"}

1. Om din butiksadministratör kör över en [säker URL](../stores-purchase/store-urls.md), ange **[!UICONTROL Use HTTPS to Get Feed]** till `Yes`.

1. Ange **[!UICONTROL Update Frequency]** för att avgöra hur ofta din inkorg uppdateras.

   Intervallet kan vara mellan 1 och 24 timmar.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

Mer information om [!UICONTROL System] konfigurationsalternativ, se [_Referenshandbok för konfiguration_](../configuration-reference/advanced/system.md).
