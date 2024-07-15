---
title: Hantera företagsanvändarkonton
description: Lär dig mer om företagsanvändarkonton och hur de fungerar i det associerade företagskontot.
exl-id: 36b55f61-e579-4eb8-8f67-0156221d378e
feature: B2B, Companies, User Account, Storefront
role: Admin, User
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Hantera företagsanvändarkonton

Företagsanvändare tilldelas av företagsadministratören och visas från administratören i rutnätet _[!UICONTROL Customers]_utifrån kundtypen_[!UICONTROL Company User]_. Dessa personer är vanligtvis köpare med olika behörighetsnivåer för att få tillgång till butikstjänster och resurser.

Företagsadministratören ställer först in [företagsstrukturen](account-company-structure.md) och slutför sedan följande uppgifter efter behov:

- Skapa företagsanvändare och tilldela användare till team

- Definiera roller och behörigheter och tilldela användare till roller

>[!IMPORTANT]
>
>Företagsanvändare kan bara läggas till, redigeras eller tas bort av företagsadministratören. Borttagningen kan inte ångras eftersom användaren har tagits bort från företagsstrukturen.

## Lägg till företagsanvändare

1. Från butiken loggar företagsadministratören in på sitt konto.

1. Välj **[!UICONTROL Company Users]** i den vänstra panelen.

   ![Företagsanvändare](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Add New User]** och gör följande:

   - Anger den nya användarens **[!UICONTROL Job Title]**.

   - Väljer lämplig **[!UICONTROL User Role]** om roller och behörigheter har definierats. Annars kan de gå tillbaka senare för att tilldela rollen.

     ![Lägg till ny användare](./assets/company-structure-users-add.png){width="700" zoomable="yes"}

   - Fyller i de återstående fälten efter användarens behov:

      - **[!UICONTROL First Name]** och **[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Phone Number]**

   Som standard är **[!UICONTROL Status]** för kontot `Active`.

1. Klicka på **[!UICONTROL Save]** när du är klar.

1. Upprepar processen att skapa så många företagsanvändare som behövs.

   De nya användarna visas i listan Företagsanvändare tillsammans med företagsadministratören.

Om du vill spara tid under den första beställningen kan företagsadministratören påminna varje företagsanvändare om att lägga till företagets standardfakturerings- och leveransadress i sin [adressbok](../customers/account-dashboard-address-book.md).

## Redigera företagsanvändare

1. Från butiken loggar företagsadministratören in på sitt konto.

1. Välj **[!UICONTROL Company Users]** i den vänstra panelen.

1. Söker efter användarposten som ska uppdateras och klickar på **[!UICONTROL Edit]**.

1. Gör de ändringar som behövs.

1. Klicka på **[!UICONTROL Save]** när du är klar.

## Ta bort en företagsanvändare

1. Från butiken loggar företagsadministratören in på sitt konto.

1. Välj **[!UICONTROL Company Structure]** i den vänstra panelen.

1. Väljer företagsanvändaren i företagsstrukturen.

1. Klicka på **[!UICONTROL Delete Selected]**.

   ![Ta bort användare](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL Delete]**.

I Admin visas företagsanvändaren fortfarande i rutnätet [Kunder](../customers/customers-all.md), men med statusen `Inactive`.

## Fältbeskrivningar

| Fält | Beskrivning |
|--------------|---------------|
| [!UICONTROL Job Title] | Företagsanvändarens jobbtitel. |
| [!UICONTROL User Role] | Den [roll](account-company-roles-permissions.md) som tilldelats företagsanvändaren. Alternativ: `Default User` / (andra roller) |
| [!UICONTROL First Name] | Företagsanvändarens förnamn. |
| [!UICONTROL Last Name] | Företagsanvändarens efternamn. |
| [!UICONTROL Email] | Företagsanvändarens e-postadress. |
| [!UICONTROL Phone Number] | Företagsanvändarens telefonnummer. |
| [!UICONTROL Status] | Status för företagsanvändarkontot. Alternativ: `Active` / `Inactive` |

{style="table-layout:auto"}
