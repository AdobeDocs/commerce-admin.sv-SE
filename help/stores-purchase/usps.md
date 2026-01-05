---
title: United States Postal Service (USPS)
description: Lär dig hur du konfigurerar USPS som fraktfirma för din butik.
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
source-git-commit: c9acf475eeadcd249467e4cc89fe61d37230bd7d
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 0%

---

# United States Postal Service (USPS)

United States Postal Service är en oberoende posttjänst som tillhör USA:s regering och erbjuder inrikes och internationell sjöfart på land och flyg.

## Steg 1: Öppna ett USPS-leveranskonto

Öppna ett [USPS Web Tools][1]-konto. När du är klar med registreringsprocessen får du ditt användar-ID och en URL till USPS-testservern.

Du kan även öppna ett [USPS Web Tools][1]-konto. När du är klar med registreringsprocessen får du ditt användar-ID och en URL till USPS-testservern. Mer information om webbverktygen för USPS finns i den [tekniska dokumentationen][2] för dem.

## Steg 2: Aktivera USPS för din butik

{{$include /help/_includes/usps-api-type-configuration-note.md}}

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Delivery Methods]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL USPS]**.

   >[!NOTE]
   >
   >Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för att ändra följande inställningar enligt beskrivningen.

1. Ange **[!UICONTROL Enabled for Checkout]** till `Yes`.

1. Ange **[!UICONTROL USPS Type]** till `USPS Rest APIs` om du använder USPS REST API.

   Om du använder USPS Web Tools API anger du **[!UICONTROL USPS Type]** till `USPS Web Tools API`.

1. Om det behövs anger du **[!UICONTROL Gateway URL]** för att få åtkomst till leveranshastigheten för USPS.

   Fältet är förinställt som standard och behöver normalt inte ändras.

1. Ange en **[!UICONTROL Title]** för den här leveransmetoden som visas under utcheckningen.

1. Använd inloggningsuppgifterna från USPS för att fylla i följande fält:

   Om du använder USPS Rest API:er måste du ange följande autentiseringsuppgifter:

   - **[!UICONTROL Consumer Key]**
   - **[!UICONTROL Consumer Secret]**
   - **[!UICONTROL Pricing Options]**

   Om du använder USPS Web Tools API måste du ange följande autentiseringsuppgifter:

   - **[!UICONTROL User ID]**
   - **[!UICONTROL Password]**

1. Ange **[!UICONTROL Mode]** till något av följande:

   - `Development` - Kör USPS i en testmiljö. När du har kört USPS i en utvecklingsmiljö måste du gå tillbaka senare och ange Läge till `Live`.
   - `Live` - Kör USPS i en aktiv produktionsmiljö.

## Steg 3: Slutför paketeringsbeskrivningen

1. Om du vill avgöra hur ordningen hanteras om den skickas som flera paket anger du **[!UICONTROL Packages Request Type]** till något av följande:

   - `Divide to Equal Weight` - (en begäran) Leveransen av flera paket kan skickas som en begäran om paketen delas med lika stor vikt.
   - `Use Origin Weight` - (Flera begäranden) Flera paket måste skickas som separata begäranden om ursprunglig vikt används som underlag för beräkning av leveranskostnaden.

1. Ange **[!UICONTROL Container]** till den typ av förpackning som normalt används för att leverera produkter som beställts för din butik.

1. Ange **[!UICONTROL Size]** för det typiska paket som levererats från din butik.

1. Ange **[!UICONTROL Machinable]** till något av följande:

   - `Yes` - Om ditt typiska paket kan bearbetas av en dator.
   - `No` - Om ditt typiska paket måste bearbetas manuellt.

1. Ange **[!UICONTROL Maximum Package Weight]** enligt transportföretagets krav.

   ![Inställningar för USPS-paketering](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## Steg 4: Ställ in hanteringsavgifter

Hanteringsavgiften är valfri och visas som en extra avgift som läggs till DHL:s fraktkostnad. Om du vill ta med en hanteringskostnad gör du följande:

1. Ange **[!UICONTROL Calculate Handling Fee]** till en av följande metoder:

   - `Fixed`
   - `Percent`

1. Ange **[!UICONTROL Handling Applied]** till något av följande för att avgöra hur hanteringsavgiften tillämpas:

   - `Per Order`
   - `Per Package`

1. Ange beloppet för **[!UICONTROL Handling Fee]** som ska debiteras.

   Om du vill ange ett procenttal använder du decimalformatet. Ange till exempel `0.25` som 25 %.

   ![Hanteringsavgift för USPS](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## Steg 5: Ange tillåtna metoder och tillämpliga länder

1. För **[!UICONTROL Allowed Methods]** väljer du varje USPS-leveransmetod som är tillgänglig för dina kunder.

   Metoderna visas under USPS vid utcheckning. Om du vill välja flera metoder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

1. Om du vill ange alternativet [Fri frakt](shipping-free.md) via USPS anger du alternativ för fri frakt:

   - Ange **[!UICONTROL Free Method]** till den metod som du vill använda för fri frakt. Om du inte vill erbjuda fri frakt via USPS väljer du `None`.

   - Om du vill kräva ett minimiorderbelopp som berättigar till en order för fri frakt med USPS anger du **[!UICONTROL Enable Free Shipping Threshold]** till `Enable`. Ange sedan det lägsta värdet i **[!UICONTROL Free Shipping Amount Threshold]**.

1. Ändra **[!UICONTROL Displayed Error Message]** om det behövs.

   Den här textrutan är förinställd med ett standardmeddelande, men du kan ange ett annat meddelande som du vill ska visas om USPS inte är tillgängligt.

   ![Tillåtna USPS-metoder](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Ship to Applicable Countries]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här leveransmetoden.
   - `Specific Countries` - När du väljer det här alternativet visas listan _Leverera till specifika länder_. Välj varje land i listan där leveransmetoden kan användas.

   ![USPS-länder](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Show Method if Not Applicable]** till något av följande:

   - `Yes` - Visar en lista över alla tillgängliga USPS-leveransmetoder under utcheckning, inklusive metoder som inte gäller för leveransen.
   - `No` - Visar endast de USPS-leveransmetoder som kan användas för leveransen.

1. Om du vill skapa en loggfil med information om USPS-leveranser som gjorts från din butik anger du **[!UICONTROL Debug]** till `Yes`.

1. För **[!UICONTROL Sort Order]** anger du ett nummer som avgör i vilken ordning USPS visas när det visas med andra leveransmetoder vid utcheckning.

   `0` = först, `1` = sekund, `2` = tredje och så vidare.

1. Klicka på **[!UICONTROL Save Config]**.

[1]: https://secure.shippingapis.com/registration/
[2]: https://www.usps.com/business/web-tools-apis/welcome.htm

<!-- Last updated from includes: 2025-11-26 10:55:00 -->
