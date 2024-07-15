---
title: Sorteringsordning för utcheckningssummor
description: Lär dig mer om den totala utcheckningen och hur du konfigurerar sorteringsordningen för utcheckningssummor i ordersammanfattningen.
exl-id: 2b1345e3-6ad3-472a-af3e-3f7b24577b13
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Sorteringsordning för utcheckningssummor

Under ordergranskningen visas summan längst ned i ordern, med eventuella justeringar för rabatter, fraktkostnader, butikskrediter och moms. Ordningen för varje objekt avgör beräkningssekvensen och anges i konfigurationen med ett nummer som tilldelas varje objekt. Delsumman är till exempel det första objektet i avsnittet och tilldelas värdet 10. Summan visas sist och tilldelas värdet 100. Alla andra objekt i summeringsavsnittet tilldelas ett värde mellan dessa värden.

![Ordersammanfattning visar den totala utcheckningen](./assets/storefront-checkout-totals.png){width="700" zoomable="yes"}

**_Så här konfigurerar du sorteringsordningen för utcheckningssummor:_**

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera avsnittet **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Sales]** under.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Checkout Totals Sort Order]**.

   ![Utcheckningssummeringsalternativ numrerade för att bestämma sorteringsordningen](../configuration-reference/sales/assets/sales-checkout-totals-sort-order.png){width="600" zoomable="yes"}

   En detaljerad beskrivning av de här konfigurationsinställningarna finns i [Sorteringsordning för utcheckningssummor](../configuration-reference/sales/sales.md#checkout-totals-sort-order) i _referenshandboken för konfiguration_.

1. Om inställningen gäller för en viss butiksvy [väljer du den butiksvy](../configuration-reference/scope-change.md#set-the-scope) där konfigurationen gäller.

   Klicka på **[!UICONTROL OK]** när du uppmanas att fortsätta.

1. Om du vill ta reda på ordningen i avsnittet _Summor_ ändrar du numret som tilldelats varje objekt.

   Ju lägre värde, desto tidigare placering i listan. I standardkonfigurationen är delsumman (`10`) den första och totalsumman (`100`) den sista.

   Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för att slutföra ändringarna.

1. Klicka på **[!UICONTROL Save Config]**.
