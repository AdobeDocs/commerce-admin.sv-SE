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

Du kan enkelt hantera dina prenumeranter med en enkel lista över aktiva prenumerationer. När en kund skickar in en begäran om att avbryta prenumerationen behöver du bara lägga in en _Avbeställ_ till en eller flera valda prenumerationer.

I uppsättningar för en enda plats med flera butiksvyer kan ett kundkonto kopplas till en viss butiksvy.

I flerbutiks- och flerplatskonfigurationer med en global [kundkontoomfång](../customers/customer-account-scope.md)kan ett kundkonto prenumerera på nyhetsbrev för flera webbplatser/butiker. I det här fallet kanske du vill redigera kundkontot för att hantera en grupp prenumerationer eller avbryta en prenumeration för en viss webbplats/butik för att efterleva en begäran.

Om du vill använda en tredjepartstjänst för att skicka nyhetsbrev kan du exportera din prenumerationslista som en CSV- eller XML-fil.

## Hantera prenumerationer för en kund

1. På _Administratör_ sidebar, gå till **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Hitta kunden i rutnätet och klicka **[!UICONTROL Edit]** i _[!UICONTROL Action]_kolumn.

1. Klicka **[!UICONTROL Newsletter]** till vänster.

1. Ändra prenumerationerna för kunden enligt inställningarna för er webbplats/butik.

   Om du har en enstaka plats eller butik kan du välja eller rensa **[!UICONTROL Subscribed to Newsletter]** kryssrutan.

   ![Kryssruta för prenumeration på nyhetsbrev för enskilda butikskunder](./assets/newsletter-customer-single-store.png){width="500" zoomable="yes"}

   För en enstaka plats/flera butiker kan du välja eller rensa **[!UICONTROL Subscribed to Newsletter]** kryssruta och ange **[!UICONTROL Subscribed on Store View]** till rätt butiksvy för prenumerationen.

   ![Kryssruta för prenumeration på nyhetsbrev för flera butiker och butiksvyväljare](./assets/newsletter-customer-multi-store.png){width="500" zoomable="yes"}

   Om du har en konfiguration för flera platser/flera butiker med ett globalt kundkonto visas prenumerationsstatusen för alla platser på sidan. Du kan markera eller rensa **[!UICONTROL Subscribed]** och/eller ändra **[!UICONTROL Store View]** för prenumerationen.

   ![Kryssrutor för prenumeration på nyhetsbrev för flera användare och butiksvyväljare](./assets/newsletter-customer-multi-site.png){width="500" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Customer]**.

## Avbryta en prenumeration från prenumerationslistan

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

   För en flersidig installation där vissa kunder har prenumerationer för mer än en webbplats visas varje prenumeration som en radobjekt i rutnätet.

1. Leta reda på prenumeranten i rutnätet och markera kryssrutan i den första kolumnen.

   >[!NOTE]
   >
   >Om du vill avbryta en satsvis prenumeration markerar du kryssrutan för varje prenumerant som du vill avbryta.

1. Ange _[!UICONTROL Action]_styra till **[!UICONTROL Unsubscribe]**och klicka **[!UICONTROL Submit]**.

   ![Avbeställ nyhetsbrev](./assets/newsletter-unsubscribe.png){width="600" zoomable="yes"}

   Postens status ändras till `Unsubscribed`.

## Exportera listan över prenumeranter

1. Från _[!UICONTROL Newsletter Subscribers]_använder du filterkontrollerna för att inkludera endast poster med_ Status _av `Subscribed` och för rätt webbplats, butik eller butiksvy.

1. Ange **[!UICONTROL Export to]** kontrollera något av följande:

   - `CSV`
   - `XML`

1. Klicka **[!UICONTROL Export]** och leta efter uppmaningen längst ned på skärmen och spara filen.

   ![Exportera prenumeranter på nyhetsbrev](./assets/newsletter-subscribers-export.png){width="600" zoomable="yes"}

## Ta bort en prenumerant från prenumerantlistan

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**.

1. Leta reda på prenumeranten i rutnätet och markera kryssrutan i den första kolumnen.

1. Ange _[!UICONTROL Action]_styra till **[!UICONTROL Delete]**och klicka **[!UICONTROL Submit]**.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.
