---
title: HIPAA-beredskap på Adobe Commerce
description: Lär dig hur du kan lägga till Adobe Commerce HIPAA-Ready-modulen och få ytterligare funktioner som gör att du kan uppfylla dina HIPAA-skyldigheter.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 7e132d66523feba579baf0bae14e1de9de4d6591
workflow-type: tm+mt
source-wordcount: '1542'
ht-degree: 0%

---

# HIPAA-beredskap på Adobe Commerce

>[!IMPORTANT]
>
>**Juridisk ansvarsfriskrivning**<br/>
>Den här informationen är avsedd att hjälpa Adobe-kunder att besvara sina frågor om Adobe HIPAA-Ready Services. Den utgör inte juridisk rådgivning. Handlarna bör samråda med sitt eget juridiska ombud för att förstå sina skyldigheter enligt HIPAA och hur Adobe produkter används och konfigureras på lämpligt sätt.

>[!BEGINSHADEBOX]

**HIPAA (Health Insurance Portability and Accounability Act)**

HIPAA (Health Insurance Portability and Accounability Act) är den viktigaste federala hälso- och sjukvårdslagstiftningen i USA och regleras av USA:s Department of Health and Human Services (HHS). HIPAA gäller för _Berörda enheter_ (t.ex. vårdgivare, försäkringsbolag och clearingorganisationer) och _Business Associates_ (t.ex. enheter som tillhandahåller tjänster till enheter som omfattas). HIPAA-kraven anges i tre separata regler: sekretessregel, säkerhetsregel och regel för meddelanden om överträdelser. Adobe fungerar som Business Associate för vissa produkter, som Adobe klassificerar som&quot;HIPAA-Ready Services&quot;. Uppgifter som regleras enligt HIPAA kallas _Skyddad hälsoinformation_ eller PHI. PHI är en delmängd av hälsoinformation som (1) skapas eller tas emot av en vårdgivare, en hälsoplan eller en vårdcentral, (2) avser en individs tidigare, nuvarande eller framtida fysiska eller psykiska hälsa eller tillstånd, tillhandahållande av hälso- och sjukvård till en individ eller tidigare, nuvarande eller framtida betalning för tillhandahållande av hälso- och sjukvård till en individ, och (3) identifierar den individ eller med avseende på vilken det finns en rimlig grund att tro informationen kan användas för att identifiera den enskilda personen. HIPAA:s sekretess- och säkerhetsregler kräver att en enhet som omfattas erhåller skriftliga garantier från en Business Associate i form av ett Business Associate-avtal, eller BAA, som kräver att Business Associate ska skydda integriteten och säkerheten för de berörda enheternas PHI. Mer information finns i [HIPAA och Adobe Products and Services](https://www.adobe.com/trust/compliance/hipaa-ready.html) i Adobe Trust Center.

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA-Ready

Adobe Commerce HIPAA-Ready har ytterligare funktioner som gör att handlare kan uppfylla sina respektive HIPAA-skyldigheter.

Adobe Commerce HIPAA-Ready levereras som ett tillägg till Adobe Commerce, `magento/hipaa-ee` som finns för Adobe Commerce i molninfrastruktur eller Adobe Managed Services-projekt. Installationsprocessen för Adobe Commerce HIPAA-Ready inaktiverar vissa inbyggda tjänster och funktioner som uppfyller kraven för HIPAA. Se [Handikappade tjänster och funktioner](#disabled-services-and-features).

*Dessa material är endast avsedda som information. Tillhandahållande av denna information berättigar inte mottagaren till några avtalsmässiga eller andra rättigheter. Även om det har gjorts ansträngningar för att säkerställa att informationen är korrekt från och med den dag då den har lämnats, finns det ingen representation om att informationen är korrekt och fullständig. Adobe förbinder sig inte att uppdatera denna information eftersom lagen eller Adobe ändras. Dokumentet får inte heller distribueras till någon annan part än den avsedda mottagaren utan skriftligt medgivande från Adobe.*

## Systemkrav

Adobe Commerce måste distribueras på antingen Adobe Commerce i molninfrastruktur eller Adobe Commerce Managed Services med version 2.4.6-p3 eller senare (inga betaversioner).

## Installation

Installera den senaste versionen av tillägget Adobe HIPAA-Ready Services (`magento/hipaa-ee`) på en instans som kör Adobe Commerce version 2.4.6-p3 eller senare. Tillägget levereras som ett dispositionsmetapaket från [repo.magento.com](https://repo.magento.com) databas.

>[!BEGINSHADEBOX]

**Förutsättning**

Du måste ha tillgång till [repo.magento.com](https://repo.magento.com) för att installera tillägget. För nyckelgenerering och för att erhålla nödvändiga rättigheter, se [Hämta dina autentiseringsnycklar](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

>[!ENDSHADEBOX]

1. På din lokala arbetsstation byter du till projektkatalogen för ditt Adobe Commerce i molninfrastrukturprojekt.

   >[!NOTE]
   >
   >Mer information om hur du hanterar Commerce projektmiljöer lokalt finns i  [Hantera filialer med CLI](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) i _Användarhandbok för infrastruktur i Adobe Commerce om molnet_.

1. Kolla in miljögrenen för att uppdatera med Adobe Commerce Cloud CLI.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Lägg till metapaketet `magento/hipaa-ee` till dispositionskonfigurationen med Composer CLI.

   ```shell
   composer require "magento/hipaa-ee" --no-update
   ```

1. Uppdatera paketberoenden.

   ```shell
   composer update "magento/hipaa-ee"
   ```

1. Lägg till, implementera och skicka den uppdaterade koden till molnmiljön.

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   När uppdateringarna skickas initieras [Commerce molndistributionsprocess](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) för att tillämpa ändringarna. Kontrollera distributionsstatusen på [distributionslogg](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

### Verifiera installation

När uppdateringarna har distribuerats kontrollerar du att `Hipaa*` tillägg är installerat

1. Använd SSH för att logga in i fjärrmolnmiljön.

   ```shell
   magento-cloud ssh
   ```

1. Använd Adobe Commerce CLI på kommandoraden för att kontrollera modulens status.

   ```shell
   bin/magento module:status
   ```

1. Kontrollera att HIPAA-modulerna finns med i listan över aktiverade moduler:

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

The `magento/hipaa-ee` i paketet introduceras vissa ändringar och förbättringar av Commerce basprodukt. I följande avsnitt finns information om dessa ändringar och hur de ändrar basprodukten.

### Åtgärdsloggar

Granskningsloggning är ett HIPAA-krav. I ADOBE COMMERCE [Åtgärdsloggar](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) funktionen registrerar alla ändringar som görs av en administratör som arbetar i din butik. För att uppfylla HIPAA-kraven för granskningsloggen har funktionen uppdaterats för att registrera alla åtgärder för administrationsanvändare och -kunder som utförts via administratörens gränssnitt och via API-anrop.

#### Åtgärdsloggsrapport

The _Åtgärdsloggar_ rapportstödraster (**[!UICONTROL System]** > Åtgärdsloggar > Rapport) har ändrats för att passa kundåtgärder som utförts via administratörens gränssnitt och API.

1. Två kolumner har lagts till:
   - ***Källa***: Visar var åtgärden utfördes.
Värden: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Klienttyp***: Visar klienttypen.
Värden: Kund | Administratör | Integrering

2. Bytt namn på ***Användarnamn*** kolonn till ***Klientidentifierare***
   - ***Klientidentifierare***: Visar inloggnings-ID för användaren som utförde åtgärden.
Värden:
      - ett e-postmeddelande om klienttypen är kund
      - ett användarnamn om klienttypen är Admin
      - ett namn om klienttypen är Integration

3. Bytt namn på ***Fullständigt åtgärdsnamn*** kolumn till ***Mål***
   - ***Mål***: Visar åtgärdens namn.
Värden:
      - en slutpunkt om källan är ett REST API eller SOAP API
      - en fråga eller ett mutationsnamn om ett GraphQL-API
      - ett åtgärdsnamn om ett administratörsgränssnitt eller kundgränssnitt används.

#### Konfigurera administratörsåtgärder för loggning

Den här funktionen är inte tillgänglig eftersom alla åtgärder måste spelas in som standard.

### Import- och exportfunktioner

Förbättringarna av import- och exportfunktionerna är inriktade på att förbättra den administrativa upplevelsen och ge bättre synlighet i användaråtgärder.

>[!NOTE]
>
>Dessa ***förbättringarna ändrar inte import- och exportens kärnlogik***, istället utökar de funktionaliteten för mer omfattande loggning och förbättrad dataattribuering. De grundläggande funktionerna för import och export ändras inte. Användarna kan fortsätta använda de befintliga funktionerna och arbetsflödena utan avbrott.

#### Loggning av administrativa åtgärder

En av de viktigaste förbättringarna i import- och exportfunktionerna är den förbättrade loggningen av administrativa åtgärder. Den här förbättringen ger möjlighet att fördjupa sig i aktiviteter som är kopplade till import och export av data, vilket bidrar till förbättrad spårning och granskning. Följande åtgärder är nu loggade och återspeglas i **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**rutnät:

| Typ | Åtgärder |
| ---- | ------- |
| Importera | <ul><li>En administratör kör en import<li>En administratör hämtar en importerad fil<li>En administratör hämtar en felfil<ul/> |
| Exportera | <ul><li>En administratörsanvändare begär<li>En administratör hämtar en exporterad fil<ul/> |
| Planerad import/export | <ul><li>Export av administratörsanvändarscheman<li>En administratör redigerar en schemalagd export<li>En administratör kör en schemalagd export<li>En administratör tar bort en schemalagd export<li>En administratör schemalägger en import<li>En administratör redigerar en schemalagd import<li>En administratör kör en schemalagd import<li>En administratör tar bort en schemalagd import<li>En administratörsanvändare kör en massborttagning av import-/exportåtgärder<ul/> |

### Visningsförbättringar och förbättrad filtrering och sortering

Tjänsten HIPAA-Ready ger administratörsanvändare tillgång till fler informativa rutnät och erbjuder flera förbättringar för att visa, filtrera och sortera data.

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

#### Planerad import och export ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- Tillagda **[!UICONTROL ID]** kolumn.
- Lagt till en **[!UICONTROL Scheduled At]** kolumn (den _datum och tid när importen eller exporten schemalades_).
- Lagt till en **[!UICONTROL User]** kolumn (den _användarnamn för en Admin-användare som har schemalagt importen eller exporten_).

## Handikappade tjänster och funktioner

För att uppfylla HIPAA-kraven är vissa tjänster och funktioner som stöds av Adobe Commerce antingen inte tillgängliga eller inaktiverade som standard. Handlare har möjlighet att återaktivera eller använda dessa tjänster och funktioner på egen risk.

### Tjänster

- **Adobe Commerce-tjänster**- Ingen av Adobe Commerce tjänster eller utökningstjänster är tillgängliga under beredskapserbjudandet för HIPAA. Dessa tjänster omfattar, men är inte begränsade till:

   - Live Search
   - API-nät
   - App Builder
   - Katalogtjänst

- **[Tjänsten SendGrid](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)**- Den här tjänsten är inaktiverad som standard eftersom programmet inte är HIPAA-kompatibelt. Handlare kan skicka in en supportförfrågan för att aktivera Sendgrid, men de måste bekräfta att de tar risken att använda tjänsten.

### Funktioner som är inaktiverade som standard

Följande funktioner är inaktiverade som standard i modulen HIPAA-beredskap. Handlare kan aktivera alla dessa funktioner på egen risk.

- **[Kassa på gäst](../stores-purchase/checkout-guest.md)**- Den här funktionen utgör en potentiell risk för olika aspekter av HIPAA, bland annat loggning, åtkomstkontroll, PHI-hygien och -hållning.

- **[Nyhetsbrev](../merchandising-promotions/newsletters.md)**- Den här funktionen är inaktiverad för att förhindra att PHI används i ett marknadsföringssammanhang.

- **[Avancerade inställningar för rapporttjänst](../getting-started/business-intelligence.md)**— Den här konfigurationsinställningen är inaktiverad för att förhindra att PHI används för analys och rapportering.
