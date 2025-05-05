---
title: Importera och exportera lager
description: Använd de inbyggda import- och exportfunktionerna med de utökade  [!DNL Inventory Management] alternativen för att uppdatera källor och kvantiteter efter SKU.
exl-id: cb2d2e0d-aef8-4b18-b013-9a7b0ab448bd
feature: Inventory, Data Import/Export
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# Importera och exportera lager

För kataloger med många produkter använder du de inbyggda import- och exportfunktionerna med de utökade [!DNL Inventory Management] alternativen för att uppdatera källor och kvantiteter efter SKU. Med dessa alternativ kan du lägga till nya källor och uppdatera lagerkvantiteter för alla eller en viss källa. Du kan till exempel exportera produkter för en källa i Tyskland utan att påverka produktinformation för källor i Frankrike, England eller USA.

- [!DNL Commerce] tilldelar automatiskt standardversionen av Source till dina produkter när du uppgraderar [!DNL Commerce] eller importerar nya produkter. Om du importerar produkter med en anpassad källa tilldelad, läggs standardvärdet för Source fortfarande till med kvantiteten 0. Använd de här importinstruktionerna om du vill uppdatera källor och kvantiteter.

- Försäljare med en enda källa använder import för att endast uppdatera produktkvantiteter. Alla befintliga och tillagda produkter tilldelas standardprodukten för Source.

- Flera källhandlare använder import för att lägga till flera källor och kvantiteter per rad och SKU.

Om du vill importera uppdateringar måste du först exportera en CSV-fil för en viss eller alla källor. Redigera CSV-filen och lägg till en rad per SKU för varje källa och kvantitet. Du behöver källkoden när du lägger till en källa och lägger till lagerkvantiteter. Du kan inte lägga till eller uppdatera lager med funktioner för import/export.

## CSV-filinnehåll

Exportimportfilen innehåller följande information beroende på källa:

- `source_code` - Koden för källor i [!DNL Commerce]. Det finns en rad för varje källa och SKU.
- `sku` - SKU för produkten i [!DNL Commerce]. SKU:n måste matcha en produkt i din butik för att [!DNL Inventory Management]-data ska kunna uppdateras korrekt.
- `status` - 0 för Out of Stock. 1 i lager. Värdet måste vara 1 för att kunna köpa lager från den här källan.
- `quantity` - Den totala lagermängden som är tillgänglig för denna SKU och källa.

Använd en CSV-fil för att snabbt uppdatera flera produkter och tilldelade källor för att uppdatera och korrigera eventuella fel i lagerposterna i stället för en i taget via programgränssnittet. För en basfil exporterar du först och uppdaterar efter behov.

![Exempel på CSV-fil för import - exportera lagerdata](assets/inventory-import-export-data.png){width="600" zoomable="yes"}

## Exportera produktdata för alla källor

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**&#x200B;på sidofältet_ Admin _.

1. Välj `Stock Sources` för **[!UICONTROL Entity Type]**.

   Exporten extraherar endast data för produkter med en SKU.

1. Klicka på **[!UICONTROL Continue]**.

   Filen genereras och hämtas för att öppnas och redigeras.

Importera filen tillbaka till [!DNL Commerce] när du har uppdaterat lagerbelopp och produktdata.

![Exportera Stock-källor för produktdata och källor](assets/inventory-export-stock-sources.png){width="350" zoomable="yes"}

## Exportera produktdata för en viss källa

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**&#x200B;på sidofältet_ Admin _.

1. Välj `Stock Sources` för **[!UICONTROL Entity Type]**.

   Exporten extraherar endast data för produkter med en SKU.

1. Använd **[!UICONTROL Entity Attributes]** för att filtrera de exporterade produkterna efter en viss källa.

   För `source_code` anger du källkoden i filterfältet.

1. Klicka på **[!UICONTROL Continue]**.

   Filen genereras och hämtas för att öppnas och redigeras.

Importera filen tillbaka till [!DNL Commerce] när du har uppdaterat lagerbelopp och produktdata.

## Importera produktdata

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**&#x200B;på sidofältet_ Admin _.

1. Välj `Stock Sources` för **[!UICONTROL Entity Type]**.

   Exporten extraherar endast data för produkter med en SKU.

1. Välj konfigurationer för **[!UICONTROL Import Behavior]**.

1. Markera CSV-filen som ska importeras.

1. Klicka på **[!UICONTROL Check Data]** och slutför importen.

![Importera produktdata och källor](assets/inventory-import-sources.png){width="600" zoomable="yes"}
