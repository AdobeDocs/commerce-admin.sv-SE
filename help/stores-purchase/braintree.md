---
title: Braintree
description: Lär dig hur du konfigurerar Braintree som en onlinebetalningslösning i din butik.
exl-id: 781b385f-926e-4047-b7da-6f7c090d75d8
feature: Payments
source-git-commit: fcd08ea5d8c3bd498eb4beae41bdf2f078a89f55
workflow-type: tm+mt
source-wordcount: '2625'
ht-degree: 0%

---

# Braintree

Braintree erbjuder en helt anpassningsbar utcheckningsupplevelse med bedrägeriidentifiering och PayPal-integrering. Den har stöd för [!DNL Apple Pay], [!DNL Google Pay], ACH, Venmo och lokala betalningsmetoder. Braintree minskar PCI-kompatibilitetsbördan för handlare eftersom transaktionen äger rum i Braintree-systemet. Integrationen av Braintree-betalningar har utvecklats av [GENE Commerce](https://www.gene.co.uk/gene-braintree-payments/).

>[!NOTE]
>
>Om du uppgraderar till 2.4.x från en tidigare version av Adobe Commerce eller Magento Open Source med tillägget Braintree från Commerce Marketplace installerat, se [2.4 Upgrade notes](#24-upgrade-notes) efter den här sidan.


## Steg 1: Hämta dina inloggningsuppgifter för Braintree

Gå till [Betalningar från Braintree][1] och registrera dig för ett konto.

## Steg 2: Slutför de grundläggande inställningarna

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Payment Methods]**.

   - Om din Commerce-installation har flera webbplatser, butiker eller vyer väljer du **[!UICONTROL Store View]** där konfigurationen gäller.

   - I _[!UICONTROL Merchant Location]_-avsnittet, verifiera att **[!UICONTROL Merchant Country]**är inställt på platsen för ditt företag.

1. Under _[!UICONTROL Recommended Solutions]_, i_[!UICONTROL Braintree Payments] (av [GENE Commerce](https://www.gene.co.uk/gene-braintree-payments/) v4.6.1 - [Versionsinformation](https://support.gene.co.uk/support/solutions/articles/35000228529)_avsnitt, klicka **[!UICONTROL Configure]**.

   ![Konfigurera Braintree](./assets/braintree-payments.png){width="600" zoomable="yes"}

1. För **[!UICONTROL Title]**, anger du en titel som identifierar Braintree som ett betalningsalternativ vid utcheckningen.

1. Ange aktuell funktion **[!UICONTROL Environment]** för Braintree-transaktioner till `Sandbox` eller `Production`

   När du testar konfigurationen i en sandlåda ska du bara använda [kreditkortsnummer][2] som rekommenderas av Braintree. När du är redo att börja producera med Braintree, **[!UICONTROL Environment]** till `Production`.

   ![Inställningar för grundläggande autentiseringsuppgifter](./assets/braintree-settings1.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Payment Action]** till något av följande:

   - `Authorize Only` - Godkänner köpet och spärrar pengarna. Beloppet dras inte tillbaka från kundens bankkonto förrän försäljningen är _fångad_ av handlaren.|
   - `Intent Sale`  - Köpbeloppet godkänns och dras omedelbart tillbaka från kundens konto. **_Obs!_** Detta värde var  _Auktorisera och hämta_ i 2.3.x och tidigare versioner.|

1. Ange **[!UICONTROL Sandbox Merchant ID / Merchant ID]** från ditt Braintree-konto.

1. Ange följande uppgifter från ditt Braintree-konto:

   - **[!UICONTROL Sandbox Public Key / Public Key]**
   - **[!UICONTROL Sandbox Private Key / Private Key]**

   >[!NOTE]
   >
   >Det finns separata fält för båda **(Sandbox and Production)** miljöer och de andra fälten återges baserat på vilken miljö som valts.

1. Innan du sparar konfigurationen klickar du på **[!UICONTROL Validate Credentials]** för att validera dina inloggningsuppgifter.

1. Ange **[!UICONTROL Enable Card Payments]** till `Yes`.

   ![Grundinställningar](./assets/braintree-settings2.png){width="600" zoomable="yes"}

   Om ni vill kunna lagra kundinformation på ett säkert sätt, så att kunderna inte behöver ange den igen varje gång de gör ett köp, ställer ni in **[!UICONTROL Enable Vault for Card Payments]** till `Yes`.

## Steg 3: Slutför de avancerade inställningarna

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Advanced Braintree Settings]** -avsnitt.

   ![Avancerade inställningar](../configuration-reference/sales/assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

1. För **[!UICONTROL Vault Title]**, anger du en beskrivande rubrik för din referens som identifierar valvet där kundkortsinformationen lagras.

1. Ange **[!UICONTROL Merchant Account ID]** från ditt Braintree-konto.

   Om du inte anger vilket handlarkonto som ska användas bearbetar Braintree transaktionen med ditt standardhandlarkonto.

1. Om du vill få en snabbare utcheckning med Express Payment-alternativ i början av utcheckningsprocessen, inklusive PayPal, PayLater, Apple Pay och Google Pay, anger du **[!UICONTROL Enable Checkout Express Payments]** till `Yes`.

1. Om du vill förhindra att transaktionen skickas för utvärdering som en del av Avancerade bedrägeriverktygskontroller anger du på beställningar som gjorts via administratören **[!UICONTROL Skip Fraud Checks on Admin Orders]** till `Yes`.

1. Ange **[!UICONTROL Bypass Fraud Protection Threshold]** så att `Advanced Fraud Protection` Kontroller ignoreras när tröskelvärdet uppnås eller överskrids.

   Om du lämnar fältet tomt inaktiveras det här alternativet.

1. Om du vill att systemet ska spara en loggfil med interaktioner mellan din butik och Braintree anger du **[!UICONTROL Debug]** till `Yes`.

1. Om du vill att kunderna ska ange den tresiffriga säkerhetskoden från baksidan av ett kreditkort anger du **[!UICONTROL CVV Verification]** till `Yes`.

   Om CVV-verifiering används, se till att aktivera AVS och/eller CVV i dialogrutan _Inställningar/bearbetning_ i ditt Braintree-konto.

1. Om du vill skicka varukorgsradobjekten för alla betalningsmetoder anger du **[!UICONTROL Send Card Line Items]** till `Yes`.

1. För **[!UICONTROL Credit Card Types]** väljer du varje kreditkort som du godkänner som betalning via Braintree.

   Om du vill välja flera korttyper håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

1. För **[!UICONTROL Sort Order]** anger du ett nummer som avgör i vilken ordning Braintree visas när det visas med andra betalningsmetoder i kassan.

## Steg 4: Slutför inställningarna för Braintree-webkroken

![Webhooks-inställningar för Braintree](../configuration-reference/sales/assets/payment-methods-braintree-webhooks-config.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enable Webhook]** till `Yes` för att möjliggöra webbokrosfunktionaliteten för bedrägeriskydd, ACH-betalningar och lokala betalningsmetoder.

1. Kopiera URL:en i **[!UICONTROL Fraud Protection URL]** fält och lägg till det på ditt Braintree-konto som _[!UICONTROL Webhook Destination URL]_.

   >[!IMPORTANT]
   >
   >Denna URL måste vara säker och allmänt tillgänglig.

1. Ange **[!UICONTROL Fraud Protection Approve Order Status]** fält för att fastställa när bedrägeriskyddet har godkänts av Braintree.

   Den valda orderstatusen tilldelas handelsordern.

1. Ange **[!UICONTROL Fraud Protection Reject Order Status]** fält som avgör när bedrägeriskyddet avvisas av Braintree.

   Den valda orderstatusen tilldelas handelsordern.

## Steg 5: Slutför de landsspecifika inställningarna

1. Ange **[!UICONTROL Payment from Applicable Countries]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här betalningsmetoden.
   - `Specific Countries` - När du har valt det här alternativet visas _[!UICONTROL Payment from Specific Countries]_visas. Håll ned Ctrl-tangenten (PC) eller Kommando-tangenten (Mac) och markera varje land i listan där kunderna kan göra inköp från din butik.

   ![landsspecifika inställningar](../configuration-reference/sales/assets/payment-methods-braintree-country-specific-config.png){width="600" zoomable="yes"}

1. Så här konfigurerar du **[!UICONTROL Country Specific Credit Card Types]**:

   - Klicka på **[!UICONTROL Add]**.

   - Ange **[!UICONTROL Country]** och välja var **[!UICONTROL Allowed Credit Card Type]**.

   - Upprepa för att identifiera kreditkort som accepteras från varje land.

## Steg 6: Slutför inställningarna för VARJE via Braintree

![ACH through Braintree](../configuration-reference/sales/assets/payment-methods-braintree-ach-config.png){width="600" zoomable="yes"}

1. Om du vill inkludera ACH som ett betalningsalternativ med Braintree anger du **[!UICONTROL Enable ACH Direct Debit]** till `Yes`.

1. Kunderna kan validera sin engångsbetalning med ACH Direct Debit och lagra den för framtida bruk. När de väl har vunnit kan kunderna återanvända VARJE autogiro utan att behöva ange eller autentisera sin betalningsinformation på nytt om detta anges **[!UICONTROL Enable Vault for ACH Direct Debit]** till `Yes`.

1. För **[!UICONTROL Sort Order]** anger du ett nummer som avgör i vilken ordning betalningsalternativet Braintree ACH visas när det visas tillsammans med andra betalningsalternativ under utcheckningen.

## Steg 7: Slutför [!UICONTROL Apple Pay] via Braintree-inställningar

![ApplePay via Braintree-inställningar](../configuration-reference/sales/assets/payment-methods-braintree-applepay-config.png){width="600" zoomable="yes"}

1. Inkludera [!DNL Apple Pay] som ett betalningsalternativ med Braintree, ange **[!UICONTROL Enable ApplePay through Braintree]** till `Yes`.

   Se till att [verifiera ditt domännamn](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3) i ditt Braintree-konto först.

1. Om du vill kunna lagra kundinformation på ett säkert sätt så att kunderna inte behöver ange den igen varje gång de gör ett köp med Apple Pay ställer du in **[!UICONTROL Enable Vault for ApplePay]** till `Yes`.

1. Ange **[!UICONTROL Payment Action]** till något av följande:

   - `Authorize Only` - Godkänner köpet och spärrar pengarna. Beloppet dras inte tillbaka från kundens bankkonto förrän försäljningen är _fångad_ av handlaren.
   - `Intent Sale` - Köpbeloppet godkänns och dras omedelbart tillbaka från kundens konto.

1. För **[!UICONTROL Merchant Name]** anger du text som anger etiketten som visas för kunderna i dialogrutan Apple Pay.

1. För **[!UICONTROL Sort Order]** anger du ett tal för att avgöra i vilken ordning [!DNL Apple Pay] betalningsalternativ visas när de visas tillsammans med andra betalningsalternativ under utcheckningen.

## Steg 8: Slutför inställningarna för lokala betalningsmetoder

1. Om du vill inkludera lokala betalningsmetoder som ett betalningsalternativ med Braintree anger du **[!UICONTROL Enable Local Payment Methods]** till `Yes`.

1. För **[!UICONTROL Title]** anger du texten som ska användas för etiketten som visas i avsnittet betalningsmetod för utcheckning (standardvärde: `Local Payments`).

1. För **[!UICONTROL Fallback Button Text]** anger du den text som ska användas för den knapp som visas på Braintree-reservsidan för att ta kunden tillbaka till webbplatsen (till exempel `Complete Checkout`).

1. För **[!UICONTROL Redirect on Fail]** anger du den URL där kunderna ska omdirigeras när lokala betalningsmetoder avbryts, misslyckas eller stöter på fel. Det ska vara betalningssidan för kassan (till exempel `https://www.domain.com/checkout#payment`).

1. För **[!UICONTROL Allowed Payment Methods]** väljer du den lokala betalningsmetod som ska aktiveras.

   Alternativ: `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` (stöds ännu inte)

   ![Inställningar för lokala betalningsmetoder](../configuration-reference/sales/assets/payment-methods-braintree-local-payment-config.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Det paketerade Braintree-tillägget stöder inte alla lokala betalningsmetoder som anges i [Braintree utvecklardokumentation](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview). Andra lokala betalningsmetoder håller på att utvecklas och kommer att stödjas i framtida versioner.

1. För **[!UICONTROL Sort Order]**, anger du ett nummer för att avgöra i vilken ordning den lokala betalningsmetoden visas när den visas tillsammans med andra betalningsalternativ under utcheckningen.

## Steg 9: Slutför [!DNL Google Pay] via Braintree-inställningar

![Google Pay via Braintree](../configuration-reference/sales/assets/payment-methods-braintree-googlepay-config.png){width="600" zoomable="yes"}

1. Inkludera [!DNL Google Pay] som ett betalningsalternativ med Braintree, ange **[!UICONTROL Enable GooglePay Through Braintree]** till `Yes`.

1. Om du vill kunna lagra kundinformation på ett säkert sätt så att kunderna inte behöver ange den igen varje gång de gör ett köp med Google Pay ställer du in **[!UICONTROL Enable Vault for GooglePay]** till `Yes`.

1. Ange **[!UICONTROL Payment Action]** till något av följande:

   - `Authorize Only` - Godkänner köpet och spärrar pengarna. Beloppet dras inte tillbaka från kundens bankkonto förrän försäljningen är _fångad_ av handlaren.
   - `Intent Sale`  - Köpbeloppet godkänns och dras omedelbart tillbaka från kundens konto.

1. Ange **[!UICONTROL Button Color]** för att bestämma färgen på [!DNL Google Pay] knapp: `White` eller `Black`

1. För **[!UICONTROL Merchant ID]** anger du ditt MerchantID (tillhandahålls av Google).

1. För **[!UICONTROL Accepted Cards]** väljer du den typ av kort som kunden kan använda för att göra en beställning med [!DNL Google Pay].

   Alternativ: `Visa` / `MasterCard` / `AMEX` / `Discover` / `JCB`

1. För **[!UICONTROL Sort Order]** anger du ett tal för att avgöra i vilken ordning [!DNL Google Pay] visas när det visas med andra betalningsalternativ under utcheckningen.

## Steg 10: Slutför inställningarna för Venmo via Braintree

1. Om du vill inkludera Venmo som betalningsalternativ med Braintree anger du **[!UICONTROL Enable Venmo through Braintree]** till `Yes`.

1. Ange **[!UICONTROL Enable Vault for Venmo]** till `Yes` för att kunna använda ett säkert valv för att lagra kundernas Venmo-konto så att kunden inte behöver logga in på sitt Venmo-konto igen för framtida transaktioner.

   ![Venmo via Braintree](../configuration-reference/sales/assets/payment-methods-braintree-venmo-config.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Payment Action]** till något av följande:

   - `Authorize Only` - Godkänner köpet och spärrar pengarna. Beloppet dras inte tillbaka från kundens bankkonto förrän försäljningen är _fångad_ av handlaren.
   - `Intent Sale`  - Köpbeloppet godkänns och dras omedelbart tillbaka från kundens konto.

1. För **[!UICONTROL Sort Order]** anger du ett nummer som avgör i vilken ordning Venmo visas när det visas med andra betalningsalternativ under utcheckningen.

## Steg 11: Slutför inställningarna för PayPal via Braintree

![PayPal via Braintree-inställningar](./assets/braintree-paypal.png){width="550" zoomable="yes"}

1. Om du vill inkludera PayPal som ett betalningsalternativ med Braintree anger du **[!UICONTROL Enable PayPal through Braintree]** till `Yes`.

1. Ange din PayPal via betalningsmetoden Braintree:

   >[!NOTE]
   >
   >Antingen **[!DNL PayPal Credit]** eller **[!DNL PayPal PayLater]** kan aktiveras. Båda metoderna kan inte aktiveras samtidigt.

   - Inkludera [!DNL PayPal Credit] som ett betalningsalternativ med Braintree, ange **[!UICONTROL Enable PayPal Credit through Braintree]** till `Yes`.

     När **Aktivera PayPal via Braintree** är inställd på `Yes`visas bara det här fältet.

     >[!NOTE]
     >
     >PayPal Credit är endast tillgängligt i USA och Storbritannien. PayPal-kredit är inaktiverad om det valda värdet för _[!UICONTROL Merchant Country]_fältet är inte `US` eller `UK`.

   - Inkludera [!DNL PayPal PayLater] som ett betalningsalternativ med Braintree, ange **[!UICONTROL Enable PayPal PayLater through Braintree]** till `Yes`.

     När **[!UICONTROL Enable PayPal PayLater through Braintree]** är inställd på `Yes`visas bara det här fältet.

     Du kan visa PayLater-meddelanden på din webbplats för erbjudanden, som _Betala 3_, vilket ger kunderna möjlighet att betala med tre räntefria månatliga betalningar. Integreringen av Braintree kan visa meddelanden på din webbplats för att marknadsföra den här funktionen. Du kan inte marknadsföra PayLater-erbjudanden med annat innehåll, marknadsföring eller material.

1. För **[!UICONTROL Title]**, anger du en titel som identifierar PayPal-alternativet i Braintree under utcheckningen.

1. Ange **[!UICONTROL Vault Enabled]** till `Yes` för att aktivera användning av ett säkert valv för att lagra kunders PayPal-konto. Vaulterat PayPal-konto kan användas för framtida transaktioner, vilket minskar antalet steg för kunderna.

1. Ange **[!UICONTROL Send Cart Line Items for PayPal]** till `Yes` om du vill skicka radartiklar (orderartiklar) till PayPal tillsammans med presentkort, presentomslutning för artiklar, presentomslutning för order, butikskrediter, leveranser och skatt som radobjekt.

1. För **[!UICONTROL Sort Order]**, anger du ett nummer som avgör i vilken ordning betalningsalternativet Braintree PayPal visas när det visas tillsammans med andra betalningsalternativ under utcheckningen.

1. Att visa ditt handlarnamn på ett annat sätt än det som definieras i din [lagringskonfiguration](../getting-started/store-details.md#store-information)anger du namnet i dialogrutan **[!UICONTROL Override Merchant Name]** så som du vill att det ska visas.

1. Ange **[!UICONTROL Payment Action]** till något av följande:

   - `Authorize Only` - Godkänner köpet och spärrar pengarna. Beloppet dras inte tillbaka från kundens bankkonto förrän försäljningen är _fångad_ av handlaren.
   - `Authorize and Capture` - Köpbeloppet godkänns och dras omedelbart tillbaka från kundens konto.

1. Ange **[!UICONTROL Payment from Applicable Countries]** till något av följande för Braintree-transaktioner som bearbetas av PayPal:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här betalningsmetoden.
   - `Specific Countries` - När du har valt det här alternativet visas _[!UICONTROL Payment from Specific Countries]_visas. Håll ned Ctrl-tangenten (PC) eller Kommando-tangenten (Mac) och markera varje land i listan där kunderna kan göra inköp från din butik.

1. Om du vill att kunderna ska ange en faktureringsadress anger du **[!UICONTROL Require Customer's Billing Address]** till `Yes`.

   >[!NOTE]
   >
   >Den här funktionen måste aktiveras för ditt konto av PayPals tekniska support.

1. Om du vill spara en loggfil med interaktioner mellan din butik och PayPal via Braintree anger du **[!UICONTROL Debug]** till `Yes`.

1. Om du vill visa PayPal-knappen på både mini-kundvagnen och kundvagnssidan anger du **[!UICONTROL Display on Shopping Cart]** till `Yes`.

## Steg 12: Ange formatinställningar

1. För **[!UICONTROL Location]** väljer du var PayPal-knappar och meddelanden ska återges: `Mini-Cart and Cart Page`, `Checkout Page`, eller `Product Page`

   ![Inställningar för PayPal-format](../configuration-reference/sales/assets/payment-methods-braintree-paypal-styling.png){width="600" zoomable="yes"}

### [!UICONTROL Mini-Cart and Cart Page]

Alternativen och inställningarna i det här avsnittet varierar beroende på inställningarna i _[!UICONTROL Location]_fält.

1. Ange **[!UICONTROL PayPal Button Type]** till en av tre knapptyper: `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button`

**[!UICONTROL PayPal Button]**

Alternativen och inställningarna i det här avsnittet varierar beroende på vilken knapptyp som har valts i dialogrutan _[!UICONTROL PayPal Button Type]_fält.

1. Om du vill visa PayPal-knappen på butiken vid den valda platsen anger du **[!UICONTROL Show PayPal Button]** till `Yes`.

1. För **[!UICONTROL Button Label]** markerar du knappetiketten PayPal: `Paypal`, `Checkout`, `Buynow`, eller `Pay`

1. För **[!UICONTROL Color]** väljer du färg för PayPal-knappen: `Blue`, `Black`, `Gold`, eller `Silver`

1. För **[!UICONTROL Shape]** markerar du knappformen PayPal: `Pill` eller `Rectangle`

1. För **[!UICONTROL Size (Deprecated)]** väljer du PayPal-knappens storlek: `Medium`, `Large`, eller `Responsive`

>[!NOTE]
>
>The **[!DNL Size(Deprecated)]** konfigurationsfältet är föråldrat och används inte för att formatera PayPal-knapparna.

**[!UICONTROL PayLater Messaging]**

1. Visa [!DNL PayLater] meddelanden på butiken på den valda platsen, ange **[!UICONTROL Show PayLater Messaging]** till `Yes`.

   Det här meddelandet innehåller information om [!DNL PayLater] meddelanden om tillgängliga erbjudanden ([begränsningar](https://developer.paypal.com/docs/checkout/pay-later/us/)).

1. För **[!UICONTROL Message Layout]** väljer du [!DNL PayLater] meddelandelayout: `Text` eller `Flex`

1. För **[!UICONTROL Logo]** väljer du PayPals logotyp: `Inline`, `Primary`, `Alternative`, eller `None`

1. För **[!UICONTROL Logo Position]** väljer du PayPals logotypposition: `Left`, `Right`, eller `Top`

1. För **[!UICONTROL Text Color]** väljer du [!DNL PayLater] meddelandetextfärg: `Black`, `White`, `Monochrome`, eller `Grayscale`

När de här alternativen är angivna kan du se förhandsvisningen av PayPal-knapparna och PayLater-meddelandena. Det finns kontroller som du kan använda för att tillämpa inställningarna eller återställa värdena:

- Om du vill lagra de valda formatinställningarna för knappar och PayLater-meddelanden och använda dem på den aktuella platsen och den aktuella knapptypen klickar du på **[!UICONTROL Apply]**.

- om du vill lagra de valda formatinställningarna för knappar och PaySenare-meddelandevärden och använda dem på alla knapptyper och platser, klickar du på **[!UICONTROL Apply to All Buttons]**.

- Om du vill återställa formatinställningarna till de rekommenderade standardvärdena för knappar och meddelanden från PaySenare och använda dem på alla knapptyper och platser klickar du på **[!UICONTROL Reset to Recommended Defaults]**.

## Steg 13: Slutför inställningarna för 3D-verifiering

1. Om du vill lägga till ett verifieringssteg för kunder som använder kreditkort som är registrerade i ett verifieringsprogram (till exempel _Verifierat av VISA_), ange **[!UICONTROL 3D Secure Verification]** till `Yes`.

   Under processen kontrolleras transaktionsbeloppet som skickas för verifiering mot det belopp som skickas för auktorisering.

2. Ställ in för att alltid verifiera 3D-säkerhetsbegäran för alla transaktioner **[!UICONTROL Always request 3DS]** till `Yes`.

3. För **[!UICONTROL Threshold Amount]** anger du det minsta orderbelopp som krävs för att utlösa 3D-verifiering.

4. Ange **[!UICONTROL Verify for Applicable Countries]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här betalningsmetoden.
   - `Specific Countries` - När du har valt det här alternativet visas _[!UICONTROL Verify for Specific Countries]_visas. Håll ned Ctrl-tangenten (PC) eller Kommando-tangenten (Mac) och markera varje land i listan där kunderna kan göra inköp från din butik.

   ![Inställningar för 3D-verifiering](../configuration-reference/sales/assets/payment-methods-braintree-3d-secure-verify-config.png){width="600" zoomable="yes"}

## Steg 14: Konfigurera de dynamiska beskrivningarna för Braintree

Följande beskrivningar används för att identifiera inköp på kundkreditkortskontoutdrag. Du kan minska antalet återbetalningar genom att tydligt identifiera det företag som är kopplat till varje köp. Om dynamiska beskrivningar inte är aktiverade för ditt konto kontaktar du supporten för Braintree.

![Dynamiska beskrivningar](../configuration-reference/sales/assets/payment-methods-braintree-dynamic-config.png){width="600" zoomable="yes"}

1. Ange den dynamiska beskrivningen för **[!UICONTROL Name]**, **[!UICONTROL Phone]** och **[!UICONTROL URL]** enligt dessa riktlinjer:

   - **[!UICONTROL Name]** - Namnbeskrivningen består av två delar, som avgränsas med en asterisk (*). Exempel:

     `company*myproduct`

     Den första delen av beskrivningen identifierar företaget eller DBA och den andra delen identifierar produkten. Längden på `company` och `product` delar av beskrivningen kan fördelas på följande sätt, med en sammanlagd längd på upp till 22 tecken.

     **_Tecken i namnbeskrivningen_**

     _Alternativ 1:_ `Company` måste bestå av tre tecken, `Product` kan innehålla upp till 18 tecken

     _Alternativ 2:_ `Company` måste vara sju tecken, `Product` kan innehålla upp till 14 tecken

     _Alternativ 3_: `Company` måste innehålla 12 tecken, `Product` kan innehålla upp till nio tecken

   - **[!UICONTROL Phone]** - Telefonbeskrivningen måste vara 10-14 tecken lång och får endast innehålla siffror, bindestreck, parenteser och punkter. Exempel:

     `9999999999`

     `(999) 999-9999`

     `999.999.9999`

   - **[!UICONTROL URL]** - URL-beskrivningen representerar ditt domännamn och kan innehålla upp till 13 tecken. Exempel:

     `company.com`

1. När konfigurationen för Braintree är klar klickar du på **[!UICONTROL Save Config]**.

## 2.4 Upgrade notes

Från och med Adobe Commerce och Magento Open Source 2.4.0 ingår tillägget Braintree i releasen. Om du migrerar till Commerce 2.4.x från en tidigare version än 2.4.0 som har tillägget Marketplace Braintree installerat måste du avinstallera det tillägget (`paypal/module-braintree` eller `gene/module-braintree`) och uppdatera alla kodanpassningar för att använda `PayPal_Braintree` namnutrymme i stället för `Magento_Braintree`. Konfigurationsinställningarna från huvudtillägget Commerce Braintree Payments och tillägget som distribueras på Commerce Marketplace kvarstår och betalningar som placerats med dessa tidigare versioner kan fortfarande hämtas, annulleras eller återbetalas som vanligt.

[1]: https://www.braintreepayments.com/
[2]: https://developers.braintreepayments.com/reference/general/testing/php
