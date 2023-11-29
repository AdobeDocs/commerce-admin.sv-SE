---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Delivery Methods]'
description: Granska konfigurationsinställningarna på [!UICONTROL Sales] &gt; [!UICONTROL Delivery Methods] sidan för Commerce Admin.
exl-id: 159b76a8-3676-4692-9cd6-18947bda4666
feature: Configuration, Shipping/Delivery
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '3812'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Delivery Methods]

{{config}}

## [!UICONTROL Basic Delivery Methods]

### [!UICONTROL Flat Rate]

![Schablonbelopp](./assets/delivery-methods-flat-rate.png)<!-- zoom -->

<!-- [Flat Rate](https://docs.magento.com/user-guide/shipping/shipping-flat-rate.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webbplats | När den är aktiverad visas Platt hastighet som ett alternativ i dialogrutan _Beräkna frakt och skatt_ i kundvagnen och på _Leverans_ under utcheckning. Alternativ: `Yes` / `No` |
| [!UICONTROL Title] | Butiksvy | Namnet som används för den här leveransmetoden vid utcheckning. |
| [!UICONTROL Method Name] | Butiksvy | Ett namn som beskriver den beräkningsmetod som används för att generera en leveransuppskattning. Metodnamnet visas bredvid den beräknade tariffen i kundvagnen. Standardvärdet är `Fixed`. |
| [!UICONTROL Type] | Webbplats | Beskriver vilken typ av beräkning som används för att fastställa schablonbeloppet. Alternativ: <br/>**`None`**- Ingen beräkning används. Ställer in schablonbelopp till noll, vilket motsvarar fri frakt.<br/>**`Per Order`** - Debiterar ett schablonbelopp för hela ordern. <br/>**`Per Item`**- Debiterar ett separat schablonbelopp för varje artikel i vagnen. Kursen multipliceras med antalet artiklar i vagnen, även om den totala kvantiteten innehåller en kombination av olika artiklar. |
| [!UICONTROL Price] | Webbplats | Det pris du debiterar kunden för frakt till fast pris. |
| [!UICONTROL Calculate Handling Fee] | Webbplats | Avgör hur hanteringskostnaden beräknas, om en sådan inkluderas. Alternativ: `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | Webbplats | Ange det belopp som ska debiteras för en hanteringsavgift, baserat på den metod du har valt för att beräkna beloppet. Om avgiften t.ex. är baserad på en fast avgift anger du beloppet i decimalform, t.ex. 4,90. Om hanteringsavgiften baseras på en procentandel av ordern anger du beloppet i procent. Om du till exempel debiterar sex procent av ordern anger du värdet som `.06`. |
| [!UICONTROL Displayed Error Message] | Butiksvy | Ett meddelande som visas om en kund väljer ett schablonbelopp, men av någon anledning är metoden inte tillgänglig. |
| [!UICONTROL Ship to Applicable Countries] | Webbplats | Identifierar de länder där ni erbjuder frakt till schablonbelopp. Alternativ: <br/>**`All Allowed Countries`**- Kunder från vilket land som helst som anges i butikskonfigurationen kan använda frakten till ett fast pris.<br/>**`Specific Countries`** - Kunder från endast vissa länder kan använda frakt till fast pris. |
| [!UICONTROL Ship to Specific Countries] | Webbplats | Identifierar varje land där kunderna kan använda prissatt frakt. |
| [!UICONTROL Show Method if Not Applicable] | Webbplats | Avgör om ett schablonbelopp visas som ett alternativ vid utcheckning om metoden inte gäller för köpet. Alternativ: `Yes` / `No` |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som bestämmer i vilken ordning som ett schablonbelopp visas när det visas med andra leveransmetoder vid utcheckning. |

{style="table-layout:auto"}

### [!UICONTROL Free Shipping]

![Fri frakt](./assets/delivery-methods-free-shipping.png)<!-- zoom -->

<!-- [Free Shipping](https://docs.magento.com/user-guide/shipping/shipping-free.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webbplats | När alternativet är aktiverat visas Fri frakt som ett alternativ i avsnittet Leverans under utcheckning. Alternativ: `Yes` / `No` |
| [!UICONTROL Title] | Butiksvy | Namnet som används för den här leveransmetoden vid utcheckning. |
| Metodnamn | Butiksvy | Ett namn som beskriver den beräkningsmetod som används för att generera en leveransuppskattning. Metodnamnet visas bredvid den beräknade tariffen i kundvagnen. Standardvärdet är `Free`. |
| Minsta orderbelopp | Webbplats | Det minimiinköp som krävs för att tillämpa Fri frakt på en order. |
| Inkludera moms i belopp | Webbplats | Avgör om moms ingår i beräkningen av minimiorderbelopp. Alternativ: <br/>**Ja** - Moms inkluderas vid beräkning av minimiorderbelopp (Delsumma + Moms - Rabatt).<br/>**Nej** - Moms inkluderas inte när minimiorderbeloppet (Delsumma - Rabatt) beräknas. |
| Felmeddelande som visas | Butiksvy | Ett meddelande som visas om en kund väljer Fri frakt, men metoden är inte tillgänglig av någon anledning. |
| Leverera till tillämpliga länder | Webbplats | Identifierar de länder där du erbjuder kostnadsfri frakt. Alternativ: <br/>**Alla tillåtna länder** - Kunder från vilket land som helst som anges i butikskonfigurationen kan använda kostnadsfri frakt. <br/>**Särskilda länder** - Kunder från endast vissa länder kan använda kostnadsfri frakt. |
| Leverera till specifika länder | Webbplats | Identifierar varje land där kunderna kan använda kostnadsfri frakt. |
| Visa metod om den inte är tillämplig | Webbplats | Avgör om Fri frakt visas som ett alternativ vid utcheckning om metoden inte gäller för köpet. Alternativ: `Yes` / `No` |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som bestämmer i vilken ordning som Fri frakt ska visas när det visas med andra leveransmetoder vid utcheckning. |

{style="table-layout:auto"}

### [!UICONTROL Table Rates]

![Tabellavgifter](./assets/delivery-methods-table-rates.png)<!-- zoom -->

<!-- [Table Rates](https://docs.magento.com/user-guide/shipping/shipping-table-rate.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webbplats | När det här alternativet är aktiverat visas Registerpriser som ett alternativ i avsnittet Beräkna frakt och moms i kundvagnen och i avsnittet Leverans under utcheckningen. Alternativ: `Yes` / `No` |
| [!UICONTROL Title] | Butiksvy | Namnet som används för den här leveransmetoden vid utcheckning. |
| Metodnamn | Butiksvy | Ett namn som beskriver den beräkningsmetod som används för att generera en leveransuppskattning. Metodnamnet visas bredvid den beräknade tariffen i kundvagnen. Standardvärdet är `Table Rate`. |
| [!UICONTROL Condition] | Webbplats | Anger det villkor som beräkningen baseras på. Formatet på den överförda CSV-filen är specifikt för varje villkor. Alternativ: `Weight vs. Destination` / `Price vs. Destination` / `# of Items vs. Destination` |
| [!UICONTROL Include Virtual Products in Price Calculation] | Webbplats | Avgör om virtuella produkter, som inte kräver frakt, inkluderas i prisberäkningarna för registersatser. |
| [!UICONTROL Calculate Handling Fee] | Webbplats | Avgör hur hanteringskostnaden beräknas, om en sådan inkluderas. Alternativ: `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | Webbplats | Beloppet för eventuella avgifter som läggs till i leveransavgiften för att täcka kostnaden för att hantera leveransen. Ange värdet i decimalform. Om avgiften t.ex. baseras på en procentandel anger du 0,06 i stället för 6 %. Ange ett fast belopp `6.00`. |
| [!UICONTROL Displayed Error Message] | Butiksvy | Ett meddelande som visas om en kund väljer Tabellavgifter, men av någon anledning är metoden inte tillgänglig. |
| [!UICONTROL Ship to Applicable Countries] | Webbplats | Identifierar de länder där du erbjuder priser för frakt. Alternativ: <br/>**`All Allowed Countries`**- Kunder från vilket land som helst som anges i butikskonfigurationen kan använda tabellradsleverans.<br/>**`Specific Countries`** - Kunder från endast vissa länder kan använda sig av priser för frakt. |
| [!UICONTROL Ship to Specific Countries] | Webbplats | Identifierar varje land där kunderna kan använda priser för frakt. |
| [!UICONTROL Show Method if Not Applicable] | Webbplats | Avgör om tabellavgifter visas som ett alternativ vid utcheckning om metoden inte gäller för köpet. Alternativ: `Yes` / `No` |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som bestämmer i vilken ordning som tabellavgifter visas när de visas tillsammans med andra leveransmetoder vid utcheckning. |

{style="table-layout:auto"}

### [!UICONTROL In-Store Delivery]

![Butiksleverans](./assets/delivery-methods-in-store-delivery.png)<!-- zoom -->

<!-- [In-Store Delivery](https://docs.magento.com/user-guide/shipping/shipping-in-store-delivery.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webbplats | När det här alternativet är aktiverat kan leverans i butik visas som ett alternativ i _Beräkna frakt och skatt_ i kundvagnen och på _Leverans_ under utcheckning. Alternativ: `Yes` / `No` |
| [!UICONTROL Method Name] | Butiksvy | Ett namn som identifierar butiksupptagningsfunktionen som en leveransmetod. Värdet visas som etikett på en flik högst upp på utcheckningssidan för leverans och i tabellen över tillgängliga leveransmetoder längst ned på samma sida. Standardvärdet är `In-store Delivery`. |
| [!UICONTROL Title] | Butiksvy | Namnet som används för den här leveransmetoden vid utcheckning. |
| [!UICONTROL Price] | Webbplats | Det pris ni debiterar kunden för en upphämtning i butik. |
| [!UICONTROL Search Radius] | Webbplats | Den radie i km som ska användas vid sökning efter upphämtningsplatser. |
| [!UICONTROL Displayed Error Message] | Butiksvy | Ett meddelande som visas när en kund väljer att hämta i butik, men leveransmetoden är inte tillgänglig. |

{style="table-layout:auto"}

## [!UICONTROL Carriers]

### [!UICONTROL UPS]

{{ups-api}}

{{beta2-updates}}

![Inställningar för UPS XML-konto](./assets/delivery-methods-ups1.png)<!-- zoom -->

<!-- [UPS XML Account Settings](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled for Checkout] | Webbplats | Avgör om UPS är tillgängligt för kunder som leveransmetod vid utcheckning. Alternativ: `Yes` / `No` |
| [!UICONTROL Enabled for RMA] | Webbplats | Avgör om UPS är tillgängligt för kunder som leveransmetod för en RMA. Alternativ: `Yes` / `No` |
| [!UICONTROL UPS Type] | Butiksvy | Anger den metod som används för att ansluta till UPS-leveranssystemet. Alternativ: <br/>**`United Parcel Service XML`**- (Standard) Butiken skickar en XML-fil med data till UPS som en begäran.<br/>**`United Parcel Service`** - Butiken skickar nyckelvärdepar till UPS som en begäran. <br/><br/>**_Obs!_**Standardtypen för United Parcel Service är schemalagd för borttagning i Commerce. För nya konfigurationer bör du använda [!UICONTROL United Parcel Service XML] typ. |
| _[!UICONTROL UPS Account Settings]_ |  |  |
| [!UICONTROL Live Account] | Butiksvy | Anger att United Parcel Service-kontot är direktsänt. Alternativ: `Yes` / `No` |
| [!UICONTROL Gateway URL] | Webbplats | Den URL som ansluter till UPS-systemet för att hämta dynamiska leveransfrekvenser. UPS-stödet för HTTP upphör. Standardvärde: `https://www.ups.com/using/services/rave/qcostcgi.cgi` |
| [!UICONTROL Title] | Butiksvy | Namnet som används för den här leveransmetoden vid utcheckning. |
| _[!UICONTROL UPS XML Account Settings]_ |  |  |
| [!UICONTROL Access License Number] | Webbplats | Ditt licensnummer för åtkomst till ditt UPS-fraktkonto. |
| [!UICONTROL Gateway XML URL] | Webbplats | För UPS XML-tjänsten visar följande URL:er som krävs för att överföra XML-data: Gateway XML-URL, Spårnings-XML-URL, Leveransbekräftets XML-URL, Leveransmottagarens XML-URL |
| [!UICONTROL Mode] | Webbplats | Anger vilket överföringssätt som används för data som skickas till UPS-systemet. Alternativ: <br/>**`Development`**- UPS:en verifierar inte att data som tas emot från Commerce Server skickas via SSL.<br/>**`Live`** - UPS verifierar att data som tas emot från Commerce-servern skickas via ett säkert socketlager (SSL). |
| Användar-ID | Webbplats | Användar-ID för ditt UPS-avsändarkonto. |
| [!UICONTROL Origin of the Shipment] | Webbplats | (Endast UPS XML) Det land eller den region där produktleveransen kommer. |
| [!UICONTROL Password] | Butiksvy | Lösenordet för ditt UPS-fraktkonto. |

{style="table-layout:auto"}

![UPS-paketinformation](./assets/delivery-methods-ups-packaging-settings.png)<!-- zoom -->

<!-- [UPS Package Information](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| _[!UICONTROL UPS Negotiated Rate Settings]_ |  |  |
| [!UICONTROL Enable Negotiated Rates] | Webbplats | (Endast UPS XML) Aktiverar/inaktiverar specialfrekvenser enligt ditt avtal med UPS. Alternativ: `Yes` / `No` |
| [!UICONTROL Packages Request Type] | Webbplats | Bestämmer hur vikt beräknas för försändelser med flera paket. Alternativ: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Shipper Number] | Webbplats | (Endast UPS XML) Det sexsiffriga UPS-leveransnumret krävs för referens till användning av förhandlade hastigheter. |
| [!UICONTROL Container] | Webbplats | Anger behållartypen som används för att paketera orderleveranser. Alternativ: `Customer Packaging` / `UPS Letter Envelope` / `Customer Packaging` / `UPS Letter Envelope` / `UPS Tube` / `UPS Express Box` / `UPS Worldwide 25 kilo` / `UPS Worldwide 10 kilo` |
| [!UICONTROL Weight Unit] | Webbplats | Anger standardmåttenheten för produktvikt i butiken. Se [Dimensionell vikt](../../stores-purchase/carriers.md#dimensional-weight) om du vill ha mer information. |
| [!UICONTROL Tracking XML URL] | Webbplats | (Endast UPS XML) Den UPS-URL som används för att spåra paket. |
| [!UICONTROL Destination Type] | Webbplats | Anger standarddestinationstypen för leverans. Alternativ: `Business` / `Residential` |
| [!UICONTROL Maximum Package Weight] | Webbplats | Anger den maximala vikt ett paket kan ha enligt UPS-inställningarna. Om de beställda produkterna överstiger den högsta paketvikten är detta fraktalternativ inte tillgängligt. Enligt [UPS.com](https://www.ups.com/us/en/global.page), får paketen inte överskrida 70 kg. Kontakta din fraktfirma för att kontrollera den högsta vikten. |
| [!UICONTROL Pickup Method] | Webbplats | Anger UPS-hämtningsmetoden. Alternativ: `Regular Daily Pickup` / `On Call Air` / `One Time Pickup` / `Letter Center` / `Customer Counter` |
| [!UICONTROL Minimum Package Weight] | Webbplats | Anger den minsta vikt som ett paket kan ha enligt UPS-inställningarna. Om de beställda produkterna väger mindre än den minsta paketvikten är detta fraktalternativ inte tillgängligt. Kontrollera med din fraktfirma om du vill kontrollera minimivikten. |
| [!UICONTROL Calculate Handling Fee] | Webbplats | Anger beräkningsmetoden för hanteringsavgift för tabellradsleverans. Alternativ: <br>**`Fixed`**- Hanteringsavgiften är en fast avgift.<br>**`Percent`** - Hanteringsavgift tillämpas som en procentandel av orderbeloppet. |
| [!UICONTROL Handling Applied] | Webbplats | Anger om hanteringsavgift tillämpas på varje order eller på varje paket i en order. |
| [!UICONTROL Handling Fee] | Webbplats | Anger den hantering som ingår i fraktpriset. Hanteringsavgift kan anges som ett fast belopp eller som en procentandel. <br/><br/>**_Obs!_**Om du anger ett procentvärde använder du decimalformatet `0.25` för 25 %. |

{style="table-layout:auto"}

![Tillåtna UPS-metoder](./assets/delivery-methods-ups-allowed-methods.png)<!-- zoom -->

<!-- [UPS Allowed Methods](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| _[!UICONTROL UPS allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Webbplats | Anger vilka UPS-leveransmetoder som erbjuds kunderna. Fraktsatser beräknas på den valda leveransmetoden. |
| [!UICONTROL Free Method] | Webbplats | Identifierar den metod som används för kostnadsfri frakt via UPS. Om du vill inaktivera fri frakt väljer du Ingen. <br/><br/>**_Obs!_**Den här metoden liknar grundläggande [Fri frakt](../../stores-purchase/shipping-free.md)men visas som ett UPS-leveransalternativ vid utcheckningen. |
| [!UICONTROL Free Shipping Amount Threshold] | Webbplats | Anger om fri frakt ska användas när orderbeloppet når tröskelvärdet för fri frakt. Alternativ: `Enable` / `Disable` |
| [!UICONTROL Free Shipping Amount Threshold] | Webbplats | Anger det minsta totala beloppet som en order måste uppnå för att få fri frakt. |
| [!UICONTROL Displayed Error Message] | Butiksvy | Felmeddelandet som visas när den här leveransmetoden inte är tillgänglig av någon anledning. |

{style="table-layout:auto"}

![UPS-länder och andra inställningar](./assets/delivery-methods-ups-ship-to.png)<!-- zoom -->

<!-- [UPS Applicable Countries and Other Settings](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| _[!UICONTROL UPS Applicable countries and other Settings]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Webbplats | Anger vilket land kunderna får använda den här leveransmetoden. Alternativ: <br/>**`All Allowed Countries`**- Kunder från alla [länder](../../getting-started/store-details.md#country-options) som anges i butikskonfigurationen kan använda den här leveransmetoden.<br/>**`Specific Countries`** - När du har valt det här alternativet visas [!UICONTROL Ship to Specific Countries] visas. Välj varje land i listan där leveransmetoden kan användas. |
| [!UICONTROL Show Method if Not Applicable] | Webbplats | Avgör om UPS alltid visas som ett leveransalternativ vid utcheckning. Alternativ: <br/>**`Yes`**- UPS visas alltid som ett leveransalternativ vid utcheckning, även om det inte gäller för ordern.<br/>**`No`** - UPS visas endast som leveransalternativ vid utcheckning om det är tillämpligt på ordern. (Om orderns vikt till exempel överstiger den maximala viktmängden.) |
| [!UICONTROL Debug] | Webbplats | Anger om dataöverföringar mellan din butik och UPS är loggade i systemet för felsökning. Om det inte finns något problem som måste spåras och loggas bör det här alternativet anges till `No`. |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som bestämmer den ordning som UPS visas i när det visas med andra leveransmetoder vid utcheckning. Retur `0` överst i listan. |

{style="table-layout:auto"}

### [!UICONTROL USPS]

{{beta2-updates}}

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| Aktiverad för utcheckning | Webbplats | Avgör om USPS är tillgängligt för kunder som leveransmetod vid utcheckning. Alternativ: `Yes` / `No` |
| _[!UICONTROL USPS Account Settings]_ |  |  |
| [!UICONTROL Gateway URL] | Webbplats | Den URL som används för att ansluta till USPS-systemet för att dynamiskt hämta fraktkostnader. |
| [!UICONTROL Secure Gateway URL] | Webbplats | Den säkra URL som används för att ansluta till USPS-systemet via ett säkert socketlager (SSL) för att dynamiskt hämta fraktkostnader. |
| [!UICONTROL Title] | Butiksvy | Titeln på det här leveransalternativet så som det visas i kundvagnskassan. |
| [!UICONTROL User ID] | Webbplats | Ditt användar-ID för USPS-avsändarens konto. |
| [!UICONTROL Password] | Webbplats | Lösenordet för ditt USPS-avsändarkonto. |
| [!UICONTROL Mode] | Webbplats | Anger vilket överföringssätt som används för data som skickas till USPS-systemet. Alternativen är: <br/>**`Development`**- USPS verifierar inte att data som tas emot från Commerce Server skickas via SSL.<br/>**`Live`** - USPS verifierar att data som tas emot från Commerce-servern skickas via ett säkert socketlager (SSL). |

{style="table-layout:auto"}

![Inställningar för USPS-paketering](./assets/delivery-methods-usps-packaging.png)<!-- zoom -->

<!-- [USPS Packaging Settings](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| _[!UICONTROL USPS packaging Settings]_ |  |  |
| [!UICONTROL Packages Request Type] | Webbplats | Bestämmer hur vikt beräknas för försändelser med flera paket. Alternativ: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Container] | Webbplats | Anger behållartypen som används för att paketera orderleveranser. Alternativ: `Variable` / `Flat Rate Box` / `Flat Rate Envelope` / `Rectangular` / Icke-rektangulär |
| [!UICONTROL Size] | Webbplats | Anger storleksalternativet till den typiska paketstorleken för leverans. Det här alternativet påverkar beräkningen av fraktkostnaden. Alternativ: `Regular` / `Large` / `Oversize` |
| [!UICONTROL Machinable] | Webbplats | Anger om paketet kan bearbetas av datorn. Det här alternativet påverkar beräkningen av fraktkostnaden. |
| [!UICONTROL Maximum Package Weight] | Webbplats | Anger den maximala vikt ett paket kan ha enligt vad som anges av USPS. Om de beställda produkterna överstiger den högsta paketvikten är detta fraktalternativ inte tillgängligt. |

{style="table-layout:auto"}

![Avgiftsinställningar för USPS-hantering](./assets/delivery-methods-usps-handling-fee.png)<!-- zoom -->

<!-- [USPS Handling Fee Settings](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| _[!UICONTROL USPS Handling Fee settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | Webbplats | Anger beräkningsmetoden för hanteringsavgift för tabellradsleverans. Alternativ: <br/>**`Fixed`**- Hanteringsavgiften är en fast avgift.<br/>**`Percent`** - Hanteringsavgift tillämpas som en procentandel av orderbeloppet. |
| [!UICONTROL Handling Applied] | Webbplats | Anger om hanteringsavgift tillämpas på varje order eller på varje paket i en order. |
| [!UICONTROL Handling Fee] | Webbplats | Anger den hantering som ingår i fraktpriset. Hanteringsavgift kan anges som ett fast belopp eller som en procentandel. <br/><br/>**_Obs!_**Använd decimalformatet när du anger ett procentvärde `0.25` för 25 %. |

{style="table-layout:auto"}

![Tillåtna USPS-metoder](./assets/delivery-methods-usps-allowed-methods.png)<!-- zoom -->

<!-- [USPS Allowed Methods](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| _[!UICONTROL USPS Allowed Methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Webbplats | Anger vilka metoder för USPS-leverans som erbjuds kunderna. Fraktsatser beräknas på den valda leveransmetoden. |
| [!UICONTROL Free Method] | Webbplats | Anger kostnadsfri leveransmetod via USPS, eller kan inaktiveras genom att välja `None`. <br/><br/>**_Obs!_**Den här leveransmetoden liknar den som används i butiken för kostnadsfri frakt, men den anges som ett alternativ för USPS-leverans och identifieras som USPS-frakt. |
| [!UICONTROL Minimum Order Amount for Free Shipping] | Webbplats | Anger det minimiorderbelopp som måste uppfyllas för att få fri frakt. |
| [!UICONTROL Displayed Error Message] | Butiksvy | Felmeddelandet som visas när USPS inte är tillgängligt av någon anledning. |

{style="table-layout:auto"}

![USPS-länder](./assets/delivery-methods-usps-countries.png)<!-- zoom -->

<!-- [USPS Applicable Countries](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| _[!UICONTROL USPS Applicable Countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Webbplats | Anger de länder där beställningar kan skickas. Alternativ: <br/>**`All Allowed Countries`**- Kunder från alla [länder](../../getting-started/store-details.md#country-options) som anges i butikskonfigurationen kan använda den här leveransmetoden.<br/>**`Specific Countries`** - När du har valt det här alternativet visas [!UICONTROL Ship to Specific Countries] visas. Välj varje land i listan där leveransmetoden kan användas. |
| [!UICONTROL Show Method if Not Applicable] | Webbplats | Kontrollerar visningen av UPS-leverans vid utcheckning. Alternativ: <br/>**`Yes`**- USPS visas alltid som ett leveransalternativ vid utcheckning, även om det inte gäller för ordern.<br/>**`No`** - USPS visas endast som leveransalternativ vid utcheckning om det är tillämpligt för ordern (dvs. ordervikten överskrider den högsta vikten). |
| [!UICONTROL Debug] | Webbplats | Avgör om en logg över dataöverföringar mellan din butik och USPS hanteras av systemet för felsökning. Om det inte finns något problem som måste spåras och loggas bör det här alternativet anges till `No`. |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som bestämmer i vilken ordning USPS visas när det visas med andra leveransmetoder vid utcheckning. Retur `0` överst i listan. |

{style="table-layout:auto"}

### [!UICONTROL FedEx]

{{beta2-updates}}

![Kontoinställningar för FedEx](./assets/delivery-methods-fedex-account-settings.png)<!-- zoom -->

<!-- [FedEx Account Settings](https://docs.magento.com/user-guide/shipping/fedex.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| _[!UICONTROL FedEx Account Settings]_ |  |  |
| [!UICONTROL Enabled for Checkout] | Webbplats | Avgör om FedEx är tillgängligt för kunder som leveransmetod vid utcheckning. Alternativ: `Yes` / `No` |
| [!UICONTROL Title] | Butiksvy | Titeln på det här leveransalternativet så som det visas i kundvagnskassan. |
| [!UICONTROL Account ID] | Webbplats | Ditt FedEx-konto-ID. |
| [!UICONTROL Meter Number] | Webbplats | Ditt FedEx-mätarnummer. |
| [!UICONTROL Key] | Webbplats | Din FedEx-kontonyckel. |
| [!UICONTROL Password] | Webbplats | Ditt FedEx-kontolösenord. |
| [!UICONTROL Sandbox Mode] | Webbplats | Om du vill köra FedEx-transaktioner i en testmiljö ställer du in sandlådeläget till `Yes`. Alternativ: `Yes` / `No`. |
| [!UICONTROL Web-Services URL] | Webbplats | Vilken URL som krävs beror på inställningen för sandlådeläge. Alternativ: <br/>**`Production`**- URL:en för åtkomst till FedEx-webbtjänster när butiken är aktiv.<br/>**`Sandbox`** - URL:en för att komma åt testmiljön för FedEx-webbtjänster. |

{style="table-layout:auto"}

![FedEx Packaging](./assets/delivery-methods-fedex-packaging.png)<!-- zoom -->

<!-- [FedEx Packaging](https://docs.magento.com/user-guide/shipping/fedex.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| _[!UICONTROL FedEx Packaging Settings]_ |  |  |
| [!UICONTROL Packages Request Type] | Webbplats | Bestämmer hur vikt beräknas för försändelser med flera paket. Alternativ: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Packaging] | Webbplats | I listan väljer du den behållartyp som du vanligtvis använder för att paketera produkter som beställts från din butik. |
| [!UICONTROL Dropoff] | Webbplats | Välj hämtningsmetod i listan: <br/>**`Regular Pickup`**- (Standard) Om du har ett stort antal leveranser kan det vara kostnadseffektivt att ordna regelbundna upphämtningar.<br/>**`Request Courier`** - Du måste anropa och begära ett FedEx-bud för att kunna hämta leveranser. <br/>**`Drop Box`**- Du måste släppa av leveranser i den lokala FedEx-listrutan.<br/>**`Business Service Center`** - Du måste släppa av leveranser på ditt lokala FedEx-affärstjänstcenter. <br/>**`Station`**- Du måste släppa av leveranser på din lokala FedEx-station. |
| [!UICONTROL Maximum Package Weight] | Webbplats | Standardvärdet för FedEx är 150 pund. Kontakta din fraktfirma för att få maximal vikt. Vi rekommenderar att du använder standardvärdet om du inte har särskilda arrangemang med FedEx. |

{style="table-layout:auto"}

![Hanteringsavgift för FedEx](./assets/delivery-methods-fedex-handling-fee.png)<!-- zoom -->

<!-- [FedEx Handling Fee](https://docs.magento.com/user-guide/shipping/fedex.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| _[!UICONTROL FedEx Handling Fee Settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | Webbplats | Bestämmer den metod som används för att beräkna hanteringsavgifter. Alternativ: `Fixed Fee` / `Percentage` <br/><br/>**_Obs!_**Hanteringsavgiften är valfri och visas som en extra avgift som läggs till fraktkostnaden för FedEx. |
| [!UICONTROL Handling Applied] | Webbplats | Avgör hur hanteringsavgifter tillämpas. Alternativ: `Per Order` / `Per Package` |
| [!UICONTROL Handling Fee] | Webbplats | Anger det belopp som debiteras som en hanteringsavgift, baserat på den metod som används för att beräkna beloppet. Om avgiften baseras på en fast avgift, ange beloppet i decimalform, t.ex. `4.90`. Om hanteringsavgiften baseras på en procentandel av ordern anger du beloppet som en procentandel. Om du till exempel vill debitera sex procent av ordern anger du värdet som `.06`. |

{style="table-layout:auto"}

![Leveransmetoder för FedEx](./assets/delivery-methods-fedex-delivery-methods.png)<!-- zoom -->

<!-- [FedEx Delivery Methods](https://docs.magento.com/user-guide/shipping/fedex.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| _[!UICONTROL FedEx delivery methods]_ |  |  |
| [!UICONTROL Residential Delivery] | Webbplats | Ange något av följande, beroende på om du säljer Business-to-Consumer (B2C) eller Business-to-Business (B2B): <br/>**`Yes`**- För B2C-leveranser<br/>**`No`** - För B2B-leveranser |
| [!UICONTROL Allowed Methods] | Webbplats | Välj de leveransmetoder som du stöder i listan. Metoderna beror på ditt FedEx-konto, hur ofta och hur stora dina leveranser är och om du tillåter internationella leveranser. Som handlare kan du välja att endast erbjuda frakt på marken. |
| [!UICONTROL Hub ID] | Webbplats | Ett ID från FedEx som används med [!DNL Smart Post] -metod. |
| [!UICONTROL Free Method] | Webbplats | I listan väljer du den leveransmetod du vill använda för erbjudanden om fri frakt. <br/><br/>**_Obs!_**Den här leveransmetoden liknar den vanliga fraktmetoden, men anges i FedEx leveransalternativ och identifieras som FedEx-leverans. |
| [!UICONTROL Free Shipping Amount Threshold] | Webbplats | Avgör om ett minimiorderbelopp krävs för fri frakt. Alternativ: <br/>**`Enable`**- Ger kostnadsfri FedEx-leverans för beställningar som uppfyller minimibeloppet.<br/>**`Disable`** - Inaktiverar fri FedEx-leverans med minimiorder. |
| [!UICONTROL Free Shipping Amount Threshold] | Webbplats | Anger det minsta orderbelopp som krävs för fri frakt. |
| [!UICONTROL Displayed Error Message] | Butiksvy | Meddelandet som visas när FedEx inte är tillgängligt av någon anledning. Du kan använda standardmeddelandet eller ange ett annat. |

{style="table-layout:auto"}

![FedEx tillämpliga länder](./assets/delivery-methods-fedex-applicable-countries.png)<!-- zoom -->

<!-- [FedEx Applicable Countries](https://docs.magento.com/user-guide/shipping/fedex.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| _[!UICONTROL FedEx Applicable Countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Webbplats | Anger de länder där dina kunder kan leverera med FedEx. Alternativ: <br/>**`All Allowed Countries`**- Kunder från alla [länder](../../getting-started/store-details.md#country-options) som anges i butikskonfigurationen kan använda den här leveransmetoden.<br/>**`Specific Countries`** - När du har valt det här alternativet visas [!UICONTROL Ship to Specific Countries] visas. Välj varje land i listan där leveransmetoden kan användas. |
| [!UICONTROL Ship to Specific Countries] | Webbplats | Anger de specifika länder där dina kunder kan leverera via FedEx. |
| [!UICONTROL Debug] | Webbplats | Avgör om en logg över dataöverföringar mellan din butik och FedEx bevaras av systemet för felsökning. Om det inte finns något problem som måste spåras och loggas bör det här alternativet anges till `No`. |
| [!UICONTROL Show Method if Not Applicable] | Webbplats | Avgör när FedEx visas som en leveransmetod vid utcheckning. Alternativ: <br/>**`Yes`**- Leveransalternativet FedEx visas i leveransmetodlistan, oavsett om beställningen är berättigad att använda den.<br/>**`No`** - Leveransalternativet FedEx visas inte i leveransmetodlistan om det inte gäller för ordern (t.ex. om orderns vikt överstiger den högsta vikten). |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som bestämmer i vilken ordning FedEx ska visas när det visas med andra leveransmetoder vid utcheckning. Retur `0` överst i listan. |

{style="table-layout:auto"}

### [!UICONTROL DHL]

![DHL-kontoinställningar](./assets/delivery-methods-dhl-account-settings.png)<!-- zoom -->

<!-- [DHL Account Settings](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| _[!UICONTROL DHL Account Settings]_ |  |  |
| [!UICONTROL Enabled for Checkout] | Webbplats | Avgör om DHL är tillgängligt för kunder som leveransmetod vid utcheckning. Alternativ: `Yes` / `No` |
| [!UICONTROL Title] | Butiksvy | Titeln på leveransmetoden så som den visas vid utcheckningen. |
| [!UICONTROL Gateway URL] | Webbplats | Vanligtvis kan du acceptera standard-gateway-URL:en. Om DHL har gett dig en alternativ URL anger du värdet i det här fältet. |
| [!UICONTROL Access ID] | Webbplats | Åtkomst-ID för DHL-speditorkontot. |
| [!UICONTROL Password] | Webbplats | Lösenord till DHL-speditorkontot. |
| [!UICONTROL Account Number] | Webbplats | Ditt DHL-fraktkontonummer. |

{style="table-layout:auto"}

![Inställningar för DHL-paket](./assets/delivery-methods-dhl-package-settings.png)<!-- zoom -->

<!-- [DHL Package Settings](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| _[!UICONTROL DHL Package Settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | Webbplats | Hanteringsavgiften är valfri och visas som en extra avgift som läggs till DHL:s fraktkostnad. I listan väljer du den metod som du vill använda för att beräkna hanteringsavgifter. Alternativ: Fast avgift/procent. |
| [!UICONTROL Handling Applied] | Webbplats | I listan väljer du hur du vill att hanteringsavgifterna ska tillämpas. Alternativ: `Per Order` / `Per Package` |
| Hanteringsavgift | Webbplats | Ange det belopp som ska debiteras för en hanteringsavgift, baserat på den metod du har valt för att beräkna beloppet. Om avgiften till exempel baseras på en fast avgift anger du beloppet i decimalform, till exempel `4.90`. Om hanteringsavgiften baseras på en procentandel av ordern anger du beloppet i procent. Om du till exempel debiterar sex procent av ordern anger du värdet som `.06`. |
| [!UICONTROL Divide Order Weight] | Butiksvy | Avgör om en order på över 70 kg kan delas upp i mindre enheter för att säkerställa en korrekt fraktkostnad. Alternativ: `Yes` / `No` |
| [!UICONTROL Weight Unit] | Butiksvy | Bestämmer måttenheten för vikt som används i leveransberäkningar. Alternativ: `Pounds` / `Kilograms` |
| [!UICONTROL Size] | Butiksvy | Anger paketets storlek. Alternativ: <br/>**`Regular`**- De levererade förpackningarna uppfyller kraven i DHL:s standardförpackningsmetoder. I [!UICONTROL Allowed Methods] väljer du de paketeringsmetoder som ska användas för att leverera produkter från din butik.<br/>**`Specific`** - Om levererade paket har anpassade dimensioner fyller du i följande: [!UICONTROL Height (cm)] / [!UICONTROL Depth (cm)] / [!UICONTROL Width (cm)] |

{style="table-layout:auto"}

![Tillåtna DHL-metoder](./assets/delivery-methods-dhl-allowed-methods.png)<!-- zoom -->

<!-- DHL Allowed Methods](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| _[!UICONTROL DHL allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Webbplats | I listan väljer du de leveransmetoder som du stöder. |
| [!UICONTROL Ready Time] | Webbplats | Anger när paketet är klart för hämtning, i timmar, efter att en beställning har skickats. |
| [!UICONTROL Displayed Error Message] | Butiksvy | Det här meddelandet visas när DHL av någon anledning inte är tillgängligt. Du kan använda standardmeddelandet eller skriva ett eget meddelande. |
| [!UICONTROL Free Method] |  | Den här leveransmetoden liknar den vanliga fraktmetoden, men anges i DHL:s leveransalternativ och identifieras som DHL-leverans. I listan väljer du den leveransmetod du vill använda för erbjudanden om fri frakt. |
| [!UICONTROL Free Shipping with Minimum Order Amount] | Webbplats | Ange något av följande: <br/>**`Enable`**- För att möjliggöra fri DHL-leverans för beställningar som uppfyller minimibeloppet.<br/>**`Disable`** - Erbjud ingen fri DHL-leverans med minimiorder. |
| [!UICONTROL Minimum Order Amount for Free Shipping] | Webbplats | Om du aktiverar [!UICONTROL Free Shipping with Minimum Order]anger du minimiorderns belopp i fältet. |

{style="table-layout:auto"}

![DHL-länder](./assets/delivery-methods-dhl-applicable-countries.png)<!-- zoom -->

<!-- [DHL Applicable Countries](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| _[!UICONTROL DHL applicable countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Webbplats | Anger vilket land kunderna får använda den här leveransmetoden. Alternativ: <br/>**Alla tillåtna länder** - Alla länder som tillåts kan använda metoden fri frakt. Tillåtna länder anges i [!UICONTROL General] konfigurationssida. <br/>**Särskilda länder** - Begränsar detta leveransalternativ till de länder som anges i listan Leverans till specifika länder. |
| [!UICONTROL Ship to Specific Countries] | Webbplats | Anger de länder där DHL-leveranser kan skickas. Den här listan över valda länder används om `Specific Countries` är markerat i [!UICONTROL Ship to Applicable Countries] alternativ. |
| [!UICONTROL Show Method if Not Applicable] | Webbplats | Avgör när DHL visas som en leveransmetod vid utcheckning. Alternativ: <br/>**`Yes`**- DHL visas alltid som ett leveransalternativ vid utcheckning, även om det inte gäller för ordern.<br/>**`No`** - DHL visas endast som leveransalternativ vid utcheckning om det är tillämpligt för ordern (dvs. ordervikten överskrider den högsta vikten). |
| [!UICONTROL Debug] | Webbplats | Skapar en loggfil med felinformation. |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som bestämmer i vilken ordning DHL visas när det visas med andra leveransmetoder vid utcheckning. Om du vill placera den högst upp i listan anger du `0`. |

{style="table-layout:auto"}
