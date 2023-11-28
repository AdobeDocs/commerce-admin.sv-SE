---
title: '[!UICONTROL Security] &gt; [!UICONTROL 2FA]'
description: Granska konfigurationsinställningarna på [!UICONTROL Security] &gt; [!UICONTROL 2FA] sidan för Commerce Admin.
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>Lager som har aktiverat IMS-autentisering (Adobe Identity Management Services) har inbyggt Adobe Commerce- och Magento Open Source tvåfaktorautentisering (2FA) inaktiverat. Administratörsanvändare som är inloggade på sin Adobe Commerce-instans med sina inloggningsuppgifter för Adobe behöver inte autentisera igen för många administratörsuppgifter. Autentisering hanteras av Adobe IMS när administratörsanvändaren loggar in på sin aktuella session. Se [Integrera Adobe Commerce med Adobe IMS - översikt](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

Mer information om hur du ändrar de här inställningarna finns i [Tvåfaktorautentisering (2FA)](../../systems/security-two-factor-authentication.md) i _Handbok för adminsystem_.

## [!UICONTROL General]

![Allmänt](./assets/2fa-general.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Providers to use] | Global | Anger de tvåfaktorautentiseringsmetoder som du behöver. Om du väljer mer än en leverantör måste varje användare konfigurera varje 2FA-metod nästa gång de loggar in. |
| [!UICONTROL Configuration Email URL for Web API] | Global | För anpassade implementeringar, URL:en för en alternativ e-postkonfigurationslänk som skickas till _Administratör_ användare vid första inloggningen. Använd platshållaren i e-postmallen `:tfat` för att ange var token matas in. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL OTP Window] | Global | Livslängden i sekunder för varje engångslösenord som genereras av Google Authenticator. Standard: `30` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Duo Security]

![Duo-säkerhet](./assets/2fa-duo-security.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Integration Key] | Global | Integreringsnyckeln från [!DNL Duo Security] konto. |
| [!UICONTROL Secret Key] | Global | Den hemliga nyckeln från din [!DNL Duo Security] konto. |
| [!UICONTROL API Hostname] | Global | API-värdnamnet från din [!DNL Duo Security] konto. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Authy]

![Authy](./assets/2fa-authy.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL API Key] | Global | API-nyckeln från [!DNL Authy] konto. |
| [!UICONTROL OneTouch Message] | Global | Meddelandet som visas i [!DNL Authy] autentiseraren vid inloggning. Standard: `Login request to your Magento Admin` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL U2F Key]

![U2F-nyckel](./assets/2fa-u2f-key.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | Global | Domänen som används för att utfärda och bearbeta [!DNL WebAuthn] problem för anpassade WebAPI-implementeringar. |

{:style=&quot;table-layout:auto&quot;}
