---
title: Identifiering av webbläsarfunktioner
description: Lär dig hur du konfigurerar identifiering av webbläsarfunktioner och visar ett meddelande om kundens webbläsarinställningar behöver ändras.
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---

# Identifiering av webbläsarfunktioner

Precis som de flesta webbplatser och tillämpningar på Internet kräver Adobe Commerce och Magento Open Source att besökarens webbläsare tillåter både cookies och JavaScript för att fungera fullt ut. Ibland är dock användarens webbläsare inställd på den högsta sekretessinställningen som förhindrar både cookies och JavaScript. Din butik kan konfigureras för att testa funktionerna i varje besökares webbläsare och visa ett meddelande om inställningarna behöver ändras.

- Om webbläsarens sekretessinställningar inte tillåter cookies kan du konfigurera systemet så att de dirigeras om automatiskt till [Aktivera cookies](../content-design/pages.md#enable-cookies) som förklarar hur du gör de rekommenderade inställningarna i de flesta webbläsare.
- Om webbläsarens sekretessinställningar inte tillåter JavaScript kan du konfigurera systemet så att följande meddelande visas ovanför sidhuvudet på varje sida.

Teknisk information finns i [Webbläsare som stöds](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html#supported-browsers) i _Installationshandbok_.

## Konfigurera identifiering av webbläsarfunktioner

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. På panelen till vänster under _[!UICONTROL General]_, välja **[!UICONTROL Web]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Browser Capabilities Detection]** och gör följande:

   - Om du vill visa instruktioner som förklarar hur du konfigurerar webbläsaren så att cookies tillåts anger du **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** till `Yes`.

   - Om du vill visa en banderoll ovanför rubriken när JavaScript är inaktiverat i användarens webbläsare anger du **[!UICONTROL Show Notice if JavaScript is Disabled]** till `Yes`.

   - Om du vill visa en banderoll ovanför rubriken när Lokal lagring är inaktiverat i användarens webbläsare anger du **[!UICONTROL Show Notice if Local Storage is Disabled]** till `Yes`.

   ![Allmän konfiguration - identifiering av webbläsarfunktioner](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
