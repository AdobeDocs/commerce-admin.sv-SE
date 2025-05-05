---
title: Ensidig utcheckning
description: Lär dig mer om hur man kan få en smidig utcheckningsprocess för din butik med en sida.
exl-id: c91347b6-bb6f-44e7-b470-f237bf430d5f
feature: Checkout
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# Ensidig utcheckning

Avsikten med en enkelsidig utcheckning är att samla in den information som behövs och slutföra försäljningen så snabbt som möjligt utan att kunden behöver klicka på något extra. När ensidig utcheckning är aktiverat utförs hela utcheckningsprocessen på en enda sida. Varje del av utcheckningsinformationen utökas efter behov.

Utcheckning av en sida är aktiverat som standard. Om du implementerar ett anpassat integrerings- eller utcheckningstillägg kan det vara nödvändigt att inaktivera enkelsidig utcheckning.

**_Så här inaktiverar du enkelsidig utcheckning:_**

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** på den vänstra panelen och välj **[!UICONTROL Checkout]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Checkout Options]**.

   ![Konfiguration - utcheckningsalternativ](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

   En detaljerad beskrivning av de här konfigurationsinställningarna finns i [Utcheckningsalternativ](../configuration-reference/sales/checkout.md#checkout-options) i _referenshandboken för konfiguration_.

1. Om inställningen gäller för en viss butiksvy [väljer du den butiksvy](../configuration-reference/scope-change.md#set-the-scope) där konfigurationen gäller.

   Klicka på **[!UICONTROL OK]** när du uppmanas att fortsätta.

1. Ange **[!UICONTROL Enable Onepage Checkout]** till `No`.

   Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för att ändra den här inställningen.

1. Klicka på **[!UICONTROL Save Config]**.
