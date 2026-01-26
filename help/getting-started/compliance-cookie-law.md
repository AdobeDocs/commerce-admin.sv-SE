---
title: Cookie-lagefterlevnad
description: För att hålla jämna steg med lagstiftningen i många länder om användningen av cookies erbjuder Adobe Commerce och Magento Open Source säljare ett urval av metoder för att få kundens samtycke.
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '2150'
ht-degree: 0%

---

# Cookie-lagefterlevnad

Cookies är små filer som sparas på datorn för varje besökare på platsen och används som tillfälliga förvaringsplatser för information. Information som sparas i cookies används för att anpassa shoppingupplevelsen, länka besökare till deras kundvagnar, mäta trafikmönster och förbättra kampanjernas effektivitet. För att hålla jämna steg med lagstiftningen i många länder om användningen av cookies erbjuder Adobe Commerce och Magento Open Source säljare ett urval av metoder för att få kundens samtycke. [Cookie Reference](#default-cookies) innehåller en lista med standardcookies i Adobe Commerce och Magento Open Source.

>[!NOTE]
>
>Om du ändrar standardsekretessinställningarna för [Google](../merchandising-promotions/google-tools.md#google-privacy-settings) så att de överensstämmer med [allmänna dataskyddsförordningen](compliance-gdpr.md) behöver du inte få användarens samtycke för användning av Google Analytics cookies.

## Begränsningsläge för cookie

När läget för begränsning av cookies är aktiverat meddelas besökare på din butik om att cookies krävs för åtgärder med alla funktioner. Beroende på temat kan meddelandet visas ovanför sidhuvudet, under sidfoten eller någon annanstans på sidan. Meddelandet länkar till din integritetspolicy för mer information och uppmuntrar besökare att klicka på Tillåt för att ge sitt samtycke. När samtycke har beviljats försvinner meddelandet.

Din [sekretesspolicy](privacy-policy.md)) ska innehålla namnet på din butik och kontaktinformation och förklara syftet med varje cookie som används av din butik. Mer information finns i [Cookie-referens](#default-cookies).

>[!NOTE]
>
>Om du ändrar URL-nyckeln för sekretesspolicyn måste du även skapa en anpassad URL-omskrivning för att dirigera om trafik till den nya URL-nyckeln. I annat fall returnerar länken i meddelandet Kakform i begränsningsläge `404 Page Not Found`.

![Exempel på butiksskylt - meddelande om begränsning av cookies](./assets/storefront-cookie-restriction-message.png){width="600"}

### Steg 1: Aktivera läget för begränsning av cookies

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_&#x200B;Admin **[!UICONTROL Configuration]**.

1. Välj **[!UICONTROL General]** i den vänstra navigeringspanelen under **[!UICONTROL Web]**.

1. Expandera avsnittet **[!UICONTROL Default Cookie Settings]** och gör följande:

   ![Webbkonfiguration - standardinställningar för cookie](./assets/web-default-cookie-settings.png){width="600"}

   - Ange **[!UICONTROL Cookie Lifetime]** i sekunder.

   - Om du vill göra cookies tillgängliga för andra mappar anger du **[!UICONTROL Cookie Path]**. Om du vill göra cookies tillgängliga var som helst på webbplatsen anger du ett snedstreck (`/`). Det här värdet kan bara innehålla cookie-sökvägen och **_får inte_** innehålla några andra cookie-parametrar.

   - Om du vill göra cookies tillgängliga för en underdomän anger du underdomännamnet i fältet **[!UICONTROL Cookie Domain]** (`subdomain.yourdomain.com`). Om du vill göra cookies tillgängliga för alla underdomäner anger du domännamnet som föregås av en punkt (`.yourdomain.com`). Det här värdet kan bara innehålla cookie-domänen och **_får inte_** innehålla några andra cookie-parametrar.

   - Om du vill förhindra att skriptspråk, som JavaScript, får åtkomst till cookies, kontrollerar du att **Använd endast HTTP** är inställt på `Yes`.

   - Ange **[!UICONTROL Cookie Restriction Mode]** till `Yes`.

     Om det behövs avmarkerar du kryssrutan och klickar på **[!UICONTROL OK]** för att bekräfta omfångsväxling.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

1. När du uppmanas att uppdatera cachen klickar du på länken **[!UICONTROL Cache Management]** i systemmeddelandet och uppdaterar varje ogiltig cache.

### Steg 2: Uppdatera din sekretesspolicy

Uppdatera din [sekretesspolicy](privacy-policy.md) så att den speglar den information som ditt företag samlar in och hur den används.

## Standardcookies

Standardcookies i Adobe Commerce och Magento Open Source klassificeras som Undanta/Ej undantagna för att hjälpa handlare att uppfylla kraven i sekretessbestämmelser som [GDPR](compliance-gdpr.md). Handläggarna bör använda denna information som vägledning och rådfråga juridiska rådgivare för att uppdatera deras integritets- och cookie-policy som en del av en övergripande strategi för efterlevnad av integritetsregler.

Följande cookies används av [!DNL Commerce] &quot;out of the box&quot; för lokala installationer och molninstallationer. Dessa cookies kan krävas av funktioner som uttryckligen begärs av kunden. Mer information om hur länge sessionscookies är giltiga finns i [Sessionens livstid](../customers/customer-online-options.md).

Vissa av dessa cookies kan innehålla konfigurationsalternativ, inklusive aktivera/inaktivera, efter behov.

### Begärda funktionskakor (undantagna)

#### `add_to_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Hämtar produkt-SKU, namn, pris och kvantitet som tagits bort från kundvagnen. Låter Google Analytics veta när en produkt har lagts till i en kundvagn.

#### `guest-view`

Länkar en gästorder till en gäst (eftersom det inte finns något konto för gästen). Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `login_redirect`

Sparar omdirigerings-URL för att dirigera användare om inloggning och användarregistrering lyckades. Sparar sidan som en användare var på innan han/hon loggade in (för att fastställa platsen dit han/hon kommer att gå tillbaka efter att han/hon loggat in).

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Lokal lagring för banderollfunktioner. Lagrar banderollinnehåll lokalt för att förbättra prestandan. Banderollinnehållet innehåller allmänna webbplatsresurser som visar information för en kund. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `mage-messages`

Spårar felmeddelanden och andra meddelanden som visas för användaren, t.ex. meddelandet om godkännande av cookie och olika felmeddelanden. Meddelandet tas bort från cookien när det har visats för shopparen. Det finns inget alternativ för att inaktivera denna cookie. Så här kommunicerar användaren med engångsinformation, t.ex. felmeddelanden. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `product_data_storage` (lokal lagring)

Lagrar konfiguration för produktdata som används för att använda funktionerna&quot;Senast visade&quot; och&quot;Jämför produkter&quot;. Lagrar en användares specifika inställningar (t.ex. om de nyligen har visat en produkt eller jämfört produkter). Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `recently_compared_product` (lokal lagring)

Lagrar produkt-ID för nyligen jämförda produkter. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `recently_compared_product_previous` (lokal lagring)

Lagrar produkt-ID:n för tidigare jämförda produkter för enkel navigering. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `recently_viewed_product` (lokal lagring)

Lagrar produkt-ID:n för nyligen visade produkter för enkel navigering. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `recently_viewed_product_previous` (lokal lagring)

Lagrar produkt-ID:n för nyligen visade produkter för enkel navigering. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Gör att Google Analytics vet när en produkt har tagits bort från en kundvagn.

#### `stf`

Registrerar de tidsmeddelanden som skickas av modulen SendFriend ([Skicka e-post till en vän](../stores-purchase/email-a-friend.md)). När en kund skickar en länk till en produkt registreras en tidsstämpel i den här cookien och en räkning upprätthålls.

#### `X-Magento-Vary`

Anger när en ny version av en sida måste hanteras från cachen. Stöd för webbplatsprestanda. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `form_key`

En säkerhetsmekanism som innehåller ett slumpmässigt genererat värde för att förhindra CSRF-attacker (Cross Site Request Forgery) genom att hjälpa till att avgöra om en begäran kommer från en äkta källa eller en dålig skådespelare. Det här är en branschstandard för att förhindra CSRF-attacker. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `mage-cache-sessid`

Detta är användbart när du ska avgöra när lokal lagring ska rensas i webbläsaren när sessionen har upphört. Detta används för att fastställa om lokal lagring måste rengöras. Frånvaro av denna cookie utlöser lokal lagringsrensning. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `mage-cache-storage`

Lokal lagring av besökarspecifikt innehåll som möjliggör e-handelsfunktioner. Används inte som standard, men när den används används den för att snabba upp utcheckningen så att grundläggande användarinformation är tillgänglig när någon lämnar och returnerar. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `mage-cache-storage-section-invalidation`

Lagrar information om vilka avsnitt på sidan som behöver göras ogiltiga och tas bort. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `persistent_shopping_cart`

Lagrar nyckel-ID:t för en beständig kundvagn så att det går att återställa kundvagnen för en anonym kund. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `private_content_version`

Lägger till ett slumpmässigt unikt nummer och en unik tid på sidor med kundinnehåll för att förhindra att de cachas på servern. Den finns på flera ställen: i PHP, i JavaScript som en cookie och i JavaScript som lokal lagring. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `section_data_ids`

Lagrar kundspecifik information om kundinitierade åtgärder, som visning av önskelistor och utcheckningsinformation. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `store`

Spårar den specifika butiksvy/det språk som valts av kunden. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `PHPSESSID`

Spåra användarsessioner i butiken. Det här är de kunder som använder slutprodukterna. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `admin`

Spåra användarsessioner på adminsidan. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `loggedOutReasonCode`

Ange när en Admin-användare låses efter ett visst antal misslyckade lösenordsförsök.

#### `section_data_clean`

Ange när en användare växlar butiksvy. Den här cookie-filen aktiverar JavaScript för att läsa in vissa avsnitt på sidan på nytt för att återspegla rätt butiksvy. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `lang`

Ange indirekt av Admin Analytics-modulen. Används endast i en butiks administrativa område. Gäller inte för kunder. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `s_fid`

Ange indirekt av Admin Analytics-modulen. Reservstämpel för unikt besökar-ID för tid/datum. Den används för att identifiera en unik besökare om standardcookien `s_vi` inte är tillgänglig på grund av cookie-begränsningar från tredje part. Används endast i en butiks administrativa område. Gäller inte för kunder. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `s_cc`

Ange indirekt av Admin Analytics-modulen. Den ställs in och läses av JavaScript-koden för att avgöra om cookies är aktiverade. Används endast i en butiks administrativa område. Gäller inte för kunder. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `apt.sid`

Anges av Gainsight PX-biblioteket som används indirekt av Admin Analytics-modulen. Syftet med den här cookien är att tillåta beständig spårning av sessions-ID i produktens toppnivådomän och används som referens-ID till den aktiva sessionen. Används endast i en butiks administrativa område. Gäller inte för kunder. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `apt.uid`

Anges av Gainsight PX-biblioteket som används indirekt av Admin Analytics-modulen. Syftet med denna cookie är att tillåta beständig ID-spårning under produktens toppnivådomän och används som referens-ID till användarentiteten. Används endast i en butiks administrativa område. Gäller inte för kunder. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `s_sq`

Ange indirekt av Admin Analytics-modulen. Används av ClickMap-funktionen som samlar in data om var besökarna klickar och vad de klickar på. Lagrar information från varje klick. Används endast i en butiks administrativa område. Gäller inte för kunder. Inaktivera inte denna cookie för att behålla systemstabiliteten.

#### `pagebuilder_modal_dismissed`

Anges av Page Builder-modulen. Innehåller en flagga som förhindrar efterföljande uppmaningar att be en administratör bekräfta en viss åtgärd från att öppnas om administratören uttryckligen har stängt dem tidigare. Används endast i en butiks administrativa område. Gäller inte för kunder.

#### `pagebuilder_template_apply_confirm`

Anges av Page Builder-modulen. Innehåller en flagga som förhindrar efterföljande uppmaningar att be en administratör bekräfta en viss åtgärd från att öppnas om administratören uttryckligen har stängt dem tidigare. Används endast i en butiks administrativa område. Gäller inte för kunder.

#### `accordion-&lbrace;VARIABLE&rbrace;-&lbrace;VARIABLE&rbrace;`

Används som en del av flikfunktionsimplementeringen endast i ett administrativt område i en butik. Gäller inte för kunder.

## Produktrekommendationer - cookies

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Följande cookies används av produktrekommendationer för Adobe Commerce-kunder. Dessa cookies installeras med [DataServices-modulen](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/getting-started/install-configure).

- `mg_dnt`: Gör att du kan [begränsa Adobe Commerce datainsamling](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/developer/setting-cookie) om du har anpassad kod för att hantera cookie-samtycke på din webbplats.
- `user_allowed_save_cookie`: Används för [begränsningsläge för cookies](#cookie-restriction-mode).
- `authentication_flag`: Anger om en kund har loggat in eller ut. Den här cookien uppdateras samtidigt som cookien `dataservices_customer_id`.
- `dataservices_customer_id`: Anger om en kund har loggat in eller ut. Denna cookie innehåller kundens unika ID i systemet.
- `dataservices_customer_group`: Anger en kunds grupp. Denna cookie lagras som [sha1](https://en.wikipedia.org/wiki/SHA-1)-kontrollsumma för kundens grupp-ID.
- `dataservices_cart_id`: Identifierar kundens kundvagnsaktiviteter. Denna cookie innehåller kundens unika kundvagn-ID i systemet.
- `dataservices_product_context`: Identifierar en kunds produktinteraktioner. Denna cookie innehåller kundens unika offert-ID i systemet.

### Produktrekommendationer, lokala lagringsdata

Följande data sparas i lokal lagring för butiker med Luma-temat när Live Search eller Produktrekommendationer är installerade:

- `ds-cart`: Sparar kundvagnsinformation för Luma-specifika funktioner
- `ds-cart-order`: Lagrar orderinformation för kundvagnsfunktioner
- `ds-purchase-history`: Spåra kundens inköpshistorik
- `ds-view-history-time-decay`: Lagrar produktvyhistorik med tidsbaserad minskning
- `ds-logged-in`: Anger kundens inloggningsstatus. Dessa data finns endast när kunden är inloggad och lagras även när läget för cookie-begränsning är aktiverat. Det här är de enda data som Commerce lagrar i lokal lagring när läget för begränsning av cookies är aktiverat, oavsett användarens medgivandestatus.

## Ytterligare cookies

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Följande cookies har angetts för Adobe Commerce-kunder. Dessa cookies installeras med [DataServices-modulen](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/getting-started/install-configure).

- `mg`: Anges av Snowplow JavaScript-spåraren. Mer information finns i [Snowplow-dokumentationen](https://docs.snowplow.io/docs/sources/trackers/javascript-trackers/web-tracker/tracker-setup/initialization-options/).
- `com.adobe.alloy.getTld`: Med tanke på den aktuella webbsidans värdnamn är detta den översta domänen som inte är ett &quot;offentligt suffix&quot; enligt https://publicsuffix.org. Detta är i princip den översta domänen som kan ta emot cookies. Den här cookien är en del av [Alloy Web SDK](https://github.com/adobe/alloy).
- `aep-segments-membership`: Innehåller [målgruppsinformation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation), t.ex. vilket segment en kund tillhör.
