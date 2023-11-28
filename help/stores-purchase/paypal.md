---
title: Betalningslösningar för PayPal
description: Lär dig mer om de integreringar av betalningslösningar från PayPal som är tillgängliga för din butik.
exl-id: d447b98e-d30c-4759-9ae0-94ccbeed9ba4
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 0%

---

# Betalningslösningar för PayPal

PayPal är världsledande inom onlinebetalningar och ett snabbt och säkert sätt för era kunder att betala online. Valet av tillgängliga PayPal-lösningar varierar beroende på var säljaren befinner sig. PayPal Express Checkout och PayPal Payments Standard kan användas i alla delar av världen. Mer information finns på [PayPal-lösningar per land](#paypal-solutions-by-country).

>[!IMPORTANT]
>
>**Krav för PSD2:** <br/>
>Från och med den 14 september 2019 kan europeiska banker avböja betalningar som inte uppfylls [PSD2](../getting-started/compliance-payment-services-directive.md) krav. För de flesta PayPal-lösningar krävs ingen åtgärd för att uppfylla PSD 2 eftersom dessa krav hanteras av PayPal.

## PayPal-företagskonto

Om du vill erbjuda PayPal som betalningsmetod i din butik måste du ha en PayPal [företagskonto][1] och/eller en [PayPal Payflow-konto][2]. Kontokraven anges i beskrivningen av varje PayPal-lösning. Ditt PayPal-handelskonto används även för att hantera alla [bedrägerifilter](#paypal-fraud-management-filters) som tillämpas på inköp från din butik.

Kunder som använder PayPal Express Checkout eller Express Checkout för Payflow Pro måste ha ett PayPal-köpkonto. PayPal Payments Standard (Web Site Payments Standard i vissa länder) kan användas direkt eller via ett köpkonto när handlaren aktiverar _Valfritt PayPal-konto_. Som standard är den här parametern aktiverad så att kunderna kan välja att ange sin kreditkortsinformation eller skapa ett köpkonto med PayPal. När det är inaktiverat måste kunderna först skapa ett PayPal-köpkonto innan de kan göra ett köp.

Webbplatsbetalningar Pro, webbplatsbetalningar Pro Payflow Edition, Payflow Pro Gateway och Payflow Link kräver att kunderna anger kreditkortsinformation under utcheckningen.

## PayPal Credit och PayLater

PayPal PayLater ger dina kunder snabb tillgång till finansiering, så att de kan köpa nu och betala med tiden, utan extra kostnad. Du debiteras inte när kunderna väljer PayPal-kreditalternativ, och du betalar bara din vanliga PayPal-transaktionsavgift. Mer information finns i [PayPals webbplats][3].

Ge försäljningen ett lyft när ni annonserar finansiering. PayPal hjälper till att göra webbläsare till köpare genom att finansiera med PayPal PayLater. Era kunder kan betala med tiden, samtidigt som ni betalar i förskott - utan extra kostnad. Använd kostnadsfria banners för PayPal för att annonsera PayPal-finansiering som ett betalningsalternativ när kunderna checkar ut med PayPal. PayPal Advertising Program har visat sig generera ytterligare inköp och öka de genomsnittliga inköpsstorlekarna med 15 % eller mer.

Du kan enkelt lägga till kostnadsfria, färdiga banners på webbplatsens och _PayPal Credit_ till kundvagnen under utcheckningen för att påminna kunderna om att finansiering är lätt tillgänglig.

>[!NOTE]
>
>Från och med version 2.4.3 stöds PayPal PayLater i distributioner som inkluderar PayPal. Med den här funktionen kan kunderna betala för en beställning varannan vecka i stället för att betala hela beloppet vid köptillfället. PayPal-kreditupplevelsen är föråldrad.

För amerikanska handlare är PayPal-kredit aktiverat som standard för [PayPal Express-kassan](paypal-express-checkout.md) betalningsalternativ. Om du vill inaktivera den för den här betalningsmetoden går du till _Funktioner_ avsnitt i [Konfiguration av PayPal Express-utcheckning](paypal-express-checkout.md#features).

PayPal-kredit är inaktiverad som standard för andra PayPal-betalningslösningar, men kan aktiveras i betalningsmetodkonfigurationen för stödlösningar:

- [Avancerade betalningar](paypal-payments-advanced.md)
- [Payments Pro](paypal-payments-pro.md)
- [Betalningar, standard](paypal-payments-standard.md)
- [Payflow Pro](paypal-payflow-pro.md)
- [Betalningslänk](paypal-payflow-link.md)

>[!IMPORTANT]
>
>Innan du konfigurerar PayPal Credit eller PayPal PayLater för din butik måste du se till att den är aktiverad i ditt PayPal-handlarkonto.

## Integrerade PayPal-lösningar

Med PayPal och Adobe Commerce kan du acceptera betalningar från alla större debet- och kreditkort. PayPal erbjuder ytterligare bekvämlighet utan extra ansträngning eftersom även kunder som inte har något PayPal-konto kan betala för sina inköp med PayPal.

>[!NOTE]
>
>Du kan inte ha flera PayPal-metoder aktiverade i butiken åt gången, förutom PayPal Express Checkout. PayPal Express Checkout kan användas med andra PayPal-betalningsmetoder, förutom PayPal Payments Standard. Om du ändrar betalningslösningar är den föregående metoden inaktiverad.

### PayPal Express-kassan

[PayPal Express-kassan](paypal-express-checkout.md)

### Betalningslösningar för allt-i-ett-betalning från PayPal

I USA erbjuder PayPal följande PCI-kompatibla lösningar för att uppfylla behoven i ditt växande företag.

- [Avancerade PayPal-betalningar](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal Payments Standard](paypal-payments-standard.md)

![PayPal allt-i-ett-betalningslösningar](./assets/paypal-all-in-one.png){width="600" zoomable="yes"}

### Betalningsgateways för PayPal

En betalningstjänst är en handelstjänst som tillhandahålls av en leverantör av e-handelsapplikationstjänster som godkänner kreditkortsbehandling eller behandling av direktbetalningar. De fungerar som mellanhänder mellan kunder och banker.

Betalningsgatewayar finns tillgängliga online och offline. Betalningar kan accepteras via telefon, online eller via en mobilapp. Transaktionen skickas till tjänsteleverantörens behandlingssystem och skickas sedan till kundens bank för verifiering och bekräftelse. Om det verifieras får handlaren betalningen utan att ha direktkontakt med kundens bankkonto.

Det finns två typer av betalningsgateways - direkt och på webben.

- Med direktbetalningsgatewayar kan användare ange sina kortuppgifter på butikens webbplats.
- Betalningsgateways på värdbasis omdirigerar användare till en värdbaserad betalningssida, utanför butikens webbplats.

Betalningsgatewayen tillhandahåller säkerhet och skydd för alla parter som deltar i en transaktion.

PayPal erbjuder två betalningsgatewaylösningar för ditt företag. Du kan låta PayPal vara värd för din utcheckning på sin säkra betalningswebbplats, eller så kan du ta kontroll över hela betalningsupplevelsen med en anpassningsbar lösning.

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [Länk till PayPal-betalningsflöde](paypal-payflow-link.md)

![Ställ in PayPal-betalningsgateways](./assets/paypal-payment-gateway.png){width="600" zoomable="yes"}

## Hanteringsfilter för PayPal-bedrägeri

Hanteringsfilter för PayPal-bedrägeri gör det enklare att upptäcka och besvara bedrägliga transaktioner och kan konfigureras att flagga, hålla kvar för granskning eller neka riskabla betalningar. Åtgärder som rör handel [orderstatus](order-status.md) värden ändrade enligt inställningarna för bedrägerifiltret:

| Åtgärd | Resultat |
| --- | --- |
| [!UICONTROL Review] | Den misstänkta ordern får status _Betalningsgranskning_ när ordern placeras. Du kan granska ordern och godkänna eller avbryta betalningen i Admin eller på PayPal-sidan. När du klickar **[!UICONTROL Accept Payment]** eller **[!UICONTROL Deny Payment]** skapas inga nya transaktioner för ordern. <br/><br/>Om du ändrar status för transaktionen på PayPal-webbplatsen måste du klicka på **[!UICONTROL Get Payment Update]** på sidan Order (Beställning) i Admin för att tillämpa ändringarna. Klicka **[!UICONTROL Accept Payment]** eller **[!UICONTROL Deny Payment]** används de ändringar som gjorts på PayPal-platsen. |
| [!UICONTROL Deny] | Den misstänkta ordern kan inte utföras av kunden eftersom motsvarande transaktion avvisas av PayPal. <br/><br/>Om du vill neka betalningen från administratören klickar du på **[!UICONTROL Deny Payment]** i det övre högra hörnet på sidan. Orderstatusen ändras till `Canceled`, transaktionen återförs och medel frisläppas på kundkontot. Motsvarande information läggs till i _[!UICONTROL Comments History]_i ordervyn. |
| [!UICONTROL Flag] | Den misstänkta ordern får statusen `Processing` när den monteras. Motsvarande transaktion är markerad med en flagga i listan över handelskontotransaktioner. |

{style="table-layout:auto"}

## PayPal-lösningar per land

| Land | Betalningslösning för PayPal |
|--- |--- |
| Australien | [!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Pro Hosted Solution]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Kanada | [!DNL PayPal Website Payments Standard]<br/>[!DNL PayPal Website Payments Pro]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) (inkluderar Express Checkout)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Frankrike | [!DNL PayPal Integral Evolution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Tyskland | [[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Hongkong SAR China | [!DNL PayPal Website Payments Pro Hosted Solution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Italien | [!DNL PayPal ProPay]<br/>[[!DNL Pal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Japan | [!DNL PayPal Website Payments Plus]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Nya Zeeland | [[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Spanien | [!DNL PayPal Pasarela Integral]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Förenade kungariket | [!DNL PayPal Payments Pro Hosted Solution] (inkluderar Express Checkout)<br/>[[!DNL PayPal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Amerikas förenta stater | [[!DNL PayPal Payments Advanced]](paypal-payments-advanced.md) (inkluderar Express Checkout)<br/>[[!DNL PayPal Payments Pro]](paypal-payments-pro.md) (inkluderar Express Checkout)<br/>[[!DNL PayPal Payments Standard+]](paypal-payments-standard.md)<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md) (inkluderar Express Checkout)<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) (inkluderar Express Checkout)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |

{style="table-layout:auto"}

### Andra länder

PayPal Express Checkout och PayPal Website Payments Standard är tillgängliga i följande länder:

- Argentina
- Österrike
- Belgien
- Brasilien
- Bulgarien
- Chile
- Costa Rica
- Cypern
- Tjeckien
- Danmark
- Dominikanska republiken
- Ecuador
- Estland
- Finland
- Franska Guyana
- Gibraltar
- Grekland
- Guadeloupe
- Ungern
- Island
- Indien
- Indonesien
- Irland
- Israel
- Jamaica
- Lettland
- Liechtenstein
- Litauen
- Luxemburg
- Malaysia
- Malta
- Martinique
- Mexico
- Nederländerna
- Norge
- Filippinerna
- Polen
- Portugal
- Réunion
- Rumänien
- San Marino
- Singapore
- Slovakien
- Slovenien
- Sydafrika
- Sydkorea
- Sverige
- Schweiz
- Taiwan
- Thailand
- Turkiet
- Förenade Arabemiraten
- Uruguay
- Venezuela
- Vietnam


[1]: https://manager.paypal.com/
[2]: https://developer.paypal.com/docs/payflow/payflow-gateway/
[3]: https://www.paypal.com/us/business/buy-now-pay-later
