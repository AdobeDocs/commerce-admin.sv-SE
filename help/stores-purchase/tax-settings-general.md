---
title: Inställningar för momskonfiguration
description: Lär dig hur du konfigurerar grundläggande skatteinställningar, inklusive momsklasser, beräkning och standardskattemål.
exl-id: e32747f9-20d0-4717-9cee-aa1bcffebb65
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 0%

---

# Inställningar för momskonfiguration

Följande instruktioner tar dig igenom den grundläggande skattekonfigurationen för din Commerce-instans. Innan du ställer in dina skatter måste du känna till dina skattekrav [locale](store-localize.md#step-3-change-the-locale-of-the-store-view). Slutför sedan skattekonfigurationen enligt dina krav.

Administratör [behörigheter](../systems/permissions.md) kan anges att begränsa [åtkomst](../systems/permissions-user-roles.md) till skattemedel, baserat på verksamheten _behöver veta_. Om du vill skapa en administratörsroll med tillgång till skatteinställningar väljer du både moms och system/skatt. Om du skapar en webbplats för en region som skiljer sig från din standardplats för leverans, måste du även tillåta åtkomst till system-/leveransresurserna för rollen. Leveransinställningarna bestämmer momssatsen som används för katalogpriser.

## Konfigurera allmänna skatteinställningar

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. För en konfiguration med flera platser anger du **[!UICONTROL Store View]** till den webbplats och butik som är målet för konfigurationen.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Tax]**.

1. Slutför följande konfigurationsinställningar.

   Rensa **[!UICONTROL Use system value]** kryssrutan för alla inställningar som är nedtonade.

### [!UICONTROL Tax Classes]

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Tax Classes]** -avsnitt.

   ![Skatteklasser](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

   - **Skatteklass för leverans** — Använd lämplig klass. Standardklasserna är: `None` och `Taxable Goods`
   - **Skatteklass för presentalternativ** — ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Ange lämplig klass. Standardklasserna är: `None` och `Taxable Goods`
   - **Standardskatteklass för produkt** — Använd lämplig klass. Standardklasserna är: `None` och `Taxable Goods`
   - **Standardskatteklass för kund** — Använd lämplig klass. Standardklassen är: `Retail Customer` och `Wholesale Customer`

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

### [!UICONTROL Calculation Settings]

1. Expandera avsnittet **[!UICONTROL Calculation Settings]**.

   ![Beräkningsinställningar](../configuration-reference/sales/assets/tax-calculation-settings.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Tax Calculation Method Based On]** till något av följande:

   - `Unit Price` - Priset för varje produkt
   - `Row Total` - Summan av radartikeln i ordern, minus rabatter
   - `Total` - Ordersumman

1. Ange **[!UICONTROL Tax Calculation Based On]** till något av följande:

   - `Shipping Address` - Den adress dit ordern ska skickas
   - `Billing Address` - Kundens eller företagets faktureringsadress
   - `Shipping Origin` - Den adress som anges som [ursprungspunkt](shipping-settings.md#point-of-origin) för din butik

1. Ange **[!UICONTROL Catalog Prices]** till `Excluding Tax` eller `Including Tax`.

1. Ange **[!UICONTROL Shipping Prices]** till `Excluding Tax` eller `Including Tax`.

1. Ange **[!UICONTROL Apply Customer Tax]** på något av följande för att fastställa om skatt tillämpas på det ursprungliga eller diskonterade priset: `After Discount` eller `Before Discount`

1. Ange **[!UICONTROL Apply Discount on Prices]** till något av följande för att avgöra om rabatterna inkluderar eller exkluderar moms: `Excluding Tax` eller `Including Tax`

1. Ange **[!UICONTROL Apply Tax On]** till `Custom price if available` eller `Original price only`.

1. Ange **[!UICONTROL Enable Cross-Border Trade]** till något av följande:

   - `Yes` - Använd enhetliga priser för olika skattesatser. Om katalogpriset innehåller moms väljer du den här inställningen för att justera priset oavsett kundens momssats.
   - `No` - Variera priset per skattesats.

   >[!IMPORTANT]
   >
   >If [gränsöverskridande handel](#cross-border-price-consistency) är aktiverat ändras vinstmarginalen per skattesats. Vinst bestäms av formeln (`Revenue - CustomerVAT - CostOfGoodsSold`). För att möjliggöra gränsöverskridande handel måste priserna anges till att omfatta skatt.

### [!UICONTROL Default Tax Destination Calculation]

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Default Tax Destination Calculation]** -avsnitt.

   ![Beräkning av standardskattedestination](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Default Country]** för skatteberäkningar.

1. Ange, om tillämpligt, **[!UICONTROL Default State]** för skatteberäkningar.

1. Ange, om tillämpligt, **[!UICONTROL Default Post Code]** för skatteberäkningar.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

### [!UICONTROL Price Display Settings]

>[!IMPORTANT]
>
>Vissa kombinationer av inställningar som är relaterade till en prisvisning som både inkluderar och exkluderar moms kan vara förvirrande för kunden. Information om hur du undviker att utlösa ett varningsmeddelande finns i [rekommenderade inställningar](taxes.md#warning-messages).

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Price Display Settings]** -avsnitt.

   ![Prisvisningsinställningar](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Display Product Prices in Catalog]** till något av följande:

   - `Excluding Tax` - Katalogpriser som visas i butiken inkluderar inte moms.
   - `Including Tax` - Katalogpriserna i butiken inkluderar endast moms om en momsregel matchar skatteursprunget eller om kundens adress matchar momsregeln. Detta kan inträffa efter att en kund har skapat ett konto, loggat in eller använder verktyget för beräkning av skatt och leverans i kundvagnen.
   - `Including and Excluding Tax` - Katalogpriser som visas i butiken visas både med och utan moms.

1. Ange **[!UICONTROL Display Shipping Prices]** till `Excluding Tax`, `Including Tax`, eller `Including and Excluding Tax`.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

### [!UICONTROL Shopping Cart Display Settings]

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Shopping Cart Display Settings]** -avsnitt.

   ![Inställningar för kundvagnsvisning](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. För följande inställningar väljer du hur du vill att skatter och priser ska visas i kundvagnen, enligt kraven för butik och språkområde:

   - Ange **[!UICONTROL Display Prices]** till `Excluding Tax`, `Including Tax`, eller `Including and Excluding Tax`.

   - Ange **[!UICONTROL Display Subtotal]** till `Excluding Tax`, `Including Tax`, eller `Including and Excluding Tax`.

   - Ange **[!UICONTROL Display Shipping Amount]** till `Excluding Tax`, `Including Tax`, eller `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Ange **[!UICONTROL Display Gift Wrapping Prices]** till `Excluding Tax`, `Including Tax`, eller `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Ange **[!UICONTROL Display Printed Card Prices]** till `Excluding Tax`, `Including Tax`, eller `Including and Excluding Tax`.

1. Ange följande visningsalternativ till antingen `Yes` eller `No`, efter dina behov:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

### [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

1. Expandera ![Utbyggnad](../assets/icon-display-expand.png) den **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** -avsnitt.

   ![Visningsinställningar för order, fakturor, kreditnotor](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Ange hur priser och skatter ska visas i order, fakturor och kreditnotor:

   - Ange **[!UICONTROL Display Prices]** till `Excluding Tax`, `Including Tax`, eller `Including and Excluding Tax`.

   - Ange **[!UICONTROL Display Subtotal]** till `Excluding Tax`, `Including Tax`, eller `Including and Excluding Tax`.

   - Ange **[!UICONTROL Display Shipping Amount]** till `Excluding Tax`, `Including Tax`, eller `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Ange **[!UICONTROL Display Gift Wrapping Prices]** till `Excluding Tax`, `Including Tax`, eller `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Ange **[!UICONTROL Display Printed Card Prices]** till `Excluding Tax`, `Including Tax`, eller `Including and Excluding Tax`.

1. Ställ in följande visningsalternativ till antingen `Yes` eller `No`, enligt dina krav:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

### [!UICONTROL Fixed Product Taxes]

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Fixed Product Taxes]** -avsnitt.

   ![Fasta produktskatter](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enable FPT]** till `Yes` eller `No`, enligt dina krav.

1. Om FPT är aktiverat anger du visningsalternativ för FPT:

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Price On Product view Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   - `Including FPT Only` - Priserna är fasta produktskatter. FPT-beloppet visas inte separat.
   - `Including FPT and FPT description` - Priserna är fasta produktskatter. FPT-beloppet visas separat.
   - `Excluding FPT. Including FPT description and final price` - De priser som visas inkluderar inte fasta produktskatter. FPT-beloppet visas separat.
   - `Excluding FPT` - De priser som visas inkluderar inte fasta produktskatter. FPT-beloppet visas inte separat.

1. Ange **[!UICONTROL Apply Discounts to FPT]** till `Yes` eller `No`, enligt dina krav.

1. Ange **[!UICONTROL FPT Tax Configuration]** för att fastställa hur FPT beräknas.

   - `Not Taxed` - Välj det här alternativet om din skattejurisdiktion inte beskattar FPT. (Exempel: Kalifornien.)
   - `Taxed` - Välj det här alternativet om din skattejurisdiktion inte beskattar FPT. (Till exempel Kanada.)
   - `Loaded and Displayed with Tax` - Klicka på det här alternativet om FPT läggs till i ordersumman innan moms används. (Exempel: EU-länder.)

1. Ange **[!UICONTROL Include FPT in Subtotal]** till `Yes` eller `No`, enligt dina krav.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Gränsöverskridande priskonsekvens

Gränsöverskridande handel (även kallad priskonsekvens) stöder EU (EU) och andra handlare som vill upprätthålla konsekventa priser för kunder vars skattesatser skiljer sig från butikens skattesats.

Handlare som är verksamma i olika regioner och regioner kan få ett enda pris genom att inkludera momsen i priset på produkten. Priserna är rena och otympliga oavsett vilken skattestruktur och vilka skattesatser som varierar från land till land. De här inställningarna kräver att ett tillägg för momsberäkning installeras från [Marketplace](../getting-started/commerce-marketplace.md), till exempel _Vertex Cloud_.

>[!NOTE]
>
>När gränsöverskridande handel är aktiverad ändras vinstmarginalen med hjälp av skattesats. Vinsten bestäms av formeln:<br>
>`Revenue - CustomerVAT - CostOfGoodsSold`

**_För att möjliggöra priskonsekvens över gränserna:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. För en konfiguration med flera platser anger du **[!UICONTROL Store View]** till den webbplats och butik som är målet för konfigurationen.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Tax]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Calculation Settings]** -avsnitt.

1. Ange **[!UICONTROL Catalog Prices]** till `Including Tax`.

1. För att möjliggöra en enhetlig prissättning över gränserna bör du ange **[!UICONTROL Enable Cross Border Trade]** till `Yes`.

   ![Aktivera inställningar för gränsöverskridande handel](./assets/cross-border-calculations-settings.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
