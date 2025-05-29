---
title: Indexhantering
description: Lär dig mer om indexhantering, inklusive åtgärder som utlöser omindexering och bästa praxis.
exl-id: cbb249a2-b957-44fe-bf81-df795a8fd5d1
feature: System, Configuration
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '1296'
ht-degree: 0%

---

# Indexhantering

Adobe Commerce och Magento Open Source indexerar om automatiskt när ett eller flera objekt ändras. Åtgärder som utlöser omindexering är bland annat prisändringar, att skapa prisregler för kataloger och kundvagnar, att lägga till nya kategorier och så vidare. För att optimera prestandan samlar Commerce in data i särskilda tabeller med hjälp av indexerare. När data ändras måste de indexerade tabellerna uppdateras - eller indexeras om. Commerce indexerar om som en bakgrundsprocess och butiken är fortfarande tillgänglig under processerna.

Omindexering av data snabbar upp bearbetningen och minskar kundens väntetid. Om du till exempel ändrar priset på ett objekt från $4.99 till $3.99 indexeras data om i Commerce så att prisändringen visas i butiken. Utan indexering måste Commerce beräkna priset på varje produkt i farten, hantera kundvagnsregler, paketpriser, rabatter, nivåpriser osv. Att läsa in priset för en produkt kan ta längre tid än kunden är beredd att vänta.

Indexerarna kan ställas in på att antingen uppdateras när de sparas eller enligt schema. Alla index kan använda båda alternativen, förutom kundstödraster som bara stöds när de sparas. När du indexerar när du sparar, startar Commerce om indexeringen när du sparar åtgärder. Indexhanteringssidan slutför uppdateringen och tömmer cacheminnet, och meddelandet om omindexering visas inom en minut eller två. Vid omindexering av ett schema körs ett omindexvärde enligt ett schema som ett cron-jobb. Ett systemmeddelande visas om ett [cron-jobb](cron.md) inte är tillgängligt för att uppdatera indexerare som blir ogiltiga. Butiken är fortfarande tillgänglig under omindexeringsprocesserna.

>[!NOTE]
> Adobe Commerce handlare som använder Live Search, Catalog Service eller Product Recommendations har möjlighet att använda en [SaaS-baserad prisindexerare](https://experienceleague.adobe.com/docs/commerce/price-indexer/index.html?lang=sv-SE).

När du behöver indexera om visas ett meddelande högst upp på sidan. Indexet och meddelandet rensas baserat på omindexeringsläget och möjliga åtgärder som du vidtar. Mer information om indexering finns i [Hur programmet implementerar indexering](https://developer.adobe.com/commerce/php/development/components/indexing/#how-the-application-implements-indexing) i _PHP-utvecklarhandboken_.

![Indexhantering - åtgärder](./assets/index-management.png){width="700" zoomable="yes"}

- Indexhantering har en något annorlunda presentation för platta produktkataloger.
- För att undvika problem när flera administratörsanvändare uppdaterar objekt som utlöser automatisk omindexering rekommenderar vi att du anger att alla indexerare ska köras enligt schemat som [cron-jobb](cron.md). Annars kan objekt med inbördes beroenden orsaka dödläge varje gång ett objekt sparas. Symtomen på ett dödläge är bland annat hög användning av CPU och MySQL-fel. Det är en god idé att använda schemalagd indexering.
- ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Som standard loggas administratörsåtgärder, som omindexering, av systemet och kan visas i [Åtgärdsloggrapporten](action-log-report.md). Åtgärdsloggning kan konfigureras i [Loggning för administrationsåtgärder](action-log.md) i butikens avancerade administratörsinställningar.

## Metodtips för omindexering

Omindexering och cachelagring har olika syften i Commerce. Indexen spårar databasinformation för bättre sökprestanda, snabbare datahämtning för butiker med mera. [Caches](cache-management.md) sparar inlästa data, bilder, format och liknande för att få bättre prestanda vid inläsning och åtkomst till butiken.

- Vanligtvis vill du indexera om när du uppdaterar data i Commerce.
- Om du har en stor butik eller flera butiker kanske du vill ställa in indexerare som kategori och produkter på schemalagda cron-jobb på grund av möjligheten att indexera om slingor. Du kanske vill ställa in omindexet enligt ett schema under icke-toppvärdesdagar.
- När du indexerar om behöver du inte också utföra en tömningscache.
- För nya Commerce-installationer måste du tömma cachen och indexera om.
- Datorns webbläsarcache rensas inte när du tömmer cacheminnet och indexerar om. Rensa webbläsarcachen när du har slutfört uppdateringarna i butiken.

## Ändra indexläge

>[!IMPORTANT]
>
>För butiker som använder [Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=sv-SE) och har angett Elasticsearch som fulltextindexerare (`catalogsearch_fulltext`): fulltextindexet måste köras igen efter att gruppbehörigheter har ändrats eller när behörighetsindexeraren är i läget Schemalagd.

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Index Management]**&#x200B;på sidofältet_ Admin _.

1. Markera kryssrutan för varje indexerare som du vill ändra.

1. Ange **[!UICONTROL Actions]** till något av följande:

   - `Update on Save`
   - `Update by Schedule`
   - `Invalidate index`

   >[!IMPORTANT]
   >
   >Kundstödraster kan bara indexeras om med `Update on Save`. Indexet har **_inte_** stöd för `Update by Schedule`.

1. Klicka på **[!UICONTROL Submit]** för att tillämpa ändringen på varje vald indexerare.

   **Indexhanteringskolumner**

   | Kolumn | Beskrivning |
   | ------ |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | [!UICONTROL Indexer] | Indexerarens namn. |
   | [!UICONTROL Description] | En beskrivning av indexeraren. |
   | [!UICONTROL Mode] | Anger det aktuella uppdateringsläget för varje indexerare. Alternativ: <br/>**[!UICONTROL Update on Save]**- Indexet är inställt på att uppdateras när en entitetsändring sparas. Dessa enheter omfattar produkter, kategorier och kunder. När sparåtgärden är klar börjar en serie steg fånga upp ändringarna och uppdatera indexet. Sidan Indexhantering uppdateras och tömmer indexeringsmeddelandet inom en minut eller två.<br/>**[!UICONTROL Update on Schedule]** - Indexet är inställt på att uppdateras enligt schemat enligt ett [cron-jobb](cron.md). cron-jobbet inkluderar schemaintervallet för omindexering och skrivning av uppdateringar till indexet vid körning. |
   | [!UICONTROL Schedule Status] | Visar schemats statusuppdateringar. |
   | [!UICONTROL Status] | Visar något av följande: <br/>**[!UICONTROL Ready]**- Indexet är uppdaterat.<br/>**[!UICONTROL Suspended]** - Omindexering har pausats. <br/>**[!UICONTROL Processing]**- Omindexering körs.<br/>**[!UICONTROL Reindex Required]** - En ändring har gjorts som kräver omindexering, men indexerarna kan inte uppdateras automatiskt. Kontrollera om [cron](cron.md) är tillgänglig och korrekt konfigurerad. |
   | [!UICONTROL Updated] | Anger det datum och den tidpunkt då ett index senast uppdaterades. |

   {style="table-layout:auto"}

## Indexera om med kommandoraden

I Commerce finns fler alternativ för indexering via kommandoraden. Fullständig information och kommandoalternativ finns i [Indexera om](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html?lang=sv-SE#reindex){:target="blank"} i _Konfigurationshandboken_.

## Utlösarhändelser för index

## Utlösare för omindexering

| Indextyp | Omindexeringshändelse |
| ---------- | ---------------- |
| [!UICONTROL Product Prices] | Lägg till kundgrupp<br/>Ändra konfigurationsinställningar |
| [!UICONTROL Flat catalog product data] | Lägg till butik<br/>Lägg till butiksgrupp<br/>Lägg till, redigera eller ta bort attribut (för sökning och filtrering) |
| [!UICONTROL Flat catalog category data] | Lägg till butik<br/>Lägg till butiksgrupp<br/>Lägg till, redigera eller ta bort attribut (för sökning och filtrering) |
| [!UICONTROL Catalog category/product index] | Lägg till, redigera eller ta bort produkter (en, flera, massvis och import)<br/>Ändra relationer mellan produkter och kategorier<br/>Lägg till, redigera eller ta bort kategorier<br/>Lägg till eller ta bort butiker<br/>Ta bort butiksgrupper<br/>Ta bort webbplatser |
| [!UICONTROL Catalog search index] | Lägg till, redigera eller ta bort produkter (en, flera, massvis och import)<br/>Lägg till eller ta bort butiker<br/>Ta bort butiksgrupper<br/>Ta bort webbplatser |
| [!UICONTROL Stock status index] | Ändra inställningar för lagerkonfiguration. |
| [!UICONTROL Category permissions index] | Lägg till butik<br/>Lägg till butiksgrupp<br/>Lägg till, ta bort eller uppdatera attribut (för sökning och filtrering) |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Vi rekommenderar inte längre att du använder en platt katalog som bästa praxis. Fortsatt användning av den här funktionen är känd för att orsaka prestandaförsämring och andra indexeringsproblem. Mer information finns i [Använd en platt katalogprodukt](../catalog/catalog-flat.md).

## Indexera åtgärder och kontroller

| Åtgärd | Resultat | Kontroller |
| ------ | ------ | -------- |
| Skapar en butik, ny kundgrupp eller någon åtgärd som listas i `Actions that Cause a Full Reindex` | Fullständig omindexering | Fullständig omindexering utförs enligt det schema som bestäms av ditt Adobe Commerce- eller Magento Open Source-jobb. |
| Massinläsning av objekt (Commerce import/export, Direct SQL-fråga och andra metoder som direkt lägger till, ändrar eller tar bort data) | Partiell omindexering (endast ändrade objekt omindexeras) | Med den frekvens som bestäms av ditt Commerce kron-jobb. |
| Ändra omfång (till exempel från global till webbplats) | Partiell omindexering (endast ändrade objekt omindexeras) | Med den frekvens som bestäms av ditt Commerce kron-jobb. |

{style="table-layout:auto"}

## Händelser som utlöser fullständig omindexering

| Indexerare | Händelse |
| ------- | ----- |
| [!UICONTROL Catalog Category Flat Indexer] | Skapa en webbutik<br/>Skapa en webbutiksvy<br/>Skapa eller ta bort ett attribut som är något av följande:<br/>- Sökbart eller synligt i avancerad sökning<br/>- Filterable<br/>- Filterbart i sökning<br/> - Används för sortering<br/>Ändra ett befintligt attribut till något av föregående.<br/>Aktivera alternativ för butiker i platta kategorier |
| [!UICONTROL Catalog Product Flat Indexer] | Skapa en webbutik<br>Skapa en webbutiksvy<br/>Skapa eller ta bort ett attribut som är något av följande:<br/>- Sökbart eller synligt i avancerad sökning<br>- Filterable<br>- Filterbart i sökning<br/> - Används för sortering <br/>Ändra ett befintligt attribut så att det blir något av föregående.<br/>Aktivera alternativ för butiker i platta kategorier |
| [!UICONTROL Stock status indexer] | När följande _alternativ för kataloginventering_ ändras i systemkonfigurationen:<br/>`Stock Options` - Visa utanför Stock-produkter<br/>`Product Stock Options` - Hantera Stock |
| [!UICONTROL Price Indexer] | Lägga till en kundgrupp.<br/>När något av följande alternativ för kataloginventering ändras i systemkonfigurationen:<br/>`Stock Options` - Visa utanför Stock-produkter<br/>`Product Stock Options` - Hantera Stock<br/>`Price` - Katalogens prisomfång |
| [!UICONTROL Category or Product Indexer] | Skapa eller ta bort en butiksvy<br/>Ta bort en butik<br/>Ta bort en webbplats |

{style="table-layout:auto"}
