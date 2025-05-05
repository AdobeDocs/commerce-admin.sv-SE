---
title: Sökresultat
description: Lär dig hur du konfigurerar hur produkterna matchar sökvillkoren som anges i snabbsökningsrutan eller i formuläret för avancerad sökning.
exl-id: c721fb3b-ee31-4d2b-b4ea-9ae2c80aa800
feature: Catalog Management, Search
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 0%

---

# Sökresultat

>[!NOTE]
>
>Den här sidan beskriver standardsökfunktioner som kan skilja sig från [Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html).

Listan _Sökresultat_ innehåller alla produkter som matchar sökvillkoren som anges i snabbsökningsrutan eller i formuläret för avancerad sökning. Alla produktlistor i katalogen har i stort sett samma kontroller. Den enda skillnaden är att det ena är resultatet av en sökfråga och den andra skillnaden är resultatet av [navigering](navigation.md).

Resultatet kan antingen formateras som ett rutnät eller en lista och sorteras efter ett urval attribut. Sidnumreringskontrollerna visas om det finns fler produkter än vad som får plats på sidan. Använd de här kontrollerna för att gå från en sida till nästa. Antalet poster per sida avgörs av konfigurationen för Catalog Frontend. Mer information finns i [Produktlistor](navigation-product-listings.md).

Med **Elasticsearch**:

- Det finns inget färdigt stöd för sökning med suffixet. Sökning med SKU kanske inte returnerar det förväntade resultatet om nyckelordet bara innehåller slutdelen av SKU:n.
- Det finns inget färdigt stöd för sökning efter prefix (partiell nyckelordssökning) endast för produktattributen `name` och `sku`. Alla andra produktattribut söks igenom med hela nyckelordet, med exakt matchning.
- Sökresultaten för produktattributen `name` och `sku` baseras på relevansen, inte på exakt matchning. De mest relevanta matchningarna, till exempel ett exakt matchat _produktnamn_ eller _SKU_, visas först. Om du vill söka efter en exakt matchning kan kunden använda dubbla citattecken i sökfrågan. En `WSH12-32-Red`-sökfråga kan till exempel returnera flera produkter, sorterade efter relevansen. Men en `"WSH12-32-Red"`-sökfråga returnerar bara en produkt med **_exakt_** matchad `sku`.

![Sökresultat med sidnumreringskontroller](./assets/storefront-search-results-shorts.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>På grund av att supporten för Elasticsearch 7 upphör i augusti 2023 rekommenderar vi att alla Adobe Commerce-kunder migrerar till sökmotorn OpenSearch 2.x. Mer information om hur du migrerar sökmotorn under produktuppgraderingen finns i [Migrera till OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) i _uppgraderingshandboken_.

## Nyckelordsmappning som utökar sökresultaten

Den här tekniken använder ett attribut för att skapa en nyckelordsbaserad association mellan två produkter så att en sökning efter någon av produkterna returnerar resultat för båda produkterna. Du kan använda nyckelordsmappning för att marknadsföra en produkt i sökresultat där den annars inte skulle visas.

![Sökresultat med nyckelordsmappning](./assets/storefront-search-results-extended.png){width="700" zoomable="yes"}

I följande exempel används nyckelordsmappning baserad på SKU. När någon av SKU:erna anges i sökrutan visas båda produkterna i resultatet. SKU:erna för följande konfigurerbara produkter mappas i stället för SKU:erna för produktvariationer:

- Montana Wind Jacket (MJ03)
- Chaz Kangaroo Hoodie (MH01)

### Steg 1: Skapa ett attribut

1. Öppna `Montana Wind Jacket` (MJ03) i redigeringsläget i listan _[!UICONTROL Products]_.
1. Klicka på **[!UICONTROL Add Attribute]** i det övre högra hörnet.
1. Klicka på **[!UICONTROL Create New Attribute]** på sidan _Välj attribut_.
1. Fyll i attributegenskaperna enligt följande:

   **[!UICONTROL Attribute Properties]**

   - [!UICONTROL Attribute Label] - `Search Keywords`
   - [!UICONTROL Catalog Input Type for Store Owner] - `Text Field`

   **[!UICONTROL Advanced Attribute Properties]**

   - [!UICONTROL Add to Column Options] - `Yes` (standard)
   - [!UICONTROL Use in Filter Options] - `Yes` (standard)

   **[!UICONTROL Storefront Properties]**

   - [!UICONTROL Use in Search] - `Yes`
   - [!UICONTROL Visible on Catalog Pages in the Storefront] - `No`
   - [!UICONTROL Used in Product Listings] - `No`

1. Klicka på **[!UICONTROL Save Attribute]** när du är klar.

   Attributet läggs till i produktens attributuppsättning.

### Steg 2: Mappa den första produkten

1. Bläddra nedåt och expandera avsnittet _[!UICONTROL Attributes]_&#x200B;på sidan med produktinställningar.
1. I fältet **[!UICONTROL Search Keywords]** anger du SKU `MH01` som ska mappas till den här produkten.

   Du kan ange flera SKU:er avgränsade med ett mellanslag i fältet Sök efter nyckelord. I det här exemplet anges bara en.

   ![Attributavsnitt med söknyckelord](./assets/search-keywords-attribute.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]** när du är klar.
1. Gå till **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**&#x200B;och uppdatera **[!UICONTROL Page Cache]**.

### Steg 3: Mappa den andra produkten

1. Öppna `Chaz Kangaroo Hoodie` (MH01) i redigeringsläget i listan _[!UICONTROL Products]_.
1. Bläddra nedåt och expandera avsnittet **[!UICONTROL Attributes]**.
1. I fältet **[!UICONTROL Search Keywords]** anger du SKU för den andra produkten, `MJ03`.
1. Klicka på **[!UICONTROL Save]**.
1. Gå till **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**&#x200B;och uppdatera **[!UICONTROL Page Cache]**.

### Steg 4: Testa det i butiken

1. Gå till butiken och ange `MJ03` i rutan _Snabbsökning_.
1. Kontrollera att båda produkterna returneras i sökresultatlistan.

## Viktad sökning

Produktattribut som är aktiverade för katalogsökning kan tilldelas en vikt för att ge dem ett högre värde i sökresultaten. Attribut med större vikt returneras före attribut med lägre vikt. Om det till exempel finns två attribut i systemet, _color_ med sökvikten 3 och _description_ med sökvikten 1. En sökning efter ordet _red_ returnerar en lista med produkter med färgattributvärdet `red` högst upp i sökresultatet och returnerar produkter med beskrivningar som innehåller ordet _red_ längst ned i sökresultatet. I det här exemplet har attributet `color` en större definierad vikt än attributet `description`.

>[!IMPORTANT]
>
>Sortering efter relevans påverkas av **_flera_**-villkor och relationer mellan dem **_samtidigt_**. [!UICONTROL Search Weight] är bara ett av dessa villkor. Det innebär att attribut med lägre sökvikt ibland kan ha större relevans än attribut med högre sökvikt. Andra villkor kan vara antalet matchningar i ett givet attribut, positionen för det sökord som hittats och den övergripande textstrukturen före och efter ett sökord.

**_Så här anger du sökviktsegenskaperna för ett attribut:_**

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**&#x200B;på sidofältet_ Admin _.

1. Leta reda på attributet i listan och öppna i redigeringsläge.

1. Välj **[!UICONTROL Storefront Properties]** i den vänstra panelen och gör följande:

   - Om du vill ta med attributet i sökfrågor anger du **[!UICONTROL Use in Search]** till `Yes`.

   - Ange **[!UICONTROL Search Weight]** till ett nummer mellan 1 och 10, där `10` har högsta prioritet, om du vill fastställa attributets sökvärde. Om inget värde anges används sökvikten `1` som standard för alla attribut.

   ![Sökvikt](./assets/search-weight.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Attribute]** när du är klar.
