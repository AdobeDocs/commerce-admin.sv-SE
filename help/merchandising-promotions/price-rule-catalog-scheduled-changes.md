---
title: Schemalagda ändringar av katalogens prisregler
description: Lär dig hur du tillämpar katalogprisregler i schemat som en del av en kampanj och grupperar dem med andra innehållsändringar.
exl-id: ec4b915f-0a27-438d-b1b0-f1bcd297af6d
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 11f8fcba70491f9dcb6c20d14b406fba4b14cab4
workflow-type: tm+mt
source-wordcount: '832'
ht-degree: 0%

---

# Schemalagda ändringar av katalogens prisregler

{{ee-feature}}

Rutan Schemalagda ändringar visas högst upp på sidan när en ny prisregel sparas eller uppdateras. Katalogens prisregler kan tillämpas på schemat som en del av en kampanj och grupperas med andra innehållsändringar. Du kan skapa en kampanj baserat på schemalagda ändringar av en prisregel eller tillämpa ändringarna på en befintlig kampanj.

>[!NOTE]
>
>Fälten [!UICONTROL From] och [!UICONTROL To] har tagits bort i ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce och kan inte ändras direkt i katalogprisregeln. Du måste skapa en schemalagd uppdatering för dessa aktiveringar.

>[!NOTE]
>
>Alla schemalagda uppdateringar tillämpas i följd. Det innebär att en enhet bara kan ha en schemalagd uppdatering vid ett tillfälle. Alla schemalagda uppdateringar tillämpas på alla butiksvyer inom tidsramen. Därför kan en enhet inte ha olika schemalagda uppdateringar för olika butiksvyer samtidigt. Alla värden för entitetsattribut i alla butiksvyer, som inte påverkas av den aktuella schemalagda uppdateringen, hämtas från standardvärdena och inte från den tidigare schemalagda uppdateringen.

Om det finns flera prisregler som körs i samma kampanj avgör inställningen Prioritet för prisregeln vilken regel som har företräde. Mer information finns i [Innehållsfördelning](../content-design/content-staging.md).

>[!IMPORTANT]
>
>Om en aktiv kampanj initialt skapas utan ett slutdatum kan kampanjen inte redigeras senare så att den innehåller ett slutdatum. I så fall är det nödvändigt att skapa en dubblettkampanj och ange det slutdatum som behövs.

![Katalogprisregel - schemalagda ändringar](./assets/price-rule-catalog-scheduled.png){width="600" zoomable="yes"}

## Schemalägg en uppdatering av en katalogprisregel

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**Katalogprisregel**på sidofältet_ Admin _.

1. Öppna regeln i redigeringsläge.

1. Klicka på **[!UICONTROL Schedule New Update]** i rutan **[!UICONTROL Scheduled Changes]** överst på sidan.

1. Markera alternativet **[!UICONTROL Save as a New Update]** och gör följande:

   - Ange ett namn för uppdateringen av regeln för **[!UICONTROL Update Name]**.

   - Ange en kort beskrivning **[!UICONTROL Description]** av uppdateringen, inklusive hur eller varför den tillämpas.

   - Använd _kalendern_ (![kalenderikonen](../assets/icon-calendar.png)) för att välja **[!DNL Start Date]** och **[!UICONTROL End Date]** för att den schemalagda ändringen ska gälla. Om du vill skapa en öppen ändring lämnar du slutdatumet tomt.

   ![Katalogprisregler - nya schemalagda ändringar](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Startdatumet och slutdatumet/sluttiden bestäms av administratörspanelens standarddatum/tid- och tidszon, inte av tidszonen för en viss webbplats. Tänk på webbplatsens tidszon för att fastställa start- och sluttider. Skapa separata regler för webbplatser i olika tidszoner som behöver starta och/eller stoppa vid specifika lokala tidpunkter.

1. Bläddra ned till avsnittet **[!UICONTROL Rule Information]** och ändra regeln efter behov.

   Du kan schemalägga ändringar för alla regelparametrar, inklusive webbplatser (omfång)/kundgrupper för regeln, regelvillkoren och de åtgärder som regeln tillämpar. Mer information finns i [Skapa en katalogprisregel](price-rules-catalog-create.md).

   >[!NOTE]
   >
   >Om du ändrar till någon av regelinformationsparametrarna kontrollerar du att _[!UICONTROL Status]_är korrekt inställd. Om du vill att ändringen ska resultera i en aktivt tillämpad regel ska statusen vara `Active`.

1. Klicka på **[!UICONTROL Save]** när du är klar.

   Den schemalagda ändringen visas överst på sidan med kampanjens start- och slutdatum.

## Redigera en schemalagd regeländring

1. Klicka på **[!UICONTROL View/Edit]** i rutan **[!UICONTROL Scheduled Changes]** överst på sidan.

1. Gör de ändringar som behövs för den schemalagda uppdateringen.

   >[!NOTE]
   >
   >Om en kampanj är länkad till mer än en katalogprisregel kan kampanjen bara redigeras från [instrumentpanelen för innehållsmellanlagring](../content-design/content-staging-dashboard.md).

1. Klicka på **[!UICONTROL Save]**.

## Förhandsgranska den schemalagda regeländringen

1. Klicka på **[!UICONTROL Preview]** i rutan **[!UICONTROL Scheduled Changes]** överst på sidan.

   Förhandsgranskningen öppnar en ny webbläsarflik som läser in butiken med den tillämpade schemalagda ändringen. Navigera till en produkt som påverkas av ändringen.

   ![Förhandsgranska schemalagd ändring](./assets/price-rule-catalog-scheduled-update-preview.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Calendar]** i det övre vänstra hörnet i förhandsgranskningsfönstret.

   Kalenderinformationen visar andra kampanjer som är schemalagda för samma dag. Varje post i listan är en separat regeluppdatering.

   ![Lista över schemalagda uppdateringar för ett specifikt datum](./assets/price-rule-catalog-scheduled-preview-calendar.png){width="600" zoomable="yes"}

1. Om du vill förhandsgranska en annan dag eller tid klickar du på **[!UICONTROL Date & Time]**-kalenderns ![kalenderikon](../assets/icon-calendar.png) och gör följande:

   - Välj ett annat datum och/eller en annan tid.

   - Klicka på **[!UICONTROL Preview]**.

1. Om du vill återgå till kalendern klickar du på **[!UICONTROL Calendar]** i sidhuvudet på sidan Förhandsgranska.

   Härifrån kan du göra följande:

   **Dela en länk till förhandsgranskningen**

   Klicka på **[!UICONTROL Share]** om du vill dela en länk till butiksförhandsgranskningen med dina kollegor. Kopiera länken till Urklipp och klistra in den i brödtexten i ett e-postmeddelande.

   >[!NOTE]
   >
   >Ett administratörsanvändarkonto krävs för att se en delad förhandsgranskning. Om din [roll har åtkomst](../systems/permissions-user-roles.md) för att skapa ett administratörsanvändarkonto måste du skapa kontot för en ny användare innan du kan dela.

   **Ändra omfattningen för förhandsgranskningen**

   Om du vill visa schemalagda ändringar för olika butiksvyer klickar du på **[!UICONTROL Scope]** i sidhuvudet på sidan Förhandsgranska. Välj den webbplats-, butik- eller butiksvy som du vill förhandsgranska.

1. Om det behövs går du tillbaka till kalendern och klickar på **[!UICONTROL View/Edit]** i kolumnen _[!UICONTROL Action]_för att öppna en annan schemalagd uppdatering.
