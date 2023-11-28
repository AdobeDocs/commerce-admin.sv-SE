---
title: '"rapportering"[!DNL New Relic]'
description: Lär dig mer om den [!DNL New Relic] rapportering som är tillgänglig för konton för Adobe Commerce i molninfrastrukturen, som innehåller programvaran för New Relic APM-tjänsten.
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
source-git-commit: e9a7645aed0e3b48bf565b04cdb6a31ce5d39ca0
workflow-type: tm+mt
source-wordcount: '1361'
ht-degree: 0%

---

# [!DNL New Relic] rapportering

[New Relic][1] är en tjänst för programvaruanalys som hjälper er att analysera och förbättra applikationsinteraktioner. Konton för Adobe Commerce i molninfrastruktur inkluderar programvaran för [!DNL New Relic APM] service. Mer information finns i [New Relic-tjänster][4] i _Handbok för Commerce on Cloud Infrastructure_.

## Steg 1: Registrera dig för en [!DNL New Relic] konto

1. Gå till [[!DNL New Relic]][1] webbplatsen och registrera dig för ett konto.

   Du kan också registrera dig för ett gratis testkonto.

1. Följ instruktionerna på webbplatsen. När du uppmanas till det väljer du den produkt som du vill installera först.

1. När du är på ditt konto letar du reda på följande autentiseringsuppgifter som krävs för att slutföra Commerce-konfigurationen:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | Konto-ID | Från [!DNL New Relic] konto-ID är kontonamnet i URL:en efter: `/accounts` |
   | Program-ID | Från [!DNL New Relic] instrumentpanel för konto, klicka på **[!UICONTROL New Relic APM]**. Välj **[!UICONTROL Applications]**. Välj sedan programmet. Program-ID är numret i URL:en efter: `/applications/` |
   | New Relic API-nyckel | Från [!DNL New Relic] instrumentpanel för konto, klicka på **[!UICONTROL Account Settings]**. Välj på menyn till vänster under Integreringar **[!UICONTROL Data Sharing]**. Du kan skapa, generera om eller ta bort API-nyckeln från den här sidan. |
   | API-nyckel för insikter | Från [!DNL New Relic] instrumentpanel för konto, klicka på **[!UICONTROL Insights]**. Välj **[!UICONTROL API Keys]**. API-nycklar för dina insikter visas på den här sidan. Klicka vid behov på plustecknet (**+**) bredvid Infoga tangenter för att generera en tangent. |

   {style="table-layout:auto"}

## Steg 2: Installera [!DNL New Relic] -agent på servern

Används [!DNL New Relic APM Pro] PHP-agenten måste vara installerad på servern för att du ska kunna samla in och överföra data.

1. När du uppmanas att välja en webbagent klickar du på **PHP**.

1. Följ instruktionerna för att konfigurera PHP-agenten på servern.

   Om du behöver hjälp, se [New Relic for PHP][3].

1. Kontrollera att kron körs på servern.

   Mer information finns på [Konfigurera och kör cron][5] i utvecklardokumentationen.

## Steg 3: Konfigurera din butik

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I den vänstra navigeringspanelen där **[!UICONTROL General]** är expanderad, välj **[!UICONTROL New Relic Reporting]** och gör följande:

   ![New Relic Reporting-konfiguration](./assets/new-relic-reporting-general.png){width="600"}

   * Ange **[!UICONTROL Enable New Relic Integration]** till `Yes`.

   * I **[!UICONTROL Insights API URL]**, ersätt procentvärdet (`%`) med ditt New Relic konto-ID.

   * Ange **[!UICONTROL New Relic Account ID]**.

   * Ange **[!UICONTROL New Relic Application ID]**.

   * Ange **[!UICONTROL New Relic API Key]**.

   * Ange dig **[!UICONTROL Insights API Key]**.

1. För **[!UICONTROL New Relic Application Name]**, anger du ett namn som identifierar konfigurationen för intern referens.

1. (valfritt) för **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]**, markera `Yes` för att skicka insamlade data för butiken och administratören som separata appar till New Relic.

   Det här alternativet kräver att ett namn anges för **[!UICONTROL New Relic Application Name]**.

   >[!NOTE]
   >
   >Om du aktiverar den här funktionen minskas antalet falska positiva [!DNL New Relic] varningar och möjliggör konfigurerad övervakning och varningar för frontend-prestanda. New Relic tar emot separata programdatafiler med programnamnet tillagt i `Adminhtml` och frontend. Exempel: `MyStore_Adminhtml`

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Steg 4: Aktivera Cron för [!DNL New Relic] rapportering

1. Expandera ![väljaren](../assets/icon-display-expand.png) eller avsnittet **[!UICONTROL Cron]** .

   ![New Relic Cron-konfiguration](./assets/new-relic-reporting-cron.png){width="600"}

1. Ange **[!UICONTROL Enable Cron]** till `Yes`.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## [!DNL New Relic] frågor

[!DNL New Relic Insights] data baseras på programsatser som skrivs i [!DNL New Relic Query Language] (NRQL) och eventuella egna parametrar som du kan inkludera. Data kan returneras från ad hoc-frågor eller från frågor som sparats på kontrollpanelen. Mer information finns i [NRQL-referens][6] i [!DNL New Relic] dokumentation.

### Administratörshändelser

#### Aktiva administratörsanvändare

Returnerar antalet aktiva Admin-användare.

    SELECT uniqueCount(AdminId)
    FRÅN-transaktion
    WHERE appName=&#39;&lt;your_app_name>&#39; SEDAN 15 minuter sedan

#### Aktiva administratörsanvändare

Returnerar namnen på aktiva Admin-användare.

    SELECT uniques(AdminName)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; SINCE 15 minutes ago
&lt;/your_app_name>
#### Senaste administratörsaktivitet

Returnerar antalet senaste Admin-åtgärder.

    SELECT count(AdminId)
    FRÅN-transaktion
    WHERE appName =&#39;&lt;your_app_name>&#39; FACET AdminName SEDAN 1 dag sedan

#### Senaste administratörsaktivitet

Returnerar detaljerad information om de senaste administratörsåtgärderna, inklusive administratörens användarnamn, varaktighet och programnamn.

    VÄLJ AdminName, varaktighet, namn
    FRÅN transaktion
    DÄR appName=&#39;&#39; OCH AdminName &lt;your_app_name>ÄR INTE NULL
    OCH AdminName!&lt;/your_app_name>= &quot;N/A&quot;-GRÄNS 50

### Cron-evenemang

#### Antal kategorier

Returnerar antalet programhändelser per kategori under den angivna tidsperioden.

    SELECT-genomsnitt (CatalogCategoryCount)
    FRÅN Cron
    DÄR CatalogCategoryCount INTE ÄR NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minuter

#### Aktuellt antal kataloger

Returnerar det genomsnittliga antalet programhändelser i katalogen per kategori under den angivna tidsperioden.

    SELECT-genomsnitt (CatalogCategoryCount)
    FRÅN Cron
    DÄR CatalogCategoryCount INTE ÄR NULL
    AND CatalogCategoryCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SEDAN 2 minutes ago LIMIT 1

#### Aktiva produkter

Returnerar antalet programhändelser per produkt under den angivna tidsperioden.

    SELECT-genomsnitt(CatalogProductActiveCount)
    FRÅN Cron
    DÄR CatalogProductActiveCount INTE ÄR NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minuter

#### Antal aktiva produkter

Returnerar det genomsnittliga antalet aktiva programhändelser per produkt under den angivna tidsperioden.

    SELECT-genomsnitt(CatalogProductActiveCount)
    FRÅN Cron
    DÄR CatalogProductActiveCount INTE ÄR NULL
    AND CatalogProductActiveCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SEDAN 2 minutes ago LIMIT 1

#### Konfigurerbara produkter

Returnerar det genomsnittliga antalet programhändelser för konfigurerbara produkter under den angivna tidsperioden.

    SELECT-genomsnitt (CatalogProductConfigurableCount)
    FRÅN Cron
    DÄR CatalogProductConfigurableCount INTE ÄR NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minuter

#### Konfigurerbart produktantal

Returnerar det genomsnittliga antalet programhändelser per konfigurerbar produkt under den angivna tidsperioden.

    SELECT-genomsnitt (CatalogProductConfigurableCount)
    FRÅN Cron
    DÄR CatalogProductConfigurableCount INTE ÄR NULL
    AND CatalogProductConfigurableCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SEDAN 2 minutes ago LIMIT 1

#### Antal produkter (alla)

Returnerar det totala antalet programhändelser för alla produkter.

    SELECT-genomsnitt(CatalogProductCount)
    FRÅN Cron
    DÄR CatalogProductCount INTE ÄR NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minuter

#### Aktuellt produktantal (alla)

Returnerar det genomsnittliga antalet programhändelser för alla produkter under den angivna tidsperioden.

    SELECT-genomsnitt(CatalogProductCount)
    FRÅN Cron
    DÄR CatalogProductCount INTE ÄR NULL
    AND CatalogProductCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SEDAN 2 minutes ago LIMIT 1

#### Kundantal

Returnerar det genomsnittliga antalet programhändelser per kund.

    SELECT-genomsnitt (CustomerCount)
    FRÅN Cron
    DÄR CustomerCount INTE ÄR NULL
    OCH CustomerCount > 0&lt;
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minuter

#### Aktuellt kundantal

Returnerar det genomsnittliga antalet kunder under den angivna tidsperioden.

    SELECT-genomsnitt (CustomerCount)
    FRÅN Cron
    DÄR CustomerCount INTE ÄR NULL
    OCH CustomerCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SEDAN 2 minutes ago LIMIT 1

#### Modulstatus

Returnerar det genomsnittliga antalet gånger som programmoduler aktiveras, inaktiveras eller installeras under den angivna tidsperioden.

    SELECT-genomsnitt (ModulesDisabled), genomsnitt (ModulesEnabled), genomsnitt
    (ModulerInstallerade)
    FRÅN KÖRN&lt;
    WHERE appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minuter

#### Aktuell modulstatus

Returnerar det genomsnittliga antalet gånger moduler aktiverades, inaktiverades eller installerades under den angivna tidsperioden.

    SELECT-genomsnitt (ModulesDisabled), genomsnitt (ModulesEnabled), genomsnitt
    (ModulerInstallerade)
    FRÅN Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; SEDAN 2 minutes ago LIMIT 1

#### Antal webbplatser och butiker

Returnerar det genomsnittliga antalet programhändelser per webbplats och butik under den angivna tidsperioden.

    SELECT-genomsnitt (StoreViewCount), genomsnitt(WebsiteCount)
    FRÅN Cron
    WHERE appName = &#39;&amp;lt;your_app_name&amp;gt;&#39; TIMESERIES 2 minuter

#### Aktuellt antal webbplatser och butiker

Returnerar det genomsnittliga antalet aktuella programhändelser under den angivna tidsperioden.

    SELECT-genomsnitt (StoreViewCount), genomsnitt(WebsiteCount)
    FRÅN Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; SEDAN 2 minutes ago LIMIT 1

#### Cron - alla data från händelse

Returnerar alla data för programhändelser.

    VÄLJ *
    FRÅN Cron
    WHERE appName = &#39;&lt;your_app_name>&#39;

### Kunder

#### Antal aktiva kunder

Returnerar antalet aktiva kunder under den angivna tidsperioden.

    SELECT uniqueCount(CustomerId)
    FRÅN-transaktion
    WHERE appName = &#39;&lt;your_app_name>&#39; SEDAN 15 minuter sedan

#### Aktiva kunder

Returnerar namnen på aktiva kunder under den angivna tidsperioden.

    SELECT uniques(CustomerName)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; SINCE 15 minutes ago
&lt;/your_app_name>
#### De vanligaste kunderna

Returnerar de främsta kunderna under den angivna tidsperioden.

    SELECT count(CustomerId)
    FRÅN-transaktion
    WHERE appName = &#39;&lt;your_app_name>&#39; FACET CustomerName SEDAN 1 dag sedan

#### Senaste administratörsaktivitet

Returnerar ett definierat antal poster för den senaste aktiviteten, som innehåller kundens namn och besökets varaktighet.

    VÄLJ CustomerName, duration, name
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39;
    AND CustomerName IS NOT NULL
    och CustomerName !&lt;/your_app_name>= &quot;N/A&quot;-GRÄNS 50

### Beställningar

#### Antal beställningar som gjorts

Returnerar antalet beställningar som gjorts under den angivna tidsperioden.

    SELECT count(Order)
    FRÅN TRANSAKTION SEDAN 1 dag

#### Totalt ordervärde

Returnerar det totala antalet radartiklar som beställts under den angivna tidsperioden.

    SELECT sum(orderValue)
    FRÅN TRANSAKTION SEDAN 1 dag

#### Totalt antal beställda radartiklar

Returnerar det totala antalet radartiklar som beställts under den angivna tidsperioden.

    SELECT sum(lineItemCount)
    FRÅN TRANSAKTION SEDAN 1 dag


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
