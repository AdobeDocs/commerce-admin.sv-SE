---
title: Scenarier för Stock-meddelanden
description: Lär dig mer om kombinationen av konfigurationsinställningar som styr meddelanden om tillgänglighet för lager på produktsidor och i produktlistor på katalogsidor.
exl-id: 63114305-e695-445b-91cd-9e0fb2729ec4
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Scenarier för Stock-meddelanden

Du kan använda en kombination av konfigurationsinställningar för att kontrollera tillgänglighetsmeddelanden för lager på produktsidor och i produktlistor på katalogsidor.

![Grupperad produkt med meddelandet &quot;Out of Stock&quot;](assets/storefront-out-of-stock-message.png){width="600" zoomable="yes"}

## Stock-meddelanden på produktsidan

Det finns flera olika varianter av meddelanden tillgängliga för produktsidan, beroende på vilken kombination av inställningarna för Hantera Stock- och Stock-tillgänglighet som finns.

### Exempel 1: Visa tillgänglighetsmeddelande

#### Scenario 1

Den här kombinationen av inställningar gör att det visas ett tillgänglighetsmeddelande på produktsidan, baserat på respektive produkts lagertillgänglighet.

| Alternativ för Stock | Inställning | Meddelande |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | |
| [!UICONTROL Manage Stock] | `Yes` | |
| [!UICONTROL Stock Availability] | `In Stock` | _[!UICONTROL Availability: In Stock]_ |
| | `Out of Stock` | _[!UICONTROL Availability: Out of Stock]_ |

#### Scenario 2

När Stock inte hanteras för en produkt kan den här kombinationen av inställningar användas för att visa tillgänglighetsmeddelandet på produktsidan.

| Alternativ för Stock | Inställning | Meddelande |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` |  |
| [!UICONTROL Manage Stock] | `No` | _[!UICONTROL Availability: In Stock]_ |

### Exempel 2: Dölj tillgänglighetsmeddelande

#### Scenario 1

Den här kombinationen av konfigurations- och produktinställningar förhindrar att tillgänglighetsmeddelandet visas på produktsidan.

| Alternativ för Stock | Inställning | Meddelande |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `Yes` |  |
| [!UICONTROL Stock Availability] | `In Stock` | Ingen |
|  | `Out of Stock` | Ingen |

#### Scenario 2

När Stock inte hanteras för en produkt förhindrar den här kombinationen av konfigurations- och produktinställningar att tillgänglighetsmeddelandet visas på produktsidan.

| Alternativ för Stock | Inställning | Meddelande |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `No` | Ingen |

## Stock-meddelanden för katalogsidor

Följande visningsalternativ är möjliga för kategorierna och sökresultatlistorna, beroende på produkttillgänglighet och konfigurationsinställningar.

![Utlagrade meddelanden på kategorisidan](assets/storefront-out-of-stock-catalog-page.png){width="600" zoomable="yes"}

### Exempel 1: Visa produkten med meddelandet &quot;Out of stock&quot;

Den här kombinationen av konfigurationsinställningar innehåller färdiga produkter i kategorierna och sökresultatlistorna och visar ett meddelande om att det inte finns något lager.

| Alternativ för Stock | Inställning | Meddelande |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | _[!UICONTROL Out of stock]_ |
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `No` | Ingen |

### Exempel 2: Visa produkten utan&quot;Utanför lager&quot;-meddelande

Den här kombinationen av konfigurationsinställningar innehåller färdiga produkter i kategorierna och sökresultatlistorna, men visar inget meddelande.

| Alternativ för Stock | Inställning | Meddelande |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` | Ingen |
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |

### Exempel 3: Dölj produkten tills den är i lager igen

Den här konfigurationsinställningen utelämnar helt från Stock-produkter från kategorierna och sökresultatlistorna tills de är tillbaka i lager.

| Alternativ för Stock | Inställning | Meddelande |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `No` | Ingen |
