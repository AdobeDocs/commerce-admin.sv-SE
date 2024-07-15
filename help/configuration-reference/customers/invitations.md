---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Invitations]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Customers] &gt; [!UICONTROL Invitations] i Commerce Admin.
exl-id: edafeaed-9c4f-4d9f-b35c-381ae5f43b67
feature: Configuration, Promotions/Events
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Invitations]

{{ee-feature}}

{{config}}

## [!UICONTROL General]

![Allmänt](./assets/invitations-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/marketing/invitations-configure.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Invitations Functionality] | Global | Avgör om modulen Inbjudningar är aktiverad. Alternativ: `Yes` / `No` |
| [!UICONTROL Enable Invitations on Frontend] | Webbplats | Avgör om inbjudningar kan hanteras från butiken. Alternativ: `Yes` / `No` |
| [!UICONTROL Referred Customer Group] | Butiksvy | Bestämmer kundgruppen för den inbjudne. Alternativ: <br/>**`Same as Inviter`**- Inbjudna tilldelas automatiskt till samma kundgrupp som de kunder som har bjudit in dem.<br/>**`Default Customer Group from Configuration`** - Inbjudna har automatiskt standardkundgruppen [Kund](../../customers/customer-groups.md). |
| [!UICONTROL New Accounts Registration] | Butiksvy | Avgör hur inbjudna kan skapa ett konto. Alternativ: <br/>**`By Invitation Only`**- Inbjudna måste följa länken i e-postmeddelandet med inbjudan för att skapa ett konto.<br/>**`Available to All`** - Inbjudna kan använda kontoregistreringsformuläret som finns i butiken. |
| [!UICONTROL Allow Customers to Add Custom Message to Invitation Email] | Butiksvy | Avgör om det finns ett fält i inbjudningsformuläret där den som bjuder in kan lägga till ett anpassat meddelande som skickas till den som bjuder in via e-post. Detta påverkar inte administratörens möjlighet att lägga till ett meddelande i en inbjudan. Alternativ: `Yes` / `No`. |
| [!UICONTROL Max Invitations Allowed to be Sent at One Time] | Butiksvy | Anger det maximala antalet inbjudningar som inbjudaren kan skicka samtidigt. En annan inbjudan skickas till varje e-postadress som inbjudaren inkluderar i formuläret. Detta skyddar serverresurserna genom att förhindra ett stort antal inbjudningar från att skickas samtidigt och gör det mindre troligt att inbjudningar skickas som skräppost. |

{style="table-layout:auto"}

## [!UICONTROL Email]

![E-post](./assets/invitations-email.png)<!-- zoom -->

<!-- [Email](https://docs.magento.com/user-guide/marketing/invitations-configure.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Customer Invitation Email Sender] | Butiksvy | Avgör avsändaren av det e-postmeddelande som inbjudna får när ett e-postmeddelande med en inbjudan skickas. Standardvärde: `General Contact` |
| [!UICONTROL Customer Invitation Email Template] | Butiksvy | Bestämmer mallen för det e-postmeddelande som inbjudna får när ett e-postmeddelande med en inbjudan skickas. Standardmall: `Customer Invitation` |

{style="table-layout:auto"}
