---
title: Tilldela en kundgrupp till ett företag
description: Lär dig hur du tilldelar en kundgrupp till ett företagskonto i din Adobe Commerce-butik.
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
source-git-commit: a5a8da076d6cd91eb6c3e573fec5b3fb9d2d3341
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Tilldela en kundgrupp till ett företag

Att tilldela en kundgrupp till ett företag är i princip detsamma som att tilldela en delad katalog. Om den delade katalogen inte är [aktiverad i konfigurationen](enable-basic-features.md), en kundgrupp - och inte en delad katalog - tilldelas ett företag.

>[!NOTE]
>
> Endast en kundgrupp eller delad katalog kan tilldelas ett företag åt gången. En kundgrupp som är associerad med en delad katalog kan inte tas bort.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Hitta företaget i rutnätet och klicka på **[!UICONTROL Edit]** i _[!UICONTROL Action]_kolumn.

   ![Redigera företag](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. Bläddra nedåt och expandera på företagssidan ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Advanced Settings]** -avsnitt.

1. Ange lämplig **[!UICONTROL Customer Group]**.

   >[!NOTE]
   >
   >The [!UICONTROL Customer Group] listan innehåller alla befintliga delade kataloger, även om delade kataloger är inaktiverade i konfigurationen.

   Om du ändrar kundgruppen som tilldelats företaget uppdateras profilerna för alla företagsmedlemmar.

   >[!NOTE]
   >
   >När företagsgruppen har ändrats måste en företagsanvändare logga ut och logga in på Storefront för att se nya priser i katalogen.

   ![Ändra kundgrupp eller delad katalog](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

   >[!NOTE]
   >
   >Om kundgruppstilldelningen ändras från en delad katalog till en vanlig kundgrupp förlorar företagsmedlemmarna åtkomsten till den delade katalogen och den primära katalogen blir tillgänglig för dem från butiken.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL Proceed]**.

1. Klicka på **[!UICONTROL Save]**.
