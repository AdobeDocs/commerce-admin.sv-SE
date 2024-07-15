---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL PayPal Payments Pro]'
description: Granska konfigurationsinställningarna i avsnittet [!UICONTROL PayPal Payments Pro] på sidan [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] i Commerce Admin.
exl-id: 08363002-e1e6-4d5e-9303-44f5ee53ee0a
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1326'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payments Pro]

>[!IMPORTANT]
>
>**PSD2-krav:** <br/>
>Från och med den 14 september 2019 kan europeiska banker avböja betalningar som inte uppfyller kraven för [PSD2](../../getting-started/compliance-payment-services-directive.md). [!DNL PayPal Payments Pro] måste integreras med [!DNL Cardinal Commerce] för att uppfylla PSD2. Mer information finns i [3-D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

{{config}}

## [!UICONTROL Required Settings]

![Nödvändiga inställningar](./assets/payment-methods-paypal-payments-pro-required.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Webbplats | (Valfritt) Alla e-postadresser som är kopplade till ditt PayPal-handelskonto. E-postadresser är skiftlägeskänsliga och måste exakt matcha adresserna som finns på ditt konto. |
| [!UICONTROL Partner] | Webbplats | Ditt PayPal Partner-ID, om tillämpligt. |
| [!UICONTROL Vendor] | Webbplats | Ditt PayPal-användarnamn. |
| Användare | Webbplats | ID för en annan användare på ditt PayPal-konto. |
| [!UICONTROL Password] | Webbplats | Lösenordet som är kopplat till ditt PayPal-handelskonto. |
| [!UICONTROL Test Mode] | Webbplats | När det är aktiverat körs PayPal Payments Pro i en testmiljö. Stäng av testläget när du är redo att börja använda i produktionsläge. Alternativ: `Yes` / `No` |
| [!UICONTROL Use Proxy] | Webbplats | En proxy kan användas för att dirigera om trafik när serverns brandvägg förhindrar direktåtkomst till PayPal-servern. Identifierar, om tillämpligt, den proxyserver som används för att upprätta anslutningen till PayPal-servern. Alternativ: `Yes` / `No` <br/><br/>Om det här alternativet är aktiverat anger du alternativen: <br/>**Proxyvärd** - IP-adressen för proxyvärden. <br/>**Proxyport** - Proxyportens nummer. |
| [!UICONTROL Enable this Solution] | Webbplats | Avgör om PayPal Payments Pro är tillgängligt för dina kunder som betalningsmetod. |
| [!UICONTROL Enable PayPal Credit] | Webbplats | Avgör om PayPal-kredit är tillgängligt för dina kunder som betalningsalternativ. |

{style="table-layout:auto"}

## [!UICONTROL Advertise PayPal Credit]

![Annonsera PayPal-kredit](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Webbplats | Det utgivar-ID som är kopplat till ditt PayPal-kreditkonto. |
| [!UICONTROL Get Publisher ID from PayPal] |  | Hämtar ditt utgivar-ID från PayPal. |
| [!UICONTROL Home Page] | Webbplats | Bestämmer placeringen och storleken på banderollen [!DNL PayPal Credit] på startsidan. Alternativ: <br/>**`Display`**- Avgör om en [!DNL PayPal Credit]-banderoll visas på butikens startsida. Alternativ: `Yes` / `No`<br/>**`Position`** - Bestämmer placeringen av banderollen [!DNL PayPal Credit] på startsidan. Alternativ: Sidhuvud (mitten)/Sidlist (höger) <br/>**`Size`**- Anger storleken på banderollen [!DNL PayPal Credit] på startsidan. Alternativ: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Webbplats | Bestämmer placeringen och storleken på banderollen [!DNL PayPal Credit] på kategorisidor. Alternativ: (samma som för [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | Webbplats | Bestämmer placeringen och storleken på banderollen [!DNL PayPal Credit] på produktsidor. Alternativ: (samma som för [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | Webbplats | Bestämmer placeringen och storleken på banderollen [!DNL PayPal Credit] på kundvagnssidan. Alternativ: (samma som för [!UICONTROL Home Page]) |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings - PayPal Payments Pro]

![Grundinställningar](./assets/payment-methods-paypal-payments-pro-basic-settings.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Title] | Butiksvy | Ett namn som identifierar PayPal Payments Pro som en betalningsmetod vid utcheckning. |
| [!UICONTROL Sort Order] | Butiksvy | Ett tal som bestämmer i vilken ordning PayPal Payments Pro visas när det visas med andra betalningsmetoder i kassan. |
| [!UICONTROL Payment Action] | Webbplats | Bestämmer vilken åtgärd som PayPal ska vidta när en order skickas. Alternativ: <br/>**`Authorization`**- Godkänn köpet, men spärrar pengarna. Beloppet dras inte tillbaka förrän handlaren&quot;fångar&quot; det.<br/>**`Sale`** - Köpbeloppet är auktoriserat och dras omedelbart tillbaka från kundens konto. |
| [!UICONTROL Credit Card Settings] |  |  |
| [!UICONTROL Allowed Credit Cart Types] | Webbplats | Bestämmer vilka kreditkort som är tillgängliga för kunder vid utcheckning. Välj varje kort som stöds. Alternativ: `American Express` (kräver ett extra avtal) / `Visa` / `MasterCard` / `Discover` / `JCB` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![Avancerade inställningar](./assets/paypal-advanced-settings.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Payment Applicable From] | Webbplats | Bestämmer det tillämpliga valet av land. Alternativ: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Webbplats | Identifierar varje land från vilket betalning accepteras. Endast kunder med en faktureringsadress i ett visst land kan göra inköp med den här betalningsmetoden. |
| [!UICONTROL Debug Mode] | Webbplats | Registrerar meddelanden som skickas mellan din butik och betalningssystemet i en loggfil. Alternativ: `Yes` / `No` <br/><br/>**_Obs!_**Loggfilen lagras på servern och är bara tillgänglig för utvecklare. I enlighet med PCI-datasäkerhetsstandarder registreras inte kreditkortsinformation i loggfilen. |
| [!UICONTROL Enable SSL Verification] | Webbplats | Avgör om den säkra kanalen på värden verifieras innan en transaktion utförs. Alternativ: `Yes` / `No` |
| [!UICONTROL Require CVV Entry] | Webbplats | Avgör om kunderna måste ange CVV-koden på baksidan av kreditkortet. Alternativ: `Yes` / `No` |
| **[!UICONTROL CVV and AVS Settings]** |  |  |
| _[!UICONTROL Reject Transaction if:]_ |  |  |
| [!UICONTROL AVS Street Does Not Match] | Webbplats | Anger vilken åtgärd som ska vidtas om tjänsten för adressverifiering fastställer att gatuadressen inte matchar informationen i systemet. Alternativ: `Yes` / `No` |
| [!UICONTROL AVS Zip Does Not Match] | Webbplats | Anger vilken åtgärd som ska vidtas om adressverifieringstjänsten fastställer att postnumret inte matchar informationen i systemet. Alternativ: `Yes` / `No` |
| [!UICONTROL International AVS Indicator Does Not Match] | Webbplats | Anger vilken åtgärd som ska vidtas om adressverifieringstjänsten fastställer att den internationella indikatorn inte matchar informationen i systemet. Alternativ: `Yes` / `No` |
| [!UICONTROL Card Security Code Does Not Match] | Webbplats | Anger vilken åtgärd som ska vidtas om den CVV-säkerhetskod som anges av kunden inte matchar informationen i systemet. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

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

{style="table-layout:auto"}

## [!UICONTROL Frontend Experience Settings]

![Inställningar för Edge Experience](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | Butiksvy | Bestämmer PayPal-logotypen som visas i din butik. Det finns fyra grundläggande format i två storlekar. Alternativ: `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| **[!UICONTROL PayPal Merchant Pages Style]** |  |  |
| [!UICONTROL Page Style] | Butiksvy | Bestämmer utseendet på din PayPal-handlarsida. Tillåtna värden: <br/>**`paypal`**- Använder sidformatet PayPal.<br/>**`primary`** - Använder det sidformat som du identifierade som &quot;primärt&quot; format i din kontoprofil. <br/>**`your_custom_value`**- Använder ett anpassat betalningssidformat som anges i din kontoprofil. |
| [!UICONTROL Header Image URL] | Butiksvy | URL-adressen till bilden som visas i det övre vänstra hörnet på utcheckningssidan. Den maximala storleken är 750 x 90 pixlar. <br/><br/>**_Obs!_**PayPal rekommenderar att bilden lagras på en säker (https) server. Annars kan kundens webbläsare varna för att&quot;sidan innehåller både säkra och osäkra objekt&quot;. |
| [!UICONTROL Header Image Background Color] | Butiksvy | Koden [hexadecimal färg](https://en.wikipedia.org/wiki/Web_colors) med sex tecken för bakgrundsfärgen för sidhuvudet på utcheckningssidan. Du kan ange koden med antingen versaler eller gemener. |
| [!UICONTROL Header Image Border Color] | Butiksvy | Den hexadecimala färgkoden med sex tecken för kanten med två pixlar runt rubriken. |
| [!UICONTROL Page Background Color] | Butiksvy | Den hexadecimala färgkoden på sex tecken för bakgrundsfärgen på den utcheckningssida som visas bakom rubriken och betalningsformuläret. |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings - PayPal Express Checkout]

![Grundinställningar för PayPal Express-utcheckning](./assets/payment-methods-paypal-payments-pro-express-checkout-basic-settings.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Title] | Butiksvy | Ett namn som identifierar betalningsmetoden PayPal Express Checkout under utcheckningen. |
| [!UICONTROL Sort Order] | Butiksvy | Ett tal som bestämmer i vilken ordning som PayPal Express Checkout ska visas när det visas med andra betalningsmetoder vid utcheckning. Ange 0 överst i listan. |
| [!UICONTROL Payment Action] | Webbplats | Bestämmer vilken åtgärd som PayPal ska utföra när den tar emot en order. Alternativ: <br/>**`Authorization`**- Godkänn köpet, men spärrar pengarna. Beloppet dras inte tillbaka förrän handlaren&quot;fångar&quot; det.<br/>**`Sale`** - Köpbeloppet är auktoriserat och dras omedelbart tillbaka från kundens konto. <br/>**`Order`**- Representerar ett avtal med PayPal som tillåter att handlaren kan hämta ett eller flera belopp upp till den beställda summan från kundens köpkonto inom en angiven tidsperiod. Det kan vara upp till 29 dagar. En eller flera fakturor måste genereras från Commerce Admin för att pengarna ska kunna hämtas. |
| [!UICONTROL URL Display on Product Details Page] | Butiksvy | Avgör om knappen&quot;Checka ut med PayPal&quot; visas på produktsidor. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL PayPal Express Checkout - Advanced Settings]

![Avancerade inställningar för PayPal Express-utcheckning](./assets/payment-methods-paypal-payments-pro-express-checkout-advanced-settings.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | Butiksvy | Avgör om PayPal Express Checkout visas som ett betalningsalternativ i kundvagnen. Alternativ: `Yes` (PayPal rekommenderar det här alternativet) / `No` |
| [!UICONTROL Payment Action Applicable From] | Webbplats | Anger intervallet för det tillämpliga landsvalet. Alternativ: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Webbplats | Identifierar varje land från vilket betalning accepteras. Endast kunder med en faktureringsadress i ett visst land kan göra inköp med den här betalningsmetoden. |
| [!UICONTROL Debug Mode] | Webbplats | Registrerar meddelanden som skickas mellan din butik och PayPal-betalningssystemet i en loggfil. Alternativ: `Yes` / `No` <br/><br/>**_Obs!_**Loggfilen lagras på servern och är bara tillgänglig för utvecklare. I enlighet med PCI-datasäkerhetsstandarder registreras inte kreditkortsinformation i loggfilen. |
| [!UICONTROL Enable SSL Verification] | Webbplats | Aktiverar verifiering av värdsäkerhetscertifikatet. Alternativ: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Webbplats | Visar en fullständig sammanfattning av radobjekten från kundens kundvagn på PayPal-webbplatsen. Alternativ: `Yes` / `No` |
| [!UICONTROL Skip Order Review Step] | Webbplats | Avgör om kunderna kan slutföra transaktionen från PayPal-webbplatsen eller måste återvända till din butik och slutföra ordergranskningssteget innan ordern skickas. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}
