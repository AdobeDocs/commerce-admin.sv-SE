---
title: Dolda kategorier
description: Lär dig hur du använder dolda kategorier för interna syften eller för att länka till en kategori som inte finns med på navigeringsmenyn.
exl-id: 43aa74b3-b4cd-488d-aa58-fa2c468fe3a2
feature: Catalog Management, Categories
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Dolda kategorier

Det finns många sätt att använda dolda kategorier. Du kanske vill skapa ytterligare kategorinivåer för dina interna syften, men bara visa kategorierna på den högre nivån för dina kunder. Du kan också länka till en kategori som inte finns med på navigeringsmenyn.

## Skapa dolda kategorier

1. Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Categories]** på sidofältet _Admin_.

1. Välj den kategori som du vill dölja i kategoriträdet och gör följande:

   - Ange **[!UICONTROL Is Active]** till `Yes`.
   - Ange **[!UICONTROL Include in Menu]** till `No`.

1. I avsnittet **[!UICONTROL Display Settings]** anger du **[!UICONTROL Anchor]** till `No`.

   ![Dold kategori](./assets/hidden-categories.png){width="600" zoomable="yes"}

   Den dolda kategorin är aktiv, men visas inte på den översta menyn eller i lagernavigering.

1. Gör följande inställningar för varje dold underkategori för att skapa underkategorier:

   >[!NOTE]
   >
   >Även om kategorin är dold kan du skapa underkategorier under den och aktivera dem.

   - Ange **[!UICONTROL Enable Category]** till `Yes`.
   - I avsnittet **[!UICONTROL Display Settings]** anger du **[!UICONTROL Anchor]** till `Yes`.

   Som aktiva kategorier kan du nu länka till dem från andra platser i din butik, men de visas inte på menyn.

1. Klicka på **[!UICONTROL Save]** när du är klar.
