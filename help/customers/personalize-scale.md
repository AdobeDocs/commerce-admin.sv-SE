---
title: Anpassning i stor skala
description: Lär dig vilka funktioner i Adobe Commerce som gör att du kan skapa en personaliserad upplevelse för dina kunder.
feature: Customers, Storefront, Personalization
source-git-commit: a4eeda918adcb74ad5e7008b80eff703fa15e878
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 0%

---

# Anpassning i stor skala

&#x200B; personalisering i stor skala gör att företag kan personalisera shoppingupplevelsen för varje kundkontaktyta baserat på direkt sammanhang och tidigare observerat beteende. Målet är att presentera den mest relevanta och personaliserade upplevelsen varje gång.

Ladda ned [_Komma igång med personalisering i stor skala_](https://business.adobe.com/resources/reports/getting-started-with-personalization-at-scale.html) rapport.

Om du vill skapa en personaliserad shoppingupplevelse måste du lära dig mer om vilken typ av data som behövs för att förstå kundsammanhanget. Därifrån får ni lära er om Adobe Commerce-funktioner som använder dessa data för att få de kundinsikter ni behöver för att skapa en personaliserad shoppingupplevelse.

Bilden nedan visar de koncept som används för att personalisera shoppingupplevelsen:

![Bygga en personaliseringsprocess](assets/personalization-journey.png){width="700" zoomable="yes"}

I den här artikeln beskrivs de ovanstående begreppen mer ingående.

## Hur personaliserar ni shoppingupplevelsen?

Framgångsrik personalisering börjar med kundsammanhang. I det här avsnittet får du lära dig mer om de datatyper som är tillgängliga för att hjälpa dig att skapa kundsammanhang.

### Lagringsdata

Data från Storefront, som även kallas beteendedata eller webbläsardata, kan visa insikter i hur era kunder interagerar med er webbplats. Exempel:

- Vilka produkter och kategorier är mina kunder mest intresserade av?
- Vilken sorts sökfrågor är mina kunder mest engagerade i?
- Lägger mina kunder produkter i varukorgen och överger den sedan?
- Använder mina kunder en stationär eller mobil webbläsare?

Följande butikshändelser samlar in data som kan hjälpa dig att svara på dessa frågor:

- [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [signIn](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [signOut](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)

### Back office-data

Back office-data, som även kallas data på serversidan, kan avslöja insikter i orderns livscykel. Exempel:

- Finns det produkter som köps oftare beroende på årstid?
- Återvänder mina kunder produkter?
- Hur kan jag beräkna kundens livstidsvärde?

Följande back office-event samlar in data som kan hjälpa dig att besvara följande frågor:

- [orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderCanceled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

### Kundprofil och segmentdata

Kundprofildata kan visa insikter om vilka era kunder är och vilka segment de är kvalificerade för. Exempel:

- Namn
- Kön
- Adress
- Förmånsstatus
- Telefonnummer
- E-postadress
- Förmånsstatus
- Telefonnummer
- E-postadress
- Rätt till uppgraderingar
- Flerkanalskunder
- Nya produkter
- Guld-, silver- eller bronsmedlemmar

Följande profilhändelser samlar in data som kan hjälpa dig att svara på dessa frågor:

- [Profilpost](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord)
- [accountCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [accountUpdated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [accountDeleted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

Data från Storefront, back office och profile utgör grunden för Commerce-kunden och ordersammanhanget, som hjälper er att veta vilka produkter era kunder tittar på och slutligen köper. Sedan kan ni inrikta er på deras intressen och personalisera deras upplevelse. I nästa avsnitt får ni lära er vilka typer av personaliserade upplevelser ni kan interagera med era kunder.

## Typer av personaliserade upplevelser

Kund- och ordersammanhangsdata i Commerce understödjer följande typer av personaliserade upplevelser:

| Upplevelse | Beskrivning |
|---|---|
| **Produktupptäckt** | Innehåller marknadsföringstjänster som [distribueras som SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas). Det här är funktioner som gör att du kan använda beteendedata, produktattribut och lagernivåer för att automatiskt anpassa produktupptäckt för sökresultat, produktrekommendationer och webbsidor. De här funktionerna används [Adobe Sensei AI](https://business.adobe.com/products/sensei/adobe-sensei.html). |
| **Webbplatsinnehåll** | Avser möjligheten att distribuera personliga dynamiska innehållsblock baserat på den aktuella kundens surfning på er webbplats. |
| **Erbjudanden och kampanjer** | Gör att ni kan distribuera personaliserat kampanjinnehåll baserat på segmentdata. |
| **Mått** | Använd dataanalys för att bättre förstå er verksamhet, inklusive intäkter, kanal- och varuprestanda, kampanjer och så vidare. |

I de följande två avsnitten får du lära dig hur du kan använda dessa data för att skapa personaliserade upplevelser i [Adobe Experience Platform](#using-commerce-data-in-adobe-experience-platform) och in [funktioner för inbyggd handel](#using-commerce-data-in-native-commerce-features).

## Använda handelsdata i Adobe Experience Platform

Om du vill skapa en personaliserad upplevelse för era kunder i alla kanaler skickar du dina Commerce-data till Experience Platform Edge-nätverket med [[!DNL Data Connection]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview) tillägg.

![Hur data flödar till Experience Platform](assets/commerce-edge.png){width="700" zoomable="yes"}

I bilden ovan skickas data om din butiks-, back office- och kundprofil till Experience Platform med hjälp av en SDK, API och en källanslutning. Du behöver inte förstå hur dessa delar fungerar när tillägget hanterar komplexiteten i datadelningen för dig. När händelsedata finns i kanten kan du hämta dessa data till andra Experience Platform-program.

I följande tabell visas några av de tillgängliga Experience Platform-programmen och hur dessa program använder dina Commerce-data.

| Upplevelse | Program | Hur handelsdata används |
|---|---|---|
| **Webbplatsinnehåll** | [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview) | Adobe Commerce data underbygger enhetliga kundprofiler, där Real-Time CDP sammanfogar data från olika källor (ERP, CRM, CMS, POS) till unika profiler. Real-Time CDP kan också skapa både regelbaserade och AI-baserade segment som sedan kan användas i alla era marknadsföringslösningar. Ni kan också använda Real-Time CDP målgrupper för att personalisera innehållsblock, kampanjer och relaterade produktregler. Se [[!DNL Audience Activation]](../customers/audience-activation.md) om du vill veta mer. &#x200B; |
|  | [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro) | Adobe Commerce-data kan aktiveras i Adobe [!DNL Target] för att testa, optimera och skapa dynamiska landningssidor. Du kan anpassa den ordning i vilken innehållet visas på en sida, till exempel beskrivningar, specifikationer, recensioner och rekommenderade produkter baserat på skickade Commerce-data. |
| **Erbjudanden och kampanjer** | [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started) | Adobe Commerce beteendedata och backoffice-data kan fungera som en utlösare för personaliserade flerkanalsresor, inklusive e-postkampanjer, SMS, push-meddelanden med mera. &#x200B; |
| **Mått** | [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview) och [Kund [!DNL Journey Analytics]](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) | Commerce skickar både butiks- och back-office-data till kunden [!DNL Journey Analytics] (och endast butiksdata till Adobe) [!DNL Analytics]) för att möjliggöra mer omfattande analyser utöver grundläggande mätvärden i Adobe Commerce Intelligence, som intäkter, varor och kampanjer. &#x200B; |

Om du vill veta mer om hur du kan skicka dina Commerce-data till Experience Platform går du till [Dataanslutning](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview).

## Använda Commerce-data i native Commerce-funktioner

I följande avsnitt får du lära dig hur du kan använda inbyggda Commerce-funktioner, som Recommendations och Live Search för att skapa en personlig shoppingupplevelse. Du får också lära dig mer om en funktion som kallas [!DNL Audience Activation], som använder data från en produkt som finns i Experience Platform som kallas Real-Time CDP, vilket nämns [tidigare](#using-commerce-data-in-adobe-experience-platform). Även om Real-Time CDP inte är inbyggt i Commerce kan dess information hämtas till Commerce via [[!DNL Audience Activation]](../customers/audience-activation.md) tillägg.

Följande tabell visar vilka funktioner i Commerce som finns för att omvandla data för Commerce-kunder och orderkontext till användbara insikter.

| Upplevelse | Funktion | Beskrivning |
|---|---|---|
| **Produktupptäckt** | [Live Search](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview) | Använder AI-rankningsalgoritmer för att anpassa och optimera sökresultat baserat på en kunds beteendebeteende på webbplatsen, vilket ökar sökrelevansen och konverteringsgraden. |
|  | [Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) | Visar AI-baserade produktrekommendationer baserat på kundbeteende, trender, produktlikhet med mera. I kombination med din Adobe Commerce-katalog ger produktrekommendationer en engagerande, relevant och personaliserad upplevelse. |
|  | [Kategorimarknadsföring](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch) | Kategorimarknadsföring görs via Live Search Admin och med hjälp av AI rangordnas produktsekvenser automatiskt på varje kategorisida för att öka relevansen och konverteringsgraden för varje kund. Du kan skapa och hantera AI-baserade regler för att automatiskt rangordna produktsekvenser på kategorisidor utifrån kundernas aktiviteter och tillhörigheter. |
| **Webbplatsinnehåll** | [Dynamiska block som bygger på inbyggda handelsfunktioner](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | Gör att ni kan leverera personaliserat webbplatsinnehåll baserat på logik som konfigurerats i prisregler och kundsegment. |
|  | [Dynamiska block som informerats av Real-Time CDP målgrupper](../customers/audience-activation.md) | Gör att handlare kan leverera personaliserat webbplatsinnehåll baserat på målgrupper som konfigurerats i Real-Time CDP. |
| **Erbjudanden och kampanjer** | [Kundprisregler](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart) | Används för att tillämpa rabatter på artiklar i kundvagnen baserat på en uppsättning villkor. |
|  | [Dynamiska block som bygger på inbyggda handelsfunktioner](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | Gör att ni kan visa personaliserade bannerkampanjer baserat på kundsegment som konfigurerats internt i Commerce. |
|  | [Dynamiska block som informerats av Real-Time CDP målgrupper](../customers/audience-activation.md) | Gör att ni kan visa personaliserade kampanjer baserat på målgrupper som konfigurerats i Real-Time CDP. |
| **Mått** | [Adobe Commerce Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) | (tidigare kallat Magento Business Intelligence) är en molnplattform som ger bästa praxis för att hjälpa er att fatta datadrivna beslut och vidta tydliga och välgrundade åtgärder. Adobe Commerce Intelligence kan analysera era data för att hjälpa er att besvara frågor om ordertillväxt, kundbeteende och hur effektiva era marknadsföringsstrategier är. |
