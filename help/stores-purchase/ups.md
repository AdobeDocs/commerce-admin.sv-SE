---
title: United Parcel Service (UPS)
description: Lär dig hur du konfigurerar UPS som fraktfirma för din butik.
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# United Parcel Service (UPS)

United Parcel Service (UPS) erbjuder inrikes och internationell sjöfart på land och flyg till över 220 länder.

{{ups-api}}

>[!NOTE]
>
>UPS kan använda [dimensionell vikt](carriers.md#dimensional-weight) för att fastställa vissa fraktpriser. Adobe Commerce stöder dock endast viktbaserad beräkning av fraktkostnaden.

## Steg 1: Öppna ett UPS-leveranskonto

Om du vill erbjuda dina kunder den här leveransmetoden måste du först öppna ett konto med UPS.

## Steg 2: Aktivera UPS för din butik

{{beta2-updates}}

1. På _Administratörssidlist_, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. På panelen till vänster, under **[!UICONTROL Sales]**, välja **[!UICONTROL Delivery Methods]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL UPS]** -avsnitt.

1. Ange **[!UICONTROL Enabled for Checkout]** till `Yes`.

1. För ett UPS XML-konto (standard) anger du **[!UICONTROL UPS Type]** till `United Parcel Service XML` och gör följande:

   - Ange dina UPS-autentiseringsuppgifter: **[!UICONTROL User ID]**, **[!UICONTROL Access License Number]** (det 16-siffriga UPS-kontot `Access Key`), och **[!UICONTROL Password]**

   - Ange **[!UICONTROL Mode]** till `Live` för att skicka data till UPS-leveranssystemet via en säker anslutning. (I utvecklingsläget skickas inga data via en säker anslutning.)

   - Verifiera **[!UICONTROL Gateway XML URL]** som krävs för att skicka begäranden via XML-fil.

   - Ange **[!UICONTROL Origin of the Shipment]** till den region där försändelsen kommer.

   - Om du har specialpriser för UPS anger du **[!UICONTROL Enable Negotiated Rates]** till `Yes` och ange det sexsiffriga **[!UICONTROL Shipper Number]** som tilldelats dig av UPS.

1. Ange ett UPS-standardkonto **[!UICONTROL UPS Type]** till `United Parcel Service` och gör följande:

   >[!NOTE]
   >
   >Standardtypen för United Parcel Service är schemalagd för borttagning. För nya konfigurationer bör du använda standardinställningen  `United Parcel Service XML` typ. XML-typen krävs också för att generera [fraktsedlar](shipping-labels.md).

   - Ange **[!UICONTROL Live Account]** till något av följande:

      - `Yes` - Kör UPS i produktionsläge och erbjuder UPS som en leveransmetod för dina kunder.
      - `No` - Kör UPS i testläge.

   - I **[!UICONTROL Gateway URL]** anger du den URL som används för att beräkna UPS-fraktkostnader.

     >[!IMPORTANT]
     >
     >UPS upphör med stödet för HTTP, som används i det aktuella standardvärdet (systemvärde). Rensa **[!UICONTROL Use system value]** och ändra URL:en för att använda HTTPS. Exempel: `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. För **[!UICONTROL Title]** anger du namnet på leveransalternativet så som du vill att det ska visas vid utcheckningen.

   Som standard är det här fältet inställt på `United Parcel Service`.

   ![Aktivera UPS](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## Steg 3: Slutför behållarbeskrivningen

1. Ange **[!UICONTROL Packages Request Type]** till något av följande:

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. För **[!UICONTROL Container]**, ange den typiska paketeringstyp som används för leveransen:

   - `Customer Packaging`
   - `UPS Letter Envelope`
   - `Customer Supplied Package`
   - `UPS Tube`
   - `PAK`
   - `UPS Express Box`
   - `UPS Worldwide 25 kilo`
   - `UPS Worldwide 10 kilo`
   - `Pallet`
   - `Small Express Box`
   - `Medium Express Box`
   - `Large Express Box`

1. Ange **[!UICONTROL Weight Unit]** till det system du använder för att mäta produktvikt.

   Det viktsystem som stöds av UPS varierar beroende på land. Om du är osäker, fråga UPS vilket viktsystem du ska använda. Alternativen är:

   - `LBS`
   - `KGS`

1. Ange **[!UICONTROL Destination Type]** till något av följande:

   - `Residential` - De flesta av dina leveranser är från företag till kund (B2C).
   - `Commercial` - De flesta av dina leveranser är business to business (B2B).

1. Ange **[!UICONTROL Maximum Package Weight]** tillåts av transportföretaget.

1. Ange **[!UICONTROL Pickup Method]** till något av följande:

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. Ange **[!UICONTROL Minimum Package Weight]** tillåts av transportföretaget.

   ![Behållarbeskrivning](./assets/ups2.png){width="600" zoomable="yes"}

## Steg 4: Ställ in hanteringsavgifter

Hanteringsavgiften är valfri och visas som en extra avgift som läggs till i UPS-leveranskostnaden. Om du vill ta med en hanteringskostnad gör du följande:

1. Ange **[!UICONTROL Calculate Handling Fee]** till någon av följande metoder:

   - `Fixed`
   - `Percent`

1. Ange hur hanteringsavgiften ska tillämpas **[!UICONTROL Handling Applied]** till något av följande:

   - `Per Order`
   - `Per Package`

1. Ange beloppet för **[!UICONTROL Handling Fee]** att debiteras.

   Om du vill ange ett procenttal använder du decimalformatet. Skriv till exempel `0.25` för 25 %.

   ![Hanteringsavgift](./assets/ups3.png){width="600" zoomable="yes"}

## Steg 5: Ange tillåtna metoder och tillämpliga länder

1. För **[!UICONTROL Allowed Methods]** väljer du varje UPS-leveransmetod som ska vara tillgänglig för dina kunder.

   Metoderna visas under UPS vid utcheckning. Om du vill välja flera metoder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

1. Om du vill ange en [Fri frakt](shipping-free.md) via UPS, ange alternativ för fri frakt:

   - Ange **[!UICONTROL Free Method]** till den metod du vill använda för fri frakt. Om du inte vill erbjuda fri frakt via UPS väljer du `None`.

   - Ange ett minimiorderbelopp som berättigar till en beställning för fri frakt med UPS **[!UICONTROL Enable Free Shipping Threshold]** till `Enable`. Ange sedan det lägsta värdet i **[!UICONTROL Free Shipping Amount Threshold]**.

1. Ändra **[!UICONTROL Displayed Error Message]**.

   Den här textrutan är förinställd med ett standardmeddelande, men du kan ange ett annat meddelande som du vill ska visas om UPS inte är tillgängligt.

   ![Tillåtna metoder](./assets/ups4.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Ship to Applicable Countries]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här leveransmetoden.
   - `Specific Countries` - När du väljer det här alternativet visas _Leverera till specifika länder_ visas. Välj varje land i listan där leveransmetoden kan användas.

1. Ange **[!UICONTROL Show Method if Not Applicable]** till något av följande:

   - `Yes` - Visar en lista över alla tillgängliga UPS-leveransmetoder under utcheckning, inklusive metoder som inte gäller för leveransen.
   - `No` - Visar endast UPS-leveransmetoder som kan användas för leveransen.

   ![Tillämpliga länder](./assets/ups5.png){width="600" zoomable="yes"}

1. Om du vill skapa en loggfil med information om UPS-leveranser som gjorts från din butik anger du **[!UICONTROL Debug]** till `Yes`.

1. För **[!UICONTROL Sort Order]** anger du ett nummer för att bestämma i vilken ordning UPS ska visas när de visas tillsammans med andra leveransmetoder vid utcheckning.

   `0` = first, `1` = sekund, `2` = tredje och så vidare.

1. Klicka på **[!UICONTROL Save Config]**.

## Steg 6: Ange leveransadress

1. Se till att [Butiksinformation](../getting-started/store-details.md#store-information) är klar.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och markera **[!UICONTROL Shipping Settings]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Origin]** på sidan och konfigurera leveransadressen.

   ![Försäljningskonfiguration - alternativ för leveransadress](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Handeln deklarerar inte det fullständiga orderpriset till UPS vid beräkning av fraktkostnader. Det här beteendet kan inte ändras.
