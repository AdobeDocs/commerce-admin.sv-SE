---
title: Utcheckningsprocess och alternativ
description: Se hur Adobe Commerce och Magento Open Source samlar in den information som behövs för att slutföra transaktionen och sidan Kassa leder kunden genom varje steg i processen.
exl-id: f503643b-a0bb-4763-9831-d592afb2c323
feature: Checkout
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# Utcheckningsprocess och alternativ

När utcheckningsprocessen börjar ändras transaktionen till en säker, krypterad kanal. En hänglåssymbol visas i webbläsarens adressfält och URL:en ändras från `http` till `https`.

## Process

Målet för utcheckningsprocessen är att samla in den information som krävs för att slutföra transaktionen. Sidan _Utcheckning_ leder kunden genom varje steg i processen. Kunder som är inloggade på sina konton kan slutföra utcheckningen snabbt eftersom mycket av informationen redan finns på deras konton. Kunder som är kopplade till ett företagskonto som använder inköpsorder har ett något annorlunda arbetsflöde.

### Leverans

Det första steget i utcheckningsprocessen är att kunden fyller i leveransadressuppgifterna och väljer leveranssätt. Om kunden har ett konto anges leveransadressen automatiskt, men kan ändras vid behov.

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Formatet på gatuadressen för mottagaren och avsändaren bestäms av egenskaperna för [kundadressattributet](../customers/address-attributes.md). Indatavalideringsinställningen avgör vilka tecken som kan användas i en leveransadress.

Förloppsindikatorn överst på sidan följer varje steg i utcheckningsprocessen och beställningssammanfattningen visar att den information som har angetts hittills har angetts.

![Leveranssida under utcheckningsprocessen](./assets/storefront-checkout-step1-shipping.png){width="600" zoomable="yes"}

#### Leverera till en annan adress

1. Om det finns ytterligare poster i adressboken hittar kunden adressen dit ordern ska skickas.

1. Klicka på **[!UICONTROL Ship Here]** om du vill välja adressen.

#### Lägg till en adress

1. Längst ned i avsnittet _[!UICONTROL Shipping Address]_&#x200B;klickar kunden på&#x200B;**[!UICONTROL + New Address]**.

1. Fyller i formuläret _[!UICONTROL Shipping Address]_.

   Som standard visas kundens för- och efternamn först i formuläret.

   ![Leveransadressformuläret innehåller namn- och adressinformation](./assets/storefront-checkout-step1-shipping-add-new-address.png){width="600" zoomable="yes"}

1. Kunden markerar kryssrutan längst ned i formuläret för att spara den nya adressen i adressboken.

1. Klicka på **[!UICONTROL Save Address]**.

   Den nya adressen har nu valts som leveransadress.

   ![Den sparade adressen markeras automatiskt på sidan Leverans](./assets/storefront-checkout-step1-shipping-new-address-selected.png){width="600" zoomable="yes"}

#### Välj leveranssätt

1. I listan över [leveransmetoder](delivery.md) väljer kunden vilket alternativ som ska användas.

   ![Leveranssidan visar alternativ för leveransmetod](./assets/storefront-checkout-step1-shipping-methods.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Next]** för att fortsätta.

### Granskning och betalningar - Regelbunden beställning

Under det andra steget i utcheckningsprocessen väljer kunden [betalningsmetod](payments.md) och tillämpar eventuella kuponger med kampanjkoder på köpet. All information kan granskas och redigeras vid behov. Om det är aktiverat måste kunden godkänna försäljningsvillkoren innan beställningen görs.

>[!NOTE]
>
>Även om Commerce tillåter konfigurering av flera kupongkoder, kan kunden bara använda en kupongkod i kundvagnen. (Mer information finns i [Kupongkoder](../merchandising-promotions/price-rules-cart-coupon.md).)

![Granska och betala under utcheckning](./assets/storefront-checkout-step2-payment-review.png){width="700" zoomable="yes"}

### Granskning och betalningar - inköpsorder

![Adobe Commerce B2B](../assets/b2b.svg) (endast tillgängligt med Adobe Commerce B2B)

När en kund är associerad med ett företag som har aktiverat [inköpsorder](../b2b/purchase-order-flow.md) behandlas alla order som inköpsorder. Tillgängliga betalningsmetoder bestäms av företagskontoinställningarna.

1. Kunden väljer en betalningsmetod.

   När du använder metoden _Betalning på konto_ kan fältet [!UICONTROL Custom Reference Number] användas för att referera till ett fakturanummer.

1. Kunden klickar på **[!UICONTROL Place Purchase Order]**.

   Inköpsordern placeras.

Om företaget har konfigurerat [godkännanderegler](../b2b/account-dashboard-approval-rules.md) går inköpsordern igenom godkännandeprocessen. Annars bearbetas den omedelbart.

![Granskning och betalning av inköpsorder](./assets/checkout-storefront-step2-b2b.png){width="700" zoomable="yes"}

### Antal objekt som visas i ordersammanfattningen

Administratörsanvändare kan ändra det maximala antalet objekt som visas i ordersammanfattningen vid utcheckning för att effektivisera visningen med färre produkter. Som standard är värdet 10.

![Antal objekt som visas i ordersammanfattning](./assets/order-summary.png){width="700" zoomable="yes"}

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Checkout]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Checkout Options]**.

1. Ange det maximala antalet objekt som ska visas för **[!UICONTROL Maximum Number of Items to Display in Order Summary]**.

1. Klicka på **[!UICONTROL Save Config]**.

   Med den här uppdateringen begränsas den ordersammanfattning som visas vid utcheckning till det angivna antalet artiklar.

### Orderbekräftelse

Orderbekräftelsen visas när ordern har placerats ut. För registrerade kunder innehåller sidan ordernumret med en länk till kundens konto och en länk för att generera ett kvitto. Registrerade kunder uppmanas att förvänta sig orderbekräftelse och spårningsinformation via e-post. Gäster uppmuntras att skapa ett konto för att spåra ordern. Registrerade kunder kan generera ett kvitto genom att klicka på en länk.

Sidan med orderbekräftelsen kallas också för sidan _Slutfört_ och används av analysprogram för att spåra konverteringar.

![Sidan Orderbekräftelse visar ett meddelande och ordernummer](./assets/storefront-checkout-confirmation-customer.png){width="700" zoomable="yes"}

## Utcheckningsalternativ

Utcheckningsalternativen styr olika attribut för utcheckningssidan, inklusive layouten. Det finns alternativ som du kan konfigurera för att placera begränsningar i utcheckningen, inklusive att tillåta gästutcheckning och verkställa ett villkorsavtal. Det finns även alternativ för att styra visningen av information under utcheckningsprocessen.

![Konfiguration - utcheckningsalternativ](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

En detaljerad beskrivning av de här konfigurationsinställningarna finns i [Utcheckningsalternativ](../configuration-reference/sales/checkout.md#checkout-options) i _referenshandboken för konfiguration_.

### Ändra alternativ för utcheckning

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.
1. Expandera **[!UICONTROL Sales]** på den vänstra panelen och välj **[!UICONTROL Checkout]**.
1. Ange något av följande alternativ som du behöver.
1. Klicka på **[!UICONTROL Save Config]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Checkout Options]**.

1. Om inställningarna gäller för en viss butiksvy [väljer du den butiksvy](../configuration-reference/scope-change.md#set-the-scope) där konfigurationen gäller.

   Klicka på **[!UICONTROL OK]** när du uppmanas att fortsätta.

1. Ange utcheckningsalternativen.

1. Klicka på **[!UICONTROL Save Config]**.

### Tillgängliga alternativ för utcheckning

| Fält | [Omfång](../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Onepage Checkout] | Butiksvy | Avgör om [ensidig utcheckning](checkout-one-page.md) är standardutcheckningsformatet. Alternativ: Ja/Nej |
| [!UICONTROL Allow Guest Checkout] | Butiksvy | Avgör om gäster kan gå igenom [utcheckningen utan att registrera](checkout-guest.md) för ett konto hos din butik. Alternativ: `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | Butiksvy | Avgör om kunderna måste godkänna [villkoren](terms-and-conditions.md) för försäljningen innan de gör ett köp. Alternativ: `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | Butiksvy | Bestämmer platsen för faktureringsadressen under utcheckningen. Alternativ: `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | Butiksvy | Anger det maximala antalet objekt som kan visas i ordersammanfattningen under utcheckningen. Standardvärdet är `10`. |
| [!UICONTROL Enable Address Search] | Webbplats | ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Avgör om kunder kan använda [adresssökning](checkout-address-search.md)-funktionalitet för _Leverans_ och _Granska och betala_-stegen. När den här funktionen är aktiverad använder du _[!UICONTROL Number of Customer Addresses Limit]_&#x200B;för att ange antalet sparade adresser som krävs för att aktivera den här funktionen vid utcheckning. Alternativ: `Yes` / `No` |
| [!UICONTROL Number of Customer Addresses Limit] | Webbplats | ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) När adresssökningen är **[!UICONTROL Enabled]** avgör hur många sparade adresser som krävs för att aktivera den här funktionen under utcheckningen. När kundens antal sparade adresser uppfyller eller överstiger det här antalet återges endast standardadressen i stegen _Leverans_ och _Granska och betala_. Kunden kan använda en sökfunktion för att ändra den valda adressen. Standardvärdet är 10. |

{style="table-layout:auto"}
