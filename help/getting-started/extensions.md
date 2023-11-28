---
title: Tillägg från Adobe
description: Granska information om tillägg för Adobe Commerce och Magento Open Source som Adobe har släppt.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: c22ad5c3220f14588131d6b29a88dab3c5347681
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 0%

---

# Tillägg från Adobe

Det här avsnittet innehåller information om tillägg för Adobe Commerce och Magento Open Source som släpps av Adobe. Tillägg lägger till funktioner, funktioner, tjänster och integreringar i Admin och storeFront. Vissa av dessa utökningar har utvecklats genom bidrag från Magento Open Source. Vissa tillägg kräver en separat installation och andra installeras som standard.

## Installerade tillägg

Det finns tillägg som installeras automatiskt med Adobe Commerce eller Magento Open Source.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) ger förbättrad hantering av lager och leveranser på en eller flera platser och i försäljningskanaler med samtidigt utcheckningsskydd och algoritmer för leveransmatchning. Spåra era lagerkvantiteter, förse kunderna med korrekta försäljningsbara lagerbelopp och leverera enligt rekommendationer eller manuella val för att kontrollera hela ert lager. Konfigurera hanteringsinställningar globalt, per källa och per produkt.

>[!NOTE]
>
>Utbyggnaden utvecklades som en del av [[!DNL Inventory Management]](https://github.com/magento/inventory) (tidigare MSI-projekt) genom gemenskapens tekniska program.

[!DNL Inventory Management] installeras med alla funktioner aktiverade som standard. Inga ytterligare steg krävs för att aktivera dessa lagerfunktioner. Mer information om [!DNL Inventory Management] funktioner, se [[!DNL Inventory Management] Användarhandbok](../inventory-management/guide-overview.md).

### Braintree

PayPal och Gene Commerce utvecklade tillsammans den officiella Braintree-utbyggnaden för Commerce 2.4.x-butiker. Uppdateringarna har en förbättrad utcheckningsupplevelse som är utformad för att öka konverteringen och innehåller PaySenare-alternativ som automatiskt visar relevanta PayLater-meddelanden och -knappar för konsumenter vid köp och utcheckning.

Tillägget installeras som standard, men kräver en [Braintree](https://www.braintreepayments.com/) och konfigurationen i administratören som ska aktiveras för din butik. Om du vill ta reda på vilka avgifter som gäller när du använder Braintree för att behandla dina transaktioner, ska du kontrollera [Braintree priser](https://www.braintreepayments.com/braintree-pricing).

Mer information om konfigurationen av Braintree i Admin finns i [Braintree](../stores-purchase/braintree.md) ämne i _Experience Guide för försäljning och inköp_.

### Google reCAPTCHA

Google reCAPTCHA ger en högre säkerhetsnivå för både butiken och administratörsgränssnittet än vad som är tillgängligt med vanliga CAPTCHA och ger dig möjlighet att:

- Verifiera när kunderna skapar konton, hämtar lösenord, loggar in på sina konton eller kontaktar företaget.
- Förbättra säkerheten när administratörsanvändare loggar in.

Det minskar eventuella användarfel när du anger en Captcha-kod och uppmuntrar till kundkonvertering utan att skapa hinder vid utcheckning. [Aktivera och konfigurera reCAPTCHA](../systems/security-google-recaptcha.md) med osynliga eller interaktiva kontroller för att ge säker åtkomst till [!DNL Commerce] Admin och storefront.

### Tvåfaktorsautentisering

The [!DNL Commerce] Admin ger all tillgång till din butik, dina beställningar och dina kunddata. [Tvåfaktorsautentisering](../systems/security-two-factor-authentication.md) (2FA eller TFA) förbättrar säkerheten genom att kräva ytterligare autentisering, utöver det vanliga inloggningsnamnet och lösenordet, för att få åtkomst till [!DNL Commerce] Administratör från alla enheter. Tillägget har stöd för flera autentiserare, inklusive Google Authenticator, Authy, [!DNL Duo]och U2F-tangenter. Den här autentiseringen gäller endast för administratörsanvändare. Det är inte tillgängligt för butikskundkonton.

De här funktionerna är aktiverade som standard. Varje Admin-användare måste installera och konfigurera en av de autentiserare som stöds.

>[!NOTE]
>
>Adobe Commerce-butiker som har aktiverat IMS-autentisering (Adobe Identity Management Services) för administratören har inaktiverat inbyggd Commerce 2FA. Användare som är inloggade på Admin med sina inloggningsuppgifter för Adobe behöver inte autentisera igen för många administratörsuppgifter. Autentisering hanteras av Adobe IMS när administratörsanvändaren loggar in på sin aktuella session. Se [Integreringsöversikt för Adobe Identity Management-tjänst (IMS)](./adobe-ims-integration-overview.md).

## Tillägg att lägga till

The [[!DNL Commerce Marketplace]](https://marketplace.magento.com/) är den globala e-handelsresursen för program och tjänster som expanderar [!DNL Commerce] lösningar med kraftfulla nya funktioner. Adobe släpper flera tillägg via [!DNL Marketplace] som kan installeras och konfigureras i din Adobe Commerce- eller Magento Open Source-butik för att ge bättre integrering och funktioner.

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) Endast Adobe Commerce

The [!DNL Live Search] tillägget kopplar din butik till Live Search-tjänsten - en kostnadsfri sökplattform från Adobe Commerce som smidigt ger säljarna möjlighet att erbjuda sina kunder en AI-förbättrad sökupplevelse. Adobe Sensei Intelligent Faceting bygger på artificiell intelligens från Adobe och hjälper handlarna att göra mer med mindre genom att ta bort det manuella arbetet med faceting/filtrering.

Se [Användarhandbok för Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html) för mer information.

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) Endast Adobe Commerce

The [!DNL Product Recommendations] som kopplar butiken till tjänsten Product Recommendations - ett kraftfullt marknadsföringsverktyg som ni kan använda för att öka konverteringarna, intäkterna och engagemanget. [!DNL Product Recommendations] byggdes av Adobe Commerce och drivs av artificiell intelligens som testats i strid, Adobe Sensei, så att ni tryggt kan skapa engagemang och konverteringar. Den här funktionen tar bort det manuella arbete som krävs för att göra relevanta produktrekommendationer till alla kunder.

Se [[!DNL Product Recommendations] Användarhandbok](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html?lang=en) för mer information.

### [!DNL Catalog Service]

The [!DNL Catalog Service] ger er möjlighet att leverera en optimerad produktupplevelse samtidigt som ni ökar prestanda, förbättrar skalbarheten och ökar konverteringsgraden. Se [[!DNL Catalog Service] Användarhandbok](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html) för mer information.

### [!DNL Payment Services]

[!DNL Payment services] för Adobe Commerce och Magento Open Source är en helintegrerad betalningslösning som förenklar betalningsprocessen och ger dina kunder möjlighet att betala på sitt sätt. Samla alla betalnings- och transaktionsdata säkert inom Adobe Commerce Admin - så att ni kan hantera order och betalningar på ett och samma ställe och få en smidig utcheckning. Se [[!DNL Payment Services] Användarhandbok](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html) för mer information.

### [!DNL Quick Checkout]

[!DNL Quick Checkout] för Adobe Commerce ger en smidig utcheckningsupplevelse som utformats för att konvertera engångsköpare till lojala kontoinnehavare.
Se [[!DNL Quick Checkout] Användarhandbok](https://experienceleague.adobe.com/docs/commerce-merchant-services/quick-checkout/overview.html) för mer information.

### [!DNL Store Fulfillment]

Store Fulfillment for Adobe Commerce and Magento Open Source ger en oöverträffad möjlighet att köpa online, plocka upp i butik (BOPIS) och maximerar produktiviteten genom att tillhandahålla ett omfattande arbetsflöde för fullgörande via en mobil enhet. Se [[!DNL Store Fulfillment] Användarhandbok](https://experienceleague.adobe.com/docs/commerce-merchant-services/store-fulfillment/guide-overview.html) för mer information.

### [!DNL Amazon Sales Channel]

The [!DNL Amazon Sales Channel] för Adobe Commerce kan ni integrera er listdatabas i Amazon Seller Central med [!DNL Commerce] produktkatalog och hantera dina Amazon-listor och -försäljningar i Commerce Admin. Se [[!DNL Amazon Sales] Handbok](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html) för mer information.

### [!DNL Channel Manager]

[!DNL Channel Manager] gör att ni kan öka försäljningen, nå nya kunder, effektivisera verksamheten och spara tid genom att integrera en Adobe Commerce- eller Magento Open Source-produktkatalog med Walmart Marketplace. När du har installerat och konfigurerat tillägget kan din personal hantera Walmart Marketplace-listor, lager, beställningar, returer och återbetalningar smidigt från [!DNL Commerce Admin]. Se [[!DNL Channel Manager] Användarhandbok](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html) för mer information.
