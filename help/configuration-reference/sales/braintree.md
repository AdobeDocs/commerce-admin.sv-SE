---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL Braintree]'
description: Granska konfigurationsinställningarna för [!UICONTROL Braintree] i [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] sidan för Commerce Admin.
exl-id: cf08bc4d-8d88-45e7-af71-f1ff90023766
feature: Configuration, Payments
source-git-commit: 1f84bf9ab20aeccacf56eab396b2778140964d17
workflow-type: tm+mt
source-wordcount: '2330'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Braintree]

>[!IMPORTANT]
>
>**Commerce 2.4-migrering:**<br/>
>För tidigare versioner av Adobe Commerce och Magento Open Source än 2.4.0 rekommenderades att handlare installerar och konfigurerar det officiella tillägget för betalningsintegration för Braintree från [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=braintree) för att ersätta kärnintegreringen. Från och med 2.4.0 ingår nu tillägget i kärnversionen.
><br/><br/>
>Vid migrering till Commerce 2.4 måste handlare avinstallera det tillägg som distribueras på Marketplace (`paypal/module-braintree` eller `gene/module-braintree`) och uppdatera alla kodanpassningar för att använda `PayPal_Braintree` namnutrymme i stället för `Magento_Braintree`. Konfigurationsinställningarna från det paketerade tillägget för Commerce och det tillägg som distribueras på Commerce Marketplace bevaras. Betalningar som gjorts med dessa versioner av tillägget fångas, annulleras eller återbetalas som vanligt.
><br/><br/>
>Om du uppgraderar till Commerce 2.4.0 och inte använder det rekommenderade Commerce Marketplace-tillägget i din tidigare version av 2.3.x fungerar inte multiadressfunktionen i version 2.4.0 av Braintree. När en kund väljer _leverera till flera adresser_ visas inte betalningsmetoden för Braintree. Tillägget Commerce Marketplace som tidigare rekommenderades för 2.3.x har detta problem med flera adresser.

{{config}}

{{beta2-updates}}

## [!UICONTROL Basic Braintree Settings]

![Inställningar för grundläggande Braintree](./assets/payment-methods-braintree-basic-config.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Title] | Butiksvy | Standardvärde: `Credit Card` (Braintree) |
| [!UICONTROL Environment] | Butiksvy | Alternativ: `Sandbox` / `Production` |
| [!UICONTROL Payment Action] | Butiksvy | Anger vilken åtgärd Braintree ska vidta när en betalning bearbetas. Alternativ: <br/>**`Authorize`**- Medel på kundens kreditkort godkänns, men överförs inte från kontot. En beställning skapas i din butiksadministratör. Du kan hämta försäljningen senare och skapa en faktura.<br/>**`Intent Sale`** (tidigare `Authorize and Capture` i tidigare versioner) - Medel på kundens kreditkort godkänns och hämtas av Braintree, och en order och faktura skapas i din butiksadministratör. |
| [!UICONTROL Sandbox Merchant ID] | Butiksvy | Detta är den unika identifieraren för hela sandlådegatewaykontot. Kallas även _offentligt ID_ eller _produktions-ID_&#x200B;är ditt handlar-ID annorlunda för din produktion och dina sandlådegateways. Det här fältet visas när _[!UICONTROL Environment]_fältet är inställt på `Sandbox`. |
| [!UICONTROL Sandbox Public Key] | Butiksvy | Detta är din användarspecifika, offentliga identifierare som begränsar åtkomsten till krypterade data. Varje användare som är associerad med din Braintree-gateway i Sandbox har en egen offentlig sandlådenyckel. Det här fältet visas när _[!UICONTROL Environment]_fältet är inställt på `Sandbox`. |
| [!UICONTROL Sandbox Private Key] | Butiksvy | Detta är din användarspecifika, privata identifierare som begränsar åtkomsten till krypterade data. Varje användare som är associerad med din Braintree-gateway i Sandbox har sin egen privata nyckel för sandlådan. Det här fältet visas när _[!UICONTROL Environment]_fältet är inställt på `Sandbox`. |
| [!UICONTROL Merchant ID] | Butiksvy | Detta är den unika identifieraren för hela gateway-kontot, inklusive de flera handlarkonton som kan finnas i din gateway. Kallas även _offentligt ID_ eller _produktions-ID_&#x200B;är ditt handlar-ID annorlunda för din produktion och dina sandlådegateways. Det här fältet visas när _[!UICONTROL Environment]_fältet är inställt på `Production`. |
| [!UICONTROL Public Key] | Butiksvy | Detta är din användarspecifika, offentliga identifierare som begränsar åtkomsten till krypterade data. Varje användare som är kopplad till din Braintree-gateway har sin egen offentliga nyckel. Det här fältet visas när _[!UICONTROL Environment]_fältet är inställt på `Production`. |
| [!UICONTROL Private Key] | Butiksvy | Detta är din användarspecifika, privata identifierare som begränsar åtkomsten till krypterade data. Varje användare som är kopplad till din Braintree-gateway har sin egen privata nyckel. Det här fältet visas när _[!UICONTROL Environment]_fältet är inställt på `Production`. |
| [!UICONTROL Enable Card Payments] | Webbplats | Avgör om betalningsmetoden för kreditkort på Braintree är tillgänglig för dina kunder som betalningsmetod. Alternativ: `Yes` / `No` |
| [!UICONTROL Enable Vault for Card Payments] | Webbplats | När det här alternativet är aktiverat tillhandahålls säker lagring för kundbetalningsinformation, så att kunderna inte behöver ange sin kreditkortsinformation igen för varje köp. Alternativ: `Yes` / `No` |
| [!UICONTROL Enable Vault CVV Reverification] | Webbplats | När det här alternativet är aktiverat valideras CVV-reglerna som har konfigurerats på ditt Braintree-konto. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Braintree Settings]

![Avancerade inställningar för Braintree](./assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Vault Title] | Webbplats | En beskrivande rubrik för din referens som identifierar valvet där kundkortsinformationen lagras. |
| [!UICONTROL Merchant Account ID] | Webbplats | Det konto-ID för handelskonto som ska associeras med transaktioner från Braintree från den här webbplatsen. Om inget anges används standardhandelskontot från ditt Braintree. |
| [!UICONTROL Skip Fraud Checks on Admin Orders] | Webbplats | Förhindrar att transaktionen skickas för utvärdering som en del av [!DNL Advanced Fraud Tools] kontroller, på beställningar som gjorts via administratören endast när den är inställd på `Yes`.<br/>Alternativ: `Yes` / `No` |
| [!UICONTROL Bypass Fraud Protection Threshold] | Webbplats | `Advanced Fraud Protection` Kontroller ignoreras när tröskelvärdet uppnås eller överskrids. Om du lämnar fältet tomt inaktiveras det här alternativet. |
| [!UICONTROL Debug] | Webbplats | Avgör om kommunikation mellan Braintree-systemet och din butik registreras i en loggfil. Alternativ: `Yes` / `No` |
| [!UICONTROL CVV Verification] | Webbplats | Avgör om kunderna måste ange den tresiffriga säkerhetskoden från baksidan av ett kreditkort. Alternativ: `Yes` / `No` |
| [!UICONTROL Send Card Line Items] | Webbplats | Skicka vagnsradobjekten för alla betalningsmetoder. Alternativ: `Yes` / `No` |
| [!UICONTROL Credit Card Types] | Webbplats | Anger varje kreditkort som du godkänner som betalning via Braintree. Tryck och håll `Ctrl` (eller `Command` på Mac) för att välja en kombination av kort. Alternativ: `American Express` / `Visa` / `MasterCard` / `Discover` / `JCB` / `Diners` / `Maestro International` |
| [!UICONTROL Sort Order] | Webbplats | Anger den ordning som Braintree visas med andra betalningsmetoder vid utcheckning. |

## [!UICONTROL Braintree Webhooks Settings]

![Webhooks-inställningar för Braintree](./assets/payment-methods-braintree-webhooks-config.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Webhook] | Webbplats | För att möjliggöra webbokrosfunktionaliteten för bedrägeriskydd gör ACH-betalningar och lokala betalningsmetoder. Alternativ: `Yes` / `No` |
| [!UICONTROL Fraud Protection URL] | Webbplats | Lägg till den här URL-adressen i ditt Braintree-konto som [!UICONTROL Webhook Destination URL]. **Denna URL måste vara säker och allmänt tillgänglig.** |
| [!UICONTROL Fraud Protection Approve Order Status] | Webbplats | När bedrägeriskyddet har godkänts av Braintree tilldelas den valda orderstatusen till handelsordern. Den här statusen används för att uppdatera status för den order där betalningsmetoden ACH används och när den flyttas till `SETTLED` i Braintree. |
| [!UICONTROL Fraud Protection Reject Order Status] | Webbplats | När bedrägeriskyddet avvisas av Braintree tilldelas den valda orderstatusen till handelsordern. Den här statusen används för att uppdatera status för den order där betalningsmetoden ACH används och när `SETTLEMENT` är `DECLINED` i Braintree. |

{style="table-layout:auto"}

## [!UICONTROL Country Specific Settings]

![Inställningar för land](./assets/payment-methods-braintree-country-specific-config.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Payment from Applicable Countries] | Webbplats | Avgör om du godkänner betalningar som har bearbetats av Braintree från alla länder, eller endast vissa länder. Alternativ: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Webbplats | Om tillämpligt, identifierar de specifika länder från vilka du godkänner betalningar som bearbetats av Braintree. |
| [!UICONTROL Country Specific Credit Card Types] | Webbplats | Identifierar de kreditkort som accepteras per land för betalningar som behandlas av Braintree. En post sparas för varje land. Alternativ: <br/>**`Country`**- Välj land.<br/>**`Allowed Card Types`** - Välj varje kreditkort som godkänts från landet som betalning via Braintree. <br/>**`Add`**- Lägg till en rad som tillåter kreditkort för ett annat land.<br/>**`Action`** - Tar bort posten med tillåtna kreditkort för landet. |

{style="table-layout:auto"}

## [!UICONTROL ACH through Braintree]

![ACH through Braintree](./assets/payment-methods-braintree-ach-config.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled ACH Direct Debit] | Webbplats | Bestämmer om [!DNL ACH Direct Debit] ingår som betalningsmetod via Braintree. Alternativ: `Yes` / `No` |
| [!UICONTROL Sort Order] | Webbplats | Bestämmer ordningen som [!DNL ACH Direct Debit] visas med andra betalningsmetoder vid utcheckning. |

{style="table-layout:auto"}

## [!UICONTROL Apple Pay through Braintree]

![Apple Pay via Braintree](./assets/payment-methods-braintree-applepay-config.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable ApplePay through Braintree] | Webbplats | Avgör om Apple Pay inkluderas som betalningsmetod via Braintree. Alternativ: `Yes` / `No` <br/><br/> Domänen måste vara [har verifierats i Braintree först](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3). |
| [!UICONTROL Payment Action] | Webbplats | Anger vilken åtgärd Braintree ska vidta när en betalning bearbetas. Alternativ: <br/>**`Authorize`**- Medel på kundkortet godkänns, men överförs inte från kundens konto. En beställning skapas i din butiksadministratör. Du kan hämta försäljningen senare och skapa en faktura.<br/>**`Intent Sale`** - Medel på kundkortet godkänns och hämtas av Braintree, och en order och faktura skapas i din butiksadministratör. **_Obs!_** Det här var `Authorize and Capture` i 2.3.x och tidigare versioner. |
| [!UICONTROL Merchant Name] | Butiksvy | Etikett som visas för kunder på ApplePay-popup-menyn. |
| [!UICONTROL Sort Order] | Webbplats | Bestämmer i vilken ordning Apple Pay ska listas med andra betalningsmetoder vid utcheckning. |

{style="table-layout:auto"}

## [!UICONTROL Local Payment Methods]

![Lokala betalningsmetoder](./assets/payment-methods-braintree-local-payment-config.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled Local Payment Methods] | Webbplats | Avgör om lokal betalningsmetod ingår som betalningsmetod via Braintree. Alternativ: `Yes` / `No` |
| [!UICONTROL Title] | Webbplats | Etikett som visas i avsnittet betalningssätt för utcheckning. Standardvärde: `Local Payments` |
| [!UICONTROL Allowed Payment Method] | Webbplats | Välj den lokala betalningsmetod som ska aktiveras. Alternativ: `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` (stöds ännu inte) |
| [!UICONTROL Sort Order] | Webbplats | Bestämmer den ordning som den lokala betalningsmetoden listas med andra betalningsmetoder vid utcheckning. |

{style="table-layout:auto"}

>[!NOTE]
>
>Det paketerade Braintree-tillägget stöder inte alla lokala betalningsmetoder som anges i [Braintree utvecklardokumentation](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview). Andra lokala betalningsmetoder håller på att utvecklas och kommer att stödjas i framtida versioner.

## [!UICONTROL GooglePay through Braintree]

![GooglePay via Braintree](./assets/payment-methods-braintree-googlepay-config.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled GooglePay through Braintree] | Webbplats | Bestämmer om [!DNL Google Pay] Betalning ingår som betalningsmetod via Braintree. Alternativ: `Yes` / `No` |
| [!UICONTROL Payment Action] | Webbplats | Anger vilken åtgärd Braintree ska vidta när en betalning bearbetas. Alternativ: <br/>**`Authorize`**- Medel på kundkortet godkänns, men överförs inte från kundens konto. En beställning skapas i din butiksadministratör. Du kan hämta försäljningen senare och skapa en faktura.<br/>**`Intent Sale`** - Medel på kundkortet godkänns och hämtas av Braintree, och en order och faktura skapas i din butiksadministratör. **_Obs!_** Det här var `Authorize and Capture` i 2.3.x och tidigare versioner. |
| [!UICONTROL Button Color] | Webbplats | Bestämmer färgen för [!DNL Google Pay] -knappen. Alternativ: `White` / `Black` |
| [!UICONTROL Merchant ID] | Butiksvy | ID från Google måste anges här. |
| [!UICONTROL Accepted Cards] | Webbplats | Välj den typ av kort som en kund kan använda för att beställa med [!DNL Google Pay]. |
| [!UICONTROL Sort Order] | Webbplats | Bestämmer i vilken ordning Google Pay ska listas med andra betalningsmetoder vid utcheckning. |

{style="table-layout:auto"}

## [!UICONTROL Venmo through Braintree]

![Venmo via Braintree](./assets/payment-methods-braintree-venmo-config.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Venmo through Braintree] | Webbplats | Bestämmer om [!DNL Venmo] ingår som betalningsmetod via Braintree. Alternativ: `Yes` / `No` |
| [!UICONTROL Payment Action] | Webbplats | Anger vilken åtgärd Braintree ska vidta när en betalning bearbetas. Alternativ: <br/>**`Authorize`**- Medel på kundkortet godkänns, men överförs inte från kundens konto. En beställning skapas i din butiksadministratör. Du kan hämta försäljningen senare och skapa en faktura.<br/>**`Intent Sale`** - Medel på kundkortet godkänns och hämtas av Braintree, och en order och faktura skapas i din butiksadministratör. **_Obs!_** Det här var  _Auktorisera och hämta_ i 2.3.x och tidigare versioner. |
| [!UICONTROL Sort Order] | Webbplats | Bestämmer den ordning som Venmo listas med andra betalningsmetoder vid utcheckning. |

{style="table-layout:auto"}

## [!UICONTROL PayPal through Braintree]

![PayPal via Braintree](./assets/payment-methods-braintree-paypal-config.png){width="550" zoomable="yes"}

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable PayPal through Braintree] | Webbplats | Avgör om PayPal inkluderas som betalningsmetod via Braintree. Alternativ: `Yes` / `No` |
| [!UICONTROL Enable PayPal Credit through Braintree] | Webbplats | Avgör om PayPal-kredit inkluderas som betalningsmetod via Braintree. Alternativ: `Yes` / `No`. Det här fältet visas när `Enable PayPal through Braintree` är inställd på `Yes` |
| [!UICONTROL Enable PayPal PayLater through Braintree] | Webbplats | Avgör om PayPal PayLater inkluderas som betalningsmetod via Braintree. Alternativ: `Yes` / `No`. Det här fältet visas när `Enable PayPal through Braintree` är inställd på `Yes` |
| [!UICONTROL Title] | Butiksvy | Etiketten som identifierar PayPal via Braintree till kunder vid utcheckning. Standardvärde: `PayPal` |
| [!UICONTROL Vault Enabled] | Webbplats | När det här alternativet är aktiverat tillhandahålls säker lagring för kundbetalningsinformation, så att kunderna inte behöver ange sin PayPal-information på nytt för varje köp. Alternativ: `Yes` / `No` |
| [!UICONTROL Sort Order] | Webbplats | Ett tal som avgör i vilken ordning PayPal via Braintree visas med andra betalningsmetoder vid utcheckning. |
| [!UICONTROL Override Merchant Name] | Butiksvy | Ett alternativt namn som kan användas för att identifiera handlaren för varje butiksvy. |
| [!UICONTROL Payment Action] | Webbplats | Bestämmer vilken åtgärd PayPal ska vidta via Braintree när en betalning bearbetas. Alternativ: <br/>**`Authorize`**- Medel på kundkortet godkänns, men överförs inte från kundens konto. En beställning skapas i din butiksadministratör. Du kan hämta försäljningen senare och skapa en faktura.<br/>**`Authorize and Capture`** - Medel på kundkortet godkänns och hämtas av PayPal via Braintree, och en order och faktura skapas i din butiksadministratör. |
| [!UICONTROL Payment from Applicable Countries] | Webbplats | Avgör om du godkänner betalningar som bearbetas av PayPal via Braintree från alla länder, eller bara vissa länder. Alternativ: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Webbplats | Om tillämpligt, identifierar de specifika länder från vilka du godkänner betalningar som bearbetats av Braintree. |
| [!UICONTROL Require Customer's Billing Address] | Webbplats | Avgör om kundens faktureringsadress krävs för att skicka en order. Alternativ: `Yes` / `No` |
| [!UICONTROL Debug] | Webbplats | Avgör om kommunikation mellan PayPal via Braintree-systemet och din butik registreras i en loggfil. Alternativ: `Yes` / `No` |
| [!UICONTROL Display on Shopping Cart] | Webbplats | Avgör om PayPal-knappen visas i dialogrutan [mini cart](../../stores-purchase/cart-configuration.md#mini-cart) och [kundvagn](../../stores-purchase/cart.md) sida. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Styling]

![PayPal-formatering](./assets/payment-methods-braintree-paypal-styling.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Location] | Webbplats | Avgör var PayPal-knappar och meddelanden återges på butiken. Alternativ: `Mini-Cart and Cart Page` / `Checkout Page` / `Product Page` |

{style="table-layout:auto"}

**[!UICONTROL Mini-Cart and Cart Page]**

Alternativet och inställningarna i det här avsnittet varierar beroende på inställningen i _[!UICONTROL Location]_fält.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL PayPal Button Type] | Webbplats | Anger en av tre typer för knappen: `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button` |

**[!UICONTROL PayPal Button]**

Alternativen och inställningarna i det här avsnittet varierar beroende på vilken knapptyp som har valts i dialogrutan _[!UICONTROL PayPal Button Type]_fält.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Show PayPal Button] | Webbplats | Anger platsen för PayPal-knappen på den valda platsen. Alternativ: `Yes` / `No` |
| [!UICONTROL Button Label] | Webbplats | Anger etiketten för PayPal-knappen. Alternativ: `Paypal` / `Checkout` / `Buy Now` / `Pay` |
| [!UICONTROL Color] | Webbplats | Bestämmer färgen på PayPal-knappen. Alternativ: `Blue` / `Black` / `Gold` / `Silver` |
| [!UICONTROL Shape] | Webbplats | Bestämmer formen på PayPal-knappen. Alternativ: `Pill` / `Rectangle` |
| [!UICONTROL Size] | Webbplats | Anger storleken på PayPal-knappen. Alternativ: `Medium` / `Large` / `Responsive` |

{style="table-layout:auto"}

**[!UICONTROL PayLater Messaging]**

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Show PayLater Messaging] | Webbplats | Aktiverar PayLater-meddelanden på den valda platsen. Alternativ: `Yes` / `No`. När det här alternativet är aktiverat visas PaySenare-meddelanden för tillgängliga erbjudanden ([begränsningar](https://developer.paypal.com/docs/checkout/pay-later/us/)). |
| [!UICONTROL Message Layout] | Webbplats | Bestämmer layouten för PayLater-meddelandet. Alternativ: `Text` / `Flex` |
| [!UICONTROL Logo] | Webbplats | Anger vilken logotyp som används för PayPal-knappen. Alternativ: `Inline` / `Primary` / `Alternative` / `None` |
| [!UICONTROL Logo Position] | Webbplats | Anger logotyppositionen för PayPal-knappen. Alternativ: `Left` / `Right` / `Top` |
| [!UICONTROL Text Color] | Webbplats | Bestämmer textfärgen för PayPal-knappen. Alternativ: `Black` / `White` / `Monochrome` / `Grayscale` |

{style="table-layout:auto"}

När de här alternativen är angivna kan du se förhandsvisningen av PayPal-knapparna och PayLater-meddelandena. Det finns kontroller som du kan använda för att tillämpa inställningarna eller återställa värdena:

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Apply] | Webbplats | Lagrar de valda formatinställningarna för knappar och PayLater-meddelanden och använder dem på den aktuella platsen och den aktuella knapptypen. |
| [!UICONTROL Apply to All Buttons] | Webbplats | Lagrar de valda formatinställningarna för knappar och PayLater-meddelandevärden och använder dem för alla knapptyper och platser. |
| [!UICONTROL Reset to Recommended Defaults] | Webbplats | Returnerar formateringsinställningarna till de rekommenderade standardvärdena för knappar och PayLater-meddelanden och använder dem för alla knapptyper och platser. |

{style="table-layout:auto"}

## Inställningar för 3d-säker verifiering

![Inställningar för säker 3D-verifiering](./assets/payment-methods-braintree-3d-secure-verify-config.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL 3D Secure Verification] | Webbplats | Avgör om en transaktion måste genomgå en extra verifieringsprocess när kunden är registrerad i ett program som _Verifierat av VISA_. Alternativ: `Yes` / `No` |
| [!UICONTROL Always request 3DS] | Webbplats | Challenge the 3D Secure request always for all the transaction. Alternativ: `Yes` / `No` |
| [!UICONTROL Threshold Amount] | Webbplats | Anger det högsta orderbelopp som tillåts för bearbetning på en enda order. Braintree avböjer auktorisering om orderbeloppet överstiger detta tröskelbelopp. |
| [!UICONTROL Verify for Applicable Countries] | Webbplats | Anger de länder där betalning måste verifieras. Alternativ: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Verify for Specific Countries] | Webbplats | I tillämpliga fall, anges de specifika länder från vilka Braintree ska kontrollera betalningen. |

{style="table-layout:auto"}

## [!UICONTROL Dynamic Descriptors]

![Dynamiska beskrivningar](./assets/payment-methods-braintree-dynamic-config.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Name] | Butiksvy | Namnbeskrivningen består av två delar, som avgränsas med en asterisk (*). Den första delen av beskrivningen identifierar företaget eller DBA och den andra delen identifierar produkten. Till exempel: `company*myproduct`  <br/><br/>Längden på delarna Company och Product i beskrivningen kan fördelas på följande sätt, för en kombinerad längd på upp till 22 tecken: <br/>**`Option 1`**- Företag måste innehålla tre tecken / Produkten kan innehålla upp till 18 tecken<br/>**`Option 2`** - Företag måste bestå av sju tecken / Produkten kan innehålla upp till 14 tecken <br/>**`Option 3`**- Företag måste innehålla 12 tecken / Produkten kan innehålla upp till nio tecken |
| [!UICONTROL Phone] | Butiksvy | Telefonbeskrivningen måste innehålla mellan tio och 14 tecken och kan bara innehålla siffror, bindestreck, parenteser och punkter. Exempel: `9999999999` `(999) 999-9999` `999.999.9999` |
| [!UICONTROL URL] | Butiksvy | URL-beskrivningen representerar ditt domännamn och kan innehålla upp till 13 tecken. Exempel: `company.com` |

{style="table-layout:auto"}
