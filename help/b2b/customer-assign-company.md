---
title: Lägga till användare i ett företagskonto
description: Lär dig hur du lägger till en befintlig kund till ett företagskonto.
exl-id: ee2f9c27-37d6-4997-8285-1c4c84f8d04c
feature: B2B, Companies, Customers
role: Admin, User
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 0%

---

# Lägga till användare i ett företagskonto

När det är aktiverat i konfigurationen lägger företagsadministratören till och hanterar företagsanvändare från butiken. Företagsanvändarkonton kan dock också läggas till och hanteras från administratören.

Om det behövs kan du tilldela en användare till mer än ett företag. Om B2B-köpare till exempel stöder flera företag kan du lägga till deras användarkonton i alla företag de gör affärer med. I butiken kan köpare som tilldelats flera företag växla mellan företagskonton genom att välja bland de tillgängliga företagen på menyn *[!UICONTROL Company]*.

![Associera med företag](./assets/company-assign-multi-switcher.png){width="700"}

>[!NOTE]
>
>Om en person redan har ett personligt konto hos din butik och senare går till arbetet för ett företag, ska du inte tilldela personens konto till företaget. Skapa i stället ett företagsanvändarkonto för personen med en e-postadress för företaget.

## Lägg till en företagsanvändare

När du lägger till en företagsanvändare är det första företaget som du associerar med användarkontot standardföretag.

1. Gå till **[!UICONTROL Customers > All Customers]** på sidlisten Admin.

1. Klicka på **[!UICONTROL Add new customer]**.

1. Konfigurera det nya kontot.

   1. Ange inledande kontostatus genom att ställa in växlingsknappen **[!UICONTROL Customer Active]**.

      Aktivera det om du vill aktivera kontot omedelbart eller inaktivera det om du vill skapa ett inaktivt konto.

   1. Välj webbplatsomfånget i listan **[!UICONTROL Associate to Website]**.

   1. Klicka på **[!UICONTROL Associate to Company]** för att visa tillgängliga företag.

      ![Associera med företag](./assets/company-assign-customer-account.png){width="675"}

      Om det behövs kan du filtrera listan genom att skriva de första bokstäverna i företagsnamnet i inmatningsrutan.

   1. I listan väljer du ett eller flera företag där du vill tilldela kunden och klickar på **[!UICONTROL Done]**.

      Företagsanvändare läggs automatiskt till i kundgruppen (eller [delad katalog](catalog-shared.md)) för varje företag som är associerat med deras konto.

   1. Ange nödvändig användarkontoinformation: **[!UICONTROL First Name]**, **[!UICONTROL Last Name]** och **[!UICONTROL Email]**.

   1. Tillåt säljarna att logga in i butiken för kundens räkning genom att aktivera **[!UICONTROL Allow remote shopping assistance]**.

   1. Tillämpa ändringarna genom att klicka på **[!UICONTROL Save Customer]**.

      ![Kundrutnät med företagstilldelningar](./assets/company-assign-user-assignments.png){width="675"}

[!UICONTROL Customers grid] visar en separat rad för varje företag som användaren har tilldelats. Följande kolumner uppdateras.

- Kolumnen _[!UICONTROL Customer Type]_uppdateras för att visa rollen som tilldelats användaren.

  Om det här är första gången som kunden har tilldelats ett företag uppdateras kolumnen _[!UICONTROL Customer Type]_från_[!UICONTROL Individual user]_ till _[!UICONTROL Company User]_.

- Kolumnen _[!UICONTROL Group]_ändras till namnet på kundgruppen (eller den delade katalogen) som har tilldelats företaget.

- Kolumnen _[!UICONTROL Company]_visar namnet på det företag som kundprofilen nu är associerad med.

## Tilldela en användare till ett eller flera företagskonton

När du tilldelar en ny användare blir det första företaget som du associerar med användarkontot standardföretag.

1. Gå till **[!UICONTROL Customers]** > **[!UICONTROL All Customers]** på sidofältet _Admin_.

1. Hitta kunden i rutnätet och klicka på **[!UICONTROL Edit]** i kolumnen _[!UICONTROL Action]_.

1. Välj **[!UICONTROL Account Information]** på den vänstra panelen.

1. I listan **[!UICONTROL Associate to Company]** väljer du ett eller flera företag att tilldela till företagsanvändaren och klickar på **[!UICONTROL Done]**.

1. Tillämpa ändringarna genom att klicka på **[!UICONTROL Save Customer]**.

## Ta bort företagstilldelning från ett användarkonto

Om du tar bort ett företag från en användarprofil återkallas användaråtkomsten till det företaget. Användardata är fortfarande tillgängliga i Admin. Om du tar bort alla företagstilldelningar ändras _[!UICONTROL Customer Type]_till *[!UICONTROL Individual user]*som inaktiverar B2B-funktioner för kontot.

1. Redigera kundprofilen som ska uppdateras från kundrutnätet i Admin.

1. I avsnittet *[!UICONTROL Account Information] tar du bort ett tilldelat företag från fältet **[!UICONTROL Associate to Company]** genom att klicka på **[!UICONTROL X]** i företagsnamnetiketten.

1. Tillämpa ändringarna genom att klicka på **[!UICONTROL Save Customer]**.

>[!NOTE]
>
>Om en företagsanvändare har tilldelats som företagsadministratör kan du inte använda företagsassociationen från den här användaren förrän du uppdaterar företagskontot för att tilldela en ny företagsadministratör.
