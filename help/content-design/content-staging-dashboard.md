---
title: Instrumentpanel för innehållstagning
description: Använd kontrollpanelen för innehållstagning för att få en översikt över alla aktiva och kommande kampanjer.
exl-id: 67c18c1c-94c3-4d89-ae1e-868a465431e3
feature: Page Content, Staging
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 07d7ca7e7f6af42fe8e06dc3c49c2df5f50d1425
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# Instrumentpanel för innehållstagning

{{ee-feature}}

Kontrollpanelen [!UICONTROL Content Staging] ger en översikt över alla aktiva och kommande kampanjer. Kontrollpanelens format kan ändras från ett rutnät till en tidslinje. Du kan också använda filter för att hitta kampanjer, anpassa kolumnlayouten och spara olika vyer av rutnätet. Mer information om arbetsytekontroller finns i [Admin workspace](../getting-started/admin-workspace.md).

![Kontrollpanelen för mellanlagring i stödrastervyn](./assets/content-staging-grid-view.png){width="600" zoomable="yes"}

## Visa kontrollpanelen för mellanlagring

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**på sidofältet_ Admin _.

1. Om du vill ändra kontrollpanelens format anger du **[!UICONTROL View As]**-kontrollen till `list`, `Grid` eller `Timeline`.

   ![Tidslinjevy](./assets/content-staging-dashboard-timeline.png){width="600" zoomable="yes"}

   När tidslinjen visas kan du använda skjutreglaget i det nedre högra hörnet för att justera vyn från en till fyra veckor. Varje kolumn representerar en dag.

1. Om tidslinjen visas drar du skjutreglaget till positionen `4w` längst till höger för att visa ett längre tidsintervall.

   ![Fyrveckorsvy](./assets/content-staging-timeline-4-week-view.png){width="600" zoomable="yes"}

1. Klicka på ett objekt på sidan om du vill visa allmän information om kampanjen.

   - Klicka på **[!UICONTROL View/Edit]** om du vill öppna kampanjen.

   - Klicka på **[!UICONTROL Preview]** om du vill se hur kampanjen ser ut för kunder i butiken den dagen.

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
| [!UICONTROL Action] | Åtgärderna som kan tillämpas på en enskild post omfattar:<br/>**[!UICONTROL View/Edit]**- Öppnar kampanjen i redigeringsläge.<br/>**[!UICONTROL Preview]** - Visar kampanjen i förhandsgranskningsläge. |

{style="table-layout:auto"}

## Redigera en kampanj

Befintliga kampanjobjekt kan redigeras från kontrollpanelen för mellanlagring, förutom för prisregelkampanjer som inte har slutdatum.

>[!NOTE]
>
>Om en aktiv kampanj initialt skapas utan ett slutdatum kan kampanjen inte redigeras senare så att den innehåller ett slutdatum. I så fall är det nödvändigt att skapa en dubblettkampanj och ange det slutdatum som behövs.

![Kampanjinformation](./assets/content-staging-dashboard-view-edit.png){width="600" zoomable="yes"}

Kampanjen i det här exemplet innehåller två kategorier och tre enskilda produkter.

Följ stegen nedan om du vill redigera något av objekten i kampanjen.

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**på sidofältet_ Admin _.

1. Hitta kampanjen i den visade listan eller tidslinjen och öppna den för att få tillgång till informationen:

   - Om du vill visa en lista klickar du på **[!UICONTROL Select]** och sedan på **[!UICONTROL View/Edit]** i kolumnen _[!UICONTROL Action]_.
   - Om du vill visa en tidslinje klickar du en gång för att visa sammanfattningen och sedan på **[!UICONTROL View/Edit]**.

1. Uppdatera inställningarna i avsnittet _[!UICONTROL General]_efter behov.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i alla avsnitt som innehåller ett objekt som ska redigeras.

   ![Uppdaterar tilldelade produkter för ett kampanjobjekt](./assets/content-staging-campaign-edit-products.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]**.
