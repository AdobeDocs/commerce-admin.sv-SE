---
title: Hantera order och leveranser från lager
description: Läs mer om de andra [!DNL Inventory Management] funktioner och alternativ för att hantera lagerkvantiteter genom leveransprocessen.
exl-id: cc4ca518-d98c-48f3-9051-6fb3c6fae9fe
feature: Inventory, Shipping/Delivery
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 0%

---

# Hantera beställningar och leveranser

[!DNL Inventory Management] innehåller ytterligare funktioner och alternativ för hantering av lagerkvantiteter genom leveransprocessen. När du granskar och levererar leveranser, annullerar beställningar och utfärdar kreditnotor uppdateras automatiskt produktförsäljnings- och lagerbehållningskvantiteter.

Denna information innehåller information om [!DNL Inventory Management]. Mer information finns i [Beställningar](../stores-purchase/orders.md){target="_blank"} ämne i _Experience Guide för försäljning och inköp_.

## Beställningar

[!DNL Commerce] har stöd för enstaka beställningar och beställningar med flera adresser som är färdiga utan ytterligare konfigurationer. När kunder eller personal lägger order [!DNL Inventory Management] spårar lager med reservationer mot den försäljningsbara kvantiteten, med avdrag för lagerkvantitet för fakturerade och levererade produkter.

### Fleradressorder

För order med flera adresser genereras en serie enstaka order - en för varje angiven måladress. Vid utcheckning genereras de produkter som är kopplade till varje adress som är kopplad till utcheckningen som enstaka order enligt måladressen. Varje beställning innehåller produkter som är kopplade per adress.

[!DNL Commerce] hanterar lager för dessa fleradressorder exakt som enstaka order. Det möjliggör rekommendationer eller åsidosättningar av algoritmen för källval under leverans, partiella leveranser, annulleringsorder och återfinansiering med lageruppdateringar.

![Flera adresser vid utcheckning](assets/inventory-multi-ship.png){width="350" zoomable="yes"}

### Återbetalningar

När en [kreditnota](../stores-purchase/credit-memo-create.md){target="_blank"} om du vill få tillbaka pengarna kan du returnera produktkvantiteten till den avdragna källan. Orderinformationen innehåller den lagerkälla som levererade produkten. Vi rekommenderar att du tilldelar den returnerade produktkvantiteten via en kreditnota när du tar emot den returnerade produkten.

![Objekt som ska återbetalas med Återgå till Stock markerat](assets/credit-memo-items-to-refund.png)
{width="350" zoomable="yes"}

### Avbryt ej levererade order

Om en order inte har levererats och annullerats (helt eller delvis), [!DNL Inventory Management] returnerar automatiskt produktlagret till den försäljningsbara kvantiteten. Till dess att faktura och frakt har levererats, reserveras inköpta produkter mot den säljbara kvantiteten, som inte har dragits av från den faktiska kvantiteten. Vid fakturering och leverans av ordern konverteras reservationen till ett lageravdrag.

Bakom kulisserna [!DNL Inventory Management] anger automatiskt en kompensationsreservation som tar bort spärren för produktkvantiteten. Kvantiteten returnerar till den aggregerade virtuella försäljningsbara kvantiteten.

## Leveranser

Med [!DNL Inventory Management] aktiverat kan du skicka partiella eller fullständiga leveranser från en eller flera källor för att slutföra beställningar. Du kontrollerar ditt utgående lager för varje order och anger vilka belopp som ska dras av, skickar en eller flera leveranser och levererar i lager och restorder när lagret är tillgängligt. Ange ett belopp som ska dras av från källkvantiteten för varje radartikel i ordern. Generera en försändelse per källa när du har ett lagerlager, tills hela ordern är slutförd.

### Partiella leveranser

För handlare med flera källor: [!DNL Commerce] genererar en leverans för varje källa som du väljer. I det allmänna arbetsflödet kan du välja en källa, ange produktkvantiteten att dra av för att slutföra ordern och fortsätta till leveransen. När det är klart skapar du ytterligare leveranser för varje källa tills du har slutfört ordern.

Handlare med en enda källa kan också skicka partiella leveranser för att stödja restorder eller saldolager när order kommer in för populära artiklar.

### Algoritm för Recommendations- och källval

The [Algoritm för källval](selection-reservations.md) (SSA) ger rekommendationer för partiella och fullständiga leveranser. Du kan komma åt algoritmer för källval när du skapar utleveransfakturor för en order. På sidan Leverans kör du algoritmen Källprioritet eller Avståndsprioritet när som helst för att hitta de bästa alternativen för att matcha beställda kvantiteter och tillgängliga källor. Systemet har stöd för att skicka en fullständig order från en källa och dela upp ordern i flera delleveranser över flera källor. Du har tillgång till dessa alternativ för omedelbar leverans och mellanliggande leveranser för att skicka mindre mängder över tiden.

För att slutföra och skicka en beställning måste den ha slutfört betalningen och fakturerats. För närvarande kan du köra SSA igen för rekommendationer och leveranser från en eller flera källor, eller åsidosätta SSA-rekommendationerna med manuellt angivna källor och kvantiteter för att slutföra leveransen.

- Vi rekommenderar att du kör SSA igen för att se rekommendationer för varje leverans.

- Om du vill ändra markeringarna kan du åsidosätta med manuella källavdrag.

### Leveranser och reservationer

När försändelser genererar, bokningar för produkter klaras och produktkvantitet dras av. Lagerbehållningskvantiteten per lageruppdatering baserad på leveransinformationen. Om du till exempel skickar leveranser för tio produkter från två källor dras 10 av kvantiteterna för dessa källor. Försäljningsmängden uppdateras automatiskt för tillhörande lager, vilket ger kunder och personal de senaste produktmängderna. Reservationerna är helt rensade och räknas inte längre mot den säljbara kvantiteten.
