---
title: Lägg till innehåll - Recommendations
description: Läs mer om Product Recommendations Content Type, som används för att lägga till en lista med rekommendationer i [!DNL Page Builder] stage.
exl-id: ca90c10d-8d7a-42a2-bb13-2602aa9d6eef
feature: Page Builder, Page Content, Recommendations
source-git-commit: 13d00168e1253a7d2698b898caa30d9ca2ad3800
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 0%

---

# Lägg till innehåll - Recommendations

Använd _Recommendations_ innehållstyp för att lägga till en befintlig, aktiv [rekommendationsenhet](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/admin/create.html) till [[!DNL Page Builder] stage](workspace.md#stage) för en CMS-sida, ett -block eller ett dynamiskt -block.

>[!NOTE]
>
>The [!DNL Page Builder] _Recommendations_ innehållstypen stöds i Adobe Commerce 2.4.4 och senare och finns i [Recommendations metapaket version 3.0.x eller senare](https://marketplace.magento.com/magento-product-recommendations.html). Lägg till [!DNL Page Builder] support för Product Recommendations, [se installationsinformationen](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html#pbsupport). **Den här innehållstypen är inte tillgänglig för Magento Open Source.**

{{$include /help/_includes/page-builder-save-timeout.md}}

## Recommendations verktygslåda

| Verktyg | Ikon | Beskrivning |
| --- | --| --- |
| Flytta | ![Ikonen Flytta](./assets/pb-icon-move.png){width="25"} | Flyttar produktrekommendationsbehållaren och dess innehåll till en annan position på scenen. |
| Inställningar | ![Ikonen Inställningar](./assets/pb-icon-settings.png){width="25"} | Öppnar sidan Redigera produktrekommendation, där du kan välja rekommendationsenhet och ändra egenskaperna för behållaren. |
| Dölj | ![Dölj ikon](./assets/pb-icon-hide.png){width="25"} | Döljer den aktuella produktrekommendationsbehållaren och dess innehåll. |
| Visa | ![Visa ikon](./assets/pb-icon-show.png){width="25"} | Visar den dolda produktrekommendationsbehållaren och dess innehåll. |
| Duplicera | ![Duplicera, ikon](./assets/pb-icon-duplicate.png){width="25"} | Skapar en kopia av produktrekommendationsbehållaren och dess innehåll. |
| Ta bort | ![Ikonen Ta bort](./assets/pb-icon-remove.png){width="25"} | Tar bort produktrekommendationsbehållaren och dess innehåll från scenen. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Lägg till en befintlig rekommendationsenhet

1. Kontrollera att du redan har [har skapat en rekommendationsenhet](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/admin/create.html) för [!DNL Page Builder] sidtyp.

>[!NOTE]
>
>Du kan skapa rekommendationsenheter för [!DNL Page Builder] endast sidtypen i standardbutiksvyn.

1. Öppna sidan, blocket eller det dynamiska blocket i redigeringsläge.

1. Expandera _[!UICONTROL Content]_och klicka **[!UICONTROL Edit with Page Builder]**eller inuti förhandsvisningsområdet för innehållet för att öppna [!DNL Page Builder] arbetsyta.

1. I [!DNL Page Builder] panel under _[!UICONTROL Layout]_, dra en **[!UICONTROL Row]**platshållare till scenen.

1. I [!DNL Page Builder] panel under _[!UICONTROL Add Content]_, dra en **[!UICONTROL Product Recommendation]**platshållare till raden.

   ![Lägga till innehållstypen Produktrekommendation](./assets/pb-add-prex-drag.png){width="600" zoomable="yes"}

1. Gör något av följande:

   - Klicka på **[!UICONTROL Edit Product Recommendation]**.
   - Håll pekaren över den tomma behållaren för att visa verktygslådan och klicka på knappen _Inställningar_ (![Ikonen Inställningar](./assets/pb-icon-settings.png){width="20"} ).

   ![Redigera produktrekommendation](./assets/pb-prex-toolbox.png){width="600" zoomable="yes"}

1. I _[!UICONTROL Selection]_avsnitt, klicka **[!UICONTROL Select]**.

1. I listan med aktiva produktrekommendationer söker du efter raden med rekommendationsenheten som du vill lägga till och klickar på **[!UICONTROL Select]** i den sista kolumnen.

   ![Vald produktrekommendation](./assets/pb-prex-select.png){width="600" zoomable="yes"}

1. Klicka på i det övre högra hörnet **[!UICONTROL Add Selected]**.

   Namnet på den valda produktrekommendationen visas i dialogrutan _[!UICONTROL Selection]_i_[!UICONTROL Edit Product Recommendation]_ sida.

1. Gör nödvändiga ändringar i [Avancerade inställningar](#advanced-settings).

   ![Redigera produktrekommendation](./assets/pb-prex-edit.png){width="600" zoomable="yes"}

1. När du är klar gör du följande:

   - Om du arbetar med ett helt maximerat webbläsarfönster klickar du på _Stäng helskärm_ (![Stäng helskärmsikonen](./assets/pb-icon-reduce.png)) i det övre högra hörnet av arbetsytan.

   - Klicka **[!UICONTROL Save]** för att använda inställningarna och gå tillbaka till [!DNL Page Builder] arbetsyta.

   När du återgår till scenen visas produktplatshållarbilder i behållaren.

## Redigera inställningar för rekommendationsenhet

1. Håll pekaren över rekommendationsenhetsbehållaren för att visa verktygslådan och klicka på _Inställningar_ (![Ikonen Inställningar](./assets/pb-icon-settings.png){width="20"} ).

   ![Rekommendationsverktygslåda](./assets/pb-placeholder-toolbox.png){width="600" zoomable="yes"}

1. Gör nödvändiga ändringar i [Avancerade inställningar](#advanced-settings).

1. När du är klar klickar du på **[!UICONTROL Save]** för att använda inställningarna och gå tillbaka till [!DNL Page Builder] arbetsyta.

## Duplicera en rekommendationsenhet

1. Håll pekaren över rekommendationsenhetsbehållaren för att visa verktygslådan och klicka på _Duplicera_ ( ![Duplicera](./assets/pb-icon-duplicate.png){width="20"} ) i verktygslådan.

   Dupliceringen visas precis nedanför originalet.

1. Om du vill flytta den duplicerade rekommendationsenheten till en ny position håller du pekaren över behållaren och klickar på knappen _Flytta_ ( ![Ikonen Flytta](./assets/pb-icon-move.png){width="20"} ) i verktygslådan.

1. Markera och dra rekommendationsenheten tills den röda stödlinjen visas på den nya positionen.

   De övre och nedre kantlinjerna i varje behållare visas som streckade linjer när rekommendationsenheten flyttas.

## Ta bort en rekommendationsenhet från scenen

1. Håll pekaren över rekommendationsenhetsbehållaren och klicka på _Ta bort_ ( ![Ikonen Ta bort](./assets/pb-icon-remove.png){width="20"} ) i verktygslådan.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

## Avancerade inställningar

1. Om du vill styra placeringen av Product Recommendations-enheten i den överordnade behållaren väljer du **[!UICONTROL Alignment]**:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | `Default` | Använder den standardinställning för justering som anges i formatmallen för det aktuella temat. |
   | `Left` | Justerar enheten längs den vänstra kanten på den överordnade behållaren, med hänsyn till eventuell utfyllnad som har angetts. |
   | `Center` | Justerar enheten i mitten av den överordnade behållaren, med hänsyn till eventuell utfyllnad som har angetts. |
   | `Right` | Justerar enheten längs den högra kanten på den överordnade behållaren, med hänsyn till eventuell utfyllnad som har angetts. |

   {style="table-layout:auto"}

1. Ange **[!UICONTROL Border]** som används på alla fyra sidorna i Product Recommendations-enheten:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | `Default` | Använder det standardkantlinjeformat som anges av den associerade formatmallen. |
   | `None` | Visar inte någon synlig indikation på enhetsgränserna. |
   | `Dotted` | Enhetsramen visas som en prickad linje. |
   | `Dashed` | Enhetsramen visas som en streckad linje. |
   | `Solid` | Enhetsramen visas som en heldragen linje. |
   | `Double` | Enhetsramen visas som en dubbel linje. |
   | `Groove` | Enhetsgränsen visas som en utdragen linje. |
   | `Ridge` | Enhetsgränsen visas som en utdragen linje. |
   | `Inset` | Enhetsramen visas som en indragen linje. |
   | `Outset` | Enhetsramen visas som en startlinje. |

   {style="table-layout:auto"}

1. Om du anger ett annat kantlinjeformat än `None`slutför du visningsalternativen för kantlinjer:

   | Alternativ | Beskrivning |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Ange färgen genom att välja en färgruta, klicka på färgväljaren eller genom att ange ett giltigt färgnamn eller motsvarande hexadecimalt värde. |
   | [!UICONTROL Border Width] | Ange antalet pixlar för kantlinjens bredd. |
   | [!UICONTROL Border Radius] | Ange antalet pixlar för att definiera radiens storlek som används för att runda varje hörn av kanten. |

   {style="table-layout:auto"}

1. (Valfritt) Ange namnen på **[!UICONTROL CSS classes]** från den aktuella formatmallen som ska användas för enheten.

   Avgränsa flera klassnamn med blanksteg.

1. Ange värden i pixlar för **[!UICONTROL Margins and Padding]** för att fastställa enhetens yttre marginaler och inre utfyllnad.

   Ange motsvarande värden i diagrammet.

   | Behållarområde | Beskrivning |
   | ------ | ----------- |
   | [!UICONTROL Margins] | Mängden tomt utrymme som används på ytterkanten på alla sidor av enheten. Alternativ: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Mängden tomt utrymme som används på den inre kanten på alla sidor av enheten. Alternativ: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}
