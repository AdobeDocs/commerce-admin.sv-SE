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

![Exempel på butik - skicka e-post till en vän](./assets/storefront-email-a-friend.png){width="700" zoomable="yes"}

## Konfigurera e-post-en-vän

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Email to a Friend]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Email Templates]** och ange alternativen:

   ![Katalogkonfiguration - e-postmallar](../configuration-reference/catalog/assets/email-to-a-friend-email-templates.png){width="600" zoomable="yes"}

   En detaljerad beskrivning av de här konfigurationsinställningarna finns i [E-postmallar](../configuration-reference/catalog/email-to-a-friend.md) i _referenshandboken för konfiguration_.

   Om du vill ändra standardinställningen för ett fält avmarkerar du kryssrutan **[!UICONTROL Use system value]** så att fältet kan redigeras.

   - Ange **[!UICONTROL Enabled]** till `Yes`.

   - Ange **[!UICONTROL Select Email Template]** till mallen som du vill använda som grund för meddelandena.

   - Om du vill kräva att bara registrerade kunder kan skicka e-post till vänner anger du **[!UICONTROL Allow for Guests]** till `No`.

   - För **[!UICONTROL Max Recipients]** anger du det maximala antalet vänner som kan finnas i distributionslistan för ett enskilt meddelande.

   - För **[!UICONTROL Max Products Sent in 1 Hour]** anger du det maximala antalet produkter som kan delas av en enskild användare med vänner under en tidsperiod på en timme.

   - Ange **[!UICONTROL Limit Sending By]** till en av följande metoder för att identifiera avsändaren av e-postmeddelanden:

     `IP Address` - (Rekommenderas) Identifierar avsändaren med IP-adressen för datorn som används för att skicka e-postmeddelanden.

     `Cookie (unsafe)` - Identifierar avsändaren via webbläsarcookie. Den här metoden är mindre effektiv eftersom avsändaren kan ta bort cookien för att kringgå gränsen.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Skicka e-post till en vän i butiken

När den här funktionen är konfigurerad följer butikskunder dessa steg för att dela produktinformation med vänner.

1. På en katalogsida klickar kunden på länken **[!UICONTROL Email]**.

1. Om funktionen bara är konfigurerad för registrerade användare gör något av följande:

   - Loggar in på ditt kundkonto.
   - Registrerar ett nytt konto.

1. Slutför **[!UICONTROL Message]** och anger mottagaren **[!UICONTROL Name]** och **[!UICONTROL Email Address]**.

   Vid behov kan kunden lägga till fler mottagare:

   - Klicka på **[!UICONTROL Add Invitee]**.

   - Anger **[!UICONTROL Name]** och **[!UICONTROL Email Address]** för den andra personen.

     De kan skicka meddelandet till så många andra personer som konfigurationen tillåter. De kan ta bort den tillagda inbjudaren genom att klicka på länken **[!DNL Remove]**.

1. När du är klar att skicka meddelandet klickar du på **[!UICONTROL Send Email]**.

   ![Exempel på butiksadress - e-post till en vän](./assets/storefront-email-a-friend-form.png){width="700" zoomable="yes"}
