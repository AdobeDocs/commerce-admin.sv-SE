---
title: Säkerhetskopiering av system
description: Lär dig hur du skapar och schemalägger systemsäkerhetskopieringar, inklusive filsystem, databaser och mediefiler.
exl-id: 3a9655c1-c124-42be-a487-b31404dada90
feature: System, Configuration
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---

# Säkerhetskopiering av system

Med Adobe Commerce och Magento Open Source kan du säkerhetskopiera olika delar av systemet - t.ex. filsystemet, databasen och mediefiler - och återställa automatiskt. En post för varje säkerhetskopiering visas i rutnätet på sidan _Säkerhetskopior_. Om du tar bort en post från listan tas även den arkiverade filen bort. Säkerhetskopieringsfiler för databaser komprimeras med GZ-format. TGZ-formatet används för systemsäkerhetskopieringar och databas- och mediesäkerhetskopieringar. Som en god vana bör du begränsa åtkomsten till säkerhetskopieringsverktygen och säkerhetskopiera innan du installerar tillägg och uppdateringar.

- **Begränsa åtkomsten till verktyg för säkerhetskopiering.** Åtkomsten till verktygen för säkerhetskopiering och återställning kan begränsas genom att [användarroller](permissions-user-roles.md) konfigureras för resurser för säkerhetskopiering och återställning. Om du vill begränsa åtkomsten låter du motsvarande kryssruta vara avmarkerad. Om du vill ha åtkomst till resurser för återställning måste du även ge åtkomst till resurser för säkerhetskopiering.

- **Säkerhetskopiera innan du installerar tillägg och uppdateringar.** Utför alltid en säkerhetskopiering innan du installerar ett tillägg eller en uppdatering.

{{$include /help/_includes/backups-note.md}}

## Aktivera och schemalägg säkerhetskopiering

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_&#x200B;Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Advanced]** i den vänstra panelen och välj **[!UICONTROL System]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) och **[!UICONTROL Backup Settings]**.

1. Ange **[!UICONTROL Enabled Schedule Backup]** till `Yes`.

1. Om du vill schemalägga automatiska korrigeringar anger du schemaläggningsalternativen:

   - Ange **[!UICONTROL Enabled Schedule Backup]** till `Yes`.
   - Ange **[!UICONTROL Scheduled Backup Type]** till den typ av säkerhetskopiering som ska köras vid det schemalagda intervallet.
   - Ange **[!UICONTROL Start Time]** till den tidpunkt på dagen då säkerhetskopieringen ska köras.
   - Ange **[!UICONTROL Frequency]** till `Daily`, `Weekly` eller `Monthly`.
   - Ange **[!UICONTROL Maintenance Mode]** till `Yes`.

   ![Avancerad konfiguration - säkerhetskopior](../configuration-reference/advanced/assets/system-scheduled-backup-settings.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Skapa en säkerhetskopia

1. Gå till _>_ > **[!UICONTROL System]** på sidofältet _[!UICONTROL Tools]_&#x200B;Admin **[!UICONTROL Backups]**.

1. Klicka i det övre högra hörnet på den typ av säkerhetskopia som du vill skapa:

   - **[!UICONTROL System Backup]** - Skapar en fullständig säkerhetskopia av databasen och filsystemet. Under processen kan du välja att ta med mediemappen i säkerhetskopian.

   - **[!UICONTROL Database and Media Backup]** - Skapar en säkerhetskopia av databasen och mediamappen.

   - **[!UICONTROL Database Backup]** - Skapar en säkerhetskopia av databasen.

   ![Systemverktyg - säkerhetskopior](./assets/tools-backups.png){width="600" zoomable="yes"}

1. Markera kryssrutan om du vill försätta arkivet i underhållsläge under säkerhetskopieringen.

   När säkerhetskopieringen är klar stängs underhållsläget av automatiskt.

1. För en systemsäkerhetskopiering markerar du kryssrutan **[!UICONTROL Include Media folder to System Backup]** för att inkludera mediamappen.

1. Bekräfta åtgärden när du uppmanas att göra det.



<!-- Last updated from includes: 2023-02-22 09:59:54 -->
