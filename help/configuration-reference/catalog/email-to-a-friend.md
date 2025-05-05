---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Email to a Friend]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Catalog] &gt; [!UICONTROL Email to a Friend] i Commerce Admin.
exl-id: cd1e3a8d-14ce-47e9-a3bc-c1b1dcbe0d8c
feature: Configuration, Communications
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Email to a Friend]

{{config}}

## [!UICONTROL Email Templates]

![E-postmallar](./assets/email-to-a-friend-email-templates.png)<!-- zoom -->

<!-- [Email Templates](https://experienceleague.adobe.com/sv/docs/commerce-admin/systems/communications/email-templates#configure-email-templates) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Butiksvy | Aktiverar processen som ger kunderna möjlighet att skicka e-post till vänner om produkter i din butik. Alternativ: `Yes` / `No` |
| [!UICONTROL Select Email Template] | Butiksvy | Identifierar e-postmallen som används för meddelanden som genereras av funktionen _Skicka e-post till en vän_. Standardmall: `Send Product to Friend` |
| [!UICONTROL Allow for Guests] | Butiksvy | Avgör om avsändaren måste vara en registrerad kund för att kunna skicka e-post om en produkt till vänner. Alternativ: `Yes` / `No` |
| [!UICONTROL Max Recipients] | Butiksvy | Begränsar antalet personer som kan vara med i distributionslistan för ett enda e-postmeddelande. |
| [!UICONTROL Max Products Sent in 1  Hour] | Butiksvy | Begränsar antalet produkter som kan delas av en enskild användare under en tidsperiod på en timme. |
| [!UICONTROL Limit Sending By] | Butiksvy | Bestämmer vilken metod som används för att identifiera avsändaren. Alternativen är: <br/>**`IP Address`**- (rekommenderas) Identifierar avsändaren med IP-adressen för den dator som används för att skicka produktmeddelanden.<br/>**`Cookie (unsafe)`** - Identifierar avsändaren med en webbläsarcookie. Den här metoden är inte säker eftersom användaren kan ta bort cookien för att undvika begränsningen. |

{style="table-layout:auto"}
