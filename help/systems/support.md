---
title: Supportverktyg
description: Lär dig mer om de supportverktyg du kan använda för att identifiera problem i systemet.
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
source-git-commit: e05d13f79ceb2fe24c1931fefb48317ebd36d1fc
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 0%

---

# Supportverktyg

{{ee-feature}}

Supportverktygen är utformade för att identifiera kända fel i systemet. De kan användas som en resurs under utvecklings- och optimeringsprocesserna och som ett diagnostiskt verktyg som hjälper vårt supportteam att identifiera och lösa problem.

## Systemrapporter

Systemrapporteringsverktyget ger dig möjlighet att ta regelbundna, fullständiga eller delvisa ögonblicksbilder av systemet och spara dem för framtida referens. Du kan jämföra prestandainställningar före och efter kodutvecklingscykler eller ändringar av serverinställningarna. Systemrapporteringsverktyget kan dramatiskt minska tiden för förberedelse och inlämning av den information som supporten behöver för att inleda en utredning.

I stödrastret Systemrapporter kan du visa och hämta befintliga rapporter, ta bort rapporter och skapa rapporter.

### Åtkomst till systemrapporter

Gå till **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**&#x200B;på sidofältet_ Admin _.

![Admin - systemrapporter](./assets/reports.png){width="600" zoomable="yes"}

### Generera en rapport

1. Klicka på **[!UICONTROL New Report]**.

1. I listan **[!UICONTROL Groups]** väljer du varje uppsättning med information som du vill ta med i rapporten. Som standard är alla grupper markerade.

   ![Systemrapport - välj grupper](./assets/report-create.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Create]** i det övre högra hörnet.

   Det kan ta några minuter innan rapporten genereras, beroende på hur många rapporttyper som har valts. När rapporten är klar visas den högst upp i rutnätet med genererat datum och genererad tid.

### Visa modulinformation

Du hittar användbar information om installerade moduler.

**_Så här visar du rapportinformation för varje installerad modul:_**

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**&#x200B;på sidofältet_ Admin _.
1. Klicka på **[!UICONTROL New Report]**.
1. Välj `Modules` i listan **[!UICONTROL Groups]**.
1. Klicka på **[!UICONTROL Create]**.
1. När rapporten har genererats klickar du på **[!UICONTROL Select]** och sedan på **[!UICONTROL View]** för att se alla modulversioner.
1. Klicka på **[!UICONTROL Download]** om du vill hämta rapporten.

### Hantera systemrapporter

Välj något av följande i kolumnen **[!UICONTROL Action]** i rutnätet:

- `View` - Använd den här funktionen om du vill visa information om rapporten.
- `Delete` - Använd den här funktionen för att ta bort den genererade rapporten från listan.
- `Download` - Använd den här funktionen om du vill spara rapporten som en HTML-fil.

### Visa systemrapportinformation

1. För den rapport du behöver väljer du **[!UICONTROL View]** i kolumnen _[!UICONTROL Actions]_.

1. Expandera ![Expanderingsväljaren](../assets/icon-display-expand.png) i den vänstra panelen för att visa detaljerna.

   ![Allmän systemrapportinformation](./assets/report-information.png){width="600" zoomable="yes"}

### Tillgängliga systemrapporter

| Rapportgrupp | Information ingår |
| ------------ | -------------------- |
| [!UICONTROL General] | Adobe Commerce-version<br>Dataantal<br>Cachestatus<br>Indexstatus |
| [!UICONTROL Environment] | Miljöinformation<br>MySQL-status |
| [!UICONTROL Data] | Duplicera kategorier efter URL-nyckel<br>Duplicera produkter efter URL-nyckel<br>Duplicera produkter efter SKU<br>Duplicera beställningar med hjälp av ID<br>Duplicera användare via e-post<br>Skadade kategoridata |
| [!UICONTROL Modules] | Lista över anpassade moduler<br>Lista över inaktiverade moduler<br>Lista över alla moduler |
| [!UICONTROL Configuration] | Konfiguration<br>Data från `app/etc/env.php`<br>leveransmetoder<br>Betalningsmetoder<br>Betalningsfunktionalitetsmatris |
| [!UICONTROL Logs] | Loggfiler<br>De vanligaste systemmeddelandena<br>De vanligaste systemmeddelandena<br>De vanligaste felsökningsmeddelandena<br>Dagens populäraste felsökningsmeddelanden<br>De vanligaste undantagen<br>Dagens vanligaste undantagsmeddelanden |
| [!UICONTROL Attributes] | Användardefinierade EAV-attribut<br>Nya EAV-attribut<br>Entitetstyper<br>Alla EAV-attribut<br>Kategori EAV-attribut<br>EAV-attribut för produkt<br>EAV-attribut för kund<br>EAV-attribut för kundadress<br>EAV-attribut för RMA-objekt |
| [!UICONTROL Events] | Anpassade globala händelser<br>Anpassade administrationshändelser<br>Anpassade fronthändelser<br>Anpassade dokumenthändelser<br>Anpassade Crontab-händelser<br>Anpassade REST-händelser<br>Anpassade SOAP-händelser<br>Centrala globala händelser<br>Viktiga administratörshändelser<br>Kärnincidenter<br>Kärnincidenter<br>Kärnincidenter<br>Core REST-händelser<br>Centrala SOAP-händelser<br>Alla globala händelser<br>Alla administrationshändelser<br>Alla frontend-händelser<br>Alla dokumenthändelser<br>Alla REST-händelser<br>Alla SOAP-händelser<br>Alla Crontab-händelser |
| [!UICONTROL Cron] | Kronscheman efter statuskod<br>Kronscheman efter jobbkod<br>Fel i kön för kronischeman<br>Lista över kronischeman<br>anpassade globala kronijobb<br>Anpassade konfigurerbara kronijobb<br>Core Global cron Jobs<br>Core Configurable Cron Jobs<br>Alla globala kron-jobb<br>Alla konfigurerbara kronijobb s |
| [!UICONTROL Design] | Lista med Administrativa teman<br>Skapa lista med befintliga teman |
| [!UICONTROL Stores] | Webbplatsträd<br>Lista över webbplatser<br>Lagrar lista<br>Lista över butiksvyer |
| OMS-anslutning <br>_(synlig med OMS-integrering)_ | Anslutningsversion<br>Anslutningsövervakning<br>Resultat av meddelandebearbetning |

{style="table-layout:auto"}
