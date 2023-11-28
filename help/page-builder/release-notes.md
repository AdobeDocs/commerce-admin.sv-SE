---
title: Versionsinformation för [!DNL Page Builder]
description: Läs versionsinformationen om du vill ha information om alla [!DNL Page Builder] releaser.
exl-id: 81abe2f9-ed48-49fe-bbf0-70699d7106b2
feature: Page Builder, Release Notes
source-git-commit: addc34aeb4418aa3a1a9c2fc3adca738352ef94f
workflow-type: tm+mt
source-wordcount: '2747'
ht-degree: 0%

---

# Versionsinformation för [!DNL Page Builder]

Versionsinformationen beskriver releaser av [!DNL Page Builder] och innehåller:

![Nytt](../assets/new.svg) Nya funktioner

![Korrigerat problem](../assets/fix.svg) Korrigeringar och förbättringar

![Känt fel](../assets/bug.svg) Kända fel

>[!IMPORTANT]
>
>Från och med version 2.4.3, [!DNL Page Builder] finns nu som pakettillägg i Magento Open Source. Det är nu standardverktyget för innehållsredigering för både Adobe Commerce och Magento Open Source och kan ersätta WYSIWG-redigeraren med en tredjepartsmodul.

## 1.7.2 för Commerce 2.4.5

![Nytt](../assets/new.svg) **Ny wrapper-entitet - [!DNL Columns] behållare som introducerats för kolumnlayouter** - Tidigare kunde användare bara lägga till kolumner i en annan behållare/wrapper-innehållstyp, till exempel en [!DNL Tab] eller [!DNL Row]. Nu [!DNL Column] har en egen wrapper och kan läggas till direkt på scenen. Dessutom finns [!DNL Columns] behållaren har ett inställningselement där användare kan ange konfiguration för den här wrapper-entiteten.<!--- PB-500-->

![Nytt](../assets/new.svg) **Nya menyalternativ för att duplicera, dölja och ta bort kolumngrupper** - Med dessa nya alternativ kan användare duplicera, dölja och ta bort [!DNL Columns] grupper - precis som de kan med innehållstyper.<!--- PB-507-->

![Nytt](../assets/new.svg) <!-- Issue 594 -->**Nytt stöd för flera kolumner har lagts till i kolumngruppen** - Med det här tillägget kan användare ändra flera rader med kolumner inuti en [!DNL Columns] för att göra kolumnlayouterna mycket mer flexibla.<!--- PB-108-->

Se [Layout - kolumn](./column.md) för information om hur du använder nya [!DNL Columns] grupp.

## 1.7.1 för Commerce 2.4.4

![Korrigerat problem](../assets/fix.svg) Page Builder är nu kompatibelt med PHP 8.1.<!--- AC-1300-->

![Korrigerat problem](../assets/fix.svg) Handlare kan nu lägga till alternativ text (`alt_text`) till bilder (Bild, Banner, Slide) för att förbättra innehållets tillgänglighet.<!--- PB-1193-->

![Korrigerat problem](../assets/fix.svg) Administratörsanvändare med begränsade behörigheter för att endast redigera innehåll ser inte längre ett fel när Page Builder används för att lägga till en produktwidget på en CMS-sida. I Page Builder visas även ett korrekt produktantal på sidan med widgetinställningar. Tidigare krävde Page Builder behörighet till katalogmodulen vid hämtning av produktantal och det här felet visades: `A technical problem with the server created an error. Try again to continue what you were doing. If the problem persists, try again later`. <!--- MC-42779-->

![Korrigerat problem](../assets/fix.svg) Visningsproblem med formatmenyn i Page Builder har lösts med biblioteksuppgraderingen TinyMCE 5. <!--- AC-446-->

![Korrigerat problem](../assets/fix.svg) Nu kan du använda musen för att redigera en **Text som ska visas** i popup-fönstret Infoga länk. <!--- AC-982-->

![Korrigerat problem](../assets/fix.svg) I Page Builder visas nu alla alternativ som förväntat på alternativmenyn Teckenstorlek. Tidigare visades inte alla alternativ. <!--- AC-1056-->

![Korrigerat problem](../assets/fix.svg) Uppgraderade `phpgt/dom` Dispositionsberoende för `magento/magento2-page-builder` till de senaste versionerna. <!--- magento/magento2-page-builder/pull/779-->

![Korrigerat problem](../assets/fix.svg) Page Builder ändrar inte längre storlek på dialogrutorna Infoga länk och Infoga bild när skjutreglaget visas i en liten kolumn. <!--- AC-973-->

![Korrigerat problem](../assets/fix.svg) Menyn Tabellegenskaper i Page Builder visas nu som förväntat. <!--- AC-407-->

![Korrigerat problem](../assets/fix.svg) Skjutreglage visas inte längre på länken Infoga eller bilden modal när musen inte hovrar över skjutreglaget. <!--- AC-406-->

![Korrigerat problem](../assets/fix.svg) Teckensnittsstorleken som används för att visa menyalternativen för Tabell har optimerats. <!--- AC-396-->

![Korrigerat problem](../assets/fix.svg) Avvikelser har korrigerats med placeringen av dialogrutorna Infoga/Redigera bild och Infoga/redigera länk. <!--- AC-397-->

![Korrigerat problem](../assets/fix.svg) Page Builder genererar inte längre något fel när du klickar på **Textredigerare** för en banner. <!--- AC-398-->

![Korrigerat problem](../assets/fix.svg) Page Builder konverterar inte längre alla dynamiska block till ett språk under uppgraderingen. <!--- MC-42265-->

## 1.6.0 för Adobe Commerce 2.4.2

![Nytt](../assets/new.svg) <!-- Issue 558 -->**Nytt [!DNL Page Builder] formatera** - [!DNL Page Builder] har gjort stora förbättringar i hur innehållet formateras. Ändringarna gör det nu enkelt att skapa enkla CSS-väljare som åsidosätter de befintliga innehållstypsformaten. Dessa ändringar gör det möjligt att skapa [!DNL Page Builder] teman med stor lyhördhet för alla innehållstyper.

![Nytt](../assets/new.svg) <!-- Issue 429 -->**Radbehållare är nu valfritt** - Nu kan du skapa innehåll i [!DNL Page Builder] utan att kräva en radbehållare. Förutom raden kan följande innehållstyper nu dras och släppas direkt på scenen: HTML, Block, Dynamiskt block, Kolumner och Tabbar.

![Nytt](../assets/new.svg) <!-- Issue 636 -->**Ny responsiv visningsportväljare** - Nu kan du förhandsgranska [!DNL Page Builder] innehåll med olika enhetsbredder (brytpunkter) med hjälp av de nya knapparna för visningsväljaren för administratörer ovanför scenen. Visningsväljaren simulerar hur innehållet är formaterat när det visas på butiken med olika enheter.

![Nytt](../assets/new.svg) <!-- Issue 637 -->**Nya brytpunktsspecifika formulärfält** - Värden för innehållstypfält kan nu ställas in på specifika brytpunkter för visningsruta. Ikonindikatorerna bredvid fälten visar visningsrutan som innehållstypens fältvärde används för.

![Nytt](../assets/new.svg) <!-- Issue 559 -->**Borttagna fördefinierade formulärfältsposter** - Avancerade formulärinställningar för marginaler, utfyllnad och kantrelaterade egenskaper (kantlinje, kantbredd och kantradie) har nu angetts som `default`så att värden kan definieras med en moduls CSS.

![Nytt](../assets/new.svg) <!-- Issue 635, 557,  -->**Lagt till mellanrum på scenen** - Rader och kolumner ger nu extra utrymme runt innehållstyper på scenen, men inte på butiken. Det extra mellanrummet gör det enklare att komma åt alternativmenyerna för muspekaren för både behållaren och innehållstyperna.

![Korrigerat problem](../assets/fix.svg) <!-- MC-37348 -->**Korrigerad automatisk rullning till granskningar** - Automatisk rullning till produktrecensioner i butiken är nu fast.

![Korrigerat problem](../assets/fix.svg) <!-- MC-36227 -->**Fast beskuret innehåll** - Längda beskrivningar av kategorier och produkter beskärs inte längre.

![Korrigerat problem](../assets/fix.svg) <!-- MC-35402 -->**Kategoriinnehåll med full bredd och utfall har åtgärdats** - Kategoriinnehåll kan nu visas i en layout med full bredd eller helt utfall.

![Korrigerat problem](../assets/fix.svg) <!-- MC-37989 -->**Säkerhetsförbättringar**

## 1.5.1 för Adobe Commerce 2.4.1-p1

![Korrigerat problem](../assets/fix.svg) <!-- PB-1140, MC-38812 -->**Felvisning** - Korrigerade ett problem där [!DNL Page Builder] visade ett fel när katalogunderkategorier lades till i Admin.

## 1.5.0 för Adobe Commerce 2.4.1

![Nytt](../assets/new.svg) <!-- Issue 510, 511, 512, 513 -->**Immersiv helskärmsredigering** - Redigering [!DNL Page Builder] innehåll visas nu endast i helskärmsläge för alla områden som styrs av [!DNL Page Builder]. Den här ändringen omfattar CMS-sidor, produkt- och kategorisidor, block och dynamiska block. Vid helskärmsredigering fokuseras ditt innehåll och ger en vy som bättre matchar användarupplevelsen i butiken.

![Nytt](../assets/new.svg) <!-- Issue 544 -->**[!DNL Page Builder] förhandsgranskning av innehåll **- Som standard [!DNL Page Builder] innehåller nu förhandsgranskningar av innehåll inte bara för CMS-sidor, block och dynamiska block, utan även för produkt- och kategorisidor. Du kan konfigurera den här funktionen så att den är aktiverad eller inaktiverad för produkt- och kategorisidor med hjälp av den nya [!DNL Page Builder] Inställningen Förhandsvisa innehåll, som du kommer åt i butikskonfigurationen på Content Management > Advanced Content Tools.

![Nytt](../assets/new.svg) <!-- Issue 543 -->**Förbättrad åtkomst till korta produktbeskrivningar** - Som standard visas nu en kort produktbeskrivning före den längre beskrivningen. Ändringen matchar den ordning som de visas i butiken och förhindrar att det längre beskrivningsinnehållet behöver bläddras igenom för att komma åt den korta beskrivningen.

![Nytt](../assets/new.svg) <!-- Issue 419 -->**Förhindrade kapslade länkar i banners och bilder** - Om du lägger till länkar till både innehållet och de yttre elementen i Banners och Slides skapades kapslade länkar som inte visades eller betedde sig korrekt i butiken. Det går inte längre att lägga till länkar för att lösa problemet *båda* området Meddelandetext och attributet Länk för banners och Presentationer.

![Korrigerat problem](../assets/fix.svg) <!-- Issue 421 --> Ett problem har korrigerats där en tom kantradie på ett flikobjekt orsakade fel och hade skadat flikobjektsinnehåll.

![Korrigerat problem](../assets/fix.svg) <!-- Issue 422 --> Ett problem har korrigerats där tillägg av vissa kombinationer av villkor till filtret för produktvillkor orsakade fel som gjorde att produktformuläret inte kunde sparas.

![Korrigerat problem](../assets/fix.svg) <!-- Issue 425 -->Ett problem som innebar att Slider-innehållstypen inte betedde sig korrekt när inställningen Oändlig loop inaktiverades har åtgärdats.

![Korrigerat problem](../assets/fix.svg) <!-- Issue 426 -->Korrigerat det lägsta kampanjpriset så att det nu fungerar i [!DNL Page Builder].

![Korrigerat problem](../assets/fix.svg) <!-- Issue 436 -->Korrigerade problemet i Safari och IE 11 som förhindrade att en bild drog och släpptes till överföringsområdet i Banners and Slides.

![Korrigerat problem](../assets/fix.svg) <!-- Issue 525 -->Korrigerade problemet där Slider-innehållstypen inte svarade i Firefox.

![Korrigerat problem](../assets/fix.svg) <!-- Issue 567 -->Korrigerade problemet där widgetkonfigurationen skapade felaktiga väljare i DOM för de olika utseendena.

![Korrigerat problem](../assets/fix.svg) <!-- Issue 609 -->Korrigerade problemet med att verktygsfältet Sidhuvud gömde innehållstypens alternativmeny, vilket förhindrade åtkomst till formuläret och andra alternativ.

![Korrigerat problem](../assets/fix.svg) <!-- Issue 612, 613 -->Korrigerade problem där reglage och flera rader som använder parallaxbakgrunder inte återges korrekt efter att helskärmsläget har växlats flera gånger.

![Korrigerat problem](../assets/fix.svg) <!--MC-35220-->Ett problem där det inte gick att kopiera innehållet från en rubrikinnehållstyp till en textinnehållstyp har åtgärdats [!DNL Page Builder] från att spara.

![Korrigerat problem](../assets/fix.svg) <!-- MC-34620 -->Korrigerade textinnehållstypen för att hantera och spara icke-latinska 1-tecken korrekt.

![Korrigerat problem](../assets/fix.svg) <!-- MC-34679 -->Fast [!DNL Page Builder] CSS-format som fick Safari 13.1 att felaktigt återge Luma-temats platsmeny för portar för små vyer och mobila skärmar.

![Korrigerat problem](../assets/fix.svg) <!-- MC-34848 -->Korrigerade innehållstypen HTML för att visa inbäddade widgetar som&quot;Order by SKU&quot; korrekt på Storefront.

## 1.4.1 för Adobe Commerce 2.4.0-p1

![Nytt](../assets/new.svg) <!-- PB-590 --> Uppgraderat till TinyMCE 4. TinyMCE 3 togs bort för att förbättra säkerheten.

## 1.4.0 för Adobe Commerce 2.4.0

![Nytt](../assets/new.svg) <!-- PB-494 -->Stöd för PHP 7.4 har lagts till.

![Korrigerat problem](../assets/fix.svg) <!-- MC-31247 -->Ett problem har korrigerats där innehållstypen Produkter inte visade konfigurerbara produkter när villkoret var inställt på pris.

![Korrigerat problem](../assets/fix.svg) <!-- PB-179 -->Korrigerade justeringskonfigurationen för produkter så att endast produktbehållaren placeras, inte innehållet i produktbehållaren, som produktnamn, pris, knappar, bilder och andra element.

![Korrigerat problem](../assets/fix.svg) <!-- MC-33556 -->Prestandaförbättringar.

![Korrigerat problem](../assets/fix.svg) Säkerhetsförbättringar.

## 1.3.3-p1 för Adobe Commerce 2.3.6-p1

![Korrigerat problem](../assets/fix.svg) Säkerhetsförbättringar.

## 1.3.3 för Adobe Commerce 2.3.6

![Korrigerat problem](../assets/fix.svg) <!-- MC-32766 -->Korrigerade textinnehållstypen så att variabeldirektiven som lagts till i html-attributen sparades korrekt.

![Korrigerat problem](../assets/fix.svg) <!-- MC-34590 -->Korrigerade textinnehållstypen för att hantera och spara icke-latinska 1-tecken korrekt.

![Korrigerat problem](../assets/fix.svg) <!-- MC-34677 -->Fast [!DNL Page Builder] CSS-format som fick Safari 13.1 att felaktigt återge Luma-temats platsmeny för portar för små vyer och mobila skärmar.

![Korrigerat problem](../assets/fix.svg) <!-- MC-34846 -->Korrigerade innehållstypen för HTML så att inbäddade widgetar som _Beställa efter SKU_ på butiken.

![Korrigerat problem](../assets/fix.svg) Korrigerade ett fel som ibland gjorde att användare inte kunde spara formulär av innehållstyp. Felet (&quot;[!DNL Page Builder] återgivning i 5 sekunder utan att frigöra lås&quot;) fick inläsarikonen att snurra oavbrutet efter att ha försökt spara ett formulär.

## 1.3.2 för Adobe Commerce 2.3.5-p2

![Nytt](../assets/new.svg) Säkerhetsförbättringar.

## 1.3.1 för Adobe Commerce 2.3.5-p1

Den här versionen av [!DNL Page Builder] är bara en versionsnummeruppdatering för Adobe Commerce 2.3.5-p1. Alla funktioner som beskrivs i version 1.3.0 gäller även den här versionen.

## 1.3.0 för Adobe Commerce 2.3.5

![Nytt](../assets/new.svg) **Mallar** - [!DNL Page Builder] har nu mallar som kan skapas från befintligt innehåll och tillämpas på nya innehållsområden. [!DNL Page Builder] -mallar sparar både innehåll och layout för befintliga sidor, block, dynamiska block, produktattribut och kategoribeskrivningar. Du kan t.ex. spara en befintlig [!DNL Page Builder] CMS-sida som mall och använd sedan mallen (med allt innehåll och alla layouter) för att snabbt skapa CMS-sidor för webbplatsen. Den här nya funktionen beskrivs här: [Mallar](templates.md).

![Nytt](../assets/new.svg) **Videobakgrunder för rader, banderoller och reglage** - [!DNL Page Builder] Nu kan rader, banderoller och reglage använda videoklipp för sina bakgrunder. Dessa nya funktioner beskrivs här: [Rader](row.md), [Banderoller](banner.md), [Skjutreglage](slider.md).

![Nytt](../assets/new.svg) **Videostöd - tillägg och förbättringar** - [!DNL Page Builder] har nu stöd för fler videoformat. Förutom YouTube- och Vimeo-videor har videoinnehållstypen och videobakgrunder nu stöd för video-URL-länkar till videoformat som `.mp4` och andra format som stöds av webbläsaren. Videoinnehållstypen lägger även till en automatisk uppspelningsfunktion. Dessa nya funktioner beskrivs här: [Videoinnehållstyp](video.md).

![Nytt](../assets/new.svg) **Rader, banners och reglage i fullhöjd** - [!DNL Page Builder] Rader, banderoller och reglage kan nu ange sina höjder till hela sidhöjden med ett tal med valfri CSS-enhet (px, %, vh, em) eller en beräkning mellan enheterna (100vh - 237px). Dessa nya funktioner beskrivs här: [Rader](row.md), [Banderoller](banner.md), [Skjutreglage](slider.md).

![Nytt](../assets/new.svg) **Uppgraderingsbibliotek för innehållstyp** - Utvecklare kan nu skapa versioner av [!DNL Page Builder] innehållstyper utan att införa bakåtkompatibla problem med tidigare versioner. Före den här versionen skulle betydande ändringar av innehållstypkonfigurationer skapa problem med visning och dataförlust med tidigare sparade [!DNL Page Builder] innehållstyper. Det nya uppgraderingsbiblioteket eliminerar dessa problem. Biblioteket är utformat för att uppgradera tidigare versioner av innehållstyper som sparats i databasen så att de matchar konfigurationsändringarna i de nya versionerna. [!DNL Page Builder] kör uppgraderingsbiblioteket på interna innehållstyper efter behov för en ny version. Den här ändringen säkerställer att den inbyggda [!DNL Page Builder] innehållstyper uppgraderas alltid för att matcha ändringar som gjorts i innehållstyper för en senare version.

>[!IMPORTANT]
>
>Om du har skapat ytterligare databasenheter för lagring [!DNL Page Builder] innehåll, _måste_ lägga till dessa enheter i `etc/di.xml`. Om du inte gör det, [!DNL Page Builder] innehåll som lagras i din enhet uppdateras inte, vilket kan orsaka dataförlust och visningsproblem. Om du t.ex. har skapat en bloggenhet som lagrar [!DNL Page Builder] innehåll måste du lägga till din bloggenhet i `etc/di.xml` fil som `UpgradableEntitiesPool` så att uppgraderingsbiblioteket kan uppdatera [!DNL Page Builder] innehållstyper som används i bloggen. Mer information och instruktioner om hur du använder uppgraderingsbiblioteket finns i [Uppgradera innehållstyper](https://developer.adobe.com/commerce/frontend-core/page-builder/upgrade-content-types/) i _Utvecklarhandbok för Page Builder_.

![Nytt](../assets/new.svg) **Dokumentation för att lägga till nya utseenden** - Utvecklarinformation som nu publiceras om [lägga till utseenden](https://developer.adobe.com/commerce/frontend-core/page-builder/content-types/extend/add-appearances/) för befintliga eller anpassade innehållstyper.

![Korrigerat problem](../assets/fix.svg) **Olika korrigeringar**

- <!-- PB-50 -->Ett problem har korrigerats där TinyMCE-menyn för bildinnehåll visas under andra innehållstyper om bildens överordnade behållare är duplicerad.
- <!-- PB-166 -->Uppdaterat [!DNL Page Builder] för att implementera en destruktionsmetod för att förhindra minnesläckor i vissa scenarier.
- <!-- PB-170 -->Förbättrade TinyMCE-prestanda när flera instanser används på Admin-scenen.
- <!-- PB-252 -->Korrigerade ett problem där innehållstypen för dynamiskt block inte återges på adminscenen om den översta raden är markerad som dold.
- <!-- PB-273 -->Förfinade mushovringshändelser på Admin-scenen genom att ta bort en 200 ms fördröjning från olika gränssnittskontroller. Den här ändringen gör det enklare att arbeta med kapslade innehållsobjekt på scenen.
- <!-- PB-294 -->Korrigerade ett problem där valutasymbolen felaktigt undrades i produktlistwidgeten i Block/Dynamic Block på Admin-scenen.
- <!-- PB-296 -->Ett problem där produktsumman på [!DNL Page Builder] redigeringspanelen fungerade inte för anpassade MSI-arkivprodukter.
- <!-- PB-317 -->Ett problem där sparandet korrigerades [!DNL Page Builder] innehåll med bakgrundsbilder på Microsoft Edge inte återger dessa bilder på butiken.
- <!-- PB-390 -->Ett problem som kapslades har korrigerats [!DNL Page Builder] det går inte att spara om användarna klickar på knappen Spara innan sidan återges fullständigt.
- <!-- PB-418 -->Ett undantagsfel som genererades i cron-jobb på grund av [!DNL Page Builder] analys.

## 1.2.2 för Adobe Commerce 2.3.4-p2

![Nytt](../assets/new.svg) Säkerhetsförbättringar.

## 1.2.1 för Adobe Commerce 2.3.4-p1

![Nytt](../assets/new.svg) Säkerhetsförbättringar.

## 1.2.0 för Adobe Commerce 2.3.4

![Nytt](../assets/new.svg)  **[!DNL Page Builder]integrering med PWA Studio** - Tillagt [!DNL Page Builder] Innehållsåtergivning till appen Venia i PWA Studio. [!DNL Page Builder] Nu kan du visa innehåll i appen PWA Studio Venia. Se [!DNL Page Builder] dokumentation inom [PWA Studio] för all information om den här nya funktionen.

![Nytt](../assets/new.svg) **Tillagd produktkarusell** - <!-- PB-77, PB-173, PB-175 -->Innehållstypen Produkter erbjuder nu ett alternativ för att visa dina produkter i karusellformat eller skjutreglage, inklusive flera alternativ för att anpassa karusellen efter dina behov.

![Nytt](../assets/new.svg) **Lagt till produktsortering** - <!-- PB-69 -->Innehållstypen Produkter erbjuder nu ett alternativ för att sortera dina produkter efter SKU i den ordning du lägger till dem i en lista i Admin.

![Nytt](../assets/new.svg) **Lagt till sortering av produktkategori** - <!-- PB-181 -->. Innehållstypen Produkter har nu ett alternativ för att sortera dina produkter efter kategori _position_, som visar dem i samma ordning som de visas i din Commerce Catalog.

![Nytt](../assets/new.svg) **Tillagda summor för produkturval** - <!-- PB-107 -->. I redigeraren för innehållstypen Produkter visas nu det totala antalet produkter som matchar dina produktval.

![Korrigerat problem](../assets/fix.svg) **Olika korrigeringar**

- <!-- PB-237 -->Säkerhetsförbättringar.
- <!-- PB-41 -->Korrigerade sökningar i användargränssnittet för att välja komponenter så att bara en AJAX per sökterm görs.
- <!-- PB-76, PB-84-->Uppdaterade produktförhandsvisningar i Admin för att matcha butiken, inklusive produktstjärngradering, färg och storleksalternativ när det är relevant.
- <!-- PB-169 -->Ett problem där [!DNL Page Builder] kunde inte sparas när JavaScript-miniatyrbilder och -paketering är aktiverat i Commerce.
- <!-- PB-241 -->Korrigerade administratörsförhandsgranskningar av produkter, block och dynamiska block för korrekt rendering i Commerce-installationer som definierar olika URL:er för administratören och frontend.
- <!-- PB-238 -->Korrigerade administratörsförhandsgranskningar av produkter, block och dynamiska block för korrekt rendering i Commerce-installationer där B2B installerats med _Endast inloggning_ aktiverat alternativ. Innan den här korrigeringen [!DNL Page Builder] förhandsgranskning kan leda till att sidan dirigeras om till kundkontoinloggningen.
- <!-- PB-239 -->Ett sessionsfel som kan inträffa vid förhandsgranskning av en stor sida i [!DNL Page Builder] Admin.
- <!-- PB-248 -->Uppdaterat [!DNL Page Builder] LESS-format för att förhindra dubblering av format i bakgrunden.

## 1.1.1 för Adobe Commerce 2.3.3-p1

![Nytt](../assets/new.svg) Säkerhetsförbättringar.

## 1.1.0 för Adobe Commerce 2.3.3

![Nytt](../assets/new.svg) <!-- MC-15250 -->Lagt till explicit produktsortering till innehållstypen Produkter.

![Nytt](../assets/new.svg) <!-- MC-17823 -->Knappar har lagts till för att infoga bilder, widgetar och variabler i innehållstypen HTML.

![Korrigerat problem](../assets/fix.svg) Förbättrat [!DNL Page Builder] säkerhet.

![Korrigerat problem](../assets/fix.svg) <!-- MC-1805 -->Uppdaterat [!DNL Page Builder] som stöd för PHP version 7.3.

![Korrigerat problem](../assets/fix.svg) <!-- MC-4137 -->TinyMCE uppdaterade till version 4.9.5. Uppdateringen, tillsammans med de ytterligare förbättringarna, åtgärdade flera TinyMCE inline-redigeringsproblem:

- Variabler, bilder och bildlänkar läggs till där markören är placerad.
- Tabeller och tabellceller kan centreras.
- Kopiera/klistra in klistrar nu in innehåll vid markörens position.
- Länkar kan användas på markerad text.
- Punkter justeras korrekt.
- Du kan spara ändringar i den infogade redigeraren utan att först klicka utanför redigeraren.

![Korrigerat problem](../assets/fix.svg) <!-- MC-3880 -->Ett problem där den minsta höjden och den lodräta justeringen inte stämde överens mellan avsnitt på redigeringspanelen för varje innehållstyp har åtgärdats.

![Korrigerat problem](../assets/fix.svg) <!-- MC-14994 -->Ett problem där verktygsfältet från rubrikens innehållstyp placerades felaktigt när det först släpptes på scenen har åtgärdats.

![Korrigerat problem](../assets/fix.svg) <!-- MC-15742 -->Fasta hårdkodade marginaler i både Slider- och Video-innehållstyper.

![Korrigerat problem](../assets/fix.svg) <!-- MC-16241 -->Ett problem där den nödvändiga asterisksymbolen visades två gånger i formulärfält har korrigerats.

## 1.0.3 för Adobe Commerce 2.3.2-p2

![Nytt](../assets/new.svg) Säkerhetsförbättringar.

## 1.0.2 för Adobe Commerce 2.3.2-p1

![Nytt](../assets/new.svg) Säkerhetsförbättringar.

## 1.0.1 för Adobe Commerce 2.3.2

![Nytt](../assets/new.svg) Garanterar kompatibilitet med Adobe Commerce 2.3.2.

## 1.0.0 för Adobe Commerce 2.3.1

![Nytt](../assets/new.svg) Allmän tillgänglighetsrelease


[PWA Studio]: https://developer.adobe.com/commerce/pwa-studio/
