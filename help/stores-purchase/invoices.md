---
title: Fakturor
description: Lär dig hur du skapar och skriver ut fakturor som stöder orderbehandling och kundserviceåtgärder.
exl-id: 6141b182-1467-4416-a07f-864333318428
feature: Invoices, Admin Workspace
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# Fakturor

En faktura är en post för betalningsposten för en order. Flera fakturor kan [skapad](#create-an-invoice) för en och samma beställning och kan innehålla så många eller några av de köpta produkterna du anger. Du kan också skapa [utskriftsklara PDF-fakturor](#print-invoices) som säljdokument för era kunder.

På _Administratör_ sidebar, gå till **[!UICONTROL Sales]** > _Operationer_ > **Fakturor** för att öppna _Fakturor_ och få tillgång till dina skapade fakturor.

![Fakturarutnät](./assets/invoices.png){width="700" zoomable="yes"}

## Kolumnbeskrivningar

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Select] | Markera kryssrutorna för de citattecken som ska bli föremål för en åtgärd, eller använd markeringskontrollen i kolumnrubriken. Alternativ: `Select All` / `Deselect All` |
| [!UICONTROL Invoice] | En unik numerisk identifierare som tilldelas när en faktura skickas från administratören. När du visar fakturainformationen visas numret högst upp på sidan i stället för offertnamnet. |
| [!UICONTROL Invoice Date] | Datum och tid då administratören först skickade fakturan. |
| [!UICONTROL Order#] | En unik numerisk identifierare som tilldelas när en order placeras av en köpare. När du visar fakturainformationen visas det här numret som en länk i blocket med beställnings- och kontoinformation. |
| [!UICONTROL Order Date] | Datum och tid då kunden först lyckades lägga en order. |
| [!UICONTROL Bill-to Name] | Namnet på den person som är ansvarig för att betala för ordern. |
| [!UICONTROL Status] | Anger det aktuella tillståndet för en faktura. Statusen kan endast ändras genom åtgärder från antingen köparen eller säljaren. |
| [!UICONTROL Grand Total (Base)] | Det totala priset på produkter som ska köpas. Det totala beloppet visas i webbplatsens basvaluta och i butikens valuta. |
| [!UICONTROL Grand Total (purchase)] | Summan av inköpta produkter i ordern. Det totala beloppet visas i webbplatsens basvaluta och i butikens valuta. |
| [!UICONTROL Purchased From] | Vyn för webbplats/butik/butik som fakturan skapades från. |
| [!UICONTROL Billing Address] | Faktureringsadressen till den kund som beställde. |
| [!UICONTROL Shipping Address] | Den adress dit ordern ska skickas. |
| [!UICONTROL Customer Name] | Förnamn och efternamn på den kund som tar emot fakturan. |
| [!UICONTROL Email] | E-postadressen till den kund som tar emot fakturan. |
| [!UICONTROL Customer Group] | Kundgruppen som tilldelats kunden som tar emot fakturan. |
| [!UICONTROL Payment Method] | Betalningsmetoden som ska användas för betalningen. |
| [!UICONTROL Shipping Information] | Den metod som ska användas för att skicka ordern. |
| [!UICONTROL Subtotal] | Delsumman för beställningen, utan frakt och expeditionsavgift. |
| [!UICONTROL Shipping and Handling] | Belopp som debiteras för frakt och hantering. |
| [!UICONTROL Action] | **[!UICONTROL View]** - öppnar fakturan i redigeringsläge. |

{style="table-layout:auto"}

## Skapa en faktura

Om du skapar en faktura för en order flyttas den till ett läge där den inte kan annulleras eller ändras. En ny fakturasida ser ut ungefär som en slutförd order med ytterligare fält. Alla aktiviteter som är relaterade till en order beskrivs i kommentarsavsnittet på fakturan.

Vanligtvis faktureras och hämtas beställningarna när leveransprocessen startar. Om betalningssättet är en inköpsorder, eller om [betalningsåtgärd](../configuration-reference/sales/payment-methods.md#payment-actions) är inställd på `Authorize and Capture`, beställningen faktureras och betalningen registreras under utcheckningen. Du kan generera en faktura med en följesedel och även skriva ut fraktsetiketter från ditt transportföretagskonto. En enda order kan delas upp i partiella leveranser, som faktureras separat om det behövs.

När status för nya order är inställd på `Processing`, alternativet att _Fakturera alla artiklar automatiskt_ blir tillgängligt i konfigurationen. Vissa betalningsmetoder för kreditkort slutför faktureringssteget som en del av processen när [betalningsåtgärd](../configuration-reference/sales/payment-methods.md#payment-actions) är inställd på `Authorize and Capture`. I så fall visas inte fakturaknappen och beställningen är klar att skickas.

>[!NOTE]
>
>Fakturor skapas inte automatiskt för order som läggs med `Gift Card`, `Store Credit`, `Reward Points`eller andra offlinebetalningsmetoder.

En faktura för ordern måste genereras innan den kan skrivas ut. Om du vill visa eller skriva ut PDF måste du först ladda ned och installera en läsare för PDF som [Adobe Acrobat Reader][1].

**_Så här fakturerar du en order:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Hitta försäljningsordern med statusen `Processing` i rutnätet. Gör sedan följande:

1. I _Åtgärd_ kolumn, klicka **[!UICONTROL View]**.

1. I försäljningsorderns huvud väljer du **[!UICONTROL Invoice]** alternativ.

   >[!NOTE]
   >
   >The _[!UICONTROL Invoice]_alternativet visas inte när [betalningsåtgärd](../configuration-reference/sales/payment-methods.md#payment-actions) för just [betalningsmetod](../configuration-reference/sales/payment-methods.md) är inställd på `Authorize and Capture`, som automatiskt genererar en faktura. Detta gäller även om ordern läggs och betalningsåtgärden för betalningsmetoden är inställd på `Authorize` och ordern faktureras.

   ![Fakturaförsäljningsorder](./assets/invoice-sales-order.png){width="700" zoomable="yes"}

   Den nya fakturasidan ser ut ungefär som en slutförd ordersida, med ytterligare fält som kan redigeras.

1. Om artiklarna är klara att skickas genererar du en följesedel för leveransen samtidigt som du skapar fakturan:

   - I _Leveransinformation_ klickar du på **[!UICONTROL Create Shipment]** för att markera den.

     Leveransposten skapas samtidigt som fakturan genereras.

   - Inkludera ett spårningsnummer:

      - Klicka på **[!UICONTROL Add Tracking Number]**.
      - Ange spårningsinformation: _[!UICONTROL Carrier]_,_[!UICONTROL Title]_ och _[!UICONTROL Number]_

     ![Skapa en Fedex-leverans](./assets/invoice-create-shipment-fedex.png){width="600" zoomable="yes"}

   - Du kan också generera en partiell faktura:

      - I _Artiklar att fakturera_ -avsnittet, uppdatera **[!UICONTROL Qty to Invoice]** -kolumn som bara ska innehålla specifika artiklar på fakturan.
      - Klicka sedan på **[!UICONTROL Update Qty's]**.

        ![Artiklar att fakturera](./assets/invoice-items-to-invoice.png){width="600" zoomable="yes"}

1. Om en onlinebetalningsmetod användes för ordern anger du **[!UICONTROL Amount]** till lämpligt alternativ.

1. Så här meddelar du kunder via e-post när fakturan genereras:

   - Välj **[!UICONTROL Email Copy of Invoice]** kryssrutan.

   - Ange **[!UICONTROL Invoice Comments]**. Om du vill inkludera kommentarerna i e-postmeddelandet markerar du **[!UICONTROL Append Comments]** kryssrutan.

1. När du är klar klickar du på **[!UICONTROL Submit Invoice]** längst ned på sidan.

   **_Onlinebetalningsmetod:_**

   ![Skicka faktura - onlinebetalningsmetod](./assets/invoice-submit-invoice-capture-online.png){width="600" zoomable="yes"}

   **_Offline-betalningsmetod:_**

   ![Skicka faktura - betalningsmetod offline)](./assets/invoice-submit-invoice.png){width="600" zoomable="yes"}

   Orderns status ändras från `Pending` till `Complete`.

   ![Sammanfattning av slutförda fakturor](./assets/invoice-complete.png){width="600" zoomable="yes"}

## Skriv ut fakturor

Fakturor kan skrivas ut individuellt eller som en batch. Innan en faktura kan skrivas ut måste den först genereras för ordern. Du kan överföra en högupplöst logotyp för en utskriftsklar PDF-faktura och inkludera [Order-ID](../stores-purchase/sales-documents.md#add-reference-ids) i sidhuvudet. Information om hur du anpassar fakturamallen med din logotyp och adress finns i [Krav för PDF-logotypen](../stores-purchase/sales-documents.md#image-formats).

>[!NOTE]
>
>Om du vill visa eller skriva ut PDF måste du ha en läsare för PDF. Du kan ladda ned [Adobe Reader][1] utan kostnad.

### Skriva ut en enda faktura

1. På _Administratör_ sidebar, gå till **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Invoices]**.

1. I _[!UICONTROL Invoices]_rutnät, leta reda på fakturan och klicka på&#x200B;**[!UICONTROL View]**i_&#x200B;Åtgärd _kolumn.

1. Klicka på längst upp på fakturan **[!UICONTROL Print]** för att generera en PDF av fakturan.

1. Spara det genererade PDF i en fil eller skriv ut den.

### Skriva ut flera fakturor

1. På _Administratör_ sidebar, gå till **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Invoices]**.

1. I _[!UICONTROL Invoices]_markerar du kryssrutan för varje faktura som ska skrivas ut.

1. Ange **[!UICONTROL Actions]** styra till `PDF Invoices`.

   ![Skriva ut flera fakturor](./assets/invoices-print-batch.png){width="600" zoomable="yes"}

Fakturorna sparas i en enda PDF-fil som kan skickas till en skrivare eller sparas.

## Felsökningsresurser

Hjälp om felsökning av fakturaproblem finns i följande _Knowledge Base för Commerce Support_ artiklar:

- [Det går inte att fakturera paketprodukter virtuellt och enkelt](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-30889-magento-patch-can-t-invoice-bundle-products-virtual-and-simple.html)
- [Fakturera utan butikskreditinformation](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31150-magento-patch-invoice-without-store-credit-info.html)
- [Moms visas på faktura med 100 % rabatt](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-22/mdva-35773-tax-appears-on-invoice-with-100-discount.html)
- [Orderfakturor skickas inte automatiskt](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-13/mdva-32545-magento-patch-order-invoices-don-t-send-automatically.html)


[1]: https://www.adobe.com/acrobat/pdf-reader.html "Skaffa Adobe Reader"
