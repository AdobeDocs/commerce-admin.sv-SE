---
title: Tilldela en kundgrupp till ett företag
description: Lär dig hur du tilldelar en kundgrupp till ett företagskonto i din Adobe Commerce-butik.
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
source-git-commit: 581d2cf82880552432471171b69a1a597da54c30
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Tilldela en kundgrupp till ett företag

Att tilldela en kundgrupp till ett företag är i princip detsamma som att tilldela en delad katalog. Om den delade katalogen inte är [aktiverad i konfigurationen](enable-basic-features.md) tilldelas en kundgrupp - och inte en delad katalog - till ett företag.

- Endast en kundgrupp eller delad katalog kan tilldelas ett företag åt gången. En kundgrupp som är associerad med en delad katalog kan inte tas bort.
- Om du ändrar kundgruppen som tilldelats företaget uppdateras profilerna för alla företagsmedlemmar.
- Om kundgruppstilldelningen ändras från en delad katalog till en vanlig kundgrupp förlorar företagsmedlemmarna åtkomsten till den delade katalogen och den primära katalogen blir tillgänglig för dem från butiken.
- När företagsgruppen har ändrats måste en företagsanvändare logga ut och logga in på Storefront för att se nya priser i katalogen.

## Ändra kundgruppen

1. Gå till **[!UICONTROL Customers]** > **[!UICONTROL Companies]** på sidofältet _Admin_.

1. Hitta företaget i rutnätet och klicka på **[!UICONTROL Edit]** i kolumnen _[!UICONTROL Action]_.

   ![Redigera företag](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. Bläddra nedåt och expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Advanced Settings]** på företagssidan.

1. Ange rätt **[!UICONTROL Customer Group]**.

   Listan [!UICONTROL Customer Group] innehåller alla befintliga delade kataloger, även om delade kataloger är inaktiverade i konfigurationen.

   ![Ändra kundgrupp eller delad katalog](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL Proceed]**.

1. Klicka på **[!UICONTROL Save]**.
