---
title: '[!UICONTROL Sales]-menyn'
description: Commerce Admin innehåller menyn [!UICONTROL Sales] som ger tillgång till verktyg för att arbeta med beställningar beroende på var de befinner sig i arbetsflödet.
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: 621b4729e23952ddd720b4dcc49b5341baae64cc
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 0%

---

# [!UICONTROL Sales]-menyn

På menyn Försäljning visas transaktioner efter var de finns i orderarbetsflödet. Du kanske ser vart och ett av alternativen som ett helt annat steg i orderns livstid.

>[!BEGINTABS]

>[!TAB Adobe Commerce]

[!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."}

![Försäljningsmenyn](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

>[!TAB Adobe Commerce as a Cloud Service]

[!BADGE Endast SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce as a Cloud Service- och Adobe Commerce Optimizer-projekt (SaaS-infrastruktur som hanteras av Adobe)."}

![Försäljningsmenyn](./assets/admin-menu-sales-accs.png){width="450" zoomable="yes"}

>[!ENDTABS]

## Visa menyn [!UICONTROL Sales]

Klicka på **[!UICONTROL Sales]** på sidofältet _Admin_.

## Menyalternativ

### [!UICONTROL Quotes]

![Adobe Commerce B2B](../assets/b2b.svg) (tillgänglig med Adobe Commerce B2B)

Auktoriserade köpare kan [förhandla om priset](../b2b/quotes.md) med säljaren genom att skicka en [förfrågan](../b2b/quote-request.md) från kundvagnen.

### [!UICONTROL Quote Templates]

![Adobe Commerce B2B](../assets/b2b.svg) (tillgänglig med Adobe Commerce B2B)

Gör att köpare och säljare kan effektivisera offertprocessen genom att skapa återanvändbara och anpassningsbara [offertmallar](../b2b/quote-templates-overview.md).

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

[!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."}

Ett [faktureringsavtal](paypal-billing-agreements.md) liknar en inköpsorder, förutom att det inte är begränsat till ett enstaka köp. Vid utcheckning väljer kunden Faktureringsavtal som betalningsmetod. Ett faktureringsavtal effektiviserar utcheckningsprocessen eftersom kunden inte behöver ange betalningsinformation för varje köp.

### [!UICONTROL Transactions]

På sidan [Transaktioner](transactions.md) visas alla betalningsaktiviteter som har utförts mellan din butik och alla betalningssystem, och du får tillgång till mer detaljerad information.

### [!UICONTROL Braintree Virtual Terminal]

[!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."}

På Braintree Virtual Terminal-sidan kan en Admin-användare acceptera betalningen för det valda beloppet. En handlare bör konfigurera grundläggande [Braintree-inställningar](braintree.md) för att göra terminalfunktionen tillgänglig. Braintree erbjuder en helt anpassningsbar utcheckningsupplevelse med bedrägeriidentifiering och PayPal-integrering.

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)

(Arkivalternativet måste vara aktiverat) [Arkiveringsorder](order-archive.md) och andra försäljningsdokument förbättrar prestanda regelbundet och håller arbetsytan fri från onödig information.
