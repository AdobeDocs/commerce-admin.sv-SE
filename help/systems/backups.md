---
title: Säkerhetskopiering av system
description: Lär dig hur du skapar och schemalägger systemsäkerhetskopieringar, inklusive filsystem, databaser och mediefiler.
exl-id: 3a9655c1-c124-42be-a487-b31404dada90
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Säkerhetskopiering av system

Med Adobe Commerce och Magento Open Source kan du säkerhetskopiera olika delar av systemet - t.ex. filsystemet, databasen och mediefiler - och återställa automatiskt. En post för varje säkerhetskopia visas i rutnätet på _Säkerhetskopior_ sida. Om du tar bort en post från listan tas även den arkiverade filen bort. Säkerhetskopieringsfiler för databaser komprimeras med GZ-format. TGZ-formatet används för systemsäkerhetskopieringar och databas- och mediesäkerhetskopieringar. Som en god vana bör du begränsa åtkomsten till säkerhetskopieringsverktygen och säkerhetskopiera innan du installerar tillägg och uppdateringar.

- **Begränsa åtkomsten till verktygen för säkerhetskopiering.** Åtkomsten till verktygen för säkerhetskopiering och återställning kan begränsas genom att konfigurera [användarroller](permissions-user-roles.md) för säkerhetskopiering och återställning. Om du vill begränsa åtkomsten låter du motsvarande kryssruta vara avmarkerad. Om du vill ha åtkomst till resurser för återställning måste du även ge åtkomst till resurser för säkerhetskopiering.

- **Säkerhetskopiera innan du installerar tillägg och uppdateringar.** Säkerhetskopiera alltid innan du installerar ett tillägg eller en uppdatering.

{{$include /help/_includes/backups-note.md}}

## Aktivera och schemalägg säkerhetskopiering

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL System]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Backup Settings]**.

1. Ange **[!UICONTROL Enabled Schedule Backup]** till `Yes`.

1. Om du vill schemalägga automatiska korrigeringar anger du schemaläggningsalternativen:

   - Ange **[!UICONTROL Enabled Schedule Backup]** till `Yes`.
   - Ange **[!UICONTROL Scheduled Backup Type]** till den typ av säkerhetskopiering som ska köras vid det schemalagda intervallet.
   - Ange **[!UICONTROL Start Time]** till den tidpunkt på dagen då säkerhetskopieringen ska utföras.
   - Ange **[!UICONTROL Frequency]** till `Daily`, `Weekly`, eller `Monthly`.
   - Ange **[!UICONTROL Maintenance Mode]** till `Yes`.

   ![Avancerad konfiguration - säkerhetskopiering](../configuration-reference/advanced/assets/system-scheduled-backup-settings.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Skapa en säkerhetskopia

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Backups]**.

1. Klicka i det övre högra hörnet på den typ av säkerhetskopia som du vill skapa:

   - **[!UICONTROL System Backup]** - Skapar en fullständig säkerhetskopiering av databasen och filsystemet. Under processen kan du välja att ta med mediemappen i säkerhetskopian.

   - **[!UICONTROL Database and Media Backup]** - Skapar en säkerhetskopia av databasen och mediamappen.

   - **[!UICONTROL Database Backup]** - Skapar en säkerhetskopia av databasen.

   ![Systemverktyg - säkerhetskopiering](./assets/tools-backups.png){width="600" zoomable="yes"}

1. Markera kryssrutan om du vill försätta arkivet i underhållsläge under säkerhetskopieringen.

   När säkerhetskopieringen är klar stängs underhållsläget av automatiskt.

1. För en systemsäkerhetskopiering väljer du **[!UICONTROL Include Media folder to System Backup]** om du vill inkludera mediamappen.

1. Bekräfta åtgärden när du uppmanas att göra det.


