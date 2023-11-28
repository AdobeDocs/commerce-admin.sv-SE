---
title: '[!UICONTROL Sales] &gt; [!UICONTROL 3D Secure]'
description: Granska konfigurationsinställningarna på [!UICONTROL Sales] &gt; [!UICONTROL 3D Secure] sidan för Commerce Admin.
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] utvecklades av [!DNL Visa] för säkra onlinetransaktioner. Exempel på [!DNL 3-D Secure] lösningar som skapats av kortnätverk verifieras av [!DNL Visa], [!DNL Mastercard SecureCode], [!DNL American Express SafeKey]och [!DNL CardinalCommerce Consumer Authentication]. [!DNL CardinalCommerce] är en global ledare inom digital transaktionsautentisering och ett helägt dotterbolag till [!DNL Visa].

[!DNL 3-D Secure] version 2.0 har stöd för många förbättringar, bland annat avancerade autentiseringsmetoder och autentiseringsflöde samt förbättrad datadelning mellan handlare och utfärdare.

>[!NOTE]
>
>The [Braintree](../../stores-purchase/braintree.md) betalningsgatewayen har även stöd för [!DNL 3-D Secure] verifiering.

{{config}}

## [!UICONTROL CardinalCommerce]

![CardinalCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Environment] | Webbplats | Anger operativsystemet för [!DNL CardinalCommerce] konto. Om du kör i en testmiljö väljer du Sandbox. Alternativ: Sandlåda/produktion (standard) |
| [!UICONTROL Org Unit ID] | Webbplats | Organisationsenhets-ID från din [!DNL CardinalCommerce] handlarkonto. |
| [!UICONTROL API Key] | Webbplats | API-nyckeln från [!DNL CardinalCommerce] handlarkonto. |
| [!UICONTROL API Identifier] | Webbplats | API-identifieraren från [!DNL CardinalCommerce] handlarkonto. |
| [!UICONTROL Debug] | Webbplats | Alternativ: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}
