---
title: '''[!DNL Adobe Commerce B2B] versionsinformation'
description: Läs versionsinformationen för information om ändringar i [!DNL Adobe Commerce B2B] releaser.
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: 35402eda770e59cc2862b204e6e54b55190ded13
workflow-type: tm+mt
source-wordcount: '6867'
ht-degree: 0%

---

# [!DNL Adobe Commerce B2B] versionsinformation

Versionsinformationen för B2B-tillägget innehåller tillägg och korrigeringar som Adobe har lagt till under en releasecykel, inklusive:

![Nytt](../assets/new.svg) Nya funktioner
![Korrigerat problem](../assets/fix.svg) Korrigeringar och förbättringar
![Känt fel](../assets/bug.svg) Kända fel

>[!NOTE]
>
>Se [Produkttillgänglighet](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) om du vill ha information om vilka versioner av B2B Commerce-tillägget som stöds för tillgängliga Adobe Commerce-utgåvor.

## B2B 1.5.0 beta

{{$include /help/_includes/b2b-beta-note.md}}

*13 november 2023*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

Betaversionen av B2B v1.5.0 innehåller nya funktioner, kvalitetsförbättringar och felkorrigeringar.

![Nytt](../assets/new.svg) Förbättrade offertfunktioner hjälper köpare och säljare att hantera offerter och offertförhandlingar mer effektivt.

- **Spara offert som utkast**<!--B2B-2566-->—När en [anbudsförfrågan](quote-request.md) från kundvagnen kan köpare nu spara offerten som ett utkast genom att välja **[!UICONTROL Save as Draft]** på [!UICONTROL Request a Quote] formulär.

  Utkastofferten har inget förfallodatum. Köpare kan granska och uppdatera offerter från [!UICONTROL My Quotes] i kontokontrollpanelen.

- **Byt namn på citat**<!--B2B-2596-->—Köpare kan nu ändra ett offertnamn från [Offertdetalj](account-dashboard-my-quotes.md#quote-actions) sida genom att välja **[!UICONTROL Rename]** alternativ. Det här alternativet är tillgängligt för auktoriserade köpare när de redigerar offerten. Namnändringshändelser registreras i offerthändelseloggen.

- **Duplicera citat**<!--B2B-2701-->—Köpare och säljare kan nu skapa en ny offert genom att kopiera en befintlig offert. En kopia skapas från offertdetaljvyn genom att välja  **[!UICONTROL Create Copy]** på [Offertdetaljvy](quote-price-negotiation.md#button-bar) i Admin eller [Storefront](account-dashboard-my-quotes.md#quote-actions).

- **Låsning av radrabatt**<!--B2B-2597-->- Vid offertförhandling kan säljarna använda rabattlåsning för att få större flexibilitet när de tillämpar rabatter. En säljare kan till exempel tillämpa en särskild artikelrabatt på en artikel och låsa artikeln för att förhindra ytterligare rabatter. När en artikel är låst kan artikelpriset inte uppdateras när en rabatt på offertnivå används. Se [Initiera offert för en köpare](sales-rep-initiates-quote.md).

![Nytt ](../assets/new.svg)**Företagshantering**<!--B2B-2901-->—Merchants kan nu visa och hantera Adobe Commerce-företag som hierarkiska organisationer genom att tilldela företag till utsedda moderbolag. När ett företag har tilldelats en överordnad kan administratören för det överordnade företaget hantera företagskontot. Endast behöriga administratörsanvändare kan lägga till och hantera företagstilldelningar. Mer information finns i [Hantera företagshierarki](assign-companies.md).

- På företagssidan finns en ny **[!UICONTROL Company Type]** identifierar överordnade och underordnade företag. Handlare kan filtrera företagsvyn efter företagstyp och hantera företag med hjälp av radartikel eller gruppåtgärder.

- Handlare kan lägga till och hantera företagstilldelningar från den nya **[!UICONTROL Company Hierarchy]** i [!UICONTROL Company Account] sida.

- API-utvecklare kan använda den nya REST API-slutpunkten för företagsrelationer `/V1/company/{parentId}/relations` för att skapa, visa och ta bort företagstilldelningar. Se [Hantera företagsobjekt](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) i *Utvecklarhandbok för webb-API*.

![Korrigerat problem](../assets/fix.svg)<!--ACP2E-1984-->Handlare som klickar på **[!UICONTROL Print]** i offertdetaljvyn i Admin uppmanas nu att spara offerten som PDF. Tidigare omdirigerades handlarna till en sida med offertinformation.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1742-->Tidigare när en kundoffert med 0 procent och en ändring av kvantitet skickades ett undantag, men kvantiteten sparades. När den här korrigeringen gäller för `0 percentage` ett riktigt undantag med ett meddelande genereras.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1742-->Under offertförhandlingen kan säljaren nu ange en `0%` rabatt i fältet Förhandlad offertrabatt och skicka offerten tillbaka till köparen. Om säljaren tidigare angav en rabatt på 0 % och skickade offerten tillbaka till köparen returnerade administratören en `Exception occurred during quote sending` felmeddelande.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-2097-->ReCaptcha-validering fungerar nu korrekt under utcheckningsprocessen för ett B2B-citat när ReCaptcha V3 har konfigurerats för utcheckning i butiken. Tidigare misslyckades valideringen med en `recaptcha validation failed, please try again` felmeddelande.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1825-->Inköpsorder kan inte längre placeras av en användare som är associerad med företaget efter att företaget har spärrats. Tidigare kunde en användare som är associerad med företaget göra inköpsorder när företaget blockerades.

![Korrigerat problem](../assets/fix.svg)<!--ACP2E-1933-->Företagsadministratörer kan nu lägga till företagsanvändare från butiken. Tidigare loggade Commerce ett fel när en Admin-användare försökte lägga till en ny användare: `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`.

## B2B v1.4.2-p1

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg) Kompatibilitet med säkerhetsuppdateringar för Adobe Commerce 2.4.7-p1+ och 2.4.6-p6+ har lagts till.


## B2B v1.4.2

*10 oktober 2023*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

B2B v1.4.2-versionen innehåller kvalitetsförbättringar och felkorrigeringar

![Korrigerat problem](../assets/fix.svg) <!--B2B-2897-->Om en säljare skapar en köpoffert som innehåller en produkt-SKU som inte är tillgänglig i den delade katalogen som är associerad med köpföretaget visas felmeddelandet `The SKU you entered is not available in the shared catalog. Please check the SKU and try again`.  Säljaren kan inte spara offerten förrän han eller hon tar bort den produkt som inte är tillgänglig. Tidigare sparades offerten med en SKU som inte var tillgänglig och det gick inte att läsa in offerten i butiken.

## B2B v1.4.1

*7 augusti 2023*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}[Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Kompatibel med Adobe Commerce 2.4.7-beta1.

B2B v1.4.1-versionen innehåller kvalitetsförbättringar och felkorrigeringar.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1825-->Inköpsorder kan inte längre placeras av en användare som är associerad med företaget efter att företaget har spärrats. Tidigare kunde en användare som är associerad med företaget göra inköpsorder när företaget blockerades.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1943-->Status för restorder av produkter visas nu korrekt i butiken. Tidigare identifierades produkter som var tillgängliga för leverans felaktigt som beställda.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1862-->Om företagsregistreringsformuläret innehåller ett attribut för kundfiltyp, inkluderas filen som överfördes under registreringsprocessen nu i företagsadministratörens kontoinformation när företaget har skapats. Tidigare saknades den bifogade filen.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1793-->Färgväljaren för en konfigurerbar produkt visas nu som förväntat på konfigurationssidan för rekvisitionslistobjekt. Tidigare visades väljaren för färgrutor som ett listrutefält på konfigurationssidan för rekvisitionslistobjekt.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1968-->När du använder [GraphQL-fråga](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) om du vill returnera företagsinformation returneras resultaten nu utan fel.

## B2B v1.4.0

*13 juni 2023*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}[Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Kompatibel med Adobe Commerce 2.4.7-beta1

Den här versionen innehåller nya funktioner och förbättringar för B2B-överlåtbara offerter och flera felkorrigeringar.

![Nytt](../assets/new.svg) Kompatibilitet med Adobe Commerce 2.4.7-beta1 har lagts till.

![Nytt](../assets/new.svg) **Försäljarens initierade offerter**—Säljare kan nu initiera en offert för en köpare direkt från rastret Offert och Kund i Admin. Detta effektiviserar offertprocessen och minskar kundens komplexitet. Om en kund inte har initierat en order kan en säljare snabbt skapa en offert för kundens räkning och påbörja förhandlingsprocessen. Tidigare gick det endast att skapa offerter från butiken av köparen eller av en säljare som är inloggad som kund.

![Nytt](../assets/new.svg) **Rabatter och förhandling för radartiklar**—<!--B2B-2440--> Inom en offert kan B2B-köpare och säljare nu förhandla på radobjektsnivå och tillämpa rabatter och utbyta noteringar tills ett avtal nås. Kommentarer som skapas och uppdateras inkluderas i radobjektet och offerthistoriken för att spåra kommunikationen. Tidigare kunde köpare och säljare bara växla noteringar och tillämpa rabatter på offertnivån.

![Korrigerat problem](../assets/fix.svg) Adobe Commerce visar nu korrekt information under betalningen när alternativet Inköpsorder är aktiverat och en virtuell offert som skapades med betalningsalternativet PayPal har valts. Tidigare visades summorna som noll under dessa villkor.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1504--> Valideringsfel uppstår inte längre när du försöker spara ett företag med en kreditgräns som överstiger 999. Tidigare infogades en kommaavgränsare för företagskreditgränser som var större än 999, vilket orsakade ett valideringsfel som hindrade uppdateringar från att sparas.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1474-->  Den valda leveransadressen ändras inte när du gör en beställning med en överlåtbar offert. Tidigare ändrades den valda leveransadressen till standardleveransadressen när du gjorde en beställning.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1429--> I Store Configuration settings for B2B Features, the **[!UICONTROL Enable Shared Catalog direct products price assigning]** fältet inaktiveras nu automatiskt. I butiken döljs den när **[!UICONTROL Enable Company]** inställning eller **[!UICONTROL Enable Shared Catalog]** inställningen är inställd på **[!UICONTROL No]**.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1683--> När du skapar ett företagskonto från butiken validerar Commerce nu e-postadressen innan företagsregistreringen bearbetas. Om e-postadressen är ogiltig misslyckas åtgärden och inga kontouppdateringar bearbetas. Tidigare skapades ett kundkonto även om begäran om att skapa ett företagskonto misslyckades på grund av en ogiltig e-postadress.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1664--> SKU:er som innehåller dubbla citattecken i den delade katalogen och prisstrukturen orsakar inte längre fel i administratören.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1498--> Varnish-konfigurationen för Commerce-programmet har uppdaterats för att förhindra att gästanvändare ser data från andra kundgrupper.

### Känt fel

Om du installerar eller uppgraderar B2B 1.4.0 på [Adobe Commerce version 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html)inträffar följande fel:

```terminal
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

Du kan åtgärda problemet genom att lägga till manuella beroenden för B2B-säkerhetspaketet genom att lägga till manuella beroenden för B2B-säkerhetspaketet med ett [stabilitetstagg](https://getcomposer.org/doc/04-schema.md#package-links). Instruktioner finns i [Adobe Commerce Knowledge Base](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html).

## B2B v1.3.5

*14 mars 2023*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg) Utgiven B2B version 1.3.5-p2 som stöd för kompatibilitet med Adobe Commerce 2.4.6-p2.

![Nytt](../assets/new.svg) Utgiven B2B version 1.3.5-p1 som stöd för kompatibilitet med Adobe Commerce 2.4.6-p1.

>[!NOTE]
>
>När du har uppgraderat Commerce från 2.4.6 till [senaste versionen](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html#2.4.6)ska du uppdatera till den version av korrigeringsfilen B2B 1.3.5 som stöds. Eller uppgradera B2B-tillägget från version 1.3.5 till version 1.4.0 eller senare för att få de senaste funktionerna.

![Nytt](../assets/new.svg) Stöd för Adobe Commerce 2.4.6 har lagts till.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-689--> Adobe Commerce visar nu korrekt information under betalningen när alternativet Inköpsorder är aktiverat och en virtuell offert som skapades med betalningsalternativet PayPal har valts. Tidigare visades summorna som noll under dessa villkor.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-609--> Listan över kundgrupper för **Tillåt bläddringskategori** inställningen innehåller inte längre kundgrupper som är relaterade till delade kataloger.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-1244--> Kundattributet för moms/momsregistreringsnummer fungerar nu som väntat med företagsadministratörskonton på både Admin och Storefront. Attribut för moms krävs inte längre för att skapa ett företagskonto. Tidigare när en handlare skapade ett företagskonto med ett eget attribut för moms, hade Adobe Commerce ett valideringsfel både i butiken och i Admin.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-1236--> Inaktivering av funktionen för delad katalog i ett visst omfång fungerar nu korrekt. Tidigare angav Adobe Commerce ett ogiltigt omfång när en handlare sparade en delad katalogkonfiguration.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-1203--> Administratörsanvändare kan nu spara egna attributvärden för kunder för företagsanvändare. Tidigare gick det inte att spara anpassade kundattribut för företagsanvändare.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-1221--> Prestandaproblem löses med valideringen av företagsbehörigheter som tillhandahålls via GraphQL när många företagsbehörigheter redan har tilldelats.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-1242--> Adobe Commerce genererar inte längre något fel på kundvagnssidan när Snabborder används för att lägga till en produkt i en kvantitet som överskrider det tillgängliga lagret.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-1090--> Prestanda för `SELECT` åtgärder för företagsbehörigheter har förbättrats.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-2456--> Kategorifrågor returnerar nu produktpriser enligt butikskonfigurationsinställningar när det inte finns några kategoribehörigheter som uttryckligen angetts för kategorin som efterfrågas.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-6829--> The **[!UICONTROL Place Order]** fungerar nu som väntat när du slutför ett köp med en godkänd offertförfrågan. Problem med överlåtbar offert `negotiableQuoteCheckoutSessionPlugin` plugin-programmet har lösts.

## B2B v1.3.4

*9 augusti 2022*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg) Stöd för Adobe Commerce 2.4.5 har lagts till.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-453-->Adobe Commerce skickar inte längre e-postmeddelanden varje gång ett befintligt företag uppdateras av ett API-anrop. Mejl skickas nu endast när ett företag skapas.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-406-->Adobe Commerce beräknar nu totalsumman för en överlåtbar offert korrekt när **[!UICONTROL Enable Cross Border Trade]** inställning för momsberäkning är aktiverad.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-322-->Konfigurerbara produkter flyttas nu till den sista positionen i produktlistan efter att Stock har uppdaterats när **[!UICONTROL Move out of stock to the bottom]** inställningen är aktiverad. En ny anpassad databasfråga implementeras för att säkerställa att sorteringsordningen för index i Elasticsearch nu följer den administratörsaktiverade sorteringsordningen. Tidigare flyttades inte konfigurerbara produkter och deras underordnade produkter längst ned i listan när den här inställningen var aktiverad.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-308-->Inköpsorder via e-post följer nu inställningen för e-postutskick för varje webbplats i en flersidig distribution. En kontroll av **[!UICONTROL Disable Email Communications]** inställningen läggs till i den anpassade logiken för e-postköer. Tidigare respekterade inte Adobe Commerce inställningen för e-postsändning för den sekundära webbplatsen.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-302-->Titeln på SKU-fältet på snabbbeställningssidan ändras för tydlighet.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-543-->Adobe Commerce visar nu ett mer informativt felmeddelande när en kund anger en ogiltig SKU i **Ange SKU eller produktnamn** fält.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-1753-->The **[!UICONTROL Account Created in]** fältet för en företagsadministratör behåller nu sitt värde som förväntat när du har sparat företaget.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-722 -->The `customer` frågan returnerar inte längre tomma resultat när den hämtar rekvisitionslistor som filtreras av `uid`.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-210 -->Ett plugin-program har lagts till före `collectQuoteTotals` ring för att säkerställa att butikskrediter endast används en gång.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-665 -->Kunder omdirigeras nu till inloggningssidan när deras konto tas bort av en administratör från administratören. Tidigare inträffade ett fel i Adobe Commerce. Plugin-programmet (`SessionPlugin`) finns nu i `try…catch` -block. Den här koden har inte paketerats i det generiska undantagshanteringsblocket.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-661 --> På sidan Snabbordning i mobilläge trycker du på **Retur** när du har angett ett giltigt produktnamn eller SKU tar kunden till nästa fält som förväntat.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-607 -->Företagsnamnet visas nu som förväntat i fakturerings- och leveransadressavsnitten i arbetsflödet för utcheckning.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-375 -->Butikskrediten är inte tillgänglig när **[!UICONTROL Zero Subtotal Checkout]** betalningsmetoden är inaktiverad. Kryssrutan Butikskrediter kunde inte användas vid orderplacering från administratören. Programmet gjorde ingen beställning med butikskrediten och visade följande fel: `The requested Payment Method is not available`.

## B2B v1.3.3

*9 augusti 2022*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg) Stöd för Adobe Commerce 2.4.4 har lagts till.

![Korrigerat problem](../assets/fix.svg) <!--- MC-41985--> Den tid det tar att uppgradera från Adobe Commerce 2.3.x till Adobe Commerce 2.4.x i installationer med över 100 000 företagsroller har minskat avsevärt.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42153--> POSTEN `V1/order/:orderId/invoice` begäran stöder nu skapande av partiella fakturor när **[!UICONTROL Payment on Account]** betalningsmetod är aktiverad. Tidigare inträffade följande fel i Adobe Commerce: `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`. [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![Korrigerat problem](../assets/fix.svg) <!--- MC-41975--> PayPal Payflow Pro fungerar nu som väntat med B2B-överlåtbara offerter när kundens kundvagn innehåller andra produkter. Adobe Commerce kan nu bearbeta beställningen och skicka ett e-postmeddelande till kunden som förväntat. Tidigare inträffade ett allvarligt fel i Adobe Commerce och ett bekräftelsemeddelande som innehöll nollvärden skickades via e-post till kunden.

![Korrigerat problem](../assets/fix.svg) <!--- MC-41819--> Sidnumreringen visas nu korrekt på katalogsökresultatsidan efter att vissa produkter i den delade katalogen har utelämnats.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42886--> Anpassade kundattribut sparas nu som förväntat när en företagsanvändare skapas eller sparas i Admin.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42927--> The **[!UICONTROL Submit]** knappen i formuläret Create New Company är nu inaktiverad efter ett klick för att förhindra att flera formulär skickas. Tidigare kunde du skicka in formuläret flera gånger genom att klicka på knappen upprepade gånger, vilket genererade ett fel.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42787--> Adobe Commerce visar inte längre länken för ombeställning i butiken när en kund loggar in i en butik där ombeställningar har inaktiverats.

![Korrigerat problem](../assets/fix.svg) <!--- MC-43115--> Snabbsorteringssökning med SKU är nu inte skiftlägeskänsligt när delad katalog är aktiverat.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42203--> Du kan nu uppdatera en fil för ett kundattribut när du skapar ett företag. Tidigare när du försökte skapa ett företag med en bifogad fil `File`, Adobe Commerce skapade inte företaget och loggade det här felet i undantagsloggen: `Something went wrong while saving file`.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42242--> Du kan nu skapa ett företag med ett kundkonto som har ett anpassat attribut med en (`File`) eller (`Image`). Tidigare gick det inte att matcha inläsaren för företagets redigeringssida om kontot hade något av dessa anpassningsbara alternativ, vilket hindrade redigering av företagsinformation.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42268--> The `products` frågan returnerar nu korrekt `total_count` när delad katalog är aktiverad.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42203-->  Du kan nu uppdatera en fil för ett kundattribut när du skapar ett företag. Tidigare när du försökte skapa ett företag med en bifogad fil `File`, Adobe Commerce skapade inte företaget och loggade det här felet i undantagsloggen: `Something went wrong while saving file`.

![Korrigerat problem](../assets/fix.svg) <!--- MC-43178--> The _Företagskonfiguration_ och _Skapa företag_ sidorna fungerar nu som väntat när du har inaktiverat en onlineseveransmetod. Verifiering har lagts till för att förhindra att försök görs att bearbeta inaktiverade leveransmoduler. Tidigare visade Adobe Commerce följande fel: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42214--> The _Kategori_ Sidan visar nu enhetliga produktdata medan behörigheter genereras under partiell indexering. En ny partiell indexerare för katalogbehörigheter har lagts till i den här processen. Tidigare var de data som visades när indexeraren kördes felaktiga.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42567--> The `categoryList` frågan returnerar nu korrekt antal produkter när katalogbehörigheter används och produkter tilldelas till en delad katalog.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42528--> The `categoryList` frågan respekterar nu kategoribehörigheter och returnerar bara tillåtna kategorier. Tidigare returnerades alla tilldelade och ej tilldelade kategorier.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42399--> The `rest/V1/company/{id}` begäran nu returnerar `is_purchase_order_enabled` attributvärden som förväntat.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-128--> Anpassade kundattribut visas nu som förväntat i _Företagsadministratör_ -fliken.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-130--> Blocket Min önskelista på sidan Mitt konto visas nu som förväntat för företagsadministratörer och företagsanvändare.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-133--> Snabborderfel visas inte längre i kundvagnen. Tidigare visade Adobe Commerce det här felet i kundvagnen när SKU:n inte hittades i katalogen:  `The SKU was not found in the catalog`.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-194--> Åtgärder för att spara delade kataloger har optimerats för att köras snabbare. Tidigare kunde det ta flera minuter att spara en delad katalog med många kundgrupper.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42240--> Adobe Commerce tar nu bort alla underkategoribehörigheter från `sharedcatalog_category_permissions` register när den överordnade kategorin tas bort. Tidigare togs endast överordnade kategoridata bort.

## B2B v1.3.2

*29 augusti 2022*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg) Stöd för Adobe Commerce 2.4.3 har lagts till.

![Korrigerat problem](../assets/fix.svg) <!--- MC-39862--> Adobe Commerce skickar nu uppdateringsmeddelanden via e-post om utgångna, överlåtbara offerter. När en överlåtbar offert hade gått ut skickade Adobe Commerce inte ut några e-postmeddelanden med uppdateringar.

![Korrigerat problem](../assets/fix.svg) <!--- MC-40682--> Adobe Commerce skickar nu uppdateringsmejl som snart går ut och som går ut med överlåtbara offerter när en `cron` jobb saknas.

### Företag

![Korrigerat problem](../assets/fix.svg) <!--- MC-41542--> I listrutan för sidan Skapa nytt företagskonto visas inte längre tomma alternativvärden. Tidigare var de två första alternativvärdena och landskoden `AN` var tomma.

![Korrigerat problem](../assets/fix.svg) <!--- MC-41260--> Klicka på **[!UICONTROL Return]** för en order som har skapats av en företagsanvändare dirigerar nu om en administrativ användare till sidan Skapa retursida som förväntat. Administratören har tidigare omdirigerats till sidan Orderhistorik.

![Korrigerat problem](../assets/fix.svg) <!--- MC-40798--> Adobe Commerce misslyckas inte längre med ett fel av typen slut på minne när programmet körs `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` metod under `bin/magento setup:upgrade`. Tidigare använde Adobe Commerce inte batchstorlek för att samla in när behörigheter initierades, utan i stället lästes in en samling med alla företagsroller.

![Korrigerat problem](../assets/fix.svg) <!--- MC-40551--> Företagsanvändare kan nu redigera och uppdatera anpassade attributvärden för kunder. Tidigare var dessa attribut inte korrekt kopplade till formuläret för att skapa och redigera användare. En företagsanvändare kunde ange olika attributvärden, men Adobe Commerce sparade inte dessa värden korrekt.

![Korrigerat problem](../assets/fix.svg) <!--- MC-32653--> Resursträdet för behörigheter för företagsroller kan nu översättas som förväntat. Tidigare översattes inte behörighetsträdet trots att det fanns giltiga översättningsfiler.

![Korrigerat problem](../assets/fix.svg) <!--- MC-40358--> Adobe Commerce sparar nu anpassade kundattributvärden för B2B-användare som förväntat. Tidigare uppstod ett mallfel när ett företagskonto som innehöll anpassade kundattribut skapades och Adobe Commerce kunde inte läsa in formuläret. Lägga till ett argument i layouten för `company_create_account` löste problemet.

![Korrigerat problem](../assets/fix.svg) <!--- MC-41721--> Företagsanvändarfilter som Visa alla användare, Visa aktiva användare och Visa inaktiva användare fungerar nu som förväntat. Tidigare orsakade filtreringsåtgärder på företagets användarsida ett JavaScript-fel.

### Företagskrediter

![Korrigerat problem](../assets/fix.svg) <!--- MC-41551--> Administratörer med begränsade konton som endast har behörighet på webbplatsnivå kan nu skapa ett företag som använder en annan valuta än webbplatsen.

![Korrigerat problem](../assets/fix.svg) <!--- MC-41523--> Adobe Commerce skickar nu e-postmeddelanden från rätt företag `from` e-postadress och omfattning. Tidigare övervägde Adobe Commerce inte webbplatsens omfattning när man skickade företagskredittilldelning eller uppdaterat e-post.

### Snabbordning

![Korrigerat problem](../assets/fix.svg) <!--- MC-42104--> Nu fungerar det som väntat att skapa en beställning med hjälp av snabbordning från en CSV-fil med SKU:er som inte finns.

![Korrigerat problem](../assets/fix.svg) <!--- MC-40268--> Du kan nu använda Snabbordning för att söka på flera SKU:er på rätt sätt. Tidigare innehöll resultaten dubblettposter.

![Korrigerat problem](../assets/fix.svg) <!--- MC-40261--> Listan med tillagda produkter hanterar nu SKU:er som anges med gemener och versaler på samma sätt när du använder SKU:er för att välja flera produkter under Snabbordning.

![Korrigerat problem](../assets/fix.svg) <!--- MC-40225--> Med Snabbbeställning läggs nu produkter i den kvantitet som anges av kunden. Tidigare lade Adobe Commerce bara till en produkt även om mängden köpare överstiger ett.

![Korrigerat problem](../assets/fix.svg) <!--- MC-41283--> Funktionen Komplettera automatiskt i snabbordning fungerar nu med partiella SKU:er.

![Korrigerat problem](../assets/fix.svg) <!--- MC-41299--> Adobe Commerce visar nu produkter som har konfigurerats som **Inte synlig separat** på snabbordningssidans lista med automatiska förslag och sökresultat.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42402--> Köpare kan nu använda snabbbeställningsformuläret för att lägga till flera produkter efter SKU:er som innehåller versaler. Tidigare lades endast den första produkten till.

### Förhandlingsbar offert

![Korrigerat problem](../assets/fix.svg) <!--- MC-41232--> Shoppare dirigeras nu till den överlåtbara offertsidan när länken till en överlåtbar offert har klistrats in i URL-fältet och loggats in. Tidigare omdirigerades kunderna till sidan Mitt konto.

![Korrigerat problem](../assets/fix.svg) <!--- MC-39317--> Beställning fungerar nu som förväntat för order som innehåller en produkt med alternativet för datumanpassning för ett kundkonto som skapades vid utcheckning. Tidigare bearbetades inte ändringsordningarna av Adobe Commerce och följande fel visades: `The product has required options. Enter the options and try again`.

![Korrigerat problem](../assets/fix.svg) <!--- MC-39063--> Leveransadressen för en överlåtbar offert kan inte längre redigeras under utcheckning när inköpsordermodulen är inaktiverad. Beteendet är ett resultat av en tidigare korrigering där `isQuoteAddressLocked` har tagits bort från den utcheckningsbara offertrenderaren.

![Korrigerat problem](../assets/fix.svg) <!--- MC-38967--> Handlare kan nu lägga till produkter i en överlåtbar offert från administratören.

### Inköpsorder

![Korrigerat problem](../assets/fix.svg) <!--- MC-39983--> Adobe Commerce visar nu ett informativt felmeddelande som väntat när du gör en inköpsorder med PayPal Express Checkout när **[!UICONTROL Name Prefix]** attribute is set to `required`. Tidigare gjorde Adobe Commerce ingen beställning och inget felmeddelande visades.

![Korrigerat problem](../assets/fix.svg) <!--- MC-39620--> Gränssnittskomponenten för faktureringsadressen i modulen Inköpsorder använder nu offertadressen korrekt när Google Tag Manager är aktiverat. Tidigare uppstod ett JavaScript-fel på betalningssidan.

### Rekvisitionslistor

![Korrigerat problem](../assets/fix.svg) <!--- MC-40426--> Handlare kan nu använda POSTEN `rest/all/V1/requisition_lists` slutpunkt för att skapa en rekvisitionslista för en kund. Tidigare inträffade detta 400-fel i Adobe Commerce när du försökte skapa en rekvisitionslista: `Could not save Requisition List`.

![Korrigerat problem](../assets/fix.svg) <!--- MC-41123--> The **[!UICONTROL Add to Requisition List]** visas nu för en varukorg i lager när varukorgen även innehåller produkter som inte finns i lager. Om en varukorg innehöll två produkter, varav en inte fanns i lager, var _[!UICONTROL Add to Requisition List]_visas inte för någon av produkterna.

![Korrigerat problem](../assets/fix.svg) <!--- MC-40877--> Du kan nu använda REST API för att lägga till en produkt i en rekvisitionslista.

![Korrigerat problem](../assets/fix.svg) <!--- MC-40155--> Rekvisitionslista **[!UICONTROL Latest Activity Date]** värden som nu följer språkformatet.

![Korrigerat problem](../assets/fix.svg) <!--- MC-39580--> Adobe Commerce genererar inte längre ett allvarligt fel när du redigerar en paketprodukt från en rekvisitionslista.

![Korrigerat problem](../assets/fix.svg) <!--- MC-40454--> Adobe Commerce visar nu rätt produktpris när du lägger till en produkt med ett anpassningsbart alternativ `(File)` till en önskelista från en rekvisitionslista. Länken till den överförda filen visas också som förväntat. Tidigare visade Adobe Commerce felaktiga produktpriser och inte länken till filen.

![Korrigerat problem](../assets/fix.svg) <!--- MC-36383--> Produkter med anpassningsbart alternativ `(File)` kan nu läggas till i en kundvagn från en rekvisitionslista.

### Delad katalog

![Korrigerat problem](../assets/fix.svg) <!--- MC-40497--> En administratör med en roll som är begränsad till en viss webbplats kan nu skapa, visa och redigera en delad katalog. Tidigare uppstod ett allvarligt fel i Adobe Commerce när en administratör med en begränsad roll försökte skapa en delad katalog.

![Korrigerat problem](../assets/fix.svg) <!--- MC-41337--> Navigeringsresultaten i flera lager innehåller nu korrekt antal produkter med filtrerade attribut, och kunderna kan nu använda flera filter. Tidigare kunde bara ett filter användas och Adobe Commerce visade ett felaktigt produktantal vid navigering i lager.

![Korrigerat problem](../assets/fix.svg) <!--- MC-40779--> Adobe Commerce visar nu produktantal korrekt i navigeringsfilter i lager i sökresultaten. Tidigare använde inte ett plugin-program för sökresultatsidan Elasticsearch utan skickade en ny fråga till databasen.

![Korrigerat problem](../assets/fix.svg) <!--- MC-39978--> Adobe Commerce tar inte längre bort nivåpriser när en handlare tar bort alla produkter från en delad standardkatalog.

![Korrigerat problem](../assets/fix.svg) <!--- MC-39802--> Filter filtreras nu efter den aktuella kategorin och visas korrekt på alla sidor när delade kataloger är aktiverade. Tidigare beräknades filter felaktigt enbart för den aktuella sidan och filtrerades inte av den aktuella kategorin.

![Korrigerat problem](../assets/fix.svg) <!--- MC-39522--> GraphQL `products` frågan returnerar inte längre en produkts prisintervall och kategori för produkter som inte är tilldelade till en delad katalog när delad katalog är aktiverad. Tidigare returnerade frågan produktens aggregeringar, även om själva produkten inte returnerades i `items` array.

## B2B v1.3.1

*9 februari 2021*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg) Stöd för Adobe Commerce 2.4.2 har lagts till.

![Nytt](../assets/new.svg) Onlinebetalningsmetoder stöds nu för inköpsorder.

![Korrigerat problem](../assets/fix.svg) Om du lägger till en konfigurerbar produkt i kundvagnen direkt från en rekvisitionslista när produkten användes i en tidigare order returneras inte längre något systemfel.

![Korrigerat problem](../assets/fix.svg) Adobe Commerce visar nu fliken Kräver mitt godkännande korrekt för inköpsorder när en delad databaskonfiguration distribueras.

![Korrigerat problem](../assets/fix.svg) Adobe Commerce visar nu information om paketprodukter och presentkort när du visar inköpsorder.

![Korrigerat problem](../assets/fix.svg) Köpare omdirigeras nu som förväntat efter att ha loggat in på sitt konto när de surfar i en butik där **[!UICONTROL Website Restriction]** är aktiverat och **[!UICONTROL Restriction Mode]** är inställd på `Private Sales: Login Only`. Tidigare omdirigerades kunderna till butikens hemsida. <!--- MC-38934-->

![Korrigerat problem](../assets/fix.svg) Beställningshistoriken läses nu in som förväntat på en företagsadministratörs kontokontrollpanel i distributioner med en B2B-företagshierarki som innehåller många kunder (större än 13000). Tidigare lästes orderhistoriken in långsamt eller inte alls och Adobe Commerce visade ett 503-fel. <!--- MC-38830-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce visar inte längre flera identiska varningsmeddelanden när du lägger till en okonfigurerad produkt med anpassningsbara alternativ i en rekvisitionslista från en kategorisida. <!--- MC-38342-->

![Korrigerat problem](../assets/fix.svg) Nya och duplicerade produkter visas nu som förväntat på kategorisidan när delade B2B-kataloger är aktiverade. <!--- MC-38307-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce har nu rätt `store_id` som är associerad med en företagsadministratör när kundgruppen för ett företag uppdateras. Tidigare `store_id` ändrades till standardbutiken när gruppen uppdaterades. <!--- MC-38196-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce sparar nu en grupperad produkt i en beställningslista som en lista över enkla produkter på samma sätt som en grupperad produkt läggs till i en kundvagn. På grund av hur Adobe Commerce sparade grupperade produkter omdirigerades länken för en grupperad produkt från rekvisitionslistan alltid till enkla produkter och inte till den grupperade produkten. <!--- MC-38049-->

![Korrigerat problem](../assets/fix.svg) Nu kan du filtrera order efter **[!UICONTROL Company Name]** när du exporterar orderinformation i CSV-format. Tidigare loggade Adobe Commerce ett fel i `var/export/{file-id}`. <!--- MC-37785-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce visar nu popup-rutan Skapa rekvisitionslista som förväntat när du väljer fliken Skapa ny rekvisitionslista i butiken. <!--- MC-37915-->

![Korrigerat problem](../assets/fix.svg) Rekvisitionslistor innehåller nu alla grupperade produkter och kvantiteter som har lagts till i listan. När en handlare navigerade till en rekvisitionslista efter att ha lagt till produkter i den från en produktinformationssida visades följande fel: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![Korrigerat problem](../assets/fix.svg) Den korrekta butiksvyn är nu kopplad till den relevanta webbplatsen när du skapar ett företag i en distribution med flera platser. Tidigare kunde du inte skapa ett företag och Adobe Commerce visade då följande fel: `The store view is not in the associated website`. <!--- MC-37488-->

![Korrigerat problem](../assets/fix.svg) Om du beställer produkter efter SKU med Snabbordning skapas inte längre dubbla produktkvantiteter i CSV-filen. <!--- MC-37427-->

![Korrigerat problem](../assets/fix.svg) The **[!UICONTROL Add to Cart]** knappen inte längre blockeras när _[!UICONTROL Enter Multiple SKUs]_-avsnittet på sidan Snabbordning innehåller ett tomt värde. I stället visas ett meddelande i Adobe Commerce där du uppmanas att ange giltiga SKU:er. <!--- MC-37387-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce visar nu det här meddelandet på produktsidan när du skickar in en produktrecension från en rekvisitionslista: `You submitted your review for moderation`. Granskningen visas även på sidan Väntande granskningar (Admin **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**). Tidigare, trots att Adobe Commerce lade till granskningen i listan över väntande granskningar, uppstod ett 404-fel på produktsidan. <!--- MC-37119-->

![Korrigerat problem](../assets/fix.svg) Prestanda för `sharedCatalogUpdateCategoryPermissions` konsumenten har förbättrats. När du har skapat en delad katalog använder katalogbehörighetsindexeraren nu bara kundgrupp-ID:t från den delade katalogen, inte alla kundgrupper. <!--- MC-36770-->

![Korrigerat problem](../assets/fix.svg) Anpassade fält för kundadressattribut som är kopplade till en köpares icke-standardadress sparas nu som förväntat i arbetsflödet för utcheckning i butiken. <!--- MC-36630-->

![Korrigerat problem](../assets/fix.svg) Beställningar av produkter som tillhör en butiks delade standardkatalog kan nu göras till kunder via Admin REST API (`rest/V1/carts/{<CART_ID>/items`) som förväntat. Adobe Commerce kontrollerar nu om produkten har tilldelats en offentlig katalog innan behörighetsvalideringen för delad katalog har gjorts i `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave`. Tidigare lade Adobe Commerce inte till produkten i kundvagnen och returnerade följande fel: `No such shared catalog entity`. <!--- MC-36535-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce skickar nu e-postmeddelanden om nya företagsanvändare från Adobe Commerce butiks adress. Tidigare skickades det här e-postmeddelandet från företagets administratörsadress. <!--- MC-36480-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce söker nu efter anpassade attribut för duplicering av reserverade företagsattributnamn innan en handlare tillåts spara ett nytt attribut. <!--- MC-36282-->

![Korrigerat problem](../assets/fix.svg) The `credit_history` frågan returnerar nu det angivna företagets kredithistorik för både det ursprungligen allokerade beloppet och det köpta beloppet. Tidigare returnerade frågan ett fel.

![Korrigerat problem](../assets/fix.svg) The **[!UICONTROL Company]** och  **[!UICONTROL Job Title]** fält på sidan Redigera kontoinformation går inte längre att redigera.

### Kända fel

- B2B-köpare kan använda onlinebetalningsmetoder för att kringgå det vanliga inköpsorderflödet. Detta scenario kan inträffa om köparen kan minska den totala utcheckningen till 0 (till exempel med en kampanjkod eller presentkort) och sedan ta bort koden eller presentkortet. Även under dessa omständigheter lägger Adobe Commerce fortfarande order på rätt belopp baserat på priserna på artiklarna i deras tilldelade katalog. **_Tillfällig lösning_**: Inaktivera presentkort och kupongkoder när online-betalningsmetoder har aktiverats för godkännande av inköpsorder. <!--- B2B-1603-->

- Köpare dirigeras om till kundvagnen när de försöker lägga en order från en inköpsorder med PayPal Express Checkout när **[!UICONTROL In-Context Mode]** är inaktiverat. <!--- B2B-1604-->

- Adobe Commerce visar ibland ett 404-fel när en köpare skapar en inköpsorder och sedan navigerar till utcheckningssidan. Det här felet inträffar när en köpare tidigare har skapat en annan inköpsorder med en onlinebetalningsmetod innan han/hon går till utcheckningssidan utan att slutföra det föregående köpet. Köparen kan fortfarande göra inköpsordern. **_Arbeta runt_**: Ingen. <!--- B2B-1605-->

- Rabatterna för en viss betalningsmetod gäller även vid utcheckning av en inköpsorder även när köparen ändrar sin betalningsmetod under den slutliga utcheckningen. Det innebär att kunderna får en rabatt som de inte har rätt till. Det här problemet inträffar eftersom en kundvagnsregel för den ursprungliga betalningsmetoden fortfarande tillämpas trots att betalningsmetoden har ändrats. **_Arbeta runt_**: Ingen. Se [Adobe Commerce 2.4.2 B2B: Rabatten gäller fortfarande för onlineinköpsorder när betalningsmetoden har ändrats](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) _Knowledge Base_ artikel. <!-- B2B-1012 -->

- The `deleteRequisitionListOutput` frågan returnerar information om den borttagna rekvisitionslistan i stället för de återstående rekvisitionslistorna. <!--- MC-39894-->

## B2B v1.3.0

*15 oktober 2020*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

Den här versionen innehåller förbättringar av ordergodkännanden, leveransmetoder, kundvagn och loggning av administratörsåtgärder.

![Nytt](../assets/new.svg) Stöd för Adobe Commerce 2.4.1 har lagts till.

![Nytt](../assets/new.svg) B2B-ordergodkännanden har förbättrats för att förbättra användbarheten och möjliggöra massåtgärder på inköpsorder.

![Nytt](../assets/new.svg) B2B-handlare kan nu styra leveransmetoder som erbjuds respektive företag.<!--- BUNDLE-160 161 162 -->

![Nytt](../assets/new.svg) Merchants kan nu låta användare rensa innehållet i kundvagnen i en enda åtgärd och kan konfigurera detta separat på varje webbplats <!--- BUNDLE-108 -->

![Nytt](../assets/new.svg) B2B-köpare kan nu lägga till enskilda artiklar eller hela innehållet i kundvagnen direkt i en rekvisitionslista. <!--- BUNDLE-145 144-->

![Nytt](../assets/new.svg) B2B-handlare kan skapa beställningar från administratören för kunders räkning med alternativet Betalning på konto som betalningsmetod. <!--- BUNDLE-166 178-->

![Nytt](../assets/new.svg) Handlare kan nu direkt visa alla offerter som är kopplade till en användare från kundens detaljsida. <!--- BUNDLE-139 -->

![Nytt](../assets/new.svg) Merchants kan nu filtrera rutnätet för kunder nu online efter företag. <!--- BUNDLE-137 -->

![Nytt](../assets/new.svg) Administratörer kan nu filtrera kunder i Admin efter säljare. <!--- BUNDLE-110 -->

![Nytt](../assets/new.svg) För att minska antalet falska konton och skräppostkonton kan handlarna nu aktivera Google reCAPTCHA i formuläret New Company Request i butiken. <!--- BUNDLE-154 -->

![Nytt](../assets/new.svg) Administratörsåtgärder som vidtas i företagsmodulerna loggas nu i Admin Actions Log. Åtgärder loggas från alla relevanta företagsmoduler: `Company`, `NegotiableQuote`, `CompanyCredit`, `SharedCatalog`.  <!--- BUNDLE-180 181 182 183 -->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce visar inte längre **[!UICONTROL Delete customer]** på **Kunder** sida när den inloggade administratören inte har behörighet att ta bort kunder i distributioner där B2B är installerat. <!--- MC-35655-->

![Korrigerat problem](../assets/fix.svg) Kundgruppen ändras inte längre automatiskt för en kund som tilldelas ett företag när du redigerar kunden i kundrutnätet. <!--- MC-35254-->

![Korrigerat problem](../assets/fix.svg) När en handlare skapar en delad katalog anges nu behörigheterna automatiskt till `Allow` för **[!UICONTROL Display Product Prices]** och **[!UICONTROL Add to Cart]** funktioner i kategorier när kundgruppen tilldelas denna åtkomst i katalogens behörighetsinställningar. Tidigare var dessa inställningar automatiskt inställda på `Deny` även när katalogbehörigheter har angetts till `Allow`.<!--- MC-34792-->

![Korrigerat problem](../assets/fix.svg) Behörigheter för kategorin för delad katalog skrivs inte längre över när en produkt redigeras från produktredigeringssidan.<!--- MC-34777-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce skickar nu ett e-postmeddelande som bekräftar att en kund har behörighet att överskrida den angivna kreditgränsen när en handlare aktiverar **[!UICONTROL Allow To Exceed Credit Limit]** inställning. Tidigare angav det e-postmeddelande som Adobe Commerce skickade att kunden inte hade behörighet att överskrida gränsen. <!--- MC-34584-->

![Korrigerat problem](../assets/fix.svg) Behållaren HTML som omger produktpriset i rekvisitionslistor återges nu korrekt för de underordnade produkterna i paketerade produkter. <!--- MC-36331-->

![Korrigerat problem](../assets/fix.svg) Handlare kan nu ange vilket språk som företagets e-post ska skickas till när de skapar ett företag i flerspråkiga distributioner. Tidigare visades inte den nedrullningsbara menyn som gör det möjligt för handlarna att välja rätt butiksvy och språk.  <!--- MC-35777-->

![Korrigerat problem](../assets/fix.svg) Anpassade fält för kundadressattribut visas nu som förväntat i arbetsflödet för utcheckning av lagerställe. <!--- MC-35607-->

![Korrigerat problem](../assets/fix.svg) Konfigurationsfliken för B2B-funktioner öppnas nu korrekt. <!--- MC-35458-->Gäster kan nu använda QuickOrder för att lägga till produkter i kundvagnen och sedan ta bort artiklar. Tidigare togs produkten inte bort när en kund använde QuickOrder för att lägga till flera produkter i kundvagnen och sedan tog bort en produkt. <!--- MC-35327-->

![Korrigerat problem](../assets/fix.svg) Ett företag kan nu uppdateras med REST API PUT `/V1/company/:companyId` begäran utan att ange `region_id` när läget är konfigurerat som **krävs inte**. Tidigare, även om `region_id` var inte obligatoriskt, Adobe Commerce genererade ett fel om det inte angavs. <!--- MC-35304-->

![Korrigerat problem](../assets/fix.svg) När du skapar eller uppdaterar ett B2B-företag med hjälp av REST API (`http://magento.local/rest/V1/company/2`, där `2` representerar företags-ID), innehåller svaret nu inställningarna för `applicable_payment_method` eller `available_payment_methods` som förväntat. <!--- MC-35248-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce visar inte längre en 404-sida när en handlare använder **Retur** i stället för att klicka på **[!UICONTROL Save]** när du skapar en rekvisitionslista i butiken.<!--- MC-35094-->

![Korrigerat problem](../assets/fix.svg) Kategoribehörigheter ändras inte längre när en ny produkt tilldelas till en offentlig delad katalog. Tidigare har kategoribehörigheter duplicerats. <!--- MC-34386-->

![Korrigerat problem](../assets/fix.svg) REST API-slutpunkten PUT `rest/default/V1/company/{id}`, som används för att uppdatera företagets e-post, är inte längre skiftlägeskänsligt. <!--- MC-34308-->

![Korrigerat problem](../assets/fix.svg) När du inaktiverar belöningsmoduler påverkas inte längre B2B-funktioner på kundkonton. Tidigare visades inte följande B2B-relaterade flikar när belöningsmoduler inaktiverades: Företagsprofil, Företagsanvändare samt Roller och behörigheter.<!--- MC-34191-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce använder nu rätt avsändarnamn i e-postmeddelanden när ändringar görs i företagskonton. Tidigare använde Adobe Commerce det allmänna kontaktavsändarnamnet som definierats i standardomfånget för alla e-postmeddelanden. <!--- MC-33917-->

![Korrigerat problem](../assets/fix.svg) Nu kan du implementera multileverans för beställningar som innehåller både fysiska och virtuella produkter. <!--- MC-33818-->

![Korrigerat problem](../assets/fix.svg) Merchants kan nu skapa företagsanvändare från _[!UICONTROL Company Users]_på sidorna Mitt konto och Företagsstruktur när **[!UICONTROL Access Restriction]**är aktiverat och **[!UICONTROL Restriction Mode]**är inställd på `Sales: Login Only`. Tidigare inträffade detta fel i Adobe Commerce när en handlare försökte skapa en användare: `Can not register new customer due to restrictions are enabled`. <!--- MC-33608-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce återställer inte längre kundens kundgrupp till standardinställningen när en kund sparar sin kontoinformation. <!--- MC-33554-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce genererar inte längre ett allvarligt fel när en administratör tilldelar en kund som har en aktiv kundvagn till en kundgrupp. <!--- MC-33313-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce har nu en `addToCart` DataLayer-händelse för snabbordning och rekvisition listar sidor.  <!--- MC-33295-->

![Korrigerat problem](../assets/fix.svg) E-postmeddelanden som skickas till säljare som tilldelats ett företag innehåller nu den tilldelade företagslogotypen. Tidigare innehöll e-postmeddelandet den förvalda LUMA-logotypen, inte den överförda företagslogotypen. <!--- MC-33232-->

![Korrigerat problem](../assets/fix.svg) En rekvisitionslista innehåller nu alla grupperade produkter och kvantiteter som har lagts till i listan. När en handlare navigerade till en rekvisitionslista efter att ha lagt till produkter i den från en produktinformationssida visades följande fel: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![Korrigerat problem](../assets/fix.svg) The `products` frågan returnerar nu korrekt `total_count` när delad katalog är aktiverad. <!--- MC-42268-->

![Korrigerat problem](../assets/fix.svg) Sidorna Företagskonfiguration och Skapa företag fungerar nu som förväntat när du har inaktiverat en onlineseveransmetod. Verifiering har lagts till för att förhindra att försök görs att bearbeta inaktiverade leveransmoduler. Tidigare visade Adobe Commerce följande fel: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`. <!--- MC-43178-->

![Korrigerat problem](../assets/fix.svg) Integrationstestets minnesförbrukning har reducerats, vilket förbättrar testprestandan och minskar den tid som krävs för att slutföra testet. <!--- AC-266-->

## B2B v1.2.0

*28 juli 2020*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg) Stöd för Adobe Commerce 2.4.0 har lagts till.

![Nytt](../assets/new.svg) Storefront Order Search, med ytterligare tack för Marek Mularczyk från [Divante](https://www.divante.com/) och communitymedlemmar.

![Nytt](../assets/new.svg) Inköpsorder har förbättrats och skrivits om. De ingår nu som standard i Adobe Commerce.

![Nytt](../assets/new.svg) Regler för godkännande av inköpsorder har implementerats. Dessa regler gör att användare kan styra arbetsflödet för inköpsorder genom att skapa inköpsregler för order.

![Nytt](../assets/new.svg) Inloggning som kund ingår nu som standard i Adobe Commerce. Med den här funktionen kan webbplatspersonalen hjälpa kunderna genom att logga in som kunden för att se vad de ser.

![Korrigerat problem](../assets/fix.svg) Attributaggregering fungerar nu korrekt för navigering i lager med Elasticsearch

![Korrigerat problem](../assets/fix.svg) Sökordrar med specialtecken fungerar nu korrekt.

![Korrigerat problem](../assets/fix.svg) Klicka på **[!UICONTROL Clear All]** Knappen utökar nu alla filter i stället för att komprimera dem.

![Korrigerat problem](../assets/fix.svg) Produkt-SKU/namn ingår nu i sökfiltersammanfattningen för orderhistorik.

![Korrigerat problem](../assets/fix.svg) Sorteringsindikatorn visas nu korrekt i stödrastret Mina inköpsorder.

![Korrigerat problem](../assets/fix.svg) Nu kan du bara klicka på knapparna Godkänn, Avbryt, Avvisa och Inköpsorder en gång. Tidigare kunde du klicka på knappen flera gånger.

![Korrigerat problem](../assets/fix.svg) Knapparna Godkänn, Avvisa, Avbryt och Validera renderas nu korrekt på mobila enheter.

![Korrigerat problem](../assets/fix.svg) Tidigare innebar ett godkännande av en inköpsorder med en rabatt som hade upphört att gälla att ordern fick det fulla beloppet och inte att inköpsordersumman uppdaterades. Nu uppdateras inköpsordersumman så att rätt summa visas.

![Korrigerat problem](../assets/fix.svg) Ett problem uppstod i 2.3.4 där anpassade tilläggsattribut inte skulle kopieras från kundadressen till offertadressen. Problemet har åtgärdats.

![Korrigerat problem](../assets/fix.svg) När B2B är installerat visas ett SQL-fel när du tilldelar kategorier till delade kataloger. Problemet har åtgärdats.

![Korrigerat problem](../assets/fix.svg) På grund av ett felaktigt variabeltypvärde kunde administratörer inte lägga till konfigurerbara produkter i en order. Alternativlistrutorna fyller inte i. Den här funktionen fungerar nu korrekt.

![Korrigerat problem](../assets/fix.svg) När du redigerade kategoribehörigheter för gruppen Inte inloggad tidigare uppstod ett fel när ändringarna sparades. Problemet har åtgärdats.

![Korrigerat problem](../assets/fix.svg) En korrigering läggs till så att lagringsadministratörer kan lägga till produkter i en order som inte finns i den delade katalogen. Tidigare visades ett felmeddelande när ett objekt som inte finns i katalogen lades till.

![Korrigerat problem](../assets/fix.svg) Tidigare, efter att kommandot körts `php bin/magento indexer:set-dimensions-mode catalog_product_price website` och sedan försöka skapa en delad katalog inträffar ett fel. Problemet har åtgärdats.

![Korrigerat problem](../assets/fix.svg) När du lägger till ett företag och tilldelar företagsadministratören till en webbplats som inte är standard skickades fel webbplats-ID, vilket orsakade ett fel. Problemet har åtgärdats.

![Korrigerat problem](../assets/fix.svg) När en kund har flyttats till en annan kundgrupp lägger du till en produkt i en beställning med _Snabbordning_ skulle misslyckas med ett fel. Problemet har åtgärdats.

![Korrigerat problem](../assets/fix.svg) Tidigare, när du försökte checka ut med WebAPI med ett B2B-citattecken, skickades ett felaktigt värde till API:t, vilket orsakade att ett fel uppstod. Problemet har åtgärdats.

![Korrigerat problem](../assets/fix.svg) Tidigare uppstod ett fel när ett företag ställdes in på&quot;Active&quot; via API:t. Problemet har nu åtgärdats.

![Korrigerat problem](../assets/fix.svg) På grund av ett onödigt `form` -taggen uppdateras ordersidan automatiskt när du trycker på Retur efter att ha ändrat en föreslagen fraktkostnad. Problemet har åtgärdats.

![Korrigerat problem](../assets/fix.svg) Tidigare uppstod ett fel när en produktvisningsgräns skulle anges för en katalogsida och gränsen var mindre än antalet totala produkter. Funktionen fungerar nu som förväntat.

![Korrigerat problem](../assets/fix.svg) Tidigare kopierades den ursprungliga administratörsadressen till den nya administratören om du ändrar administratör för ett företag, och de får två adresser. Nu läggs bara rätt adress till.

![Korrigerat problem](../assets/fix.svg) Tidigare gick det inte att använda API:t för att spara ett offertobjekt när Git är inställt på Tillåten och Meddela kund. Detta API-anrop fungerar nu som förväntat.

![Korrigerat problem](../assets/fix.svg) Fast produktskatt visas nu på informationssidan för offerter.

![Korrigerat problem](../assets/fix.svg) Tidigare gick det inte att hämta filen om du klickade på en bifogad fil på fliken Kommentarer på sidan Mina offerter. Detta beteende fungerar nu som förväntat.

### Kända fel

- Adobe Commerce genererar ett undantag vid uppgradering till B2B 1.2.0 i en flerwebbplatsdistribution. När `setup:upgrade` körs, det här felet inträffar på `PurchaseOrder` modul: `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`. **Tillfällig lösning**: Installera `B2B-716 Add NonTransactionableInterface` till `InitPurchaseOrderSalesSequence` snabbkorrigering för datakorrigering, som nu är tillgänglig från **Mitt konto** > **Nedladdningar** avsnitt i `magento.com`.
- Om en rabattkod förfaller innan en inköpsorder godkänns fortsätter inköpsordern att visa det rabatterade beloppet, men när inköpsordern har godkänts placeras ordern på den icke-rabatterade summan. **Tillfällig lösning**: Installera `B2B-709 Purchase Order Discount patch` snabbkorrigering för det här problemet, som nu är tillgänglig via **Mitt konto** > **Nedladdningar** avsnitt i `magento.com`.
- Om artiklar i en inköpsorder inte finns i lager eller om det inte finns tillräckligt med kvantitet när inköpsordern konverteras till en faktisk order inträffar ett fel. Om restorder är aktiverade bearbetas ordern normalt.
