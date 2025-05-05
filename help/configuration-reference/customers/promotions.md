---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Promotions]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Customers] &gt; [!UICONTROL Promotions] i Commerce Admin.
exl-id: 93035d46-2e9e-466d-a5e3-d69ce6b662b8
feature: Configuration, Promotions/Events
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Promotions]

{{config}}

## [!UICONTROL Automated Email Reminder Rules]

{{ee-feature}}

![Automatiska påminnelseregler för e-post](./assets/promotions-automated-email-reminder-rules.png)<!-- zoom -->

<!-- [Automated Email Reminder Rules](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules#configure-email-reminders) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Reminder Emails] | Global | Aktiverar automatiska e-postpåminnelser. Om inställningen är Nej ignoreras de återstående inställningarna. Alternativ: `Yes` / `No` |
| [!UICONTROL Frequency] | Global | Anger hur ofta Commerce ska söka efter nya kunder som är berättigade till automatiska e-postpåminnelser. Alternativ: <br/>**`Minute Intervals`**- Skickar e-postmeddelandet enligt det valda intervallet. (5 minuter, 10 minuter, 15 minuter, 20 minuter eller 30 minuter)<br/>**`Hourly`** - Skickar e-post varje timme, vid en minut efter den angivna timmen. Ange ett värde mellan 0 och 59. <br/>**`Daily`**- Skickar e-post dagligen från starttiden. |
| [!UICONTROL Interval] | Global | Intervallet måste vara lika med eller större än din cron.php-startperiod. Alternativ: `5 minutes` / `10 minutes` / `15 minutes` / `20 minutes` / `30 minutes` |
| [!UICONTROL Start Time] | Global | Anger den dag, minut och sekund som e-postmeddelandet skickas. Anges i 24-timmarsformat, baserat på systemtiden på servern. |
| [!UICONTROL Maximum Emails per One Run] | Global | Begränsar antalet e-postmeddelanden som skickas i ett schemalagt block. |
| [!UICONTROL Email Send Failure Threshold] | Global | Antalet gånger som påminnelsen försöker skicka ut meddelanden till en viss e-postadress och misslyckas. När värdet är 0 finns det inget tröskelvärde och meddelanden skickas även fortsättningsvis trots eventuella fel. |
| [!UICONTROL Reminder Email Sender] | Butiksvy | Butiksidentiteten som visas som avsändare av e-postmeddelandet. |

{style="table-layout:auto"}

## [!UICONTROL Auto Generated Specific Coupon Codes]

![Autogenererade specifika kupongkoder](./assets/promotions-auto-generated-specific-coupon-codes.png)<!-- zoom -->

<!-- [Auto Generated Specific Coupon Codes](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart-coupon#configure-coupon-codes)  -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Code Length] | Global | Definierar längden på kupongkoden, exklusive prefix, suffix och avgränsare. |
| [!UICONTROL Code Format] | Global | Definierar kupongkodformatet. Alternativen är: <br/>**`Alphanumeric`**- Valfri kombination av bokstäver och siffror.<br/>**`Alphabetical`** - Endast bokstäver. <br/>**`Numeric`**- Endast siffror. |
| [!UICONTROL Code Prefix] | Global | Ett värde som läggs till i början av alla kupongkoder. Om du inte vill använda ett prefix lämnar du fältet tomt. |
| [!UICONTROL Code Suffix] | Global | Ett värde som läggs till i slutet av alla koder. Om du inte vill använda ett suffix lämnar du fältet tomt. |
| [!UICONTROL Dash Every X Characters] | Global | Intervallet för att infoga ett bindestreck (-) i alla kupongkoder. Om du inte vill använda ett streck lämnar du fältet tomt. <br/>_&#x200B;**Obs!**&#x200B;_ Kupongkoder som bara skiljer sig åt med bindestreck anses vara olika koder. |

{style="table-layout:auto"}
