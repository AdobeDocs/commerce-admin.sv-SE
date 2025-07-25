---
title: Moms (moms)
description: '&lt;Lägg till beskrivning här&gt;'
exl-id: 20dbcb86-e558-47f2-968d-b5c9ec5f665b
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1990'
ht-degree: 0%

---

# Moms (moms)

Vissa länder tar ut mervärdesskatt på varor och tjänster. Det kan finnas olika momssatser beroende på vilket stadium i tillverknings- eller distributionsprocessen, material eller tjänster du säljer till dina kunder. Du kan tillämpa mer än en momssats för att korrekt beräkna den skatt som ska betalas.

Commerce kan konfigureras att debitera en mervärdesskatt baserat på antingen handlarens eller kundens adress, om båda finns i samma land. Momsberäkningarna baseras vanligtvis på försändelsens destination, i stället för dess ursprungsplats. I de flesta fall räcker det med en konfigurationsinställning som beräknar moms baserat på kundens leveransadress.

## Exempel på scenarier

- För en momsregistrerad verksamhet i ett EU-land som levererar varor till en privatperson i ett annat EU-land beräknas momsen som&quot;distansförsäljning&quot; baserad på var handlaren befinner sig.

- Ett företag i Nederländerna som gör ett inköp från en butik i Storbritannien som levererar till en adress i Storbritannien måste betala momssatserna i Storbritannien.

- För försäljning av [nedladdningsbara produkter](../catalog/product-create-downloadable.md), eller _digitala varor_, baseras momssatsen på leveransmålet i stället för på försäljningsstället. Se [Plats för leverans av digitala varor](taxes.md#place-of-supply-for-digital-goods-eu).

>[!TIP]
>
>Vissa gränsöverskridande leveranser och B2B-leveranser har mer komplexa skattekrav. Om du vill utöka de inbyggda funktionerna i din Commerce-installation kan du lägga till en skattehanteringslösning från [Marketplace](https://marketplace.magento.com/extensions/accounting-finance/taxes.html).

## Konfigurera moms

Följande instruktioner innehåller ett exempel på hur man lägger upp 20 % moms i Storbritannien för försäljning till detaljhandelskunder. För andra skattesatser och länder ska du följa det allmänna förfarandet men ange specifik information som motsvarar ditt land, momssats, kundtyp osv.

>[!NOTE]
>
>Innan du fortsätter måste du ta reda på vilka regler och bestämmelser som gäller för moms i ditt område.

I vissa affärstransaktioner görs ingen uppskattning av moms. Commerce kan validera en kunds moms-ID för att säkerställa att momsen utvärderas (eller inte utvärderas) korrekt. Se [moms-ID-validering](#vat-id-validation).

### Steg 1: Ställ in kundmomsklasser

Processen med att skapa en momsregel börjar med att lägga till en skattesats.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**&#x200B;på sidofältet_ Admin _.

   ![Konfigurera kundmomsklasser](./assets/vat-zones.png){width="600" zoomable="yes"}

1. Se till att det finns en lämplig kundskatteklass att använda med momsen.

   I det här exemplet måste du se till att det finns en kundmomsklass med namnet _Detaljkund_. Om den här skatteklassen inte finns klickar du på **[!UICONTROL Add New Tax Rate]**.

1. Ange **[!UICONTROL Tax Identifier]** som ny momsklass.

   Alla momssatser visas i fältet _Momssats_ i _Information om momsregel_ när du skapar momsregler.

1. Markera kryssrutan **[!UICONTROL Zip/Post is Range]** om du vill ange postnummerintervall (från / till).

1. Välj **[!UICONTROL Country]** där momssatsen gäller.

1. Ange **[!UICONTROL Rate Percent]** som skulle användas för momsberäkning vid köp.

1. Klicka på **[!UICONTROL Save Rate]** när du är klar.

Baserat på den inskickade skattesatsen kan du skapa efterföljande momsregler. I avsaknad av skattesatser blir det omöjligt att skapa skatteregler.

### Steg 2: Ange produktskatteklasser

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add New Tax Rule]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Additional Settings]**.

   ![Ställ in produktskatteklasser](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Add New Tax Class]** under _Produktskatteklass_.

1. Om du vill lägga till den nya klassen i listan över tillgängliga produktskatteklasser och skapa tre nya klasser anger du den nya klassen **[!UICONTROL Name]** och klickar på bockmarkeringen:

   - `VAT Standard`
   - `VAT Reduced`
   - `VAT Zero`

1. Klicka på **[!UICONTROL Save Class]** för varje ny klass som du lägger till.

1. Klicka på **[!UICONTROL Save Rule]**.

### Steg 3: Ange momszoner och skattesatser

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**&#x200B;på sidofältet_ Admin _.

   I det här exemplet kan du ta bort amerikanska skattesatser eller låta dem vara som de är.

1. Klicka på **[!UICONTROL Add New Tax Rate]**.

   ![Ställ in momszoner och skattesatser](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

1. Definiera nya priser enligt följande:

   **Momsstandard**

   - Skatteidentifierare: `VAT Standard`
   - Land och stat: `United Kingdom`
   - Frekvens i procent: `20.00`

   **Moms reducerad**

   - Skatteidentifierare: `VAT Reduced`
   - Land och stat: `United Kingdom`
   - Frekvens i procent: `5.00`

1. Klicka på **[!UICONTROL Save Rate]** för varje frekvens.

### Steg 4: Ange momsregler

En momsregel är en kombination av en kundskatteklass, en produktskatteklass och en momssats.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**&#x200B;på sidofältet_ Admin _.

1. Lägg till nya momsregler enligt följande:

   **Momsstandard**

   - Namn: `VAT Standard`
   - Kundmomsklass: `Retail Customer`
   - Produktskatteklass: `VAT Standard`
   - Momssats: `VAT Standard Rate`

   **momsen reducerad**

   - Namn: `VAT Reduced`
   - Kundmomsklass: `Retail Customer`
   - Produktskatteklass: `VAT Reduced`
   - Momssats: `VAT Reduced Rate`

1. Klicka på **[!UICONTROL Save Rule]** för varje frekvens.

### Steg 5: Använd momsklasser på produkter

1. Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Manage Products]** på sidofältet _Admin_.

1. Öppna en produkt från katalogen i redigeringsläge.

1. På sidan _Allmänt_ letar du reda på alternativet **[!UICONTROL Tax Class]** och väljer det **[!UICONTROL VAT Class]** som gäller för produkten.

1. Klicka på **[!UICONTROL Save]** när du är klar.

   ![Använd momsklasser på produkter](./assets/vat-apply-classes.png){width="600" zoomable="yes"}

## Fältbeskrivningar

### Butiksinformation

Commerce använder följande [konfigurationsinställningar för lagringsinformation](../configuration-reference/general/general.md#store-information) för att beräkna moms baserat på försäljningsinformation.

**[!UICONTROL VAT Number]** - Momsnumret som är tilldelat handlaren.

**[!UICONTROL Validate VAT Number]** - [momsvalidering](#vat-id-validation) bekräftar att momsregistreringsnumret matchar motsvarande post i databasen [Europeiska kommissionen](https://ec.europa.eu/taxation_customs/vies/).

### Kundinformation

Commerce använder följande fält för att beräkna moms baserat på [kundinformation](../customers/account-dashboard-account-information.md)).

#### Kontoinformation

**[!UICONTROL Tax/VAT Number]** - Om tillämpligt, momsregistreringsnumret eller momsregistreringsnumret som tilldelats kunden.

#### Adresser

**[!UICONTROL VAT Number]** - Om tillämpligt, momsregistreringsnumret som är associerat med en viss fakturerings- eller leveransadress för kunden. För försäljning av [digitala varor](taxes.md#place-of-supply-for-digital-goods-eu) inom EU baseras momsbeloppet på leveransmålet.

### Kundkonto

Commerce använder följande [kundkonfigurationsinställningar](../customers/account-options-new.md) för att beräkna moms.

**[!UICONTROL Show VAT Number on Storefront]** - Anger om fältet för kundens momsregistreringsnummer är inkluderat i adressboken som är tillgänglig i kundkontot.

**[!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID]** - moms-ID är en intern identifierare för kundens momsregistreringsnummer när det används vid momsvalidering. Under momsvalideringen bekräftar Commerce att antalet matchar databasen [Europeiska kommissionen](https://ec.europa.eu/taxation_customs/vies/). Kunder kan automatiskt tilldelas en av de fyra standardkundgrupperna baserat på valideringsresultaten.

## moms-ID-validering

_moms-ID-validering_ beräknar automatiskt den obligatoriska momsen för B2B-transaktioner som äger rum inom EU utifrån handels- och kundens språkområde. Commerce utför validering av moms-ID med webbtjänsterna på servern [Europeiska kommissionen][1].

>[!NOTE]
>
>Momsrelaterade skatteregler påverkar inte andra skatteregler och hindrar inte tillämpningen av andra skatteregler. Endast en momsregel kan användas vid en viss tidpunkt.

- moms tas ut om handlaren och kunden befinner sig i samma EU-land.
- Moms debiteras inte om handlaren och kunden befinner sig i olika EU-länder och båda parterna är EU-registrerade affärsenheter.

Butiksadministratören skapar mer än en standardkundgrupp som automatiskt kan tilldelas till kunden när kontot skapas, adressen skapas eller uppdateras samt checkas ut. Resultatet är att olika skatteregler används för försäljning inom landet (inhemska) och inom EU.

>[!IMPORTANT]
>
>Om du säljer virtuella eller nedladdningsbara produkter som inte kräver frakt, ska momssatsen för en kunds land användas för både försäljning inom unionen och för försäljning på den inhemska marknaden. Skapa ytterligare enskilda momsregler för produktskatteklasser som motsvarar de virtuella produkterna.

### Arbetsflöde för kundregistrering

Om moms-ID-validering är aktiverat föreslås varje kund att ange momsregistreringsnumret efter registreringen. Det är dock bara kunder som är registrerade momsregistreringskunder som förväntas fylla i detta fält.

När kunden har angett momsregistreringsnummer och andra adressfält och väljer att spara, sparar systemet adressen och skickar valideringsbegäran om momsregistreringsnummer till Europeiska kommissionens server. Enligt resultatet av valideringen tilldelas en kund en av standardgrupperna. Den här gruppen kan ändras om en kund eller administratör ändrar momsregistreringsnumret för standardadressen eller ändrar hela standardadressen. Ibland kan gruppen ändras tillfälligt (gruppändringen emuleras) vid en sidutcheckning.

Om den är aktiverad kan du åsidosätta moms-ID-validering för enskilda kunder genom att markera kryssrutan på sidan _[!UICONTROL Customer Information]_.

### Arbetsflöde för kassor

Om en kunds momsvalidering utförs under utcheckningen sparas ID för momsförfrågan och momsförfrågningsdatum i kommentarshistoriken för ordern.

Det systembeteende som gäller för valideringen av moms-ID och kundgruppsändringen under utcheckningen beror på hur inställningarna Validera på varje transaktion och Inaktivera automatisk gruppändring är konfigurerade. I det här avsnittet beskrivs implementeringen av funktionen för validering av moms-ID för utcheckning på klientsidan.

Om kunden använder Google Express Checkout, PayPal Express Checkout eller någon annan extern utcheckningsmetod, utförs utcheckningen helt och hållet på den externa betalningsgatewayens sida. I det här scenariot kan inte inställningen _Validera för varje transaktion_ användas och kundgruppen kan inte ändras under utcheckning.

![Utcheckningsarbetsflöde för momsvalidering](./assets/vat-id-validation2.png){width="550" zoomable="yes"}

### Konfigurera moms-ID-validering

Om du vill konfigurera validering av moms-ID måste du först skapa kundgrupper som behövs och skapa relaterade momsklasser, skattesatser och regler. Aktivera sedan moms-ID-validering för butiken och slutför konfigurationen.

I följande exempel visas hur momsklasser och momssatser används för moms-ID-validering. Granska exemplen och följ sedan instruktionerna för att konfigurera de momsklasser och regler som behövs för din butik.

#### Exempel: Minimala momsregler krävs för validering av moms-ID

| Skatteregel nr 1 |  |
|--- |--- |
| Kundens skatteklass | Kundmomsklasser måste innehålla: <br />En klass för inhemska kunder. <br />En klass för kunder med felaktigt formaterade moms-ID.<br />En klass för kunder vars moms-ID-validering misslyckades. |
| Produktmomsklass | Produktmomsklasser måste innehålla en klass för produkter av alla typer, förutom paket och virtuella. |
| Momssats | Skattesatsen måste inkludera momssatsen för handlarens land. |

{style="table-layout:auto"}

| Skatteregel nr 2 |   |
|--- |--- |
| Kundens skatteklass | En klass för fackliga kunder. |
| Produktmomsklass | En klass för produkter av alla typer, förutom virtuella. |
| Momssats | Momssatser för alla EU-länder, utom handlarens land. För närvarande är den här nivån 0 %. |

{style="table-layout:auto"}

| Skatteregel nr 3 | (Krävs för virtuella och nedladdningsbara produkter) |
|--- |--- |
| Kundens skatteklass | Kundmomsklasser måste innehålla: <br/>En klass för inhemska kunder <br/>En klass för kunder med ogiltigt moms-ID En klass för kunder vars moms-ID-validering misslyckades |
| Produktmomsklass | En klass för virtuella produkter. |
| Momssats | Momssats för handlarens land. |

{style="table-layout:auto"}

| Skatteregel nr 4 | (Krävs för virtuella och nedladdningsbara produkter) |
|--- |--- |
| Kundens skatteklass | En klass för fackliga kunder. |
| Produktmomsklass | En klass för virtuella produkter. |
| Momssats | Momssatser för alla EU-länder, utom handlarens land. För närvarande är den här nivån 0 %. |

{style="table-layout:auto"}

#### Steg 1: Skapa momsrelaterade kundgrupper

moms-ID-validering tilldelar automatiskt en av de fyra standardkundgrupperna till kunder enligt moms-ID-valideringsresultat:

- Hushållsnära
- Intra-EU
- Ogiltigt moms-ID
- Valideringsfel

Du kan skapa kundgrupper för moms-ID-validering eller använda befintliga grupper, om de följer din affärslogik. När du konfigurerar moms-ID-validering måste du tilldela varje kundgrupp som standard till kunder med lämpliga moms-ID-valideringsresultat.

#### Steg 2: Skapa momsrelaterade klasser, priser och regler

Varje momsregel definieras av tre enheter:

- Kundmomsklasser
- Produktmomsklasser
- Momssatser

Skapa [momsreglerna](tax-rules.md) för att effektivt använda moms-ID-validering.

- Momsregler inkluderar momssatser och [momsklasser](tax-class.md).
- Skatteklasser tilldelas [kundgrupper](../customers/customer-groups.md).

#### Steg 3: Aktivera och konfigurera validering av moms-ID

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Ange **[!UICONTROL Store View]** för konfigurationen om det behövs.

1. Expandera **[!UICONTROL Customers]** i den vänstra panelen och välj **[!UICONTROL Customer Configuration]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Create New Account Options]**.

   I följande exempel är de allmänna kundinställningarna som inte är relaterade till momsvalidering nedtonade.

   ![Skapa nya kontoalternativ](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enable Automatic Assignment to Customer Group]** till `Yes` och fyll i följande fält efter behov.

   - **[!UICONTROL Default Group]**
   - **[!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID]**
   - **[!UICONTROL Show VAT Number on Storefront]**

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

#### Steg 4: Ange momsregistreringsnummer och land

1. Expandera **[!UICONTROL General]** i den vänstra panelen och välj **[!UICONTROL General]** under.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Store Information]**.

   ![Lagra information](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. Välj din **[!UICONTROL Country]**.

1. Ange din **[!UICONTROL VAT Number]** och klicka på **[!UICONTROL Validate VAT Number]**.

   Resultatet visas omedelbart.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

#### Steg 5: Verifiera listan över EU-medlemsländer

1. Expandera ![Expanderingsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Countries Options]** på konfigurationssidan _Allmänt_ .

   ![Alternativ för länder](../configuration-reference/general/assets/general-country-options.png){width="600" zoomable="yes"}

1. Kontrollera att varje medlemsland i EU är markerat i listan **[!UICONTROL European Union Countries]**.

   Om du vill ändra standardinställningen avmarkerar du kryssrutan **Använd systemvärden**. Håll ned Ctrl-tangenten (PC) eller Kommando-tangenten (Mac) och klicka på varje land som du vill lägga till eller ta bort.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.


[1]: https://ec.europa.eu/taxation_customs/vies/
