---
title: Vad är butiken?
description: Lär dig mer om de sidor och funktionselement som din butik kan tillhandahålla som stöd för shoppingupplevelsen för dina kunder.
exl-id: 1c64888f-2bc0-4e2e-b7da-0e7182ea67e0
feature: Storefront
source-git-commit: 3b359ed43e81a2771a372c8e3c7557853b3eecad
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---

# Vad är butiken?

Inom implementeringen av Adobe Commerce eller Magento Open Source är butiken den externa, offentliga delen av din butik. Det innehåller innehåll och funktionskomponenter som kunderna använder för att handla och köpa.

Den väg kunderna går till en försäljning kallas ibland för _köpväg_, och din butik innehåller komponenter som kunderna kan använda för att slutföra den här vägen. I följande avsnitt finns en översikt över de grundläggande sidtyperna som ger ett strategiskt värde - de platser kunderna vanligtvis besöker när de handlar i din butik. När du tittar på dem bör du överväga olika butiksfunktioner som kan användas i varje skede av kundresan.

## Startsida

Visste du att de flesta bara tillbringar några sekunder på en sida innan de bestämmer sig för att stanna eller åka någon annanstans? Det är inte länge sedan att göra ett intryck. Studier visar att man också älskar fotografier, särskilt av andra. Vilken design du än väljer bör allt på din hemsida flytta besökarna mot nästa steg i försäljningsprocessen. Tanken är att leda deras uppmärksamhet i ett sammanhängande flöde från en punkt till nästa.

![Exempel på startsida för butiker](./assets/storefront-homepage-full.png){width="700"}

## Katalogsida

Katalogsidlistor har vanligtvis små produktbilder och korta beskrivningar och kan formateras som en lista eller ett rutnät. Du kan lägga till block, videoklipp och beskrivningar med nyckelord och även skapa specialdesigner för en kampanj eller säsong. Du kan skapa en särskild kategori för en livsstil eller ett varumärke som är en välstrukturerad samling produkter från olika kategorier.

Den första produktbeskrivningen ger oftast kunderna tillräckligt med information för att de ska kunna ta en närmare titt. Folk som vet vad de vill ha kan lägga produkten i sina varukorgar och gå. Kunder som är inloggade på sina konton får en personlig shoppingupplevelse.

![Samlingssida i butiken](./assets/storefront-collection-page.png){width="700"}

## Sökresultat

Visste du att det är nästan dubbelt så troligt att personer som använder sökningar köper något som de som bara använder navigering? Dessa kunder kan betraktas som _förkvalificerade_.

### [!DNL Live Search]

Med [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) för Adobe Commerce kan din butik erbjuda en snabb, superrelevant och intuitiv sökupplevelse och är tillgänglig för Adobe Commerce utan extra kostnad.

![Exempel på Live-sökning - sök medan du skriver](./assets/storefront-search-as-you-type.png){width="700"}

### Standardkatalogsökning

Med [standardkatalogsökning](../catalog/search.md) innehåller din butik en sökruta i det övre högra hörnet och en länk till avancerad sökning i sidfoten. Alla söktermer som kunderna skickar sparas så att du kan se exakt vad de letar efter. Du kan ge förslag och ange synonymer och vanliga felstavningar. Visa sedan en viss sida när en sökterm anges.

![Exempel på standardsökresultat för kataloger](./assets/storefront-search-results-page-full.png){width="700"}

## Produktsida

Det är mycket som pågår på produktsidan! Det första som fångar ögat på produktsidan är huvudbilden med ett högupplöst zoom- och miniatyrgalleri. Förutom pris och tillgänglighet finns det ett flikområde med mer information och en lista över relaterade produkter.

![Exempelproduktsida för butiker](./assets/storefront-product-page-full-m.png){width="700"}

## Kundvagn

Kundvagnen är den plats där ordersumman kan bestämmas, plus rabattkuponger och uppskattad frakt och moms, och en bra plats där du kan visa dina kreditmärken och sigill. Det är också en idealisk möjlighet att erbjuda en sista artikel. Som korsförsäljning kan du välja vilka artiklar som ska erbjudas som ett impulsköp när en viss artikel visas i kundvagnen.

![Exempel på kundvagnssida i butiken](./assets/storefront-cart-full.png){width="700"}

## Utcheckningssida

Utcheckningsprocessen består av två steg:

1. Leveransinformation

   Det första steget i utcheckningsprocessen är att kunden fyller i leveransadressuppgifterna och väljer leveranssätt. Om kunden har ett konto anges leveransadressen automatiskt, men kan ändras vid behov.
Om en gästkund anger en e-postadress som känns igen som registrerad tidigare visas inloggningsmeddelandet om fältet [!UICONTROL Enable Guest Checkout Login] i butikskonfigurationen är inställt på `Yes` (se [[!UICONTROL Checkout Options]](../configuration-reference/sales/checkout.md#checkout-options) i _Konfigurationsreferenshandboken_). Den här inställningen kan dock visa kundinformation för oautentiserade användare.

   ![Exempel på utcheckningssida för lagerframsida](./assets/storefront-checkout-shipping-full.png){width="700"}

1. Granska och betala

   Det andra steget i utcheckningsprocessen är att kunden väljer betalningsmetod och kan välja att använda en rabattkod.

   >[!NOTE]
   >
   >Även om [!DNL Commerce] tillåter konfigurering av flera kupongkoder, kan kunden bara använda en kupongkod i kundvagnen. (Mer information finns i [Kupongkoder](../merchandising-promotions/price-rules-cart-coupon.md#coupon-codes).)

   ![Exempel på utcheckningssida för lagerframsida](./assets/storefront-checkout-payment-full.png){width="700"}

Förloppsindikatorn överst på sidan följer varje steg i utcheckningsprocessen och i _ordersammanfattningen_ visas den information som har angetts fram till den här punkten.

>[!NOTE]
>
>Undantaget för en tvåstegs utcheckning gäller för virtuella och/eller hämtningsbara produkter. Om det bara finns sådana produkter i kundvagnen omvandlas utcheckningen automatiskt till en enstegsprocedur eftersom ingen leveransinformation behövs.
