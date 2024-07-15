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

Funktionen Åtgärdsloggar registrerar (loggar) alla ändringar som görs av en Admin-användare som arbetar i din butik. På så sätt kan du spåra alla ändringar som gjorts i din butik. Genom att spåra dessa ändringar, tillsammans med att ställa in [administratörsbehörighet](permissions.md) för en användare, kan du skydda din butik från oönskade ändringar.

För de flesta administratörsåtgärder omfattar den loggade informationen åtgärden, användarens namn, om åtgärden lyckades eller misslyckades samt ID:t för objektet som påverkas av åtgärden. IP-adressen och datumet loggas också.

Som standard är alla administratörsåtgärder aktiverade och loggade. Om du vill konfigurera loggning av administratörsåtgärder granskar du alternativen och markerar eller avmarkerar kryssrutan för varje åtgärdstyp. Adobe Commerce loggar endast markerade typer.

Visa [Åtgärdsloggrapporten](action-log-report.md) om du vill granska loggade administratörsåtgärder och detaljer.

![Avancerad konfiguration - loggning av administratörsåtgärder](../configuration-reference/advanced/assets/admin-actions-logging.png){width="600" zoomable="yes"}

En detaljerad lista över konfigurationsinställningarna finns i [Arkivering av administratörsåtgärdslogg](../configuration-reference/advanced/system.md) i _Konfigurationsreferens_.

## Konfigurera administratörsåtgärder för loggning

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Advanced]** i den vänstra panelen och välj **[!UICONTROL Admin]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Admin Actions Logging]** och gör följande för varje åtgärd:

   - Markera kryssrutan om du vill aktivera administratörsloggning för åtgärden.
   - Avmarkera kryssrutan om du vill inaktivera administratörsloggning för åtgärden.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Logg för administratörsåtgärder

Administratörsåtgärdsloggar kan arkiveras i valfritt antal dagar. Arkiv kan också tas bort efter en angiven varaktighet.

1. Expandera **[!UICONTROL Advanced]** i den vänstra panelen och välj **[!UICONTROL System]**.

1. Expandera **[!UICONTROL Admin Action Log Archiving]** och ange alternativ:

   - **[!UICONTROL Logs Entry Lifetime, Days]** - Ange antalet dagar som arkiverad logg ska sparas.
   - **[!UICONTROL Log Archiving Frequency]** - Ange frekvens för att skapa arkiv.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
