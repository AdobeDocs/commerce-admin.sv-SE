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

Med _inställningarna för att skicka e-post_ kan du dirigera returnerad e-post eller svar till en viss adress. Om din butik körs på en SMTP- eller Windows-server kan du kontrollera värd- och portinställningarna.

>[!IMPORTANT]
>
>**Säkerhetsmeddelande** Alla handlare bör omedelbart ställa in sin sändningskonfiguration för e-post för att skydda mot en nyligen identifierad potentiell fjärrexekvering av kod. Vi rekommenderar att du undviker att använda [!DNL Sendmail] för e-postkommunikation tills problemet är löst. Kontrollera att _[!UICONTROL Set Return Path]_&#x200B;är inställt på `No` i&#x200B;_[!UICONTROL Mail Sending Settings]_.

En detaljerad lista över konfigurationsinställningarna finns i [_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md) i _konfigurationsreferensen_.

## Konfigurera e-postkommunikation

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Advanced]** i den vänstra panelen och välj **[!UICONTROL System]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Mail Sending Settings]** och gör följande:

   ![Avancerad konfiguration - inställningar för e-postsändning](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL Disable Email Communications]** till `No` om det behövs.

   - För **[!UICONTROL Transport]** väljer du transporttyp för e-postkommunikation från butiken: `Sendmail` eller `SMTP`

   - Om du kör på en SMTP- eller Windows-server kontrollerar du följande inställningar:

      - **[!UICONTROL Host]** - `localhost` eller annan

      - **[!UICONTROL Port (25)]** - `25` eller annan

   - Välj något av följande alternativ för **[!UICONTROL Set Return Path]**:

      - `No` - (rekommenderat säkerhetsmått) Rutorna returnerade e-post till standardbutikens e-postadress.
      - `Yes` - Vägarna returnerade e-post till standardbutikens e-postadress.
      - `Specified` - Vägarna returnerade e-post till den e-postadress som angavs i **[!UICONTROL Return Path Email]**.

   - Konfigurera anslutningen om den körs på en SMTP-server:

      - **[!UICONTROL Username]** - Ange inloggningsanvändarnamnet för SMTP-servern.
      - **[!UICONTROL Password]** - Ange lösenordet för SMTP-serverinloggningen.
      - **[!UICONTROL Auth]** - Välj autentiseringstyp för SMTP-serveranslutningen: `NONE`, `PLAIN` eller `LOGIN`
      - **[!UICONTROL SSL]** - Välj verifieringstyp för serversäkerhetscertifikatet: `SSL` eller `TLS`

     ![Avancerad konfiguration - inställningar för e-postsändning](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Sales Emails]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL General Settings]**.

1. Ange **[!UICONTROL Asynchronous sending]** till `Enable`.

   ![Försäljningskonfiguration - allmänna inställningar för e-post](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   En detaljerad lista över konfigurationsinställningarna finns i [_Allmänna inställningar_](../configuration-reference/sales/sales-emails.md) i _Konfigurationsreferens_.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
