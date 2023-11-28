---
title: Integrering med Adobe Identity Management Service (IMS) - översikt
description: Introducerar den valfria integreringen av Adobe Commerce Admin-inloggningar med Adobe IMS
exl-id: 106d731c-a541-4a19-a38c-221e80740508
feature: Identity Management
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# Integrering med Adobe Identity Management Service (IMS) - översikt

{{ee-feature}}

Adobe Commerce Admin-användare som har ett Adobe-konto kan nu använda sin Adobe ID för att logga in på Adobe Commerce. Adobe Identity Management-tjänsten (IMS) är en Adobe OAuth 2.0-baserad identitetshanteringsfunktion som stöder autentisering. Genom att integrera Commerce Admin-autentiseringen i Adobe Business Product autentiseringsarbetsflöde kan autentiseringsprocessen effektiviseras för användare som arbetar med andra Adobe-produkter. Den här integreringen är valfri och aktiveras per instans. Endast arbetsflöden för administrationsanvändare påverkas när den här integreringen är aktiverad. 

Modulerna som krävs för Commerce Admin IMS-integrering paketeras i  `adobe-ims-metapackage`som medföljer Adobe Commerce Core-releaser.

Information om hur du implementerar integreringen finns i [Konfigurera Commerce Admin-integrering med IMS](./adobe-ims-config.md).

## Ändringar i administratörens arbetsflöden och gränssnitt efter integrering med IMS

När den här integreringen är aktiverad, kommer Commerce Admin-användare att uppleva ändringar i standardarbetsflödet för inloggning och autentisering i Commerce Admin när de utför rutinuppgifter i Admin som kräver omautentisering, till exempel skapar en Admin-användare. Tvåfaktorautentisering (2FA) krävs på organisationsnivå i Adobe för modulaktivering. Administratörsinloggningen och 2FA är inaktiverade och _[!UICONTROL Sign In with Adobe ID]_ersätts standardformuläret för administratörsinloggning. Tillstånd hanteras fortfarande från administratören.

## Hur administratörsintegrering med IMS påverkar Commerce-lösenord

Commerce-distributioner som har integrerats med Adobe IMS kräver ett Adobe ID-konto med tillgång till den Adobe IMS-organisation som är konfigurerad för Commerce-programmet under IMS-aktiveringsprocessen.  När IMS-integreringen är aktiverad autentiseras administratörsanvändare via inloggningssidan för Adobe med hjälp av inloggningsuppgifterna för Adobe. Commerce-lösenord och användarnamn för administratörsanvändare används inte längre för autentisering så länge som Adobe IMS-integreringen är aktiverad.

Om IMS-integreringen är inaktiverad måste administratörsanvändare autentisera via Adobe Commerce igen med sitt Commerce-användarnamn och lösenord. Administratörsanvändare bör spara sina inloggningsuppgifter för Commerce Admin (användarnamn och lösenord) och 2FA-autentiseringsuppgifter innan integreringen aktiveras.

Vissa backend-komponenter som är involverade i användarautentisering kräver fortfarande ett lösenord som inte är null. För att uppfylla detta krav skapas slumpmässiga lösenord för nyskapade administratörsanvändare i `admin_user` tabell.

Användarkonton och rollbehörigheter för Commerce-programmet hanteras fortfarande från Commerce Admin.


## Generering av webb-API-token med IMS-referenser

API:er för Commerce Admin påverkas när Admin-autentisering med Adobe IMS är aktiverat i en Commerce-instans. Administratörsanvändare kan inte längre använda de autentiseringsuppgifter som utfärdats av Commerce-instansen. Detta är de autentiseringsuppgifter som krävs för att logga in på Admin och för att få åtkomsttokens som tjänster kan använda för att göra förfrågningar till API:erna Admin REST och SOAP.

När integreringen med Adobe IMS är aktiverad måste administratörsanvändare använda [Adobe IMS OAuth-tokens](https://developer.adobe.com/developer-console/docs/guides/authentication/OAuthIntegration/) för Adobe Commerce API-slutpunkter som kräver autentisering. Klientlösningarna hämtar token dynamiskt för webb-API-användning. Den här autentiseringsmekanismen är aktiverad för REST- och SOAP-webb-API-områden som en del av konfigurationen av den här integreringen.

Se [Tokenbaserad autentisering](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-token/) för en översikt över hur webb-API:er använder Commerce-åtkomsttoken, inklusive IMS-åtkomsttoken.

## Hantering av Commerce-sessioner och Adobe IMS-åtkomsttoken

Åtkomsttoken innehåller både inloggningsuppgifter och inloggningssessionsinformation. När en användare har autentiserats och en session har börjat läggs dessa två variabler till i användarens session:

`token_last_check_time`. Identifierar aktuell tid och används av `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` plugin-program.

`adobe_access_token` — Identifierar `ACCESS_TOKEN` värde som tagits emot under auktoriseringen.

The `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` plugin-programmet kontrollerar om `token_last_check_time` uppdaterades för 10 min sedan. Om `token_last_check_time` kontrollerades för tio minuter sedan, så gör autentiseringsarbetsflödet ett API-anrop till IMS för att validera åtkomsttoken, och sessionen fortsätter. Om åtkomsttoken är giltig, `token_last_check_time` värdet uppdateras till aktuell tid. Om token inte är giltig avslutas sessionen.

## Viktiga filer

`adminAdobeIms` - Tillhandahåller en implementering av Admin-inloggningen baserat på `AdobeImsApi` -modul.

`admin_adobe_ims_webapi` - Upprätthåller en post med alla verifierade åtkomsttoken. När en token valideras eller ogiltigförklaras bevaras en post om dess status i den här tabellen.

`adobeIms` - Implementerar all affärslogik som är relaterad till integrationen med Adobe IMS (bevaras för att förhindra bakåtkompabilitet).

`adobeImsApi` - Deklarerar de gränssnitt som stöder integrering med Adobe IMS.

`adminadobe-ims.log` - Felloggfil.

## Aktivera integreringen

Adobe IMS-metapaketet installeras med Adobe Commerce 2.4.5 eller senare, men måste konfigureras för användning. Den utökar `AdobeIms` som stöder modulen som aktiverar autentiseringslogik (`AdminAdobeIms`).

Mer information om hur du aktiverar integreringen finns i [Konfigurera Commerce Admin-integrering med Adobe IMS](./adobe-ims-config.md).
