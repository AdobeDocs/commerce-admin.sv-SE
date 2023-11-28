---
title: Skapa ett enskilt kundkonto
description: Besökarna kan enkelt skapa ett individuellt kundkonto för att hantera sina inköp.
exl-id: 8d08c0e1-f3ba-4423-98a7-ffa8ba5a1b8b
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 0%

---

# Skapa ett enskilt kundkonto

Besökare i din butik kan öppna ett konto för att hantera sina inköp och aktiviteter. Kunderna skapar vanligtvis egna konton från din butik. Du kan även skapa kundkonton direkt från administratören, vilket är användbart om du vill hjälpa kunder via telefon.

Följande instruktioner representerar standardkonfigurationen för kundkontot. Information om hur du ändrar markering och beteende för vissa fält i formuläret finns i [Konfigurera kundkonton](../customers/customer-account-scope.md).

Som butiksadministratör kan du även ange [nya kontoalternativ](../customers/account-options-new.md) för att skicka en bekräftelse via e-post till nya registrerade kunder, vilket gör det lättare att säkerställa att registrerade konton är giltiga.

{{beta-updates}}

## Skapa konto från butiken

En butikskund skapar ett konto i butiken.

1. I butiken klickar du **[!UICONTROL Create an Account]** i sidhuvudets övre högra hörn.

   ![Skapa ett konto](assets/storefront-create-an-account-link.png){width="700" zoomable="yes"}

1. Under **[!UICONTROL Personal Information]**, anger **[!UICONTROL First Name]** och **[!UICONTROL Last Name]**.

   ![Personlig information](assets/storefront-create-account-personal-information.png){width="600" zoomable="yes"}

1. Om de vill lägga till sitt namn och sin e-postadress i listan över nyhetsbrevets prenumeranter väljer kunden **[!UICONTROL Sign Up for Newsletter]** kryssrutan.

   >[!INFO]
   >
   > Det här alternativet visas även om butiken inte publicerar något nyhetsbrev.

1. Om de vill lagra supportpersonalen på [se vad de ser](../customers/login-as-customer.md) och ger fjärrhjälp väljer kunden **[!UICONTROL Allow remote shopping assistance]** kryssrutan.

1. Under **[!UICONTROL Sign-in Information]**, anger **[!UICONTROL Email]** adress.

   >[!INFO]
   >
   > Den här e-postadressen blir en del av inloggningsuppgifterna och kan inte kopplas till något annat kundkonto.

   ![Inloggningsinformation](assets/storefront-create-account-signin-information.png){width="600" zoomable="yes"}

1. Skriver in a **[!UICONTROL Password]** som innehåller tre av följande typer av information:

   - Gemener
   - Versaler
   - Nummer
   - Specialtecken

   Efter att de tryckt **[!UICONTROL Enter]**, utvärderas lösenordets styrka och visas under fältet. Om lösenordet anses vara _Svag_ kan du prova ett annat tills det utvärderas som _Stark_.

   ![Ett starkt lösenord rekommenderas](assets/storefront-customer-account-create-password-strong.png){width="600" zoomable="yes"}

1. Sedan anger kunden det igen för **[!UICONTROL Confirm Password]**.

1. Klicka vid behov **[!UICONTROL Show Password]** för att visa lösenordet du angav.

1. När det är klart klickar du **Skapa ett konto**.

Kunden kan sedan använda sin e-postadress och sitt lösenord för att [logga in](../customers/customer-sign-in.md) till deras konto och fyll i adressinformationen.

## Skapa ett konto från administratören

Som handlare kan du skapa ett kundkonto från administratören.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Klicka på **[!UICONTROL Add New Customer]**.

### Steg 1: Fyll i kontoinformationen

![Kundinformation](assets/new-information.png){width="700" zoomable="yes"}

1. I **[!UICONTROL Account Information]** gör du följande:

   - För installation på flera platser anger du **[!UICONTROL Associate to Website]** på den webbplats där kundkontot gäller.
   - Tilldela kunden till en annan **[!UICONTROL Customer Group]**.
   - Om du använder [moms-ID-validering](../stores-purchase/vat.md) och vill **[!UICONTROL Disable Automatic Group Change Based on VAT ID]** markerar du kryssrutan.

1. Fyll i obligatoriska fält:

   - **[!UICONTROL First Name]**
   - **[!UICONTROL Last Name]**
   - **[!UICONTROL Email]**

1. Fyll i de valfria fälten efter behov:

   - **[!UICONTROL Name Prefix]**
   - **[!UICONTROL Middle Name/Initial]**
   - **[!UICONTROL Name Suffix]**
   - **[!UICONTROL Date of Birth]**
   - **[!UICONTROL Tax/VAT Number]**
   - **[!UICONTROL Gender]**

   >[!WARNING]
   >
   >I enlighet med gällande säkerhets- och integritetspraxis bör du vara medveten om eventuella juridiska risker och säkerhetsrisker som är förknippade med lagring av kundernas fullständiga födelsedatum (månad, dag, år) med andra personliga identifierare. Vi rekommenderar att du begränsar lagringen av kundernas födelsedatum och föreslår att du använder kundens födelseår som ett alternativ.

1. Ange **[!UICONTROL Send Welcome Email From]** till butiksvyn som _Välkommen_ e-post ska skickas.

   >[!INFO]
   >
   > Om butiken har vyer för olika [språk](../stores-purchase/store-localize.md)anger den här inställningen språket för välkomstmeddelandet.

1. Klicka **[!UICONTROL Save and Continue Edit]** överst på sidan.

   >[!INFO]
   >
   >När kundkontot har sparats visas alla alternativ på den vänstra panelen och på menyn överst på sidan. The _[!UICONTROL Customer View]_på -fliken visas en sammanfattning av kontot.

   ![Kundvy](assets/customer-account-create-saved.png){width="600" zoomable="yes"}

### Steg 2: Fyll i adressinformationen

1. Välj **[!UICONTROL Addresses]** och klicka **[!UICONTROL Add New Addresses]**.

1. Om samma adress används för både fakturering och leverans kan du växla mellan alternativen.

   - **[!UICONTROL Default Billing Address]**
   - **[!UICONTROL Default Shipping Address]**

   ![Lägg till kundadressinformation](assets/information-addresses.png){width="600" zoomable="yes"}

1. Bläddra nedåt och fyll i de obligatoriska adressfälten i den andra kolumnen.

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City]**
   - **[!UICONTROL Country]**
   - **[!UICONTROL State/Province]**
   - **[!UICONTROL ZIP/Postal Code]**

1. Ange **[!UICONTROL Phone Number]** för den här adressen.

1. Ange **[!UICONTROL VAT Number]** som är kopplad till kunden.

1. Om den här adressen är den enda som behövs för kontot klickar du på **[!UICONTROL Save]**.

   Annars klickar du på **[!UICONTROL Save and Continue Edit]** och upprepa föregående steg för att lägga till ytterligare adresser.

   Den nya adressen visas i [!UICONTROL Addresses] sida med markerad _[!UICONTROL Default Billing]_och_[!UICONTROL Default Shipping]_ adresser ovanför den fullständiga listan.

   ![Vyn Adresser](assets/address-list.png){width="600" zoomable="yes"}

### Steg 3: Återställ lösenordet

Kundkonton som skapas från administratören har inte tilldelats några lösenord från början.

1. Hitta det nya kundkontot i rutnätet.

1. Klicka **[!UICONTROL Edit]** i _[!UICONTROL Action]_kolumn.

1. Klicka på i menyraden överst på sidan **[!UICONTROL Reset Password]**.

1. Meddelande skickas till kontoägaren med instruktioner om hur lösenordet ska anges.

## Knappfält

Ytterligare knappar blir tillgängliga när profilen sparas för första gången. Mer information finns på [Uppdatera en kundprofil](../customers/update-account.md).

| Knapp | Beskrivning |
|--- |--- |
| **[!UICONTROL Back]** | Återgår till _[!UICONTROL Customers]_utan att spara ändringarna. |
| **[!UICONTROL Delete Customer]** | Tar bort den aktuella kunden. Slutförda order som är kopplade till kunden tas inte bort. |
| **[!UICONTROL Reset]** | Återställer alla osparade ändringar i kundformuläret till deras tidigare värden. |
| **[!UICONTROL Create Order]** | Skapar en order för kunden. |
| **[!UICONTROL Reset Password]** | Skickar en [återställ lösenord](../customers/password-reset.md) länk till kunden via e-post. |
| **[!UICONTROL Force Sign-in]** | Återkallar OAuth-åtkomsttoken som är associerade med kundkontot. Den här funktionen kan bara användas med kundkonton som har tilldelats OAuth-tokens som en del av ett webb-API [integration](../systems/integrations.md). Mer information finns på [OAuth-baserad autentisering](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) i utvecklardokumentationen. |
| **[!UICONTROL Manage Shopping Cart]** | Låter administratören hantera kundvagnen. |
| **[!UICONTROL Save and Continue Edit]** | Sparar ändringar och håller kundprofilen öppen. |
| **[!UICONTROL Save Customer]** | Sparar ändringar och stänger kundprofilen. |

{style="table-layout:auto"}

## Fältbeskrivningar

### [!UICONTROL Account Information]

| Fält | Beskrivning |
|--- |--- |
| **[!UICONTROL Associate to Website]** | Identifierar webbplatsen som är kopplad till kundkontot. |
| **[!UICONTROL Group]** | Anger [kundgrupp](../customers/customer-groups.md) där kunden är medlem. Om tillämpligt markerar du kryssrutan för att inaktivera automatisk gruppändring baserat på moms. |
| **[!UICONTROL Name Prefix]** | Om det används, det prefix som är kopplat till kundens namn (t.ex. Mr., Ms. eller Dr.). Prefixvärdena bestäms av [konfiguration](../configuration-reference/customers/customer-configuration.md). Beroende på konfigurationen kan indatakontrollen vara ett textfält eller en lista med alternativ. |
| **[!UICONTROL First Name]** | Kundens förnamn. |
| **[!UICONTROL Middle Name / Initial]** | Kundens mellannamn eller initialnamn. Det här fältet inkluderas endast om det anges i [konfiguration](../configuration-reference/customers/customer-configuration.md) ämne. |
| **[!UICONTROL Last Name]** | Kundens efternamn. |
| **[!UICONTROL Name Suffix]** | Om det används, det suffix som är associerat med kundens namn (till exempel Jr., Sr. eller III). Suffixvärdena bestäms av [konfiguration](../configuration-reference/customers/customer-configuration.md). Beroende på konfigurationen kan indatakontrollen vara ett textfält eller en listruta med alternativ. |
| **[!UICONTROL Email]** | Kundens e-postadress. |
| **[!UICONTROL Date of Birth]** | Kundens födelsedatum. Födelsedatumet inkluderas om det anges i [konfiguration](../configuration-reference/customers/customer-configuration.md) ämne. <br><br>I enlighet med gällande säkerhets- och integritetspraxis bör du vara medveten om eventuella juridiska risker och säkerhetsrisker som är förknippade med lagring av kundernas fullständiga födelsedatum (månad, dag, år) med andra personliga identifierare. Vi rekommenderar att du begränsar lagringen av kundernas födelsedatum och föreslår att du använder kundens födelseår som ett alternativ. |
| **[!UICONTROL Tax / VAT Number]** | Kundens momsregistreringsnummer eller momsregistreringsnummer, om tillämpligt. |
| **[!UICONTROL Gender]** | Identifierar kundens kön. Kön inkluderas om det anges i [konfiguration](../configuration-reference/customers/customer-configuration.md). Alternativ: `Male` / `Female` / `Not Specified` |
| **[!UICONTROL Send Welcome Email From]** | Om du har flera butiksvyer identifierar den här inställningen den butiksvy som välkomstmeddelandet skickas från. Om butiksvyer används för olika språk avgör den här inställningen språket i välkomstmeddelandet. |

### [!UICONTROL Addresses]

| Fält | Beskrivning |
|--- |--- |
| **[!UICONTROL New Addresses]** | Identifierar typen av ny adress. Alternativ: `Default Billing Address` / `Default Shipping Address` |
| **[!UICONTROL Add New Addresses]** | Visar ett annat nytt adressavsnitt som identifierar vilken typ av adress som ska anges. |
| **[!UICONTROL Company]** | Företagsnamn, om tillämpligt för den här adressen. |
| **[!UICONTROL Street Address]** | Kundens gatuadress. En andra rad på gatuadressen är tillgänglig om den anges i [konfiguration](../configuration-reference/customers/customer-configuration.md) ämne. |
| **[!UICONTROL City]** | Ort där kundadressen finns. |
| **[!UICONTROL Country]** | Det land där kundadressen finns. |
| **[!UICONTROL State/Province]** | Delstaten eller regionen där kundadressen finns. |
| **[!UICONTROL Zip/Postal Code]** | Postnumret där kundadressen finns. |
| **[!UICONTROL Phone Number]** | Kundens telefonnummer som är kopplat till adressen. |
| **[!UICONTROL VAT Number]** | Om tillämpligt, det momsregistreringsnummer som gäller för kunden på den här adressen. |
