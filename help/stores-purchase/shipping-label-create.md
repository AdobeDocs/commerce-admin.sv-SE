---
title: Skapa etiketter och paket
description: Lär dig hur du paketerar artiklar i en beställning och skapar leveransetiketter.
exl-id: ed9be72a-0dcd-4dbf-82ba-b1d75a1e76fd
feature: Shipping/Delivery, Orders
source-git-commit: be8a4e9d7cbcf34452724f8055980007794f525f
workflow-type: tm+mt
source-wordcount: '1944'
ht-degree: 0%

---

# Skapa leveransetiketter

Om du vill skapa etiketter för frakt måste du först skapa ett fraktförares konto som stöder etiketter. Följ sedan instruktionerna för att ange en beskrivning av paketet och dess innehåll.

När du har konfigurerat etikettinformationen för frakt och skickat en beställning ansluter Commerce till transportföretagets system, skickar en beställning och får en fraktsetikett och ett spårningsnummer. Om det finns en leveransetikett för den här leveransen i systemet ersätts den med en ny. Befintliga spårningsnummer ersätts dock inte. Alla nya spårningsnummer läggs till i det befintliga.

## Steg 1: Kontakta dina fraktfirmor

Innan du börjar kontrollerar du att leveranskontona är inställda på processetiketter. Vissa transportföretag kan ta ut en extra avgift för att lägga till etiketter till ditt konto.

Kontakta varje fraktfirma som du använder för att aktivera leveransetiketter för din butik.

Följ instruktionerna från respektive fraktfirma för att lägga till stöd för leveransetiketter till ditt konto.

- **FedEx** - Kontakta [FedEx Web Integration Services][1] om du vill veta mer om etikettutskriftskraven för ditt konto.
- **USPS** - Läs [API-portalen för webbverktyg][4] i supportcentret för Shipper om du vill veta hur du ställer in etikettens utskriftsautentiseringsuppgifter.
- **UPS**- Kontakta [UPS][2] för att bekräfta att ditt konto har stöd för etiketter för leverans. Om du vill generera leveransetiketter måste du använda alternativet UPS XML.
- **DHL** - Kontakta [DHL eCommerce Solutions][3] om du vill veta mer om kraven för etikettutskrift för ditt konto.

## Steg 2: Uppdatera konfigurationen för varje transportföretag

1. Kontrollera att din [Store-information](../getting-started/store-details.md#store-information) är fullständig.

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_&#x200B;Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Shipping Settings]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Origin]** och konfigurera **[!UICONTROL Shipping Origin Address]**.

1. Följ instruktionerna nedan för varje transportföretagskonto som aktiveras för etikettutskrift.

### UPS-konfiguration

United Parcel Service levererar både internt och internationellt. Leveransetiketter kan bara genereras för leveranser som har sitt ursprung i USA.

1. Välj _[!UICONTROL Sales]_&#x200B;i avsnittet **[!UICONTROL Delivery Methods]**&#x200B;i den vänstra panelen.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL UPS]**.

1. Kontrollera att din UPS **[!UICONTROL Shipper Number]** är korrekt.

   Ditt leveransnummer visas bara när [!DNL United Parcel Service XML] är aktiverat.

1. Klicka på **[!UICONTROL Save Config]**.

### USPS-konfiguration

[!DNL United States Postal Service] levereras både nationellt och internationellt.

{{$include /help/_includes/usps-api-type-configuration-note.md}}

1. Expandera **[!UICONTROL Delivery Methods]**-expanderingsväljaren ![&#x200B; i avsnittet &#x200B;](../assets/icon-display-expand.png) i **[!UICONTROL USPS]**-konfigurationen.

1. Välj **[!UICONTROL USPS Type]** som `USPS Rest APIs` eller `USPS Web Tools API`.

1. Kontrollera att **[!UICONTROL Secure Gateway URL]** är korrekt.

1. Ange **[!UICONTROL Password]** som du fått från USPS.

1. Kontrollera att följande konfiguration är klar baserat på vald **[!UICONTROL USPS Type]**:

   Om du använder USPS Web Tools API:
   - Användar-ID
   - Lösenord

   Om du använder USPS REST API:er:
   - Konsumentnyckel
   - Konsumenthemlighet
   - Prisalternativ
   - Kontotyp
   - Kontonummer
   - Kundregistrerings-ID (CRID)
   - Mailer Identifier (MID)
   - Manifest MID
   - AES/ITN

1. Ange **[!UICONTROL Size]** till `Large` och ange värden för följande dimensioner:

   - Längd
   - Bredd
   - Höjd
   - Girth

1. Klicka på **[!UICONTROL Save Config]**.

### FedEx-konfiguration

FedEx levererar nationellt och internationellt. Lager utanför USA kan endast skapa FedEx-etiketter för internationella leveranser.

1. Expandera **[!UICONTROL Delivery Methods]**-expanderingsväljaren ![&#x200B; i avsnittet &#x200B;](../assets/icon-display-expand.png) i **[!UICONTROL FedEx]**-konfigurationen.

1. Kontrollera att följande FedEx-autentiseringsuppgifter är korrekta:

   - Mätarnummer
   - Nyckel
   - Lösenord

1. Klicka på **[!UICONTROL Save Config]**.

### DHL-konfiguration

DHL tillhandahåller internationella sjöfartstjänster.

1. Expandera **[!UICONTROL Delivery Methods]**-expanderingsväljaren ![&#x200B; i avsnittet &#x200B;](../assets/icon-display-expand.png) i **[!UICONTROL DHL]**-konfigurationen.

1. Kontrollera att **[!UICONTROL Gateway URL]** är korrekt.

1. Kontrollera att följande autentiseringsuppgifter är fullständiga:

   - Åtkomst-ID
   - Lösenord
   - Kontonummer

1. Klicka på **[!UICONTROL Save Config]**.

## Steg 3: Skapa etiketter för frakt

### Metod 1: Skapa etikett för ny leverans

1. Gå till _>_ på sidofältet **[!UICONTROL Sales]** Admin **[!UICONTROL Orders]**.

1. Leta reda på ordningen i rutnätet och öppna posten.

   Orderns status måste vara antingen `Pending` eller `Processing`.

1. Klicka på **[!UICONTROL Ship]** i det övre högra hörnet.

1. Bekräfta leveransinformationen enligt transportföretagets krav.

1. Markera kryssrutan **[!UICONTROL Create Shipping Label]** i det nedre högra hörnet.

1. Klicka på **[!UICONTROL Submit Shipment]**.

1. Lägg till eller uppdatera produkter i paketet:

   - Om du vill lägga till produkter från ordningen i paketet klickar du på **[!UICONTROL Add Products]**. Kolumnen _[!UICONTROL Quantity]_&#x200B;visar det maximala antalet produkter som är tillgängliga för paketet.

   - Markera kryssrutan för varje produkt som ska läggas till i paketet och ange **[!UICONTROL Quantity]** för varje produkt. Klicka sedan på **[!UICONTROL Add Selected Product(s) to Package]**.

   - Klicka på **[!UICONTROL Add Package]** om du vill lägga till ett paket.

   - Klicka på **[!UICONTROL Delete Package]** om du vill ta bort ett paket.

   - Om du vill avbryta en beställning klickar du på **[!UICONTROL Cancel]**. Ingen leveransetikett har skapats och kryssrutan _[!UICONTROL Create Shipping Label]_&#x200B;har tagits bort.

   >[!NOTE]
   >
   >Om du använder en annan pakettyp än standardtypen eller kräver en signatur kan leveranskostnaden skilja sig från den du har debiterat kunden. Eventuella skillnader i leveranskostnaden framgår inte av butiken.

1. Klicka på **[!UICONTROL OK]**.

   Commerce ansluter till transportföretagets system, skickar beställningen och får en etikett och ett spårningsnummer för varje paket.

### Metod 2: Skapa etikett för befintlig leverans

1. Gå till _>_ > **[!UICONTROL Sales]** på sidofältet _[!UICONTROL Operations]_&#x200B;Admin **[!UICONTROL Orders]**.

1. Hitta beställningen i rutnätet och öppna leveransformuläret.

1. Klicka på _[!UICONTROL Shipping and Tracking Information]_&#x200B;i avsnittet **[!UICONTROL Create Shipping Label]**.

1. Distribuera de beställda produkterna till rätt paket och klicka på **[!UICONTROL OK]**.

1. Klicka på **[!UICONTROL Show Packages]** om du vill granska paketinformationen.

## Steg 4: Skriv ut etiketterna

Leveransetiketter genereras i PDF-format och kan skrivas ut från administratören. Varje etikett innehåller ordernummer och paketnummer.

>[!NOTE]
>
>Eftersom en enskild leveransorder skapas för varje paket kan flera fraktsetiketter tas emot för en enskild leverans.

### Metod 1: Skriv ut etikett från utleveransformulär

1. Gå till någon av följande sidor på _Admin-sidlisten_ och leta sedan reda på försändelseposten:

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - Hitta ordningen i rutnätet och öppna posten. Välj **[!UICONTROL Shipments]** på den vänstra panelen. Öppna sedan försändelseposten.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Hitta leveransen i rutnätet och öppna posten.

1. Om du vill hämta PDF-filen går du till avsnittet _[!UICONTROL Shipping and Tracking]_&#x200B;i formuläret och klickar på&#x200B;**[!UICONTROL Print Shipping Label]**.

   Beroende på inställningarna i webbläsaren kan etiketterna visas och skrivas ut direkt från PDF-filen.

   Knappen _[!UICONTROL Print Shipping Label]_&#x200B;visas bara efter att transportören har genererat etiketter för leveransen. Om knappen saknas klickar du på&#x200B;**[!UICONTROL Create Shipping Label]**. Knappen visas när Commerce har tagit emot etiketten från transportören.

### Metod 2: Skriv ut etiketter för flera order

1. Gå till någon av följande sidor på sidofältet _Admin_ och välj sedan beställningar eller leveranser för utskrift:

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - I rutnätet markerar du kryssrutan för varje order med leveransetiketter som ska skrivas ut.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Markera kryssrutan för varje leverans med etiketter som ska skrivas ut i rutnätet.

1. Ställ in kontrollen **[!UICONTROL Actions]** på `Print Shipping Labels`.

1. Klicka på **[!UICONTROL Submit]**.

En fullständig uppsättning fraktsetiketter skrivs ut för varje leverans som är relaterad till de valda beställningarna.

## Obligatoriska inställningar för bärare

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Type] | Pakettyperna skiljer sig åt beroende på transportör och metod. Standardpakettypen för varje bärare väljs från början. USPS kräver inte pakettypen för inhemska leveranser. |
| [!UICONTROL Customs Value] | (Endast internationella transporter) Det deklarerade värdet eller försäljningspriset för innehållet i en internationell transport. |
| [!UICONTROL Total Weight] | Den totala vikten för alla produkter som läggs till i paketet beräknas automatiskt. Värdet kan också ändras manuellt och anges som pund eller kilogram. |
| [!UICONTROL Length, Width, Height] | (Valfritt) Paketdimensionerna används endast för anpassade paket. Du kan ange måttenheter som tum eller centimeter.<br/><br/>**[!UICONTROL Not Required]**: Fraktbolaget har inte skickat någon bekräftelse på leveransen till butiken.<br/><br/>**[!UICONTROL No Signature]**: Leveransbekräftelse utan mottagarens signatur skickas till butiken av fraktfirman.<br/><br/>**[!UICONTROL Signature Required]**: Transportföretaget får mottagarens signatur och förser butiken med en utskriven kopia.<br/><br/>**[!UICONTROL Direct]**: (Endast FedEx) FedEx hämtar en signatur från någon på leveransadressen. Om ingen kan signera för paketet försöker fraktfirman leverera paketet vid ett annat tillfälle.<br/><br/>**[!UICONTROL Indirect]**: (Endast FedEx-leveranser för boende) FedEx hämtar signaturen för någon (eventuellt en granne eller byggnadschef) på leveransadressen. Mottagaren kan lämna en signerad FedEx-dörrtagg för att godkänna att paketet lämnas utan att någon är närvarande för att signera det.<br/><br/>**[!UICONTROL Contents]**: (Endast USPS) Välj en av följande beskrivningar av paketet: <br/>- Gift<br/>- Documents<br/>- Commercial Sample<br/>- Returned Goods<br/>- Merchandise<br/>- Other <br/><br/>**[!UICONTROL Explanation]**: (Endast USPS) En detaljerad beskrivning av paketets innehåll.<br/><br/>**[!UICONTROL Adult Required]**: Transportföretaget får en vuxenmottagares signatur och förser butiken med en utskriven kopia. |

{style="table-layout:auto"}

## Skapa paket

Fönstret _[!UICONTROL Create Packages]_&#x200B;visas när du väljer att skapa en leveransetikett. Du kan börja konfigurera det första paketet omedelbart.

### Konfigurera ett paket

>[!NOTE]
>
>Om du väljer ett icke-standardvärde för [!UICONTROL Type] eller väljer att kräva en signaturbekräftelse, kan priset på en leverans skilja sig från det du debiterade kunden.

1. Om du vill visa en lista över levererade produkter och lägga till dem i paketet klickar du på **[!UICONTROL Add Products]**.

   - Ange produkter och kvantiteter.

     Kolumnen _[!UICONTROL Qty]_&#x200B;visar den maximala kvantitet som är tillgänglig att lägga till. För den första förpackningen är numret den totala kvantiteten av produkten som ska levereras.

   - Klicka på **[!UICONTROL Add Selected Product(s) to Package]** om du vill lägga till produkterna i paketet.

1. Klicka på **[!UICONTROL Add Package]** om du vill lägga till ett paket.

   Du kan lägga till flera paket och redigera dem samtidigt.

1. Klicka på **[!UICONTROL Delete Package]** om du vill ta bort ett paket.

När produkterna har lagts till i paketet kan kvantiteten inte redigeras direkt.

### Öka kvantiteten

1. Klicka på **[!UICONTROL Add Selection]**.

1. Ange den ytterligare kvantiteten.

   Numret läggs till den tidigare kvantiteten av produkten i paketet.

### Minska kvantiteten

1. Ta bort produkten från paketet.

1. Klicka på **[!UICONTROL Add Selection]**.

1. Ange det nya, mindre värdet.

### Generera fraktsetiketter

När du har distribuerat alla produkter är det totala antalet paket som du kommer att använda lika med antalet för det sista paketet i listan. Knappen _OK_ inaktiveras tills alla levererade artiklar distribueras till paket och all nödvändig information är slutförd.

Klicka på **[!UICONTROL OK]** om du vill generera etiketterna.

Om det behövs kan du klicka på **[!UICONTROL Cancel]** för att stoppa processen. Paketen sparas inte och leveransetikettprocessen avbryts.

### Fältbeskrivningar

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Type] | Anger typen av paket. Välj ett av de fördefinierade värdena. De tillgängliga pakettyperna är olika för varje fraktfirma. När popup-fönstret Skapa paket öppnas visas standardpaketet för transportföretaget i fältet Typ. Om du väljer ett paket som inte är utformat av en fraktfirma måste du ange paketets mått. För leveransetiketter som skapats för DHL-, FedEx- och UPS-leveranser anges fältet Typ av varor till `Merchandise`. För USPS visar fältet värdet från fältet _Contents_ i fönstret _[!UICONTROL Create Packages]_. |
| [!UICONTROL Total Weight] | Paketets totala vikt. Fältet är förifyllt med den totala vikten av produkter i ett paket. Måttenheten kan anges till antingen pund eller kilo. |
| [!UICONTROL Length] | Längden på ett paket, ett heltal och flyttal. Fältet aktiveras om den anpassade pakettypen används. Måttenheten kan anges till antingen tum eller centimeter. |
| [!UICONTROL Width] | Bredden på ett paket, heltal och flyttal. Fältet aktiveras om den anpassade pakettypen används. Måttenheterna kan anges i listrutan bredvid fältet Höjd. Välj mellan tum och centimeter. |
| [!UICONTROL Height] | Höjden på ett paket, ett heltal och flyttal. Fältet aktiveras om den anpassade pakettypen används. Måttenheterna kan anges i listrutan bredvid fältet Höjd. Välj mellan tum och centimeter. |
| [!UICONTROL Signature] | Definierar leveransbekräftelse. Alternativ:<br/><br/>**[!UICONTROL Not Required]**: Inget leveransbekräftelsemeddelande skickas till dig.<br/><br/>**[!UICONTROL No Signature]**: Ett leveransbekräftelsemeddelande utan en mottagares signatur skickas till dig.<br/><br/>**[!UICONTROL Signature Required]**: Leveransföretaget får mottagarens signatur och förser dig med den utskrivna kopian.<br/><br/>**[!UICONTROL Adult Required]**: Transportföretaget får den vuxenmottagarens signatur och förser dig med den utskrivna kopian.<br/><br/>**[!UICONTROL Direct (FedEx only)]**: FedEx hämtar en signatur från någon på leveransadressen och försöker leverera igen om ingen kan signera för paketet.<br/><br/>**[!UICONTROL Indirect (FedEx only)]**: FedEx får en signatur på något av följande tre sätt: <br/>(1) från någon på leveransadressen; <br/>(2) från en granne, byggnadschef eller annan person på adressen; eller <br/>(3) kan mottagaren lämna en signerad FedEx-dörrtagg som godkänner att paketet släpps utan någon närvarande. Endast tillgängligt för leveranser på bostäder. Alternativen kan variera något för olika fraktsätt. Den senaste informationen finns i transportföretagets resurser. |
| [!UICONTROL Contents] | (Endast tillgängligt för USPS-leveranser) Beskrivning av paketets innehåll. Alternativ: `Gift` / `Documents` / `Commercial Sample` / `Returned Goods` / `Merchandise` / `Other` |
| [!UICONTROL Explanation] | (Endast USPS-leveranser) Detaljerad beskrivning av paketets innehåll. |

{style="table-layout:auto"}

[1]: https://www.fedex.com/en-us/api/get-support.html
[2]: https://www.ups.com/us/en/support/contact-us.page
[3]: https://www.dhl.com/us-en/home/our-divisions/ecommerce-solutions.html
[4]: https://www.usps.com/business/web-tools-apis/#ssc

<!-- Last updated from includes: 2025-10-29 05:34:15 -->
