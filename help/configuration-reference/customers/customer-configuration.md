---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Customer Configuration]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Customers] &gt; [!UICONTROL Customer Configuration] i Commerce Admin.
exl-id: 596359d7-3891-4e0c-9604-3647032188fd
feature: Configuration, Customers
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1890'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Customer Configuration]

{{config}}

## [!UICONTROL Account Sharing Options]

![Alternativ för kontodelning](./assets/customer-configuration-account-sharing-options.png)<!-- zoom -->

<!-- [Account Sharing Options](https://experienceleague.adobe.com/sv/docs/commerce-admin/customers/customer-accounts/customer-account-scope) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Share Customer Accounts] | Global | Bestämmer omfattningen för kundkonton i butikshierarkin. Alternativ: <br/>**`Global`**- Kundkontoinformation delas med alla webbplatser och butiker i Commerce-installationen.<br/>**`Per Website`** - Kundkontoinformationen är begränsad till webbplatsen där kontot skapades. |

{style="table-layout:auto"}

## [!UICONTROL Online Customers Options]

![Alternativ för onlinekunder](./assets/customer-configuration-online-customers-options.png)<!-- zoom -->

<!-- [Online Customers Options](https://experienceleague.adobe.com/sv/docs/commerce-admin/customers/customers-menu/now-online) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Online Minutes Interval] | Global | Anger hur länge en kunds onlineaktivitet är tillgänglig från administratören. Lämna tomt i standardintervallet 15 minuter. |
| [!UICONTROL Customer Data Lifetime] | Global | Fastställer antalet minuter innan osparade data som anges av kunden förfaller. Som standard upphör osparade data att gälla efter 60 minuter. |

{style="table-layout:auto"}

## [!UICONTROL Create New Account Options]

![Skapa nya kontoalternativ](./assets/customer-configuration-create-new-account-options.png)<!-- zoom -->

![Skapa nya kontoalternativ (momsfält)](./assets/customer-configuration-create-new-account-options-vat.png)<!-- zoom -->

<!-- [Create New Account Options (VAT Fields)](https://experienceleague.adobe.com/sv/docs/commerce-admin/customers/customer-accounts/configure/login-landing-page) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Automatic Assignment to Customer Group] | Butiksvy | Avgör om kunder automatiskt tilldelas standardkundgruppen. Om du vill visa momsregistreringsnumret i butiken anger du Visa momsregistreringsnummer i butiken och väljer `Yes`. Alternativ: <br/>**`Yes`**- Systemet validerar inte kundens moms-ID automatiskt och ändrar inte heller kundgrupper.<br/>**`No`** - Systembeteendet är som vanligt och standardkundgruppen kan anges i fältet Standardgrupp. |
| [!UICONTROL Default Group] | Butiksvy | Identifierar den första kundgruppen som tilldelas när ett konto skapas. |
| [!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID] | Global | (Endast tillgängligt om det aktuella konfigurationsomfånget är inställt på `Default Group`.) Välj om den automatiska ändringen av kundgrupp baserat på moms-ID är aktiverad eller inaktiverad som standard. Inställningen kan åsidosättas på produktnivå. Inställningen påverkar systembeteendet i följande situationer: <br/> - moms-ID för kundens standardadress eller hela standardadressen ändras. <br/> - Ändringen av kundgruppen emulerades under utcheckningen för en registrerad kund som inte hade någon tidigare sparad adress eller för en kund som registrerade sig under utcheckningen. <br/>Om den automatiska gruppändringen är aktiverad ändras kundgruppen automatiskt i det första fallet och i det andra fallet tilldelas den tillfälligt emulerade kundgruppen till kunden. Om den automatiska gruppändringen är inaktiverad ändras aldrig kundgruppen som tilldelas, såvida inte administratören ändrar den manuellt. |
| [!UICONTROL Show VAT Number on Storefront] | Webbplats | Avgör om momsregistreringsnumret är synligt för kunderna i butiken. Alternativ: `Yes` / `No` <br/> Påverkar endast vanliga icke-B2B-kundkonton. Företagskonton har sina egna separata fält för momsregistreringsnummer. |
| [!UICONTROL Default Email Domain] | Butiksvy | Identifierar butikens standarddomän för e-post. Till exempel: `mystore.com` |
| [!UICONTROL Default Welcome Email] | Butiksvy | Identifierar e-postmallen som används för standardmeddelandet _Välkommen_. |
| [!UICONTROL Default Welcome Email Without Password] | Butiksvy | En alternativ mall för välkomstmeddelanden som används för nya kundkonton som skapas av administratören och som ännu inte har tilldelats något lösenord. |
| [!UICONTROL Email Sender] | Butiksvy | Identifierar den butikskontakt som visas som avsändare av välkomstmeddelandet. |
| [!UICONTROL Require Emails Confirmation] | Webbplats | Avgör om en begäran om att skapa ett konto kräver en bekräftelse från kunden. Alternativ: `Yes` / `No`. <br/><br/> _&#x200B;**Obs!**&#x200B;_ Från och med version 2.4.7 måste kunderna ange sina e-postadresser och lösenord igen för att logga in på sina konton efter att e-postbekräftelsen har skickats, oavsett webbläsare. |
| [!UICONTROL Confirmation Link Email] | Butiksvy | Identifierar e-postmallen som används för bekräftelsemeddelandet. Standardmall: `New account confirmation key` |
| [!UICONTROL Welcome Email] | Butiksvy | Identifierar e-postmallen som används för välkomstmeddelandet som skickas när kontot har bekräftats. |
| [!UICONTROL Generate Human-Friendly Customer ID] | Global | Anger om fältet som används för att ange och lagra momsregistreringsnumret är synligt från butiken. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Password Options]

![Lösenordsalternativ](./assets/customer-configuration-password-options.png)<!-- zoom -->

<!-- [Password Options](https://experienceleague.adobe.com/sv/docs/commerce-admin/customers/customer-accounts/configure/password-options) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Password Reset Protection Type] | Butiksvy | Bestämmer vilken metod som används för att återställa ett lösenord för ett kundkonto. Alternativ: <br/>**`By IP and Email`**- Lösenordet kan återställas online efter att ett svar har tagits emot från ett återställningsmeddelande som skickas till den e-postadress som är kopplad till administratörskontot.<br/>**`By IP`** - Lösenordet kan återställas online. <br/>**`By Email`**- Lösenordet kan återställas genom att svara på ett e-postmeddelande som skickas till den e-postadress som är kopplad till administratörskontot.<br/>**`None`** - Lösenordet kan bara återställas av butiksadministratören. |
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

{style="table-layout:auto"}

## [!UICONTROL Account Information Options]

![Alternativ för kontoinformation](./assets/customer-configuration-account-info-options.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Change Email Template] | Butiksvy | Identifierar den standardmall för e-post som används när en kund ändrar sin e-postadress. |
| [!UICONTROL Change Email and Password Template] | Butiksvy | Identifierar den standardmall för e-post som används när en kund ändrar e-postadress och lösenord. |

{style="table-layout:auto"}

## [!UICONTROL Name and Address Options]

### Alternativ för Magento Open Source

{{ce-feature}}

![Alternativ för namn och adress - öppna Source](./assets/customer-configuration-name-address-options-ce.png)<!-- zoom -->

<!-- [Name and Address Options - Open Source](https://experienceleague.adobe.com/sv/docs/commerce-admin/customers/customer-accounts/configure/name-address-options) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Number of Lines in a Street Address] | Webbplats | Anger antalet rader i gatuadressen. Gatuadressen består av `1` till `4` rader. Om fältet är tomt används standardgatuadressen för tre (`3`) rader. |
| [!UICONTROL Show Prefix] | Webbplats | Avgör om kundnamnet innehåller ett prefix i början, till exempel Mr. och MS. Options: `No` / `Optional` / `Required` |
| [!UICONTROL Prefix Dropdown Options] | Webbplats | Definierar listan med prefixalternativ. Avgränsa värden med semikolon. Placera ett semikolon före det första värdet om du vill visa ett tomt värde högst upp i listan. |
| [!UICONTROL Show Middle Name (initial)] | Webbplats | Avgör om den mittersta initialen inkluderas som en del av kundnamnet. Om det används är den mittersta initialen ett valfritt fält. Alternativ: `Yes` / `No` |
| [!UICONTROL Show Suffix] | Webbplats | Avgör om kundnamnet innehåller ett suffix i slutet, till exempel Jr., Sr. och III. Alternativ: `No` / `Optional` / `Required` |
| [!UICONTROL Suffix Dropdown Options] | Webbplats | Definierar listan med suffixalternativ. Avgränsa värden med semikolon. Placera ett semikolon före det första värdet om du vill visa ett tomt värde högst upp i listan. |
| [!UICONTROL Show Date of Birth] | Webbplats | Avgör om kundens födelsedatum är inkluderat i namn- och adressformuläret. Alternativ: `No` / `Optional` / `Required` <br><br>**_Viktigt:_**&#x200B;I enlighet med gällande säkerhets- och sekretesspraxis bör du vara medveten om eventuella juridiska risker och säkerhetsrisker som är förknippade med lagring av kunders fullständiga födelsedatum (månad, dag, år) med andra personliga identifierare. Vi rekommenderar att du begränsar lagringen av kundernas födelsedatum och föreslår att du använder kundens födelseår som ett alternativ. |
| [!UICONTROL Show Tax/VAT Number] | Webbplats | Avgör om moms eller [momsregistreringsnummer](../../stores-purchase/vat.md) ingår i namn- och adressformuläret. Alternativ: `No` / `Optional` / `Required` |
| [!UICONTROL Show Gender] | Webbplats | Avgör om kön ingår i namn- och adressformuläret. Alternativ: `No` / `Optional` / `Required` |
| [!UICONTROL Show Telephone] | Webbplats | Avgör om kundens telefonnummer är inkluderat i namn- och adressformuläret. Alternativ: `No` / `Optional` / `Required` |
| [!UICONTROL Show Company] | Webbplats | Avgör om kundens företag ingår i namn- och adressformuläret. Alternativ: `No` / `Optional` / `Required` |
| [!UICONTROL Show Fax] | Webbplats | Avgör om kundens faxnummer är inkluderat i namn- och adressformuläret. Alternativ: `No` / `Optional` / `Required` |

{style="table-layout:auto"}

### Adobe Commerce-alternativ

{{ee-feature}}

![Alternativ för namn och adress - Commerce](./assets/customer-configuration-name-address-options-ee.png)<!-- zoom -->

<!-- [Name and Address Options - Commerce](https://experienceleague.adobe.com/sv/docs/commerce-admin/customers/customer-accounts/configure/name-address-options) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Prefix Dropdown Options] | Webbplats | Definierar listan med prefixalternativ. Avgränsa värden med semikolon. Placera ett semikolon före det första värdet om du vill visa ett tomt värde högst upp i listan. |
| [!UICONTROL Suffix Dropdown Options] | Webbplats | Definierar listan med suffixalternativ. Avgränsa värden med semikolon. Placera ett semikolon före det första värdet om du vill visa ett tomt värde högst upp i listan. |
| [!UICONTROL Show Telephone] | Webbplats | Avgör om kundens telefonnummer är inkluderat i namn- och adressformuläret. Alternativ: `No` / `Optional` / `Required` |
| [!UICONTROL Show Company] | Webbplats | Avgör om kundens företag ingår i namn- och adressformuläret. Alternativ: `No` / `Optional` / `Required` |
| [!UICONTROL Show Fax] | Webbplats | Avgör om kundens faxnummer är inkluderat i namn- och adressformuläret. Alternativ: `No` / `Optional` / `Required` |

{style="table-layout:auto"}

## [!UICONTROL Store Credit Options]

{{ee-feature}}

![Butikskreditalternativ](./assets/customer-configuration-store-credit-options.png)<!-- zoom -->

<!-- [Store Credit Options](https://experienceleague.adobe.com/sv/docs/commerce-admin/customers/customer-accounts/store-credit/credit-configure) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Store Credit Functionality] | Global | Avgör om Store Credit är aktiverat. Om du inaktiverar den tas Store Credit bort från kundkonton och från sidan Admin Manage Customers. Alternativ: `Yes` / `No`. |
| [!UICONTROL Show Store Credit History to Customers] | Webbplats | Avgör om saldohistoriken visas i kundkonton. Alternativ: `Yes` / `No`. |
| [!UICONTROL Refund Store Credit Automatically] | Global | Avgör om butiksåterbetalning utfärdas automatiskt. Alternativ: `Yes` / `No` |
| [!UICONTROL Store Credit Update Email Sender] | Butiksvy | Bestämmer den butiksidentitet som visas som avsändare av kredituppdateringsmeddelanden som skickas till kunder. |
| [!UICONTROL Store Credit Update Email Template] | Butiksvy | Bestämmer e-postmallen som används för kredituppdateringar. |

{style="table-layout:auto"}

## [!UICONTROL Login Options]

![Inloggningsalternativ](./assets/customer-configuration-login-options.png)<!-- zoom -->

<!-- [Login Options](https://experienceleague.adobe.com/sv/docs/commerce-admin/customers/customer-accounts/configure/login-landing-page) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Redirect Customer to Account Dashboard after Logging in] | Webbplats | Avgör vad som händer efter det att kunderna har loggat in på sina konton. Välj `Yes` om du vill dirigera om kunder till deras kontokontrollpanel. Alternativ: <br/>**`Yes`**- Kontokontrollpanelen visas när kunderna loggar in på sina konton.<br/>**`No`** - Kunder kan fortsätta att handla efter att ha loggat in på sina konton. |

{style="table-layout:auto"}

## [!UICONTROL Address Templates]

![Adressmallar](./assets/customer-configuration-address-templates.png)<!-- zoom -->

<!-- [Address Templates](https://experienceleague.adobe.com/sv/docs/commerce-admin/customers/customer-accounts/attributes/address-templates) -->

| Mall | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Text] | Butiksvy | Mallen används för alla adresser som skrivs ut. |
| [!UICONTROL Text One Line] | Butiksvy | Den här mallen definierar ordningen på adressenheter i kundens lista över kundvagnsadresser. Förlopp under utcheckning. |
| [!UICONTROL HTML] | Butiksvy | Den här mallen definierar ordningen för adressfält som finns under området _Kundadresser_ på panelen Admin ([!UICONTROL Customers] > [!UICONTROL Manage Customers]). Detta påverkar även dem som finns på sidan _Lägg till ny adress_ när en kund skapar en fakturerings- eller leveransadress på sin kontosida. |
| [!UICONTROL PDF] | Butiksvy | Mallen definierar hur fakturerings- och leveransadresserna visas på utskrivna fakturor, försändelser och kreditnotor. |

{style="table-layout:auto"}

## [!UICONTROL Customer Segments]

{{ee-feature}}

![Kundsegment](./assets/customer-configuration-customer-segments.png)<!-- zoom -->

<!-- [Customer Segments](https://experienceleague.adobe.com/sv/docs/commerce-admin/customers/segments/customer-segments) -->

| Mall | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Customer Segment Functionality] | Global | Avgör om kundsegment kan användas för att skapa riktade kampanjer. Alternativ: `Yes` / `No` |
| [!UICONTROL Real-time Check if Customer is Matched by Segment] | Global | Avgör om kundsegment valideras i realtid. Alternativ: <br/>**[!UICONTROL Yes]**- Kundsegment valideras i realtid (standardvärde).<br/>**[!UICONTROL No]** - Kundsegment valideras av en enda SQL-villkorsfråga. Detta förbättrar resultatet för segmentvalidering om det finns många kundsegment i systemet. Valideringen fungerar dock inte med en delad databas eller när det inte finns några registrerade kunder. |

{style="table-layout:auto"}

## [!UICONTROL CAPTCHA]

![CAPTCHA](./assets/customer-configuration-captcha.png)<!-- zoom -->

<!-- [CAPTCHA](https://experienceleague.adobe.com/sv/docs/commerce-admin/systems/security/captcha/security-captcha) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable CAPTCHA on Storefront] | Webbplats | Aktiverar CAPTCHA i butikerna som är kopplade till Commerce webbplats. Alternativ: `Yes` / `No` |
| [!UICONTROL Font] | Webbplats | Anger vilket teckensnitt som används för att visa CAPTCHA. Om du vill lägga till ett eget teckensnitt placerar du teckensnittsfilen i samma katalog som din Commerce-installation och lägger till deklarationen i filen `config.xml` på `app/code/Magento/Captcha/etc`. |
| [!UICONTROL Forms] | Webbplats | Bestämmer vilka formulär som CAPTCHA används i. Alternativ: <br />`Applying Coupon Code` <br />`Checkout/Placing Order`<br />`Create user` <br />`Login` <br />`Forgot password` <br />`Contact Us` <br />`Change password` <br />`Share Wishlist Form` <br />`Send to Friend Form` <br />`Payflow Pro` (se [säkerhetskorrigering](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html?lang=sv-SE)) <br />`Add Gift Card Code` ![Adobe Commerce](../../assets/adobe-logo.svg) <br />`Create company` ![Adobe Commerce](../../assets/adobe-logo.svg) <br /><br />_&#x200B;**Obs!**&#x200B;_ Formulären Skapa användare, Glömt lösenord och Payflow Pro är alltid aktiverat när det är markerat. |
| [!UICONTROL Displaying Mode] | Webbplats | Avgör när CAPTCHA visas. Alternativ: <br/>**`Always`**- CAPTCHA krävs alltid för inloggning.<br/>**`After number of attempts to login`** - Det här alternativet gäller bara för formuläret Administratörsinloggning. När du väljer det här alternativet visas fältet _[!UICONTROL Number of Unsuccessful Attempts to Login]_. Ange antalet inloggningsförsök som du vill tillåta. Värdet `0` (noll) liknar inställningen [!UICONTROL Displaying Mode] till `Always`.<br/>_&#x200B;**Obs!**&#x200B;_För att spåra antalet misslyckade inloggningsförsök räknas varje försök att logga in under en e-postadress och från en IP-adress. Det maximala antalet inloggningsförsök från samma IP-adress är 1 000. Den här begränsningen gäller bara när CAPTCHA är aktiverat. |
| [!UICONTROL Number of Unsuccessful Attempts to Login] | Webbplats | Anger hur många gånger en kund kan försöka logga in innan kontot är låst. |
| [!UICONTROL CAPTCHA Timeout (minutes)] | Webbplats | Anger livslängden för aktuell CAPTCHA. När CAPTCHA förfaller måste användaren läsa in sidan igen. |
| [!UICONTROL Number of Symbols] | Webbplats | Anger antalet symboler som visas i CAPTCHA, med maximalt 8. Du kan också ange ett intervall, till exempel 5-8. |
| [!UICONTROL Symbols Used in CAPTCHA] | Webbplats | Avgör vilka bokstäver (a-z och A-Z) och siffror (0-9) som visas i CAPTCHA. Symboler som är svåra att skilja från andra symboler, som `i`, `l` eller `1`, ingår inte i standarduppsättningen med CAPTCHA-symboler. |
| [!UICONTROL Case Sensitive] | Webbplats | Avgör om CAPTCHA-tecken är skiftlägeskänsliga. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}
