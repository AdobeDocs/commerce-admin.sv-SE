---
title: Hantera söktermer
description: Lär dig hur du hanterar sökvillkoren för din butik för att dirigera om kunder med felstavade eller alternativa termer.
exl-id: e21ece58-2bc2-49ef-96d3-3be930e09f94
feature: Catalog Management, Search
source-git-commit: 3851258543ba829a4bdbfdb5d3d053ec4627184a
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 0%

---

# Hantera söktermer

The [landningssida](../content-design/pages.md) för en sökterm kan vara en innehållssida, en kategorisida, en produktinformationssida eller till och med en sida på en annan webbplats.

Använd söktermer för att fånga vanliga felstavningar och dirigera om dem till rätt sida. Om du till exempel säljer möbler av järn vet du att många personer stavar fel på termen som _råjärn_, eller till och med _rosenjärn_. Du kan ange de felstavade orden som sökord och göra dem synonymer för _bearbetat järn_. Även om ordet är felstavat dirigeras sökningen till sidan för ifyllt järn.

Du kan också ta reda på vad kunderna letar efter genom att undersöka de söktermer de använder för att hitta produkter i din butik. Om tillräckligt många söker efter en produkt som inte finns i din katalog kan det tyda på en säljmöjlighet. I stället för att lämna dem tomma kan du dirigera om dem till en annan produkt i katalogen.

## Lägg till söktermer

När du lär dig nya ord som andra använder för att söka i din butik kan du lägga till dem i sökordslistan för att dirigera personer till de produkter som matchar bäst i din katalog.

![Rutnät för söktermer](./assets/search-terms.png){width="700" zoomable="yes"}

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Search Query] | Frågan som användes för att utföra sökningen. |
| [!UICONTROL Store] | Det arkiv där sökfrågan tillämpades. |
| [!UICONTROL Results] | Antal resultat som hittats av frågan. |
| [!UICONTROL Uses] | Antal användare. |
| [!UICONTROL Redirect URL] | URL för målsidan där användaren omdirigerades efter att sökningen utförts. |
| [!UICONTROL Suggested Terms] | Avgör om frågeresultatet visar föreslagna termer. |
| [!UICONTROL Actions] | Öppnar produkten i redigeringsläge. |

{style="table-layout:auto"}

>[!NOTE]
>
>Antalet resultat uppdateras varje gång en kund gör en sökning med den här sökfrågan. Den uppdateras inte om någon av produkterna ändras eller tas bort.

### Lägg till en sökterm

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. Klicka på **[!UICONTROL Add New Search Term]**.

   ![Allmän information om söktermer](./assets/search-terms-information.png){width="600" zoomable="yes"}

1. Under _[!UICONTROL General Information]_i **[!UICONTROL Search Query]**anger du det ord eller den fras som du vill lägga till som ett nytt sökord.

1. Om din butik finns tillgänglig på flera språk väljer du lämplig **[!UICONTROL Store]** vy.

1. Om du vill dirigera om sökresultaten till en annan sida i din butik, eller till en annan webbplats, anger du målsidans fullständiga URL i dialogrutan **[!UICONTROL Redirect URL]** fält.

1. Om du vill att den här termen ska vara tillgänglig som förslag när sökningen inte ger några resultat anger du **[!UICONTROL Display in Suggested Terms]** till `Yes`.

1. När du är klar klickar du på **[!UICONTROL Save Search]**.

## Redigera en sökterm

1. I _[!UICONTROL Search Terms]_om du vill öppna söktermen i redigeringsläge klickar du på raden för en post.

1. Gör de ändringar som behövs.

1. När du är klar klickar du på **[!UICONTROL Save Search]**.

## Ta bort en sökterm

Det finns två metoder för att ta bort en sökterm - från rutnätet och på redigeringssidan.

**Metod 1:** I _[!UICONTROL Search Terms]_rutnät

1. Markera kryssrutan för den term som ska tas bort i listan.

1. I listans övre vänstra hörn anger du **[!UICONTROL Actions]** till `Delete`.

1. När du är klar klickar du på **[!UICONTROL Submit]**.

**Metod 2:** På _[!UICONTROL Edit a Search Term]_page

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. Sök efter den sökterm som ska tas bort och öppna den i redigeringsläge.

1. Klicka på **[!UICONTROL Delete Search]**.

1. Bekräfta åtgärden genom att klicka **[!UICONTROL OK]**.

## Vanliga söktermer

The _Sökvillkor_ i butikens sidfot visar de söktermer som besökarna använder i butiken, rankade efter popularitet. Söktermer visas i en _tagmoln_ format, där storleken på texten anger termens popularitet.

Vanliga söktermer är som standard aktiverade som sökmotoroptimeringsverktyg, men har ingen direkt anslutning till katalogsökprocessen. Eftersom sidan Sökvillkor indexeras av sökmotorer kan alla termer på sidan hjälpa dig att förbättra din sökmotorrankning och butikens synlighet. URL:en för sidan Popular Search Terms är: `mystore.com/search/term/popular/`

![Exempel på butiker - vanliga söktermer](./assets/store-front-search-terms-yoga-pants.png){width="600" zoomable="yes"}

**_Så här konfigurerar du vanliga söktermer:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Search Engine Optimization]** -avsnitt.

   ![Katalogkonfiguration - sökmotoroptimering](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   En detaljerad lista över dessa alternativ finns på [Sökmotoroptimering](../configuration-reference/catalog/catalog.md#search-engine-optimization) i _Konfigurationsreferens_.

1. Ange **[!UICONTROL Popular Search Terms]** efter behov.

   Rensa **[!UICONTROL Use system value]** om du vill ändra inställningen.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Du kan konfigurera cachelagring av populära filer ytterligare [katalogsökningar](search-configuration.md).

## Sök synonymer

Ett sätt att förbättra effektiviteten hos [katalogsökning](search-configuration.md) ska innehålla olika termer som andra kan använda för att beskriva samma objekt. Du vill inte förlora en försäljning bara för att någon letar efter en _sofa_ och din produkt listas som _soffa_. Du kan hämta fler söktermer genom att ange _sofa_, _davenport_ och _loveseat_ som synonymer för _soffa_ och dirigera dem till samma landningssida.

Adobe Commerce har stöd för två olika synonymhanteringslösningar:

- Live Search [Synonymer](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/synonyms/synonyms.html) finns för Adobe Commerce-installationer med Live Search installerat.
- Standardfunktionen för söksynonymer (som beskrivs på den här sidan) är tillgänglig direkt för alla Adobe Commerce-installationer.

>[!NOTE]
>
>Standardfunktionen för söksynonymer som är färdig att användas `name` och `sku` produktattribut **_endast_**.

>[!IMPORTANT]
>
>Söksynonymfunktionen använder endast en fulltextmatchande sökmetod.

![Exempel på storefront - sökresultat med synonymer](./assets/storefront-search-results-synonyms.png){width="700" zoomable="yes"}

### Skapa en synonymgrupp

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Synonyms]**.

   The _[!UICONTROL Search Synonyms]_visas. Om det är första gången du använder söksynonymer är rutnätet tomt.

   ![Sök synonymrutnät](./assets/search-synonyms-grid-empty.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL New Synonym Group]**.

   ![Ny synkroniseringsgrupp för sökning](./assets/search-synonym-group-new.png){width="700" zoomable="yes"}

1. Ange **[!UICONTROL Scope]** till de butiksvyer där synonymerna gäller.

1. Ange varje synonym i gruppen, avgränsade med kommatecken. Välj ord som andra kan använda som sökvillkor. Exempel:

   - `sweatshirt, sweat shirt, hoodie, fleece`
   - `cell phone, mobile phone, smart phone`
   - `couch, sofa, davenport`
   - `wrought iron, rot iron, rod iron`

1. Om du vill sammanfoga dessa synonymer i en grupp med andra som har samma omfång väljer du **[!UICONTROL Merge existing synonyms]** kryssrutan.

1. När du är klar klickar du på **[!UICONTROL Save Synonym Group]**.

### Redigera en synonymgrupp

1. I _[!UICONTROL Search Synonyms]_genom att klicka på raden för en post för att öppna synonymgruppen i redigeringsläge.

1. Gör de ändringar som behövs.

1. När du är klar klickar du på **[!UICONTROL Save Synonym Group]**.

### Ta bort en synonymgrupp

Det finns två metoder för att ta bort en synonymgrupp - från stödrastret och på redigeringssidan.

**Metod 1:** I stödrastret Sök efter synonymer

1. I _[!UICONTROL Search Synonyms]_markerar du kryssrutan för gruppen som ska tas bort.

1. I listans övre vänstra hörn anger du **[!UICONTROL Actions]** till `Delete`.

1. När du är klar klickar du på **[!UICONTROL Submit]**.

**Metod 2:** På sidan Redigera en synonymgrupp

1. I stödrastret Sök synonymer klickar du på raden för en post för att öppna synonymgruppen i redigeringsläge.

1. Klicka på **[!UICONTROL Delete Synonym Group]**.

1. Bekräfta borttagningen av gruppen när du uppmanas till detta.

## Rapport om sökvillkor

I rapporten Sökvillkor visas antalet resultat för varje term och antalet träffar som termen användes. Rapportdata kan filtreras efter term, butik, resultat och träffar, och exporteras för ytterligare analys.

### Visa rapporten

1. På _Administratör_ sidebar, gå till **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Search Terms]**.

1. Använd kontrollerna för att filtrera rapporten efter behov.

   ![Rapport över söktermer](./assets/search-terms-report.png){width="700" zoomable="yes"}

## Exportera rapporten

1. För **[!UICONTROL Export to]** väljer du ett exportformat:

   - `CSV` - en kommaavgränsad värdefil som innehåller oformaterade textdata
   - `Excel XML` - Ett XML-baserat kalkylbladsdataformat

1. Klicka på **[!UICONTROL Export]**.

   Den genererade filen sparas automatiskt i den mapp du har valt för nedladdning.

### Rapportkolumner

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL ID] | Unikt, numeriskt ID genererat för söktermsposten |
| [!UICONTROL Search Query] | Frågan som användes för att utföra sökningen |
| [!UICONTROL Store] | Det arkiv där sökfrågan tillämpades |
| [!UICONTROL Results] | Antal resultat |
| [!UICONTROL Hits] | Antal användare |

{style="table-layout:auto"}
