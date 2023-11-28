---
title: Returnerar attribut
description: Lär dig mer om returattributen och hur du skapar de attribut som behövs för att bearbeta returer på din butik.
exl-id: 639c1e94-1211-4a4e-8599-e54ed99b2355
feature: Attributes, Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Returnerar attribut

{{ee-feature}}

Returattributen används för att lagra information som behövs under produktreturen. Standardattributen innehåller villkoret för den returnerade produkten, orsaken till returvärdet och ett fält som anger hur returneringen löstes. Processen för att skapa ett returattribut liknar den för att skapa ett [kundattribut](../customers/attribute-properties.md).

![Admin - Returnerar attribut](./assets/attribute-returns.png){width="700" zoomable="yes"}

## Skapa ett returattribut

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Returns]**.

1. Klicka på i det övre högra hörnet **[!UICONTROL Add New Attribute]**.

   ![Ny Retur - attributegenskaper](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### Definiera egenskaperna

1. Om du vill identifiera attributet under datainmatning anger du **[!UICONTROL Default Label]**.

1. För **[!UICONTROL Attribute Code]** anger du en kod som identifierar attributet i systemet.

1. Ange vilken typ av indatakontroll som ska användas för datainmatning **[!UICONTROL Input Type]** till något av följande:

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. Gör fältet till ett obligatoriskt objekt genom att ange **[!UICONTROL Values Required]** till `Yes`.

1. Om du vill tilldela ett initialt värde till fältet anger du ett **[!UICONTROL Default Value]**.

1. Om du vill validera de data som anges i fältet innan posten sparas anger du **[!UICONTROL Input Validation]** till något av följande:

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. För `Text Field` och `Text Area` indatatyper, ange **[!UICONTROL Minimum Text Length]** och **[!UICONTROL Maximum Text Length]**.

1. Om du vill använda ett förbearbetningsfilter anger du **[!UICONTROL Input/Output Filter]** till något av följande:

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. Ange attributet så att det blir synligt för kunderna **[!UICONTROL Show on Storefront]** till `Yes` i _[!UICONTROL Storefront Properties]_-avsnitt.

1. (valfritt) för **[!UICONTROL Sort Order]** anger du ett tal som anger var attributet ska visas i förhållande till de andra på samma del av sidan. (`0` = first, `1` = sekund, `2` = tredje och så vidare.)

### Hantera etiketter/alternativ

1. Välj **[!UICONTROL Manage Labels/Options]**.

1. I **[!UICONTROL Manage Titles (Size, Color, etc.)]** anger du etiketten för varje butiksvy.

   ![Hantera etiketter](./assets/return-attributes.png){width="600" zoomable="yes"}

1. Om **[!UICONTROL Input Type]** för attributet är `Dropdown`, hanterar alternativen i **[!UICONTROL Manage Options (Values of Your Attribute)]** -avsnitt.

   - Om du vill lägga till ett alternativ klickar du **[!UICONTROL Add Option]** och ange etiketten för Admin och varje butiksvy.
   - Om du vill göra ett alternativ till det valda standardalternativet väljer du **[!UICONTROL Is Default]**.
   - Om du vill ta bort ett alternativ klickar du **[!UICONTROL Delete]**.

1. Om du vill spara ändringarna klickar du **[!UICONTROL Save Attribute]**.
