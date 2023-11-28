---
title: Skapa e-postpåminnelser
description: Lär dig hur du ställer in en påminnelseregel för e-post som använder en befintlig kundvagnsprisregel.
exl-id: b04dc8a3-5daa-43f2-bf52-d85bfd2554b7
feature: Merchandising, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 0%

---

# Skapa e-postpåminnelser

Innan du ställer in en påminnelseregel för e-post måste du först ställa in en kundprisregel för att definiera den kampanj som erbjuds. Regelvillkor som utlöser en e-postpåminnelse kan baseras på egenskaper för kundvagn, önskelisteegenskaper eller båda.

>[!NOTE]
>
>Påminnelser via e-post kan höja en kundvagnsregel med eller utan en kupong. En kundprisregel som definierar en autogenererad kupong genererar en slumpmässig kupongkod för varje kund.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Reminder Rules]**.

1. Klicka på i det övre högra hörnet **[!UICONTROL Add New Rule]**.

1. Slutför _[!UICONTROL Rule Information]_, enligt följande:

   ![Påminnelseregel för e-post](./assets/email-reminder-new.png){width="700" zoomable="yes"}

   - Ange en **[!UICONTROL Rule Name]** för att identifiera regeln internt.

   - Ange en kort beskrivning **[!UICONTROL Description]** av regeln.

   - Välj **[!UICONTROL Cart Price Rule]** marknadsföring att den här påminnelsen ska annonsera, klicka på **[!UICONTROL Select Rule…]** och markera regeln.

     ![Kundregel - välj](./assets/email-reminder-select-rule.png){width="600" zoomable="yes"}

   - Om du vill att regeln ska börja gälla omedelbart anger du **[!UICONTROL Status]** till `Active`.

   - Om du vill ange ett datumintervall för att regeln ska vara aktiv anger du **[!UICONTROL From]** och **[!UICONTROL To]** datum.

     Du kan också välja datumet i kalendern ( ![Kalenderikon](../assets/icon-calendar.png) ).

   - Om du vill skicka påminnelsen mer än en gång anger du antalet dagar före nästa e-postmeddelande i dialogrutan **[!UICONTROL Repeat Schedule]** fält.

1. Välj **[!UICONTROL Conditions]**.

   Minst ett villkor måste definieras för regeln. Processen påminner om att skapa en [katalogprisregel.](price-rules-catalog.md)

   ![Villkor för e-postpåminnelse](./assets/email-reminder-conditions.png){width="600" zoomable="yes"}

   Klicka _Lägg till_ ( ![Ikonen Lägg till](../assets/icon-add-green-circle.png)) om du vill visa en lista med alternativ och sedan välja något av följande villkor:

   - Önsklista
   - Kundvagn

   >[!NOTE]
   >
   >Om en kund har fler än en matchande övergiven kundvagn, önskelista eller kombination av båda aktiveras e-postpåminnelsen endast en gång för den kunden. Om du vill aktivera samma e-postpåminnelse igen använder du _[!UICONTROL Repeat Schedule]_fält för att ange antalet dagar mellan e-postmeddelanden.

   Slutför villkoret för att beskriva scenariot som utlöser e-postpåminnelsen.

   ![exempel på e-postpåminnelsevillkor](./assets/email-reminder-condition-example.png){width="600" zoomable="yes"}

1. Välj **[!UICONTROL Emails and Labels]**.

   ![Påminnelseregel för e-post - e-postmallar och etikettmallar ](./assets/email-reminder-rule-emails-labels-email-templates.png){width="600" zoomable="yes"}

1. I **[!UICONTROL Email Templates]** väljer du den e-postmall som ska användas för varje webbplats och butiksvy i [butikshierarki](../getting-started/websites-stores-views.md).

   Om du inte vill skicka påminnelsen via e-post till kunder i en butiksvy lämnar du värdet `Not Selected`.

1. I _Standardtitlar och -beskrivning_ gör du följande:

   - Ange **[!UICONTROL Rule Title for All Store Views]**.

     >[!NOTE]
     >
     >Det här värdet kan införlivas i e-postmallar med `promotion_name` variabel.

   - Ange **[!UICONTROL Rule Description for All Store Views]**.

     ![Påminnelser via e-post - titlar och beskrivningar](./assets/email-reminders-emails-and-labels-default-titles-description.png){width="500" zoomable="yes"}

   - I _[!UICONTROL Titles and Descriptions Per Store View]_anger du **[!UICONTROL Rule Title]**och **[!UICONTROL Description]**för_ Standardbutiksvy _. Om du har flera butiksvyer anger du lämplig rubrik och beskrivning för varje.

     >[!NOTE]
     >
     >Beskrivningen kan infogas i e-postmallar med variabeln promotion_description.

     ![Titlar och beskrivningar - butiksvyn](./assets/email-reminder-rules-title-descriptions-per-store-view.png){width="500" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save]**.

## Utlösarvillkor

| Källa | Utlösare |
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
| [!UICONTROL Repeat Schedule] | Antalet dagar innan regeln aktiveras och påminnelsemeddelandet skickas igen, förutsatt att villkoren uppfylls. Om du vill utlösa regeln mer än en gång anger du antalet dagar före nästa e-postsändning, avgränsade med kommatecken. Skriv till exempel `7` om du vill att regeln ska aktiveras igen sju dagar senare, ange `7,14` för att få regeln utlöst på sju dagar, och återigen 14 dagar senare. |
| [!UICONTROL Email Templates] | Bestämmer e-postmallen som ska användas för varje butiksvy. |
| [!UICONTROL Rule Title for All Store Views] | Anger regelns rubrik för varje butiksvy. |
| [!UICONTROL Rule Description for All Store Views] | Anger beskrivningen av regeln för varje butiksvy. |

{style="table-layout:auto"}
