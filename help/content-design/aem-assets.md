---
title: Experience Manager Assets Integration för Commerce
description: Lär dig hur du integrerar Experience Manager Assets med din [!DNL Commerce] -instans för att få tillgång till ett oändligt antal mediefiler som kan användas i din butik.
feature: CMS, Media, Configuration, Integration
source-git-commit: d91ba86b77ef91e849d1737628b575f2309376b8
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# Experience Manager Assets Integration för Commerce

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Integrationen mellan Commerce och Adobe Experience Manager (AEM) Assets kombinerar AEM robusta funktioner som ett DAM-system (Digital Asset Management) med Adobe Commerce för att förbättra e-handelsupplevelsen. Denna integrering utnyttjar AEM kraftfulla funktioner för resurshantering för att ge ett smidigt, skalbart och effektivt sätt att hantera och leverera resurser i butiker.

**Viktiga funktioner**

- **Centraliserad resurshantering**

   - **AEM Assets som Single Source of Truth**-AEM Assets fungerar som central lagringsplats för alla digitala resurser och ser till att alla e-handelsplattformar har tillgång till varumärkesanpassade, godkända mediefiler.

   - **Massresurshantering**-Organisationer kan hantera stora volymer resurser effektivt tack vare AEM robusta resurshanteringsfunktioner. Detta gör att marknadsförare och handlare kan kartlägga stora mängder bilder för nya produktlinjer effektivt.

- **Personaliserade Commerce-upplevelser**-Med GenAI-tjänster i AEM kan organisationer generera miljontals produktvariationer för personaliserade e-handelsupplevelser. Marknadsförare och handlare kan använda dessa bilder för att skapa dynamiska butiker för produktlanseringar och säsongskampanjer, vilket ökar engagemanget och ökar konverteringsgraden.

- **Automatiserad resursmatchning**-Integreringen innehåller en regelmotortjänst som automatiskt matchar resurser i AEM med produkter i Adobe Commerce baserat på SKU eller andra nyckelattribut. Tjänsten ser till att de senaste produktresurserna och variationerna alltid är tillgängliga i e-butiker. Det minskar också den manuella arbetsinsatsen som krävs för att hantera resurser och frigör tid för mer strategiska aktiviteter.

- **Effektivare processer**
   - **Aktivera och konfigurera integreringen från Commerce Admin**-Administratörer och utvecklare kan installera och konfigurera integreringen från Adobe Commerce med välbekanta verktyg och processer.
   - **Dynamiska uppdateringar**-Håll produktbilderna aktuella med de senaste ändringarna i resurshanteringssystemet. Dessa automatiska uppdateringar säkerställer att butikerna alltid har den senaste produktinformationen.
   - **Effektiv kataloghantering**-Förenklar underhåll av produktkatalogen genom att automatisera rensning och uppdatering av resurser.

## Integrera Commerce och Experience Manager Assets

>[!BEGINSHADEBOX]

**Förutsättningar**

- Adobe Commerce måste konfigureras med [Commerce Admin-integreringen med Adobe ID](/help/getting-started/adobe-ims-config.md) med ett tilldelat organisations-ID.
- Experience Manager Assets måste tilldelas som en produkt till samma organisations-ID.
- Användaren som konfigurerar integreringen måste ha ett konto i samma organisation med administratörsbehörighet för åtkomst till Adobe Commerce och Experience Manager Assets.

>[!ENDSHADEBOX]

Aktivera Commerce-integrationen med Experience Manager Assets genom att utföra följande uppgifter:

1. [Konfigurera ditt Experience Manager Assets-projekt för att hantera Commerce-resurser](aem-assets-configure-aem.md)

1. [Installera Experience Manager Assets Integration-tillägget och konfigurera Adobe Commerce](aem-assets-configure-commerce.md)

1. [Aktivera resurssynkronisering](aem-assets-setup-synchronization.md)
