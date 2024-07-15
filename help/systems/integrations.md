---
title: Integreringar
description: Lär dig hur du konfigurerar OAuth-autentiseringsuppgifter och omdirigerings-URL för tredjepartsintegreringar.
exl-id: b7632994-b07b-4cdb-b62c-79bc7a3a01c8
role: Admin, Developer
feature: System, Integration, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Integreringar

Genom att definiera en integrering i Commerce Admin kan du fastställa platsen för OAuth-autentiseringsuppgifter och omdirigerings-URL för tredjepartsintegreringar och identifiera tillgängliga API-resurser som behövs för integreringen. Mer information om integreringsregistreringsprocessen finns i [OAuth-baserad autentisering](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) i dokumentationen för Commerce-utvecklare.

![Integrationer](./assets/integrations.png){width="700" zoomable="yes"}

## Arbetsflöde för introduktion

1. **Auktorisera integreringen** - Gå till sidan **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**, hitta den relevanta integreringen och auktorisera.
1. **Verifiera och upprätta inloggning** - Acceptera den begärda åtkomsten när du uppmanas till det. Om du omdirigeras till en tredje part loggar du in på systemet eller skapar ett konto. När inloggningen är klar återgår du till integreringssidan.
1. **Ta emot en bekräftelse på auktoriserad integrering** - Systemet skickar ett meddelande om att integreringen har auktoriserats. När du har konfigurerat en integrering och tagit emot inloggningsuppgifterna behöver du inte längre ringa anrop för att få åtkomst till eller begära tokens.

## Lägg till en integrering

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**på sidofältet_ Admin _.

   ![Ny integrering](./assets/integration-new.png){width="600" zoomable="yes"}

1. Ange följande integreringsinformation:

   - Ange **[!UICONTROL Name]** för integreringen och kontaktadressen **[!UICONTROL Email]**.

   - Ange **[!UICONTROL Callback URL]** dit OAuth-autentiseringsuppgifter kan skickas när OAuth används för tokenutbyte. Vi rekommenderar starkt att du använder `https://`.

   - Ange **[!UICONTROL Identity Link URL]** för att omdirigera användare till ett tredjepartskonto med dessa Adobe Commerce- eller Magento Open Source-integreringsuppgifter.

   >[!NOTE]
   >
   > Varningsetiketten `Integration not secure` visas nära varje integrationsnamn i [!UICONTROL Integrations]-rutnätet som en påminnelse tills HTTPS-URL:er sparas i fälten [!UICONTROL Callback URL] och [!UICONTROL Identity Link URL].

   - Ange ditt lösenord för att bekräfta din identitet när du uppmanas till detta.

1. Välj **[!UICONTROL API]** i den vänstra panelen och gör följande:

   - Ange **[!UICONTROL Resource Access]** till något av följande:

      - `All`
      - `Custom`

   - Markera kryssrutan för varje resurs som behövs för anpassad åtkomst.

     ![Integreringar - tillgängligt API](./assets/integrations-available-api.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]** när du är klar.

## Aktivera en integrering

Som standard visas en sparad integrering i rutnätet med statusen `Inactive`. Så här aktiverar du den:

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**på sidofältet_ Admin _.

1. Hitta den nyskapade integreringen och klicka på länken **[!UICONTROL Activate]**.

1. Klicka på **[!UICONTROL Allow]** i det övre högra hörnet.

   Den här åtgärden visar integreringstoken för tillägg. Kopiera den här informationen till en säker, krypterad plats som kan användas med integreringen.

   ![Integreringstoken för tillägg](./assets/integration-tokens-for-extensions.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Done]** i det övre högra hörnet.

## Återauktorisera en integrering

Om du vill generera en ny integreringsåtkomsttoken och åtkomsttokenhemlighet har du auktoriserat integreringen från administratören igen:

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**på sidofältet_ Admin _.

1. Hitta integreringen med statusen **[!UICONTROL Active]**.

1. Klicka på **[!UICONTROL Reauthorize]** i kolumnen _[!UICONTROL Activate]_.

1. Klicka på **[!UICONTROL Reauthorize]** för att godkänna åtkomst till API-resurserna.

1. Spara de nya integrationstoken för tillägg och klicka på **[!UICONTROL Done]**.

## Ändra säkerhetsinställningen för API-gäståtkomst

Som standard tillåter systemet inte anonym gäståtkomst till CMS, kataloger och andra lagringsresurser. Om du måste ändra inställningen gör du följande:

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Services]** i den vänstra panelen och välj **[!UICONTROL Magento Web API]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Web API Security Setting]**.

   ![Tjänstkonfiguration - säkerhetsinställningar för webb-API](../configuration-reference/services/assets/web-api-security.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Allow Anonymous Guest Access]** till `Yes`.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

Mer information finns i [Begränsa åtkomst till anonyma webb-API:er](https://developer.adobe.com/commerce/webapi/rest/use-rest/anonymous-api-security/) i dokumentationen för Commerce-utvecklare.

## Ta bort en integrering

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**på sidofältet_ Admin _.

1. Leta reda på den befintliga integrationen och klicka på ikonen ( ![papperskorgsikonen](../assets/icon-delete-trashcan-solid.png) ) i kolumnen **[!UICONTROL Delete]** .

1. Bekräfta åtgärden genom att klicka på **[!UICONTROL OK]**.
