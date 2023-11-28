---
title: Importera och exportera lager
description: Använd den inbyggda import- och exportfunktionen med utökade [!DNL Inventory Management] alternativ för att uppdatera källor och kvantiteter per SKU.
exl-id: cb2d2e0d-aef8-4b18-b013-9a7b0ab448bd
feature: Inventory, Data Import/Export
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Importera och exportera lager

För kataloger med många produkter använder du de inbyggda import- och exportfunktionerna med utökade [!DNL Inventory Management] alternativ för att uppdatera källor och kvantiteter per SKU. Med dessa alternativ kan du lägga till nya källor och uppdatera lagerkvantiteter för alla eller en viss källa. Du kan till exempel exportera produkter för en källa i Tyskland utan att påverka produktinformation för källor i Frankrike, England eller USA.

- [!DNL Commerce] tilldelar automatiskt standardkällan till dina produkter när du uppgraderar [!DNL Commerce] eller importera nya produkter. Om du importerar produkter med en anpassad källa tilldelad, läggs standardkällan fortfarande till med kvantiteten 0. Använd de här importinstruktionerna om du vill uppdatera källor och kvantiteter.

- Försäljare med en enda källa använder import för att endast uppdatera produktkvantiteter. Alla befintliga och tillagda produkter tilldelas standardkällan.

- Flera källhandlare använder import för att lägga till flera källor och kvantiteter per rad och SKU.

Om du vill importera uppdateringar måste du först exportera en CSV-fil för en viss eller alla källor. Redigera CSV-filen och lägg till en rad per SKU för varje källa och kvantitet. Du behöver källkoden när du lägger till en källa och lägger till lagerkvantiteter. Du kan inte lägga till eller uppdatera lager med funktioner för import/export.

## CSV-filinnehåll

Exportimportfilen innehåller följande information beroende på källa:

- `source_code` - Koden för källor i [!DNL Commerce]. Det finns en rad för varje källa och SKU.
- `sku` - SKU:n för produkten i [!DNL Commerce]. SKU:n måste matcha en produkt i din butik för att kunna uppdateras korrekt [!DNL Inventory Management] data.
- `status` - 0 för Out of Stock. 1 i lager. Värdet måste vara 1 för att kunna köpa lager från den här källan.
- `quantity` - Den totala lagermängden som är tillgänglig för denna SKU och denna källa.

Använd en CSV-fil för att snabbt uppdatera flera produkter och tilldelade källor för att uppdatera och korrigera eventuella fel i lagerposterna i stället för en i taget via programgränssnittet. För en basfil exporterar du först och uppdaterar efter behov.

![Exempel på CSV-fil för import - exportera lagerdata](assets/inventory-import-export-data.png){width="600" zoomable="yes"}

## Exportera produktdata för alla källor

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. För **[!UICONTROL Entity Type]**, välja `Stock Sources`.

   Exporten extraherar endast data för produkter med en SKU.

1. Klicka på **[!UICONTROL Continue]**.

   Filen genereras och hämtas för att öppnas och redigeras.

När du har uppdaterat lagerbelopp och produktdata importerar du filen tillbaka till [!DNL Commerce].

![Exportera lagerkällor för produktdata och källor](assets/inventory-export-stock-sources.png){width="350" zoomable="yes"}

## Exportera produktdata för en viss källa

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. För **[!UICONTROL Entity Type]**, välja `Stock Sources`.

   Exporten extraherar endast data för produkter med en SKU.

1. Använd **[!UICONTROL Entity Attributes]** om du vill filtrera de exporterade produkterna efter en viss källa.

   För `source_code`anger du källkoden i filterfältet.

1. Klicka på **[!UICONTROL Continue]**.

   Filen genereras och hämtas för att öppnas och redigeras.

När du har uppdaterat lagerbelopp och produktdata importerar du filen tillbaka till [!DNL Commerce].

## Importera produktdata

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. För **[!UICONTROL Entity Type]**, välja `Stock Sources`.

   Exporten extraherar endast data för produkter med en SKU.

1. Välj konfigurationer för **[!UICONTROL Import Behavior]**.

1. Markera CSV-filen som ska importeras.

1. Klicka **[!UICONTROL Check Data]** och slutför importen.

![Importera produktdata och källor](assets/inventory-import-sources.png){width="600" zoomable="yes"}
