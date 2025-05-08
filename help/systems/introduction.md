---
title: Introduktion till administratörssystem
description: Lär dig mer om de systemverktyg och funktioner som butiksadministratören kan använda för att hantera webbplatser, data, integreringar och admin-användare på ett effektivt sätt.
exl-id: 52792a89-8f6f-4230-9a04-e193b3943410
source-git-commit: 51c8b526e1f03e65ad71eb00ec3cdf82365bd33c
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---

# Introduktion till administratörssystem

Butiksadministratören är det säkra back office där handlare ställer in produkter och kampanjer, hanterar beställningar och utför andra administrativa uppgifter. Alla grundläggande konfigurationsuppgifter och lagringshanteringsåtgärder utförs från administratören. Det finns också funktioner som ger stöd för flera olika butiksfunktioner som administratörer kan hantera för sina organisationer.

## Variabler och kundkommunikation

Variabler är information som kan skapas en gång och användas på flera platser. Butiken innehåller många fördefinierade variabler som enkelt kan användas för att anpassa mallar för [e-post](email-templates.md) och [nyhetsbrev](../merchandising-promotions/newsletter-template.md) samt andra typer av [innehåll](../content-design/introduction.md#content). Du kan också skapa anpassade variabler för att inkludera information som är specifik för dina behov.

- [Fördefinierade variabler](variables-predefined.md)
- [Anpassade variabler](variables-custom.md)

En av uppgifterna du bör utföra innan du lanserar din butik är att granska e-postmallarna som används för all kommunikation som skickas från din butik för att se till att de speglar ditt varumärke. Detta inkluderar anpassning av e-postmallar och [nyhetsbrevmallar](../merchandising-promotions/newsletter-template.md) samt PDF fakturor och följesedlar. Det omfattar även att anpassa innehållet med variabler och [markup-taggar](markup-tags.md).

## Driftshantering

Administratören stöder även olika uppgifter för systemadministratörer som kan hantera administratörsanvändare inom organisationen och hantera butiken. De innehåller följande verktyg:

- **Administratörsanvändarkonton och behörigheter** - Hantera administratörsanvändarkonton [&#128279;](permissions-users-all.md), samt associerade [roller och behörigheter](permissions-user-roles.md) som styr deras åtkomst till platser och funktionsområden i administratören.
- **Administratörssessioner och webbplatsbegränsningar** - Granska [säkerheten](security.md) och lär dig hantera administratörssessioner och autentiseringsuppgifter, implementera CAPTCHA och hantera webbplatsbegränsningar.
- **Systemverktyg** - Utför rutinmässiga [index](index-management.md)- och [cache](cache-management.md)-hanteringsåtgärder, [säkerhetskopiera](backups.md) systemet, hantera [schemalagda åtgärder](data-scheduled-import-export.md) och använd ett sortiment av [utvecklingsverktyg](developer-tools.md).
- **Dataöverföring** - Använd [dataöverföringsverktygen](data-transfer.md) för att importera och exportera data, samt för att hantera produkt-, prissättnings-, kund- och momsdata.
- **Integrationer** - Ange platsen för OAuth-autentiseringsuppgifter och omdirigerings-URL för [tredjepartsintegreringar](integrations.md) och identifiera tillgängliga API-resurser.
- **Åtgärdsloggar** - ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Åtkomst till posterna ([åtgärdsloggar](action-log.md)) för ändringar gjorda av administratörsanvändare som arbetar i din butik.
- **Supportverktyg** - ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) [Systemrapporter](support.md#access-system-reports) är utformade för att identifiera kända fel i systemet. De kan användas som en resurs under utvecklings- och optimeringsprocesserna och som ett diagnostiskt verktyg som hjälper vårt supportteam att identifiera och lösa problem.
