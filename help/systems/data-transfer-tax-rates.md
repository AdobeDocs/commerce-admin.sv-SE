---
title: Uppdatera momstariffdata
description: Lär dig hur du använder export- och importåtgärder för att uppdatera skattesatser för din butik.
exl-id: a3ef718d-b296-41d7-a1b8-ae8274da71b6
feature: Taxes, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 0%

---

# Uppdatera momstariffdata

Om du gör affärer i flera länder och levererar en stor mängd produkter kan det ta väldigt lång tid att ange skattesatser manuellt. Det går snabbare och effektivare att ladda ned skattesatser per postnummer och importera dem till Commerce. I följande exempel visas hur du importerar en uppsättning statsspecifika skattesatser som hämtats från en betrodd källa. Avalara tillhandahåller [tabeller för skattesatser](https://www.avalara.com/taxrates/en/download-tax-tables.html) som du kan hämta utan kostnad för varje ZIP-kod i USA.

>[!NOTE]
>
>Om du är intresserad av att automatisera din försäljning och använda skatteefterlevnad och rapportering hittar du Commerce-tillförlitliga alternativ på webbplatsen [Commerce Partners](https://solutionpartners.adobe.com/s/directory/?solution=commerce).

## Steg 1: Exportera Commerce momssatser

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import/Export Tax Rates]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Export Tax Rates]**.

1. Leta efter filen på hämtningsplatsen för webbläsaren.

1. Spara och öppna filen i ett kalkylblad.

   I det här exemplet används [!DNL OpenOffice Calc].

   Exporterade data för Commerce momssats innehåller följande kolumner:
   - Code
   - Land
   - Läge
   - Postnummer/Post
   - Hastighet
   - Intervall från
   - Intervall till
   - En kolumn för varje butiksvy

   ![Exporterade data - momssatser](./assets/data-exported-tax-rates.png){width="500" zoomable="yes"}

1. Öppna de nya momssatserna i en andra instans av kalkylbladet så att du kan se dem sida vid sida.

1. I de nya momssatserna bör du tänka på eventuella ytterligare momssatser som du kan behöva ange i din butik innan data importeras.

   Till exempel innehåller momssatserna för Kalifornien även:

   - `TaxRegionName`
   - `CombinedRate`
   - `StateRate`
   - `CountyRate`
   - `CityRate`
   - `SpecialRate`

   Om du behöver importera ytterligare [momszoner och skattesatser](../stores-purchase/tax-zones-rates.md) måste du först definiera dem från administratören för din butik och uppdatera [momsreglerna](../stores-purchase/tax-rules.md) efter behov. Exportera sedan data och öppna filen i en textredigerare så att den kan användas som referens. För att det här exemplet ska vara enkelt importerar vi bara standardkolumner för momssatser.

## Steg 2: Förbered importdata

Du har två kalkylblad öppna, sida vid sida. Den ena innehåller exportfilsstrukturen för Commerce och den andra innehåller de nya momssatserna som du vill importera.

1. Om du vill skapa en plats att arbeta på i kalkylbladet med de nya momssatserna infogar du så många tomma kolumner till höger som behövs för att lägga till data från Commerce exportfil. Använd klipp ut och klistra in för att lägga till data och sedan ordna om kolumnerna så att de matchar ordningen i Commerce exportdatafil.

1. Byt namn på kolumnrubrikerna så att de matchar Commerce exportdata.

1. Ta bort kolumner som inte har några data.

   I annat fall måste importfilens struktur matcha Commerce ursprungliga exportdata.

1. Innan du sparar filen bläddrar du nedåt och ser till att momskolumnerna bara innehåller numeriska data.

   All text som finns i en kolumn för skattesats förhindrar att data importeras.

1. Spara förberedda data som en .CSV-fil.

   Kontrollera att ett komma används som fältavgränsare och dubbla citattecken som textavgränsare när du uppmanas att göra det. Klicka sedan på **[!UICONTROL OK]**.

## Steg 3: Importera skattesatser

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import/Export Tax Rates]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Choose File]** och välj den CSV-momstarifffil som du förberedde för import.

1. Klicka på **[!UICONTROL Import Tax Rates]**.

   Det kan ta flera minuter att importera data. När processen är klar visas meddelandet `The tax rate has been imported`. Om du får ett felmeddelande rättar du till problemet i data och försöker igen.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**&#x200B;på sidofältet_ Admin _.

   Importerade frekvenser visas i listan.

1. Använd sidkontrollerna för att visa de nya momssatserna.

   ![Momssatser för dataimport](../stores-purchase/assets/tax-zones-rates.png){width="600" zoomable="yes"}

1. Kör några testtransaktioner i din butik med kunder från olika postnummer för att säkerställa att de nya skattesatserna fungerar korrekt.
