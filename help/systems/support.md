---
title: Supportverktyg
description: Lär dig mer om de supportverktyg du kan använda för att identifiera problem i systemet.
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
source-git-commit: 97eeb733836f0336401664c5cfb3df2b9f2f2ccf
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# Supportverktyg

{{ee-feature}}

Supportverktygen är utformade för att identifiera kända fel i systemet. De kan användas som en resurs under utvecklings- och optimeringsprocesserna och som ett diagnostiskt verktyg som hjälper vårt supportteam att identifiera och lösa problem.

## Datainsamlare

Datainsamlaren samlar in den information om ditt system som vårt supportteam behöver för att felsöka problem med din Adobe Commerce-installation. Säkerhetskopian som skapas tar flera minuter att slutföra och innehåller både kod och databasdump. Data kan exporteras till en CSV- eller Excel XML-fil.

![System - Datainsamling](./assets/data-collector.png){width="600" zoomable="yes"}

### Kör datainsamlaren

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Klicka på i det övre högra hörnet **[!UICONTROL New Backup]**.

   Det tar några minuter att generera säkerhetskopian. Du kan övervaka resultatet av bearbetningen genom att klicka **[!UICONTROL Refresh Status]**. När du är klar visas säkerhetskopian i _[!UICONTROL Data Collector]_rutnät.

1. Så här visar du en logg med säkerhetskopieringsinformation:

   - I _[!UICONTROL Action]_kolumn, markera **[!UICONTROL Show Log]**.

   - Klicka **[!UICONTROL Back]** för att gå tillbaka till rutnätet.

   ![datainsamlingslogg](./assets/data-collector-log.png){width="600" zoomable="yes"}

### Exportera säkerhetskopieringsdata

1. I den första kolumnen markerar du kryssrutan för den säkerhetskopia som ska exporteras.

1. Använd **[!UICONTROL Export]** för att välja exportdatas format.

   ![Exportformat](./assets/data-collector-export.png){width="600" zoomable="yes"}

1. Få åtkomst till filen via webbläsarens nedladdningsplats och **[!UICONTROL Save]** den.

### Hämta säkerhetskopieringsdata

När säkerhetskopieringen har skapats kan du hämta en kopia av kod- och databasdata.

1. Hitta den säkerhetskopieringsenhet som behövs i rutnätet.

1. Se till att den har en `Complete` status.

1. Klicka på enhetsnamnet i _[!UICONTROL Code Dump]_eller_[!UICONTROL DB Dump]_ kolumner.

Hämtningsprocessen bör starta automatiskt.

## Ta bort säkerhetskopieringsdata

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Sök efter och markera de säkerhetskopierade data som ska tas bort.

1. I _[!UICONTROL Action]_kolumn, klicka **[!UICONTROL Delete]**.

1. Bekräfta åtgärden genom att klicka **[!UICONTROL OK]**.

## Systemrapporter

Systemrapporteringsverktyget ger dig möjlighet att ta regelbundna, fullständiga eller delvisa ögonblicksbilder av systemet och spara dem för framtida referens. Du kan jämföra prestandainställningar före och efter kodutvecklingscykler eller ändringar av serverinställningarna. Systemrapporteringsverktyget kan dramatiskt minska tiden för förberedelse och inlämning av den information som supporten behöver för att inleda en utredning.

I stödrastret Systemrapporter kan du visa och hämta befintliga rapporter, ta bort rapporter och skapa rapporter.

### Åtkomst till systemrapporter

På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![Administratör - systemrapporter](./assets/reports.png){width="600" zoomable="yes"}

### Generera en rapport

1. Klicka på **[!UICONTROL New Report]**.

1. I **[!UICONTROL Groups]** väljer du varje uppsättning med information som du vill ta med i rapporten. Som standard är alla grupper markerade.

   ![Systemrapport - välj grupper](./assets/report-create.png){width="600" zoomable="yes"}

1. Klicka på i det övre högra hörnet **[!UICONTROL Create]**.

   Det kan ta några minuter innan rapporten genereras, beroende på hur många rapporttyper som har valts. När rapporten är klar visas den högst upp i rutnätet med genererat datum och genererad tid.

### Visa modulinformation

Du hittar användbar information om installerade moduler.

**_Så här visar du rapportinformation för varje installerad modul:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. Klicka på **[!UICONTROL New Report]**.
1. Välj `Modules` från **[!UICONTROL Groups]** lista.
1. Klicka på **[!UICONTROL Create]**.
1. När rapporten har skapats klickar du på **[!UICONTROL Select]** och sedan **[!UICONTROL View]** om du vill se alla modulversioner.
1. Klicka **[!UICONTROL Download]** för att ladda ned rapporten.

### Hantera systemrapporter

I **[!UICONTROL Action]** markerar du något av följande i rutnätskolumnen:

- `View` - Använd den här funktionen om du vill visa information om rapporten.
- `Delete` - Använd den här funktionen om du vill ta bort den genererade rapporten från listan.
- `Download` - Med den här funktionen sparar du rapporten som en HTML-fil.

### Visa systemrapportinformation

1. För rapporten du behöver väljer du **[!UICONTROL View]** i _[!UICONTROL Actions]_kolumn.

1. Expandera på den vänstra panelen ![Expansionsväljare](../assets/icon-display-expand.png) varje avsnitt i rapporten för att visa detaljerna.

   ![Allmän systemrapportinformation](./assets/report-information.png){width="600" zoomable="yes"}

### Tillgängliga systemrapporter

| Rapportgrupp | Information ingår |
| ------------ | -------------------- |
| [!UICONTROL General] | Adobe Commerce Version<br>Antal data<br>Cachestatus<br>Indexstatus |
| [!UICONTROL Environment] | Miljöinformation<br>MySQL-status |
| [!UICONTROL Data] | Duplicera kategorier efter URL-nyckel<br>Duplicera produkter efter URL-nyckel<br>Duplicera produkter efter SKU<br>Duplicera order med öknings-ID<br>Duplicera användare via e-post<br>Skadade kategoridata |
| [!UICONTROL Modules] | Lista med anpassade moduler<br>Lista över inaktiverade moduler<br>Alla modullistor |
| [!UICONTROL Configuration] | Konfiguration<br>Data från `app/etc/env.php`<br>Leveransmetoder<br>Betalningsmetoder<br>Betalningsfunktionalitetsmatris |
| [!UICONTROL Logs] | Loggfiler<br>Viktiga systemmeddelanden<br>Dagens populäraste systemmeddelanden<br>Vanliga felsökningsmeddelanden<br>Dagens populäraste felsökningsmeddelanden<br>De vanligaste undantagsmeddelandena<br>Dagens viktigaste undantagsmeddelanden |
| [!UICONTROL Attributes] | Användardefinierade EAV-attribut<br>Nya EAV-attribut<br>Enhetstyper<br>Alla EAV-attribut<br>EAV-attribut för kategori<br>EAV-attribut för produkt<br>EAV-attribut för kund<br>EAV-attribut för kundadress<br>EAV-attribut för RMA-objekt |
| [!UICONTROL Events] | Anpassade globala händelser<br>Anpassade administrationshändelser<br>Anpassade frontend-händelser<br>Anpassade dokumenthändelser<br>Anpassade Crontab-händelser<br>Anpassade REST-händelser<br>Anpassade SOAP-händelser<br>Globala händelser<br>Core Admin Events<br>Core FrontEnd-händelser<br>Core Doc Events<br>Core Crontab Events<br>Core REST Events<br>Core SOAP Events<br>Alla globala händelser<br>Alla administrationshändelser<br>Alla frontend-händelser<br>Alla dokumenthändelser<br>Alla REST-händelser<br>Alla SOAP-händelser<br>Alla Crontab-händelser |
| [!UICONTROL Cron] | Cron Schedules efter statuskod<br>Cron Schedules per jobbkod<br>Fel i Cron Schedules-kö<br>Cron Schedules List<br>Anpassade globala kundprojekt<br>Anpassade konfigurerbara kron-jobb<br>Core Global Cron Jobs<br>Core Configurable Cron Jobs<br>Alla globala kreditjobb<br>Alla konfigurerbara kronijobb |
| [!UICONTROL Design] | Lista med administrationsteman<br>Lista med färdiga teman |
| [!UICONTROL Stores] | Webbplatsträd<br>Webbplatslista<br>Lagringslista<br>Lista över butiksvyer |
| OMS-anslutning <br>_(synlig med OMS-integrering)_ | Kopplingsversion<br>Anslutningsövervakning<br>Resultat av meddelandebearbetning |

{style="table-layout:auto"}
