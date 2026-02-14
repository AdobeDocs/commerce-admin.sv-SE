---
title: Kundsegment
description: Med kundsegment kan ni dynamiskt visa innehåll och kampanjer för specifika kunder.
exl-id: b254a6ac-cb0b-46c1-9ef7-ffc97360a98e
source-git-commit: 0b9f394a792171e93ee72f3b4ebb904b96ea1051
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Kundsegment

Med kundsegment kan ni dynamiskt visa innehåll och kampanjer för specifika kunder utifrån olika egenskaper. Några exempel är kundadress, orderhistorik och kundvagnsinnehåll. Ni kan optimera marknadsföringssatsningar baserat på riktade segment med kundvagnsprisregler. Ni kan också generera rapporter och exportera listan över målkunder. Eftersom kundsegmentsinformationen uppdateras kontinuerligt kan kunderna associeras och kopplas bort från ett segment när de handlar i din butik.

För att bättre förstå skillnaden mellan [kundgrupper](../customers/customer-groups.md) och kundsegment bör du notera var de används:

|  | Kundsegment | Kundgrupp |
|--- |--- |--- |
| Katalogprisregel |  | ✔️ |
| Kundprisregel | ✔️ | ✔️ |
| Pris |  | ✔️ |
| Relaterad produktregel | ✔️ |  |
| Dynamiskt block | ✔️ |  |
| Belöningsbaserade växelkurser |  | ✔️ |
| Kategoribehörigheter |  | ✔️ |
| Inbjudningar |  | ✔️ |

{style="table-layout:auto"}

## Kundsegmentattribut

Kundsegmentens attribut definieras på ett sätt som liknar reglerna för kundvagn och katalogpris. För att ett attribut ska kunna användas i ett kundsegment måste _[!UICONTROL Use in Customer Segment]_[property](attribute-properties.md#) anges till `Yes`. Villkoren för kundsegment kan innehålla följande typer av attribut:

| Attribut | Beskrivning |
|---|---|
| `Customer Address Fields` | Du kan definiera alla adressfält, till exempel ort eller land. Alla adresser i en kunds adressbok kan matcha dessa villkor för att kunden ska matcha. Eller så kan du ange att bara standardadresserna för fakturering eller leverans kan användas för att matcha en kund. Kundadressattribut är bara tillgängliga för kunder som är inloggade på sina konton. |
| `Customer Information Fields` | Du kan definiera olika kundinformation, inklusive kundgrupp, namn, e-post, prenumerationsstatus för nyhetsbrev och Butikskreditsaldo. Kundinformation är bara tillgänglig för kunder som är inloggade på sina konton. |
| `Cart Fields` | Kundvagnegenskaper kan baseras antingen på kvantitet (radartiklar eller total kvantitet) eller värdet (till exempel totalsumma, moms och presentkort) för kundvagnens innehåll. |
| `Products` | Du kan referera till produkter som finns i kundvagnen eller önskelistan, eller som tidigare har visats eller beställts. Du kan också ange ett datumintervall där det inträffade. Produkterna definieras med hjälp av produktattribut. |
| `Order Fields` | Orderegenskaper för tidigare order kan definieras baserat på fakturerings-/leveransadressen i ordern, det totala (eller genomsnittliga) beloppet eller kvantiteten för ordern eller det totala antalet order. Du kan också ange ett datumintervall för när det inträffade och orderstatus för de order som matchar dessa villkor. Endast tillgängligt för kunder som är inloggade. Villkor som ställs in för kunder som inte är inloggade slutar att fungera när de loggar in. |

{style="table-layout:auto"}

Mer information om hur du definierar kundsegment finns i [Skapa och ta bort kundsegment](../customers/customer-segment-create.md).

## eBooks

- **Kundsegmentering** - Hämta [eBook](https://business.adobe.com/se/resources/identifying-your-most-profitable-customers-introduction-customer-segmentation.html) och lär dig hur du kan öka vinsten och få nöjda kunder.
- **Segmenteringsstrategi** - Hämta [eBook](https://business.adobe.com/se/resources/3-segmentation-tactics-ignite-conversion.html) för att förbättra målsättningen för dina meddelanden och kampanjer och skapa meningsfulla konversationer med dina kunder.
