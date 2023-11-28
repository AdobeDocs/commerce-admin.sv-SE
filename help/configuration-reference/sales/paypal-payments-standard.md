---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL PayPal Payments Standard]'
description: Granska konfigurationsinställningarna i [!UICONTROL PayPal Payments Standard] i [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] sidan för Commerce Admin.
exl-id: 846d9b6f-92b9-4610-b894-625f67f4cff8
feature: Configuration, Payments
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '1314'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payments Standard]

>[!IMPORTANT]
>
>**Krav för PSD2:**<br/>
>Från och med den 14 september 2019 kan europeiska banker avböja betalningar som inte uppfyller [PSD2](../../getting-started/compliance-payment-services-directive.md) krav. Ingen åtgärd krävs för [!DNL PayPal Payments Standard] att uppfylla PSD 2 eftersom alla krav hanteras av PayPal.

{{config}}

## [!UICONTROL Required Settings]

![Nödvändiga inställningar](./assets/payment-methods-paypal-payments-standard-required.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Webbplats | (Valfritt) Alla e-postadresser som är kopplade till ditt PayPal-handelskonto. E-postadresser är skiftlägeskänsliga och måste exakt matcha adresserna som finns på ditt konto. |
| [!UICONTROL Partner] | Webbplats | Ditt PayPal Partner-ID, om tillämpligt. |
| [!UICONTROL Vendor] | Webbplats | Ditt PayPal-användarnamn. |
| Användare | Webbplats | ID för en annan användare på ditt PayPal-konto. |
| [!UICONTROL Password] | Webbplats | Lösenordet som är kopplat till ditt PayPal-handelskonto. |
| [!UICONTROL Test Mode] | Webbplats | När det är aktiverat körs PayPal Payments Pro i en testmiljö. Stäng av testläget när du är redo att börja använda i produktionsläge. Alternativ: `Yes` / `No` |
| [!UICONTROL Use Proxy] | Webbplats | En proxy kan användas för att dirigera om trafik när serverns brandvägg förhindrar direktåtkomst till PayPal-servern. Identifierar, om tillämpligt, den proxyserver som används för att upprätta anslutningen till PayPal-servern. Alternativ: `Yes` / `No` <br/><br/>Om det här alternativet är aktiverat anger du alternativen: <br/>**`Proxy Host`**- IP-adressen för proxyvärden.<br/>**`Proxy Port`** - Proxyportens nummer. |
| [!UICONTROL Enable this Solution] | Webbplats | Avgör om PayPal Payments Pro är tillgängligt för dina kunder som betalningsmetod. |
| [!UICONTROL Enable PayPal Credit] | Webbplats | Avgör om PayPal-kredit är tillgängligt för dina kunder som betalningsalternativ. |

{:style=&quot;table-layout:auto&quot;}

## Annonsera PayPal Credit

![Annonsera PayPal Credit](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Webbplats | Det utgivar-ID som är kopplat till ditt PayPal-kreditkonto. |
| [!UICONTROL Get Publisher ID from PayPal] |  | Hämtar ditt utgivar-ID från PayPal. |
| [!UICONTROL Home Page] | Webbplats | Bestämmer positionen och storleken för [!DNL PayPal Credit] banner på startsidan. Alternativ: <br/>**`Display`**- Bestämmer om en [!DNL PayPal Credit] bannern visas på butikens hemsida. Alternativ: `Yes` / `No`<br/>**`Position`** - Bestämmer positionen för [!DNL PayPal Credit] banner på startsidan. Alternativ: `Header (center)` / `Sidebar (right)` <br/>**`Size`**- Anger storleken på [!DNL PayPal Credit] banner på startsidan. Alternativ: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Webbplats | Bestämmer positionen och storleken för [!DNL PayPal Credit] på kategorisidor. Alternativ: (samma som [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | Webbplats | Bestämmer positionen och storleken för [!DNL PayPal Credit] banner på produktsidor. Alternativ: (samma som [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | Webbplats | Bestämmer positionen och storleken för [!DNL PayPal Credit] banner on cart page. Alternativ: (samma som [!UICONTROL Home Page]) |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Basic Settings - PayPal Payments Standard]

![Grundinställningar](./assets/paypal-standard-basic-settings.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Title] | Butiksvy | Ett namn som identifierar PayPal Payments Pro som en betalningsmetod vid utcheckning. |
| [!UICONTROL Sort Order] | Butiksvy | Ett tal som bestämmer i vilken ordning PayPal Payments Pro visas när det visas med andra betalningsmetoder i kassan. |
| [!UICONTROL Payment Action] | Webbplats | Bestämmer vilken åtgärd som PayPal ska vidta när en order skickas. Alternativ: <br/>**`Authorization`**- Godkänner köpet, men spärrar pengarna. Beloppet dras inte tillbaka förrän handlaren&quot;fångar&quot; det.<br/>**`Sale`** - Köpbeloppet godkänns och dras omedelbart tillbaka från kundens konto. |
| [!UICONTROL Credit Card Settings] |  |  |
| [!UICONTROL Allowed Credit Cart Types] | Webbplats | Bestämmer vilka kreditkort som är tillgängliga för kunder vid utcheckning. Välj varje kort som stöds. Alternativ: `American Express` (kräver ett extra avtal) / `Visa` / `MasterCard` / `Discover` / `JCB` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Advanced Settings]

![Avancerade inställningar](./assets/payment-methods-paypal-payment-standard-advanced.png)<!-- zoom -->

| Fält | Omfång | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | Butiksvy | Avgör om PayPal Express Checkout visas som ett betalningsalternativ i kundvagnen. Alternativ: `Yes` (rekommenderas) / `No` |
| [!UICONTROL Payment Action Applicable From] | Webbplats | Anger intervallet för det tillämpliga landsvalet. Alternativ: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Webbplats | Identifierar varje land från vilket betalning accepteras. Endast kunder med en faktureringsadress i ett visst land kan göra inköp med den här betalningsmetoden. |
| [!UICONTROL Debug Mode] | Webbplats | Registrerar meddelanden som skickas mellan din butik och PayPal-betalningssystemet i en loggfil. Alternativ: `Yes` / `No` <br/><br/>**_Obs!_**Loggfilen lagras på servern och är bara tillgänglig för utvecklare. I enlighet med PCI-datasäkerhetsstandarder registreras inte kreditkortsinformation i loggfilen. |
| [!UICONTROL Enable SSL Verification] | Webbplats | Aktiverar verifiering av värdsäkerhetscertifikatet. Alternativ: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Webbplats | Visar en fullständig sammanfattning av radobjekten från kundens kundvagn på PayPal-webbplatsen. Alternativ: `Yes` / `No` |
| [!UICONTROL Transfer Shipping Options] | Webbplats | Inkluderar upp till tio leveransalternativ på PayPal-sajten. Alternativ: `Yes` / `No` |
| [!UICONTROL Shortcut Buttons Flavor] | Butiksvy | Bestämmer vilken typ av bild som används för PayPal-accepteringsknappen. Alternativ: <br/>**`Dynamic`**- (Rekommenderas) Visar en bild som kan ändras dynamiskt från PayPal-servern.<br/>**`Static`** - Visar en statisk bild som inte kan ändras dynamiskt. |
| [!UICONTROL Enable PayPal Guest Checkout] | Webbplats | Tillåter kunder som inte har PayPal-konton att göra inköp med PayPal Express Checkout. Alternativ: `Yes` / `No` |
| [!UICONTROL Require Customer's Billing Address] | Webbplats | Avgör om kundens faktureringsadress krävs. Alternativ: `Yes` / `No` / `For Virtual Quotes Only` |
| [!UICONTROL Billing Agreement Signup] | Webbplats | Avgör om kunderna kan delta i en [faktureringsavtal](../../stores-purchase/paypal-billing-agreements.md) med din butik. Alternativ: <br/>**`Auto`**- Kunden kan registrera sig för ett faktureringsavtal under Express Checkout.<br/>**`Ask Customer`** - Kunden tillfrågas om de vill registrera sig för ett faktureringsavtal. <br/>**`Never`**- Kunderna erbjuds inte möjligheten att registrera sig för ett faktureringsavtal. |
| [!UICONTROL Skip Order Review Step] | Webbplats | Avgör om kunderna kan slutföra transaktionen från PayPal-webbplatsen eller måste återvända till din butik och slutföra ordergranskningssteget innan ordern skickas. Alternativ: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Billing Agreement Setting]

![Inställningar för faktureringsavtal](./assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png)<!-- zoom -->

| Fält | Omfång | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webbplats | När det här alternativet är aktiverat visas faktureringsavtal som ett betalningsalternativ vid utcheckning. Alternativ: `Yes` / `No` |
| [!UICONTROL Title] | Butiksvy | Etiketten för det PayPal-faktureringsavtalsalternativ som visas som ett betalningsalternativ vid utcheckning. |
| [!UICONTROL Sort Order] | Butiksvy | Bestämmer i vilken ordning faktureringsavtal visas med andra betalningsmetoder vid utcheckning. |
| [!UICONTROL Payment Action] | Webbplats | Avgör hur PayPal hanterar transaktionen: Alternativ: <br/>**`Authorization`**- Godkänner köpet, men spärrar pengarna. Beloppet dras inte tillbaka förrän handlaren&quot;fångar&quot; det.<br/>**`Sale`** - Köpbeloppet godkänns och dras omedelbart tillbaka från kundens konto. |
| [!UICONTROL Payment Applicable From] | Webbplats | Anger intervallet för det tillämpliga landsvalet. Alternativ: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Webbplats | Identifierar varje land från vilket betalning accepteras. Endast kunder med en faktureringsadress i ett visst land kan göra inköp med den här betalningsmetoden. |
| [!UICONTROL Debug Mode] | Webbplats | Registrerar kommunikation med betalningssystemet i en loggfil. Alternativ: `Yes` / `No` <br/><br/>**_Obs!_**Loggfilen lagras på servern och är bara tillgänglig för utvecklare. I enlighet med PCI-datasäkerhetsstandarder registreras inte kreditkortsinformation i loggfilen. |
| [!UICONTROL Enable SSL Verification] | Webbplats | Aktiverar ett verifieringssteg som ser till att transaktionen äger rum över en krypterad SSL-kanal. Alternativ: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Webbplats | När det här alternativet är aktiverat visas en sammanfattning av radobjekt från kundvagnen på din PayPal-betalningssida. Alternativ: `Yes` / `No` |
| [!UICONTROL Allow in Billing Agreement Wizard] | Webbplats | När det här alternativet är aktiverat kan kunderna initiera ett faktureringsavtal från kontrollpanelen för sina kundkonton. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Settlement Report Settings]

![Inställningar för kvittningsrapport](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Login] | Webbplats | Ditt användarnamn som krävs för att logga in på PayPals säkra FTP-server. |
| [!UICONTROL Password] | Webbplats | Ditt lösenord som krävs för att logga in på PayPals säkra FTP-server. |
| [!UICONTROL Sandbox Mode] | Webbplats | När det här alternativet är aktiverat körs rapporter i en testmiljö innan de publiceras i produktionsmiljön. Alternativ: `Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | Webbplats | Den URL där kvittningsrapporter hanteras. Standardvärde: `reports.paypal.com` |
| [!UICONTROL Custom Path] | Webbplats | Sökvägen där kvittningsrapporter sparas på servern. Standardvärde: `/ppreports/outgoing` |
| [!UICONTROL Scheduled Fetching] |  |  |
| [!UICONTROL Enable Automatic Fetching] | Webbplats | När det här alternativet är aktiverat hämtas kvittningsrapporter automatiskt enligt schemat. Alternativ: `Yes` / `No` |
| [!UICONTROL Schedule] | Global | Avgör hur ofta kvittningsrapporter genereras av PayPal. Alternativ: `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | Global | Anger timmen, minuten och sekunden som kvittningsrapporter genereras. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Frontend Experience Settings]

![Frontend Experience Settings](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | Butiksvy | Bestämmer PayPal-logotypen som visas i din butik. Det finns fyra grundläggande format i två storlekar. Alternativ: `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| [!UICONTROL PayPal Merchant Pages Style] |  |  |
| [!UICONTROL Page Style] | Butiksvy | Bestämmer utseendet på din PayPal-handlarsida. Tillåtna värden: <br/>**`paypal`**- Använder sidformatet PayPal.<br/>**`primary`** - Använder det sidformat som du identifierade som &quot;primärt&quot; format i din kontoprofil. <br/>**`your_custom_value`**- Använder ett anpassat betalningssidformat som anges i din kontoprofil. |
| [!UICONTROL Header Image URL] | Butiksvy | URL-adressen till bilden som visas i det övre vänstra hörnet på utcheckningssidan. Den maximala storleken är 750 x 90 pixlar. <br/><br/>**_Obs!_**PayPal rekommenderar att bilden lagras på en säker server (https). Annars kan kundens webbläsare varna för att&quot;sidan innehåller både säkra och osäkra objekt&quot;. |
| [!UICONTROL Header Image Background Color] | Butiksvy | De sex tecknen [hexadecimal färg](https://en.wikipedia.org/wiki/Web_colors) kod för bakgrundsfärgen för sidhuvudet på utcheckningssidan. Du kan ange koden med antingen versaler eller gemener. |
| [!UICONTROL Header Image Border Color] | Butiksvy | Den hexadecimala färgkoden med sex tecken för kanten med två pixlar runt rubriken. |
| [!UICONTROL Page Background Color] | Butiksvy | Den hexadecimala färgkoden på sex tecken för bakgrundsfärgen på den utcheckningssida som visas bakom rubriken och betalningsformuläret. |

{:style=&quot;table-layout:auto&quot;}
