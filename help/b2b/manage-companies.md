---
title: Företagshantering
description: Effektivisera administration och hantering av B2B-organisationer med komplexa operativa modeller.
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 1fc1e07f20e2c22ac430f384e9e2b278edae405c
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# Företagsledning

Företagshantering i Adobe Commerce har ett stort antal verktyg för administratörer som kan ordna, konfigurera och övervaka affärsrelationer inom B2B. Den här funktionen är viktig för företag som arbetar med flera företagskunder, dotterbolag eller komplexa organisationsstrukturer.

Med företagshantering kan ni

* **Organisera affärsrelationer** - Skapa och hantera enskilda företagskonton för dina B2B-kunder
* **Skapa hierarkier i organisationen** - Strukturera överordnade och underordnade relationer som speglar verkliga företagsorganisationer
* **Centralisera administration** - Hantera flera företag och deras inställningar från ett enda administrativt gränssnitt
* **Effektivisera åtgärder** - Använd konsekventa konfigurationer och principer i relaterade företag
* **Stöd för komplexa strukturer** - Hantera dotterbolag, franchises, multi-location business, and corporate Division

Administratörsanvändare kan skapa en företagshierarki för att spegla en B2B-organisation genom att tilldela företag till ett utsett överordnat företag. Med den här tilldelningen kan administratören för det överordnade företaget visa och hantera företag inom organisationen.

Initiera företagshanteringsuppgifter från vyn *[!UICONTROL Companies]*. Gå till **[!UICONTROL Customers]** > **[!UICONTROL Companies]** i Admin.

![Hantera företagstödraster för B2B](./assets/companies-grid-view.png){width="700" zoomable="yes"}

## Förutsättningar

Innan du hanterar företag måste du se till att

* B2B-funktioner aktiveras i din Adobe Commerce-installation
* Du har administrativ åtkomst med behörigheter för företagshantering
* Företagskonton är korrekt konfigurerade med nödvändig företagsinformation
* Användarroller och behörigheter definieras för företagsadministratörer och användare

## Användningsexempel

Företagshantering är idealisk för:

* **Flerlokaliseringsföretag** med centraliserade inköp men platsspecifika behov
* **Franchise-åtgärder** som kräver både företagstillsyn och lokal självständighet
* **Företagsdotterbolag** med delade principer men oberoende åtgärder
* **Stora företag** med flera divisioner eller affärsenheter
* **Distributionsnätverk** med återförsäljare, återförsäljare eller kanalpartners

## Förstå företagshierarki och företagstyper

Företagshierarkin strukturerar affärsrelationerna genom att ordna flera företag under ett enda moderföretag. Den här funktionen speglar verkliga organisationsstrukturer samtidigt som den möjliggör centraliserad hantering och bevarar enskilda företagsidentiteter.

### Företagstyper

Kolumnen *[!UICONTROL Company Type]* i företagsrutnätet visar hur varje företag passar i din B2B-organisation:

* **Överordnad** - Centralt nav med ett eller flera tilldelade företag
   * Kontrollerar flera underordnade företag men kan inte tilldelas till en annan överordnad
   * **Använd fall** - Huvudkontor, huvudsakliga franchiseorganisation eller holdingföretag

* **Underordnad** - Företag tilldelat till en överordnad organisation
   * Fungerar under överordnad styrning och kan ärva konfigurationer
   * Kan bara tillhöra en överordnad åt gången
   * **Använd skiftläge** - Filialer, franchise-kontor eller regionala avdelningar

* **Företag** - oberoende enskilt företag
   * Fungerar oberoende utan hierarkirelationer
   * Kan konvertera till överordnad (genom att tilldela företag) eller underordnad (genom att tilldela till överordnad)
   * **Använd fall** - Enskilda företagskunder eller fristående klienter

### Konverterar företagstyper

* **Enskilt företag → Överordnad** - Tilldela andra företag till det
* **Enkelt företag → Underordnad** - Tilldela det till ett befintligt överordnat företag
* **Child → Single** - Ta bort tilldelningen av det underordnade företaget från dess överordnade
* **Överordnad → Underordnad** - Inte möjligt utan att först ta bort alla tilldelade företag

### Hantera företagets hierarkier

När du redigerar företag i en hierarki expanderar du *[!UICONTROL Company Hierarchy]* för att visa alla relaterade företag. En `Current`-flagga anger vilket företag som redigeras.

![Företagshierarki för B2B](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

Detaljerade stegvisa instruktioner finns i [Hantera företagshierarkin](manage-company-hierarchy.md).

## Företagsledningsuppgifter

När administratörer hanterar företag från företagsrutnätet kan de utföra följande uppgifter från rutnätet *[!UICONTROL Company Hierarchy]*:

* **Visa och hantera företagsrelationer**
   * **Visa associerade företag** - Se alla företag länkade till en överordnad organisation i en centraliserad vy
   * **Övervaka företagsstatus** - Spåra aktiva, väntande och inaktiva företag i hierarkin
   * **Åtkomst till företagsinformation** - Navigera direkt till individuella företagskonfigurationssidor

* **Skapa och ändra hierarkier**
   * **Tilldela företag** - Lägg till befintliga företag till en överordnad organisation från företagsinformationssidan
   * **Skapa överordnade-underordnade relationer** - Strukturera företag så att de återspeglar verkliga affärsrelationer
   * **Omorganisera strukturer** - Flytta företag mellan olika överordnade organisationer när affärsbehoven ändras

* **Hantering av masskonfiguration**
   * **Använd inställningar för flera företag** - Uppdatera avancerade inställningar för flera företag samtidigt med kontrollen [!UICONTROL Actions] i företagsrutnätet
   * **Standardisera konfigurationer** - Säkerställ konsekventa principer i närliggande organisationer
   * **Åsidosätt enskilda inställningar** - Överför överordnade företagskonfigurationer till valda underordnade företag

* **Administrativa åtgärder**
   * **Ta bort företagsrelationer** - Använd åtgärden *[!UICONTROL Unassign from parent]* för att lösa upp organisationsrelationer
   * **Hantera företagsåtkomst** - Styr vilka administratörer som kan visa och ändra företagsrelationer
   * **Ändringar i övervakningshierarkin** - Spåra ändringar i organisationsstrukturer

## God praxis

Tänk på följande när du hanterar företag:

* **Skapa företagshierarkier** - När du hanterar komplexa företagsstrukturer ska du planera din hierarki så att den matchar verkliga affärsrelationer samtidigt som strukturerna är enkla för att undvika förvirring hos användaren. Dokumentera alla företagsrelationer och deras affärskopplingar för framtida referens.

* **Konfigurationshantering** - Testa konfigurationsändringar på enskilda företag innan du använder dem på hela hierarkier, och dokumentera alltid aktuella inställningar innan du gör gruppändringar. Förmedla planerade ändringar till berörda företagsadministratörer i förväg.

* **Säkerhet** - Begränsa behörigheter för företagshantering till endast betrodda administratörer, utför regelbundna granskningar av företagsrelationer och åtkomstbehörigheter samt övervaka alla hierarkiändringar i granskningssyfte.

>[!MORELIKETHIS]
>
>* [Skapa ett företagskonto](account-company-create.md)
>* [Hantera företagshierarkier](manage-company-hierarchy.md)
>* [Företagsroller och behörigheter](account-company-roles-permissions.md)
>* [Företagets kredithantering](credit-company.md)
>* [Aktivera B2B-funktioner](enable-basic-features.md)
