---
title: DHL
description: Lär dig hur du konfigurerar DHL som fraktfirma för din butik.
exl-id: 765e5f90-3e93-43cf-a5bc-6132e00b506c
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# DHL

DHL erbjuder integrerade internationella tjänster och skräddarsydda, kundfokuserade lösningar för hantering och transport av brev, varor och information.

## Steg 1: Aktivera DHL

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Delivery Methods]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL DHL]**.

   >[!NOTE]
   >
   >Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för att ändra följande inställningar enligt beskrivningen.

1. Ange **[!UICONTROL Enabled for Checkout]** till `Yes`.

1. Vanligtvis kan du acceptera standardvärdet **[!UICONTROL Gateway URL]**.

   Om DHL har gett dig en alternativ URL anger du det värdet i det här fältet.

1. Använd autentiseringsuppgifterna från DHL för att fylla i följande fält:

   - **[!UICONTROL Access ID]**
   - **[!UICONTROL Password]**
   - **[!UICONTROL Account Number]**

![DHL-kontoinställningar](../configuration-reference/sales/assets/delivery-methods-dhl-account-settings.png){width="600" zoomable="yes"}

## Steg 2: Ange paketbeskrivning och hanteringsavgift

1. I listan **[!UICONTROL Content Type]** väljer du det alternativ som bäst beskriver vilken typ av paket du levererar:

   - `Documents`
   - `Non documents`

1. Konfigurera alternativ för hanteringsavgift enligt dina behov.

   Hanteringsavgiften är valfri och visas som en extra avgift som läggs till DHL:s fraktkostnad. Om du vill ta med en hanteringskostnad gör du följande:

   - För **[!UICONTROL Calculate Handling Fee]** väljer du den metod som du vill använda för att beräkna hanteringsavgifter:

      - `Fixed`
      - `Percentage`

   - För **[!UICONTROL Handling Applied]** väljer du hur du vill att hanteringsavgifterna ska tillämpas:

      - `Per Order`
      - `Per Package`

   - För **[!UICONTROL Handling Fee]** anger du beloppet som ska debiteras, baserat på den metod som du har valt för att beräkna beloppet.

     Om avgiften till exempel baseras på en fast avgift anger du beloppet i decimalform, till exempel `4.90`. Om hanteringsavgiften baseras på en procentandel av ordern anger du beloppet i procent. Om du till exempel debiterar sex procent av ordern anger du värdet som `.06`.

   - Om du vill tillåta att den totala ordervikten delas upp för att säkerställa en korrekt beräkning av fraktkostnader anger du **[!UICONTROL Divide Order Weight]** till `Yes`.

   - Ange **[!UICONTROL Weight Unit]** för paketet till något av följande:

      - `Pounds`
      - `Kilograms`

   - Ange **[!UICONTROL Size]** för ett typiskt paket till något av följande:

      - `Regular`
      - `Specific`

     Om du väljer `Specific` anger du paketets **[!UICONTROL Height]**, **[!UICONTROL Depth]** och **[!UICONTROL Width]** i centimeter.

   ![Inställningar för DHL-paket](../configuration-reference/sales/assets/delivery-methods-dhl-package-settings.png){width="600" zoomable="yes"}

## Steg 3: Ange tillåtna leveransmetoder

1. För **[!UICONTROL Allowed Methods]** väljer du de metoder du vill ska vara tillgängliga för kunderna.

   Om du vill välja flera metoder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

   Om du vill visa rätt lista över leveransmetoder måste du först ange [Ursprungsland](../configuration-reference/sales/shipping-settings.md).

1. För **[!UICONTROL Ready Time]** anger du antalet timmar efter att en order har skickats att ett paket är klart att skickas.

1. Redigera **[!UICONTROL Displayed Error Message]** efter behov.

   Det här meddelandet visas när en vald metod inte är tillgänglig.

1. Om du vill ange alternativet [Fri frakt](shipping-free.md) via DHL anger du alternativ för fri frakt.

   - För **[!UICONTROL Free Method]** väljer du den metod du vill använda för fri frakt.

   - Ange **[!UICONTROL Free Shipping Amount Threshold]**:

     `Enable` - Om du erbjuder fri frakt med minimiorder anger du **[!UICONTROL Minimum Order Amount for Free Shipping]**.

     `Disable` - Ingen DHL-leverans används för några beställningar.

     Den här inställningen liknar den för standardmetoden _Fri frakt_, men visas i DHL-avsnittet så att kunderna vet vilken metod som används för beställningen.

   - För **[!UICONTROL Free Shipping Amount Threshold]** anger du minimibeloppet för en order för att få fri frakt.

     ![Tillåtna DHL-metoder](../configuration-reference/sales/assets/delivery-methods-dhl-allowed-methods.png){width="600" zoomable="yes"}

## Steg 4: Ange vilka länder som är tillämpliga

1. Ange **[!UICONTROL Ship to Applicable Countries]** till något av följande:

   - `All Allowed Countries`
   - `Specific Countries`

   Om du levererar till specifika länder väljer du varje land i listan **[!UICONTROL Ship to Specific Countries]**.

1. Ange **[!UICONTROL Show Method if Not Applicable]**:

   `Yes` - Visar DHL som en leveransmetod vid utcheckning, även om den inte är tillämplig för ordern.

   `No` - Visar DHL som en leveransmetod vid utcheckning endast om tillämpligt.

1. Om du vill skapa en loggfil med information om DHL-leveranser som gjorts från din butik anger du **[!UICONTROL Debug]** till `Yes`.

1. För **[!UICONTROL Sort Order]** anger du ett nummer som avgör i vilken ordning DHL visas när den visas tillsammans med andra leveransmetoder vid utcheckning.

   `0` = först, `1` = sekund, `2` = tredje och så vidare.

1. Klicka på **[!UICONTROL Save Config]**.

   ![DHL-länder](../configuration-reference/sales/assets/delivery-methods-dhl-applicable-countries.png){width="600" zoomable="yes"}
