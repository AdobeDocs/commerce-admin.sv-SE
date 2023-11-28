---
title: Konfigurera e-postkommunikation
description: Lär dig hur du konfigurerar e-postkommunikation, inklusive dirigering av returnerad e-post eller svar till en viss e-postadress.
exl-id: 7e62e9c5-f214-4fd5-becc-99dcb093cd5c
feature: Communications, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Konfigurera e-postkommunikation

The _Inställningar för att skicka e-post_ ger dig möjlighet att dirigera returnerad e-post eller svar till en viss adress. Om din butik körs på en SMTP- eller Windows-server kan du kontrollera värd- och portinställningarna.

>[!IMPORTANT]
>
>**Säkerhetsmeddelande** Alla handlare bör omedelbart ställa in sin sändningskonfiguration för e-post för att skydda mot en nyligen identifierad potentiell fjärrexekvering av kod. Du bör undvika att använda [!DNL Sendmail] för e-postkommunikation. I _[!UICONTROL Mail Sending Settings]_måste du se till att_[!UICONTROL Set Return Path]_ är inställd på `No`.

En detaljerad lista över konfigurationsinställningarna finns i [_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md) i _Konfigurationsreferens_.

## Konfigurera e-postkommunikation

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL System]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Mail Sending Settings]** och gör följande:

   ![Avancerad konfiguration - inställningar för e-postsändning](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - Ange vid behov **[!UICONTROL Disable Email Communications]** till `No`.

   - För **[!UICONTROL Transport]** väljer du transporttyp för e-postkommunikation från butiken: `Sendmail` eller `SMTP`

   - Om du kör på en SMTP- eller Windows-server kontrollerar du följande inställningar:

      - **[!UICONTROL Host]** - `localhost` eller andra

      - **[!UICONTROL Port (25)]** - `25` eller andra

   - För **[!UICONTROL Set Return Path]** väljer du något av följande alternativ:

      - `No` - (Rekommenderat säkerhetsmått) Rutorna returnerade e-post till standardbutikens e-postadress.
      - `Yes` - Vägarna returnerade e-post till standardbutikens e-postadress.
      - `Specified` - Vägarna returnerade e-post till den e-postadress som angavs i **[!UICONTROL Return Path Email]**.

   - Konfigurera anslutningen om den körs på en SMTP-server:

      - **[!UICONTROL Username]** - Ange inloggningsnamnet för SMTP-servern.
      - **[!UICONTROL Password]** - Ange lösenordet för SMTP-serverinloggningen.
      - **[!UICONTROL Auth]** - Välj autentiseringstyp för SMTP-serveranslutningen: `NONE` , `PLAIN`, eller `LOGIN`
      - **[!UICONTROL SSL]** - Välj verifieringstyp för serversäkerhetscertifikatet: `SSL` eller `TLS`

     ![Avancerad konfiguration - inställningar för e-postsändning](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Sales Emails]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL General Settings]** -avsnitt.

1. Ange **[!UICONTROL Asynchronous sending]** till `Enable`.

   ![Försäljningskonfiguration - allmänna inställningar för e-post](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   En detaljerad lista över konfigurationsinställningarna finns i [_Allmänna inställningar_](../configuration-reference/sales/sales-emails.md) i _Konfigurationsreferens_.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
