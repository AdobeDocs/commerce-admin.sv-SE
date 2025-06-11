---
title: Använd ett leveransnätverk
description: Lär dig hur du använder ett CDN (Content Delivery Network) för att lagra mediefiler.
exl-id: cb612b79-f3e3-4f1b-8cf9-d47886486686
feature: Page Content, Media, Configuration
level: Experienced
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---

# Använd ett leveransnätverk

Ett leveransnätverk kan användas för att lagra mediefiler. I Adobe Commerce molninfrastruktur ingår snabbt-CDN (se [Snabbt](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/fastly.html) i _Commerce on Cloud Infrastructure Guide_). En Commerce-instans som är installerad _lokalt_ innehåller ingen integrering med ett specifikt CDN. Du kan använda valfritt CDN.

När du har konfigurerat CDN måste du slutföra konfigurationen från administratören. Ändringarna kan göras antingen globalt eller på webbplatsnivå. När ett CDN används för medielagring ändras alla sökvägar till media på Commerce Store-sidor till de CDN-sökvägar som anges i konfigurationen.

## CDN-arbetsflöde

1. **Webbläsaren begär media** - en sida från butiken öppnas i kundens webbläsare och webbläsaren begär media som har angetts i HTML.
1. **Begäran skickades till CDN; bilder hittades och kunde hanteras** - Begäran skickas först till CDN. Om CDN har bilderna i lager skickas mediefilerna till kundens webbläsare.
1. **Mediet hittades inte, begäran skickades till [!DNL Commerce] webbservern** - Om CDN inte har mediefilerna skickas begäran till [!DNL Commerce]-webbservern. Om mediefilerna hittas i filsystemet skickas de till kundens webbläsare av webbservern.

>[!IMPORTANT]
>
>Av säkerhetsskäl fungerar inte JavaScript korrekt om ett CDN används som medielagring om det finns utanför din underdomän.

## Konfigurera ett nätverk för innehållsleverans

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Välj **[!UICONTROL Web]** i den vänstra panelen under _[!UICONTROL General]_.

1. Ange **[!UICONTROL Store View]** efter behov i det övre vänstra hörnet.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Base URLs]** och gör följande:

   ![Allmän konfiguration - webbbas-URL:er](./assets/web-base-urls.png){width="600" zoomable="yes"}

   - Uppdatera **[!UICONTROL Base URL for Static View Files]** med URL:en för den plats i CDN där statiska vyfiler lagras.

   - Uppdatera **[!UICONTROL Base URL for User Media Files]** med URL:en för JavaScript-filerna på CDN:en.

     Båda dessa fält kan lämnas tomma eller börja med platshållaren: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Base URLs (Secure)]** och gör följande:

   ![Allmän konfiguration - webbbas-URL:er (säkra)](./assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - Uppdatera **[!UICONTROL Secure Base URL for Static View Files]** med URL:en för den plats i CDN där statiska vyfiler lagras.

   - Uppdatera **[!UICONTROL Secure Base URL for User Media Files]** med URL:en för JavaScript-filerna på CDN:en.

     Båda dessa fält kan lämnas tomma eller börja med platshållaren: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
