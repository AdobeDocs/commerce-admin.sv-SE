---
title: Lägg till innehåll - produkter
description: Läs mer om innehållstypen Produkter som används för att lägga till en lista med produkter i [!DNL Page Builder] stage.
exl-id: 8ef38669-a6f6-493b-b963-b0fc4e3bbff4
feature: Page Builder, Page Content, Products
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1912'
ht-degree: 0%

---

# Lägg till innehåll - produkter

Använd _Produkter_ innehållstyp för att lägga till en lista med produkter i [[!DNL Page Builder] stage](workspace.md#stage), med antingen ett rutnät eller en Carousel-layout. Använd [Lägg till innehåll - blockera](block.md) för att placera blocket på [!DNL Page Builder] och sedan placera en produktlista i blocket. Du kan också lägga till produktlistan direkt på en rad på en sida.

## Riktlinjer för användning av karusellen

Produktkarusellen är ett kraftfullt och engagerande sätt att visa upp dina produkter. För att få ut så mycket som möjligt av det rekommenderar vi följande riktlinjer:

- Lägg in produktkaruseller direkt i sidbreddsbehållare som rader, tabbar eller enkolumnslayouter. Med sidbreddslayouter får du bästa möjliga responsiva visning av dina produkter. [!DNL Page Builder] minskar antalet produkter som visas beroende på sidans bredd, inte behållarens bredd.

- Lägg inte till en produktkarusell i en smal kolumn. Som nämndes [!DNL Page Builder]Anger som standard antalet produkter som ska visas baserat på sidbredden, inte på kolumnbredden.

- Om du vill att din produktCarousel ska rulla kontinuerligt ställer du in båda **[!UICONTROL Autoplay]** och **[!UICONTROL Infinite Loop]** till `Yes`. Om Autoplay är inställt på `Yes` men Infinite Loop är inställd på `No`stoppas automatiskt vid slutet av produktlistan.

- Ange **[!UICONTROL Carousel Mode]** till `Continuous` för att markera, centrera och rulla en produkt i taget i karusellen. De andra produkterna visas i listan, men de är genomskinliga för att framhäva den centrerade produkten.

  ![Produktlista i sammanhängande karusellläge](./assets/pb-products-settings-carousel-continuous.png){width="600"}

- Om du vill visa och bläddra upp till fem produkter i taget i karusellen ska du behålla **[!UICONTROL Carousel Mode]** ange till `Default`.

  ![Produktlista i standardkarusellläge](./assets/pb-products-settings-carousel-default.png){width="600"}

Följande instruktioner visar hur du lägger till en produktlista i ett block. Du kan sedan använda en [widget](../content-design/widgets.md) om du vill placera blocket på en viss plats på en sida i din butik.

{{$include /help/_includes/page-builder-save-timeout.md}}

## Verktygslådan Produkter

| Verktyg | Ikon | Beskrivning |
| --------- | ------------- | ----------------- |
| Flytta | ![Ikonen Flytta](./assets/pb-icon-move.png){width="25"} | Flyttar produktbehållaren och dess innehåll till en annan position på scenen. |
| Inställningar | ![Ikonen Inställningar](./assets/pb-icon-settings.png){width="25"} | Öppnar _Redigera produkter_ där du kan välja produktlistan och ändra egenskaperna för behållaren. |
| Dölj | ![Dölj ikon](./assets/pb-icon-hide.png){width="25"} | Döljer den aktuella produktbehållaren och dess innehåll. |
| Visa | ![Visa ikon](./assets/pb-icon-show.png){width="25"} | Visar den dolda produktbehållaren och dess innehåll. |
| Duplicera | ![Duplicera, ikon](./assets/pb-icon-duplicate.png){width="25"} | Skapar en kopia av produktbehållaren och dess innehåll. |
| Ta bort | ![Ikonen Ta bort](./assets/pb-icon-remove.png){width="25"} | Tar bort produktbehållaren och dess innehåll från scenen. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Skapa ett produktlistblock

1. På _Administratör_ sidebar, gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Klicka på **[!UICONTROL Add New Block]**.

1. Ange **[!UICONTROL Block Title]** och **[!UICONTROL Identifier]**.

1. Välj **[!UICONTROL Store View]** där blocket ska vara tillgängligt.

1. Rulla ned och klicka **[!UICONTROL Edit with Page Builder]** eller inuti förhandsvisningsområdet för innehållet för att öppna [!DNL Page Builder] arbetsyta.

1. I [!DNL Page Builder] panel, expandera **[!UICONTROL Add Content]** och dra en **[!UICONTROL Products]** platshållare till scenen.

   ![Lägg till innehållstyp för produkter](./assets/pb-add-content-products-drag.png){width="600" zoomable="yes"}

## Konfigurera behållaren för produktlistan

Hovra över tom _Produkter_ för att visa verktygslådan och klicka på _Inställningar_ (![Ikonen Inställningar](./assets/pb-icon-settings.png){width="20"} ).

![Verktygslådan Produkter](./assets/pb-add-content-products-toolbox.png){width="500" zoomable="yes"}

Slutför _Inställningar_ enligt följande avsnitt:

### Utseende

1. Om du vill bestämma hur produktlistan ska visas på sidan väljer du en av utseendetyperna:

   | Typ | Beskrivning |
   | ---- | ----------- |
   | Produktstödraster | Visar produkterna i ett rutnät som visar fem produkter per rad (som standard), med så många rader som behövs för att visa numret som anges i **[!UICONTROL Number of Products to Display]** inställning. |
   | Product Carousel | Visar produkterna i en karusell (kallas även skjutreglage). Karusellen visar upp till fem produkter per bild. <br/><br/>**Varning om svarstider**: När du väljer det här utseendet är det bäst att lägga till innehållstypen Produkter direkt i en rad-, tabb- eller enkolumnslayout där den är responsiv, med färre produkter per sida på mindre skärmar. Om du lägger till den i innehållstyper som är smalare än sidans bredd (till exempel en smal kolumn), visar karusellen fler produkter per bildruta än vad behållaren tillåter, oavsett skärmstorlek. |

   {style="table-layout:auto"}

   ![Produktutseende](./assets/pb-products-appearances.png){width="300"}

   Om du väljer produktkarusellen måste du även konfigurera [Carousel-inställningar](#carousel-settings).

1. För **[!UICONTROL Select Products By]** väljer du metod för produktval:

   Du kan välja produkter efter kategori, SKU eller villkor. Dessa alternativ utesluter varandra. Du kan t.ex. inte markera alternativet Kategori, använda kategoriväljaren och sedan växla till alternativet Villkor för att lägga till vissa villkor. Dina produkter väljs endast baserat på vad du ställt in för _en_ av dessa tre alternativ.

   - **[!UICONTROL Category]** - Välj det här alternativet om du vill visa produkter i en vald kategori.

     ![Val av produkt per kategori](./assets/pb-products-settings_category.png){width="500"}

     När du väljer det här alternativet får du en **[!UICONTROL Category]** väljare. Klicka på pilen och gå ned för att välja vilken produktkategori som ska visas. I [!DNL Commerce] exempeldata, detaljera och välja _Kvinnor > Tops > Tests_ visar alla produkter för den kategorin.

     ![Välja en katalogkategori](./assets/pb-select-products-by-category.png){width="500"}

   - **[!UICONTROL SKU]** - Välj det här alternativet om du vill visa produkter med en eller flera SKU:er

     När du väljer det här alternativet får du en **[!UICONTROL Product SKUs]** textruta där du måste ange en kommaavgränsad lista med SKU:er som ska visas.

     ![Produktval efter SKU](./assets/pb-products-settings_sku.png){width="500"}

   - **[!UICONTROL Condition]** - Välj det här alternativet om du vill visa produkter enligt ett eller flera villkor som du anger.

     När du väljer det här alternativet finns det verktyg som du kan använda för att lägga till villkor i produkturvalet. Du kan till exempel bara välja produkter med könet inställt på Unisex.

     ![Val av produkt efter villkor](./assets/pb-products-settings_condition.png){width="500"}

     >[!NOTE]
     >
     >Om du väljer Kategori eller SKU får du tillgång till **[!UICONTROL Sort By]** alternativ för `Position`. Med det här sorteringsalternativet visas produkterna i samma ordning som de visas i katalogen.</br>
     >
     >För alternativet Kategori visas produkterna i samma ordning som de visas i katalogen när de sorteras efter position. För SKU-alternativet visar sortering efter position produkterna i den ordning som du anger dem i **[!UICONTROL Product SKUs]** textruta.

1. För **[!UICONTROL Sort By]** väljer du sorteringsordning för produkterna i listan:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | `Position` (endast för alternativ för Kategori och SKU) | När du väljer alternativet Kategori visas produkterna i samma ordning som de befinner sig i katalogen. När du väljer SKU-alternativet visas produkterna i samma ordning som SKU:erna i textrutan Produkt-SKU:er. |
   | `Newest products first` | Sorterar produkter efter det datum då de lades till i katalogen och visar produkterna med de senaste anmälningsdatumen först. |
   | `Oldest products first` | Sorterar produkterna efter det datum de lades till i katalogen och visar de produkter som har de äldsta anmälningsdatumen först. |
   | `Name: A - Z` | Sorterar produkterna i alfabetisk ordning. |
   | `Name: Z - A` | Sorterar produkterna i omvänd alfabetisk ordning. |
   | `SKU: ascending` | Sorterar produkter efter SKU i alfanumerisk ordning. |
   | `SKU: descending` | Sorterar produkter efter SKU i omvänd alfanumerisk ordning. |
   | `Stock: low stock first` | Sorterar produkter från det lägsta till det högsta tillgängliga lagret. |
   | `Stock: high stock first` | Sorterar produkter från det högsta till det lägsta tillgängliga lagret. |
   | `Price: high to low` | Sorterar produkter från högsta till lägsta pris. |
   | `Price: low to high` | Sorterar produkter från lägsta till högsta pris. |

   {style="table-layout:auto"}

   ![Produktsorteringsalternativ](./assets/pb-products-sortby.png){width="300"}

1. Ange **[!UICONTROL Number of Products to Display]** i karusellen eller rutnätet.

   Värden kan komma från `1` till `999`. Standardvärdet är `5` för ett rutnät och `20` för en karusell.

   >[!NOTE]
   >
   >Vissa produkter i inställningarna för Kategori, SKU eller Villkor kanske inte visas i produktrutnätet eller karusellen. Till exempel visas inte inaktiverade produkter, produkter som inte är synliga, produkter som inte finns i lager och produkter som är tilldelade till en annan webbplats.

   >[!IMPORTANT]
   >
   >Priserna för konfigurerbara, grupperade och paketerade (dynamiskt pris) produkter är odefinierade i administratören. Därför visas dessa produkter inte i **[!UICONTROL Preview]** om produkterna filtreras efter pris. Dessa produkter kan inte beställas korrekt i **[!UICONTROL Preview]** om de beställts till ett pris.

### Carousel-inställningar

1. Om du vill bestämma hur produkterna ska visas i karusellen väljer du **[!UICONTROL Carousel Mode]**:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | `Default` | Carousel visar som standard fem produkter per bild och minskar responsivt det antalet efter behov. |
   | `Continuous` | Carousel visar fem produkter per bild som standard (med hälften av en produkt till höger och vänster), men centrerar och rullar en produkt i taget i en oändlig slinga. Produkterna till höger och vänster om den centrerade produkten är nedtonade så att den centrala produkten markeras. |

   {style="table-layout:auto"}

   Om du växlar mellan dessa två lägen behålls övriga inställningar för Carousel, förutom **[!UICONTROL Infinite Loop]** inställning, som alltid är inställd på `Yes` i Kontinuerligt läge och fältet är inaktiverat.

   ![Carousel-inställningar](./assets/pb-products-carousel-settings.png){width="600" zoomable="yes"}

1. Om det behövs anger du **[!UICONTROL Autoplay]** alternativ till `Yes`.

   När automatisk uppspelning är aktiverat börjar karusellen rulla automatiskt när sidan läses in. Om du lämnar standardinställningen (`No`) måste kunden klicka på bildrutenavigeringen (punkter eller pilar) för att visa varje bildruta i följd.

   Om du aktiverar den här funktionen anger du **[!UICONTROL Autoplay Speed]** för att ange fördröjning i millisekunder mellan varje bildruta. Standardvärdet är `4000` (4 sekunder).

1. Om det behövs anger du **[!UICONTROL Infinite Loop]** alternativ till `Yes`.

   När oändlig slinga är aktiverad spelas bildspelet upp oändligt när sidan är öppen. Om du lämnar standardinställningen (`No`) spelas bildspelet bara upp en gång.

   >[!NOTE]
   >
   >Om du anger **[!UICONTROL Infinite Loop]** till `No` och **[!UICONTROL Autoplay]** ange till `Yes`stoppas automatiskt när antalet produkter som ska visas är slut.

1. Om det behövs anger du **[!UICONTROL Show Arrows]** alternativ till `Yes`.

   När det här alternativet är aktiverat innehåller varje bild _nästa_ och _föregående_ navigeringspilarna till vänster och höger. Om du lämnar standardinställningen (`No`) visas inte navigeringspilarna i bildrutorna.

1. Om det behövs anger du **[!UICONTROL Show Dots]** alternativ till `No`.

   När den är inställd på standardinställningen (`Yes`) visas navigeringspunkter längst ned i karusellreglaget. Om du inaktiverar den här inställningen visas inga navigeringspunkter i Carousel-reglaget.

### Avancerat

1. Om du vill styra placeringen av produktlistan i den överordnade behållaren väljer du **[!UICONTROL Alignment]**:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | `Default` | Använder den standardinställning för justering som anges i formatmallen för det aktuella temat. |
   | `Left` | Justerar listan längs den vänstra kanten på den överordnade behållaren, med hänsyn till eventuell utfyllnad som har angetts. |
   | `Center` | Justerar listan i mitten av den överordnade behållaren, med hänsyn till eventuell utfyllnad som har angetts. |
   | `Right` | Justerar listan längs den högra kanten på den överordnade behållaren, med hänsyn till eventuell utfyllnad som har angetts. |

   {style="table-layout:auto"}

1. Ange **[!UICONTROL Border]** som används på alla fyra sidor i behållaren Produkter:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | `Default` | Använder det standardkantlinjeformat som anges av den associerade formatmallen. |
   | `None` | Visar inte någon synlig indikation för behållarkanterna. |
   | `Dotted` | Behållarramen visas som en prickad linje. |
   | `Dashed` | Behållarramen visas som en streckad linje. |
   | `Solid` | Behållarramen visas som en heldragen linje. |
   | `Double` | Behållarramen visas som en dubbel linje. |
   | `Groove` | Behållarkanten visas som en utdragen linje. |
   | `Ridge` | Behållarkanten visas som en rak linje. |
   | `Inset` | Behållarramen visas som en indragen linje. |
   | `Outset` | Behållarramen visas som en startrad. |

   {style="table-layout:auto"}

1. Om du anger ett annat kantlinjeformat än `None`slutför du visningsalternativen för kantlinjer:

   | Alternativ | Beskrivning |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Ange färgen genom att välja en färgruta, klicka på färgväljaren eller genom att ange ett giltigt färgnamn eller motsvarande hexadecimalt värde. |
   | [!UICONTROL Border Width] | Ange antalet pixlar för kantlinjens bredd. |
   | [!UICONTROL Border Radius] | Ange antalet pixlar för att definiera radiens storlek som används för att runda varje hörn av kanten. |

   {style="table-layout:auto"}

1. (Valfritt) Ange namnen på **[!UICONTROL CSS classes]** från den aktuella formatmallen som ska användas för behållaren.

   Avgränsa flera klassnamn med blanksteg.

1. Ange värden i pixlar för **[!UICONTROL Margins and Padding]** för att bestämma de yttre marginalerna och den inre utfyllnaden för behållaren Produkter.

   Ange motsvarande värden i diagrammet.

   | Behållarområde | Beskrivning |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | Mängden tomt utrymme som används på ytterkanten på behållarens alla sidor. Alternativ: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Mängden tomt utrymme som används på behållarens inre kant på alla sidor. Alternativ: `Top` / `Right` / `Bottom` / `Left` |


## Spara och förhandsgranska på scenen

Klicka på i det övre högra hörnet **[!UICONTROL Save]** för att använda inställningarna och gå tillbaka till [!DNL Page Builder] arbetsyta.

Om du har konfigurerat en karusell bör den se ut ungefär som i följande exempel:

![Produktkarusell på scenen](./assets/pb-products-admin-carousel.png){width="600"}

Nu kan du använda en [widget](../content-design/widgets.md) om du vill placera det här blocket där du vill att det ska visas i butiken. Eller så kan du använda [Lägg till innehåll - blockera](block.md) om du vill lägga till blocket på en befintlig sida, flik eller block.
