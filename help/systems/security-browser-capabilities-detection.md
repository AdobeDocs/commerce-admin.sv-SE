---
title: Identifiering av webbläsarfunktioner
description: Lär dig hur du konfigurerar identifiering av webbläsarfunktioner och visar ett meddelande om kundens webbläsarinställningar behöver ändras.
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# Identifiering av webbläsarfunktioner

Precis som de flesta webbplatser och tillämpningar på Internet kräver Adobe Commerce och Magento Open Source att besökarens webbläsare tillåter både cookies och JavaScript för att fungera fullt ut. Ibland är dock användarens webbläsare inställd på den högsta sekretessinställningen som förhindrar både cookies och JavaScript. Din butik kan konfigureras för att testa funktionerna i varje besökares webbläsare och visa ett meddelande om inställningarna behöver ändras.

- Om webbläsarens sekretessinställningar inte tillåter cookies kan du konfigurera systemet så att de dirigeras om automatiskt till sidan [Aktivera cookies](../content-design/pages.md#enable-cookies) , som förklarar hur du gör de rekommenderade inställningarna i de flesta webbläsare.
- Om webbläsarens sekretessinställningar inte tillåter JavaScript kan du konfigurera systemet så att följande meddelande visas ovanför sidhuvudet på varje sida.

Mer teknisk information finns i [Webbläsare som stöds](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html?lang=sv-SE#supported-browsers) i _installationshandboken_.

## Konfigurera identifiering av webbläsarfunktioner

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Välj **[!UICONTROL Web]** på panelen till vänster under _[!UICONTROL General]_.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Browser Capabilities Detection]** och gör följande:

   - Om du vill visa instruktioner som förklarar hur du konfigurerar webbläsaren så att cookies tillåts anger du **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** till `Yes`.

   - Om du vill visa en banderoll ovanför rubriken när JavaScript är inaktiverat i användarens webbläsare anger du **[!UICONTROL Show Notice if JavaScript is Disabled]** till `Yes`.

   - Om du vill visa en banderoll ovanför rubriken när Lokal lagring är inaktiverat i användarens webbläsare anger du **[!UICONTROL Show Notice if Local Storage is Disabled]** till `Yes`.

   ![Allmän konfiguration - identifiering av webbläsarfunktioner](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
