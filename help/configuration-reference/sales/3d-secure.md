---
title: '[!UICONTROL Sales] &gt; [!UICONTROL 3D Secure]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Sales] &gt; [!UICONTROL 3D Secure] i Commerce Admin.
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] utvecklades av [!DNL Visa] för att befordra säkra onlinetransaktioner. Exempel på [!DNL 3-D Secure] lösningar som skapats av kortnätverk verifieras av [!DNL Visa], [!DNL Mastercard SecureCode], [!DNL American Express SafeKey] och [!DNL CardinalCommerce Consumer Authentication]. [!DNL CardinalCommerce] är en global ledare inom autentisering av digitala transaktioner och ett helägt dotterbolag till [!DNL Visa].

[!DNL 3-D Secure] version 2.0 har stöd för många förbättringar, bland annat avancerade autentiseringsmetoder och autentiseringsflöde samt förbättrad datadelning mellan handlare och utfärdare.

>[!NOTE]
>
>Betalningsgatewayen [Braintree](../../stores-purchase/braintree.md) har också stöd för verifiering av [!DNL 3-D Secure].

{{config}}

## [!UICONTROL CardinalCommerce]

![CardinalCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Environment] | Webbplats | Anger operativsystemet för ditt [!DNL CardinalCommerce]-konto. Om du kör i en testmiljö väljer du Sandbox. Alternativ: Sandlåda/produktion (standard) |
| [!UICONTROL Org Unit ID] | Webbplats | Organisationsenhets-ID från ditt [!DNL CardinalCommerce]-handlarkonto. |
| [!UICONTROL API Key] | Webbplats | API-nyckeln från ditt [!DNL CardinalCommerce]-handlarkonto. |
| [!UICONTROL API Identifier] | Webbplats | API-identifieraren från ditt [!DNL CardinalCommerce]-handlarkonto. |
| [!UICONTROL Debug] | Webbplats | Alternativ: `Yes` / `No` |

{style="table-layout:auto"}
