---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Reward Points]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Customers] &gt; [!UICONTROL Reward Points] i Commerce Admin.
exl-id: 0b7f8806-74c5-4467-87da-0faae50f164b
feature: Configuration, Rewards
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Reward Points]

{{ee-feature}}

{{config}}

>[!NOTE]
>
>[Konfiguration av belöningsvalutakurser](../../merchandising-promotions/reward-exchange-rates.md) krävs för att kunder och administratörer ska kunna lösa in belöningspunkter under utcheckning.

## [!UICONTROL Reward Points]

![Belöningspunkter](./assets/reward-points-reward-points.png)<!-- zoom -->

<!-- [Reward Points](https://experienceleague.adobe.com/sv/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Reward Points Functionality] | Global | Aktiverar eller inaktiverar belöningspoäng. Alternativ: `Yes` / `No`. |
| [!UICONTROL Enable Reward Points Functionality on Storefront] | Webbplats | När det här alternativet är aktiverat kan kunderna tjäna in poäng genom sina aktiviteter och lösa in dem i kassan. Om det är inaktiverat kan bara administratörsanvändare tilldela och lösa in poäng för kunders räkning. Alternativ: `Yes` / `No`. |
| [!UICONTROL Customers May See Reward Points History] | Webbplats | När det här alternativet är aktiverat kan kunderna se en detaljerad historik med varje periodisering, inlösen och förfallodatum för belöningspoäng på sin kontokontrollpanel. Alternativ: `Yes` / `No` |
| [!UICONTROL Reward Points Balance Redemption Threshold] | Webbplats | Kräver att kunderna uppnår ett minimipoängsaldo innan de kan lösa in dem för order. Lämna tomt utan minimikrav. |
| [!UICONTROL Cap Reward Points Balance At] | Webbplats | Hindrar kunder från att anskaffa mer än det här maximala poängsaldot. Lämna tomt om du inte vill ha något maximum. |
| [!UICONTROL Reward Points Expire in (days)] | Webbplats | Anger belöningspoängens livstid i dagar. Varje batch med poäng som intjänas under olika aktiviteter har en separat livstid. Varje batch i historiken för belöningspunkter anger antalet dagar som återstår innan poängen upphör att gälla. Historien kan visas från kundens kontouppsättning, om den är aktiverad, och från administratören. Lämna tomt utan förfallodatum. |
| [!UICONTROL Reward Points Expiry Calculation] | Webbplats | Bestämmer vilken metod som används för att bestämma när belöningspunkter förfaller. Alternativ: <br/>**`Static`**- Fastställer den återstående livstiden för belöningspunkter baserat på antalet dagar som angetts i konfigurationen. Om utgångsgränsen i konfigurationen ändras ändras inte utgångsdatumet för befintliga punkter.<br/>**`Dynamic`** - Beräknar antalet dagar som återstår när belöningspunktssaldot ökar. Om utgångsgränsen i konfigurationen ändras uppdateras förfalloberäkningarna för alla befintliga punkter. |
| [!UICONTROL Refund Reward Points Automatically] | Global | Avgör om tillgängliga belöningspoäng återbetalas automatiskt. Alternativ: `Yes` / `No` |
| [!UICONTROL Deduct Reward Points from Refund Amount Automatically] | Global | Detta avgör om belöningspoäng som intjänats genom inköp annulleras helt eller delvis vid orderåterbetalning, när den här funktionen är aktiverad. Endast belöningspoäng från den order som de har fått påverkas när den ordern återbetalas. Alternativ: `Yes` / `No`. |
| [!UICONTROL Landing Page] | Butiksvy | Anger den CMS-sida som förklarar belöningspoängprogrammet. En länk till standardsidan för belöningar visas på de platser i din butik där poäng kan erhållas. |

{style="table-layout:auto"}

## [!UICONTROL Actions for Acquiring Reward Points by Customers]

![Åtgärder för att hämta belöningspoäng av kunder](./assets/reward-points-actions-for-acquiring.png)<!-- zoom -->

<!-- [Actions for Acquiring Reward Points by Customers](https://experienceleague.adobe.com/sv/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Purchase] | Webbplats | Avgör om belöningspoäng upptas för inköp baserat på de konfigurerade [belöningskurserna](../../merchandising-promotions/reward-exchange-rates.md). Alternativ: `Yes` / `No` |
| [!UICONTROL Registration] | Webbplats | Anger antalet poäng som tjänats in för att öppna ett kundkonto. |
| [!UICONTROL Newsletter Signup] | Webbplats | Anger antalet poäng som en registrerad kund tjänat som prenumererar på ett nyhetsbrev. (Poäng är inte tillgängliga för abonnemang av gäster.) Om en kund säger upp prenumerationen och sedan prenumererar igen får kunden inga poäng för den andra prenumerationen. |
| [!UICONTROL Converting Invitation to Customer] | Webbplats | Anger antalet poäng som en kund som skickar en inbjudan får när mottagaren sedan öppnar ett kundkonto. |
| [!UICONTROL Invitation to Customer Conversions Quantity Limit] | Webbplats | Begränsar antalet inbjudningskonverteringar som kan användas för att tjäna poäng för den kund som skickar inbjudan. Lämna tomt om du inte vill ha någon begränsning. |
| [!UICONTROL Converting Invitation to Order] | Webbplats | Anger antalet poäng en kund tjänat in som skickar en inbjudan när mottagaren gör en första beställning. |
| [!UICONTROL Invitation to Order Conversions Quantity Limit] | Webbplats | Begränsar antalet orderkonverteringar som kan generera poäng för den person som skickar inbjudan. Om det är tomt finns det ingen maxgräns. |
| [!UICONTROL Invitation Conversion to Order Reward] | Webbplats | Anger hur ofta en kund kan få belöningspoäng när den bjuder in. Alternativ: <br/>**`Each`**- Kunden får belöningspoäng för varje fakturerad order som faktureras av mottagaren. Belöningspoäng ges enligt de växelkurser som fastställts för den nödvändiga kombinationen av en webbplats och en kundgrupp.<br/>**`First`** - Kunden får belöningspoäng endast för den första fakturerade ordern som har lagts av fakturamottagarna. Om fler än en beställare registrerar och lägger en order konverteras endast beloppet för den första beställningen till belöningspoäng och beviljas kunden. |
| [!UICONTROL Review Submission] | Webbplats | Fastställer antalet poäng som en kund som skickar in en granskning som godkänts för publicering får. |
| [!UICONTROL Rewarded Reviews Submission Quantity Limit] | Webbplats | Begränsar antalet recensioner som kan användas för att få poäng per kund. Lämna tomt om du inte vill ha någon begränsning. |

{style="table-layout:auto"}

## [!UICONTROL Email Notification Settings]

![Inställningar för e-postavisering](./assets/reward-points-email-notification-settings.png)<!-- zoom -->

<!-- [Email Notification Settings](https://experienceleague.adobe.com/sv/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Email Sender] | Butiksvy | Bestämmer den butikskontakt som visas som avsändare av e-postmeddelanden om saldouppdatering och förfallodatum. |
| [!UICONTROL Subscribe Customers by Default] | Global | Bestämmer standardprenumerationsstatus för kunder för meddelanden om både saldouppdatering och förfallodatum. |
| [!UICONTROL Balance Update Email] | Butiksvy | Bestämmer vilken mall som används för meddelandet som skickas till kunder när deras punktbalans uppdateras. Standardmall: `Reward Points Balance Update` |
| [!UICONTROL Reward Points Expiry Warning Email] | Butiksvy | Bestämmer mallen för e-postmeddelandet som kunderna får när utgångsvarningsgränsen har nåtts för en grupp punkter. Standardmall: `Reward Points Expiry Warning` |
| [!UICONTROL Expiry Warning before (days)] | Global | Anger hur många dagar före utgångsdatum som meddelandet ska skickas. Lämna tomt om du inte vill skicka några förfallomeddelanden. Meddelandet skickas inte om antalet angivna dagar är större än poängens återstående livstid. |

{style="table-layout:auto"}
