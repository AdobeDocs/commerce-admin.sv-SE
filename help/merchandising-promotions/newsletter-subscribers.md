---
title: Hantera prenumeranter på nyhetsbrev
description: Lär dig hur du hanterar prenumeranter på nyhetsbrev med en enkel lista över aktiva prenumerationer.
exl-id: c7e8e642-e3fd-4979-9ea3-2d96839730b2
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# Hantera prenumeranter på nyhetsbrev

Som en god vana bör du hantera din prenumerationslista regelbundet och se till att behandla alla förfrågningar om att avbryta prenumerationen. I vissa jurisdiktioner krävs enligt lag att ansökningar om avanmälan behandlas inom en viss tidsperiod.

Du kan enkelt hantera dina prenumeranter med en enkel lista över aktiva prenumerationer. När en kund skickar en begäran om att avbryta prenumerationen kan du helt enkelt utföra en _Unsubscribe_ -åtgärd på en eller flera valda prenumerationer.

I uppsättningar för en enda plats med flera butiksvyer kan ett kundkonto kopplas till en viss butiksvy.

I flerbutiks- och flerplatsinställningar med ett globalt [kundkontoomfång](../customers/customer-account-scope.md) kan ett kundkonto prenumereras på nyhetsbrev för flera platser/butiker. I det här fallet kanske du vill redigera kundkontot för att hantera en grupp prenumerationer eller avbryta en prenumeration för en viss webbplats/butik för att efterleva en begäran.

Om du vill använda en tredjepartstjänst för att skicka nyhetsbrev kan du exportera din prenumerationslista som en CSV- eller XML-fil.

## Hantera prenumerationer för en kund

1. Gå till **[!UICONTROL Customers]** > **[!UICONTROL All Customers]** på sidofältet _Admin_.

1. Hitta kunden i rutnätet och klicka på **[!UICONTROL Edit]** i kolumnen _[!UICONTROL Action]_.

1. Klicka på **[!UICONTROL Newsletter]** i den vänstra panelen.

1. Ändra prenumerationerna för kunden enligt inställningarna för er webbplats/butik.

   Du kan markera eller avmarkera kryssrutan **[!UICONTROL Subscribed to Newsletter]** för en enskild plats/enskild butik.

   ![Kryssruta för prenumeration på nyhetsbrev för kunder i en butik](./assets/newsletter-customer-single-store.png){width="500" zoomable="yes"}

   För en enstaka plats-/multibutiksinställning kan du markera eller avmarkera kryssrutan **[!UICONTROL Subscribed to Newsletter]** och ställa in **[!UICONTROL Subscribed on Store View]** på rätt butiksvy för prenumerationen.

   ![Prenumerationsruta för nyhetsbrev för flera butiker och visningsväljare för butiksvyn](./assets/newsletter-customer-multi-store.png){width="500" zoomable="yes"}

   Om du har en konfiguration för flera platser/flera butiker med ett globalt kundkonto visas prenumerationsstatusen för alla platser på sidan. Du kan markera eller avmarkera kryssrutan **[!UICONTROL Subscribed]** och/eller ändra **[!UICONTROL Store View]** för prenumerationen.

   ![Kryssrutor för prenumeration på nyhetsbrev för flera användare och butiksvyväljare](./assets/newsletter-customer-multi-site.png){width="500" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Customer]**.

## Avbryta en prenumeration från prenumerationslistan

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**på sidofältet_ Admin _.

   För en flersidig installation där vissa kunder har prenumerationer för mer än en webbplats visas varje prenumeration som en radobjekt i rutnätet.

1. Leta reda på prenumeranten i rutnätet och markera kryssrutan i den första kolumnen.

   >[!NOTE]
   >
   >Om du vill avbryta en satsvis prenumeration markerar du kryssrutan för varje prenumerant som du vill avbryta.

1. Ställ in kontrollen _[!UICONTROL Action]_på&#x200B;**[!UICONTROL Unsubscribe]**och klicka på&#x200B;**[!UICONTROL Submit]**.

   ![Avbeställ nyhetsbrev](./assets/newsletter-unsubscribe.png){width="600" zoomable="yes"}

   Postens status ändras till `Unsubscribed`.

## Exportera listan över prenumeranter

1. Använd filterkontrollerna i listan _[!UICONTROL Newsletter Subscribers]_för att endast inkludera poster med statusen_ _för `Subscribed` och för rätt webbplats-, butik- eller butiksvy.

1. Ställ in kontrollen **[!UICONTROL Export to]** på något av följande:

   - `CSV`
   - `XML`

1. Klicka på **[!UICONTROL Export]** och leta efter uppmaningen längst ned på skärmen och spara filen.

   ![Exportera prenumeranter på nyhetsbrev](./assets/newsletter-subscribers-export.png){width="600" zoomable="yes"}

## Ta bort en prenumerant från prenumerantlistan

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**på sidofältet_ Admin _.

1. Leta reda på prenumeranten i rutnätet och markera kryssrutan i den första kolumnen.

1. Ställ in kontrollen _[!UICONTROL Action]_på&#x200B;**[!UICONTROL Delete]**och klicka på&#x200B;**[!UICONTROL Submit]**.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.
