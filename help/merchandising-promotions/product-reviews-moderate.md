---
title: Moderera produktrecensioner
description: Lär dig hur du kan moderera produktrecensioner för att säkerställa att inlämnade recensioner passar för offentlig visning i din butik.
exl-id: 90c3e918-f435-4468-b41b-e8044ad14fb0
feature: Merchandising, Products
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Moderera produktrecensioner

För produktgranskningar i Commerce måste en inskickad produktrecension godkännas innan den kan visas. Detta garanterar att granskningarna är lämpliga för offentlig visning av din butik. En inskickad granskning är `Pending` status tills den har godkänts eller avvisats.

## Visa produktrecensioner i administratören

Så här visar du alla granskningar för en viss produkt i Admin:

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Hitta den produkt du vill visa och klicka på **[!UICONTROL Edit]** i _[!UICONTROL Action]_kolumn.

1. Bläddra nedåt och expandera på produktsidan ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Product Reviews]** -avsnitt.

   I det här rutnätet kan du även ändra den specifika granskningen genom att klicka på **[!UICONTROL Edit]** i _[!UICONTROL Action]_kolumn.

## Uppdatera status för granskningar

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL User Content]_>**[!UICONTROL Pending Reviews]**eller **[!UICONTROL All Reviews]**.

1. Klicka på en väntande granskning i listan för att visa informationen och redigera vid behov.

1. Ändra **[!UICONTROL Status]** enligt din bedömning:

   - Om du vill godkänna en pågående granskning väljer du `Approved`.

   - Om du vill avvisa en granskning väljer du `Not Approved`. Ej godkända granskningar tas bort från listan över _[!UICONTROL Pending Reviews]_sida.

   >[!NOTE]
   >
   >Recensioner med `Pending` och `Not Approved` statusvärden visas inte i butiken.

1. Ange **[!UICONTROL Visibility]** av en produktrecension som kan visas i olika butiksvyer.

1. Ändra vid behov värdena för **[!UICONTROL Detailed Rating]**, **[!UICONTROL Nickname]** och **[!UICONTROL Summary of Review]**.

   Om du vill ändra butiksvyn där en granskning är tillgänglig väljer du önskad butiksvy i _[!UICONTROL Visibility]_kolumn.

   ![Redigera granskningssida](./assets/edit-review-page.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Review]**.

## Batchuppdatering

Du kan uppdatera eller ta bort flera granskningar samtidigt:

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL User Content]_>**[!UICONTROL All Reviews]**.

1. Välj de granskningar som du vill uppdatera.

1. Använd _[!UICONTROL Action]_om du vill använda en åtgärd i det övre vänstra hörnet.

1. Klicka på **[!UICONTROL Submit]**

## Ta bort en produktgranskning

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL User Content]_>**[!UICONTROL All Reviews]**.

1. Hitta den produktgranskning som ska tas bort och öppna den i redigeringsläge.

1. Klicka på **[!UICONTROL Delete Review]** -knappen.

1. Bekräfta åtgärden genom att klicka **[!UICONTROL OK]**.

## Knappfält

| Knapp | Beskrivning |
|----------|--------------|
| **[!UICONTROL Back]** | Återgår till sidan Recensioner utan att spara ändringarna |
| **[!UICONTROL Delete Review]** | Tar bort granskningen |
| **[!UICONTROL Reset]** | Återställer alla osparade ändringar i granskningsformuläret till deras tidigare värden |
| **[!UICONTROL Previous]** | Öppnar föregående granskning |
| **[!UICONTROL Next]** | Öppnar nästa granskning |
| **[!UICONTROL Save and Previous]** | Sparar aktuella ändringar och öppnar den föregående granskningen. Den här knappen visas om det finns andra granskningar. |
| **[!UICONTROL Save and Next]** | Sparar de aktuella ändringarna och öppnar nästa vy. Den här knappen visas om det finns andra granskningar. |
| **[!UICONTROL Save Review]** | Sparar ändringar och stänger granskningssidan |
