---
title: Köp och inlösen av presentkort
description: Lär dig mer om presentkortets livscykel för köp till inlösen när du inkluderar presentkort i din butikskatalog.
exl-id: ecaa39aa-f504-4bfd-874b-12b44093c2a9
feature: Products, Gift
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 0%

---

# Köp och inlösen av presentkort

{{ee-feature}}

Presentkort löses in i kundvagnen på ungefär samma sätt som en kupong tillämpas på en order. Under utcheckningen anger kunden presentkortskoden för att använda ett belopp från presentkortet till köpet. Presentkortsinnehavare som har kundkonton kan kontrollera status och återstående saldo från sin kontokontrollpanel. Ett och flera presentkort kan användas för att betala för hela eller delar av en order.

Den tillämpade presentkortskoden kan visas genom att du öppnar ordern i _Admin_, vilket gör det möjligt för dig att hämta koden och placera den på ett fysiskt presentkort, om det behövs. Om en presentkortsorder annulleras eller återbetalas måste du manuellt annullera det associerade presentkortskontot. Du kan antingen ta bort kontot helt eller inaktivera det.

![Presentkortsinformation i kundvagnen](./assets/storefront-gift-card-order-customer-account.png){width="700" zoomable="yes"}

En kund som handlar i en demo-Luma-butik kan till exempel köpa ett virtuellt eller fysiskt presentkort.

**Virtuellt presentkort** - Ett virtuellt Luma-presentkort skickas med e-post med ett valfritt meddelande till mottagaren. Den kan lösas in på alla Luma-webbplatser och kan aldrig upphöra att gälla.

**Fysiskt presentkort** - Ett Luma-presentkort paketeras i en anpassad utgivare och skickas utan kostnad till mottagaren. Den kan produceras i förväg, märkas med unika koder och lösas in i butik, via telefon eller på någon av Lumas webbplatser. Den upphör aldrig att gälla.

**Kombinerat presentkort** - Ett kombinerat presentkort har samma egenskaper som både ett virtuellt och ett fysiskt presentkort. Ett kombinerat presentkort från Luma skickas och skickas med e-post till mottagaren. E-postadress och leveransadress krävs när du köper presentkortet. Den upphör aldrig att gälla.

## Presentkortets livscykel

1. **Kunden bestämmer presentkortsvärdet**.

   Kunden bestämmer värdet på presentkortet från produktsidan. Beroende på konfigurationen finns det antingen ett fast prisfält, en lista med prisalternativ eller båda. Alla belopp visas i den valuta som används i butiken.

1. **Kunden fyller i presentkortsinformationen**.

   För ett fysiskt presentkort anger kunden **Avsändarnamn** och **Mottagarnamn**. För virtuella eller kombinerade presentkort anger kunden även **avsändarens e-postadress** och **mottagarens e-postadress**. Om kunden är inloggad anges avsändarens namn (och avsändarens e-postadress, om tillämpligt) automatiskt från deras konto. Beroende på konfigurationen kan kunden även skriva ett meddelande till mottagaren.

1. **Kunden slutför utcheckningen**.

   Presentkortet visas som en radartikel i kundvagnen med detaljerad information om avsändarens, mottagarens och meddelandets namn, om tillämpligt. Det belopp som är associerat med presentkortet konverteras till butikens basvaluta när det läggs till i kundvagnen.

1. **Kunden får en bekräftelse på ordern**.

   Presentkortsköparen kan klicka på länken i bekräftelsen för att spåra beställningen från sin kontouppsättning.

1. **Mottagaren får presentkortet**.

   För virtuella eller kombinerade presentkort får mottagaren ett e-postmeddelande med presentkortskoden, avsändarens namn och, om tillämpligt, ett meddelande. Om flera presentkort köps i en och samma beställning och typen är antingen virtuell eller kombinerad, skickas alla motsvarande presentkortskoder till mottagaren i ett enda e-postmeddelande. Fysiska presentkort kan skickas direkt till mottagaren eller till kunden, som sedan kan skicka presentkortet till mottagaren.

1. **Mottagaren använder presentkort för inköp**.

   Mottagaren köper en artikel i din butik och använder presentkortskoden vid utcheckningen. Varje gång ett presentkort används under utcheckningen visas beloppet i ordersummeringsblocket och dras ifrån totalsumman. Hela saldot för varje presentkort dras av från kundvagnssumman. Om flera presentkort används för ett inköp används de i stigande ordning, med början med kortet med det minsta återstående saldot, tills alla används eller totalsumman är noll. När totalsumman är noll får det sista presentkortskontot som används i vagnen ett partiellt avdrag. Kort som inte har tillämpats på vagnen får inget saldoavdrag. Beloppen dras av från presentkortskontona först efter att ordern har lagts.

## StoreFront

Hur presentkort fungerar i butiken:

- Presentkortskoden kan användas i kundvagnen eller i kassan för att täcka orderns totala belopp.

- I katalogen visas ett presentkort som en separat typ av produkt.

- Presentkortskoden aktiveras när ordern har fakturerats. Om ordern inte betalas kan den mottagande kunden inte använda presentkortet.

- Konton för presentkoder skapas för att spåra saldot för en viss verifikation. En butiksadministratör kan justera saldot manuellt.

Den mottagande kunden kan använda avsnittet _[!UICONTROL Gift Card]_på kontouppsättningen för att kontrollera saldot på sitt [presentkortskonto](product-gift-card-accounts.md) och inlösa presentkort för [butikskrediter](../customers/store-credit-using.md).

![Presentkort](./assets/account-dashboard-gift-card.png){width="700" zoomable="yes"}

### Kontrollera status och saldo för presentkortet

1. Från butiken loggar kunden in och öppnar sin kundkontosida.

1. Kunden öppnar sidan **[!UICONTROL Gift Card]** och anger presentkortskoden.

1. Kunden klickar på **[!UICONTROL Check status and balance]**.

![Presentkortssaldo](./assets/gift-balance.png){width="700" zoomable="yes"}

Återstoden av presentkortet visas.

### Aktivering av presentkort

1. På sidan _[!UICONTROL Gift Card]_anger kunden presentkortskoden.

1. Kunden klickar på **[!UICONTROL Redeem Gift Card]**.

![Meddelande om att presentkortet har aktiverats](./assets/gift-redeemed-balance.png){width="700" zoomable="yes"}

Presentkortsbeloppet aktiveras och läggs till i det totala butikskreditsaldot.

![Butikskreditsaldo](./assets/store-credit.png){width="700" zoomable="yes"}

Alla åtgärder för presentkortssaldot är tillgängliga på sidan _[!UICONTROL Store Credit]_.

### Använd ett presentkort vid utcheckning

Om presentkortet inte går att lösa in kan kunden använda presentkortskoden under utcheckningen.

1. Under steget _Granska och betala_ klickar kunden på **[!UICONTROL Apply Gift Card]**.

1. Ange presentkortskoden och klicka sedan på **[!UICONTROL Apply]**.

   Rabatten bör återspeglas i _[!UICONTROL Order Summary]_.

1. Klicka på **[!UICONTROL Place Order]** för att slutföra ordningen.
