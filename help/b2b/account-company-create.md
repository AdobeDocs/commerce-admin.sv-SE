---
title: Skapa ett företagskonto
description: Läs om hur du skapar företagskonton i Adobe Commerce Admin och i butiken.
exl-id: 8c06395b-102b-4a41-8eb3-e6a344feac70
feature: B2B, Companies, Configuration, Storefront
role: Admin, User
source-git-commit: 2e119bcb8278432bde1c12f3f44a112cde59fb18
workflow-type: tm+mt
source-wordcount: '2444'
ht-degree: 0%

---

# Skapa ett företagskonto

Med företagskonton kan B2B-företag hantera sina inköp, användare och krediter inom Adobe Commerce. I det här avsnittet beskrivs hela processen att skapa, konfigurera och aktivera företagskonton.

## Översikt över att skapa företagskonto

Företagskonton kan skapas på två sätt, som passar olika affärsscenarier:

* **Storefront Registration** - Självbetjäningskontouppgifter från företag
* **Skapa administratör** - Inställningar för försäljningskonton med förkonfigurerad information

Alla företagskonton kräver administratörsgodkännande innan de blir aktiva, vilket säkerställer korrekt kontroll och konfiguration.

## Förutsättningar

Innan du skapar företagskonton måste du se till att följande krav uppfylls:

* **Systemkrav:**
   * [B2B-funktioner är aktiverade](enable-basic-features.md) i din Adobe Commerce-installation
   * Företagsregistrering är aktiverat för att skapa butiker
   * E-postmeddelanden har konfigurerats för arbetsflöden för godkännande

* **Affärskrav:**
   * Processer och riktlinjer för godkännande har fastställts
   * Säljare tilldelas (för konton som skapas av administratörer)
   * Kreditpolicyer definieras (om företagskrediter används)
   * Kundgrupper och delade kataloger har konfigurerats

* **Administrativ åtkomst:**
   * Lämpliga behörigheter för företagsledning
   * Tillgång till kundtjänst och företagsadministration

Systemet tilldelar rollen [företagsadministratör](account-company-admin.md) till den person som ställer in ett företagskonto från butiken. När butiksadministratören har godkänt begäran om att skapa företagskonto i Admin kan företagsadministratören ange ett kontolösenord och logga in på kontot.

## Metod 1: Kunden skapar kontot från butiken

**När den här metoden ska användas:**

* Självbetjäningsregistrering är att föredra
* Kunderna har all nödvändig affärsinformation till hands
* Arbetsflödet för standardgodkännande är tillräckligt
* Ingen särskild konfiguration eller förifyllning krävs

>[!IMPORTANT]
>
>Kontrollera att [B2B-funktionerna](enable-basic-features.md) är aktiverade om du vill ha stöd för den här metoden (så att kunderna kan registrera sitt företag från butiken).

1. I det övre högra hörnet av butikshuvudet klickar kunden på **[!UICONTROL Create an Account]** och väljer **[!UICONTROL Create New Company Account]**.

   ![Skapa nytt företagskonto](./assets/company-account-create-storefront-options.png){width="700" zoomable="yes"}

   >[!NOTE]
   >
   >Om en besökare är inloggad på ett registrerat användarkonto kan de skapa ett företagskonto genom att gå till _[!UICONTROL Customer Profile]_>**[!UICONTROL Company Structure]**>**[!UICONTROL Create a Company Account]**.

1. I avsnittet _[!UICONTROL Company Information]_&#x200B;gör kunden följande:

   * Fyller i de obligatoriska fälten:

      * **[!UICONTROL Company Name]**
      * **[!UICONTROL Company Email]**

   * Fyller i de återstående fälten, beroende på vad som är tillämpligt:

      * **[!UICONTROL Company Legal Name]**
      * **[!UICONTROL VAT/TAX ID]**
      * **[!UICONTROL Reseller ID]**

   ![Företagsinformation](./assets/company-information-storefront.png){width="700" zoomable="yes"}

1. Fyller i obligatoriska fält i avsnittet _[!UICONTROL Legal Address]_.

   * **[!UICONTROL Street Address]**
   * **[!UICONTROL City]**
   * **[!UICONTROL Country]**
   * **[!UICONTROL State/Province]**
   * **[!UICONTROL ZIP/Postal Code]**
   * **[!UICONTROL Phone Number]**

   ![Juridisk adress](./assets/company-legal-address-storefront.png){width="700" zoomable="yes"}

1. Gör följande i avsnittet _[!UICONTROL Company Administrator]_:

   * Anger **[!UICONTROL Email address]** för företagsadministratören.

     E-postadressen till företagsadministratören kan vara samma som företagets e-postadress eller en annan e-postadress. Om du anger en annan e-postadress skapas ett företagsanvändarkonto, förutom företagsadministratörskontot.

   * Anger **[!UICONTROL First Name]** och **[!UICONTROL Last Name]** för företagsadministratören.

   * Fyller i följande fält om du vill:

      * **[!UICONTROL Job Title]**
      * **[!UICONTROL Work Phone Number]**
      * **[!UICONTROL Gender]**

   ![Företagsadministratör](./assets/company-administrator-account-storefront.png)

1. Slutför valideringen om reCAPTCHA är aktiverat för den här butiksfunktionen.

1. När informationen är klar väljer du **[!UICONTROL Submit]**.

   När handlaren godkänner begäran om att skapa ett företagskonto skickas ett e-postmeddelande till företagsadministratören.

   ![Exempel på välkomstmeddelande](./assets/company-admin-welcome-email.png){width="500"}

   När lösenordet har angetts kan företagsadministratören [logga in](../customers/customer-sign-in.md) på kontot.

## Metod 2: Merchant skapar kontot från administratören

**När den här metoden ska användas:**

* Skapande av försäljningskonto rekommenderas
* Förifyll kontoinformation från befintliga affärsrelationer
* Anpassad konfiguration krävs (kreditgränser, specialpris)
* Omedelbar aktivering utan godkännande krävs

Processen att skapa ett företag från Admin är i stort sett densamma som i butiken, men med ytterligare fält.

![Lägg till ett nytt företag från administratören](./assets/company-add-new.png){width="700" zoomable="yes"}

1. Gå till _>_ på sidofältet **[!UICONTROL Customers]** Admin **[!UICONTROL Companies]**.

1. Klicka på **[!UICONTROL Add New Company]** och gör följande:

   * Fyll i dessa obligatoriska fält:

      * **[!UICONTROL Company Name]**
      * **[!UICONTROL Company Email]**

   * Om du inte är redo för att kontot ska börja gälla anger du **[!UICONTROL Status]** till `Pending Approval`. (Inställd på `Active` som standard.)

   * Välj i tillämpliga fall administratörskontot för **[!UICONTROL Sales Representative]** som ska hantera kontot.

1. Gör följande i avsnittet _[!UICONTROL Account Information]_:

   * Fyll i följande fält efter behov:

      * **[!UICONTROL Company Legal Name]**
      * **[!UICONTROL VAT/TAX ID]**
      * **[!UICONTROL Reseller ID]**

   * För **[!UICONTROL Comment]** anger du eventuell ytterligare information om kunden som kan behövas.

     Kommentarerna visas bara från administratören.

   ![Kontoinformation](./assets/company-create-account-information-admin.png){width="700" zoomable="yes"}

1. När du först skapar ett företag visas stödrastret _[!UICONTROL Company Hierarchy]_&#x200B;som tomt när du expanderar det. När du har sparat företaget kan du inkludera det i en företagshierarki. Se [Företagshantering](manage-companies.md).

1. Fyll i följande obligatoriska fält i avsnittet _[!UICONTROL Legal Address]_:

   * **[!UICONTROL Street Address]**
   * **[!UICONTROL City]**
   * **[!UICONTROL Country]**
   * **[!UICONTROL ZIP/Postal Code]**
   * **[!UICONTROL Phone Number]**

1. Gör följande i avsnittet _[!UICONTROL Company Admin]_:

   * Fyll i dessa obligatoriska fält:

      * **[!UICONTROL Email]**
      * **[!UICONTROL First Name]**
      * **[!UICONTROL Last Name]**

   * Fyll i följande valfria delar av namnet, som kan gälla för vissa kundnamn mer än andra och som du kan använda efter eget gottfinnande:

      * **[!UICONTROL Prefix]**
      * **[!UICONTROL Middle Name/Initial]**
      * **[!UICONTROL Suffix]**

   * Om informationen är tillgänglig fyller du i de återstående fälten för att beskriva företagsadministratören:

      * **[!UICONTROL Website]**
      * **[!UICONTROL Job Title]**
      * **[!UICONTROL Work Phone Number]**
      * **[!UICONTROL Gender]**
      * **[!UICONTROL Send Welcome Email From]**

   ![Företagsadministratör](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. I avsnittet _[!UICONTROL Company Credit]_, som visar en sammanfattning av kundens kreditaktivitet, fyller du i så många som möjligt av fälten i den nedre delen av avsnittet:

   * **[!UICONTROL Credit Currency]**
   * **[!UICONTROL Credit Limit]**
   * **[!UICONTROL Allow to Exceed Credit Limit]**
   * **[!UICONTROL Reason for Change]**

   ![Företagskrediter](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

1. Gör följande i avsnittet _[!UICONTROL Advanced Settings]_:

   >[!NOTE]
   >
   >Kundgruppstilldelningen avgör vilken delad katalog som är tillgänglig för företaget och dess anställda. Som standard tilldelas företaget till kundgruppen som konfigurerats som standard.

   * Du kan ändra tilldelningen **[!UICONTROL Customer Group]** för företaget och dess anställda till en grupp som har åtkomst till en annan delad katalog eller till en standardkundgrupp. Du uppmanas att bekräfta innan du ändrar gruppen.

     ![Ändrar kundgruppen](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

   * Om du vill tillåta företagsanställda att generera offerter från sina konton anger du **[!UICONTROL Allow Quotes]** till `Yes`.

   * Om du vill tillåta företagsanställda att skapa och använda inköpsorder från sina konton anger du **[!UICONTROL Enable Purchase Orders]** till `Yes`.

   * Om du vill ändra de **[!UICONTROL Applicable Payment Methods]** som är tillgängliga för företaget avmarkerar du kryssrutan **[!UICONTROL Use config settings]** och väljer något av följande:

     | Alternativ | Beskrivning |
     |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
     | `B2B Payment Methods` | (Standard) Aktiverar alla [betalningsmetoder som angetts som standard](../configuration-reference/general/b2b-features.md#default-b2b-payment-methods) för B2B-order. |
     | `All Enabled Payment Methods` | Gör alla [aktiverade betalningsmetoder](../configuration-reference/sales/payment-methods.md) tillgängliga för kundkonton som är kopplade till företagskontot. |
     | `Selected Payment Methods` | Gör att du kan välja betalningsmetoder som är tillgängliga för kundkonton som är kopplade till företagskontot. Om du vill välja flera betalningsmetoder håller du ned Ctrl (PC) eller Kommando (Mac) och väljer varje alternativ. |

     {style="table-layout:auto"}

   * Om du vill ändra de **[!UICONTROL Applicable Shipping Methods]** som är tillgängliga för företaget avmarkerar du kryssrutan **[!UICONTROL Use config settings]** och väljer något av följande:

     | Alternativ | Beskrivning |
     |--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
     | `B2B Shipping Methods` | (Standard) Aktiverar alla [leveransmetoder som angetts som standard](../configuration-reference/general/b2b-features.md#default-b2b-shipping-methods) för B2B-beställningar. |
     | `All Enabled Shipping Methods` | Gör alla [aktiverade leveransmetoder](../configuration-reference/sales/delivery-methods.md) tillgängliga för kundkonton som är kopplade till företagskontot. |
     | `Selected Shipping Methods` | Gör att du kan välja leveransmetoder som är tillgängliga för kundkonton som är kopplade till företagskontot. Om du vill välja flera leveransmetoder håller du ned Ctrl (PC) eller Kommando (Mac) och väljer varje alternativ. |

     {style="table-layout:auto"}

1. När du är klar väljer du **[!UICONTROL Save]**.

   När begäran om att skapa ett företagskonto godkänns av handlaren skickas ett e-postmeddelande till företagsadministratörens e-postadress.

   När lösenordet har angetts kan företagsadministratören [logga in](../customers/customer-sign-in.md) på kontot.

## Efter att kontot skapats

När ett företagskonto har skapats utförs följande process:

### &#x200B;1. Arbetsflöde för godkännande

* **Väntande status** - Nya konton väntar på administratörsgranskning
* **Granskningsprocess** - Lagra administratörer som verifierar affärsinformation och som godkänner/avvisar begäranden
* **Statusuppdateringar** - Företag får e-postmeddelanden om statusändringar för godkännande

### &#x200B;2. Kontoaktivering

* **Välkomstmeddelande** - Godkända företagsadministratörer får konfigurationsinstruktioner
* **Lösenordskonfiguration** - Administratörer skapar säkra lösenord för kontoåtkomst
* **Inledande inloggning** - Första gången du får tillgång till företagets kontrollpanel och funktioner

### &#x200B;3. Nästa steg för företagsadministratörer

Efter aktiveringen bör företagsadministratörer

* **[Konfigurera företagsstruktur](account-company-structure.md)** - Konfigurera avdelningar och användarhierarki
* **[Hantera företagsanvändare](account-company-users.md)** - Lägg till anställda och tilldela roller
* **[Konfigurera inköpsorder](purchase-order-flow.md)** - Konfigurera arbetsflöden för godkännande vid behov
* **[Granska kreditinställningar](credit-company.md)** - Förstå och hantera företagskrediter (om aktiverat)

## Vanliga problem och felsökning

### Problem med att skapa konto

**Registreringsformuläret kan inte skickas**

* Kontrollera att alla obligatoriska fält är korrekt ifyllda
* Kontrollera att e-postadresserna är giltiga och unika
* Se till att B2B-funktioner är aktiverade och att företagsregistrering är tillåtet
* Rensa webbläsarens cache och försök igen

**Företag finns redan**

* Välj ett unikt företagsnamn
* Kontakta administratören om du tror att detta är ett fel
* Överväg att lägga till plats- eller affärsenhets-ID

**E-postadressproblem**

* Använd e-postadresser i stället för personliga
* Kontrollera att företagets administratörs e-postadress är tillgänglig
* Kontrollera att domänen inte blockeras av e-postfilter

### Problem med godkännande och aktivering

**E-post för godkännande togs inte emot**

* Kontrollera skräppostmappar
* Verifiera att e-postadressen angavs korrekt under registreringen
* Kontakta butiksadministratören om du vill ha en statuskontroll för manuellt godkännande
* Tillåt 24-48 timmar för bearbetning under vardagar

**Det går inte att ange lösenordet efter godkännande**

* Använd den exakta länken i e-postmeddelandet om godkännande
* Kontrollera om aktiveringslänken har upphört att gälla
* Begär ett nytt aktiveringsmeddelande från administratören

**Åtkomstproblem efter aktivering**

* Verifiera att du loggar in via rätt företagskontoportal
* Kontrollera att din kontostatus är &quot;aktiv&quot;
* Kontrollera att du använder företagsadministratörens autentiseringsuppgifter
* Kontakta support om behörigheterna verkar vara felaktiga

## Bästa praxis för säkerhet

När du skapar och hanterar företagskonton:

* **Använd starka lösenord** - Kräv komplexa lösenord för företagsadministratörer
* **Verifiera företagsinformation** - Verifiera företagsinformation under godkännandeprocessen
* **Övervaka kontoaktivitet** - Granska regelbundet åtkomst och behörigheter för företagsanvändare
* **Skydda känsliga data** - Se till att kredit- och finansiell information är korrekt skyddad

## Användargränssnittsreferens för företagskonto

### Knappfält

| Knapp | Beskrivning |
|---------------------------|------------------------------------------------------------------|
| [!UICONTROL Back] | Återgår till sidan Företag utan att spara ändringar. |
| [!UICONTROL Reset] | Återställer originalvärdena till fält som inte har sparats. |
| [!UICONTROL Save] | Sparar ändringar i företaget och håller profilen öppen. |
| [!UICONTROL Save & Close] | Sparar ändringar i företaget och stänger profilen. |

{style="table-layout:auto"}

### Fältbeskrivningar

| Fält | Beskrivning |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Name] | Företagsnamnet anges när företagskontot skapas för första gången och kan vara en förkortad version av det fullständiga juridiska namnet. |
| [!UICONTROL Status] | (Endast administratör) Anger det aktuella tillståndet för företagskontot. Alternativ: <br/>**[!UICONTROL Active]**- Företagskontot har godkänts av butiksadministratören. Företagsadministratören och associerade medlemmar kan logga in kontot från butiken och göra inköp.<br/>**[!UICONTROL Pending Approval]** - En begäran om att öppna ett företagskonto har skickats, men har ännu inte godkänts av butiksadministratören. <br/>**[!UICONTROL Rejected]**- En begäran om att öppna ett företagskonto har skickats, men inte godkänts av butiksadministratören. De inloggningsuppgifter som användes för att skicka begäran blockeras.<br/>**&#x200B; Blockerad &#x200B;**- Företagsmedlemmar kan logga in och komma åt katalogen, men de kan inte göra inköp. Butiksadministratören kan blockera ett företagskonto som inte är i gott skick. Butiksadministratören kan när som helst ta bort blocket på kontot. |
| [!UICONTROL Company Email] | E-postadressen som är associerad med företagskontot. |
| [!UICONTROL Sales Representative] | (Endast administratör) Den Admin-användare som är den primära kontakten för företagskontot. |

{style="table-layout:auto"}

#### [!UICONTROL Account Information]

| Fält | Beskrivning |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | Företagets officiella, fullständiga namn. |
| [!UICONTROL VAT / TAX ID] | [Moms](../stores-purchase/vat.md)-numret som tilldelas företaget av vissa jurisdiktioner för momsrapportering. Information om hur du konfigurerar kundens moms-/momsregistreringsnummer så att det visas i butiken finns i [Skapa nya kontoalternativ](../configuration-reference/customers/customer-configuration.md). <br/> **_Obs!:_** Företagsadministratören och andra företagsanvändare har inte sina egna separata momsregistreringsnummer i sina kundkonton. |
| [!UICONTROL Reseller ID] | Återförsäljningsnumret som har tilldelats företaget för momsrapportering. |
| [!UICONTROL Comment] | (Endast admin) Anteckningarna om företagskontot är till för referens och visas bara från administratören. |

{style="table-layout:auto"}

#### [!UICONTROL Company Hierarchy]

| Fält | Beskrivning |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | Företagets ID-nummer. |
| [!UICONTROL Company Name] | Företagets fullständiga namn. <br/>En `current company indicator` visas på den företagsrad som redigeras. |
| [!UICONTROL Company Email] | E-postadressen som är associerad med företagskontot. |
| [!UICONTROL Phone Number] | Företagets primära telefonnummer. |
| [!UICONTROL Country] | Det land där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL State/Province] | Den delstat eller provins där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL City] | Ort där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL Group/Shared Catalog] | (Endast administratör) Visar den [kundgrupp](../customers/customer-groups.md) eller [delade katalog](catalog-shared.md) som tilldelats företaget. |
| [!UICONTROL Company Admin] | Företagsadministratörens fullständiga namn. |
| [!UICONTROL Action] | Listan över möjliga åtgärder för den företagsraden. |

{style="table-layout:auto"}

#### [!UICONTROL Legal Address]

| Fält | Beskrivning |
|------------------------------|-----------------------------------------------------------------------------|
| [!UICONTROL Street Address] | Den gatuadress där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL City] | Ort där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL Country] | Det land där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL State/Province] | Den delstat eller provins där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL ZIP/Postal Code] | Postnummer där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL Phone Number] | Företagets primära telefonnummer. |

{style="table-layout:auto"}

#### [!UICONTROL Company Admin]

| Fält | Beskrivning |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Website] | Anger webbplatsen som företagsadministratören tillhör. |
| [!UICONTROL Job Title] | Namnet på den företagsadministratör som hanterar företagskontot. |
| [!UICONTROL Work Phone Number] | Telefonnumret till den företagsadministratör som hanterar företagskontot. |
| [!UICONTROL Email] | Företagsadministratörens e-postadress kan vara samma som företagets e-postadress. Om du anger en annan e-postadress skapar systemet ett separat individuellt konto för företagsadministratören, förutom företagskontot. |
| [!UICONTROL Prefix] | Om det är tillämpligt, det prefix som är associerat med företagsadministratörens namn (till exempel `Mr.`, `Ms.`, `Mrs.` eller `Dr.`). Beroende på konfigurationen kan inmatningsfältet vara ett textfält eller en lista. |
| [!UICONTROL First Name] | Företagsadministratörens förnamn. |
| [!UICONTROL Middle Name/Initial] | Företagsadministratörens mellannamn eller initialnamn. |
| [!UICONTROL Last Name] | Företagsadministratörens efternamn. |
| [!UICONTROL Suffix] | Det suffix som är associerat med namnet på företagsadministratören (till exempel `Jr.`, `Sr.` eller `III.`), om tillämpligt. Beroende på konfigurationen kan inmatningsfältet vara ett textfält eller en lista. |
| [!UICONTROL Gender] | Företagsadministratörens kön. Alternativ: `Male` / `Female` / `Not Specified` |
| [!UICONTROL Send Welcome Email From] | Den butiksvy som systemet skickar välkomstmeddelandet från. |

{style="table-layout:auto"}

#### [!UICONTROL Company Credit]

| Fält | Beskrivning |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Credit Currency] | (Endast administratör) Valutan som accepteras av butiken för köp av företagskrediter. |
| [!UICONTROL Credit Limit] | (Endast administratör) Den kreditgräns som utökas till företagskontot. |
| [!UICONTROL Allow to Exceed Credit Limit] | (Endast administratör) Anger om företaget har behörighet att överskrida kreditgränsen. Alternativ: `Yes` / `No` |
| [!UICONTROL Reason for Change] | (Endast administratör) En anteckning som förklarar varför företaget tillåts eller inte tillåts överskrida kreditgränsen. Det här fältet är bara aktivt om behörigheten att överskrida kreditgränsen ändras. |

{style="table-layout:auto"}

#### [!UICONTROL Advanced Settings]

Du kan konfigurera avancerade inställningar för enskilda företag. Om du skapar en företagshierarki kan du effektivisera konfigurationen av inställningarna genom att konfigurera inställningarna för det överordnade företaget och tillämpa inställningarna på alla eller valda underordnade företag i stället för att konfigurera varje underordnat företag individuellt. Mer information finns i [Hantera företagshierarkin](manage-company-hierarchy.md).

| Fält | Beskrivning |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Customer Group] | (Endast administratör) Visar den [kundgrupp](../customers/customer-groups.md) eller [delade katalog](catalog-shared.md) som tilldelats företaget. |
| [!UICONTROL Allow Quotes] | (Endast administratör) Avgör om företagsmedlemmar kan förbereda och skicka överlåtbara offerter för företagets räkning. |
| [!UICONTROL Enable Purchase Orders] | (Endast administratör) Avgör om företagsmedlemmar kan skicka order som [inköpsorder](account-dashboard-my-purchase-orders.md) för företagets räkning. |
| Tillämpliga betalningsmetoder | (Endast administratör) Anger betalningsmetoder som är tillgängliga för företagsköp. Alternativ: `B2B Payment Methods` / `All Enabled Payment Methods` / `Selected Payment Methods` |
| [!UICONTROL Payment Methods] | (Endast admin) Börjar vara aktivt om du aktiverar vissa betalningsmetoder. Om du vill göra flera betalningsmetoder tillgängliga för företagskontot håller du ned Ctrl-tangenten (PC) eller Kommando-tangenten (Mac) och väljer varje alternativ. |
| [!UICONTROL Applicable Shipping Methods] | (Endast administratör) Anger leveransmetoder som är tillgängliga för företagsköp. Alternativ: `B2B Shipping Methods` / `All Enabled Shipping Methods` / `Selected Shipping Methods` |
| [!UICONTROL Shipping Methods] | (Endast admin) Börjar vara aktivt om du aktiverar specifika leveransmetoder. Om du vill göra flera leveransmetoder tillgängliga för företagskontot håller du ned Ctrl-tangenten (PC) eller Kommando-tangenten (Mac) och väljer varje alternativ. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Aktivera B2B-funktioner](enable-basic-features.md) - Konfigurera grundläggande B2B-funktioner
>* [Företagets kontostruktur](account-company-structure.md) - Ordna användare och avdelningar från butiken
>* [Hantera företagsanvändare](account-company-users.md) - Lägg till och konfigurera medarbetarkonton från butiken
>* [Företagsadministratörsroll](account-company-admin.md) - Förstå administratörsansvar
>* [Hantera företag](manage-companies.md) - Administrativ översikt över företagshantering
>* [Företagets kredithantering](credit-company.md) - Konfigurera och hantera företagskrediter från administratören
>* [Arbetsflöde för inköpsorder](purchase-order-flow.md) - Konfigurera godkännandeprocesser från administratören
>* [Företagsroller och behörigheter](account-company-roles-permissions.md) - Kontrollera åtkomstnivåer för användare från administratören
>* [B2B-konfigurationsreferens](../configuration-reference/general/b2b-features.md) - Detaljerade systeminställningar
