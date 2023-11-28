---
title: Hantera företagshierarkin
description: Bygg och hantera företagshierarkier för att stödja B2B-organisationer med komplexa operativa modeller.
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 10b01db562777ef2fcc224177d7a83c0a6fc90e7
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Hantera [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Endast tillgängligt för betaprogramdeltagare"}

Administratörer kan skapa en [!UICONTROL Company Hierarchy] genom att tilldela närstående företag till ett utsett moderföretag, som är företaget överst i organisationshierarkin.

Skapa ett överordnat företag genom att redigera ett företag som inte har tilldelats till ett befintligt [!UICONTROL Company Hierarchy]och att utse närstående företag.

![Stödraster för företagshierarki](./assets/company-detail-view.png){width="700"}

När ett företag har tilldelats en hierarki [!UICONTROL Company type] kolumn i **Företag** identifierar företaget som en `Parent` eller  `Child` företag.  Om [!UICONTROL Company Type] är `Company`är företaget inte del av en företagshierarki och kan bli ett moderföretag eller tilldelas ett befintligt moderföretag.

>[!NOTE]
>
>Mer information om [!UICONTROL Company Hierarchy] stödraster, se [Företagshierarki](account-company-create.md#company-hierarchy) fältbeskrivningar.

I Admin hanterar du företagstilldelningar genom att redigera ett företag och sedan använda [!UICONTROL Company Hierarchy] i [!UICONTROL Company] sida för att tilldela eller ta bort tilldelningar av företag.

## Tilldela företag till ett moderföretag

1. På _Administratör_ sidlist, navigera till **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Företagsrutnät](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Öppna företagsinformationssidan i företagsrutnätet för att skapa tilldelningarna.

   - Om du vill tilldela ytterligare företag till ett befintligt överordnat företag väljer du **[!UICONTROL Edit]** åtgärd för huvudföretaget.
   - Om du vill skapa ett nytt överordnat företag väljer du **[!UICONTROL Edit]** åtgärd för det företag som anges som moderföretag.

     Du kan inte skapa ett nytt överordnat företag från ett befintligt överordnat eller underordnat företag.

   ![Nytt företag](./assets/company-update.png){width="700" zoomable="yes"}

1. På sidan Företagsinformation expanderar du **[!UICONTROL Company Hierarchy]** och markera **[!UICONTROL Assign Companies]**.

   ![Nytt företag](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

   När du expanderar den här vyn kan du se befintliga företagstilldelningar, om det finns några. Det överordnade företaget visas alltid ovanpå _[!UICONTROL Company Hierarchy]_stödraster med `current company indicator` visas på den företagsrad som redigeras.

1. Företag som är tillgängliga för tilldelning visas i rutnätet. Välj de företag som ska tilldelas och välj sedan **[!UICONTROL Assign Selected Companies]**.

1. Du kan **Markera alla på den här sidan** eller en specifik företagsradartikel och klicka på **[!UICONTROL Assign Selected Companies]**.

   ![Nytt företag](./assets/assign-selected-companies.png){width="700" zoomable="yes"}

1. Slutför företagstilldelningen genom att välja **[!UICONTROL Assign]**.

## Ta bort tilldelning från ett moderföretag

1. På _Administratör_ sidlist, navigera till **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Företagsrutnät](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. På sidan Företag öppnar du företagsinformationssidan för det överordnade företaget genom att välja **[!UICONTROL Edit]** åtgärd.

   ![Nytt företag](./assets/company-update.png){width="700" zoomable="yes"}

1. Visa listan över tilldelade företag genom att expandera **[!UICONTROL Company Hierarchy]** nedrullningsbar meny.

1. Ta bort tilldelningen av ett företag genom att välja **[!UICONTROL Select]** åtgärd för företaget och sedan välja **[!UICONTROL Unassign from parent]**.

   ![Nytt företag](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

1. Ta bort det tilldelade företaget från hierarkin genom att välja **[!UICONTROL Unassign]**.
