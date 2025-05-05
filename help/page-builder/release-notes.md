---
title: Versionsinformation för  [!DNL Page Builder]
description: Läs versionsinformationen om du vill ha information om alla  [!DNL Page Builder] releaser.
exl-id: 81abe2f9-ed48-49fe-bbf0-70699d7106b2
feature: Page Builder, Release Notes
source-git-commit: addc34aeb4418aa3a1a9c2fc3adca738352ef94f
workflow-type: tm+mt
source-wordcount: '2813'
ht-degree: 0%

---

# Versionsinformation för [!DNL Page Builder]

I versionsinformationen beskrivs releaser av [!DNL Page Builder] och här ingår:

![Nya](../assets/new.svg) nya funktioner

![Korrigerat problem](../assets/fix.svg) Korrigeringar och förbättringar

![Känt fel](../assets/bug.svg) Kända fel

>[!IMPORTANT]
>
>Från och med version 2.4.3 är [!DNL Page Builder] nu tillgängligt som ett paketerat tillägg i Magento Open Source. Det är nu standardverktyget för innehållsredigering för både Adobe Commerce och Magento Open Source och kan ersätta WYSIWG-redigeraren med en tredjepartsmodul.

## 1.7.2 för Commerce 2.4.5

![Nytt](../assets/new.svg) **Ny wrapper-entitet - [!DNL Columns] behållare introducerad för kolumnlayouter** - Tidigare kunde användare bara lägga till kolumner inuti en annan behållar-/wrapper-innehållstyp, till exempel en [!DNL Tab] eller [!DNL Row]. [!DNL Column] har nu en egen wrapper och kan läggas till direkt på scenen. Behållaren [!DNL Columns] har också ett inställningselement där användare kan ange konfiguration för den här wrapper-entiteten.<!--- PB-500-->

![Nytt](../assets/new.svg) **Nya menyalternativ för att duplicera, dölja och ta bort kolumngrupper** - Med dessa nya alternativ kan användare duplicera, dölja och ta bort [!DNL Columns] grupper, precis som de kan med innehållstyper.<!--- PB-507-->

![Nytt](../assets/new.svg) <!-- Issue 594 -->**Nytt stöd för flera kolumner har lagts till i kolumngruppen** - Med det här tillägget kan användare ändra flera rader med kolumner inuti en [!DNL Columns]-grupp för att göra kolumnlayouterna mycket mer flexibla.<!--- PB-108-->

Mer information om hur du använder den nya gruppen [!DNL Columns] finns i [Layout - kolumn ](./column.md).

## 1.7.1 för Commerce 2.4.4

![Åtgärdat problem](../assets/fix.svg) Page Builder är nu kompatibelt med PHP 8.1.<!--- AC-1300-->

![Korrigerat problem](../assets/fix.svg) Marknadsförare kan nu lägga till alternativ text (`alt_text`) till bilder (bild, banderoll, bild) för att förbättra innehållets tillgänglighet.<!--- PB-1193-->

![Ett problem har korrigerats](../assets/fix.svg) Administratörsanvändare med begränsad behörighet till endast innehållsredigering kan inte längre se ett fel när Page Builder används för att lägga till en produktwidget på en CMS-sida. I Page Builder visas även ett korrekt produktantal på sidan med widgetinställningar. Tidigare krävde Page Builder behörighet till katalogmodulen vid hämtning av produktantal och följande fel visades: `A technical problem with the server created an error. Try again to continue what you were doing. If the problem persists, try again later`. <!--- MC-42779-->

![Ett problem har korrigerats](../assets/fix.svg) Visningsproblem med Page Builder-formatmenyn har åtgärdats med biblioteksuppgraderingen TinyMCE 5. <!--- AC-446-->

![Korrigerat problem](../assets/fix.svg) Du kan nu använda musen för att redigera ett **Text att visa** -värde i popup-fönstret Infoga länk. <!--- AC-982-->

![Åtgärdat problem](../assets/fix.svg) I Page Builder visas nu alla alternativ som förväntat på alternativmenyn Teckenstorlek. Tidigare visades inte alla alternativ. <!--- AC-1056-->

![Korrigerat problem](../assets/fix.svg) Uppgraderade `phpgt/dom` dispositionsberoendet för tillägget `magento/magento2-page-builder` till de senaste versionerna. <!--- magento/magento2-page-builder/pull/779-->

![Åtgärdat problem](../assets/fix.svg) Sidverktyget ändrar inte längre storlek på dialogrutorna Infoga länk och Infoga bild när skjutreglaget visas i en liten kolumn. <!--- AC-973-->

![Korrigerat problem](../assets/fix.svg) Menyn Egenskaper för Page Builder-tabell visas nu som förväntat. <!--- AC-407-->

![Korrigerat problem](../assets/fix.svg) Skjutreglage visas inte längre på länken Infoga eller bilden modal när musen inte hålls över skjutreglaget. <!--- AC-406-->

![Ett problem har korrigerats](../assets/fix.svg) Teckensnittsstorleken som används för att visa alternativen på menyn Tabell har optimerats. <!--- AC-396-->

![Korrigerat problem](../assets/fix.svg) Korrigerade avvikelser med placeringen av dialogrutorna Infoga/redigera bild och Infoga/redigera länk. <!--- AC-397-->

![Åtgärdat problem](../assets/fix.svg) Page Builder genererar inte längre ett fel när du klickar på **Textredigeraren** för en banderoll. <!--- AC-398-->

![Åtgärdat problem](../assets/fix.svg) I Page Builder konverteras inte längre alla dynamiska block till ett språk under uppgraderingen. <!--- MC-42265-->

## 1.6.0 för Adobe Commerce 2.4.2

![Nytt](../assets/new.svg) <!-- Issue 558 -->**Nytt [!DNL Page Builder] format** - [!DNL Page Builder] har gjort stora förbättringar i hur innehållet formateras. Ändringarna gör det nu enkelt att skapa enkla CSS-väljare som åsidosätter de befintliga innehållstypsformaten. Dessa ändringar gör det möjligt att skapa [!DNL Page Builder] teman med hög svarstid för alla innehållstyper.

![Ny](../assets/new.svg) <!-- Issue 429 -->**Radbehållare är nu valfri** - du kan nu skapa innehåll i [!DNL Page Builder] utan att behöva använda en radbehållare. Förutom raden kan följande innehållstyper nu dras och släppas direkt på scenen: HTML, Block, Dynamiskt block, Kolumner och Tabbar.

![Nytt](../assets/new.svg) <!-- Issue 636 -->**Ny responsiv visningsportväljare** - Du kan nu förhandsgranska ditt [!DNL Page Builder]-innehåll med olika enhetsbredder (brytpunkter) med de nya administratörsvisningsruteknapparna ovanför scenen. Visningsväljaren simulerar hur innehållet är formaterat när det visas på butiken med olika enheter.

![Nytt](../assets/new.svg) <!-- Issue 637 -->**Nya brytpunktsspecifika formulärfält** - Fältvärden för innehållstyp kan nu ställas in på specifika brytpunkter för visningsruta. Ikonindikatorerna bredvid fälten visar visningsrutan som innehållstypens fältvärde används för.

![Nytt](../assets/new.svg) <!-- Issue 559 -->**Borttagna fördefinierade formulärfältsposter** - Avancerade formulärinställningar för marginaler, utfyllnader och kantlinjerelaterade egenskaper (kantlinje, kantbredd och kantradie) har nu angetts som `default` så att värden kan definieras med en moduls CSS.

![Nytt](../assets/new.svg) <!-- Issue 635, 557,  -->**Mellanrum på scenen har lagts till** - Rader och kolumner har nu extra mellanrum runt innehållstyper på scenen, men inte på lagerframsidan. Det extra mellanrummet gör det enklare att komma åt alternativmenyerna för muspekaren för både behållaren och innehållstyperna.

![Korrigerat problem](../assets/fix.svg) <!-- MC-37348 -->**Automatisk rullning till granskningar har korrigerats** - Autobullning till produktgranskningar i butiken har nu åtgärdats.

![Korrigerat problem](../assets/fix.svg) <!-- MC-36227 -->**Fast beskuret innehåll** - Längd kategori och produktbeskrivningar beskärs inte längre.

![Korrigerat problem](../assets/fix.svg) <!-- MC-35402 -->**Fast Kategori med full bredd** - Kategoriinnehåll kan nu visas i en layout med full bredd eller helt utfall.

![Korrigerat problem](../assets/fix.svg) <!-- MC-37989 -->**Säkerhetsförbättringar**

## 1.5.1 för Adobe Commerce 2.4.1-p1

![Korrigerat problem](../assets/fix.svg) <!-- PB-1140, MC-38812 -->**Felvisning** - Korrigerat ett fel där [!DNL Page Builder] visade ett fel när katalogens underkategorier lades till i administratören.

## 1.5.0 för Adobe Commerce 2.4.1

![Nytt](../assets/new.svg) <!-- Issue 510, 511, 512, 513 -->**Immersiv helskärmsredigering** - Innehåll som redigeras [!DNL Page Builder] visas nu endast i helskärmsläge för alla områden som styrs av [!DNL Page Builder]. Den här ändringen omfattar CMS-sidor, produkt- och kategorisidor, block och dynamiska block. Vid helskärmsredigering fokuseras ditt innehåll och ger en vy som bättre matchar användarupplevelsen i butiken.

![Nya](../assets/new.svg) <!-- Issue 544 -->**[!DNL Page Builder] förhandsgranskningar av innehåll &#x200B;**- Som standard innehåller [!DNL Page Builder] nu förhandsgranskningar av innehåll inte bara för CMS-sidor, block och dynamiska block, utan även för produkt- och kategorisidor. Du kan konfigurera den här funktionen så att den är aktiverad eller inaktiverad för produkt- och kategorisidor med den nya inställningen [!DNL Page Builder] för förhandsvisning av innehåll, som du kommer åt i butikskonfigurationen på Innehållshantering > Avancerade innehållsverktyg.

![Nytt](../assets/new.svg) <!-- Issue 543 -->**Förbättrad åtkomst till korta produktbeskrivningar** - Som standard visas en kort produktbeskrivning före den längre beskrivningen. Ändringen matchar den ordning som de visas i butiken och förhindrar att det längre beskrivningsinnehållet behöver bläddras igenom för att komma åt den korta beskrivningen.

![Nytt](../assets/new.svg) <!-- Issue 419 -->**Förhindra kapslade länkar i banners och bilder** - Lägg till länkar till både innehållet och de yttre elementen i banners och Presentationer som skapade kapslade länkar som inte visades eller beteddes korrekt i butiken. Lös problemet genom att inte längre lägga till länkar i *både* meddelandetextområdet och länkattributet för banderoller och bilder.

![Korrigerat problem](../assets/fix.svg) <!-- Issue 421 --> Ett problem har korrigerats där en tom kantradie för ett flikobjekt orsakade fel och hade skadat flikobjektsinnehåll.

![Korrigerat problem](../assets/fix.svg) <!-- Issue 422 --> Ett problem där tillägg av vissa kombinationer av villkor till filtret för produktvillkor orsakade fel som gjorde att produktformuläret inte kunde sparas har åtgärdats.

![Korrigerat problem](../assets/fix.svg) <!-- Issue 425 -->Korrigerat problem där Slider-innehållstypen inte betedde sig korrekt när Inställningen för oändlig slinga inaktiverades.

![Korrigerat problem](../assets/fix.svg) <!-- Issue 426 -->Korrigerat lägsta kampanjpris så att det nu fungerar i [!DNL Page Builder].

![Korrigerat problem](../assets/fix.svg) <!-- Issue 436 -->Korrigerat problemet i Safari och IE 11 som förhindrade att en bild drog och släpptes till överföringsområdet i Banners and Presentationer.

![Ett problem som orsakade att Slider-innehållstypen inte svarade i Firefox har åtgärdats.](../assets/fix.svg) <!-- Issue 525 -->Ett problem har korrigerats.

![Korrigerat problem](../assets/fix.svg) <!-- Issue 567 -->Ett problem där widgetkonfigurationen skapade felaktiga väljare i DOM för de olika utseendena har korrigerats.

![Korrigerat problem](../assets/fix.svg) <!-- Issue 609 -->Korrigerade ett fel där innehållstypens alternativmeny doldes av sidhuvudsverktygsfältet, vilket förhindrade åtkomst till formuläret och andra alternativ.

![Korrigerat problem](../assets/fix.svg) <!-- Issue 612, 613 -->Korrigerade problem där reglage och flera rader som använder parallaxbakgrunder inte återges korrekt efter att helskärmsläget har växlats flera gånger.

![Korrigerat problem](../assets/fix.svg) <!--MC-35220-->Ett problem där det inte gick att spara [!DNL Page Builder] när innehållet skulle kopieras från en rubrikinnehållstyp till en textinnehållstyp har åtgärdats.

![Korrigerat problem](../assets/fix.svg) <!-- MC-34620 -->Korrigerat textinnehållstypen så att icke-latinska 1 tecken kunde hanteras och sparas korrekt.

![Korrigerat problem](../assets/fix.svg) <!-- MC-34679 -->Korrigerade CSS-format [!DNL Page Builder] som gjorde att Safari 13.1 felaktigt återgav Luma-temats webbplatsmeny för små visningsportar och mobila skärmar.

![Korrigerat problem](../assets/fix.svg) <!-- MC-34848 -->Innehållstypen HTML har korrigerats så att inbäddade widgetar som &quot;Order by SKU&quot; på Storefront visas korrekt.

## 1.4.1 för Adobe Commerce 2.4.0-p1

![Nytt](../assets/new.svg) <!-- PB-590 --> Uppgraderat till TinyMCE 4. TinyMCE 3 togs bort för att förbättra säkerheten.

## 1.4.0 för Adobe Commerce 2.4.0

![Nytt](../assets/new.svg) <!-- PB-494 -->Stöd för PHP 7.4 har lagts till.

![Korrigerat problem](../assets/fix.svg) <!-- MC-31247 -->Ett problem där innehållstypen Produkter inte visade konfigurerbara produkter när villkoret var inställt på pris har åtgärdats.

![Korrigerat problem](../assets/fix.svg) <!-- PB-179 -->Konfigurationen för produktjustering har korrigerats så att endast produktbehållaren placerades, inte innehållet i produktbehållaren, som produktnamn, pris, knappar, bilder och andra element.

![Korrigerat problem](../assets/fix.svg) <!-- MC-33556 -->Prestandaförbättringar.

![Åtgärdat problem](../assets/fix.svg) Säkerhetsförbättringar.

## 1.3.3-p1 för Adobe Commerce 2.3.6-p1

![Åtgärdat problem](../assets/fix.svg) Säkerhetsförbättringar.

## 1.3.3 för Adobe Commerce 2.3.6

![Korrigerat problem](../assets/fix.svg) <!-- MC-32766 -->Textinnehållstypen har korrigerats så att variabeldirektiven som lagts till i HTML-attributen sparades korrekt.

![Korrigerat problem](../assets/fix.svg) <!-- MC-34590 -->Korrigerat textinnehållstypen så att icke-latinska 1 tecken kunde hanteras och sparas korrekt.

![Korrigerat problem](../assets/fix.svg) <!-- MC-34677 -->Korrigerade CSS-format [!DNL Page Builder] som gjorde att Safari 13.1 felaktigt återgav Luma-temats webbplatsmeny för små visningsportar och mobila skärmar.

![Korrigerat problem](../assets/fix.svg) <!-- MC-34846 -->Innehållstypen HTML har korrigerats så att inbäddade widgetar som _Order by SKU_ på butiken visas korrekt.

![Korrigerat problem](../assets/fix.svg) Ett fel som ibland gjorde att användare inte kunde spara formulär av innehållstyp har korrigerats. Felet ([!DNL Page Builder] återgav i 5 sekunder utan att frigöra lås) gjorde att inläsarikonen snurrade oavbrutet efter att ett formulär hade sparats.

## 1.3.2 för Adobe Commerce 2.3.5-p2

![Nya](../assets/new.svg) säkerhetsförbättringar.

## 1.3.1 för Adobe Commerce 2.3.5-p1

Den här versionen av [!DNL Page Builder] är bara en versionsnummeruppdatering för Adobe Commerce 2.3.5-p1. Alla funktioner som beskrivs i version 1.3.0 gäller även den här versionen.

## 1.3.0 för Adobe Commerce 2.3.5

![Nytt](../assets/new.svg) **Mallar** - [!DNL Page Builder] har nu mallar som kan skapas från befintligt innehåll och tillämpas på nya innehållsområden. [!DNL Page Builder]-mallar sparar både innehåll och layout för befintliga sidor, block, dynamiska block, produktattribut och kategoribeskrivningar. Du kan till exempel spara en befintlig [!DNL Page Builder] CMS-sida som en mall och sedan använda mallen (med allt innehåll och alla layouter) för att snabbt skapa CMS-sidor för platsen. Den här nya funktionen beskrivs här: [Mallar](templates.md).

![Nytt](../assets/new.svg) **Videobakgrunder för rader, banderoller och reglage** - [!DNL Page Builder] Rader, banderoller och reglage kan nu använda videoklipp för sina bakgrunder. De här nya funktionerna beskrivs här: [Rader](row.md), [Banderoller](banner.md), [Skjutreglage](slider.md).

![Nytt](../assets/new.svg) **Videostöd för tillägg och förbättringar** - [!DNL Page Builder] har nu stöd för fler videoformat. Förutom YouTube- och Vimeo-videofilmer har videoinnehållstypen och videobakgrunder nu stöd för video-URL-länkar till videoformat som `.mp4` och andra format som stöds av webbläsaren. Videoinnehållstypen lägger även till en automatisk uppspelningsfunktion. De här nya funktionerna beskrivs här: [Videoinnehållstyp](video.md).

![Nytt](../assets/new.svg) **Rader, banners och reglage i fullhöjd** - [!DNL Page Builder] Rader, banners och reglage kan nu ange höjden på sidan med en siffra med valfri CSS-enhet (px, %, vh, em) eller en beräkning mellan enheterna (100vh - 237px). De här nya funktionerna beskrivs här: [Rader](row.md), [Banderoller](banner.md), [Skjutreglage](slider.md).

![Nytt](../assets/new.svg) **Uppgraderingsbibliotek för innehållstyp** - Utvecklare kan nu skapa versioner av [!DNL Page Builder] innehållstyper utan att införa bakåtkompatibla problem med tidigare versioner. Före den här versionen skulle betydande ändringar av innehållstypkonfigurationer skapa problem med visning och dataförlust med tidigare sparade [!DNL Page Builder] innehållstyper. Det nya uppgraderingsbiblioteket eliminerar dessa problem. Biblioteket är utformat för att uppgradera tidigare versioner av innehållstyper som sparats i databasen så att de matchar konfigurationsändringarna i de nya versionerna. [!DNL Page Builder] kör uppgraderingsbiblioteket på interna innehållstyper efter behov för en ny version. Den här ändringen säkerställer att de inbyggda [!DNL Page Builder]-innehållstyperna alltid uppgraderas för att matcha ändringar som gjorts i innehållstyper för en senare version.

>[!IMPORTANT]
>
>Om du har skapat ytterligare databasentiteter för lagring av [!DNL Page Builder]-innehåll _måste_ lägga till dessa entiteter i `etc/di.xml`. Om du inte gör det uppdateras inte [!DNL Page Builder]-innehållet som lagras i din entitet, vilket kan orsaka dataförlust och visningsproblem. Om du t.ex. har skapat en bloggenhet som lagrar [!DNL Page Builder]-innehåll måste du lägga till blogginlägget i din `etc/di.xml`-fil som en `UpgradableEntitiesPool`-typ så att uppgraderingsbiblioteket kan uppdatera de [!DNL Page Builder]-innehållstyper som används i bloggen. Mer information och instruktioner om hur du använder uppgraderingsbiblioteket finns i [Uppgradera innehållstyper](https://developer.adobe.com/commerce/frontend-core/page-builder/upgrade-content-types/) i _Utvecklarhandbok för Page Builder_.

![Nytt](../assets/new.svg) **Dokumentation för att lägga till nya utseenden** - Utvecklarinformation har nu publicerats om [att lägga till utseenden](https://developer.adobe.com/commerce/frontend-core/page-builder/content-types/extend/add-appearances/) för befintliga eller anpassade innehållstyper.

![Korrigerat problem](../assets/fix.svg) **Flera korrigeringar**

- &#x200B;<!-- PB-50 -->Ett problem har korrigerats där TinyMCE-menyn för bildinnehåll visas under andra innehållstyper om bildens överordnade behållare är duplicerad.
- &#x200B;<!-- PB-166 -->[!DNL Page Builder] har uppdaterats för att implementera en borttagningsmetod för att förhindra minnesläckor i vissa scenarier.
- &#x200B;<!-- PB-170 -->Förbättrade TinyMCE-prestanda när flera instanser används på Admin-scenen.
- &#x200B;<!-- PB-252 -->Korrigerade ett problem där innehållstypen för dynamiskt block inte återges på adminscenen om den översta raden är markerad som dold.
- &#x200B;<!-- PB-273 -->Förfinade mushovringshändelser på Admin-scenen genom att ta bort en 200 ms fördröjning från olika gränssnittskontroller. Den här ändringen gör det enklare att arbeta med kapslade innehållsobjekt på scenen.
- &#x200B;<!-- PB-294 -->Korrigerade ett problem där valutasymbolen felaktigt undrades i produktlistwidgeten i Block/Dynamic Block på Admin-scenen.
- &#x200B;<!-- PB-296 -->Ett problem har korrigerats där produktsumman på redigeringspanelen [!DNL Page Builder] inte fungerade för anpassade MSI-arkivprodukter.
- &#x200B;<!-- PB-317 -->Ett problem har korrigerats där [!DNL Page Builder]-innehåll med bakgrundsbilder på Microsoft Edge inte återger dessa bilder i butiken.
- &#x200B;<!-- PB-390 -->Korrigerade ett problem där kapslat [!DNL Page Builder]-innehåll inte kunde sparas om användarna klickar på knappen Spara innan sidan återges fullständigt.
- &#x200B;<!-- PB-418 -->Ett undantagsfel som uppstod i cron-jobb på grund av [!DNL Page Builder]-analyser har åtgärdats.

## 1.2.2 för Adobe Commerce 2.3.4-p2

![Nya](../assets/new.svg) säkerhetsförbättringar.

## 1.2.1 för Adobe Commerce 2.3.4-p1

![Nya](../assets/new.svg) säkerhetsförbättringar.

## 1.2.0 för Adobe Commerce 2.3.4

![Ny ](../assets/new.svg) **[!DNL Page Builder]-integrering med PWA Studio** - [!DNL Page Builder] innehållsrendering har lagts till i Venia-appen i PWA Studio. [!DNL Page Builder] innehåll kan nu visas i appen PWA Studio Venia. Mer information om den här nya funktionen finns i [!DNL Page Builder]-dokumentationen i [PWA Studio].

![Nytt](../assets/new.svg) **Lagt till produktkarusell** - <!-- PB-77, PB-173, PB-175 -->Innehållstypen Produkter innehåller nu ett alternativ för att visa dina produkter i karusellformat eller skjutreglage, inklusive flera alternativ för att anpassa karusellen efter dina behov.

![Nytt](../assets/new.svg) **Lagt till produkt-SKU-sortering** - <!-- PB-69 -->Innehållstypen Produkter innehåller nu ett alternativ för att sortera dina produkter efter SKU i den ordning som du lägger till dem i en lista i Admin.

![Ny](../assets/new.svg) **Lagt till produktkategorisortering** - <!-- PB-181 -->. Innehållstypen Produkter har nu ett alternativ för att sortera dina produkter efter kategori _position_ och visa dem i samma ordning som de visas i din Commerce-katalog.

![Nytt](../assets/new.svg) **Produkturvalssummor har lagts till** - <!-- PB-107 -->. I redigeraren för innehållstypen Produkter visas nu det totala antalet produkter som matchar dina produktval.

![Korrigerat problem](../assets/fix.svg) **Flera korrigeringar**

- &#x200B;<!-- PB-237 -->Säkerhetsförbättringar.
- &#x200B;<!-- PB-41 -->Korrigerade sökningar i användargränssnittet för att välja komponenter så att bara en AJAX per sökterm görs.
- &#x200B;<!-- PB-76, PB-84-->Uppdaterade produktförhandsvisningar i Admin för att matcha butiken, inklusive produktstjärngradering, färg och storleksalternativ när det är relevant.
- &#x200B;<!-- PB-169 -->Korrigerade ett problem där [!DNL Page Builder] inte kunde sparas när JavaScript minification and bundling är aktiverat i Commerce.
- &#x200B;<!-- PB-241 -->Korrigerade administratörsförhandsgranskningarna av Produkter, Block och Dynamic Blocks för korrekt rendering på Commerce-installationer som definierar olika URL:er för Admin och frontend.
- &#x200B;<!-- PB-238 -->Korrigerade administratörsförhandsgranskningarna av Produkter, Block och Dynamic Blocks så att de återges korrekt på Commerce-installationer med B2B installerat med alternativet _Endast inloggning_ aktiverat. Före den här korrigeringen skulle förhandsgranskningen [!DNL Page Builder] göra att sidan dirigeras om till kundkontoinloggningen.
- &#x200B;<!-- PB-239 -->Ett sessionsfel som kan uppstå vid förhandsgranskning av en stor sida i [!DNL Page Builder]-administratören har korrigerats.
- &#x200B;<!-- PB-248 -->[!DNL Page Builder] LESS-format har uppdaterats för att förhindra dubblering av storefront-format.

## 1.1.1 för Adobe Commerce 2.3.3-p1

![Nya](../assets/new.svg) säkerhetsförbättringar.

## 1.1.0 för Adobe Commerce 2.3.3

![Nytt](../assets/new.svg) <!-- MC-15250 -->En explicit produktsortering har lagts till i innehållstypen Produkter.

![Nytt](../assets/new.svg) <!-- MC-17823 -->Knappar har lagts till för att infoga bilder, widgetar och variabler i innehållstypen HTML.

![Korrigerat problem](../assets/fix.svg) Förbättrad [!DNL Page Builder] säkerhet.

![Korrigerat problem](../assets/fix.svg) <!-- MC-1805 -->Uppdaterat [!DNL Page Builder] med stöd för PHP-version 7.3.

![Korrigerat problem](../assets/fix.svg) <!-- MC-4137 -->TinyMCE har uppdaterats till version 4.9.5. Uppdateringen, tillsammans med de ytterligare förbättringarna, åtgärdade flera TinyMCE inline-redigeringsproblem:

- Variabler, bilder och bildlänkar läggs till där markören är placerad.
- Tabeller och tabellceller kan centreras.
- Kopiera/klistra in klistrar nu in innehåll vid markörens position.
- Länkar kan användas på markerad text.
- Punkter justeras korrekt.
- Du kan spara ändringar i den infogade redigeraren utan att först klicka utanför redigeraren.

![Korrigerat problem](../assets/fix.svg) <!-- MC-3880 -->Ett problem där den minsta höjden och den lodräta justeringen inte stämde överens mellan avsnitten på redigeringspanelen för varje innehållstyp har korrigerats.

![Korrigerat problem](../assets/fix.svg) <!-- MC-14994 -->Ett problem där verktygsfältet från rubrikens innehållstyp placerades felaktigt när det först släpptes på scenen har åtgärdats.

![Korrigerat problem](../assets/fix.svg) <!-- MC-15742 -->Fast hårdkodade marginaler i både Slider- och Video-innehållstyper har åtgärdats.

![Korrigerat problem](../assets/fix.svg) <!-- MC-16241 -->Ett problem där den nödvändiga asterisksymbolen visades två gånger i formulärfält har åtgärdats.

## 1.0.3 för Adobe Commerce 2.3.2-p2

![Nya](../assets/new.svg) säkerhetsförbättringar.

## 1.0.2 för Adobe Commerce 2.3.2-p1

![Nya](../assets/new.svg) säkerhetsförbättringar.

## 1.0.1 för Adobe Commerce 2.3.2

![Nytt](../assets/new.svg) Säkerställer kompatibilitet med Adobe Commerce 2.3.2.

## 1.0.0 för Adobe Commerce 2.3.1

![Ny](../assets/new.svg) allmän tillgänglighetsrelease


[PWA Studio]: https://developer.adobe.com/commerce/pwa-studio/
