---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL Payment Services]'
description: Granska konfigurationsinställningarna i [!UICONTROL Payment Services] i [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] sidan för Commerce Admin.
exl-id: 255b7bd8-1d32-4393-9eba-43dc7754c752
feature: Configuration, Payments
source-git-commit: bf166c1debd7f10a4d988d231a1a47f32c4cea9e
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Payment Services]



Betalningstjänster erbjuder en nyckelfärdig självbetjäningslösning, inklusive sandlådetestning och en enkel konfiguration, för att tillhandahålla robust och säker betalningshantering. Mer information finns i [_Användarhandbok för betaltjänster_](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

Om du vill komma åt konfigurationsinställningarna för Betalningstjänster går du till _Administratör_ sidebar går till **[!UICONTROL Sales]** > **[!UICONTROL Payment Services]** och klicka **[!UICONTROL Settings]**.

![Betalningstjänster](assets/payment-services-menu-small.png){width="400"}

>[!NOTE]
>
>Använda den äldre konfigurationen i stället för [Inställningar](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/configure/settings.html), se [Äldre konfiguration](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/configure/configure-admin.html).

## [!UICONTROL General]

![Allmänna inställningar](assets/payments-general-settings.png){width="600" zoomable="yes"}

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|---|---|---|
| [!UICONTROL Enable] | webbplats | Aktivera eller inaktivera [!DNL Payment Services] för er webbplats. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Payment mode] | butiksvy | Ange metod, eller miljö, för din butik. Alternativ: [!UICONTROL Sandbox] / [!UICONTROL Production] |
| [!UICONTROL Sandbox Merchant ID] | butiksvy | Ditt handlar-ID för sandlådan, som genereras automatiskt vid introduktion av sandlådor. |
| [!UICONTROL Production Merchant ID] | butiksvy | Ditt handlar-ID för produktion, som genereras automatiskt när sandlådan introduceras. |
| [!UICONTROL Soft Descriptor] | webbplats eller butiksvy | Lägg till en mjuk beskrivning till webbplatserna och butiksvyer som ger information om kundtransaktioner och avgränsar varumärken, butiker eller produktlinjer. The [!UICONTROL Use website] växlingsknappen använder alla mjuka beskrivningar som har lagts till på webbplatsnivå. The [!UICONTROL Use default] växlingsknappen använder alla mjuka beskrivningar som har lagts till som standard. |

{style="table-layout:auto"}

## [!UICONTROL Credit card fields]

![Inställningar för kreditkortsfält](assets/payments-ccfields-settings.png){width="600" zoomable="yes"}

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|---|---|---|
| [!UICONTROL Title] | butiksvy | Lägg till texten som ska visas som rubrik för det här betalningsalternativet i vyn Betalningsmetod vid utcheckning. |
| [!UICONTROL Payment Action] | webbplats | The [betalningsåtgärd](payment-methods.md#payment-actions) för den angivna betalningsmetoden. Alternativ: [!UICONTROL Authorize] / [!UICONTROL Authorize and Capture] |
| [!UICONTROL 3DS Secure authentication] | webbplats | Aktivera eller inaktivera [Säker 3DS-autentisering](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/security-compliance/security.html#3ds). Alternativ: [!UICONTROL Always] / [!UICONTROL When Required] / [!UICONTROL Off] |
| [!UICONTROL Show on checkout page] | webbplats | Aktivera eller inaktivera kreditkortsfält som ska visas på utcheckningssidan. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Vault enabled] | butiksvy | Aktivera eller inaktivera [kreditkortsvalv](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/payments-checkout/vaulting.html). Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show vaulted payment methods in Admin] | butiksvy | Aktivera eller inaktivera möjligheten att slutföra beställningar för kunder i administratören [med en betalningsmetod som är skyddad](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/payments-checkout/vaulting.html). Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Debug Mode] | webbplats | Aktivera eller inaktivera felsökningsläget. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |

{style="table-layout:auto"}

## [!UICONTROL Payment buttons]

![Inställningar för betalningsknappar](assets/payments-ppbuttons-settings.png){width="600" zoomable="yes"}

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|---|---|---|
| [!UICONTROL Title] | butiksvy | Lägg till texten som ska visas som rubrik för det här betalningsalternativet i vyn Betalningsmetod vid utcheckning. |
| [!UICONTROL Payment Action] | webbplats | The [betalningsåtgärd](payment-methods.md#payment-actions){target="_blank"} för den angivna betalningsmetoden. Alternativ: [!UICONTROL Authorize] / [!UICONTROL Authorize and Capture] |
| [!UICONTROL Show PayPal buttons on checkout page] | butiksvy | Aktivera eller inaktivera [!DNL PayPal Smart Buttons] på utcheckningssidan. Alternativ: [!UICONTROL  Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons on product detail page] | butiksvy | Aktivera eller inaktivera [!DNL PayPal Smart Buttons] på produktinformationssidan. Alternativ: [!UICONTROL  Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons in mini-cart preview] | butiksvy | Aktivera eller inaktivera [!DNL PayPal Smart Buttons] i minikundvagnen. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons on cart page] | butiksvy | Aktivera eller inaktivera [!DNL PayPal Smart Buttons] på kundvagnssidan. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Pay Later button] | butiksvy | Aktivera eller inaktivera utseendet på betalningsalternativ vid ett senare tillfälle där betalningsknappar visas. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Pay Later Message] | webbplats | Aktivera eller inaktivera meddelandet Betala senare i kundvagnen, på produktsidan, i minikundvagnen och under kassaflödet. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show Venmo button] | butiksvy | Aktivera eller inaktivera betalalternativet Venmo där betalningsknappar visas. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show Apple Pay button] | butiksvy | Aktivera eller inaktivera betalningsalternativet Apple Pay där betalningsknappar visas. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Credit and Debit card button] | butiksvy | Aktivera eller inaktivera alternativet för kredit- och betalkortsbetalning där betalningsknappar visas. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Debug Mode] | webbplats | Aktivera eller inaktivera felsökningsläget. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |

{style="table-layout:auto"}

## [!UICONTROL PayPal Smart Button Styling]

![Ställningsinställningar för PayPal-betalningsknappar](assets/payments-buttonstyle-settings.png){width="600" zoomable="yes"}

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Layout] | Butiksvy | Definiera layoutformat för betalningsknappar. Alternativ: [!UICONTROL Vertical] / [!UICONTROL Horizontal] |
| [!UICONTROL Tagline] | Butiksvy | Aktivera/inaktivera tagline. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Color] | Butiksvy | Definiera färg på betalningsknapparna. Alternativ: [!UICONTROL Blue] / [!UICONTROL Gold] / [!UICONTROL Silver] / [!UICONTROL White] / [!UICONTROL Black] |
| [!UICONTROL Shape] | Butiksvy | Definiera formen på betalningsknapparna. Alternativ: [!UICONTROL Rectangular] / [!UICONTROL Pill] |
| [!UICONTROL Responsive Button Height] | Butiksvy | Definierar om betalningsknappar använder en standardhöjd. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Height] | Butiksvy | Definiera höjden på betalningsknapparna. Standardvärde: ingen |
| [!UICONTROL Label] | Butiksvy | Definiera etikett som visas i betalningsknapparna. Alternativ: [!UICONTROL PayPal] / [!UICONTROL Checkout] / [!UICONTROL Buynow] / [!UICONTROL Pay] / [!UICONTROL Installment] |

{style="table-layout:auto"}
