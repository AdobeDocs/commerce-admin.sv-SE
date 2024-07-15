---
title: Relaterade produktregler
description: Lär dig mer om relaterade produktregler och hur de används för att dynamiskt presentera relaterade produkter, merförsäljning och korsförsäljning till dina kunder.
exl-id: ff566e13-cbe8-42f1-be3a-684e364b86dd
feature: Merchandising, Products, Storefront
source-git-commit: 4971fe457b7fd58d8b71951981bc889386610a99
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# Relaterade produktregler (målregler)

{{ee-feature}}

Med relaterade produktregler kan ni inrikta er på de produkter som presenteras för kunderna som relaterade produkter, merförsäljning och korsförsäljning. Varje produktregel kan kopplas till ett [kundsegment](../customers/customer-segments.md) för att skapa en dynamisk visning av riktad marknadsföring.

Eftersom flera aktiva regler kan aktiveras samtidigt kan du ange en prioritet för varje regel. Den definierar i vilken ordning reglerna tillämpas och produkterna visas på sidan.

Gå till **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**om du vill komma åt de relaterade produktreglerna.

![Listan med relaterade produktregler](./assets/related-products-rules.png){width="700" zoomable="yes"}

## Kolumnbeskrivningar

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL ID] | En unik numerisk identifierare som tilldelas varje relaterad produktregel |
| [!UICONTROL Rule] | Namnet på den relaterade produktregeln |
| [!UICONTROL Start] | Använd de dynamiska kalenderfälten (_[!UICONTROL To:]_och_[!UICONTROL From:]_) för att filtrera listan baserat på regelns startdatum som det definierades när regeln skapades. |
| [!UICONTROL End] | Använd de dynamiska kalenderfälten (_[!UICONTROL To:]_och_[!UICONTROL From:]_) för att filtrera listan baserat på regelns slutdatum som det definierades när regeln skapades. |
| [!UICONTROL Priority] | Ange text i det här fältet om du vill filtrera listan baserat på den prioritet som har definierats för en regel. |
| [!UICONTROL Applies To] | Det här alternativet filtrerar listan med regler som gäller för `Related Products`, `Up-sells` och `Cross-sells`. |
| [!UICONTROL Status] | Använd det här alternativet om du vill filtrera listan baserat på regelstatus (`Active` eller `Inactive`). |

{style="table-layout:auto"}

## Regelprioritet

Det kan när som helst finnas flera aktiva regler som kan aktiveras för att visa relaterade produkter, merförsäljning och korsförsäljning. Prioriteten för varje regel avgör i vilken ordning produkterna visas på sidan. Värdet kan anges till vilket heltal som helst med `1` som har högst prioritet.

Antalet produkt-ID:n som kan inkluderas i en produktrelationsregel bestäms av värdet `Result Limit`, som har högst 20. Värdet `Result Limit` i kombination med `Configurable Maximum` för den specifika regelbaserade produktkampanjen blir `Real Limit` och avgör det faktiska antalet matchande produkter som kan visas i listan.

[Resultatgräns] + [Konfigurerbart maximum] = [Verklig gräns]

Anta till exempel att du har tre regler med prioriteten `1`, `2` och `3`.

- Två matchande produkter returnerades för _Regel 1_, sex matchande produkter för _Regel 2_ och 20 matchande produkter för _Regel 3_.
- I konfigurationen är _[!UICONTROL Maximum Number of Products for Related Products List]_inställd på `6`.

  | Regler | Prioritet | Matchande produkter |
  |---|---|-----|
  | Regel 1 | `1` | `2` |
  | Regel 2 | `2` | `6` |
  | Regel 3 | `3` | `20` |

Om den första regeln returnerar fler matchande produkter än vad som tillåts av den _konfigurerbara maxgränsen_, men mindre än den _reella gränsen_, används matchande produkter från de andra reglerna (i prioritetsordning) tills den _reella gränsen_ nås.

De matchande produkter som returneras från _Regel 1_ kan först användas för att fylla alla 26 tillgängliga platser. Regel 1 returnerade bara två matchande produkter, och det finns fortfarande utrymme för ytterligare 24. _Regel 2_ har den näst högsta prioriteten och returnerar ytterligare sex matchande produkter. Det finns nu 18 tillgängliga kortplatser att fylla i. _Regel 3_ har nästa prioritetsnivå, med tillräckligt många matchande produkter för att fylla de återstående 18 kortplatserna. När alla tillgängliga kortplatser är fyllda, och beroende på vilket rotationsläge som är inställt, kan produkter blandas eller beställas med ID i varje prioritet och sedan reduceras till den konfigurerbara maxgränsen. I så fall finns de återstående sex produkterna i butiken.

>[!NOTE]
>
>De valda produkterna visas alltid före de regelbaserade produkterna oavsett rotationsläge.

## Konfigurera regelbaserade produktrelationer

Beteendet för produktrelationsregler och visningen av matchade produkter bestäms av konfigurationsinställningarna. Dessa inställningar avgör hur många produkter som matchar regeln som kan visas och i vilken ordning de visas.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Catalog]** i panelen till vänster och välj **[!UICONTROL Catalog]** under.

1. Expandera ![Utökning](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Rules-Based Product Relations]**.

   ![Katalogkonfiguration - regelbaserade produktrelationer](../configuration-reference/catalog/assets/catalog-rule-based-product-relations.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Maximum Number of Products in the Related Products List]**.

1. Ange **[!UICONTROL Show Related Products]** till något av följande:

   - `Both Selected and Rule Based`
   - `Selected Only`
   - `Rule-Based Only`

1. Ange **[!UICONTROL Rotation Mode for Products in Related Product List]** till något av följande:

   - `By Priority, Then by ID`
   - `By Priority, Then Random`
   - `Weighted Random`

1. Så här slutför du korsförsäljningsproduktinställningarna:

   - Ange **[!UICONTROL Maximum Number of Products in the Cross-Sell Product List]**.

   - Ange **[!UICONTROL Show Cross-Sell Products]** till något av följande:

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - Ange **[!UICONTROL Rotation Mode for Products in Cross-Sell Product List]** till något av följande:

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. Så här slutför du produktinställningarna för merförsäljning:

   - Ange **[!UICONTROL Maximum Number of Products in the Upsell Product List]**.

   - Ange **[!UICONTROL Show Upsell Products]** till något av följande:

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - Ange **[!UICONTROL Rotation Mode for Products in Upsell Product List]** till något av följande:

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

### Rotationslägen

| Läge | Beskrivning |
|---|---|
| [!UICONTROL By Priority, Then by ID] | Produkterna sorteras efter prioritet och sorteras sedan efter ID i varje prioritet. Produkter från regeln med lägre prioritet visas bara när de inte finns några produkter kvar från regeln med högre prioritet för att fylla de tillgängliga platserna. |
| [!UICONTROL By Priority, Then Random] | Produkterna sorteras efter prioritet och sedan slumpmässigt inom varje prioritet. Produkter från regeln med lägre prioritet visas bara när de inte finns några produkter kvar från regeln med högre prioritet för att fylla de tillgängliga platserna. |
| [!UICONTROL Weighted Random] | Produkterna är randomiserade så att produkter som tillhör en regel med högre prioritet har större sannolikhet att visas än de som tillhör en regel med lägre prioritet. Produkterna reduceras sedan till den konfigurerbara maxgränsen och grupperas sedan om efter prioritet. Det här läget ger en chans att produkter med lägre prioritet visas ibland även om de återstående platserna kan fyllas med produkter med högre prioritet i en regel |

{style="table-layout:auto"}

## Använd Real-Time CDP målgrupper för att informera om relaterade produktregler

>[!NOTE]
>
>Den här funktionen är i betaversion. Om du vill gå med i betaprogrammet skickar du en begäran till [dataconnection@adobe.com](mailto:dataconnection@adobe.com).


Lär dig hur du [aktiverar](../customers/audience-activation.md) Real-Time CDP-målgrupper i din Adobe Commerce-instans för att informera om relaterade produktregler.
