---
title: Hantera företagskonton
description: Läs mer om företagssidan och verktygen i rutnätet som hjälper dig att hantera företagskonton för din Adobe Commerce-butik.
exl-id: 9e125fc2-d20e-463e-a391-582fa0bcb68d
feature: B2B, Companies, Configuration
source-git-commit: 1123cf4b257a83a61914c378104c43e952512e7d
workflow-type: tm+mt
source-wordcount: '2500'
ht-degree: 0%

---

# Hantera företagskonton

The _[!UICONTROL Companies]_visas alla aktuella företagskonton, oavsett status. Eventuella väntande begäranden om godkännande visas högst upp i listan. Standarden [arbetsplatskontroller](../getting-started/admin-workspace.md) kan användas för att filtrera listan, ändra [kolumnlayout](../getting-started/admin-grid-controls.md), spara vyer eller exportera data.

The _[!UICONTROL Actions]_kontroll ovanför rutnätet kan användas för att tillämpa en åtgärd på flera företagsposter. I stället för att godkänna varje enskild företagsbegäran kan du till exempel välja flera begäranden och aktivera kontona i en enda åtgärd. Vilka åtgärder som är tillgängliga beror på [behörigheter](../systems/permissions.md) för rollen som tilldelas ditt administratörskonto.

Använd _[!UICONTROL Search]_funktion för att hitta företag i **Företag**stödraster efter nyckelord. Det kommer att hitta företaget genom att söka efter det angivna nyckelordet i **Företagsnamn**och **Överordnad**kolumner. Du kan filtrera efter **Företagstyp**för att visa moderbolag och deras närstående företag, eller endast visa underordnade företag.

![Företagsrutnät](./assets/companies-grid-view.png){width="700" zoomable="yes"}

## Resurser för företagsroll

The [Rollresurser](../systems/permissions-user-roles.md#role-resources) inställningarna avgör möjligheten att

- Lägg till ett företag
- Ta bort ett företag
- Använda en saldoåterbetalning
- Visa företag

Dessa rollresurser måste anges för [Användarroll](../systems/permissions-user-roles.md) som är tilldelad för administratörens användarkonto.

## Använda en åtgärd

Följande åtgärder kan tillämpas på en eller flera poster.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. I stödrastrets första kolumn markerar du kryssrutan för varje post som du vill uppdatera och följer instruktionerna för den åtgärd som du vill använda:

### Aktivera företagskonton

1. Ange **[!UICONTROL Actions]** styra till `Set Active`.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

### Ange aktiv/inaktiv

Kunder med inaktiva konton kan inte logga in eller göra inköp från sina konton. Det finns två metoder för att ange ett kundkonto som aktivt eller inaktivt:

Metod 1: **Från kundrutnätet**

1. På _Administratör_ sidebar, gå till [!UICONTROL **Kunder**] > [!UICONTROL **Alla kunder**].

1. Ange [!UICONTROL **Åtgärder**] kontrollera något av följande:

   - `Active`
   - `Inactive`

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

Metod 2: **Från kontoredigeringssidan**

1. På _Administratör_ sidebar, gå till [!UICONTROL **Kunder**] > [!UICONTROL **Alla kunder**].

1. Leta reda på kundposten som ska redigeras i rutnätet.

1. I _Åtgärder_ kolumn längst till höger, klicka på [!UICONTROL **Redigera**].

1. Välj [!UICONTROL **Kontoinformation**] -fliken.

1. Ange [!UICONTROL **Kundaktiv**] till `Yes` eller `No`.

1. Klicka [!UICONTROL **Spara kund**].

### Blockera företagskonton

Användare som är kopplade till ett blockerat företagskonto kan logga in och komma åt katalogen, men kan inte göra inköp. Ett företag med ett konto som inte fungerar som det ska kan tillfälligt blockeras tills ärendet är löst.

1. Ange **[!UICONTROL Actions]** styra till `Block`.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

### Ta bort företagskonton

Borttagna företagskonton kan inte återställas. Statusen för användarkonton som är kopplade till företaget är inställd på `Inactive` och företags-ID tas bort från profilerna för användarkonton. Information om företagsaktivitet och transaktioner sparas i systemet.

1. Ange **[!UICONTROL Actions]** styra till `Delete`.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

### Konvertera kreditvalutan

Krediten i konton för valda företag konverteras till den aktuella kursen för den valda valutan.

1. Ange **[!UICONTROL Actions]** styra till `Convert Currency`.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

1. Välj **[!UICONTROL Credit Currency]** som ska användas för de valda företagskontona.

   Beloppen beräknas om enligt aktuella konverteringsgrader, om sådana finns. Om den inte är tillgänglig kan du ange anpassade konverteringsgrader manuellt. Systemet visar så många konverteringsberäkningar som behövs för den kreditvaluta som används av de valda företagen.

1. Klicka **[!UICONTROL Proceed]** för att slutföra konverteringen.

### Redigera ett företagskonto

Metod 1: **Snabbredigering**

1. I den första kolumnen markerar du kryssrutan för det företagskonto som ska redigeras.

1. Ange **[!UICONTROL Actions]** kolumn till `Edit`.

   Varje värde som kan uppdateras visas i en textruta.

   ![Snabbredigering för ett företagskonto](./assets/companies-grid-quick-edit.png){width="700" zoomable="yes"}

1. Uppdatera något av följande värden efter behov:

   - **[!UICONTROL Company Name]**

   - **[!UICONTROL Company Email]**

   - **[!UICONTROL Phone Number]**

1. Klicka på **[!UICONTROL Save]**.

Metod 2: **Fullständig redigering**

1. Leta reda på den företagspost som ska redigeras i rutnätet.

1. Klicka **[!UICONTROL Edit]** i _[!UICONTROL Action]_kolumn.

1. Gör nödvändiga ändringar i företagsinformationen.

Fältbeskrivningar finns i [Skapa ett företagskonto](account-company-create.md).

1. När du är klar klickar du på **[!UICONTROL Save]**.

## Tilldela en säljare

Säljaren är en [Administratörsanvändare](../systems/permissions.md) som är tilldelad som kontaktpunkt för ett företagskonto och får alla automatiska [e-postmeddelanden](../b2b/enable-basic-features.md#configure-company-email-options) som är närstående företaget. Endast en säljare kan tilldelas per företagskonto, men en säljare kan hantera flera företagskonton. Standardadministratörens användarkonto tilldelas som säljare, såvida inte en annan administratörsanvändare har tilldelats.

Namnet och e-postadressen för den tilldelade försäljningsombudet visas för företagsmedlemmar från företagskontot och offertsidan.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Hitta företaget i rutnätet och öppna i redigeringsläge.

1. Ange **[!UICONTROL Sales Representative]** till den Admin-användare som du vill tilldela som kontaktpunkt för företaget.

1. När du är klar klickar du på **[!UICONTROL Save]**.

   Den tilldelade säljaren får ett e-postmeddelande om tilldelningen.

## Uppdatera en företagsprofil

Företagsprofilen kan underhållas från butiken av företagsadministratören och även från administratören av en butiksadministratör.

![Företagsprofil](./assets/company-update.png){width="700" zoomable="yes"}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Hitta företaget i rutnätet och klicka på **[!UICONTROL Edit]** i _[!UICONTROL Action]_kolumn.

1. Uppdatera fältvärdena i varje avsnitt efter behov med fältbeskrivningarna som referens.

1. När du är klar klickar du på **[!UICONTROL Save]**.

## Företagskontodemo

I den här videon får du lära dig mer om hur du hanterar företagskonton:

>[!VIDEO](https://video.tv.adobe.com/v/344447?quality=12)

## Företagsledning

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Endast tillgängligt för betaprogramdeltagare"}

När ett företag har skapats kan administratörsanvändare med lämplig behörighet använda [!UICONTROL Company Hierarchy] för att skapa en överordnad företagsorganisation genom att redigera det utsedda överordnade företaget och tilldela närstående företag.

Om ett företag har lagts till i en hierarki [!UICONTROL Company Hierarchy] rutnätet visar det överordnade företaget och alla tilldelade företag i rutnätet.

Se [Hantera företagshierarki](assign-companies.md) för mer information.

## Företagsalternativ och kolumner

I följande avsnitt finns en referens för de tillgängliga åtgärderna, alternativen och den information som visas för hantering av företagskonton.

### Alternativ för åtgärdskontroll

| Alternativ | Beskrivning |
|--- |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Set Active] | Anger status för alla valda företagsposter till `Active`. Företagsadministratörer får instruktioner om hur de anger sina lösenord så att de kan komma åt sina konton och hantera sina företag direkt i butiken. |
| [!UICONTROL Block] | Begränsar företagskonton som inte är i gott skick samtidigt som kontot bevaras. Företagsmedlemmar kan logga in och komma åt katalogen, men de kan inte göra beställningar för företagets räkning. |
| [!UICONTROL Delete] | Tar bort valda företagskonton. Statusen för användarkonton som är associerade med ett borttaget företag är inställd på `Inactive` och företags-ID tas bort från profilerna för användarkonton. Information om företagsaktivitet och transaktioner sparas i systemet. |
| [!UICONTROL Edit] | Tillåter att vissa värden för den valda företagsposten redigeras från rutnätet. Som standard är värdena Företagsnamn, Företagets e-postadress och Telefonnummer tillgängliga för en snabb redigering. |
| [!UICONTROL Convert Credit] | Konverterar krediten à conto för de valda företagen enligt kurserna i den angivna valutan. |

{style="table-layout:auto"}

### Kolumnbeskrivningar


#### Standardkolumnlayout

| Kolumn | Beskrivning |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Select] | Kryssrutor som används för att markera företagsposter som ska bli en del av en åtgärd, eller använder markeringskontrollen i kolumnrubriken för att markera/avmarkera alla. |
| [!UICONTROL ID] | En unik numerisk identifierare som tilldelas när begäran om att skapa ett företag skickas. |
| [!UICONTROL Company Name] | Företagsnamnet anges när företagskontot skapas för första gången och kan vara en förkortad version av det fullständiga juridiska namnet. |
| [!UICONTROL Company Type] | Typ av [företag](manage-companies.md). Alternativ: <br/>**[!UICONTROL Company]**- Som standard skapas nya företag som enskilda företag.<br/>**[!UICONTROL Parent]** - Företaget är ett moderbolag till andra företag. <br/>**[!UICONTROL Child]**- Det här företaget är närstående ett moderbolag. |
| [!UICONTROL Parent] | Visar det överordnade företaget för den här specifika företagsraden. |
| [!UICONTROL Company Email] | E-postadressen som är associerad med företagskontot. |
| [!UICONTROL Phone Number] | Företagets primära telefonnummer. |
| [!UICONTROL Country] | Det land där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL State Province] | Den delstat eller provins där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL City] | Ort där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL Group/Shared Catalog] | Kolumnnamnet beror på om Delad katalog är aktiverat i konfigurationen. Alternativ: <br/>**[!UICONTROL Customer Group]**- Om Delad katalog inte är aktiverad i konfigurationen, anger namnet på [kundgrupp](../customers/customer-groups.md) som företaget tillhör.<br/>**[!UICONTROL Shared Catalog]** - Om Delad katalog är aktiverat i konfigurationen, anger namnet på den delade katalogen som är tilldelad kunden. |
| [!UICONTROL Outstanding Balance] | Det utestående saldot på företagskontot. kolumnen är tom om företaget inte har någon kredithistorik och dess kreditgräns är noll. |
| [!UICONTROL Company Admin] | Företagsadministratörens för för- och efternamn. |
| [!UICONTROL Job Title] | Företagsadministratörens jobbtitel. |
| [!UICONTROL Email] | Företagsadministratörens e-postadress. |
| [!UICONTROL Action] | **[!UICONTROL Edit]** - Öppnar företagskontot i redigeringsläge. |

{style="table-layout:auto"}

#### Ytterligare kolumner

Följande kolumner är tillgängliga genom att ändra [kolumnlayout](../getting-started/admin-grid-controls.md) i rutnätet.

| Kolumn | Beskrivning |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | Företagets officiella, fullständiga namn. |
| [!UICONTROL Street Address] | Den gatuadress där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL ZIP] | Postnummer där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL Reseller ID] | Återförsäljningsnumret som har tilldelats företaget för momsrapportering. |
| [!UICONTROL VAT/TAX ID] | The [moms](../stores-purchase/vat.md) Nummer som tilldelas företaget av vissa jurisdiktioner för momsrapportering. Information om hur du konfigurerar kundens moms-/momsregistreringsnummer så att det visas i butiken finns i [Skapa nya kontoalternativ](../configuration-reference/customers/customer-configuration.md). |
| [!UICONTROL Credit Limit] | Kreditgränsen som utökas till företagskontot. |
| [!UICONTROL Credit Currency] | Valutan som accepteras av butiken för inköp av företagskrediter. |
| [!UICONTROL Status] | Anger [status](account-company-approve.md) av företagskontot. Alternativ: <br/>**[!UICONTROL Active]**- Företagskontot har godkänts av butiksadministratören. Företagsadministratören och associerade medlemmar kan logga in kontot från butiken och göra inköp.<br/>**[!UICONTROL Pending Approval]** - En begäran om att öppna ett företagskonto har skickats, men har ännu inte godkänts av butiksadministratören. <br/>**[!UICONTROL Rejected]**- En begäran om att öppna ett företagskonto har skickats, men inte godkänts av butiksadministratören. De inloggningsuppgifter som användes för att skicka begäran blockeras.<br/>**[!UICONTROL Blocked]** - Företagsmedlemmar kan logga in och komma åt katalogen, men kan inte göra inköp. Butiksadministratören kan blockera ett företagskonto som inte är i gott skick. Butiksadministratören kan när som helst ta bort blocket på kontot. |
| [!UICONTROL Gender] | Företagsadministratörens kön. Alternativ: hane/hona/Ej angivet |
| [!UICONTROL Comment] | Anteckningar om företagskontot som referens och som bara visas från administratören. |

{style="table-layout:auto"}

### Knappfält

| Knapp | Beskrivning |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Back] | Återgår till sidan Företag utan att spara ändringar. |
| [!UICONTROL Login as Customer] | Tillåter en administratör att [logga in i butiken som kund](../customers/login-as-customer.md) och hjälpa till med deras order. |
| [!DNL Delete Company] | Tar bort företagskontot. Statusen för användarkonton som är kopplade till företaget är inställd på `Inactive` och företags-ID tas bort från profilerna för användarkonton. Information om företagsaktivitet och transaktioner sparas i systemet. |
| [!DNL Reset] | Återställer originalvärdena till fält som inte har sparats. |
| [!DNL Reimburse Balance] | Låter administratören återbetala saldot från butikskrediten, som PO-numret refererar till. |
| [!DNL Save] | Sparar ändringar i företaget och håller profilen öppen. |
| [!UICONTROL Save & Close] | Sparar ändringar i företaget och stänger profilen. |

{style="table-layout:auto"}

### Fältbeskrivningar

| Fält | Beskrivning |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Name] | Företagsnamnet anges när företagskontot skapas för första gången och kan vara en förkortad version av det fullständiga juridiska namnet. |
| [!UICONTROL Status] | Anger [status](account-company-approve.md) av företagskontot. Alternativ: <br/>**[!UICONTROL Active]**- Företagskontot har godkänts av butiksadministratören. Företagsadministratören och associerade medlemmar kan logga in kontot från butiken och göra inköp.<br/>**[!UICONTROL Pending Approval]** - En begäran om att öppna ett företagskonto har skickats, men har ännu inte godkänts av butiksadministratören. <br/>**[!UICONTROL Rejected]**- En begäran om att öppna ett företagskonto har skickats, men inte godkänts av butiksadministratören. De inloggningsuppgifter som användes för att skicka begäran blockeras.<br/>**[!UICONTROL Blocked]** - Företagsmedlemmar kan logga in och komma åt katalogen, men kan inte göra inköp. Butiksadministratören kan blockera ett företagskonto som inte är i gott skick. Butiksadministratören kan när som helst ta bort blocket på kontot. |
| [!UICONTROL Company Email] | E-postadressen som är associerad med företagskontot. |
| [!UICONTROL Sales Representative] | Administratörsanvändaren som är den primära kontakten för företagskontot. |

{style="table-layout:auto"}

#### [!UICONTROL Account Information]

| Fält | Beskrivning |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | Företagets officiella, fullständiga namn. |
| [!UICONTROL VAT / TAX ID] | Skatten eller [moms](../stores-purchase/vat.md) nummer som har tilldelats företaget för momsrapportering. |
| [!UICONTROL Reseller ID] | Återförsäljningsnumret som har tilldelats företaget för momsrapportering. |
| [!UICONTROL Comment] | Anteckningarna om företagskontot är till för referens och visas endast från administratören. |
| **[!UICONTROL Legal Address]** |                                                                                                                            |
| [!UICONTROL Street Address] | Den gatuadress där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL City] | Ort där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL Country] | Det land där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL State/Province] | Den delstat eller provins där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL ZIP/Postal Code] | Postnummer där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL Phone Number] | Företagets primära telefonnummer. |

{style="table-layout:auto"}

#### [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Endast tillgängligt för betaprogramdeltagare"}

| Kolumner | Beskrivning |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | Företagets ID-nummer. |
| [!UICONTROL Company Name] | Företagets fullständiga namn. <br/>A `current company indicator` visas på den företagsrad som redigeras. |
| [!UICONTROL Company Email] | E-postadressen som är associerad med företagskontot. |
| [!UICONTROL Phone Number] | Företagets primära telefonnummer. |
| [!UICONTROL State/Province] | Den delstat eller provins där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL City] | Ort där företaget är registrerat för att bedriva verksamhet. |
| [!UICONTROL Customer Group] | (Endast administratör) Anger [kundgrupp](../customers/customer-groups.md) eller [delad katalog](catalog-shared.md) som har tilldelats företaget. |
| [!UICONTROL Company Admin] | Företagsadministratörens fullständiga namn. |
| [!UICONTROL Action] | Listan över möjliga åtgärder för den företagsraden. |

{style="table-layout:auto"}

#### [!UICONTROL Company Admin]

| Fält | Beskrivning |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Job Title] | Namnet på den företagsadministratör som hanterar företagskontot. |
| [!UICONTROL Email] | Företagsadministratörens e-postadress kan vara samma som företagets e-postadress. Om en annan e-postadress anges skapas ett separat individuellt konto för företagsadministratören utöver företagskontot. |
| [!UICONTROL Prefix] | Om tillämpligt, det prefix som är associerat med namnet på företagsadministratören (till exempel `Mr.`, `Ms.`, `Mrs.`, eller `Dr.`). Beroende på konfigurationen kan inmatningsfältet vara ett textfält eller en lista. |
| [!UICONTROL First Name] | Företagsadministratörens förnamn. |
| [!UICONTROL Middle Name/Initial] | Företagsadministratörens mellannamn eller initialnamn. |
| [!UICONTROL Last Name] | Företagsadministratörens efternamn. |
| [!UICONTROL Suffix] | Det suffix som är associerat med namnet på företagsadministratören (till exempel `Jr.`, `Sr.`, eller `III`). Beroende på konfigurationen kan inmatningsfältet vara ett textfält eller en lista. |
| [!UICONTROL Gender] | Företagsadministratörens kön. Alternativ: `Male` / `Female` / `Not Specified` |

{style="table-layout:auto"}

#### [!UICONTROL Company Credit]

| Fält | Beskrivning |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Credit Currency] | Valutan som accepteras av butiken för inköp av företagskrediter. |
| [!UICONTROL Credit Limit] | Kreditgränsen som utökas till företagskontot. |
| [!UICONTROL Allow to Exceed Credit Limit] | Anger om företaget har behörighet att överskrida kreditgränsen. Alternativ: Ja/Nej |
| [!UICONTROL Reason for Change] | En anteckning som förklarar varför företaget tillåts eller inte tillåts överskrida kreditgränsen. Det här fältet är bara aktivt om behörigheten att överskrida kreditgränsen ändras. |

{style="table-layout:auto"}

#### [!UICONTROL Advanced Settings]

| Fält | Beskrivning |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Customer Group] | Anger [kundgrupp](../customers/customer-groups.md) eller [delad katalog](catalog-shared.md) som har tilldelats företaget. |
| [!UICONTROL Allow Quotes] | Avgör om företagsmedlemmar kan förbereda och skicka överlåtbara offerter för företagets räkning. |
| [!UICONTROL Enable Purchase Orders] | Avgör om inköpsorder är tillåtna för företaget. För att inköpsorder ska fungera för företagsmedlemskonton måste företagsadministratören även aktivera den här funktionen i butiken. |
| [!UICONTROL Applicable Payment Methods] | Anger de betalningsmetoder som är tillgängliga för företagsköp. Alternativ: `B2B Payment Methods` / `All Enabled Payment Methods` / `Specific Payment Methods` |
| [!UICONTROL Payment Methods] | (Endast administratör) Börjar vara aktivt om särskilda betalningsmetoder anges. Om du vill välja flera betalningsmetoder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ. |

{style="table-layout:auto"}
