---
title: Tilldela en företagsadministratör
description: Lär dig tilldela ett företagskonto som utsedd företagsadministratör för företagskontot.
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Tilldela en företagsadministratör

Företagsadministratören tilldelas initialt när företagskontot skapas första gången och kan bara ändras av en butiksadministratör från administratören.

- Varje företag kan bara ha en tilldelad administratör.
- En företagsanvändare kan bara vara administratör för ett företag.
- Ändringar av den tilldelade företagsadministratören måste slutföras av en butiksadministratör från administratören.

## Ändra tilldelad företagsadministratör

1. Gå till **[!UICONTROL Customers]** > **[!UICONTROL Companies]** i sidopanelen _Admin_.

   ![Företag](./assets/companies-grid.png){width="700" zoomable="yes"}

1. Hitta företaget i listan och klicka sedan på **[!UICONTROL Edit]**.

1. Expandera avsnittet ![Expansionsväljare](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Company Admin]**.

   ![Företagsadministratör](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. Ange **[!UICONTROL Job Title]** för den nya företagsadministratören.

   Den här åtgärden rensar formuläret och de obligatoriska _[!UICONTROL First Name]_- och&#x200B;_[!UICONTROL Last Name]_-fälten markeras.

1. Ange adressen **[!UICONTROL Email]** till den nya företagsadministratören.

   Om systemet inte hittar e-postadressen i databasen uppmanas du att bekräfta att du vill ersätta företagsadministratören.

   - Om det inte finns något användarkonto för den nya företagsadministratören skapar systemet ett konto av typen `Company Admin`.

   - Om användarkontot finns i systemet flyttas det till företagsadministratörspositionen i företagsstrukturen.

1. Ange **[!UICONTROL First Name]** och **[!UICONTROL Last Name]** och annan information som är relevant för den nya företagsadministratören.

1. Klicka på **[!UICONTROL Save]** när det är klart.

   Det individuella kontot för den tidigare företagsadministratören finns kvar i systemet som ett aktivt användarkonto, tilldelat standardanvändarrollen. Om detta är det enda företaget som är associerat med användarkontot ändras kontotypen från *[!UICONTROL Company user]* till *[!UICONTROL Individual user]*.

   Systemet skickar ett e-postmeddelande om ändringen till de nya och tidigare företagsadministratörerna.

