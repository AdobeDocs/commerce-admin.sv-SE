---
title: Platta frakt
description: Lär dig hur du ställer in ett alternativ för frakt till fast pris för din butik.
exl-id: a6874509-a79b-42ab-aa93-d70d18fc33f6
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# Platta frakt

_Schablonbelopp_ är en fast, fördefinierad avgift som kan tillämpas per artikel eller per leverans. Platta är en enkel fraktlösning, särskilt om den används tillsammans med den platta förpackningen som finns hos vissa transportföretag. När det här alternativet är aktiverat visas _Platta priser_ som ett alternativ vid utcheckning. Eftersom ingen specifik bärare har angetts kan du använda en valfri bärare.

## Ställ in frakt med schablonbelopp

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Delivery Methods]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **Platt hastighet**.

   ![Platt hastighet](../configuration-reference/sales/assets/delivery-methods-flat-rate.png){width="600" zoomable="yes"}

   En detaljerad beskrivning av de här konfigurationsinställningarna finns i [Platt hastighet](../configuration-reference/sales/delivery-methods.md#flat-rate) i _referenshandboken för konfiguration_.

1. Ange **[!UICONTROL Enabled]** till `Yes`.

   Platta priser visas som ett alternativ i avsnittet Beräkna frakt och moms i kundvagnen och även i avsnittet Leverans under utcheckningen.

1. Ange en beskrivande **[!UICONTROL Title]** för metoden Platt hastighet.

1. Ange ett **metodnamn** som ska visas bredvid den beräknade tariffen i kundvagnen.

   Standardmetodnamnet är `Fixed`. Om du debiterar en hanteringsavgift kan du ändra den här texten till `Plus Handling`, eller något annat som är lämpligt.

1. Ange **Type** till något av följande för att beskriva hur frakt med schablonbelopp kan användas:

   - `None` - Inaktiverar betalningstypen. Alternativet för schablonbelopp anges i kundvagnen, men med en nollkostnad, vilket är detsamma som fri frakt.
   - `Per Order` - Debiterar ett schablonbelopp för hela ordern.
   - `Per Item` - Debiterar en fast avgift för varje objekt. Kursen multipliceras med antalet artiklar i vagnen, oavsett om det finns flera kvantiteter av samma eller olika artiklar.

1. Ange det **pris** som du vill debitera för frakt till fast pris.

1. Konfigurera alternativ för hanteringsavgift enligt dina behov.

   Hanteringsavgiften är valfri och visas som en extra avgift som läggs till i leveranskostnaden. Om du vill ta med en hanteringskostnad gör du följande:

   - För **Beräkna hanteringsavgift** väljer du den metod som du vill använda för att beräkna hanteringsavgifter:

      - `Fixed`
      - `Percent`

   - För **Hanteringsavgift** anger du det belopp som ska debiteras baserat på den metod du har valt för att beräkna beloppet.

     Om avgiften till exempel baseras på en fast avgift anger du beloppet i decimalform, till exempel `4.90`. Om hanteringsavgiften baseras på en procentandel av leveranskostnaden anger du beloppet i procent. Om du till exempel debiterar sex procent av leveranskostnaden anger du värdet som `6`.

1. Ändra **Visa felmeddelande** om det behövs.

   Den här textrutan är förinställd med ett standardmeddelande, men du kan ange ett annat meddelande som du vill ska visas om frakten med schablonbelopp inte är tillgänglig.

1. Ange **Leverera till tillämpliga länder**:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här leveransmetoden.
   - `Specific Countries` - När du väljer det här alternativet visas listan _Leverera till specifika länder_. Välj varje land i listan där leveransmetoden kan användas.

1. Ange **Visa metod om den inte är tillämplig**:

   - `Yes` - Visar alltid metoden för schablonbelopp, även om den inte är tillämplig.
   - `No` - Visar metoden för schablonbelopp endast när det är tillämpligt.

1. För **[!UICONTROL Sort Order]** anger du ett nummer för att bestämma i vilken ordning som frakt med platt hastighet ska visas när den visas tillsammans med andra leveransmetoder vid utcheckning.

   `0` = först, `1` = sekund, `2` = tredje och så vidare.

1. Klicka på **[!UICONTROL Save Config]**.
