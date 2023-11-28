---
title: Skatter
description: Lär dig hur du konfigurerar din butik för att beräkna skatter enligt kraven för din språkinställning.
exl-id: bf807132-416f-497a-82c4-b00dba4d3092
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1115'
ht-degree: 0%

---

# Skatter

Konfigurera din butik för att beräkna skatter enligt kraven för din språkinställning. Du kan konfigurera [momsklasser](tax-class.md) för produkter och kundgrupper, och skapa [momsregler](tax-rules.md) som kombinerar produkt- och kundklasser, skattezoner och skattesatser. Commerce innehåller även konfigurationsinställningar för fasta produktskatter, sammansatta skatter och visning av priser över internationella gränser. Om du måste samla in en [moms](vat.md)kan du konfigurera din butik så att den automatiskt beräknar lämplig mängd med validering.

>[!NOTE]
>
>Adobe Commerce och Magento Open Source, version 2.4.0 till 2.4.3, innehåller tillägget Vertex som utvecklades av leverantören och som används för att integrera med Vertex Cloud för att tillhandahålla skattehantering och adressrensning. Från och med version 2.4.4 är det här tillägget inte längre bundet till kärnversionen och måste installeras och uppdateras från Commerce Marketplace eller direkt från leverantören. [Kontakthörn](https://marketplace.magento.com/partner/vertex_inc) om du vill ha information om tillägget och dokumentationen.<br><br>
>
>Om du har det paketerade tillägget aktiverat och konfigurerat måste du uppdatera filen Composer.json som en del av uppgraderingsprocessen för 2.4.4 och hantera tilläggsuppdateringar vidare. Se [Uppgraderingsmoduler](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) i _Uppgraderingshandbok_.

## Snabbreferens

Vissa skatteinställningar har ett val av alternativ som bestämmer hur skatten beräknas och presenteras för kunden. Mer information finns i [Internationella skatteriktlinjer](international-tax-guidelines.md).

Använd följande tabeller som referens när du konfigurerar inställningar för momsberäkning:

### Momsberäkningsmetoder

Alternativ för beräkningsmetod för moms inkluderar [!UICONTROL Unit Price], [!UICONTROL Row Total]och [!UICONTROL Total]. I följande tabell beskrivs hur avrundning (till två siffror) hanteras för olika inställningar.

| Inställning | Beräkning och visning |
|--- |--- |
| [!UICONTROL Unit Price] | Commerce beräknar momsen för varje artikel och visar priser inklusive moms. För att beräkna den totala momssumman avrundas momsen för varje artikel och läggs sedan ihop. |
| [!UICONTROL Row Total] | Commerce beräknar momsen för varje rad. För att beräkna den totala momssumman avrundas momsen för varje radartikel och läggs sedan ihop. |
| [!UICONTROL Total] | Commerce beräknar momsen för varje artikel och lägger till dessa momsvärden för att beräkna det totala oavrundade momsbeloppet för ordern. Sedan tillämpas det angivna avrundningsläget på den totala momsen för att fastställa orderns totala moms. |

{style="table-layout:auto"}

### Katalogpriser med eller utan moms

De möjliga visningsfälten varierar beroende på beräkningsmetoden och om katalogpriserna innehåller eller exkluderar skatter. Visningsfält har två decimaler i normala beräkningar. I vissa kombinationer av prisinställningar visas priser som både inkluderar och exkluderar moms. När båda visas på samma radartikel kan det vara förvirrande för kunderna och utlösa en [varning](taxes.md#warning-messages).

| Inställning | Beräkning och visning |
|--- |--- |
| [!UICONTROL Excluding Tax] | Med den här inställningen används basartikelpriset som det anges och momsberäkningsmetoderna används. |
| [!UICONTROL IncludingTax] | Med den här inställningen beräknas det basartikelpris som exkluderar moms först. Det här värdet används som baspris och momsberäkningsmetoderna används. |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Det finns förändringar jämfört med tidigare versioner för EU-handlare eller andra momshandlare som visar priser, inklusive skatt, och som är verksamma i flera länder med olika butiksvyer. Om ni läser in priser med fler än två siffror avrundar Commerce automatiskt alla priser till två siffror för att säkerställa att ett konsekvent pris presenteras för köparna.

### Leveranspriser med eller utan moms

| Inställning | Visa | Beräkning |
|--- |--- |--- |
| [!UICONTROL Excluding Tax] | Visas utan moms. | Normal beräkning. Leverans läggs till i kundvagnssumman, som vanligtvis visas som en separat artikel. |
| [!UICONTROL Including Tax] | Kan vara inklusive moms, eller moms kan visas separat. | Leverans behandlas som en annan artikel i varukorgen med skatter, med samma beräkningar. |

{style="table-layout:auto"}

### Momsbelopp som radartiklar

Om du vill visa två olika momsbelopp som separata radobjekt, till exempel GST och PST för kanadensiska butiker, måste du ange olika prioriteringar för relaterade momsregler. I tidigare skatteberäkningar skulle dock skatter med olika prioriteringar automatiskt kompletteras. Om du vill visa separata skattebelopp utan att göra en felaktig sammanställning av momsbeloppen kan du ange olika prioriteringar och även välja _Beräkna endast av delsumma_ kryssrutan. Den här inställningen skapar korrekt beräknade momsbelopp som visas som separata radartiklar.

## Varningsmeddelanden

Vissa kombinationer av skatterelaterade alternativ kan vara förvirrande för kunderna och utlösa en varning. Dessa villkor kan uppstå när momsberäkningsmetoden är inställd på `Row` eller `Total`och kunden får priser som både exkluderar och inkluderar moms. Den kan också inträffa när det finns moms per artikel i kundvagnen. Eftersom momsberäkningen är avrundad kan beloppet som visas i kundvagnen skilja sig från det belopp som kunden förväntar sig att betala.

Om momsberäkningen baseras på en problematisk konfiguration visas följande varningar:

![Utropstecken](../assets/icon-warning.png) **Varning**. `Tax discount configuration might result in different discounts than a customer might expect for store(s); Europe Website (French), Europe Website (German). Please see source for more details.`

![Utropstecken](../assets/icon-warning.png) **Varning**. `Tax configuration can result in rounding errors for store(s): Europe Websites (French), Europe Websites (German).`

## Leveransort för digitala varor (EU)

Handlare inom EU måste rapportera sina digitala varor som säljs kvartalsvis till varje medlemsland. Digitala varor beskattas baserat på kundens leveransadress. Enligt lagen ska handlarna göra en skatterapport och identifiera relevanta skattebelopp för digitala varor, till skillnad från fysiska varor.

Handlarna måste varje kvartal rapportera alla digitala varor som sålts av EU:s medlemsstater till en central skattemyndighet, tillsammans med betalning för skatt som tagits ut under perioden.

Handlare som ännu inte har nått tröskelvärdet (50 000/100 00 euro i årsverksamhet) måste fortsätta att rapportera fysiska varor som sålts till de EU-länder där de har registrerade momsregistreringsnummer.

Handlare som är föremål för revision av skatter som betalas för digitala varor måste lämna två stödjande uppgifter för att fastställa kundens bostad.

- Kundens leveransadress och ett kvitto på en lyckad betalningstransaktion kan användas för att fastställa kundens bosättningsort. (Betalning accepteras endast om leveransadressen stämmer överens med betalarens information.)
- Informationen kan också hämtas direkt från datalagret i Commerce-databastabellerna.

_**Så här samlar du in skatteinformation för digitala varor:**_

1. Läs in skattesatserna för alla EU:s medlemsländer.

1. Skapa en produktskatalog för digitala varor.

1. Tilldela alla era digitala varor till produktskatterna för digitala varor.

1. Skapa [momsregler](tax-rules.md) för fysiska varor, med användning av fysiska produktskatteklasser och koppla dem till lämpliga skattesatser.

1. Skapa skatteregler för era digitala varor med produktskatterna för digitala varor och koppla dem till lämplig skattesats för EU:s medlemsländer.

1. Kör momsrapporten för lämplig period och samla in den information om digitala varor som krävs.

1. Exportera de skattebelopp som är relaterade till skattesatserna för produktskatterna för digitala varor.

Ytterligare resurser:

- [Europeiska kommissionens skatteunion och tullunion][1]
- [EU 1015 Förändringar av leveransplats][2]

[1]: https://europa.eu/youreurope/business/taxation/vat/vat-rules-rates/index_en.htm
[2]: https://www2.deloitte.com/global/en/services/tax.html
