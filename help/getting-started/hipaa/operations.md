---
title: Operationer
description: Riktlinjer för migrering till ett HIPAA-klart erbjudande och användning av den sekundära mellanlagringsmiljön för felsökning.
exl-id: 058b43de-1cee-4557-b2e3-87ee7422bf9b
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 77e7eb00e9f8d5af6361059c287707993180c4c4
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Operationer

Använd de här riktlinjerna om du vill lära dig mer om hur du migrerar till det HIPAA-klara erbjudandet för Adobe Commerce och om hur du använder `staging_for_support`-miljön för felsökning.

## Migrering

Kunder som migrerar från ett icke-HIPAA Commerce-erbjudande till ett HIPAA-klart erbjudande måste följa följande riktlinjer:

1. **Ta bort befintliga datamängder**: Före migreringen måste alla befintliga datamängder tas bort för att förhindra att känsliga och icke-känsliga data kombineras i Adobe Commerce SaaS-lagret. Skapa en supportbiljett för att ta bort dina dataspaces.
1. **Konfigurera ny miljö**: [Installationen av Commerce Services Connector](https://experienceleague.adobe.com/sv/docs/commerce/user-guides/integration-services/saas) i den nya HIPAA Commerce-instansen bör konfigureras först efter att datamängderna har tagits bort. Den nya SaaS-miljön för HIPAA bör endast användas efter att de gamla dataspaces har tagits bort. Installationen av Commerce Services Connector aktiverar automatiskt skapandet av nya SaaS-dataspaces.
1. **Migreringsstrategi**: Borttagningen av SaaS-dataspaces är en oåterkallelig process och tar bort alla katalogdata och relaterade konfigurationer. Det måste finnas en migreringsstrategi om du vill överföra några av dina gamla data eller konfigurationer. Handlaren ansvarar för denna strategi. En supportbiljett för borttagning av befintliga datamängder bör skapas först när säkerhetskopieringen av migreringsdata (om tillämpligt) har slutförts.

>[!NOTE]
>Om du vill ta bort befintliga datamängder måste du skapa en Adobe Commerce Support-biljett med namnet&quot;HIPAA Migration: Delete SaaS dataspaces&quot;, ange deras `MAGEID` och ange de projekt-ID:n för SaaS som behöver tas bort.

## Felsökning med Adobe Commerce Support

Adobe Commerce HIPAA-erbjudande innehåller ytterligare en `staging_for_support`-miljö som kan användas av Adobe Commerce supportteam i felsökningssyfte.

Kunderna måste se till att `staging_for_support`-miljön:

- Innehåller inga känsliga data, som, men inte begränsat till, Skyddad hälsoinformation (PHI).
- Får inte användas för någon produktionsverksamhet.
- Du får inte ange ett annat namn än `staging_for_support` för att undvika förvirring.
- Uppdateras med både kod och konfiguration från produktionsmiljön för att säkerställa att felsökningen utförs i en miljö som ligger så nära produktionen som möjligt.

## Commerce-tjänster

- **Commerce-tjänster som inte är HIPAA-klara** - Kunder får inte använda Adobe Commerce-tjänster, till exempel Live Search, Produktrekommendationer, Betalningstjänster, Försäljningskanaler eller Commerce Intelligence eftersom de inte är HIPAA-klara. Kunder bör endast använda [HIPAA-förberedda tjänster](overview.md).

- **Dataanslutning** - Endast den bakomliggande kontors-samlaren i tillägget [Dataanslutning](https://experienceleague.adobe.com/sv/docs/commerce/data-connection/overview) är HIPAA-klar. Kunder bör inte skicka PHI till dataanslutningstjänster som inte är HIPAA-förberedda, som butikshändelser och Audience Activation. Kunderna måste se till att datainsamlingen för butiken är inaktiverad.

- **Katalogtjänsten** - Enligt design bearbetar inte [katalogtjänsten](https://experienceleague.adobe.com/sv/docs/commerce/catalog-service/overview) PHI, vilket innebär att den inte omfattas av beredskapsgranskningen och kompatibiliteten för HIPAA. Kunderna ansvarar för att säkerställa att de använder denna tjänst baserat på sin egen utvärdering av användningsfall och i samråd med jurister. Kunder bör inte heller använda katalogtjänsten via den federerade tjänsten för att undvika risken att skicka PHI till icke-HIPAA-klara tjänster.

- **SaaS-dataexport** - Tjänsten [SaaS-dataexport](https://experienceleague.adobe.com/sv/docs/commerce/saas-data-export/overview) bör konfigureras så att den endast skickar data för HIPAA-komponenter i Adobe Commerce.
