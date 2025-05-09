---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] i Commerce Admin.
exl-id: 6545b980-c8ef-460a-a884-d5315f5ad513
feature: Configuration, Payments
source-git-commit: 489c72652693a15ffe1c745277bbaa9da084dcba
workflow-type: tm+mt
source-wordcount: '1772'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods]

>[!TIP]
>
>Betalningstjänster för Adobe Commerce och Magento Open Source erbjuder en nyckelfärdig självbetjäningslösning, inklusive sandlådetestning och en enkel konfiguration, för stabil och säker betalningshantering. Om du vill veta mer om den här kraftfulla verktygsuppsättningen och hur den kan ge dig de insikter och den kontroll du behöver för att skapa den bästa upplevelsen för dina köpare kan du läsa [_användarhandboken för betaltjänster_](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html).

{{config}}

## [!UICONTROL Merchant Location]

[!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."}

![Affärsplats](./assets/payment-methods-merchant-location.png)<!-- zoom -->

<!-- [Merchant Location](https://experienceleague.adobe.com/en/docs/commerce-admin/start/setup/store-details#merchant-location) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Merchant Country] | Webbplats | Ange det land där handlaren är registrerad för att bedriva verksamhet. |

{style="table-layout:auto"}

## Rekommenderade lösningar

Följande betalningslösningar rekommenderas som ett enkelt sätt för handlare som just har börjat acceptera onlinebetalningar via PayPal-konto eller kreditkort. I takt med att verksamheten växer kan ni kombinera dessa med ytterligare betallösningar från PayPal.

- [Betalningstjänster](payment-services.md)
- [!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."} [PayPal Express Checkout](paypal-express-checkout.md)
- [!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."} [Braintree](braintree.md)

>[!NOTE]
>
>Vissa betalningsintegreringar och programtillägg har tagits bort i version 2.4.x och flyttats till Commerce Marketplace. Du hittar de senaste officiella tilläggen för betalningsintegrering i [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}.
><br/>
>**Amazon Pay** och **Klarna**: Adobe Commerce och Magento Open Source version 2.4.0 till 2.4.3 innehåller dessa tillägg som utvecklats av återförsäljare. Från och med version 2.4.4 paketeras dessa tillägg inte längre med kärnversionen och måste installeras och uppdateras från Commerce Marketplace. Marketplace ger också tillgång till aktuell dokumentation från tilläggsutvecklaren.
><br/>
>Om du har aktiverat och konfigurerat något av de här paketerade tilläggen måste du uppdatera din `composer.json`-fil som en del av uppgraderingsprocessen för 2.4.4 och hantera tilläggsuppdateringar. Mer information finns i [Uppgraderingsmoduler](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) i _uppgraderingshandboken_.<br/>
><br/>
>**Worldplay**, **Eway**, **CyberSource** och **Authorize.Net**: Mer information om hur du gör en säker övergång från dessa betalningsintegreringar finns i [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}.

## Andra PayPal-metoder

[!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."}

PayPal erbjuder olika betalningslösningar som uppfyller behoven hos företag av alla storlekar och som är engagerade i affärer över hela världen. Med PayPal kan du acceptera betalningar från alla större debet- och kreditkort. PayPal erbjuder ytterligare bekvämlighet utan extra ansträngning eftersom även kunder som inte har något PayPal-konto kan betala för sina inköp med PayPal.

### PayPal - allt-i-ett-metoder

[!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."}

- [Avancerad PayPal-betalning](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal Payments Standard](paypal-payments-standard.md)

### Betalningsgateways för PayPal

[!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."}

- [PayPal Payflow Pro](paypal-payflow-pro.md) (inkluderar Express Checkout)
- [PayPal Payflow Link](paypal-payflow-link.md) (inkluderar Express Checkout)

## Grundläggande betalningsmetoder

Följande betalningsmetoder är inbyggda i Commerce och använder inte en tredjepartsleverantör för att behandla transaktionen. Många av de grundläggande betalningssätten hanteras offline, i stället för online.

### [!UICONTROL Check / Money Order]

![Kontrollera/Pengar beställ](./assets/payment-methods-check-money-order.png)<!-- zoom -->

<!-- [Check / Money Order](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/payments/offline/check-money-order) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webbplats | Avgör om kunderna kan betala med check eller penningorder. Alternativ: `Yes` / `No` |
| [!UICONTROL Title] | Butiksvy | Namnet på den här betalningsmetoden som visas för kunder vid utcheckning. |
| [!UICONTROL New Order Status] | Webbplats | Fastställer den initiala [orderstatusen](../../stores-purchase/order-status.md) som tilldelats order som betalas av en check eller en betalningsorder. Standardvärde: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Webbplats | Avgör från vilka länder du godkänner betalning med check eller betalningsorder. Alternativ: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Webbplats | Identifierar de specifika länder från vilka du godkänner betalning med check eller betalningsorder. |
| [!UICONTROL Make Check Payable to] | Butiksvy | Namnet på den enhet som checkar och betalningsorder ska betalas till. |
| [!UICONTROL Send Check to] | Butiksvy | Gatuadress eller PO Box dit checkar och betalningsorder ska skickas. |
| [!UICONTROL Minimum Order Total] | Webbplats | Det minsta orderbeloppet som kan betalas med check eller penningorder. |
| [!UICONTROL Maximum Order Total] | Webbplats | Det största orderbeloppet som kan betalas med check eller penningorder. <br/><br/>**_Obs!_**En order kvalificerar om summan är mellan, eller matchar, den minsta eller högsta ordersumman. |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som bestämmer ordern som betalning med check eller betalningsorder visas när det visas med andra betalningsmetoder i kassan. Ange `0` om du vill placera den överst i listan. |

{style="table-layout:auto"}

### [!UICONTROL Bank Transfer Payment]

![Banköverföringsbetalning](./assets/payment-methods-bank-transfer-payment.png)<!-- zoom -->

<!-- [Bank Transfer Payment](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/payments/offline/bank-transfer) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webbplats | Avgör om kunder kan betala genom att överföra betalning direkt från sin bank till ditt handlarkonto. Alternativ: `Yes` / `No` |
| [!UICONTROL Title] | Butiksvy | Namnet på den här betalningsmetoden som visas för kunder vid utcheckning. |
| [!UICONTROL New Order Status] | Webbplats | Bestämmer den initiala orderstatusen som tilldelats order som betalas via banköverföring. Standardvärde: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Webbplats | Avgör från vilka länder du godkänner betalning via banköverföring. Alternativ: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Webbplats | Identifierar de specifika länder från vilka du godkänner betalning via banköverföring. |
| [!UICONTROL Minimum Order Total] | Webbplats | Det minsta orderbelopp som kan betalas genom banköverföring. |
| [!UICONTROL Maximum Order Total] | Webbplats | Det största orderbeloppet som kan betalas med banköverföring. <br/><br/>**_Obs!_**En order kvalificerar om summan är mellan, eller matchar, den minsta eller högsta ordersumman. |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som bestämmer ordern som betalning via banköverföring visas när det visas med andra betalningsmetoder under utcheckning. Ange `0` om du vill placera den överst i listan. |

{style="table-layout:auto"}

### [!UICONTROL Payment on Account]

{{b2b-feature}}

![Betalning på konto](./assets/payment-methods-payment-on-account.png)<!-- zoom -->

<!-- [Payment on Account](https://experienceleague.adobe.com/en/docs/commerce-admin/b2b/enable-basic-features#configure-payment-on-account) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webbplats | Avgör om företag kan använda företagskrediter för att göra inköp. Alternativ: `Yes` / `No` |
| [!UICONTROL Title] | Butiksvy | Namnet på den här betalningsmetoden som visas för kunder vid utcheckning. |
| [!UICONTROL New Order Status] | Webbplats | Bestämmer status för nya order som debiteras ett företagskonto. Alternativ: `Pending (default)` / `Processing` / `Suspected Fraud` |
| [!UICONTROL Payment from Applicable Countries] | Webbplats | Bestämmer de länder där du tillåter företag att debitera sina konton för inköp. Alternativ: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Webbplats | Identifierar de specifika länder där företag kan debitera sina konton för inköp. |
| [!UICONTROL Minimum Order Total] | Webbplats | Anger det minsta orderbelopp som kan debiteras ett företagskonto. |
| [!UICONTROL Maximum Order Total] | Webbplats | Det största orderbelopp som kan debiteras ett företagskonto. <br/><br/>**_Obs!_**En order kvalificerar om summan är mellan, eller matchar, den minsta eller högsta ordersumman. |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som bestämmer den order som betalning på konto visas när det visas med andra betalningsmetoder vid utcheckning. Ange `0` om du vill placera den överst i listan. |

{style="table-layout:auto"}

>[!NOTE]
>
>Betalning på konto stöds inte för order med [flera leveransadresser](../../stores-purchase/shipping-settings.md#multiple-addresses) och visas inte bland betalningsalternativen.

### [!UICONTROL Cash On Delivery Payment]

![Kontant vid betalning](./assets/payment-methods-cash-on-delivery-payment.png)<!-- zoom -->

<!-- [Cash On Delivery Payment](../../stores-purchase/cash-on-delivery.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webbplats | Avgör om kunder kan betala genom att överföra betalning direkt från sin bank till ditt handlarkonto. Alternativ: `Yes` / `No` |
| [!UICONTROL Title] | Butiksvy | Namnet på den här betalningsmetoden som visas för kunder vid utcheckning. |
| [!UICONTROL New Order Status] | Webbplats | Bestämmer den initiala orderstatusen som tilldelats order som betalas via banköverföring. Standardvärde: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Webbplats | Avgör från vilka länder du godkänner betalning via banköverföring. Alternativ: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Webbplats | Identifierar de specifika länder från vilka du godkänner betalning via banköverföring. |
| [!UICONTROL Minimum Order Total] | Webbplats | Anger det minsta orderbelopp som kan betalas genom banköverföring. |
| [!UICONTROL Maximum Order Total] | Webbplats | Det största orderbeloppet som kan betalas med banköverföring. <br/><br/>**_Obs!_**En order kvalificerar om summan är mellan, eller matchar, den minsta eller högsta ordersumman. |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som bestämmer ordern som betalning via banköverföring visas när det visas med andra betalningsmetoder under utcheckning. Ange `0` om du vill placera den överst i listan. |

{style="table-layout:auto"}

### [!UICONTROL Zero Subtotal Checkout]

![Ingen deltotal utcheckning](./assets/payment-methods-zero-subtotal-checkout.png)<!-- zoom -->

<!-- [Zero Subtotal Checkout](../../stores-purchase/zero-subtotal-checkout.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Title] | Butiksvy | Namnet som används för den här betalningsmetoden vid utcheckning. Standardvärde: Ingen betalningsinformation krävs |
| [!UICONTROL Enabled] | Webbplats | Avgör om noll deltotal utcheckning är tillgänglig för butiksadministratören för att hantera order som har delsumman noll, till exempel en som har beskattats, men en rabatt har reducerat beloppet till noll. Alternativ: `Yes` / `No` |
| [!UICONTROL New Order Status] | Webbplats | Bestämmer den initiala orderstatusen som tilldelats order som bearbetats som noll deltotal utcheckning. Standardvärde: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Webbplats | Bestämmer från vilka länder som utcheckning av delsummor kan användas. Alternativ: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Webbplats | Identifierar de specifika länder för vilka noll deltotal utcheckning kan tillämpas. |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som bestämmer i vilken ordning titeln, t.ex. &quot;Ingen betalningsinformation krävs&quot;, visas när det visas tillsammans med andra betalningsmetoder vid utcheckning. Ange `0` om du vill placera den överst i listan. |

{style="table-layout:auto"}

## [!UICONTROL Payment actions]

[!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."}

Betalningsåtgärder är konfigurerade _per betalningsmetod_. Betalningsåtgärden avgör när medlen hämtas och när fakturor skapas för dina försäljningsorder.

I avsnittet Grundinställningar för varje enskild betalningsmetod finns en omfattande lista med de olika konfigurationsalternativen.

| Betalningsåtgärd | Beskrivning |
|--- |---|
| [!UICONTROL Authorization] | Godkänner köpet, men spärrar medlen. Beloppet dras inte tillbaka förrän handlaren har tagit det. |
| [!UICONTROL Authorize] | Auktoriserar köparens konto för ordersumman men tar inte emot betalningen. Hämta betalning genom att skapa en faktura. Auktoriserade order kan annulleras eller annulleras. |
| [!UICONTROL Authorize and Capture] | Auktoriserar köparens konto för ordersumman och tar emot betalningen. En faktura skapas automatiskt. Du kan återbetala insamlade medel via kreditnota. Du kan inte annullera en order när betalningen har hämtats. |
| [!UICONTROL Charge on shipment] | Amazon tar emot en registreringsförfrågan och debiterar kunden när en faktura skapas i Commerce. |
| [!UICONTROL Charge on order] | Amazon skapar fakturan och debiterar kunden när ordern läggs. |
| [!UICONTROL Not Capture] | När fakturan skickas registreras inte betalningen. Du förutsätts betala via Commerce senare. Det finns en hämtningsknapp i den ifyllda fakturan. Innan du hämtar kan du annullera fakturan. När du har hämtat kan du skapa en kreditnota och annullera fakturan. |
| [!UICONTROL Order] | Representerar ett avtal med PayPal som gör att handlaren kan hämta ett eller flera belopp upp till ordersumman från kundens köparkonto inom en angiven tidsperiod (upp till 29 dagar). |
| [!UICONTROL Sale] | Köpbeloppet godkänns och dras omedelbart tillbaka från kundens konto. |

{style="table-layout:auto"}

>[!NOTE]
>
>Välj inte alternativet _[!UICONTROL Not Capture]_om du inte är säker på att du kommer att hämta betalningen via Commerce senare. Du kan inte skapa en kreditnota förrän betalningen har hämtats med knappen Hämta.

## [!UICONTROL Purchase Order]

![Inköpsorder](./assets/payment-methods-purchase-order.png)<!-- zoom -->

<!-- [Purchase Order](../../stores-purchase/purchase-order.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webbplats | Bestämmer om kunderna kan betala med inköpsorder (PO). Alternativ: `Yes` / `No` |
| [!UICONTROL Title] | Butiksvy | Namnet på den här betalningsmetoden som visas för kunder vid utcheckning. |
| [!UICONTROL New Order Status] | Webbplats | Bestämmer den initiala [orderstatusen](../../stores-purchase/order-status.md) som tilldelats order som betalats av inköpsorder. Standardvärde: Väntande |
| [!UICONTROL Payment from Applicable Countries] | Webbplats | Bestämmer från vilka länder du godkänner betalning av inköpsorder. Alternativ: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Webbplats | Identifierar de specifika länder från vilka du godkänner betalning från inköpsorder. |
| [!UICONTROL Minimum Order Total] | Webbplats | Det minsta orderbelopp som kan betalas av inköpsorder. |
| [!UICONTROL Maximum Order Total] | Webbplats | Det största orderbelopp som kan betalas av inköpsorder. <br/><br/>**_Obs!_**En order kvalificerar om summan är mellan, eller matchar, den minsta eller högsta ordersumman. |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som bestämmer den order som betalning via inköpsorder visas när det visas med andra betalningsmetoder vid utcheckning. Ange `0` om du vill placera den överst i listan. |

{style="table-layout:auto"}
