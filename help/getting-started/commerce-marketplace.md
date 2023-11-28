---
title: '[!DNL Adobe Commerce Marketplace]'
description: Läs mer om [!DNL Commerce Marketplace], som erbjuder handlare ett välstrukturerat urval av lösningar och ger kvalificerade utvecklare de verktyg, den plattform och den plats där de ska arbeta för att skapa ett livskraftigt företag.
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 1a5a00493e9994343c7decc763f2decdd11192c7
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 0%

---

# Adobe Commerce Marketplace

[Adobe Commerce Marketplace][1] är den applikationsbutik som erbjuder handlare ett välstrukturerat urval av lösningar och ger kvalificerade utvecklare de verktyg, den plattform och den plats där de bäst kan bygga upp ett livskraftigt företag. [!DNL Commerce Marketplace] erbjuder ett urval tillägg som är tillgängliga utan kostnad och andra som är till salu. Inköp kan betalas med kreditkort eller [PayPal][2].

Alla tillägg är tillgängliga på [!DNL Commerce Marketplace] har gått igenom en omfattande granskning. The [Tilläggskvalitetsprogram][3] (EQP) kombinerar [!DNL Commerce] expertis, riktlinjer för utveckling och kontrollverktyg för att säkerställa att alla tillägg på Commerce Marketplace uppfyller kodningsstandarder och bästa praxis. Granskningsprocessen innefattar både en automatiserad kontroll och en manuell QA-granskning. Under processen undersöks och testas strukturen och koden för varje förlängning för tecken på virus-/virusinfektion och eventuella tecken på plagiarism. Översynen innehåller en djupgående teknisk undersökning och en hygienkontroll som utförs av en [!DNL Commerce] -tekniker, med fokus på dokumentation, kodningsstruktur, prestanda, skalbarhet, säkerhet och kompatibilitet med [!DNL Commerce] kärna.

Även om du kan köpa tillägg från andra källor är det bara de tillägg som är tillgängliga på [!DNL Commerce Marketplace] verifieras genom omfattande tekniska granskningar och marknadsföringsgranskningar inom Extension Quality Program.

## Appresurser

Utvecklare har traditionellt använt PHP för att skapa tillägg i processen som lägger till funktioner, funktioner, tjänster och integreringar i Adobe Commerce. Genom att skapa program med utbyggbarhet som inte har bearbetats, i motsats till tillägg, kan du undvika kompatibilitetsproblem.

Följande resurser är en startpunkt för nya användare som vill bekanta sig med appar:

### Handelsresurser:

- [Konfigurera I/O-händelser för Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/)
- [Konfigurera händelser för Adobe Commerce](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [Konfigurera administratörens användargränssnitts-SDK](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [Konvertera ett tillägg till en app](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### App Builder-resurser:

- [Översikt över Commerce App Builder](https://developer.adobe.com/commerce/extensibility/app-development/)
- [Konfigurera API Mesh för Adobe Developer App Builder](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [Distribuera App Builder-appar](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [CI/CD för App Builder-appar](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- Komma igång med App Builder/Developer Console
   - [Komma igång med App Builder](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [Förstå projekt och arbetsytor](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] autentiseringsuppgifter

Innan du kan installera ett tillägg som du köpt från [!DNL Commerce Marketplace], logga in på [!DNL Commerce] och verifiera att du har en aktiv åtkomstnyckel. Du kan logga in på [!DNL Commerce] konto från huvudet på [[!DNL Marketplace]][1] eller [Magento.com][6].

Din åtkomstnyckel är en uppsättning offentliga och privata nycklar som används för att synkronisera dina [!DNL Commerce] installera med [!DNL Commerce] och verifiera dina uppgifter. När ditt konto har synkroniserats måste du ange din privata nyckel varje gång du installerar ett tillägg eller en modul från Commerce Marketplace eller uppgraderar din [!DNL Commerce] installation.

Du kan skapa flera åtkomstnycklar för olika syften och aktivera eller inaktivera dem efter behov. Du måste dock använda samma åtkomstnyckel som användes för att installera [!DNL Commerce] program. Du kan till exempel inte använda en Magento Open Source-åtkomstnyckel för att uppdatera eller uppgradera Adobe Commerce, eller omvänt. Du kan inte heller använda en åtkomstnyckel som tillhör en annan användare eller en som kommer från en [delat konto](commerce-account-share.md).

### Skapa en åtkomstnyckel

1. Logga in på [!DNL Commerce] konto.

1. På _[!UICONTROL My Account]_väljer du **[!UICONTROL Marketplace]**-fliken.

1. Klicka på nedpilen i det övre högra hörnet bredvid ditt namn och välj **[!UICONTROL My Profile]**.

   ![Dina [!DNL Marketplace] profil](./assets/marketplace-profile.png){width="600"}

1. På _[!UICONTROL Marketplace]_flik under_[!UICONTROL My Products]_, klicka **[!UICONTROL Access Keys]** och gör sedan något av följande:

   - Kontrollera om du redan har en uppsättning nycklar för dina Marketplace-inköp. Du kan skapa flera uppsättningar åtkomstnycklar för olika syften.

   ![Åtkomsttangenter](./assets/access-keys.png){width="600"}

   - Klicka på **[!UICONTROL Create a New Access Key]**. Ange ett namn för det nya nyckelparet och klicka på **[!UICONTROL OK]**. Giltiga tecken är versala och gemena tecken och bindestreck i stället för mellanslag.

1. När du är klar klickar du på **[!UICONTROL OK]**.

   Din nya åtkomstnyckel är aktiverad och visas i listan.

   Lägg märke till _Kopiera_ efter varje offentlig och privat nyckel. I nästa steg kommer du att kopiera och klistra in dessa värden för att synkronisera din butik med Commerce Marketplace.

## Installationsprocess

>[!IMPORTANT]
>
>Från och med Adobe Commerce och Magento Open Source 2.4.0 tas guiden Konfigurera webben bort och du måste använda kommandoraden för att [installera](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) eller [uppgradera](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) din instans. Detta krav omfattar även [moduler](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) och [tillägg](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

Installationsprocessen för [!DNL Marketplace] köp skiljer sig åt för _lokal_ installationer av Commerce än för installationer som ligger på [Adobe Cloud-arkitekturen][4].

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## Support

Om du behöver hjälp med att installera eller använda ett tillägg ska du först titta i dokumentationen som medföljer tillägget. Om du inte hittar svaret på din fråga kan du kontakta utvecklaren direkt med kontaktinformationen i tilläggslistan.

Om det du köper på Commerce Marketplace inte uppfyller dina behov kan du begära en återbetalning inom 25 dagar från inköpsdatumet. Adobe granskar alla ansökningar om återbetalning och utfärdar, om det godkänns, rätt återbetalning.

Information om supportfrågor som rör Commerce Marketplace finns i [[!DNL Marketplace] Help Center][5].

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[5]: https://marketplacesupport.magento.com/hc/en-us
[6]: https://business.adobe.com/products/magento/magento-commerce.html
