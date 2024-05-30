---
title: Skapa övertygande, personaliserade upplevelser i stor skala
description: Lär dig vilka funktioner som finns i Adobe [!DNL Commerce] gör att ni kan skapa en personaliserad upplevelse för era kunder.
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 9884d0991cceda7c2917f723467230d3702b2d0f
workflow-type: tm+mt
source-wordcount: '1648'
ht-degree: 0%

---

# Skapa övertygande, personaliserade upplevelser i stor skala

Adobe [!DNL Commerce] ger er en kraftfull verktygslåda för att personalisera alla kundkontaktytor och öka kundernas engagemang, konverteringar och intäkter.

I den här artikeln får du lära dig:

- Vad är personalisering?
- Vilka data behöver jag för att uppnå personalisering?
- Hur gör Adobe? [!DNL Commerce] Lås upp personalisering?
- Tillgängliga användningsfall för personalisering

## Vad är personalisering?

Personalisering innebär att skräddarsy olika aspekter av varje kunds köpupplevelse för att uppfylla deras unika behov, sammanhang och önskemål. Personalisering begränsas inte till innehåll på webbplatsen, eller rekommendationer av bäst lämpade produkter, utan omfattar i stället alla kontaktytor under hela kundresan, inklusive:

- **Kampanjer och kommunikation** - Leverera relevanta och enhetliga meddelanden via kampanjer och kommunikation
- **Produktidentifiering** - Visa rätt produkter för rätt kunder i rätt ögonblick
- **Kampanjer och erbjudanden** - Målinriktade kampanjer och erbjudanden som får varje kund att konvertera
- **Innehållsupplevelser** - Skräddarsy webbplatsinnehåll så att det känns hyper relevant för varje kund och deras resa

![Typer av personalisering](assets/types-personalization.png){width="700" zoomable="yes"}

Även om den här typen av personaliserade upplevelser kan tyckas vara genomförbara för en liten del av kunderna, och personalisering i stor skala för tusentals eller miljontals kunder över alla kontaktytor och kanaler, kan allt i realtid kännas omöjligt. I följande avsnitt får du lära dig hur Adobe [!DNL Commerce] och Adobe Experience Cloud kan hjälpa till.

## Vilka data behöver jag för att uppnå personalisering?

Effektiv personalisering kräver sammanhang eller signaler som ger information om kunder som sedan kan användas för att ändra deras upplevelse. I följande tabell visas de olika datatyperna och rollen som Adobe [!DNL Commerce] spelar en roll när det gäller att stödja insamling och aktivering av dessa data.

| Datatyper | data från Storefront (beteendehändelser) | Back office-data (händelser på serversidan) | Kundprofil och segmentdata |
|---|---|---|---|
| **Definition** | Klicka på eller vidta de åtgärder som kunderna ska vidta på er webbplats. | Information om livscykeln och detaljer för varje order (tidigare och aktuell). | Vilka era kunder är och vilka segment är de kvalificerade för? |
| **Evenemang tagna med Adobe Commerce** | [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#pageview)<br>[productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)<br>[searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchrequestsent)<br>[searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchresponsereceived)<br>[addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtocart)<br>[openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#opencart)<br>[signIn](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signin)<br>[signOut](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signout)<br>[startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#startcheckout)<br>[completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#completecheckout)<br>[createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#createrequisitionlist)<br>[addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtorequisitionlist)<br>[removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#removefromrequisitionlist) | **Orderstatus**:<br>[orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderplaced)<br>[orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsreturnedinitiated)<br>[orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsshipped)<br>[orderCanceled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#ordercancelled)<br>[**Orderhistorik**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/fundamentals/connect-data#send-historical-order-data):<br>- SKU, namn, prisantal, rabatt<br>- produktkategori<br>- Betalningsbelopp, typ, valuta<br>- Leveranssätt och belopp<br>- Återbetalnings-ID, belopp, valuta<br>- Returorsak, villkor, upplösning<br>- Adress<br>- E-post | [**Profilpost**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord): (Namn, kön, adress, lojalitetsstatus, telefonnummer, e-postadress)<br>**Kontostatus**:<br>[accountCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountcreated)<br>[accountUpdated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountupdated)<br>[accountDeleted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountdeleted) |

Med allt detta rika förstapartsprogram [!DNL Commerce] är ni redo att målinrikta och personalisera varje kundupplevelse. I nästa avsnitt får du lära dig hur [!DNL Commerce] och Adobe Experience Cloud hjälper er att skapa personaliserade upplevelser och de användningsfall ni kan aktivera.

## Hur gör Adobe? [!DNL Commerce] möjliggör personalisering?

Adobe [!DNL Commerce] Med Data Sharing kan ni samla in och dela datatyperna i den föregående tabellen med andra Adobe Experience Cloud-produkter för att skapa enhetliga kundprofiler och målgrupper, personaliserade kampanjer samt omfattande analyser och insikter.

![Hur data flödar till Experience Platform](assets/commerce-edge.png){width="700" zoomable="yes"}

Adobe [!DNL Commerce] Datautbyte innehåller två huvudkomponenter:

1. [Dataanslutning](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview): Dela butiks-, back office- och kundprofildata från Adobe [!DNL Commerce] till Adobe Experience Platform gränsnätverk som kan användas i alla Adobe Experience Cloud-program, inklusive

   - [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview): Använd data från olika källor (ERP, CRM, POS) i enhetliga profiler och skapa regelbaserade eller AI-baserade segment.
   - [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started): Lansera personaliserade flerkanalsresor, inklusive e-postkampanjer, SMS, push-meddelanden med mera.
   - [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) och [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview): Få insikter om kunden och företaget.
   - [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro): Testa och optimera innehåll, rekommenderade produkter, erbjudanden, navigering med mera.

1. [[!DNL Audience Activation]](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation): Använd [!DNL Real-Time CDP] målgrupper för att personalisera dynamiska innehållsblock, kampanjer och relaterade produktregler på Adobe [!DNL Commerce] webbplats.

### Enkel personalisering: Kom igång med äkta Adobe [!DNL Commerce] funktioner

Adobe [!DNL Commerce] levererar kraftfull personalisering med sina inbyggda färdiga funktioner. I följande tabell beskrivs [!DNL Commerce] funktioner som ni kan aktivera direkt för att komma igång med personaliseringsresan.

| Kategori | Funktioner |
|---|---|
| Personaliserad produktupptäckt | [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview): Personalisera och optimera sökresultaten baserat på en kunds beteendebeteende och tillhörighet på plats med hjälp av AI-baserad sökning.<br>[Intelligent kategorimarknadsföring](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch): AI-driven produktrankning på kategorisidor baserad på en kunds beteendebeteende och tillhörighet på plats.<br>[Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview): AI-baserade produktrekommendationer baserade på kundernas beteende, trender och engagemang.<br>[Relaterade produktregler](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules): Definiera anpassade regler för att visa produkter från din katalog för att driva merförsäljning. |
| Personaliserat webbplatsinnehåll | [Dynamiska innehållsblock](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks): Visa personliga innehållsblock, till exempel banners, baserat på kundsegment i Adobe Commerce. |
| Personaliserade erbjudanden och kampanjer | [Kundprisregler](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart): Använd rabatter på artiklar i kundvagnen baserat på en uppsättning villkor, inklusive kundsegment i Adobe [!DNL Commerce]. |
| Insikter och mätning | [Adobe [!DNL Commerce] Intelligens](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started): Förstå hur era personaliseringsstrategier fungerar och förbättras över tid. |

## De vanligaste användningsområdena för personalisering

Adobe [!DNL Commerce] kunderna använder färdiga funktioner och delar data med Adobe Experience Cloud för en rad olika användningsområden. I följande avsnitt beskrivs de vanligaste användningsområdena och hur de implementeras med Adobe [!DNL Commerce] Endast eller [!DNL Commerce] plus Experience Cloud-appar.

### Personaliserade kampanjer och kommunikation

| Användningsfall | Lösning |
|---|---|
| **Övergiven kundvagn och bläddring** - Leverera ett personaliserat e-postmeddelande om återengagemang när en kund överger sin kundvagn eller surfsession efter att ha visat ett högt engagemang | **Adobe [!DNL Commerce] Endast**:<br>[E-postpåminnelser](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules)<br>**Adobe [!DNL Commerce] med Adobe Journey Optimizer**:<br>[!DNL Commerce] data fungerar som utlösare för en flerkanalig avhoppsresa. Anpassa den resan utifrån kundattribut, vad de överger, andra shoppingbeteenden och tidigare köp.<br>Commerce med Adobe Journey Optimizer och Real-Time CDP: Skräddarsy kampanjer för att överge kunderna baserat på enhetliga kundprofiler och centralt hanterade målgrupper, till exempel för att skapa en hög övergivningsfrekvens. |
| **Centraliserad målgruppsproduktion** - Skapa regelbaserade eller AI-baserade målgrupper baserat på webbplatsbeteende, tidigare köp, profilattribut, kategoritillhörighet, lojalitetsstatus, kundvärde med mera | **Adobe [!DNL Commerce] Endast**:<br>Samla in kundprofilinformation när [!DNL Commerce] kunder skapar konton. Skapa regelbaserade [kundsegment](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/segments/customer-segments) och kundgrupper för att personalisera innehåll och kampanjer.<br>**Adobe [!DNL Commerce] med Adobe Real-Time CDP**:<br> [Enhetliga profiler](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home) från olika datakällor och kanaler, regelbaserade eller AI-baserade målgrupper. |
| **Personaliserat e-post-/SMS-erbjudande baserat på köpbeteende** - Skicka skräddarsydda erbjudanden till kunder via riktad e-post baserat på tidigare köp och kundbeteende, till exempel skicka erbjudanden för produkter eller kategorier som kunderna har tittat på eller varit engagerade i. | **Adobe [!DNL Commerce] Endast**:<br>Exportera data för användning med automatiserade marknadsföringslösningar.<br>**Adobe [!DNL Commerce] med Adobe Journey Optimizer och Real-Time CDP**:<br>[!DNL Commerce] data fungerar som utlösare för e-post- eller SMS-erbjudanden och ger signaler (kundbeteenden) att personalisera utifrån. Real-Time CDP behövs inte, men i allmänhet skapas dessa erbjudanden och kampanjer runt målgrupper, som skapas och hanteras inom Real-Time CDP. |
| **Cross or Upsell Compatible Products/Brands** - Om en kund köper en produkt eller ett varumärke som är kompatibelt eller som visar på hög affinitet till en annan produkt eller ett annat varumärke, skickar du en kampanj (e-post/SMS) för att driva konverteringen av korsförsäljning. | **Adobe [!DNL Commerce] Endast**:<br>Använd Adobe [!DNL Commerce] [Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) för att rekommendera specifika produkter på webbplatsen. Du kan också använda [Relaterade produktregler](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) för att föreslå andra produkter.<br>**[!DNL Commerce] med [!DNL Target]**:<br>Adobe [!DNL Target] har också en inbyggd motor för produktrekommendationer med kraftfulla funktioner som kategoritillhörighet. Detta kan användas för korsning eller merförsäljning.<br>**[!DNL Commerce] med Adobe Journey Optimizer**:<br>Använd [!DNL Target] eller [!DNL Commerce] för att avgöra vilka produkter som ska rekommenderas och sedan leverera via Adobe Journey Optimizer. |

### Personaliserade webbplatsupplevelser

| Användningsfall | Lösning |
|---|---|
| **Personaliserat webbplatsinnehåll** - Anpassa banners för webbplatser och annat sidinnehåll baserat på kundernas agerande, som surfning och kategoritillhörighet. Distribuera innehåll som passar bäst baserat på resultaten från A/B-tester eller affärsmål. | **Adobe [!DNL Commerce] Endast**:<br>Distribuera segmentspecifika [dynamiska innehållsblock](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks).<br>**[!DNL Commerce] med Real-Time CDP **:<br>Använd [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) för att driftsätta målgruppsspecifika dynamiska innehållsblock som svarar på åtgärder i realtid och enhetliga kundprofildata, samtidigt som de centralt hanterar profiler och målgrupper i Real-Time CDP.<br>**[!DNL Commerce] med[!DNL Target]**:<br>Anpassa alla delar av sajten, inklusive innehåll, navigeringsobjekt, sidlayout med mera med Adobe [!DNL Commerce] data i Adobe [!DNL Target]. A/B-testinnehåll, välj och distribuera automatiskt vinnande innehåll för varje kund.<br>**[!DNL Commerce] med AEM Assets **:<br>Lagra allt innehåll i Adobe Experience Manager Assets. Få direkt tillgång till materialet inifrån Adobe Commerce. Använd GenAI för att skapa innehållsvariationer som kan anpassas för olika segment eller målgrupper. |
| **Personaliserat erbjudande på plats baserat på beteende** - Skräddarsy kampanjer baserat på kundernas agerande, som surfning och kategoritillhörighet. Distribuera nästa bästa erbjudande baserat på resultaten av A/B-tester eller affärsmål. | **Adobe [!DNL Commerce] Endast**:<br>Distribuera segmentspecifik katalog och [kundprisregler](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart).<br>**Adobe [!DNL Commerce] med Real-Time CDP**:<br>Använd [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) för att driftsätta målgruppsspecifika erbjudanden och centralt hantera profiler/målgrupper i Real-Time CDP.<br>**Commerce med[!DNL Target]**: Använd offer decisioning för att avgöra vilket erbjudande som ska distribueras, A/B-tester eller ange affärsmål för att vägleda erbjudanden som distribueras i Adobe Commerce. |

### Analyser och insikter

| Användningsfall | Lösning |
|---|---|
| **Kundbeteende efter kanal** - Förstå nyanserna om hur kunderna engagerar sig i varje kanal (webb, personlig, app, övrigt) för att påverka marknadsföringsstrategier för varje kanal, förstå kundtratten och svagheterna i kundupplevelsen. | **Adobe [!DNL Commerce] Endast**:<br>[Adobe [!DNL Commerce] Intelligens](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) ger innehållsrik analys om [!DNL Commerce] kanal, men inte över flera kanaler eller större delar av kundresan.<br>**Adobe [!DNL Commerce] med Customer Journey Analytics**:<br>[!DNL Commerce] data matar in datapaneler för fullständig detaljrikedom i alla faser av kundupplevelsen (i alla kanaler). Förstå alla kontaktytor och den bredare tratten för att identifiera svaga punkter i kundresan där kunderna kan falla bort. |
| **Inköpstrender** - Förstå köpbeteenden under en viss tidsperiod (t.ex. kundkorgsanalys, produktanalys) för att identifiera trender, säsongsvariation och optimera marknadsföring baserat på historiska köpmönster. | **Adobe [!DNL Commerce] Endast**:<br>[Adobe [!DNL Commerce] Intelligens](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) ger innehållsrik analys om [!DNL Commerce] kanal, men inte över flera kanaler eller större delar av kundresan.<br>**Adobe [!DNL Commerce] med Customer Journey Analytics**:<br>[!DNL Commerce] data matar in datapaneler för fullständig detaljrikedom i alla faser av kundupplevelsen (i alla kanaler). Förstå alla kontaktytor och den bredare tratten för att identifiera svaga punkter i kundresan där kunderna kan falla bort. |

## Exempel på användningsfall

- Läs om hur du kan använda Adobe Journey Optimizer för att [skicka ett övergivet kundvagnsmeddelande](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/using-ajo).
- Lär dig hur [skapa en publik i Real-Time CDP](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/create-audience) för att informera om en kundvagnsprisregel i Adobe [!DNL Commerce].
