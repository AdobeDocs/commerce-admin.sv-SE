---
title: Schemalagda produktuppdateringar
description: Lär dig schemalägga ändringar i produktlistor för supportkampanjer och kampanjprogram.
exl-id: ce1aebe6-9032-438d-b950-4b13116b8ed3
feature: Catalog Management, Products
source-git-commit: 1e809696ee6d623d162226628329ed53e8f71511
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%

---

# Schemalägg produktuppdateringar

{{ee-feature}}

Produktuppdateringar kan tillämpas enligt schema och grupperas med andra innehållsändringar. Du kan använda [innehållstagning](../content-design/content-staging.md) för att skapa en kampanj baserat på planerade ändringar av produkten eller tillämpa ändringarna på en befintlig kampanj.

>[!NOTE]
>
>Alla schemalagda uppdateringar tillämpas i följd, vilket innebär att alla enheter bara kan ha en schemalagd uppdatering åt gången. Alla schemalagda uppdateringar tillämpas på alla butiksvyer inom tidsramen. Därför kan en enhet inte ha olika schemalagda uppdateringar för olika butiksvyer samtidigt. Alla värden för entitetsattribut i alla butiksvyer, som inte påverkas av den aktuella schemalagda uppdateringen, hämtas från standardvärdena och inte från den tidigare schemalagda uppdateringen.

>[!NOTE]
>
>En mellanlagringsförhandsvisning för en schemalagd uppdatering startar alltid från **standard** butiksvy, som emulerar kundens upplevelse av att navigera genom kampanjen för mellanlagringsuppdatering.

## Skapa en schemalagd uppdatering

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Välj en befintlig produkt och klicka på **[!UICONTROL Edit]**.

1. Klicka på **[!UICONTROL Schedule New Update]**.

1. Välj **[!UICONTROL Save as a New Update]**.

1. För **[!UICONTROL Update Name]** anger du ett namn för den nya innehållstagningskampanjen.

1. Ange en kort beskrivning **[!UICONTROL Description]** av uppdateringen och hur den ska användas.

1. Använd kalendern (![kalenderikon](../assets/icon-calendar.png)) för att välja **[!UICONTROL Start Date]** och **[!UICONTROL End Date]** för kampanjen.

   >[!NOTE]
   >
   >Campaign **[!UICONTROL Start Date]** och **[!UICONTROL End Date]** måste definieras med hjälp av **_standard_** Administratörens tidszon, som konverteras från den lokala tidszonen för varje webbplats. Om du till exempel har flera webbplatser i olika tidszoner där du vill starta en kampanj som baseras på en tidszon i USA måste du schemalägga en separat uppdatering för varje lokal tidszon. Ange **[!UICONTROL Start Date]** och **[!UICONTROL End Date]** för varje, och konverteras från den lokala webbplatsens tidszon till administratörens standardtidszon.

   ![Schemalägg som ny uppdatering](./assets/product-schedule-as-new.png){width="600" zoomable="yes"}

1. Bläddra nedåt till _[!UICONTROL Price]_och klicka **[!UICONTROL Advanced Pricing]**.

1. Ange en **[!UICONTROL Special Price]** för produkten under den schemalagda kampanjen och klicka **[!UICONTROL Done]**.

1. När du är klar klickar du på **[!UICONTROL Save]**.

## Tilldela till befintlig uppdatering

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Välj en befintlig produkt och klicka på **[!UICONTROL Edit]**.

1. Klicka på **[!UICONTROL Schedule New Update]**.

1. Välj **[!UICONTROL Assign to Existing Campaign]**.

1. Välj den kampanj som ska ändras i listan.

   ![Tilldela till en befintlig kampanj](./assets/scheduled-changes-assign-to-existing-campaign.png){width="600" zoomable="yes"}

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

1. När du är klar klickar du på **[!UICONTROL Save]**.

## Visa den schemalagda ändringen

Den schemalagda ändringen visas högst upp på produktsidan med kampanjens start- och slutdatum.

![Schemalagd ändring](./assets/view-product-scheduled-changes.png){width="600" zoomable="yes"}

## Redigera den schemalagda ändringen

1. I _[!UICONTROL Scheduled Changes]_överst på sidan klickar du på&#x200B;**[!UICONTROL View/Edit]**.

1. Gör de ändringar som behövs för den schemalagda uppdateringen.

1. Klicka på **[!UICONTROL Save]**.

## Ta bort den schemalagda ändringen

1. I _[!UICONTROL Scheduled Changes]_överst på sidan klickar du på&#x200B;**[!UICONTROL View/Edit]**.

1. Klicka på i det övre fältet **[!UICONTROL Remove from Update]**.

   ![Ta bort schemalagd ändring](./assets/remove-product-scheduled-changes.png){width="600" zoomable="yes"}

1. I dialogrutan väljer du **[!UICONTROL Delete the Update]** och klicka **[!UICONTROL Done]**.

   >[!NOTE]
   >
   >Produkten tas bort från uppdateringen och alla schemalagda ändringar går förlorade.

## Schemalägg en designuppdatering

{{ce-feature}}

The _[!UICONTROL Schedule Design Update]_ger dig möjlighet att göra tillfälliga ändringar av utseendet på produktsidan. Du kan schemalägga designändringar för en säsong, en befordran eller bara för att göra saker och ting fräscha. Designändringar kan schemaläggas i förväg så att de träder i kraft, eller_ droppa _, enligt angivet schema.

![Schemalagd designuppdatering](./assets/product-design-update-scheduled-ce.png){width="600" zoomable="yes"}


| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | Anger datumintervallet när en anpassad layout används på produkten. |
| [!UICONTROL New Theme] | Använder ett anpassat tema för produkten. |
| [!UICONTROL New Layout] | Använder en annan layout på produktsidan. Alternativ: <br/>**[!UICONTROL No layout updates]**- Som standard är layoutuppdateringar inte tillgängliga för produktsidan.<br/>**[!UICONTROL Empty]** - Här kan du definiera en egen layout, t.ex. en sida med fyra kolumner. (Kräver förståelse för XML.) <br/>**[!UICONTROL 1 column]**- Använder en layout med en kolumn på produktsidan.<br/>**[!UICONTROL 2 columns with left bar]** - En layout med två kolumner och vänster sidospalt används på produktsidan. <br/>**[!UICONTROL 2 columns with right bar]**- Använder en layout med två kolumner och höger sidospalt på produktsidan.<br/>**[!UICONTROL 3 columns]** - Använder en layout med tre kolumner på produktsidan. |

{style="table-layout:auto"}
