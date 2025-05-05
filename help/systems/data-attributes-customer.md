---
title: Referens för kunddataattribut
description: Använd den här referensen för kunddataattribut när du arbetar med kunddataimport och -export.
exl-id: d22ebfed-f439-4a3f-b39e-e957b65c8c21
feature: Customers, Attributes
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# Referens för kunddataattribut

I följande tabell visas attributen från en typisk export av kundens huvudfil och kundadresser. Installationen som användes för att exportera dessa data har två webbplatser och flera butiksvyer, med exempeldata installerade.

Varje attribut, eller fält, representeras i CSV-filen som en kolumn, och kundposter representeras av rader. Kolumner som börjar med ett understreck är tjänstenheter som innehåller egenskaper eller komplexa data.

## Kundens huvudfil

| Attribut | Beskrivning |
|--- |--- |
| `email` | Kundens e-postadress. |
| `_website` |  |
| `_store` |  |
| `confirmation` | Bekräftelseflagga. |
| `created_at` | Datumet då kundkontot skapades. |
| `created_in` | Butiksvyn där kontot skapades. |
| `disable_auto_group_change` | Avgör om kundgrupper kan tilldelas dynamiskt under moms-ID-validering. |
| `dob` | Kundens födelsedatum. <br><br>**_Viktigt!_**&#x200B;I enlighet med aktuella säkerhets- och sekretessrutiner bör du granska lagring och bearbetning av kundernas fullständiga födelsedatum (månad, dag, år). När det samlas in med andra personliga identifierare (till exempel_fullständigt namn _) är det en potentiell juridisk risk och säkerhetsrisk. Vi rekommenderar att man begränsar lagringen av kundernas födelsedatum och istället föreslår att man använder kundens födelseår som ett alternativ. |
| `firstname` | Kundens förnamn. |
| `gender` | Kundens kön. |
| `group_id` | ID för kundgruppen där kunden är tilldelad. |
| `lastname` | Kundens efternamn. |
| `middlename` | Kundens mellannamn eller mellaninitial. |
| `password_hash` | Lösenordshash |
| `prefix` | Alla prefix som används med kundnamnet (till exempel `Mr.`, `Ms.`, `Mrs.` och `Dr.`). |
| `rp_token` | Återställ lösenordstoken. |
| `rp_token_created_at` | Datum när lösenordet återställdes. |
| `store_id` | Butiks-ID |
| `suffix` | Alla suffix som används med kundnamnet (till exempel `Jr.`, `Sr.` och `Esquire`). |
| `taxvat` |  |
| `website_id` | Webbplats-ID för webbplatsen där kundkontot skapades. |
| `password` | Kundens lösenord. |

{style="table-layout:auto"}

## Kundadresser

| Attribut | Beskrivning |
|--- |--- |
| `_website` |  |
| `_email` |  |
| `_entity_id` |  |
| `city` | Ort där kundadressen finns. |
| `company` | Företagsnamn, om tillämpligt för den här adressen. |
| `country_id` | Det land-ID där kundadressen finns. |
| `fax` | Kundens faxnummer, om tillämpligt. |
| `firstname` | Kundens förnamn. |
| `lastname` | Kundens efternamn. |
| `middlename` | Kundens mellannamn eller mellaninitial. |
| `postcode` | Postnumret där kundadressen finns. |
| `prefix` | Alla prefix som används med kundnamnet (till exempel `Mr.`, `Ms.`, `Mrs.` och `Dr.`). |
| `region` | Regionen där kundadressen finns. |
| `region_id` | Region-ID |
| `street` | Kundens gatuadress. En andra rad av gatuadressen är tillgänglig om den anges i konfigurationen. |
| `suffix` | Om det används är det suffix som är associerat med kundens namn (till exempel `Jr.`, `Sr.` eller `III`). |
| `telephone` | Kundens telefonnummer som är kopplat till adressen. |
| `vat_id` | Moms-ID är en intern identifierare för kundens momsregistreringsnummer när det används vid momsvalidering. |
| `vat_is_valid` |  |
| `vat_request_date` |  |
| `vat_request_id` |  |
| `vat_request_success` |  |
| `_address_default_billing_` | Identifierar standardfaktureringsadressen. Värdet `1` anger att adressen är kundens standardfaktureringsadress. Värden: 1 / 0 |
| `_address_default_shipping_` | Identifierar standardleveransadressen. Värdet `1` anger att adressen är kundens standardleveransadress. Värden: `1` / `0` |

{style="table-layout:auto"}
