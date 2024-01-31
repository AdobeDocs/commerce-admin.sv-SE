---
title: Hantera företagshierarkin
description: Lär dig hantera B2B-organisationer med komplexa operativa modeller genom att bygga upp företagshierarkier
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# Hantera [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Endast tillgängligt för betaprogramdeltagare"}

Administratörer kan skapa en [!UICONTROL Company Hierarchy] genom att tilldela närstående företag till ett utsett moderbolag, som är det företag som ligger överst i organisationen. Om [!UICONTROL Company Type] är `Company`, är företaget inte en del av en organisation och är berättigat att bli moderbolag, eller att tilldelas ett befintligt moderföretag.

I Admin hanterar du företagstilldelningar genom att redigera ett företag och sedan uppdatera [!UICONTROL Company Hierarchy] konfiguration för att tilldela eller ta bort tilldelning av företag.

![Stödraster för företagshierarki](./assets/company-detail-hierarchy-current-flag.png){width="700"}

>[!NOTE]
>
>Mer information om [!UICONTROL Company Hierarchy] stödraster, se [Företagshierarki](account-company-create.md#company-hierarchy) fältbeskrivningar.

## Tilldela företag till en organisation

1. Från _Administratör_ sidlist, navigera till **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Företagsrutnät](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. I [!UICONTROL Companies] öppnar du företagsinformationssidan för att skapa tilldelningarna.

   - Om du vill tilldela ytterligare företag till ett befintligt överordnat företag väljer du **[!UICONTROL Edit]** åtgärd för huvudföretaget.
   - Om du vill skapa ett överordnat företag väljer du **[!UICONTROL Edit]** åtgärd för det företag som ska utses till överordnad.

     Du kan inte skapa ett överordnat företag från ett befintligt överordnat eller underordnat företag.

1. Utöka på sidan med företagsinformation **[!UICONTROL Company Hierarchy]**.

   ![Stödraster för företagshierarki](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

   I rutnätet visas befintliga företagstilldelningar, om sådana finns. Det överordnade företaget är alltid placerat högst upp i [!UICONTROL Company Hierarchy] rutnät. The `[!UICONTROL Current]` anger vilket företag som redigeras.

1. Lägg till företag i den överordnade organisationen.

   - Välj från en lista över tillgängliga företag genom att välja **[!UICONTROL Assign Companies]**.

   - **Markera alla på den här sidan** eller välj en eller flera specifika företagsradartiklar.

   - Välj **[!UICONTROL Assign Selected Companies]**.

   - Slutför företagstilldelningen genom att välja **[!UICONTROL Assign]**.

     ![Tilldela företag till organisation](./assets/assign-selected-companies-hierarchy.png){width="675" zoomable="yes"}

## Ta bort tilldelning från ett moderföretag

1. På _Administratör_ sidlist, navigera till **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Företagsrutnät](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. I [!UICONTROL Companies] rutnät, öppna företagsinformationssidan för det överordnade företaget genom att välja **[!UICONTROL Edit]**.

1. Visa listan över tilldelade företag genom att expandera **[!UICONTROL Company Hierarchy]**.

1. Från [!UICONTROL Company Hierarchy] rutnät, ta bort tilldelning från ett företag med hjälp av **[!UICONTROL Select]** funktionsmakrokontroll att välja **[!UICONTROL Unassign from parent]**.

   ![Ta bort tilldelning av företag från en överordnad organisation](./assets/company-hierarchy-grid-unassign.png){width="700" zoomable="yes"}

1. Ta bort det tilldelade företaget från hierarkin genom att välja **[!UICONTROL Unassign]**.
