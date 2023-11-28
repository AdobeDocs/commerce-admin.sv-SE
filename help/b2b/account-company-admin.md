---
title: Tilldela en företagsadministratör
description: Lär dig hur du tilldelar ett företagsanvändarkonto som angiven företagsadministratör för företagskontot.
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
source-git-commit: fb075822e318073053cdf8cdd5cd9bb3a6343904
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Tilldela en företagsadministratör

Företagsadministratören tilldelas först när företagskontot skapas och kan endast ändras av en butiksadministratör från administratören.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Hitta företaget i listan och klicka på **[!UICONTROL Edit]**.

   ![Företag](./assets/companies-grid.png){width="700" zoomable="yes"}

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Company Admin]** -avsnitt.

   ![Företagsadministratör](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. Ange **[!UICONTROL Job Title]** den nya företagsadministratören och klicka på **[!UICONTROL Proceed]** för att fortsätta.

   Den här åtgärden rensar formuläret och de obligatoriska _[!UICONTROL First Name]_och_[!UICONTROL Last Name]_ fält markeras.

1. Ange **[!UICONTROL Email]** den nya företagsadministratörens adress.

   Om systemet inte hittar e-postadressen i databasen uppmanas du att bekräfta att du vill ersätta företagsadministratören.

   - Om ett användarkonto inte finns för den nya företagsadministratören skapas ett konto för `Company Admin` typ.

   - Om användarkontot finns i systemet flyttas det till företagsadministratörspositionen i företagsstrukturen.

1. Ange **[!UICONTROL First Name]** och **[!UICONTROL Last Name]** och all annan information som gäller för den nya företagsadministratören.

1. När du är klar klickar du på **[!UICONTROL Save]**.

   Det enskilda kontot för den tidigare företagsadministratören finns kvar i systemet som ett aktivt enskilt användarkonto i företagsstrukturen, som tilldelats standardanvändarrollen.

   Systemet skickar ett e-postmeddelande om ändringen till nya och tidigare företagsadministratörer.
