---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods]'
description: Granska konfigurationsinställningarna på [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] sidan för Commerce Admin.
exl-id: 6545b980-c8ef-460a-a884-d5315f5ad513
feature: Configuration, Payments
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '1691'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods]

>[!TIP]
>
>Betalningstjänster för Adobe Commerce och Magento Open Source utgör en nyckelfärdig självbetjäningslösning, inklusive sandlådetestning och en enkel konfiguration, för tillförlitlig och säker betalningshantering. Om du vill veta mer om den här kraftfulla verktygsuppsättningen och hur den kan ge dig de insikter och den kontroll du behöver för att skapa den bästa upplevelsen för dina köpare kan du läsa [_Användarhandbok för betaltjänster_](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

{{config}}

## [!UICONTROL Merchant Location]

![Affärsplats](./assets/payment-methods-merchant-location.png)<!-- zoom -->

<!-- [Merchant Location](https://docs.magento.com/user-guide/payment/merchant-location.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Merchant Country] | Webbplats | Ange det land där handlaren är registrerad för att bedriva verksamhet. |

{:style=&quot;table-layout:auto&quot;}

## Rekommenderade lösningar

Följande betalningslösningar rekommenderas som ett enkelt sätt för handlare som just har börjat acceptera onlinebetalningar via PayPal-konto eller kreditkort. I takt med att verksamheten växer kan ni kombinera dessa med ytterligare betallösningar från PayPal.

- [PayPal Express-kassan](paypal-express-checkout.md)
- [Braintree](braintree.md)
- [Betalningstjänster](payment-services.md)

>[!NOTE]
>
>Vissa betalningsintegreringar och paketerade tillägg har tagits bort i version 2.4.x och flyttats till Commerce Marketplace. Du hittar de senaste officiella tilläggen för betalningsintegration i [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target=&quot;_blank&quot;}.
><br/>
>**Amazon Pay** och **Klarna**: Adobe Commerce och Magento Open Source, version 2.4.0 till 2.4.3, innehåller dessa tillägg som utvecklats av återförsäljare. Från och med version 2.4.4 ingår inte längre dessa tillägg i kärnversionen och måste installeras och uppdateras från Commerce Marketplace. Marketplace ger också tillgång till aktuell dokumentation från tilläggsutvecklaren.
><br/>
>Om du har aktiverat och konfigurerat något av dessa paketerade tillägg måste du uppdatera `composer.json` som en del av uppgraderingsprocessen för 2.4.4 och för att hantera tilläggsuppdateringar. Se [Uppgraderingsmoduler](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) i _Uppgraderingshandbok_ för mer information.<br/>
><br/>
>**Worldplay**, **Eway**, **CyberSource** och **Authorize.Net**: Mer information om hur du gör en säker övergång från dessa betalningsintegreringar finns i [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target=&quot;_blank&quot;}.

## Andra PayPal-metoder

PayPal erbjuder olika betalningslösningar som uppfyller behoven hos företag av alla storlekar och som är engagerade i affärer över hela världen. Med PayPal kan du acceptera betalningar från alla större debet- och kreditkort. PayPal erbjuder ytterligare bekvämlighet utan extra ansträngning eftersom även kunder som inte har något PayPal-konto kan betala för sina inköp med PayPal.

### PayPal - allt-i-ett-metoder

- [Avancerad PayPal-betalning](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal Payments Standard](paypal-payments-standard.md)

### Betalningsgateways för PayPal

- [PayPal Payflow Pro](paypal-payflow-pro.md) (Inkluderar Express Checkout)
- [Länk till PayPal-betalningsflöde](paypal-payflow-link.md) (Inkluderar Express Checkout)

## Grundläggande betalningsmetoder

Följande betalningsmetoder är inbyggda i Commerce och använder inte en tredjepartsleverantör för att bearbeta transaktionen. Många av de grundläggande betalningssätten hanteras offline, i stället för online.

### [!UICONTROL Check / Money Order]

![Check/penningorder](./assets/payment-methods-check-money-order.png)<!-- zoom -->

<!-- [Check / Money Order](https://docs.magento.com/user-guide/payment/check-money-order.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webbplats | Avgör om kunderna kan betala med check eller penningorder. Alternativ: `Yes` / `No` |
| [!UICONTROL Title] | Butiksvy | Namnet på den här betalningsmetoden som visas för kunder vid utcheckning. |
| [!UICONTROL New Order Status] | Webbplats | Bestämmer startvärdet [orderstatus](../../stores-purchase/order-status.md) som har tilldelats order som har betalats av en check eller en betalningsorder. Standardvärde: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Webbplats | Avgör från vilka länder du godkänner betalning med check eller betalningsorder. Alternativ: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Webbplats | Identifierar de specifika länder från vilka du godkänner betalning med check eller betalningsorder. |
| [!UICONTROL Make Check Payable to] | Butiksvy | Namnet på den enhet som checkar och betalningsorder ska betalas till. |
| [!UICONTROL Send Check to] | Butiksvy | Gatuadress eller PO Box dit checkar och betalningsorder ska skickas. |
| [!UICONTROL Minimum Order Total] | Webbplats | Det minsta orderbeloppet som kan betalas med check eller penningorder. |
| [!UICONTROL Maximum Order Total] | Webbplats | Det största orderbeloppet som kan betalas med check eller penningorder. <br/><br/>**_Obs!_**En order kvalificerar om summan är mellan, eller matchar, minsta eller högsta ordersumma. |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som bestämmer ordern som betalning med check eller betalningsorder visas när det visas med andra betalningsmetoder i kassan. Retur `0` om du vill placera den högst upp i listan. |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Bank Transfer Payment]

![Betalning av banköverföring](./assets/payment-methods-bank-transfer-payment.png)<!-- zoom -->

<!-- [Bank Transfer Payment](https://docs.magento.com/user-guide/payment/bank-transfer.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webbplats | Avgör om kunder kan betala genom att överföra betalning direkt från sin bank till ditt handlarkonto. Alternativ: `Yes` / `No` |
| [!UICONTROL Title] | Butiksvy | Namnet på den här betalningsmetoden som visas för kunder vid utcheckning. |
| [!UICONTROL New Order Status] | Webbplats | Bestämmer den initiala orderstatusen som tilldelats order som betalas via banköverföring. Standardvärde: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Webbplats | Avgör från vilka länder du godkänner betalning via banköverföring. Alternativ: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Webbplats | Identifierar de specifika länder från vilka du godkänner betalning via banköverföring. |
| [!UICONTROL Minimum Order Total] | Webbplats | Det minsta orderbelopp som kan betalas genom banköverföring. |
| [!UICONTROL Maximum Order Total] | Webbplats | Det största orderbeloppet som kan betalas med banköverföring. <br/><br/>**_Obs!_**En order kvalificerar om summan är mellan, eller matchar, minsta eller högsta ordersumma. |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som bestämmer ordern som betalning via banköverföring visas när det visas med andra betalningsmetoder under utcheckning. Retur `0` om du vill placera den högst upp i listan. |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Payment on Account]

{{b2b-feature}}

![Betalning à conto](./assets/payment-methods-payment-on-account.png)<!-- zoom -->

<!-- [Payment on Account](https://docs.magento.com/user-guide/payment/payment-on-account.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webbplats | Avgör om företag kan använda företagskrediter för att göra inköp. Alternativ: `Yes` / `No` |
| [!UICONTROL Title] | Butiksvy | Namnet på den här betalningsmetoden som visas för kunder vid utcheckning. |
| [!UICONTROL New Order Status] | Webbplats | Bestämmer status för nya order som debiteras ett företagskonto. Alternativ: `Pending (default)` / `Processing` / `Suspected Fraud` |
| [!UICONTROL Payment from Applicable Countries] | Webbplats | Bestämmer de länder där du tillåter företag att debitera sina konton för inköp. Alternativ: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Webbplats | Identifierar de specifika länder där företag kan debitera sina konton för inköp. |
| [!UICONTROL Minimum Order Total] | Webbplats | Anger det minsta orderbelopp som kan debiteras ett företagskonto. |
| [!UICONTROL Maximum Order Total] | Webbplats | Det största orderbelopp som kan debiteras ett företagskonto. <br/><br/>**_Obs!_**En order kvalificerar om summan är mellan, eller matchar, minsta eller högsta ordersumma. |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som bestämmer den order som betalning på konto visas när det visas med andra betalningsmetoder vid utcheckning. Retur `0` om du vill placera den högst upp i listan. |

{:style=&quot;table-layout:auto&quot;}

>[!NOTE]
>
>Betalning på konto stöds inte för order med [flera leveransadresser](../../stores-purchase/shipping-settings.md#multiple-addresses) och visas inte bland betalningsalternativen.

### [!UICONTROL Cash On Delivery Payment]

![Kontant vid leverans](./assets/payment-methods-cash-on-delivery-payment.png)<!-- zoom -->

<!-- [Cash On Delivery Payment](../../stores-purchase/cash-on-delivery.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webbplats | Avgör om kunder kan betala genom att överföra betalning direkt från sin bank till ditt handlarkonto. Alternativ: `Yes` / `No` |
| [!UICONTROL Title] | Butiksvy | Namnet på den här betalningsmetoden som visas för kunder vid utcheckning. |
| [!UICONTROL New Order Status] | Webbplats | Bestämmer den initiala orderstatusen som tilldelats order som betalas via banköverföring. Standardvärde: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Webbplats | Avgör från vilka länder du godkänner betalning via banköverföring. Alternativ: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Webbplats | Identifierar de specifika länder från vilka du godkänner betalning via banköverföring. |
| [!UICONTROL Minimum Order Total] | Webbplats | Anger det minsta orderbelopp som kan betalas genom banköverföring. |
| [!UICONTROL Maximum Order Total] | Webbplats | Det största orderbeloppet som kan betalas med banköverföring. <br/><br/>**_Obs!_**En order kvalificerar om summan är mellan, eller matchar, minsta eller högsta ordersumma. |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som bestämmer ordern som betalning via banköverföring visas när det visas med andra betalningsmetoder under utcheckning. Retur `0` om du vill placera den högst upp i listan. |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Zero Subtotal Checkout]

![Noll delsumma, utcheckning](./assets/payment-methods-zero-subtotal-checkout.png)<!-- zoom -->

<!-- [Zero Subtotal Checkout](../../stores-purchase/zero-subtotal-checkout.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Title] | Butiksvy | Namnet som används för den här betalningsmetoden vid utcheckning. Standardvärde: Ingen betalningsinformation krävs |
| [!UICONTROL Enabled] | Webbplats | Avgör om noll deltotal utcheckning är tillgänglig för butiksadministratören för att hantera order som har delsumman noll, till exempel en som har beskattats, men en rabatt har reducerat beloppet till noll. Alternativ: `Yes` / `No` |
| [!UICONTROL New Order Status] | Webbplats | Bestämmer den initiala orderstatusen som tilldelats order som bearbetats som noll deltotal utcheckning. Standardvärde: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Webbplats | Bestämmer från vilka länder som utcheckning av delsummor kan användas. Alternativ: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Webbplats | Identifierar de specifika länder för vilka noll deltotal utcheckning kan tillämpas. |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som bestämmer i vilken ordning titeln, t.ex. &quot;Ingen betalningsinformation krävs&quot;, visas när det visas tillsammans med andra betalningsmetoder vid utcheckning. Retur `0` om du vill placera den högst upp i listan. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Payment actions]

Betalningsåtgärder har konfigurerats _per betalningsmetod_. Betalningsåtgärden avgör när medlen hämtas och när fakturor skapas för dina försäljningsorder.

I avsnittet Grundinställningar för varje enskild betalningsmetod finns en omfattande lista med de olika konfigurationsalternativen.

| Betalningsåtgärd | Beskrivning |
|--- |---|
| [!UICONTROL Authorization] | Godkänner köpet, men spärrar medlen. Beloppet dras inte tillbaka förrän handlaren har tagit det. |
| [!UICONTROL Authorize] | Auktoriserar köparens konto för ordersumman men tar inte emot betalningen. Hämta betalning genom att skapa en faktura. Auktoriserade order kan annulleras eller annulleras. |
| [!UICONTROL Authorize and Capture] | Auktoriserar köparens konto för ordersumman och tar emot betalningen. En faktura skapas automatiskt. Du kan återbetala insamlade medel via kreditnota. Du kan inte annullera en order när betalningen har hämtats. |
| [!UICONTROL Charge on shipment] | Amazon tar emot en registreringsförfrågan och debiterar kunden när en faktura skapas i Commerce. |
| [!UICONTROL Charge on order] | Amazon skapar fakturan och debiterar kunden när ordern läggs. |
| [!UICONTROL Not Capture] | När fakturan skickas registreras inte betalningen. Du måste hämta betalningen via Commerce senare. Det finns en hämtningsknapp i den ifyllda fakturan. Innan du hämtar kan du annullera fakturan. När du har hämtat kan du skapa en kreditnota och annullera fakturan. |
| [!UICONTROL Order] | Representerar ett avtal med PayPal som gör att handlaren kan hämta ett eller flera belopp upp till ordersumman från kundens köparkonto inom en angiven tidsperiod (upp till 29 dagar). |
| [!UICONTROL Sale] | Köpbeloppet godkänns och dras omedelbart tillbaka från kundens konto. |

{:style=&quot;table-layout:auto&quot;}

>[!NOTE]
>
>Markera inte _[!UICONTROL Not Capture]_om du inte är säker på att du kommer att hämta betalningen via Commerce senare. Du kan inte skapa en kreditnota förrän betalningen har hämtats med knappen Hämta.

## [!UICONTROL Purchase Order]

![Inköpsorder](./assets/payment-methods-purchase-order.png)<!-- zoom -->

<!-- [Purchase Order](../../stores-purchase/purchase-order.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webbplats | Bestämmer om kunderna kan betala med inköpsorder (PO). Alternativ: `Yes` / `No` |
| [!UICONTROL Title] | Butiksvy | Namnet på den här betalningsmetoden som visas för kunder vid utcheckning. |
| [!UICONTROL New Order Status] | Webbplats | Bestämmer startvärdet [orderstatus](../../stores-purchase/order-status.md) som tilldelats order som betalats av PO. Standardvärde: Väntande |
| [!UICONTROL Payment from Applicable Countries] | Webbplats | Bestämmer från vilka länder du godkänner betalning av inköpsorder. Alternativ: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Webbplats | Identifierar de specifika länder från vilka du godkänner betalning från inköpsorder. |
| [!UICONTROL Minimum Order Total] | Webbplats | Det minsta orderbelopp som kan betalas av inköpsorder. |
| [!UICONTROL Maximum Order Total] | Webbplats | Det största orderbelopp som kan betalas av inköpsorder. <br/><br/>**_Obs!_**En order kvalificerar om summan är mellan, eller matchar, minsta eller högsta ordersumma. |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som bestämmer den order som betalning via inköpsorder visas när det visas med andra betalningsmetoder vid utcheckning. Retur `0` om du vill placera den högst upp i listan. |

{:style=&quot;table-layout:auto&quot;}
