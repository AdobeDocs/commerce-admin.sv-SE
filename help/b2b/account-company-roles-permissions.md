---
title: Företagsroller och behörigheter
description: Lär dig mer om roller och behörigheter som en företagsadministratör kan tillämpa på företagsanvändare, vilket ger olika nivåer åtkomst till orderinformation och resurser.
exl-id: 9fe20d6a-2c9c-4618-a395-805d64dcf0de
feature: B2B, Companies, Roles/Permissions
role: Admin
source-git-commit: bad59798a1a6d97826dc421fe8614ef511e067bd
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# Företagsroller och behörigheter

Roller för företagsanvändare skapas med olika behörighetsnivåer för att komma åt säljinformation och säljresurser. Som standard är företagsadministratören en _superanvändare_ med fullständig behörighet. Sidan [Åtkomst nekad](../content-design/pages.md#access-denied) visas om användaren inte har behörighet att komma åt sidan.

![Sidan Roller och behörigheter med standardrollen](./assets/company-roles-permissions.png){width="700" zoomable="yes"}

Systemet har en fördefinierad standardanvändarroll, som du kan använda _som_ eller ändra efter behov. Du kan skapa så många roller som behövs för att matcha företagets struktur och organisationsansvar, som exempelvis följande:

- **Standardanvändare** - Standardanvändaren har fullständig åtkomst till aktiviteter relaterade till försäljning och offerter, och skrivskyddad åtkomst till företagsprofil och kreditinformation.

- **Senior Buyer** - En Senior Buyer kan ha åtkomst till alla Sales- och Quotes-resurser och endast visa behörigheter för företagsprofilen, användare och team, betalningsinformation och företagskrediter.

- **Assistant Buyer** - En assistentköpare kan ha behörighet att göra en beställning med _Checka ut med offert_ och visa beställningar, offerter och information i företagsprofilen.

## Hantera roller och behörigheter

1. Företagsadministratören loggar in på sitt butikskonto.

1. Välj **[!UICONTROL Roles and Permissions]** i den vänstra panelen.

1. Slutför någon av följande uppgifter.

### Skapa en roll

1. Klicka på **[!UICONTROL Add New Role]**.

   ![Lägg till ny roll](./assets/company-roles-permissions-add-storefront.png){width="600" zoomable="yes"}

1. Anger en beskrivande **[!UICONTROL Role Name]**.

1. Gör något av följande under _[!UICONTROL Role Permissions]_:

   - Markerar kryssrutan för varje resurs eller aktivitet som användare som har tilldelats rollen har behörighet att komma åt.

   - Markerar kryssrutan **[!UICONTROL All]** och avmarkerar kryssrutan för varje resurs eller aktivitet som användare som har tilldelats rollen inte har behörighet att komma åt.

1. Klicka på **[!UICONTROL Save Role]**.

1. Skapar så många roller som behövs genom att upprepa de här stegen.

### Ändra en roll

1. Företagsadministratören klickar på **[!UICONTROL Edit]** i kolumnen _[!UICONTROL Actions]_&#x200B;för rollen som ska ändras.

1. Gör nödvändiga ändringar i namn- och behörighetsinställningarna.

1. Klicka på **[!UICONTROL Save Role]** när du är klar.

### Duplicera en roll

1. Företagsadministratören klickar på **[!UICONTROL Duplicate]** i kolumnen _[!UICONTROL Actions]_&#x200B;för att rollen ska dupliceras.

1. Gör nödvändiga ändringar i namn- och behörighetsinställningarna.

1. Klicka på **[!UICONTROL Save Role]** när du är klar.

### Ta bort en roll

1. Företagsadministratören hittar rollen som ska tas bort i listan över roller.

   Endast roller utan tilldelade användare kan tas bort.

1. Klicka på **[!UICONTROL Delete]** i kolumnen _[!UICONTROL Actions]_.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

## Åtgärder

| Åtgärd | Beskrivning |
|-----------| ----------- |
| [!UICONTROL Duplicate] | Skapar en kopia av den valda rollen. Namnet på den duplicerade rollen har `- Duplicated` lagts till i slutet. |
| [!UICONTROL Edit] | Ändra namn och/eller uppsättning behörigheter. |
| [!UICONTROL Delete] | Ta bort rollen. Endast roller utan tilldelade användare kan tas bort. |

{style="table-layout:auto"}

## Rollbehörigheter

Företagsadministratörer kan uppdatera behörighetskonfigurationen för en roll genom att markera [!UICONTROL Edit action] och sedan välja eller ta bort behörigheter i listan **Rollbehörigheter**.

![Roller och behörighetslista](./assets/role-permissions-list.png){width="700" zoomable="yes"}

## Tilldela en roll till en företagsanvändare

När du har definierat de roller som behövs tilldelar företagsadministratören en roll till varje företagsanvändare.

1. Loggar in på deras företagskonto som företagsadministratör.

1. Välj **[!UICONTROL Company Users]** i den vänstra panelen.

   ![Företagsanvändare](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Söker efter användaren i listan och klickar på **[!UICONTROL Edit]**.

1. Väljer lämplig **[!UICONTROL User Role]** för användaren.

   ![Redigera användare - välj en användarroll](./assets/company-user-assign-role.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]**.
