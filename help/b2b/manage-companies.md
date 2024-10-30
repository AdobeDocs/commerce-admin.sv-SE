---
title: Företagsledning
description: Effektivisera administration och hantering av B2B-organisationer med komplexa operativa modeller.
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 6b06f52eb4ee8ca136a1c60fd6dc04a9ac96bbfa
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# Företagsledning

Företagshantering effektiviserar affärsverksamheten för företag med komplexa organisationsstrukturer. Administratörsanvändare kan skapa en företagshierarki för att spegla en B2B-organisation genom att tilldela företag till det utsedda överordnade företaget. Med den här tilldelningen kan administratören för det överordnade företaget visa och hantera företag inom organisationen.

Initiera företagshanteringsuppgifter från vyn *[!UICONTROL Companies]*. Gå till **[!UICONTROL Customers]** > **[!UICONTROL Companies]** i Admin.

![Hantera företagstödraster för B2B](./assets/companies-grid-view.png){width="700" zoomable="yes"}

Kolumnen *[!UICONTROL Company Type]* anger om ett företag hanteras som en del av en organisation eller som ett separat företag.

- `Parent` är en affärsorganisation med ett eller flera tilldelade företag. Ett överordnat företag kan inte tilldelas som underordnat till ett annat företag.

- `Child` är ett företag som har tilldelats en organisation. Ett företag kan bara tilldelas till ett överordnat företag.

- `Company` representerar ett enskilt företag. Ett enskilt företag kan bli en del av en organisation genom att göra det till ett moderföretag eller genom att tilldela det till ett befintligt moderföretag.

När du redigerar ett överordnat eller underordnat företag expanderar du *[!UICONTROL Company Hierarchy]* så att alla företag i organisationen visas. En `Current`-flagga anger vilket företag du redigerar.

![Företagshierarki för B2B](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

## Visa och konfigurera [!UICONTROL Company Hierarchy]

När företaget skapades är stödrastret *[!UICONTROL Company Hierarchy]* tomt. Det är också tomt om företaget är ett enda företag.

![Företagshierarkistödraster för B2B](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

Om företaget är ett överordnat företag för en organisation, och företagskontona för andra företag i organisationen redan har konfigurerats i Adobe Commerce, kan administratörsanvändare med lämplig behörighet tilldela företag och använda stödrastret *[!UICONTROL Company Hierarchy]* för att slutföra andra företagshanteringsuppgifter:

- Visa alla företag som är associerade med det överordnade företaget.
- Tilldela fler företag till organisationen från detaljsidan för ett överordnat företag.
- Ta bort ett företag från en organisation med åtgärden *[!UICONTROL Unassign from parent]*.
- Uppdatera *[!UICONTROL Advanced Settings]*-konfigurationen så att samma inställningar används för flera företag.

Mer information finns i [Hantera företagshierarkin](manage-company-hierarchy.md).

