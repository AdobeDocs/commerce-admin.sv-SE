---
title: Produktinställningar - [!UICONTROL Customizable Options]
description: För en produkt är [!UICONTROL Customizable Options] kan du välja mellan olika alternativ för text, markering och datuminmatning.
exl-id: 7d23c5c5-2b2a-4f2a-b843-9c27b851be5f
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 0%

---

# Produktinställningar - [!UICONTROL Customizable Options]

Att lägga till anpassningsbara alternativ till en produkt är ett enkelt sätt att erbjuda ett urval av alternativ med text, urval och datuminmatningstyper. Anpassningsbara alternativ är en bra lösning om era inventeringsbehov är enkla. Eftersom de baseras på variationer av en enda SKU kan de dock inte användas för att hantera aktier eller som grund för prisregelvillkoren. Om du har flera produkter med samma alternativ kan du konfigurera en produkt och importera alternativen till de andra produkterna.

När en kund köper en produkt med ett anpassningsbart alternativ visas en beskrivning av varje valt alternativ under produktbeskrivningen och eventuella tillhörande pålägg (eller pålägg) tillämpas automatiskt på artikelns pris.

![Produktinformation med anpassningsbart alternativ](./assets/storefront-customizable-option-product-detail.png){width="700" zoomable="yes"}

Om en kundvagnsprisregel utlöses av köpet gäller den första beräkningen först produktpriset och därefter radartikelpriset med eventuella justeringar för tillämpliga anpassningsbara alternativ. I följande exempel köper kunden en dubblettpåse för 74,00 USD plus ett anpassningsbart alternativ för ett monogram. Ett pålägg på 14,80 USD tillämpas på basproduktpriset och det justerade priset visas som 88,80 USD. I det här fallet utlöser köpet av dubblettpåsen en kundvagnsregel som baseras på produktens SKU och tillämpar en rabatt på köpet, plus fri frakt. Även om kundvagnsprisregeln inte aktiveras av det anpassningsbara alternativet tillämpas rabatten på kundvagnens innehåll, som inkluderar pålägg för det anpassningsbara alternativet.

![Kundvagn med anpassningsbart alternativ och prisregel](./assets/storefront-customizable-option-cart-price-rule.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Rabatten för katalogprisregel gäller inte för alternativ som kan anpassas till fasta priser.

## Skapa anpassningsbara alternativ

1. Öppna produkten i redigeringsläge.

1. Rulla ned och expandera ![Expansionsväljare](../assets/icon-display-expand.png) den _[!UICONTROL Customizable Options]_-avsnitt.

1. Klicka på **[!UICONTROL Add Option]**.

   ![Anpassningsbara alternativ](./assets/product-customizable-options.png){width="600" zoomable="yes"}

1. Ange de nya inställningarna:

   - För **[!UICONTROL Option Title]** anger du ett namn för alternativet.

   - Ange **[!UICONTROL Option Type]** för typen av datainmatning.

   - Om alternativet inte krävs för att köpa produkten avmarkerar du **[!UICONTROL Required]** kryssrutan.

1. Fyll i fälten enligt datainmatningstyp:

   - För **[!UICONTROL Title]** anger du ett namn för det här alternativet.

   - (valfritt) för **[!UICONTROL Price]** anger du eventuella pålägg eller pålägg från basproduktpriset som gäller för det här alternativet.

   - Ange **[!UICONTROL Price Type]** till något av följande:

      - `Fixed` - Variationspriset skiljer sig från basproduktens pris med ett fast penningbelopp, t.ex. $1.
      - `Percentage` - Priset på variationen skiljer sig från priset på basprodukten med en procentsats, t.ex. 10 %.

   - (Valfritt) Ange en **[!UICONTROL SKU]** för alternativet. Alternativet SKU är ett suffix som läggs till i produktens SKU.

   - Om _[!UICONTROL Option Type]_är `File`anger du filens parametrar. För **[!UICONTROL Compatible File Extensions]**anger du de giltiga tilläggen som kommaavgränsade värden (till exempel `png, jpg, gif`). För **[!UICONTROL Maximum Image Size]**anger du den maximala bildstorleken i pixlar. Om det är en textinmatning anger du det maximala värdet för **[!UICONTROL Maximum Characters]**.

   ![Lägg till värden för anpassningsalternativ](./assets/product-customizable-options-add-values.png){width="600" zoomable="yes"}

1. (Valfritt) Om du vill lägga till ytterligare ett anpassbart alternativ klickar du på **[!UICONTROL Add Option]**.

   - Slutför inställningarna som tidigare.

   - Om du vill ändra alternativens ordning klickar du på _[!UICONTROL Order]_![Ikon för sorteringsordning](../assets/icon-sort-order.png) och dra alternativet till en ny plats i listan.

   Upprepa det här steget för varje alternativ som ska läggas till.

1. När du är klar klickar du på **[!UICONTROL Save]**.

## Importera anpassningsbara alternativ

1. I _Anpassningsbara alternativ_ avsnitt, klicka **[!UICONTROL Import Options]**.


1. Alla produkter med anpassningsbara alternativ visas i rutnätet.

1. I listan markerar du kryssrutan för produkten med de alternativ som du vill importera.

1. Klicka på **[!UICONTROL Import]**.

1. När du är klar kan du fortsätta lägga till fler anpassade alternativ eller klicka på **[!UICONTROL Save and Close]**.

## Indatatyper

| Typ | Beskrivning |
|---------------------|---------------|
| [!UICONTROL Text] | En inmatningsrad eller textruta där kunden kan ange nödvändig information. Alternativ:<br />**[!UICONTROL Field]**- Ett enkelradigt inmatningsfält för text.<br />**[!UICONTROL Area]** - Ett flerradigt indatafält. Den här typen stöder inte avancerad formatering som HTML. Använd Max. tecken för att begränsa hur lång text som kan anges och för att säkerställa korrekt återgivning av den angivna texten i Admin. |
| [!UICONTROL File] | Låter kunden överföra en fil. |
| [!UICONTROL Select] | Låter kunden välja ett eller flera alternativ, beroende på vilken indatatyp som används. Alternativ:<br />**[!UICONTROL Drop-down]**- En nedrullningsbar lista med alternativ som bara tillåter ett val.<br />**[!UICONTROL Radio Buttons]** - En uppsättning alternativ som bara tillåter en markering.<br />**[!UICONTROL Checkbox]**- En kryssruta är en variant av ett ja/nej-alternativ. Om produkten har flera kryssrutor kan du göra flera val.<br />**[!UICONTROL Multiple Select]** - En listruta med alternativ som accepterar flera val. Om du vill välja flera alternativ håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ. |
| [!UICONTROL Date] | Låter kunden ange ett datum eller en tid eller välja värdet från en kalender. Alternativ: <br />**[!UICONTROL Date]**- Ett inmatningsfält för ett datumvärde. Datumet kan anges direkt i fältet eller väljas från en lista eller kalender. Indatametoden och indataformatet bestäms av [datum- och tidsalternativ](attributes-input-types.md#date-and-time-options) konfiguration.<br />**[!UICONTROL Date & Time]** - Ett inmatningsfält för ett datum- och tidsvärde.<br />**[!UICONTROL Time]**- Ett indatafält för ett tidsvärde. |

{style="table-layout:auto"}
