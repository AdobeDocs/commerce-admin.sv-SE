---
title: Återbetalningar på kontrollpanelen för kundkonton
description: Butikskunder kan visa den återbetalningsinformation som är kopplad till ordern på sin kontokontrollpanel.
exl-id: 8fd6d4e7-74ba-4f39-9a19-7c77ee63b913
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Återbetalningar på kontrollpanelen för kundkonton

{{ee-feature}}

Om en återbetalning har utfärdats för en beställning kan kunderna visa den återbetalningsinformation som är kopplad till beställningen på sin kontokontrollpanel. Om du har aktiverat alternativet [!UICONTROL _Visa butikskredithistorik för kunder_] för [butikskreditkonfiguration](../customers/credit-configure.md) kan kunderna även komma åt sin [butikskredithistorik](../customers/store-credit.md).

## Visa en återbetalning i butiken

1. Från butiken loggar kunden in på sitt konto.

1. Söker efter deras ordning på något av följande sätt:

   * Söker efter ordningen i listan med **Senaste order** och klickar på **[!UICONTROL View]**.
   * Välj **[!UICONTROL My Orders]** på den vänstra panelen. Leta reda på ordningen i listan och klicka på **[!UICONTROL View]**.

1. Kunden klickar på fliken **[!UICONTROL Refunds]** för att visa information om återbetalningen.

   ![Återbetalningsdetaljer på butiken](assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

## Visa saldo och historik för butikskrediter på butiken

Metod 1: **Från kontrollpanelen för kundkonton**

1. Från butiken loggar kunden in på kontot.

1. Om återbetalningen tillämpades på butikskrediten väljer **[!UICONTROL Store Credit]** i den vänstra panelen.

1. Det belopp som återbetalas till deras butikskrediter visas i listan med datum och tid för åtgärden.

   ![Återbetalt belopp för att lagra kredit](assets/customer-account-store-credit.png){width="700" zoomable="yes"}

   >[!INFO]
   >
   >Butikskreditsidan innehåller också en länk så att kunden kan lösa in ett [presentkort](../stores-purchase/product-gift-card-workflow.md#check-status-and-balance-of-the-gift-card).

Metod 2: **Från sidan _Granska och betala_**

1. Kunden lägger till en produkt i kundvagnen.

2. Fortsätter till sidan _Utcheckning_.

3. Skickar steget **[!UICONTROL Shipping]**.

4. Om butikskrediten är tillgänglig klickar kunden på **[!UICONTROL Use Store Credit]**.

   ![Lagra kredit från sidan Granska och betalningar](assets/customer-account-order-refund-from-checkout.png){width="700" zoomable="yes"}

5. Om kunden ändrar sig när det gäller att använda butikskrediten klickar du på **[!UICONTROL Remove]** i avsnittet _Ordersammanfattning_.

## Betalningsåtgärder i administratören

Du kan konfigurera betalningsåtgärder för din specifika [betalningsmetod](../configuration-reference/sales/payment-methods.md). Varje betalningsmetod har en egen uppsättning betalningsåtgärder.

| Betalningsåtgärd | Beskrivning |
|--- |---|
| [!UICONTROL Capture Online] | När fakturan skickas hämtar systemet betalningen från tredjepartsbetalningsgatewayen. En Admin-användare kan sedan skapa en kreditnota och annullera fakturan. |
| [!UICONTROL Capture Offline] | När fakturan skickas registreras inte betalningen. Det antas att betalningen hämtas direkt via gatewayen och att betalningen inte kan hämtas via Adobe Commerce. En administratör kan sedan skapa en kreditnota, men kan inte annullera fakturan. (Även om ordern innehöll en onlinebetalning är fakturan i princip en offlinefaktura.) |
| [!UICONTROL Not Capture] | När fakturan skickas registreras inte betalningen. Det antas att betalningen görs via Adobe Commerce senare. Det finns en [!UICONTROL _hämtningsknapp_] i den slutförda fakturan. Innan du hämtar fakturan kan du annullera den. När du har hämtat kan du skapa en kreditnota och annullera fakturan. |

{style="table-layout:auto"}

>[!WARNING]
>
>Välj alternativet [!UICONTROL _Inte hämtad_] om du inte är säker på att du kommer att hämta betalningen via Adobe Commerce senare. Du kan inte skapa en kreditnota förrän betalningen har hämtats med knappen [!UICONTROL _Hämta_].
