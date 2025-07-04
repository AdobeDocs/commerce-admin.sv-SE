---
title: Kundsegment i prisregler
description: Lär dig hur du associerar kundsegment med en kundprisregel så att du kan definiera riktade kampanjer för din butik.
exl-id: eaa04e7a-c0f9-4f09-8e65-75965ccbdc69
feature: Customers, Configuration, Price Rules
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---

# Kundsegment i prisregler

{{ee-feature}}

Ett kundsegment kan användas för riktade kampanjer genom att associera det med en [kundprisregel](../merchandising-promotions/price-rules-cart.md).

![Kundprisregel - riktat kundsegment](assets/price-rule-cart-condition-segments.png){width="700" zoomable="yes"}

_&#x200B;**Så här associerar du ett segment med en kundprisregel:**&#x200B;_

1. Gå till **[!UICONTROL Marketing]** > _Kampanjer_ > **[!UICONTROL Cart Price Rules]** på sidofältet _Admin_.

1. Öppna en ny eller befintlig regel:

   * Om du vill använda en ny regel klickar du på **[!UICONTROL Add New Rule]** i det övre högra hörnet.
   * Om du vill använda en befintlig regel klickar du på regeln i listan för att öppna den i redigeringsläge.

1. Bläddra nedåt och expandera avsnittet **[!UICONTROL Conditions]**.

1. Lägg till villkoret.

   * Klicka på ikonen _Lägg till_ (![listikon](../assets/icon-add-green-circle.png)) som visar listan med villkor. Välj sedan **[!UICONTROL Customer Segment]**.

   ![Kundprisregel - lägg till kundsegmentvillkor](assets/condition-customer-segment.png){width="600" zoomable="yes"}

   Som standard är villkoret inställt på att söka efter ett matchande villkor. Om det behövs klickar du på länken **[!UICONTROL matches]** och ändrar operatorn till något av följande:

   * `does not match`
   * `is one of`
   * `is not one of`

   ![Villkorsoperator](assets/price-rule-condition-customer-segment-operator.png){width="600" zoomable="yes"}

1. Om du vill ange ett visst segment som mål klickar du på länken Mer **...** för att visa ytterligare alternativ. Klicka sedan på ikonen _Väljare_ (![Lista-ikon](../assets/icon-list-chooser.png)) för att visa listan över kundsegment.

1. I listan markerar du kryssrutan för varje segment som du vill använda som mål med villkoret.

   ![Kundprisregel - lista med villkorsväljare](assets/condition-segment-chooser-list.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Select]** för att placera de valda kundsegmenten i villkoret.

1. Slutför resten av prisregeln efter behov.

1. Klicka på **[!UICONTROL Save]** när du är klar.
