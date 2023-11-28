---
title: '''[!DNL Inventory Management] versionsinformation'
description: Läs versionsinformationen om du vill ha information om alla [!DNL Inventory Management] releaser.
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '3361'
ht-degree: 0%

---

# [!DNL Inventory Management] versionsinformation

Versionsinformationen beskriver releaser av [!DNL Inventory Management] och innehåller:

![Nytt](../assets/new.svg) Nya funktioner
![Korrigerat problem](../assets/fix.svg) Korrigeringar och förbättringar
![Känt fel](../assets/bug.svg) Kända fel

[!DNL Inventory Management] är ett specialprojekt för Magento Open Source Community Engineering som är öppet för medverkande. Se [GitHub-projekt](https://github.com/magento/inventory) databas och [wiki](https://github.com/magento/inventory/wiki) för att komma igång. Om du vill diskutera projektet går du med i [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) kanal ([självregistrering](https://opensource.magento.com/slack)).

[Frigör schema](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html){target="_blank"} för kompatibla versioner.

## v1.2.6

[!DNL Inventory Management] 1.2.6 (modulversion: `magento/inventory-metapackage = 1.2.6`) stöds i version 2.4.6 och är kompatibelt med version 2.4.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och kodbasen Magento Open Source.

![Korrigerat problem](../assets/fix.svg) I butiken visas nu sammansatta produkter (konfigurerbara, paketerade och grupperade) som i lager när underordnade produkter som har sålts returneras till lagret. Tidigare angav storefront att den sammansatta produkten inte fanns i lager under dessa förhållanden. <!-- ACP2E-1106-->

![Korrigerat problem](../assets/fix.svg) Konfigurerbara produktalternativ visas nu som förväntat utanför lagret om alternativet skapades med kvantitet satt till 0 och **[!UICONTROL Display out-of-stock products]** är aktiverat. <!-- ACP2E-1148-->

![Korrigerat problem](../assets/fix.svg) Cacheminnen för kategorisidor ogiltigförklaras inte längre när lagerkvantiteten ändras och produkten fortfarande finns i lager. Adobe Commerce läser nu in sidor från cacheminnet i stället för att återskapa dem när produktkvantiteten (och inget annat) på kategoritappen för butiker ändras. <!-- ACP2E-118-->

![Korrigerat problem](../assets/fix.svg) Antalet produkter i kategorilistan är nu korrekt när du använder Inventory i läget med en källa med **[!UICONTROL Display Out-Of-Stock Products]** inställning aktiverad. Adobe Commerce kontrollerar nu om en produkt går att sälja vid inventering. <!-- ACP2E-1033-->

![Korrigerat problem](../assets/fix.svg) Kundprisreglerna för butiksleverans fungerar nu som väntat när Lager är aktiverat. Tidigare tillämpades inte rabatter som genererats av kundvagnsregler under dessa villkor. <!-- ACP2E-1015-->

![Korrigerat problem](../assets/fix.svg) När produktinventeringen uppdateras i schemalagt läge rensas inte längre alla cacheminnen. Tidigare rensade lagerindexeraren alla konfigurationscache. <!-- ACP2E-1003-->

![Korrigerat problem](../assets/fix.svg) Värdet för **[!UICONTROL Allow Multiple Boxes for Shipping]** attribut för en produkt i Avancerat lager sparas nu som förväntat. <!-- ACP2E-992-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce ger nu rätt reservationskompensation efter en partiell återbetalning av en order som lagts med en butiksupphämtning. Tidigare har en felaktig reservation sparats i `inventory_reservation` register när en administratörsanvändare har skapat en kreditnota utan att välja **[!UICONTROL Return to Stock]** kryssrutan. <!-- ACP2E-979-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce visar inte längre konfigurerbara produkter som lagrade utanför lagret när en av dess varianter manuellt har återförts till lager vid distributioner som implementerar lager med flera källor. <!-- ACP2E-952-->

![Korrigerat problem](../assets/fix.svg) Kolumnposition i produktrutnätet (**[!UICONTROL Catalog]** > **[!UICONTROL Products]**) återgår inte längre till sin tidigare position efter att sidan har lästs in på nytt i distributioner med flera konfigurerade lagerkällor. <!-- ACP2E-925-->

![Korrigerat problem](../assets/fix.svg) Lagerkvantiteten är nu korrekt efter att en kreditnota har utfärdats för en virtuell produkt när **[!UICONTROL Back to stock]** är inte markerad. <!-- ACP2E-908-->

![Korrigerat problem](../assets/fix.svg) Nu kan du spara kategorier med automatisk produktsortering och omfång som är tilldelat till lager som inte är standard. Tidigare sparade inte Adobe Commerce kategorin och det här felet visades: `Something went wrong while saving the category`. <!-- ACP2E-859-->

![Korrigerat problem](../assets/fix.svg) Konfigurerbar produktlagerstatus uppdateras nu som förväntat när produkten skapas med alla lagerfria variationer. <!-- ACP2E-813-->

![Korrigerat problem](../assets/fix.svg) Verktyget för analys av reservationsinkonsekvens fungerar nu korrekt med delvis levererade order som innehåller konfigurerbara, paketerade och grupperade produkter. Sammansatta produkttyper analyseras nu. Tidigare sparades annulleringar och återbetalningar endast för överordnade produkter, inte för underproduktbeställningsartiklar för konfigurerbara paketprodukter och paketprodukter som kunde levereras tillsammans. <!-- ACP2E-924-->

![Korrigerat problem](../assets/fix.svg) Ett fel visas inte längre i Adobe Commerce när en administratör försöker tilldela 200 eller fler lagerkällor till ett lager eller en produkt. <!-- ACP2E-1180-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce har nu stöd för att skapa en kreditnota för en order från vilken en produkt har tagits bort. Tidigare kunde handlarna inte skapa en kreditnota när produkter hade tagits bort från ordern efter att en faktura hade skapats. Programmet visade följande fel: `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![Korrigerat problem](../assets/fix.svg) Lager filtreras nu baserat på både ett och flera lagrings-ID. The `event` produktattributkoden har lagts till i listan över reserverade attributkoder. Tidigare utlöstes ett undantag i rapporten LågStock när modulen Lager installerades. <!-- ACP2E-1017-->

![Korrigerat problem](../assets/fix.svg) Navigeringsfilter i flera lager fungerar nu som förväntat, och färdiga produkter läggs nu till i produktlistan för kategorin store. Den nya `is_out_of_stock` sorteringsattributet använder den dynamiska fältmapparen Elasticsearch för butikens produktsamling. <!-- ACP2E-748-->

![Korrigerat problem](../assets/fix.svg) Ställningsstatus för sammansatt produkt (paket, grupperad och konfigurerbar) uppdateras som förväntat när statusen för underordnad produkt ändras av en REST `POST /rest/V1/inventory/source-items` ring. <!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 (modulversion: `magento/inventory-metapackage = 1.2.5`) stöds i version 2.4.5 och är kompatibelt med version 2.4.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och kodbasen Magento Open Source.

![Korrigerat problem](../assets/fix.svg) Standardlagerstatus för paket och grupperade produkter uppdateras nu som förväntat när en handlare skapar en leverans från administratören. Tidigare förblev dessa produkters status oförändrad efter det att en leverans skapades. <!--- ACP2E-418-->

![Korrigerat problem](../assets/fix.svg) Konfigurerbara produkter returneras nu till lagret när något av följande villkor uppfylls: 1. Den överordnade produkten har minst en sparad underordnad i lager. 2. Själva den konfigurerbara produkten har uppdaterats och ställts in som **i lager** och har minst ett barn i lager. <!--- ACP2E-443-->

![Korrigerat problem](../assets/fix.svg) Lagerändringar som implementerats via REST API visas nu som förväntat på produktinformationssidor. Cacheminnet för katalogprodukter rensas nu när den senaste och nuvarande Stock-statusen har jämförts. Om återanropsfunktionen utelämnades tidigare utfördes en felaktig utvärdering av ändringar i Stock-status, vilket inte utlöste den nödvändiga cacherengöringen. Detta ledde till att lagerstället inte återspeglade lagerändringarna. <!--- ACP2E-161-->

![Korrigerat problem](../assets/fix.svg) Produkter som har tilldelats standardlager och som tidigare inte fanns i lager visas nu i butiken när källartikeln har uppdaterats med `/V1/inventory/source-items`. Tidigare hade den här REST API-slutpunkten fel `stock_status`. <!--- ACP2E-562-->

![Korrigerat problem](../assets/fix.svg) Ta bort tilldelning av lagerkällor via massåtgärd (**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**) fungerar nu som väntat när källor innehåller SKU:er som är dubbletter förutom en inledande nolla (till exempel `01234` och `1234`). Programmen tog inte bort tilldelningen av inventeringskällor och returnerade ett fel. <!--- ACP2E-2641-->

![Korrigerat problem](../assets/fix.svg) Produktens lagerstatus är nu alltid **i lager** i butiken när oändliga restorder är aktiverade och produkten tilldelas till ett anpassat lager, oavsett hur många restorder som lagts. Tidigare gick produkterna ut ur lagret även när restorder aktiverades. <!--- ACP2E-664-->

![Korrigerat problem](../assets/fix.svg) Det konfigurerbara överordnade och underordnade produktpaketet uppdateras nu korrekt när källobjektet har uppdaterats med `POST /V1/inventory/source-items`. När den underordnade produkten har uppdaterats via API:t uppdateras en ny inventerings-plugin för standardlagerkontroller och konfigurerbar produktkvantitet och status uppdateras. <!--- ACP2E-442-->

![Korrigerat problem](../assets/fix.svg) Grupperade produkter som inte finns i lager visas inte längre på kategorisidan för butiker. <!--- ACP2E-2082-->

![Korrigerat problem](../assets/fix.svg) Paketnamnet i har korrigerats `CatalogInventory` `composer.json`. <!--- ACP2E-2914-->

![Korrigerat problem](../assets/fix.svg) Status för restorder visas nu korrekt i Admin efter att en order med noll-kvantitet har lagts i en multikällprodukt-/lagerdistribution. [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![Korrigerat problem](../assets/fix.svg) Produkterna i paketet visas inte längre i butikskategorisidan när paketprodukten uppdateras från lageravsnittet. <!--- ACP2E-2012-->

![Korrigerat problem](../assets/fix.svg) Kompatibilitetsproblem med PHP 7.4 har åtgärdats. <!--- AC-3192-->

![Korrigerat problem](../assets/fix.svg) Prestanda för sparåtgärder som omfattar paketprodukter som innehåller många alternativ (flera 100) har förbättrats. Tidigare tog det flera minuter att spara de här stora paketprodukterna och resulterade ibland i timeout i distributioner med Inventory services aktiverat. [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![Korrigerat problem](../assets/fix.svg) Verktyget för gruppåtgärd (**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**) fungerar nu som förväntat när du tilldelar en lagerkälla till flera produkter när SKU:er är dubblerade, förutom en radavståndskälla `0` (till exempel `01234` och `1234`). Tidigare hade bara en produkt tilldelats en lagerkälla. [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![Korrigerat problem](../assets/fix.svg) The `ProductInterface.only_x_left_in_stock` fältet returnerar nu 0 om lagret är 0. Tidigare returnerade den null. [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![Korrigerat problem](../assets/fix.svg) Du kan nu redigera standardlager från administratören **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**. Tidigare visades ett JavaScript-fel i konsolen när du försökte lägga till eller ta bort källor från standardlagret, men du kunde tilldela webbplatser till standardlagret. <!--- ACP2E-545-->

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-274--> Antalet produkter i kategorilistan är nu korrekt när du använder läget för en enda källa för lagret med **[!UICONTROL Display Out-Of-Stock Products]** inställning aktiverad. Ett nytt plugin-program använder nu `AreProductsSalableInterface` och `StockConfigurationInterface` för att fastställa det totala antalet produkter. Tidigare returnerade kategoriproduktlistan fel produktkvantitet.

![Korrigerat problem](../assets/fix.svg) <!--- ACP2E-322--> Konfigurerbara produkter flyttas nu till den sista positionen i produktlistan efter att Stock har uppdaterats när **[!UICONTROL Move out of stock to the bottom]** inställningen är aktiverad. En ny anpassad databasfråga implementeras för att negera sorteringsordningen i Elasticsearch-index, vilket inte tar hänsyn till den administratörsaktiverade sorteringsordningen. Tidigare flyttades inte konfigurerbara produkter och deras underordnade produkter längst ned i listan när den här inställningen var aktiverad.

## v1.2.4

Inventory management 1.2.4 (modulversion: `magento/inventory-metapackage = 1.2.4`) stöds i version 2.4.4 och är kompatibelt med version 2.4.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och kodbasen Magento Open Source.

![Korrigerat problem](../assets/fix.svg) I Commerce visas nu ett korrekt värde för säljbar kvantitet för alla produkter i produktlistvyn för Admin. Tidigare visades ett tomt värde för säljbar kvantitet lagerförda produkter med SKU:er som innehöll specialtecken. <!--- MC-41936-->

![Korrigerat problem](../assets/fix.svg) Prestandan har förbättrats för kundvagn och utcheckning som att lägga till produkter i varukorgen i installationer med många (ungefär 10 000) inventeringskällor. <!--- MC-42570-->

![Korrigerat problem](../assets/fix.svg) The `bin/magento inventory:reservation:list-inconsistencies` kommandot hanterar nu order med partiella leveranser korrekt, även om reservationerna missas från databasen och cachen har rensats. När det här kommandot kördes med en förrensad cache visades följande fel i Commerce: `Area code is not set`. <!--- MC-42142-->

![Korrigerat problem](../assets/fix.svg) Inkrementell indexering av grupperade underordnade produkter medför inte längre att andra grupperade produkter indexeras felaktigt när underordnade produkter delas. <!--- MC-41963-->

![Korrigerat problem](../assets/fix.svg) På sidan för butikskategori visas nu rätt produktantal när en produkt har tagits bort från en kategori via API. Tidigare var antalet produkter på kategorisidan felaktigt tills en omindexering gjordes. <!--- MC-42287-->

![Korrigerat problem](../assets/fix.svg) Konfigurerbara produkter kan nu returneras till lager när en kreditnota skapas när **[!UICONTROL Manage Stock]** alternativet är inaktiverat. I Commerce visades tidigare inte **Återgå till lager** kryssrutan på sidan där kreditnotan skapades när det här alternativet inaktiverades. <!--- MC-42002-->

![Korrigerat problem](../assets/fix.svg) Hanteringen av lager som överstiger 10 000 artiklar har förbättrats. Tidigare hindrade prestationsproblem ibland handlarna från att redigera material i administratören innan de lanserade sin webbplats. <!--- MC-42643-->

![Korrigerat problem](../assets/fix.svg) The **[!UICONTROL User Roles]** sidan i Admin har uppdaterats för att ge administratörer begränsad behörighet till konfigurationen av leveransmetoder. The _Leveransmetoder_ har bytt namn till _[!UICONTROL Delivery methods]_och_[!UICONTROL In-Store Pickup]_ flyttas under _[!UICONTROL Delivery methods]_-avsnitt. [GitHub-30053](https://github.com/magento/magento2/issues/30053)  <!--- MC-41545-->

![Korrigerat problem](../assets/fix.svg) Adobe Commerce skapar inte längre en dubblettproduktreservation efter att en kreditnota har uppdaterats av API. <!--- MC-41757-->

![Korrigerat problem](../assets/fix.svg) Byt från _[!UICONTROL Pick up in Store]_till_[!UICONTROL Shipping]_ -fliken i arbetsflödet för utcheckning utlöser inte längre ett JavaScript-fel när endast hämtningsleverans i butiken är tillgänglig. <!--- MC-42808-->

![Korrigerat problem](../assets/fix.svg) Försäljningsbar produktkvantitet och produktkvantitet i lager synkroniseras nu korrekt. Tidigare återskapades inte kompensation för lagerreservation för annullerade order. <!--- MC-42485-->

![Korrigerat problem](../assets/fix.svg) Validerarens prestanda är optimerad för att förhindra att nya källor läggs till i en paketerad produkts underordnade produkt med leveranstyp `Ship Together`. <!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 (modulversion: `magento/inventory-metapackage = 1.2.3`) stöds i version 2.4.3 och är kompatibelt med version 2.4.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och kodbasen Magento Open Source.

![Korrigerat problem](../assets/fix.svg) Korrigerade flera problem relaterade till synligheten för den sammansatta produkten på frontend.

![Korrigerat problem](../assets/fix.svg) Förbättrad hantering av kundvagnssidor med minsta antal som krävs.

![Korrigerat problem](../assets/fix.svg) Flera korrigeringar är avsedda för att lösa problem med att skapa källan, artiklar som inte finns i lager, anskaffning av lager, sortering av allokerade källor, leverans i butik och lagerkommandon.

![Korrigerat problem](../assets/fix.svg) [!DNL Commerce] har nu stöd för tresiffriga kanadensiska postnummer för leverans i butik. Sexsiffriga koder stöds inte på grund av begränsningar som anges av `geonames.org`.

![Korrigerat problem](../assets/fix.svg) Administratören visar nu korrekt kvantitet för inaktiverade produkter på **Produkter** rutnät och **Redigera produkt** sida för distributioner i flera butiker.

![Korrigerat problem](../assets/fix.svg) [!DNL Commerce] uppdaterar nu kategoriproduktcachen när en paketprodukt kommer tillbaka i lager.

## 1.2.2

[!DNL Inventory Management] 1.2.2 (modulversion: `magento/inventory-metapackage = 1.2.2`) stöds i version 2.4.2 och är kompatibelt med version 2.4.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och kodbasen Magento Open Source.

![Korrigerat problem](../assets/fix.svg) Korrigerade flera problem relaterade till synligheten för den sammansatta produkten på frontend.

![Korrigerat problem](../assets/fix.svg) Förbättrade kundvagnssidans prestanda under kvantitetsuppdatering på B2B.

![Korrigerat problem](../assets/fix.svg) Flera korrigeringar är avsedda att lösa problem med hämtning i butik, massuppdateringar och lagertröskelvärden.

![Nytt](../assets/new.svg) **Funktionstester.** Nya funktionstester och korrigeringar för befintliga tester har införts för att göra dem mer stabila.

## 1.2.1

[!DNL Inventory Management] 1.2.1 (modulversion: `magento/inventory-metapackage = 1.2.1`) stöds i version 2.4.1 och är kompatibelt med version 2.4.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och kodbasen Magento Open Source.

![Korrigerat problem](../assets/fix.svg) Ett känt problem som rör `inventory_cleanup_reservations` cron job och åtgärdade ett problem med funktionen för hämtning i butik för paketprodukter. Uppdateringen innehåller även allmänna förbättringar av lagerberäkning, produktsupport och backorder-funktioner.

![Nytt](../assets/new.svg) **Funktionstester.** Nya funktionstester introducerades som ger ytterligare täckning för funktionen för hämtning i butiken.

## 1.2.0

[!DNL Inventory Management] 1.2.0 (modulversion: `magento/inventory-metapackage = 1.2.0`) stöds i version 2.4.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och kodbasen Magento Open Source.

![Korrigerat problem](../assets/fix.svg) Flera korrigeringar som åtgärdar problem med källtilldelning, stöd för skalbara miljöfunktioner och kompatibilitet med PHP 7.4, MySQL 8 och PHPUNIT 9.

![Nytt](../assets/new.svg) **Leveranssätt i butik.** Ett alternativ för användare att välja en källa som ska användas som hämtningsplats vid utcheckning har lagts till. Se [Butiksleverans](../stores-purchase/shipping-in-store-delivery.md) i _Experience Guide för försäljning och inköp_.

![Nytt](../assets/new.svg) **Paket med produktstöd för flerkälläge.** Inventeringen stöder alla produkttyper med flera källor.

![Nytt](../assets/new.svg) **Asynkron omindexering av lager.** Lagringsmöjligheten att indexera om lager asynkront och prestandan för flera kritiska scenarier har förbättrats.

![Nytt](../assets/new.svg) **Massgränssnitt.** Nya gränssnitt för massvis för skalbarhetskontroll: `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`, `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![Nytt](../assets/new.svg) **Ökad testtäckning.** Ny funktionalitet täcks av automatiserade tester, inklusive utökad täckning för identifierade och åtgärdade problem.

![Känt fel](../assets/bug.svg) **Känt fel.** Frånvaro av `object_id` fältet i bokningsmetadata förhindrar `inventory_cleanup_reservations` cron-jobb fungerar inte som de ska. Den här frågan introducerades i [magento/lager#3046](https://github.com/magento/inventory/pull/3046).

**Lösning:** Utför följande MySQL-frågor för att manuellt rensa reservationer:

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

[!DNL Inventory Management] 1.1.6 (modulversion: `inventory-composer-metapackage = 1.1.6`) stöds i version 2.3.6 och är kompatibel med version 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1 och 2.3.0 av Adobe Commerce, Adobe Commerce i molninfrastruktur och kodbasen Magento Open Source.

![Korrigerat problem](../assets/fix.svg) Korrigeringar för att lösa problem relaterade till restorder, kreditnotor, rutnät för rapporter om låg stocknivå, korrigeringar kopplade till CLI-verktyget för att lösa inkonsekvenser samt allmänna förbättringar.

![Nytt](../assets/new.svg) **Asynkron omindexering av lager.** Lagringsmöjligheten att indexera om lager asynkront och prestandan för flera kritiska scenarier har förbättrats.

## 1.1.5

[!DNL Inventory Management] 1.1.5 (modulversion: `inventory-composer-metapackage = 1.1.5`) stöds i version 2.3.5 och är kompatibelt med version 2.3.4, 2.3.3, 2.3.2, 2.3.1 och 2.3.0 av Adobe Commerce, Adobe Commerce i molninfrastruktur och kodbasen Magento Open Source.

![Nytt](../assets/new.svg) **Uppdatera lagret när produkt-SKU har ändrats.** En ny konfigurationsinställning introducerades för att växla till det nya beteendet: Synkronisera med katalog.

![Nytt](../assets/new.svg) **Funktionstester.** Nya funktionstester för att eliminera luckan i testtäckningen introducerades. Korrigerade flera problem som gjorde testerna mer stabila och tillförlitliga).

![Känt fel](../assets/bug.svg) Korrigeringar för att förhindra överförsäljning av produkter,&quot;Out of stock&quot;-produktsynlighet på butiken, flera korrigeringar för skalbart stöd för miljö och förbättringar av användargränssnittet.

## 1.1.4

[!DNL Inventory Management] 1.1.4 (modulversion: `inventory-composer-metapackage = 1.1.4`) stöds i version 2.3.4 och är kompatibelt med version 2.3.3, 2.3.2, 2.3.1 och 2.3.0 av Adobe Commerce, Adobe Commerce i molninfrastruktur och kodbasen Magento Open Source.

![Korrigerat problem ](../assets/fix.svg)**Förbättrade prestanda.** Introducerad bunchningslogik för CLI-kommando för lagerreservationer för att minska minnesanvändningen och undvika fall när processen fastnar utan något svar.

![Nytt ](../assets/new.svg)**Ökad testtäckning.** Många nya funktionstester introducerades. Nästan alla manuella inventeringsscenarier täcks av automatiserade tester.

![Känt fel](../assets/bug.svg) Flera korrigeringar som är inriktade på att lösa problem med kreditnotor, grupperade produkter samt käll- och aktiemassåtgärder.

## 1.1.3

[!DNL Inventory Management] 1.1.3 (modulversion: `inventory-composer-metapackage = 1.1.3`) stöds i version 2.3.3 och är kompatibelt med version 2.3.2, 2.3.1 och 2.3.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och kodbasen Magento Open Source.

![Korrigerat problem ](../assets/fix.svg)**Bättre integrering med Adobe Commerce- och B2B-funktioner.** [!DNL Inventory Management] fungerar nu korrekt med följande funktioner för webbplatser som använder andra lagerkällor än standardlager:

- Beställ på SKU (Adobe Commerce)
- Snabbordning (B2B)
- Rekvisitionslistor (B2B)

![Nytt ](../assets/new.svg)**Förbättrade prestanda.** Prestandan för katalogbläddring i Storefront har förbättrats för webbplatser som kör standardlagret och standardkällan.

![Nytt ](../assets/new.svg)**Ökad testtäckning.** Det automatiska funktions- och integreringstestets täckning har ökat avsevärt.

## 1.1.2

[!DNL Inventory Management] 1.1.2 (modulversion: `inventory-composer-metapackage = 1.1.2`) stöds i version 2.3.2 och är kompatibelt med version 2.3.1 och 2.3.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och kodbasen Magento Open Source.

![Korrigerat problem](../assets/fix.svg) Tillagd `source_code` GETENS svar `/V1/shipments` REST-slutpunkt. <!-- https://github.com/magento/inventory/pull/2142 -->

![Korrigerat problem](../assets/fix.svg) Löste problem med att rensa reservationer och uppdatera produktkvantiteter korrekt efter att ha utfärdat en kreditnota för en ej levererad order. När du väljer alternativet att <!-- https://github.com/magento/inventory/pull/2179 -->

![Korrigerat problem](../assets/fix.svg) Löste problem med att spara kvantitet för konfigurerbara underordnade produkter när kvantiteter anges när produkten skapas. <!-- https://github.com/magento/inventory/pull/2158 -->

Nya moduler för [!DNL Inventory Management] 1.1.2 Beta:

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![Nytt](../assets/new.svg) **Lagt till en slutpunkt för massöverföring av delar av lager** - Aktuella slutpunkter för massöverföring flyttar alla tilldelade kvantiteter från en ursprungskälla till en målkälla. Den nya `/rest/V1/inventory/bulk-partial-source-transfer` slutpunkten tillåter handlare att överföra partiellt lager från källan till källan som en gruppåtgärd. Om du vill överföra en viss kvantitet anger du en begäran till slutpunkten med `sku`, `qty`, `origin_source_code`och `destination_source_code`. Överföringar verifierar att källan har tilldelats `sku`, det finns tillräckligt med kvantitet att överföra och så vidare. Se [Massåtgärder för lager](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} i REST API-dokumentationen. <!-- https://github.com/magento/inventory/pull/2117 -->

![Nytt](../assets/new.svg) **Tillagd reserverings-CLI** - Nya kommandon ger dig möjlighet att upptäcka och lösa reservationsinkonsekvenser. När order skickas och ändrar status, [!DNL Inventory Management] genererar initiala reservationer och uppdateringar via kompensationsreservationer. Dessa kommandon returnerar en lista över upptäckta inkonsekvenser per order-ID, SKU och Stock-ID och skapar reservationer att lösa. Se [CLI-referens](cli.md) för mer information. <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![Nytt](../assets/new.svg) **Prestandaförbättringar för källor och SSA-alternativ** - Sortering och val av källor under transport orsakade prestandaförsämring för lager med ett stort antal källor. Den här versionen innehåller viktiga prestandaförbättringar för att lista och sortera tillgängliga källor när du granskar och väljer SSA-alternativ i leveranser. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![Nytt](../assets/new.svg) **GraphQL-stöd för Inventory management har lagts till** - Den här versionen installerar en ny `magento/module-inventory-graph-ql` -modul. GraphQL [ProductInterface-attribut](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} innehåller nu `only_x_left_in_stock` och `stock_status` attribut för [!DNL Inventory Management] support. <!-- https://github.com/magento/inventory/pull/2124 -->

![Nytt](../assets/new.svg) **Förenklat användargränssnitt för tilldelade källor** - Tabellen Tilldelade källor på produktsidor har förenklat innehåll för enklare uppdateringar och högre prestanda när många källor visas. Alla källor visas efter källnamn (hovra över för `source_code`).

![Nytt](../assets/new.svg) **Exportera Aggregerad Stock-tjänst** - Den här versionen innehåller en ny exportsammanställd lagerservice (med reservationer i systemet) som stöder externa Sales Channeler som Amazon, eBay och Google Shopping Reads.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0 (modulversion: `inventory-composer-metapackage = 1.1.0`) stöds och är kompatibelt med version 2.3.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och kodbasen Magento Open Source. [!DNL Inventory Management] 1.1.1 släpps endast som en paketnamnsuppdatering, som stöds för version 2.3.1 och är kompatibel med version 2.3.0 av Adobe Commerce, Adobe Commerce i molninfrastrukturen och kodbasen Magento Open Source.

![Korrigerat problem](../assets/fix.svg) **Stöd för Elasticsearch för single- och multi-source-lägen har lagts till** — Du kan nu konfigurera och använda Elasticsearch med anpassade lager. Se [Konfigurera tjänsten Elasticsearch](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html){target="_blank"} för installationsinformation. <!-- PR https://github.com/magento/inventory/pull/1943 -->

![Korrigerat problem](../assets/fix.svg) Åtgärdade prestandaproblem med Default Stock för att drastiskt öka prestanda med flera åtgärder. Förbättringar ökar prestandan för single-source-läge, Överför lager till källa, Kategorisidor i Storefront och Beräkningar av försäljningsmängd.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![Korrigerat problem](../assets/fix.svg) Löste problem med utlagerstatus och bulklageröverföring till Stock för konfigurerbara och grupperade produkter. Produktstatusen påverkas inte om du väljer de överordnade produkterna och utför massåtgärder. Om den överordnade produkten var i Stock finns den kvar i Stock.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![Nytt](../assets/new.svg) **Avståndsprioritetsalgoritm** — Algoritmen Distance Priority (Avståndsprioritet) är en ny, körklar algoritm för val av källa för avståndsbaserade leveransrekommendationer. Den här algoritmen jämför platsen för leveransdestinationsadressen med källplatserna för att avgöra vilken källa som är närmast för att leverera försändelser. Avståndet kan avgöras av antingen fysiskt avstånd eller den tid som tillbringas med att resa från en plats till en annan, med hjälp av importerade geokodsdata eller Google-anvisningar (körning, gång eller cykling).

![Nytt](../assets/new.svg) **Utökad källkvantitetslista** — Handlare med ett stort antal källor kan enkelt hovra och visa alla källor per produkt via produktrutnätet. Varje produkt har minst fem källor och motsvarande kvantiteter. När du hovrar över källorna kan du bläddra igenom hela listan med källor och aktuella kvantiteter.

![Känt fel](../assets/bug.svg) Känt problem med Magento Open Source och Adobe Commerce v2.3.1 - Asynkron datamigrering mellan källor påträffar problem på grund av ändringar i asynkrona API:er med ämnesnamn som avspeglar PHP-klass- och metodnamn. Använda synkrona åtgärder, ange **[!UICONTROL Run asynchronously]** till `No`, rekommenderas.
