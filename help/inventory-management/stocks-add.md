---
title: Lägg till ett lagerställe
description: Lär dig hur du lägger till en aktie- och kartkälla i försäljningskanaler (webbplatser), vilket ger en direktlänk till säljbara kvantiteter och produktinventeringar.
exl-id: d0032ed7-c0d6-4654-b182-43a165e7dcf6
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 1%

---

# Lägg till en aktie

Stock mappar dina källor till försäljningskanaler (eller webbplatser), vilket ger en direkt länk till säljbara kvantiteter och produktinventeringar.

När du skapar en anpassad resurs tilldelar du webbplatser och källor. Källor kan innehålla aktiverade och inaktiverade källor. Du kan till exempel lägga till ett lagerställe i ditt lager och förbereda att öppna platsen för hantering av lager och slutförande av leveranser.

När du har lagt till källor måste du prioritera ordningen för källorna uppifrån (första) och nedåt (sista). Ordern påverkar rekommendationer under orderleverans.

![Nytt Stock](assets/inventory-stock-new.png){width="600" zoomable="yes"}

## Lägg till lagret

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stock]**.

1. Klicka på **[!UICONTROL Add New Stock]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL General]** och ange ett unikt **[!UICONTROL Name]** för att identifiera den nya aktien.

   ![Allmänna aktieoptioner](assets/inventory-stock-general.png){width="350" zoomable="yes"}

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Sales Channels]** -avsnittet och välj **[!UICONTROL Websites]** där detta lager finns tillgängligt.

   Om du vill installera på flera webbplatser håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje webbplats.

   >[!NOTE]
   >
   >Om du väljer en webbplats eller en försäljningskanal som har tilldelats en annan aktie, kopplas den inte från den aktien. Alla Sales Channeler som inte har tilldelats ett anpassat lager tilldelas standardlagret.

   ![Sales Channeler för stockar](assets/inventory-sales-channel.png){width="350" zoomable="yes"}

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Sources]** och gör följande för alla andra lager än standardlagret:

   - Klicka på **[!UICONTROL Assign Sources]**.

   ![Tilldelade källor](assets/inventory-stock-sources.png){width="350" zoomable="yes"}

   - Markera kryssrutor för alla källor som du vill tilldela till lagret.

   >[!IMPORTANT]
   >
   >Om du tilldelar samma källa till flera lager kan det leda till överförsäljning av de produkter som är tilldelade den källan.

   - Klicka på **[!UICONTROL Done]**.

     De tillagda källorna visas i Tilldelade källor.

     ![Tilldela källor till Stock](assets/inventory-assign-sources.png){width="600" zoomable="yes"}

1. Använd ![Sorteringsikon](assets/icon-sort.png) om du vill dra och släppa källorna i en prioritet från överkanten (första) till nederkanten (sista).

   Källordningen är viktig vid leveransorder.

   ![Exempel på tilldelade källor](assets/inventory-stock-priority-after.png){width="600" zoomable="yes"}

1. På _[!UICONTROL Save]_(![Menypil](../assets/icon-menu-down-arrow-red.png)) väljer du **[!UICONTROL Save & Close]**.

## Fältbeskrivningar

| Fält | Beskrivning |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | Namn på aktien. Exempel: `UK Stock`, `US Stock` |
| **[!UICONTROL Sales Channels]** | |
| [!UICONTROL Websites] | Definierar [omfång](../getting-started/websites-stores-views.md#scope-settings) av stocken genom att tilldela den till specifika webbplatser som _försäljningskanaler_. Välj en eller flera webbplatser per Stock. Varje webbplats kan bara tilldelas till ett lager. |
| **[!UICONTROL Sources]** | |
| [!UICONTROL Assign Sources] | Tilldelar lagerkällor till detta lager. Anpassade källor kan inte tilldelas standardlager. |
| [!UICONTROL Assigned Sources] | Lista över tilldelade källor. Dra och släpp källorna med ![Sorteringsikon](assets/icon-sort.png) i en prioriterad order för orderhantering och leverans.<br/><br/>**[!UICONTROL Code]**- Unikt kod-ID för källan.<br/>**[!UICONTROL Name]** - Namnbeskrivning för källan.<br/>**[!UICONTROL Unassign]**- Ta bort den tilldelade källan från lagret med ![Papperskorgsikon](../assets/icon-delete-trashcan-solid.png). |
