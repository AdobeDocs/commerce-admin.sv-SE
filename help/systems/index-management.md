---
title: Indexhantering
description: Lär dig mer om indexhantering, inklusive åtgärder som utlöser omindexering och bästa praxis.
exl-id: cbb249a2-b957-44fe-bf81-df795a8fd5d1
feature: System, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1281'
ht-degree: 0%

---

# Indexhantering

Adobe Commerce och Magento Open Source indexerar om automatiskt när ett eller flera objekt ändras. Åtgärder som utlöser omindexering är bland annat prisändringar, att skapa prisregler för kataloger och kundvagnar, att lägga till nya kategorier och så vidare. För att optimera prestandan samlar Commerce in data i särskilda tabeller med hjälp av indexerare. När data ändras måste de indexerade tabellerna uppdateras - eller indexeras om. Commerce indexerar om som en bakgrundsprocess och butiken är fortfarande tillgänglig under processerna.

Omindexering av data snabbar upp bearbetningen och minskar kundens väntetid. Om du till exempel ändrar priset på ett objekt från $4.99 till $3.99 indexeras data om i Commerce så att prisändringen visas i butiken. Utan indexering måste Commerce beräkna priset på varje produkt i farten, hantera kundvagnsregler, paketpriser, rabatter, nivåpriser osv. Att läsa in priset för en produkt kan ta längre tid än kunden är beredd att vänta.

Indexerarna kan ställas in på att antingen uppdateras när de sparas eller enligt schema. Alla index kan använda båda alternativen, förutom kundstödraster som bara stöds när de sparas. När du indexerar när du sparar, startar Commerce om indexeringen när du sparar åtgärder. Indexhanteringssidan slutför uppdateringen och tömmer cacheminnet, och meddelandet om omindexering visas inom en minut eller två. Vid omindexering av ett schema körs ett omindexvärde enligt ett schema som ett cron-jobb. Ett systemmeddelande visas om en [cron](cron.md) är inte tillgänglig för att uppdatera indexerare som blir ogiltiga. Butiken är fortfarande tillgänglig under omindexeringsprocesserna.

>[!NOTE]
> Adobe Commerce handlare som använder Live Search, Catalog Service eller Product Recommendations kan använda en [SaaS-baserad prisindexerare](https://experienceleague.adobe.com/docs/commerce-merchant-services/price-indexer/index.html).

När du behöver indexera om visas ett meddelande högst upp på sidan. Indexet och meddelandet rensas baserat på omindexeringsläget och möjliga åtgärder som du vidtar. Mer information om indexering finns i [Hur programmet implementerar indexering](https://developer.adobe.com/commerce/php/development/components/indexing/#how-the-application-implements-indexing) i _Utvecklarhandbok för PHP_.

![Indexhantering - åtgärder](./assets/index-management.png){width="700" zoomable="yes"}

- Indexhantering har en något annorlunda presentation för platta produktkataloger.
- För att undvika problem när flera administratörsanvändare uppdaterar objekt som utlöser automatisk omindexering rekommenderar vi att du ställer in alla indexerare att köras enligt schema som [cron](cron.md). Annars kan objekt med inbördes beroenden orsaka dödläge varje gång ett objekt sparas. Symtomen på ett dödläge är bland annat hög processoranvändning och MySQL-fel. Det är en god idé att använda schemalagd indexering.
- ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Som standard loggas administratörsåtgärder, som omindexering, av systemet och kan visas i [Åtgärdsloggsrapport](action-log-report.md). Åtgärdsloggning kan konfigureras i [Loggning av administratörsåtgärder](action-log.md) i butikens avancerade administratörsinställningar.

## Metodtips för omindexering

Omindexering och cachelagring har olika syften i Commerce. Indexen spårar databasinformation för bättre sökprestanda, snabbare datahämtning för butiker med mera. [Cacher](cache-management.md) spara inlästa data, bilder, format och liknande för bättre prestanda vid inläsning och åtkomst till butiken.

- Vanligtvis vill du indexera om när du uppdaterar data i Commerce.
- Om du har en stor butik eller flera butiker kanske du vill ställa in indexerare som kategori och produkter på schemalagda cron-jobb på grund av möjligheten att indexera om slingor. Du kanske vill ställa in omindexet enligt ett schema under icke-toppvärdesdagar.
- När du indexerar om behöver du inte också utföra en tömningscache.
- För nya Commerce-installationer måste du tömma cachen och indexera om.
- Datorns webbläsarcache rensas inte när du tömmer cacheminnet och indexerar om. Rensa webbläsarcachen när du har slutfört uppdateringarna i butiken.

## Ändra indexläge

>[!IMPORTANT]
>
>För butiker som använder [Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html) och har angett Elasticsearch som fulltext (`catalogsearch_fulltext`) indexerare: fulltextindexet måste köras igen efter att gruppbehörigheter har ändrats eller när permissions-indexeraren är i läget Scheduled.

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Index Management]**.

1. Markera kryssrutan för varje indexerare som du vill ändra.

1. Ange **[!UICONTROL Actions]** till något av följande:

   - `Update on Save`
   - `Update by Schedule`
   - `Invalidate index`

   >[!IMPORTANT]
   >
   >Kundstödraster kan endast indexeras om med `Update on Save`. Det här indexet gör **_not_** support `Update by Schedule`.

1. Klicka **[!UICONTROL Submit]** för att tillämpa ändringen på varje vald indexerare.

   **Indexhanteringskolumner**

   | Kolumn | Beskrivning |
   | ------ |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | [!UICONTROL Indexer] | Indexerarens namn. |
   | [!UICONTROL Description] | En beskrivning av indexeraren. |
   | [!UICONTROL Mode] | Anger det aktuella uppdateringsläget för varje indexerare. Alternativ: <br/>**[!UICONTROL Update on Save]**- Indexet ställs in på att uppdateras när en entitetsändring sparas. Dessa enheter omfattar produkter, kategorier och kunder. När sparåtgärden är klar börjar en serie steg fånga upp ändringarna och uppdatera indexet. Sidan Indexhantering uppdateras och tömmer indexeringsmeddelandet inom en minut eller två.<br/>**[!UICONTROL Update on Schedule]** - Indexet är inställt på att uppdateras enligt ett schema [cron](cron.md). cron-jobbet inkluderar schemaintervallet för omindexering och skrivning av uppdateringar till indexet vid körning. |
   | [!UICONTROL Schedule Status] | Visar schemats statusuppdateringar. |
   | [!UICONTROL Status] | Visar något av följande: <br/>**[!UICONTROL Ready]**— Indexet är uppdaterat.<br/>**[!UICONTROL Suspended]** - Omindexering har pausats. <br/>**[!UICONTROL Processing]**- Omindexering pågår.<br/>**[!UICONTROL Reindex Required]** - En ändring har gjorts som kräver omindexering, men indexerarna kan inte uppdateras automatiskt. Kontrollera om [cron](cron.md) är tillgänglig och korrekt konfigurerad. |
   | [!UICONTROL Updated] | Anger det datum och den tidpunkt då ett index senast uppdaterades. |

   {style="table-layout:auto"}

## Indexera om med kommandoraden

I Commerce finns fler alternativ för indexering via kommandoraden. Fullständig information och kommandoalternativ finns i [Indexera om](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html#reindex){:target=&quot;blank&quot;} i _Konfigurationshandbok_.

## Utlösarhändelser för index

## Utlösare för omindexering

| Indextyp | Omindexeringshändelse |
| ---------- | ---------------- |
| [!UICONTROL Product Prices] | Lägg till kundgrupp<br/>Ändra konfigurationsinställningar |
| [!UICONTROL Flat catalog product data] | Lägg till butik<br/>Lägg till butiksgrupp<br/>Lägg till, redigera eller ta bort attribut (för sökning och filtrering) |
| [!UICONTROL Flat catalog category data] | Lägg till butik<br/>Lägg till butiksgrupp<br/>Lägg till, redigera eller ta bort attribut (för sökning och filtrering) |
| [!UICONTROL Catalog category/product index] | Lägga till, redigera eller ta bort produkter (en, massan och import)<br/>Ändra relationer mellan produkter och kategorier<br/>Lägga till, redigera eller ta bort kategorier<br/>Lägg till eller ta bort butiker<br/>Ta bort butiksgrupper<br/>Ta bort webbplatser |
| [!UICONTROL Catalog search index] | Lägga till, redigera eller ta bort produkter (en, massan och import)<br/>Lägg till eller ta bort butiker<br/>Ta bort butiksgrupper<br/>Ta bort webbplatser |
| [!UICONTROL Stock status index] | Ändra inställningar för lagerkonfiguration. |
| [!UICONTROL Category permissions index] | Lägg till butik<br/>Lägg till butiksgrupp<br/>Lägg till, ta bort eller uppdatera attribut (för sökning och filtrering) |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Vi rekommenderar inte längre att du använder en platt katalog som bästa praxis. Fortsatt användning av den här funktionen är känd för att orsaka prestandaförsämring och andra indexeringsproblem. Se [Använd platt katalogprodukt](../catalog/catalog-flat.md) för mer information.

## Indexera åtgärder och kontroller

| Åtgärd | Resultat | Kontroller |
| ------ | ------ | -------- |
| Skapa en butik, ny kundgrupp eller någon åtgärd som listas i `Actions that Cause a Full Reindex` | Fullständig omindexering | Fullständig omindexering utförs enligt det schema som bestäms av ditt Adobe Commerce- eller Magento Open Source-jobb. |
| Massinläsning av objekt (Commerce import/export, Direct SQL-fråga och andra metoder som direkt lägger till, ändrar eller tar bort data) | Partiell omindexering (endast ändrade objekt omindexeras) | Med den frekvens som bestäms av ditt Commerce kron-jobb. |
| Ändra omfång (till exempel från global till webbplats) | Partiell omindexering (endast ändrade objekt omindexeras) | Med den frekvens som bestäms av ditt Commerce kron-jobb. |

{style="table-layout:auto"}

## Händelser som utlöser fullständig omindexering

| Indexerare | Händelse |
| ------- | ----- |
| [!UICONTROL Catalog Category Flat Indexer] | Skapa en webbutik<br/>Skapa en webbutiksvy<br/>Skapa eller ta bort ett attribut som är något av följande:<br/>- Sökbar eller synlig vid avancerad sökning<br/>- Filterbar<br/>- Filterbar i sökningen<br/>- Används för sortering<br/>Ändra ett befintligt attribut till något av föregående.<br/>Aktivera alternativ för butiker i platta kategorier |
| [!UICONTROL Catalog Product Flat Indexer] | Skapa en webbutik<br>Skapa en webbutiksvy<br/>Skapa eller ta bort ett attribut som är något av följande:<br/>- Sökbar eller synlig vid avancerad sökning<br>- Filterbar<br>- Filterbar i sökningen<br/>- Används för sortering <br/>Ändra ett befintligt attribut till något av föregående.<br/>Aktivera alternativ för butiker i platta kategorier |
| [!UICONTROL Stock status indexer] | När följande _Alternativ för kataloginventering_ ändring av systemkonfigurationen:<br/>`Stock Options` - Visa ej lagrade produkter<br/>`Product Stock Options` - Hantera Stock |
| [!UICONTROL Price Indexer] | Lägga till en kundgrupp.<br/>När något av följande alternativ för kataloginventering ändras i systemkonfigurationen:<br/>`Stock Options` - Visa ej lagrade produkter<br/>`Product Stock Options` - Hantera Stock<br/>`Price` - Katalogens prisomfång |
| [!UICONTROL Category or Product Indexer] | Skapa eller ta bort en butiksvy<br/>Ta bort en butik<br/>Ta bort en webbplats |

{style="table-layout:auto"}
