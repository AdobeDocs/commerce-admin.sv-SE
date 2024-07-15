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

1. Gå till **[!UICONTROL Customers]** > **[!UICONTROL All Customers]** på sidofältet _Admin_.

1. Hitta kunden i rutnätet och klicka på **[!UICONTROL Edit]** i kolumnen _[!UICONTROL Action]_.

1. Välj **[!UICONTROL Account Information]** på den vänstra panelen.

1. Klicka på **[!UICONTROL Associate to Company]** och skriv de första bokstäverna i företagsnamnet i indatarutan.

   Systemet genererar en lista över alla möjliga matchningar.

   ![Associera med företag](./assets/company-assign-customer-account.png){width="600"}

1. I listan väljer du det företag där du vill tilldela kunden och klickar på **[!UICONTROL Done]**.

1. Om kunden tidigare har tilldelats ett annat företag klickar du på **[!UICONTROL Confirm]**.

   Kunden tilldelas om till kundgruppen (eller [delad katalog](catalog-shared.md)) för företaget och läggs till i dess [företagsstruktur](account-company-structure.md).

1. Klicka på **[!UICONTROL Save Customer]** när du är klar.

   Följande kolumner uppdateras i rutnätet [Kunder](../customers/customers-all.md):

   - Kolumnen _[!UICONTROL Group]_ändras till namnet på kundgruppen (eller den delade katalogen) som har tilldelats företaget.
   - Kolumnen _[!UICONTROL Company]_visar namnet på det företag som kundprofilen nu är associerad med.
