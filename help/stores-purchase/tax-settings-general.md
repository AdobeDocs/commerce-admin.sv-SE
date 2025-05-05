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

Följande instruktioner tar dig igenom grundläggande skattekonfiguration för din Commerce-instans. Innan du konfigurerar dina skatter måste du känna till skattekraven för ditt [språkområde](store-localize.md#step-3-change-the-locale-of-the-store-view). Slutför sedan skattekonfigurationen enligt dina krav.

Administratörens [behörigheter](../systems/permissions.md) kan ställas in så att [åtkomst](../systems/permissions-user-roles.md) begränsas till skatteresurser, baserat på vilket företag _behöver känna till_. Om du vill skapa en administratörsroll med tillgång till skatteinställningar väljer du både moms och system/skatt. Om du skapar en webbplats för en region som skiljer sig från din standardplats för leverans, måste du även tillåta åtkomst till system-/leveransresurserna för rollen. Leveransinställningarna bestämmer momssatsen som används för katalogpriser.

## Konfigurera allmänna skatteinställningar

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Om du vill ha en konfiguration med flera platser anger du **[!UICONTROL Store View]** till webbplatsen och lagret som är målet för konfigurationen.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Tax]**.

1. Slutför följande konfigurationsinställningar.

   Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för de inställningar som är nedtonade.

### [!UICONTROL Tax Classes]

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Tax Classes]**.

   ![Skatteklasser](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

   - **Skatteklass för leverans** - Ange lämplig klass. Standardklasserna är: `None` och `Taxable Goods`
   - **Skatteklass för presentalternativ** — ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Ange till lämplig klass. Standardklasserna är: `None` och `Taxable Goods`
   - **Standardskatteklass för produkt** - Ange lämplig klass. Standardklasserna är: `None` och `Taxable Goods`
   - **Standardskatteklass för kund** - Ange lämplig klass. Standardklassen är: `Retail Customer` och `Wholesale Customer`

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

### [!UICONTROL Calculation Settings]

1. Expandera avsnittet **[!UICONTROL Calculation Settings]**.

   ![Beräkningsinställningar](../configuration-reference/sales/assets/tax-calculation-settings.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Tax Calculation Method Based On]** till något av följande:

   - `Unit Price` - priset för varje produkt
   - `Row Total` - Summan av radobjektet i ordern, minus rabatter
   - `Total` - Ordersumman

1. Ange **[!UICONTROL Tax Calculation Based On]** till något av följande:

   - `Shipping Address` - Den adress dit ordern ska skickas
   - `Billing Address` - Kundens eller företagets faktureringsadress
   - `Shipping Origin` - Den adress som anges som [ursprungspunkt](shipping-settings.md#point-of-origin) för din butik

1. Ange **[!UICONTROL Catalog Prices]** till `Excluding Tax` eller `Including Tax`.

1. Ange **[!UICONTROL Shipping Prices]** till `Excluding Tax` eller `Including Tax`.

1. Ange **[!UICONTROL Apply Customer Tax]** till något av följande för att avgöra om moms tillämpas på det ursprungliga eller rabatterade priset: `After Discount` eller `Before Discount`

1. Ange **[!UICONTROL Apply Discount on Prices]** till något av följande för att avgöra om rabatterna inkluderar eller exkluderar moms: `Excluding Tax` eller `Including Tax`

1. Ange **[!UICONTROL Apply Tax On]** till `Custom price if available` eller `Original price only`.

1. Ange **[!UICONTROL Enable Cross-Border Trade]** till något av följande:

   - `Yes` - Använd konsekventa priser för olika skattesatser. Om katalogpriset innehåller moms väljer du den här inställningen för att justera priset oavsett kundens momssats.
   - `No` - Variera priset per momssats.

   >[!IMPORTANT]
   >
   >Om [gränsöverskridande handel](#cross-border-price-consistency) är aktiverad ändras vinstmarginalen per skattesats. Vinsten bestäms av formeln (`Revenue - CustomerVAT - CostOfGoodsSold`). För att möjliggöra gränsöverskridande handel måste priserna anges till att omfatta skatt.

### [!UICONTROL Default Tax Destination Calculation]

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Default Tax Destination Calculation]**.

   ![Beräkning av standardmomsmål](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Default Country]** för momsberäkningar.

1. Ange **[!UICONTROL Default State]** för momsberäkningar om tillämpligt.

1. Ange **[!UICONTROL Default Post Code]** för momsberäkningar om tillämpligt.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

### [!UICONTROL Price Display Settings]

>[!IMPORTANT]
>
>Vissa kombinationer av inställningar som är relaterade till en prisvisning som både inkluderar och exkluderar moms kan vara förvirrande för kunden. Information om hur du undviker att utlösa ett varningsmeddelande finns i [rekommenderade inställningar](taxes.md#warning-messages).

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Price Display Settings]**.

   ![Prisvisningsinställningar](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Display Product Prices in Catalog]** till något av följande:

   - `Excluding Tax` - Katalogpriser som visas i butiken inkluderar inte moms.
   - `Including Tax` - Katalogpriser i butiken inkluderar endast moms om en momsregel matchar skatteursprunget eller om kundens adress matchar momsregeln. Detta kan inträffa efter att en kund har skapat ett konto, loggat in eller använder verktyget för beräkning av skatt och leverans i kundvagnen.
   - `Including and Excluding Tax` - Katalogpriser som visas i butiken visas både med och utan moms.

1. Ange **[!UICONTROL Display Shipping Prices]** till `Excluding Tax`, `Including Tax` eller `Including and Excluding Tax`.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

### [!UICONTROL Shopping Cart Display Settings]

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Shopping Cart Display Settings]**.

   ![Visningsinställningar för kundvagn](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. För följande inställningar väljer du hur du vill att skatter och priser ska visas i kundvagnen, enligt kraven för butik och språkområde:

   - Ange **[!UICONTROL Display Prices]** till `Excluding Tax`, `Including Tax` eller `Including and Excluding Tax`.

   - Ange **[!UICONTROL Display Subtotal]** till `Excluding Tax`, `Including Tax` eller `Including and Excluding Tax`.

   - Ange **[!UICONTROL Display Shipping Amount]** till `Excluding Tax`, `Including Tax` eller `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Ange **[!UICONTROL Display Gift Wrapping Prices]** till `Excluding Tax`, `Including Tax` eller `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Ange **[!UICONTROL Display Printed Card Prices]** till `Excluding Tax`, `Including Tax` eller `Including and Excluding Tax`.

1. Ange följande visningsalternativ till antingen `Yes` eller `No`, beroende på dina behov:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

### [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

1. Expandera ![Utökning](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]**.

   ![Visningsinställningar för beställningar, fakturor och kreditnotor](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Ange hur priser och skatter ska visas i order, fakturor och kreditnotor:

   - Ange **[!UICONTROL Display Prices]** till `Excluding Tax`, `Including Tax` eller `Including and Excluding Tax`.

   - Ange **[!UICONTROL Display Subtotal]** till `Excluding Tax`, `Including Tax` eller `Including and Excluding Tax`.

   - Ange **[!UICONTROL Display Shipping Amount]** till `Excluding Tax`, `Including Tax` eller `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Ange **[!UICONTROL Display Gift Wrapping Prices]** till `Excluding Tax`, `Including Tax` eller `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Ange **[!UICONTROL Display Printed Card Prices]** till `Excluding Tax`, `Including Tax` eller `Including and Excluding Tax`.

1. Ange följande visningsalternativ till antingen `Yes` eller `No`, enligt dina krav:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

### [!UICONTROL Fixed Product Taxes]

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Fixed Product Taxes]**.

   ![Fasta produktskatter](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enable FPT]** till antingen `Yes` eller `No` enligt dina krav.

1. Om FPT är aktiverat anger du visningsalternativ för FPT:

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Price On Product view Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   - `Including FPT Only` - Priserna visas inklusive fasta produktskatter. FPT-beloppet visas inte separat.
   - `Including FPT and FPT description` - Priserna visas inklusive fasta produktskatter. FPT-beloppet visas separat.
   - `Excluding FPT. Including FPT description and final price` - De visade priserna inkluderar inte fasta produktskatter. FPT-beloppet visas separat.
   - `Excluding FPT` - De visade priserna inkluderar inte fasta produktskatter. FPT-beloppet visas inte separat.

1. Ange **[!UICONTROL Apply Discounts to FPT]** till `Yes` eller `No` enligt dina krav.

1. Ange **[!UICONTROL FPT Tax Configuration]** för att bestämma hur FPT ska beräknas.

   - `Not Taxed` - Välj det här alternativet om din skattejurisdiktion inte beskattar FPT. (Exempel: Kalifornien.)
   - `Taxed` - Välj det här alternativet om din skattejurisdiktion inte beskattar FPT. (Till exempel Kanada.)
   - `Loaded and Displayed with Tax` - Klicka på det här alternativet om FPT läggs till i ordersumman innan moms används. (Exempel: EU-länder.)

1. Ange **[!UICONTROL Include FPT in Subtotal]** till `Yes` eller `No` enligt dina krav.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Gränsöverskridande priskonsekvens

Gränsöverskridande handel (även kallad priskonsekvens) stöder EU (EU) och andra handlare som vill upprätthålla konsekventa priser för kunder vars skattesatser skiljer sig från butikens skattesats.

Handlare som är verksamma i olika regioner och regioner kan få ett enda pris genom att inkludera momsen i priset på produkten. Priserna är rena och otympliga oavsett vilken skattestruktur och vilka skattesatser som varierar från land till land. Dessa inställningar kräver att ett tillägg för momsberäkning installeras från [Marketplace](../getting-started/commerce-marketplace.md), till exempel _Vertex Cloud_.

>[!NOTE]
>
>När gränsöverskridande handel är aktiverad ändras vinstmarginalen med hjälp av skattesats. Vinsten bestäms av formeln:<br>
>`Revenue - CustomerVAT - CostOfGoodsSold`

**_Så här aktiverar du gränsöverskridande priskonsekvens:_**

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Om du vill ha en konfiguration med flera platser anger du **[!UICONTROL Store View]** till webbplatsen och lagret som är målet för konfigurationen.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Tax]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Calculation Settings]**.

1. Ange **[!UICONTROL Catalog Prices]** till `Including Tax`.

1. Om du vill aktivera priskonsekvens över gränserna anger du **[!UICONTROL Enable Cross Border Trade]** till `Yes`.

   ![Aktivera inställningar för gränsöverskridande handel](./assets/cross-border-calculations-settings.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
