---
title: '''[!DNL Inventory Management] CLI-referens'
description: Läs mer om kommandona i [!DNL Inventory Management] för att hantera lagerdata och konfigurationsinställningar.
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---

# [!DNL Inventory Management] CLI-referens

[!DNL Inventory Management] innehåller kommandon för att hantera lagerdata och konfigurationsinställningar.

Bland dessa kommandon finns:

- Kontrollera och lösa reservationsinkonsekvenser som påverkar försäljningsbar kvantitet
- Lägga till geokoder för algoritmen Avståndsprioritet

## Lös inkonsekvenser i reservationer

Reservationer placerar en försäljningsbar kvantitet för produkt-SKU:er per lager. När du skickar, lägger till produkter, annullerar eller återför en order, anger du kompensationsreservationer för att placera eller rensa dessa spärrar.

[!DNL Inventory Management] innehåller två kommandon för att kontrollera och lösa reservationsinkonsekvenser:

- [`lager:reservation:inkonsekvenser i listor`A](#list-inconsistencies-command)
- [`lager:reservation:skapa-kompensering`](#create-compensations-command)

### Orsaker till inkonsekvenser i reservationer

[!DNL Inventory Management] genererar reservationer för viktiga händelser:

- Orderplacering (ursprunglig reservation)
- Orderleverans (kompensationsreservation)
- Återbetalningsorder eller utfärda en kreditnota (reservation för kompensation)
- Annullering av order (kompensationsreservation)

Reservationsinkonsekvenser kan uppstå när:

- [!DNL Inventory Management] förlorar den ursprungliga reservationen och anger för många reservationskompensationer (överkompenserar och leder till inkonsekventa belopp)
- [!DNL Inventory Management] placerar den inledande reservationen korrekt, men förlorar kompenserande reservationer.

Du kan manuellt granska och kontrollera bokningar i `inventory_reservation` tabell.

Följande konfigurationer och händelser kan orsaka inkonsekvenser i reservationen:

- **Uppgradera till 2.3.x med beställningar som inte är klara (Fullständigt, Avbrutet eller Stängt).** [!DNL Inventory Management] skapar kompenserande reservationer för dessa order, men anger eller har inte den ursprungliga reservationen som dras av från den försäljningsbara kvantiteten. Du bör använda dessa kommandon när du har uppgraderat till Adobe Commerce eller Magento Open Source v2.3.x från 2.1.x eller 2.2.x. Om du har väntande order uppdaterar kommandona din försäljningsbara kvantitet och reservationer korrekt för försäljning och orderhantering.
- **Du hanterar inte Stock och ändrar sedan konfigurationen senare.** Du kan börja använda 2.3.x med **[!UICONTROL Manage Stock]** ange till `No` i konfigurationen. [!DNL Commerce] bokar inte reservationer vid orderplacering och försändelsehändelser. Om du aktiverar **[!UICONTROL Manage Stock]** konfiguration och en del order skapas. Den säljbara kvantiteten skadas med kompensationsreservation när du hanterar och slutför ordern.
- **Du omtilldelar Stock för en webbplats när beställningar skickas till den webbplatsen**. Den ursprungliga reservationen förs in i det ursprungliga lagret och alla kompensationsreservationer förs in i det nya lagret.
- **Summan av alla reservationer kan inte tolkas som `0`.** Alla reservationer inom omfånget av en order i ett slutligt tillstånd (Fullständigt, Avbrutet, Stängt) ska tolkas som `0`, rensar alla lager för försäljningsbar kvantitet.

### Visa inkonsekvenser, kommando

The `list-inconsistencies` kommandot identifierar och visar alla reservationsinkonsekvenser. Använd kommandoalternativen för att kontrollera endast slutförda eller ofullständiga order, eller alla.

```bash
bin/magento inventory:reservation:list-inconsistencies
```

Kommandoalternativ:

- `-c`, `--complete-orders` - Returnerar inkonsekvenser för slutförda order. Felaktiga reservationer kan fortfarande vara spärrade för slutförda order.
- `-i`, `--incomplete-orders` - Returnerar inkonsekvenser för ofullständiga order (delvis levererade, ej levererade). Felaktiga reservationer kan innehålla för mycket eller för lite säljbar kvantitet för order.
- `-b`, `--bunch-size` - Definierar hur många order som ska läsas in samtidigt.
- `-r`, `--raw` - Råutdata.

Svar med `-r` return in `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` format:

- Order-ID anger omfattningen för inkonsekvensen.
- SKU anger produkten med inkonsekvensen.
- Kvantitet anger det belopp som ska anges för reservationskompensationen.
- Stock-ID definierar i omfattning för lager, som använder reservationer för att beräkna försäljningsbar kvantitet.

Exempel:

```terminal
bin/magento inventory:reservation:list-inconsistencies

Inconsistencies found on following entries:
Order 172:
- Product bike-123 should be compensated by +2.000000 for stock 1
```

```terminal
bin/magento inventory:reservation:list-inconsistencies -r

172:bike-123:+2.000000:1
```

Om inga problem hittas returneras meddelandet: Inga orderinkonsekvenser hittades.

### Skapa kompenseringar, kommando

The `create-compensations` kommandot skapar kompensationsreservationer. Beroende på utgåvan skapas nya reservationer för att antingen placera eller frisläppa en spärr för försäljningsbar kvantitet.

Skapa reservationer genom att ange kompenseringar med formatet `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` som `172:bike-123:+2.000000:1`.

```bash
bin/magento inventory:reservation:create-compensations
```

Kommandoalternativ:

- `-r`, `--raw` - Returnerar råutdata.

Om begäran har ett felaktigt format visas följande meddelande:

```terminal
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

När kommandot skapar bokningar visas meddelanden som anger uppdateringarna efter SKU, ordning och lager.

```terminal
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

Om SKU:n för en kompensationspost innehåller mellanslag, omsluter du SKU:n med citattecken.

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### Identifiera inkonsekvenser och skapa kompenseringar

Du kan upptäcka inkonsekvenser och omedelbart skapa kompenseringar genom att använda ett rör för att köra båda `list-inconsistencies` och `create-compensations`. Använd `-r` kommandoalternativ för att generera och skicka rådata till `create-compensations`.

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

Exempelsvar:

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

```terminal
Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
- Product bikehat-456 was compensated by +1.000000 for stock 1
```

När uppdateringarna är klara kör du listkommandot för att verifiera:

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```terminal
No order inconsistencies were found.
```

Du kan också flytta kommandona för att upptäcka inkonsekvenser och skapa kompenseringar för endast ofullständiga (`-i`) eller fullständigt (`-c`) beställningar.

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## Importera geokoder

[!DNL Inventory Management] ger [Algoritmen Avståndsprioritet](distance-priority-algorithm.md), som hjälper till att avgöra vilket alternativ som är bäst för att leverera en hel eller delvis beställning. Algoritmen använder GPS-information eller geokoder för att beräkna avståndet mellan källan (ett lagerställe eller annan fysisk plats) för varje artikel i en order och leveransadressen. Med utgångspunkt i dessa resultat rekommenderar algoritmen vilken källa som ska användas för att skicka ut varje objekt i ordningen.

Handlaren väljer leverantör av GPS- eller geokoddata som krävs för att beräkna avstånd:

- **GOOGLE MAP** använder [Google Maps Platform](https://mapsplatform.google.com/) tjänster för att beräkna avståndet och tiden mellan leveransdestinationsadressen och källplatserna. Det här alternativet kräver en Google-faktureringsplan och kan medföra avgifter via Google.

- **Offlineberäkning** beräknar avståndet med data som hämtas från [geonames.org](https://www.geonames.org/) och importerade till Commerce med ett kommando. Det här alternativet är kostnadsfritt.

Så här importerar du geokoder för offlineberäkning:

Ange följande kommando med en blankstegsavgränsad lista över [ISO-3166 alpha2-landskoder](https://www.geonames.org/countries/):

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

Exempel:

```bash
bin/magento inventory-geonames:import us ca gb de
```

Systemet hämtar och importerar geokodsdata till din databas och visar sedan meddelandet  `Importing <country code>: OK`.
