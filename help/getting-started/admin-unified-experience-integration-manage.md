---
title: Hantera Experience Cloud-integrering
description: Lär dig hur du hanterar Experience Cloud-integrering och felsöker problem
hide: false
hidefromtoc: false
feature: Integration
exl-id: 451bf2e1-7c38-40be-a7c1-aaf0fe9f486c
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---

# Hantera Experience Cloud-integrering

Efter den första aktiveringen kan du hantera statusen för Experience Cloud-integreringen genom att aktivera eller inaktivera tillägget Commerce Admin Unified Experience.

- Om Commerce Admin Unified Experience-tillägget är aktiverat och administratörskonton [har etablerats korrekt](#manage-admin-user-accounts) kan Commerce-administratörer visa och komma åt tillgängliga Commerce-projekt från Adobe Experience Cloud. Administratörer kan fortfarande komma åt enskilda projekt via Admin URL för Commerce projektmiljö.

- Om Commerce Admin Unified Experience-tillägget är inaktiverat inaktiveras åtkomsten via Experience Cloud. Administratörer måste logga in på enskilda projekt med Admin URL för Commerce projektmiljö.

>[!WARNING]
>
>Om integreringen av Adobe Identity Management-tjänsten (IMS) inaktiveras Experience Cloud-integreringen automatiskt.

## Hantera integreringen från administratören

1. Öppna menyn Konfiguration av butik i Commerce Admin genom att välja **[!UICONTROL Stores]** i den vänstra navigeringsmenyn och sedan välja **[!UICONTROL Configuration]**.

1. Välj **[!UICONTROL Advanced > Admin]** på menyn Konfiguration och expandera sedan **[!UICONTROL Unified Experience option]**.

   ![Konfiguration av Admin Store för Experience Cloud-integrering](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. Aktivera eller inaktivera integreringen genom att välja värdet **[!UICONTROL Enable]**.

1. Ändra projektnamnet som visas på arbetsytan i Commerce Projects genom att lägga till eller uppdatera värdet **[!UICONTROL Project Name]**.

1. Spara konfigurationen.

1. Rensa cachen.

## Hantera integreringen med Adobe Commerce CLI

Commerce systemadministratörer med administratörsåtkomst till Commerce molnprojekt kan använda Adobe Commerce CLI-kommandon för att hantera Experience Cloud-integreringen.

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

Alla Commerce Admin-användare måste ha både ett Admin-konto på Commerce-instansen och ett Adobe-användarkonto (Adobe ID) för att få tillgång till Adobe produkter och tjänster. Båda kontona måste vara kopplade till samma e-postadress.

- **Commerce Admin-konto**—[Hantera Commerce Admin-användare](../systems/permissions-users-all.md) från Admin för Commerce-instansen. Användarkonton för Commerce-administratörer måste tilldelas rollen Admin.

  Systemadministratörer i Commerce-projektet kan använda [SSH för att ansluta till fjärrmiljön](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html?lang=sv-SE#connect-to-a-remote-environment) och använda kommandona Commerce CLI `admin:user:create` och `admin:user:unlock` för att lägga till eller låsa upp administratörskonton.

- **Adobe-användarkonto** - En administratör för den Adobe-organisation som är kopplad till Commerce-instansen måste logga in på Adobe Admin Console och lägga till Adobe ID för varje Commerce-administratör i organisationen. Sedan måste de tilldela produktbehörigheter och behörigheter för att få tillgång till Commerce-programmet. Se [Konfigurera Adobe Commerce-användare i Adobe Admin Console](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console).

Administratörer som hanterar konfigurationen för Experience Cloud-integrering från Adobe Developer Console måste ha ett Adobe-användarkonto med åtkomst för systemadministratör eller utvecklare.

>[!NOTE]
>
>Ett Adobe ID är ett konto som skapats via Adobe och som krävs för att få tillgång till produkter och tjänster via Experience Cloud. Commerce-administratörer som inte har någon Adobe ID kan [skapa ett kostnadsfritt konto](https://helpx.adobe.com/se/manage-account/using/create-update-adobe-id.html) med samma e-postadress som de använder för att logga in på Commerce Admin.
