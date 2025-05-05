---
title: Source algoritmer och reservationer
description: Läs mer om Source Selection Algorithm and Reservations systems som körs i bakgrunden för att hålla dina säljbara kvantiteter uppdaterade.
exl-id: dcd63322-fb4c-4448-b6e7-0c54350905d7
feature: Inventory, Shipping/Delivery
source-git-commit: fdc14758788fa5cd0391371ebfafb478dadec8a4
workflow-type: tm+mt
source-wordcount: '2196'
ht-degree: 0%

---

# Source algoritmer och reservationer

Kärnan i [!DNL Inventory Management] spårar alla tillgängliga produkter praktiskt taget och i era lagerlokaler och butiker. Systemen Source Selection Algorithm and Reservations körs i bakgrunden, vilket håller dina säljbara kvantiteter uppdaterade, checkar ut utan kollisioner och leveransalternativ rekommenderas.

>[!NOTE]
>
>Mer information om att arbeta med [!DNL Inventory Management]-systemet med programkod finns i [utvecklardokumentationen](https://developer.adobe.com/commerce/php/development/framework/inventory-management/).

## Source Selection Algorithm

Source Selection Algorithm (SSA) analyserar och fastställer den bästa matchningen för källor och leveranser med hjälp av prioritetsordningen för källor som konfigurerats i ett lager. Vid orderleverans innehåller algoritmen en rekommenderad lista över källor, tillgängliga kvantiteter och belopp som ska dras av enligt den valda algoritmen. [!DNL Inventory Management] innehåller en prioritetsalgoritm och stöder tillägg för nya alternativ.

Med flera olika platser kan globala kunder och transportföretag med olika leveransalternativ och fraktavgifter vara svåra att hitta, eftersom ni vet att ert faktiska lager är tillgängligt och att det är svårt att hitta det bästa leveransalternativet. SSA utför arbetet åt dig från att spåra lagerförsäljningsbara kvantiteter över alla källor till att beräkna och göra rekommendationer för leveranser.

**Spåra lager** - Med hjälp av lager och källor kontrollerar SSA försäljningskanalen för inkommande produktbegäranden och fastställer tillgängligt lager:

- Beräknar den aggregerade virtuella försäljningsbara kvantiteten för alla tilldelade källor per lager: aggregerad kvantitet - tröskelvärde för lagerutleverans per källa
- Subtraherar tröskelvärdet för lagerutleverans från säljbar kvantitet för att skydda mot överförsäljning
- Reserverar lagerkvantiteter vid orderinlämning, avdrag från lagerbehållning vid orderbearbetning och leverans
- Stöder backorder med utökade alternativ för negativa tröskelvärden

**Hantera leveranser** - Algoritmen hjälper dig att bearbeta och skicka beställningar. Du kan köra algoritmen för att få rekommendationer om de bästa källorna för leverans av produkten eller åsidosätta valen till:

- Leverera partiella leveranser, skicka endast ett fåtal produkter från specifika platser och slutför hela beställningen senare
- Leverera hela beställningen från en källa
- Dela upp försändelserna mellan flera källor i olika mängder, och ha ett balanserat lager i alla lagerställen och butiker

SSA kan utökas för support från tredje part och anpassade algoritmer för att rekommendera kostnadseffektiva leveranser.

>[!NOTE]
>
>SSA fungerar annorlunda för virtuella och nedladdningsbara produkter, vilket kanske inte medför fraktkostnader. I dessa fall körs algoritmen implicit när den skapar fakturor och de föreslagna resultaten används alltid. Du kan inte justera dessa resultat för virtuella och hämtningsbara produkter.

### Source prioritetsalgoritm

Anpassade lager innehåller en lista över källor att sälja och leverera tillgängligt produktlager via din butik. Source prioritetsalgoritm använder ordningen för tilldelade källor i lagret för att rekommendera produktavdrag per källa vid fakturering och leverans av ordern.

Vid körning, algoritmen:

- Fungerar genom den konfigurerade källordningen på lagernivå med början överst
- Rekommenderar en kvantitet att leverera och källa per produkt baserat på beställningsordningen, tillgänglig kvantitet och beställd kvantitet
- Fortsätter nedåt i listan tills orderleveransen har fyllts i
- Hoppar över inaktiverade källor om de hittas i listan

Om du vill konfigurera, tilldela och beställa källor till ett anpassat lager. Se [Prioritera källor för en Stock](stocks-prioritize-sources.md).

I följande exempel visas mappade källor i ordning, tillgängligt antal och rekommenderad källa och belopp att dra av och skicka. Den främsta källan är en Drop Shipper i Storbritannien med en tillgänglig kvantitet på 240.

![Exempel på SSA-rekommendationer för en bergscykel](assets/ssa-sources-example.png){width="600" zoomable="yes"}

### Avståndsprioritetsalgoritm

Algoritmen Avståndsprioritet jämför platsen för leveransdestinationsadressen med källplatserna för att fastställa den närmaste källan för leverans av försändelser. Avståndet kan bestämmas genom fysiskt avstånd eller den tid som tillbringas med att resa från en plats till en annan med hjälp av importerade databasplatser eller Google-anvisningar (körning, gång eller cykling).

Du har två alternativ för att beräkna avståndet och tiden för att hitta den närmaste källan för leverans:

- **Google MAP** - Använder [Google Maps Platform][1]-tjänster för att beräkna avståndet och tiden mellan leveransdestinationsadressen och källplatserna (adress och GPS-koordinater). Det här alternativet använder källans latitud och longitud. En Google API-nyckel krävs med [API för geokodning][2] och [API:t för distansmatris][3] aktiverat. Det här alternativet kräver en Google-faktureringsplan och kan medföra avgifter via Google.

- **Offlineberäkning** - Beräknar avståndet med nedladdade och importerade geokoddata för att fastställa närmaste källa till leveransens måladress. Det här alternativet använder landskoderna för leveransadressen och källan. Om du vill konfigurera det här alternativet kan du behöva utvecklarassistans för att initialt hämta och importera geokoder via en kommandorad.

Om du vill konfigurera väljer du konfigurationer och slutför ytterligare steg som Google API-nyckeln eller hämtar leveransdata. Se [Konfigurera algoritmen för avståndsprioritet](distance-priority-algorithm.md).

### Anpassade algoritmer

[!DNL Commerce] stöder anpassad utveckling och tillägg för att lägga till alternativa algoritmer för att prioritera källor. Du kan t.ex. ha en prioritetsalgoritm som baseras på geografi och en annan som baseras på utgiften av stocken eller ett kundattribut. När kostnaden för Stock ändras kan implementeringen enkelt ändra algoritmer för att säkerställa lägsta kostnad.

## Reservationer

I stället för att omedelbart dra av eller lägga till produktlagerkvantiteter håller reservationer lagerbelopp tills order skickas eller annulleras. Reservationer fungerar helt och hållet i bakgrunden för att automatiskt uppdatera din försäljningsbara kvantitet på lagernivå.

>[!NOTE]
>
>[!BADGE PaaS endast]{type=Informative url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."} Reservationsfunktionen kräver att meddelandekökonsumenten `inventory.reservations.updateSalabilityStatus` körs kontinuerligt. Använd kommandot `bin/magento queue:consumers:list` om du vill kontrollera om det körs. Om meddelandekökonsumenten inte finns med i listan startar du den: `bin/magento queue:consumers:start inventory.reservations.updateSalabilityStatus`.

### Beställningsreservationer

Reservationsplats håller på lagerkvantiteter som dras av från den försäljningsbara kvantiteten när en order skickas. Reservationerna är på lagernivå, och räknas mot kvantiteter tills ordern har fakturerats och skickats, annullerats och så vidare. När du skickar ordern kan du använda SSA-rekommendationerna eller manuellt ange kvantitetsavdrag per källa. Vid leverans rensas reservationerna automatiskt och kvantiteten dras av. Den försäljningsbara kvantiteten omberäknas för lagret med en uppdaterad kvantitet och eventuella reservationsbelopp som återstår i systemet.

Följande diagram hjälper till att definiera processen för reservationer under en order och fram till leverans.

![Reservationer från beställning till leverans](assets/diagram-quantity.png){width="600" zoomable="yes"}

En kund skickar en order. [!DNL Commerce] kontrollerar den aktuella lagerförsäljningskvantiteten. Om det finns tillräckligt med lager på lagernivå, kan en reservation placera en tillfällig förvaring för produkt-SKU (för det lagret) och beräkna om den försäljningsbara kvantiteten.

När du har fakturerat ordern bestämmer du vilka produktbelopp som ska dras av och skickas från källorna. Leveransen bearbetas och skickas från en eller flera valda källor till kunden. Kvantiteterna dras automatiskt från källagrets kvantitet och reservationer som är klara. Fullständig information och exempel finns i [Om beställningsstatus och beställning](order-status.md).

## Reservationsberäkningar

Systemet skapar en reservation för varje produkt när följande händelser inträffar:

- En kund eller handlare gör en beställning.
- En kund eller handlare annullerar en order helt eller delvis.
- Handlaren skapar en leverans för en fysisk produkt.
- Handlaren skapar en faktura för en virtuell eller nedladdningsbar produkt.
- Handlaren utfärdar en kreditnota.

Reservationer är åtgärder som bara kan läggas till som tillägg, ungefär som en logg med händelser. Den ursprungliga reservationen tilldelas ett negativt kvantitetsvärde. Alla efterföljande reservationer som skapas när ordern bearbetas är positiva värden. När ordern är slutförd är summan av alla reservationer för produkten 0.

Innan systemet kan utfärda en reservation som svar på en ny order, avgör det om det finns tillräckligt med säljbara artiklar för att ordern ska kunna utföras. Följande kvantitetsfaktor i beräkningen:

- **StockItem-kvantitet**. StockItem-kvantiteten är den aggregerade lagermängden från alla fysiska källor för den aktuella försäljningskanalen. Tänk dig ett exempel där Baltimore-källan har 20 enheter av en produkt, där Austin-källan har 25 enheter av samma produkt och Reno-källan har 10. När alla dessa källor är kopplade till Stock A är antalet StockItem för den här produkten 55 (20 + 25 + 10). (När artiklar levereras uppdaterar lagerindexeraren de tillgängliga kvantiteterna vid varje källa.)

- **Utestående reservationer**. Systemet summerar alla ursprungliga reservationer som inte har kompenserats. Talet är alltid negativt. Om kund A har en reservation för tio artiklar, och kund B har en reservation på 5 för artiklar, så har vi utestående reservationer för produktsumman -15.

Handlaren kan därför utföra en inkommande order så länge som kunden beställer mindre än 40 (55 + -15) enheter.

När du har slutfört bearbetningen av en order (Fullständigt, Avbrutet, Stängt), bör alla reservationer i orderns omfattning matchas till `0`. Detta rensar alla försäljningsbara kvantiteter.

>[!NOTE]
>
>Restorder (med tröskelvärden utanför lager) och Notify for Quantity Under Threshold settings (Meddela om kvantitet under tröskelvärde) påverkar också beräkningen av försäljningsbara kvantiteter, men de ligger utanför det här ämnets räckvidd. Mer information om de här inställningarna finns i [Konfigurera [!DNL Inventory Management]](./configuration.md).

## Reservationsobjekt

En reservation innehåller följande information:

| Parameter | Datatyp | Beskrivning |
| --- | --- | --- |
| `reservation_id` | Heltal | Ett systemgenererat ID |
| `stock_id` | Heltal | ID för det lager som produkten är tilldelad till |
| `sku` | Sträng | Produktens SKU |
| `quantity` | Float | Antalet artiklar i den här reservationen |
| `metadata` | Sträng | Händelsetyp, objekttyp och objekt-ID för denna reservation. Exempel: `{"event_type":"order_placed","object_type":"order",| "object_id":"8"}` |

{style="table-layout:auto"}

Metadata `event_type` kan ha följande värden:

- `order_placed`
- `order_canceled`
- `shipment_created`
- `creditmemo_created`
- `invoice_created`

För närvarande måste metadataobjektstypen vara `order` och objekt-ID:t är order-ID:t.

I framtida versioner kan det vara möjligt att skapa en reservation när en kund lägger till en artikel i en kundvagn. Varje artikel kan reserveras för en fast tidsperiod, t.ex. 15 minuter, så att kunden kan reservera artiklar medan han/hon fortsätter att handla. När den här typen av reservation är aktiverad kan metadata innehålla ytterligare typer av information.

## Reservationslivscykel

I följande exempel visas sekvensen med reservationer som genererats för en enkel order.

1. Kunden gör en inköpsorder för 25 enheter av produkten `SKU-1`. Reservationen innehåller följande information:

   ```text
   reservation_id = 1
   stock_id = 1
   sku = SKU-1
   quantity = -25
   event_type = order_placed
   ```

1. Kunden skickar en faktura för 20 artiklar, vilket innebär att 5 av de beställda enheterna annulleras.

   ```text
   reservation_id = 2
   stock_id = 1
   sku = SKU-1
   quantity = 5
   event_type = order_canceled
   ```

1. Handlaren levererar de köpta 20 enheterna.

   ```text
   reservation_id = 3
   stock_id = 1
   sku = `SKU-1`
   quantity = 20
   event_type = shipment_created
   ```

De tre `quantity`-värdena är summerade till 0 (-25 + 5 + 20). Systemet ändrar inga befintliga reservationer.

## Tar bort bearbetade reservationer

Kronjobbet `inventory_cleanup_reservations` kör SQL-frågor för att rensa reservationsdatabastabellen. Som standard körs den varje dag vid midnatt, men du kan konfigurera tider och frekvens. Kronjobbet kör ett skript som frågar databasen efter fullständiga reservationssekvenser där summan av kvantitetsvärdena är 0. När alla reservationer för en viss produkt som har sitt ursprung samma dag (eller annan konfigurerad tid) har kompenserats, tar kronijobbet bort alla reservationer samtidigt.

Kronijobbet `inventory_reservations_cleanup` är inte detsamma som meddelandekökonsumenten `inventory.reservations.cleanup`. Konsumenten tar asynkront bort reservationer per produkt-SKU efter att en produkt har tagits bort, medan kronijobbet rensar hela reservationstabellen. Konsumenten krävs när du aktiverar alternativet [**Synkronisera med katalog**](../configuration-reference/catalog/inventory.md) i butikskonfigurationen. Se [Hantera meddelandeköer](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html?lang=sv-SE) i _Konfigurationshandboken_.

Ofta går det inte att kompensera alla ursprungliga reservationer som gjorts under en och samma dag. Detta kan inträffa när en kund gör en beställning precis innan kronijobbet påbörjas eller gör ett köp med en offlinebetalningsmetod, som en banköverföring. De kompenserade reservationssekvenserna finns kvar i databasen tills de alla kompenseras. Denna praxis påverkar inte reservationsberäkningar, eftersom summan för varje reservation är 0.

>[!NOTE]
>
>Det finns CLI-kommandon som du kan använda för att identifiera och hantera reservationsinkonsekvenser (se [[!DNL Inventory Management] CLI-referens](cli.md)).

### Reservationsuppdateringar

När ändringar är slutförda i order och produktbelopp registrerar [!DNL Commerce] automatiskt reservationskompensationer. Du behöver inte ange kompenseringar via administratören eller koden för att uppdatera eller rensa dessa spärrar. Reservationer påverkas endast av angivna reservationer för att spärra en kvantitet eller för att rensa ett spärrbelopp (som kompenserar för reservationerna).

Så här fungerar de:

- **Skickad order** - När en order skickas för flera produkter, bokförs en reservation för det beloppet. Om du t.ex. beställer fem bakåtpaket från en amerikansk webbplats får du en reservation på `-5` för denna SKU och detta lager. Den säljbara kvantiteten minskas med 5.

- **Avbruten order** - När en order annulleras (helt eller delvis), bokförs en kompensationsreservation för att rensa beloppet. Om du till exempel avbryter tre ryggpaket anges en +3-reservation för den SKU:n och aktien, vilket rensar spärren. Den säljbara kvantiteten ökas med 3.

- **Levererad order** - När en order levereras (helt eller delvis), bokförs en kompensation för att rensa beloppet. Om du till exempel skickar två bakpaket anges en +2-reservation för den SKU:n och aktien, vilket rensar spärren. Produktkvantiteten minskas direkt med 2 för leveransen. Den beräknade försäljningsbara kvantiteten uppdateras också för det reducerade lagerbeloppet, men påverkas inte längre av reservationen.

![Reservationsuppdateringar](assets/diagram-reservation.png){width="600" zoomable="yes"}

Alla reservationer måste rensas av kompenseringar när order har slutförts, produkter har annullerats, kreditnotor har utfärdats osv. Om det inte går att ta bort reservationer med kompensationer kan du ha kvantiteter i stas (som inte går att sälja och aldrig levereras).

>[!NOTE]
>
>Om du vill granska reservationer finns det ett antal kommandoradsalternativ. Du kan bara granska reservationer via ett kommandoradsgränssnitt. Det kan krävas utvecklarhjälp för att använda CLI-kommandon. Se [[!DNL Inventory Management] CLI-referens](cli.md).

Om du tar bort alla källor från en produkt för ett lager med väntande order kan du ha fastnat i reservationer.

{{$include /help/_includes/unassign-source.md}}

[1]: https://cloud.google.com/maps-platform/
[2]: https://developers.google.com/maps/documentation/geocoding/start
[3]: https://developers.google.com/maps/documentation/distance-matrix/start
