---
title: '[!UICONTROL Sales]-menyn'
description: Commerce Admin innehåller menyn [!UICONTROL Sales] som ger tillgång till verktyg för att arbeta med beställningar beroende på var de befinner sig i arbetsflödet.
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# [!UICONTROL Sales]-menyn

På menyn Försäljning visas transaktioner efter var de finns i orderarbetsflödet. Du kanske ser vart och ett av alternativen som ett helt annat steg i orderns livstid.

![Försäljningsmenyn](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

## Visa menyn [!UICONTROL Sales]

Klicka på **[!UICONTROL Sales]** på sidofältet _Admin_.

## Menyalternativ

### [!UICONTROL Quotes]

![Adobe Commerce B2B](../assets/b2b.svg) (tillgänglig med Adobe Commerce B2B)

Auktoriserade köpare kan [förhandla om priset](../b2b/quotes.md) med säljaren genom att skicka en [förfrågan](../b2b/quote-request.md) från kundvagnen.

### [!UICONTROL Orders]

När en [order](orders.md) placeras skapas en försäljningsorder som en tillfällig post för transaktionen. Betalningen har inte bearbetats och ordern kan fortfarande annulleras.

### [!UICONTROL Invoices]

En [faktura](invoices.md) är en post för mottagande av betalning för en order. Flera fakturor kan skapas för en enda order, var och en med så många eller några av de köpta produkter som du anger. Beroende på betalningsåtgärden kan betalningen hämtas automatiskt när fakturan skapas.

### [!UICONTROL Shipments]

En [försändelse](shipments.md) är en post för produkterna i en beställning som har skickats. Precis som med fakturor kan flera leveranser associeras med en enda order tills alla produkter i ordern har levererats.

### [!UICONTROL Credit Memos]

En [kreditnota](credit-memos.md) är ett dokument som visar det belopp som ska betalas av kunden för en fullständig eller partiell återbetalning. Beloppet kan tillämpas på ett köp eller återbetalas till kunden.

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)

En [returnerad varuauktorisering](returns.md) (RMA) kan beviljas kunder som begär att returnera en artikel för ersättning eller återbetalning. RMA-nummer kan utfärdas för produkttyperna Simple, Grouped, Configurable och Bundle. RMA-nummer är dock inte tillgängliga för virtuella och nedladdningsbara produkter eller presentkort.

### [!UICONTROL Billing Agreements]

Ett [faktureringsavtal](paypal-billing-agreements.md) liknar en inköpsorder, förutom att det inte är begränsat till ett enstaka köp. Vid utcheckning väljer kunden Faktureringsavtal som betalningsmetod. Ett faktureringsavtal effektiviserar utcheckningsprocessen eftersom kunden inte behöver ange betalningsinformation för varje köp.

### [!UICONTROL Transactions]

På sidan [Transaktioner](transactions.md) visas alla betalningsaktiviteter som har utförts mellan din butik och alla betalningssystem, och du får tillgång till mer detaljerad information.

### [!UICONTROL Braintree Virtual Terminal]

På sidan Virtuell terminal i Braintree kan en Admin-användare acceptera betalningen för det valda beloppet. En handlare bör konfigurera grundläggande [Braintree-inställningar](braintree.md) för att göra terminalfunktionen tillgänglig. Braintree erbjuder en helt anpassningsbar utcheckningsupplevelse med bedrägeriidentifiering och PayPal-integrering.

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)

(Arkivalternativet måste vara aktiverat) [Arkiveringsorder](order-archive.md) och andra försäljningsdokument förbättrar prestanda regelbundet och håller arbetsytan fri från onödig information.
