---
title: Lägg till innehåll - produktrekommendationer
description: Läs mer om innehållstypen Produktrekommendationer som används för att lägga till en lista med rekommendationer på  [!DNL Page Builder] scenen.
exl-id: ca90c10d-8d7a-42a2-bb13-2602aa9d6eef
feature: Page Builder, Page Content, Recommendations
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---

# Lägg till innehåll - produktrekommendationer

Använd innehållstypen _Produktrekommendationer_ för att lägga till en befintlig, aktiv [rekommendationsenhet](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/admin/create) på [[!DNL Page Builder] scenen](workspace.md#stage) för en CMS-sida, ett-block eller ett dynamiskt block.

>[!NOTE]
>
>Innehållstypen [!DNL Page Builder] _Produktrekommendationer_ stöds i Adobe Commerce 2.4.4 och senare och finns i [produktrekommendationspaketet version 3.0.x eller senare](https://commercemarketplace.adobe.com/magento-product-recommendations.html). Om du vill lägga till [!DNL Page Builder]-stöd för produktrekommendationer [läser du installationsinformationen](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/getting-started/install-configure). **Den här innehållstypen är inte tillgänglig för Magento Open Source.**

{{$include /help/_includes/page-builder-save-timeout.md}}

## Verktygslåda för produktrekommendationer

| Verktyg | Ikon | Beskrivning |
| --- | --| --- |
| Flytta | ![Ikonen Flytta](./assets/pb-icon-move.png){width="25"} | Flyttar produktrekommendationsbehållaren och dess innehåll till en annan position på scenen. |
| Inställningar | ![Ikon för inställningar](./assets/pb-icon-settings.png){width="25"} | Öppnar sidan Redigera produktrekommendation, där du kan välja rekommendationsenhet och ändra egenskaperna för behållaren. |
| Dölj | ![Dölj ikon](./assets/pb-icon-hide.png){width="25"} | Döljer den aktuella produktrekommendationsbehållaren och dess innehåll. |
| Visa | ![Visa ikon](./assets/pb-icon-show.png){width="25"} | Visar den dolda produktrekommendationsbehållaren och dess innehåll. |
| Duplicera | ![Duplicera ikon](./assets/pb-icon-duplicate.png){width="25"} | Skapar en kopia av produktrekommendationsbehållaren och dess innehåll. |
| Ta bort | ![Ikonen Ta bort](./assets/pb-icon-remove.png){width="25"} | Tar bort produktrekommendationsbehållaren och dess innehåll från scenen. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Lägg till en befintlig rekommendationsenhet

1. Kontrollera att du redan [har skapat en rekommendationsenhet](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/admin/create) för sidtypen [!DNL Page Builder].

>[!NOTE]
>
>Du kan bara skapa rekommendationsenheter för sidtypen [!DNL Page Builder] i standardbutiksvyn.

1. Öppna sidan, blocket eller det dynamiska blocket i redigeringsläge.

1. Expandera avsnittet _[!UICONTROL Content]_och klicka på&#x200B;**[!UICONTROL Edit with Page Builder]**eller inuti förhandsvisningsområdet för innehåll för att öppna arbetsytan för [!DNL Page Builder].

1. Dra en [!DNL Page Builder]-platshållare till scenen på panelen _[!UICONTROL Layout]_under **[!UICONTROL Row]**.

1. Dra en [!DNL Page Builder]-platshållare till raden på panelen _[!UICONTROL Add Content]_under **[!UICONTROL Product Recommendation]**.

   ![Lägger till produktrekommendationens innehållstyp](./assets/pb-add-prex-drag.png){width="600" zoomable="yes"}

1. Gör något av följande:

   - Klicka på **[!UICONTROL Edit Product Recommendation]**.
   - Håll pekaren över den tomma behållaren för att visa verktygslådan och klicka på ikonen _Inställningar_ (![Inställningar-ikon](./assets/pb-icon-settings.png)).

   ![Redigera produktrekommendation](./assets/pb-prex-toolbox.png){width="600" zoomable="yes"}

1. Klicka på _[!UICONTROL Selection]_i avsnittet **[!UICONTROL Select]**.

1. I listan med aktiva produktrekommendationer letar du reda på raden med rekommendationsenheten som du vill lägga till och klickar på **[!UICONTROL Select]** i den sista kolumnen.

   ![Vald produktrekommendation](./assets/pb-prex-select.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Add Selected]** i det övre högra hörnet.

   Namnet på den valda produktrekommendationen visas i avsnittet _[!UICONTROL Selection]_på sidan_[!UICONTROL Edit Product Recommendation]_.

1. Gör de ändringar som krävs för de [avancerade inställningarna](#advanced-settings).

   ![Redigera produktrekommendation](./assets/pb-prex-edit.png){width="600" zoomable="yes"}

1. När du är klar gör du följande:

   - Om du arbetar med ett helt maximerat webbläsarfönster klickar du på ikonen _Stäng helskärm_ (![Stäng helskärm ](./assets/pb-icon-reduce.png)) i det övre högra hörnet av arbetsytan.

   - Klicka på **[!UICONTROL Save]** om du vill använda inställningarna och återgå till arbetsytan i [!DNL Page Builder].

   När du återgår till scenen visas produktplatshållarbilder i behållaren.

## Redigera inställningar för rekommendationsenhet

1. Håll pekaren över rekommendationsenhetsbehållaren för att visa verktygslådan och klicka på ikonen _Inställningar_ (![Inställningar-ikon](./assets/pb-icon-settings.png)).

   ![Rekommendationsverktygslåda](./assets/pb-placeholder-toolbox.png){width="600" zoomable="yes"}

1. Gör de ändringar som krävs för de [avancerade inställningarna](#advanced-settings).

1. När du är klar klickar du på **[!UICONTROL Save]** för att tillämpa inställningarna och återgå till arbetsytan i [!DNL Page Builder].

## Duplicera en rekommendationsenhet

1. Håll pekaren över rekommendationsenhetsbehållaren för att visa verktygslådan och klicka på ikonen _Duplicera_ (![Duplicera ikon](./assets/pb-icon-duplicate.png)) i verktygslådan.

   Dupliceringen visas precis nedanför originalet.

1. Om du vill flytta den duplicerade rekommendationsenheten till en ny plats håller du pekaren över behållaren och klickar på ikonen _Flytta_ (![Flytta ](./assets/pb-icon-move.png)) i verktygslådan.

1. Markera och dra rekommendationsenheten tills den röda stödlinjen visas på den nya positionen.

   De övre och nedre kantlinjerna i varje behållare visas som streckade linjer när rekommendationsenheten flyttas.

## Ta bort en rekommendationsenhet från scenen

1. Håll pekaren över rekommendationsenhetsbehållaren och klicka på ikonen _Ta bort_ ( ![Ta bort ikon](./assets/pb-icon-remove.png)) i verktygslådan.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

## Avancerade inställningar

1. Om du vill styra placeringen av produktrekommendationsenheten i den överordnade behållaren väljer du **[!UICONTROL Alignment]**:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | `Default` | Använder den standardinställning för justering som anges i formatmallen för det aktuella temat. |
   | `Left` | Justerar enheten längs den vänstra kanten på den överordnade behållaren, med hänsyn till eventuell utfyllnad som har angetts. |
   | `Center` | Justerar enheten i mitten av den överordnade behållaren, med hänsyn till eventuell utfyllnad som har angetts. |
   | `Right` | Justerar enheten längs den högra kanten på den överordnade behållaren, med hänsyn till eventuell utfyllnad som har angetts. |

   {style="table-layout:auto"}

1. Ange den **[!UICONTROL Border]**-stil som ska användas på alla fyra sidorna av enheten för produktrekommendationer:

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

1. Om du anger ett annat kantlinjeformat än `None` fyller du i visningsalternativen för kantlinjen:

   | Alternativ | Beskrivning |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Ange färgen genom att välja en färgruta, klicka på färgväljaren eller genom att ange ett giltigt färgnamn eller motsvarande hexadecimalt värde. |
   | [!UICONTROL Border Width] | Ange antalet pixlar för kantlinjens bredd. |
   | [!UICONTROL Border Radius] | Ange antalet pixlar för att definiera radiens storlek som används för att runda varje hörn av kanten. |

   {style="table-layout:auto"}

1. (Valfritt) Ange namnen på **[!UICONTROL CSS classes]** från den aktuella formatmallen som ska användas för enheten.

   Avgränsa flera klassnamn med blanksteg.

1. Ange värden (i pixlar) för **[!UICONTROL Margins and Padding]** för att fastställa enhetens yttre marginaler och inre utfyllnad.

   Ange motsvarande värden i diagrammet.

   | Behållarområde | Beskrivning |
   | ------ | ----------- |
   | [!UICONTROL Margins] | Mängden tomt utrymme som används på ytterkanten på alla sidor av enheten. Alternativ: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Mängden tomt utrymme som används på den inre kanten på alla sidor av enheten. Alternativ: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
