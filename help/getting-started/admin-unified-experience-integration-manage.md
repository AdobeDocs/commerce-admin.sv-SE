---
title: Hantera integreringen med Experience Cloud
description: Lär dig hur du hanterar integreringen av Experience Cloud och felsöker problem
hide: false
hidefromtoc: false
feature: Integration
exl-id: 451bf2e1-7c38-40be-a7c1-aaf0fe9f486c
source-git-commit: 15569794c1e66ba5a93e46206244e2951522923e
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Hantera integreringen med Experience Cloud

Efter den första aktiveringen kan du hantera statusen för integreringen av Experience Cloud genom att aktivera eller inaktivera tillägget för enhetlig körning i Commerce Admin.

- Om tillägget Enhetlig upplevelse i Commerce Admin är aktiverat och administratörskonton är [tillhandahålls korrekt](#manage-admin-user-accounts)kan Commerce-administratörer visa och komma åt tillgängliga Commerce-projekt från Adobe Experience Cloud. Administratörer kan fortfarande komma åt enskilda projekt via Admin URL för Commerce-projektmiljön.

- Om tillägget för Commerce Admin Unified Experience är inaktiverat inaktiveras åtkomsten via Experience Cloud. Administratörer måste logga in på enskilda projekt med Admin URL för Commerce-projektmiljön.

>[!WARNING]
>
>Om integreringen av Adobe Identity Management-tjänsten (IMS) är inaktiverad inaktiveras integreringen av Experience Cloud automatiskt.

## Hantera integreringen från administratören

1. Öppna menyn Konfiguration av butik i Commerce Admin genom att välja **[!UICONTROL Stores]** från den vänstra navigeringsmenyn och välj **[!UICONTROL Configuration]**.

1. Välj på menyn Konfiguration **[!UICONTROL Advanced > Admin]** och sedan expandera **[!UICONTROL Unified Experience option]**.

   ![Konfiguration av Admin Store för integrering med Experience Cloud](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. Aktivera eller inaktivera integreringen genom att välja **[!UICONTROL Enable]** värde.

1. Ändra projektnamnet som visas på arbetsytan för Commerce Projects genom att lägga till eller uppdatera **[!UICONTROL Project Name]** värde.

1. Spara konfigurationen.

1. Rensa cachen.

## Hantera integreringen med Adobe Commerce CLI

Administratörer i Commerce-system med administratörsåtkomst till Commerce-molnprojektet kan använda Adobe Commerce CLI-kommandon för att hantera integreringen med Experience Cloud.

1. Logga in i molnprojektet från din lokala utvecklingsmiljö.

   ```bash
   magento-cloud login
   ```

1. Anslut till Commerce-programservern från rotkatalogen i din molnprojektmiljö.

   ```bash
   ssh magento-cloud
   ```

1. Kontrollera status för Admin Unified Experience-tillägget:

   ```bash
   bin/magento admin:uex:status
   ```

1. Ändra status för tillägget för att inaktivera integreringen

   - **Aktivera**—`bin/magento config:set admin/unified_experience/enabled 1`

   - **Inaktivera**—`bin/magento config:set admin/unified_experience/enabled 0`

## Hantera administratörsanvändarkonton

Alla Commerce Admin-användare måste ha både ett administratörskonto i Commerce-instansen och ett Adobe-användarkonto (Adobe ID) för att få tillgång till produkter och tjänster i Adobe. Båda kontona måste vara kopplade till samma e-postadress.

- **Commerce Admin-konto**—[Hantera användare i Commerce Admin](../systems/permissions-users-all.md) från Admin för Commerce-instansen. Användarkonton för Commerce-administratörer måste tilldelas rollen Admin.

  Systemadministratörer i Commerce-projektet kan använda [SSH för att ansluta till fjärrmiljön](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment)och använda Commerce CLI `admin:user:create` och `admin:user:unlock` kommandon för att lägga till eller låsa upp administratörsanvändarkonton.

- **Adobe användarkonto**—Administratörer för den Adobe-organisation som är associerad med Commerce-instansen måste logga in på Adobe Admin Console och lägga till Adobe ID för varje Commerce-administratör i organisationen. Sedan måste de tilldela produkträttigheter och behörigheter för att få tillgång till Commerce-programmet. Se [Konfigurera Adobe Commerce-användare i Adobe Admin Console](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console).

Administratörer som hanterar konfigurationen för integreringen av Experience Cloud från Adobe Developer Console måste ha ett Adobe-användarkonto med åtkomst för systemadministratör eller utvecklare.

>[!NOTE]
>
>Ett Adobe ID är ett konto som skapats via Adobe som krävs för att få tillgång till produkter och tjänster via Experience Cloud. Handläggare som inte har någon Adobe ID kan [skapa ett kostnadsfritt konto](https://helpx.adobe.com/manage-account/using/create-update-adobe-id.html) med samma e-postadress som de använder för att logga in på Commerce Admin.
