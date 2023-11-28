---
title: Instrumentpanel för innehållstagning
description: Använd kontrollpanelen för innehållstagning för att få en översikt över alla aktiva och kommande kampanjer.
exl-id: 67c18c1c-94c3-4d89-ae1e-868a465431e3
feature: Page Content, Staging
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Instrumentpanel för innehållstagning

{{ee-feature}}

The [!UICONTROL Content Staging] Dashboard ger en översikt över alla aktiva och kommande kampanjer. Kontrollpanelens format kan ändras från ett rutnät till en tidslinje. Du kan också använda filter för att hitta kampanjer, anpassa kolumnlayouten och spara olika vyer av rutnätet. Mer information om arbetsytans kontroller finns i [Arbetsyta för administratörer](../getting-started/admin-workspace.md).

![Kontrollpanel för mellanlagring i stödrastervyn](./assets/content-staging-grid-view.png){width="600" zoomable="yes"}

## Visa kontrollpanelen för mellanlagring

1. På _Administratör_ sidebar, gå till  **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. Om du vill ändra kontrollpanelens format anger du **[!UICONTROL View As]** styra till `list`, `Grid`, eller `Timeline`.

   ![Tidslinjevy](./assets/content-staging-dashboard-timeline.png){width="600" zoomable="yes"}

   När tidslinjen visas kan du använda skjutreglaget i det nedre högra hörnet för att justera vyn från en till fyra veckor. Varje kolumn representerar en dag.

1. Om tidslinjen visas drar du skjutreglaget till `4w` längst till höger om du vill visa ett längre tidsintervall.

   ![Fyrveckorsvy](./assets/content-staging-timeline-4-week-view.png){width="600" zoomable="yes"}

1. Klicka på ett objekt på sidan om du vill visa allmän information om kampanjen.

   - Klicka på **[!UICONTROL View/Edit]**.

   - Om du vill se hur kampanjen ser ut för kunderna i butiken den dagen klickar du på **[!UICONTROL Preview]**.

   ![Kampanjinformation](./assets/content-staging-campaign-info.png){width="600" zoomable="yes"}

## Kolumnbeskrivningar för mellanlagringspanelen

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Status] | Kampanjens status. `Active` eller `Upcoming`. |
| [!UICONTROL Update Name] | Namnet på kampanjen. |
| [!UICONTROL Includes] | Definierar hur många objekt som ingår i kampanjen. |
| [!UICONTROL Start Time] | Det datum då kampanjen startar. |
| [!UICONTROL End Time] | Datumet då kampanjen avslutas. |
| [!UICONTROL Description] | Ytterligare beskrivning av varje kampanj. |
| [!UICONTROL Action] | De åtgärder som kan tillämpas på en enskild post är bland annat:<br/>**[!UICONTROL View/Edit]**- Öppnar kampanjen i redigeringsläge.<br/>**[!UICONTROL Preview]** - Visar kampanjen i förhandsgranskningsläge. |

{style="table-layout:auto"}

## Redigera en kampanj

Befintliga kampanjobjekt kan redigeras från kontrollpanelen för mellanlagring, förutom för prisregelkampanjer som inte har slutdatum.

>[!NOTE]
>
>Om en kampanj som innehåller en prisregel ursprungligen skapas utan ett slutdatum, kan kampanjen inte redigeras senare för att inkludera ett slutdatum. I så fall är det nödvändigt att skapa en dubblettkampanj och ange det slutdatum som behövs.

![Kampanjinformation](./assets/content-staging-dashboard-view-edit.png){width="600" zoomable="yes"}

Kampanjen i det här exemplet innehåller två kategorier och tre enskilda produkter.

Följ stegen nedan om du vill redigera något av objekten i kampanjen.

1. På _Administratör_ sidebar, gå till  **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. Hitta kampanjen i den visade listan eller tidslinjen och öppna den för att få tillgång till informationen:

   - Om du vill visa en lista klickar du **[!UICONTROL Select]** och sedan **[!UICONTROL View/Edit]** i _[!UICONTROL Action]_kolumn.
   - Om du vill visa en tidslinje klickar du en gång för att visa sammanfattningen och sedan på **[!UICONTROL View/Edit]**.

1. Uppdatera någon av inställningarna i _[!UICONTROL General]_efter behov.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) alla avsnitt som innehåller ett objekt som ska redigeras.

   ![Uppdaterar tilldelade produkter för en kampanjartikel](./assets/content-staging-campaign-edit-products.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]**.
