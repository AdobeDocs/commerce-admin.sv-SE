---
title: Fast produktskatt
description: Lär dig hur du kan ställa in en fast produktskatt som måste läggas till i vissa typer av produkter.
exl-id: f1b475cb-a6fe-4b51-a0c3-7d0a202bd332
feature: Checkout, Invoices, Taxes, Products
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '867'
ht-degree: 0%

---

# Fast produktskatt

Vissa skattejurisdiktioner har en fast skatt som måste läggas till vissa typer av produkter. Du kan konfigurera en _fast produktskatt_ (FPT) efter behov för butikens momsberäkningar. I vissa länder kan FPT användas för att införa en skatt på avfall som utgörs av eller innehåller elektrisk och elektronisk utrustning (WEEE). Denna skatt kallas också _ekologisk skatt_ eller _miljöskatt_ och samlas in för vissa typer av elektronik för att kompensera för återvinningskostnaderna. Det är ett fast belopp i stället för en procentandel av produktpriset.

Fasta produktskatter tillämpas på artikelnivå, baserat på produkten. I vissa jurisdiktioner är denna skatt föremål för en extra procentuell skatteberäkning. Skattejurisdiktionen kan också innehålla regler om hur produktpriset ser ut för kunderna, med eller utan skatt. Se till att du förstår reglerna och anger visningsalternativen för FPT utifrån detta.

Var försiktig när du anger priser för bildrutepresentationer via e-post, eftersom prisskillnaden kan påverka kundernas förtroende för beställningarna. Om du t.ex. visar priser för ordergranskning utan att visa FPT, ser kunder som köper artiklar med tillhörande FPT en summa som inkluderar FPT-momsbeloppet, men utan en specificerad uppdelning. Skillnaden i pris kan leda till att vissa kunder överger sina varukorgar eftersom summan skiljer sig från det förväntade beloppet.

## Visningspriser för FPT

| FPT | Visningsinställning och beräkning | |
|--- |--- |---|
| Ej beskattad | **[!UICONTROL Excluding FPT]** | FPT visas som en separat rad i kundvagnen och värdet används i lämpliga momsberäkningar. |
| | **[!UICONTROL Including FPT]** | FPT läggs till baspriset för en artikel, men inkluderas inte i momsregelbaserade beräkningar. |
| | **[!UICONTROL Excluding FPT, FPT Description, Final Price]** | Priserna visas utan FPT-belopp eller beskrivning. FPT ingår inte i momsbaserade beräkningar. |
| Skattepliktig | **[!UICONTROL Excluding FPT]** | FPT visas som en separat rad i kundvagnen och värdet används i lämpliga momsberäkningar. |
| | **[!UICONTROL Including FPT]** | FPT ingår i priset för en artikel och ingen ändring av momsberäkningar krävs. |
| | **[!UICONTROL Excluding FPT, FPT Description, Final Price]** | Priserna visas utan FPT-belopp eller beskrivning. FPT ingår dock i momsbaserade beräkningar. |

{style="table-layout:auto"}

## Konfigurera FPT

FPT (Fixed Product Tax) [indatatyp](../catalog/attributes-input-types.md) skapar ett avsnitt med fält för att hantera moms för varje region.

Följande instruktioner visar hur du ställer in en fast produktskatt för din butik, med&quot;miljöskatt&quot; som exempel. När du har angett skatteomfånget och de länder och lägen där skatten ska gälla, och beroende på vilka alternativ du väljer, kan inmatningsfälten ändras enligt lokala krav. Mer information finns på [Skapa produktattribut](../catalog/attribute-product-create.md).

### Steg 1: Aktivera fast produktskatt

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Tax]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Fixed Product Taxes]** -avsnitt.

1. Ange **[!UICONTROL Enable FPT]** till `Yes`.

1. Om du vill avgöra hur fasta produktskatter används i butikspriser väljer du FPT-inställningen för var och en av följande prisvisningsställen:

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Prices on Product View Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   Alternativ (samma för varje):

   - `Including FPT Only`
   - `Including FPT and FPT description`
   - `Excluding FPT. Including FPT description and final price`
   - `Excluding FPT`

1. Ange **[!UICONTROL Apply Tax to FPT]** efter behov.

1. Ange **[!UICONTROL Include FPT in Subtotal]** efter behov.

   ![Fasta produktskatter](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

   En detaljerad beskrivning av de här konfigurationsinställningarna finns i [Fasta produktskatter](../configuration-reference/sales/tax.md#fixed-product-taxes) i _Referenshandbok för konfiguration_.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

### Steg 2: Skapa ett FPT-attribut

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Klicka på i det övre högra hörnet **[!UICONTROL Add New Attribute]** och gör följande:

   - För **[!UICONTROL Default Label]** anger du en etikett som identifierar attributet.

   - Ange **[!UICONTROL Catalog Input for Store Owner]** till `Fixed Product Tax`.

   ![Attributegenskaper](./assets/tax-fpt-attribute-properties.png){width="600" zoomable="yes"}

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Advanced Attribute Properties]** och ange egenskapsalternativ:

   - **[!UICONTROL Attribute Code]** - Ange en unik identifierare i gemener, utan mellanslag eller specialtecken. Maximala längden är 30 tecken. Du kan lämna fältet tomt till texten från fältet Standardetikett.

   - **[!UICONTROL Add to Column Options]** - Om du vill att FPT-fältet ska visas i [Produktlista](../catalog/products-list.md), ställs in på `Yes`.

   - **[!UICONTROL Use in Filter Options]** - Om du vill kunna [filter](../getting-started/admin-workspace.md) produkter i rutnätet baserat på FPT-fältets värde, inställt på `Yes`.

   ![Avancerade attributegenskaper](./assets/tax-fpt-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. (Valfritt) Välj **[!UICONTROL Manage Labels]** och ange en etikett som ska användas i stället för standardetiketten för varje butiksvy.

   ![Hantera etiketter](./assets/attribute-new-manage-labels.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Attribute]**.

1. Uppdatera [cache](../systems/cache-management.md).

### Steg 3: Lägg till FPT-attributet i en attributuppsättning

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Klicka på attributuppsättningen i listan för att öppna posten i redigeringsläge.

   ![Attributuppsättningslista](./assets/attribute-sets-list.png){width="600" zoomable="yes"}

1. Dra FPT-attributet från listan med **[!UICONTROL Unassigned Attributes]** till höger till **[!UICONTROL Groups]** i mittkolumnen.

   Varje gruppmapp motsvarar ett avsnitt i produktinformationen. Du kan placera attributet där du vill att det ska visas när produkten är öppen i redigeringsläge.

   ![Redigera attributuppsättning](./assets/tax-fpt-attribute-set-drag.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save]**.

1. Upprepa det här steget för varje attributuppsättning som ska innehålla fast produktskatt.

### Steg 4: Tillämpa FPT på specifika produkter

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Öppna den produkt som behöver en fast produktskatt i redigeringsläge.

1. Hitta **[!UICONTROL FPT]** avsnitt med fält som du har lagt till i attributuppsättningen och klickar på **[!UICONTROL Add Tax]**.

1. Ange tillämplig moms för produkten:

   ![Fast produktskatt för Kanada](./assets/tax-product-fpt-canada.png){width="600" zoomable="yes"}

   - Om din Commerce-instans har flera webbplatser väljer du lämplig **[!UICONTROL Website]** och basvaluta. I det här exemplet är fältet som standard inställt på `All Websites [USD]`.

   - Ange **[!UICONTROL Country/State]** till den region där den fasta produktskatten gäller.

   - För **[!UICONTROL Tax]** anger du den fasta produktskatten som ett decimalbelopp.

1. Om du vill lägga till fler fasta produktskatter klickar du på **[!UICONTROL Add Tax]** och upprepa processen.

1. När du är klar klickar du på **[!UICONTROL Save]**.
