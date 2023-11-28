---
title: Skicka e-post till en vän
description: Lär dig hur du skapar en e-postlänk som gör det enkelt för dina kunder att dela länkar till produkter med sina vänner.
exl-id: 46cf9994-6490-4cb4-85b7-9a7cab7783e0
feature: Storefront, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Skicka e-post till en vän

Länken E-post gör det enkelt för dina kunder att dela länkar till produkter med sina vänner. I demobutiken Luma visas länken E-post som en kuvertikon. Meddelandemallen kan anpassas efter din röst och ditt varumärke. För att förhindra skräppost kan du begränsa antalet mottagare för varje e-postmeddelande och antalet produkter som kan delas under en timma.

![Exempel på butik - skicka ett e-postmeddelande till en vän](./assets/storefront-email-a-friend.png){width="700" zoomable="yes"}

## Konfigurera e-post-en-vän

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL Email to a Friend]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Email Templates]** och ange alternativ:

   ![Katalogkonfiguration - e-postmallar](../configuration-reference/catalog/assets/email-to-a-friend-email-templates.png){width="600" zoomable="yes"}

   En detaljerad beskrivning av de här konfigurationsinställningarna finns i [E-postmallar](../configuration-reference/catalog/email-to-a-friend.md) i _Referenshandbok för konfiguration_.

   Om du vill ändra standardinställningen för ett fält avmarkerar du **[!UICONTROL Use system value]** för att göra fältet redigerbart.

   - Ange **[!UICONTROL Enabled]** till `Yes`.

   - Ange **[!UICONTROL Select Email Template]** till mallen som du vill använda som grund för meddelandena.

   - Om du vill att bara registrerade kunder ska kunna skicka e-post till vänner anger du **[!UICONTROL Allow for Guests]** till `No`.

   - För **[!UICONTROL Max Recipients]** anger du det maximala antalet vänner som kan finnas i distributionslistan för ett enda meddelande.

   - För **[!UICONTROL Max Products Sent in 1 Hour]** anger du det maximala antalet produkter som en enskild användare kan dela med vänner under en tidsperiod på en timme.

   - Ange **[!UICONTROL Limit Sending By]** till någon av följande metoder för att identifiera avsändaren av e-postmeddelanden:

     `IP Address`  - (Rekommenderas) Identifierar avsändaren med IP-adressen för den dator som används för att skicka e-postmeddelanden.

     `Cookie (unsafe)` - Identifierar avsändaren via webbläsarens cookie. Den här metoden är mindre effektiv eftersom avsändaren kan ta bort cookien för att kringgå gränsen.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Skicka e-post till en vän i butiken

När den här funktionen är konfigurerad följer butikskunder dessa steg för att dela produktinformation med vänner.

1. På en katalogsida klickar kunden på **[!UICONTROL Email]** länk.

1. Om funktionen bara är konfigurerad för registrerade användare gör något av följande:

   - Loggar in på ditt kundkonto.
   - Registrerar ett nytt konto.

1. Slutför **[!UICONTROL Message]** och anger mottagaren **[!UICONTROL Name]** och **[!UICONTROL Email Address]**.

   Vid behov kan kunden lägga till fler mottagare:

   - Klickningar **[!UICONTROL Add Invitee]**.

   - Anger **[!UICONTROL Name]** och **[!UICONTROL Email Address]** för den andra personen.

     De kan skicka meddelandet till så många andra personer som konfigurationen tillåter. De kan ta bort den tillagda inbjudaren genom att klicka på **[!DNL Remove]** länk.

1. När du är klar att skicka meddelandet klickar du **[!UICONTROL Send Email]**.

   ![Exempelbutiken - e-post till en vän](./assets/storefront-email-a-friend-form.png){width="700" zoomable="yes"}
