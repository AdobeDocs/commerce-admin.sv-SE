---
title: Schemalägg en innehållsuppdatering
description: Granska det här kampanjexemplet som används för att schemalägga en tillfällig prisändring för en produkt.
exl-id: 36b7d7f6-4590-4192-a82b-e5f645b05f62
feature: Page Content, Staging
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 07d7ca7e7f6af42fe8e06dc3c49c2df5f50d1425
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 0%

---

# Schemalägg en innehållsuppdatering

{{ee-feature}}

I följande exempel visas hur du schemalägger en tillfällig prisändring för en produkt. Det inkluderar schemaläggning och förhandsgranskning av ändringar samt visning av schemalagda uppdateringar i kalendern. Även om det här exemplet bara innehåller en enda ändring, kan en kampanj innehålla flera ändringar av produkter, prisregler, CMS-sidor och andra enheter som är schemalagda att äga rum samtidigt. Följ en liknande metod för att ange från-/till-datum för attributet [!UICONTROL Set Product As New].

>[!NOTE]
>Du måste skapa en schemalagd uppdatering för att ange start- (och slutdatum) för [!UICONTROL Set Product As New]. För [!UICONTROL Special Price] och [!UICONTROL Design Change] tas datumfälten från/till bort från Adobe Commerce och är endast tillgängliga i Magento Open Source.
>
>Alla schemalagda uppdateringar tillämpas i följd, vilket innebär att alla enheter bara kan ha en schemalagd uppdatering åt gången. Alla schemalagda uppdateringar tillämpas på alla butiksvyer inom tidsramen. Därför kan en enhet inte ha en annan schemalagd uppdatering för olika butiksvyer samtidigt. Alla värden för entitetsattribut i alla butiksvyer, som inte påverkas av den aktuella schemalagda uppdateringen, hämtas från standardvärdena och inte från den tidigare schemalagda uppdateringen.

## Schemalägg en uppdatering för en produkt

1. Öppna en produkt i redigeringsläge från stödrastret _[!UICONTROL Products]_.

1. Klicka på **[!UICONTROL Schedule New Update]** i rutan _[!UICONTROL Scheduled Changes]_överst på sidan.

   ![Schemalägg ny uppdatering](./assets/content-staging-product-schedule-new-update.png){width="600" zoomable="yes"}

1. Med alternativet **[!UICONTROL Save as a New Update]** markerat anger du de grundläggande parametrarna för uppdateringen:

   - Ange ett namn för den nya innehållstagningskampanjen för **[!UICONTROL Update Name]**.

   - Ange en kort **[!UICONTROL Description]** av uppdateringen och hur den ska användas.

   - Använd kalenderverktyget (![kalenderikonen](../assets/icon-calendar.png)) för att välja kampanjens **startdatum** och **slutdatum**.

     Om du vill skapa en öppen kampanj ska du inte ange något slutdatum (lämna tomt). I det här exemplet ska kampanjen börja vid midnatt för det nya året, 1 januari 2021 kl. 12.00 PST.


     För en prisregelkampanj som har skapats utan ett slutdatum kan ett slutdatum inte läggas till senare. I så fall måste du skapa en kampanj och ange startdatumet till det datum då du vill att den gamla kampanjen ska sluta och den nya ska börja. På det startdatumet upphör den gamla kampanjen och den nya kampanjen börjar som den är definierad.

     ![Planerar en produktuppdatering](./assets/content-staging-campaign-schedule-update.png){width="600" zoomable="yes"}

     >[!NOTE]
     >
     >Kampanjens startdatum och slutdatum måste definieras med hjälp av administratörstidszonen **_default_** som konverteras från den lokala tidszonen på varje webbplats. Om du till exempel har flera webbplatser i olika tidszoner, men vill starta en kampanj som baseras på en amerikansk (standard) tidszon, måste du schemalägga en separat uppdatering för varje lokal tidszon. I det här fallet anger du **[!UICONTROL Start Date]** och **[!UICONTROL End Date]** som konverterade från alla lokala webbplatsers tidszon till administratörens standardtidszon.

1. Bläddra ned till _[!UICONTROL Price]_och klicka på&#x200B;**[!UICONTROL Advanced Pricing]**.

1. Ange **[!UICONTROL Special Price]** för produkten under den schemalagda kampanjen och klicka på **[!UICONTROL Done]**.

1. Klicka på **[!UICONTROL Save]** när du är klar.

   Den schemalagda ändringen visas högst upp på produktsidan med kampanjens start- och slutdatum.

   ![Schemalagd ändring](./assets/content-staging-product-scheduled-update-preview-rope.png){width="600" zoomable="yes"}

## Redigera den schemalagda ändringen

1. Klicka på **[!UICONTROL View/Edit]** i rutan _Schemalagda ändringar_ längst upp på sidan.

1. Gör de ändringar som behövs för den schemalagda uppdateringen.

1. Klicka på **[!UICONTROL Save]**.

## Förhandsgranska den schemalagda ändringen

Klicka på **[!UICONTROL Preview]** i rutan _Schemalagda ändringar_ längst upp på sidan.

Förhandsgranskningen öppnar en ny flik i webbläsaren och visar hur produkten visas under den schemalagda kampanjen.

>[!NOTE]
>
>En mellanlagringsförhandsvisning för en schemalagd uppdatering startar alltid från butiksvyn **default** som emulerar kundens upplevelse av att navigera genom mellanlagringsuppdateringskampanjen.

Mer information om hur du använder verktygen för förhandsgranskning av innehåll för att ändra datumet och omfattningen för förhandsgranskningen finns i [Förhandsgranska en kampanj](content-staging-preview.md). Du kan även dela en länk till butiksförhandsgranskningen med dina kollegor.
