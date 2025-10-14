---
title: Kundlista
description: I kundrutnätet visas alla kunder som har registrerat sig för ett konto hos din butik eller som har lagts till av administratören.
exl-id: a7d9b098-4892-492c-b937-61cc33b836d8
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Kundlista

I Admin visas i rutnätet [!UICONTROL Customers] alla kunder som har registrerat sig för ett konto hos din butik eller som har lagts till av administratören. Använd [standardkontrollerna för stödraster](../getting-started/admin-grid-controls.md) för att filtrera listan och justera kolumnlayouten. Mer information finns i [Hantera kundkonton](../customers/manage-account.md).

![Kundlista](assets/customer-accounts-all-grid.png){width="700" zoomable="yes"}

## Uppdatera kundinformation

1. Gå till **[!UICONTROL Customers]** > **[!UICONTROL All Customers]** på sidofältet _Admin_.

1. Hitta kundposten och klicka på [!UICONTROL **Redigera**] i kolumnen _[!UICONTROL Action]_.

1. I den vänstra panelen väljer du den information som du vill redigera och gör de ändringar som behövs.

   >[!NOTE]
   >
   >Mer information finns i [Uppdatera kundkonton](../customers/update-account.md).

1. Klicka på **[!UICONTROL Save Customer]** när du är klar.

## Workspace

| Kontroll | Beskrivning |
| --- | --- |
| **[!UICONTROL Add New Customer]** | Skapar ett kundkonto. |
| **[!UICONTROL Search]** | Startar en sökning efter kunder baserat på de aktuella filtren. |
| **[!UICONTROL Filters]** | Definierar en uppsättning sökparametrar som används för att filtrera posterna som visas i [rutnätet](../getting-started/admin-grid-controls.md). |
| **[!UICONTROL Default View]** | Anger stödrastrets standardkolumn [layout](../getting-started/admin-grid-controls.md). |
| **[!UICONTROL Columns]** | Bestämmer markeringen av [kolumner](../getting-started/admin-grid-controls.md) och deras konton i rutnätet. Kolumnlayouten kan ändras och sparas som en _vy_. Som standard inkluderas bara vissa av kolumnerna i rutnätet. |
| **[!UICONTROL Export]** | Exporterar de markerade posterna som en CSV- eller Excel XML-fil. |

{style="table-layout:auto"}

## Kolumner

| Kolumn | Beskrivning |
| --- | --- |
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
| **[!UICONTROL Date of Birth]** | Kundens födelsedatum. <br><br>**_Viktigt!_**&#x200B;I enlighet med aktuella säkerhets- och sekretessrutiner ska du vara medveten om eventuella juridiska risker och säkerhetsrisker som är förknippade med lagring av kunders födelsedatum (månad, dag, år) med andra personliga identifierare. Vi rekommenderar att du begränsar lagringen av kundernas födelsedatum och föreslår att du använder kundens födelseår som ett alternativ. |
| **[!UICONTROL Tax / VAT Number]** | Om tillämpligt, momsregistreringsnumret eller [momsregistreringsnumret &#x200B;](../stores-purchase/vat.md) som tilldelats kunden. <br/><br/>Det här fältet är inte detsamma som momsregistreringsnumret. |
| **[!UICONTROL Gender]** | Kundens kön. |
| **[!UICONTROL Action]** | Redigera - Öppnar företagskontot i redigeringsläge. |

{style="table-layout:auto"}

### Ytterligare kolumner

De här kolumnerna är tillgängliga genom att ändra [kolumnlayouten](../getting-started/admin-grid-controls.md) för stödrastret.

| Kolumn | Beskrivning |
| --- | --- |
| **[!UICONTROL Company]** | Kundens företagsnamn. |
| **[!UICONTROL Street Address]** | Kundens gatuadress. |
| **[!UICONTROL City]** | Ort där kunden finns. |
| **[!UICONTROL Fax]** | Kundens faxnummer, om tillämpligt. |
| **[!UICONTROL Billing Firstname]** | Förnamnet i kundens faktureringsadress. |
| **[!UICONTROL Billing Lastname]** | Efternamnet i kundens faktureringsadress. |
| **[!UICONTROL Billing Address]** | Den adress dit faktureringsinformation ska skickas. |
| **[!UICONTROL Shipping Address]** | Den adress dit beställningar ska skickas. |
| **[!UICONTROL VAT Number]** | Momsnumret som är associerat med kundadressen. För [digitala varor](../stores-purchase/taxes.md) som säljs i EU baseras momsen på kundens faktureringsadress. <br/><br/>Det här fältet är inte detsamma som moms-/momsregistreringsnumret. |
| **[!UICONTROL Account Lock]** | Anger kontots status. Som en säkerhetsåtgärd kan kundkonton vara [låsta](../customers/password-options.md) efter för många inloggningsförsök. Värden: `Locked` / `Unlocked` |

{style="table-layout:auto"}
