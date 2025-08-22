---
title: '[!DNL New Relic]-rapportering'
description: Läs mer om  [!DNL New Relic] rapporteringen för konton för Adobe Commerce i molninfrastrukturen, som innehåller programvaran för New Relic APM-tjänsten.
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: c406add80981387305755221f21624dad475e63f
workflow-type: tm+mt
source-wordcount: '1399'
ht-degree: 0%

---

# [!DNL New Relic]-rapportering

[New Relic][1] är en tjänst för programvaruanalys som hjälper dig att analysera och förbättra programinteraktioner. Konton för Adobe Commerce i molninfrastrukturen inkluderar programvaran för tjänsten [!DNL New Relic APM]. Mer information finns i [New Relic-tjänster][4] i _Commerce on Cloud Infrastructure Guide_.

## Steg 1: Registrera ett [!DNL New Relic]-konto

1. Gå till webbplatsen [[!DNL New Relic]][1] och registrera dig för ett konto.

   Du kan också registrera dig för ett kostnadsfritt provkonto.

1. Följ instruktionerna på webbplatsen. När du uppmanas till det väljer du den produkt du vill installera först.

1. När du är på ditt konto kan du hitta följande autentiseringsuppgifter som krävs för att slutföra Commerce-konfigurationen:

   | Alternativ | Beskrivning |
   | ------ | ----------- |
   | Konto-ID | Från din [!DNL New Relic]-kontokontrollpanel är konto-ID numret i URL:en efter: `/accounts` |
   | Program-ID | Klicka på [!DNL New Relic] på kontrollpanelen för ditt **[!UICONTROL New Relic APM]**-konto. Välj **[!UICONTROL Applications]** på menyn. Välj sedan programmet. Program-ID är numret i URL:en efter: `/applications/` |
   | New Relic API-nyckel | Klicka på [!DNL New Relic] på kontrollpanelen för ditt **[!UICONTROL Account Settings]**-konto. Välj **[!UICONTROL Data Sharing]** på menyn till vänster under Integreringar. Du kan skapa, generera om eller ta bort API-nyckeln från den här sidan. |
   | API-nyckel för insikter | Klicka på [!DNL New Relic] på kontrollpanelen för ditt **[!UICONTROL Insights]**-konto. Välj **[!UICONTROL API Keys]** på menyn till vänster under Administration. API-nycklar för dina insikter visas på den här sidan. Klicka vid behov på plustecknet (**+**) bredvid Infoga tangenter för att generera en tangent. |

   {style="table-layout:auto"}

## Steg 2: Installera agenten [!DNL New Relic] på servern

Om du vill använda [!DNL New Relic APM Pro] för att samla in och överföra data måste PHP-agenten vara installerad på servern.

1. När du uppmanas att välja en webbagent klickar du på **PHP**.

1. Följ instruktionerna för att konfigurera PHP-agenten på servern.

   Om du behöver hjälp kan du läsa [New Relic för PHP][3].

1. Kontrollera att kron körs på servern.

   Mer information finns i [Konfigurera och köra cron][5] i utvecklardokumentationen.

## Steg 3: Konfigurera din butik

>[!NOTE]
>Dessa konfigurationsalternativ gäller inte för Adobe Commerce i molninfrastrukturen.
>
>Om du har ett Pro-avtal är New Relic redan [förkonfigurerat och aktiverat som standard](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). Om du har startplaner måste du slutföra de [konfigurationssteg för New Relic](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) som ingår i installationsprocessen.

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_Admin **[!UICONTROL Configuration]**.

1. Välj **[!UICONTROL General]** i den vänstra navigeringspanelen där **[!UICONTROL New Relic Reporting]** är expanderat och gör följande:

   ![New Relic Reporting-konfiguration](./assets/new-relic-reporting-general.png){width="600"}

   * Ange **[!UICONTROL Enable New Relic Integration]** till `Yes`.

   * I **[!UICONTROL Insights API URL]** ersätter du procentsymbolen (`%`) med ditt New Relic konto-ID.

   * Ange din **[!UICONTROL New Relic Account ID]**.

   * Ange din **[!UICONTROL New Relic Application ID]**.

   * Ange din **[!UICONTROL New Relic API Key]**.

   * Ange **[!UICONTROL Insights API Key]**.

1. För **[!UICONTROL New Relic Application Name]** anger du ett namn som identifierar konfigurationen för intern referens.

1. (Valfritt) För **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]** väljer du `Yes` om du vill skicka insamlade data för butiken och administratören som separata appar till New Relic.

   Det här alternativet kräver ett namn angivet för **[!UICONTROL New Relic Application Name]**.

   >[!NOTE]
   >
   >Om du aktiverar den här funktionen minskas antalet [!DNL New Relic]-varningar som är falskt positiva och det går att konfigurera övervakning och varningar med strikt hänsyn till klientens prestanda. New Relic tar emot separata programdatafiler med namnen Application Name (Programnamn) tillagt i `Adminhtml` och FrontLine. Till exempel: `MyStore_Adminhtml`

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Steg 4: Aktivera Cron för [!DNL New Relic]-rapportering

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Cron]**.

   ![New Relic Cron-konfiguration](./assets/new-relic-reporting-cron.png){width="600"}

1. Ange **[!UICONTROL Enable Cron]** till `Yes`.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## [!DNL New Relic] frågor

[!DNL New Relic Insights]-data baseras på satser som är skrivna i [!DNL New Relic Query Language] (NRQL) och eventuella egna parametrar som du kan inkludera. Data kan returneras från ad hoc-frågor eller från frågor som sparats på kontrollpanelen. Mer information finns i [NRQL-referens][6] i [!DNL New Relic]-dokumentationen.

### Administratörshändelser

#### Aktiva administratörsanvändare

Returnerar antalet aktiva Admin-användare.

    SELECT uniqueCount(AdminId)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; SEDAN 15 minuter sedan

#### Aktiva administratörsanvändare

Returnerar namnen på aktiva Admin-användare.

    SELECT uniques(AdminName)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; SEDAN 15 minuter sedan

#### Senaste administratörsaktivitet

Returnerar antalet senaste Admin-åtgärder.

    SELECT count(AdminId)
    FROM Transaction
    WHERE appName =&#39;&lt;ditt_app_name>&#39; FACET AdminName SEDAN 1 dag sedan

#### Senaste administratörsaktivitet

Returnerar detaljinformation om de senaste administratörsåtgärderna, inklusive administratörens användarnamn, varaktighet och programnamn.

    VÄLJ AdminName, duration, name
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; OCH AdminName ÄR INTE NULL
    AND AdminName != &#39;N/A&#39; LIMIT 50

### Cron-händelser

#### Kategoriantal

Returnerar antalet programhändelser per kategori under den angivna tidsperioden.

    SELECT Average(CatalogCategoryCount)
    FROM Cron
    WHERE CatalogCategoryCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minutes

#### Aktuellt antal kataloger

Returnerar det genomsnittliga antalet programhändelser i katalogen per kategori under den angivna tidsperioden.

    SELECT Average(CatalogCategoryCount)
    FROM Cron
    WHERE CatalogCategoryCount IS NOT NULL
    AND CatalogCategoryCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SEDAN 2 minuter sedan LIMIT 1

#### Aktiva produkter

Returnerar antalet programhändelser per produkt under den angivna tidsperioden.

    SELECT Average(CatalogProductActiveCount)
    FROM Cron
    WHERE CatalogProductActiveCount IS NOT NULL
    AND appName = &#39;&lt;ditt_app_name>&#39; TIMESERIES 2 minutes

#### Antal aktiva produkter

Returnerar det genomsnittliga antalet aktiva programhändelser per produkt under den angivna tidsperioden.

    SELECT Average(CatalogProductActiveCount)
    FROM Cron
    WHERE CatalogProductActiveCount IS NOT NULL
    AND CatalogProductActiveCount > 0
    AND appName = &#39;&lt;ditt_app_name>&#39; SEDAN 2 minutes SEDAN LIMIT 1

#### Konfigurerbara produkter

Returnerar det genomsnittliga antalet programhändelser för konfigurerbara produkter under den angivna tidsperioden.

    SELECT Average(CatalogProductConfigurableCount)
    FROM Cron
    DÄR CatalogProductConfigurableCount INTE ÄR NULL
    AND appName = &#39;&lt;ditt_app_name>&#39; TIMESERIES 2 minuter

#### Konfigurerbart produktantal

Returnerar det genomsnittliga antalet programhändelser per konfigurerbar produkt under den angivna tidsperioden.

    SELECT Average(CatalogProductConfigurableCount)
    FROM Cron
    WHERE CatalogProductConfigurableCount IS NOT NULL
    AND CatalogProductConfigurableCount > 0
    AND appName = &#39;&lt;ditt_app_name>&#39; SEDAN 2 minuter sedan LIMIT 1

#### Antal produkter (alla)

Returnerar det totala antalet programhändelser för alla produkter.

    SELECT Average(CatalogProductCount)
    FROM Cron
    WHERE CatalogProductCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minutes

#### Aktuellt produktantal (alla)

Returnerar det genomsnittliga antalet programhändelser för alla produkter under den angivna tidsperioden.

    SELECT Average(CatalogProductCount)
    FROM Cron
    WHERE CatalogProductCount IS NOT NULL
    AND CatalogProductCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SEDAN 2 minuter sedan LIMIT 1

#### Kundantal

Returnerar det genomsnittliga antalet programhändelser per kund.

    VÄLJ medel(CustomerCount)
    FRÅN KRON
    DÄR CustomerCount INTE ÄR NULL
    OCH CustomerCount > 0&lt;
    AND appName = &#39;&lt;ditt_app_name>&#39; TIDSERVAR 2 minuter

#### Aktuellt kundantal

Returnerar det genomsnittliga antalet kunder under den angivna tidsperioden.

    VÄLJ medel(CustomerCount)
    FROM Cron
    DÄR CustomerCount INTE ÄR NULL
    OCH CustomerCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SEDAN 2 minuter sedan BEGRÄNSNING 1

#### Modulstatus

Returnerar det genomsnittliga antalet gånger som programmoduler aktiveras, inaktiveras eller installeras under den angivna tidsperioden.

    SELECT-genomsnitt(ModulesDisabled), medel(ModulesEnabled), medel
    (ModulesInstalled)
    FROM Cron&lt;
    WHERE appName = &#39;&lt;ditt_app_name>&#39; TIMESERIES 2 minuter

#### Aktuell modulstatus

Returnerar det genomsnittliga antalet gånger moduler aktiverades, inaktiverades eller installerades under den angivna tidsperioden.

    SELECT-genomsnitt(ModulesDisabled), medel(ModulesEnabled), medel
    (ModulesInstalled)
    FROM Cron
    WHERE appName = &#39;&lt;ditt_app_name>&#39; SEDAN 2 minuter sedan LIMIT 1

#### Antal webbplatser och butiker

Returnerar det genomsnittliga antalet programhändelser per webbplats och butik under den angivna tidsperioden.

    SELECT Average(StoreViewCount), Average(WebsiteCount)
    FROM Cron
    WHERE appName = &#39;&amp;lt;your_app_name&amp;gt;&#39; TIMESERIES 2 minuter

#### Aktuellt antal webbplatser och butiker

Returnerar det genomsnittliga antalet aktuella programhändelser under den angivna tidsperioden.

    SELECT Average(StoreViewCount), Average(WebsiteCount)
    FROM Cron
    WHERE appName = &#39;&lt;ditt_app_name>&#39; SEDAN 2 minuter sedan LIMIT 1

#### Cron - alla data från händelse

Returnerar alla data för programhändelser.

    SELECT *
    FROM Cron
    WHERE appName = &#39;&lt;ditt_appnamn>&#39;

### Kunder

#### Antal aktiva kunder

Returnerar antalet aktiva kunder under den angivna tidsperioden.

    SELECT uniqueCount(CustomerId)
    FROM Transaction
    WHERE appName = &#39;&lt;ditt_app_name>&#39; SEDAN 15 minuter sedan

#### Aktiva kunder

Returnerar namnen på aktiva kunder under den angivna tidsperioden.

    SELECT uniques(CustomerName)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; SEDAN 15 minuter sedan

#### De vanligaste kunderna

Returnerar de främsta kunderna under den angivna tidsperioden.

    SELECT count(CustomerId)
    FROM Transaction
    WHERE appName = &#39;&lt;ditt_app_name>&#39; FACET CustomerName SEDAN 1 dag sedan

#### Senaste administratörsaktivitet

Returnerar ett definierat antal poster för den senaste aktiviteten, som innehåller kundens namn och besökets längd.

    VÄLJ CustomerName, duration, name
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39;
    OCH CustomerName ÄR INTE NULL
    OCH CustomerName != &#39;N/A&#39; LIMIT 50

### Beställningar

#### Antal beställningar

Returnerar antalet order som placerats under den angivna tidsperioden.

    SELECT count(Order)
    FROM Transaction SEINCE 1 day ago

#### Totalt ordervärde

Returnerar det totala antalet radartiklar som beställts under den angivna tidsperioden.

    SELECT sum(orderValue)
    FROM Transaction SEDAN 1 dag sedan

#### Totalt antal beställda radartiklar

Returnerar det totala antalet radartiklar som beställts under den angivna tidsperioden.

    SELECT sum(lineItemCount)
    FROM Transaction SEDAN 1 dag sedan


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
