---
title: Leveranser
description: Lär dig hur du skapar försändelseposter för fakturor och annullerar försändelser.
exl-id: 6df83549-ba38-43f7-aab1-dbf3f6b89d74
feature: Shipping/Delivery, Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 0%

---

# Leveranser

The _[!UICONTROL Shipments]_rutnät visar försändelseposten för alla fakturor som har förberetts för leverans. En försändelsepost kan genereras när en order [fakturerad](invoices.md) eller senare.

Adobe Commerce och Magento Open Source stöder partiell och fullständig orderleverans, med ytterligare alternativ från [Inventory management](../inventory-management/introduction.md) och tillägg från tredje part.

![Leveransrutnät](./assets/shipments.png){width="600" zoomable="yes"}

## Kolumnbeskrivningar

| Kolumn eller kontroll | Beskrivning |
|--- |--- |
| [!UICONTROL Select] | Markera kryssrutan för varje citat som ska bli föremål för en åtgärd, eller använd markeringskontrollen i kolumnrubriken. Alternativ: `Select All` / `Deselect All` |
| [!UICONTROL Shipment] | Ett unikt sekventiellt nummer som tilldelas när en ny leverans sparas för första gången |
| [!UICONTROL Ship Date] | Leveransdatum |
| [!UICONTROL Order] | Unikt nummer för ordern |
| [!UICONTROL Order Date] | Datum och tid då ordern lades |
| [!UICONTROL Ship-to Name] | Namnet på den person som ordern skickas till |
| [!UICONTROL Total Quantity] | Total kvantitet artiklar att leverera |
| [!UICONTROL Action] | Visa öppnar leveransen i redigeringsläge |

{style="table-layout:auto"}

Ytterligare kolumner:

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Order Status] | Anger orderstatus |
| [!UICONTROL Purchased From] | Anger webbplatsen, butiken och butiksvyn där beställningen placerades |
| [!UICONTROL Customer Name] | Namnet på den kund eller köpare som lade ordern |
| [!UICONTROL Email] | E-postadressen till en registrerad kund |
| [!UICONTROL Customer Group] | Namnet på den kundgrupp eller delade katalog som kunden är tilldelad till |
| [!UICONTROL Billing Address] | Namnet på den kund eller köpare som lade ordern |
| [!UICONTROL Shipping Address] | Namnet på den person som ordern skickas till |
| [!UICONTROL Payment Method] | Betalningsmetoden som ska användas för ordern |
| [!UICONTROL Shipping Information] | Den metod som ska användas för att skicka ordern |

{style="table-layout:auto"}

## Skapa en leverans

Följ instruktionerna nedan om du vill skapa en leverans i Adobe Commerce eller Magento Open Source. Om du har aktiverat Inventory management kan du behöva granska [Skapa leveranser med flera källor](../inventory-management/shipments-create.md) och välj en källa (eller plats) och en kvantitet som ska skickas per radartikel.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Leta reda på ordningen i rutnätet och öppna den.

1. Om ordern är betald, fakturerad och klar att skickas klickar du på **[!UICONTROL Ship]**.

   Avsnitten högst upp i leveransen innehåller namn, adress och betalningsinformation från försäljningsordern.

1. Fyll i varje avsnitt i leveransformuläret enligt instruktionerna i följande avsnitt.

### [!UICONTROL Items to Ship]

För varje radartikel i ordningen ändrar du **[!UICONTROL Qty to Ship]** efter behov.

### [!UICONTROL Shipping Information]

**Metod 1:** Använda ordersidan

1. På _Administratör_ sidebar, gå till **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. I **[!UICONTROL Action]** kolumn för vald ordning, klicka **[!UICONTROL View]**.

1. Klicka på **[!UICONTROL Ship]**.

1. Bläddra nedåt till _[!UICONTROL Payment & Shipping Method]_blockera och klicka **[!UICONTROL Add Tracking Number]**.

1. Ange **[!UICONTROL Carrier]**:

   - `Custom Value`
   - `DHL`
   - `Federal Express`
   - `United Parcel Service`
   - `United States Postal Service`

1. Om du vill spåra leveransen anger du **[!UICONTROL Title]** och **[!UICONTROL Number]** .

**Metod 2:** Använda försändelsesidan

Den här metoden tillåts bara om orderleveransen redan har skapats från ordersidan.
Du kan ändra frakt- och spårningsinformation efter behov med hjälp av direktutleveranssidan:

1. På _Administratör_ sidebar, gå till **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Hitta och öppna leveransen i redigeringsläge.

1. Bläddra nedåt till _[!UICONTROL Payment & Shipping Method]_-block.

1. Välj **[!UICONTROL Carrier]**.

1. Ange en **[!UICONTROL Title]** för paketet.

1. Ange spårning **[!UICONTROL Number]**.

1. Klicka på **[!UICONTROL Add]**.

1. Om du vill skicka ett e-postmeddelande med spårningsinformation till kunden klickar du på **[!UICONTROL Send Tracking Information]** och bekräfta åtgärden.

   Om du vill spåra platsen för en leverans öppnar du den önskade leveransen i redigeringsläge och klickar på **[!UICONTROL Track this shipment]**.

   ![Leverans- och spårningsinformation](./assets/tracking-information.png){width="600" zoomable="yes"}

### Knappar

| Knapp | Beskrivning |
|--- |--- |
| **[!UICONTROL Back]** | Stänger formuläret Ny utleverans och återgår till ordern |
| **[!UICONTROL Submit Shipment]** | Lägger till leveransen för ordern. |
| **[!UICONTROL Reset]** | Återställer alla fält till ursprungsvärdena. |

{style="table-layout:auto"}

### Leveranskommentarer

1. Retur **Kommentar** för transporten, om det behövs.

1. När leveransen är klar klickar du **Skicka utleverans**.

## Ställ in kommentarer för leveranser

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Under _[!UICONTROL Sales]_väljer du **[!UICONTROL Sales Email]**.

1. Expandera **Leveranskommentarer** och ändra inställningarna efter behov:

   ![Konfiguration av leveranskommentar](../configuration-reference/sales/assets/sales-emails-shipment-comments.png){width="600" zoomable="yes"}

   - The **[!UICONTROL Enabled]** option is set to `Yes` som standard, vilket innebär att e-postmeddelandet skickas till en kund när en leveranskommentar anges.

   - För **[!UICONTROL Shipment Comment Email Sender]** väljer du den person från vilken e-postmeddelandet med försändelsekommentarer skickas. Standardinställningen har fem e-postadresser.

   - För **[!UICONTROL Shipment Comment Email Template]** väljer du mallen utifrån dina behov eller standardalternativet.

   - För **[!UICONTROL Shipment Comment Email Template for Guests]** väljer du den mall som ska användas för kunder som inte har något konto i din butik.

   - För **[!UICONTROL Shipment Comment Email Copy To]** anger du e-postadresserna för att skicka en e-postkopia av en försändelsekommentar. Avgränsa flera e-postadresser med komma.

   - För **[!UICONTROL Shipment Comment Email Copy Method]**, markera `bcc` (blind kopia) eller `separate email copy` baserat på dina önskemål.

1. Klicka på **[!UICONTROL Save Config]**.

## Avbryt en leverans

Innan en försändelse skickas till en transportör kan den avbrytas genom att man öppnar ordern och navigerar till försändelsen, förutsatt att transportören stöder annulleringar. Vissa transportföretag begränsar eller begränsar annulleringar efter en bokning. UPS tillåter till exempel annulleringar, men kräver att du väntar 24 timmar efter att leveransen har bokförts. Om en leverans avbryts kan annulleringen inte återföras. Det enda sättet är att återskapa ordern.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Hitta ordningen i rutnätet.

1. I _Åtgärd_ kolumn, välja **[!UICONTROL View]**.

1. Välj **[!UICONTROL Shipments]**.

   Om leveransen kan avbrytas _[!UICONTROL Cancel Shipment]_visas som ett alternativ i det övre knappfältet.

1. Klicka på **[!UICONTROL Cancel Shipment]**.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

Status för leveransen ändras till `Canceled`. Om transportören inte stöder annulleringar visas ett felmeddelande som förklarar varför leveransen inte kunde avbrytas.

## Beskrivningar av leveransfält

### [!UICONTROL Shipping Information]

| Fält | Beskrivning |
|-----|-----------|
| [!UICONTROL Carrier] | Namnet på den valda transportören |
| [!UICONTROL Title] | Ett beskrivande namn som tilldelats paketet av transportören. |
| [!UICONTROL Number] | Det länkade spårningsnumret som är tilldelat paketet. |
| [!UICONTROL Action] | ![Kontrollkanarikon](../assets/icon-delete-trashcan-solid.png) - Tar bort paketinformationen från försändelseposten. |
| [!UICONTROL Add] | Lägg till ett annat paket till leveransen. |

{style="table-layout:auto"}

### [!UICONTROL Route Information]

| Fält | Beskrivning |
|-----|-----------|
| [!UICONTROL Origin Location] | Visar en lista över tillgängliga platser. |
| [!UICONTROL International] | Om det här alternativet är markerat identifieras leveransen som en internationell transport. |

{style="table-layout:auto"}

### [!UICONTROL Items Ordered]

| Fält | Beskrivning |
|-----|-----------|
| [!UICONTROL Description] | Beskrivningen av artikeln. |
| [!UICONTROL SKU] | Lagerhållningsenheten för artikeln. |
| [!UICONTROL Weight] | Artikelns vikt. |
| [!UICONTROL Qty Ordered] | Kvantiteten för artikeln som beställts. |
| [!UICONTROL Qty Shipped] | Kvantiteten artiklar som har levererats. |
| [!UICONTROL Qty Packed] | Antalet objekt som ingår i det här paketet. |

{style="table-layout:auto"}

### [!UICONTROL Shipment Comments]

| Fält | Beskrivning |
|-----|-----------|
| [!UICONTROL Comments] | Kommentarer om leveransen är avsedda för internt bruk. |

{style="table-layout:auto"}

### [!UICONTROL Documentation]

| Fält | Beskrivning |
|-----|-----------|
| [!UICONTROL Package Label] | **PNG** - Hämta etiketten för försändelsepaketet. Storlek: A6 (105 x 148 mm; 4,1 x 5,6 tum) |

{style="table-layout:auto"}
