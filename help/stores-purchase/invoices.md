---
title: Fakturor
description: Lär dig hur du skapar och skriver ut fakturor som stöder orderbehandling och kundserviceåtgärder.
exl-id: 6141b182-1467-4416-a07f-864333318428
feature: Invoices, Admin Workspace
source-git-commit: 80cc27c4247230eb5e43bca46a34d358f9f0bcea
workflow-type: tm+mt
source-wordcount: '1181'
ht-degree: 0%

---

# Fakturor

En faktura är en post för betalningsposten för en order. Flera fakturor kan [skapas](#create-an-invoice) för en enda order, och var och en kan innehålla så många eller några av de köpta produkterna som du anger. Du kan också skapa [utskriftsklara PDF-fakturor](#print-invoices) som försäljningsdokument för dina kunder.

Gå till _>_&#x200B;Åtgärder **[!UICONTROL Sales]** > _Fakturor_ på sidofältet **Admin** för att öppna rutnätet _Fakturor_ och få tillgång till dina skapade fakturor.

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

Vanligtvis faktureras och hämtas beställningarna när leveransprocessen startar. Om betalningsmetoden är en inköpsorder, eller om [betalningsåtgärden](../configuration-reference/sales/payment-methods.md#payment-actions) är inställd på `Authorize and Capture`, faktureras ordern och betalningen registreras under utcheckningen. Du kan generera en faktura med en följesedel och även skriva ut fraktsetiketter från ditt transportföretagskonto. En enda order kan delas upp i partiella leveranser, som faktureras separat om det behövs.

När tillståndet för nya order är `Processing` blir alternativet _Fakturera alla objekt automatiskt_ tillgängligt i konfigurationen. Vissa betalningsmetoder för kreditkort slutför faktureringssteget som en del av processen när [betalningsåtgärden](../configuration-reference/sales/payment-methods.md#payment-actions) är inställd på `Authorize and Capture`. I så fall visas inte fakturaknappen och beställningen är klar att skickas.

>[!NOTE]
>
>Fakturor skapas inte automatiskt för order som har placerats med `Gift Card`, `Store Credit`, `Reward Points` eller andra offlinebetalningsmetoder.

En faktura för ordern måste genereras innan den kan skrivas ut. Om du vill visa eller skriva ut PDF hämtar och installerar du först en PDF-läsare, till exempel [Adobe Acrobat Reader](https://www.adobe.com/acrobat/pdf-reader.html "Hämta Adobe Reader").

**_Om du vill fakturera en order:_**

1. Gå till _>_ > **[!UICONTROL Sales]** på sidofältet _[!UICONTROL Operations]_Admin **[!UICONTROL Orders]**.

1. Hitta försäljningsordern med statusen `Processing` i rutnätet. Gör sedan följande:

1. Klicka på _i kolumnen_&#x200B;Åtgärd **[!UICONTROL View]**.

1. Välj alternativet **[!UICONTROL Invoice]** i försäljningsorderhuvudet.

   >[!NOTE]
   >
   >Alternativet _[!UICONTROL Invoice]_visas inte när [betalningsåtgärden](../configuration-reference/sales/payment-methods.md#payment-actions) för din specifika [betalningsmetod](../configuration-reference/sales/payment-methods.md) är inställd på `Authorize and Capture`, vilket automatiskt genererar en faktura. Detta gäller också om ordern har lagts och betalningsåtgärden för betalningsmetoden har angetts till `Authorize` och ordern har fakturerats.

   ![Fakturaförsäljningsorder](./assets/invoice-sales-order.png){width="700" zoomable="yes"}

   Den nya fakturasidan ser ut ungefär som en slutförd ordersida, med ytterligare fält som kan redigeras.

1. Om artiklarna är klara att skickas genererar du en följesedel för leveransen samtidigt som du skapar fakturan:

   - Markera kryssrutan _i avsnittet_ Leveransinformation **[!UICONTROL Create Shipment]**.

     Leveransposten skapas samtidigt som fakturan genereras.

   - Inkludera ett spårningsnummer:

      - Klicka på **[!UICONTROL Add Tracking Number]**.
      - Ange spårningsinformationen: _[!UICONTROL Carrier]_,_[!UICONTROL Title]_ och _[!UICONTROL Number]_

     ![Skapa en Fedex-leverans](./assets/invoice-create-shipment-fedex.png){width="600" zoomable="yes"}

   - Du kan också generera en partiell faktura:

      - I avsnittet _Artiklar till faktura_ ska du uppdatera kolumnen **[!UICONTROL Qty to Invoice]** så att den bara innehåller specifika artiklar på fakturan.
      - Klicka sedan på **[!UICONTROL Update Qty's]**.

        ![Artiklar att fakturera](./assets/invoice-items-to-invoice.png){width="600" zoomable="yes"}

1. Om en onlinebetalningsmetod användes för ordern anger du **[!UICONTROL Amount]** till lämpligt alternativ.

1. Så här meddelar du kunder via e-post när fakturan genereras:

   - Markera kryssrutan **[!UICONTROL Email Copy of Invoice]**.

   - Ange **[!UICONTROL Invoice Comments]**. Markera kryssrutan **[!UICONTROL Append Comments]** om du vill inkludera kommentarerna i e-postmeddelandet.

1. Klicka **[!UICONTROL Submit Invoice]** längst ned på sidan när du är klar.

   **_Betalningsmetod online:_**

   ![Skicka faktura - onlinebetalningsmetod](./assets/invoice-submit-invoice-capture-online.png){width="600" zoomable="yes"}

   **_Betalningsmetod offline:_**

   ![Skicka faktura - betalningsmetod offline)](./assets/invoice-submit-invoice.png){width="600" zoomable="yes"}

   Orderns status ändras från `Pending` till `Complete`.

   ![Fakturasammanfattning slutförd](./assets/invoice-complete.png){width="600" zoomable="yes"}

## Skriv ut fakturor

Fakturor kan skrivas ut individuellt eller som en batch. Innan en faktura kan skrivas ut måste den först genereras för ordern. Du kan överföra en högupplöst logotyp för en utskriftsklar PDF-faktura och inkludera [Order ID](../stores-purchase/sales-documents.md#add-reference-ids) i rubriken. Information om hur du anpassar fakturamallen med din logotyp och adress finns i [PDF logotypkrav](../stores-purchase/sales-documents.md#image-formats).

>[!NOTE]
>
>Om du vill visa eller skriva ut PDF måste du ha en PDF-läsare. Du kan ladda ned [Adobe Reader](https://www.adobe.com/acrobat/pdf-reader.html "Hämta Adobe Reader") utan kostnad.

### Skriva ut en enda faktura

1. Gå till _>_ > **[!UICONTROL Sales]** på sidofältet _[!UICONTROL Operations]_Admin **[!UICONTROL Invoices]**.

1. Leta reda på fakturan i rutnätet _[!UICONTROL Invoices]_och klicka på&#x200B;**[!UICONTROL View]**i kolumnen_&#x200B;Åtgärd _.

1. Klicka på **[!UICONTROL Print]** högst upp på fakturan för att generera en PDF av fakturan.

1. Spara den genererade PDF-filen i en fil eller skriv ut den.

### Skriva ut flera fakturor

1. Gå till _>_ > **[!UICONTROL Sales]** på sidofältet _[!UICONTROL Operations]_Admin **[!UICONTROL Invoices]**.

1. I rutnätet _[!UICONTROL Invoices]_markerar du kryssrutan för varje faktura som ska skrivas ut.

1. Ställ in kontrollen **[!UICONTROL Actions]** på `PDF Invoices`.

   ![Skriv ut flera fakturor](./assets/invoices-print-batch.png){width="600" zoomable="yes"}

Fakturorna sparas i en enda PDF-fil som kan skickas till en skrivare eller sparas.

## Anpassade fångstbelopp

[!BADGE Endast SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce as a Cloud Service-projekt (SaaS-infrastruktur som hanteras av Adobe)."}

För att ge säljarna större flexibilitet vid partiella klipp och specialiserade betalningsscenarier har API:t för faktura stöd för anpassade fångstbelopp med hjälp av tilläggsattribut.

Du kan göra REST-anrop för att hämta ett anpassat belopp när du skapar en faktura.  Använd REST-slutpunkten [`POST V1/order/:orderId/invoice`](https://developer.adobe.com/commerce/webapi/reference/rest/saas/) och ange det anpassade beloppet i fältet `extension_attributes.custom_capture_amount` i nyttolasten.

>[!NOTE]
>
>Kontakta din supportrepresentant för att aktivera den här funktionen.
>
>På grund av juridiska begränsningar är det anpassade fångstbeloppet endast tillgängligt i Nordamerika-regionen och i andra regioner där överbetalning är tillåten.
