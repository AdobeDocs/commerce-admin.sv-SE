---
title: Leveransetiketter
description: Lär dig mer om leveransetikettarbetsflöde för vanliga leveranser och produkter med returvaruauktorisering.
exl-id: 5da03cf9-5e92-4bb8-ba53-67c6469665ed
feature: Shipping/Delivery, Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Leveransetiketter

Handeln omfattar en hög nivå av integration med större fraktfirmor, vilket ger er tillgång till fraktfirmor för att spåra beställningar, skapa etiketter för frakt med mera. Leveransetiketter kan skapas för vanliga leveranser och produkter med returtillstånd. Förutom de uppgifter som fraktföretaget lämnat innehåller etiketten även handelsordernummer, paketnummer och totalt antal paket för leveransen.

![Leveransetikett för prioritetsordning för USPS](./assets/shipping-usps-priority-label.png){width="300"}

- [Konfigurera etiketter för leverans](shipping-label-configure.md)
- [Skapa etiketter och paket](shipping-label-create.md)

## Arbetsflöde för leveransetikett

Leveransetiketter kan skapas när en leverans skapas eller senare. Leveransetiketter sparas i PDF-format och hämtas till din dator.

### Steg 1: Merchant skickar begäran om frakt-etikett

Handläggaren fyller i den information som krävs för att generera etiketter och skickar in begäran.

### Steg 2: Begäran har skickats till transportföretaget

Commerce kontaktar transportföretaget och skapar en order i transportföretagets system. En separat order skapas för varje paket som skickas.

### Steg 3: Transportföretaget skickar etikett- och spårningsnummer

Transportföretaget skickar leveransetiketten och spårningsnumret för leveransen.

- En enstaka leverans med flera paket får flera fraktsedlar.

- Om du genererar samma etiketter flera gånger bevaras de ursprungliga spårningsnumren.

- För returnerade produkter med RMA-nummer ersätts de gamla spårningsnumren med nya.

### Steg 4: Merchant hämtar och skriver ut etiketten

När leveransetiketten har skapats sparas den nya leveransen och etiketten kan skrivas ut. Om leveransetiketten inte kan skapas på grund av anslutningsproblem eller andra orsaker skapas inte leveransen. Beroende på inställningarna i webbläsaren kan PDF-filen öppnas och skrivas ut. Varje etikett visas på en separat sida i PDF.
