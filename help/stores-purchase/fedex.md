---
title: FedEx
description: Lär dig hur du konfigurerar FedEx som fraktfirma för din butik.
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
source-git-commit: ad5da1d77b63bf6bcc0227a5c467e369b7bb8d89
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# FedEx

FedEx är ett av världens största rederier som tillhandahåller luft-, frakt- och marktjänster med flera prioriteringsnivåer.

![Leveransalternativ för FedEx vid utcheckning](./assets/storefront-checkout-shipping-fedex.png){width="700" zoomable="yes"}

>[!NOTE]
>
>FedEx kan använda [dimensionell vikt](carriers.md#dimensional-weight) för att fastställa vissa fraktsatser. Adobe Commerce och Magento Open Source stöder dock endast viktbaserad beräkning av fraktkostnaden.

## Steg 1: Registrera dig för FedEx Web Services-produktion

FedEx-handlarkonto och registrering för FedEx Web Services Production Access krävs. När du har skapat ett FedEx-konto kan du läsa igenom informationssidan för produktionskontot och sedan klicka på länken _Hämta produktionsnyckel_ längst ned på sidan för att registrera och få en nyckel.

>[!NOTE]
>
>Se till att kopiera eller skriva ned autentiseringsnyckeln. Du måste konfigurera FedEx i leveransinställningarna för Commerce.

## Steg 2: Aktivera FedEx för Store

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Delivery Methods]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL FedEx]**.

1. Ange **[!UICONTROL Enabled for Checkout]** till `Yes`.

1. För **[!UICONTROL Title]** anger du en titel som identifierar leveransmetoden FedEx under utcheckningen.

1. Ange följande information från ditt FedEx-konto:

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Api Key]**
   - **[!UICONTROL Secret Key]**

1. Aktivera följande konfiguration om du har olika autentiseringsuppgifter för spårnings-API:

   - **[!UICONTROL Enable Tracking API credentials]**

1. Ange följande information från ditt FedEx-konto:

   - **[!UICONTROL Tracking API Key]**
   - **[!UICONTROL Tracking API Secret Key]**

1. Om du har konfigurerat en FedEx-sandlåda och vill arbeta i testmiljön anger du **[!UICONTROL Sandbox Mode]** till `Yes`.

   >[!NOTE]
   >
   >Kom ihåg att ställa in sandlådeläget på `No` när du är redo att erbjuda FedEx som en leveransmetod till dina kunder.

   ![Kontoinställningar för FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

## Steg 3: Paketbeskrivning och hanteringsavgifter

1. Ange **[!UICONTROL Pickup Type]** till den hämtningsmetod som används för försändelser.

   - `DropOff at Fedex Location` - (Standard) Anger att du släpper av leveranser på din lokala FedEx-station.
   - `Contact Fedex to Schedule` - Anger att du kontaktar FedEx för att begära en hämtning.
   - `Use Scheduled Pickup` - Anger att leveransen plockas upp som en del av en vanlig schemalagd hämtning.
   - `On Call` - Anger att hämtningen är schemalagd genom att anropa FedEx.
   - `Package Return Program` - Anger att leveransen plockas upp av FedEx Ground Package Return Program.
   - `Regular Stop` - Anger att leveransen plockas upp enligt det vanliga hämtningsschemat.
   - `Tag` - Anger att leveransupphämtningen är specifik för en Express-tagg eller markanropstaggupphämtning. Detta gäller endast för returetiketter.

1. För **[!UICONTROL Packages Request Type]** väljer du den begärantyp som bäst beskriver din inställning när en order delas upp i flera leveranser:

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. För **[!UICONTROL Packaging]** väljer du den typ av FedEx-förpackning som du vanligtvis använder för att leverera produkter från din butik.

1. Ange **[!UICONTROL Weight Unit]** till den måttenhet som används i ditt språkområde.

   - `Pounds`
   - `Kilograms`

1. Ange **[!UICONTROL Maximum Package Weight]** som tillåts för FedEx-leveranser.

   Standardmaxvikten för FedEx är 150 lbs. Kontakta din fraktfirma för mer information. Standardvärdet rekommenderas, såvida du inte har gjort speciella arrangemang med FedEx. Mer information finns i [Dimensionell vikt](carriers.md#dimensional-weight).

   ![Inställningar för FedEx-paket](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

1. Konfigurera alternativ för hanteringsavgift enligt dina behov.

   Hanteringsavgiften är valfri och visas inte vid utcheckning. Om du vill ta med en hanteringskostnad gör du följande:

   - Ange **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed Fee`
      - `Percentage`

   - För **[!UICONTROL Handling Applied]** väljer du en av följande metoder för att hantera hanteringsavgifter:

      - `Per Order`
      - `Per Package`

   - Ange **[!UICONTROL Handling Fee]** som antingen ett `fixed`-belopp eller `percentage`, beroende på beräkningsmetoden.

1. Ange **[!UICONTROL Residential Delivery]** till något av följande, beroende på om du säljer Business-to-Consumer (B2C) eller Business-to-Business (B2B).

   - `Yes` - För leveranser av B2C-boende.
   - `No` - För leveranser med B2B-boende.

   ![Inställningar för FedEx-hantering av avgift](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

## Steg 4: Tillåtna metoder och tillämpliga länder

1. Ange **[!UICONTROL Allowed Methods]** för varje leveransmetod som du vill erbjuda.

   När du väljer metoder bör du tänka på ditt FedEx-konto, frekvens och storlek för dina leveranser och om du tillåter internationella leveranser. Du kan erbjuda så många eller få metoder du vill, till exempel:

   - Europe First Priority
   - Leveransdagsalternativ: 1 dagars frakt, 2 dagars frakt, 2 dagars AM, 2 dagars frakt, 3 dagars frakt
   - Hushållsalternativ - Express Saver, Ground, First, Overnight, Home Delivery, Standard Overnight
   - Internationella alternativ - internationell ekonomi, internationell ekonomi, internationell frakt, internationell först, internationell mark, internationell prioritet
   - Prioritetsalternativ - frakt, prioritet över natten
   - Smart post-If-erbjudande med metoden Smart Post (ange **nav-ID**)
   - Alternativ för frakt - frakt, nationell frakt

1. Om du vill ange alternativet [Fri frakt](shipping-free.md) via FedEx anger du alternativ för fri frakt.

   - Ange **[!UICONTROL Free Method]** till den metod som du vill använda för fri frakt. Om du inte vill erbjuda fri frakt via FedEx väljer du `None`.

   - Ange **[!UICONTROL Enable Free Shipping Threshold]** till `Enable` om du vill kräva ett minimiorderbelopp som kvalificerar en order för fri frakt med FedEx. Ange sedan det lägsta värdet i **[!UICONTROL Free Shipping Amount Threshold]**.

   Den här inställningen liknar den för den vanliga kostnadsfria leveransmetoden, men visas i FedEx-avsnittet vid utcheckning, så att kunderna vet vilken metod som används för beställningen.

1. Ändra **[!UICONTROL Displayed Error Message]** om det behövs.

   Den här textrutan är förinställd med ett standardmeddelande, men du kan ange ett annat meddelande som du vill ska visas om FedEx inte är tillgängligt.

   ![Tillåtna leveransmetoder för FedEx ](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här leveransmetoden.

   - `Specific Countries` - När du väljer det här alternativet visas listan _Leverera till specifika länder_. Välj varje land i listan där leveransmetoden kan användas.

1. Om du vill spara en logg över all kommunikation mellan din butik och FedEx-systemet anger du **[!UICONTROL Debug]** till `Yes`.

1. Ange **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes` - Visar alla FedEx-leveransmetoder för kunder, oavsett deras tillgänglighet.
   - `No` - Visar endast de FedEx-leveransmetoder som gäller för ordern.

1. För **[!UICONTROL Sort Order]** anger du ett nummer för att bestämma i vilken ordning FedEx ska visas när den visas med andra leveransmetoder vid utcheckning.

   `0` = först, `1` = sekund, `2` = tredje och så vidare.

1. Klicka på **[!UICONTROL Save Config]**.

   ![FedEx tillämpliga länder](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Commerce deklarerar alltid det fullständiga orderpriset till FedEx vid beräkning av fraktkostnader. Det här beteendet kan inte ändras.
