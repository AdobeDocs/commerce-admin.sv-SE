---
title: Tillägg från Adobe
description: Granska information om tillägg för Adobe Commerce och Magento Open Source som släpps av Adobe.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: e37ca150c72bb46066690524a35de52d6db6d56a
workflow-type: tm+mt
source-wordcount: '1326'
ht-degree: 0%

---

# Tillägg från Adobe

Det här avsnittet innehåller information om PHP-tillägg för Adobe Commerce och Magento Open Source som släpps av Adobe.

Tillägg lägger till funktioner, funktioner, tjänster och integreringar i Admin och storeFront. Vissa av dessa utökningar har utvecklats genom bidrag från Magento Open Source Community. Vissa tillägg installeras som standard och andra kräver separat installation.

+++Läs mer om hur du utökar Adobe Commerce

Adobe erbjuder två huvudstrategier för att utöka eller anpassa dina Adobe Commerce-projekt:

- Pågående utökningsmöjligheter: Använder anpassad kod och tillägg som körs i Adobe Commerce-programprocessen, till exempel PHP-tillägg. Detta traditionella tillvägagångssätt tillåter djup integrering men kräver noggrann hantering vid uppgraderingar.

- Utbyggbar utanför processen: Använder anpassad kod och program som fungerar oberoende av huvudprogramvaran. Detta moderna tillvägagångssätt hjälper till att minska den totala ägandekostnaden genom att:

   - Förenkla uppgraderingar eftersom tilläggen inte hänger ihop med kärnan
   - Ge utvecklarna bättre kontroll över implementeringstidpunkter och -metoder
   - Aktivera oberoende skalning och underhåll av tilläggskomponenter

Adobe Commerce erbjuder strategier och verktyg som stöder båda typerna av utbyggbarhet. Mer information finns i [Utbyggbarhet för Adobe Commerce](https://developer.adobe.com/commerce/extensibility/).

+++

## Adobe-tillägg som installeras som standard

Följande Adobe-tillägg ingår i Adobe Commerce och installeras automatiskt med Adobe Commerce-programmet. Vissa tillägg kräver ytterligare konfiguration eller aktivering i Admin, vilket beskrivs i tilläggsbeskrivningen.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) erbjuder förbättrad hantering av lager och leveranser på en eller flera platser och i försäljningskanaler med samtidigt utcheckningsskydd och leveransmatchningsalgoritmer. Spåra era lagerkvantiteter, förse kunderna med korrekta försäljningsbara lagerbelopp och leverera enligt rekommendationer eller manuella val för att kontrollera hela ert lager. Konfigurera hanteringsinställningar globalt, per källa och per produkt.

>[!NOTE]
>
>Det här tillägget utvecklades som en del av [[!DNL Inventory Management]](https://github.com/magento/inventory)-projektet (tidigare MSI) via gemenskapens tekniska program.

[!DNL Inventory Management] installeras med alla funktioner aktiverade som standard. Inga ytterligare steg krävs för att aktivera dessa lagerfunktioner. Mer information om funktionerna i [!DNL Inventory Management] finns i [[!DNL Inventory Management] användarhandboken](../inventory-management/guide-overview.md).

### Braintree

PayPal och Gene Commerce har tillsammans utvecklat Braintree-tillägget för Commerce 2.4.x-butiker. Uppdateringarna har en förbättrad utcheckningsupplevelse som är utformad för att öka konverteringen och innehåller PaySenare-alternativ som automatiskt visar relevanta PayLater-meddelanden och -knappar för konsumenter vid köp och utcheckning.

Tillägget är installerat som standard, men kräver att ett [Braintree-konto](https://www.braintreepayments.com/) och en konfiguration i administratören är aktiverad för din butik. Kontrollera [Braintree-priset](https://www.braintreepayments.com/braintree-pricing) för att fastställa vilka avgifter som gäller när du använder Braintree för att bearbeta dina transaktioner.

Mer information om Braintree-konfigurationen i Admin finns i avsnittet [Braintree](../stores-purchase/braintree.md) i _Handboken för försäljnings- och inköpsupplevelser_.

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
>Adobe Commerce-butiker som har aktiverat Adobe Identity Management Services (IMS)-autentisering för administratören har inaktiverat Commerce 2FA. Användare som är inloggade på Admin med sina Adobe-inloggningsuppgifter behöver inte autentisera igen för många administratörsuppgifter. Autentisering hanteras av Adobe IMS när administratörsanvändaren loggar in på sin aktuella session. Se [Integreringsöversikt för Adobe Identity Management-tjänst (IMS)](./adobe-ims-integration-overview.md).

## Adobe-tillägg som kräver installation

Adobe erbjuder ytterligare tillägg som måste installeras separat med Composer. Dessa tillägg är tillgängliga via olika kanaler:

- Databasåtkomst (repo.magento.com)

  Följande tillägg kräver kontoetablering och autentiseringsuppgifter för att kunna installeras. Kontakta din Adobe-kontorepresentant om du behöver hjälp.

   - [Adobe Commerce B2B](#adobe-commerce-b2b)
   - [AEM Assets Integration för Commerce](#assets-integration-for-commerce)

- Adobe Commerce Marketplace

  Följande Adobe-tillägg är tillgängliga för allmänheten på [marketplace.magento.com](https://marketplace.magento.com). Dessa tillägg är tillgängliga utan extra kostnad.

   - [Live Search](#live-search)
   - [Produktrekommendationer](#product-recommendations)
   - [Katalogtjänst](#catalog-service)
   - [Betalningstjänster](#payment-services)

### [!DNL Adobe Commerce B2B]

![Endast Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce, kräver en separat licens.

[!DNL Adobe Commerce B2B] är ett integrerat tillägg som omvandlar vanliga Commerce-butiker till heltäckande affärs-till-företag-plattformar. Det gör det möjligt för företag att hantera komplexa organisationsstrukturer med flera köpare, anpassade roller och inköpsbehörigheter under enhetliga företagskonton. Viktiga funktioner är bland annat företagsspecifika kataloger och priser, överlåtbara offerter, hantering av inköpsorder, rekvisitionslistor och funktioner för snabb beställning. Lösningen har stöd för både B2B- och B2C-modeller i ett och samma fall, vilket gör den flexibel för olika affärsbehov. Tillägget kräver en separat licens och är sömlöst integrerat med Adobe Commerce kärnfunktioner för att ge en komplett e-handelslösning för B2B.

Kontakta din Adobe-kontorepresentant för att få hjälp med etableringen. Implementeringsinformation och konfigurationssteg finns i [[!DNL B2B for Adobe Commerce] användarhandboken](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=sv-SE).

### [!DNL AEM Assets Integration for Commerce]

![Endast Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce, kräver även licenser för Adobe Experience Manager (AEM) Assets och AEM Dynamic Media.

[!DNL AEM Assets Integration for Commerce] ansluter Adobe Commerce till Adobe Experience Manager Digital Asset Management-system (DAM) för att ge centraliserad kontroll över alla digitala resurser. Integreringen möjliggör automatisk resurssynkronisering, uppdateringar i realtid och effektiv återanvändning av innehåll i alla e-handelslager. Genom att kombinera AEM robusta resurshanteringsfunktioner med Commerce kan företag dra nytta av effektiva arbetsflöden, enhetliga varumärkesupplevelser och optimerad mediedistribution via molnbaserad infrastruktur.

Kontakta din Adobe-kontorepresentant för att få hjälp med etableringen. Implementeringsinformation och konfigurationssteg finns i [[!DNL Assets Integration] användarhandboken](../content-design/aem-assets-integration.md).

### [!DNL Live Search]

![Endast Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce

Live Search är en Adobe Commerce-exklusiv funktion som ger en AI-baserad söklösning med sökfunktioner i realtid. Det ger snabba, relevanta resultat med produktminiatyrer samtidigt som kunderna skriver, tillsammans med intelligent ansikteshantering som automatiskt justerar filter baserat på köpbeteende. Lösningen innehåller säljfunktioner för produktförstärkning och -nedladdning, synonymhantering och sökanalys. [!DNL Live Search] ingår utan extra kostnad i Adobe Commerce och ersätter standardsökfunktionen med en mer avancerad SaaS-baserad sökfunktion. Den kräver minimal konfiguration för att komma igång.

Implementeringsinformation och tekniska krav finns i [Live Search-användarhandboken](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=sv-SE).

### [!DNL Product Recommendations]

![Endast Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce

[!DNL Product Recommendations] är en Adobe Commerce-exklusiv funktion som drivs av Adobe Sensei AI-teknik som ger skräddarsydda produktförslag under kundens hela kundresa. Lösningen analyserar kundernas beteende och produktrelationer i realtid för att automatiskt generera relevanta rekommendationer, vilket kräver att det inte finns några manuella försäljningsregler. Detta AI-drivna tillvägagångssätt hjälper till att öka konverteringsgraden och intäktspotentialen samtidigt som man skapar mer engagerande produktupptäckt för kunderna.

Implementeringsinformation och bästa praxis finns i [[!DNL Product Recommendations] användarhandboken](https://experienceleague.adobe.com/docs/commerce/product-recommendations/overview.html?lang=sv-SE).

### [!DNL Catalog Service]

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

[!DNL Catalog Service] är en högpresterande lösning för Adobe Commerce och Magento Open Source som ger optimerad åtkomst till katalogdata via GraphQL slutpunkter. Den har en separat synkroniserad databas med produktinformation och relaterad information, och slipper direkt kommunikation för att ge snabbare sidinläsning. Tjänsten är särskilt värdefull för produktinformationssidor, kategorilistor och sökresultatsidor, vilket gör den idealisk för både traditionella och headless-handelsimplementationer.

Instruktioner och teknisk information finns i [[!DNL Catalog Service] användarhandboken](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html?lang=sv-SE).

>[!NOTE]
>
>Katalogtjänster installeras automatiskt när Live Search eller Produktrekommendationer är aktiverade. Manuell installation krävs inte.

### [!DNL Payment Services]

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

[!DNL Payment Services] är en nyckelfärdig betalningslösning för Adobe Commerce- och Magento Open Source-butiker som erbjuder omfattande funktioner för betalningshantering. Tjänsten integrerar en säker betalningstjänstfunktion med inbyggt skydd mot bedrägeri, samtidigt som den erbjuder flera betalningsalternativ, inklusive kredit-/betalkort, PayPal-, Venmo- (US) och PayLater-planer. Den har enhetlig transaktionsrapportering och orderhantering via Commerce Admin-gränssnittet, vilket gör det enkelt för handlarna att spåra betalningar, hantera kassaflöden och stämma av ekonomiska data på ett och samma ställe.

Detaljerade konfigurationssteg och betalningsalternativ finns i [[!DNL Payment Services] användarhandboken](https://experienceleague.adobe.com/sv/docs/commerce/payment-services/overview).
