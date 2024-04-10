---
title: United States Postal Service (USPS)
description: Lär dig hur du konfigurerar USPS som fraktfirma för din butik.
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# United States Postal Service (USPS)

United States Postal Service är en oberoende posttjänst som tillhör USA:s regering och erbjuder inrikes och internationell sjöfart på land och flyg.

## Steg 1: Öppna ett USPS-leveranskonto

Öppna en [USPS Web Tools][1] konto. När du är klar med registreringsprocessen får du ditt användar-ID och en URL till USPS-testservern.

Du kan även öppna en [USPS Web Tools][1] konto. När du är klar med registreringsprocessen får du ditt användar-ID och en URL till USPS-testservern. Mer information om webbverktygen för USPS finns i [Teknisk dokumentation][2].

## Steg 2: Aktivera USPS för din butik

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Delivery Methods]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL USPS]** -avsnitt.

   >[!NOTE]
   >
   >Om det behövs avmarkerar du **[!UICONTROL Use system value]** om du vill ändra följande inställningar enligt beskrivningen.

1. Ange **[!UICONTROL Enabled for Checkout]** till `Yes`.

1. Ange vid behov **[!UICONTROL Gateway URL]** för att få tillgång till fraktkostnaderna för USPS.

   >[!IMPORTANT]
   >
   >Från och med 24 juni 2021 kommer webbverktygen för USPS att ta bort stöd för alla osäkra HTTP-slutpunkter. Efter den här ändringen kommer alla API:er för webbverktyg att misslyckas för osäkra HTTP-slutpunkter. Se till att **[!UICONTROL Gateway URL]** använder den säkra HTTPS-slutpunkten.

   Fältet är förinställt som standard och behöver normalt inte ändras.

1. Ange en **[!UICONTROL Title]** för den här leveransmetoden som visas under utcheckningen.

1. Ange **[!UICONTROL User ID]** och **[!UICONTROL Password]** för ditt USPS-konto.

1. Ange **[!UICONTROL Mode]** till något av följande:

   - `Development` - Kör USPS i en testmiljö. När du har kört USPS i en utvecklingsmiljö måste du gå tillbaka senare och ställa in Mode på `Live`.
   - `Live` - Kör USPS i en produktionsmiljö.

## Steg 3: Slutför paketeringsbeskrivningen

1. Ange hur ordningen ska hanteras om den skickas som flera paket **[!UICONTROL Packages Request Type]** till något av följande:

   - `Divide to Equal Weight` - (En begäran) Leveransen av flera paket kan skickas som en begäran om paketen delas upp i lika stor vikt.
   - `Use Origin Weight` - (Flera ansökningar) Flera paket måste skickas som separata ansökningar om ursprunglig vikt används som underlag för beräkning av fraktkostnaden.

1. Ange **[!UICONTROL Container]** till den typ av förpackning som normalt används för att leverera produkter som beställts för din butik.

1. Ange **[!UICONTROL Size]** av det typiska paket som levererats från din butik.

1. Ange **[!UICONTROL Machinable]** till något av följande:

   - `Yes` - Om ditt typiska paket kan bearbetas av en dator.
   - `No` - Om ditt typiska paket måste behandlas manuellt.

1. Ange **[!UICONTROL Maximum Package Weight]** i enlighet med transportörens krav.

   ![Inställningar för USPS-paketering](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## Steg 4: Ställ in hanteringsavgifter

Hanteringsavgiften är valfri och visas som en extra avgift som läggs till DHL:s fraktkostnad. Om du vill ta med en hanteringskostnad gör du följande:

1. Ange **[!UICONTROL Calculate Handling Fee]** till någon av följande metoder:

   - `Fixed`
   - `Percent`

1. Ange hur hanteringsavgiften ska tillämpas **[!UICONTROL Handling Applied]** till något av följande:

   - `Per Order`
   - `Per Package`

1. Ange beloppet för **[!UICONTROL Handling Fee]** att debiteras.

   Om du vill ange ett procenttal använder du decimalformatet. Skriv till exempel `0.25` för 25 %.

   ![Hanteringsavgift för USPS](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## Steg 5: Ange tillåtna metoder och tillämpliga länder

1. För **[!UICONTROL Allowed Methods]** väljer du varje leveranssätt för USPS som ska vara tillgänglig för dina kunder.

   Metoderna visas under USPS vid utcheckning. Om du vill välja flera metoder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

1. Om du vill ange en [Fri frakt](shipping-free.md) via USPS, ange alternativ för fri frakt:

   - Ange **[!UICONTROL Free Method]** till den metod du vill använda för fri frakt. Om du inte vill erbjuda fri frakt via USPS väljer du `None`.

   - Ange ett minimiorderbelopp som berättigar till en order om fri frakt med USPS **[!UICONTROL Enable Free Shipping Threshold]** till `Enable`. Ange sedan det lägsta värdet i **[!UICONTROL Free Shipping Amount Threshold]**.

1. Ändra **[!UICONTROL Displayed Error Message]**.

   Den här textrutan är förinställd med ett standardmeddelande, men du kan ange ett annat meddelande som du vill ska visas om USPS inte är tillgängligt.

   ![Tillåtna USPS-metoder](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Ship to Applicable Countries]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här leveransmetoden.
   - `Specific Countries` - När du väljer det här alternativet visas _Leverera till specifika länder_ visas. Välj varje land i listan där leveransmetoden kan användas.

   ![USPS-länder](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Show Method if Not Applicable]** till något av följande:

   - `Yes` - Visar en lista över alla tillgängliga leveransmetoder för USPS vid utcheckning, inklusive metoder som inte gäller för leveransen.
   - `No` - Visar endast de USPS-leveransmetoder som kan användas för leveransen.

1. Om du vill skapa en loggfil med information om USPS-leveranser från din butik anger du **[!UICONTROL Debug]** till `Yes`.

1. För **[!UICONTROL Sort Order]** anger du ett nummer som bestämmer i vilken ordning USPS visas när det visas med andra leveransmetoder vid utcheckning.

   `0` = first, `1` = sekund, `2` = tredje och så vidare.

1. Klicka på **[!UICONTROL Save Config]**.


[1]: https://secure.shippingapis.com/registration/
[2]: https://www.usps.com/business/web-tools-apis/welcome.htm
