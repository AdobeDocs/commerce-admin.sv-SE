---
title: Hantera företagskonton
description: Lär dig hur du hanterar företagskonton för din Adobe Commerce-butik med hjälp av företagssidan och verktygen i rutnätet.
exl-id: 9e125fc2-d20e-463e-a391-582fa0bcb68d
feature: B2B, Companies, Configuration
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '2726'
ht-degree: 0%

---

# Hantera företagskonton

På sidan _[!UICONTROL Companies]_visas alla aktuella företagskonton, oavsett status. Eventuella väntande begäranden om godkännande visas högst upp i listan.

![Företagsstödraster](./assets/companies-grid-view.png){width="700" zoomable="yes"}

Använd kontrollen *[!UICONTROL Columns]* för att anpassa de kolumner som visas i rutnätet. Anpassa de företag som visas i vyn med hjälp av sök- och filterfunktionerna.

- Hitta företag i rutnätet **Företag** med hjälp av _[!UICONTROL Search]_. Sökningen indexerar kolumnerna **Företagsnamn**och **Överordnad**.

- Anpassa vyn så att den innehåller poster som uppfyller specifika villkor med [!UICONTROL Filter]. Om till exempel B2B-webbplatsen är konfigurerad att hantera både enskilda företagskonton och [företagshierarkier](manage-companies.md) kan du filtrera efter `[!UICONTROL Company Type - Company]` om du bara vill visa enskilda företag, eller efter `[!UICONTROL Company Type - Parent]` om du bara vill visa det överordnade företaget för varje hierarki.

Använd en åtgärd på flera företagsposter med kontrollen _[!UICONTROL Actions]_ovanför rutnätet. I stället för att godkänna varje enskild företagsbegäran kan du till exempel välja flera begäranden för att aktivera kontona i en enda åtgärd. Vilka åtgärder som är tillgängliga beror på [behörigheterna](../systems/permissions.md) för rollen som tilldelas ditt administratörskonto.

## Resurser för företagsroll

Inställningarna för [rollresurser](../systems/permissions-user-roles.md#role-resources) avgör möjligheten att:

- Lägg till ett företag
- Ta bort ett företag
- Använda en saldoåterbetalning
- Visa företag

De här rollresurserna måste anges för [användarrollen](../systems/permissions-user-roles.md) som har tilldelats administratörskontot.

## Hantera företagskonton från företagsrutnätet

Visa och hantera användarkonton för företag på Admin-menyn genom att välja **[!UICONTROL Customers]** > **[!UICONTROL Companies]** för att öppna sidan *[!UICONTROL Companies]*.

Du kan hantera konton individuellt eller i grupper.

- Visa eller ändra konfigurationsinställningar för ett enskilt företagskonto genom att välja **[!UICONTROL Edit]** i kolumnen **[!UICONTROL Action]** för företagskontoposten.

  ![Välj åtgärd som ska tillämpas på valda företag](assets/companies-change-settings-edit-selection.png){width="675" zoomable="yes"}

- Visa eller ändra en grupp av valda företagskonton genom att använda de alternativ som är tillgängliga i kontrollen [!UICONTROL Actions]** ovanför rutnätet.

  ![Välj åtgärd som ska tillämpas på valda företag](assets/companies-change-settings-mass-action-selection.png){width="675" zoomable="yes"}

I följande avsnitt finns instruktioner om hur du använder varje åtgärd.

### Aktivera företagskonton

1. Välj **[!UICONTROL Set Active]** i kontrollen **[!UICONTROL Actions]**.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

### Ange aktiv/inaktiv

Kunder med inaktiva konton kan inte logga in eller göra inköp från sina konton. Det finns två metoder för att ange ett kundkonto som aktivt eller inaktivt:

Metod 1: **Från kundrutnätet**

1. Gå till [!UICONTROL **Kunder**] > [!UICONTROL **Alla kunder**] på sidofältet _Admin_.

1. Välj något av följande på menyn **[!UICONTROL Actions]**:

   - **[!UICONTROL Active]**
   - **[!UICONTROL Inactive]**

1. Välj **[!UICONTROL OK]** när du uppmanas att göra ändringen.

Metod 2: **Från sidan för kontoredigering**

1. Gå till [!UICONTROL **Kunder**] > [!UICONTROL **Alla kunder**] på sidofältet _Admin_.

1. Leta reda på kundposten som ska redigeras i rutnätet.

1. Välj [!UICONTROL **Redigera**] i kolumnen _Åtgärder_ längst till höger.

1. Välj fliken [!UICONTROL **Kontoinformation**].

1. Ange [!UICONTROL **Kundens aktiva**] till `Yes` eller `No`.

1. Klicka på [!UICONTROL **Spara kund**].

### Blockera företagskonton

Användare som är kopplade till ett blockerat företagskonto kan logga in och komma åt katalogen, men kan inte göra inköp. Ett företag med ett konto som inte fungerar som det ska kan tillfälligt blockeras tills ärendet är löst.

1. Välj **[!UICONTROL Block]** i kontrollen **[!UICONTROL Actions]**.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

### Ta bort företagskonton

Borttagna företagskonton kan inte återställas. Statusen för användarkonton som är associerade med företaget är inställd på `Inactive` och företags-ID tas bort från profilerna för användarkonton. Information om företagsaktivitet och transaktioner sparas i systemet.

1. Välj **[!UICONTROL Delete]** i kontrollen **[!UICONTROL Actions]**.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

### Ändra företagsinställningar

Uppdatera konfigurationen för [Avancerade inställningar](account-company-create.md#advanced-settings) om du vill använda samma inställningar för flera företag som har valts i stödrastret *Företag*.

>[!NOTE]
>
>Hantera den avancerade inställningskonfigurationen för en företagsorganisation med en överordnad och associerade underordnade företag från vyn [Företagshierarki](manage-company-hierarchy.md#change-company-settings).

1. Välj **[!UICONTROL Change company settings]** i kontrollen **[!UICONTROL Actions]**.

   I formuläret *[!UICONTROL Change company settings]* är de initiala konfigurationsinställningarna inställda på standardvärden.

1. För varje konfigurationsinställning som ska ändras markerar du kryssrutan **[!UICONTROL Change]** för att aktivera inställningen. Uppdatera sedan inställningen efter behov.

   ![Ändra företagsinställningar för flera företag](assets/companies-change-advanced-settings-action.png){width="675" zoomable="yes"}

1. När du har uppdaterat konfigurationsinställningarna väljer du **[!UICONTROL Apply Changes]**.

1. Välj **[!UICONTROL Change settings]** när du uppmanas att uppdatera konfigurationen för de valda företagen.

>[!TIP]
>
>Du kan ändra konfigurationen för avancerade inställningar för ett enskilt företag genom att välja **[!UICONTROL Edit]** i kolumnen **[!UICONTROL Action]** för företagskontoposten.

### Konvertera kreditvalutan

Krediten i konton för valda företag konverteras till den aktuella kursen för den valda valutan.

1. Välj **[!UICONTROL Convert Currency]** i kontrollen **[!UICONTROL Actions]**.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

1. Välj **[!UICONTROL Credit Currency]** som ska användas för de valda företagskontona.

   Beloppen beräknas om enligt aktuella konverteringsgrader, om sådana finns. Om den inte är tillgänglig kan du ange anpassade konverteringsgrader manuellt. Systemet visar så många konverteringsberäkningar som behövs för den kreditvaluta som används av de valda företagen.

1. Klicka på **[!UICONTROL Proceed]** för att slutföra konverteringen.

## Redigera ett företagskonto

Metod 1: **Snabbredigering**

1. I den första kolumnen markerar du kryssrutan för det företagskonto som ska redigeras.

1. Välj **[!UICONTROL Edit]** i kontrollen **[!UICONTROL Actions]**.

   Varje värde som kan uppdateras visas i en textruta.

   ![Snabbredigering för ett företagskonto](./assets/companies-grid-quick-edit.png){width="675" zoomable="yes"}

1. Uppdatera något av följande värden efter behov:

   - **[!UICONTROL Company Name]**

   - **[!UICONTROL Company Email]**

   - **[!UICONTROL Phone Number]**

1. Klicka på **[!UICONTROL Save]**.

Metod 2: **Fullständig redigering**

1. Leta reda på den företagspost som ska redigeras i rutnätet.

1. Välj **[!UICONTROL Edit]** i kolumnen _[!UICONTROL Action]_.

1. Gör nödvändiga ändringar i företagsinformationen.

   Fältbeskrivningar finns i [Skapa ett företagskonto](account-company-create.md).

1. Klicka på **[!UICONTROL Save]** när du är klar.

## Tilldela en säljare

Försäljningsrepresentanten är en [Admin-användare](../systems/permissions.md) som har tilldelats som kontaktpunkt för ett företagskonto och får alla automatiska [e-postmeddelanden](../b2b/enable-basic-features.md#configure-company-email-options) som är relaterade till företaget. Endast en säljare kan tilldelas per företagskonto, men en säljare kan hantera flera företagskonton. Standardadministratörens användarkonto tilldelas som säljare, såvida inte en annan administratörsanvändare har tilldelats.

Namnet och e-postadressen för den tilldelade försäljningsombudet visas för företagsmedlemmar från företagskontot och offertsidan.

1. Gå till **[!UICONTROL Customers]** > **[!UICONTROL Companies]** på sidofältet _Admin_.

1. Hitta företaget i rutnätet och öppna i redigeringsläge.

1. Ange **[!UICONTROL Sales Representative]** till den Admin-användare som du vill tilldela som kontaktpunkt för företaget.

1. Klicka på **[!UICONTROL Save]** när du är klar.

   Den tilldelade säljaren får ett e-postmeddelande om tilldelningen.

## Uppdatera en företagsprofil

Företagsprofilen kan underhållas från butiken av företagsadministratören och även från administratören av en butiksadministratör.

![Företagsprofil](./assets/company-update.png){width="700" zoomable="yes"}

1. Gå till **[!UICONTROL Customers]** > **[!UICONTROL Companies]** på sidofältet _Admin_.

1. Hitta företaget i rutnätet och klicka på **[!UICONTROL Edit]** i kolumnen _[!UICONTROL Action]_.

1. Uppdatera fältvärdena i varje avsnitt efter behov med fältbeskrivningarna som referens.

1. Klicka på **[!UICONTROL Save]** när du är klar.

## Företagskontodemo

I den här videon får du lära dig mer om hur du hanterar företagskonton:

>[!VIDEO](https://video.tv.adobe.com/v/344447?quality=12&learn=on)

## Företagsledning

När ett företag har skapats kan administratörsanvändare med lämplig behörighet använda avsnittet [!UICONTROL Company Hierarchy] för att skapa en överordnad företagsorganisation genom att redigera det utsedda överordnade företaget och tilldela relaterade företag.

Om ett företag har lagts till i en hierarki visar rutnätet [!UICONTROL Company Hierarchy] det överordnade företaget och alla tilldelade företag i rutnätet.

Mer information finns i [Hantera företagshierarki](manage-company-hierarchy.md).

## Företagsalternativ och kolumner

I följande avsnitt finns en referens för de tillgängliga åtgärderna, alternativen och den information som visas för hantering av företagskonton.

### Alternativ för åtgärdskontroll

| Alternativ | Beskrivning |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Set Active] | Anger status för alla valda företagsposter till `Active`. Företagsadministratörer får instruktioner om hur de anger sina lösenord så att de kan komma åt sina konton och hantera sina företag direkt i butiken. |
| [!UICONTROL Block] | Begränsar företagskonton som inte är i gott skick samtidigt som kontot bevaras. Företagsmedlemmar kan logga in och komma åt katalogen, men de kan inte göra beställningar för företagets räkning. |
| [!UICONTROL Delete] | Tar bort valda företagskonton. Statusen för användarkonton som är associerade med ett borttaget företag är inställd på `Inactive` och företags-ID tas bort från profilerna för användarkonton. Information om företagsaktivitet och transaktioner sparas i systemet. |
| [!UICONTROL Edit] | Tillåter att vissa värden för den valda företagsposten redigeras från rutnätet. Som standard är värdena Företagsnamn, Företagets e-postadress och Telefonnummer tillgängliga för en snabb redigering. |
| [!UICONTROL Change company settings] | Öppnar formuläret *Ändra företagsinställningar* för att uppdatera konfigurationen för [Avancerade inställningar](account-company-create.md#advanced-settings) och tillämpa ändringarna på de valda företagen. |
| [!UICONTROL Convert Credit] | Konverterar krediten à conto för de valda företagen enligt kurserna i den angivna valutan. |

{style="table-layout:auto"}

### Kolumnbeskrivningar


#### Standardkolumnlayout

| Kolumn | Beskrivning |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Select] | Kryssrutor som används för att markera företagsposter som ska bli en del av en åtgärd, eller använder markeringskontrollen i kolumnrubriken för att markera/avmarkera alla. |
| [!UICONTROL ID] | En unik numerisk identifierare som tilldelas när begäran om att skapa ett företag skickas. |
| [!UICONTROL Company Name] | Företagsnamnet anges när företagskontot skapas för första gången och kan vara en förkortad version av det fullständiga juridiska namnet. |
| [!UICONTROL Company Type] | Typen av [företag](manage-companies.md). Alternativ: <br/>**[!UICONTROL Company]**- Som standard skapas nya företag som enskilda företag.<br/>**[!UICONTROL Parent]** - Företaget är ett moderföretag till andra företag. <br/>**[!UICONTROL Child]**- Det här företaget är relaterat till ett överordnat företag. |
| [!UICONTROL Parent] | Visar det överordnade företaget för den här specifika företagsraden. |
| [!UICONTROL Company Email] | E-postadressen som är associerad med företagskontot. |
| [!UICONTROL Phone Number] | Företagets primära telefonnummer. |
| [!UICONTROL Country] | Det land där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL State Province] | Den delstat eller provins där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL City] | Ort där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL Group/Shared Catalog] | Kolumnnamnet beror på om Delad katalog är aktiverat i konfigurationen. Alternativ: <br/>**[!UICONTROL Customer Group]**- Om delad katalog inte är aktiverad i konfigurationen, anger namnet på den [kundgrupp](../customers/customer-groups.md) som företaget tillhör.<br/>**[!UICONTROL Shared Catalog]** - Om delad katalog är aktiverad i konfigurationen, anger det namnet på den delade katalogen som är tilldelad kunden. |
| [!UICONTROL Outstanding Balance] | Det utestående saldot på företagskontot. kolumnen är tom om företaget inte har någon kredithistorik och dess kreditgräns är noll. |
| [!UICONTROL Company Admin] | Företagsadministratörens för för- och efternamn. |
| [!UICONTROL Job Title] | Företagsadministratörens jobbtitel. |
| [!UICONTROL Work Phone Number] | Företagsadministratörens arbetstelefonnummer. |
| [!UICONTROL Email] | Företagsadministratörens e-postadress. |
| [!UICONTROL Action] | **[!UICONTROL Edit]** - Öppnar företagskontot i redigeringsläge. |

{style="table-layout:auto"}

#### Ytterligare kolumner

Följande kolumner är tillgängliga genom att ändra [kolumnlayouten](../getting-started/admin-grid-controls.md) för stödrastret.

| Kolumn | Beskrivning |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | Företagets officiella, fullständiga namn. |
| [!UICONTROL Street Address] | Den gatuadress där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL ZIP] | Postnummer där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL Reseller ID] | Återförsäljningsnumret som har tilldelats företaget för momsrapportering. |
| [!UICONTROL VAT/TAX ID] | [Moms](../stores-purchase/vat.md)-numret som tilldelas företaget av vissa jurisdiktioner för momsrapportering. Information om hur du konfigurerar kundens moms-/momsregistreringsnummer så att det visas i butiken finns i [Skapa nya kontoalternativ](../configuration-reference/customers/customer-configuration.md). |
| [!UICONTROL Credit Limit] | Kreditgränsen som utökas till företagskontot. |
| [!UICONTROL Credit Currency] | Valutan som accepteras av butiken för inköp av företagskrediter. |
| [!UICONTROL Status] | Anger [status](account-company-approve.md) för företagskontot. Alternativ: <br/>**[!UICONTROL Active]**- Företagskontot har godkänts av butiksadministratören. Företagsadministratören och associerade medlemmar kan logga in kontot från butiken och göra inköp.<br/>**[!UICONTROL Pending Approval]** - En begäran om att öppna ett företagskonto har skickats, men har ännu inte godkänts av butiksadministratören. <br/>**[!UICONTROL Rejected]**- En begäran om att öppna ett företagskonto har skickats, men inte godkänts av butiksadministratören. De inloggningsuppgifter som användes för att skicka begäran blockeras.<br/>**[!UICONTROL Blocked]** - Företagsmedlemmar kan logga in och komma åt katalogen, men kan inte göra inköp. Butiksadministratören kan blockera ett företagskonto som inte är i gott skick. Butiksadministratören kan när som helst ta bort blocket på kontot. |
| [!UICONTROL Gender] | Företagsadministratörens kön. Alternativ: hane/hona/Ej angivet |
| [!UICONTROL Comment] | Anteckningar om företagskontot som referens och som bara visas från administratören. |

{style="table-layout:auto"}

### Knappfält

| Knapp | Beskrivning |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Back] | Återgår till sidan Företag utan att spara ändringar. |
| [!DNL Delete Company] | Tar bort företagskontot. Statusen för användarkonton som är associerade med företaget är inställd på `Inactive` och företags-ID tas bort från profilerna för användarkonton. Information om företagsaktivitet och transaktioner sparas i systemet. |
| [!DNL Reset] | Återställer originalvärdena till fält som inte har sparats. |
| [!DNL Reimburse Balance] | Låter administratören återbetala saldot från butikskrediten, som PO-numret refererar till. |
| [!DNL Save] | Sparar ändringar i företaget och håller profilen öppen. |
| [!UICONTROL Save & Close] | Sparar ändringar i företaget och stänger profilen. |

{style="table-layout:auto"}

### Fältbeskrivningar

| Fält | Beskrivning |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Name] | Företagsnamnet anges när företagskontot skapas för första gången och kan vara en förkortad version av det fullständiga juridiska namnet. |
| [!UICONTROL Status] | Anger [status](account-company-approve.md) för företagskontot. Alternativ: <br/>**[!UICONTROL Active]**- Företagskontot har godkänts av butiksadministratören. Företagsadministratören och associerade medlemmar kan logga in kontot från butiken och göra inköp.<br/>**[!UICONTROL Pending Approval]** - En begäran om att öppna ett företagskonto har skickats, men har ännu inte godkänts av butiksadministratören. <br/>**[!UICONTROL Rejected]**- En begäran om att öppna ett företagskonto har skickats, men inte godkänts av butiksadministratören. De inloggningsuppgifter som användes för att skicka begäran blockeras.<br/>**[!UICONTROL Blocked]** - Företagsmedlemmar kan logga in och komma åt katalogen, men kan inte göra inköp. Butiksadministratören kan blockera ett företagskonto som inte är i gott skick. Butiksadministratören kan när som helst ta bort blocket på kontot. |
| [!UICONTROL Company Email] | E-postadressen som är associerad med företagskontot. |
| [!UICONTROL Sales Representative] | Administratörsanvändaren som är den primära kontakten för företagskontot. |

{style="table-layout:auto"}

#### [!UICONTROL Account Information]

| Fält | Beskrivning |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | Företagets officiella, fullständiga namn. |
| [!UICONTROL VAT / TAX ID] | Moms- eller [momsregistreringsnummer ](../stores-purchase/vat.md) som tilldelas företaget för momsrapportering. |
| [!UICONTROL Reseller ID] | Återförsäljningsnumret som har tilldelats företaget för momsrapportering. |
| [!UICONTROL Comment] | Anteckningarna om företagskontot är till för referens och visas endast från administratören. |

{style="table-layout:auto"}

#### [!UICONTROL Company Hierarchy]

| Kolumner | Beskrivning |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | Företagets ID-nummer. |
| [!UICONTROL Company Name] | Företagets fullständiga namn. <br/>En `current company indicator` visas på den företagsrad som redigeras. |
| [!UICONTROL Company Email] | E-postadressen som är associerad med företagskontot. |
| [!UICONTROL Phone Number] | Företagets primära telefonnummer. |
| [!UICONTROL State/Province] | Den delstat eller provins där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL City] | Ort där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL Customer Group] | (Endast administratör) Anger den [kundgrupp](../customers/customer-groups.md) eller [delade katalog](catalog-shared.md) som är tilldelad företaget. |
| [!UICONTROL Company Admin] | Företagsadministratörens fullständiga namn. |
| [!UICONTROL Action] | Listan över möjliga åtgärder för den företagsraden. |

{style="table-layout:auto"}

#### [!UICONTROL Legal Address]

| Kolumner | Beskrivning |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Street Address] | Den gatuadress där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL City] | Ort där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL Country] | Det land där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL State/Province] | Den delstat eller provins där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL ZIP/Postal Code] | Postnummer där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL Phone Number] | Företagets primära telefonnummer. |

{style="table-layout:auto"}

#### [!UICONTROL Company Admin]

| Fält | Beskrivning |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Website] | Ange webbplatsomfånget [för ](../getting-started/websites-stores-views.md) för företagskontot. Standardvärdet är *[!UICONTROL Main Website]*. |
| [!UICONTROL Job Title] | Namnet på den företagsadministratör som hanterar företagskontot. |
| [!UICONTROL Work Phone Number] | Telefonnumret till den företagsadministratör som hanterar företagskontot. |
| [!UICONTROL Email] | Företagsadministratörens e-postadress kan vara samma som företagets e-postadress. Om en annan e-postadress anges skapas ett separat individuellt konto för företagsadministratören utöver företagskontot. |
| [!UICONTROL Prefix] | Om det är tillämpligt, det prefix som är associerat med namnet på företagsadministratören (till exempel `Mr.`, `Ms.`, `Mrs.` eller `Dr.`). Beroende på konfigurationen kan inmatningsfältet vara ett textfält eller en lista. |
| [!UICONTROL First Name] | Företagsadministratörens förnamn. |
| [!UICONTROL Middle Name/Initial] | Företagsadministratörens mellannamn eller initialnamn. |
| [!UICONTROL Last Name] | Företagsadministratörens efternamn. |
| [!UICONTROL Suffix] | Det suffix som är associerat med namnet på företagsadministratören (till exempel `Jr.`, `Sr.` eller `III`), om tillämpligt. Beroende på konfigurationen kan inmatningsfältet vara ett textfält eller en lista. |
| [!UICONTROL Gender] | Företagsadministratörens kön. Alternativ: `Male` / `Female` / `Not Specified` |
| [!UICONTROL Send Welcome Email From] | Ange att butiksgranskningen ska användas när välkomstmeddelandet skickas till den nya företagsadministratören om du inte vill använda *[!UICONTROL Default Store View]*. |

{style="table-layout:auto"}

#### [!UICONTROL Company Credit]

| Fält | Beskrivning |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Credit Currency] | Valutan som accepteras av butiken för inköp av företagskrediter. |
| [!UICONTROL Credit Limit] | Kreditgränsen som utökas till företagskontot. |
| [!UICONTROL Allow to Exceed Credit Limit] | Anger om företaget har behörighet att överskrida kreditgränsen. Alternativ: Ja/Nej |
| [!UICONTROL Reason for Change] | En anteckning som förklarar omständigheterna när företaget kan eller inte kan överskrida kreditgränsen. Det här fältet är bara aktivt om behörigheten att överskrida kreditgränsen ändras. |

{style="table-layout:auto"}

#### [!UICONTROL Advanced Settings]

| Fält | Beskrivning |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Customer Group] | Anger den [kundgrupp](../customers/customer-groups.md) eller [delade katalog](catalog-shared.md) som har tilldelats företaget. |
| [!UICONTROL Allow Quotes] | Avgör om företagsmedlemmar kan förbereda och skicka överlåtbara offerter för företagets räkning. |
| [!UICONTROL Enable Purchase Orders] | Avgör om inköpsorder är tillåtna för företaget. För att inköpsorder ska fungera för företagsmedlemskonton måste företagsadministratören även aktivera den här funktionen i butiken. |
| [!UICONTROL Applicable Payment Methods] | Anger de betalningsmetoder som är tillgängliga för företagsköp. Alternativ: `B2B Payment Methods` / `All Enabled Payment Methods` / `Specific Payment Methods` |
| [!UICONTROL Payment Methods] | (Endast administratör) Börjar vara aktivt om särskilda betalningsmetoder anges. Om du vill välja flera betalningsmetoder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ. |

{style="table-layout:auto"}
