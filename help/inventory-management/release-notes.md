---
title: Versionsinformation för [!DNL Inventory Management]
description: Läs versionsinformationen om du vill ha information om alla  [!DNL Inventory Management] releaser.
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: fdc14758788fa5cd0391371ebfafb478dadec8a4
workflow-type: tm+mt
source-wordcount: '3462'
ht-degree: 0%

---

# Versionsinformation för [!DNL Inventory Management]

I versionsinformationen beskrivs releaser av [!DNL Inventory Management] och här ingår:

![Nya](../assets/new.svg) nya funktioner
![ Åtgärdat problem ](../assets/fix.svg) Korrigeringar och förbättringar
![Kända fel](../assets/bug.svg)

[!DNL Inventory Management] är ett specialprojekt för Magento Open Source Community Engineering som är öppet för medverkande. Om du vill delta och bidra läser du [GitHub-projektet](https://github.com/magento/inventory) och [wiki](https://github.com/magento/inventory/wiki) för att komma igång. Om du vill diskutera projektet går du med i [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY)-kanalen ([självregistrering](https://opensource.magento.com/slack)).

[Frigör schema](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html){target="_blank"} för kompatibla och stöds.

## v1.2.7

Versionsinformation för [!DNL Inventory Management] 1.2.7 finns i versionsinformationen för [core 2.4.7 ](https://experienceleague.adobe.com/en/docs/commerce-operations/release/notes/adobe-commerce/2-4-7#inventory-management-1).

## v1.2.6

[!DNL Inventory Management] 1.2.6 (modulversion: `magento/inventory-metapackage = 1.2.6`) stöds med version 2.4.6 och är kompatibel med version 2.4.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och Magento Open Source kodbas.

![Korrigerat problem](../assets/fix.svg) I butiken visas nu sammansatta produkter (konfigurerbara, paketerade och grupperade) som i lager när underordnade produkter som har sålts ut returneras till lager. Tidigare angav storefront att den sammansatta produkten inte fanns i lager under dessa förhållanden. <!-- ACP2E-1106-->

![Åtgärdat problem](../assets/fix.svg) Konfigurerbara produktalternativ visas nu som förväntat utanför lagret om alternativet skapades med kvantitet inställd på 0 och **[!UICONTROL Display out-of-stock products]** är aktiverat. <!-- ACP2E-1148-->

![Åtgärdat problem](../assets/fix.svg) Kategorisidcache ogiltigförklaras inte längre när lagerkvantiteten ändras och produkten fortfarande finns i lager. Adobe Commerce läser nu in sidor från cacheminnet i stället för att återskapa dem när produktkvantiteten (och inget annat) på kategoritappen för butiker ändras. <!-- ACP2E-118-->

![Korrigerat problem](../assets/fix.svg) Antalet produkter i kategorilistan är nu korrekt när du använder Inventory i enkälläge med inställningen **[!UICONTROL Display Out-Of-Stock Products]** aktiverad. Adobe Commerce kontrollerar nu om en produkt går att sälja vid inventering. <!-- ACP2E-1033-->

![Korrigerat problem](../assets/fix.svg) Kundprisregler för butiksleverans fungerar nu som förväntat när Lager är aktiverat. Tidigare tillämpades inte rabatter som genererats av kundvagnsregler under dessa villkor. <!-- ACP2E-1015-->

![Korrigerat problem](../assets/fix.svg) Om produktlager uppdateras i schemalagt läge rensas inte längre alla cacheminnen. Tidigare rensade lagerindexeraren alla konfigurationscache. <!-- ACP2E-1003-->

![Korrigerat problem](../assets/fix.svg) Värdet för attributet **[!UICONTROL Allow Multiple Boxes for Shipping]** för en produkt i avancerad inventering sparas nu som förväntat. <!-- ACP2E-992-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce utfärdar nu korrekt reservationskompensation efter en partiell återbetalningskreditnota för en order som placerats med inlagerhämtning. Tidigare sparades en felaktig reservation i tabellen `inventory_reservation` när en administratörsanvändare skapade en kreditnota utan att markera kryssrutan **[!UICONTROL Return to Stock]**. <!-- ACP2E-979-->

![Åtgärdat problem](../assets/fix.svg) Adobe Commerce visar inte längre konfigurerbara produkter som finns utanför lagret när en av dess variationer manuellt har returnerats till lager i distributioner som implementerar lager med flera källor. <!-- ACP2E-952-->

![Åtgärdat problem](../assets/fix.svg) Kolumnpositionen i produktrutnätet (**[!UICONTROL Catalog]** > **[!UICONTROL Products]**) återgår inte längre till den tidigare positionen när sidan har lästs in på nytt i distributioner med flera konfigurerade lagerkällor. <!-- ACP2E-925-->

![Åtgärdat problem](../assets/fix.svg) Lagerkvantiteten är nu korrekt efter att en kreditnota har utfärdats för en virtuell produkt när kryssrutan **[!UICONTROL Back to stock]** inte har valts. <!-- ACP2E-908-->

![Korrigerat problem](../assets/fix.svg) Du kan nu spara kategorier med automatisk produktsortering och omfång som är tilldelat till lager som inte är standard. Tidigare sparade inte Adobe Commerce kategorin och det här felet visades: `Something went wrong while saving the category`. <!-- ACP2E-859-->

![Ett problem har korrigerats](../assets/fix.svg) Statusen för konfigurerbar produkt uppdateras nu som förväntat när produkten skapas med alla icke-lagerförda konfigurerbara variationer. <!-- ACP2E-813-->

![Åtgärdat problem](../assets/fix.svg) Verktyget för analys av reservationsinkonsekvens fungerar nu korrekt med delvis levererade order som innehåller konfigurerbara, paketerade och grupperade produkter. Sammansatta produkttyper analyseras nu. Tidigare sparades annulleringar och återbetalningar endast för överordnade produkter, inte för underproduktbeställningsartiklar för konfigurerbara paketprodukter och paketprodukter som kunde levereras tillsammans. <!-- ACP2E-924-->

![Åtgärdat problem](../assets/fix.svg) Ett fel visas inte längre i Adobe Commerce när en administratörsanvändare försöker tilldela 200 eller fler lagerkällor till ett lager eller en produkt. <!-- ACP2E-1180-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce har nu stöd för att skapa en kreditnota för en order från vilken en produkt har tagits bort. Tidigare kunde handlarna inte skapa en kreditnota när produkter hade tagits bort från ordern efter att en faktura hade skapats. Programmet visade följande fel: `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![Åtgärdade problem](../assets/fix.svg) Lager filtreras nu baserat på både ett och flera lagrings-ID. Produktattributkoden `event` har lagts till i listan över reserverade attributkoder. Tidigare utlöstes ett undantag i rapporten LågStock när modulen Lager installerades. <!-- ACP2E-1017-->

![Ett problem har korrigerats](../assets/fix.svg) Navigeringsfilter i lager fungerar nu som väntat, och färdiga produkter läggs nu till i produktlistan för butikskategori. Det nya sorteringsattributet `is_out_of_stock` använder Elasticsearch Dynamic Field Mapper för butiksproduktsamlingen. <!-- ACP2E-748-->

![Åtgärdat problem](../assets/fix.svg) Den sammansatta produktens (bundle, grouped och configurable) Stock-status uppdateras som förväntat när den underordnade produktens Stock-status ändras av ett REST `POST /rest/V1/inventory/source-items` -anrop. <!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 (modulversion: `magento/inventory-metapackage = 1.2.5`) stöds med version 2.4.5 och är kompatibel med version 2.4.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och Magento Open Source kodbas.

![Åtgärdat problem](../assets/fix.svg) Standardlagerstatusen för paket och grupperade produkter uppdateras nu som förväntat när en handlare skapar en leverans från administratören. Tidigare förblev dessa produkters status oförändrad efter det att en leverans skapades. <!--- ACP2E-418-->

![Ett problem har korrigerats](../assets/fix.svg) Konfigurerbara produkter återställs till lager när något av följande villkor uppfylls: 1. Den överordnade produkten har minst en sparad underordnad i lager. 2. Själva den konfigurerbara produkten uppdaterades och angavs som **i lager** och hade minst ett underordnat objekt i lager. <!--- ACP2E-443-->

![Åtgärdat problem](../assets/fix.svg) Lagerändringar som implementerats via REST API visas nu som förväntat på produktinformationssidor. Cacheminnet för katalogprodukter rensas nu när den senaste och nuvarande Stock-statusen har jämförts. Om återanropsfunktionen utelämnades tidigare utfördes en felaktig utvärdering av ändringar i Stock-status, vilket inte utlöste den nödvändiga cacherengöringen. Detta ledde till att lagerstället inte återspeglade lagerändringarna. <!--- ACP2E-161-->

![Åtgärdat problem](../assets/fix.svg) Produkter som har tilldelats standardlager och som tidigare inte fanns i lager visas nu i butiken när källobjektet har uppdaterats med `/V1/inventory/source-items`. Tidigare hade den här REST API-slutpunkten fel `stock_status`. <!--- ACP2E-562-->

![Ett problem har korrigerats](../assets/fix.svg) Det fungerar nu som förväntat när källor innehåller SKU:er som är dubbletter förutom en inledande nolla (till exempel `01234` och `1234`) när lagerkällor frigörs via massåtgärd (**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**). Programmen tog inte bort tilldelningen av inventeringskällor och returnerade ett fel. <!--- ACP2E-2641-->

![Åtgärdat problem](../assets/fix.svg) Produktlagerstatus är nu alltid **i lager** på butiken när oändliga restorder är aktiverade och produkten tilldelas till ett anpassat lager, oavsett restorderns kvantitet. Tidigare gick produkterna ut ur lagret även när restorder aktiverades. <!--- ACP2E-664-->

![Ett problem har korrigerats](../assets/fix.svg) Det konfigurerbara överordnade och underordnade produktpaketet uppdateras nu korrekt när källobjektet har uppdaterats med `POST /V1/inventory/source-items`. När den underordnade produkten har uppdaterats via API:t uppdateras en ny inventerings-plugin för standardlagerkontroller och konfigurerbar produktkvantitet och status uppdateras. <!--- ACP2E-442-->

![Åtgärdat problem](../assets/fix.svg) Ej lagrade grupperade produkter visas inte längre på kategorisidan för butiker. <!--- ACP2E-2082-->

![Korrigerat problem](../assets/fix.svg) Paketnamnet i `CatalogInventory` `composer.json` har korrigerats. <!--- ACP2E-2914-->

![Åtgärdat problem](../assets/fix.svg) Status för restorder representeras nu korrekt i Admin efter att en order med noll kvantitet har lagts i en flerkät-/lagerdistribution. [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![Åtgärdat problem](../assets/fix.svg) Produkterna i ett lagerfritt paket visas inte längre på kategorisidan för butiker när paketprodukten uppdateras från lageravsnittet. <!--- ACP2E-2012-->

![Korrigerat problem](../assets/fix.svg) Kompatibilitetsproblem med PHP 7.4 har åtgärdats. <!--- AC-3192-->

![Ett problem har korrigerats](../assets/fix.svg) Prestandan för sparåtgärder som inkluderar paketprodukter som innehåller många alternativ (flera 100) har förbättrats. Tidigare tog det flera minuter att spara de här stora paketprodukterna och resulterade ibland i timeout i distributioner med Inventory services aktiverat. [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![Ett problem har korrigerats](../assets/fix.svg) Produktmassåtgärdsverktyget (**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**) fungerar nu som väntat när lagerkällan tilldelas till flera produkter när SKU:er är dubblerade, förutom radavståndet `0` (till exempel `01234` och `1234`). Tidigare hade bara en produkt tilldelats en lagerkälla. [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![Åtgärdat problem](../assets/fix.svg) Fältet `ProductInterface.only_x_left_in_stock` returnerar nu 0 om lagret är 0. Tidigare returnerade den null. [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![Korrigerat problem](../assets/fix.svg) Du kan nu redigera standardlager från Admin **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**. Tidigare visades ett JavaScript-fel i konsolen när du försökte lägga till eller ta bort källor från standardlagret, men du kunde tilldela webbplatser till standardlagret. <!--- ACP2E-545-->

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-274--> Antalet produkter i kategorilistan är nu korrekt när du använder läget för en källa för lager med inställningen **[!UICONTROL Display Out-Of-Stock Products]** aktiverad. Ett nytt plugin-program använder nu `AreProductsSalableInterface` och `StockConfigurationInterface` för att fastställa det totala antalet produkter. Tidigare returnerade kategoriproduktlistan fel produktkvantitet.

![Ett problem har korrigerats](../assets/fix.svg) <!--- ACP2E-322--> Konfigurerbara produkter har flyttats till den sista positionen i produktlistan när Stock har uppdaterats när inställningen **[!UICONTROL Move out of stock to the bottom]** är aktiverad. En ny anpassad databasfråga implementeras för att negera sorteringsordningen i Elasticsearch index, vilket ignorerar den sorteringsordning som är aktiverad av Admin. Tidigare flyttades inte konfigurerbara produkter och deras underordnade produkter längst ned i listan när den här inställningen var aktiverad.

## v1.2.4

Inventory management 1.2.4 (modulversion: `magento/inventory-metapackage = 1.2.4`) stöds med version 2.4.4 och är kompatibelt med version 2.4.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och Magento Open Source kodbas.

![Korrigerat problem](../assets/fix.svg) Commerce visar nu ett korrekt värde för försäljningsbar kvantitet för alla produkter i produktlistvyn för Admin. Tidigare visades ett tomt värde för säljbar kvantitet lagerförda produkter med SKU:er som innehöll specialtecken. <!--- MC-41936-->

![Korrigerat problem](../assets/fix.svg) Prestandan har förbättrats för kundvagn och utcheckning, t.ex. när produkter läggs till i varukorgen i distributioner med många (ungefär 10 000) lagerkällor. <!--- MC-42570-->

![Korrigerat problem](../assets/fix.svg) [!BADGE PaaS endast]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."} Kommandot `bin/magento inventory:reservation:list-inconsistencies` hanterar nu order med partiella leveranser korrekt, även om reservationerna missas från databasen och cachen har rensats. Tidigare visades följande fel när det här kommandot kördes med en förrensad cache: `Area code is not set`. <!--- MC-42142-->


![Korrigerat problem](../assets/fix.svg) Inkrementell indexering av underordnade produkter i grupperade produkter medför inte längre att andra grupperade produkter indexeras felaktigt när underordnade produkter delas. <!--- MC-41963-->

![Korrigerat problem](../assets/fix.svg) På sidan för butikskategori visas nu rätt produktantal efter att en produkt tagits bort från en kategori via API. Tidigare var antalet produkter på kategorisidan felaktigt tills en omindexering gjordes. <!--- MC-42287-->

![Ett problem har korrigerats](../assets/fix.svg) Konfigurerbara produkter kan nu returneras till Stock när en kreditnota skapas när alternativet **[!UICONTROL Manage Stock]** är inaktiverat. Tidigare visades inte kryssrutan **Återgå till lager** på sidan där kreditnotan skapades när det här alternativet inaktiverades. <!--- MC-42002-->

![Ett problem har korrigerats](../assets/fix.svg). Hanteringen av lager som överskrider 10 000 artiklar har förbättrats. Tidigare hindrade prestationsproblem ibland handlarna från att redigera material i administratören innan de lanserade sin webbplats. <!--- MC-42643-->

![Ett problem har korrigerats](../assets/fix.svg) Sidan **[!UICONTROL User Roles]** i Admin har uppdaterats för att ge administratörer begränsad behörighet till konfigurationen av leveransmetoder. Avsnittet _Leveransmetoder_ har bytt namn till _[!UICONTROL Delivery methods]_och_[!UICONTROL In-Store Pickup]_ flyttas under avsnittet _[!UICONTROL Delivery methods]_. [GitHub-30053](https://github.com/magento/magento2/issues/30053) <!--- MC-41545-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce skapar inte längre en dubblettproduktreservation efter att en kreditnota har uppdaterats av API. <!--- MC-41757-->

![Korrigerat problem](../assets/fix.svg) Om du växlar från fliken _[!UICONTROL Pick up in Store]_till fliken_[!UICONTROL Shipping]_ i arbetsflödet för utcheckning utlöses inte längre ett JavaScript-fel när endast hämtningsleverans i butiken är tillgänglig. <!--- MC-42808-->

![Korrigerat problem](../assets/fix.svg) Försäljningsbar produktkvantitet och produktkvantitet i lager synkroniseras nu korrekt. Tidigare återskapades inte kompensation för lagerreservation för annullerade order. <!--- MC-42485-->

![Ett problem har korrigerats](../assets/fix.svg) Validerarens prestanda har optimerats för att förhindra att en ny källa läggs till i en paketerad produkts underordnade produkt med leveranstypen `Ship Together`. <!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 (modulversion: `magento/inventory-metapackage = 1.2.3`) stöds med version 2.4.3 och är kompatibel med version 2.4.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och Magento Open Source kodbas.

![Korrigerat problem](../assets/fix.svg) Korrigerade flera problem relaterade till synligheten för den sammansatta produkten på klientsidan.

![Korrigerat problem](../assets/fix.svg) Förbättrade prestanda för hantering av kundvagnssidor med minsta antal som krävs.

![Korrigerat problem](../assets/fix.svg) Flera korrigeringar har gjorts för att lösa problem med att skapa källan, lösa problem med att skapa lager, hämta lager, sortera allokerade källor, leverera i butik och lagerkommandon.

![Korrigerat problem](../assets/fix.svg) [!DNL Commerce] har nu stöd för tresiffriga kanadensiska postnummer för leverans i butik. Sex-siffriga koder stöds inte på grund av begränsningar som angetts av `geonames.org`.

![Korrigerat problem](../assets/fix.svg) Administratören visar nu korrekt kvantitet av standardlager för inaktiverade produkter i stödrastret **Produkter** och sidan **Redigera produkt** för distributioner i flera butiker.

![Åtgärdat problem](../assets/fix.svg) [!DNL Commerce] uppdaterar nu kategoriproduktcachen när en paketprodukt kommer tillbaka i lager.

## 1.2.2

[!DNL Inventory Management] 1.2.2 (modulversion: `magento/inventory-metapackage = 1.2.2`) stöds med version 2.4.2 och är kompatibel med version 2.4.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och Magento Open Source kodbas.

![Korrigerat problem](../assets/fix.svg) Korrigerade flera problem relaterade till synligheten för den sammansatta produkten på klientsidan.

![Korrigerat problem](../assets/fix.svg) Förbättrade prestanda för kundvagnssidor under kvantitetsuppdatering på B2B.

![Korrigerat problem](../assets/fix.svg) Flera korrigeringar har gjorts för att lösa problem med hämtning i butik, massuppdateringar och lagertröskelvärde.

![Nya](../assets/new.svg) **funktionstester.** introducerade nya funktionstester och tillhandahöll korrigeringar för befintliga tester för att göra dem mer stabila.

## 1.2.1

[!DNL Inventory Management] 1.2.1 (modulversion: `magento/inventory-metapackage = 1.2.1`) stöds med version 2.4.1 och är kompatibel med version 2.4.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och Magento Open Source kodbas.

![Korrigerat problem](../assets/fix.svg) Ett känt problem som rör seriejobbet `inventory_cleanup_reservations` har korrigerats och ett problem som rör funktionen för hämtning i butiken för paketprodukter har åtgärdats. Uppdateringen innehåller även allmänna förbättringar av lagerberäkning, produktsupport och backorder-funktioner.

![Nya](../assets/new.svg) **funktionstester.** introducerade nya funktionstester som ger ytterligare täckning för funktionen för hämtning i butiken.

## 1.2.0

[!DNL Inventory Management] 1.2.0 (modulversion: `magento/inventory-metapackage = 1.2.0`) stöds med version 2.4.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och Magento Open Source kodbas.

![Ett problem har korrigerats](../assets/fix.svg) Ett flertal åtgärder för att lösa problem med källtilldelning, stöd för skalbara miljöfunktioner och kompatibilitet med PHP 7.4, MySQL 8 och PHPUNIT 9 har åtgärdats.

![Ny](../assets/new.svg) **Leveransmetod i butik.** lade till ett alternativ för användare att välja en källa som ska användas som hämtningsplats vid utcheckning. Se [Butiksleverans](../stores-purchase/shipping-in-store-delivery.md) i _Handboken för försäljning och köp_.

![Nytt](../assets/new.svg) **Paket med produktstöd för flerkälläge.** Inventering stöder alla produkttyper med flera källor.

![Nytt](../assets/new.svg) **Asynkron omindexering av lager.** lade till möjligheten att indexera om lager asynkront och förbättrade prestanda för flera kritiska scenarier.

![Nytt](../assets/new.svg) **Massgränssnitt.** Introducerade nya bulkgränssnitt för skalbarhet: `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`, `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![Nytt](../assets/new.svg) **Ökad testtäckning.** Nya funktioner täcks av automatiserade tester, inklusive utökad täckning för identifierade och åtgärdade problem.

![Känt fel](../assets/bug.svg) **Känt fel.** Frånvaron av fältet `object_id` i bokningsmetadata förhindrar att seriejobbet för `inventory_cleanup_reservations` fungerar korrekt. Den här utgåvan introducerades i [magento/invecklat#3046](https://github.com/magento/inventory/pull/3046).

**Tillfällig lösning:** Utför följande MySQL-frågor för att manuellt rensa reservationer:

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

[!DNL Inventory Management] 1.1.6 (modulversion: `inventory-composer-metapackage = 1.1.6`) stöds med version 2.3.6 och är kompatibel med version 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1 och 2.3.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och Magento Open Source kodbas.

![Korrigerat problem](../assets/fix.svg) Åtgärdat problem som rör restorder, kreditnotor, rutnät för låg stockrapport, korrigeringar kopplade till CLI-verktyget för att lösa inkonsekvenser och allmänna förbättringar.

![Nytt](../assets/new.svg) **Asynkron omindexering av lager.** lade till möjligheten att indexera om lager asynkront och förbättrade prestanda för flera kritiska scenarier.

## 1.1.5

[!DNL Inventory Management] 1.1.5 (modulversion: `inventory-composer-metapackage = 1.1.5`) stöds med version 2.3.5 och är kompatibelt med version 2.3.4, 2.3.3, 2.3.2, 2.3.1 och 2.3.0 av Adobe Commerce, Adobe Commerce i molninfrastruktur samt Magento Open Source kodbas.

![Nytt](../assets/new.svg) **Uppdatera lagret när produkt-SKU ändras.** Introducerade en ny konfigurationsinställning för att växla till det nya beteendet: Synkronisera med katalog.

![Nya](../assets/new.svg) **funktionstester.** introducerade nya funktionstester för att eliminera luckan i testningen. Korrigerade flera problem som gjorde testerna mer stabila och tillförlitliga).

![Känt fel](../assets/bug.svg) Korrigeringar för att förhindra överförsäljning av produkter, synlighet för produkter utanför lagret, flera korrigeringar för skalbar miljö och förbättringar av användargränssnittet.

## 1.1.4

[!DNL Inventory Management] 1.1.4 (modulversion: `inventory-composer-metapackage = 1.1.4`) stöds med version 2.3.4 och är kompatibel med version 2.3.3, 2.3.2, 2.3.1 och 2.3.0 av Adobe Commerce, Adobe Commerce i molninfrastruktur samt Magento Open Source kodbas.

![Korrigerat problem ](../assets/fix.svg)**Förbättrade prestanda.** Introducerade buntlogik för CLI-kommandot för lagerreservationer för att minska minnesanvändningen och undvika fall när processen fastnar utan något svar.

![Nytt ](../assets/new.svg)**Ökad testtäckning.** introducerade många nya funktionstester. Nästan alla manuella inventeringsscenarier täcks av automatiserade tester.

![Känt fel](../assets/bug.svg) Flera korrigeringar har gjorts för att lösa problem med kreditnotor, grupperade produkter samt käll- och aktiemassåtgärder.

## 1.1.3

[!DNL Inventory Management] 1.1.3 (modulversion: `inventory-composer-metapackage = 1.1.3`) stöds med version 2.3.3 och är kompatibel med version 2.3.2, 2.3.1 och 2.3.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och Magento Open Source kodbas.

![Korrigerat problem ](../assets/fix.svg)**Bättre integrering med Adobe Commerce- och B2B-funktioner.** [!DNL Inventory Management] fungerar nu korrekt med följande funktioner för webbplatser som använder lagerkällor och lager som inte är standard:

- Beställ på SKU (Adobe Commerce)
- Snabbordning (B2B)
- Rekvisitionslistor (B2B)

![Nytt ](../assets/new.svg)**Förbättrade prestanda.** Katalogbläddringsprestanda för Storefront har förbättrats för webbplatser som kör standardlagret och standardkällan för lager.

![Nytt ](../assets/new.svg)**Ökad testtäckning.** Det automatiska funktions- och integreringstestets täckning har ökat avsevärt.

## 1.1.2

[!DNL Inventory Management] 1.1.2 (modulversion: `inventory-composer-metapackage = 1.1.2`) stöds med version 2.3.2 och är kompatibel med version 2.3.1 och 2.3.0 av Adobe Commerce, Adobe Commerce i molninfrastruktur samt Magento Open Source kodbas.

![Korrigerat problem](../assets/fix.svg) lades till `source_code` i svaret för GET `/V1/shipments` REST-slutpunkten. <!-- https://github.com/magento/inventory/pull/2142 -->

![Korrigerat problem](../assets/fix.svg) Korrigerat problem med att rensa reservationer och uppdatera produktkvantiteter efter att ha utfärdat en kreditnota för en ej levererad order. När du väljer alternativet för <!-- https://github.com/magento/inventory/pull/2179 -->

![Korrigerat problem](../assets/fix.svg) Korrigerat problem med att spara kvantitet för konfigurerbara underordnade produkter när kvantiteter anges när produkten skapas. <!-- https://github.com/magento/inventory/pull/2158 -->

Nya moduler för [!DNL Inventory Management] 1.1.2 Beta omfattar:

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![Nytt](../assets/new.svg) **Lagt till en slutpunkt för gruppöverföring** - Aktuell slutpunkt för gruppöverföring flyttar alla tilldelade kvantiteter från en ursprungskälla till en målkälla. Den nya slutpunkten `/rest/V1/inventory/bulk-partial-source-transfer` tillåter handlare att överföra partiellt lager från källan till källan som en gruppåtgärd. Om du vill överföra en viss kvantitet anger du en begäran till slutpunkten med `sku`, `qty`, `origin_source_code` och `destination_source_code`. Överföringar verifierar att källan har tilldelats `sku`, att det finns tillräckligt med kvantitet att överföra och så vidare. Se [Inventeringsmassåtgärder](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} i REST API-dokumentationen. <!-- https://github.com/magento/inventory/pull/2117 -->

![Nytt](../assets/new.svg) **Tillagt reserverings-CLI** - Nya kommandon ger dig alternativ för att upptäcka och lösa reservationsinkonsekvenser. När order skickas och ändrar status genererar [!DNL Inventory Management] initiala reservationer och uppdateringar via kompensationsreservationer. Dessa kommandon returnerar en lista över upptäckta inkonsekvenser per order-ID, SKU och Stock-ID och skapar reservationer att lösa. Mer information finns i [CLI-referensen](cli.md). <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![Nytt](../assets/new.svg) **Prestandaförbättringar för källor och SSA-alternativ** - Sortering och val av källor vid leverans orsakade prestandaförsämringar för lager med ett stort antal källor. Den här versionen innehåller viktiga prestandaförbättringar för att lista och sortera tillgängliga källor när du granskar och väljer SSA-alternativ i leveranser. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![Nytt](../assets/new.svg) **GraphQL-stöd för Inventory management har lagts till** - Den här versionen installerar en ny `magento/module-inventory-graph-ql`-modul. GraphQL [ProductInterface-attributen](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} innehåller nu attributen `only_x_left_in_stock` och `stock_status` för [!DNL Inventory Management] som stöds. <!-- https://github.com/magento/inventory/pull/2124 -->

![Nytt](../assets/new.svg) **Förenklat gränssnitt för tilldelade källor** - Tabellen Tilldelade källor på produktsidor har förenklat innehåll för enklare uppdateringar och högre prestanda när många källor visas. Alla källor visas efter källnamn (hovra över för `source_code`).

![Ny](../assets/new.svg) **Exportera aggregerad lagertjänst** - Den här versionen innehåller en ny exportaggregerad lagertjänst (med reservationer i systemet) som stöder externa försäljningskanaler, som Amazon, eBay och Google Shopping-annonser.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0 (modulversion: `inventory-composer-metapackage = 1.1.0`) stöds och är kompatibelt med version 2.3.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och Magento Open Source kodbas. [!DNL Inventory Management] 1.1.1 släpps endast som en paketnamnsuppdatering som stöds för version 2.3.1 och är kompatibel med version 2.3.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och Magento Open Source kodbas.

![Ett problem har korrigerats](../assets/fix.svg) **Stöd för Elasticsearch för single- och multi-source-lägen har lagts till** - du kan nu konfigurera och använda Elasticsearch med anpassade lager. Se [Konfigurera Elasticsearch-tjänsten](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html){target="_blank"} för installationsinformation. <!-- PR https://github.com/magento/inventory/pull/1943 -->

![Korrigerat problem](../assets/fix.svg) Åtgärdade prestandaproblem med standardlagret för att drastiskt öka prestanda med flera åtgärder. Förbättringar ökar prestandan för single-source-läge, Överför lager till Source, Storefront Category-sidor och beräkningar för försäljningsantal.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![Korrigerat problem](../assets/fix.svg) Löste problem med utlagringsstatus och bulklageröverföring till Stock för konfigurerbara och grupperade produkter. Produktstatusen påverkas inte om du väljer de överordnade produkterna och utför massåtgärder. Om den överordnade produkten var i Stock finns den kvar i Stock.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![Ny](../assets/new.svg) **Algoritm för avståndsprioritet** - Algoritmen för avståndsprioritet är en ny färdig Source-algoritm för avståndsbaserade leveransrekommendationer. Den här algoritmen jämför platsen för leveransdestinationsadressen med källplatserna för att avgöra vilken källa som är närmast för att leverera försändelser. Avståndet kan avgöras av antingen fysiskt avstånd eller den tid som tillbringas med att resa från en plats till en annan, med hjälp av importerade geokodsdata eller Google-anvisningar (körning, gång eller cykling).

![Ny](../assets/new.svg) **Lista över utökad källkvantitet** - Det är enkelt att hovra och visa alla källor per produkt via produktstödrastret för handlare med ett stort antal källor. Varje produkt har minst fem källor och motsvarande kvantiteter. När du hovrar över källorna kan du bläddra igenom hela listan med källor och aktuella kvantiteter.

![Känt fel](../assets/bug.svg) Problem med Magento Open Source och Adobe Commerce v2.3.1 - Asynkron migrering av data mellan källor påträffar problem på grund av ändringar i asynkrona API:er med ämnesnamn som återspeglar PHP-klass- och metodnamn. Du bör använda synkrona åtgärder genom att ange **[!UICONTROL Run asynchronously]** till `No`.
