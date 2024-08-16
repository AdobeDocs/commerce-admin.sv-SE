---
title: Attributuppsättningar
description: Lär dig hur du organiserar attribut i grupper, som bestämmer var de visas i produktposten.
exl-id: de0c5fa2-158c-44ff-b84d-e4904ed8aa7d
feature: Catalog Management, Products
source-git-commit: 43550b9370f4ed4b631ae7773324ed0913718a79
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Attributuppsättningar

Ett av de första stegen när du skapar en produkt är att välja den attributuppsättning som används som mall för produktposten. Attributuppsättningen avgör vilka fält som är tillgängliga under datainmatningen och vilka värden som visas för kunden.

Attributen är ordnade i grupper som bestämmer var de visas i produktposten. Butiken innehåller en inledande attributuppsättning (som kallas _standard_) som innehåller en uppsättning vanliga attribut. Om du bara vill lägga till ett fåtal attribut kan du lägga till dem i den här standardattributuppsättningen. Om du säljer produkter som kräver viss typ av information kan det vara bättre att skapa en dedikerad attributuppsättning som innehåller de specifika attribut som krävs för produkten.

![Attributuppsättningar](./assets/attribute-sets.png){width="700" zoomable="yes"}

## Skapa en attributuppsättning

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add New Set]**.

   ![Attributuppsättning - redigera namn](./assets/attribute-set-new.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Name]** som attributuppsättning.

1. Ange **[!UICONTROL Based On]** som en befintlig attributuppsättning som ska användas som mall.

1. Klicka på **[!UICONTROL Save]**.

   På nästa sida visas följande:

   - I den vänstra kolumnen visas namnet på attributuppsättningen. Namnet används som intern referens och kan ändras vid behov.
   - Mitten av sidan visar det aktuella urvalet av attributgrupper.
   - I den högra kolumnen visas de attribut som för närvarande inte är tilldelade till attributuppsättningen.

1. Om du vill lägga till ett attribut i uppsättningen drar du attributet från listan **[!UICONTROL Unassigned Attributes]** till rätt mapp i kolumnen **[!UICONTROL Groups]**. Om du vill ta bort ett attribut från uppsättningen drar du det till listan **[!UICONTROL Unassigned Attributes]**.

   >[!NOTE]
   >
   >Systemattribut är markerade med en punkt och kan inte tas bort från listan _[!UICONTROL Groups]_. De kan dock dras till en annan grupp i attributuppsättningen.

1. Klicka på **[!UICONTROL Save]** när du är klar.

![Attributuppsättning - redigera](./assets/attribute-set-edit.png){width="600" zoomable="yes"}

## Skapa en attributgrupp

1. Klicka på **[!UICONTROL Add New]** i kolumnen _[!UICONTROL Groups]_i attributuppsättningen.

1. Ange en **[!UICONTROL Name]** för den nya gruppen och klicka på **[!UICONTROL OK]**.

1. Gör något av följande:

   - Dra **[!UICONTROL Unassigned Attributes]** till den nya gruppen.
   - Dra attribut från en annan grupp till den nya gruppen.
   - Dra onödiga attribut till **[!UICONTROL Unassigned Attributes]**.

   Den nya gruppen blir en del av attribut i en produkt som är baserad på attributuppsättningen.

## Ta bort en attributuppsättning

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**på sidofältet_ Admin _.

1. Markera attributuppsättningen i listan och öppna i redigeringsläge.

1. Klicka på **[!UICONTROL Delete]**.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.
