---
title: Attributuppsättningar
description: Lär dig hur du organiserar attribut i grupper, som bestämmer var de visas i produktposten.
exl-id: de0c5fa2-158c-44ff-b84d-e4904ed8aa7d
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# Attributuppsättningar

Ett av de första stegen när du skapar en produkt är att välja den attributuppsättning som används som mall för produktposten. Attributuppsättningen avgör vilka fält som är tillgängliga under datainmatningen och vilka värden som visas för kunden.

Attributen är ordnade i grupper som bestämmer var de visas i produktposten. Butiken levereras med en inledande attributuppsättning (som kallas _standard_) som innehåller en uppsättning vanliga attribut. Om du bara vill lägga till ett fåtal attribut kan du lägga till dem i den här standardattributuppsättningen. Om du säljer produkter som kräver viss typ av information kan det vara bättre att skapa en dedikerad attributuppsättning som innehåller de specifika attribut som krävs för produkten.

![Attributuppsättningar](./assets/attribute-sets.png){width="700" zoomable="yes"}

## Skapa en attributuppsättning

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Klicka på **[!UICONTROL Add New Set]**.

   ![Attributuppsättning - redigera namn](./assets/attribute-set-new.png){width="600" zoomable="yes"}

1. Ange en **[!UICONTROL Name]** för attributuppsättningen.

1. Ange **[!UICONTROL Based On]** till en befintlig attributuppsättning som ska användas som mall.

1. klicka **[!UICONTROL Save]**.

   På nästa sida visas följande:

   - I den vänstra kolumnen visas namnet på attributuppsättningen. Namnet används som intern referens och kan ändras vid behov.
   - Mitten av sidan visar det aktuella urvalet av attributgrupper.
   - I den högra kolumnen visas de attribut som för närvarande inte är tilldelade till attributuppsättningen.

1. Om du vill lägga till ett attribut i uppsättningen drar du attributet från **[!UICONTROL Unassigned Attributes]** till lämplig mapp i **[!UICONTROL Groups]** kolumn.

   >[!NOTE]
   >
   >Systemattribut är markerade med en punkt och kan inte tas bort från _[!UICONTROL Groups]_lista. De kan dock dras till en annan grupp i attributuppsättningen.

1. När du är klar klickar du på **[!UICONTROL Save]**.

![Attributuppsättning - redigera](./assets/attribute-set-edit.png){width="600" zoomable="yes"}

## Skapa en attributgrupp

1. I _[!UICONTROL Groups]_kolumn i attributuppsättningen, klicka på&#x200B;**[!UICONTROL Add New]**.

1. Ange en **[!UICONTROL Name]** för den nya gruppen och klicka på **[!UICONTROL OK]**.

1. Gör något av följande:

   - Dra **[!UICONTROL Unassigned Attributes]** till den nya gruppen.
   - Dra attribut från en annan grupp till den nya gruppen.

   Den nya gruppen blir en del av attribut i en produkt som är baserad på attributuppsättningen.

## Ta bort en attributuppsättning

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Markera attributuppsättningen i listan och öppna i redigeringsläge.

1. Klicka på **[!UICONTROL Delete]**.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.
