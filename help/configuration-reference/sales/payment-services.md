---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL Payment Services]'
description: Granska konfigurationsinställningarna i avsnittet [!UICONTROL Payment Services] på sidan [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] i Commerce Admin.
exl-id: 255b7bd8-1d32-4393-9eba-43dc7754c752
feature: Configuration, Payments
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Payment Services]



Betalningstjänster erbjuder en nyckelfärdig självbetjäningslösning, inklusive sandlådetestning och en enkel konfiguration, för att tillhandahålla robust och säker betalningshantering. Mer information finns i [_Användarhandboken för betaltjänster_](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html).

Om du vill komma åt konfigurationsinställningarna för Betalningstjänster går du till **[!UICONTROL Sales]** > **[!UICONTROL Payment Services]** på sidofältet _Admin_ och klickar på **[!UICONTROL Settings]**.

![Inställningar för betaltjänster](assets/payment-services-menu-small.png){width="400"}

>[!NOTE]
>
>Information om hur du använder den äldre konfigurationen i stället för [Inställningar](https://experienceleague.adobe.com/docs/commerce/payment-services/configure/settings.html) finns i [Äldre konfiguration](https://experienceleague.adobe.com/docs/commerce/payment-services/configure/configure-admin.html).

## [!UICONTROL General]

![Allmänna inställningar](assets/payments-general-settings.png){width="600" zoomable="yes"}

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|---|---|---|
| [!UICONTROL Enable] | webbplats | Aktivera eller inaktivera [!DNL Payment Services] för webbplatsen. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Payment mode] | butiksvy | Ange metod, eller miljö, för din butik. Alternativ: [!UICONTROL Sandbox] / [!UICONTROL Production] |
| [!UICONTROL Sandbox Merchant ID] | butiksvy | Ditt handlar-ID för sandlådan, som genereras automatiskt vid introduktion av sandlådor. |
| [!UICONTROL Production Merchant ID] | butiksvy | Ditt handlar-ID för produktion, som genereras automatiskt när sandlådan introduceras. |
| [!UICONTROL Soft Descriptor] | webbplats eller butiksvy | Lägg till en mjuk beskrivning till webbplatserna och butiksvyer som ger information om kundtransaktioner och avgränsar varumärken, butiker eller produktlinjer. [!UICONTROL Use website]-växeln använder alla mjuka beskrivningar som har lagts till på webbplatsnivå. [!UICONTROL Use default]-växeln använder valfri mjuk beskrivning som lagts till som standard. |

{style="table-layout:auto"}

## [!UICONTROL Credit card fields]

![Inställningar för kreditkortsfält](assets/payments-ccfields-settings.png){width="600" zoomable="yes"}

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|---|---|---|
| [!UICONTROL Title] | butiksvy | Lägg till texten som ska visas som rubrik för det här betalningsalternativet i vyn Betalningsmetod vid utcheckning. |
| [!UICONTROL Payment Action] | webbplats | [betalningsåtgärden](payment-methods.md#payment-actions) för den angivna betalningsmetoden. Alternativ: [!UICONTROL Authorize] / [!UICONTROL Authorize and Capture] |
| [!UICONTROL 3DS Secure authentication] | webbplats | Aktivera eller inaktivera [3DS-säker autentisering](https://experienceleague.adobe.com/docs/commerce/payment-services/security-compliance/security.html#3ds). Alternativ: [!UICONTROL Always] / [!UICONTROL When Required] / [!UICONTROL Off] |
| [!UICONTROL Show on checkout page] | webbplats | Aktivera eller inaktivera kreditkortsfält som ska visas på utcheckningssidan. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Vault enabled] | butiksvy | Aktivera eller inaktivera [kreditkortssäkringen](https://experienceleague.adobe.com/docs/commerce/payment-services/payments-checkout/vaulting.html). Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show vaulted payment methods in Admin] | butiksvy | Aktivera eller inaktivera möjligheten att slutföra beställningar för kunder i administratören [med en betalningsmetod som är skyddad](https://experienceleague.adobe.com/docs/commerce/payment-services/payments-checkout/vaulting.html). Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Debug Mode] | webbplats | Aktivera eller inaktivera felsökningsläget. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |

{style="table-layout:auto"}

## [!UICONTROL Payment buttons]

![Inställningar för PayPal-betalningsknappar](assets/payments-ppbuttons-settings.png){width="600" zoomable="yes"}

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|---|---|---|
| [!UICONTROL Title] | butiksvy | Lägg till texten som ska visas som rubrik för det här betalningsalternativet i vyn Betalningsmetod vid utcheckning. |
| [!UICONTROL Payment Action] | webbplats | [betalningsåtgärden](payment-methods.md#payment-actions){target="_blank"} för den angivna betalningsmetoden. Alternativ: [!UICONTROL Authorize] / [!UICONTROL Authorize and Capture] |
| [!UICONTROL Show PayPal buttons on checkout page] | butiksvy | Aktivera eller inaktivera [!DNL PayPal Smart Buttons] på utcheckningssidan. Alternativ: [!UICONTROL &#x200B; Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons on product detail page] | butiksvy | Aktivera eller inaktivera [!DNL PayPal Smart Buttons] på produktinformationssidan. Alternativ: [!UICONTROL &#x200B; Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons in mini-cart preview] | butiksvy | Aktivera eller inaktivera [!DNL PayPal Smart Buttons] i förhandsvisningen av minikundvagnen. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons on cart page] | butiksvy | Aktivera eller inaktivera [!DNL PayPal Smart Buttons] på kundvagnssidan. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Pay Later button] | butiksvy | Aktivera eller inaktivera utseendet på betalningsalternativ vid ett senare tillfälle där betalningsknappar visas. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Pay Later Message] | webbplats | Aktivera eller inaktivera meddelandet Betala senare i kundvagnen, på produktsidan, i minikundvagnen och under kassaflödet. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show Venmo button] | butiksvy | Aktivera eller inaktivera betalalternativet Venmo där betalningsknappar visas. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show Apple Pay button] | butiksvy | Aktivera eller inaktivera betalningsalternativet Apple Pay där betalningsknappar visas. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Credit and Debit card button] | butiksvy | Aktivera eller inaktivera alternativet för kredit- och betalkortsbetalning där betalningsknappar visas. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Debug Mode] | webbplats | Aktivera eller inaktivera felsökningsläget. Alternativ: [!UICONTROL Yes] / [!UICONTROL No] |

{style="table-layout:auto"}

## [!UICONTROL PayPal Smart Button Styling]

![Formatinställningar för knappar för huvudbetalning](assets/payments-buttonstyle-settings.png){width="600" zoomable="yes"}

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
