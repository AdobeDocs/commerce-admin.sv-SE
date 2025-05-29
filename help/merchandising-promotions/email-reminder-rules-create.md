---
title: Skapa e-postpåminnelser
description: Lär dig hur du ställer in en påminnelseregel för e-post som använder en befintlig kundvagnsprisregel.
exl-id: b04dc8a3-5daa-43f2-bf52-d85bfd2554b7
feature: Merchandising, Communications
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Skapa e-postpåminnelser

Innan du konfigurerar en påminnelseregel för e-post måste du först [ställa in en kundprisregel](price-rules-cart-create.md) för att definiera den befordran som erbjuds. Regelvillkor som utlöser en e-postpåminnelse kan baseras på egenskaper för kundvagn, önskelisteegenskaper eller båda.

>[!NOTE]
>
>Påminnelser via e-post kan höja en kundvagnsregel med eller utan en kupong. En kundprisregel som definierar en autogenererad kupong genererar en slumpmässig kupongkod för varje kund.

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Reminder Rules]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add New Rule]** i det övre högra hörnet.

1. Slutför _[!UICONTROL Rule Information]_&#x200B;enligt följande:

   ![Påminnelseregel för e-post](./assets/email-reminder-new.png){width="700" zoomable="yes"}

   - Ange en **[!UICONTROL Rule Name]** för att identifiera regeln internt.

   - Ange en kort **[!UICONTROL Description]** av regeln.

   - Om du vill välja den **[!UICONTROL Cart Price Rule]**-kampanj som den här påminnelsen ska annonsera klickar du på **[!UICONTROL Select Rule…]** och väljer regeln.

     ![Kundvagnsregel - välj](./assets/email-reminder-select-rule.png){width="600" zoomable="yes"}

   - Om du vill att regeln ska börja gälla omedelbart anger du **[!UICONTROL Status]** till `Active`.

   - Om du vill ange ett datumintervall för att regeln ska vara aktiv anger du datumen **[!UICONTROL From]** och **[!UICONTROL To]**.

     Du kan också välja datum från kalendern ( ![kalenderikon](../assets/icon-calendar.png) ).

   - Om du vill skicka påminnelsen mer än en gång anger du antalet dagar före nästa e-postmeddelande i fältet **[!UICONTROL Repeat Schedule]**.

1. Välj **[!UICONTROL Conditions]** i panelen till vänster.

   Minst ett villkor måste definieras för regeln. Processen liknar att skapa en [katalogprisregel.](price-rules-catalog.md)

   ![Villkor för e-postpåminnelse](./assets/email-reminder-conditions.png){width="600" zoomable="yes"}

   Klicka på _Lägg till_ ( ![Lägg till ikon](../assets/icon-add-green-circle.png)) för att visa listan med alternativ och välj sedan ett av följande villkor:

   - Önsklista
   - Kundvagn

   >[!NOTE]
   >
   >Om en kund har fler än en matchande övergiven kundvagn, önskelista eller kombination av båda aktiveras e-postpåminnelsen endast en gång för den kunden. Om du vill utlösa samma e-postpåminnelse igen använder du fältet _[!UICONTROL Repeat Schedule]_&#x200B;för att ange antalet dagar mellan e-postmeddelanden. <br/>
   >
   >Samma e-postpåminnelse hämtas **_inte_** för samma kund för **_nya_** övergivna kundvagnar och önskelistor **_när_** _[!UICONTROL Repeat Schedule]_-perioden är slut.

   Slutför villkoret för att beskriva scenariot som utlöser e-postpåminnelsen.

   ![exempel på villkor för e-postpåminnelse](./assets/email-reminder-condition-example.png){width="600" zoomable="yes"}

1. Välj **[!UICONTROL Emails and Labels]** i panelen till vänster.

   ![Regel för påminnelse via e-post - mallar för e-post och etiketter ](./assets/email-reminder-rule-emails-labels-email-templates.png){width="600" zoomable="yes"}

1. I avsnittet **[!UICONTROL Email Templates]** väljer du den e-postmall som ska användas för varje webbplats och butiksvy i din [butikshierarki](../getting-started/websites-stores-views.md).

   Om du inte vill skicka påminnelsemeddelandet till kunder i en butiksvy lämnar du värdet `Not Selected`.

1. Gör följande i avsnittet _Standardtitlar och beskrivning_:

   - Ange **[!UICONTROL Rule Title for All Store Views]**.

     >[!NOTE]
     >
     >Det här värdet kan införlivas i e-postmallar med variabeln `promotion_name`.

   - Ange **[!UICONTROL Rule Description for All Store Views]**.

     ![Påminnelser via e-post - titlar och beskrivningar](./assets/email-reminders-emails-and-labels-default-titles-description.png){width="500" zoomable="yes"}

   - I avsnittet _[!UICONTROL Titles and Descriptions Per Store View]_&#x200B;anger du **[!UICONTROL Rule Title]**&#x200B;och **[!UICONTROL Description]**&#x200B;för_ standardbutiksvyn _. Om du har flera butiksvyer anger du lämplig rubrik och beskrivning för varje.

     >[!NOTE]
     >
     >Beskrivningen kan infogas i e-postmallar med variabeln promotion_description.

     ![Titlar och beskrivningar - butiksvy](./assets/email-reminder-rules-title-descriptions-per-store-view.png){width="500" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]** när du är klar.

## Utlösarvillkor

| Source | Utlösare |
|--- |--- |
| [!UICONTROL Wish List] | [!UICONTROL Conditions Combination]<br/>[!UICONTROL Sharing]<br/>[!UICONTROL Number of Items]<br/>[!UICONTROL Items Sub selection] |
| [!UICONTROL Shopping Cart] | [!UICONTROL Conditions Combination]<br/>[!UICONTROL Coupon Code]<br/>[!UICONTROL Cart Line Items]<br/>[!UICONTROL Items Quantity]<br/>[!UICONTROL Virtual Only]<br/>[!UICONTROL Total Amount]<br/>[!UICONTROL Items Subselection] |

{style="table-layout:auto"}

## Fältbeskrivningar

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Rule Name] | Namnet på den automatiska påminnelseregeln identifierar regeln internt. |
| [!UICONTROL Description] | En beskrivning av regeln för intern referens. |
| [!UICONTROL Shopping Cart Price Rule] | Kundvagnsregeln som är associerad med den här e-postpåminnelsen. Påminnelsemeddelanden kan befordra en kundvagnsprisregel med eller utan kupong. Om en kundvagnsprisregel innehåller en autogenererad kupong, genererar påminnelseregeln en slumpmässig, unik kupongkod för varje kund. |
| [!UICONTROL Assigned to Website] | De webbplatser som får automatiska påminnelser via e-post baserade på den här regeln. |
| [!UICONTROL Status] | Aktiverar regeln. Om status är inaktiv ignoreras alla andra inställningar och regeln aktiveras inte. Alternativ: `Active` / `Inactive` |
| [!UICONTROL From Date] | Startdatum för den här automatiska påminnelseregeln. Om inget datum anges aktiveras regeln omedelbart. |
| [!UICONTROL To Date] | Slutdatumet för den här automatiska påminnelseregeln. Om inget datum anges blir regeln aktiv i oändlighet. |
| [!UICONTROL Repeat Schedule] | Antalet dagar innan regeln aktiveras och påminnelsemeddelandet skickas igen, förutsatt att villkoren uppfylls. Om du vill utlösa regeln mer än en gång anger du antalet dagar före nästa e-postsändning, avgränsade med kommatecken. Ange till exempel `7` om du vill att regeln ska aktiveras igen sju dagar senare. Ange `7,14` om du vill att regeln ska aktiveras om sju dagar och sedan 14 dagar senare. |
| [!UICONTROL Email Templates] | Bestämmer e-postmallen som ska användas för varje butiksvy. |
| [!UICONTROL Rule Title for All Store Views] | Anger regelns rubrik för varje butiksvy. |
| [!UICONTROL Rule Description for All Store Views] | Anger beskrivningen av regeln för varje butiksvy. |

{style="table-layout:auto"}
