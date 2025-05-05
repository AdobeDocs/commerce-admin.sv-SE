---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Checkout]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Sales] &gt; [!UICONTROL Checkout] i Commerce Admin.
exl-id: a912beb0-37a9-407b-83bd-dc6cd0554dc4
feature: Configuration, Checkout
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Checkout]

{{config}}

## [!UICONTROL Checkout Options]

![Utcheckningsalternativ](./assets/checkout-checkout-options.png)<!-- zoom -->

<!--[Checkout Options](https://experienceleague.adobe.com/sv/docs/commerce-admin/stores-sales/point-of-purchase/checkout/checkout-process#checkout-options) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|------------------------------------------------------------------|--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Guest Checkout Login] | Butiksvy | Aktivera den här inställningen för att tillåta oautentiserade användare (storefront och API:er) att fråga om en e-postadress redan är kopplad till ett kundkonto. Detta kan användas för att förbättra arbetsflödet för utcheckning av gäster genom att visa en inloggningsfråga om den angivna e-postadressen redan är registrerad på ett kundkonto, men medför att information exponeras för oautentiserade användare.  Alternativ: `Yes` / `No` |
| [!UICONTROL Enable Onepage Checkout] | Butiksvy | Avgör om [Utcheckning på en sida](../../stores-purchase/checkout-process.md#checkout-options) är standardutcheckningsformatet. Alternativ: `Yes` / `No` |
| [!UICONTROL Allow Guest Checkout] | Butiksvy | Avgör om gäster kan gå igenom [utcheckningen utan att registrera](../../stores-purchase/checkout-guest.md) för ett konto hos din butik. Alternativ: `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | Butiksvy | Avgör om kunderna måste godkänna [villkoren](../../stores-purchase/terms-and-conditions.md) för försäljningen innan de gör ett köp. Alternativ: `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | Butiksvy | Bestämmer platsen för faktureringsadressen under utcheckningen. Alternativ: `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | Butiksvy | Avgör det maximala antalet objekt som kan visas i _ordersammanfattningen_ vid utcheckning. Standardvärdet är `10`. |
| [!UICONTROL Enable Address Search] | Webbplats | ![Adobe Commerce](../../assets/adobe-logo.svg) (endast Adobe Commerce) Avgör om kunder kan använda [adresssökning](../../stores-purchase/checkout-address-search.md) för leverans och granska och betala-steg. När detta är aktiverat använder du alternativet Antal kundadresser (Limit) för att ange antalet sparade adresser som krävs för att aktivera den här funktionen vid utcheckning. Alternativ: `Yes` / `No` |
| Gräns för antal kundadresser | Webbplats | ![Adobe Commerce](../../assets/adobe-logo.svg) (endast Adobe Commerce) När adresssökning är aktiverat avgör hur många sparade adresser som krävs för att aktivera den här funktionen vid utcheckning. När kundens antal sparade adresser uppfyller eller överstiger det här antalet återges endast standardadressen i stegen _Leverans_ och _Granska och betala_. Kunden kan använda en sökfunktion för att ändra den valda adressen. Standardvärdet är `10`. |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart]

![Kundvagn](./assets/checkout-shopping-cart.png)<!-- zoom -->

<!--[Shopping Cart](https://experienceleague.adobe.com/sv/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Quote Lifetime (days)] | Webbplats | Bestämmer [livstiden för ett citerat pris](../../stores-purchase/cart-configuration.md#quote-lifetime), i dagar. |
| [!UICONTROL After Adding a Product Redirect to Shopping Cart] | Butiksvy | Avgör om kundvagnssidan [visas](../../stores-purchase/cart-configuration.md#redirect-to-cart) omedelbart efter att en produkt har lagts till i kundvagnen. Alternativ: `Yes` / `No` |
| [!UICONTROL Number of Items to Display Pager] | Butiksvy | Fastställer antalet artiklar i kundvagnen innan personsökaren aktiveras. Standardvärde: `20` |
| [!UICONTROL Show Cross-sell Items in the Shopping Cart] | Butiksvy | Anger om [korsförsäljningsartiklar](../../catalog/related-products-up-sells-cross-sells.md#cross-sells) visas i kundvagnen, vilket ger kunderna ytterligare försäljningsalternativ. Alternativ: `Yes` (standard) / `No` |
| [!UICONTROL Grouped Product Image] | Butiksvy | Bestämmer den [miniatyrbild](../../stores-purchase/cart-configuration.md#cart-thumbnails) som visas för en [grupperad produkt](../../catalog/product-create-grouped.md) i kundvagnen. Alternativ: `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Configurable Product Image] | Butiksvy | Bestämmer den [miniatyrbild](../../stores-purchase/cart-configuration.md#cart-thumbnails) som visas för en konfigurerbar produkt i kundvagnen. Alternativ: `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Preview Quote Lifetime (minutes)] | Butiksvy | Bestämmer den maximala åldern för offerten i minuter när den förhandsgranskas från kundvagnen. |
| [!UICONTROL Enable Clear Shopping Cart] | Webbplats | Avgör om kundvagnen visar alternativet för användare att rensa innehållet i vagnen i en enda åtgärd. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL My Cart Link]

![Min kundvagnslänk](./assets/checkout-my-cart-link.png)<!-- zoom -->

<!-- [*My Cart Link*](https://experienceleague.adobe.com/sv/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#mini-cart) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Display Cart Summary] | Webbplats | Anger vilket värde som visas inom parentes efter länken Min kundvagn. Alternativ: `Display number of items in cart` / `Display item quantities` |

{style="table-layout:auto"}

## Mini Cart

![Mini Cart](./assets/checkout-mini-cart.png)<!-- zoom -->

<!-- [*Mini Cart*](https://experienceleague.adobe.com/sv/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#mini-cart) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Display Mini Cart] | Butiksvy | Avgör om mini-vagnen visas på butikssidorna när användaren klickar på varukorsikonen i sidhuvudet. Visningen av minivagnen beror på temat. Alternativ: `Yes` / `No` |
| [!UICONTROL Number of Items to Display Scrollbar] | Butiksvy | Anger antalet objekt som kan visas i minivagnen innan rullningslisten aktiveras. Standard: `5` |
| [!UICONTROL Maximum Number of Items to Display] | Butiksvy | Anger det maximala antalet artiklar som kan visas i minivagnen. Standard: `10` |

{style="table-layout:auto"}

## [!UICONTROL Payment Failed Emails]

![Betalningen misslyckades med e-post](./assets/checkout-payment-failed-emails.png)<!-- zoom -->

<!-- [*Payment Failed Emails*](https://experienceleague.adobe.com/sv/docs/commerce-admin/stores-sales/point-of-purchase/checkout/checkout-payment-failed-emails) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Payment Failed Email Receiver] | Butiksvy | Identifierar den butikskontakt som tar emot e-postmeddelanden om misslyckade betalningar. Standardmottagare: `General Contact` |
| [!UICONTROL Payment Failed Email Sender] | Butiksvy | Identifierar den butikskontakt som visas som meddelandeavsändare av e-postmeddelanden om misslyckade betalningar. Standardavsändare: `General Contact` |
| [!UICONTROL Payment Failed Template] | Butiksvy | Identifierar mallen som används för att skicka misslyckade e-postmeddelanden. Standardmall: `Payment Failed` |
| [!UICONTROL Send Payment Failed Copy To] | Butiksvy | Anger e-postadressen till alla som ska få en kopia av ett e-postmeddelande om misslyckade betalningar. Avgränsa flera adresser med komma. |
| [!UICONTROL Send Payment Failed Copy Method] | Butiksvy | Anger den e-postmetod som används för att skicka kopian. Alternativ: <br />**`Bcc`**- Skickar en hemlig kopia genom att inkludera mottagaren i rubriken för samma e-postmeddelande som skickas till kunden. Mottagaren av hemlig kopia är inte synlig för kunden.<br />**`Separate Email`** - Skickar kopian som ett separat e-postmeddelande. |

{style="table-layout:auto"}
