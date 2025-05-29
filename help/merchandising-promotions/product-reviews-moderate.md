---
title: Moderera produktrecensioner
description: Lär dig hur du kan moderera produktrecensioner för att säkerställa att inlämnade recensioner passar för offentlig visning i din butik.
exl-id: 90c3e918-f435-4468-b41b-e8044ad14fb0
feature: Merchandising, Products
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# Moderera produktrecensioner

För Commerce produktrecensioner måste en inskickad produktrecension godkännas innan den kan visas. Detta garanterar att granskningarna är lämpliga för offentlig visning av din butik. En skickad granskning har statusen `Pending` tills den har godkänts eller avvisats.

## Visa produktrecensioner i administratören

Så här visar du alla granskningar för en viss produkt i Admin:

1. Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]** på sidofältet _Admin_.

1. Hitta den produkt du vill visa och klicka på **[!UICONTROL Edit]** i kolumnen _[!UICONTROL Action]_.

1. Bläddra nedåt och expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Product Reviews]** på produktsidan.

   I det här rutnätet kan du även ändra den specifika granskningen genom att klicka på länken **[!UICONTROL Edit]** i kolumnen _[!UICONTROL Action]_.

## Uppdatera status för granskningar

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL User Content]_>**[!UICONTROL Pending Reviews]**&#x200B;eller **[!UICONTROL All Reviews]**&#x200B;på sidofältet_ Admin _.

1. Klicka på en väntande granskning i listan för att visa informationen och redigera vid behov.

1. Ändra **[!UICONTROL Status]** enligt din bedömning:

   - Om du vill godkänna en väntande granskning väljer du `Approved`.

   - Om du vill avvisa en granskning väljer du `Not Approved`. Ej godkända granskningar tas bort från listan på sidan _[!UICONTROL Pending Reviews]_.

   >[!NOTE]
   >
   >Granskningar med statusvärdena `Pending` och `Not Approved` visas inte i butiken.

1. Om det är tillämpligt anger du **[!UICONTROL Visibility]** för en produktgranskning så att den visas i olika butiksvyer.

1. Ändra värdena för **[!UICONTROL Detailed Rating]**, **[!UICONTROL Nickname]** och **[!UICONTROL Summary of Review]** om det behövs.

   Om du vill ändra butiksvyn där en granskning är tillgänglig väljer du önskad butiksvy i kolumnen _[!UICONTROL Visibility]_.

   ![Redigera granskningssida](./assets/edit-review-page.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Review]** när du är klar.

## Batchuppdatering

Du kan uppdatera eller ta bort flera granskningar samtidigt:

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL User Content]_>**[!UICONTROL All Reviews]**&#x200B;på sidofältet_ Admin _.

1. Välj de granskningar som du vill uppdatera.

1. Använd _[!UICONTROL Action]_-väljaren i det övre vänstra hörnet för att tillämpa en åtgärd.

1. Klicka på **[!UICONTROL Submit]**

## Ta bort en produktgranskning

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL User Content]_>**[!UICONTROL All Reviews]**&#x200B;på sidofältet_ Admin _.

1. Hitta den produktgranskning som ska tas bort och öppna den i redigeringsläge.

1. Klicka på knappen **[!UICONTROL Delete Review]** på menyraden.

1. Bekräfta åtgärden genom att klicka på **[!UICONTROL OK]**.

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
