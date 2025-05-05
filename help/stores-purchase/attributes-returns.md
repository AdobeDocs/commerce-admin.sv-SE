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

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Returns]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add New Attribute]** i det övre högra hörnet.

   ![Ny Retur - attributegenskaper](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### Definiera egenskaperna

1. Ange **[!UICONTROL Default Label]** om du vill identifiera attributet under datainmatning.

1. För **[!UICONTROL Attribute Code]** anger du en kod som identifierar attributet i systemet.

1. Ange **[!UICONTROL Input Type]** till något av följande för att avgöra vilken typ av indatakontroll som används för datainmatning:

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. Om du vill göra fältet till ett obligatoriskt objekt anger du **[!UICONTROL Values Required]** till `Yes`.

1. Om du vill tilldela ett initialt värde till fältet anger du **[!UICONTROL Default Value]**.

1. Om du vill validera data som anges i fältet innan posten sparas anger du **[!UICONTROL Input Validation]** till något av följande:

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. Ange **[!UICONTROL Minimum Text Length]** och **[!UICONTROL Maximum Text Length]** för indatatyperna `Text Field` och `Text Area`.

1. Om du vill använda ett förbearbetningsfilter anger du **[!UICONTROL Input/Output Filter]** till något av följande:

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. Om du vill göra attributet synligt för kunderna anger du **[!UICONTROL Show on Storefront]** till `Yes` i avsnittet _[!UICONTROL Storefront Properties]_.

1. (Valfritt) För **[!UICONTROL Sort Order]** anger du ett nummer som avgör var det här attributet visas i förhållande till de andra på samma del av sidan. (`0` = först, `1` = sekund, `2` = tredje o.s.v.)

### Hantera etiketter/alternativ

1. Välj **[!UICONTROL Manage Labels/Options]** på den vänstra panelen.

1. I avsnittet **[!UICONTROL Manage Titles (Size, Color, etc.)]** anger du etiketten för varje butiksvy.

   ![Hantera etiketter](./assets/return-attributes.png){width="600" zoomable="yes"}

1. Om **[!UICONTROL Input Type]** för attributet är `Dropdown` hanterar du alternativen i avsnittet **[!UICONTROL Manage Options (Values of Your Attribute)]**.

   - Om du vill lägga till ett alternativ klickar du på **[!UICONTROL Add Option]** och anger etiketten för Admin och varje butiksvy.
   - Välj **[!UICONTROL Is Default]** om du vill göra ett alternativ till det valda standardalternativet.
   - Klicka på **[!UICONTROL Delete]** om du vill ta bort ett alternativ.

1. Klicka på **[!UICONTROL Save Attribute]** om du vill spara ändringarna.
