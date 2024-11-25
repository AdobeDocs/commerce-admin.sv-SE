---
title: Skatteriktlinjer per land
description: Granska rekommenderade skatteinställningar utifrån land.
exl-id: 027da0a2-0ff4-40a7-9b9c-eefad888bb7a
feature: Taxes
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '1311'
ht-degree: 0%

---

# Skatteriktlinjer per land

## Amerikansk momskonfiguration

Dessa rekommenderade inställningar kan användas för de flesta momskonfigurationer för butiker i USA.

| Momsalternativ | Rekommendation |
|--- |--- |
| Läs in katalogpriser | exklusive moms |
| FPT | Nej, eftersom FPT inte beskattas. |
| Moms baserad på | Leveransursprung |
| Skatteberäkning | På totalt |
| Fraktfritt? | Nej |
| Använd rabatt | Före moms |
| Kommentar | Alla momszoner har samma prioritet, och helst en zon för delstat och en eller flera zoner för postkodsökning. |

{style="table-layout:auto"}

### Skatteklasser

| Skatteklass | Rekommenderad inställning |
|--- |--- |
| Skatteklass för leverans | Ingen |

{style="table-layout:auto"}

### Beräkningsinställningar

| Alternativ | Rekommenderad inställning |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Origin` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### Beräkning av standardmomsmål

| Alternativ | Rekommenderad inställning |
|--- |--- |
| [!UICONTROL Default Country] | `United States` |
| [!UICONTROL Default State] | Stat där företaget finns. |
| [!UICONTROL Default Post Code] | Postnumret som används i dina skattezoner. |

{style="table-layout:auto"}

### Prisvisningsinställningar

| Alternativ | Rekommenderad inställning |
|--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | `Excluding Tax` |
| [!UICONTROL Display Shipping Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### Visningsinställningar för varukorg

| Alternativ | Rekommenderad inställning |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Display Gift Wrapping Prices] | `Excluding Tax` |
| [!UICONTROL Display Printed Card Prices] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### Beställningar, fakturor, kreditnotor och visningsinställningar

| Alternativ | Rekommenderad inställning |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### Fasta produktskatter (FPT)

| Alternativ | Rekommenderad inställning |
|--- |--- |
| [!UICONTROL Enable FPT] | `No`, utom i Kalifornien. |

{style="table-layout:auto"}

## Konfiguration av brittisk skatt

Dessa rekommenderade inställningar kan användas för de flesta momskonfigurationer för butiker i Storbritannien.

### Konfiguration av brittisk B2C-skatt

| Momsalternativ | Rekommendation |
|--- |--- |
| Läs in katalogpriser | exklusive moms |
| FPT | Ja, inklusive FPT och beskrivning |
| Moms baserad på | [!UICONTROL Shipping Address] |
| Skatteberäkning | På totalt |
| Fraktfritt? | Ja |
| Använd rabatt | Före skatt, rabatter på priser, inklusive moms. |
| Kommentar | För handlare som anger leverantörsfakturor (inklusive moms). |

{style="table-layout:auto"}

### Konfiguration av brittisk B2B-skatt

| Momsalternativ | Rekommendation |
|--- |--- |
| Läs in katalogpriser | exklusive moms |
| FPT | Ja, inklusive FPT och beskrivning |
| Moms baserad på | [!UICONTROL Shipping Address] |
| Skatteberäkning | På artikel |
| Fraktfritt? | Ja |
| Använd rabatt | Före skatt, rabatter på priser, inklusive moms. |
| Kommentar | För B2B-handlare att enklare ta hänsyn till momskedjan. Skatteberäkning på rad är också giltig, men kontakta din skattejurisdiktion. Installationsprogrammet förutsätter att en handlare finns i leveranskedjan och att sålda varor används av andra leverantörer för momsrabatter och så vidare. Den här definitionen gör det enkelt att ta reda på moms per artikel för snabbare rabattgenerering. <br/><br/>**_Obs!_**Vissa jurisdiktioner kräver olika avrundningsstrategier som inte stöds av Commerce och att inte alla jurisdiktioner tillåter artikel- eller radnivåskatt. |

{style="table-layout:auto"}

## Kanadensisk momskonfiguration

>[!IMPORTANT]
>
>Merchants in a GST/PST Province (Montreal) should create one tax rule and show a combined tax amount. Kontakta en behörig skattemyndighet om du har några frågor.

| Momsalternativ | Rekommendation |
|--- |--- |
| Läs in katalogpriser | exklusive moms |
| FPT | Ja, inklusive FPT, beskrivning och moms för FPT. |
| Moms baserad på | Leveransursprung |
| Skatteberäkning | På totalt |
| Fraktfritt? | Ja |
| Använd rabatt | Före moms |

{style="table-layout:auto"}

I följande exempel visas hur du ställer in GST-skattesatser för Kanada och PST-skattesatser för Saskatchewan, med skatteregler som beräknar och visar de två skattesatserna. Den här informationen innehåller ett exempel på konfiguration. Kontrollera att du har rätt skattesatser och regler för din skattejurisdiktion. När du konfigurerar skatter anger du butiksomfånget att tillämpa konfigurationen på alla tillämpliga butiker och webbplatser.

- Fast produktskatt inkluderas för relevanta varor som ett produktattribut.
- I Quebec kallas PST TVQ. Om du vill ställa in en frekvens för Quebec måste du använda TVQ som identifierare.

### Steg 1: Fullständiga inställningar för momsberäkning

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Om du vill ha en konfiguration med flera platser anger du **[!UICONTROL Store View]** till webbplatsen och lagret som är målet för konfigurationen.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Tax]**.

1. Klicka för att expandera varje avsnitt på sidan och slutföra följande inställningar:

#### Inställningar för momsberäkning

| Fält | Rekommenderad inställning |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price` (om tillgängligt) |

{style="table-layout:auto"}

#### Skatteklasser

| Fält | Rekommenderad inställning |
|--- |--- |
| [!UICONTROL Tax Class for Shipping] | `Shipping` (frakt beskattas) |

{style="table-layout:auto"}

#### Beräkning av standardskattedestination

| Fält | Rekommenderad inställning |
|--- |--- |
| [!UICONTROL Default Country] | `Canada` |
| [!UICONTROL Default State] | (i tillämpliga fall) |
| [!UICONTROL Default Postal Code] | `*` (asterisk) |

{style="table-layout:auto"}

#### Inställningar för kundvagnsvisning

| Fält | Rekommenderad inställning |
|--- |--- |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero in Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

#### Fasta produktskatter

| Fält | Rekommenderad inställning |
|--- |--- |
| [!UICONTROL Enable FPT] | `Yes` |
| Alla FPT-visningsinställningar | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `No` |

{style="table-layout:auto"}

### Steg 2: Konfigurera kanadensisk moms (GST)

Skriv ut GST-numret på fakturor och andra försäljningsdokument genom att inkludera det i namnet på tillämpliga skattesatser. GST visas som en del av GST-beloppet i alla ordersammanfattningar.

#### Hantera skattezoner och skattesatser

| Fält | Rekommenderad inställning |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-GST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `*` (asterisk) |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` (asterisk) |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### Steg 3: Ställ in kanadensisk statlig omsättningsskatt

Ställ in en annan skattesats för den tillämpliga provinsen.

#### Information om momssats

| Fält | Rekommenderad inställning |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-SK-PST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `Saskatchewan` |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` (asterisk) |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### Steg 4: Skapa en momsregel

Om du vill undvika att momsen blandas och visa den beräknade momsen som separata radobjekt för GST och PST, anger du olika prioriteter för varje regel och markerar kryssrutan **Beräkna endast för delsumma**. Varje moms visas som en separat radartikel, men momsbeloppen är inte sammansatta.

#### Information om momsregel

| Fält | Rekommenderad inställning |
|--- |--- |
| Namn | `Retail-Canada-GST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-GST` |
| [!UICONTROL Priority] | `0` |
| [!UICONTROL Calculate off subtotal only] | Markera kryssrutan. |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### Steg 5: Skapa en PST-momsregel för Saskatchewan

För den här momsregeln måste du ange prioriteten till 0 och markera kryssrutan **Beräkna endast för delsumma**. Varje moms visas som en separat radartikel, men momsbeloppen är inte sammansatta.

#### Information om momsregel

| Fält | Rekommenderad inställning |
|--- |--- |
| [!UICONTROL Name] | `Retail-Canada-PST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-SK-PT` |
| [!UICONTROL Priority] | `1` |
| [!UICONTROL Calculate off subtotal only] | Markera kryssrutan. |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### Steg 6: Spara och testa resultaten

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

1. Gå tillbaka till butiken och skapa en exempelordning för att testa resultaten.

## EU-momskonfiguration

I följande exempel visas en butik baserad i Frankrike som säljer mer än 100 kB i Frankrike och mer än 100 kB i Tyskland.

- Skatteberäkningar hanteras på webbplatsnivå.
- Valutakonverterings- och momsvisningsalternativen styrs individuellt i butiksvyn (markera kryssrutan Använd webbplats om du vill åsidosätta standardinställningen).
- Genom att ange standardland för skatt kan du dynamiskt visa rätt skatt för jurisdiktionen.
- Fast produktskatt inkluderas för relevanta varor som ett produktattribut.
- Du kan behöva redigera katalogen för att den ska visas i rätt kategori/webbplats/butiksvy.

### Steg 1: Skapa tre produktskatteklasser

I det här exemplet antas att det inte behövs flera momsreducerade produktskatteklasser.

1. Skapa en momsklass.

1. Skapa en momsreducerad produktskatalog.

1. Skapa en momsfri produktklass.

### Steg 2: Skapa skattesatser för Frankrike och Tyskland

Skapa följande skattesatser:

| Skattesatser | Inställningar |
|--- |--- |
| France-StandardVAT | Land: Frankrike <br/>Delstat/region: * <br/>Postnummer: * <br/>Andel: 20 % |
| Frankrike-reduceradmoms | Land: Frankrike <br/>Delstat/region: * <br/>Postnummer: * <br/>Rate: 5 % |
| Tyskland - StandardVAT | Land: Tyskland <br/>Delstat/region: * <br/>Postnummer: * Hastighet: 19 % |
| Tyskland-reduceradMoms | Land: Tyskland <br/>Delstat/region: * <br/>Postnummer: * <br/>Kurs: 7 % |

{style="table-layout:auto"}

### Steg 3: Ange momsregler

Skapa följande momsregler:

| Skatteregler | Inställningar |
|--- |--- |
| Retail-France-StandardVAT | Kundklass: Butikskund <br/>Skatteklass: moms-standard <br/>Momssats: Frankrike-StandardMoms <br/>Prioritet: 0 <br/>Sorteringsordning: 0 |
| Retail-France-ReducedVAT | Kundklass: Butikskund <br/>Momsklass: Moms reducerad <br/>Momssats: Frankrike-reduceradMoms <br/>Prioritet: 0 <br/>Sorteringsordning: 0 |
| Retail-Germany-StandardVAT | Kundklass: Butikskund <br/>Skatteklass: moms-standard <br/>Momssats: Tyskland-StandardMoms <br/>Prioritet: 0 <br/>Sorteringsordning: 0 |
| Retail-Germany-ReducedVAT | Kundklass: Butikskund <br/>Skatteklass: Momsreducerad <br/>Momssats: tysk-reduceradMoms <br/>Prioritet: 0 <br/>Sorteringsordning: 0 |

{style="table-layout:auto"}

### Steg 4: Konfigurera en butiksvy för Tyskland

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**på sidofältet_ Admin _.

1. Skapa en butiksvy för **[!UICONTROL Germany]** under standardwebbplatsen.

1. Gör sedan följande:

   - Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

   - I det övre vänstra hörnet anger du **[!UICONTROL Default Config]** till den franska butiken.

   - Expandera ![Expanderingsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Countries Options]** på sidan Allmänt och ange standardlandet till `France`.

   - Slutför språkinställningarna efter behov.

1. Välj tyska **[!UICONTROL Store View]** i det övre vänstra hörnet.

1. På sidan _Allmänt_ expanderar du ![Expansionsväljaren](../assets/icon-display-expand.png) **[!UICONTROL Countries Options]** och anger standardlandet till `Germany`.

1. Slutför språkinställningarna efter behov.

### Steg 5: Konfigurera skatteinställningar för Frankrike

Ange följande allmänna skatteinställningar:

| Fält | Rekommenderad inställning |
|--- |--- |
| [[!UICONTROL Tax Classes]](../configuration-reference/sales/tax.md#tax-classes) |  |
| [!UICONTROL Tax Class for Shipping] | `Shipping` (frakt beskattas) |
| [[!UICONTROL Calculation Settings]](../configuration-reference/sales/tax.md#calculation-settings) |  |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Including Tax` |
| [!UICONTROL Shipping Prices] | `Including Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Including Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price if available` |
| [[!UICONTROL Default Tax Destination Calculation]](../configuration-reference/sales/tax.md#default-tax-destination-calculation) |  |
| [!UICONTROL Default Country] | `France` |
| [!UICONTROL Default State] |  |
| [!UICONTROL Default Postal Code] | `*` (asterisk) |
| [[!UICONTROL Fixed Product taxes]](../configuration-reference/sales/tax.md#fixed-product-taxes) |  |
| [!UICONTROL Enable FPT] | `Yes` |
| [!UICONTROL All FPT Display Settings] | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `Yes` |

{style="table-layout:auto"}

### Steg 6: Konfigurera skatteinställningar för Tyskland

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. I det övre högra hörnet anger du **[!UICONTROL Store View]** till vyn till den tyska butiken och klickar på **[!UICONTROL OK]** för att bekräfta.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Tax]**.

1. Gör följande i avsnittet **[!UICONTROL Default Tax Destination Calculation]**:

   - Avmarkera kryssrutan **[!UICONTROL Use Website]** efter varje fält,

   - Uppdatera följande värden om du vill matcha webbplatsens leveransinställningar [punkt ](shipping-settings.md#point-of-origin):

      - Standardland
      - Standardläge
      - Standardpostnummer

     Den här inställningen ser till att momsen beräknas korrekt när produktpriserna inkluderar moms.

     ![Beräkning av standardmomsmål](./assets/destination-calc-french.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
