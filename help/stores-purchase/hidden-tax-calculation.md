---
title: Dold momsberäkning
description: Lär dig hur du konfigurerar en dold momsberäkning när det finns en rabatt som innehåller inbäddad skatt.
exl-id: be2000b1-09d7-4a28-814a-f5da7591e387
feature: Invoices, Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Dold momsberäkning

_Dold skatt_ är den moms som ett rabattbelopp har. Det är inte noll när alla dessa villkor är uppfyllda:

- Katalogpriser inkluderar moms
- Momsen är inte noll
- Det finns en rabatt

När det finns en rabatt med inbäddad moms beräknar Commerce en _dold skatt_ som läggs till för att beräkna det rabatterade priset.

`discountedItemPrice = fullPriceWithoutTax - discountAmountOnFullPriceWithoutTax + vatAmountOnDiscountedPrice + hiddenTax`

## Exempel

1. Fullpris för artikeln, inklusive moms: $100
1. moms: 20 %
1. Rabatt på 10 % tillämpas på artikelpris exklusive moms:

### Ogiltigt förväntat resultat

- Artikelpris efter skatt utan rabatt=100 USD
- Artikelpris före skatt utan rabatt=100/1.2=83.33 USD
- Rabatt=83.33 \ *0.1=8.33 USD
- Tax=(83.33-8.33) \ *0.2=**15 USD (ogiltigt)**
- Summa exkl. moms=83.33-8.33=**75 USD (ogiltigt)**
- Ordersumma inklusive skatt=75+15=**90 USD (ogiltig)**

### Giltigt faktiskt resultat i kundvagn

![Dold momsberäkning i kundvagn](./assets/hidden-tax.png){width="700" zoomable="yes"}

### Giltiga beräkningar

1. Objektets fullpris utan moms är: $100 / 1.2 = **$83.33**

1. Momsbeloppet för hela artikelpriset är: $100 - $83.33 = $16.67

   _Kan även beräknas som: $100 \ * (1 - 1/1.2)._

1. Rabatten på 10 % på 83,33 USD är: **$8,33** (när du inte har någon rabatt)

1. Rabatterat pris för artikel med moms är: $100 - $8,33 = $91.67

   >[!NOTE]
   >
   >Den här ekvationen illustrerar kundens uppfattning om hur rabatterna tillämpas.

1. Rabatterat pris på artikeln utan moms är: $91.67 / 1.2 = $76.39

1. Momsbeloppet för det rabatterade priset är: $91.67 - $76.39 = **$15.28 (giltigt)**

   _Kan även beräknas som: $91.67 \ * (1 - 1/1.2)._

1. Dold skatt eller _Rabattskattekompensation_ är skillnaden mellan momsbeloppet för fullpriset och det rabatterade priset: 16,67 - 15,28 USD = **$1,39**

   _Ett annat sätt att se på det: dold skatt är momsbeloppet som ingår i rabatten $8,33: $8,33 \* (1 - 1/1.2)._

1. Hur kunden vanligtvis förstår det rabatterade priset (ordersumma):

   _Fullt pris på artikeln inklusive moms **minus**rabattbeloppet: $100 - $8,33 = $91.67_

1. **Hur Commerce beräknar det rabatterade priset** (se tidigare för en formel):

   _$83.33 - $8.33 + 15.28 + 1.39 =**$91.67***_
