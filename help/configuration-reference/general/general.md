---
title: '[!UICONTROL General] &gt; [!UICONTROL General]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL General] &gt; [!UICONTROL General] i Commerce Admin.
exl-id: 67760d24-ad12-4c49-9649-0607c57f5cf0
feature: Configuration, System
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL General]

{{config}}

## [!UICONTROL Country Options]

Mer information om dessa konfigurationsfält och alternativ finns i [Alternativ för länder](../../getting-started/store-details.md#country-options).

![Allmänt > Alternativ för länder](./assets/general-country-options.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Default Country] | Butiksvy | Det land där din butik finns. |
| [!UICONTROL Allow Countries] | Webbplats | De länder där du godkänner beställningar. |
| [!UICONTROL Zip/Postal Code is Optional for] | Global | Länder som inte kräver postnummer i leveransadressen. |
| [!UICONTROL European Union Countries] | Global | Länder som är medlemmar i Europeiska unionen. |
| [!UICONTROL Top Destinations] | Butiksvy | De primära länder som du riktar in dig på för försäljning. |

{style="table-layout:auto"}

## [!UICONTROL State Options]

Mer information om dessa konfigurationsfält och alternativ finns i [Tillståndsalternativ](../../getting-started/store-details.md#state-options).

![Allmänt > Lägesalternativ](./assets/general-state-options.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL State is required for] | Global | De länder (där du bedriver verksamhet) som kräver att en region eller stat ska anges i postadressen. |
| [!UICONTROL Allow to Choose State if It is Optional for Country] | Global | För länder där det inte är obligatoriskt, avgör om fältet _Region/delstat_ är inkluderat i kundens postadress.<br /> <br />**`Yes`**- Inkluderar fältet _Region/delstat_ i kundadressen, även om det inte krävs av landet.<br />**`No`** - Utelämnar fältet Region/delstat från kundadressen om det inte krävs av landet. |

{style="table-layout:auto"}

## [!UICONTROL Locale Options]

Mer information om dessa konfigurationsfält och alternativ finns i [Språkalternativ](../../getting-started/store-details.md#locale-options).

![Allmänt > Språkalternativ](./assets/general-locale-options.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Timezone] | Webbplats | Den tidszon på primärmarknaden som betjänas av webbplatsen. Vanligtvis är tidszonen densamma som den som används i ditt företags fysiska plats. |
| [!UICONTROL Locale] | Butiksvy | Språk, valuta och måttsystem som används på den marknad som butiksvyn betjänar. |
| [!UICONTROL Weight Unit] | Butiksvy | Den måttenhet som vanligtvis används för leveranser från språkområdet. Alternativ: `lbs` / `kgs` |
| [!UICONTROL First Day of Week] | Butiksvy | Den dag som anses vara den första dagen i veckan på den marknad som butiksvyn betjänar. |
| [!UICONTROL Weekend Days] | Butiksvy | Dagar som infaller på helgen på marknaden som hanteras av butiksvyn. |

{style="table-layout:auto"}

## [!UICONTROL Website Restrictions]

{{ee-feature}}

![Allmänt > Begränsningar för webbplatser](./assets/general-website-restrictions.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Åtkomstbegränsningar](../../merchandising-promotions/event-configure.md#access-restrictions) i _Handboken för marknadsföring och marknadsföring_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Access Restriction] | Webbplats | Avgör om webbplatsen fungerar i begränsat läge.<br /> <br />**`Yes`**- Webbplatsåtkomst är begränsad på det sätt som anges i fälten nedan.<br />**`No`** - Begränsningar är inaktiverade och följande inställningar har ingen effekt. |
| [!UICONTROL Restriction Mode] | Webbplats | Anger vilken typ av åtkomstbegränsning som gäller för webbplatsen.<br /> <br />**`Website Closed`**- All åtkomst till butikens framsida är begränsad, och butikens URL:er omdirigeras tillfälligt till landningssidan. Den här inställningen kan vara användbar vid webbplatsunderhåll eller före start.<br />**`Private Sales: Login Only`** - Endast registrerade kunder kan logga in för att komma åt butiken. Alla butiks-URL:er omdirigeras tillfälligt till antingen den angivna landningssidan eller inloggningsformuläret. Användare kan inte skapa ett konto i det här läget.<br />**`Private Sales: Login and Register`**- Användare måste logga in för att komma åt butiken. Alla butiks-URL:er omdirigeras tillfälligt till inloggningsformuläret tills användaren loggar in. Användare kan registrera sig för ett konto medan webbplatsen är i det här läget. |
| [!UICONTROL Startup Page] | Butiksvy | När webbplatsen är i läget Privat försäljning avgör den här inställningen vilken sida som visas tills kunden loggar in.<br />  <br />**`To login form`**- Användare omdirigeras till inloggningsformuläret tills de loggar in.<br />**`To landing page`** - Användare omdirigeras till den statiska sidan som anges nedan tills de loggar in.<br /> <br />**_Viktigt!_**Se till att du inkluderar en länk till inloggningssidan från den angivna landningssidan så att kunderna kan logga in för att komma åt den fullständiga webbplatsen. |
| [!UICONTROL Landing Page] | Butiksvy | Bestämmer den första sidan som visas när webbplatsen är i läget Privat försäljning. |
| [!UICONTROL HTTP Response] | Webbplats | Bestämmer det HTTP-svar som skickas när webbplatsen stängs och en anslutning görs av en robot, crawler eller spindel.<br /> <br />**`503 Service unavailable`**- Sidan är inte tillgänglig, men spindeln bör inte uppdatera indexet.<br />**`200 OK`** - landningssidan är korrekt och ska av spindeln behandlas som den enda sidan på platsen. |
| [!UICONTROL Enable Autocomplete on login/forgot password forms] | Webbplats | Avgör om fälten i formulären _Inloggning_ och _Glömt lösenord_ fylls i automatiskt från tidigare poster. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Store Information]

![Allmänt > Lagra information](./assets/general-store-information.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Lagra information](../../getting-started/store-details.md) i _Komma igång-guiden_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Store Name] | Butiksvy | Namnet på den butik som är associerad med butiksvyn. |
| [!UICONTROL Store Phone Number] | Butiksvy | Butikens primära telefonnummer (kopplat till butiksvyn) är öppet för företag. Till exempel: Mån - fre, 9-5, Lör 9-16 PST |
| Land | Webbplats | Det land där företaget som driver webbplatsen är beläget. |
| [!UICONTROL Region/State] | Webbplats | Regionen eller delstaten för det företag som driver webbplatsen. |
| [!UICONTROL ZIP/Postal Code] | Webbplats | Postnummer för det företag som driver webbplatsen. |
| [!UICONTROL City] | Webbplats | Platsen för det företag som driver webbplatsen. |
| [!UICONTROL Street Address] | Webbplats | Gatuadress eller adress till det företag som driver webbplatsen. |
| [!UICONTROL Street Address Line 2|]Webbplats | Affärsgatans andra linje, om det behövs. |
| [!UICONTROL VAT Number] | Webbplats | Momsnumret för det företag som äger Commerce-installationen, om tillämpligt. |
| [!UICONTROL Validate VAT Number] |  | Verifierar momsregistreringsnumret. |

{style="table-layout:auto"}

## [!UICONTROL Single-Store Mode]

![Allmänt > Enbutiksläge](./assets/general-single-store-mode.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Enkelt lagringsläge](../../getting-started/websites-stores-views.md#single-store-mode) i _Starthandboken_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Single-Store Mode] | Global | När det är aktiverat för single store-installationer döljs konfigurationsomfångsrutan och relaterade fältetiketter Alternativ: `Yes` / `No` <br/>**_Obs!_**Enstaka lagringsläge ignoreras för butiker med mer än en vy.<br/> Om du aktiverar läget för en lagringsplats kopieras alla katalog- och produktarkivspecifika data från standardbutiksvyn till alla lagringsvyomfång. Den kopierar bara katalog- och produktdata om butiken bara har en granskning. Om arkivet har en inaktiverad butiksgranskning och en aktiverad butik kopieras inte katalog- och produktdata.<br/> Om du aktiverar läget för en enskild lagring ignoreras de butiksspecifika konfigurationsinställningarna för innehållsspecifika data. I stället används konfigurationsinställningar som definierats på den globala nivån för att säkerställa konsekvens mellan administratörsgränssnittet och butiken. |

{style="table-layout:auto"}

## [!UICONTROL Data Services]

![Allmänt > Datatjänster](./assets/general-data-services.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Commerce Events Enabled] | Global | Den här konfigurationen är inaktiverad som standard om du är vårdkund och har installerat tillägget [Data Services HIPAA](https://experienceleague.adobe.com/en/docs/commerce/data-connection/hipaa-readiness). Detta innebär att händelsedata för storefront som används av Live Search och produktrekommendationer inte längre registreras. Detta beror på att händelsedata för storefront genereras på klientsidan. Om du vill fortsätta att hämta och skicka händelsedata för butiker som ska användas av tjänsterna [Live Search](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview) och [Produktrekommendationer](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview) anger du **Commerce Events Enabled** till `Yes`. |

{style="table-layout:auto"}
