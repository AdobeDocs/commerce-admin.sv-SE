---
title: '[!UICONTROL Customers]  &gt; [!UICONTROL Customer Configuration]'
description: Granska konfigurationsinställningarna på [!UICONTROL Customers] &gt; [!UICONTROL Customer Configuration] sidan för Commerce Admin.
exl-id: 596359d7-3891-4e0c-9604-3647032188fd
feature: Configuration, Customers
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '1898'
ht-degree: 0%

---

# [!UICONTROL Customers]  > [!UICONTROL Customer Configuration]

{{config}}

## [!UICONTROL Account Sharing Options]

![Alternativ för kontodelning](./assets/customer-configuration-account-sharing-options.png)<!-- zoom -->

<!-- [Account Sharing Options](https://docs.magento.com/user-guide/customers/account-scope.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Share Customer Accounts] | Global | Bestämmer omfattningen för kundkonton i butikshierarkin. Alternativ: <br/>**`Global`**- Kundkontoinformationen delas med alla webbplatser och butiker i Commerce-installationen.<br/>**`Per Website`** - Kundkontoinformationen är begränsad till den webbplats där kontot skapades. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Online Customers Options]

![Alternativ för onlinekunder](./assets/customer-configuration-online-customers-options.png)<!-- zoom -->

<!-- [Online Customers Options](https://docs.magento.com/user-guide/customers/now-online.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Online Minutes Interval] | Global | Anger hur länge en kunds onlineaktivitet är tillgänglig från administratören. Lämna tomt i standardintervallet 15 minuter. |
| [!UICONTROL Customer Data Lifetime] | Global | Fastställer antalet minuter innan osparade data som anges av kunden förfaller. Som standard upphör osparade data att gälla efter 60 minuter. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Create New Account Options]

{{beta-updates}}

![Skapa nya kontoalternativ](./assets/customer-configuration-create-new-account-options.png)<!-- zoom -->

![Skapa nya kontoalternativ (momsfält)](./assets/customer-configuration-create-new-account-options-vat.png)<!-- zoom -->

<!-- [Create New Account Options (VAT Fields)](https://docs.magento.com/user-guide/customers/customer-account-configuration.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Automatic Assignment to Customer Group] | Butiksvy | Avgör om kunder automatiskt tilldelas standardkundgruppen. Om du vill visa momsregistreringsnumret i butiken anger du Visa momsregistreringsnummer i butiken och väljer `Yes`. Alternativ: <br/>**`Yes`**- Systemet validerar inte kundens moms-ID automatiskt och ändrar inte heller kundgrupper.<br/>**`No`** - Systembeteendet är som vanligt och standardkundgruppen kan ställas in i fältet Standardgrupp. |
| [!UICONTROL Default Group] | Butiksvy | Identifierar den första kundgruppen som tilldelas när ett konto skapas. |
| [!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID] | Global | (Endast tillgängligt om aktuellt konfigurationsomfång är inställt på `Default Group`.) Välj om den automatiska ändringen av kundgrupp baserat på moms-ID är aktiverad eller inaktiverad som standard. Inställningen kan åsidosättas på produktnivå. Inställningen påverkar systembeteendet i följande situationer: <br/> - Moms-ID för kundens standardadress eller hela standardadressen ändras. <br/> - Ändringen av kundgruppen emulerades under utcheckningen för en registrerad kund som inte hade någon tidigare sparad adress eller för en kund som registrerade sig under utcheckningen. <br/>Om den automatiska gruppändringen är aktiverad ändras kundgruppen automatiskt i det första fallet, och i det andra fallet tilldelas den tillfälligt emulerade kundgruppen. Om den automatiska gruppändringen är inaktiverad ändras aldrig kundgruppen som tilldelas, såvida inte administratören ändrar den manuellt. |
| [!UICONTROL Show VAT Number on Storefront] | Webbplats | Avgör om momsregistreringsnumret är synligt för kunderna i butiken. Alternativ: `Yes` / `No` <br/> Påverkar endast vanliga icke-B2B-kundkonton. Företagskonton har sina egna separata fält för momsregistreringsnummer. |
| [!UICONTROL Default Email Domain] | Butiksvy | Identifierar butikens standarddomän för e-post. Exempel: `mystore.com` |
| [!UICONTROL Default Welcome Email] | Butiksvy | Identifierar e-postmallen som används som standard _Välkommen_ e-post. |
| [!UICONTROL Default Welcome Email Without Password] | Butiksvy | En alternativ mall för välkomstmeddelanden som används för nya kundkonton som skapas av administratören och som ännu inte har tilldelats något lösenord. |
| [!UICONTROL Email Sender] | Butiksvy | Identifierar den butikskontakt som visas som avsändare av välkomstmeddelandet. |
| [!UICONTROL Require Emails Confirmation] | Webbplats | Avgör om en begäran om att skapa ett konto kräver en bekräftelse från kunden. Alternativ: `Yes` / `No` |
| [!UICONTROL Confirmation Link Email] | Butiksvy | Identifierar e-postmallen som används för bekräftelsemeddelandet. Standardmall: `New account confirmation key` |
| [!UICONTROL Welcome Email] | Butiksvy | Identifierar e-postmallen som används för välkomstmeddelandet som skickas när kontot har bekräftats. |
| [!UICONTROL Generate Human-Friendly Customer ID] | Global | Anger om fältet som används för att ange och lagra momsregistreringsnumret är synligt från butiken. Alternativ: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Password Options]

![Alternativ för lösenord](./assets/customer-configuration-password-options.png)<!-- zoom -->

<!-- [Password Options](https://docs.magento.com/user-guide/customers/password-options.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Password Reset Protection Type] | Butiksvy | Bestämmer vilken metod som används för att återställa ett lösenord för ett kundkonto. Alternativ: <br/>**`By IP and Email`**- Lösenordet kan återställas online när ett svar har tagits emot från ett återställningsmeddelande som skickas till den e-postadress som är kopplad till administratörskontot.<br/>**`By IP`** - Lösenordet kan återställas online. <br/>**`By Email`**- Lösenordet kan återställas genom att svara på ett e-postmeddelande som skickas till den e-postadress som är kopplad till administratörskontot.<br/>**`None`** - Lösenordet kan bara återställas av butiksadministratören. |
| [!UICONTROL Max Number of Password Reset Requests] | Butiksvy | Begränsar antalet begäranden om återställning av lösenord per timme. För obegränsade begäranden anger du noll (0). |
| [!UICONTROL Min Time Between Password Reset Requests] | Butiksvy | Anger antalet minuter mellan begäranden om återställning av lösenord. Ange noll (0) om det inte ska dröja något mellan begäranden. |
| [!UICONTROL Forgot Email Template] | Butiksvy | Identifierar den e-postmall som används när kunderna glömmer sina lösenord. Standardmall: `Forgot Password` |
| [!UICONTROL Remind Email Template] | Butiksvy | Identifierar e-postmallen som används när kunderna får en lösenordspåminnelse eller tips. Standardmall: `Remind Password` |
| [!UICONTROL Reset Password Template] | Butiksvy | Bestämmer e-postmallen som används när kunderna återställer sina lösenord. |
| [!UICONTROL Password Template Email Sender] | Butiksvy | Anger den butikskontakt som visas som avsändare av lösenordsrelaterade e-postmeddelanden. |
| [!UICONTROL Recovery Link Expiration Period (hours)] | Global | Anger antalet timmar innan en länk för lösenordsåterställning går ut. |
| [!UICONTROL Enable Autocomplete on login/forgot password forms] | Webbplats | Avgör om Fyll i automatiskt är aktiverat i lösenordsformulär för inloggning/glömt. Alternativ: `Yes` / `No` |
| [!UICONTROL Number of Required Character Classes] | Global | Anger antalet olika teckenklasser (gemener, versaler, numeriska tecken och specialtecken) som måste ingå i ett lösenord. |
| [!UICONTROL Maximum Login Failures to Lockout Account] | Global | Fastställer antalet misslyckade inloggningsförsök tills kundkontot är låst. För obegränsat antal försök anger du noll (`0`). |
| [!UICONTROL Minimum Password Length] | Global | Anger det minsta antalet tecken som tillåts i ett lösenord. Talet måste vara större än noll (`0`). |
| [!UICONTROL Lockout Time (minutes)] | Global | Anger hur många minuter ett kundkonto är låst efter för många misslyckade inloggningsförsök. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Account Information Options]

![Alternativ för kontoinformation](./assets/customer-configuration-account-info-options.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Change Email Template] | Butiksvy | Identifierar den standardmall för e-post som används när en kund ändrar sin e-postadress. |
| [!UICONTROL Change Email and Password Template] | Butiksvy | Identifierar den standardmall för e-post som används när en kund ändrar e-postadress och lösenord. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Name and Address Options]

### Alternativ för Magento Open Source

{{ce-feature}}

![Alternativ för namn och adress - öppen källa](./assets/customer-configuration-name-address-options-ce.png)<!-- zoom -->

<!-- [Name and Address Options - Open Source](https://docs.magento.com/user-guide/customers/name-address-options.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Number of Lines in a Street Address] | Webbplats | Anger antalet rader i gatuadressen. Gatuadressen består av `1` till `4` rader. Om fältet är tomt är standardgatuadressen tre (`3`) rader används. |
| [!UICONTROL Show Prefix] | Webbplats | Avgör om kundnamnet innehåller ett prefix i början, t.ex. Mr. och Ms. Options: `No` / `Optional` / `Required` |
| [!UICONTROL Prefix Dropdown Options] | Webbplats | Definierar listan med prefixalternativ. Avgränsa värden med semikolon. Placera ett semikolon före det första värdet om du vill visa ett tomt värde högst upp i listan. |
| [!UICONTROL Show Middle Name (initial)] | Webbplats | Avgör om den mittersta initialen inkluderas som en del av kundnamnet. Om det används är den mittersta initialen ett valfritt fält. Alternativ: `Yes` / `No` |
| [!UICONTROL Show Suffix] | Webbplats | Avgör om kundnamnet innehåller ett suffix i slutet, till exempel Jr., Sr. och III. Alternativ: `No` / `Optional` / `Required` |
| [!UICONTROL Suffix Dropdown Options] | Webbplats | Definierar listan med suffixalternativ. Avgränsa värden med semikolon. Placera ett semikolon före det första värdet om du vill visa ett tomt värde högst upp i listan. |
| [!UICONTROL Show Date of Birth] | Webbplats | Avgör om kundens födelsedatum är inkluderat i namn- och adressformuläret. Alternativ: `No` / `Optional` / `Required`  <br><br>**_Viktigt:_**I enlighet med gällande säkerhets- och integritetspraxis bör du vara medveten om eventuella juridiska risker och säkerhetsrisker som är förknippade med lagring av kundernas fullständiga födelsedatum (månad, dag, år) med andra personliga identifierare. Vi rekommenderar att du begränsar lagringen av kundernas födelsedatum och föreslår att du använder kundens födelseår som ett alternativ. |
| [!UICONTROL Show Tax/VAT Number] | Webbplats | Bestämmer om momsen eller [Momsnummer](../../stores-purchase/vat.md) finns i namn- och adressformuläret. Alternativ: `No` / `Optional` / `Required` |
| [!UICONTROL Show Gender] | Webbplats | Avgör om kön ingår i namn- och adressformuläret. Alternativ: `No` / `Optional` / `Required` |
| [!UICONTROL Show Telephone] | Webbplats | Avgör om kundens telefonnummer är inkluderat i namn- och adressformuläret. Alternativ: `No` / `Optional` / `Required` |
| [!UICONTROL Show Company] | Webbplats | Avgör om kundens företag ingår i namn- och adressformuläret. Alternativ: `No` / `Optional` / `Required` |
| [!UICONTROL Show Fax] | Webbplats | Avgör om kundens faxnummer är inkluderat i namn- och adressformuläret. Alternativ: `No` / `Optional` / `Required` |

{:style=&quot;table-layout:auto&quot;}

### Adobe Commerce-alternativ

{{ee-feature}}

![Alternativ för namn och adress - Handel](./assets/customer-configuration-name-address-options-ee.png)<!-- zoom -->

<!-- [Name and Address Options - Commerce](https://docs.magento.com/user-guide/customers/name-address-options.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Prefix Dropdown Options] | Webbplats | Definierar listan med prefixalternativ. Avgränsa värden med semikolon. Placera ett semikolon före det första värdet om du vill visa ett tomt värde högst upp i listan. |
| [!UICONTROL Suffix Dropdown Options] | Webbplats | Definierar listan med suffixalternativ. Avgränsa värden med semikolon. Placera ett semikolon före det första värdet om du vill visa ett tomt värde högst upp i listan. |
| [!UICONTROL Show Telephone] | Webbplats | Avgör om kundens telefonnummer är inkluderat i namn- och adressformuläret. Alternativ: `No` / `Optional` / `Required` |
| [!UICONTROL Show Company] | Webbplats | Avgör om kundens företag ingår i namn- och adressformuläret. Alternativ: `No` / `Optional` / `Required` |
| [!UICONTROL Show Fax] | Webbplats | Avgör om kundens faxnummer är inkluderat i namn- och adressformuläret. Alternativ: `No` / `Optional` / `Required` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Store Credit Options]

{{ee-feature}}

![Butikskreditalternativ](./assets/customer-configuration-store-credit-options.png)<!-- zoom -->

<!-- [Store Credit Options](https://docs.magento.com/user-guide/customers/credit-configure.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Store Credit Functionality] | Global | Avgör om Store Credit är aktiverat. Om du inaktiverar den tas Store Credit bort från kundkonton och från sidan Admin Manage Customers. Alternativ: `Yes` / `No`. |
| [!UICONTROL Show Store Credit History to Customers] | Webbplats | Avgör om saldohistoriken visas i kundkonton. Alternativ: `Yes` / `No`. |
| [!UICONTROL Refund Store Credit Automatically] | Global | Avgör om butiksåterbetalning utfärdas automatiskt. Alternativ: `Yes` / `No` |
| [!UICONTROL Store Credit Update Email Sender] | Butiksvy | Bestämmer den butiksidentitet som visas som avsändare av kredituppdateringsmeddelanden som skickas till kunder. |
| [!UICONTROL Store Credit Update Email Template] | Butiksvy | Bestämmer e-postmallen som används för kredituppdateringar. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Login Options]

![Inloggningsalternativ](./assets/customer-configuration-login-options.png)<!-- zoom -->

<!-- [Login Options](https://docs.magento.com/user-guide/customers/login-landing-page.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Redirect Customer to Account Dashboard after Logging in] | Webbplats | Avgör vad som händer efter det att kunderna har loggat in på sina konton. Om du vill dirigera om kunder till deras kontouppläggningar väljer du `Yes`. Alternativ: <br/>**`Yes`**- Kontrollpanelen för kontot visas när kunderna loggar in på sina konton.<br/>**`No`** - Kunderna kan fortsätta handla efter att ha loggat in på sina konton. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Address Templates]

![Adressmallar](./assets/customer-configuration-address-templates.png)<!-- zoom -->

<!-- [Address Templates](https://docs.magento.com/user-guide/customers/address-templates.html) -->

| Mall | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Text] | Butiksvy | Mallen används för alla adresser som skrivs ut. |
| [!UICONTROL Text One Line] | Butiksvy | Den här mallen definierar ordningen på adressenheter i kundens lista över kundvagnsadresser. Förlopp under utcheckning. |
| [!UICONTROL HTML] | Butiksvy | Den här mallen definierar ordningen för adressfält som finns under _Kundadresser_ i administrationspanelen ([!UICONTROL Customers] > [!UICONTROL Manage Customers]). Detta påverkar även dem som _Lägg till ny adress_ sida när en kund skapar en faktura- eller leveransadress på sin kontosida. |
| [!UICONTROL PDF] | Butiksvy | Mallen definierar hur fakturerings- och leveransadresserna visas på utskrivna fakturor, försändelser och kreditnotor. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Customer Segments]

{{ee-feature}}

![Kundsegment](./assets/customer-configuration-customer-segments.png)<!-- zoom -->

<!-- [Customer Segments](https://docs.magento.com/user-guide/marketing/customer-segments.html) -->

| Mall | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Customer Segment Functionality] | Global | Avgör om kundsegment kan användas för att skapa riktade kampanjer. Alternativ: `Yes` / `No` |
| [!UICONTROL Real-time Check if Customer is Matched by Segment] | Global | Avgör om kundsegment valideras i realtid. Alternativ: <br/>**[!UICONTROL Yes]**- Kundsegment valideras i realtid (standardvärde).<br/>**[!UICONTROL No]** - Kundsegment valideras av en enda SQL-villkorsfråga. Detta förbättrar resultatet för segmentvalidering om det finns många kundsegment i systemet. Valideringen fungerar dock inte med en delad databas eller när det inte finns några registrerade kunder. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL CAPTCHA]

![CAPTCHA](./assets/customer-configuration-captcha.png)<!-- zoom -->

<!-- [CAPTCHA](https://docs.magento.com/user-guide/stores/security-captcha.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable CAPTCHA on Storefront] | Webbplats | Aktiverar CAPTCHA i butikerna som är kopplade till Commerce-webbplatsen. Alternativ: `Yes` / `No` |
| [!UICONTROL Font] | Webbplats | Anger vilket teckensnitt som används för att visa CAPTCHA. Om du vill lägga till ett eget teckensnitt placerar du teckensnittsfilen i samma katalog som din Commerce-installation och lägger till deklarationen i `config.xml` fil på `app/code/Magento/Captcha/etc`. |
| [!UICONTROL Forms] | Webbplats | Bestämmer vilka formulär som CAPTCHA används i. Alternativ: <br />`Applying Coupon Code` <br />`Checkout/Placing Order`<br />`Create user` <br />`Login` <br />`Forgot password` <br />`Contact Us` <br />`Change password` <br />`Share Wishlist Form` <br />`Send to Friend Form` <br />`Payflow Pro` (se [säkerhetsuppdatering](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html)) <br />`Add Gift Card Code` ![Adobe Commerce](../../assets/adobe-logo.svg)  <br />`Create company` ![Adobe Commerce](../../assets/adobe-logo.svg)  <br /><br />_**Obs!**_ Formulären Skapa användare, Glömt lösenord och Payflow Pro aktiveras alltid när de markeras. |
| [!UICONTROL Displaying Mode] | Webbplats | Avgör när CAPTCHA visas. Alternativ: <br/>**`Always`**- CAPTCHA krävs alltid för att logga in.<br/>**`After number of attempts to login`** - Det här alternativet gäller endast för inloggningsformuläret för administratörer. När du väljer det här alternativet visas _[!UICONTROL Number of Unsuccessful Attempts to Login]_visas. Ange antalet inloggningsförsök som du vill tillåta. Värdet för `0` (noll) liknar inställningen [!UICONTROL Displaying Mode] till `Always`.<br/>_**Obs!**_För att spåra antalet misslyckade inloggningsförsök räknas varje försök att logga in under en e-postadress och från en IP-adress. Det maximala antalet inloggningsförsök från samma IP-adress är 1 000. Den här begränsningen gäller bara när CAPTCHA är aktiverat. |
| [!UICONTROL Number of Unsuccessful Attempts to Login] | Webbplats | Anger hur många gånger en kund kan försöka logga in innan kontot är låst. |
| [!UICONTROL CAPTCHA Timeout (minutes)] | Webbplats | Anger livslängden för aktuell CAPTCHA. När CAPTCHA förfaller måste användaren läsa in sidan igen. |
| [!UICONTROL Number of Symbols] | Webbplats | Anger antalet symboler som visas i CAPTCHA, med maximalt 8. Du kan också ange ett intervall, till exempel 5-8. |
| [!UICONTROL Symbols Used in CAPTCHA] | Webbplats | Avgör vilka bokstäver (a-z och A-Z) och siffror (0-9) som visas i CAPTCHA. Symboler som är svåra att skilja från andra symboler, till exempel `i`, `l`, eller `1`, ingår inte i standarduppsättningen med CAPTCHA-symboler. |
| [!UICONTROL Case Sensitive] | Webbplats | Avgör om CAPTCHA-tecken är skiftlägeskänsliga. Alternativ: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}
