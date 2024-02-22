---
title: Instrumentpanel för datahantering
description: Lär dig hur du får information om dataströmmar för Catalog Service, Live Search, Product Recommendations.
feature: Products, Customers, Data Import/Export
source-git-commit: eed80afd8755d416d979c362f8c21fe97ce2d2ba
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---


# Instrumentpanel för datahantering

Kontrollpanelen för datahantering ger insikt i dataströmmar för Adobe Commerce SaaS-produkter. Användare av [!DNL Live Search], [!DNL Product Recommendations]och [!DNL Catalog Service] kan visa produktsynkroniseringsstatus och synkronisera om data från en enda kontrollpanel.

Kontrollpanelen för datahantering finns på *System* > Dataöverföring > *Instrumentpanel för datahantering*.

![Instrumentpanel för datahantering](assets/data-management-dashboard.png)

## Inställningar

The **[!UICONTROL Settings]** till höger på sidan öppnas en dialogruta där du kan synkronisera om katalogdata.

Om katalogdata synkroniseras igen måste tjänsten hämta data från Commerce-databasen. Den här åtgärden används vanligtvis under första gången du startar programmet när katalogsynkroniseringen inte har körts på ett par timmar.

## Synkroniseringsstatus

The _[!UICONTROL Sync]_statuspanelen visar antalet produkter som har synkroniserats under de senaste tre timmarna. Om du gör ovanliga uppdateringar av katalogen är det här värdet ofta noll. Klicka **[!UICONTROL Refresh]**för att uppdatera antalet.

## Antal produkter

Panelen för produktantal visar det totala antalet katalogprodukter som är tillgängliga för tjänsten.

The [!DNL Product Recommendations] och [!DNL Live Search] instrumentpaneler visar totalt antal _visningsbar_ produkter. [!DNL Catalog Service] filtrerar inte produkter efter visning, så om du har båda [!DNL Catalog Service] och [!DNL Live Search] eller [!DNL Product Recommendations] kan de två kontrollpanelerna visa två olika värden för antalet produkter.

## Synkroniserade produkter

Registret Synced Products (Synkroniserade produkter) innehåller information om produkterna i indexet. Som standard sorteras den här tabellen efter&quot;Senast uppdaterad&quot;.

Om du vill hitta en viss produkt använder du **[!UICONTROL Search by SKU]** fält .
Om du vill styra vilka kolumner som ska visas klickar du på **[!UICONTROL Customize Table]** till höger om bordet.
