---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront] i Commerce Admin.
exl-id: 6c03ee68-7421-4c74-bdc1-0855f088b7f9
feature: Configuration, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1283'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront]

>[!IMPORTANT]
>
>Innan du kan konfigurera Google reCAPTCHA måste du se till att filen `PHP.ini` innehåller följande inställning: `allow_url_fopen = 1`. Detta kan kräva hjälp av utvecklare. Se [PHP-inställningar](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) i _installationshandboken_.

{{config}}

Mer information om hur du använder Google reCAPTCHA för att skydda din butik finns i Google [reCAPTCHA](../../systems/security-google-recaptcha.md) i _Admin Systems Guide_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 (&quot;Jag är inte en robot&quot;)](./assets/recaptcha-storefront-v2-not-robot.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--|--|--|
| [!UICONTROL Google API Website Key] | Webbplats | Den webbplatsnyckel som skapas när du registrerar ditt Google reCAPTCHA-konto. |
| [!UICONTROL Google API Secret Key] | Webbplats | Den hemliga nyckel som är kopplad till ditt Google reCAPTCHA-konto. |
| [!UICONTROL Size] | Webbplats | Storleken på rutan Google reCAPTCHA som visas när en kund loggar in på sitt konto. Alternativ: `Normal` (standard) / `Compact` |
| [!UICONTROL Theme] | Webbplats | Anger formatet för rutan Google reCAPTCHA. Alternativ: `Light Theme` (standard) / `Dark Theme` |
| [!UICONTROL Language Code] | Butiksvy | Koden [med två tecken](https://developers.google.com/recaptcha/docs/language) som anger vilket språk som används för Google reCAPTCHA-text och -meddelanden. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 Osynlig](./assets/recaptcha-storefront-v2-invisible.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--|--|--|
| [!UICONTROL Google API Website Key] | Webbplats | Den webbplatsnyckel som skapas när du registrerar ditt Google reCAPTCHA-konto. |
| [!UICONTROL Google API Secret Key] | Webbplats | Den hemliga nyckel som är kopplad till ditt Google reCAPTCHA-konto. |
| [!UICONTROL Invisible Badge Position] | Webbplats | Positionen för det osynliga reCAPTCHA-märket på varje sida. Alternativ: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Global | Anger formatet för rutan Google reCAPTCHA. Alternativ: `Light Theme` (standard) / `Dark Theme` |
| [!UICONTROL Language Code] | Butiksvy | En [kod med två tecken](https://developers.google.com/recaptcha/docs/language) som anger vilket språk som används för Google reCAPTCHA-text och -meddelanden. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 osynlig](./assets/recaptcha-storefront-v3-invisible.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--|--|--|
| [!UICONTROL Google API Website Key] | Webbplats | Den webbplatsnyckel som skapas när du registrerar ditt Google reCAPTCHA-konto. |
| [!UICONTROL Google API Secret Key] | Webbplats | Den hemliga nyckel som är kopplad till ditt Google reCAPTCHA-konto. |
| [!UICONTROL Minimum Score Threshold] | Global | Det lägsta poängvärde som identifierar en användarinteraktion som en potentiell risk, där 1.0 är en typisk användarinteraktion och 0.0 är troligtvis en robot. Standard: `0.5` |
| [!UICONTROL Invisible Badge Position] | Webbplats | Positionen för det osynliga reCAPTCHA-märket på varje sida. Alternativ: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Webbplats | Anger formatet för rutan Google reCAPTCHA. Alternativ: `Light Theme` (standard) / `Dark Theme` |
| [!UICONTROL Language Code] | Butiksvy | En [kod med två tecken](https://developers.google.com/recaptcha/docs/language) som anger vilket språk som används för Google reCAPTCHA-text och -meddelanden. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![Felmeddelanden](./assets/recaptcha-storefront-failure-messages.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | Butiksvy | Meddelandet som visas i butiken om verifieringen misslyckas. Standardtext: `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | Butiksvy | Meddelandet som visas i butiken om reCAPTCHA inte returnerar ett verifieringsresultat. Standardtext: `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![Storefront](./assets/recaptcha-storefront.png)<!-- zoom -->

>[!NOTE]
>
>Typen reCAPTCHA som du väljer måste matcha den typ som är associerad med API-nyckeln från ditt Google reCAPTCHA-konto.

>[!WARNING]
>
>När du använder reCAPTCHA version 3 kan en äkta användare med låg poäng inte fortsätta. För version 2 får en äkta användare med låg poäng en utmaning. Tänk efter noga om äkta användare med låg poäng ska kunna lösa ett problem (version 2) eller blockeras (version 3).

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--|--|--|
| [!UICONTROL Enable for Customer Login] | Webbplats | Anger den typ av reCAPTCHA som används när kunder [loggar in](../../customers/customer-sign-in.md) på sina konton. Alternativ:<br/>**`No`**- (standard) Verifierar inte inloggningsbegäran.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Kräver att användaren markerar kryssrutan _Jag är inte en robot_.<br />**`Invisible reCAPTCHA v2`**- Validerar användarbeteende i bakgrunden utan att det krävs interaktioner baserat på poäng.<br/>**`Invisible reCAPTCHA v3`** - (Rekommenderas) Validerar användarbeteende i bakgrunden baserat på interaktionspoäng. |
| [!UICONTROL Enable for Forgot Password] | Webbplats | Anger den typ av reCAPTCHA som används när kunderna begär en [lösenordsåterställning](../../customers/password-reset.md). Alternativ:<br/>**`No`**- (standard) Verifierar inte begäran om återställning av lösenord.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Kräver att användaren markerar kryssrutan _Jag är inte en robot_.<br />**`Invisible reCAPTCHA v2`**- Validerar användarbeteende i bakgrunden utan att det krävs interaktioner baserat på poäng.<br/>**`Invisible reCAPTCHA v3`** - (Rekommenderas) Validerar användarbeteende i bakgrunden baserat på interaktionspoäng. |
| [!UICONTROL Enable for Create New Customer Account] | Webbplats | Anger den typ av reCAPTCHA som används när kunden registrerar sig för ett [nytt konto](../../customers/account-create.md). Alternativ:<br/>**`No`**- (standard) Verifierar inte kontobegäran.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Kräver att användaren markerar kryssrutan _Jag är inte en robot_.<br />**`Invisible reCAPTCHA v2`**- Validerar användarbeteende i bakgrunden utan att det krävs interaktioner baserat på poäng.<br/>**`Invisible reCAPTCHA v3`** - (Rekommenderas) Validerar användarbeteende i bakgrunden baserat på interaktionspoäng. |
| [!UICONTROL Enable for Edit Customer Account] | Webbplats | Anger den typ av reCAPTCHA som används när kunden ändrar sin [kontoinformation](../../customers/account-dashboard-account-information.md). Alternativ:<br/>**`No`**- (standard) Verifierar inte kontobegäran.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Kräver att användaren markerar kryssrutan _Jag är inte en robot_.<br />**`Invisible reCAPTCHA v2`**- Validerar användarbeteende i bakgrunden utan att det krävs interaktioner baserat på poäng.<br/>**`Invisible reCAPTCHA v3`** - (Rekommenderas) Validerar användarbeteende i bakgrunden baserat på interaktionspoäng. |
| [!UICONTROL Enable for Create New Company Account] | Webbplats | ![Adobe Commerce B2B](../../assets/b2b.svg) (endast tillgängligt med Adobe Commerce B2B) Anger den typ av reCAPTCHA som används när ett nytt [företagskonto](../../b2b/account-company-create.md) skapas. Alternativ:<br/>**`No`**- (standard) Verifierar inte kontobegäran.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Kräver att användaren markerar kryssrutan _Jag är inte en robot_.<br />**`Invisible reCAPTCHA v2`**- Validerar användarbeteende i bakgrunden utan att det krävs interaktioner baserat på poäng.<br/>**`Invisible reCAPTCHA v3`** - (Rekommenderas) Validerar användarbeteende i bakgrunden baserat på interaktionspoäng. |
| [!UICONTROL Enable for Contact Us] | Webbplats | Anger den typ av reCAPTCHA som används för att skicka ett meddelande från sidan [Kontakta oss](../../getting-started/store-details.md#contact-us-form) i din butik. Alternativ:<br/>**`No`**- (standard) Verifierar inte meddelandebegäran.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Kräver att användaren markerar kryssrutan _Jag är inte en robot_.<br />**`Invisible reCAPTCHA v2`**- Validerar användarbeteende i bakgrunden utan att det krävs interaktioner baserat på poäng.<br/>**`Invisible reCAPTCHA v3`** - (Rekommenderas) Validerar användarbeteende i bakgrunden baserat på interaktionspoäng. |
| [!UICONTROL Enable for Product Review] | Webbplats | Anger den typ av reCAPTCHA som används när kunder skickar en [produktgranskning](../../merchandising-promotions/product-reviews.md). Alternativ:<br/>**`No`**- (standard) Verifierar inte produktgranskningsbegäran.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Kräver att användaren markerar kryssrutan _Jag är inte en robot_.<br />**`Invisible reCAPTCHA v2`**- Validerar användarbeteende i bakgrunden utan att det krävs interaktioner baserat på poäng.<br/>**`Invisible reCAPTCHA v3`** - (Rekommenderas) Validerar användarbeteende i bakgrunden baserat på interaktionspoäng. |
| [!UICONTROL Enable for Newsletter Subscription] | Webbplats | Anger den typ av osynlig reCAPTCHA som används när kunder registrerar sig för en [nyhetsbrevsprenumeration](../../merchandising-promotions/newsletter-subscribers.md). Alternativ:<br/>**`No`**- (standard) Validerar inte prenumerationsbegäran för nyhetsbrev.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Kräver att användaren markerar kryssrutan _Jag är inte en robot_.<br />**`Invisible reCAPTCHA v2`**- Validerar användarbeteende i bakgrunden utan att det krävs interaktioner baserat på poäng.<br/>**`Invisible reCAPTCHA v3`** - (Rekommenderas) Validerar användarbeteende i bakgrunden baserat på interaktionspoäng. |
| [!UICONTROL Enable for Gift Card] | Webbplats | ![Adobe Commerce](../../assets/adobe-logo.svg) (endast Adobe Commerce) Anger den typ av reCAPTCHA som används när kunder anger en [presentkortskod](../../catalog/product-gift-card-create.md). Alternativ:<br/>**`No`**- (standard) Validerar inte presentkortets kodskickning.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Kräver att användaren markerar kryssrutan _Jag är inte en robot_.<br />**`Invisible reCAPTCHA v2`**- Validerar användarbeteende i bakgrunden utan att det krävs interaktioner baserat på poäng.<br/>**`Invisible reCAPTCHA v3`** - (Rekommenderas) Validerar användarbeteende i bakgrunden baserat på interaktionspoäng. |
| [!UICONTROL Enable for Invitation Create Account] | Webbplats | Anger den typ av reCAPTCHA som används när kunder skickar en [inbjudan](../../merchandising-promotions/invitations.md)-kod för att skapa ett konto. Alternativ:<br/>**`No`**- (standard) Verifierar inte e-postinlämningen av inbjudan.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Kräver att användaren markerar kryssrutan _Jag är inte en robot_.<br />**`Invisible reCAPTCHA v2`**- Validerar användarbeteende i bakgrunden utan att det krävs interaktioner baserat på poäng.<br/>**`Invisible reCAPTCHA v3`** - (Rekommenderas) Validerar användarbeteende i bakgrunden baserat på interaktionspoäng. |
| [!UICONTROL Enable for Send to Friend] | Webbplats | Anger den typ av reCAPTCHA som används när kunder [delar en produkt](../../stores-purchase/email-a-friend.md) med en vän. Alternativ:<br/>**`No`**- (standard) Verifierar inte e-postinlämningen.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Kräver att användaren markerar kryssrutan _Jag är inte en robot_.<br />**`Invisible reCAPTCHA v2`**- Validerar användarbeteende i bakgrunden utan att det krävs interaktioner baserat på poäng.<br/>**`Invisible reCAPTCHA v3`** - (Rekommenderas) Validerar användarbeteende i bakgrunden baserat på interaktionspoäng. |
| [!UICONTROL Enable for Wishlist Sharing] | Webbplats | Anger den typ av reCAPTCHA som används när kunder [delar en önskelista](../../stores-purchase/wishlist-storefront.md#share-the-wish-list). Alternativ:<br/>**`No`**- (standard) Validerar inte meddelandet och e-postöverföringen.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Kräver att användaren markerar kryssrutan _Jag är inte en robot_.<br />**`Invisible reCAPTCHA v2`**- Validerar användarbeteende i bakgrunden utan att det krävs interaktioner baserat på poäng.<br/>**`Invisible reCAPTCHA v3`** - (Rekommenderas) Validerar användarbeteende i bakgrunden baserat på interaktionspoäng. |
| [!UICONTROL Enable for Coupon Codes] | Webbplats | Anger den typ av reCAPTCHA som används när kunderna anger en [kupongkod](../../merchandising-promotions/price-rules-cart-coupon.md). Alternativ:<br/>**`No`**- (standard) Verifierar inte inskickandet av kupongkoden.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Kräver att användaren markerar kryssrutan _Jag är inte en robot_.<br />**`Invisible reCAPTCHA v2`**- Validerar användarbeteende i bakgrunden utan att det krävs interaktioner baserat på poäng.<br/>**`Invisible reCAPTCHA v3`** - (Rekommenderas) Validerar användarbeteende i bakgrunden baserat på interaktionspoäng. |
| [!UICONTROL Enable for PayPal Payflow Pro payment form] | Webbplats | Anger den typ av reCAPTCHA som används när kunder betalar för ett köp med [PayPal Payflow Pro](../../stores-purchase/paypal-payflow-pro.md). Alternativ:<br/>**`No`**- (standard) Verifierar inte begäran om återställning av lösenord.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Kräver att användaren markerar kryssrutan _Jag är inte en robot_.<br />**`Invisible reCAPTCHA v2`**- Validerar användarbeteende i bakgrunden utan att det krävs interaktioner baserat på poäng.<br/>**`Invisible reCAPTCHA v3`** - (Rekommenderas) Validerar användarbeteende i bakgrunden baserat på interaktionspoäng. |

{style="table-layout:auto"}
