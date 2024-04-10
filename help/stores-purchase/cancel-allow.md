---
title: Tillåt annulleringsorder
description: Lär dig hur du kan ge kunderna möjlighet att avbryta.
feature: Orders, Storefront
source-git-commit: 613c081c02dd9b5e55de37dccd021af4e429d424
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---


# Tillåt annulleringsorder

När det här alternativet är aktiverat kan du avbryta en beställning direkt från kundens konto. Avbryt är inaktiverat som standard.

## Kriterier för annullering som ska aktiveras för en order

- The _Tillåt annulleringsorder_ konfigurationsalternativet måste vara aktiverat.

- Om ordern är i `Hold`, `Canceled`, `Complete`, eller `Closed` status är alternativet för att avbryta inaktiverat i butiken.

- Om någon av artiklarna i ordern har levererats är alternativet Avbryt inaktiverat i butiken.

- Om någon artikel har betalats är alternativet för att avbryta aktiverat och återbetalningen skapas för den artikeln.

- Om ordern är i `Pending` eller `Processing` status är alternativet för att avbryta aktiverat i butiken.

## Konfigurera för att tillåta kundannullering och anpassa orsaker till annullering

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och markera **[!UICONTROL Sales]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Order cancellation]** -avsnitt.

   ![Alternativ för annullering av order](../configuration-reference/sales/assets/sales-order-cancellation.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Order cancellation through GraphQL]** till `Yes`.

   Den här inställningen aktiverar funktionen för att avbryta från kundkontot i butiken.

1. I **[!UICONTROL Order Order cancellation reasons]** du kan lägga till, ta bort eller ändra en orsak till annullering.

   Med den här inställningen visas annulleringsorsaker i butiken för kunden när de annullerar en order.
Se till att du har angett minst en orsak.

1. Klicka på **[!UICONTROL Save Config]**.

## Avbryt från butiken

Kunden kan initiera avbeställningsfunktionen för en viss order från tre sidor:

- _Mina beställningar_ page

- _Ordervy_ page

- _Mitt konto_ page

### Mina beställningar

The _Avbryt beställning_ visas på sidan Mina beställningar om beställningen kan avbrytas.

![Exempel på butiker - sidan Mina beställningar](./assets/my-order-page-view-cancel.png){width="700" zoomable="yes"}

### Sidan Ordervy

The _Avbryt beställning_ visas på sidan Visa ordning om det går att avbryta ordern.

![Sidan med orderinformation](./assets/order-view-page-cancel.png){width="700" zoomable="yes"}

### Mitt konto

The _Avbryt beställning_ visas under Senaste beställningar på sidan Mitt konto, om beställningen kan annulleras.

![Sidan Mitt konto](./assets/my-account-page-view-cancel.png){width="700" zoomable="yes"}


