---
title: Versionsinformation för [!DNL Adobe Commerce B2B]
description: Granska versionsinformationen för information om ändringar i  [!DNL Adobe Commerce B2B] releaser.
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: 561d6f46340333820a47c938332a7977d8f332a8
workflow-type: tm+mt
source-wordcount: '8736'
ht-degree: 0%

---

# Versionsinformation för [!DNL Adobe Commerce B2B]

Versionsinformationen för B2B-tillägget innehåller tillägg och korrigeringar som Adobe har lagt till under en releasecykel, inklusive:

![Nya](../assets/new.svg) nya funktioner
![ Åtgärdat problem ](../assets/fix.svg) Korrigeringar och förbättringar
![Kända fel](../assets/bug.svg)

>[!NOTE]
>
>Mer information om vilka versioner av B2B Commerce-tillägget som stöds för tillgängliga Adobe Commerce-versioner finns i [Produkttillgänglighet](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html?lang=sv-SE).

## B2B 1.5.2

*8 april 2025*

[!BADGE Säkerhetsuppdateringar som stöds]{type=Informative tooltip="Stöds"} Adobe Commerce version 2.4.8, 2.4.7-p5 och 2.4.6-p10.
Kompatibel med Adobe Commerce version 2.4.7 till 2.4.7-p4, 2.4.6 till 2.4.6-p9

B2B v1.5.2-versionen innehåller kvalitetsförbättringar och felkorrigeringar.

### Företagsledning

![Nytt](../assets/new.svg)<!-- B2B-4123 -->Administratörer kan nu hantera flera företag från ett enda konto med hjälp av butiksföretagsväljaren. Några viktiga fördelar:

- **Förenklad hantering för flera företag** - Nu kan administratörer övervaka flera företag från ett användarkonto, vilket eliminerar behovet av att skapa och hantera separata inloggningar för varje företag.
- **Effektiv företagsväxling** - Med ett intuitivt gränssnitt kan administratörer snabbt växla mellan företag och göra uppdateringar, vilket förbättrar produktiviteten vid hantering av flera enheter.
- **Effektivare åtgärder** - Regionala chefer och företagsledare kan hantera alla sina företag centralt, vilket ger snabbare beslutsfattande och smidigare affärsåtgärder.

Den här förbättringen bygger på B2B 1.5.0:s funktioner för medlemskap för flera företag, som gör att användare kan tillhöra flera företag, men som inte har stöd för administratörsåtkomst mellan olika företag. Företagets väljare eliminerar behovet av separata administratörskonton samtidigt som rätt åtkomstkontroll och företagsspecifika vyer bibehålls.

### Företag

![Korrigerat problem](../assets/fix.svg)<!-- B2B-4480 --> Ett problem där gästkunder skulle få ett `No such entity with cartId = ?`-felmeddelande när de loggade in som företagsanvändare med produkter i kundvagnen har åtgärdats.

### Förhandlingsbar offert

![Ett problem har korrigerats](../assets/fix.svg) I B2B v1.5.2-versionen finns följande korrigeringar för överlåtbara offerter:

- &#x200B;<!-- B2B-3252 -->Fältet [!UICONTROL Line Item Discount Amount] validerar indata för att förhindra att negativa rabattvärden anges.
- &#x200B;<!-- B2B-3224 -->Korrigerade ett användarupplevelseproblem där anteckningar för långradsobjekt trunkerades och var svåra att läsa för B2B-kunder.
- &#x200B;<!-- B2B-2865 -->B2B-kunder kan nu ange produktkvantiteter med hjälp av decimalvärden (till exempel 1.5 eller 2.75) när de skapar offerter.

### Offertmall

![Ny](../assets/new.svg)<!-- B2B-4104 --> funktion för B2B-köpare och säljare att bifoga externa dokumentlänkar till offertmallar. Med den här funktionen kan du länka till dokument som lagras i tjänster som DocuSign och Adobe Sign direkt från citattecken, vilket kompletterar den befintliga funktionen för bifogade filer. Några viktiga fördelar:

- Effektivt samarbete genom direkt åtkomst till viktiga avtal och kontrakt
- Förbättrad genomskinlighet med omedelbar tillgång till den senaste dokumentationen
- Snabbare offertförhandlingar eftersom man slipper ladda ned och ladda upp filer
- Flexibel dokumenthantering med externa dokumentvärdtjänster

## B2B 1.5.1

*11 februari 2025*

[!BADGE Säkerhetsuppdateringar som stöds]{type=Informative tooltip="Stöds"} av Adobe Commerce version 2.4.7-p4+ och 2.4.6-p9+.
Kompatibel med Adobe Commerce version 2.4.8-beta1 till 2.4.8-beta2, 2.4.7 till 2.4.7-p3, 2.4.6 till 2.4.6-p8

B2B v1.5.1-versionen innehåller kvalitetsförbättringar och felkorrigeringar.

### Företag

![Korrigerat problem](../assets/fix.svg)<!-- B2B-4422 --> Om en kund försöker byta företag på sidan Offertinformation dirigerar systemet nu om kunden till en *Åtkomst nekad* -sida för att säkerställa att en offert som skapats för ett företag inte kan användas för att göra en beställning med ett annat företags priser. Tidigare kunde en användare skapa en offert med priset för ett företag och sedan byta till ett annat företag för att lägga en order med olika priser.

### Rabatter för radartiklar

![Korrigerat problem](../assets/fix.svg)<!-- B2B-2938 --> Förbättrad systemeffektivitet genom att åtgärda en prestandaförsämring som observerats i offertberäkningsscenariot. Tidigare lades två nya enheter till i varje vagnsradsobjekt, vilket ledde till en märkbar ökning av databasförfrågningar, vilket ledde till lägre prestanda.

### Förhandlingsbar offert

![Ett problem har korrigerats](../assets/fix.svg)<!-- B2B-3820 --> Systemet behåller nu positionen för gränssnittselement när JavaScript-validering tillämpas på fälten *[!UICONTROL min/max qty]* på mallsidan för Luma Storefront-offert. Tidigare förändrades andra gränssnittselement på sidan om du tillämpade JavaScript-validering på dessa fält.

### Kundvagn

![Korrigerat problem](../assets/fix.svg)<!-- B2B-4222 --> Introducerade ett nytt kundvagnshanteringssystem som utformats för att effektivisera shoppingupplevelsen för användare som hanterar flera företagskonton. Det nya systemet kopplar kundvagnar till enskilda företag i stället för till kundkontot för att effektivisera shoppingupplevelsen och förbättra arbetsflödet genom att stödja följande funktioner.

- **Företagsspecifika varukorgar:** - Kundvagnarna är nu kopplade till enskilda företag för att stödja företagsspecifika priser och produktalternativ.
- **Sömlös växling** - Användare kan enkelt växla mellan olika företagskonton utan att innehållet i respektive företags kundvagn påverkas.
- **Sammanhangsbaserad integritet** - All kundvagnsinformation finns kvar i respektive företags kontext, vilket ger en konsekvent och tillförlitlig shoppingupplevelse.

## B2B 1.5.0

*30 oktober 2024*

[!BADGE Säkerhetsuppdateringar som stöds i &#x200B;]{type=Informative tooltip="Stöds"} Adobe Commerce version 2.4.7-p3+ och 2.4.6-p8+.
Kompatibel med Adobe Commerce version 2.4.8-beta1, 2.4.7 till 2.4.7-p2, 2.4.6 till 2.4.6-p7.

Adobe Commerce B2B version 1.5.0 är även kompatibel med PHP 8.3 och stöder [GraphQL Application Server](https://experienceleague.adobe.com/sv/docs/commerce-operations/performance-best-practices/concepts/application-server).

B2B v1.5.0 innehåller nya funktioner, kvalitetsförbättringar och felkorrigeringar.

>[!NOTE]
>
> Lär dig mer om bakåtkompatibla ändringar (BIC) som introducerades i B2B 1.5.0 genom att granska markeringar och referensinformation i avsnittet [Bakåtkompatibla ändringar](backward-incompatible-changes.md).

### Företagshantering

![Nytt](../assets/new.svg) **Företagshantering**<!--B2B-2901--> - Nu kan affärsfolk visa och hantera Adobe Commerce-företag som hierarkiska organisationer genom att tilldela företag till utsedda överordnade företag. När ett företag har tilldelats en överordnad kan administratören för det överordnade företaget hantera företagskontot. Endast behöriga administratörsanvändare kan lägga till och hantera företagstilldelningar. Mer information finns i [Hantera företagshierarki](manage-company-hierarchy.md).

- Lägg till och hantera företagstilldelningar från det nya *[!UICONTROL Company Hierarchy]*-avsnittet på sidan *[!UICONTROL Company Account]* i Admin.

- Sortera och filtrera företag efter den nya *[!UICONTROL Company Type]*-inställningen. I företagsrutnätet anger kolumnen *[!UICONTROL Company Type]* om ett företag är ett enskilt företag eller en del av organisationshierarkin (överordnat eller underordnat).

![Nytt](../assets/new.svg) **Hantera företagskonfiguration i skala**<!--B2B-2849--> - Ändra företagskonfigurationsinställningar snabbt för utvalda företag med hjälp av gruppåtgärden *[!UICONTROL Change company setting]* som nu är tillgänglig när du hanterar företag från rutnätet *[!UICONTROL Companies]* eller *[!UICONTROL Company Hierarchy]*. Om du till exempel skapar en ny delad katalog för en grupp företag kan du ändra den delade katalogkonfigurationen i en enda åtgärd i stället för att redigera varje företag individuellt.

![Nya](../assets/new.svg) API-utvecklare kan använda den nya REST API-slutpunkten `/V1/company/{parentId}/relations` för företagsrelationer för att skapa, visa och ta bort företagstilldelningar. Se [Hantera företagsobjekt](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) i *Utvecklarhandbok för webb-API*.

### Företagskonton

![Nytt](../assets/new.svg)<!--B2B-2828--> **Flerföretagstilldelning** - Förenkla åtkomst till företagskonton för företagsanvändare genom att tilldela en användare till flera företag. Om du till exempel har en köpare som beställer från flera företagswebbplatser, skapar du ett enda konto och tilldelar alla företag som köparen arbetar med till det kontot. Sedan kan köparen logga in en gång och växla mellan olika företagskonton genom att välja företaget från butiken.

>[!NOTE]
>
>En företagsanvändare kan tilldelas till flera företag, men kan bara vara företagsadministratör för ett företag.

![Nytt](../assets/new.svg) <!--B2B-2747--> **Företagsomfångsväljare** - Ger möjlighet för företagsanvändare som har tilldelats flera företag att ändra företag i butiken. När omfånget ändras uppdateras data för att visa information baserat på det nya företagssammanhanget. Om det nya företaget till exempel använder en annan delad katalog, ser företagsanvändaren produkter, priser och annan information baserat på den nya delade katalogen. Innehåll som rör order, offerter och offertmallar uppdateras också baserat på det valda företagets sammanhang.

>[!NOTE]
>Innehållet i kundvagnen återspeglar artiklar som valts av den aktuella kunden. Om kunden har en aktiv kundvagn och väljer ett annat företag uppmanas de att uppdatera kundvagnen för att återspegla produktsortiment, priser och kampanjrabatter baserat på det nya företagssammanhanget. Produkter som inte är tillgängliga i den katalog som är kopplad till det nya företaget tas bort från kundvagnen. Om produkten har ett annat pris eller en annan tillgänglighet uppdateras kundvagnen så att den återspeglar tillgängliga data i det valda företagets kontext.<!--B2B-4222-->

![Korrigerat problem](../assets/fix.svg)<!--ACP2E-1933--> Företagsadministratörer kan nu lägga till företagsanvändare från butiken. Tidigare loggade Commerce ett fel när en Admin-användare försökte lägga till en ny användare: `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`.

### Offerter och offertmallar

Förbättrade offertfunktioner hjälper köpare och säljare att hantera offerter och offertförhandlingar mer effektivt.

![Nya](../assets/new.svg) **Offertmallar**—<!--B2B-3367-->Köpare och säljare kan nu effektivisera offertprocessen genom att skapa återanvändbara och anpassningsbara offertmallar. Med offertmallar kan offertförhandlingen slutföras en gång, och köpare kan generera på förhand godkända länkade offerter för återkommande order i stället för att gå igenom offertförhandlingen för varje order. Offertmallar utökar de befintliga offertfunktionerna genom att lägga till följande avancerade funktioner:

- **Beställningströsklar** tillåter säljarna att ange minsta och högsta orderåtaganden, vilket säkerställer att köparen följer de avtalade inköpsvolymerna.
- **Genom att ställa in minsta och högsta antal artikelorderkvantiteter** får köparen flexibilitet att justera orderkvantiteter för den länkade offerten utan att det krävs en ny mall eller ytterligare förhandling.
- **Spåra antalet länkade offerter som genererats och slutfört order** för att få insikter om hur förhandlingsavtalen uppfylls.
- **Länkade offerter** är förgodkända offerter som köparen genererar från en aktiv offertmall för att skicka återkommande order baserat på de villkor som förhandlats i offertmallen.

![Nytt](../assets/new.svg) **Förbättringar av befintliga offertfunktioner**

- **Uppdaterade ACL-regler (Commerce Access Control List)** gör det möjligt för B2B-hanterare och ansvariga att hantera offerter och offertmallar för underordnade användare. Separata regler har stöd för detaljerad konfiguration för att visa, redigera och ta bort åtkomst.

- **Spara offert som utkast**<!--B2B-2566--> - När en [offertförfrågan](quote-request.md) skapas från kundvagnen kan köpare nu spara offerten som ett utkast så att de kan granska och uppdatera den innan offertförhandlingen inleds med säljaren. Utkastofferten har inget förfallodatum. Köpare kan granska och uppdatera offertutkast från avsnittet [!UICONTROL My Quotes] på sin kontokontrollpanel.

- **Byt namn på offert**<!--B2B-2596--> - Nu kan köpare ändra ett offertnamn från sidan [Offertdetaljer](account-dashboard-my-quotes.md#quote-actions) genom att välja alternativet **[!UICONTROL Rename]**. Det här alternativet är tillgängligt för auktoriserade köpare när de redigerar offerten. Namnändringshändelser registreras i offerthändelseloggen.

- **Duplicera offert**<!--B2B-2701--> - Nu kan köpare och säljare skapa en ny offert genom att kopiera en befintlig offert. En kopia skapas från offertdetaljvyn genom att välja **[!UICONTROL Create Copy]** i [offertdetaljvyn](quote-price-negotiation.md#button-bar) i Admin eller [Storefront](account-dashboard-my-quotes.md#quote-actions).

- **Flytta offertobjekt till rekvisitionslista**<!--B2B-2755--> - Nu kan köpare ta bort produkter från en offert och spara dem i en rekvisitionslista om de bestämmer sig för att inte ta med dem i offertförhandlingen.

- **Ta bort flera produkter från en offert**<!--B2B-2881--> - På offerter med ett stort antal produkter kan köpare nu ta bort flera produkter från offerten genom att markera dem och använda alternativet *[!UICONTROL Remove]* från kontrollen *[!UICONTROL Actions]* på offertdetaljsidan. I tidigare versioner var en köpare tvungen att ta bort produkter en gång.

- **Låsning av rabattrader**<!--B2B-2597--> - Under offertförhandling kan säljarna använda låsning av radrabjekt för större flexibilitet när de tillämpar rabatter under offertförhandlingen. En säljare kan till exempel tillämpa en särskild artikelrabatt på en artikel och låsa artikeln för att förhindra ytterligare rabatter. När en artikel är låst kan artikelpriset inte uppdateras när en rabatt på offertnivå används. Se [Initiera offert för en köpare](sales-rep-initiates-quote.md).

![Ett problem har korrigerats](../assets/fix.svg) **Korrigeringar för befintliga offertfunktioner**

- Handlare som klickar på knappen *[!UICONTROL Print]* i offertdetaljvyn i Admin uppmanas nu att spara offerten som en PDF. Tidigare omdirigerades handlarna till en sida med offertinformation. <!--ACP2E-1984-->

- Tidigare när en kundoffert med `0` procent och varierande kvantitet skickades genereras ett undantag, men kvantiteten sparades. När den här korrigeringen har tillämpats genereras ett fel för `0 percentage` med ett meddelande. <!--ACP2E-1742-->

- Under offertförhandlingen kan en säljare nu ange en `0%`-rabatt i fältet Förförhandlad offertrabatt och skicka offerten tillbaka till köparen. Om säljaren tidigare angav en rabatt på 0 % och skickade offerten tillbaka till köparen returnerade administratören ett `Exception occurred during quote sending`-felmeddelande. <!--ACP2E-1742-->

- ReCaptcha-validering fungerar nu korrekt under utcheckningsprocessen för ett B2B-citat när ReCaptcha V3 har konfigurerats för utcheckning i butiken. Tidigare misslyckades valideringen med ett `recaptcha validation failed, please try again`-felmeddelande.  <!--ACP2E-2097-->

### Inköpsorder

![Åtgärdat problem](../assets/fix.svg) <!--ACP2E-1825-->Inköpsorder kan inte längre placeras av en användare som är associerad med företaget efter att företaget har blockerats. Tidigare kunde en användare som är associerad med företaget göra inköpsorder när företaget blockerades.

## B2B v1.4.2-p5

*8 april 2025*

[!BADGE Säkerhetsuppdateringar som stöds]{type=Informative tooltip="Stöds"} Adobe Commerce 2.4.7-p5+ och 2.4.6-p10+.

![Nytt](../assets/new.svg) Kompatibilitet med säkerhetsuppdateringar för Adobe Commerce 2.4.7-p5+ och 2.4.6-p10+ har lagts till.

![Åtgärdat problem](../assets/fix.svg) Innehåller de säkerhetskorrigeringar som beskrivs i [Säkerhetsbulletin APSB25-26](https://helpx.adobe.com/se/security/products/magento/apsb25-26.html).

{{b2b-compatibility}}

## B2B v1.4.2-p4

*11 februari 2025*

[!BADGE Säkerhetsuppdateringar som stöds &#x200B;]{type=Informative tooltip="Stöds"} Adobe Commerce 2.4.7-p4+ och 2.4.6-p9+.

![Nytt](../assets/new.svg) Kompatibilitet med säkerhetsuppdateringar för Adobe Commerce 2.4.7-p4+ och 2.4.6-p9+ har lagts till.

![Åtgärdat problem](../assets/fix.svg) Innehåller de säkerhetskorrigeringar som beskrivs i [Säkerhetsbulletin APSB25-08](https://helpx.adobe.com/se/security/products/magento/apsb25-08.html).

{{b2b-compatibility}}

## B2B v1.4.2-p3

*8 oktober 2024*

[!BADGE Säkerhetsuppdateringar som stöds &#x200B;]{type=Informative tooltip="Stöds"} Adobe Commerce 2.4.7-p3+ och 2.4.6-p8+.

![Nytt](../assets/new.svg) Kompatibilitet med säkerhetsuppdateringar för Adobe Commerce 2.4.7-p3+ och 2.4.6-p8+ har lagts till.

![Åtgärdat problem](../assets/fix.svg) Innehåller de säkerhetskorrigeringar som beskrivs i [Säkerhetsbulletin APSB24-73](https://helpx.adobe.com/se/security/products/magento/apsb24-73.html).

{{b2b-compatibility}}

## B2B v1.4.2-p2

[!BADGE Säkerhetsuppdateringar som stöds &#x200B;]{type=Informative tooltip="Stöds"} Adobe Commerce 2.4.7-p2+ och 2.4.6-p7+.

![Nytt](../assets/new.svg) Kompatibilitet med säkerhetsuppdateringar för Adobe Commerce 2.4.7-p2+ och 2.4.6-p7+ har lagts till.

![Åtgärdat problem](../assets/fix.svg) Innehåller de säkerhetskorrigeringar som beskrivs i Säkerhetsbulletin xxxx.

{{b2b-compatibility}}

## B2B v1.4.2-p1

*9 augusti 2024*

[!BADGE Säkerhetsuppdateringar som stöds &#x200B;]{type=Informative tooltip="Stöds"} Adobe Commerce 2.4.7-p1+ och 2.4.6-p6+.

![Nytt](../assets/new.svg) Kompatibilitet med säkerhetsuppdateringar för Adobe Commerce 2.4.7-p1+ och 2.4.6-p6+ har lagts till.

{{b2b-compatibility}}

## B2B v1.4.2

*10 oktober 2023*

[!BADGE Stöds]{type=Informative tooltip="Stöds"} Adobe Commerce version 2.4.7 och version från 2.4.6 till 2.4.6-p5.

B2B v1.4.2-versionen innehåller kvalitetsförbättringar och felkorrigeringar.

![Korrigerat problem](../assets/fix.svg) <!--B2B-2897-->Om en säljare skapar en köpoffert som innehåller en produkt-SKU som inte är tillgänglig i den delade katalog som är associerad med köpföretaget visas felmeddelandet `The SKU you entered is not available in the shared catalog. Please check the SKU and try again`.  Säljaren kan inte spara offerten förrän han eller hon tar bort den produkt som inte är tillgänglig. Tidigare sparades offerten med en SKU som inte var tillgänglig och det gick inte att läsa in offerten i butiken.

>[!IMPORTANT]
>
>Adobe Commerce B2B version 1.4.2+ är kompatibel med PHP 8.2. Om du uppgraderar Commerce-instansen till version 2.4.7+ måste du se till att den använder PHP-version 8.2 för att bibehålla kompatibiliteten med Adobe Commerce B2B-versionen. Dessutom stöder inte B2B 1.4.2+ för närvarande [GraphQL Application Server](https://experienceleague.adobe.com/sv/docs/commerce-operations/performance-best-practices/concepts/application-server).

## B2B v1.4.1

*7 augusti 2023*

[!BADGE Stöds]{type=Informative tooltip="Stöds"} [Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html?lang=sv-SE). Kompatibel med Adobe Commerce 2.4.7-beta1.

B2B v1.4.1-versionen innehåller kvalitetsförbättringar och felkorrigeringar.

![Åtgärdat problem](../assets/fix.svg) <!--ACP2E-1825-->Inköpsorder kan inte längre placeras av en användare som är associerad med företaget efter att företaget har blockerats. Tidigare kunde en användare som är associerad med företaget göra inköpsorder när företaget blockerades.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1943-->Status för restorder av produkt visas nu korrekt i butiken. Tidigare identifierades produkter som var tillgängliga för leverans felaktigt som beställda.

![Ett problem har korrigerats](../assets/fix.svg) <!--ACP2E-1862-->Om företagsregistreringsformuläret innehåller ett attribut för kundfiltyp, inkluderas filen som överfördes under registreringsprocessen nu i kontoinformationen för företagsadministratören när företaget har skapats. Tidigare saknades den bifogade filen.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1793-->Färgväljaren för en konfigurerbar produkt visas nu som förväntat på konfigurationssidan för rekvisitionslistobjektet. Tidigare visades väljaren för färgrutor som ett listrutefält på konfigurationssidan för rekvisitionslistobjekt.

![Ett problem har korrigerats](../assets/fix.svg) <!--ACP2E-1968-->När [GraphQL-frågan](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) används för att returnera företagsinformation returneras resultat nu utan fel.

## B2B v1.4.0

*13 juni 2023*

[!BADGE Stöds]{type=Informative tooltip="Stöds"} [Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html?lang=sv-SE). Kompatibel med Adobe Commerce 2.4.7-beta1

Den här versionen innehåller nya funktioner och förbättringar för B2B-överlåtbara offerter och flera felkorrigeringar.

![Nytt](../assets/new.svg) Kompatibilitet med Adobe Commerce 2.4.7-beta1 har lagts till.

![Nytt](../assets/new.svg) **Offerter som initierats av säljaren** - Nu kan säljare initiera en offert för en köpare direkt från rastret Offert och Kund i administratören. Detta effektiviserar offertprocessen och minskar kundens komplexitet. Om en kund inte har initierat en order kan en säljare snabbt skapa en offert för kundens räkning och påbörja förhandlingsprocessen. Tidigare gick det endast att skapa offerter från butiken av köparen eller av en säljare som är inloggad som kund.

![Nytt](../assets/new.svg) **Rabatter och förhandling för radobjekt**—<!--B2B-2440--> Inom en offert kan B2B-köpare och säljare nu förhandla på radobjektsnivå och tillämpa rabatter och utbyta anteckningar tills ett avtal nås. Kommentarer som skapas och uppdateras inkluderas i radobjektet och offerthistoriken för att spåra kommunikationen. Tidigare kunde köpare och säljare bara växla noteringar och tillämpa rabatter på offertnivån.

![Korrigerat problem](../assets/fix.svg) Adobe Commerce visar nu korrekt information under betalningen när alternativet Inköpsorder är aktiverat och en virtuell offert som skapades med betalningsalternativet PayPal har valts. Tidigare visades summorna som noll under dessa villkor.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1504--> Valideringsfel uppstår inte längre när du försöker spara ett företag med en kreditgräns som överstiger 999. Tidigare infogades en kommaavgränsare för företagskreditgränser som var större än 999, vilket orsakade ett valideringsfel som hindrade uppdateringar från att sparas.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1474--> Den valda leveransadressen ändras inte när du gör en beställning med en överlåtbar offert. Tidigare ändrades den valda leveransadressen till standardleveransadressen när du gjorde en beställning.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1429--> I Store Configuration-inställningarna för B2B-funktioner inaktiveras nu fältet **[!UICONTROL Enable Shared Catalog direct products price assigning]** automatiskt. I butiken döljs den när inställningen **[!UICONTROL Enable Company]** eller **[!UICONTROL Enable Shared Catalog]** är inställd på **[!UICONTROL No]**.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1683--> När ett företagskonto skapas från butiken validerar Commerce nu e-postadressen innan företagsregistreringen bearbetas. Om e-postadressen är ogiltig misslyckas åtgärden och inga kontouppdateringar bearbetas. Tidigare skapades ett kundkonto även om begäran om att skapa ett företagskonto misslyckades på grund av en ogiltig e-postadress.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1664--> Produktartiklar som innehåller dubbla citattecken i den delade katalogen och prisstrukturen orsakar inte längre fel i administratören.

![Korrigerat problem](../assets/fix.svg) <!--ACP2E-1498--> Varnish-konfigurationen för Commerce-programmet har uppdaterats för att förhindra att gästanvändare ser data från andra kundgrupper.

### Känt fel

Om du installerar eller uppgraderar B2B 1.4.0 på [Adobe Commerce version 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html?lang=sv-SE) inträffar följande fel:

```
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

Du kan åtgärda det här problemet genom att lägga till manuella beroenden för B2B-säkerhetspaketet genom att lägga till manuella beroenden för B2B-säkerhetspaketet med en [stabilitetstagg](https://getcomposer.org/doc/04-schema.md#package-links). Instruktioner finns i [Adobe Commerce Knowledge Base](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html?lang=sv-SE).

## B2B v1.3.5-p10

*8 april 2025*

[!BADGE Säkerhetsuppdateringar för Adobe Commerce 2.4.6-p10+ stöds]{type=Informative tooltip="Stöds"}.

![Nytt](../assets/new.svg) Kompatibilitet med säkerhetsuppdateringar för Adobe Commerce 2.4.6-p10 har lagts till.

![Åtgärdat problem](../assets/fix.svg) Innehåller de säkerhetskorrigeringar som beskrivs i [Säkerhetsbulletin APSB25-26](https://helpx.adobe.com/se/security/products/magento/apsb25-26.html).

## B2B v1.3.5-p9

*11 februari 2025*

[!BADGE Säkerhetsuppdateringar för Adobe Commerce 2.4.6-p9+ stöds]{type=Informative tooltip="Stöds"}.

![Nytt](../assets/new.svg) Kompatibilitet med säkerhetsuppdateringar för Adobe Commerce 2.4.6-p9 har lagts till.

![Åtgärdat problem](../assets/fix.svg) Innehåller de säkerhetskorrigeringar som beskrivs i [Säkerhetsbulletin APSB25-08](https://helpx.adobe.com/se/security/products/magento/apsb25-08.html).

## B2B v1.3.5-p8

*8 oktober 2024*

[!BADGE Säkerhetsuppdateringar för Adobe Commerce 2.4.6-p8+ stöds]{type=Informative tooltip="Stöds"}.

![Nytt](../assets/new.svg) Kompatibilitet med säkerhetsuppdateringar för Adobe Commerce 2.4.6-p8 har lagts till.

![Åtgärdat problem](../assets/fix.svg) Innehåller de säkerhetskorrigeringar som beskrivs i [Säkerhetsbulletin APSB24-73](https://helpx.adobe.com/se/security/products/magento/apsb24-73.html).

## B2B v1.3.5-p7

*9 augusti 2024*

[!BADGE Säkerhetsuppdateringar för Adobe Commerce 2.4.6-p7+ stöds]{type=Informative tooltip="Stöds"}.

![Nytt](../assets/new.svg) Kompatibilitet med säkerhetsuppdateringar för Adobe Commerce 2.4.6-p7 har lagts till.

## B2B v1.3.5

*14 mars 2023*

[!BADGE Stöds]{type=Informative tooltip="Stöds"} Adobe Commerce 2.4.0 - 2.4.6 och senare versioner

![Nytt](../assets/new.svg) B2B-version 1.3.5-p2 har släppts för kompatibilitet med Adobe Commerce 2.4.6-p2.

![Nytt](../assets/new.svg) B2B-version 1.3.5-p1 har släppts för kompatibilitet med Adobe Commerce 2.4.6-p1.

>[!NOTE]
>
>När du har uppgraderat Commerce från 2.4.6 till den [senaste utgåvan](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html?lang=sv-SE#2.4.6) måste du uppdatera till den version av B2B 1.3.5 som stöds. Eller uppgradera B2B-tillägget från version 1.3.5 till version 1.4.0 eller senare för att få de senaste funktionerna.

![Nytt](../assets/new.svg) Stöd för Adobe Commerce 2.4.6 har lagts till.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-689--> Adobe Commerce visar nu korrekt information under betalningen när alternativet Inköpsorder är aktiverat och en virtuell offert som skapades med betalningsalternativet PayPal har valts. Tidigare visades summorna som noll under dessa villkor.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-609--> Listan över kundgrupper för inställningen **Tillåt bläddring i kategori** innehåller inte längre kundgrupper som är relaterade till delade kataloger.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-1244--> Kundattributet Skatt/momsregistreringsnummer fungerar nu som väntat med företagsadministratörskonton både i Admin och i butiken. Attribut för moms krävs inte längre för att skapa ett företagskonto. Tidigare när en handlare skapade ett företagskonto med ett eget attribut för moms, hade Adobe Commerce ett valideringsfel både i butiken och i Admin.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-1236--> Det går nu korrekt att inaktivera funktionen för delad katalog i ett specifikt omfång. Tidigare angav Adobe Commerce ett ogiltigt omfång när en handlare sparade en delad katalogkonfiguration.

![Ett problem har korrigerats](../assets/fix.svg) <!--- ACP2E-1203--> Administratörsanvändare kan nu spara anpassade attributvärden för kunder för företagsanvändare. Tidigare gick det inte att spara anpassade kundattribut för företagsanvändare.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-1221--> Prestandaproblem har lösts med valideringen av företagsbehörigheter som tillhandahålls via GraphQL när många företagsbehörigheter redan har tilldelats.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-1242--> Adobe Commerce genererar inte längre ett fel på kundvagnssidan när Snabborder används för att lägga till en produkt i en kvantitet som överskrider det tillgängliga lagret.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-1090--> Prestandan för `SELECT` företagsbehörighetsåtgärder har förbättrats.

![Åtgärdat problem](../assets/fix.svg) <!--- ACP2E-2456--> Kategorifrågor returnerar nu produktpriser enligt butikens konfigurationsinställningar när det inte finns någon kategoribehörighet uttryckligen angiven för kategorin som frågas.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-6829--> Knappen **[!UICONTROL Place Order]** fungerar nu som väntat när du slutför ett köp med en godkänd offertförfrågan. Problem med den överlåtbara offerten `negotiableQuoteCheckoutSessionPlugin` har lösts.

## B2B v1.3.4-p12

*8 april 2025*

[!BADGE Stöds]{type=Informative tooltip="Stöds"} Adobe Commerce 2.4.0 och senare versioner

![Nytt](../assets/new.svg) Stöd för Adobe Commerce 2.4.5-p12 har lagts till.

![Åtgärdat problem](../assets/fix.svg) Innehåller de säkerhetskorrigeringar som beskrivs i [Säkerhetsbulletin APSB25-26](https://helpx.adobe.com/se/security/products/magento/apsb25-26.html).

## B2B v1.3.4-p11

*11 februari 2025*

[!BADGE Stöds]{type=Informative tooltip="Stöds"} Adobe Commerce 2.4.0 och senare versioner

![Nytt](../assets/new.svg) Stöd för Adobe Commerce 2.4.5-p11 har lagts till.

![Åtgärdat problem](../assets/fix.svg) Innehåller de säkerhetskorrigeringar som beskrivs i [Säkerhetsbulletin APSB25-08](https://helpx.adobe.com/se/security/products/magento/apsb25-08.html).

## B2B v1.3.4-p10

*9 oktober 2024*

[!BADGE Stöds]{type=Informative tooltip="Stöds"} Adobe Commerce 2.4.0 och senare versioner

![Nytt](../assets/new.svg) Stöd för Adobe Commerce 2.4.5-p10 har lagts till.

![Åtgärdat problem](../assets/fix.svg) Innehåller de säkerhetskorrigeringar som beskrivs i [Säkerhetsbulletin APSB24-73](https://helpx.adobe.com/se/security/products/magento/apsb24-73.html).

## B2B v1.3.4

*9 augusti 2022*

[!BADGE Stöds]{type=Informative tooltip="Stöds"} Adobe Commerce 2.4.0 och senare versioner

![Nytt](../assets/new.svg) Stöd för Adobe Commerce 2.4.5 har lagts till.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-453-->Adobe Commerce skickar inte längre e-postmeddelanden varje gång ett befintligt företag uppdateras av ett API-anrop. Mejl skickas nu endast när ett företag skapas.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-406-->Adobe Commerce beräknar nu korrekt totalsumman för en överlåtbar offert när skatteberäkningsinställningen **[!UICONTROL Enable Cross Border Trade]** är aktiverad.

![Ett problem har korrigerats](../assets/fix.svg) <!--- ACP2E-322-->Konfigurerbara produkter har flyttats till den sista positionen i produktlistan när Stock har uppdaterats när inställningen **[!UICONTROL Move out of stock to the bottom]** är aktiverad. En ny anpassad databasfråga har implementerats för att säkerställa att sorteringsordningen i Elasticsearch index nu följer den administratörsaktiverade sorteringsordningen. Tidigare flyttades inte konfigurerbara produkter och deras underordnade produkter längst ned i listan när den här inställningen var aktiverad.

![Ett problem som har korrigerats](../assets/fix.svg) <!--- ACP2E-308-->E-postmeddelandet om inköpsorder följer nu inställningen för e-postsändning för varje webbplats i en multisitedistribution. En kontroll för inställningen **[!UICONTROL Disable Email Communications]** har lagts till i den anpassade logiken för e-postköer. Tidigare respekterade inte Adobe Commerce inställningen för e-postsändning för den sekundära webbplatsen.

![Ett problem har korrigerats](../assets/fix.svg) <!--- ACP2E-302-->Titeln på SKU-fältet på sidan Snabbordning har ändrats för att bli tydligare.

![Korrigerat fel](../assets/fix.svg) <!--- ACP2E-543-->Adobe Commerce visar nu ett mer informativt felmeddelande när en kund anger en ogiltig SKU i fältet **Ange SKU eller produktnamn**.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-1753-->Fältet **[!UICONTROL Account Created in]** för en företagsadministratör behåller nu det värde som du förväntade dig när du har sparat företaget.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-722 -->Frågan `customer` returnerar inte längre tomma resultat när den hämtar rekvisitionslistor som filtrerats av `uid`.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-210 -->Ett plugin-program lades till före `collectQuoteTotals`-anropet för att säkerställa att butikskrediter bara används en gång.

![Ett problem har korrigerats](../assets/fix.svg) <!--- ACP2E-665 -->Kunder omdirigeras nu till inloggningssidan när deras konto tas bort av en administratör från administratören. Tidigare inträffade ett fel i Adobe Commerce. Plugin-programkodblocket (`SessionPlugin`) finns nu inuti `try…catch` -blocket. Den här koden har inte paketerats i det generiska undantagshanteringsblocket.

![Ett problem har korrigerats](../assets/fix.svg) <!--- ACP2E-661 --> På snabbbeställningssidan i mobilläge när du trycker på **Retur** efter att du angett ett giltigt produktnamn eller SKU visas nu nästa fält som förväntat.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-607 -->Företagsnamnet visas nu som förväntat i fakturerings- och leveransadressavsnitten i arbetsflödet för utcheckning.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-375 -->Butikskrediten är inte tillgänglig när betalningsmetoden **[!UICONTROL Zero Subtotal Checkout]** är inaktiverad. Kryssrutan Butikskrediter kunde inte användas vid orderplacering från administratören. Programmet gjorde ingen beställning med butikskrediten och visade följande fel: `The requested Payment Method is not available`.

## B2B v1.3.3

*9 augusti 2022*

[!BADGE Stöds]{type=Informative tooltip="Stöds"} Adobe Commerce 2.4.0 och senare versioner

![Nytt](../assets/new.svg) Stöd för Adobe Commerce 2.4.4 har lagts till.

![Korrigerat problem](../assets/fix.svg) <!--- MC-41985--> Den tid som krävs för att uppgradera från Adobe Commerce 2.3.x till Adobe Commerce 2.4.x i distributioner med mer än 100 000 företagsroller har reducerats avsevärt.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42153--> POST `V1/order/:orderId/invoice`-begäran stöder nu skapande av partiella fakturor när betalningsmetoden **[!UICONTROL Payment on Account]** är aktiverad. Tidigare inträffade följande fel i Adobe Commerce: `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`. [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![Korrigerat problem](../assets/fix.svg) <!--- MC-41975--> PayPal Payflow Pro fungerar nu som väntat med B2B-överlåtbar offert när kundvagnen innehåller andra produkter. Adobe Commerce kan nu bearbeta beställningen och skicka ett e-postmeddelande till kunden som förväntat. Tidigare inträffade ett allvarligt fel i Adobe Commerce och ett bekräftelsemeddelande som innehöll nollvärden skickades via e-post till kunden.

![Korrigerat problem](../assets/fix.svg) <!--- MC-41819--> Sidnumreringen visas nu korrekt på katalogsökresultatsidan efter att vissa produkter har utelämnats i en delad katalog.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42886--> Kundanpassade attribut sparas nu som förväntat när en företagsanvändare skapas eller sparas i Admin.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42927--> Knappen **[!UICONTROL Submit]** i formuläret Skapa nytt företag inaktiveras nu efter en klickning för att förhindra att flera formulär skickas. Tidigare kunde du skicka in formuläret flera gånger genom att klicka på knappen upprepade gånger, vilket genererade ett fel.

![Ett problem som har åtgärdats](../assets/fix.svg) <!--- MC-42787--> Adobe Commerce visar inte längre länken för att ordna om i butiken när en kund loggar in i en butik där ombeställningar har inaktiverats.

![Ett problem har korrigerats](../assets/fix.svg) <!--- MC-43115--> Snabbsorteringssökning med SKU är nu skiftlägeskänsligt när delad katalog är aktiverad.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42203--> Du kan nu uppdatera en fil för ett kundattribut när du skapar ett företag. Tidigare när du försökte skapa ett företag med en bifogad fil av typen `File`, skapade inte Adobe Commerce företaget och loggade det här felet i undantagsloggen: `Something went wrong while saving file`.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42242--> Du kan nu skapa ett företag med ett kundkonto som har ett anpassat attribut av typen (`File`) eller (`Image`). Tidigare gick det inte att matcha inläsaren för företagets redigeringssida om kontot hade något av dessa anpassningsbara alternativ, vilket hindrade redigering av företagsinformation.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42268--> Frågan `products` returnerar nu ett korrekt `total_count`-fält när delad katalog är aktiverad.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42203--> Du kan nu uppdatera en fil för ett kundattribut när du skapar ett företag. Tidigare när du försökte skapa ett företag med en bifogad fil av typen `File`, skapade inte Adobe Commerce företaget och loggade det här felet i undantagsloggen: `Something went wrong while saving file`.

![Korrigerat problem](../assets/fix.svg) <!--- MC-43178--> Sidorna _Företagskonfiguration_ och _Skapa företag_ fungerar nu som förväntat när du har inaktiverat en onlineseveransmetod. Verifiering har lagts till för att förhindra att försök görs att bearbeta inaktiverade leveransmoduler. Tidigare visade Adobe Commerce följande fel: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42214--> Sidan _Kategori_ visar nu konsekventa produktdata medan behörigheter genereras under partiell indexering. En ny partiell indexerare för katalogbehörigheter har lagts till i den här processen. Tidigare var de data som visades när indexeraren kördes felaktiga.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42567--> Frågan `categoryList` returnerar nu korrekt antal produkter när katalogbehörigheter används och produkter tilldelas till en delad katalog.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42528--> Frågan `categoryList` respekterar nu kategoribehörigheter och returnerar endast tillåtna kategorier. Tidigare returnerades alla tilldelade och ej tilldelade kategorier.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42399--> `rest/V1/company/{id}`-begäran returnerar nu `is_purchase_order_enabled` attributvärden som förväntat.

![Åtgärdat problem](../assets/fix.svg) <!--- ACP2E-128--> Anpassade kundattribut visas nu som förväntat på fliken _Företagsadministratör_.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-130--> Min önskelista på sidan Mitt konto visas nu som förväntat för företagsadministratörer och företagsanvändare.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-133--> Snabborderfel visas inte längre i kundvagnen. Tidigare visade Adobe Commerce det här felet i kundvagnen när SKU inte hittades i katalogen: `The SKU was not found in the catalog`.

![Åtgärdat problem](../assets/fix.svg) <!--- ACP2E-194--> Åtgärden för att spara delade kataloger har optimerats för att kunna köras snabbare. Tidigare kunde det ta flera minuter att spara en delad katalog med många kundgrupper.

![Korrigerat problem](../assets/fix.svg) <!--- MC-42240--> Adobe Commerce tar nu bort alla underkategoribehörigheter från tabellen `sharedcatalog_category_permissions` när den överordnade kategorin tas bort. Tidigare togs endast överordnade kategoridata bort.

## B2B v1.3.2

*29 augusti 2022*

[!BADGE Stöds]{type=Informative tooltip="Stöds"} Adobe Commerce 2.4.0 och senare versioner

![Nytt](../assets/new.svg) Stöd för Adobe Commerce 2.4.3 har lagts till.

![Korrigerat problem](../assets/fix.svg) <!--- MC-39862--> Adobe Commerce skickar nu uppdateringsmeddelanden via e-post om utgångna överlåtbara offerter. När en överlåtbar offert hade gått ut skickade Adobe Commerce inte ut några e-postmeddelanden med uppdateringar.

![Korrigerat problem](../assets/fix.svg) <!--- MC-40682--> Adobe Commerce skickar nu e-postmeddelanden om att de snart ska upphöra att gälla och utgånget, överlåtbara offerter när ett `cron`-jobb saknas.

### Företag

![Korrigerat problem](../assets/fix.svg) <!--- MC-41542--> Listrutan Skapa nytt företagskonto visar inte längre tomma alternativvärden. Tidigare var de två första alternativvärdena och landskoden `AN` tomma.

![Korrigerat problem](../assets/fix.svg) <!--- MC-41260--> Om du klickar på knappen **[!UICONTROL Return]** för en order som har skapats av en företagsanvändare dirigeras nu en administrativ användare till sidan Skapa retursida som förväntat. Administratören har tidigare omdirigerats till sidan Orderhistorik.

![Korrigerat problem](../assets/fix.svg) [!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."} <!--- MC-40798--> Adobe Commerce misslyckas inte längre med ett minnesfel när metoden `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` körs under `bin/magento setup:upgrade`. Tidigare använde Adobe Commerce inte batchstorlek för att samla in när behörigheter initierades, utan i stället lästes in en samling med alla företagsroller.

![Ett problem har korrigerats](../assets/fix.svg) <!--- MC-40551--> Företagsanvändare kan nu redigera och uppdatera anpassade attributvärden för kunder. Tidigare var dessa attribut inte korrekt kopplade till formuläret för att skapa och redigera användare. En företagsanvändare kunde ange olika attributvärden, men Adobe Commerce sparade inte dessa värden korrekt.

![Korrigerat problem](../assets/fix.svg) <!--- MC-32653--> Resursträdet för behörigheter för företagsroller kan nu översättas som förväntat. Tidigare översattes inte behörighetsträdet trots att det fanns giltiga översättningsfiler.

![Korrigerat problem](../assets/fix.svg) <!--- MC-40358--> Adobe Commerce sparar nu anpassade kundattributvärden för B2B-användare som förväntat. Tidigare uppstod ett mallfel när ett företagskonto som innehöll anpassade kundattribut skapades och Adobe Commerce kunde inte läsa in formuläret. Problemet löstes genom att ett argument lades till i layouten för `company_create_account`.

![Korrigerat problem](../assets/fix.svg) <!--- MC-41721--> Företagsanvändarfilter som Visa alla användare, Visa aktiva användare och Visa inaktiva användare fungerar nu som förväntat. Tidigare orsakade filtreringsåtgärder på företagets användarsida ett JavaScript-fel.

### Företagskrediter

![Ett problem har korrigerats](../assets/fix.svg) <!--- MC-41551--> Administratörer med begränsade konton som endast har webbplatsprivilegier kan nu skapa ett företag som använder en annan valuta än webbplatsen.

![Korrigerat problem](../assets/fix.svg) <!--- MC-41523--> Adobe Commerce skickar nu företagsmeddelanden från rätt `from` e-postadress och omfattning. Tidigare övervägde Adobe Commerce inte webbplatsens omfattning när man skickade företagskredittilldelning eller uppdaterat e-post.

### Snabbordning

![Korrigerat problem](../assets/fix.svg) <!--- MC-42104--> Det går nu som väntat att skapa en beställning med hjälp av snabbordning från en CSV-fil med SKU:er som inte finns.

![Korrigerat problem](../assets/fix.svg) <!--- MC-40268--> Det går nu som väntat att använda snabbordning för att söka efter flera SKU:er. Tidigare innehöll resultaten dubblettposter.

![Korrigerat problem](../assets/fix.svg) <!--- MC-40261--> Listan med tillagda produkter hanterar nu SKU:er som anges med gemener och versaler på samma sätt när du använder SKU:er för att välja flera produkter under Snabbordning.

![Ett problem har korrigerats](../assets/fix.svg) <!--- MC-40225--> när snabbbeställning användes har nu lagt till produkter i den kvantitet som anges av kunden. Tidigare lade Adobe Commerce bara till en produkt även om mängden köpare överstiger ett.

![Ett problem har korrigerats](../assets/fix.svg) <!--- MC-41283--> Funktionen för automatisk komplettering av snabbordning fungerar nu med partiella SKU:er.

![Korrigerat problem](../assets/fix.svg) <!--- MC-41299--> Adobe Commerce visar nu produkter som har konfigurerats som **Inte visas individuellt** på snabbordersidans lista över automatiska förslag och sökresultat.

![Ett åtgärdat problem](../assets/fix.svg) <!--- MC-42402--> Köpare kan nu använda snabbbeställningsformuläret för att lägga till flera produkter från SKU:er som innehåller versaler. Tidigare lades endast den första produkten till.

### Förhandlingsbar offert

![Korrigerat problem](../assets/fix.svg) <!--- MC-41232--> Köpare omdirigeras nu till sidan med överlåtbara offerter efter att länken till ett överlåtbart offertfält har klistrats in i URL-fältet och inloggningen har slutförts. Tidigare omdirigerades kunderna till sidan Mitt konto.

![Korrigerat problem](../assets/fix.svg) <!--- MC-39317--> Ombeställning fungerar nu som väntat för order som innehåller en produkt med alternativet för datumanpassning för ett kundkonto som skapades vid utcheckning. Tidigare bearbetades inte ändringsordningen av Adobe Commerce och följande fel visades: `The product has required options. Enter the options and try again`.

![Korrigerat problem](../assets/fix.svg) <!--- MC-39063--> Leveransadressen för en överlåtbar offert kan inte längre redigeras under utcheckning när inköpsordermodulen är inaktiverad. Det här beteendet är ett resultat av en tidigare korrigering där `isQuoteAddressLocked` togs bort från den utcheckningsbara offertrenderaren.

![Korrigerat problem](../assets/fix.svg) <!--- MC-38967--> Merchants kan nu lägga till produkter i en överlåtbar offert från administratören.

### Inköpsorder

![Korrigerat problem](../assets/fix.svg) <!--- MC-39983--> Adobe Commerce visar nu ett informativt felmeddelande som väntat när du gör en inköpsorder med PayPal Express Checkout när attributet **[!UICONTROL Name Prefix]** är inställt på `required`. Tidigare gjorde Adobe Commerce ingen beställning och inget felmeddelande visades.

![Ett problem har korrigerats](../assets/fix.svg) <!--- MC-39620--> Gränssnittskomponenten för faktureringsadressen i modulen Inköpsorder använder nu offertadressen korrekt när Google Tag Manager är aktiverat. Tidigare inträffade ett JavaScript-fel på betalningssidan.

### Rekvisitionslistor

![Korrigerat problem](../assets/fix.svg) <!--- MC-40426--> Merchants kan nu använda POST `rest/all/V1/requisition_lists`-slutpunkten för att skapa en rekvisitionslista för en kund. Tidigare inträffade detta 400-fel i Adobe Commerce när du försökte skapa en rekvisitionslista: `Could not save Requisition List`.

![Ett problem har korrigerats](../assets/fix.svg) <!--- MC-41123--> Knappen **[!UICONTROL Add to Requisition List]** visas nu för en kundvagns produkter i lager när vagnen även innehåller produkter som inte finns i lager. Tidigare visades inte knappen _[!UICONTROL Add to Requisition List]_&#x200B;för någon av produkterna om en varukorg innehöll två produkter, varav en inte fanns i lager.

![Korrigerat problem](../assets/fix.svg) <!--- MC-40877--> Du kan nu använda REST API för att lägga till en produkt i en rekvisitionslista.

![Korrigerat problem](../assets/fix.svg) <!--- MC-40155--> Värden för rekvisitionslista **[!UICONTROL Latest Activity Date]** följer nu språkformatet.

![Korrigerat problem](../assets/fix.svg) <!--- MC-39580--> Adobe Commerce genererar inte längre ett allvarligt fel när du redigerar en paketprodukt från en rekvisitionslista.

![Korrigerat problem](../assets/fix.svg) <!--- MC-40454--> Adobe Commerce visar nu rätt produktpris när du lägger till en produkt med ett anpassningsbart alternativ `(File)` i en önskelista från en rekvisitionslista. Länken till den överförda filen visas också som förväntat. Tidigare visade Adobe Commerce felaktiga produktpriser och inte länken till filen.

![Korrigerat problem](../assets/fix.svg) <!--- MC-36383--> Produkter med ett anpassningsbart alternativ `(File)` kan nu läggas till i en kundvagn från en rekvisitionslista.

### Delad katalog

![Korrigerat problem](../assets/fix.svg) <!--- MC-40497--> En administratör med en roll som är begränsad till en viss webbplats kan nu skapa, visa och redigera en delad katalog. Tidigare uppstod ett allvarligt fel i Adobe Commerce när en administratör med en begränsad roll försökte skapa en delad katalog.

![Åtgärdat problem](../assets/fix.svg) <!--- MC-41337--> Navigeringsresultaten i lager innehåller nu ett korrekt antal produkter med filtrerade attribut, och kunderna kan nu använda flera filter. Tidigare kunde bara ett filter användas och Adobe Commerce visade ett felaktigt produktantal vid navigering i lager.

![Korrigerat problem](../assets/fix.svg) <!--- MC-40779--> Adobe Commerce visar nu produktantal korrekt i navigeringsfilter i lager i sökresultat. Tidigare använde inte ett plugin-program för sökresultatsidan Elasticsearch utan skickade en ny fråga till databasen.

![Åtgärdat problem](../assets/fix.svg) <!--- MC-39978--> Adobe Commerce tar inte längre bort nivåpriser när en handlare tar bort alla produkter från en delad standardkatalog.

![Åtgärdat problem](../assets/fix.svg) <!--- MC-39802--> Filter filtreras nu efter den aktuella kategorin och visas korrekt på alla sidor när delade kataloger är aktiverade. Tidigare beräknades filter felaktigt enbart för den aktuella sidan och filtrerades inte av den aktuella kategorin.

![Korrigerat problem](../assets/fix.svg) <!--- MC-39522--> GraphQL `products`-frågan returnerar inte längre en produkts prisintervall och kategori för produkter som inte har tilldelats till en delad katalog när delad katalog är aktiverad. Tidigare returnerade frågan produktens aggregeringar, även om själva produkten inte returnerades i `items`-arrayen.

## B2B v1.3.1

*9 februari 2021*

[!BADGE Stöds]{type=Informative tooltip="Stöds"} Adobe Commerce 2.4.0 och senare versioner

![Nytt](../assets/new.svg) Stöd för Adobe Commerce 2.4.2 har lagts till.

![Nya](../assets/new.svg) onlinebetalningsmetoder stöds nu för inköpsorder.

![Korrigerat problem](../assets/fix.svg) Om en konfigurerbar produkt läggs till i kundvagnen direkt från en rekvisitionslista när produkten användes i en tidigare order returneras inte längre något systemfel.

![Korrigerat problem](../assets/fix.svg) Adobe Commerce visar nu fliken Kräver mitt godkännande korrekt för inköpsorder när en delad databaskonfiguration distribueras.

![Åtgärdat problem](../assets/fix.svg) Adobe Commerce visar nu information om paketprodukter och presentkort när du visar inköpsorder.

![Korrigerat problem](../assets/fix.svg) Shoppare omdirigeras nu som förväntat efter inloggning på deras konto när de surfar i en butik där **[!UICONTROL Website Restriction]** är aktiverat och **[!UICONTROL Restriction Mode]** är inställd på `Private Sales: Login Only`. Tidigare omdirigerades kunderna till butikens hemsida. <!--- MC-38934-->

![Åtgärdat problem](../assets/fix.svg) Orderhistoriken läses nu in som förväntat på en företagsadministratörs kontokontrollpanelssida i distributioner med en B2B-företagshierarki som innehåller många kunder (större än 13000). Tidigare lästes orderhistoriken in långsamt eller inte alls och Adobe Commerce visade ett 503-fel. <!--- MC-38830-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce visar inte längre flera identiska varningsmeddelanden när du lägger till en okonfigurerad produkt med anpassningsbara alternativ i en rekvisitionslista från en kategorisida. <!--- MC-38342-->

![Åtgärdat problem](../assets/fix.svg) Nya och duplicerade produkter visas nu som förväntat på kategorisidan när delade B2B-kataloger är aktiverade. <!--- MC-38307-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce behåller nu rätt `store_id` som är associerad med en företagsadministratör när kundgruppen för ett företag uppdateras. Tidigare ändrades `store_id` till standardbutiken när gruppen uppdaterades. <!--- MC-38196-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce sparar nu en grupperad produkt i en rekvisitionslista som en lista med enkla produkter på samma sätt som en grupperad produkt läggs till i en kundvagn. På grund av hur Adobe Commerce sparade grupperade produkter omdirigerades länken för en grupperad produkt från rekvisitionslistan alltid till enkla produkter och inte till den grupperade produkten. <!--- MC-38049-->

![Korrigerat problem](../assets/fix.svg) Du kan nu filtrera order efter fältet **[!UICONTROL Company Name]** när du exporterar orderinformation i CSV-format. Tidigare loggade Adobe Commerce ett fel i `var/export/{file-id}`. <!--- MC-37785-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce visar nu popup-fönstret Skapa rekvisitionslista som förväntat när du väljer fliken Skapa ny rekvisitionslista i butiken. <!--- MC-37915-->

![Åtgärdat problem](../assets/fix.svg) Rekvisitionslistor innehåller nu alla grupperade produkter och kvantiteter som har lagts till i listan. Tidigare, när en handlare navigerade till en rekvisitionslista efter att ha lagt till produkter på en produktinformationssida, visade Adobe Commerce följande fel: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![Korrigerat problem](../assets/fix.svg) Den korrekta butiksvyn är nu associerad med den relevanta webbplatsen när du skapar ett företag i en distribuering med flera platser. Tidigare kunde du inte skapa ett företag och Adobe Commerce visade följande fel: `The store view is not in the associated website`. <!--- MC-37488-->

![Korrigerat problem](../assets/fix.svg) Om du beställer produkter via SKU med Snabbordning skapas inte längre dubbla produktkvantiteter i CSV-filen. <!--- MC-37427-->

![Ett problem har korrigerats](../assets/fix.svg) Knappen **[!UICONTROL Add to Cart]** blockeras inte längre när _[!UICONTROL Enter Multiple SKUs]_-avsnittet på sidan Snabbordning innehåller ett tomt värde. I stället visas ett meddelande i Adobe Commerce där du uppmanas att ange giltiga SKU:er. <!--- MC-37387-->

![Korrigerat problem](../assets/fix.svg) Det här meddelandet visas nu på produktsidan när du skickar en produktgranskning från en rekvisitionslista: `You submitted your review for moderation`. Granskningen visas också på sidan Väntande granskningar (Admin **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**). Tidigare, trots att Adobe Commerce lade till granskningen i listan över väntande granskningar, uppstod ett 404-fel på produktsidan. <!--- MC-37119-->

![Ett problem har korrigerats](../assets/fix.svg) Prestandan för konsumenten `sharedCatalogUpdateCategoryPermissions` har förbättrats. När du har skapat en delad katalog använder katalogbehörighetsindexeraren nu bara kundgrupp-ID:t från den delade katalogen, inte alla kundgrupper. <!--- MC-36770-->

![Åtgärdat problem](../assets/fix.svg) Anpassade fält för kundadressattribut som är kopplade till en köpares icke-standardadress sparas nu som förväntat i arbetsflödet för utcheckning i bakgrunden. <!--- MC-36630-->

![Ett problem har korrigerats](../assets/fix.svg) Beställningar för produkter som tillhör en butiks delade standardkatalog kan nu placeras för kunder via Admin REST API (`rest/V1/carts/{<CART_ID>/items`) som förväntat. Adobe Commerce kontrollerar nu om produkten har tilldelats en offentlig katalog innan den har validerats för delad katalogbehörighet i `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave`. Tidigare lade Adobe Commerce inte till produkten i kundvagnen och returnerade följande fel: `No such shared catalog entity`. <!--- MC-36535-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce skickar nu e-postmeddelanden om nya företagsanvändare från Adobe Commerce-butikens adress. Tidigare skickades det här e-postmeddelandet från företagets administratörsadress. <!--- MC-36480-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce kontrollerar nu anpassade attribut för duplicering av reserverade företagsattributnamn innan en handlare tillåts spara ett nytt attribut. <!--- MC-36282-->

![Åtgärdat problem](../assets/fix.svg) Frågan `credit_history` returnerar nu det angivna företagets kredithistorik för både det ursprungligen allokerade beloppet och det köpta beloppet. Tidigare returnerade frågan ett fel.

![Åtgärdat problem](../assets/fix.svg) Fälten **[!UICONTROL Company]** och **[!UICONTROL Job Title]** på sidan Redigera kontoinformation kan inte längre redigeras.

### Kända fel

- B2B-köpare kan använda onlinebetalningsmetoder för att kringgå det vanliga inköpsorderflödet. Detta scenario kan inträffa om köparen kan minska den totala utcheckningen till 0 (till exempel med en kampanjkod eller presentkort) och sedan ta bort koden eller presentkortet. Även under dessa omständigheter lägger Adobe Commerce fortfarande order på rätt belopp baserat på priserna på artiklarna i deras tilldelade katalog. **_Tillfällig lösning_**: Inaktivera presentkort och kupongkoder när onlinebetalningsmetoder har aktiverats för godkännande av inköpsorder. <!--- B2B-1603-->

- Köpare dirigeras om till kundvagnen när de försöker lägga en order från en inköpsorder med PayPal Express Checkout när **[!UICONTROL In-Context Mode]** är inaktiverat. <!--- B2B-1604-->

- Adobe Commerce visar ibland ett 404-fel när en köpare skapar en inköpsorder och sedan navigerar till utcheckningssidan. Det här felet inträffar när en köpare tidigare har skapat en annan inköpsorder med en onlinebetalningsmetod innan han/hon går till utcheckningssidan utan att slutföra det föregående köpet. Köparen kan fortfarande göra inköpsordern. **_Arbeta runt_**: Ingen. <!--- B2B-1605-->

- Rabatterna för en viss betalningsmetod gäller även vid utcheckning av en inköpsorder även när köparen ändrar sin betalningsmetod under den slutliga utcheckningen. Det innebär att kunderna får en rabatt som de inte har rätt till. Det här problemet inträffar eftersom en kundvagnsregel för den ursprungliga betalningsmetoden fortfarande tillämpas trots att betalningsmetoden har ändrats. **_Arbeta runt_**: Ingen. Se den kända utgåvan av [Adobe Commerce 2.4.2 B2B: Rabatten gäller fortfarande för onlineinköpsorder när betalningsmetoden har ändrats.](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html?lang=sv-SE) _Kunskapsbasen_ är en artikel. <!-- B2B-1012 -->

- Frågan `deleteRequisitionListOutput` returnerar information om listan med borttagna rekvisitioner i stället för de återstående rekvisitionslistorna. <!--- MC-39894-->

## B2B v1.3.0

*15 oktober 2020*

[!BADGE Stöds]{type=Informative tooltip="Stöds"} Adobe Commerce 2.4.0 och senare versioner

Den här versionen innehåller förbättringar av ordergodkännanden, leveransmetoder, kundvagn och loggning av administratörsåtgärder.

![Nytt](../assets/new.svg) Stöd för Adobe Commerce 2.4.1 har lagts till.

![Nya](../assets/new.svg) B2B-ordergodkännanden har förbättrats för att förbättra användbarheten och möjliggöra massåtgärder på inköpsorder.

![Nya](../assets/new.svg) B2B-handlare kan nu styra leveransmetoder som erbjuds varje företag.<!--- BUNDLE-160 161 162 -->

![Ny](../assets/new.svg)-handlare kan nu tillåta användare att rensa innehållet i kundvagnen i en enda åtgärd och konfigurera funktionen separat på varje webbplats <!--- BUNDLE-108 -->

![Nya](../assets/new.svg) B2B-köpare kan nu lägga till enskilda artiklar eller hela innehållet i kundvagnen direkt i en rekvisitionslista. <!--- BUNDLE-145 144-->

![Nya](../assets/new.svg) B2B-handlare kan skapa beställningar från administratören å kundernas vägnar med Betalning på konto som betalningsmetod. <!--- BUNDLE-166 178-->

![Nytt](../assets/new.svg)-handlare kan nu direkt visa alla offerter som är kopplade till en användare från kundens detaljsida. <!--- BUNDLE-139 -->

![Nyheter](../assets/new.svg)-handlare kan nu filtrera rutnätet för kunder nu online efter företag. <!--- BUNDLE-137 -->

![Nya](../assets/new.svg) administratörer kan nu filtrera kunder i Admin efter säljare. <!--- BUNDLE-110 -->

![Nytt](../assets/new.svg) För att minska antalet falska konton och skräppostkonton kan handlare nu aktivera Google reCAPTCHA i formuläret New Company Request i butiken. <!--- BUNDLE-154 -->

![Nya](../assets/new.svg) administratörsåtgärder som vidtas i företagsmodulerna är nu loggade i Admin Actions Log. Åtgärder loggas från alla relevanta företagsmoduler: `Company`, `NegotiableQuote`, `CompanyCredit`, `SharedCatalog`. <!--- BUNDLE-180 181 182 183 -->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce visar inte längre knappen **[!UICONTROL Delete customer]** på sidan **Kunder** när den inloggade administratören inte har behörighet att ta bort kunder i distributioner där B2B är installerat. <!--- MC-35655-->

![Åtgärdat problem](../assets/fix.svg) Kundgruppen ändras inte längre automatiskt för en kund som tilldelas ett företag när du redigerar kunden i kundrutnätet. <!--- MC-35254-->

![Ett problem har korrigerats](../assets/fix.svg) När en handlare skapar en delad katalog anges nu behörigheterna automatiskt till `Allow` för funktionerna **[!UICONTROL Display Product Prices]** och **[!UICONTROL Add to Cart]** i kategorierna när kundgruppen tilldelas den här åtkomsten i katalogens behörighetsinställningar. Tidigare var de här inställningarna automatiskt inställda på `Deny` även när katalogbehörigheterna var inställda på `Allow`.<!--- MC-34792-->

![Korrigerat problem](../assets/fix.svg) Behörigheter för kategorin Delad katalog skrivs inte längre över när en produkt redigeras från produktredigeringssidan.<!--- MC-34777-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce skickar nu ett e-postmeddelande som bekräftar att en kund har behörighet att överskrida den angivna kreditgränsen när en handlare aktiverar inställningen **[!UICONTROL Allow To Exceed Credit Limit]**. Tidigare angav det e-postmeddelande som Adobe Commerce skickade att kunden inte hade behörighet att överskrida gränsen. <!--- MC-34584-->

![Korrigerat problem](../assets/fix.svg) HTML-behållaren som omger produktpriset i rekvisitionslistor återges nu korrekt för underordnade produkter i paketerade produkter. <!--- MC-36331-->

![Korrigerat problem](../assets/fix.svg) Marknadsförare kan nu ange vilket språk som företagets användar-e-post ska skickas på när ett företag skapas i flerspråkiga distributioner. Tidigare visades inte den nedrullningsbara menyn som gör det möjligt för handlarna att välja rätt butiksvy och språk.  <!--- MC-35777-->

![Åtgärdat problem](../assets/fix.svg) Fälten för anpassade kundadressattribut visas nu som förväntat i arbetsflödet för utcheckning av lagerlokal. <!--- MC-35607-->

![Korrigerat problem](../assets/fix.svg) Konfigurationsfliken för B2B-funktioner öppnas nu korrekt. <!--- MC-35458-->Gäster kan nu använda QuickOrder för att lägga till produkter i kundvagnen och sedan ta bort artiklar. Tidigare togs produkten inte bort när en kund använde QuickOrder för att lägga till flera produkter i kundvagnen och sedan tog bort en produkt. <!--- MC-35327-->

![Korrigerat problem](../assets/fix.svg) Ett företag kan nu uppdateras med REST API PUT `/V1/company/:companyId` -begäran utan att ange `region_id` när tillståndet är konfigurerat som **inte obligatoriskt**. Tidigare inträffade ett fel i Adobe Commerce om `region_id` inte hade angetts, trots att  inte krävdes. <!--- MC-35304-->

![Korrigerat problem](../assets/fix.svg) När du skapar eller uppdaterar ett B2B-företag med REST API (`http://magento.local/rest/V1/company/2`, där `2` representerar företags-ID), innehåller svaret nu inställningarna för `applicable_payment_method` eller `available_payment_methods` som förväntat. <!--- MC-35248-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce visar inte längre en 404-sida när en handlare använder knappen **Retur** i stället för att klicka på knappen **[!UICONTROL Save]** när de skapar en rekvisitionslista i butiken.<!--- MC-35094-->

![Korrigerat problem](../assets/fix.svg) Kategoribehörigheter ändras inte längre när en ny produkt tilldelas till en offentlig delad katalog. Tidigare har kategoribehörigheter duplicerats. <!--- MC-34386-->

![Korrigerat problem](../assets/fix.svg) REST API-slutpunkten PUT `rest/default/V1/company/{id}`, som används för att uppdatera företagets e-post, är inte längre skiftlägeskänslig. <!--- MC-34308-->

![Åtgärdat problem](../assets/fix.svg) Inaktivering av belöningsmoduler påverkar inte längre B2B-funktioner på kundkonton. Tidigare visades inte följande B2B-relaterade flikar när belöningsmoduler inaktiverades: Företagsprofil, företagsanvändare samt roller och behörigheter.<!--- MC-34191-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce använder nu rätt avsändarnamn i e-postmeddelanden när ändringar görs i företagskonton. Tidigare använde Adobe Commerce det allmänna kontaktavsändarnamnet som definierats i standardomfånget för alla e-postmeddelanden. <!--- MC-33917-->

![Korrigerat problem](../assets/fix.svg) Du kan nu implementera multileverans för order som innehåller både fysiska och virtuella produkter. <!--- MC-33818-->

![Korrigerat problem](../assets/fix.svg) Merchants kan nu skapa företagsanvändare från avsnittet _[!UICONTROL Company Users]_&#x200B;på sidorna Mitt konto och Företagsstruktur när **[!UICONTROL Access Restriction]**&#x200B;är aktiverat och **[!UICONTROL Restriction Mode]**&#x200B;är inställd på `Sales: Login Only`. Tidigare inträffade det här felet i Adobe Commerce när en handlare försökte skapa en användare: `Can not register new customer due to restrictions are enabled`. <!--- MC-33608-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce återställer inte längre en kunds kundgrupp till standardvärdet när en kund sparar sin kontoinformation. <!--- MC-33554-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce genererar inte längre ett allvarligt fel när en administratör tilldelar en kund som har en aktiv kundvagn till en kundgrupp. <!--- MC-33313-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce tillhandahåller nu en `addToCart` DataLayer-händelse för listsidor för snabbordning och rekvisitioner.  <!--- MC-33295-->

![Korrigerat problem](../assets/fix.svg) E-postmeddelanden som skickas till säljare som tilldelats ett företag innehåller nu den tilldelade företagslogotypen. Tidigare innehöll e-postmeddelandet den förvalda LUMA-logotypen, inte den överförda företagslogotypen. <!--- MC-33232-->

![Åtgärdat problem](../assets/fix.svg) En rekvisitionslista innehåller nu alla grupperade produkter och kvantiteter som har lagts till i listan. Tidigare, när en handlare navigerade till en rekvisitionslista efter att ha lagt till produkter på en produktinformationssida, visade Adobe Commerce följande fel: `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![Ett problem har korrigerats](../assets/fix.svg) Frågan `products` returnerar nu ett korrekt `total_count`-fält när delad katalog är aktiverad. <!--- MC-42268-->

![Korrigerat problem](../assets/fix.svg) Sidorna Företagskonfiguration och Skapa företag fungerar nu som förväntat efter att du har inaktiverat en onlineseveransmetod. Verifiering har lagts till för att förhindra att försök görs att bearbeta inaktiverade leveransmoduler. Tidigare visade Adobe Commerce följande fel: `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`. <!--- MC-43178-->

![Korrigerat problem](../assets/fix.svg) Integrationstestets minnesförbrukning har reducerats, vilket förbättrar testprestanda och minskar tiden som krävs för att slutföra testet. <!--- AC-266-->

## B2B v1.2.0

*28 juli 2020*

[!BADGE Stöds]{type=Informative tooltip="Stöds"} Adobe Commerce 2.4.0 och senare versioner

![Nytt](../assets/new.svg) Stöd för Adobe Commerce 2.4.0 har lagts till.

![Ny](../assets/new.svg) Storefront Order Search, med ytterligare tack för Marek Mularczyk från [Divante](https://www.divante.com/) och communitymedlemmar.

![Nya](../assets/new.svg) inköpsorder har förbättrats och skrivits om. De ingår nu som standard i Adobe Commerce.

![Nya](../assets/new.svg) regler för godkännande av inköpsorder har implementerats. Dessa regler gör att användare kan styra arbetsflödet för inköpsorder genom att skapa inköpsregler för order.

![Ny](../assets/new.svg) inloggning som kund ingår nu som standard i Adobe Commerce. Med den här funktionen kan webbplatspersonalen hjälpa kunderna genom att logga in som kunden för att se vad de ser.

![Åtgärdat problem](../assets/fix.svg) Attributaggregering fungerar nu korrekt för lagernavigering med Elasticsearch

![Ett problem har korrigerats](../assets/fix.svg) Sökordningarna efter specialtecken fungerar nu korrekt.

![Åtgärdat problem](../assets/fix.svg) Om du klickar på knappen **[!UICONTROL Clear All]** expanderas nu alla filter i stället för att de komprimeras.

![Åtgärdat problem](../assets/fix.svg) Produkt-SKU/namn ingår nu i sökfiltersammanfattningen för orderhistorik.

![Åtgärdat problem](../assets/fix.svg) Sorteringsindikatorn visas nu korrekt i stödrastret Mina inköpsorder.

![Korrigerat problem](../assets/fix.svg) Nu kan du bara klicka på knapparna Godkänn, Avbryt, Avvisa och Inköpsorder en gång. Tidigare kunde du klicka på knappen flera gånger.

![Korrigerat problem](../assets/fix.svg) Knapparna Godkänn, Avvisa, Avbryt och Validera återges nu korrekt på mobila enheter.

![Ett problem har korrigerats](../assets/fix.svg) Tidigare där en inköpsorder med en rabatt som har gått ut godkände orderns fulla belopp och inte inköpsordersumman uppdaterades. Nu uppdateras inköpsordersumman så att rätt summa visas.

![Korrigerat problem](../assets/fix.svg) Ett problem uppstod i 2.3.4 där anpassade tilläggsattribut inte skulle kopieras från kundadressen till offertadressen. Problemet har åtgärdats.

![Ett problem har korrigerats](../assets/fix.svg) När B2B är installerat visas ett SQL-fel när kategorier tilldelas till delade kataloger. Problemet har åtgärdats.

![Korrigerat problem](../assets/fix.svg) På grund av ett felaktigt variabeltypvärde kunde administratörer inte lägga till konfigurerbara produkter i en order. Alternativlistrutorna fyller inte i. Den här funktionen fungerar nu korrekt.

![Ett problem har korrigerats](../assets/fix.svg) Tidigare uppstod ett fel när kategoribehörigheter för gruppen Ej inloggad redigerades när ändringarna sparades. Problemet har åtgärdats.

![Ett problem har korrigerats](../assets/fix.svg). Butiksadministratörer kan lägga till produkter i en order som inte finns i den delade katalogen. Tidigare visades ett felmeddelande när ett objekt som inte finns i katalogen lades till.

![Ett problem har korrigerats](../assets/fix.svg) [!BADGE PaaS endast]{type=Informative url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."} Tidigare uppstod ett fel när kommandot `php bin/magento indexer:set-dimensions-mode catalog_product_price website` kördes och sedan en delad katalog skapades. Problemet har åtgärdats.

![Korrigerat problem](../assets/fix.svg) När ett företag lades till och företagsadministratören tilldelades en icke-standardwebbplats skickades fel webbplats-ID, vilket orsakade ett fel. Problemet har åtgärdats.

![Ett problem har korrigerats](../assets/fix.svg). När en kund flyttats till en annan kundgrupp gick det inte att lägga till en produkt i en beställning med _Snabbordning_. Problemet har åtgärdats.

![Ett fel ](../assets/fix.svg) har korrigerats vid försök att checka ut med WebAPI med ett B2B-citattecken. Ett felaktigt värde skickades till API:t, vilket orsakade att ett fel uppstod. Problemet har åtgärdats.

![Ett fel har korrigerats](../assets/fix.svg) Tidigare uppstod ett fel när ett företag ställdes in på &quot;Active&quot; via API:t. Problemet har nu åtgärdats.

![Korrigerat problem](../assets/fix.svg) På grund av en `form` -tagg som inte behövs uppdaterades ordersidan automatiskt när du tryckte på Retur efter att ha ändrat en föreslagen fraktkostnad. Problemet har åtgärdats.

![Ett fel uppstod när en produktvisningsgräns för en katalogsida angavs och gränsen var mindre än antalet totala produkter.](../assets/fix.svg) Funktionen fungerar nu som förväntat.

![Ett problem har korrigerats](../assets/fix.svg) Tidigare kopierades den ursprungliga administratörsadressen till den nya administratören när administratören för ett företag ändrades, och två adresser angavs. Nu läggs bara rätt adress till.

![Ett problem har korrigerats](../assets/fix.svg) Tidigare gick det inte att använda API:t för att spara ett offertobjekt när Git är inställt på Tillåten och Meddela kund. Detta API-anrop fungerar nu som förväntat.

![Åtgärdat problem](../assets/fix.svg) Fast produktskatt visas nu på informationssidan för offerter.

![Ett problem har korrigerats](../assets/fix.svg) Om du tidigare klickade på en bilaga på fliken Kommentarer på sidan Mina offerter kunde filen inte hämtas. Detta beteende fungerar nu som förväntat.

### Kända fel

- Adobe Commerce genererar ett undantag vid uppgradering till B2B 1.2.0 i en flerwebbplatsdistribution. När `setup:upgrade` körs inträffar det här felet i modulen `PurchaseOrder`: `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`. **Tillfällig lösning**: Installera `B2B-716 Add NonTransactionableInterface`-gränssnittet till snabbkorrigeringen `InitPurchaseOrderSalesSequence` för datakorrigering, som nu är tillgänglig från **Mitt konto** > **Hämtningar** i `magento.com`.
- Om en rabattkod förfaller innan en inköpsorder godkänns fortsätter inköpsordern att visa det rabatterade beloppet, men när inköpsordern har godkänts placeras ordern på den icke-rabatterade summan. **Tillfällig lösning**: Installera snabbkorrigeringen `B2B-709 Purchase Order Discount patch` för det här problemet, som nu är tillgänglig i avsnittet **Mitt konto** > **Hämtningar** i `magento.com`.
- Om artiklar i en inköpsorder inte finns i lager eller om det inte finns tillräckligt med kvantitet när inköpsordern konverteras till en faktisk order inträffar ett fel. Om restorder är aktiverade bearbetas ordern normalt.
