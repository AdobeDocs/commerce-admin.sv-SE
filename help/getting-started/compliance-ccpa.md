---
title: CCPA-kompatibilitet
description: Läs mer om California Consumer Privacy Act (CCPA), som utökar konsumenternas rättigheter i Kalifornien att avgöra hur deras personuppgifter samlas in, lagras och används.
exl-id: 165c8b78-683e-4015-b3c4-d3211750799e
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '2260'
ht-degree: 0%

---

# CCPA-kompatibilitet

>[!NOTE]
>
>Informationen är en del av ett antal ämnen som hjälper Adobe Commerce handlare och utvecklare att förstå vad Kaliforniens konsumentsekretesslag innebär. Informationen baseras på lagens text. Kontakta er advokat för att bekräfta om CCPA gäller ditt företag.

The [California Consumer Privacy Act][5] (CCPA) utvidgar konsumenternas rättigheter i Kalifornien när det gäller att fastställa hur deras personuppgifter samlas in, lagras och används. Dess betoning är att skydda konsumenterna mot otillåten försäljning eller otillåtet utbyte av eller deras personuppgifter. CCPA antogs 2018 och trädde i kraft den 1 januari 2020.

CCPA ger konsumenterna följande nya rättigheter:

- **Rätt att få veta** de kategorier av personuppgifter om dem som samlats in, använts, delats eller sålts under de senaste tolv månaderna.
- **Rätt att radera** vissa typer av personuppgifter som innehas av ett företag och/eller deras tjänsteleverantörer.
- **Rätt att avanmäla sig** om försäljningen av deras personuppgifter.
- **Rätt till icke-diskriminering** i termer av pris eller tjänst för att ha utövat en integritetsrätt enligt CCPA.

För CCPA definieras personuppgifter i detta sammanhang som:

>Information som identifierar, relaterar till, beskriver, kan kopplas till eller rimligen kan kopplas till, direkt eller indirekt, en viss konsument eller ett visst hushåll. (Avsnitt 1798.140)

I detta avseende omfattar den vissa dataelement som inte kan betraktas som personuppgifter inom ramen för andra lagar eller andra författningar. Handlarna bör tänka på detta när de avgör om och hur de ska följa lagen.

CCPA kräver också att företagen tillhandahåller _rimlig säkerhet_, och omfattar utökade dataskyddsbestämmelser för konsumenter, inklusive rätten att vidta rättsliga åtgärder om det föreligger en dataöverträdelse.

Kontakta ditt juridiska ombud för att fastställa om och hur ni ska uppfylla alla CCPA-krav som kan gälla för er och ert företag. Detta omfattar nya krav på meddelande, avanmälan och registrering som företag måste införa i enlighet med lagen.

## Affärskrav

CCPA gäller ideella företag som bedriver verksamhet i Kalifornien och som uppfyller något av följande:

- Har en årlig bruttointäkt på över 25 miljoner dollar
- Köp, ta emot eller sälja personuppgifter om minst 100 000 invånare, hushåll eller enheter i Kalifornien
- Få 50 % eller mer av årsinkomsterna från försäljning av personuppgifter för personer bosatta i Kalifornien.

## CCPA-överensstämmelseguide

I det här avsnittet finns en översikt på hög nivå över de steg som krävs för att handlare ska kunna följa sekretessbestämmelser, som California Consumer Privacy Act (CCPA).

### GDPR och CCPA

Om ditt företag måste uppfylla båda [Allmän dataskyddsförordning](compliance-gdpr.md) (GDPR) och CCPA kan ni använda en del av arbetet från era GDPR-kompatibilitetsprogram för CCPA. Även om reglerna har vissa likheter är det några skillnader:

- Definitionen av personuppgifter skiljer sig åt för de olika förordningarna.
- Den allmänna dataskyddsförordningen kräver att konsumenterna väljer att inte få använda sina personuppgifter för vissa ändamål. CCPA ger konsumenterna rätt att avanmäla sig.
- CCPA har ytterligare krav på datalager och datamappning.
- Reglerna har olika krav på integritetspolicy.

Företag som följer GDPR kan ha ytterligare skyldigheter enligt CCPA. Mer information finns i [CCPA-faktablad][3]{:target=&quot;_blank&quot;}.

### Vägkarta för regelefterlevnad

Det krävs en samordnad insats för att utveckla och genomföra en plan för att uppfylla kraven. Använd den här färdplanen som guide för att mobilisera resurser och prioritera uppgifter så att ni kan gå vidare på flera fronter. Processen är i stort sett densamma för alla [!DNL Commerce] installationer, med följande undantag:

- **Adobe Commerce i molninfrastruktur**: Handlare med butiker på Adobe [molninfrastruktur][4]{:target=&quot;_blank&quot;} kan be sin Adobe Commerce Technical Account Manager eller kundsupport om hjälp med att svara på konsumentförfrågningar.

- **Lokal**: Handlare med anläggningsinstallationer av Adobe Commerce eller Magento Open Source måste utveckla egna processer och verktyg för att hantera konsumentförfrågningar som rör sekretessbestämmelser.

#### Steg 1: Samla ihop ett funktionsövergripande team för att följa lagar och förordningar

Samla ihop ett team som representerar följande funktionella roller i ert företag och boka en utbildningssession för att få dem att komma igång med lagstiftningen. Tilldela sedan nödvändiga uppgifter till intressenter efter roll.

- Affärsstrategi och drift
- Juridisk
- Informationsteknik
- Användarupplevelse
- Kundtjänst
- Administrativt stöd

Ur ett affärsmässigt perspektiv måste ni avgöra om ert företag endast ska erbjuda kunderna i Kalifornien dessa integritetsskyddsåtgärder eller göra dem tillgängliga för alla konsumenter, oavsett var de befinner sig.

#### Steg 2: Inventera dina digitala egenskaper

**Intressenter:** Informationsteknik, juridisk och administrativ support

Ta reda på era digitala resurser, inklusive alla integreringar och vem som har tillgång till era konsumentdata.

1. Bestäm vilken offentlig och privat personlig information som samlas in via era webbplatser och mobilappar. En standarddatabas för Commerce lagrar till exempel följande typer av offentlig och privat personlig information:

   - **Offentlig**: Önsklistorna, produktrecensioner

   - **Privat**: Kundinformation, orderinformation, belöningspoäng, presentregister, adressbok, butikskrediter, betalningsmetoder, faktureringsavtal, nyhetsbrev, inbjudningar.

     Om [!DNL Commerce] installationen har anpassats, ytterligare personuppgifter kan samlas in. Personuppgifter kan också finnas i [cookies](./compliance-cookie-law.md), taggar och annan teknik som samlar in information.

1. Identifiera de parter som du delar data med. Förteckningen bör omfatta tjänsteleverantörer och tredje parter. Tredje parter omfattar annonsnätverk, internetleverantörer, dataanalytiker, myndigheter, operativsystem och plattformar, sociala nätverk och återförsäljare av konsumentdata som inte direkt samlar in personuppgifter från era konsumenter.

   - **Serviceföretag**: Enheter som har tillgång till dina konsumentdata för ett affärsmässigt ändamål och som tillhandahåller tjänster åt dig. Adobe är t.ex. tjänsteleverantör, liksom vissa utvecklare av anpassningar, tillägg och tjänster.

     Kontrollera standardinställningarna för Google Universal Analytics, Google Tag Manager och andra datatjänster som du använder och gör de ändringar som krävs för att följa reglerna. Mer information finns på [Sekretessinställningar för Google](../merchandising-promotions/google-tools.md#google-privacy-settings).

   - **Andra tredje parter**: Enheter som du delar eller säljer konsumentdata med. Du kan till exempel dela konsumentdata med ett annonsnätverk i utbyte mot reklam.

#### Steg 3: Kartlägg kundresan och datainsamlingsprocessen i era butiker

**Intressenter:** Användarupplevelse, informationsteknik, administrativ support

1. Identifiera varje punkt i [kundresa] där personuppgifter samlas in, och vilken typ av information som samlas in i varje steg.

   Besökare på webbplatsen måste meddelas i förväg eller vid datainsamlingen. En butik utan anpassade integreringar samlar till exempel in personuppgifter när ett kundkonto skapas och under utcheckningen. Om din butik har anpassade integreringar kan det finnas ytterligare dataobjekt och attribut att identifiera.

1. Se följande avsnitt för relevanta dataflödesdiagram och databastentitetsmappningar för respektive version:

   - [Referens till personuppgifter (2.x)][1]
   - [Referens till personuppgifter (1.x)][2]

   ![diagram](./assets/privacy-frontend-diagram.svg)

#### Steg 4: Upprätta rutiner och mekanismer för att besvara kundförfrågningar

**Intressenter:** Kundtjänst, informationsteknik, användarupplevelse, administrativ support

Ur datahanteringsperspektiv omfattar varje begäran om personuppgifter följande parter:

- **Dataobjekt** (Konsumenter): Enligt CCPA kan personer i Kalifornien som lämnar personuppgifter för att göra ett köp och/eller för att underhålla ett kundkonto begära åtkomst till eller radera sina personuppgifter.

- **Enheter som fungerar som företag inom ramen för CCPA** (Varumärken): [!DNL Commerce] handlare samlar in och lagrar personuppgifter från sina kunder och gäster som handlar i sina butiker.

- **Dataprocessor** (Teknikleverantörer): Adobe Commerce och Magento Open Source fungerar som behandlare av de personuppgifter som lagras som en del av de tjänster som tillhandahålls handlare. Som personuppgiftsbiträde behandlar Adobe personuppgifter i enlighet med handlarens tillstånd och instruktioner, i enlighet med licensavtalet.

Handlarna ansvarar för följande:

1. Identifiera de parter som är inblandade i begäran om åtkomst till registrerade personer (DSAR) och verifiera identiteten på den person som begär att få veta, avanmäla sig eller radera. Detta gäller en person som har ett lösenordsskyddat kundkonto, eller en som handlar i din butik som gäst.

1. informera en konsument som svar på deras begäran om rättigheter inom 45 dagar efter det att konsumenten har mottagit en kontrollerbar begäran, såvida detta inte är möjligt. (Lagen innehåller vissa andra krav för att ett företag ska uppfylla kraven för att kunna fortsätta uppfylla kraven vid förseningar på upp till 45 dagar till).

   Handlarna måste svara på varje enskild DSAR inom 45 dagar från och med den dag då begäran tas emot. Om det behövs kan handlarna ta upp till 45 dagar på sig att svara, i maximalt 90 dagar från den dag då begäran mottogs. Detta kräver att handlaren meddelar kunden om orsaken till förseningen.

1. Utveckla en mekanism för att presentera de meddelanden som krävs i er butik och samla in kundsvar.

1. Fastställa svarsförfaranden och dokumentera varje begäran om

   - **Begäranden att känna till** - Besökare i din butik måste informeras om alla arrangemang som du måste sälja eller dela med dig av deras personuppgifter till tredje part och få avanmäla dig. Detaljerna om hur du använder personuppgifter och vilka parter du delar eller säljer uppgifter med kan bevaras i din integritetspolicy.

   - **Begäranden att avanmäla** - Om personuppgifter säljs eller överförs till tredje part i utbyte mot vederlag krävs en _Sälj inte mina uppgifter_ länka vid varje punkt där den samlas in. Ytterligare användaraktiverade indatakontroller, som kryssrutor och knappar, kan användas i e-postmeddelanden, webbplatsinställningar eller i webbplatsformulär vid datainsamlingen för att skicka en giltig avanmälningsbegäran.

   - **Begäranden att radera**

      - Handlare vars butiker ligger hos Adobe Commerce Cloud bör kontakta Adobe Support för att få hjälp med att radera personuppgifter. Kontakta den tekniska kontohanteraren eller kundsupporten på Adobe för mer information.
      - Handlare som kör installationer av Adobe Commerce eller Magento Open Source lokalt måste implementera sin egen process och skript för att radera personuppgifter på begäran.

#### Steg 5: Skriv innehållet för de kundmeddelanden som krävs

**Intressenter:** Juridik, kundtjänst, användarupplevelse, informationsteknik, administrativ support

1. I samarbete med ditt juridiska ombud kan du fastställa vilka typer av meddelanden som ska läggas till på webbplatsen för att uppfylla CCPA-skyldigheterna.

   - **Meddelande om samling**: Ett meddelande som ges vid eller före tidpunkten då personuppgifter samlas in från konsumenten. Meddelandet ska vara skrivet på ett enkelt språk och lätt för den genomsnittliga personen att förstå. Meddelandet ska vara tydligt och tillgängligt på ett eller flera språk som motsvarar innehållet på din webbplats.

   - **Meddelande om rättighet att avanmäla sig**: Ett meddelande som informerar konsumenterna om deras rätt att avanmäla sig från försäljning av sina personuppgifter.

   - **Meddelande om ett finansiellt incitament**: Ett meddelande som förklarar varje ekonomisk fördel, pris eller tjänsteskillnad som ditt företag får i utbyte mot personuppgifter.

   - **Skicka in en begäran om insamling och användning av personuppgifter**: Instruktioner för enskilda att lämna in en begäran om att du lämnar ut de personuppgifter som du har samlat in om den enskilda personen, inklusive:

      - Specifika personuppgifter som du har samlat in om konsumenten
      - Kategorier av personuppgifter som du har samlat in om konsumenten
      - Kategorier av källor från vilka personuppgifterna samlas in
      - Kategorier av personuppgifter om konsumenten som du har sålt eller lämnat ut för ett affärssyfte
      - Kategorier av tredje parter till vilka personuppgifterna har sålts eller lämnats ut för ett ändamål som rör verksamheten
      - Orsakerna till varför ert företag samlar in och/eller säljer personuppgifter

1. Skicka innehållet till teamet och, om möjligt, till ditt juridiska ombud för granskning.

1. Bestäm var meddelandena ska visas, hur de ska fungera (för varje besök, vid autentisering eller vid klickning) och deras position och format i förhållande till annat innehåll.

1. Skicka det godkända innehållet till ditt utvecklingsteam.

#### Steg 6: Granska dina avtal med tjänsteleverantörer

**Intressenter:** Juridisk support

Granska och vid behov uppdatera alla tjänsteleverantörskontrakt för att återspegla CCPA-kraven.

#### Steg 7: Uppdatera din sekretesspolicy

**Intressenter:** Juridisk support

Granska din nuvarande integritetspolicy och överväg vilka ytterligare uppgifter som behövs, om några.

- **Användning av personuppgifter**: Du måste uppge vilka personuppgifter som samlas in och eventuella ekonomiska incitament som du får i utbyte mot försäljningen av personuppgifter. Ni måste också förklara hur incitamentet är tillåtet enligt CCPA och hur värdet av personuppgifterna beräknas.

- **Ålder för samtycke**: Om du samlar in eller använder personuppgifter om minderåriga kan du uppfylla följande krav:

   - **Underåriga &lt; 13**: Föräldratillstånd krävs för att minderåriga under 13 år ska kunna välja att inte sälja sina personuppgifter.

   - **Underåriga 13 till &lt; 16**: Underåriga som är minst 13 och yngre än 16 år kan välja att sälja sina personuppgifter, förutsatt att företaget fastställer en rimlig process för att dokumentera åtgärden. Processen måste beskrivas i företagets [integritetspolicy](privacy-policy.md). När ett företag tar emot förfrågningar från minderåriga i denna åldersgrupp måste det informera dem om deras rätt att avanmäla sig senare och förklara hur man gör det.

  >[!IMPORTANT]
  >
  >Handlare får inte lagra barns personuppgifter på [!DNL Commerce] plattform eller system. Om det finns anledning att tro att insamlade data tillhör en minderårig måste de tas bort från en [!DNL Commerce] plattformen omedelbart för att undvika brott mot Adobe licensvillkor.

#### Steg 8: Dokumentera alla relaterade procedurer och föra register

**Intressenter:** Kundtjänst, administrativ support

Under 24 månader efter att varje enskild begäran om rättigheter har tagits emot ska du föra ett register över begäran och ditt företags svar.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/security-and-compliance/reference/data-m2.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/security-and-compliance/reference/data-m1.html
[3]: https://oag.ca.gov/system/files/attachments/press_releases/CCPA%20Fact%20Sheet%20%2800000002%29.pdf
[4]: https://www.adobe.com/commerce/magento.html
[5]: https://oag.ca.gov/privacy/ccpa
