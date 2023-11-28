---
title: Konfigurera Experience Cloud-integrering för Commerce Admin
description: Lär dig hur du konfigurerar ett Commerce-projekt för att ge administratörsåtkomst via Experience Cloud.
hide: false
hidefromtoc: false
feature: Integration
role: Admin, Leader
exl-id: b2522d25-8255-4219-98b5-4b764430dea2
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '1130'
ht-degree: 0%

---

# Konfigurera integreringen av Experience Cloud med Commerce Admin

{{$include /help/_includes/admin-unified-experience-beta-note.md}}

Kom igång med integreringen av Experience Cloud med Commerce Admin genom att konfigurera Commerce-programmet så att det använder tilläggen för Enhetlig upplevelse och handelshändelser i Commerce Admin.


## Förutsättningar

- Adobe Commerce måste vara konfigurerat att använda [Adobe IMS-autentisering](../getting-started/adobe-ims-config.md)
- Kontoetablering och behörigheter - Administratörer måste ha en [Adobe affärsprofil](https://helpx.adobe.com/enterprise/kb/introducing-adobe-profiles.html#:~:text=Adobe%20profiles%20help%20you%20manage,under%20the%20same%20email%20address) med tillgång till följande resurser för att konfigurera integreringen av Experience Cloud:
   - [Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html)—Lägg till och hantera användare- och utvecklarkonton för Adobe för organisationen
   - [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/getting-started/)—Åtkomst för utvecklare eller systemadministratör för att skapa App Builder-projekt och generera anslutningsinformationen och projektkonfigurationen för att använda tjänsten Adobe I/O Events
   - [Commerce on cloud Infrastructure project](https://experienceleague.adobe.com/docs/commerce-cloud-service/start/onboarding.html#get-started-with-the-project-web-interface)—Installera nödvändiga moduler och konfigurera Commerce-programservern med Adobe Commerce CLI
   - [Commerce Admin](https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html)—Uppdatera butikskonfiguration och hantera Commerce-användarkonton

## Konfigurationsöversikt

Aktivera integreringen genom att utföra följande uppgifter:

1. [Kontrollera Commerce-miljön och programkonfigurationen](#check-the-commerce-environment-and-application-configuration).

1. [Aktivera tillägget Enhetlig upplevelse för Commerce Admin](#enable-the-commerce-admin-unified-experience-extension).

1. [Ställ in Adobe I/O-händelser för handel](#set-up-adobe-io-events).

1. [Testa integreringen](#test-the-integration).

## Kontrollera Commerce-miljön och programkonfigurationen

Innan du konfigurerar integreringen med Experience Cloud bör du kontrollera att ditt projekt och ditt Commerce-program uppfyller kraven.

1. Byt till projektkatalogen för ditt Commerce-projekt på din lokala arbetsstation.

1. Kolla in miljögrenen där instansen kan integreras med Experience Cloud.

1. Kontrollera att Adobe IMS är aktiverat.

   - Använd [URL för SSH-åtkomst](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html) för miljön att ansluta till Commerce-programservern.

   - Använd Adobe Commerce CLI på kommandoraden för att kontrollera IMS-modulens status.

     ```bash
     bin/magento admin:adobe-ims:status
     ```

   Om modulen inte är aktiverad [aktivera det med hjälp av organisationen och inloggningsuppgifterna för IMS-integrationsprojektet](../getting-started/adobe-ims-config.md#step-3-enable-the-adminadobeims-module). Om du inte har inloggningsuppgifterna [skicka en Adobe Support-biljett](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket).

1. Kontrollera att administratörsanvändaren kan logga in i Commerce Admin med sin Adobe ID.

   - Gå till Commerce Admin URL.

   - Logga ut om du är inloggad.

   - Se till att administratörsanvändaren omdirigeras för att logga in med sin Adobe ID.

     ![Adobe Commerce Logga in med Adobe ID](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

1. Kontrollera att Commerce Admin Unified Experience-tillägget är installerat från molnprojektkatalogen på din lokala arbetsstation.

   ```bash
   composer show *unified-experience*
   ```

   Om tillägget är installerat returnerar Composer tilläggets namn och beskrivning.

   ```
   magento/module-unified-experience <version> Commerce module responsible for integration with Adobe Experience Cloud
   ```

   Om tillägget inte är installerat kan du installera det med Composer. Verkställ sedan ändringarna och distribuera om molnmiljön.

   ```
   composer require magento/module-unified-experience
   composer update
   ```

## Aktivera Enhetlig upplevelse för Commerce Admin

Aktivera tillägget Commerce Admin Unified Experience och logga sedan in via Experience Cloud.

>[!NOTE]
>
>Dessa instruktioner visar hur en Commerce Cloud-projektadministratör kan aktivera tillägget med Adobe Commerce CLI. Commerce Admin-användare kan även aktivera tillägget genom att uppdatera [Konfigurationsinställningar för Commerce Store](admin-unified-experience-integration-manage.md#from-the-commerce-admin).

1. Använd rotkatalogen i din molnprojektmiljö på din lokala arbetsstation [magento-cloud CLI tool](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/dev-tools/cloud-cli/cloud-cli-overview.html) för att logga in på Commerce-programservern.

   ```bash
   magento-cloud ssh
   ```

1. Aktivera `magento/module-unified-experience` tillägg med Adobe Commerce CLI:

   ```bash
   bin/magento config:set admin/unified_experience/enabled 1
   Admin Unified Experience integration is enabled
   ```

1. Rensa cachen.

   ```bash
   bin/magento cache:clean
   ```

## Ställ in Adobe I/O-händelser för handel

När integreringen av Experience Cloud är aktiverad skickar händelsetjänsten Adobe I/O-händelser Commerce-data till Experience Cloud för att hantera administratörsåtkomst till Commerce-projekt. Tjänstkonfigurationen kräver att Adobe I/O Events för Commerce-tillägget aktiveras (`magento/commerce-eventing`) och konfigurera Adobe I/O Events-tjänsten i Admin.

### Aktivera Commerce Events

Aktivera tillägget Commerce Events (`magento/commerce-eventing`) för att skicka anpassade händelsedata från Commerce-programmet till Adobe I/O Events-tjänsten.

>[!NOTE]
>
>I Commerce 2.4.6 och senare installeras tillägget Commerce Events som standard. För handelsprojekt med Commerce 2.4.5 använder du först Composer för att [installera tillägget](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce)och sedan aktivera den.

1. Lägg till följande konfiguration i den lokala utvecklingsmiljön för Commerce `.magento.env.yaml` -fil.

   ```yaml
   stage:
     global:
       ENABLE_EVENTING: true
     deploy:
       CRON_CONSUMERS_RUNNER:
         cron_run: true
         max_messages: 0
         consumers: []
   ```

1. Lägg till, implementera och distribuera den uppdaterade `.magento.env.yaml file` till molnmiljön.

>[!TIP]
>
>Mer information om hur du konfigurerar och hanterar miljövariabler med `.magento.env.yaml` -fil, se [Konfigurera miljövariabler för distribution](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/configure-env-yaml.html).

### Konfigurera integrering av Commerce Events

Konfigurera integreringen av Commerce Events genom att utföra följande uppgifter. Detaljerade anvisningar finns i [Adobe I/O Events for Commerce](https://developer.adobe.com/commerce/extensibility/events/project-setup/) dokumentation för utvecklare.

1. [Skapa ett App Builder-projekt](https://developer.adobe.com/commerce/extensibility/events/project-setup/) för att ta emot händelsedata från Commerce-instansen.

   Du behöver autentiseringsuppgifter och konfigurationsdata från App Builder-projektet för att konfigurera integreringen i Commerce Admin.

1. Konfigurera Adobe Commerce att använda Adobe I/O Events.

   - [Uppdatera inställningarna för butikskonfiguration för tjänsten Adobe I/O Events](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#begin-configuring-events-on-commerce).

   - [Konfigurera en händelseleverantör för att skicka Commerce-händelser](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#create-an-event-provider-and-complete-the-commerce-configuration).

1. [Uppdatera App Builder-projektet för att ta emot händelsedata från Commerce-instansen](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#subscribe-and-register-events).

   Registrera eller prenumerera inte på händelser från Commerce-instansen. Händelseregistreringen skickas till App Builder-projektet när du konfigurerar händelseprovidern för Commerce-programmet.

   När du har anslutit händelseprovidern till App Builder-projektet kan du prenumerera på `observer.uex_commerce_instance_update` och spara ändringarna.

1. Om du vill upprätta anslutningen skickar du en händelse via händelseprovidern till konsumenten.

   - Från kommandoraden i den lokala molnprojektkatalogen [använd SSH för att ansluta till Commerce-programservern](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment).

     ```bash
     magento-cloud ssh
     ```

   - Skicka händelsedata genom att kontrollera statusen för Admin Unified Experience-tillägget med Adobe Commerce CLI.

     ```bash
     bin/magento bin/magento admin:uex:status
     ```

### Testa integreringen

Verifiera att en Commerce Administrator kan logga in på Experience Cloud för att visa tillgängliga Commerce-projekt och komma åt Admin och Storefront för varje projekt.

1. [Logga in på Experience Cloud](https://experiencecloud.adobe.com/library) med den Adobe ID och organisation som är associerad med Commerce-instansen.

   ![Få åtkomst till Commerce-projekt från Experience Cloud hemsida](./assets/admin-uex-home-page.png){width="600" zoomable="yes"}

1. Visa tillgängliga Commerce Projects genom att välja **[!UICONTROL Commerce]**.

   ![Arbetsytan för Commerce Projects för Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="600" zoomable="yes"}

1. Öppna administratören för en instans genom att välja **[!UICONTROL Open]**.

   ![Commerce Admin-vyn med integrering med Experience Cloud aktiverad](./assets/admin-dashboard.png){width="600" zoomable="yes"}

1. Verifiera att du kan utföra administratörsåtgärder som förväntat.

   Samma process bör användas för arbetsflöden i Commerce Admin. Om du får arbetsflödesändringar eller fel när du har aktiverat integreringen med Experience Cloud kontaktar du din Commerce-systemadministratör eller [skicka en Adobe Support-biljett](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket).

När du har konfigurerat integreringen med Experience Cloud kontrollerar du att administratörskonton har etablerats korrekt för att få åtkomst till Commerce-projekt via Experience Cloud. Se [Hantera administratörsanvändare](/help/getting-started/admin-unified-experience-integration-manage.md#manage-admin-user-accounts).
