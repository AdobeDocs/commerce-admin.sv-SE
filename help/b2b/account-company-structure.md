---
title: Företagets kontostruktur
description: Lär dig mer om företagsstrukturer och hur en företagsadministratör kan definiera dem som stöd för sina arbetsflöden och policyer.
exl-id: 4724b208-b6ac-4de5-9a4c-bc4d68402506
feature: B2B, Companies
role: Admin
source-git-commit: fec72b792cf3149c05803874795c45f9f4e28673
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---

# Företagets kontostruktur

Ett företagskonto kan skapas för att återspegla affärsstrukturen. Till att börja med innehåller företagsstrukturen bara företagsadministratören, men kan utvidgas till att omfatta användargrupper. Användarna kan associeras med team eller vara organiserade i en hierarki av divisioner och indelningar inom företaget.

![Företagsstruktur med divisioner](./assets/company-structure-diagram.svg){width="500"}

I företagsadministratörens kontokontrollpanel i butiken representeras företagsstrukturen som ett träd och består inledningsvis av endast företagsadministratören.

![Företagsstruktur med företagsadministratör](./assets/company-structure-tree-admin.png){width="700" zoomable="yes"}

För handlare återspeglas den fullständiga företagsstrukturen i rutnäten _Företag_ och _Kunder_ i Admin. I företagsrutnätet visas alla företag oavsett status.

![Företagsstödraster](./assets/companies-grid.png){width="700" zoomable="yes"}

I följande exempel visas rutnätet [!UICONTROL Customers] med de inledande företagskontona för varje företag.

![Kundrutnät med företagsadministratörskonton](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

När du har skapat kontot kan företagsadministratören definiera en företagsstruktur med [team](account-company-structure.md), konfigurera [företagsanvändarna](account-company-users.md) och upprätta [roller och behörigheter](account-company-roles-permissions.md) för varje.

>[!NOTE]
>
>När en företagsanvändare läggs till läggs företagsanvändaren till i rotföretagsstrukturen, som är underordnad företagsadministratören. Om företagsadministratören utför flera roller inom företaget skapar du separata företagsanvändarkonton med olika e-postadresser för varje roll.

## Företagsstrukturikoner

| Ikon | Beskrivning |
| ---- | ----------------- |
| ![Ikon för företagsadministratör](./assets/company-icon-admin.png) | Representerar företagsadministratören i företagsstrukturen. |
| ![Teamikon](./assets/company-icon-team.png) | Representerar ett team i företagsstrukturen. |
| ![Användarikon](./assets/company-icon-user.png) | Representerar en användare i företagsstrukturen. |
| ![Ikonen Flytta](./assets/company-icon-move.png) | Flyttar ett team till en annan position i företagsstrukturen. |
| ![Utbyggnadsikon](./assets/company-icon-expand.png) | Utökar ett team i företagsstrukturen. |
| ![Komprimera ikon](./assets/company-icon-collapse.png) | Komprimerar ett team i företagsstrukturen. |

{style="table-layout:auto"}

## Skapa företagsteam

Strukturen för ett företagskonto bör återspegla inköpsorganisationen, oavsett om det är enkelt och platt eller en komplex organisation med olika team för varje avdelning och avdelning i företaget.

Om butiken är [konfigurerad](enable-basic-features.md) för att tillåta företag att hantera sina egna konton, är konfigurering av företagsstrukturen en av de första uppgifterna som en företagsadministratör kan utföra efter att kontot har godkänts. I företagskontot representeras företagets struktur som ett träd med företagsadministratören högst upp.

![Företagsstruktur med team](./assets/company-structure-teams-diagram.svg){width="450"}

1. Företagsadministratören loggar in på sitt konto.

1. Välj **[!UICONTROL Company Structure]** i den vänstra panelen.

1. Under **[!UICONTROL Business Structure]** klickar du på **[!UICONTROL Add Team]** och gör följande:

   - Anger **[!UICONTROL Team Title]** och **[!UICONTROL Description]**.

     Team Title kan vara vad som helst som representerar företagets struktur, till exempel ett team, kontor eller en division inom företaget

     ![Lägg till team](./assets/company-structure-add-team.png){width="700" zoomable="yes"}

   - Klicka på **[!UICONTROL Save]** när du är klar.

   - Skapar så många team som behövs.

1. Om du vill skapa en hierarki av team gör administratören följande:

   - Väljer det överordnade teamet och klickar på **[!UICONTROL Add Team]**.

     ![Företagsstruktur med divisioner](./assets/company-structure-northwest-division.png){width="600" zoomable="yes"}

   - Anger **[!UICONTROL Team Title]** och **[!UICONTROL Description]**.

   - Klicka på **[!UICONTROL Save]**.

1. Upprepar dessa steg för att skapa så många team, eller divisioner och indelningar som behövs.

   ![Företagsstruktur med divisioner och indelningar](./assets/company-structure-divisions.png){width="600" zoomable="yes"}

## Flytta ett team

När företagsadministratören arbetar med företagsstrukturen kan de dra team eller avdelningar till andra platser i strukturen.

1. Företagsadministratören hittar teamet som ska flyttas.

1. Klicka och dra teamet till en ny position i företagsstrukturen.

## Ta bort ett team

>[!NOTE]
>
>Innan du tar bort ett team bör du kontrollera att rätt team har valts - borttagna team kan inte återställas.

1. Företagsadministratören väljer det team som ska tas bort.

1. Klicka på **[!UICONTROL Delete Selected]**.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL Delete]**.

## Expandera eller komprimera teamstrukturen

När företagsadministratören arbetar med företagsstrukturen kan de komprimera eller expandera trädet:

- Klicka på **[!UICONTROL Collapse All]** eller **[!UICONTROL Expand All]**.

- Klicka på ![Utökad ikon](../assets/icon-display-collapse.png) om du vill komprimera ett team eller på ![Komprimerad ikon](../assets/icon-display-expand.png) om du vill expandera ett team.

## Tilldela användare till team

När team och användare först läggs till i [företagsstrukturen](account-company-structure.md) placeras de på samma nivå under företagsadministratören.

![Företagsstruktur med användare och team](./assets/company-users-added.png){width="700" zoomable="yes"}

| Kontroll | Beskrivning |
|--- |--- |
| [!UICONTROL Collapse All / Expand All] | Komprimerar eller utökar affärsstrukturträdet |
| [!UICONTROL Add User] | Skapar en användare under det aktuella teamet |
| [!UICONTROL Add Team] | Skapar ett team |
| [!UICONTROL Edit Selected / Remove from Structure] | Redigerar användarinformation eller tar bort användare från affärsträdet. Mer information finns i [Hantera företagsanvändarkonton](account-company-users.md). |

{style="table-layout:auto"}

1. I den vänstra panelen väljer företagsadministratören **[!UICONTROL Company Structure]**.

1. Om du vill tilldela en användare till ett befintligt team drar de (![ikonen Flytta](../assets/icon-move.png)) användaren till rätt team.

   ![Grupptilldelningar](./assets/company-structure-teams-users-assigned.png){width="700" zoomable="yes"}
