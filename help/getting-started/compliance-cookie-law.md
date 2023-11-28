---
title: Cookie-lagefterlevnad
description: För att hålla jämna steg med lagstiftningen i många länder om användningen av cookies erbjuder Adobe Commerce och Magento Open Source handlare ett urval av metoder för att få kundens samtycke.
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: ae43d97bb3031a06ce6a0211ee304aae53e4eb08
workflow-type: tm+mt
source-wordcount: '2145'
ht-degree: 0%

---

# Cookie-lagefterlevnad

Cookies är små filer som sparas på datorn för varje besökare på platsen och används som tillfälliga förvaringsplatser för information. Information som sparas i cookies används för att anpassa shoppingupplevelsen, länka besökare till deras kundvagnar, mäta trafikmönster och förbättra kampanjernas effektivitet. För att hålla jämna steg med lagstiftningen i många länder om användningen av cookies erbjuder Adobe Commerce och Magento Open Source handlare ett urval av metoder för att få kundens samtycke. En lista över standardcookies i Adobe Commerce och Magento Open Source finns på [Cookie-referens](#default-cookies).

>[!NOTE]
>
>Om du ändrar standardinställningen [Google sekretessinställningar](../merchandising-promotions/google-tools.md#google-privacy-settings) att följa [Allmän dataskyddsförordning](compliance-gdpr.md), det är inte nödvändigt att få användarens samtycke för användning av cookies från Google Analytics.

## Metod 1: Underförstått samtycke

Underförstådda samtycke innebär att besökare i din butik har en tydlig förståelse för att cookies är en nödvändig del av verksamheten, och genom att använda din webbplats har de indirekt beviljat tillstånd att använda dem. Nyckeln till att få underförstått samtycke är att tillhandahålla tillräckligt med information för att en besökare ska kunna fatta ett välgrundat beslut. I många butiker visas ett meddelande högst upp på alla standardsidor med en kort översikt över hur cookies används, med en länk till butikens integritetspolicy. Integritetspolicyn bör beskriva vilken typ av information som lagras och hur den används.

## Metod 2: Uttryckligt samtycke

Använd butiken i _begränsat läge för cookie_ kräver att besökarna ger sitt samtycke innan cookies kan sparas på deras datorer. Om du inte ger ditt medgivande finns många funktioner i din butik inte tillgängliga. Om Google Analytics till exempel är tillgängligt för din butik kan det bara anropas efter att besökaren har gett behörighet att använda cookies.

## Begränsningsläge för cookie

När läget för begränsning av cookies är aktiverat meddelas besökare på din butik om att cookies krävs för åtgärder med alla funktioner. Beroende på temat kan meddelandet visas ovanför sidhuvudet, under sidfoten eller någon annanstans på sidan. Meddelandet länkar till din integritetspolicy för mer information och uppmuntrar besökare att klicka på Tillåt för att ge sitt samtycke. När samtycke har beviljats försvinner meddelandet.

Dina [integritetspolicy](privacy-policy.md)) ska innehålla namnet på din butik och kontaktinformation samt förklara syftet med varje cookie som används av din butik. Mer information finns på [Cookie-referens](#default-cookies).

>[!NOTE]
>
>Om du ändrar URL-nyckeln för sekretesspolicyn måste du även skapa en anpassad URL-omskrivning för att dirigera om trafik till den nya URL-nyckeln. I annat fall returneras länken i meddelandet Kakform i begränsningsläge `404 Page Not Found`.

![Exempel på storefront - meddelande om cookie-begränsning](./assets/storefront-cookie-restriction-message.png){width="600"}

### Steg 1: Aktivera läget för begränsning av cookies

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I den vänstra navigeringspanelen under **[!UICONTROL General]**, välja **[!UICONTROL Web]**.

1. Expandera **[!UICONTROL Default Cookie Settings]** och gör följande:

   ![Webbkonfiguration - standardinställningar för cookie](./assets/web-default-cookie-settings.png){width="600"}

   - Ange **[!UICONTROL Cookie Lifetime]** på några sekunder.

   - Om du vill göra cookies tillgängliga för andra mappar anger du **[!UICONTROL Cookie Path]**. Om du vill göra cookies tillgängliga var som helst på webbplatsen anger du ett snedstreck (`/`). Detta värde får endast innehålla cookie-sökvägen, och **_inte_** innehåller andra cookie-parametrar.

   - Om du vill göra cookies tillgängliga för en underdomän anger du underdomännamnet i **[!UICONTROL Cookie Domain]** fält (`subdomain.yourdomain.com`). Om du vill göra cookies tillgängliga för alla underdomäner anger du domännamnet som föregås av en punkt (`.yourdomain.com`). Det här värdet får endast innehålla cookie-domänen, och **_inte_** innehåller andra cookie-parametrar.

   - Om du vill förhindra att skriptspråk, som JavaScript, får åtkomst till cookies, ska du se till att **Använd endast HTTP** är inställd på `Yes`.

   - Ange **[!UICONTROL Cookie Restriction Mode]** till `Yes`.

     Om det behövs avmarkerar du kryssrutan och klickar **[!UICONTROL OK]** för att bekräfta omfångsbyte.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

1. När du uppmanas att uppdatera cachen klickar du på **[!UICONTROL Cache Management]** i systemmeddelandet. Uppdatera sedan varje ogiltig cache.

### Steg 2: Uppdatera din sekretesspolicy

Uppdatera dina [integritetspolicy](privacy-policy.md) så att den återspeglar den information som företaget samlar in och hur den används.

## Standardcookies

Standardcookies i Adobe Commerce och Magento Open Source klassificeras som Undanta/Icke-undantagna för att hjälpa handlare att uppfylla kraven på sekretesslagstiftning, som [GDPR](compliance-gdpr.md). Handläggarna bör använda denna information som vägledning och rådfråga juridiska rådgivare för att uppdatera deras integritets- och cookie-policy som en del av en övergripande strategi för efterlevnad av integritetsregler.

Följande cookies används av [!DNL Commerce] &quot;ut ur kartongen&quot; för installationer på plats och i molnet. Dessa cookies kan krävas av funktioner som uttryckligen begärs av kunden. Om du vill veta mer om hur länge sessionscookies är aktiva kan du läsa [Sessionslivstid](../customers/customer-online-options.md).

Vissa av dessa cookies kan innehålla konfigurationsalternativ, inklusive aktivera/inaktivera, efter behov.

### Begärda funktionskakor (undantagna)


#### `add_to_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Används av Google Tag Manager. Hämtar SKU, namn, pris och kvantitet för produkten som tagits bort från kundvagnen och gör informationen tillgänglig för framtida integrering med skript från tredje part.

#### `guest-view`

Lagrar det beställnings-ID som gästkunder använder för att hämta sin orderstatus. Vyn Gästorder. Används i _[!DNL Orders and Returns]_widgetar.

- Är säker? Nej
- Endast HTTP: Ja
- Förfalloprincip: session
- Modul: `Magento_Sales`

#### `login_redirect`

Bevarar målsidan som lästes in innan kunden omdirigerades till inloggning. En omdirigering av inloggning används med mini-vagnen för inloggade kunder om [Visa minikort](../stores-purchase/cart-configuration.md#mini-cart) konfigurationsalternativet är inställt på `Yes`.

- Är säker? Nej
- Endast HTTP: Nej
- Förfalloprincip: session
- Modul: `Magento_Customer`

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Lagrar banderollinnehåll lokalt för att förbättra prestandan.

#### `mage-messages`

Spårar felmeddelanden och andra meddelanden som visas för användaren, t.ex. meddelandet om godkännande av cookie och olika felmeddelanden. Meddelandet tas bort från cookien när det har visats för shopparen.

Det finns inget alternativ för att inaktivera denna cookie.

- Är säker? Nej
- Endast HTTP: Nej
- Förfalloprincip: Varaktighet 1 år. Rensas vid frontend när meddelandet visas för användaren.
- Modul: `Magento_Theme`

#### `mage-translation-storage` (lokal lagring)

Lagrar översatt innehåll när kunden begär det. Används när [Översättningsstrategi](../configuration-reference/advanced/developer.md) är konfigurerad som &quot;Lexikon (översättning på Storefront side)&quot;.

- Är säker? Nej
- Endast HTTP: Nej
- Förfalloprincip: Per lokal lagringsregel
- Modul: `Magento_Translation`

#### `mage-translation-file-version` (lokal lagring)

Spårar versionen av översättningar i lokal lagring. Används när [Översättningsstrategi](../configuration-reference/advanced/developer.md) är konfigurerad som `Dictionary (Translation on Storefront side)`.

- Är säker? Nej
- Endast HTTP: Nej
- Förfalloprincip: Per lokal lagringsregel
- Modul: `Magento_Translation`

#### `product_data_storage` (lokal lagring)

Lagrar konfiguration för produktdata som är relaterade till nyligen visade/jämförda produkter.

- Är säker? Nej
- Endast HTTP: Nej
- Förfalloprincip: Per lokal lagringsregel
- Modul: `Magento_Catalog`

#### `recently_compared_product` (lokal lagring)

Lagrar produkt-ID för nyligen jämförda produkter.

- Är säker? Nej
- Endast HTTP: Nej
- Förfalloprincip: Per lokal lagringsregel
- Modul: `Magento_Catalog`

#### `recently_compared_product_previous` (lokal lagring)

Lagrar produkt-ID:n för tidigare jämförda produkter för enkel navigering.

- Är säker? Nej
- Endast HTTP: Nej
- Förfalloprincip: Per lokal lagringsregel
- Modul: `Magento_Catalog`

#### `recently_viewed_product` (lokal lagring)

Lagrar produkt-ID:n för nyligen visade produkter för enkel navigering.

- Är säker? Nej
- Endast HTTP: Nej
- Förfalloprincip: Per lokal lagringsregel
- Modul: `Magento_Catalog`

#### `recently_viewed_product_previous` (lokal lagring)

Lagrar produkt-ID:n för nyligen visade produkter för enkel navigering.

- Är säker? Nej
- Endast HTTP: Nej
- Förfalloprincip: Per lokal lagringsregel
- Modul: `Magento_Catalog`

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Används av [Google Tag Manager](../merchandising-promotions/google-tag-manager.md). Hämtar SKU, namn, pris och kvantitet för produkten som läggs till i kundvagnen och gör informationen tillgänglig för framtida integrering av skript från tredje part.

#### `stf`

Registrerar när meddelanden skickas av SendFriend ([Skicka e-post till en vän](../stores-purchase/email-a-friend.md)).

- Är säker? Ja
- Endast HTTP: Ja
- Förfalloprincip: session
- Modul: `Magento_SendFriend`

#### `X-Magento-Vary`

Konfigurationsinställning som förbättrar prestanda när statisk innehållscachning i engelska används.

- Är säker? Ja
- Endast HTTP: Ja
- Förfalloprincip: Baserad på PHP-inställningssession.cookie_life
- Modul: `Magento_PageCache`

#### `form_key`

En säkerhetsåtgärd som lägger till en slumpmässig sträng i alla formuläröverföringar för att skydda data från CSRF (Cross-Site Request Forgery).

- Är säker? Nej
- Endast HTTP: Nej
- Förfalloprincip:
   - PHP: Baserat på PHP-inställningssession.cookie_life
   - JS: Session
- Modul: Sidcache

#### `mage-cache-sessid`

Värdet för denna cookie utlöser rensning av lokal cachelagring. När cookien tas bort av serverdelsprogrammet rensar administratören upp det lokala lagringsutrymmet och ställer in cookie-värdet på `true`.

- Är säker? Nej
- Endast HTTP: Nej
- Förfalloprincip: session
- Modul: `Magento_Customer`

#### `mage-cache-storage`

Lokal lagring av besökarspecifikt innehåll som möjliggör e-handelsfunktioner.

- Är säker? Nej
- Endast HTTP: Nej
- Förfalloprincip: session
- Modul: `Magento_Customer`, `Magento_Persistent`

#### `mage-cache-storage` (lokal lagring)

Lokal lagring av besökarspecifikt innehåll som möjliggör e-handelsfunktioner.

- Är säker? Nej
- Endast HTTP: Nej
- Förfalloprincip: session
- Modul: `Magento_Customer`, `Magento_Persistent`, `Magento_NegotiableQuote`

#### `mage-cache-storage-section-invalidation` (lokal lagring)

Tvingar lokal lagring av specifika innehållsavsnitt som ska ogiltigförklaras.

- Är säker? Nej
- Endast HTTP: Nej
- Förfalloprincip: Per lokal lagring
- Modul: `Magento_Customer`

#### `persistent_shopping_cart`

Lagrar nyckeln (ID) för en beständig kundvagn så att du kan återställa kundvagnen för en anonym kund.

- Är säker? Ja
- Endast HTTP: Ja
- Förfalloprincip: Baserad på [Beständig kundvagn](../stores-purchase/cart-persistent.md) - Konfiguration av beständighetens livstid (sekunder)
- Modul: `Magento_Persistent`

#### `private_content_version`

Lägger till ett slumpmässigt unikt nummer och en unik tid på sidor med kundinnehåll för att förhindra att de cachas på servern.

Den ställs in på flera platser: i PHP, i JavaScript som en cookie och i JavaScript till lokal lagring.

Endast för HTTP=`Yes` (baserat på begäran) betyder det att cookien är säker om den anges under HTTPS-begäran och osäker om den anges under HTTP-begäran.

- Är säker? `Yes` (på begäran), `No`
- Endast HTTP: `No`
- Förfalloprincip: Baserad på [Beständig kundvagn](../stores-purchase/cart-persistent.md) - Konfiguration av beständighetens livstid (sekunder)
   - PHP: `1` år / `315360000s` (tio år)
   - JS: `1` dag
   - Lokal lagringsplats för JS: Lagringsregler per lokal lagringsplats (för alltid)
- Modul: `Magento_PageCache`, `Magento_Customer`

#### `section_data_ids`

Lagrar kundspecifik information om kundinitierade åtgärder, som visning av önskelistor och utcheckningsinformation.

- Är säker? `No`
- Endast HTTP: `No`
- Förfalloprincip: `Session`
- Modul: `Magento_Customer`

#### `store`

Spårar butiksvyn/språkområdet som valts av kunden.

- Är säker? `No`
- Endast HTTP: `Yes`
- Förfalloprincip: `1` år
- Modul: `Magento_Store`

#### `mage-banners-cache-storage` - lokal lagring

![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Lokal lagring för banderollfunktioner.

- Är säker? `No`
- Endast HTTP: `No`
- Förfalloprincip: Per lokal lagringsregel
- Modul: `Magento_Banner`

## Google Analytics cookies

Följande cookies används när [Google Analytics](../merchandising-promotions/google-analytics.md) eller Google Universal Analytics är helt aktiverat för din installation. Information om hur du inaktiverar dessa cookies för efterlevnad av sekretesslagstiftningen finns i [Sekretessinställningar för Google](../merchandising-promotions/google-tools.md#google-privacy-settings). Mer information finns på [Google Analytics Cookie-användning på webbplatser][1].

### Google Universal Analytics-cookies - icke-undantagna

![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) JavaScript-bibliotek: `gtag.js` och `analytics.js`

- `_ga`: Skiljer besökare till din webbplats.
- `_gid`: Skiljer besökare till din webbplats.
- `gat`: Används för att begränsa begärandehastigheten.
- `dc_gtm_<property-id>`: Begränsar begärandahastighet när Google Analytics distribueras med [Google Tag Manager](../merchandising-promotions/google-tag-manager.md).
- `AMP_TOKEN`: Innehåller en token som kan användas för att hämta ett klient-ID från tjänsten för AMP-klient-ID. Andra möjliga värden är avanmälan, informationsbegäran eller ett fel vid hämtning av ett klient-ID från tjänsten AMP Client ID.
- `_gac_<property-id>`: Innehåller kampanjrelaterad information för användaren. Google AdWords-konverteringstaggar läser denna cookie om Google Analytics är länkad till din [AdWords][2] konto.

### Google Analytics cookies - icke-undantagna

![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) JavaScript-bibliotek: `ga.js`

- `__utma`: Skiljer shoppare och sessioner. Denna cookie skapas när JavaScript-biblioteket körs och det inte finns någon befintlig `__utma` cookie. Cookien uppdateras varje gång data skickas till Google Analytics.
- `__utmt`: Används för att begränsa begärandehastigheten.
- `__utmb`: Bestämmer nya sessioner/besök. Denna cookie skapas när JavaScript-biblioteket körs och det inte finns någon befintlig `__utmb` cookie. Cookien uppdateras varje gång data skickas till Google Analytics.
- `_utmz`: Sparar trafikkällan eller kampanjen som förklarar hur kunden nådde er webbplats. Cookien skapas när JavaScript-biblioteket körs och uppdateras varje gång data skickas till Google Analytics.
- `__utmv`: Lagrar anpassade variabeldata på besökarnivå. Denna cookie skapas när en utvecklare använder `_setCustomVar` med en anpassad variabel på besökarnivå. Denna cookie uppdateras varje gång data skickas till Google Analytics.

## Recommendations cookies

![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Följande cookies används av Recommendations för Adobe Commerce-kunder. Dessa cookies installeras med [DataServices-modul](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg_dnt`: Gör att du kan [begränsa Adobe Commerce datainsamling](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/developer/setting-cookie.html) om du har anpassad kod för att hantera cookie-samtycke på din webbplats.
- `user_allowed_save_cookie`: Används för [begränsat läge för cookie](#cookie-restriction-mode).
- `authentication_flag`: Anger om en kund har loggat in eller ut. Denna cookie uppdateras samtidigt som `dataservices_customer_id` cookie.
- `dataservices_customer_id`: Anger om en kund har loggat in eller ut. Denna cookie innehåller kundens unika ID i systemet.
- `dataservices_customer_group`: Anger en kunds grupp. Den här cookien lagras som [sha1](https://en.wikipedia.org/wiki/SHA-1) kontrollsumma för kundens grupp-ID.
- `dataservices_cart_id`: Identifierar kundens kundvagnsaktiviteter. Denna cookie innehåller kundens unika kundvagn-ID i systemet.
- `dataservices_product_context`: Identifierar en kunds produktinteraktioner. Denna cookie innehåller kundens unika offert-ID i systemet.

## Ytterligare cookies

![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Följande cookies är angivna för Adobe Commerce-kunder. Dessa cookies installeras med [DataServices-modul](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg`: Anges av Snowplow JavaScript-spåraren. Mer information finns i [Snowplow-dokumentation](https://docs.snowplow.io/docs/collecting-data/collecting-from-own-applications/javascript-trackers/javascript-tracker/javascript-tracker-v3/tracker-setup/initialization-options).
- `com.adobe.alloy.getTld`: Med tanke på den aktuella webbsidans värdnamn är detta den översta domänen som inte är ett&quot;offentligt suffix&quot; enligt https://publicsuffix.org. Detta är i princip den översta domänen som kan ta emot cookies. Den här kakan ingår i [Alloy Web SDK](https://github.com/adobe/alloy).

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
