---
title: Översikt över katalogsökning
description: Läs mer om de snabbsöknings- och avancerade sökverktyg som kunderna kan använda för att hitta produkter i butiken.
exl-id: a796fa48-212a-47c7-ab6e-98edd4d040f4
feature: Catalog Management, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# Översikt över katalogsökning

>[!TIP]
>
>[[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) ger en snabb, superrelevant och intuitiv sökupplevelse som är tillgänglig för Adobe Commerce utan extra kostnad. I det här avsnittet beskrivs standardsökfunktionen som kan skilja sig från [!DNL Live Search].

Forskning visar att personer som använder sökningar är mer benägna att köpa än kunder som bara använder navigering. Enligt vissa undersökningar är sannolikheten att köpa sökningar nästan dubbelt så stor för dem.

I följande avsnitt beskrivs de grundläggande katalogsökfunktionerna. Mer information om hur du konfigurerar och anpassar sökfunktionerna i den inbyggda katalogen finns i:

- [Konfigurera katalogsökning](search-configuration.md)
- [Sökresultat](search-results.md)
- [Hantera söktermer](search-terms.md)

>[!NOTE]
>
>Den inbyggda sökfunktionen i Commerce ger exakt matchande sökresultat. while [!DNL Live Search], en valfri modul som är tillgänglig för installation och aktivering i Adobe Commerce, implementeras annorlunda och resultatet begränsas inte till den exakta söksträngen. Om du t.ex. har tio produkter numrerade efter _Omega_: En sökning efter `Omega 1` ger en enda matchning för _Omega 1_ med den inbyggda sökfunktionen. Men samma söksträng som bygger på Live Search ger en matchning för flera objekt, _Omega 1_ och _Omega 10_.

## Snabbsökning

>[!NOTE]
>
>När [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html) när sökrutan är installerad returneras sökresultatet i en ruta.

Sökrutan i butikens sidhuvud hjälper besökare att hitta produkter i din katalog. Söktexten kan vara det fullständiga eller delvisa produktnamnet eller något annat ord eller fras som beskriver produkten. De söktermer som andra använder för att hitta produkter kan hanteras från administratören.

1. För **[!UICONTROL Search]** anger kunden de första bokstäverna i vad de vill hitta.

   Eventuella matchningar i katalogen visas nedan med antalet resultat.

1. Kunden trycker på Retur eller klickar på ett resultat i listan över matchande produkter.

   ![Sök](./assets/storefront-search-box.png){width="700" zoomable="yes"}

## Avancerad sökning

>[!NOTE]
>
>Funktionen för avancerad formulärsökning som beskrivs här gäller inte för [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

Med avancerad sökning kan kunderna söka i katalogen baserat på värden som anges i ett formulär. Eftersom formuläret innehåller flera fält kan en sökning innehålla flera parametrar. Resultatet är en lista över alla produkter i katalogen som uppfyller villkoren. En länk till den avancerade sökningen finns i sidfoten på din butik.

![Avancerad sökning](./assets/storefront-search-advanced.png){width="700" zoomable="yes"}

Varje fält i formuläret motsvarar ett attribut från produktkatalogen. Om du vill lägga till ett fält anger du attributets egenskaper för kantlinje till `Include in Advanced Search`. Som en god praxis bör du bara inkludera de fält som kunderna mest sannolikt använder för att hitta en produkt, eftersom sökningen går för långsammare.

1. I butikens sidfot klickar kunden **[!UICONTROL Advanced Search]**.

1. I _Avancerad sökning_ lägger till hela eller delar av värden i så många fält som behövs.

1. Klickningar **[!UICONTROL Search]** för att visa resultaten.

   ![Sökresultat](./assets/storefront-search-advanced-results-modify.png){width="700" zoomable="yes"}

1. Om de inte ser vad de letar efter i sökresultaten klickar kunden **[!UICONTROL Modify your search]** och försöker med en annan kombination av villkor.
