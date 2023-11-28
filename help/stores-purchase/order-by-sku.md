---
title: Beställa efter SKU
description: Lär dig hur du konfigurerar din butik så att den stöder beställning via SKU som en smidighet för dina kunder.
exl-id: cb39554f-ab76-46d5-8217-e43bc8f9f88d
feature: Orders, Storefront, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%

---

# Beställa efter SKU

{{ee-feature}}

En SKU är en Stock Keeping Unit. SKU:er hjälper i allmänhet onlineförsäljare att identifiera de viktigaste produktegenskaperna, till exempel storlek, färg, pris och material. Produkt-ID:n skiljer sig från SKU:er:

- The `Product ID` är en sekventiell serie med nummer som används internt för att identifiera produkter och som inte är tillgängliga för kunder.
- The `SKU` genereras av säljaren, vanligtvis baserat på produktnamn och attribut för marknadsföring eller intern spårning. Exempel: En blå, bomull T-shirt, storleksmedelstor: T-COT-MED-BL. SKU:n kan vid behov ändras av säljaren.

I vanliga fall innehåller en SKU en uppsättning förkortningar som anger produktens särskiljande egenskaper. Den maximala SKU-längden är 64 tecken. SKU:er är viktiga för att effektivt spåra och hantera lager, så att det är viktigt att konfigurera dem på rätt sätt för e-handel.

_Beställa efter SKU_ är en [widget](../content-design/widgets.md) som kan visas i butiken som en bekvämlighet för alla kunder, eller göras tillgängliga för endast kunder i specifika kundgrupper. Köpare kan antingen ange SKU- och kvantitetsinformation direkt i Order by SKU-blocket eller överföra en csv-fil från sitt kundkonto. Oberoende av konfiguration är beställning via SKU alltid tillgängligt för lagringsadministratörer.

![Beställ av SKU i butiken](./assets/storefront-order-by-sku.png){width="700" zoomable="yes"}

## Konfigurera order efter SKU

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Sales]** och välja **[!UICONTROL Sales]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Order by SKU Settings]** -avsnitt.

1. Ange **[!UICONTROL Enable Order by SKU on my Account in Storefront]** till något av följande:

   - `Yes, for Everyone` - Blocket Order by SKU är tillgängligt i butiken för alla kunder.
   - `Yes, for Specified Customer Groups` - Order by SKU är endast tillgängligt för medlemmar i en viss kundgrupp, som `Wholesale`.
   - `No` - Blocket Order by SKU visas inte i butiken och sidan Order by SKU är inte tillgänglig i kundkontot.

   ![Inställningar för beställning efter SKU](../configuration-reference/sales/assets/sales-order-by-sku-settings.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]**.

![B2B för Adobe Commerce](../assets/b2b.svg) (B2B endast för Adobe Commerce) _**Om du vill aktivera funktionen Ordna efter SKU inaktiverar du funktionen Snabbordning:**_

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I den vänstra panelen under _[!UICONTROL General]_, välja **[!UICONTROL B2B Features]**

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL B2B Features]** -avsnitt.

1. Ange **[!UICONTROL Enable Quick Order]** till `No`.

   The [Snabbbeställningsfunktion](../b2b/quick-order.md) gör det möjligt för kunder och gäster att snabbt göra beställningar baserat på SKU eller produktnamn.

## StoreFront

När funktionen är konfigurerad för butiken kan kunderna beställa på SKU från vilken sida som helst som innehåller _Beställa efter SKU_ widgeten eller från deras kontokontrollpanel.

### Sortera efter SKU från sidblocket

1. I _Beställa efter SKU_ -block, kunden anger **[!UICONTROL SKU]** och **[!UICONTROL Qty]** av artikeln som ska beställas.

1. Om du vill lägga till ett annat objekt klickar du **[!UICONTROL Add Row]** och upprepa processen.

1. Klickningar **[!UICONTROL Add to Cart]**.

### Beställ av SKU från ett kundkonto

1. Från butiken loggar kunden in på sitt konto.

1. I panelen till vänster väljer **[!UICONTROL Order by SKU]**.

1. Lägger till enskilda objekt efter inställning:

   _**Lägger till varje objekt efter SKU:**_

   - Anger **[!UICONTROL SKU]** och **[!UICONTROL Qty]** av artikeln som ska beställas.

   - Om du vill lägga till fler objekt efter behov klickar du _Lägg till rad_ ![Plusteckenknapp](../assets/button-add-item.png) och upprepas för så många objekt som behövs.

   - Klickningar **[!UICONTROL Add to Cart]**.

   _**Överför en CSV-fil med flera objekt:**_

   - Förbereder [importera data CSV](../systems/data-csv.md) (Kommaavgränsat värde) fil som innehåller kolumner för `SKU` och `Qty`.

   ![SKU:er att importera](./assets/account-dashboard-order-by-sku-import.png){width="500" zoomable="yes"}

   - Om du vill överföra CSV-filen klickar du på **[!UICONTROL Choose File]** och välj den fil som ska överföras.

   - Klickningar **[!UICONTROL Add to Cart]**.

   Om någon av produkterna har ytterligare alternativ får kunden ett meddelande i kundvagnen om att produkten behöver åtgärdas.

   ![Produkten måste åtgärdas](./assets/account-dashboard-order-by-sku-cart-product-requires-attention.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Om det finns dubbla SKU:er kombineras kvantiteterna till en radartikel i kundvagnen. Kunden kan ändra kvantiteten för valfri artikel och klicka på **[!UICONTROL Update Shopping Cart]** för att beräkna om summorna.

