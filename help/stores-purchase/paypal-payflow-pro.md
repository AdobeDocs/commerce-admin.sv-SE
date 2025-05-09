---
title: PayPal Payflow Pro
description: Lär dig hur du konfigurerar PayPal Payflow Pro som en onlinebetalningslösning i din butik.
exl-id: c720b33c-44e1-4954-b5be-38932393a43c
feature: Payments
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '2211'
ht-degree: 0%

---

# PayPal Payflow Pro

PayPal Payflow Pro-gatewayen, som tidigare kallades _Verisign_, är tillgänglig för kunder i USA, Kanada, Australien och Nya Zeeland. Till skillnad från andra betalningsmetoder i PayPal debiteras handlarna en fast månadsavgift plus en fast avgift för varje transaktion, oavsett antal.

![Checka ut med PayPal](./assets/storefront-cart-paypal.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>**PSD2-krav:** <br/>
>Från och med den 14 september 2019 kan europeiska banker avböja betalningar som inte uppfyller kraven för [PSD2](../getting-started/compliance-payment-services-directive.md). För att uppfylla kraven i PSD2 måste PayPal Payflow Pro integreras med ett plugin-program från en annan leverantör. Mer information finns i [3-D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-mpi/).

## Krav

- [PayPal Business Account][1] - PayPal Payflow Pro-gatewayen länkar handlarkontot på PayPal till handlarens webbplats, vilket fungerar som både gateway och handlarkonto.

- Om du hanterar flera Adobe Commerce- och Magento Open Source-webbplatser måste du ha ett separat PayPal-handelskonto för varje webbplats.

## Kundarbetsflöde

1. **Kunden går till kassan** - I kassan väljer kunden att betala med PayPal Payflow Pro och anger kreditkortsinformationen. Kunder behöver inte ha personliga PayPal-konton. Beroende på vilket land det gäller kan kunderna även använda sitt personliga PayPal-konto för att betala ordern.
1. **Kunden skickar beställning** - Kunden skickar beställningen och beställningsinformationen skickas till PayPal för behandling. Kunden lämnar inte utcheckningssidan på er webbplats.
1. **PayPal slutför transaktionen** - Betalningar accepteras när ordern läggs. Beroende på betalningsåtgärden som anges i konfigurationen skapas antingen en försäljningsorder eller en försäljningsorder och en faktura.

## Arbetsflöde för onlinebeställning

1. **Administratören skickar onlinefaktura** - Butiksadministratören skickar en onlinefaktura och därmed skapas en motsvarande transaktion och faktura.
1. **PayPal tar emot transaktionen** - Orderinformationen skickas till PayPal. En post för transaktionen och en faktura genereras. Du kan visa alla Payflow Pro Gateway-transaktioner i ditt [PayPal-handelskonto][2].

>[!NOTE]
>
>Delfakturor och partiella återbetalningar stöds inte av PayPal Payflow Pro.

## Konfigurera ditt PayPal-konto

1. Logga in på ditt [PayPal-företagskonto][2].

1. Konfigurera [värdbaserade utcheckningssidor][4] med PayPal Manager med följande inställningar:

   - Under **[!UICONTROL Choose your settings]** anger du **[!UICONTROL Transaction Process Mode]** till `Live`.

   - Under **[!UICONTROL Display options on payment page]** anger du **Avbryt URL-metod** till `POST`.

   - Under **[!UICONTROL Billing Information]** markerar du kryssrutorna **[!UICONTROL CSC]** för kortets säkerhetskod för både obligatoriska och redigerbara fält.

   - Under **[!UICONTROL Payment Confirmation]** anger du **[!UICONTROL Return URL Method]** till `POST`.

   - Fyll i följande inställningar under **[!UICONTROL Security Options]**:

      - **[!UICONTROL AVS]**: `No`
      - **[!UICONTROL CSC]**: `No`
      - **[!UICONTROL Enable Secure Token]**: `Yes`

   - Välj **[!UICONTROL Customize]** och välj sedan **[!UICONTROL Layout C]**.

     Layout C visar endast kredit- och betalkortsfält och kan antingen ramas in på din webbplats eller användas som ett fristående popup-fönster. Storleken är fast på 490 x 565 pixlar, med extra utrymme för felmeddelanden. I vissa system åtgärdar den här inställningen ett problem med genomskinlig omdirigering.

1. När konfigurationsinställningarna är klara klickar du på **[!UICONTROL Save and Publish]**.

1. Välj **[!UICONTROL Account Administration]** på PayPal Manager-menyn.

1. Klicka på **[!UICONTROL Transaction Settings]** under **[!UICONTROL Manage Security]** och gör följande:

   - Ange **[!UICONTROL Allow reference transactions]** till `Yes`.

   - Klicka på **[!UICONTROL Confirm]**.

     >[!NOTE]
     >
     >Om du har flera Commerce-webbplatser måste du skapa ett separat konto för PayPal Payments Advanced för varje.

1. Konfigurera en annan användare (rekommenderas av PayPal):

   - Klicka på **[!UICONTROL Manage Users]** på den andra raden i huvudmenyn.

   - Klicka på **[!UICONTROL Add User]** om du vill lägga till en annan användare till kontot. Länken finns precis ovanför rubriken Hantera användare.

   - Fyll i de obligatoriska fälten i följande avsnitt i formuläret _[!UICONTROL Add User]_:

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - Klicka på **[!UICONTROL Update]**.

1. Logga ut från ditt PayPal-konto.

## Ställ in PayPal Payflow Pro i Commerce

>[!TIP]
>
>Klicka på **[!UICONTROL Save Config]** när du vill spara förloppet.

### Steg 1: Påbörja konfigurationen

Den här installationsmetoden förutsätter att du har ett befintligt PayPal-konto.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Payment Methods]**.

1. Om din Commerce-installation har flera webbplatser, butiker eller vyer anger du **[!UICONTROL Store View]** i butiksvyn där du vill använda den här konfigurationen.

1. I avsnittet _[!UICONTROL Merchant Location]_&#x200B;väljer du **[!UICONTROL Merchant Country]**&#x200B;där ditt företag finns.

   Den här inställningen bestämmer valet av PayPal-lösningar som visas i konfigurationen.

   ![Handelsland](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Expandera **[!UICONTROL PayPal Payment Gateways]** (om det behövs) och klicka på **[!UICONTROL Configure]** för **[!UICONTROL Payflow Pro]**.

   ![Konfigurera - Payflow Pro](./assets/payflow-pro.png){width="600" zoomable="yes"}

### Steg 2: Slutför de obligatoriska PayPal-inställningarna

![Obligatoriska inställningar - PayPal Payflow Pro](./assets/payflow-pro-required-a.png){width="600" zoomable="yes"}

1. (Valfritt) Ange **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >E-postadresser är skiftlägeskänsliga. För att kunna ta emot betalning måste e-postadressen matcha den e-postadress som har angetts i PayPal-handelskontot.

1. Ange en av följande autentiseringsuppgifter som du använder för att logga in på ditt PayPal-handelskonto:

   - **[!UICONTROL Partner]** - Ditt PayPal Partner-ID.
   - **[!UICONTROL User]** - Om du konfigurerar en eller flera ytterligare användare för kontot är det här värdet ID:t för den användare som har behörighet att bearbeta transaktioner. Om du inte har konfigurerat ytterligare användare har **[!UICONTROL USER]** samma värde som **[!UICONTROL Vendor]**.
   - **[!UICONTROL Vendor]** - Ditt inloggnings-ID för handlare skapades när du registrerade dig för kontot.

1. Ange **[!UICONTROL Password]** som är associerad med ditt PayPal-konto.

1. Om du vill köra testtransaktioner anger du **[!UICONTROL Test Mode]** till `Yes`.

   När du testar konfigurationen i en sandlåda ska du bara använda [kreditkortsnummer][3] som rekommenderas av PayPal. När du är redo att börja producera återgår du till konfigurationen och ställer in testläget på `No`.

1. Om systemet använder en proxyserver för att upprätta anslutningen till PayPal-systemet anger du **[!UICONTROL Use Proxy]** till `Yes` och gör följande:

   - Ange IP-adressen för **[!UICONTROL Proxy Host]**.

   - Ange portnumret för **[!UICONTROL Proxy Port]**.

     En proxy används när serverns brandvägg förhindrar direktåtkomst till PayPal-servern. I så fall används en tredjepartsserver för att vidarebefordra trafik.

1. Ange **[!UICONTROL Enable this Solution]** till `Yes`.

1. Om du vill erbjuda dina kunder [PayPal-kredit](paypal.md#paypal-credit-and-pay-later) anger du **[!UICONTROL Enable PayPal Credit]** till `Yes`.

1. Om du vill lagra information om kundbetalningar/kreditkort på ett säkert sätt, så att kunderna inte behöver ange betalningsinformation igen varje gång, anger du **[!UICONTROL Vault Enabled]** till `Yes`.

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

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) för de återstående avsnitten och upprepa föregående steg för inställningarna för startsidan:

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### Annonsera PayPal PayLater

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Advertise PayPal PayLater]**.

1. Ange **[!UICONTROL Enable PayPal PayLater]** till `Yes`.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Home Page]**.

   ![Annonsera inställningar för startsidan för PayPal-kredit](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

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

1. Expandera ![Expanderingsväljaren](../assets/icon-display-expand.png) för de återstående avsnitten och upprepa föregående steg:

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### Steg 4: Slutför de grundläggande inställningarna

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Basic Settings - PayPal Payflow Pro]**.

   ![Grundinställningar - PayPal Payflow Pro_](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-basic-settings.png){width="600" zoomable="yes"}

1. För **[!UICONTROL Title]** anger du en titel som identifierar PayPal Payflow Pro under utcheckningen.

   Vi rekommenderar att du använder titeln _Debit eller Credit Card_.

1. Om du erbjuder flera betalningsmetoder anger du ett nummer för **[!UICONTROL Sort Order]** för att bestämma i vilken ordning Payflow Pro ska visas när det listas med de andra betalningsmetoderna.

   Det här talet är relativt till de andra betalningsmetoderna. (`0` = först, `1` = sekund, `2` = tredje o.s.v.)

1. Ange **[!UICONTROL Payment Action]** till något av följande:

   - `Authorization` - Godkänner köpet och spärrar pengarna. Beloppet dras inte tillbaka förrän handlaren har tagit det.
   - `Sale` - Köpbeloppet är auktoriserat och dras omedelbart tillbaka från kundens konto.

1. För **[!UICONTROL Credit Card Settings]** väljer du de kreditkort som du godkänner för betalning i din butik.

   Om du vill markera flera kort håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på vart och ett av dem.

   >[!NOTE]
   >
   >American Express kräver ett extra avtal.

### Steg 5: Slutför de avancerade inställningarna

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Advanced Settings]**.

   ![Avancerade inställningar - PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-advanced-settings.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Payment Applicable From]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här betalningsmetoden.
   - `Specific Countries` - När du har valt det här alternativet visas listan _[!UICONTROL Payment from Specific Countries]_. Håll ned Ctrl-tangenten (PC) eller Kommando-tangenten (Mac) och markera varje land i listan där kunderna kan göra inköp från din butik.

1. Om du vill skriva kommunikation med betalningssystemet till loggfilen anger du **[!UICONTROL Debug Mode]** till `Yes`.

   >[!NOTE]
   >
   >I enlighet med PCI-datasäkerhetsstandarder registreras inte kreditkortsinformation i loggfilen.

1. Ange **[!UICONTROL Enable SSL Verification]** till `Yes` om du vill aktivera verifiering av värdautenticitet.

1. Ange **[!UICONTROL Require CVV Entry]** till `Yes` om du vill att kunderna ska ange en CVV-kod.

1. Fyll i följande avsnitt efter behov:

   - [Inställningar för CVV och AVS](#cvv-and-avs-settings)
   - [Inställningar för kvittningsrapport](#settlement-report-settings)
   - [Frontend Experience Settings](#frontend-experience-settings)

#### Inställningar för CVV och AVS

Ange hur olika scenarier ska hanteras för att avgöra när en transaktion ska avvisas när adressverifieringssystemet identifierar en avvikelse.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL CVV and AVS Settings]**.

   ![Inställningar för CVV och AVS - PayPal Payflow Pro](./assets/payflow-pro-cvv-avs.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL AVS Street Does Not Match]** till `Yes` om du vill avvisa en transaktion som baseras på en felmatchad gatufelmatchning.

1. Om du vill avvisa en transaktion baserat på ett felaktigt matchat postnummer anger du **[!UICONTROL AVS Zip Does Not Match]** till `Yes`.

1. Om du vill avvisa en transaktion baserat på en felaktig matchning av en lands-ID anger du **[!UICONTROL International AVS Indicator Does Not Match]** till `Yes`.

1. Om du vill avvisa en transaktion baserat på en felaktig CVV-kod anger du **[!UICONTROL International Card Security Code Does Not Match]** till `Yes`.

#### Inställningar för kvittningsrapport

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Settlement Report Settings]**.

   ![Inställningar för kvittningsrapport - PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Gör följande för **[!UICONTROL SFTP Credentials]**:

   - Om du har registrerat dig för PayPal Secure FTP-servern anger du följande inloggningsuppgifter för SFTP:

      - Inloggning
      - Lösenord

   - Om du vill köra testrapporter innan du publicerar med Express Checkout på webbplatsen anger du **[!UICONTROL Sandbox Mode]** till `Yes`.

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

Använd Frontend Experience Settings för att välja vilka PayPal-logotyper som ska visas på er webbplats och för att anpassa utseendet på PayPals handlarsidor.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Frontend Experience Settings]**.

   ![Frontend Experience Settings - PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

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

### Steg 6: Slutför de grundläggande inställningarna för PayPal Express Checkout

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Basic Settings - PayPal Express Checkout]**.

   ![Grundläggande inställningar för Express Checkout](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. För **[!UICONTROL Title]** anger du en titel som identifierar betalningsmetoden vid utcheckning.

   Du bör ange titeln till _PayPal_ för varje butiksvy.

1. Om du erbjuder flera betalningsmetoder anger du ett nummer för **[!UICONTROL Sort Order]** för att bestämma i vilken ordning som PayPal Express Checkout ska visas när den visas tillsammans med andra betalningsmetoder.

   Det här talet är relativt till de andra betalningsmetoderna. (`0` = först, `1` = sekund, `2` = tredje o.s.v.)

1. Ange **[!UICONTROL Payment Action]** till något av följande:

   - `Authorization` - Godkänner köpet och spärrar pengarna. Beloppet dras inte tillbaka förrän det _har hämtats_ av handlaren.
   - `Sale` - Köpbeloppet är auktoriserat och dras omedelbart tillbaka från kundens konto.

1. Om du vill visa knappen _[!UICONTROL Check out with PayPal]_&#x200B;på produktsidan anger du **[!UICONTROL Display on Product Details Page]**&#x200B;till `Yes`.

### Steg 7: Slutför de avancerade inställningarna för PayPal Express Checkout

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Advanced Settings]**.

   ![Avancerad inställning för Express Checkout](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Display on Shopping Cart]** till `Yes`.

1. Ange **[!UICONTROL Payment Applicable From]** till något av följande:

   - `All Allowed Countries` - Kunder från alla länder som anges i din butikskonfiguration kan använda den här betalningsmetoden.
   - `Specific Countries` - När du har valt det här alternativet visas listan _[!UICONTROL Payment from Specific Countries]_. Om du vill markera flera länder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje objekt.

1. Om du vill skriva kommunikation med betalningssystemet till loggfilen anger du **[!UICONTROL Debug Mode]** till `Yes`.

   >[!NOTE]
   >
   >I enlighet med PCI-datasäkerhetsstandarder registreras inte kreditkortsinformation i loggfilen.

1. Ange **[!UICONTROL Enable SSL Verification]** till `Yes` om du vill aktivera verifiering av värdautenticitet.

1. Om du vill visa en fullständig sammanfattning av kundorder per radobjekt från PayPal-webbplatsen anger du **[!UICONTROL Transfer Cart Line Items]** till `Yes`.

1. Om du vill att kunden ska kunna slutföra transaktionen från PayPal-webbplatsen utan att gå tillbaka till din butik för ordergranskning anger du **[!UICONTROL Skip Order Review Step]** till `Yes`.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

### Steg 8: Lägg till Google reCAPTCHA

Aktivera Google reCAPTCHA för att bättre skydda utcheckningen av PayPal Payflow Pro. Det innehåller alternativ för att köra reCAPTCHA med ett klickbart gränssnitt eller en osynlig kontroll för att validera kunden. Det osynliga alternativet rekommenderas för att öka konverteringen och skydda din butik. Mer information finns i [Google reCAPTCHA](../systems/security-google-recaptcha.md).

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/integration-guide/configure-hosted-checkout/#configuring-hosted-pages-using-paypal-manager
