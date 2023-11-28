---
title: HIPAA-beredskap på Adobe Commerce
description: Lär dig hur du kan lägga till Adobe Commerce HIPAA-Ready-modulen och få ytterligare funktioner som gör att du kan uppfylla dina HIPAA-skyldigheter.
feature: Security, Compliance
hide: true
hidefromtoc: true
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 10b01db562777ef2fcc224177d7a83c0a6fc90e7
workflow-type: tm+mt
source-wordcount: '1472'
ht-degree: 0%

---

# HIPAA-beredskap på Adobe Commerce

>[!IMPORTANT]
>
>**Juridisk ansvarsfriskrivning**<br/>
>Den här informationen är avsedd att hjälpa Adobe-kunder att besvara sina frågor om Adobe HIPAA-Ready Services. Den utgör inte juridisk rådgivning. Handlarna bör samråda med sitt eget juridiska ombud för att förstå sina skyldigheter enligt HIPAA och hur Adobe produkter används och konfigureras på lämpligt sätt.

## HIPAA (Health Insurance Portability and Accounability Act)

HIPAA (Health Insurance Portability and Accounability Act) är den viktigaste federala hälso- och sjukvårdslagstiftningen i USA och regleras av USA:s Department of Health and Human Services (HHS). HIPAA gäller för _Berörda enheter_ (t.ex. vårdgivare, försäkringsbolag och clearingorganisationer) och _Business Associates_ (t.ex. enheter som tillhandahåller tjänster till enheter som omfattas). HIPAA-kraven anges i tre separata regler: sekretessregel, säkerhetsregel och regel för meddelanden om överträdelser. Adobe fungerar som Business Associate för vissa produkter, som Adobe klassificerar som&quot;HIPAA-Ready Services&quot;. Uppgifter som regleras enligt HIPAA kallas _Skyddad hälsoinformation_ eller PHI. PHI är en delmängd av hälsoinformation som (1) skapas eller tas emot av en vårdgivare, en hälsoplan eller en vårdcentral, (2) avser en individs tidigare, nuvarande eller framtida fysiska eller psykiska hälsa eller tillstånd, tillhandahållande av hälso- och sjukvård till en individ eller tidigare, nuvarande eller framtida betalning för tillhandahållande av hälso- och sjukvård till en individ, och (3) identifierar den individ eller med avseende på vilken det finns en rimlig grund att tro informationen kan användas för att identifiera den enskilda personen. HIPAA:s sekretess- och säkerhetsregler kräver att en enhet som omfattas erhåller skriftliga garantier från en Business Associate i form av ett Business Associate-avtal, eller BAA, som kräver att Business Associate ska skydda integriteten och säkerheten för de berörda enheternas PHI.

## Adobe Commerce HIPAA-Ready

Adobe Commerce HIPAA-Ready har ytterligare funktioner som gör att handlare kan uppfylla sina respektive HIPAA-skyldigheter. Du kan installera Adobe Commerce HIPAA-Ready (`magento/hipaa-ee`) till din Adobe Commerce om molninfrastruktur. Det finns också vissa funktioner som måste inaktiveras för att vara kompatibla med HIPAA.

*Dessa material är endast avsedda som information. Tillhandahållande av denna information berättigar inte mottagaren till några avtalsmässiga eller andra rättigheter. Även om det har gjorts ansträngningar för att säkerställa att uppgifterna är korrekta från och med den dag då de tillhandahölls, finns det inga belägg för att dessa uppgifter är korrekta och fullständiga, och Adobe förbinder sig inte att uppdatera dessa uppgifter när lagen eller Adobe ändras. Dokumentet får inte heller distribueras till någon annan part än den avsedda mottagaren utan skriftligt medgivande från Adobe.*

## Systemkrav

HIPAA-beredskap för Adobe Commerce har samma systemkrav som Adobe Commerce med ytterligare krav:

- Adobe Commerce version 2.4.6-p3 eller senare (ej beta)
- Adobe Commerce i molninfrastruktur eller Adobe Commerce i Managed Services
- Senaste versionen av `magento/hipaa-ee` extension

## Installation

Adobe HIPAA-Ready Services är tekniskt sett ett kompositmetapaket `magento/hipaa-ee` som innehåller länkar till särskilda moduler. Det här metapaketet finns i databasen [repo.magento.com](https://repo.magento.com).

1. För installation `magento/hipaa-ee` metapackage, du måste ha tillgång till det. För nyckelgenerering och erhållande av nödvändiga rättigheter, se [Hämta dina autentiseringsnycklar](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html?lang=en).

1. Kontrollera miljön där du ska installera paketet och se till att det uppfyller de allmänna kraven [systemkrav](#system-requirements).

1. Lägg till metapaketet `magento/hipaa-ee` till dispositionskonfigurationen.

   Det enklaste sättet är att använda dispositionsverktyget CLI. Exempel:

   ```shell
   composer require magento/hipaa-ee
   ```

1. Om Adobe Commerce inte är installerat ännu kan du starta installationen (följ [Installationsanvisningar](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html?lang=en)).

   Om Adobe Commerce redan är installerat kan du köra `bin/magento setup:upgrade` och följ sedan rekommendationerna.

   ```shell
   bin/magento setup:upgrade
   ```

   När det här kommandot körs aktiveras de nyligen hämtade modulerna och de skript som behövs för att installera dem startas. Mer information om modulhantering finns i [Aktivera eller inaktivera moduler](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=en).

1. När installationen eller uppdateringen är klar bör du kontrollera om `Hipaa*` relevanta moduler har inkluderats.

   Kör kommandot:

   ```shell
   bin/magento module:status
   ```

   Om HIPAA-dispositionspaketet lades till korrekt visas HIPAA-modulerna i utdata från kommandot. Exempel:

   ```text
   List of enabled modules:
   <truncated for brevity>
   Magento_HipaaAnalytics
   Magento_HipaaCheckout
   Magento_HipaaLogging
   Magento_HipaaScheduledImportExport
   Magento_HipaaAdminLogging
   Magento_HipaaCustomerLogging
   Magento_HipaaNewsletter
   Magento_HipaaImportExport
   Magento_HipaaApiLogging
   <truncated for brevity>
   ```

   Alla moduler med prefix `Magento_Hipaa` måste finnas i avsnittet med aktiverade moduler.

## Förbättrade funktioner för HIPAA-beredskap

The `magento/hipaa-ee` paket innehåller en del ändringar och förbättringar av Commerce-basprodukten. I följande avsnitt finns information om dessa ändringar och hur de ändrar basprodukten.

### Åtgärdsloggar

Granskningsloggning är ett HIPAA-krav. I ADOBE COMMERCE [Åtgärdsloggar](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) funktionen registrerar alla ändringar som görs av en administratör som arbetar i din butik. För att uppfylla HIPAA-kraven för granskningslogg finns det ändringar i funktionen för att registrera alla åtgärder för administrationsanvändare och -kunder som utförts via Admin-gränssnittet och via API-anrop.

#### Åtgärdsloggsrapport

The _Åtgärdsloggar_ rapportstödraster (**[!UICONTROL System]** > Åtgärdsloggar > Rapport) har ändrats för att passa kundåtgärder som utförts via administratörens gränssnitt och API.

1. Två extra kolumner:
   - ***Källa***: Visar var åtgärden utfördes.\
     Värden: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Klienttyp***: Visar klienttypen.\
     Värden: Kund | Administratör | Integrering


2. Byt namn ***Användarnamn*** till ***Klientidentifierare***
   - ***Klientidentifierare***: Visar inloggnings-ID för den användare som utförde åtgärden\
     Värden:
      - ett e-postmeddelande om klienttypen är kund
      - ett användarnamn om klienttypen är Admin
      - ett namn om klienttypen är Integration

3. Byt namn ***Fullständigt åtgärdsnamn*** till ***Mål***
   - ***Mål***: Visar åtgärdens namn\
     Värden:
      - en slutpunkt om källan är REST API eller SOAP API
      - ett fråge-/mutationsnamn om GraphQL API
      - ett åtgärdsnamn om administratörsgränssnittet eller kundgränssnittet.

#### Konfigurera administratörsåtgärder för loggning

Den här funktionen är inte tillgänglig eftersom alla åtgärder måste spelas in som standard.

### Import-/exportfunktioner

Förbättringarna av import-/exportfunktionerna är inriktade på att förbättra den administrativa upplevelsen och ge bättre insyn i användaråtgärder.

>[!NOTE]
>
>Dessa ***förbättringar ändrar inte import/export av kärnlogik***, istället utökar de funktionaliteten för mer omfattande loggning och förbättrad dataattribuering. De grundläggande funktionerna för import/export ändras inte. Användarna kan fortsätta använda de befintliga funktionerna och arbetsflödena utan avbrott.

#### Loggning av administrativa åtgärder

En av de viktigaste förbättringarna i import-/exportfunktionerna är den förbättrade loggningen av administrativa åtgärder. Detta introducerar möjligheten att fördjupa sig i aktiviteter som är kopplade till import/export av data, vilket bidrar till förbättrad spårning och granskning. Följande åtgärder är nu loggade och återspeglas i **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**rutnät:

| Typ | Åtgärder |
| ---- | ------- |
| Importera | <ul><li>En administratör kör en import<li>En administratör hämtar en importerad fil<li>En administratör hämtar en felfil<ul/> |
| Exportera | <ul><li>En administratörsanvändare begär<li>En administratör hämtar en exporterad fil<ul/> |
| Planerad import/export | <ul><li>Export av administratörsanvändarscheman<li>En administratör redigerar en schemalagd export<li>En administratör kör en schemalagd export<li>En administratör tar bort en schemalagd export<li>En administratör schemalägger en import<li>En administratör redigerar en schemalagd import<li>En administratör kör en schemalagd import<li>En administratör tar bort en schemalagd import<li>En administratörsanvändare kör en massborttagning av import-/exportåtgärder<ul/> |

### Visningsförbättringar och förbättrad filtrering/sortering

För att ge administratörsanvändare tillgång till mer informativa rutnät finns det flera förbättringar när det gäller visning av data samt filtrerings- och sorteringsfunktioner:

#### Importhistorik ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- Aktiverad filtrering för alla kolumner utom **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]** och **[!UICONTROL Summary]**.

#### Exportera ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- Tillagda **[!UICONTROL ID]** kolumn.
- Lagt till en **[!UICONTROL Requested At]** kolumn (_datum och tid när export begärdes_).
- Lagt till en **[!UICONTROL User]** kolumn (_användarnamn för en administratör som gjorde begäran_).
- Borttagen en **[!UICONTROL Action]** kolumn.
- Flyttade **[!UICONTROL Download]** länk till en **[!UICONTROL File name]** kolumn (_som stödrastret Importera historik_).
- Inaktiverade åtgärden som ansvarar för borttagningen av en exporterad fil (_för att förbättra spårning_).
- Aktiverad sortering för alla kolumner utom **[!UICONTROL File name]**.
- Aktiverad filtrering för alla kolumner.

#### Planerad import/export ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- Tillagda **[!UICONTROL ID]** kolumn.
- Lagt till en **[!UICONTROL Scheduled At]** kolumn (_datum och tid när importen eller exporten schemalades_).
- Lagt till en **[!UICONTROL User]** kolumn (_användarnamn för en Admin-användare som har schemalagt import/export_).

## Inaktiverade funktioner för HIPAA-beredskap

### SaaS-tjänster

Ingen av de SaaS-tjänster som erbjuds Adobe Commerce är tillgängliga i HIPAA-beredskapserbjudandet. Detta omfattar, men är inte begränsat till:

- Live Search
- API-nät
- App Builder
- Katalogtjänst

### Inaktiverad gästutcheckning som standard

- Utcheckning av gäster utgör en potentiell risk för olika aspekter av HIPAA, bland annat loggning, åtkomstkontroll, PHI-hygien och -hållning.
- Gästutcheckning är inaktiverat som standard i modulen för beredskap för HIPAA, men kan aktiveras för mina handlare på egen risk.

### Inaktiverad nyhetsbrevfunktion som standard

- Nyhetsbrevfunktionen är som standard inaktiverad för att förhindra att PHI används i marknadsföringssammanhang, men kan aktiveras av handlaren på egen risk.

### Inaktiverade inställningen för tjänsten Advanced Reporting som standard

Inställningen för tjänsten Advanced Reporting är som standard inaktiverad för att förhindra att PHI används för analys och rapportering, men kan aktiveras av handlaren på egen risk.
