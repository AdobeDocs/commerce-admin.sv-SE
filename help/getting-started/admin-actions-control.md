---
title: Åtgärdskontroll
description: Lär dig hur du använder åtgärdskontrollen för att tillämpa en åtgärd på en eller flera poster i Admin.
exl-id: 03f313a9-bc17-4151-a2c8-8906342f025d
source-git-commit: a3fb702d0b6e08c3aaaa0d6b5e07aa825026ef76
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# Åtgärdskontroll

När du arbetar med en samling poster i rutnätet kan du använda åtgärdskontrollen för att tillämpa en åtgärd på en eller flera poster. Kontrollen Åtgärder visar alla åtgärder som är tillgängliga för den specifika datatypen. Du kan till exempel använda kontrollen Åtgärder för att uppdatera attributen för valda produkter och ändra statusen från `Disabled` till `Enabled`eller för att ta bort poster från databasen.

Du kan göra så många ändringar som behövs och sedan uppdatera posterna i ett enda steg. Det är mycket effektivare än att ändra inställningarna individuellt för varje produkt. Att redigera en grupp med poster är en asynkron åtgärd som körs i bakgrunden så att du kan fortsätta arbeta i administratören utan att vänta på att åtgärden ska slutföras. Ett meddelande visas när uppgiften är slutförd.

Valet av tillgängliga åtgärder varierar beroende på listan och ytterligare alternativ kan visas beroende på vilken åtgärd som har valts. Om du till exempel ändrar status för en grupp med poster, kan du _[!UICONTROL Status]_visas bredvid kontrollen Åtgärder med ytterligare alternativ.

## Steg 1: Välj poster

Kryssrutan i den första kolumnen i listan identifierar varje post som är mål för åtgärden. The [filterkontroller](admin-grid-controls.md) kan användas för att begränsa listan till de poster som du vill använda som mål för åtgärden.

1. Om det behövs ställer du in filtren längst upp i varje kolumn så att bara de poster som du vill ta med visas.

1. Markera kryssrutan för varje post som är mål för åtgärden, eller använd kolumnväljaren för att välja en gruppmarkering.

![Markera eller avmarkera allt eller allt på sidan](./assets/action-change-selection.png){width="500"}

## Steg 2: Tillämpa en åtgärd på valda poster

1. Ange **[!UICONTROL Actions]** styr den åtgärd som du vill använda.

   **_Exempel:_** Uppdatera attribut

   - Markera kryssrutan för varje post som ska uppdateras i listan.

   - Ange **[!UICONTROL Actions]** styra till `Update Attributes`.

     ![Välj åtgärden Uppdatera attribut](./assets/action-select.png){width="450"}

   - Klicka på **[!UICONTROL Submit]**.

     På sidan Uppdatera attribut visas alla tillgängliga attribut, ordnade efter grupp på panelen till vänster.

     ![Sidan Uppdatera attribut](./assets/action-update-attributes.png){width="700" zoomable="yes"}

   - Välj **[!UICONTROL Change]** intill varje attribut och gör nödvändiga ändringar.

   - Klicka **[!UICONTROL Save]** om du vill uppdatera attributen för gruppen med markerade poster.

1. När du är klar klickar du på **[!UICONTROL Submit]**.

## Åtgärder för kryssrutor

| Åtgärd | Beskrivning |
|--- |--- |
| [!UICONTROL Select All] | Markerar kryssrutan för alla poster i listan. |
| [!UICONTROL Unselect All] | Rensar kryssrutan för alla poster i listan. |
| [!UICONTROL Select All on This Page] | Markerar kryssrutan för poster som visas på den aktuella sidan. |
| [!UICONTROL Deselect All on This Page] | Rensar kryssrutan för poster som visas på den aktuella sidan. |

{style="table-layout:auto"}
