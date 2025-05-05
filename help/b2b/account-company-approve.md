---
title: Godkänn ett företagskonto
description: Lär dig hur du godkänner begäranden om företagskonton i Admin.
exl-id: c7123383-0e94-4d6c-be3c-b6ca84145a59
feature: B2B, Companies, Configuration
role: Admin, User
source-git-commit: 2b86fe55f980c22839de10ecc4c9023034eb9ea1
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# Godkänn ett företagskonto

Status för begäranden som tagits emot från butiken för att skapa ett företag är `Pending Approval` tills begäran granskas av butiksadministratören och antingen godkänns eller avvisas. Statusen för ett företagskonto kan vara något av följande:

- [!UICONTROL Active]
- [!UICONTROL Pending Approval]
- [!UICONTROL Rejected]
- [!UICONTROL Blocked]

Du kan också använda [åtgärdskontrollen](account-company-manage.md) för att godkänna flera företagsförfrågningar.

![Väntar på godkännande](./assets/companies-pending-approval.png){width="700" zoomable="yes"}

## Godkänn ett väntande företagskonto

1. Gå till **[!UICONTROL Customers]** > **[!UICONTROL Companies]** på sidofältet _Admin_.

   Du kan använda väljaren _[!UICONTROL Columns]_&#x200B;ovanför stödrastret för att visa kolumnen **[!UICONTROL Status]**.

1. Klicka på **[!UICONTROL Edit]** i kolumnen _[!UICONTROL Action]_.

1. Ange **[!UICONTROL Company Status]** till `Active`.

   ![Ange företagsstatus](./assets/company-status-active.png){width="700" zoomable="yes"}

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL Change status]**.

   Företagsadministratören får ett e-postmeddelande om att företaget nu är aktivt.

1. Ange **[!UICONTROL Sales Representative]** till ett specifikt administratörsanvändarkonto om tillämpligt.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Account Information]** och använd fältet **[!UICONTROL Comment]** för att ange anteckningar om kontot.

   Kommentarerna visas inte i butiken.

1. Klicka på **[!UICONTROL Save]** när du är klar.

   Ett bekräftelsemeddelande skickas till företaget och företagsadministratören som bekräftar att företagskontot har godkänts.

## Företagsstatus

| Status | Beskrivning |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Active] | Företaget har godkänts och kan hanteras från butiken av företagsadministratören. |
| [!UICONTROL Pending Approval] | En begäran om att skapa ett företagskonto har skickats från butiken, men har ännu inte granskats. |
| [!UICONTROL Rejected] | Begäran om att skapa ett företagskonto avvisades av butiksadministratören. |
| [!UICONTROL Blocked] | Företagskontot är inte längre i gott skick. Kunden har åtkomst till kontot från butiken, men kan inte göra inköp. |

{style="table-layout:auto"}
