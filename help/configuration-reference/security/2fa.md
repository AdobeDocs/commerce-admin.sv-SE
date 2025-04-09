---
title: '[!UICONTROL Security] &gt; [!UICONTROL 2FA]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Security] &gt; [!UICONTROL 2FA] i Commerce Admin.
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
source-git-commit: 22bfff98a9189f3020de21b31705351510dcf1be
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>Lager som har aktiverat autentisering med Adobe Identity Management Services (IMS) har inbyggt Adobe Commerce- och Magento Open Source tvåfaktorautentisering (2FA) inaktiverat. Administratörsanvändare som är inloggade på sin Adobe Commerce-instans med sina Adobe-inloggningsuppgifter behöver inte autentisera igen för många administratörsuppgifter. Autentisering hanteras av Adobe IMS när administratörsanvändaren loggar in på sin aktuella session. Se [Integrera Adobe Commerce med Adobe IMS - översikt](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

Mer information om hur du ändrar de här inställningarna finns i [Tvåfaktorautentisering (2FA)](../../systems/security-two-factor-authentication.md) i _Admin Systems Guide_.

## [!UICONTROL General]

![Allmänt](./assets/2fa-general.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Providers to use] | Global | Indicates the two-factor authentication methods that you require. If you select more than one provider, each user is required to configure each 2FA method the next time they log in. |
| [!UICONTROL Configuration Email URL for Web API] | Global | For custom implementations, the URL for an alternate email configuration link that is sent to _Admin_ users at first login. Använd platshållaren `:tfat` i e-postmallen för att ange var token matas in. |
| [!UICONTROL Retry attempt limit for Two-Factor Authentication] | Global | Avgör hur många gånger en administratör kan ange en [!DNL one-time password (OTP)] innan deras konto tillfälligt inaktiveras. Standard: `10` |
| [!UICONTROL Two-Factor Authentication lockout time (seconds)] | Global | Avgör hur länge (i sekunder) som en administratör kan vänta med att ange [!DNL one-time password (OTP)] innan deras konto inaktiveras tillfälligt. Standard: `300` |

{style="table-layout:auto"}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL OTP Window] | Global | Avgör hur länge (i sekunder) som systemet accepterar en administratörs [!DNL one-time-password (OTP)] efter att det har gått ut. Kan inte vara längre än en engångslösenord (vanligtvis 30 sekunder). Standard: `29` |

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![Duo-säkerhet](./assets/2fa-duo-security.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Client Id] | Global | Klient-ID från ditt [!DNL Duo Security]-konto. |
| [!UICONTROL Client Secret] | Global | The Client Secret from your [!DNL Duo Security] account. |
| [!UICONTROL Integration Key] | Global | Integreringsnyckeln från ditt [!DNL Duo Security] API-konto. |
| [!UICONTROL Secret Key] | Global | Den hemliga nyckeln från ditt [!DNL Duo Security] API-konto. |
| [!UICONTROL API Hostname] | Global | API-värdnamnet från ditt [!DNL Duo Security]-konto. |

{style="table-layout:auto"}

## [!UICONTROL Authy]

![Autenticera](./assets/2fa-authy.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL API Key] | Global | API-nyckeln från ditt [!DNL Authy]-konto. |
| [!UICONTROL OneTouch Message] | Global | The message that appears in the [!DNL Authy] authenticator at login. Standard: `Login request to your Magento Admin` |

{style="table-layout:auto"}

## [!UICONTROL U2F Key]

![U2F Key](./assets/2fa-u2f-key.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | Global | Domänen som används för att utfärda och bearbeta [!DNL WebAuthn]-utmaningar för anpassade WebAPI-implementeringar. |

{style="table-layout:auto"}
