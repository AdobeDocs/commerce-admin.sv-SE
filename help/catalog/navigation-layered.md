---
title: Navigering i flera lager
description: Se hur lagerstyrd navigering gör det enkelt för kunderna att hitta produkter baserat på kategori, prisintervall eller något annat tillgängligt attribut.
exl-id: 5f17528a-3593-449c-a044-98736a4ae913
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 99049260b4ff490845affd1c98fa4d2536edebd7
workflow-type: tm+mt
source-wordcount: '1303'
ht-degree: 0%

---

# Navigering i flera lager

>[!NOTE]
>
>Den standardnavigering i lager som beskrivs i det här avsnittet skiljer sig från filtrerad navigering i Live Search med [facets](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/facets/facets.html).

Navigering i flera lager gör det enkelt att hitta produkter baserat på kategori, prisintervall eller något annat tillgängligt attribut. Navigering med flera lager visas vanligtvis i den vänstra kolumnen med sökresultat och kategorisidor och ibland på hemsidan. Standardnavigeringen innehåller en _Shop By_-lista med kategorier och prisintervall. Du kan konfigurera visningen av lagerstyrd navigering, inklusive produktantal och prisintervall.

![Navigering i lager per kategori och pris](./assets/navigation-layered-basic.png){width="700" zoomable="yes"}

## Filterbara attribut

>[!NOTE]
>
>De filterbara attributkraven som beskrivs i det här avsnittet skiljer sig åt för [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html). Mer information finns i [Fasetter](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/facets/facets.html).

Navigering i flera lager kan användas för att söka efter produkter efter kategori eller attribut. När en kund t.ex. väljer kategorin Mens/Korts i den övre navigeringen innehåller de inledande resultaten alla produkter i kategorin. Du kan filtrera listan ytterligare genom att välja ett specifikt format, klimat, färg, material, mönster eller pris, eller en kombination av värden. Filterbara attribut visas i ett expanderande avsnitt som visar varje attributvärde. Som ett alternativ kan listan med produkter med matchande resultat konfigureras så att den innehåller produkter med eller utan en matchning.

Attributegenskaperna, i kombination med produktindatatypen, avgör vilka attribut som kan användas för lagerstyrd navigering. Navigering i lager är bara tillgängligt för [_ankarpunktskategorier_](categories-display-settings.md), men kan även läggas till på sökresultatsidor. Egenskapen **Katalogindatatyp för butiksägare** för varje attribut måste anges till `Yes/No`, `Dropdown`, `Multiple Select` eller `Price`. För att attributen ska kunna filtreras måste egenskapen **Använd i navigering i lager** anges till antingen `Filterable (with results)` eller `Filterable (no results)`.

_Exempel: Filterbara attribut med resultat_

![Filterbara attribut i lagernavigering](./assets/storefront-layered-navigation-filtered.png){width="700" zoomable="yes"}

_Exempel: Filterbara värden för färgrutor visas utan resultat_

![Filterbart färgrutevärde utan resultat](./assets/storefront-product-attribute-filter-no-results.png){width="700" zoomable="yes"}

Följande instruktioner visar hur du ställer in grundläggande lagerstyrd navigering med filterbara attribut. Mer information om avancerad lagerbaserad navigering med prissteg finns i [Prisnavigering](navigation-layered.md#configure-price-navigation).

## Steg 1: Ange attributegenskaperna

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**på sidofältet_ Admin _.

1. Bläddra eller använd filtrerad sökning för att hitta ett attribut i listan och öppna det i redigeringsläge.

   ![Ange söktermer per kolumn om du vill använda filtrerad sökning](./assets/attribute-search.png){width="700" zoomable="yes"}

1. Välj **[!UICONTROL Storefront Properties]** i den vänstra panelen och ange **[!UICONTROL Use In Layered Navigation]** till något av följande:

   - `Filterable (with results)` - Navigering i lager innehåller bara de filter för vilka matchande produkter kan hittas. Alla attributvärden som redan gäller för alla produkter som visas i listan bör fortfarande visas som ett tillgängligt filter. Attributvärden med antalet noll (0) produktmatchningar utelämnas från listan med tillgängliga filter. Den filtrerade listan innehåller bara de produkter som matchar filtret. Produktlistan uppdateras bara om de valda filtren ändrar vad som visas.

   - `Filterable (no results)` - Navigering i lager innehåller filter för alla tillgängliga attributvärden och deras produktantal, inklusive produkter med noll (0) produktmatchningar. Om attributvärdet är en färgruta visas värdet som ett filter, men stryks över. Prisnivåfiltrering stöds inte av det här alternativet och påverkar inte prisfilter.

1. Ange **[!UICONTROL Use In Search Results Layered Navigation]** till `Yes`.

   ![Storefront-egenskaper](./assets/attribute-storefront-properties.png){width="600" zoomable="yes"}

1. Upprepa dessa steg för varje attribut som du vill inkludera i navigeringen i lager.

>[!NOTE]
>
>När inställningen _[!UICONTROL Use in Search]_är inställd på `No` visas inte inställningen_[!UICONTROL Use in Search Results Layered Navigation]_ och produktattributet används inte i sökningen med något [!UICONTROL Use in Layered Navigation]-inställningsvärde.

>[!NOTE]
>
>Fältet [!UICONTROL Position] är som standard nedtonat, så du måste spara attributet innan du kan ändra den här inställningen.

## Steg 2: Gör kategorin till en ankarpunkt

1. Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Categories]** på sidofältet _Admin_.

1. I kategoriträdet väljer du den kategori där du vill använda lagerstyrd navigering.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Display Settings]** och ange **[!UICONTROL Anchor]** till `Yes`.

   ![Inställningar för kategorivisning](./assets/category-layered-navigation-anchor.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]**.

## Steg 3: Testa resultaten

Testa inställningarna på din butik och navigera till kategorin på huvudmenyn. Urvalet av filterbara attribut visas i kategorinsidans lagernavigering.

Sök, filtrera och granska de visade produkterna.

## Ta bort filterbara attributvärden från navigering i lager

Navigering i flera lager innehåller filter för alla tillgängliga attributvärden och deras produktantal, inklusive produkter med noll (0) produktmatchningar (som i bilden nedan).

![Inga filter visas](./assets/filterable-attributes-on-plp.png){width="700" zoomable="yes"}

Detta kan göra det svårt för kunderna att välja en föredragen produkt och det finns inget behov av att visa attributvärden &#x200B; &#x200B; med 0 produkter i frontend.

Du kan använda följande steg för att ta bort filterbara attributvärden med 0 produkter från lagernavigeringen:

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**på sidofältet_ Admin _.

1. Bläddra eller använd filtrerad sökning för att hitta ett attribut i listan och öppna det i redigeringsläge.

1. Klicka på **[!UICONTROL Storefront Properties]** under _[!UICONTROL Attribute Information]_.

1. Välj `Filterable (with results)` för **[!UICONTROL Layered Navigation]**.

   ![Avsnittet Attributinformation](./assets/storefront-properties-tab.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Attribute]**.

## Prisnavigering

>[!NOTE]
>
>Den prisnavigeringskonfiguration som beskrivs i det här avsnittet skiljer sig åt för [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

Prisnavigering kan användas för att distribuera produkter efter prisintervall i lagernavigering. Du kan också dela upp varje intervall i intervall. Det finns några sätt att beräkna prisnavigering:

- Automatiskt (Utjämna prisintervall)
- Automatiskt (Utjämna produktantal)
- Manuell

Med de första två metoderna beräknas navigeringsstegen automatiskt. Med den manuella metoden kan du ange en divisionsgräns för prisintervall. I följande exempel visas skillnaden mellan prisnavigeringsstegen 10 och 100.

Iterativ uppdelning ger den bästa produktfördelningen mellan olika prisintervall. Med iterativ uppdelning kan kunden, efter att ha valt intervallet 0,00-99 USD, gå igenom flera olika prisintervall. Prisintervallsdelningen avbryts när antalet produkter når det tröskelvärde som anges av Avdelningsgränsen.

## Exempel: Prisnavigeringssteg

| Prissteg med 10 | Prissteg med 100 |
|----------|--------|
| 20,00 - 29,99 USD (1) | $0,00 - $99,99 (4) |
| 30,00-39,99 USD (2) | 100-199,99 USD (5) |
| 70,00-79,99 USD (1) | 400,00-499,99 USD (2) |
| 100,00 - 109,99 USD (1) | $700.00 och högre (1) |
| 120,00 - 129,99 USD (2) |   |
| 150,00 - 159,99 USD (1) |   |
| 180,00 - 189,99 USD (1) |   |
| 420,00 - 429,99 USD (1) |   |
| 440,00 - 449,99 USD (1) |   |
| $710.00 och högre (1) |   |

{style="table-layout:auto"}

## Konfigurera prisnavigering

>[!IMPORTANT]
>
>Om du vill visa produkter och deras priser på rätt sätt enligt _prisfilter_ i lagernavigeringen, kontrollerar du att inställningarna för prisvisningen i [momskonfigurationen](../configuration-reference/sales/tax.md) har samma värde (`Excluding Tax` **eller** `Including Tax`). Kontrollera värdet **[!UICONTROL Catalog Prices]** för _[!UICONTROL Calculation Settings]_. Och för_[!UICONTROL Price Display Settings]_, kontrollera värdet **[!UICONTROL Display Product Prices in Catalog]**. Om de har olika värden kan prisfiltren i lagernavigeringen eventuellt inte filtrera och sortera produkter efter pris.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet _Navigering i lager_.

   Som standard är **[!UICONTROL Display Product Count]** inställd på `Yes`. Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för att ändra den här inställningen.

   ![Navigering i lager](../configuration-reference/catalog/assets/layered-navigation.png){width="600" zoomable="yes"}

   En detaljerad lista över dessa konfigurationsalternativ finns i [Navigering i lager](../configuration-reference/catalog/catalog.md#layered-navigation) i _Konfigurationsreferens_.

1. Ange **[!UICONTROL Price Navigation Steps Calculation]** för en av metoderna i följande avsnitt.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

### Metod 1: Automatisk (jämför prisintervall)

Låt **[!UICONTROL Price Navigation Steps Calculation]** vara inställt på `Automatic (Equalize Price Ranges)` (standard). Den här inställningen använder standardalgoritmen för prisnavigering.

### Metod 2: Automatisk (utjämna antalet produkter)

>[!TIP]
>
>Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för att ändra inställningarna.

1. Ange **[!UICONTROL Price Navigation Steps Calculation]** till `Automatic (equalize product counts)`.

1. Om du vill visa ett enda pris när flera produkter har samma pris anger du **[!UICONTROL Display Price Interval as One Price]** till `Yes`.

1. För **[!UICONTROL Interval Division Limit]** anger du tröskelvärdet för antalet produkter inom ett prisintervall.

   Intervallet kan inte delas ytterligare efter den här gränsen. Standardvärdet är `9`.

   ![Automatisk (utjämna produktantal)](../configuration-reference/catalog/assets/layered-navigation-equalize-product-counts.png){width="600" zoomable="yes"}

### Metod 3: Manuell

>[!NOTE]
>
>Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för att ändra inställningarna.

1. Ange **[!UICONTROL Price Navigation Steps Calculation]** till `Manual`.

1. Ange ett värde som bestämmer **[!UICONTROL Default Price Navigation Step]**.

1. Ange **[!UICONTROL Maximum Number of Price Intervals]** som tillåts, upp till `100`.

   ![Manuell](../configuration-reference/catalog/assets/layered-navigation-manual.png){width="600" zoomable="yes"}

## Konfigurera lagernavigering

>[!NOTE]
>
>Standardkonfigurationen som beskrivs på den här sidan skiljer sig åt för [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

Konfigurationen för lagerstyrd navigering avgör om ett produktantal visas inom parentes efter varje attribut och storleken på stegberäkningen som används i prisnavigeringen.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera avsnittet _[!UICONTROL Catalog]_i den vänstra panelen och välj **[!UICONTROL Catalog]**under.

1. Expandera avsnittet _[!UICONTROL Layered Navigation]_.

   >[!NOTE]
   >
   >Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för att ändra inställningarna.

1. Om du vill visa antalet produkter som hittas för varje attribut anger du **[!UICONTROL Display Product Count]** till `Yes`.

1. Ange **[!UICONTROL Price Navigation Step Calculation]** till `Automatic (equalize price ranges)`.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
