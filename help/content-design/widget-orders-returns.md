---
title: Widgeten Beställningar och returer
description: Lär dig hur du använder widgeten för beställningar och returer för att ge kunderna möjlighet att kontrollera status för sina beställningar, skriva ut fakturor och spåra leveranser.
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---

# Widgeten Beställningar och returer

Widgeten _Beställningar och Returer_ ger gästerna möjlighet att kontrollera status för sina beställningar, skriva ut fakturor och spåra leveranser. När widgeten läggs till i butiken visas den bara för gäster och för kunder som inte är inloggade på sina konton. Gäster kan hitta beställningar genom att ange beställnings-ID, efternamn för fakturering och antingen e-postadress eller postnummer.

![Widgeten Beställningar och Returer i sidofältet på butiken](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## Widgeten för order och returer i butiken

1. Kunden kan använda alternativet **[!UICONTROL Find Order By]** för att välja en av följande parametrar som ska användas för att hitta ordern:

   - E-postadress
   - Postnummer

1. Kunden anger **[!UICONTROL Order ID]** och **[!UICONTROL Billing Last Name]**.

1. Anger antingen faktureringen **[!UICONTROL Email Address]** eller **[!UICONTROL ZIP Code]** som är associerad med ordern.

1. Klicka på **[!UICONTROL Search]** för att hämta ordern.

   ![Beställningsinformation visas i butiken](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## Ställa in widgeten för beställningar och returer

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add Widget]** i det övre högra hörnet.

1. Gör följande i avsnittet _[!UICONTROL Settings]_:

   - Ange **[!UICONTROL Type]** till `Orders and Returns`.

   - Välj den **[!UICONTROL Design Theme]** som används av butiken.

1. Klicka på **[!UICONTROL Continue]**.

1. Gör följande i avsnittet _[!UICONTROL Storefront Properties]_:

   - För **[!UICONTROL Widget Title]** anger du en beskrivande titel för widgeten.

     Den här titeln visas bara från administratören.

   - För **[!UICONTROL Assign to Store Views]** väljer du de butiksvyer där widgeten visas.

     Du kan välja en viss butiksvy eller `All Store Views`. Om du vill markera flera vyer håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

   - (Valfritt) Ange ett nummer för **[!UICONTROL Sort Order]** för att avgöra i vilken ordning det här objektet visas med andra på samma del av sidan. (`0` = först, `1` = sekund, `3` = tredje o.s.v.)

1. Klicka på **[!UICONTROL Add Layout Update]** i avsnittet _[!UICONTROL Layout Updates]_&#x200B;och gör följande:

   - Ange **[!UICONTROL Display On]** till den typ av sida där du vill att widgeten ska visas.

   - Om du vill bestämma var widgeten ska visas på sidan, fyller du i resten av layoutuppdateringsinformationen.

1. Klicka på **[!UICONTROL Save]** när du är klar.

1. När du uppmanas att uppdatera cacheminnet klickar du på länken i meddelandet längst upp på sidan och följer instruktionerna.
