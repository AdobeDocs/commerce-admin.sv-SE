---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Tax]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Sales] &gt; [!UICONTROL Tax] i Commerce Admin.
exl-id: eb929a6c-adb2-45ac-b6ec-6239938355bf
feature: Configuration, Taxes
source-git-commit: f95e6d22f83b518c64b254f0d98147e3c6ebaf42
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Tax]

>[!NOTE]
>
>Adobe Commerce och Magento Open Source, version 2.4.0 till 2.4.3, innehöll tillägget Vertex som utvecklades av leverantören och som användes för att integrera med [!UICONTROL Vertex Cloud]. Från och med version 2.4.4 är det här tillägget inte längre paketerat med kärnversionen och måste installeras och uppdateras från Commerce Marketplace. Marketplace ger också tillgång till aktuell dokumentation från tilläggsutvecklaren.
><br><br>
>Om du har det paketerade tillägget aktiverat och konfigurerat måste du uppdatera filen Composer.json som en del av uppgraderingsprocessen för 2.4.4 och hantera tilläggsuppdateringar vidare. Mer information finns i [Uppgraderingsmoduler och tillägg](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) i _Uppgraderingshandboken_.

{{config}}

## [!UICONTROL Tax Classes]

![Skatteklasser](./assets/tax-tax-classes.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Skatteklasser](../../stores-purchase/tax-class.md) i _Handboken för butiker och köp_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Tax Class for Shipping] | Webbplats | Identifierar den momsklass som används för leverans. Alternativen inkluderar alla tillgängliga produktskatteklasser: `None` / `Taxable Goods` / `Shipping` / `Tax Exempt` |
| [!UICONTROL Tax Class for Gift Options] | Webbplats | ![Adobe Commerce](../../assets/adobe-logo.svg) (endast Adobe Commerce) Identifierar den standardskatteklass som används för presentalternativ. |
| [!UICONTROL Default Tax Class for Product] | Global | Identifierar den standardskatteklass som används för produkter. |
| [!UICONTROL Default Tax Class for Customer] | Global | Identifierar den standardskatteklass som används för kunder. |

{style="table-layout:auto"}

## [!UICONTROL Calculation Settings]

![Beräkningsinställningar](./assets/tax-calculation-settings.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | Webbplats | Bestämmer metoden som används för att beräkna momsen för en order. Alternativ:<br/>**`Unit Price`**- Skatteberäkningar baseras på enhetspriset för varje produkt.<br/>**`Row Total`** - Skatteberäkningar baseras på radartikelsumman. <br/>**`Total`**- Skatteberäkningar baseras på ordersumman.<br/><br/>_ **&#x200B; Obs!**&#x200B;_Om ett tillägg för momsberäkning installeras från Marketplace, till exempel _Vertex Cloud_ , visas tilläggstjänsten som ett alternativ. |
| [!UICONTROL Tax Calculation Based On] | Webbplats | Avgör om momsberäkningen baseras på leveransadress, faktureringsadress eller leveransens ursprung. Alternativ: `Shipping Address` / `Billing Address` / `Shipping Origin` |
| [!UICONTROL Catalog Prices] | Webbplats | Avgör om katalogpriser innehåller eller exkluderar moms. Alternativ: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Shipping Prices] | Webbplats | Anger fraktpriser inklusive eller exklusive moms. Alternativ: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Apply Customer Tax] | Webbplats | Avgör om moms tillämpas före eller efter en rabatt. Alternativ: `Before Discount` / `After Discount` |
| [!UICONTROL Apply Discount on Prices] | Webbplats | Avgör om rabattpriser inkluderar eller exkluderar moms. Alternativ: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Apply Tax On] | Webbplats | Avgör om momsen gäller för det ursprungliga priset eller för ett anpassat pris, om tillgängligt. Alternativ: `Custom price if available` / `Original price only` |
| [!UICONTROL Enable Cross Border Trade] | Webbplats | När det här alternativet är aktiverat tillämpas konsekventa priser över gränserna för regioner med olika skattesatser. Alternativ: `Yes` / `No` <br/><br/>**_Obs!_**&#x200B;Om du använder gränsöverskridande handel justeras vinstmarginalen efter skattesats. |

{style="table-layout:auto"}

## [!UICONTROL Default Tax Destination Calculation]

![Beräkning av standardmomsmål](./assets/tax-default-tax-destination-calculation.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Default Country] | Butiksvy | Anger det land som momsberäkningarna baseras på. |
| [!UICONTROL Default State] | Butiksvy | Anger vilket tillstånd momsberäkningar baseras på. En asterisk (*) kan fungera som ett jokertecken för att ange alla lägen i det valda landet. |
| [!UICONTROL Default Post Code] | Butiksvy | Identifierar postnumret eller postnumret som momsberäkningarna baseras på. En asterisk (*) kan fungera som jokertecken för att ange alla postnummer i det valda läget. |

{style="table-layout:auto"}

## [!UICONTROL Price Display Settings]

![Prisvisningsinställningar](./assets/tax-price-display-settings.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Konfigurera visningsinställningar för pris](../../stores-purchase/display-settings.md#configure-price-display-settings) i _butiker och inköpsupplevelseguiden_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | Butiksvy | Avgör om produktpriser som publiceras i katalogen inkluderar eller exkluderar moms, eller visar två versioner av priset, en med och den andra utan moms. Alternativ: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` <br/><br/>**_Obs!_**&#x200B;Om du anger att fältet Visa produktpriser ska vara `Including Tax` visas momsen bara om det finns en momsregel som matchar skatteursprunget eller om det finns en kundadress som matchar momsregeln. Händelser som kan utlösa en matchning är bland annat att skapa ett kundkonto, logga in eller använda skattnings- och leveransberäkningsverktyget i kundvagnen. |
| [!UICONTROL Display Shipping Prices] | Butiksvy | Avgör om leveranspriserna inkluderar eller exkluderar moms, eller visar två versioner av leveranspriset; den ena med och den andra utan moms. Alternativ: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart Display Settings]

![Visningsinställningar för kundvagn](./assets/tax-shopping-cart-display-settings.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Konfigurera visningsinställningar för kundvagn](../../stores-purchase/display-settings.md#step-2-configure-shopping-cart-display-settings) i _Handboken för butiker och köp_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Display Prices] | Butiksvy | Avgör om kundvagnspriserna inkluderar eller exkluderar moms, eller visar två versioner av priset; den ena med och den andra utan moms. Alternativ: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Subtotal|Store View] | Avgör om delsumman i kundvagnen innehåller eller exkluderar moms, eller visar två versioner av delsumman; den ena med och den andra utan moms. Alternativ: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | Butiksvy | Avgör om kundvagnens leveransbelopp inkluderar eller exkluderar moms, eller visar två versioner av fraktbeloppet, den ena med och den andra utan moms. Alternativ: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Additionally Show Order Total Without Tax] | Butiksvy | Avgör om en extra rad med totalbeloppet utan moms visas i kundvagnen. Alternativ: `Yes` / `No` |
| [!UICONTROL Display Full Tax Summary] | Butiksvy | Avgör om kundvagnen innehåller en fullständig momssammanfattning. Alternativ: `Yes` / `No` |
| [!UICONTROL Display Zero Tax Subtotal] | Butiksvy | Avgör om kundvagnen innehåller en momsdelsumma när momsen är noll. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

![Visningsinställningar för beställningar, fakturor och kreditnotor](./assets/tax-orders-invoices-credit-memos-display-settings.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Konfigurera visningsinställningar för order, fakturor och kreditnotor](../../stores-purchase/display-settings.md#step-3-configure-order-invoice-and-credit-memo-display-settings) i _Handboken för butiker och köp_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Display Prices] | Butiksvy | Avgör om priserna på försäljningsdokument inkluderar eller exkluderar moms, eller om varje dokument visar två versioner av priset; den ena med och den andra utan moms. Alternativ: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Subtotal] | Butiksvy | Avgör om delsumman i försäljningsdokument inkluderar eller exkluderar moms, eller om varje dokument visar två versioner av delsumman; den ena med och den andra utan moms. Alternativ: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | Butiksvy | Avgör om leveransbeloppet i försäljningsdokument inkluderar eller exkluderar moms, eller om varje dokument visar två versioner av delsumman; den ena med och den andra utan moms. Alternativ: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Additionally Show Order Total Without Tax] | Butiksvy | Avgör om en extra rad med totalbeloppet utan moms visas på försäljningsdokument. Alternativ: `Yes` / `No` |
| [!UICONTROL Display Full Tax Summary] | Butiksvy | Avgör om den fullständiga momssammanfattningen visas på försäljningsdokument. Alternativ: `Yes` / `No` |
| [!UICONTROL Display Zero Tax Subtotal] | Butiksvy | Avgör delsummeavsnittet i försäljningsdokument när ingen moms debiteras. Alternativ: `Yes` / `No` |
| [!UICONTROL Display Gift Wrapping Prices] | Butiksvy | ![Adobe Commerce](../../assets/adobe-logo.svg) (endast Adobe Commerce) Avgör om presentförpackningspriserna ingår i delsumman. Alternativ: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Printed Card Prices] | Butiksvy | ![Adobe Commerce](../../assets/adobe-logo.svg) (endast Adobe Commerce) Avgör om utskrivna kortpriser ingår i delsumman. Alternativ: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |

{style="table-layout:auto"}

## [!UICONTROL Fixed Product Taxes]

![Fast produktskatt](./assets/tax-fixed-product-taxes.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Fast produktskatt (FPT)](../../stores-purchase/fixed-product-tax.md) i _Handboken för butiker och köp_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable FPT] | Webbplats | Avgör om FPT är tillgängligt. Alternativ: `Yes` / `No` |
| [!UICONTROL Display Prices in Product Lists] | Webbplats | Styr visningen av FPT i produktlistor. Alternativ:<br/> **`Including FPT Only`** - Priserna visas inklusive fasta produktskatter. FPT-beloppet visas inte separat.<br/>**`Including FPT and FPT description`**- Priserna visas inklusive fasta produktskatter. FPT-beloppet visas separat.<br/>**`Excluding FPT. Including FPT description and final price`** - De visade priserna inkluderar inte fasta produktskatter. FPT-beloppet visas separat.<br/>**`Excluding FPT`**- De visade priserna inkluderar inte fasta produktskatter. FPT-beloppet visas inte separat. |
| [!UICONTROL Display Prices On Product View Page] | Webbplats | Styr visningen av FPT på produktsidan. Alternativ:<br/> **`Including FPT Only`** - Priserna visas inklusive fasta produktskatter. FPT-beloppet visas inte separat.<br/>**`Including FPT and FPT description`**- Priserna visas inklusive fasta produktskatter. FPT-beloppet visas separat.<br/>**`Excluding FPT. Including FPT description and final price`** - De visade priserna inkluderar inte fasta produktskatter. FPT-beloppet visas separat.<br/>**`Excluding FPT`**- De visade priserna inkluderar inte fasta produktskatter. FPT-beloppet visas inte separat. |
| [!UICONTROL Display Prices in Sales Modules] | Webbplats | Styr visningen av FPT i kundvagnen och under utcheckningen. Alternativ:<br/> **`Including FPT Only`** - Priserna visas inklusive fasta produktskatter. FPT-beloppet visas inte separat.<br/>**`Including FPT and FPT description`**- Priserna visas inklusive fasta produktskatter. FPT-beloppet visas separat.<br/>**`Excluding FPT. Including FPT description and final price`** - De visade priserna inkluderar inte fasta produktskatter. FPT-beloppet visas separat.<br/>**`Excluding FPT`**- De visade priserna inkluderar inte fasta produktskatter. FPT-beloppet visas inte separat. |
| [!UICONTROL Display Prices in Emails] | Webbplats | Styr visningen av FPT i e-post. Alternativ:<br/> **`Including FPT Only`** - Priserna visas inklusive fasta produktskatter. FPT-beloppet visas inte separat.<br/>**`Including FPT and FPT description`**- Priserna visas inklusive fasta produktskatter. FPT-beloppet visas separat.<br/>**&#x200B; exklusive FPT. FPT-beskrivning och slutpris &#x200B;** ingår inte - de visade priserna inkluderar inte fasta produktskatter. FPT-beloppet visas separat.<br/>**`Excluding FPT`** - De visade priserna inkluderar inte fasta produktskatter. FPT-beloppet visas inte separat. |
| [!UICONTROL Apply Tax to FPT] | Webbplats | Avgör om moms tillämpas på FPT-beloppet. Alternativ: `Yes` / `No` |
| [!UICONTROL Include FPT in Subtotal] | Webbplats | Avgör om FPT ingår i kundvagnens delsumma. Alternativ: <br/>**`Yes`**- Inkluderar FPT i kundvagnens delsumma.<br/>**`No`** - FPT ingår inte i delsumman och placeras efter delsumman i kundvagnen. |

{style="table-layout:auto"}
