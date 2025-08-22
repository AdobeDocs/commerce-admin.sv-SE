---
title: Kundrapporter
description: Kundrapporter som finns i Adobe Commerce och Magento Open Source ger insikt i kundaktiviteten under en viss tidsperiod eller ett visst datumintervall.
exl-id: 7bee414b-b605-4aed-9749-78bb8056a6a4
feature: Customers, Reporting
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: c406add80981387305755221f21624dad475e63f
workflow-type: tm+mt
source-wordcount: '893'
ht-degree: 0%

---

# Kundrapporter

Kundrapporter ger insikt i kundaktivitet under en viss tidsperiod eller ett visst datumintervall.

## [!UICONTROL Order Total Report]

[!UICONTROL Order Total Report] visar kundorder för ett angivet tidsintervall eller datumintervall. Rapporten innehåller antalet order per kund, genomsnittligt orderbelopp och totalt belopp.

Gå till _>_ > **[!UICONTROL Reports]** på sidofältet _[!UICONTROL Customers]_&#x200B;Admin **[!UICONTROL Order Total]**.

![Ordersummeringsrapport](./assets/customers-order-total.png){width="600"}

### Workspace

| Kontroll | Beskrivning |
|--- |--- |
| [!UICONTROL From / To] | Används för att definiera en sökning efter order baserat på start- och slutdatum. |
| [!UICONTROL Show By] | Definierar granulariteten för delningen av orderposten. Alternativ: `Month` / `Day` / `Year` |
| [!UICONTROL Refresh] | Uppdaterar rutnätet till de angivna filtren. |
| [!UICONTROL Export] | Exporterar de markerade posterna som en CSV- eller Excel XML-fil. |
| [!UICONTROL Scope] | Används för att ange platsen eller arkivet som rapporten genereras för. |

{style="table-layout:auto"}

### Kolumnbeskrivningar

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Interval] | Totalt orderintervall, av `Month` / `Day` / `Year`. |
| [!UICONTROL Customer] | Namnet på den kund som lade beställningarna. |
| [!UICONTROL Orders] | Antalet order för det angivna intervallet. |
| [!UICONTROL Average] | Genomsnittligt orderbelopp. Detta belopp beräknas alltid för produktpriser **exklusive moms**, även om katalogproduktpriser, orderdelsumma och ordersumma inkluderar moms. Det innebär att det belopp som visas i rapporten skiljer sig från det belopp som visas i orderinformationen om ordersummorna inkluderar moms. |
| [!UICONTROL Total] | Summan av alla order för perioden. Detta belopp beräknas alltid för produktpriser **exklusive moms**, även om katalogproduktpriser, orderdelsumma och ordersumma inkluderar moms. Resultatet blir att summan som visas i rapporten skiljer sig från det belopp som visas i orderdetaljerna om ordersummorna inkluderar moms. |

{style="table-layout:auto"}

## [!UICONTROL Order Count Report]

[!UICONTROL Order Count Report] visar antalet order per kund för ett angivet tidsintervall eller datumintervall. Rapporten innehåller antalet order per kund, genomsnittligt orderbelopp och totalt belopp.

Gå till _>_ > **[!UICONTROL Reports]** på sidofältet _[!UICONTROL Customers]_&#x200B;Admin **[!UICONTROL Order Count]**.

![Orderräkningsrapport](./assets/customer-order-count.png){width="600"}

### Workspace

| Kontroll | Beskrivning |
|--- |--- |
| [!UICONTROL From / To] | Används för att definiera en sökning efter order baserat på start- och slutdatum. |
| [!UICONTROL Show By] | Definierar granulariteten för delningen av orderposten. Alternativ: `Month` / `Day` / `Year` |
| [!UICONTROL Refresh] | Uppdaterar rutnätet till de angivna filtren. |
| [!UICONTROL Export] | Exporterar de markerade posterna som en CSV- eller Excel XML-fil. |
| [!UICONTROL Scope] | Används för att ange platsen eller arkivet som rapporten genereras för. |

{style="table-layout:auto"}

### Kolumnbeskrivningar

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Interval] | Intervall för orderantal, av `Month` / `Day` / `Year`. |
| [!UICONTROL Customer] | Kunden som gjorde beställningen. |
| [!UICONTROL Orders] | Antalet order för det angivna intervallet. |
| [!UICONTROL Average] | Genomsnittligt orderbelopp. Detta belopp beräknas alltid för produktpriser **exklusive moms**, även om katalogproduktpriser, orderdelsumma och ordersumma inkluderar moms. Det innebär att det belopp som visas i rapporten skiljer sig från det belopp som visas i orderinformationen om ordersummorna inkluderar moms. |
| [!UICONTROL Total] | Summan av alla order för perioden. Detta belopp beräknas alltid för produktpriser **exklusive moms**, även om katalogproduktpriser, orderdelsumma och ordersumma inkluderar moms. Resultatet blir att det belopp som visas i rapporten skiljer sig från det belopp som visas i orderdetaljerna om ordersummorna inkluderar uppgifter. |

{style="table-layout:auto"}

## [!UICONTROL New Accounts Report]

[!UICONTROL New Accounts Report] visar antalet nya kundkonton som öppnats under ett angivet tidsintervall eller datumintervall.

Gå till _>_ > **[!UICONTROL Reports]** på sidofältet _[!UICONTROL Customers]_&#x200B;Admin **[!UICONTROL New]**.

![Rapport om nya konton](./assets/customers-new-accounts.png){width="600"}

### Workspace

| Kontroll | Beskrivning |
|--- |--- |
| [!UICONTROL From / To] | Används för att definiera en sökning efter nya konton baserat på start- och slutdatum. |
| [!UICONTROL Show By] | Definierar granulariteten för delningen av orderposten. Alternativ: Månad / Dag / År |
| [!UICONTROL Refresh] | Uppdaterar rutnätet till de angivna filtren. |
| [!UICONTROL Export] | Exporterar de markerade posterna som en CSV- eller Excel XML-fil. |
| [!UICONTROL Scope] | Används för att ange platsen eller arkivet som rapporten genereras för. |

{style="table-layout:auto"}

### Kolumnbeskrivningar

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Interval] | Intervall för att skapa nya konton, per månad/dag/år. |
| [!UICONTROL New Accounts] | Antalet nya konton som skapats under ett visst intervall. |

{style="table-layout:auto"}

## [!UICONTROL Customer Wish List Report]

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)

[!UICONTROL Customer Wish List Report] innehåller information om kundernas önskelistor.

Gå till _>_ > **[!UICONTROL Reports]** på sidofältet _[!UICONTROL Customers]_&#x200B;Admin **[!UICONTROL Wish Lists]**.

![Önsklisterapport](./assets/customer-wish-list.png){width="600"}

### Workspace

| Kontroll | Beskrivning |
|--- |--- |
| [!UICONTROL Scope] | Används för att ange platsen eller arkivet som rapporten genereras för. |
| [!UICONTROL Search] | Startar en sökning med de angivna parametrarna. |
| [!UICONTROL Reset Filter] | Initierar en återställning av alla sökparametrar. |
| [!UICONTROL Per Page] | Anger hur många poster som ska visas på en sida. |
| [!UICONTROL Export] | Exporterar de markerade posterna som en CSV- eller Excel XML-fil. |
| [!UICONTROL From / To] | Används för att definiera en sökning efter önskelistor baserat på start- och slutdatum. |
| [!UICONTROL Wishlist] | Initierar en sökning efter önskelista efter namn. |
| [!UICONTROL Status] | Status för önskelistan. Alternativ: `Private` / `Public` |
| [!UICONTROL Comment] | Startar en sökning efter text i önskelistekommentarer. |

{style="table-layout:auto"}

### Kolumnbeskrivningar

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Added] | Datum när önskelistan skapades. |
| [!UICONTROL Customer] | Förnamn och efternamn för kunden som skapade önskelistan. |
| [!UICONTROL Wishlist] | Namn på önskelistan. |
| [!UICONTROL Status] | Status för önskelistan. Alternativ: `Private` / `Public` |
| [!UICONTROL Product] | Namnet på produkten som lagts till i önskelistan. |
| [!UICONTROL SKU] | SKU för produkten som lagts till i önskelistan. |
| [!UICONTROL Comment] | Kommentarstexten som angavs när önskelistan skapades. |

{style="table-layout:auto"}

## [!UICONTROL Customer Segment Report]

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)

[!UICONTROL Customer Segment Report] ger information om antalet kunder i varje segment.

Gå till _>_ > **[!UICONTROL Reports]** på sidofältet _[!UICONTROL Customers]_&#x200B;Admin **[!UICONTROL Segments]**.

![Segmentrapport](./assets/customers-segments.png){width="600"}

### Workspace

| Kontroll | Beskrivning |
|--- |--- |
| [!UICONTROL Search] | Startar en sökning med de angivna parametrarna. |
| [!UICONTROL Reset Filter] | Initierar en återställning av alla sökparametrar. |
| [!UICONTROL Action] | Initierar visningen av segment efter parametrar. Alternativ: `Action` / `View Combined Report` |
| [!UICONTROL Per Page] | Anger hur många poster som ska visas på en sida. |

{style="table-layout:auto"}

### Kolumnbeskrivningar

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL ID] | En unik numerisk identifierare som tilldelas varje segment. |
| [!UICONTROL Segment] | Segmentnamn. |
| [!UICONTROL Status] | Segmentstatus. Alternativ: `Active` / `Inactive` |
| [!UICONTROL Website] | Webbplats som segmentet är tilldelat till. |
| [!UICONTROL Customers] | Antal kunder som tilldelats segmentet. |

{style="table-layout:auto"}
