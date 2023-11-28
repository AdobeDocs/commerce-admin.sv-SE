---
title: PayPal Payments Standard
description: Lär dig hur du konfigurerar PayPal Payments Standard som en onlinebetalningslösning i din butik.
exl-id: b4024dac-34d7-4f1a-ad9d-0fc406194609
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2073'
ht-degree: 0%

---

# PayPal Payments Standard

[PayPal Payments Standard][4] är det enklaste sättet att acceptera betalningar online. Du kan erbjuda dina kunder en smidig betalning både med kreditkort och PayPal genom att lägga till en utcheckningsknapp i din butik.

>[!NOTE]
>
>För handlare utanför USA anropas den _PayPal Web Site Payments Standard_.

Med PayPal Payments Standard kan du svepa kreditkort på mobila enheter. Det kostar inget och du får betalt via eBay. Följande kreditkort stöds: Visa, MasterCard, Discover och American Express. Dessutom kan kunderna betala direkt från sina PayPal-konton. PayPal Payments Standard finns i alla länder i PayPals globala referenslista.

>[!IMPORTANT]
>
>**Krav för PSD2:** <br/>
>Från och med den 14 september 2019 kan europeiska banker avböja betalningar som inte uppfyller [PSD2](../getting-started/compliance-payment-services-directive.md) krav. Ingen åtgärd krävs för att PayPal Payments Standard ska uppfylla PSD2 eftersom alla krav hanteras av PayPal.

## Krav för handlare

- [PayPal Business Account][1]

## Arbetsflöde för kassor

För kunder är PayPal Payments Standard en enstegsprocess om kreditkortsinformationen på deras personliga PayPal-konton är aktuell.

1. **Kundens platsorder** - Kunden klickar/trycker på _Betala nu_ för att slutföra köpet.

1. **PayPal bearbetar transaktionen** - Kunden omdirigeras till PayPal-webbplatsen för att slutföra transaktionen.

## Ställ in PayPal Payments Standard

>[!NOTE]
>
>PayPal Payments Standard kan inte användas samtidigt med någon annan PayPal-metod, inklusive Express Checkout. Om du ändrar betalningslösningar inaktiveras den som användes tidigare.

>[!TIP]
>
>Klicka **[!UICONTROL Save Config]** när som helst för att spara förloppet.

### Steg 1: Påbörja konfigurationen

Den här installationsmetoden förutsätter att du har ett befintligt PayPal-konto.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Payment Methods]**.

1. Om din Commerce-installation har flera webbplatser, butiker eller vyer anger du **[!UICONTROL Store View]** till butiksvyn där du vill använda den här konfigurationen.

1. I _[!UICONTROL Merchant Location]_väljer du **[!UICONTROL Merchant Country]**där företaget finns.

   Den här inställningen bestämmer valet av PayPal-lösningar som visas i konfigurationen.

   ![Handelsland](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Expandera **[!UICONTROL PayPal All-in-One Payment Solutions]** och klicka **[!UICONTROL Configure]** for **[!UICONTROL Payments Standard]**.

   ![PayPal Payments Standard](./assets/paypal-payments-standard.png){width="700" zoomable="yes"}

### Steg 2: Aktivera och ansluta ditt PayPal-konto

![Konfiguration av PayPal Payments Standard](./assets/paypal-payments-display.png){width="600" zoomable="yes"}

1. Koppla ditt konto för test eller produktion:

   - Om du vill testa (utveckla) läget klickar du på **[!UICONTROL Sandbox Credentials]** och ange [PayPal, sandlåda][3] autentiseringsuppgifter.
   - För produktionsläge klickar du på **[!UICONTROL Connect with PayPal]** och ange autentiseringsuppgifter för produktionskontot.

   När anslutningen har verifierats kan du fortsätta.

1. Ange **[!UICONTROL Enable this Solution]** till `Yes`.

1. Om du vill erbjuda [PayPal Credit](paypal.md#paypal-credit-and-pay-later) till era kunder, **[!UICONTROL Enable PayPal Credit]** till `Yes`.

### Steg 3: Slutför inställningarna för betalningsstandard

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Payments Standard]** -avsnitt.

   ![Nödvändiga inställningar](../configuration-reference/sales/assets/payment-methods-paypal-payments-standard-required.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >E-postadresser är skiftlägeskänsliga. För att kunna ta emot betalning måste den e-postadress du anger motsvara den e-postadress som har angetts i PayPal-handelskontot.

   Om du inte har något PayPal-konto klickar du på **[!UICONTROL Start accepting payments via PayPal]**.

1. Ange **[!UICONTROL API Authentication Methods]** till något av följande:

   - `API Signature` - Den här PayPal-autentiseringsmetoden är enklast att implementera och baseras på ditt användarnamn, lösenord och en unik sträng med tecken och siffror som identifierar ditt konto. API-signaturens autentiseringsuppgifter upphör inte att gälla.
   - `API Certificate` - Den här PayPal-autentiseringsmetoden är säkrare och baseras på ditt användarnamn, lösenord och ett hämtningsbart certifikat. API-autentiseringsuppgifterna går ut efter tre år och måste förnyas.

   Fyll i följande om det behövs:

   - **[!UICONTROL API Username]**
   - **[!UICONTROL API Password]**
   - **[!UICONTROL API Signature]**

1. Om du använder inloggningsuppgifter från ditt sandlådekonto anger du **[!UICONTROL Sandbox Mode]** till `Yes`.

   När du testar konfigurationen i en sandlåda ska du bara använda [kreditkortsnummer][2] som rekommenderas av PayPal. När du är redo att börja producera går du tillbaka till konfigurationen och ställer in sandlådeläget på `No` och ansluta till ditt PayPal-produktionskonto.

1. Om systemet använder en proxyserver för att upprätta anslutningen mellan Adobe Commerce eller Magento Open Source och betalningssystemet PayPal anger du **[!UICONTROL API Uses Proxy]** till `Yes` och slutför följande:

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

### Steg 4: Ställa in annonsering för PayPal-kredit/Adverise PayPal PayLater (valfritt)

Från och med version 2.4.3 stöds PayPal PayLater i distributioner som inkluderar PayPal. Med den här funktionen kan kunderna betala för en beställning varannan vecka i stället för att betala hela beloppet vid köptillfället. PayPal-kreditupplevelsen är föråldrad.

Ange **[!UICONTROL Enable PayPal PayLater Experience]** till något av följande:

- `Yes` - För att konfigurera Advertize PayPal PayLater
- `No` - För att ställa in Advertize PayPal Credit

#### Annonsera PayPal Credit

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Advertise PayPal Credit]** -avsnitt.

   ![Annonsera inställningar för startsidan för PayPal-kredit](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. Om du vill hämta din kontoinformation klickar du på **[!UICONTROL Get Publisher ID from PayPal]** och följ instruktionerna.

1. Ange **[!UICONTROL Publisher ID]**.

   ![Annonsera PayPal Credit](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Home Page]** -avsnitt.

1. Om du vill placera en banderoll på sidan anger du **[!UICONTROL Display]** till `Yes`.

1. Ange **[!UICONTROL Position]** till något av följande:

   - `Header (center)`
   - `Sidebar (right)`

1. Ange **[!UICONTROL Size]** till något av följande:

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) de återstående avsnitten och upprepa föregående steg:

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### Annonsera PayPal PayLater

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Advertise PayPal PayLater]** -avsnitt.

1. Ange **[!UICONTROL Enable PayPal PayLater]** till `Yes`.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Home Page]** -avsnitt.

   ![Annonsera inställningar för startsidan för PayPal-kredit](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. Om du vill placera en banderoll på sidan anger du **[!UICONTROL Display]** till `Yes`.

1. Ange **[!UICONTROL Position]** till något av följande:

   - `Header (center)`
   - `Sidebar`

1. Ange **[!UICONTROL Style Layout]** till något av följande:

   - `Text`
   - `Flex`

1. För [!UICONTROL Style Layout] **[!UICONTROL Text]** only, set **[!UICONTROL Logo Type]** till något av följande:

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. För [!UICONTROL Style Layout] **[!UICONTROL Text]** only, set **[!UICONTROL Logo Position]** till något av följande:

   - `Left`
   - `Right`
   - `Top`

1. För [!UICONTROL Style Layout] **[!UICONTROL Text]** only, set **[!UICONTROL Text Color]** till något av följande:

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. För [!UICONTROL Style Layout] **[!UICONTROL Text]** only, set **[!UICONTROL Text Size]** till något av följande:

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. För [!UICONTROL Style Layout] **[!UICONTROL Flex]** only, set **[!UICONTROL Ratio]** till något av följande:

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. För [!UICONTROL Style Layout] **[!UICONTROL Flex]** only, set **[!UICONTROL Color]** till något av följande:

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) de återstående avsnitten och upprepa föregående steg:

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **Betalningssteg för utcheckning**
   - **[!UICONTROL Catalog Category Page]**

### Steg 5: Slutför de grundläggande inställningarna

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Basic Settings - PayPal Website Payments Standard]** -avsnitt.

   ![Grundinställningar](./assets/paypal-payments-basic.png){width="600" zoomable="yes"}

1. För **[!UICONTROL Title]**, anger du en titel som identifierar betalningsmetoden under utcheckningen.

   Vi rekommenderar att du använder titeln _PayPal_ för alla butiksvyer.

1. Om du erbjuder flera betalningsmetoder anger du ett nummer för **[!UICONTROL Sort Order]** för att bestämma i vilken ordning som PayPal Payments Standard ska visas när den anges med andra betalningsmetoder.

   Det här talet är relativt till de andra betalningsmetoderna. (`0` = first, `1` = sekund, `2` = tredje och så vidare.)

1. Ange **[!UICONTROL Payment Action]** till något av följande:

   - `Authorization` - Godkänner köpet och spärrar pengarna. Beloppet dras inte tillbaka förrän handlaren har tagit det.
   - `Sale` - Köpbeloppet godkänns och dras omedelbart tillbaka från kundens konto.

1. Visa _[!UICONTROL Check out with PayPal]_på produktsidan, ange **[!UICONTROL Display on Product Details Page]**till `Yes`.

### Steg 6: Slutför de avancerade inställningarna

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Advanced Settings]** -avsnitt.

   ![Avancerade inställningar](../configuration-reference/sales/assets/payment-methods-paypal-payment-standard-advanced.png){width="600" zoomable="yes"}

1. Ställ in PayPal Payments Standard från både kundvagnen och minikorgen **[!UICONTROL Display on Shopping Cart]** till `Yes`.

1. Ange **[!UICONTROL Payment from Applicable Countries]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här betalningsmetoden.
   - `Specific Countries` - När du har valt det här alternativet visas _[!UICONTROL Payment from Specific Countries]_visas. Om du vill markera flera länder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

1. Om du vill registrera kommunikation med betalningssystemet i loggfilen anger du **[!UICONTROL Debug Mode]** till `Yes`.

   >[!NOTE]
   >
   >Loggfilen lagras på servern och är bara tillgänglig för utvecklare. I enlighet med PCI-datasäkerhetsstandarder registreras inte kreditkortsinformation i loggfilen.

1. Om du vill aktivera SSL-verifiering anger du **[!UICONTROL Enable SSL Verification]** till `Yes`.

1. Om du vill visa en sammanfattning av varje radobjekt i beställningen på din PayPal-betalningssida anger du **[!UICONTROL Transfer Cart Line Items]** till `Yes`.

   Om du vill inkludera upp till tio leveransalternativ i sammanfattningen anger du **[!UICONTROL Transfer Shipping Options]** till `Yes`. (Det här alternativet visas bara om radobjekten är inställda på överföring.)

1. Ange vilken typ av bild som ska användas för accepteringsknappen för PayPal **[!UICONTROL Shortcut Buttons Flavor]** till något av följande:

   - `Dynamic` - (Rekommenderas) Visar en bild som kan ändras dynamiskt från PayPal-servern.
   - `Static` - Visar en viss bild som inte kan ändras dynamiskt.

1. Om du vill att kunder som inte har ett PayPal-konto ska kunna göra ett köp med den här metoden anger du **[!UICONTROL Enable PayPal Guest Checkout]** till `Yes`.

1. Ange **[!UICONTROL Require Customer's Billing Address]** till något av följande:

   - `Yes` - Kräver kundens faktureringsadress för alla inköp.
   - `No` - Kräver inte kundens faktureringsadress för några inköp.
   - `For Virtual Quotes Only` - Kräver endast kundens faktureringsadress för virtuella offerter.

1. Så här tillåter du en kund att göra en [PayPal-faktureringsavtal](paypal-billing-agreements.md) med din butik när det inte finns några aktiva faktureringsavtal tillgängliga i kundkontot, ange **[!UICONTROL Billing Agreement Signup]** till något av följande:

   - `Auto` - Kunden kan antingen ingå ett faktureringsavtal under Express Checkout-flödet eller använda en annan betalningsmetod.
   - `Ask Customer` - Kunden kan bestämma sig för om han eller hon ska ingå ett faktureringsavtal under arbetsflödet för Express Checkout.
   - `Never` - Kunden kan inte ingå ett faktureringsavtal under arbetsflödet Express Checkout.

   >[!NOTE]
   >
   >Handlarna måste begära teknisk support för PayPal Merchant för att kunna aktivera faktureringsavtal i sina konton. The _Registrering av faktureringsavtal_ parametern kan bara aktiveras efter att PayPal har bekräftat att faktureringsavtal är aktiverade för ditt handlarkonto.

1. Om du vill att kunden ska kunna slutföra transaktionen från PayPal-webbplatsen utan att behöva besöka din butik för ordergranskning anger du **[!UICONTROL Skip Order Review Step]** till `Yes`.

### Steg 7: Slutför och spara konfigurationsinställningarna

1. Fyll i följande avsnitt efter behov:

   - [Inställningar för PayPal-faktureringsavtal](#paypal-billing-agreement-settings)
   - [Inställningar för kvittningsrapport](#settlement-report-settings)
   - [Frontend Experience Settings](#frontend-experience-settings)

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

#### Inställningar för PayPal-faktureringsavtal

A [faktureringsavtal](paypal-billing-agreements.md) är ett försäljningsavtal mellan handlaren och kunden som har godkänts av PayPal för användning med flera order. Under utcheckningsprocessen visas betalningsalternativet Faktureringsavtal endast för kunder som redan har tecknat ett faktureringsavtal med ditt företag. När PayPal har godkänt avtalet utfärdar betalningssystemet ett unikt referens-ID för att identifiera varje order som är kopplad till avtalet. På samma sätt som en inköpsorder finns det ingen gräns för hur många faktureringsavtal en kund kan ställa in hos ditt företag.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL PayPal Billing Agreement Settings]** -avsnitt.

   ![Inställningar för faktureringsavtal](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enabled]** till `Yes`.

1. För **[!UICONTROL Title]**, anger du en titel som identifierar metoden PayPal-faktureringsavtal under utcheckningen.

1. Om du erbjuder flera betalningsmetoder anger du ett nummer i **[!UICONTROL Sort Order]** för att bestämma i vilken ordning faktureringsavtalet ska visas när det visas med andra betalningsmetoder vid utcheckning.

1. Ange **[!UICONTROL Payment Action]** till något av följande:

   - `Authorization` - Godkänner köpet och spärrar pengarna. Beloppet dras inte tillbaka förrän handlaren&quot;fångar&quot; det.
   - `Sale` - Köpbeloppet godkänns och dras omedelbart tillbaka från kundens konto.

1. Ange **[!UICONTROL Payment Applicable From]** till något av följande:

   - `All Allowed Countries` - Kunder från alla länder som anges i din butikskonfiguration kan använda den här betalningsmetoden.
   - `Specific Countries` - När du har valt det här alternativet visas _[!UICONTROL Payment from Specific Countries]_visas. Om du vill markera flera länder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på vart och ett av dem.

1. Om du vill registrera kommunikation med betalningssystemet i loggfilen anger du **[!UICONTROL Debug Mode]** till `Yes`.

   >[!NOTE]
   >
   >Loggfilen lagras på servern och är bara tillgänglig för utvecklare. I enlighet med PCI-datasäkerhetsstandarder registreras inte kreditkortsinformation i loggfilen.

1. Om du vill aktivera SSL-verifiering anger du **[!UICONTROL Enable SSL Verification]** till `Yes`.

1. Om du vill visa en sammanfattning av varje radobjekt i kundens order på din PayPal-betalningssida anger du **[!UICONTROL Transfer Cart Line Items]** till `Yes`.

1. Om du vill att kunderna ska kunna initiera ett faktureringsavtal från kontrollpanelen för sina kundkonton anger du **[!UICONTROL Allow in Billing Agreement Wizard]** till `Yes`.

#### Inställningar för kvittningsrapport

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Settlement Report Settings]** -avsnitt.

   ![Inställningar för kvittningsrapport](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. För **[!UICONTROL SFTP Credentials]** gör du följande:

   - Om du har registrerat dig för PayPal Secure FTP-servern anger du följande inloggningsuppgifter för SFTP:

      - Inloggning
      - Lösenord

   - Om du vill köra testrapporter innan du publicerar med Express Checkout på webbplatsen anger du **[!UICONTROL Sandbox Mode]** till `Yes`.

   - Ange **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     Som standard är värdet `reports.paypal.com`.

   - Ange **[!UICONTROL Custom Path]** där rapporter sparas.

     Som standard är värdet `/ppreports/outgoing`.

1. Om du vill generera rapporter enligt ett schema fyller du i **[!UICONTROL Scheduled Fetching]** inställningar:

   - Ange **[!UICONTROL Enable Automatic Fetching]** till `Yes`.

   - Ange **[!UICONTROL Schedule]** till något av följande:

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal bevarar varje rapport i 45 dagar.

   - Ange **[!UICONTROL Time of Day]** till timme, minut och sekund när du vill att rapporterna ska genereras.

#### Frontend Experience Settings

Använd _[!UICONTROL Frontend Experience Settings]_för att välja vilka PayPal-logotyper som ska visas på din webbplats och för att anpassa utseendet på PayPals handlarsidor.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Frontend Experience Settings]** -avsnitt.

   ![Frontend Experience Settings](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. Välj **[!UICONTROL PayPal Product Logo]** som du vill ska visas i PayPal-blocket i din butik.

   PayPal-logotyperna finns i fyra format och två storlekar:

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. Så här anpassar du utseendet på PayPal-handlarsidorna:

   - Ange namnet på **[!UICONTROL Page Style]** som du vill använda på dina PayPal-handlarsidor:

      - `paypal` - Använder sidformatet PayPal.
      - `primary` - Använder det sidformat som du identifierade som _primär_ format i din kontoprofil.
      - `your_custom_value` - Använder ett anpassat betalningssidformat som anges i din kontoprofil.

   - För **[!UICONTROL Header Image URL]** anger du URL-adressen till bilden som du vill ska visas i det övre vänstra hörnet på betalningssidan. Den maximala filstorleken är 750 pixlar bred och 90 pixlar hög.

     >[!NOTE]
     >
     >PayPal rekommenderar att bilden finns på en säker server (https). I annat fall kan en webbläsare varna för att _sidan innehåller både säkra och osäkra objekt_.

   - Om du vill ange färg för sidorna anger du hexadecimalkoden med sex tecken, utan `#` -symbol, för var och en av följande:

      - **[!UICONTROL Header Background Color]** - Bakgrundsfärg för sidhuvudet i kassan.
      - **[!UICONTROL Header Border Color]** - Färg för kantlinje med två pixlar runt sidhuvudet.
      - **[!UICONTROL Page Background Color]** - Bakgrundsfärg för utcheckningssidan och runt rubriken och betalningsformuläret.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[3]: https://developer.paypal.com/docs/api-basics/sandbox/
[4]: https://developer.paypal.com/docs/paypal-payments-standard/mobile-paypal-payments-standard/
