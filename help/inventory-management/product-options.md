---
title: "Konfigurera [!DNL Inventory Management] produktalternativ"
description: Lär dig hur du konfigurerar [!DNL Inventory Management] produktkonfigurationsalternativ.
exl-id: b5cff7d2-5197-4362-9503-b07c80793ac7
feature: Inventory, Products
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 0%

---

# Konfigurera [!DNL Inventory Management] produktalternativ

Dessa konfigurationer gäller endast den redigerade produkten och åsidosätter alla konfigurationer på global webbplatsnivå. Ändra de här inställningarna när du redigerar en produkt via _[!UICONTROL Sources]_och_[!UICONTROL Advanced Inventory]_ sida.

- Konfigurera produktalternativ efter källa
- Konfigurera produktalternativ för avancerat lager

## Produktalternativ efter källa

Konfigurera kvantiteter och ytterligare inställningar per [tillagd källa](sources-add.md) för produkten.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Öppna en produkt i redigeringsläge.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Sources]** och konfigurera produktinställningar för varje källa:

   - Ange en **[!UICONTROL Qty]** (kvantitet) belopp.

   - Ange **[!UICONTROL Source Item Status]** as `In Stock` eller `Out of Stock`.

   - Om du vill ändra Notify for Quantify Below per source rensar eller väljer du **[!UICONTROL Notify Quantity Use Default]** kryssrutan.

     Om det är avmarkerat anger du det lagernivåbelopp som utlöser artikeln i lagermeddelanden. Det angivna beloppet subtraheras från artikelns säljbara kvantitet på lagernivå.

     `Select to use Default` - [!DNL Commerce] kontrollerar om det finns konfigurationsinställningar i alternativen för avancerad inventering för produkten.
     `Clear to Modify` - Ange ett värde för Notify Quantity och åsidosätt konfigurationsinställningarna Advanced Inventory och Store.

   ![Källavsnitt för en produkt](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Done]** sedan **[!UICONTROL Save]**.

### Fältbeskrivningar

| Fält | Omfång | Beskrivning |
|--|--|--|
| [!UICONTROL Source Code] | Global | Unik kod för en [källa](sources-manage.md). |
| [!UICONTROL Name] | Global | Det unika namnet för en källa. |
| [!UICONTROL Status] | Global | Produkten är aktiverad eller inaktiverad i katalogen. |
| [!UICONTROL Source Item Status] | Global | Bestämmer produktens aktuella tillgänglighet. Alternativ:<br />`In Stock` - Gör produkten tillgänglig att köpa.<br />`Out of Stock` - Om inte Restorder är aktiverade förhindrar du att produkten kan köpas och tar bort listan från katalogen. |
| [!UICONTROL Qty] | Global | Lagringsbelopp för varje källa eller plats. |
| [!UICONTROL Notify Quantity] | Global | Ett belopp för _[!UICONTROL Notify for Quantity Below]_för denna specifika källa om_[!UICONTROL Notify Quantity Use Default]_ är inte markerat. |
| [!UICONTROL Notify Quantity Use Default] | Global | Anger att standardinställningen för _[!UICONTROL Notify for Quantity Below]_i produkten_[!UICONTROL Advanced Inventory]_ eller globala inställningar i butikskonfigurationen. |

## Avancerade produktalternativ

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Öppna en produkt i redigeringsläge.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Sources]** och klicka **[!UICONTROL Advanced Inventory]**.

1. Aktivera [lagerstyrning](enable.md) för katalogen, ange **[!UICONTROL Manage Stock]** till `Yes`.

   >[!NOTE]
   >
   >[!UICONTROL Manage Stock] inställningarna i underordnade produkter åsidosätter en konfigurerbar produkt.

   ![Avancerat lager för en produkt](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. Ange ett belopp för **[!UICONTROL Out-of-Stock Threshold]**:

   | Värde | Beskrivning |
   | ----- | ----- |
   | Positivt belopp | Med _[!UICONTROL Backorders]_inaktiverat anger du ett positivt värde. |
   | Noll | Med _[!UICONTROL Backorders]_aktiverad, ange `0` ger oändliga efterbeställningar. |
   | Negativt belopp | Med _[!UICONTROL Backorders]_aktiverat rekommenderas att ett negativt värde anges. Beloppet läggs till i den säljbara kvantiteten. Skriv till exempel `-50` för att tillåta order upp till detta belopp. |

1. Ange **[!UICONTROL Minimum Qty Allowed in Shopping Cart]**.

1. Ange **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

1. Ange **[!UICONTROL Qty uses Decimals]** till `Yes` om kunderna kan använda ett decimalvärde i stället för ett heltal när de anger beställd kvantitet.

1. Ange **[!UICONTROL Allow Multiple Boxes for Shipping]** till `Yes` om produkten kan säljas separat, i många lådor. Det här alternativet visas när **[!UICONTROL Qty Uses Decimals]** är inställd på `Yes` endast.

1. Ange **[!UICONTROL Backorders]** till något av följande:

   | Alternativ | Beskrivning |
   | ----- | ----- |
   | `No Backorders` | Att inte acceptera restorder när produkten inte finns i lager. |
   | `Allow Qty Below 0` | Att acceptera restorder när kvantiteten är under noll. |
   | `Allow Qty Below 0 and Notify Customer` | Om du vill acceptera restorder när kvantiteten är under noll och meddela kunden att ordern fortfarande kan läggas. |

   Mer information finns i [Konfigurera backorders](backorders.md).

1. Om du vill aktivera kvantitetsökningar för produkten anger du **[!UICONTROL Enable Qty Increments]** till `Yes` och ange antalet artiklar som måste köpas för att uppfylla kravet i **[!UICONTROL Qty Increments]** fält.

   Till exempel kan en artikel som säljs i steg om sex köpas i kvantiteter om 6, 12, 18 osv.

   **[!UICONTROL Qty Increments]** anges hur många produktartiklar som måste köpas som en enskild produkt och som underordnade till konfigurerbara, grupperade och paketerade produkter.

1. När du är klar klickar du på **[!UICONTROL Done]** och sedan **[!UICONTROL Save]**.

### Fältbeskrivningar

| Fält | Omfång | Beskrivning |
|--|--|--|
| [!UICONTROL Manage Stock] | Global | Fastställer om lagerkontroll används för att hantera den här produkten i din katalog. Ange om du vill aktivera eller inaktivera alla [!DNL Inventory Management] funktioner. När du slutför en retur eller en kreditnota returneras produktkvantiteten automatiskt till den berörda källkvantiteten. Du kan inaktivera om du använder ett ERP-system från en annan leverantör. |
| [!UICONTROL Out-of-Stock Threshold] | Global | Bestämmer lagernivån där en produkt anses vara ur lager. Alternativ:<br />Positivt värde - När restorder är inaktiverade anger du ett positivt belopp.<br />Noll (0) - Om du aktiverar Restorder kan du ange noll för oändliga efterbeställningar.<br />Negativt värde - När restorder är aktiverade rekommenderas ett negativt belopp. Beloppet läggs till i den säljbara kvantiteten. Skriv till exempel `-50` för att tillåta order upp till detta belopp. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Global | Fastställer det minsta antalet produkter som kan köpas i en enda order. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Global | Fastställer det högsta antalet produkter som kan köpas i en enda order. |
| [!UICONTROL Qty Uses Decimals] | Global | Avgör om kunderna kan använda ett decimalvärde i stället för ett heltal när de anger beställd kvantitet. Alternativ:<br />`Yes` - Tillåter att värden anges som decimaler i stället för som heltal. Decimaler är lämpliga för produkter som säljs efter vikt, volym eller längd.<br />`No` - Kräver att kvantitetsvärden anges som heltal. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Global | Anger om delar av produkten kan levereras separat. Det här alternativet visas när **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Global | Avgör hur restorder hanteras. Restorder ändrar inte orderns bearbetningsstatus. Pengarna godkänns eller hämtas direkt när beställningen görs, oavsett om produkten finns i lager eller inte. Produkterna levereras när de blir tillgängliga. När det här alternativet är aktiverat bör du ange ett negativt värde för tröskelvärdet för Ej lagrad. Alternativ:<br/>`No Backorders` - Tar inte emot restorder när produkten inte finns i lager.<br />`Allow Qty Below 0` - Accepterar restorder när kvantiteten är under noll.<br />`Allow Qty Below 0 and Notify Customer` - Accepterar restorder när kvantiteten är under noll, men meddelar kunderna att beställningar fortfarande kan göras. |
| [!UICONTROL Enable Qty Increments] | Global | Avgör om produkten kan säljas i kvantitetssteg. Ökningar anger hur många produktartiklar som måste köpas som en enda produkt och som underordnade till konfigurerbara, grupperade och paketerade produkter. |

>[!NOTE]
>
>Enkel produktkonfiguration åsidosätter konfigurerbara produktkonfigurationer för en viss produkt.
