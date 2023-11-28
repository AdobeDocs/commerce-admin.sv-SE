---
title: Skatteregler
description: Lär dig hur du definierar skatteregler med hjälp av produktklass, kundklass och momssats.
exl-id: 38d65998-7769-49ce-9814-e65df9d77bba
feature: Taxes, Currency
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# Skatteregler

Skattereglerna innehåller en kombination av produktklass, kundklass och momssats. Varje kund tilldelas en kundklass och varje produkt tilldelas en produktklass. Commerce analyserar kundvagnen och beräknar lämplig skatt enligt kund- och produktklasserna samt regionen. Regionen baseras på kundens leveransadress, faktureringsadress eller leveransadress.

>[!NOTE]
>
>När du måste definiera flera skattesatser kan du förenkla processen genom att importera dem.

![Skatteregler](./assets/tax-rules.png){width="600" zoomable="yes"}

## Steg 1: Fyll i momsregelinformationen

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Klicka på i det övre högra hörnet **[!UICONTROL Add New Tax Rule]**.

1. Under _Information om momsregel_, ange **[!UICONTROL Name]** för den nya regeln.

   ![Information om momsregel](./assets/tax-rule-information.png){width="600" zoomable="yes"}

1. Välj **[!UICONTROL Tax Rate]** som gäller för regeln.

   Så här redigerar du en befintlig skattesats:

   - Håll muspekaren över momssatsen och klicka på _Redigera_ ![Pennikon](../assets/icon-edit-pencil.png) -ikon.

   - Uppdatera formuläret efter behov och klicka på **[!UICONTROL Save]**.

1. Använd någon av följande metoder för att ange skattesatser:

### Metod 1: Ange momssatser manuellt

1. Klicka på **[!UICONTROL Add New Tax Rate]**.

1. Fyll i formuläret efter behov (se [Skattezoner och skattesatser](tax-zones-rates.md)).

1. När du är klar klickar du på **[!UICONTROL Save]**.

   ![Ny momssats](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

### Metod 2: Importskattesatser

1. Rulla ned till avsnittet längst ned på sidan.

1. Så här importerar du momssatser:

   - Klicka **[!UICONTROL Choose File]** och navigera till CSV-filen med momssatserna som ska importeras.

   - Klicka på **[!UICONTROL Import Tax Rates]**.

1. Om du vill exportera momssatser klickar du på **[!UICONTROL Export Tax Rates]** (se [Importera/exportera momssatser](../systems/data-transfer-tax-rates.md)).

![Importera/exportera momssatser](./assets/tax-rule-new-import-export.png){width="600" zoomable="yes"}

## Steg 2: Slutför de extra inställningarna

1. Klicka på **[!UICONTROL Additional Settings]**.

   ![Ytterligare inställningar för momsregel](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. Välj **[!UICONTROL Customer Tax Class]** som regeln gäller.

   - Om du vill redigera en kundskatteklass klickar du på _Redigera_ ![Pennikon](../assets/icon-edit-pencil.png) , uppdatera formuläret efter behov och klicka på **[!UICONTROL Save]**.

   - Om du vill skapa en skatteklass klickar du på **[!UICONTROL Add New Tax Class]** fylla i formuläret efter behov och klicka **[!UICONTROL Save]**.

1. Välj **[!UICONTROL Product Tax Class]** som regeln gäller.

   - Om du vill redigera en produktmomsklass klickar du på _Redigera_ ![Pennikon](../assets/icon-edit-pencil.png) , uppdatera formuläret efter behov och klicka på **[!UICONTROL Save]**.

   - Om du vill skapa en skatteklass klickar du på **[!UICONTROL Add New Tax Class]** fylla i formuläret efter behov och klicka **[!UICONTROL Save]**.

1. När mer än en skatt är tillämplig anger du ett nummer som anger prioriteten för den här skatten för **[!UICONTROL Priority]**.

   Om två momsregler med samma prioritet gäller läggs skatterna till. Om det finns två skatter med olika prioritetsinställningar läggs skatterna samman.

1. Om du vill att moms ska baseras på orderdelsumman väljer du **[!UICONTROL Calculate off Subtotal Only]** kryssrutan.

1. För **[!UICONTROL Sort Order]** anger du ett nummer som anger ordningen för den här momsregeln när den visas tillsammans med andra.

1. När du är klar klickar du på **[!UICONTROL Save Rule]**.

## Demo av valutor och momsregler

Läs om hur du hanterar valuta- och momsregler i den här videon:

>[!VIDEO](https://video.tv.adobe.com/v/343657/?quality=12)
