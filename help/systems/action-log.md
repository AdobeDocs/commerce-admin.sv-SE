---
title: Åtgärdsloggar
description: Lär dig mer om åtgärdsloggar och hur du konfigurerar loggade åtgärder så att du kan spåra alla ändringar som gjorts i din butik.
exl-id: a482adfe-a63f-428b-b078-7542a1e2ecee
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Åtgärdsloggar

{{ee-feature}}

Funktionen Åtgärdsloggar registrerar (loggar) alla ändringar som görs av en Admin-användare som arbetar i din butik. På så sätt kan du spåra alla ändringar som gjorts i din butik. Spåra dessa ändringar tillsammans med inställningar [Administratörsbehörigheter](permissions.md) för en användare kan hjälpa till att skydda din butik mot oönskade ändringar.

För de flesta administratörsåtgärder omfattar den loggade informationen åtgärden, användarens namn, om åtgärden lyckades eller misslyckades samt ID:t för objektet som påverkas av åtgärden. IP-adressen och datumet loggas också.

Som standard är alla administratörsåtgärder aktiverade och loggade. Om du vill konfigurera loggning av administratörsåtgärder granskar du alternativen och markerar eller avmarkerar kryssrutan för varje åtgärdstyp. Adobe Commerce loggar endast markerade typer.

Visa [Åtgärdsloggsrapport](action-log-report.md) för att granska loggade administratörsåtgärder och detaljer.

![Avancerad konfiguration - loggning av administratörsåtgärder](../configuration-reference/advanced/assets/admin-actions-logging.png){width="600" zoomable="yes"}

En detaljerad lista över konfigurationsinställningarna finns i [Loggarkivering för administratörsåtgärder](../configuration-reference/advanced/system.md) i _Konfigurationsreferens_.

## Konfigurera administratörsåtgärder för loggning

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL Admin]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Admin Actions Logging]** och gör följande för varje åtgärd:

   - Markera kryssrutan om du vill aktivera administratörsloggning för åtgärden.
   - Avmarkera kryssrutan om du vill inaktivera administratörsloggning för åtgärden.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Logg för administratörsåtgärder

Administratörsåtgärdsloggar kan arkiveras i valfritt antal dagar. Arkiv kan också tas bort efter en angiven varaktighet.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL System]**.

1. Expandera **[!UICONTROL Admin Action Log Archiving]** och ange alternativ:

   - **[!UICONTROL Logs Entry Lifetime, Days]** - Ange antalet dagar som arkiverad logg ska sparas.
   - **[!UICONTROL Log Archiving Frequency]** - Ange frekvens för att skapa arkiv.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
