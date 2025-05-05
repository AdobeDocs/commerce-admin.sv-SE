---
title: Hantera kundkonton
description: Använd stödrastret [!UICONTROL Customers] för att hitta ett kundkonto och få tillgång till information för enskilda kundkonton.
exl-id: 5f817ca8-9d1f-4498-b3bd-989713f0b6ad
source-git-commit: 0316475a37ee09948b9ba3649e059155212ab1ae
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 0%

---

# Hantera kundkonton

Använd stödrastret _[!UICONTROL Customers]_&#x200B;för att hitta ett kundkonto. Du kan använda standardkontrollerna för [arbetsplats](../getting-started/admin-workspace.md) för att filtrera listan, ändra [kolumnlayouten](../getting-started/admin-grid-controls.md), spara vyer och exportera data. [Åtgärdskontrollen](../getting-started/admin-actions-control.md) ovanför rutnätet kan användas för att tillämpa en åtgärd på flera kundposter.

![Alla kunder](assets/customers-all-customers.png){width="700" zoomable="yes"}

Mer information om hur du gör manuella uppdateringar av ett kundkonto finns i [Uppdatera kundprofil](update-account.md).

## Kundkontoåtgärder

1. Gå till **[!UICONTROL Customers]** > **[!UICONTROL All Customers]** på sidofältet _Admin_.

1. Markera kryssrutan för varje post som du vill uppdatera i den första kolumnen i rutnätet.

1. Följ instruktionerna för den åtgärd som du vill använda.

   >[!INFO]
   >
   >Följande åtgärder kan tillämpas på en eller flera poster.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

### Prenumerera på nyhetsbrevet

I flerbutiks- och flerplatsinställningar med ett globalt [kundkontoomfång](../customers/customer-account-scope.md) kan ett kundkonto prenumerera på nyhetsbrev på flera webbplatser eller butiker. Om du tillämpar åtgärden _Prenumerera_ på ett kundkonto aktiveras nyhetsbrevprenumerationen endast för standardvyn för plats/butik.

* Ställ in kontrollen **[!UICONTROL Actions]** på `Subscribe to newsletter`.

Mer information om hur du hanterar prenumerationer på nyhetsbrev för en kund finns i [Hantera prenumeranter](../merchandising-promotions/newsletter-subscribers.md).

### Avbeställ nyhetsbrev

I flerbutiks- och flerplatsinställningar med ett globalt [kundkontoomfång](customer-account-scope.md) kan ett kundkonto prenumereras på nyhetsbrev för flera platser/butiker. Om du tillämpar åtgärden _Avbeställ_ på ett kundkonto kommer alla aktiva prenumerationer att avbrytas.

1. Ställ in kontrollen **[!UICONTROL Actions]** på `Unsubscribe to newsletter`.

1. När du uppmanas att bekräfta klickar du på **OK**.

### Tilldela en kundgrupp

1. Ställ in kontrollen **[!UICONTROL Actions]** på `Assign a customer group`.

1. Välj den kundgrupp som alla valda kundposter ska tilldelas till.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

### Ta bort kundkonton

Borttagna kundkonton kan inte återställas. Information om kundaktivitet och transaktioner sparas i systemet.

1. Ställ in kontrollen **[!UICONTROL Actions]** på `Delete`.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

## Exportera kundkonton

1. Gå till **[!UICONTROL Customers]** > **[!UICONTROL All Customers]** på sidofältet _Admin_.

1. Klicka på **[!UICONTROL Export]** på tabellrubrikmenyn och välj önskat format:

   * CSV
   * Excel XML

1. Klicka på **[!UICONTROL OK]**.

   Filen placeras i standardmappen för nedladdningar.

Instruktionen ovan exporterar alla kundkonton. Om du vill exportera en begränsad uppsättning markerar du kryssrutorna för de konton du vill exportera, eller använder filter på kontrollpanelen för att välja ett intervall med kundkonton.

## Åtgärder/kontroller

| Alternativ | Beskrivning |
|--- |--- |
| **[!UICONTROL Delete]** | Tar bort valda kundkonton. Om kundkontot tillhör en företagsadministratör för en B2B-butik måste en annan företagsanvändare tilldelas administratörsbehörighet innan kundkontot kan tas bort. |
| **[!UICONTROL Subscribe to Newsletter]** | Prenumererar på utvalda kunder i nyhetsbrevet. |
| **[!UICONTROL Unsubscribe from Newsletter]** | Avbeställ nyhetsbrevet. |
| **[!UICONTROL Assign a Customer Group]** | Tilldelar valda kunder till en kundgrupp. |
| **[!UICONTROL Edit]** | Tillåter att vissa värden för en vald kundpost redigeras från rutnätet. Som standard är följande värden tillgängliga för snabbredigering: E-post, Grupp, Telefon, ZIP, Webbplats, Momsnummer och Kön. |

{style="table-layout:auto"}

## Kolumner

| Kolumn | Beskrivning |
|--- |--- |
| **[!UICONTROL Select]** | Hanterar kryssruteval för kundposter för att tillämpa en åtgärd. Du kan också använda markeringskontrollen i kolumnrubriken för att markera/avmarkera alla. |
| **[!UICONTROL ID]** | En unik numerisk identifierare som tilldelas när kundkontot skapas. |
| **[!UICONTROL Name]** | Kundens för- och efternamn. |
| **[!UICONTROL Email]** | Kundens e-postadress. |
| **[!UICONTROL Group]** | Kundgruppen som kunden är tilldelad till. |
| **[!UICONTROL Phone]** | Kundens telefonnummer. |
| **[!UICONTROL ZIP]** | Kundens postnummer. |
| **[!UICONTROL Country]** | Det land där kunden finns. |
| **[!UICONTROL State/Province]** | Delstaten eller regionen där kunden finns. |
| **[!UICONTROL Customer Since]** | Datum och tid då kundkontot skapades. |
| **[!UICONTROL Web Site]** | Webbplatsen i butikshierarkin som kundkontot är kopplat till. |
| **[!UICONTROL Confirmed Email]** | Anger om ett bekräftelsemeddelande krävs. |
| **[!UICONTROL Account Created In]** | Anger butiksvyn som kundkontot skapades från. |
| **[!UICONTROL Date of Birth]** | Kundens födelsedatum. I enlighet med gällande säkerhets- och integritetspraxis bör du vara medveten om eventuella juridiska risker och säkerhetsrisker som är förknippade med lagring av kundernas fullständiga födelsedatum (månad, dag, år) med andra personliga identifierare. Vi rekommenderar att du begränsar lagringen av kundernas födelsedatum och föreslår att du använder kundens födelseår som ett alternativ. |
| **[!UICONTROL Tax / VAT Number]** | Om tillämpligt, momsregistreringsnumret eller [momsregistreringsnumret ](../stores-purchase/vat.md) som tilldelats kunden. <br/><br/> Det här fältet är inte detsamma som momsregistreringsnumret. |
| **[!UICONTROL Gender]** | Kundens kön. |
| **[!UICONTROL Action]** | Redigera - Öppnar företagskontot i redigeringsläge. |

{style="table-layout:auto"}

### Ytterligare kolumner

De här kolumnerna är tillgängliga genom att ändra [kolumnlayouten](../getting-started/admin-grid-controls.md) för stödrastret.

| Kolumn | Beskrivning |
|--- |--- |
| **[!UICONTROL Company]** | Kundens företagsnamn. |
| **[!UICONTROL Street Address]** | Kundens gatuadress. |
| **[!UICONTROL City]** | Ort där kunden finns. |
| **[!UICONTROL Fax]** | Kundens faxnummer, om tillämpligt. |
| **[!UICONTROL Billing Firstname]** | Förnamnet i kundens faktureringsadress. |
| **[!UICONTROL Billing Lastname]** | Efternamnet i kundens faktureringsadress. |
| **[!UICONTROL Billing Address]** | Den adress dit faktureringsinformation ska skickas. |
| **[!UICONTROL Shipping Address]** | Den adress dit beställningar ska skickas. |
| **[!UICONTROL VAT Number]** | Momsnumret som är associerat med kundadressen. För [digitala varor](../stores-purchase/taxes.md) som säljs i EU baseras momsen på kundens faktureringsadress. <br/><br/> Det här fältet är inte detsamma som moms-/momsregistreringsnumret. |
| **[!UICONTROL Account Lock]** | Anger kontots status. Som en säkerhetsåtgärd kan kundkonton vara [låsta](../customers/password-options.md) efter för många inloggningsförsök. Värden: `Locked` / `Unlocked` |
| **[!UICONTROL Status]** | Aktuell användarstatus. Alternativ: `Active` / `Inactive` |
| **[!UICONTROL Customer Type]** | Kundklassificering. Alternativ: `Individual user` / `Company admin` / `Company user` |
| **[!UICONTROL Sales Representative]** | Den säljare som är tilldelad som kontaktpunkt för ett företagskonto och får alla automatiska e-postmeddelanden som rör företaget. |

{style="table-layout:auto"}
