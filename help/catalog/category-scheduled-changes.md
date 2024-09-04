---
title: Schemalagda ändringar för kategorier
description: Lär dig schemalägga kategoriändringar för att stödja marknadsföringskampanjer och butikskampanjer.
exl-id: 9e25082f-4e76-4148-b76e-dca0b14971eb
feature: Catalog Management, Categories
source-git-commit: 74cc26e74c3efabc914c27b6d8327a85a77fd6e6
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# Schemalagda ändringar för kategorier

{{ee-feature}}

Kategoriuppdateringar kan tillämpas enligt schema och grupperas med andra innehållsändringar. Du kan skapa en kampanj baserat på schemalagda ändringar av kategorin eller tillämpa ändringarna på en befintlig kampanj. Mer information finns i [Innehållsfördelning](../content-design/content-staging.md).

>[!NOTE]
>
>Fliken [!UICONTROL Schedule Design Update] har tagits bort i ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce och kan inte ändras direkt i kategorin. Du måste skapa en schemalagd uppdatering för dessa aktiveringar.

>[!NOTE]
>
>Alla schemalagda uppdateringar tillämpas i följd, vilket innebär att alla enheter bara kan ha en schemalagd uppdatering åt gången. Alla schemalagda uppdateringar tillämpas på alla butiksvyer inom tidsramen. Därför kan en enhet inte ha flera schemalagda uppdateringar för olika butiksvyer samtidigt. Alla värden för entitetsattribut i alla butiksvyer, som inte påverkas av den aktuella schemalagda uppdateringen, hämtas från standardvärdena och inte från den tidigare schemalagda uppdateringen.

## Schemalägg en uppdatering av en kategori

1. Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Categories]** på sidofältet _Admin_.

1. Välj den kategori som ska ändras i kategoriträdet till vänster.

1. Klicka på **[!UICONTROL Schedule New Update]** i rutan _Schemalagda ändringar_ längst upp på sidan.

   ![Schemalagda ändringar](./assets/category-scheduled-changes.png){width="600" zoomable="yes"}

1. Med alternativet **[!UICONTROL Save as a New Update]** markerat anger du de grundläggande parametrarna för uppdateringen:

   - Ange ett namn för den nya innehållstagningskampanjen för **[!UICONTROL Update Name]**.

   - Ange en kort **[!UICONTROL Description]** av uppdateringen och hur den ska användas.

   - Använd kalenderverktyget ( ![kalenderikonen](../assets/icon-calendar.png) ) för att välja **[!UICONTROL Start Date]** och **[!UICONTROL End Date]** för kampanjen.

   >[!IMPORTANT]
   >
   >Kampanjen **[!UICONTROL Start Date]** och **[!UICONTROL End Date]** måste definieras med hjälp av administratörstidszonen **_default_** som konverteras från den lokala tidszonen på varje webbplats. Om du till exempel har flera webbplatser i olika tidszoner där du vill starta en kampanj som baseras på en tidszon i USA måste du schemalägga en separat uppdatering för varje lokal tidszon. Du ställer in **[!UICONTROL Start Date]** och **[!UICONTROL End Date]** för varje, som konverteras från den lokala webbplatsens tidszon till administratörens standardtidszon.

   ![Schemalagda ändringar](./assets/category-scheduled-changes-new-update.png){width="600" zoomable="yes"}

1. Gör de ändringar som behövs för den schemalagda uppdateringen.

1. Om du vill förhandsgranska ändringarna klickar du på **[!UICONTROL Preview]** i det övre högra knappfältet.

1. Klicka på **[!UICONTROL Save]** när du är klar.

## Tilldela till en befintlig uppdatering

1. Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Categories]** på sidofältet _Admin_.

1. Välj den kategori som ska ändras i kategoriträdet till vänster.

1. Klicka på **[!UICONTROL Schedule New Update]** i rutan _Schemalagda ändringar_ längst upp på sidan.

1. Välj **[!UICONTROL Assign to Existing Campaign]**.

1. Leta reda på den kampanj som behövs i listan och klicka på **[!UICONTROL Select]**.

1. Gör de ändringar som krävs i den schemalagda uppdateringen.

1. Klicka på **[!UICONTROL Save]** när du är klar.

   >[!NOTE]
   >
   >Om en kampanj är länkad till mer än en kategori kan kampanjen bara redigeras från [instrumentpanelen för innehållsindelning](../content-design/content-staging-dashboard.md).