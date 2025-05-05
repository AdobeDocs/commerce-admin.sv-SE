---
title: Mellanlagring av innehåll
description: Med Content Staging kan ert affärsteam enkelt skapa, förhandsgranska och schemalägga en mängd olika innehållsuppdateringar för er butik direkt från administratören.
exl-id: 929cd020-cbc7-40bf-a22c-02df35212ecf
feature: Page Content, Staging
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 07d7ca7e7f6af42fe8e06dc3c49c2df5f50d1425
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# Mellanlagring av innehåll

{{ee-feature}}

Med innehållstaggning kan ditt affärsteam enkelt skapa, förhandsgranska och schemalägga en mängd innehållsuppdateringar för din butik direkt från _Admin_. I stället för att tänka på en statisk sida bör du överväga att en sida ska vara en samling med olika element som kan aktiveras _den_ eller _av_ baserat på ett schema. Du kan använda innehållstaggning för att skapa en sida som ändras automatiskt under året enligt ett schema.

Termen _kampanj_ refererar till posten för en schemalagd ändring, eller en samling ändringar som hanteras från mellanlagringsinstrumentpanelen. Ändringarna kan visas i en kalender eller tidslinje. Termerna _schemalagd ändring_ och _schemalagd uppdatering_ är utbytbara och refererar till en enskild ändring.

När du schemalägger en innehållsändring för en viss tidsperiod återgår innehållet till den tidigare versionen när den schemalagda ändringen upphör att gälla. Du kan skapa flera versioner av samma baslinjeinnehåll som ska användas för framtida uppdateringar. Du kan också stega dig tillbaka genom tidslinjen för att visa tidigare versioner av innehållet. Om du vill spara ett utkast anger du bara ett datum på tidslinjen som är så långt in i framtiden att det aldrig går till produktion.

## Mellanlagringsobjekt och kampanjer för innehåll

Fält som är relaterade till startdatum och slutdatum har tagits bort från Adobe Commerce och kan inte ändras direkt på kundvagnsprisregeln, katalogprisregeln, produkten, kategorin och CMS-sidan. Du måste skapa en schemalagd uppdatering för dessa aktiveringar.

Alla schemalagda uppdateringar tillämpas i följd, vilket innebär att alla enheter bara kan ha en schemalagd uppdatering åt gången. Alla schemalagda uppdateringar tillämpas på alla butiksvyer inom tidsramen. Därför kan en enhet inte ha en annan schemalagd uppdatering för olika butiksvyer samtidigt. Alla värden för entitetsattribut i alla butiksvyer, som inte påverkas av den aktuella schemalagda uppdateringen, hämtas från standardvärdena och inte från den tidigare schemalagda uppdateringen.

När en ny schemalagd uppdatering skapas för något av följande objekt skapas en motsvarande kampanj som platshållare och rutan _[!UICONTROL Scheduled Changes]_&#x200B;visas längst upp på sidan. Platshållarkampanjen har ett startdatum, men inte ett slutdatum. Du kan schemalägga uppdateringar av innehållet som en del av en kampanj och sedan förhandsgranska och dela ändringarna per datum, tid eller butiksvy. När en ny kampanj har skapats för ett objekt kan du tilldela den som en schemalagd uppdatering för andra objekt.

- [Produkter](../catalog/product-scheduled-changes.md)
- [Kategorier](../catalog/category-scheduled-changes.md)
- [Katalogprisregler](../merchandising-promotions/price-rule-catalog-scheduled-changes.md)
- [Kundprisregler](../merchandising-promotions/price-rule-cart-scheduled-changes.md)
- [CMS Pages](pages-workspace.md#scheduled-changes)
- [CMS Blocks](blocks.md)

## Arbetsflöde för innehållstagning

1. **Skapa baslinjeinnehållet**

   Baslinjen är innehållet i en resurs utan kampanj och innehåller allt under avsnittet _[!UICONTROL Scheduled Changes]_&#x200B;överst på sidan. Baslinjeinnehållet används alltid, såvida det inte finns en aktiv kampanj med ändringar schemalagda för den platsen på tidslinjen.

1. **Skapa den första kampanjen**

   Skapa din första kampanj med start- och slutdatum efter behov. Lämna slutdatumet tomt om du vill att kampanjen ska vara öppen. När den första kampanjen avslutas återställs det ursprungliga baslinjeinnehållet.

   Startdatum och slutdatum för kampanj måste definieras med hjälp av administratörstidszonen **_default_** som konverteras från den lokala tidszonen för varje webbplats. Tänk dig ett exempel där du har flera webbplatser i olika tidszoner, men du vill starta en kampanj som baseras på en tidszon i USA. I det här fallet måste du schemalägga en separat uppdatering för varje lokal tidszon och ange **[!UICONTROL Start Date]** och **[!UICONTROL End Date]** som konverteras från varje lokal webbplats tidszon till standardtidszonen för administratörer.

1. **Lägg till en andra kampanj**

   Skapa den andra kampanjen med start- och slutdatum efter behov. Den andra kampanjen kan tilldelas en helt annan tidsperiod. När du skapar flera kampanjer för samma resurs kan kampanjerna inte överlappa varandra. Ni kan skapa så många kampanjer som behövs.

   Flera resurser kan tilldelas till en befintlig kampanj som inte har startats ännu. Två olika produktpriser kan till exempel uppdateras inom samma kampanj med ett framtida startdatum.

   >[!NOTE]
   >
   >Om en kampanj är länkad till mer än en entitet kan kampanjen bara redigeras från [kontrollpanelen för innehållsmellanlagring](content-staging-dashboard.md).

1. **Återställ baslinjeinnehållet**

   Om alla kampanjer har slutdatum återställs baslinjeinnehållet när alla aktiva kampanjer avslutas.

   >[!NOTE]
   >
   >Om en aktiv kampanj initialt skapas utan ett slutdatum kan kampanjen inte redigeras senare så att den innehåller ett slutdatum. I så fall är det nödvändigt att skapa en dubblettkampanj och ange det slutdatum som behövs.

>[!NOTE]
>
>När en mellanlagringsuppdatering är aktiv för en entitet redigerar entiteten den aktuella aktiva mellanlagringsuppdateringen. Det påverkar inte baslinjeinnehållet, som återställs när mellanlagringsuppdateringen avslutas.

## Kontrollpanel för [!UICONTROL Content Staging]

[!UICONTROL Content Staging] [dashboard](content-staging-dashboard.md) ger synlighet i alla planerade webbplatsändringar och uppdateringar. Alla dagar, datumintervall och tidsperioder i en kampanj kan förhandsgranskas och delas med andra.

![Kontrollpanel för mellanlagring](./assets/content-staging-dashboard-grid.png){width="600" zoomable="yes"}

## Demo om innehållstagning

Titta på den här videon om du vill veta mer om innehållstagning:

>[!VIDEO](https://video.tv.adobe.com/v/343784?quality=12&learn=on)

## Felsökningsresurser

Hjälp med felsökning av problem med innehållstagning finns i följande artiklar i [!DNL Commerce] kunskapsbasen med supportfrågor:

- [Fel 404 på alla sidor på grund av problem med mellanlagring av innehåll](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/site-down-or-unresponsive/error-404-on-all-pages-due-to-content-staging-issue.html?lang=sv-SE)
- [Uppdateringar för schemalagd förproduktion av innehåll visas inte med inaktuell snabbcache](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/scheduled-content-staging-updates-not-displayed-with-stale-fastly-cache.html?lang=sv-SE)
- [Kan jag schemalägga uppdateringar av innehållsmellanlagring för priser i en delad katalog?](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/faq/can-i-schedule-content-staging-updates-for-prices-in-a-shared-catalog.html?lang=sv-SE)
