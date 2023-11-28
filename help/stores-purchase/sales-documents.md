---
title: Försäljningsdokument
description: Lär dig hur du konfigurerar säljdokument för att stödja kundorder och leveranser för din Commerce Store.
exl-id: 869d79ca-688a-4032-a95c-c66ebf7f2775
feature: Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Försäljningsdokument

För att stödja orderarbetsflödet och ge kunderna dokumentation om de order de skickar in, ska du konfigurera de relaterade säljdokumenten så att de speglar ert butiksmärke och inkludera referensinformation.

## Konfigurera fakturor och följesedlar

Till skillnad från logotypbilderna som används på butikssidor kan logotypen för PDF-fakturor och andra säljdokument vara en högupplöst bild på 300 dpi. Tänk på att bevara proportionerna när du ändrar storlek på logotypen. Ändra storlek på logotypen så att den passar höjden och oroa dig inte för något oanvänt utrymme till höger.

![Exempellogotyp](./assets/logo-pdf.png){width="200"}

Ett sätt att ändra storlek på logotypen så att den passar den önskade storleken är att skapa en ny, tom bild med rätt dimensioner. Klistra sedan in logotypbilden och ändra storleken så att den passar höjden. I de flesta bildredigeringsprogram kan du antingen skala den i procent för att bevara proportionerna eller hålla ned Skift och manuellt ändra storlek på bilden.

**_Så här uppdaterar du logotypen:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Sales]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Invoice and Packing Slip Design]** och gör följande:

   ![Försäljningskonfiguration - design av försäljningsfaktura och följesedel](../configuration-reference/sales/assets/sales-invoice-packing-slip-design.png){width="600" zoomable="yes"}

   - Ladda upp **[!UICONTROL Logo for PDF Print-outs]**, klicka **[!UICONTROL Choose File]**, hitta logotypen som du har förberett och klicka på **[!UICONTROL Open]**.

   - Ladda upp **[!UICONTROL Logo for HTML Print View]**, klicka **[!UICONTROL Choose File]**, hitta logotypen som du har förberett och klicka på **[!UICONTROL Open]**.

   - Ange din adress som du vill att den ska visas på fakturor och följesedlar.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

   Som referens visas en miniatyrbild av den överförda bilden före varje fält. Oroa dig inte om miniatyrbilden ser förvrängd ut. Logotypens andel är korrekt på fakturan.

### Ersätta en bild

1. Klicka **[!UICONTROL Choose File]** och väljer en annan logotypfil.

1. Välj **[!UICONTROL Delete Image]** kryssrutan för den bild som du vill ersätta.

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

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL PDF Print-outs]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **Faktura** -avsnitt.

1. Ange **[!UICONTROL Display Order ID in Header]** enligt dina önskemål.

1. Upprepa för **[!UICONTROL Shipment]** och **[!UICONTROL Credit Memo]** -avsnitt.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

**_Så här ändrar du inställningen för kundens IP-adress:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Sales]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL General]** -avsnitt.

   ![Försäljningskonfiguration - allmänna försäljningsinställningar](../configuration-reference/sales/assets/sales-general.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Hide Customer IP]** efter dina önskemål.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
