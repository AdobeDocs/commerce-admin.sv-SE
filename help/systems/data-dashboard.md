---
title: Instrumentpanel för datahantering
description: Lär dig hur du får tillgång till insikter om dataströmmar för  [!DNL Catalog Service], [!DNL Live Search] och [!DNL Product Recommendation]s.
feature: Products, Customers, Data Import/Export
exl-id: 63c261c1-1a52-46f7-93f8-81055edf1f7b
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Instrumentpanel för datahantering

Kontrollpanelen för datahantering ger en översikt över synkroniseringsstatusen för produktdata som överförs från Commerce-databasen till Commerce SaaS-tjänster. Användare kan enkelt övervaka status för produktsynkronisering och initiera omsynkronisering av data från en enhetlig kontrollpanel. Den här funktionen ger värdefulla insikter om tillgängligheten av produktdata för butiken, så att den snabbt kan visas för kunderna.

## Målgrupp

Kontrollpanelen för datahantering är tillgänglig utan extra kostnad för alla Commerce-handlare som använder [[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview), [[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/en/docs/commerce/live-search/guide-overview) eller [[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview) med en aktiv licens.

Kontrollpanelen för datahantering finns på *System* > Dataöverföring > *Kontrollpanelen för datahantering*.

![Instrumentpanel för datahantering](assets/data-management-dashboard.png)

Kontrollpanelen innehåller följande fält:

| Fält | Beskrivning |
|--- |--- |
| Omfång | Specifik webbplats för synkroniserade data. |
| [!DNL Product Recommendations] | Visar synkroniseringsstatus, antal synkroniserade produkter och en tabell över de [visningsbara](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) synkroniserade produkterna för [!DNL Product Recommendations]. |
| [!DNL Live Search] | Visar synkroniseringsstatus, antal synkroniserade produkter och en tabell över de [visningsbara](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) synkroniserade produkterna för [!DNL Live Search]. |
| [!DNL Catalog Service] | Visar synkroniseringsstatus, antal synkroniserade produkter och en tabell över synkroniserade produkter för [!DNL Catalog Service]. |
| Inställningar | Öppnar en dialogruta där du kan [synkronisera om katalogdata manuellt](#resync-catalog-data). |
| Synkroniseringsstatus | Visar antalet produkter som har överförts från Commerce-databasen till någon av SaaS-tjänsterna under de senaste tre timmarna. Om du gör ovanliga uppdateringar av katalogen är det här värdet ofta noll. Om en synkronisering pågår klickar du på **[!UICONTROL Refresh]** för att få ett uppdaterat antal. |
| Antal produkter | Återspeglar det totala antalet katalogprodukter som är tillgängliga för tjänsten. Kontrollpanelerna [!DNL Product Recommendations] och [!DNL Live Search] visar det totala antalet _visningsbara_ produkter. [!DNL Catalog Service] filtrerar inte produkter efter visning, så om du har både [!DNL Catalog Service] och [!DNL Live Search] eller [!DNL Product Recommendations] installerat kan de två kontrollpanelerna visa två olika värden för produktantalet. |
| Synkroniserade produkter | Innehåller information om produkterna i Commerce index. Som standard sorteras den här tabellen efter&quot;Senast uppdaterad&quot;. Om du vill hitta en viss produkt använder du fältet **[!UICONTROL Search by SKU]**. Om du vill styra vilka kolumner som visas klickar du på **[!UICONTROL Customize Table]** till höger om tabellen. |

## Använda kontrollpanelen för datahantering

När du uppdaterar produkter i Commerce-databasen överförs produktdata till SaaS-tjänster enligt din systemkonfiguration. När synkroniseringsprocessen initieras visar **Antal produkter** antalet produkter som skickats till SaaS-tjänster.

>[!IMPORTANT]
>
>Den tid det tar att slutföra synkroniseringen varierar beroende på katalogstorleken och volymen på uppdaterade data.

När antalet bearbetade produkter matchar antalet uppdaterade produkter anger det att synkroniseringen är klar.

>[!NOTE]
>
>Adobe tillhandahåller också ett kommandoradsgränssnitt och systemloggar som utvecklare och systemintegratörer kan använda för att hantera och spåra synkroniseringsåtgärder och felsöka fel för Commerce SaaS-tjänster. Mer information finns i [Exportguiden för SaaS-data](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview).

### Lista över synkroniserade produkter

Om du vill visa information om en synkroniserad produkt klickar du på produkten i tabellen.

![Synkroniserad produktinformation](assets/sync-product-detail.png)

### Synkronisera om katalogdata

För att dina Commerce SaaS-tjänster alltid ska vara uppdaterade med den senaste produktinformationen bör du [implementera ett schema](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-indexers#reindex) för synkronisering av katalogdata.

Även om du [manuellt kan initiera](#manually-resync-catalog) en omsynkronisering av katalogdata från Commerce-databasen till SaaS-tjänster, rekommenderas inte det eftersom det kan öka belastningen på maskinvaruresurserna. Du kan behöva synkronisera om katalogen manuellt i följande scenarier:

- När du gör stora ändringar i produktkatalogen, till exempel lägger till nya produkter, uppdaterar produktinformation eller ändrar kategorier

- Om du märker några avvikelser eller prestandaproblem när du visar produktdata i dina butiker

- Följa uppdateringar eller ändringar av integreringar mellan Commerce-databasen och SaaS-tjänsterna

- När anpassningar eller konfigurationer distribueras som påverkar hanteringen av produktdata eller synkroniseringsprocesserna

Genom att följa dessa riktlinjer och aktivt återsynkronisera katalogdata efter behov kan du upprätthålla datakonsekvens, precision och tillförlitlighet i hela Adobe Commerce-ekosystemet.

#### Synkronisera om katalog manuellt

Om du behöver synkronisera om katalogdata klickar du på **[!UICONTROL Settings]** till höger på sidan för att visa en dialogruta där du kan starta en omsynkronisering. Om katalogdata synkroniseras igen tvingas tjänsten att hämta data från Commerce-databasen till SaaS-tjänster.

![Synkronisera produkter manuellt](assets/resync-data.png)
