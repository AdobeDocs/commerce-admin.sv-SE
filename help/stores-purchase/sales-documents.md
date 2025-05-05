---
title: Försäljningsdokument
description: Lär dig hur du konfigurerar säljdokument så att de kan hantera kundbeställningar och leveranser för din Commerce-butik.
exl-id: 869d79ca-688a-4032-a95c-c66ebf7f2775
feature: Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Försäljningsdokument

För att stödja orderarbetsflödet och ge kunderna dokumentation om de order de skickar in, ska du konfigurera de relaterade säljdokumenten så att de speglar ert butiksmärke och inkludera referensinformation.

## Konfigurera fakturor och följesedlar

Till skillnad från logotypbilderna som används på butikssidor kan logotypen för PDF-fakturor och andra säljdokument vara en högupplöst bild på 300 dpi. Tänk på att bevara proportionerna när du ändrar storlek på logotypen. Ändra storlek på logotypen så att den passar höjden och oroa dig inte för något oanvänt utrymme till höger.

![Exempellogotyp](./assets/logo-pdf.png){width="200"}

Ett sätt att ändra storlek på logotypen så att den passar den önskade storleken är att skapa en ny, tom bild med rätt dimensioner. Klistra sedan in logotypbilden och ändra storleken så att den passar höjden. I de flesta bildredigeringsprogram kan du antingen skala den i procent för att bevara proportionerna eller hålla ned Skift och manuellt ändra storlek på bilden.

**_Så här uppdaterar du logotypen:_**

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Sales]** under.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Invoice and Packing Slip Design]** och gör följande:

   ![Försäljningskonfiguration - design av försäljningsfaktura och följesedel](../configuration-reference/sales/assets/sales-invoice-packing-slip-design.png){width="600" zoomable="yes"}

   - Om du vill överföra **[!UICONTROL Logo for PDF Print-outs]** klickar du på **[!UICONTROL Choose File]**, letar upp logotypen som du har förberett och klickar på **[!UICONTROL Open]**.

   - Om du vill överföra **[!UICONTROL Logo for HTML Print View]** klickar du på **[!UICONTROL Choose File]**, letar upp logotypen som du har förberett och klickar på **[!UICONTROL Open]**.

   - Ange din adress som du vill att den ska visas på fakturor och följesedlar.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

   Som referens visas en miniatyrbild av den överförda bilden före varje fält. Oroa dig inte om miniatyrbilden ser förvrängd ut. Logotypens andel är korrekt på fakturan.

### Ersätta en bild

1. Klicka på **[!UICONTROL Choose File]** och välj en annan logotypfil.

1. Markera kryssrutan **[!UICONTROL Delete Image]** för bilden som du vill ersätta.

1. Klicka på **[!UICONTROL Save Config]**.

### Bildformat

| Format | Krav |
|--- |------------------------------------------|
| **_PDF_** |  |
| Filformat | JPG (JPEG), PNG, TIF (TIFF) |
| Bildstorlek | Upp till 1 080 pixlar bred x 270 pixlar hög |
| Upplösning | 300 DPI rekommenderas |
| **_HTML_** |  |
| Filformat | JPG (JPEG), PNG, GIF |
| Bildstorlek | Bestäms efter tema. |
| Upplösning | 72 eller 96 DPI |

{style="table-layout:auto"}

## Lägg till referens-ID:n

Orderns ID och kundens IP-adress kan inkluderas i rubriken för försäljningsdokument som medföljer en order. Som standard visas både beställnings-ID:t och kundens IP-adress i huvudet för fakturor, följesedlar och kreditnotor.

![Försäljningskonfiguration - utskrifter i PDF](./assets/config-sales-pdf-print-outs.png){width="600" zoomable="yes"}

**_Så här ändrar du inställningen för order-ID:_**

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL PDF Print-outs]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **Faktura**.

1. Ange **[!UICONTROL Display Order ID in Header]** enligt dina önskemål.

1. Upprepa för avsnitten **[!UICONTROL Shipment]** och **[!UICONTROL Credit Memo]**.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

**_Så här ändrar du inställningen för kundens IP-adress:_**

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Sales]** under.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL General]**.

   ![Försäljningskonfiguration - allmänna försäljningsinställningar](../configuration-reference/sales/assets/sales-general.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Hide Customer IP]** som din inställning.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
