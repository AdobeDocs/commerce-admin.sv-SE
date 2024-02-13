---
title: Instrumentpanel för datahantering
description: Läs mer om Dashboard för datahantering
feature: Products, Customers, Data Import/Export
source-git-commit: 925af4d3841f2972dfffcd52125a41c4a4b28815
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Instrumentpanel för datahantering

Kontrollpanelen för datahantering ger insikt i dataströmmar för Adobe Commerce SaaS-produkter. Användare av [!DNL Live Search], [!DNL Product Recommendations]och [!DNL Catalog Service] kan visa produktsynkroniseringsstatus och synkronisera om data från en enda kontrollpanel.

Kontrollpanelen för datahantering finns på *System* > Dataöverföring > *Instrumentpanel för datahantering*.

![Instrumentpanel för datahantering](assets/data-management-dashboard.png)

## Inställningar

Knappen Inställningar till höger på sidan öppnar dialogrutan [[!DNL Catalog Sync]](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/data-services/catalog-sync.html) inställningsdialogrutan.

Normalt visas [!DNL Catalog Sync] körs automatiskt en gång i timmen.

Om katalogdata synkroniseras igen tvingas tjänsten att hämta data från Commerce-databasen och se till att de senaste ändringarna återspeglas i tjänsten och på din webbplats. Använd den här knappen om du har gjort flera produktändringar och du behöver uppdatera dessa innan den normala automatiska synkroniseringsprocessen.

## Synkroniseringsstatus

The _[!UICONTROL Sync]_statuspanelen visar antalet produkter som har synkroniserats under de senaste tre timmarna. Om du gör ovanliga uppdateringar av katalogen är det här värdet ofta noll. Klicka **[!UICONTROL Refresh]**för att uppdatera antalet.

## Antal produkter

Panelen för produktantal visar det totala antalet katalogprodukter som är tillgängliga för tjänsten.

The [!DNL Catalog Service] Kontrollpanelen visar det totala antalet produkter i katalogen som är tillgängliga för tjänsten. Detta är vanligtvis alla produkter i Commerce-databasen.

På panelerna för Recommendations och Live Search visas det totala antalet [_sökbar_](https://experienceleague.adobe.com/docs/commerce-admin/catalog/catalog/search/search.html) produkter. Om vissa produkter inte är inställda på att vara sökbara, skulle detta medföra skillnaden i produktsummor mellan [!DNL Product Recommendations] och [!DNL Live Search]och [!DNL Catalog Service].

## Synkroniserade produkter

Registret Synced Catalog Products innehåller information om produkterna i indexet. Som standard sorteras den här tabellen efter&quot;Senast uppdaterad&quot;.

Om du vill hitta en viss produkt använder du**[!UICONTROL Search by SKU]** fält .
Om du vill styra vilka kolumner som ska visas klickar du på **[!UICONTROL Customize Table]** till höger om bordet.
