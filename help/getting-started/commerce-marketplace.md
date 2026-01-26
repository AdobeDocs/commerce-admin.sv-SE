---
title: '[!DNL Adobe Commerce Marketplace]'
description: Lär dig mer om  [!DNL Commerce Marketplace], som erbjuder handlare ett välstrukturerat urval av lösningar, och ger kvalificerade utvecklare verktyg, plattform och primär plats för att skapa ett livskraftigt företag.
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1282'
ht-degree: 0%

---

# Adobe Commerce Marketplace

[Adobe Commerce Marketplace](https://marketplace.magento.com/) är en programbutik som erbjuder handlare ett välstrukturerat urval av lösningar och ger kvalificerade utvecklare de verktyg, den plattform och den plats där de ska skapa ett livskraftigt företag. [!DNL Commerce Marketplace] erbjuder ett urval tillägg som är tillgängliga utan kostnad och andra som är till salu. Inköp kan betalas med kreditkort eller [PayPal](https://www.paypal.com/us/home).

Alla tillägg som är tillgängliga på [!DNL Commerce Marketplace] har genomgått en omfattande granskning. [EQP (Extension Quality Program](https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/)) kombinerar [!DNL Commerce] expertis, riktlinjer för utveckling och verifieringsverktyg för att säkerställa att alla tillägg i Commerce Marketplace uppfyller kodningsstandarder och bästa praxis. Granskningsprocessen innefattar både en automatiserad kontroll och en manuell QA-granskning. Under processen undersöks och testas strukturen och koden för varje förlängning för tecken på virus-/virusinfektion och eventuella tecken på plagiarism. Granskningen innehåller en djupgående teknisk undersökning och en säkerhetskontroll utförd av en [!DNL Commerce]-tekniker, med fokus på dokumentation, kodningsstruktur, prestanda, skalbarhet, säkerhet och kompatibilitet med [!DNL Commerce]-kärnan.

Även om du kan köpa tillägg från andra källor verifieras endast de tillägg som är tillgängliga på [!DNL Commerce Marketplace] via omfattande teknisk granskning och marknadsföringsgranskning i Extension Quality Program.

## Appresurser

Utvecklare har traditionellt använt PHP för att skapa tillägg i processen som lägger till funktioner, funktioner, tjänster och integreringar i Adobe Commerce. Genom att skapa program med utbyggbarhet som inte har bearbetats, i motsats till tillägg, kan du undvika kompatibilitetsproblem.

Följande resurser är en startpunkt för nya användare som vill bekanta sig med appar:

### Commerce-resurser

- [Konfigurera I/O-händelser för Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/)
- [Konfigurera händelser för Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [Konfigurera administratörsgränssnittet för SDK](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [Konverterar ett tillägg till ett program](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### App Builder-resurser

- [Commerce App Builder - översikt](https://developer.adobe.com/commerce/extensibility/app-development/)
- [Konfigurera API-nät för Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [Distribuerar App Builder-program](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [CI/CD för App Builder-program](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- Komma igång med App Builder/Developer Console
   - [Komma igång med App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [Förstå projekt och arbetsytor](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] autentiseringsuppgifter

Innan du kan installera ett tillägg som köpts från [!DNL Commerce Marketplace] loggar du in på ditt [!DNL Commerce]-konto och kontrollerar att du har en aktiv åtkomstnyckel. Du kan logga in på ditt [!DNL Commerce]-konto från huvudet på [[!DNL Marketplace]](https://marketplace.magento.com/) eller [Magento.com](https://business.adobe.com/products/magento/magento-commerce.html).

Din åtkomstnyckel är en uppsättning offentliga och privata nycklar som används för att synkronisera din [!DNL Commerce]-installation med ditt [!DNL Commerce]-konto och verifiera dina autentiseringsuppgifter. När ditt konto har synkroniserats måste du ange din privata nyckel varje gång du installerar ett tillägg eller en modul från Commerce Marketplace eller uppgraderar din [!DNL Commerce]-installation.

Du kan skapa flera åtkomstnycklar för olika syften och aktivera eller inaktivera dem efter behov. Du måste dock använda samma åtkomstnyckel som användes för att installera programvaran [!DNL Commerce]. Du kan till exempel inte använda en Magento Open Source-åtkomstnyckel för att uppdatera eller uppgradera Adobe Commerce, eller omvänt. Du kan inte heller använda en åtkomstnyckel som tillhör en annan användare eller en som kommer från ett [delat konto](commerce-account-share.md).

### Skapa en åtkomstnyckel

1. Logga in på ditt [!DNL Commerce]-konto.

1. Välj fliken _[!UICONTROL My Account]_&#x200B;på sidan **[!UICONTROL Marketplace]**.

1. Klicka på nedpilen i det övre högra hörnet bredvid ditt namn och välj **[!UICONTROL My Profile]**.

   ![Din [!DNL Marketplace]-profil](./assets/marketplace-profile.png){width="600"}

1. Klicka på _[!UICONTROL Marketplace]_&#x200B;på fliken&#x200B;_[!UICONTROL My Products]_ under **[!UICONTROL Access Keys]** och gör sedan något av följande:

   - Kontrollera om du redan har en uppsättning nycklar för dina Marketplace-inköp. Du kan skapa flera uppsättningar åtkomstnycklar för olika syften.

   ![Åtkomstnycklar](./assets/access-keys.png){width="600"}

   - Klicka på **[!UICONTROL Create a New Access Key]**. Ange ett namn för det nya nyckelparet och klicka på **[!UICONTROL OK]**. Giltiga tecken är versala och gemena tecken och bindestreck i stället för mellanslag.

1. Klicka på **[!UICONTROL OK]** när du är klar.

   Din nya åtkomstnyckel är aktiverad och visas i listan.

   Lägg märke till länken _Kopiera_ efter varje offentlig och privat nyckel. I nästa steg kommer du att kopiera och klistra in dessa värden för att synkronisera din butik med Commerce Marketplace.

## Installationsprocess

>[!IMPORTANT]
>
>Från och med Adobe Commerce och Magento Open Source 2.4.0 tas webbinstallationsguiden bort och du måste använda kommandoraden för att [installera](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) eller [uppgradera](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) din instans. Detta krav omfattar även [moduler](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) och [tillägg](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

Installationsprocessen för [!DNL Marketplace]-köp skiljer sig åt för _lokala_-installationer av Commerce jämfört med för installationer som finns på [Adobe Cloud-arkitekturen](https://www.adobe.com/commerce/magento/enterprise.html).

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## Support

Om du behöver hjälp med att installera eller använda ett tillägg ska du först titta i dokumentationen som medföljer tillägget. Om du inte hittar svaret på din fråga kan du kontakta utvecklaren direkt med kontaktinformationen i tilläggslistan. Om det du köper på Marketplace inte uppfyller dina behov kan du [begära en återbetalning](#refund-requests) inom 25 dagar från inköpsdatumet. Adobe granskar alla återbetalningsansökningar och (om det godkänns) utfärdar rätt återbetalningsvillkor. För problem relaterade till Commerce Marketplace:

Metod 1: Skicka en supportförfrågan från formuläret [Adobe Commerce Marketplace - kontakta oss](https://commercemarketplace.adobe.com/contact-us/).

Metod 2: [E-postsupport](mailto:commercemarketplacesupport@adobe.com).

### Utcheckningsproblem

Adressfälten i din kontoprofil måste fyllas i för verifieringsändamål i Marketplace-inköpssystemet.

1. Lägg till adressfälten i din Marketplace-kontoprofil.
1. Spara den uppdaterade profilen.
1. Fortsätt med utcheckningen.

### Inloggningsproblem

Inloggningsproblem är vanligtvis relaterade till en felmatchning mellan ditt MAGEID och e-postadressen i kontodatabasen. Kontakta Marketplace Support om du behöver hjälp.

>[!INFO]
>
>Program- och tilläggsköp kan inte [överföras](#purchase-transfers) till ett nytt konto.

### Frågor om öppen källkod

Marketplace Support-teamet löser problem som bara gäller webbplatserna [commercialMarketplace.adobe.com/](https://commercemarketplace.adobe.com/) och [commercialDeveloper.adobe.com/](https://commercedeveloper.adobe.com/) . Du kan ställa frågor om Magento Open Source till [Community-forumet](https://community.magento.com/) eller [kontakta en partner](https://business.adobe.com/products/magento/partners.html) som kan hjälpa till med Magento Open Source.

### Återbetalningsbegäranden

Om du vill få pengarna tillbaka för ett Marketplace-köp loggar du in på ditt konto och följer dessa steg:

1. Klicka på [!UICONTROL **Min profil**] > [!UICONTROL **Inköpshistorik**].
1. Leta upp köpet och klicka på [!UICONTROL **Begär återbetalning**].
1. Fyll i formuläret för återbetalningsorder.

Marketplace Support begär information när återbetalningsbegäran har genererats. Återbetalningsalternativet är tillgängligt i 25 dagar efter inköpsdatum. Se [Marketplace-kundavtalet](https://www.adobe.com/legal/terms/enterprise-licensing/magento-legacy-terms.html).

### Orderfakturor

Du kan hämta orderfakturor från [!UICONTROL **Inköpshistorik**] på ditt Marketplace-konto. Fakturan anger inte säljarens moms eller adress eftersom det för närvarande inte är ett Marketplace-krav.

Om du vill hämta en orderfaktura för ett Marketplace-inköp loggar du in på ditt Marketplace-konto och följer dessa steg:

1. Klicka på [!UICONTROL **Min profil**] > [!UICONTROL **Inköpshistorik**].
1. Hitta köpet.
1. Klicka på skrivarikonen i det övre högra hörnet av ordningen.

### Inköpsöverföringar

Marketplace Support-teamet har inte möjlighet att överföra inköp till ett annat konto. Du måste köpa alla program och tillägg under det primära Commerce-kontot för att undvika installations- och distributionsproblem. Adobe Commerce har rätt till en unik identifierare. Eftersom Composer används för installation kan bara en uppsättning [åtkomstnycklar](#create-an-access-key) som är kopplade till det primära kontot användas. Den enda tillgängliga lösningen är att [begära en återbetalning](#refund-requests) från Marketplace-inköpskontot (om det tillåts enligt Adobe Commerce återbetalningsvillkor).

Du kan [dela](commerce-account-share.md) en Commerce-instans via det primära kontot. Delad åtkomst ger särskilda behörigheter till ett underordnat konto från ett primärt konto. Den delade åtkomstpunkten genereras från det primära kontot. Det primära kontot kan vara Commerce-kontot, huvudhandelskontot eller ett konto som delas inom en organisation.

Dessa särskilda behörigheter ger samma åtkomstnivå på Adobe Commerce som den primära, men överförs inte till Adobe Commerce Marketplace eller Developer Portal. Det innebär att köp av ett tillägg från ett underordnat konto på Marketplace inte kan delas med det primära kontot. Delad åtkomst är en enkelriktad gata (primärt konto för underordnade). Det fungerar inte när ett underordnat konto försöker dela tillbaka till det primära kontot.
