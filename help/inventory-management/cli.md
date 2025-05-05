---
title: CLI-referens för [!DNL Inventory Management]
description: Lär dig mer om de kommandon som finns i modulen  [!DNL Inventory Management] för att hantera lagerdata och konfigurationsinställningar.
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# CLI-referens för [!DNL Inventory Management]

[!DNL Inventory Management] innehåller kommandon för att hantera lagerdata och konfigurationsinställningar.

Bland dessa kommandon finns:

- Kontrollera och lösa reservationsinkonsekvenser som påverkar försäljningsbar kvantitet
- Lägga till geokoder för algoritmen Avståndsprioritet

## Lös inkonsekvenser i reservationer

Reservationer placerar en försäljningsbar kvantitet för produkt-SKU:er per lager. När du skickar, lägger till produkter, annullerar eller återför en order, anger du kompensationsreservationer för att placera eller rensa dessa spärrar.

[!DNL Inventory Management] innehåller två kommandon för att kontrollera och lösa reservationsinkonsekvenser:

- [&quot;Inventering:reservation:inkonsekvenser i lista&quot;](#list-inconsistencies-command)
- [&quot;lager:reservation:skapa-kompenseringar&quot;](#create-compensations-command)

### Orsaker till inkonsekvenser i reservationer

[!DNL Inventory Management] genererar reservationer för nyckelhändelser:

- Orderplacering (ursprunglig reservation)
- Orderleverans (kompensationsreservation)
- Återbetalningsorder eller utfärda en kreditnota (reservation för kompensation)
- Annullering av order (kompensationsreservation)

Reservationsinkonsekvenser kan uppstå när:

- [!DNL Inventory Management] förlorar den ursprungliga reservationen och anger för många reservationskompensationer (överkompenserar och leder till inkonsekventa belopp)
- [!DNL Inventory Management] placerar den inledande reservationen korrekt, men förlorar kompensationsreservationer.

Du kan granska och kontrollera reservationer manuellt i tabellen `inventory_reservation`.

Följande konfigurationer och händelser kan orsaka inkonsekvenser i reservationen:

- **Uppgradera till 2.3.x med beställningar som inte är i det slutliga tillståndet (Fullständigt, Avbrutet eller Stängt).** [!DNL Inventory Management] skapar kompenserande reservationer för dessa order, men den varken anger eller har den ursprungliga reservationen som dras från den försäljningsbara kvantiteten. Du bör använda dessa kommandon när du har uppgraderat till Adobe Commerce eller Magento Open Source v2.3.x från 2.1.x eller 2.2.x. Om du har väntande order uppdaterar kommandona din försäljningsbara kvantitet och reservationer korrekt för försäljning och orderhantering.
- **Du hanterar inte Stock och ändrar sedan konfigurationen senare.** Du kan börja använda 2.3.x med **[!UICONTROL Manage Stock]** inställt på `No` i konfigurationen. [!DNL Commerce] placerar inte reservationer vid orderplacerings- och leveranshändelser. Om du senare aktiverar **[!UICONTROL Manage Stock]**-konfigurationen och vissa order skapas, skadas den säljbara kvantiteten med kompensationsreservation när du hanterar och slutför den ordern.
- **Du tilldelar om Stock för en webbplats när du beställer för att få skicka till den webbplatsen**. Den ursprungliga reservationen förs in i det ursprungliga lagret och alla kompensationsreservationer förs in i det nya lagret.
- **Summan av alla reservationer kan inte matchas till `0`.** Alla reservationer inom omfånget för en order i ett slutligt tillstånd (Fullständigt, Avbrutet, Stängt) ska matchas till `0`, så att alla lager för försäljningsbar kvantitet rensas.

### Visa inkonsekvenser, kommando

Kommandot `list-inconsistencies` identifierar och visar alla reservationsinkonsekvenser. Använd kommandoalternativen för att kontrollera endast slutförda eller ofullständiga order, eller alla.

```bash
bin/magento inventory:reservation:list-inconsistencies
```

Kommandoalternativ:

- `-c`, `--complete-orders` - Returnerar inkonsekvenser för slutförda order. Felaktiga reservationer kan fortfarande vara spärrade för slutförda order.
- `-i`, `--incomplete-orders` - Returnerar inkonsekvenser för ofullständiga order (delvis levererade, ej levererade). Felaktiga reservationer kan innehålla för mycket eller för lite säljbar kvantitet för order.
- `-b`, `--bunch-size` - Definierar hur många order som ska läsas in samtidigt.
- `-r`, `--raw` - råutdata.

Svar som använder `-r` retur i `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>`-format:

- Order-ID anger omfattningen för inkonsekvensen.
- SKU anger produkten med inkonsekvensen.
- Kvantitet anger det belopp som ska anges för reservationskompensationen.
- Stock-ID definierar i omfattning för lager, som använder reservationer för att beräkna försäljningsbar kvantitet.

Exempel:

```bash
bin/magento inventory:reservation:list-inconsistencies

Inconsistencies found on following entries:
Order 172:
- Product bike-123 should be compensated by +2.000000 for stock 1
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r

172:bike-123:+2.000000:1
```

Om inga problem hittas returneras meddelandet: Inga orderinkonsekvenser hittades.

### Skapa kompenseringar, kommando

Kommandot `create-compensations` skapar kompensationsreservationer. Beroende på utgåvan skapas nya reservationer för att antingen placera eller frisläppa en spärr för försäljningsbar kvantitet.

Om du vill skapa reservationer anger du kompenseringar med formatet `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>`, till exempel `172:bike-123:+2.000000:1`.

```bash
bin/magento inventory:reservation:create-compensations
```

Kommandoalternativ:

- `-r`, `--raw` - Returnerar råutdata.

Om begäran har ett felaktigt format visas följande meddelande:

```
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

När kommandot skapar bokningar visas meddelanden som anger uppdateringarna efter SKU, ordning och lager.

```bash
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

Om SKU:n för en kompensationspost innehåller mellanslag, omsluter du SKU:n med citattecken.

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### Identifiera inkonsekvenser och skapa kompenseringar

Du kan identifiera inkonsekvenser och omedelbart skapa kompenseringar genom att använda ett rör för att köra både `list-inconsistencies` och `create-compensations`. Använd kommandoalternativet `-r` för att generera och skicka rådata till `create-compensations`.

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

Exempelsvar:

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

```
Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
- Product bikehat-456 was compensated by +1.000000 for stock 1
```

När uppdateringarna är klara kör du listkommandot för att verifiera:

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```
No order inconsistencies were found.
```

Du kan också flytta kommandona för att identifiera inkonsekvenser och skapa kompenseringar för endast ofullständiga (`-i`) eller fullständiga (`-c`) order.

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## Importera geokoder

[!DNL Inventory Management] innehåller algoritmen [Distansprioritet](distance-priority-algorithm.md) som hjälper dig att avgöra vilket alternativ som är bäst för att leverera en fullständig eller partiell order. Algoritmen använder GPS-information eller geokoder för att beräkna avståndet mellan källan (ett lagerställe eller annan fysisk plats) för varje artikel i en order och leveransadressen. Med utgångspunkt i dessa resultat rekommenderar algoritmen vilken källa som ska användas för att skicka ut varje objekt i ordningen.

Handlaren väljer leverantör av GPS- eller geokoddata som krävs för att beräkna avstånd:

- **Google MAP** använder [Google Maps Platform](https://mapsplatform.google.com/)-tjänster för att beräkna avståndet och tiden mellan leveransdestinationsadressen och källplatserna. Det här alternativet kräver en Google-faktureringsplan och kan medföra avgifter via Google.

- **Offlineberäkning** beräknar avståndet med data som hämtats från [geonames.org](https://www.geonames.org/) och importerats till Commerce med ett kommando. Det här alternativet är kostnadsfritt.

Så här importerar du geokoder för offlineberäkning:

Ange följande kommando med en blankstegsavgränsad lista med [ISO-3166 alpha2-landskoder](https://www.geonames.org/countries/):

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

Exempel:

```bash
bin/magento inventory-geonames:import us ca gb de
```

Systemet hämtar och importerar geokodsdata till din databas och visar sedan meddelandet `Importing <country code>: OK`.
