---
title: CSV-datafiler
description: Lär dig mer om strukturen som används i CSV-filen för att stödja import och export av data.
exl-id: 86e362af-2af7-4557-ac49-1efad2f0e976
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# CSV-datafiler

CSV-filformatet (kommaavgränsat värde) används som bas för dataöverföringsåtgärder och stöds av alla kalkylarks- och databasprogram. Följande filtyper stöds för import och export:

- Importera: `CSV` och `ZIP` (en komprimerad CSV-fil)
- Exportera: `CSV`

>[!IMPORTANT]
>
>Vi rekommenderar att du använder ett program som har stöd för UTF-8-kodning, till exempel Anteckningar++, för att redigera CSV-filer. Microsoft® Excel infogar ytterligare tecken i kolumnrubriken i CSV-filen, vilket kan förhindra att data importeras tillbaka till Commerce. Om du arbetar i Mac kan du spara data i CSV-format (Windows).

CSV-filer har en specifik struktur som måste matcha databasen. Varje kolumnrubrik motsvarar attributkoden för fältet som representeras av kolumnen. För att kolumnrubrikerna ska kunna läsas av Commerce måste du först exportera data från din butik som en CSV-fil. Du kan sedan redigera data och importera dem på nytt till Commerce.

Om du öppnar en exporterad CSV-fil i ett textredigeringsprogram ser du att värden avgränsas med kommatecken och att flera värden omges med dubbla citattecken. Under importen kan du ange ett eget avgränsningstecken, men som standard används ett komma.

## Struktur för produkt-CSV

En fullständig export av produktdatabasen innehåller information om varje produkt i katalogen och relationerna mellan dem. Varje post har ett fast urval kolumner som motsvarar attributen i katalogen, även om attributens ordning ignoreras under importprocessen.

Den första raden i tabellen innehåller namnen på attributen, som används som kolumnrubriker. De återstående raderna beskriver de enskilda produktposterna. Alla rader som börjar med ett värde i SKU-kolumnen är början av en ny produktpost. En enstaka produkt kan innehålla flera rader som innehåller information om flera bilder eller produktalternativ. Nästa rad som har ett värde i SKU-kolumnen börjar med en ny produkt.

Kategorikolumnen innehåller en sökväg för varje kategori som produkten är tilldelad till. Sökvägen innehåller rotkategorin, följt av ett snedstreck (`/`) mellan varje nivå. Som standard används kommatecknet `,` för att skilja olika kategorisökvägar åt. (Du kan ange ett annat avgränsningstecken med alternativet _[!UICONTROL Multiple value separator]_.) Exempel:

`Default Category/Gear,Default Category/Gear/Bags`

Om du vill importera data behöver du bara inkludera SKU:n och eventuella kolumner med ändringar. Alla tomma kolumner ignoreras under importprocessen. Det går inte att lägga till attribut under importprocessen. Du kan bara inkludera befintliga attribut.

En detaljerad beskrivning av varje produktattribut finns i [Product CSV File Structure](data-attributes-product.md).

| Kolumnnamn | Beskrivning |
| ----------- | ----------- |
| `_<name>` | Kolumnrubriker som börjar med ett understreck innehåller egenskaper för tjänstentitet eller komplexa data. Tjänstkolumner är inte produktattribut. |
| `<attribute_name>` | Kolumnrubriker med en attributkod eller ett fältnamn identifierar datakolumnen. En kolumn kan representera ett systemattribut, eller ett som har skapats av butiksadministratören. |

{style="table-layout:auto"}

## Kundens CSV-struktur

Kundernas CSV-fil innehåller kundinformation från databasen och har följande struktur:

Den första raden i tabellen innehåller namnen på attributkolumnerna (som är desamma som attributkoder). Det finns två typer av kolumnnamn, vilket visas i följande tabell. Andra rader innehåller attributvärden, tjänstdata och komplexa data. Varje rad med värden som inte är tomma i kolumnerna `email` och `_website` startar beskrivningen av efterföljande kund. Varje rad kan representera kunddata med eller utan adressdata, eller enbart adressdata. Om en rad bara innehåller adressdata ignoreras värdena i kolumnerna, som är relaterade till kundprofilen, och kan vara tomma.

Om du vill lägga till eller ersätta mer än en adress för en kund lägger du till en rad för varje ny adress med tomma kunddata och nya eller uppdaterade adressdata nedanför kunddataraden.

En detaljerad beskrivning av varje kundattribut finns i [Kundens CSV-filstruktur](data-attributes-customer.md).

| Kolumnnamn | Beskrivning |
| ----------- | ----------- |
| `_<name>` | Kolumnrubriker som börjar med ett understreck innehåller egenskaper för tjänstentitet eller komplexa data. Tjänstkolumner är inte kundattribut. |
| `<attribute name>` | Namnen på kolumnerna med värden för både systemskapade attribut och attribut som skapas av lagringsadministratören. |

{style="table-layout:auto"}
