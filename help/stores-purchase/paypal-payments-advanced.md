---
title: Avancerade PayPal-betalningar
description: Lär dig hur du ställer in PayPal Payments Advanced som en onlinebetalningslösning i din butik.
exl-id: 018dd999-2f17-4650-8f61-624809ae76c6
feature: Payments
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '2162'
ht-degree: 0%

---

# Avancerade PayPal-betalningar

[Avancerade PayPal-betalningar](https://developer.paypal.com/docs/payflow/gs-ppa-hosted-pages/) är en [PCI-kompatibel](../getting-started/compliance-pci.md) lösning som gör att dina kunder kan betala med hjälp av debet eller kreditkort utan att lämna din plats. Den innehåller en inbäddad utcheckningssida som kan anpassas för att skapa en sömlös och säker utcheckning.

Även kunder som saknar ett PayPal-konto kan göra inköp via den säkra betalningsgatewayen PayPal. Följande kort kan användas: Visa-, MasterCard-, Switch-/Maestro- och Solo-kreditkort i USA och Storbritannien. För ytterligare enkelhet ingår PayPal Express Checkout i Avancerade PayPal-betalningar.

>[!IMPORTANT]
>
>**PSD2-krav:** <br/>
>Från och med den 14 september 2019 kan europeiska banker avböja betalningar som inte uppfyller kraven för [PSD2](../getting-started/compliance-payment-services-directive.md). För att uppfylla kraven i PSD2 måste PayPal Payments Advanced integreras med ett plugin-program från tredje part. Mer information finns i [3-D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-mpi/).

>[!NOTE]
>
>Avancerade PayPal-betalningar kan inte användas för beställningar som har skapats av administratören för din butik.

## Krav

- [PayPal-företagskonto](https://www.paypal.com/webapps/mpp/how-to-sell-online)
- Om du hanterar flera Adobe Commerce- och Magento Open Source-webbplatser måste du ha ett separat PayPal-handelskonto för varje webbplats.

## Arbetsflöde för kassor

1. **Kunden väljer betalningsmetod** - Vid utcheckning väljer kunden att betala med Avancerade PayPal-betalningar. Knappen Betala nu visas i stället för knappen Montera ordning.

1. **Betala nu** - Kunden klickar/trycker _Betala nu_ och ett PayPal-formulär visas. Kunden anger kortinformationen och kortet verifieras. Om du lyckas visas orderbekräftelsesidan.

   **Betala med PayPal** - Formuläret innehåller även knappen _Betala med PayPal_ som dirigerar om kunden till PayPal-webbplatsen, där betalning kan göras med PayPal Express Checkout.

1. **Felsökning** - Om transaktionen misslyckas av någon anledning visas ett felmeddelande på utcheckningssidan och kunden uppmanas att försöka igen. Alla problem hanteras av PayPal.

## Arbetsflöde för orderbehandling

Bearbetningsorder med Avancerade PayPal-betalningar är samma som för vanliga PayPal-order. Beställningar faktureras och skickas och kreditnotor genereras för både online- och offlineåterbetalningar. Flera onlineåterbetalningar är dock inte tillgängliga för beställningar som har betalats med Avancerade PayPal-betalningar.

1. **Kunden lägger order** - I det sista steget i utcheckningen trycker kunden på knappen Placera order.

1. **PayPal svarar** - PayPal utvärderar begäran. Om det är giltigt bearbetar PayPal transaktionen.

1. **Commerce anger orderstatus** - Commerce får svar från PayPal och anger orderstatus till något av följande:

   - **Bearbetar** - transaktionen lyckades.
   - **Väntande betalning** - Systemet fick inget svar från PayPal.
   - **Avbruten** - Transaktionen misslyckades av någon anledning
   - **Misstänkt bedrägeri** - Transaktionen överförde inte några av [PayPal-bedrägerifiltren](paypal.md#paypal-fraud-management-filters). Systemet får ett svar från PayPal om att transaktionen granskas av bedrägeritjänsten.

1. **Merchant slutför beställning** - Handlingsfakturorna och skickar ordern.

## Konfigurera ditt PayPal-konto

Innan du konfigurerar Avancerade PayPal-betalningar i Commerce måste du konfigurera ditt konto på PayPals webbplats.

1. Logga in på ditt [PayPal-företagskonto](https://manager.paypal.com/).

1. Gå till **[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up Menu]** och fyll i följande inställningar:

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. **[!UICONTROL Save]** inställningarna.

   >[!NOTE]
   >
   >Om du har flera Commerce-webbplatser måste du skapa ett separat konto för PayPal Payments Advanced för varje.

1. Gör följande när du uppmanas att skapa en layout:

   - Klicka på **[!UICONTROL Customize]** överst på sidan.

   - Välj **[!UICONTROL Layout C]**.

   - Klicka på **[!UICONTROL Save and Publish]**.

1. Konfigurera en annan användare (rekommenderas av PayPal):

   - Logga in på ditt [PayPal-företagskonto](https://manager.paypal.com/).

   - Följ instruktionerna för att konfigurera en annan användare.

   - **[!UICONTROL Save]** ändringarna.

## Ställ in avancerade PayPal-betalningar i Commerce

>[!NOTE]
>
>Du kan ha två PayPal-lösningar aktiva samtidigt: Express Checkout, plus en allt-i-ett- eller Payment Gateway-lösning. Om du ändrar betalningslösningar inaktiveras den som användes tidigare.

>[!TIP]
>
>Klicka på **[!UICONTROL Save Config]** när du vill spara förloppet.

### Steg 1: Påbörja konfigurationen

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_&#x200B;Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Payment Methods]**.

1. Om din Commerce-installation har flera webbplatser, butiker eller vyer anger du **[!UICONTROL Store View]** i butiksvyn där du vill använda den här konfigurationen.

1. I avsnittet _[!UICONTROL Merchant Location]_&#x200B;väljer du **[!UICONTROL Merchant Country]**&#x200B;där ditt företag finns.

   Den här inställningen bestämmer valet av PayPal-lösningar som visas i konfigurationen.

   ![Handelsland](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Expandera **[!UICONTROL PayPal All-in-One Payment Solution]** och klicka på **[!UICONTROL Configure]** för **[!UICONTROL Payments Advanced]**.

   ![Avancerade PayPal-betalningar](./assets/paypal-payments-advanced.png){width="600" zoomable="yes"}

### Steg 2: Slutför de obligatoriska inställningarna

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Required PayPal Settings]** om det behövs.

   ![Avancerade nödvändiga inställningar - Avancerade PayPal-betalningar](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-required.png){width="600" zoomable="yes"}

1. (Valfritt) Ange **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >E-postadresser är skiftlägeskänsliga. För att kunna ta emot betalning måste e-postadressen matcha den e-postadress som har angetts i PayPal-handelskontot.

   Om du inte har något PayPal-konto klickar du på **[!UICONTROL Start accepting payments via PayPal]**.

1. Ange en av följande autentiseringsuppgifter som du använder för att logga in på ditt PayPal-handelskonto:

   - **[!UICONTROL Partner]** - Ditt PayPal Partner-ID.
   - **[!UICONTROL Vendor]** - Ditt PayPal-användarnamn.
   - **[!UICONTROL User]** - ID:t för en annan användare som är konfigurerad för ditt PayPal-konto.

1. Ange **[!UICONTROL Password]** som är associerad med ditt PayPal-konto.

1. Om du vill köra testtransaktioner anger du **[!UICONTROL Test Mode]** till `Yes`.

   När du testar konfigurationen i en sandlåda ska du bara använda [kreditkortsnummer](https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm) som rekommenderas av PayPal. När du är redo att börja producera återgår du till konfigurationen och ställer in testläget på `No`.

1. Om systemet använder en proxyserver för att upprätta anslutningen till PayPal-systemet anger du **[!UICONTROL Use Proxy]** till `Yes` och gör följande:

   - Ange IP-adressen för **[!UICONTROL Proxy Host]**.

   - Ange portnumret för **[!UICONTROL Proxy Port]**.

     En proxy används när serverns brandvägg förhindrar direktåtkomst till PayPal-servern. I det här fallet används en tredjepartsserver för att vidarebefordra trafik.

1. Ange **[!UICONTROL Enable this Solution]** till `Yes`.

1. Om du vill erbjuda dina kunder [PayPal-kredit](paypal.md#paypal-credit-and-pay-later) anger du **[!UICONTROL Enable PayPal Credit]** till `Yes`.

### Steg 3: Ställa in annonsering för PayPal-kredit/Adverise PayPal PayLater (valfritt)

Från och med version 2.4.3 stöds PayPal PayLater i distributioner som inkluderar PayPal. Med den här funktionen kan kunderna betala för en beställning varannan vecka i stället för att betala hela beloppet vid köptillfället. PayPal-kreditupplevelsen är föråldrad.

Ange **[!UICONTROL Enable PayPal PayLater Experience]** till något av följande:

- `Yes` - Om du vill konfigurera annonser för PayPal PayLater
- `No` - För att konfigurera annonsering för PayPal-kredit

#### Annonsera PayPal Credit

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Advertise PayPal Credit]**.

   ![Annonsera PayPal-kredit](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Om du vill hämta din kontoinformation klickar du på **[!UICONTROL Get Publisher ID from PayPal]** och följer instruktionerna.

1. Ange din **[!UICONTROL Publisher ID]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Home Page]**.

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

   ![Annonsera inställningar för startsidan för PayPal-kredit](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. Expandera ![Expanderingsväljaren](../assets/icon-display-expand.png) för de återstående avsnitten och upprepa föregående steg:

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### Annonsera PayPal PayLater

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Advertise PayPal PayLater]**.

1. Ange **[!UICONTROL Enable PayPal PayLater]** till `Yes`.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Home Page]**.

1. Om du vill placera en banderoll på sidan anger du **[!UICONTROL Display]** till `Yes`.

1. Ange **[!UICONTROL Position]** till något av följande:

   - `Header (center)`
   - `Sidebar`

1. Ange **[!UICONTROL Style Layout]** till något av följande:

   - `Text`
   - `Flex`

1. För [!UICONTROL Style Layout] **[!UICONTROL Text]** anger du **[!UICONTROL Logo Type]** till något av följande:

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. För [!UICONTROL Style Layout] **[!UICONTROL Text]** anger du **[!UICONTROL Logo Position]** till något av följande:

   - `Left`
   - `Right`
   - `Top`

1. För [!UICONTROL Style Layout] **[!UICONTROL Text]** anger du **[!UICONTROL Text Color]** till något av följande:

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. För [!UICONTROL Style Layout] **[!UICONTROL Text]** anger du **[!UICONTROL Text Size]** till något av följande:

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. För [!UICONTROL Style Layout] **[!UICONTROL Flex]** anger du **[!UICONTROL Ratio]** till något av följande:

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. För [!UICONTROL Style Layout] **[!UICONTROL Flex]** anger du **[!UICONTROL Color]** till något av följande:

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

   ![Annonsera inställningar för startsidan för PayPal-kredit](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. Expandera ![Expanderingsväljaren](../assets/icon-display-expand.png) för de återstående avsnitten och upprepa föregående steg:

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### Steg 4: Slutför de grundläggande inställningarna

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Basic Settings - PayPal Payments Advanced]** om det behövs.

   ![Avancerade grundläggande inställningar för PayPal-betalningar](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-basic-settings.png){width="600" zoomable="yes"}

1. Om du vill identifiera Avancerade PayPal-betalningar under utcheckningen anger du **[!UICONTROL Title]**.

   Vi rekommenderar att du använder titeln _Debit eller Credit Card_.

1. Om du erbjuder flera betalningsmetoder anger du ett nummer för **[!UICONTROL Sort Order]** för att avgöra i vilken ordning avancerade PayPal-betalningar visas när de visas tillsammans med andra betalningsmetoder vid utcheckning.

   Det här talet är relativt till de andra betalningsmetoderna. (`0` = först, `1` = sekund, `2` = tredje o.s.v.)

1. Ange **[!UICONTROL Payment Action]** till något av följande:

   - `Authorization` - Godkänn köpet, men spärrar pengarna. Beloppet dras inte tillbaka förrän det _har hämtats_ av handlaren.
   - `Sale` - Köpbeloppet är auktoriserat och dras omedelbart tillbaka från kundens konto.

### Steg 5: Slutför de avancerade inställningarna

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Advanced Settings]**.

   ![Avancerade inställningar - Avancerade PayPal-betalningar](./assets/paypal-payments-advanced2.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Payment Applicable From]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här betalningsmetoden.
   - `Specific Countries` - När du har valt det här alternativet visas listan _[!UICONTROL Payment from Specific Countries]_. Håll ned Ctrl-tangenten (PC) eller Kommando-tangenten (Mac) och markera varje land i listan där kunderna kan göra inköp från din butik.

1. Om du vill skriva kommunikation med betalningssystemet till loggfilen anger du **[!UICONTROL Debug Mode]** till `Yes`.

   Loggfilen för Avancerade PayPal-betalningar är `payments_payflow_advanced.log`.

   >[!NOTE]
   >
   >I enlighet med PCI-datasäkerhetsstandarder registreras inte kreditkortsinformation i loggfilen.

1. Ange **[!UICONTROL Enable SSL Verification]** till `Yes` om du vill aktivera verifiering av värdautenticitet.

1. Om du vill att kunden ska kunna korrigera sin inmatning av den tresiffriga CVV-säkerhetskoden från baksidan av ett kreditkort anger du **[!UICONTROL CVV Entry is Editable]** till `Yes`.

1. Ange **[!UICONTROL Require CVV Entry]** till `Yes` om du vill att kunderna ska ange en CVV-kod.

1. Om du vill skicka en bekräftelse av betalningen till kunden anger du **[!UICONTROL Send Email Confirmation]** till `Yes`.

1. Om du vill ta reda på vilken metod som används för att utbyta information med PayPal-servern under en transaktion anger du **[!UICONTROL URL method for Cancel URL and Return URL]** till något av följande:

   - `GET` - (Standard) Hämtar information som är resultatet av en process.
   - `POST` - Tillhandahåller ett block med data, t.ex. data som har angetts i ett formulär, till en datahanteringsprocess.

   _Avbryt URL_ och _Retur-URL_ refererar till sidan där kunden returnerar efter att ha slutfört eller annullerat betalningsdelen av utcheckningsprocessen på PayPal-servern.

1. Fyll i följande avsnitt efter behov:

   - [Inställningar för kvittningsrapport](#settlement-report-settings)
   - [Frontend Experience Settings](#frontend-experience-settings)

#### Inställningar för kvittningsrapport

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Settlement Report Settings]**.

   ![Rapportinställningar för PayPal-kvittning](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Gör följande för **[!UICONTROL SFTP Credentials]**:

   - Om du har registrerat dig för PayPals säkra FTP-server anger du följande inloggningsuppgifter för SFTP:

      - Inloggning
      - Lösenord

   - Om du vill köra testrapporter innan du publicerar anger du **[!UICONTROL Sandbox Mode]** till `Yes`.

   - Ange **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     Som standard är värdet `reports.paypal.com`.

   - Ange **[!UICONTROL Custom Path]** där rapporter sparas.

     Som standard är värdet `/ppreports/outgoing`.

1. Om du vill generera rapporter enligt ett schema, fyll i inställningarna för **[!UICONTROL Scheduled Fetching]**:

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

   - Ange **[!UICONTROL Time of Day]** till timma, minut och sekund när du vill att rapporterna ska genereras.

#### Frontend Experience Settings

Använd _[!UICONTROL Frontend Experience Settings]_&#x200B;för att välja vilka PayPal-logotyper som ska visas på din webbplats och för att anpassa utseendet på PayPals handlarsidor.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Frontend Experience Settings]**.

   ![Inställningar för PayPal-klientens upplevelse](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png){width="600" zoomable="yes"}

1. Markera **[!UICONTROL PayPal Product Logo]** som du vill ska visas i PayPal-blocket i din butik.

   PayPal-logotyperna finns i fyra format och två storlekar:

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. Så här anpassar du utseendet på PayPal-handlarsidorna:

   - Ange namnet på **[!UICONTROL Page Style]** som du vill tillämpa på dina PayPal-handlarsidor:

      - `paypal` - Använder sidformatet PayPal.
      - `primary` - Använder det sidformat som du identifierade som _primär_-format i din kontoprofil.
      - `your_custom_value` - Använder ett anpassat betalningssidformat som anges i din kontoprofil.

   - För **[!UICONTROL Header Image URL]** anger du URL-adressen till bilden som du vill ska visas i det övre vänstra hörnet på betalningssidan. Den maximala filstorleken är 750 pixlar bred och 90 pixlar hög.

   >[!NOTE]
   >
   >PayPal rekommenderar att bilden finns på en säker server (https). Annars kan en webbläsare varna för att _sidan innehåller både säkra och osäkra objekt_.

   - Om du vill ange färg för sidorna anger du hexadecimalkoden på sex tecken, utan symbolen `#`, för vart och ett av följande:

      - **[!UICONTROL Header Background Color]** - Bakgrundsfärg för sidhuvudet i kassan.
      - **[!UICONTROL Header Border Color]** - Färg för en kant på två pixlar runt huvudet.
      - **[!UICONTROL Page Background Color]** - Bakgrundsfärg för utcheckningssidan och runt rubriken och betalningsformuläret.

### Steg 6: Slutför grundläggande inställningar för PayPal Express Checkout

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Basic Settings - PayPal Express Checkout]**.

   ![Grundinställningar för PayPal Express-utcheckning](../configuration-reference/sales/assets/payment-methods-paypal-advanced-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. För **[!UICONTROL Title]** anger du en titel som identifierar betalningsmetoden vid utcheckning.

   Du bör ange titeln till _PayPal_ för varje butiksvy.

1. Om du erbjuder flera betalningsmetoder anger du ett nummer för **[!UICONTROL Sort Order]** för att bestämma i vilken ordning som PayPal Express Checkout ska visas när den visas tillsammans med andra betalningsmetoder.

   Det här talet är relativt till de andra betalningsmetoderna. (`0` = först, `1` = sekund, `2` = tredje o.s.v.)

1. Ange **[!UICONTROL Payment Action]** till något av följande:

   - `Authorization` - Godkänner köpet och spärrar pengarna. Beloppet dras inte tillbaka förrän det _har hämtats_ av handlaren.
   - `Sale` - Köpbeloppet är auktoriserat och dras omedelbart tillbaka från kundens konto.

1. Om du vill visa knappen _[!UICONTROL Check out with PayPal]_&#x200B;på produktsidan anger du **[!UICONTROL Display on Product Details Page]**&#x200B;till `Yes`.

### Steg 7: Slutför avancerade inställningar - PayPal Express Checkout

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Advanced Settings]**.

   ![Avancerade inställningar för PayPal Express-utcheckning](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-express-checkout-advanced.png){width="600" zoomable="yes"}

1. Om du vill att PayPal Express Checkout ska vara tillgängligt både i kundvagnen och i minivagnen anger du **[!UICONTROL Display on Shopping Cart]** till `Yes`.

1. Ange **[!UICONTROL Payment Applicable From]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här betalningsmetoden.
   - `Specific Countries` |När du har valt det här alternativet visas listan _Betalning från specifika länder_ . Håll ned Ctrl-tangenten (PC) eller Kommando-tangenten (Mac) och klicka på varje land i listan där kunderna kan göra inköp från din butik.

1. Om du vill skriva kommunikation med betalningssystemet till loggfilen anger du **[!UICONTROL Debug Mode]** till `Yes`.

   >[!NOTE]
   >
   >I enlighet med [PCI-datasäkerhetsstandarder](../getting-started/compliance-pci.md) registreras inte kreditkortsinformation i loggfilen.

1. Ange **[!UICONTROL Enable SSL Verification]** till `Yes` om du vill aktivera verifiering av värdautenticitet.

1. Om du vill visa en fullständig sammanfattning av kundens order per radobjekt från PayPal-webbplatsen anger du **[!UICONTROL Transfer Cart Line Items]** till `Yes`.

1. Om du vill att kunden ska kunna slutföra transaktionen från PayPal-webbplatsen utan att gå tillbaka till din butik för ordergranskning anger du **[!UICONTROL Skip Order Review Step]** till `Yes`.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
