---
title: HIPAA-beredskap på Adobe Commerce
description: Läs om hur du kan lägga till tillägget Adobe Commerce HIPAA-Ready och få ytterligare funktioner som gör att du kan uppfylla dina skyldigheter enligt HIPAA.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: bce0e581e89139875e09b671038a21976eccebca
workflow-type: tm+mt
source-wordcount: '1568'
ht-degree: 1%

---

# HIPAA-beredskap på Adobe Commerce

>[!IMPORTANT]
>
>**Juridisk ansvarsfriskrivning**<br/>
>Den här informationen är avsedd att hjälpa Adobe-kunder att besvara sina frågor om Adobe HIPAA-Ready Services. Den utgör inte juridisk rådgivning. Handlarna bör samråda med sitt eget juridiska ombud för att förstå sina skyldigheter enligt HIPAA och hur Adobe produkter används och konfigureras på lämpligt sätt.

>[!BEGINSHADEBOX]

**HIPAA (Health Insurance Portability and Accounability Act)**

HIPAA (Health Insurance Portability and Accounability Act) är den viktigaste federala hälso- och sjukvårdslagstiftningen i USA och regleras av USA:s Department of Health and Human Services (HHS). HIPAA gäller för _täckta entiteter_ (t.ex. vårdgivare, försäkringsgivare och clearinghus) och _Business Associates_ (t.ex. de entiteter som tillhandahåller tjänster till täckta entiteter). HIPAA-kraven anges i tre separata regler: sekretessregel, säkerhetsregel och regel för meddelanden om överträdelser. Adobe fungerar som Business Associate för vissa produkter, som Adobe klassificerar som&quot;HIPAA-Ready Services&quot;. Data som regleras under HIPAA kallas _Skyddad hälsoinformation_ eller PHI. PHI är en delmängd av hälsoinformation som (1) skapas eller tas emot av en vårdgivare, en hälsoplan eller en vårdcentral, (2) avser en individs tidigare, nuvarande eller framtida fysiska eller psykiska hälsa eller tillstånd, tillhandahållande av hälso- och sjukvård till en individ eller tidigare, nuvarande eller framtida betalning för tillhandahållande av hälso- och sjukvård till en individ, och (3) identifierar den individ eller med avseende på vilken det finns en rimlig grund att tro informationen kan användas för att identifiera den enskilda personen. HIPAA:s sekretess- och säkerhetsregler kräver att en enhet som omfattas erhåller skriftliga garantier från en Business Associate i form av ett Business Associate-avtal, eller BAA, som kräver att Business Associate ska skydda integriteten och säkerheten för de berörda enheternas PHI. Mer information finns i [HIPAA och Adobe Products and Services](https://www.adobe.com/trust/compliance/hipaa-ready.html) i Adobe Trust Center.

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA-Ready

Utbyggnaden av Adobe Commerce HIPAA-Ready lägger till ytterligare funktioner och funktioner i Adobe Commerce-installationer som gör att handlarna kan uppfylla sina respektive HIPAA-skyldigheter.

Adobe Commerce HIPAA-Ready-tillägget, `magento/hipaa-ee`, är tillgängligt för Adobe Commerce i molninfrastruktur eller Adobe Managed Services-projekt. Installationsprocessen för Adobe Commerce HIPAA-Ready inaktiverar vissa inbyggda tjänster och funktioner som uppfyller kraven för HIPAA. Se [Inaktiverade tjänster och funktioner](#disabled-services-and-features).

>[!NOTE]
>
>Tillgång till HIPAA-funktioner är endast tillgänglig för handlare som har köpt tillägget för hälsovård för Adobe Commerce.

*De här materialen är endast avsedda som information. Tillhandahållande av denna information berättigar inte mottagaren till några avtalsmässiga eller andra rättigheter. Även om det har gjorts ansträngningar för att säkerställa att informationen är korrekt från och med den dag då den har lämnats, finns det ingen representation om att informationen är korrekt och fullständig. Adobe förbinder sig inte att uppdatera denna information eftersom lagen eller Adobe ändras. Dokumentet ska inte distribueras till någon annan part än den avsedda mottagaren utan skriftligt medgivande från Adobe.*

## Systemkrav

Adobe Commerce måste distribueras på antingen Adobe Commerce i molninfrastruktur eller Adobe Commerce Managed Services med version 2.4.6-p3 eller senare (inga betaversioner).

## Installation

**Förutsättning**

>[!BEGINSHADEBOX]

- Adobe har etablerat ditt Adobe Commerce-konto för att komma åt tillägget HIPAA Ready.
- Åtkomst till [repo.magento.com](https://repo.magento.com) för att installera tillägget. Om du vill ha nyckelgenerering och de nödvändiga rättigheterna kan du läsa [Hämta dina autentiseringsnycklar](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

>[!ENDSHADEBOX]

Installera den senaste versionen av tillägget Adobe HIPAA-Ready Services (`magento/hipaa-ee`) på en instans som kör Adobe Commerce version 2.4.6-p3 eller senare. Tillägget levereras som ett kompositmetapaket från databasen [repo.magento.com](https://repo.magento.com). Metapaketet innehåller en samling moduler som aktiverar HIPAA-funktionerna för en Adobe Commerce-instans.

1. På din lokala arbetsstation byter du till projektkatalogen för ditt Adobe Commerce i molninfrastrukturprojekt.

   >[!NOTE]
   >
   >Mer information om att hantera Commerce projektmiljöer lokalt finns i [Hantera grenar med CLI](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) i _Adobe Commerce on Cloud Infrastructure User Guide_.

1. Kolla in miljögrenen för att uppdatera med Adobe Commerce Cloud CLI.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Lägg till metapaketet `magento/hipaa-ee` i dispositionskonfigurationen med hjälp av dispositionsgränssnittet.

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

   När uppdateringarna skickas initieras [Commerce molndistributionsprocess](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) för att ändringarna ska börja gälla. Kontrollera distributionsstatusen från [distributionsloggen](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

### Verifiera installation

När uppdateringarna har distribuerats kontrollerar du att tillägget `Hipaa*` har installerats

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

   Alla moduler som har prefixet `Magento_Hipaa` måste finnas i avsnittet med aktiverade moduler.

## Förbättrade funktioner för HIPAA-beredskap

Tillägget `magento/hipaa-ee` innehåller några ändringar och förbättringar av Commerce basprodukt. I följande avsnitt finns information om dessa ändringar och hur de ändrar basprodukten.

### Åtgärdsloggar

Granskningsloggning är ett HIPAA-krav. I Adobe Commerce registrerar funktionen [Åtgärdsloggar](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) alla ändringar som gjorts av en Admin-användare som arbetar i din butik. För att uppfylla HIPAA-kraven för granskningsloggen har funktionen uppdaterats för att registrera alla åtgärder för administrationsanvändare och -kunder som utförts via administratörens gränssnitt och via API-anrop.

#### Åtgärdsloggsrapport

Rapportrutnätet _Åtgärdsloggar_ (**[!UICONTROL System]** > Åtgärdsloggar > Rapport) har ändrats för att passa kundåtgärder som utförts via administratörens gränssnitt och API.

1. Två kolumner har lagts till:
   - ***Source***: Visar var åtgärden utfördes.
Värden: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***Klienttyp***: Visar klienttypen.
Värden: Kund | Administratör | Integrering

2. Namnet på kolumnen ***Användarnamn*** har ändrats till ***Klientidentifierare***
   - ***Klientidentifierare***: Visar inloggnings-ID för användaren som utförde åtgärden.
Värden:
      - ett e-postmeddelande om klienttypen är kund
      - ett användarnamn om klienttypen är Admin
      - ett namn om klienttypen är Integration

3. Namnet på kolumnen ***Fullständigt åtgärdsnamn*** har ändrats till ***Mål***
   - ***Mål***: Visar åtgärdsnamnet.
Värden:
      - en slutpunkt om Source är en REST API eller SOAP API
      - en fråga eller ett mutationsnamn om ett GraphQL-API
      - ett åtgärdsnamn om ett administratörsgränssnitt eller kundgränssnitt används.

#### Konfigurera administratörsåtgärder för loggning

Den här funktionen är inte tillgänglig eftersom alla åtgärder måste spelas in som standard.

### Import- och exportfunktioner

Förbättringarna av import- och exportfunktionerna är inriktade på att förbättra den administrativa upplevelsen och ge bättre synlighet i användaråtgärder.

>[!NOTE]
>
>De här ***förbättringarna ändrar inte import- och exportlogiken***, utan utökar funktionerna för att erbjuda mer omfattande loggning och förbättrad dataattribuering. De grundläggande funktionerna för import och export ändras inte. Användarna kan fortsätta använda de befintliga funktionerna och arbetsflödena utan avbrott.

#### Loggning av administrativa åtgärder

En av de viktigaste förbättringarna i import- och exportfunktionerna är den förbättrade loggningen av administrativa åtgärder. Den här förbättringen ger möjlighet att fördjupa sig i aktiviteter som är kopplade till import och export av data, vilket bidrar till förbättrad spårning och granskning. Följande åtgärder är nu loggade och återspeglas i stödrastret **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**:

| Typ | Åtgärder |
| ---- | ------- |
| Importera | <ul><li>En administratör kör en import<li>En administratör hämtar en importerad fil<li>En administratör hämtar en felfil<ul/> |
| Exportera | <ul><li>En administratörsanvändare begär<li>En administratör hämtar en exporterad fil<ul/> |
| Planerad import/export | <ul><li>Export av administratörsanvändarscheman<li>En administratör redigerar en schemalagd export<li>En administratör kör en schemalagd export<li>En administratör tar bort en schemalagd export<li>En administratör schemalägger en import<li>En administratör redigerar en schemalagd import<li>En administratör kör en schemalagd import<li>En administratör tar bort en schemalagd import<li>En administratörsanvändare kör en massborttagning av import-/exportåtgärder<ul/> |

### Visningsförbättringar och förbättrad filtrering och sortering

Tjänsten HIPAA-Ready ger administratörsanvändare tillgång till fler informativa rutnät och erbjuder flera förbättringar för att visa, filtrera och sortera data.

#### Importhistorik ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- Aktiverad filtrering för alla kolumner förutom **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]** och **[!UICONTROL Summary]**.

#### Exportera ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- En **[!UICONTROL ID]**-kolumn har lagts till.
- En **[!UICONTROL Requested At]**-kolumn (_datum och tid när export begärdes_) har lagts till.
- En **[!UICONTROL User]**-kolumn (_användarnamn för en administratör som gjorde begäran_) har lagts till.
- En **[!UICONTROL Action]**-kolumn har tagits bort.
- Länken **[!UICONTROL Download]** har flyttats till en **[!UICONTROL File name]**-kolumn (_som till exempel fältet för importhändelser_).
- Inaktiverade åtgärden som ansvarar för borttagningen av en exporterad fil (_för att förbättra spårningen_).
- Aktiverad sortering för alla kolumner utom **[!UICONTROL File name]**.
- Aktiverad filtrering för alla kolumner.

#### Schemalagda importer och exporter ([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- En **[!UICONTROL ID]**-kolumn har lagts till.
- En **[!UICONTROL Scheduled At]**-kolumn (datum och tid _när import eller export schemalagdes_) har lagts till.
- En **[!UICONTROL User]**-kolumn har lagts till (användarnamnet _för en administratörsanvändare som har schemalagt importen eller exporten_).

## Handikappade tjänster och funktioner

För att uppfylla HIPAA-kraven är vissa tjänster och funktioner som stöds av Adobe Commerce antingen inte tillgängliga eller inaktiverade som standard. Handlare har möjlighet att återaktivera eller använda dessa tjänster och funktioner på egen risk.

### Tjänster

- **Adobe Commerce-tjänster** - Ingen av Adobe Commerce-tjänsterna eller utökningstjänsterna är tillgängliga under beredskapserbjudandet för HIPAA. Dessa tjänster omfattar, men är inte begränsade till:

   - Live Search
   - API-nät
   - App Builder

- **[SendGrid-tjänsten](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)** - Den här tjänsten är inaktiverad som standard eftersom programmet inte är HIPAA-kompatibelt.

### Funktioner som är inaktiverade som standard

Följande funktioner är inaktiverade som standard i modulen HIPAA-beredskap. Handlare kan aktivera alla dessa funktioner på egen risk.

- **[Gästutcheckning](../stores-purchase/checkout-guest.md)** - Den här funktionen utgör en potentiell risk för olika aspekter av HIPAA, bland annat loggning, åtkomstkontroll, PHI-hygien och -hållning.

- **[Nyhetsbrevsfunktion](../merchandising-promotions/newsletters.md)** - Den här funktionen är inaktiverad för att förhindra att PHI används i marknadsföringssammanhang.

- **[Avancerad rapporttjänstinställning](../getting-started/business-intelligence.md)** - Den här konfigurationsinställningen är inaktiverad för att förhindra att PHI används för analys och rapportering.
