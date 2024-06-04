---
title: '[!UICONTROL Sales] menu'
description: Commerce Admin innehåller [!UICONTROL Sales] -menyn, som ger tillgång till verktyg för att arbeta med beställningar beroende på var de finns i arbetsflödet.
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# [!UICONTROL Sales] meny

På menyn Försäljning visas transaktioner efter var de finns i orderarbetsflödet. Du kanske ser vart och ett av alternativen som ett helt annat steg i orderns livstid.

![Försäljningsmeny](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

## Visa [!UICONTROL Sales] meny

På _Administratör_ sidlist, klicka **[!UICONTROL Sales]**.

## Menyalternativ

### [!UICONTROL Quotes]

![Adobe Commerce B2B](../assets/b2b.svg) (Finns med Adobe Commerce B2B)

Auktoriserade köpare kan [förhandla om priset](../b2b/quotes.md) med säljaren genom att skicka en [förfrågan](../b2b/quote-request.md) från kundvagnen.

### [!UICONTROL Orders]

När en [beställa](orders.md) placeras, skapas en försäljningsorder som en tillfällig post för transaktionen. Betalningen har inte bearbetats och ordern kan fortfarande annulleras.

### [!UICONTROL Invoices]

An [faktura](invoices.md) är ett kvitto på mottagande av betalning för en order. Flera fakturor kan skapas för en enda order, var och en med så många eller några av de köpta produkter som du anger. Beroende på betalningsåtgärden kan betalningen hämtas automatiskt när fakturan skapas.

### [!UICONTROL Shipments]

A [försändelse](shipments.md) är ett register över produkterna i en beställning som har levererats. Precis som med fakturor kan flera leveranser associeras med en enda order tills alla produkter i ordern har levererats.

### [!UICONTROL Credit Memos]

A [kreditnota](credit-memos.md) är ett dokument som visar det belopp som ska betalas av kunden för en fullständig eller partiell återbetalning. Beloppet kan tillämpas på ett köp eller återbetalas till kunden.

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)

A [returnerad varuauktorisering](returns.md) (RMA) kan beviljas kunder som begär att få returnera en artikel för ersättning eller återbetalning. RMA-nummer kan utfärdas för produkttyperna Simple, Grouped, Configurable och Bundle. RMA-nummer är dock inte tillgängliga för virtuella och nedladdningsbara produkter eller presentkort.

### [!UICONTROL Billing Agreements]

A [faktureringsavtal](paypal-billing-agreements.md) liknar en inköpsorder, förutom att den inte är begränsad till ett enstaka köp. Vid utcheckning väljer kunden Faktureringsavtal som betalningsmetod. Ett faktureringsavtal effektiviserar utcheckningsprocessen eftersom kunden inte behöver ange betalningsinformation för varje köp.

### [!UICONTROL Transactions]

The [Transaktioner](transactions.md) På sidan visas alla betalningsaktiviteter som har utförts mellan din butik och alla betalningssystem. Där finns också mer detaljerad information.

### [!UICONTROL Braintree Virtual Terminal]

På sidan Virtuell terminal i Braintree kan en Admin-användare acceptera betalningen för det valda beloppet. För att terminalfunktionen ska vara tillgänglig bör en handlare konfigurera grundläggande [Inställningar för Braintree](braintree.md). Braintree erbjuder en helt anpassningsbar utcheckningsupplevelse med bedrägeriidentifiering och PayPal-integrering.

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)

(Alternativet Arkiv måste vara aktiverat) [Arkivera order](order-archive.md) och andra säljdokument förbättrar prestanda regelbundet och håller arbetsytan fri från onödig information.
