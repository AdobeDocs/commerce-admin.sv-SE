---
title: Lägga till kunder till ett företagskonto
description: Lär dig hur du lägger till en befintlig kund till ett företagskonto.
exl-id: ee2f9c27-37d6-4997-8285-1c4c84f8d04c
feature: B2B, Companies, Customers
role: Admin, User
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# Lägga till kunder till ett företagskonto

När det är aktiverat i konfigurationen lägger företagsadministratören till användare i företaget. Företagstilldelningen av en kundprofil kan dock också göras eller ändras från administratören.

>[!NOTE]
>
>Om en person redan har ett personligt konto hos din butik och senare går till arbetet för ett företag, ska du inte tilldela personens konto till företaget. Skapa i stället ett företagsanvändarkonto för personen med en e-postadress för företaget.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Hitta kunden i rutnätet och klicka **[!UICONTROL Edit]** i _[!UICONTROL Action]_kolumn.

1. Välj **[!UICONTROL Account Information]**.

1. Klicka **[!UICONTROL Associate to Company]** och skriv de första bokstäverna i företagsnamnet i inmatningsrutan.

   Systemet genererar en lista över alla möjliga matchningar.

   ![Associera med företag](./assets/company-assign-customer-account.png){width="600"}

1. I listan väljer du det företag där du vill tilldela kunden och klickar på **[!UICONTROL Done]**.

1. Om kunden tidigare har tilldelats ett annat företag klickar du på **[!UICONTROL Confirm]**.

   Kunden omfördelas till kundgruppen (eller [delad katalog](catalog-shared.md)) av företaget och lades till [företagsstruktur](account-company-structure.md).

1. När du är klar klickar du på **[!UICONTROL Save Customer]**.

   Följande kolumner uppdateras i [Kunder](../customers/customers-all.md) rutnät:

   - The _[!UICONTROL Group]_kolumn ändras till namnet på kundgruppen (eller den delade katalogen) som är tilldelad företaget.
   - The _[!UICONTROL Company]_visas namnet på det företag som kundprofilen nu är associerad med.
