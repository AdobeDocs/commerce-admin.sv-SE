---
title: Länk till PayPal-betalningsflöde
description: Lär dig hur du konfigurerar PayPal Payflow Link som en onlinebetalningslösning i din butik.
exl-id: dba4057e-1fea-4a23-8594-cc85f619d664
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2172'
ht-degree: 0%

---

# Länk till PayPal-betalningsflöde

PayPal Payflow Link är endast tillgängligt för handlare i USA och Kanada. Kunder behöver inte ha ett personligt PayPal-konto och anger sin kreditkortsinformation i en form som hanteras av PayPal. Informationen lagras aldrig på din Adobe Commerce- eller Magento Open Source-server. Betalflödeslänk kan inte användas för order som har skapats från administratören.

Kreditnotor stöds för både online- och offlineåterbetalningar. Flera onlineåterbetalningar stöds dock inte.

>[!IMPORTANT]
>
>**Krav för PSD2:** <br/>
>Från och med den 14 september 2019 kan europeiska banker avböja betalningar som inte uppfyller [PSD2](../getting-started/compliance-payment-services-directive.md) krav. För att uppfylla PSD2 måste PayPal Payflow Link integreras med kardinalhandeln. Mer information finns på [3-D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

## Krav

- [PayPal Business Account][1] PayPal Payflow Pro-gatewayen länkar handlarkontot på PayPal till handlarens webbplats och fungerar som både gateway och handlarkonto.

- Om du hanterar flera Commerce-webbplatser måste du ha ett separat PayPal-handelskonto för varje webbplats.

## Kundarbetsflöde

1. **Kunden går till kassan** - I kassan väljer kunden att betala med länken PayPal Payflow och anger kreditkortsinformationen. Kunden behöver inte ha ett personligt PayPal-konto.
1. **Kunden väljer Betala nu** - Kunden trycker på knappen Betala nu för att skicka ordern.
1. **Kunden anger kreditkortsinformation** - Kunden anger kreditkortsinformationen i ett formulär som hanteras av PayPal. Om kunden klickar på _Avbryt betalning_ länk, kunden återgår till kassan med betalningsinformation och orderstatusen ändras till _Avbruten_.
1. **Kunden skickar ordern** - Kreditkortsinformationen skickas direkt till PayPal och sparas inte någonstans på handelsplatsen.

## Orderarbetsflöde

1. **PayPal tar emot begäran** - PayPal tar emot kundens förfrågan till Pay Now.
1. **PayPal verifierar betalningsinformationen** - PayPal verifierar kreditkortsinformationen och tilldelar lämplig status:
   - **Betalning verifierad:** Om den är verifierad visas _Väntande betalning_ status är ursprungligen tilldelad ordern tills transaktionen är kvittad.
   - **Bearbetar** - Transaktionen lyckades.
   - **Väntande betalning** - Systemet fick inget svar från PayPal.
   - **Avbruten** - Transaktionen misslyckades av någon anledning.
   - **Misstänkt bedrägeri** - transaktionen godkändes inte av en del av [Bedrägerifilter för PayPal](paypal.md#paypal-fraud-management-filters). Systemet får ett svar från PayPal om att transaktionen granskas av bedrägeritjänsten.
   - **Avbryt betalning:** Om kunden klickar på _Avbryt betalning_ länk, kunden återgår till kassan med betalningsinformation och orderstatusen ändras till _Avbruten_.
1. **Kunden omdirigeras till bekräftelsesidan**  - Om transaktionen slutförs utan fel dirigeras kunden om till orderbekräftelsesidan i din butik. Om transaktionen misslyckas av någon anledning visas ett felmeddelande på utcheckningssidan och kunden omdirigeras till att upprepa utcheckningsprocessen. Dessa situationer hanteras av PayPal.
1. **Merchant slutför order** - Handlarfakturorna och skickar ordern som vanligt.

## Konfigurera ditt PayPal-konto

1. Logga in på [PayPal-företagskonto][2].

1. Konfigurera [Hosted Checkout Pages][4] med PayPal Manager med följande inställningar:

   - Under **[!UICONTROL Security Options]** utför du följande inställningar:

     **[!UICONTROL AVS]**: `No`

     **[!UICONTROL CSC]**: `No`

     **[!UICONTROL Enable Secure Token]**: `Yes`

   - Välj **[!UICONTROL Customize]** och sedan välja **[!UICONTROL Layout C]**.

     Layout C visar endast kredit- och betalkortsfält och kan antingen ramas in på din webbplats eller användas som ett fristående popup-fönster. Storleken är fast på 490 x 565 pixlar, med extra utrymme för felmeddelanden. I vissa system åtgärdar den här inställningen ett problem med genomskinlig omdirigering.

1. När konfigurationsinställningarna är klara klickar du **[!UICONTROL Save and Publish]**.

1. Konfigurera en extra användare (rekommenderas av PayPal):

   - På den andra raden i huvudmenyn klickar du på **[!UICONTROL Manage Users]**.

   - Om du vill lägga till en annan användare till kontot klickar du på **[!UICONTROL Add User]**.

   - Fyll i de obligatoriska fälten i följande avsnitt i _Lägg till användare_ formulär:

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - Klicka på **[!UICONTROL Update]**.

## Ställ in PayPal Payflow Link

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

1. Expandera **[!UICONTROL PayPal Payment Gateways]** (om det behövs) och klicka på **[!UICONTROL Configure]** for **[!UICONTROL Payflow Link]**.

   ![Betalflödeslänk - Konfigurera](./assets/payflow-link.png){width="600" zoomable="yes"}

### Steg 2: Slutför de obligatoriska PayPal-inställningarna

![Nödvändiga PayPal-inställningar - PayPal-betalningsflödeslänk](./assets/payflow-required-link.png){width="600" zoomable="yes"}

1. (Valfritt) Ange **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >E-postadresser är skiftlägeskänsliga. För att kunna ta emot betalning måste e-postadressen matcha den e-postadress som har angetts i PayPal-handelskontot.

1. Ange en av följande autentiseringsuppgifter som du använder för att logga in på ditt PayPal-handelskonto:

   - **[!UICONTROL Partner]** - Ditt PayPal Partner-ID.
   - **[!UICONTROL User]** - ID:t för en annan användare som är konfigurerad för ditt PayPal-konto.
   - **[!UICONTROL Vendor]** - Ditt PayPal-användarnamn.

1. Ange **[!UICONTROL Password]** som är kopplat till ditt PayPal-konto.

1. Så här kör du testtransaktioner: ange **[!UICONTROL Test Mode]** till `Yes`.

   När du testar konfigurationen i en sandlåda ska du bara använda [kreditkortsnummer][3] som rekommenderas av PayPal. När du är redo att börja producera återgår du till konfigurationen och ställer in testläget på `No`.

1. Om systemet använder en proxyserver för att upprätta anslutningen till PayPal-systemet anger du **[!UICONTROL Test Mode]** till `Yes` och gör följande:

   - Ange IP-adressen för **[!UICONTROL Proxy Host]**.

   - Ange portnumret för **[!UICONTROL Proxy Port]**.

     En proxy används när serverns brandvägg förhindrar direktåtkomst till PayPal-servern. I så fall används en tredjepartsserver för att vidarebefordra trafik.

1. Ange **[!UICONTROL Enable Payflow Link]** till `Yes`.

1. Om du vill aktivera [PayPal Express-kassan](paypal-express-checkout.md) alternativ för kunder, ange **[!UICONTROL Enable Express Checkout]** till `Yes`.

1. Om du vill erbjuda [PayPal Credit](paypal.md#paypal-credit-and-pay-later) till era kunder, **[!UICONTROL Enable PayPal Credit]** till `Yes`.

### Steg 3: Ställa in annonsering för PayPal-kredit/Adverise PayPal PayLater (valfritt)

Från och med version 2.4.3 stöds PayPal PayLater i distributioner som inkluderar PayPal. Med den här funktionen kan kunderna betala för en beställning varannan vecka i stället för att betala hela beloppet vid köptillfället. PayPal-kreditupplevelsen är föråldrad.

Ange **[!UICONTROL Enable PayPal PayLater Experience]** till något av följande:

- `Yes` - För att konfigurera Advertize PayPal PayLater
- `No` - För att ställa in Advertize PayPal Credit

#### Annonsera PayPal Credit

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Advertise PayPal Credit]** -avsnitt.

   ![Annonsera PayPal Credit](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Om du vill hämta din kontoinformation klickar du på **[!UICONTROL Get Publisher ID from PayPal]** och följ instruktionerna.

1. Ange **[!UICONTROL Publisher ID]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Home Page]** -avsnitt.

   ![Annonsera inställningar för startsidan för PayPal-kredit](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

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

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) de återstående avsnitten och upprepa föregående steg för konfigurationen av hemsidan:

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
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### Steg 4: Slutför de grundläggande inställningarna

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Basic Settings - PayPal Payflow Link]** -avsnitt.

   ![Grundinställningar - Länk till PayPal-betalningsflöde](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-basic-settings.png){width="600" zoomable="yes"}

1. För **[!UICONTROL Title]**, anger du en titel som identifierar PayPal Payflow Link under utcheckningen.

   Vi rekommenderar att du använder titeln _Debet- eller kreditkort_.

1. Om du erbjuder flera betalningsmetoder anger du ett nummer för **[!UICONTROL Sort Order]** för att bestämma i vilken ordning Payflow Link ska visas när de visas tillsammans med andra betalningsmetoder.

   Det här talet är relativt till de andra betalningsmetoderna. (`0` = first, `1` = sekund, `2` = tredje och så vidare.)

1. Ange **[!UICONTROL Payment Action]** till något av följande:

   - `Authorization` - Godkänner köpet och spärrar pengarna. Beloppet dras inte tillbaka förrän handlaren har tagit det.
   - `Sale` - Köpbeloppet godkänns och dras omedelbart tillbaka från kundens konto.

### Steg 5: Slutför de avancerade inställningarna

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Advanced Settings]** -avsnitt.

   ![Avancerade inställningar - Länk till PayPal-betalningsflöde](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-advanced-settings.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Payment Applicable From]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här betalningsmetoden.
   - `Specific Countries` - När du har valt det här alternativet visas _[!UICONTROL Payment from Specific Countries]_visas. Håll ned Ctrl-tangenten och markera varje land i listan där kunderna kan göra inköp från din butik.

1. Om du vill skriva kommunikation med betalningssystemet till loggfilen anger du **[!UICONTROL Debug Mode]** till `Yes`.

   >[!NOTE]
   >
   >I enlighet med PCI-datasäkerhetsstandarder registreras inte kreditkortsinformation i loggfilen.

1. Om du vill aktivera verifiering av värdautenticitet anger du **[!UICONTROL Enable SSL Verification]** till `Yes`.

1. Om du vill att kunden ska kunna korrigera sin inmatning av den tresiffriga CVV-säkerhetskoden från kreditkortets baksida anger du **[!UICONTROL CVV Entry is Editable]** till `Yes`.

1. Ange en CVV-kod om du vill att kunderna ska ange den **[!UICONTROL Require CVV Entry]** till `Yes`.

1. Om du vill skicka en bekräftelse på betalningen till kunden anger du **[!UICONTROL Send Email Confirmation]** till `Yes`.

1. Om du vill ta reda på vilken metod som används för att utbyta information med PayPal-servern under en transaktion anger du **[!UICONTROL URL method for Cancel URL and Return URL]** till något av följande:

   - `GET` - Hämtar information som är resultatet av en process (standardmetod).
   - `POST` - Tillhandahåller ett block med data, t.ex. data som matats in i ett formulär, till en datahanteringsprocess.

   The _Avbryt URL_ och _Returnera URL_ hänvisar till sidan där kunden returnerar efter att ha slutfört eller annullerat betalningsdelen av utcheckningsprocessen på PayPal-servern

1. Fyll i följande avsnitt efter behov:

   - [Inställningar för kvittningsrapport](#settlement-report-settings)
   - [Frontend Experience Settings](#frontend-experience-settings)

#### Inställningar för kvittningsrapport

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Settlement Report Settings]** -avsnitt.

   ![Inställningar för kvittningsrapport - PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

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

   ![Frontend Experience Settings - PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

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

### Steg 6: Slutför de grundläggande inställningarna för PayPal Express Checkout

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Basic Settings - PayPal Express Checkout]** -avsnitt.

   ![Grundinställningar](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. För **[!UICONTROL Title]**, anger du en titel som identifierar betalningsmetoden under utcheckningen.

   Ange titeln till _PayPal_ rekommenderas för varje butiksvy.

1. Om du erbjuder flera betalningsmetoder anger du ett nummer för **[!UICONTROL Sort Order]** för att bestämma i vilken ordning som PayPal Express Checkout ska visas när den visas tillsammans med andra betalningsmetoder.

   Det här talet är relativt till de andra betalningsmetoderna. (`0` = first, `1` = sekund, `2` = tredje och så vidare.)

1. Ange **[!UICONTROL Payment Action]** till något av följande:

   - `Authorization` - Godkänner köpet och spärrar pengarna. Beloppet dras inte tillbaka förrän det _fångad_ av handlaren.
   - `Sale` - Köpbeloppet godkänns och dras omedelbart tillbaka från kundens konto.

1. Visa _[!UICONTROL Check out with PayPal]_på produktsidan, ange **[!UICONTROL Display on Product Details Page]**till `Yes`.

### Steg 7: Slutför de avancerade inställningarna för PayPal Express Checkout

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Advanced Settings]** -avsnitt.

   ![Avancerade inställningar](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Display on Shopping Cart]** till `Yes`.

1. Ange **[!UICONTROL Payment Applicable From]** till något av följande:

   - `All Allowed Countries` - Kunder från alla länder som anges i din butikskonfiguration kan använda den här betalningsmetoden.
   - `Specific Countries` - När du har valt det här alternativet visas _[!UICONTROL Payment from Specific Countries]_visas. Om du vill markera flera länder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje objekt.

1. Om du vill skriva kommunikation med betalningssystemet till loggfilen anger du **[!UICONTROL Debug Mode]** till `Yes`.

   >[!NOTE]
   >
   >I enlighet med PCI-datasäkerhetsstandarder registreras inte kreditkortsinformation i loggfilen.

1. Om du vill aktivera verifiering av värdautenticitet anger du **[!UICONTROL Enable SSL Verification]** till `Yes`.

1. Om du vill visa en fullständig sammanfattning av kundordern per radobjekt från PayPal-webbplatsen anger du **[!UICONTROL Transfer Cart Line Items]** till `Yes`.

1. Om du vill att kunden ska kunna slutföra transaktionen från PayPal-webbplatsen utan att behöva besöka din butik för ordergranskning anger du **[!UICONTROL Skip Order Review Step]** till `Yes`.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/integration-guide/configure-hosted-checkout/#configuring-hosted-pages-using-paypal-manager
