---
title: Använd ett leveransnätverk
description: Lär dig hur du använder ett CDN (Content Delivery Network) för att lagra mediefiler.
exl-id: cb612b79-f3e3-4f1b-8cf9-d47886486686
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Använd ett leveransnätverk

Ett leveransnätverk kan användas för att lagra mediefiler. Adobe Commerce i molninfrastrukturen innehåller Fast CDN (se [Snabbt](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/fastly.html) i _Handbok för Commerce on Cloud Infrastructure_). En Commerce-instans som är installerad _lokal_ innehåller ingen integrering med något specifikt CDN, du kan använda det CDN som du väljer.

När du har konfigurerat CDN måste du slutföra konfigurationen från administratören. Ändringarna kan göras antingen globalt eller på webbplatsnivå. När ett CDN används för medielagring ändras alla sökvägar till media på Commerce Store-sidor till de CDN-sökvägar som anges i konfigurationen.

## CDN-arbetsflöde

1. **Webbläsaren begär media** - En sida från butiken öppnas i kundens webbläsare och webbläsaren begär media som är angivet i HTML.
1. **Begäran skickad till CDN; bilder hittades och kunde hanteras** - Begäran skickas först till CDN. Om CDN har bilderna i lager skickas mediefilerna till kundens webbläsare.
1. **Mediet hittades inte, begäran skickades till [!DNL Commerce] webbserver** - Om leveransnätverket inte har några mediefiler skickas begäran till [!DNL Commerce] webbserver. Om mediefilerna hittas i filsystemet skickas de till kundens webbläsare av webbservern.

>[!IMPORTANT]
>
>Av säkerhetsskäl fungerar inte JavaScript korrekt om ett CDN används som medielagring om CDN finns utanför din underdomän.

## Konfigurera ett nätverk för innehållsleverans

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I den vänstra panelen under _[!UICONTROL General]_, välja **[!UICONTROL Web]**.

1. I det övre vänstra hörnet anger du **[!UICONTROL Store View]** efter behov.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Base URLs]** och gör följande:

   ![Allmän konfiguration - webbbasens URL:er](./assets/web-base-urls.png){width="600" zoomable="yes"}

   - Uppdatera **[!UICONTROL Base URL for Static View Files]** med URL:en för den plats i CDN där statiska vyfiler lagras.

   - Uppdatera **[!UICONTROL Base URL for User Media Files]** med URL:en för JavaScript-filerna på CDN:en.

     Båda dessa fält kan lämnas tomma eller börja med platshållaren: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Base URLs (Secure)]** och gör följande:

   ![Allmän konfiguration - webbbas-URL:er (säkra)](./assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - Uppdatera **[!UICONTROL Secure Base URL for Static View Files]** med URL:en för den plats i CDN där statiska vyfiler lagras.

   - Uppdatera **[!UICONTROL Secure Base URL for User Media Files]** med URL:en för JavaScript-filerna på CDN:en.

     Båda dessa fält kan lämnas tomma eller börja med platshållaren: `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
