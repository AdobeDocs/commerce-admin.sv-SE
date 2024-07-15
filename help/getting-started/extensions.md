---
title: Tillägg från Adobe
description: Granska information om tillägg för Adobe Commerce och Magento Open Source som Adobe har släppt.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: 6414a7aea7dcbe0f2379ed74455518220a1fbd64
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 0%

---

# Tillägg från Adobe

Det här avsnittet innehåller information om tillägg för Adobe Commerce och Magento Open Source som släpps av Adobe. Tillägg lägger till funktioner, funktioner, tjänster och integreringar i Admin och storeFront. Vissa av dessa utökningar har utvecklats genom bidrag från Magento Open Source. Vissa tillägg kräver en separat installation och andra installeras som standard.

## Installerade tillägg

Det finns tillägg som installeras automatiskt med Adobe Commerce eller Magento Open Source.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) erbjuder förbättrad hantering av lager och leveranser på en eller flera platser och i försäljningskanaler med samtidigt utcheckningsskydd och leveransmatchningsalgoritmer. Spåra era lagerkvantiteter, förse kunderna med korrekta försäljningsbara lagerbelopp och leverera enligt rekommendationer eller manuella val för att kontrollera hela ert lager. Konfigurera hanteringsinställningar globalt, per källa och per produkt.

>[!NOTE]
>
>Det här tillägget utvecklades som en del av [[!DNL Inventory Management]](https://github.com/magento/inventory)-projektet (tidigare MSI) via gemenskapens tekniska program.

[!DNL Inventory Management] installeras med alla funktioner aktiverade som standard. Inga ytterligare steg krävs för att aktivera dessa lagerfunktioner. Mer information om funktionerna i [!DNL Inventory Management] finns i [[!DNL Inventory Management] användarhandboken](../inventory-management/guide-overview.md).

### Braintree

PayPal och Gene Commerce har tillsammans utvecklat det officiella Braintree-tillägget för Commerce 2.4.x-butiker. Uppdateringarna har en förbättrad utcheckningsupplevelse som är utformad för att öka konverteringen och innehåller PaySenare-alternativ som automatiskt visar relevanta PayLater-meddelanden och -knappar för konsumenter vid köp och utcheckning.

Tillägget är installerat som standard, men kräver att ett [Braintree-konto](https://www.braintreepayments.com/) och en konfiguration i Admin är aktiverad för din butik. Kontrollera [Braintree-priset](https://www.braintreepayments.com/braintree-pricing) om du vill fastställa vilka avgifter som gäller när du använder Braintree för att bearbeta dina transaktioner.

Mer information om konfigurationen av Braintree i Admin finns i avsnittet [Braintree](../stores-purchase/braintree.md) i _Handboken för försäljnings- och inköpsupplevelser_.

### Google reCAPTCHA

Google reCAPTCHA ger en högre säkerhetsnivå för både butiken och administratörsgränssnittet än vad som är tillgängligt med vanliga CAPTCHA och ger dig möjlighet att:

- Verifiera när kunderna skapar konton, hämtar lösenord, loggar in på sina konton eller kontaktar företaget.
- Förbättra säkerheten när administratörsanvändare loggar in.

Det minskar eventuella användarfel när du anger en Captcha-kod och uppmuntrar till kundkonvertering utan att skapa hinder vid utcheckning. [Aktivera och konfigurera reCAPTCHA](../systems/security-google-recaptcha.md) med osynliga eller interaktiva kontroller för att förbättra säker åtkomst till [!DNL Commerce] Admin och storefront.

### Tvåfaktorsautentisering

Administratören [!DNL Commerce] ger all åtkomst till din butik, dina beställningar och dina kunddata. [Tvåfaktorautentisering](../systems/security-two-factor-authentication.md) (2FA eller TFA) förbättrar säkerheten genom att kräva ytterligare autentisering, utöver standardinloggningsnamnet och -lösenordet, för att komma åt [!DNL Commerce]-administratören från alla enheter. Tillägget har stöd för flera autentiserare, inklusive Google Authenticator-, Authy-, [!DNL Duo]- och U2F-nycklar. Den här autentiseringen gäller endast för administratörsanvändare. Det är inte tillgängligt för butikskundkonton.

De här funktionerna är aktiverade som standard. Varje Admin-användare måste installera och konfigurera en av de autentiserare som stöds.

>[!NOTE]
>
>Adobe Commerce-butiker som har aktiverat IMS-autentisering (Adobe Identity Management Services) för administratören har inaktiverat Commerce 2FA. Användare som är inloggade på Admin med sina inloggningsuppgifter för Adobe behöver inte autentisera igen för många administratörsuppgifter. Autentisering hanteras av Adobe IMS när administratörsanvändaren loggar in på sin aktuella session. Se [Integreringsöversikt för Adobe Identity Management-tjänsten (IMS)](./adobe-ims-integration-overview.md).

## Tillägg att lägga till

[[!DNL Commerce Marketplace]](https://marketplace.magento.com/) är den globala e-handelsresursen för program och tjänster som utökar [!DNL Commerce]-lösningar med kraftfulla nya funktioner. Adobe släpper flera tillägg via [!DNL Marketplace] som kan installeras och konfigureras i din Adobe Commerce- eller Magento Open Source-butik för att tillhandahålla förbättrade integreringar och funktioner.

### [!DNL Live Search]

![Endast Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce

Tillägget [!DNL Live Search] kopplar din butik till Live Search-tjänsten, en kostnadsfri sökplattform från Adobe Commerce som sömlöst ger säljarna möjlighet att ge kunderna en AI-förbättrad sökupplevelse. Adobe Sensei Intelligent Faceting bygger på artificiell intelligens från Adobe och hjälper handlarna att göra mer med mindre genom att ta bort det manuella arbetet med faceting/filtrering.

Mer information finns i [Live Search-användarhandboken](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html).

### [!DNL Product Recommendations]

![Endast Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce

Tillägget [!DNL Product Recommendations] kopplar din butik till tjänsten Product Recommendations - ett kraftfullt marknadsföringsverktyg som du kan använda för att öka konverteringar, intäkter och engagemang. [!DNL Product Recommendations] har byggts av Adobe Commerce och drivs av den artificiella intelligensen som har testats i striden, Adobe Sensei, så att du tryggt kan skapa engagemang och konverteringar. Den här funktionen tar bort det manuella arbete som krävs för att göra relevanta produktrekommendationer till alla kunder.

Mer information finns i [[!DNL Product Recommendations] användarhandboken](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html?lang=en).

### [!DNL Catalog Service]

Med [!DNL Catalog Service] kan du ge kunderna en optimerad produktupplevelse samtidigt som du ökar prestanda, förbättrar skalbarheten och ökar konverteringsgraden. Mer information finns i [[!DNL Catalog Service] användarhandboken](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html).

### [!DNL Payment Services]

[!DNL Payment services] för Adobe Commerce och Magento Open Source är en helintegrerad betalningslösning som förenklar processen att hantera betalningar och ger dina kunder möjlighet att betala på sitt sätt. Samla alla betalnings- och transaktionsdata säkert inom Adobe Commerce Admin - så att ni kan hantera order och betalningar på ett och samma ställe och få en smidig utcheckning. Mer information finns i [[!DNL Payment Services] användarhandboken](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

### [!DNL Store Fulfillment]

Store Fulfillment for Adobe Commerce and Magento Open Source ger en oöverträffad möjlighet att köpa online, plocka upp i butik (BOPIS) och maximerar produktiviteten genom att tillhandahålla ett omfattande arbetsflöde för fullgörande via en mobil enhet. Mer information finns i [[!DNL Store Fulfillment] användarhandboken](https://experienceleague.adobe.com/docs/commerce-merchant-services/store-fulfillment/guide-overview.html).

### [!DNL Amazon Sales Channel]

Med [!DNL Amazon Sales Channel] för Adobe Commerce kan du integrera listdatabasen för Amazon Seller Central med din [!DNL Commerce]-produktkatalog och hantera Amazon listor och försäljning i Commerce Admin. Mer information finns i [[!DNL Amazon Sales] användarhandboken för handboken](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html).

### [!DNL Channel Manager]

Med [!DNL Channel Manager] kan du öka försäljningen, nå nya kunder, effektivisera verksamheten och spara tid genom att integrera en produktkatalog för Adobe Commerce eller Magento Open Source med Walmart Marketplace. När du har installerat och konfigurerat tillägget kan din personal hantera Walmart Marketplace-listor, lager, order, returer och återbetalningar sömlöst från [!DNL Commerce Admin]. Mer information finns i [[!DNL Channel Manager] användarhandboken](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html).
