---
title: Omedelbart köp
description: Läs om Direktköp och hur det kan ge en snabb utcheckning av registrerade kundkonton.
exl-id: f299f364-d7e3-4567-8c7b-955129011a19
feature: Checkout
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# Omedelbart köp

Med _Direktköp_ kan kunderna gå igenom kassan snabbare med hjälp av information som sparas i deras konto. När det här alternativet är aktiverat visas knappen _Direktköp_ nedanför knappen _Lägg till i kundvagnen_ på produktsidan för kunder som uppfyller kraven.

![Produktsida med alternativet Direktköp visas](./assets/storefront-checkout-instant-purchase.png){width="700" zoomable="yes"}

## Kundkrav

- Kunden är [inloggad](../customers/customer-sign-in.md) på sitt konto.

- Kundkontot har en [standardadress för fakturering och leverans](../customers/account-dashboard-address-book.md).

- Minst en [leveransmetod](delivery.md) är tillgänglig för landet som anges i standardleveransadressen.

- Kundkontot har en [lagrad betalningsmetod](../stores-purchase/stored-payment-methods.md) med valv aktiverat.

  Följande betalningsmetoder kan användas för att ge säker åtkomst till sparad kreditkortsinformation:

   - [Braintree-kreditkort](braintree.md) (Direktköp kan inte användas med Braintree-kreditkort om 3D-säkerhet är aktiverat.)
   - [Braintree med PayPal aktiverat](braintree.md)
   - [PayPal Payflow Pro](paypal-payflow-pro.md)

## Direktköp i butiken

1. I butiken går kunden till produktsidan för artikeln som ska köpas.

1. Markerar de nödvändiga alternativen och klickar på **[!UICONTROL Instant Purchase]**.

   ![Bekräftelsedialogrutan för att bekräfta direktköpet](./assets/storefront-checkout-instant-purchase-confirmation.png){width="500" zoomable="yes"}

1. Granska **[!UICONTROL Instant Purchase Confirmation]**-informationen och klicka på **[!UICONTROL OK]** för att slutföra transaktionen.

   Ett bekräftelsemeddelande och ordernummer visas högst upp på produktsidan.

## Konfigurera direktköp

### Steg 1: Öppna konfigurationssidan

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

### Steg 2: Konfigurera betalningsmetodvalvet

Du kan använda Direktköp med Braintree eller Betalningstjänster för Adobe Commerce och Magento Open Source. Vaulting måste vara aktiverat innan en kund kan använda funktionen Direktköp.

Lär dig hur du konfigurerar betalningsmetoden och aktiverar säkringar för Braintree eller betaltjänster:

- [Braintree](braintree.md)
- [Betalningstjänster - dokumentation](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html)

### Steg 3: Aktivera direktköp

1. Välj **[!UICONTROL Sales]** i den vänstra panelen under avsnittet _[!UICONTROL Sales]_.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Instant Purchase]**.

1. Om den här ändringen gäller för en viss butiksvy [väljer du den butiksvy](../configuration-reference/scope-change.md#set-the-scope) där konfigurationen gäller.

   Klicka på **[!UICONTROL OK]** när du uppmanas att fortsätta.

1. Ange **[!UICONTROL Enabled]** till `Yes`.

1. Ange **[!UICONTROL Button Text]** som du vill ska visas på knappen.

   Knapptexten kan ändras för varje butiksvy eller språk. Knapptexten är som standard `Instant Purchase`.

   ![Konfiguration - Alternativ för direktköp](../configuration-reference/sales/assets/sales-instant-purchase.png){width="600" zoomable="yes"}

   En detaljerad beskrivning av de här konfigurationsinställningarna finns i [Direktköp](../configuration-reference/sales/sales.md#instant-purchase) i _referenshandboken för konfiguration_.

1. Klicka på **[!UICONTROL Save Config]**.

1. När du uppmanas att uppdatera cachen klickar du på **[!UICONTROL Cache Management]** i systemmeddelandet och följer instruktionerna för att tömma cachen.
