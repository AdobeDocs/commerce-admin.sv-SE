---
title: Designkonfiguration
description: Designkonfigurationen gör det enkelt att redigera designrelaterade regler och konfigurationsinställningar genom att visa inställningarna på en enda sida.
exl-id: 43fec57f-d76d-45a9-812b-ba1947cea46d
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# Designkonfiguration

Designkonfigurationen gör det enkelt att redigera designrelaterade regler och konfigurationsinställningar genom att visa inställningarna på en enda sida.

![Designkonfigurationssida](./assets/configuration.png){width="700" zoomable="yes"}

## Ändra designkonfigurationen

1. På _Administratör_ sidebar, gå till **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Leta reda på butiksvyn som du vill konfigurera och klicka på **[!UICONTROL Edit]** i _[!UICONTROL Action]_kolumn.

   På sidan visas de aktuella designinställningarna för butiksvyn.

1. Om du vill ändra standardtemat anger du **[!UICONTROL Applied Theme]** till temat som du vill använda i vyn.

   Om inget tema anges används systemets standardtema. Vissa tillägg från tredje part ändrar systemets standardtema.

1. Om temat bara ska användas för en viss enhet anger du **[!UICONTROL User Agent Rules]**.

   ![Regler för användaragent](./assets/configuration-user-agent-rules.png){width="400" zoomable="yes"}

   För varje enhetstyp där du vill ange ett tema:

   - Klicka på **[!UICONTROL Add New User Agent Rule]**.

   - För **[!UICONTROL Search String]** anger du webbläsar-ID för den specifika enheten.

     En söksträng kan antingen vara ett normalt uttryck eller ett Perl Compatible Regular Expression (PCRE) (se [Användaragent](https://en.wikipedia.org/wiki/User_agent) för mer information). Följande söksträng identifierar Firefox:

         /^mozilla/i
     
   - För **[!UICONTROL Theme Name]** väljer du det tema som ska användas för den angivna enheten.

   >[!NOTE]
   >
   >Du kan lägga till så många regler för de enheter som du vill ange. Söksträngarna matchas i den ordning de anges.

1. Under _[!UICONTROL Other Settings]_expanderar du varje avsnitt och följer instruktionerna i de länkade avsnitten för att redigera inställningarna efter behov.

   - [[!UICONTROL Pagination]](../catalog/navigation-product-listings.md#pagination-controls)
   - [[!UICONTROL HTML Head]](page-setup.md#html-head)
   - [[!UICONTROL Header]](page-setup.md#header)
   - [[!UICONTROL Footer]](page-setup.md#footer)
   - [[!UICONTROL Search Engine Robots]](../merchandising-promotions/seo-overview.md#search-engine-robots)
   - [[!UICONTROL Product Image Watermarks]](../catalog/product-image.md#watermarks)
   - [[!UICONTROL Transactional Emails]](../systems/email-templates.md#configure-email-templates)

   ![Andra inställningar som påverkar designen](./assets/configuration-other-settings.png){width="500" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Configuration]**.
