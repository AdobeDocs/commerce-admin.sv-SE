---
title: Checklista för återstart
description: Använd den här listan för att kontrollera de nödvändiga konfigurationsinställningarna för att se till att allt är korrekt innan din butik går till produktion.
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Checklista för återstart

När du är klar med design, utveckling och testning av din butik kontrollerar du följande konfigurationsinställningar för att se till att allt är korrekt före butiken _går live_. En omfattande beskrivning av alla konfigurationsinställningar finns i [_Konfigurationsreferens_](../configuration-reference/guide-overview.md).

## Allmänna inställningar

- [Lagra URL:er](../stores-purchase/store-urls.md) - Verifiera att butiks-URL:erna för storefront och Admin är korrekta för en aktiv produktionsmiljö.
- Säkerhetscertifikat - Installera ett 100 % signerat och pålitligt säkerhetscertifikat för den domän som anges i bas-URL:en innan du startar arkivet.
- [E-postadresser för butik](../getting-started/store-details.md#store-email-addresses) - Fyll i alla e-postadresser som används för att skicka och ta emot e-postmeddelanden, t.ex. nya order, fakturor, leveranser, kreditnotor, produktprismeddelanden och nyhetsbrev. Se till att varje fält innehåller en giltig e-postadress för företag.

## Marknadsinställningar

- [E-postmallar](../systems/email-templates.md) - Uppdatera standardmallarna för e-post så att de speglar ert varumärke. Uppdatera konfigurationen om du skapar mallar.
- [Säljkommunikation](../stores-purchase/introduction.md#order-management-and-operations) - Se till att dina fakturor och följesedlar innehåller rätt affärsinformation och att de återspeglar ditt varumärke.
- [Google Tools](../merchandising-promotions/google-tools.md) - [!DNL Commerce] har integrering med Google API så att ert företag kan använda Google Analytics och Google AdWords.

## Försäljningsinställningar

- [Alternativ för kundvagn](../stores-purchase/cart-configuration.md) - Titta på inställningarna för kundvagnen för att se om det finns något som du vill ändra, till exempel att ange minimiorderbelopp och prislivstid i kundvagnen.
- [Utcheckningsalternativ](../stores-purchase/checkout-process.md#checkout-options) - Titta på alternativen för utcheckning för att se om det finns något som du vill ändra, som att ställa in villkor och konfigurera gästutcheckning.
- [Skatter](../stores-purchase/taxes.md) - Se till att skatterna är korrekt konfigurerade enligt dina affärsskatteregler och lokala krav.
- [Leveransmetoder](../stores-purchase/delivery.md) - Gör det möjligt för företaget att använda alla transportföretag och leveransmetoder.
- [PayPal](../stores-purchase/paypal.md) - Om du tänker erbjuda dina kunder möjlighet att betala med PayPal öppnar du ett PayPal Merchant-konto och anger en betalningsmetod. Kör vissa testtransaktioner i sandlådeläge innan butiken publiceras.
- [Betalningsmetoder](../stores-purchase/payments.md) - Aktivera de betalningsmetoder som du tänker använda och kontrollera att de är korrekt konfigurerade. Kontrollera orderstatusinställningarna, accepterad valuta, tillåtna länder och så vidare.

## Systeminställningar

[Kron (schemalagda aktiviteter)](../systems/cron.md) - Kronjobb används för att bearbeta e-post, katalogprisregler, nyhetsbrev, kundvarningar, Google webbplatskartor, uppdatera valutakurser osv. Kontrollera att Cron-jobb är inställda på att köras med rätt tidsintervall i minuter.
