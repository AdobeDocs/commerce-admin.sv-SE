---
title: Administratörsbehörigheter
description: Lär dig mer om administratörens användarkonton och hur roller används för att ge åtkomst till butikshanteringsfunktioner.
exl-id: 54e4a322-4747-4472-b60b-cfe84c109f86
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Administratörsbehörigheter

Adobe Commerce och Magento Open Source använder roller och behörigheter för att skapa olika åtkomstnivåer för administratören. När din butik konfigureras för första gången får du en uppsättning inloggningsuppgifter för administratörsrollen som har fullständig behörighet. Du kan dock begränsa behörighetsnivån baserat på&quot;behov att känna till&quot; för andra personer som arbetar på din webbplats. En medlem i ett designteam kan till exempel bara få tillgång till innehållsdesignverktygen, men inte till områden med kund- och orderinformation.

Dessutom kan du begränsa administratörsåtkomsten ytterligare till endast en viss plats eller en uppsättning webbplatser och tillhörande data. Om du har flera varumärken eller affärsenheter med separata butiker i samma Commerce-installation kan du ge administratörsåtkomst till varje affärsenhet men dölja och skydda deras data från andra Admin-användare.

När en administratörsanvändares åtkomst är begränsad till en viss webbplats eller butik visas de där de inte är auktoriserade inte eller visas nedtonade. Endast säljdata och andra data för tillåtna webbplatser och butiker visas för användaren.

- ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Som standard loggar systemet automatiskt (registrerar) alla åtgärder som en användare utför när ändringar görs i en butik. Administratörsåtgärder kan granskas i [Åtgärdsloggsrapport](action-log-report.md). Konfigurera inloggning [Loggning av administratörsåtgärder](action-log.md) i butikens avancerade administratörsinställningar.

![Administratör - alla användarkonton](./assets/users-all.png){width="700" zoomable="yes"}
