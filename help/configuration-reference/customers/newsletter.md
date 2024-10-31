---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Newsletter]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Customers] &gt; [!UICONTROL Newsletter] i Commerce Admin.
exl-id: a97003ca-985e-47fa-9ff3-677e05ef3729
feature: Configuration, Customers, Communications
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Newsletter]

{{config}}

>[!NOTE]
>
>Nyhetsbrevet är en del av marknadsföringsinstrument som gör det möjligt att skicka nyheter, rabatter och andra marknadsföringsmejl till kunderna. Registrerade kunder kan hantera sin prenumeration från sin [kontokontrollpanel](../../customers/account-dashboard-my-account.md).

## [!UICONTROL General Options]

![Allmänna alternativ](./assets/newsletter-general-options.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Butiksvy | Avgör om nyhetsbrev är aktiverade för butiksvyns omfång. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Subscription Options]

![Prenumerationsalternativ](./assets/newsletter-subscription-options.png)<!-- zoom -->

<!-- [Subscription Options](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/newsletters/newsletters) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Allow Guest Subscription] | Butiksvy | Avgör om oregistrerade gäster kan prenumerera på ett nyhetsbrev. Alternativ: `Yes` / `No` |
| [!UICONTROL Need to Confirm] | Butiksvy | Avgör om prenumerationsförfrågningar måste bekräftas. Den här metoden med dubbel anmälan är en valideringsåtgärd som förhindrar att personer prenumererar utan deras samtycke. Alternativ: `Yes` / `No` |
| [!UICONTROL Confirmation Email Sender] | Butiksvy | Identifierar den butikskontakt som visas som avsändare av ett e-postmeddelande som bekräftar en prenumerationsbegäran. |
| [!UICONTROL Confirmation Email Template] | Butiksvy | Bestämmer e-postmallen som används för meddelandet som skickas för att bekräfta en begäran om att prenumerera på ett nyhetsbrev. Standardmall: `Newsletter subscription confirmation` |
| E-postavsändaren lyckades | Butiksvy | Identifierar den butikskontakt som visas som avsändare av e-post som skickas till dem som kan prenumerera på ett nyhetsbrev. |
| [!UICONTROL Success Email Template] | Butiksvy | Bestämmer e-postmallen som används för meddelandet som skickas till dem som kan prenumerera på ett nyhetsbrev. Standardmall: `Newsletter subscription success` |
| [!UICONTROL Unsubscription Email Sender] | Butiksvy | Identifierar den butikskontakt som visas som avsändare av e-postmeddelanden som skickas till dem som begär att få avsluta sin nyhetsbrevsprenumeration. |
| [!UICONTROL Unsubscription Email Template] | Butiksvy | Bestämmer e-postmallen som används för meddelandet som skickas till dem som begär att få avsluta sin nyhetsbrevsprenumeration. Standardmall: `Newsletter unsubscription success` |

{style="table-layout:auto"}
