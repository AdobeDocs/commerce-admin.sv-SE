---
title: Konfigurera presentregister
description: Lär dig hur du aktiverar presentregister och konfigurerar relaterade e-postmeddelanden.
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '358'
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

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Customers]** i den vänstra panelen och välj **[!UICONTROL Gift Registry]**

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL General Options]** och gör följande:

   ![Kundkonfiguration - presentregister allmänt](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - Presentregistret är aktiverat som standard. Ange **[!UICONTROL Enable Gift Registry]** till `Yes` om det behövs.

   - För **[!UICONTROL Maximum Registrants]** anger du det maximala antalet personer som kan bjudas in att delta i en presentregisterhändelse.

## Steg 2. Konfigurera e-postmeddelanden

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Owner Notification]** och gör följande:

   ![Kundkonfiguration - meddelande om ägare av presentregister](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - Välj den **[!UICONTROL Email Template]** som meddelar presentregisterägare när deras register skapas.

   - Välj den [butikskontakt](../getting-started/store-details.md#store-email-addresses) som visas som **[!UICONTROL Email Sender]** i meddelandet.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Gift Registry Sharing]** och gör följande:

   ![Kundkonfiguration - delning av presentregister](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - Välj den **[!UICONTROL Email Template]** som meddelar mottagarna i presentregistret när ett register delas med dem.

   - Välj den butiksidentifiering som visas som **[!UICONTROL Email Sender]** för meddelandet.

   - För **[!UICONTROL Maximum Sent Emails Threshold]** anger du det maximala antalet e-postmeddelanden som kan skickas samtidigt.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Gift Registry Update]** och gör följande:

   ![Kundkonfiguration - uppdatering av presentregistret](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - Välj den **[!UICONTROL Email Template]** som meddelar presentregisterägare om ändringar i registret.

   - Välj den butiksidentifiering som visas som **[!UICONTROL Email Sender]** för meddelandet.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

1. Uppdatera cacheminnet när du uppmanas att göra det.

   När cachen har uppdaterats visas presentregistret på menyn Lager under Andra inställningar och blir tillgängligt på kundkonton.
