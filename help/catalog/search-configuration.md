---
title: Konfigurera katalogsökning
description: Lär dig konfigurera katalogsökning för din butik.
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# Konfigurera katalogsökning

Det finns två varianter av katalogsökningskonfigurationen. Den första metoden beskriver de tillgängliga inställningarna när [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) installeras. Den andra metoden beskriver konfigurationsinställningarna för Adobe Commerce med [Elasticsearch][1]{:target=&quot;_blank&quot;}.

## Metod 1: Adobe Commerce med [!DNL Live Search]

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Catalog Search]**.

   ![Katalogsökning för Live-sökning](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   En detaljerad lista över dessa alternativ finns i [Adobe Commerce med Live Search](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) i _Konfigurationsreferens_.

1. Om du vill begränsa längden och antalet ord för söktexten anger du ett värde för **[!UICONTROL Minimal Query Length]** och **[!UICONTROL Maximum Query Length]**.

1. Om du vill begränsa mängden populära sökresultat till cache för snabbare svar anger du ett värde för **[!UICONTROL Number of top search results to cache]**.

   Standardvärdet är `100`. Om du anger värdet `0` cachelagras alla söktermer och sökresultat när de anges en andra gång.

1. Om du vill ändra det maximala antalet rader som är tillgängliga för returnerade resultat i [storefront-popup-fönstret över](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html) anger du ett annat **[!UICONTROL Autocomplete Limit]**-värde.

   Genom att begränsa antalet rader förbättras sökningens prestanda och storleken på den returnerade listan minskas. Standardvärdet är `8` rader.

## Metod 2: Commerce med Elasticsearch

>[!IMPORTANT]
>
>På grund av meddelandet [!DNL Elasticsearch 7] om att supporten upphör i augusti 2023 rekommenderar vi att alla Adobe Commerce-kunder migrerar till sökmotorn OpenSearch 2.x. Mer information om hur du migrerar sökmotorn under produktuppgraderingen finns i [Migrera till OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) i _uppgraderingshandboken_.

### Steg 1: Konfigurera allmänna sökalternativ

>[!NOTE]
>
>Med Elasticsearch finns det inget körklart stöd för sökning med suffixet. Sökning med SKU kanske inte returnerar det förväntade resultatet om nyckelordet bara innehåller slutdelen av SKU:n.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Catalog Search]**.

   ![Inställningar för Elasticsearch](../configuration-reference/catalog/assets/catalog-search-elasticsearch.png){width="600" zoomable="yes"}

   Mer information om de här alternativen finns i [Adobe Commerce med Elasticsearch](../configuration-reference/catalog/catalog.md#adobe-commerce-with-elasticsearch) i _Konfigurationsreferens_.

1. Om du vill begränsa längden och antalet ord för söktexten anger du ett värde för **[!UICONTROL Minimal Query Length]** och **[!UICONTROL Maximum Query Length]**.

   >[!IMPORTANT]
   >
   >Det värde som anges för detta lägsta och högsta intervall måste vara kompatibelt med motsvarande intervall som anges i sökmotorkonfigurationen för Elasticsearch. Om du till exempel anger de här värdena som `2` och `300` i Commerce, uppdaterar du motsvarande värden i sökmotorn.

1. Om du vill begränsa mängden populära sökresultat till cache för snabbare svar anger du ett värde för **[!UICONTROL Number of top search results to cache]**.

   Standardvärdet är `100`. Om du anger värdet `0` cachelagras alla söktermer och sökresultat när de anges en andra gång.

1. Om du vill aktivera eller inaktivera Product EAV-indexeraren anger du **[!UICONTROL Enable EAV Indexer]**.

   Den här funktionen förbättrar indexeringshastigheten och begränsar indexeraren från att användas av tillägg från tredje part.

1. Om du vill begränsa det maximala antalet sökresultat som ska visas för automatisk slutförd sökning anger du ett belopp för **[!UICONTROL Autocomplete Limit]**.

   Om du begränsar den här mängden ökar sökningens prestanda och storleken på den visade listan minskar. Standardvärdet är `8`.

### Steg 2: Konfigurera anslutningen till Elasticsearch

>[!IMPORTANT]
>
>Fälten **[!UICONTROL Search Engine]**, **[!UICONTROL Elasticsearch Server Hostname]**, **[!UICONTROL Elasticsearch Server Port]**, **[!UICONTROL Elasticsearch Index Prefix]**, **[!UICONTROL Enable Elasticsearch HTTP Auth]** och **[!UICONTROL Elasticsearch Server Timeout]** konfigurerades när Commerce installerades eller uppgraderades. Dessa värden bör endast ändras när du uppgraderar eller ändrar Elasticsearch.

1. Acceptera standardvärdet `Elasticsearch 7` för **[!UICONTROL Search Engine]**.

   Elasticsearch 7.6.x krävs för alla installationer av Commerce.

1. Acceptera standardvärdet som konfigurerades när Commerce installerades för **[!UICONTROL Elasticsearch Server Hostname]**.

   I detta exempel är standardvärdet `elasticsearch.internal`.

1. Acceptera standardvärdet som konfigurerades när Commerce installerades för **[!UICONTROL Elasticsearch Server Port]**.

   I detta exempel är standardvärdet `9200`.

1. För **[!UICONTROL Elasticsearch Index Prefix]** anger du ett prefix som identifierar indexvärdet för Elasticsearch.

   Standardvärdet är `magento2`.

1. Om du vill använda HTTP-autentisering för att fråga efter användarnamn och lösenord för att få åtkomst till Elasticsearch Server anger du **[!UICONTROL Enable Elasticsearch HTTP Auth]** till `Yes`.

1. För **[!UICONTROL Elasticsearch Server Timeout]** anger du antalet sekunder innan systemtimeout inträffar.

   Standardvärdet är `15`.

1. Verifiera konfigurationen genom att klicka på **[!UICONTROL Test Connection]**.

### Steg 3: Konfigurera förslag och rekommendationer

>[!NOTE]
>
>Sökförslag och rekommendationer kan påverka serverprestanda.

1. Ange **[!UICONTROL Enable Search Recommendations]** till `Yes` och gör följande om du vill erbjuda rekommendationer:

   - Ange antalet rekommendationer som ska erbjudas för **[!UICONTROL Search Recommendation Count]**.

   - Om du vill visa antalet resultat som hittats för varje rekommendation anger du **[!UICONTROL Show Results Count for Each Recommendation]** till `Yes`.

1. Ange **[!UICONTROL Enable Search Suggestions]** till `Yes` och gör följande:

   - För **[!UICONTROL Search Suggestions Count]** anger du antalet sökförslag som ska erbjudas.

   - Om du vill visa antalet resultat för varje förslag anger du **[!UICONTROL Show Results for Each Suggestion]** till `Yes`.

### Steg 4: Konfigurera minimivillkor för att matcha

Ange ett värde för **[!UICONTROL Minimum Terms to Match]** om du vill kontrollera det minsta antal termer från din fråga som sökresultaten ska matcha för retur. Om du anger det här värdet blir resultatet optimalt relevant för kunderna. En lista över godkända värden finns i [minimum_should_match-parametern](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-minimum-should-match.html) i dokumentationen för Elasticsearch.

Klicka på **[!UICONTROL Save Config]** när du är klar.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/search/overview-search.html
