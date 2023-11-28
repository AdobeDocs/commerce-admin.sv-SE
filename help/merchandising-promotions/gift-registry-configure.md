---
title: Konfigurera presentregister
description: Lär dig hur du aktiverar presentregister och konfigurerar relaterade e-postmeddelanden.
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Konfigurera presentregister

{{ee-feature}}

Innan du kan erbjuda dina kunder presentregister måste du aktivera presentregister och konfigurera relaterade e-postmeddelanden. Adobe Commerce skickar följande e-postmeddelanden som svar på händelser i presentregistrets arbetsflöde.

- När ett nytt presentregister skapas skickas ett e-postmeddelande till ägaren med en länk till registret som kan delas.
- Butiken kan också skicka ett meddelande med en länk till presentregistret till vänner och familj som äger presentregistret.
- Ägaren meddelas när artiklar köps in från presentregistret, men anger inte köparen.

Adobe Commerce har fördefinierade mallar för vart och ett av dessa e-postmeddelanden som kan anpassas för ert varumärke.

## Steg 1. Aktivera presentregister

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Customers]** och välja **[!UICONTROL Gift Registry]**

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL General Options]** och gör följande:

   ![Kundkonfiguration - presentregister allmänt](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - Presentregistret är aktiverat som standard. Ange vid behov **[!UICONTROL Enable Gift Registry]** till `Yes`.

   - För **[!UICONTROL Maximum Registrants]** anger du det maximala antalet personer som kan bjudas in att delta i en presentregisterhändelse.

## Steg 2. Konfigurera e-postmeddelanden

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Owner Notification]** och gör följande:

   ![Kundkonfiguration - meddelande om ägare av presentregister](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - Välj **[!UICONTROL Email Template]** som meddelar ägare av presentregister när deras register skapas.

   - Välj [butikskontakt](../getting-started/store-details.md#store-email-addresses) som visas som **[!UICONTROL Email Sender]** av meddelandet.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Gift Registry Sharing]** och gör följande:

   ![Kundkonfiguration - delning av presentregister](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - Välj **[!UICONTROL Email Template]** som meddelar mottagarna i presentregistret när ett register delas med dem.

   - Välj den butiksidentifiering som visas som **[!UICONTROL Email Sender]** av meddelandet.

   - För **[!UICONTROL Maximum Sent Emails Threshold]** anger du det maximala antalet e-postmeddelanden som kan skickas samtidigt.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Gift Registry Update]** och gör följande:

   ![Kundkonfiguration - uppdatering av presentregister](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - Välj **[!UICONTROL Email Template]** som informerar presentatörens ägare om ändringar i registret.

   - Välj den butiksidentifiering som visas som **[!UICONTROL Email Sender]** av meddelandet.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

1. Uppdatera cacheminnet när du uppmanas att göra det.

   När cachen har uppdaterats visas presentregistret på menyn Lager under Andra inställningar och blir tillgängligt på kundkonton.
