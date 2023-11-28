---
title: Företagskonton
description: Se hur företagskonton som hanteras i din Adobe Commerce-butik gör det möjligt att gå med flera köpare som tillhör samma företag i ett enda företagskonto.
exl-id: 0b3c3635-a1cf-4ee6-a8bc-e7cbcb4e2e63
feature: B2B, Companies, Configuration
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 0%

---

# Företagskonton

När du lägger in B2B-företagskonton i din butik kan du förenkla företagets shoppingupplevelse genom att göra det möjligt för företag att skapa flera underkonton med flexibel behörighet baserat på användarroller i organisationen. Beroende på vilket företag det är kan en butiksadministratör anpassa kampanjer och priser efter deras behov och skapa skräddarsydda erbjudanden som tillgodoser kundernas krav och ökar beställningarna. Lägga till en företagskontoassociation till en standard [individuell](../customers/account-create.md) låter kunden använda de specifika inköpsarbetsflöden som definierats för företaget.

Fördelar med ett företagskonto:

- Obegränsat [företagsanvändare](account-company-users.md) och att skapa ytterligare konton, vilket förenklar företagsköp.

- Inkluderar stöd för _smart_ företagskontohierarki med annan [roller och behörigheter](account-company-roles-permissions.md) för beställningar.

- Tillhandahåller en mekanism för handlare att öka intäkterna genom att erbjuda [företagskredit](credit-company.md) som betalningsmetod.

- Stöder [hantering](account-company-manage.md) av alla företagskonton i Admin.

## Visa företagskonton

The _Företag_ visas alla aktiva företagskonton och väntande begäranden, oavsett statusinställning. Det innehåller även verktyg för [skapa](account-company-create.md) och [hantera](account-company-manage.md) företag. Använd standardkontrollerna för stödraster för att filtrera listan och justera kolumnlayouten. En lista med kolumnbeskrivningar finns i _Kolumnbeskrivningar_ avsnitt i [Hantera företagskonton](account-company-manage.md).

Kunder kan skapa ett företagskonto från butiken eller en handlare kan skapa ett från administratören. Som standard är möjligheten att skapa företagskonton från butiken aktiverad. Om konfigurationen tillåter det kan en besökare i butiken begära att få öppna ett företagskonto. När företagskontot har godkänts kan företagsadministratören ställa in företagsstrukturen och användare med olika behörighetsnivåer.

I _Administratör_ sidebar, gå till **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Företagsrutnät](./assets/companies-grid.png){width="700" zoomable="yes"}

The [!UICONTROL Companies] visas alla företag oavsett status. Det exempel som visas visar konton för två företag:&quot;ACME&quot;-företaget och&quot;Vandelay&quot;-företaget.

## Företagsadministratör

I följande exempel visas _Kunder_ rutnät med de ursprungliga företagsadministratörskontona.

![Kundrutnät med företagskonto](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

Det är möjligt att den person som fungerar som företagsadministratör har flera roller inom företaget. Om en separat e-postadress anges för företagsadministratören, innehåller den inledande företagsstrukturen företagsadministratören plus ett individuellt användarkonto i företagsadministratörens namn. I så fall kan företagsadministratören logga in på kontot som företag eller som en enskild användare.

Efter att kontot har skapats definierar företagsadministratören företagsstrukturen för [team](account-company-structure.md), ställer in [företagsanvändare](account-company-users.md)och upprättar [roller och behörigheter](account-company-roles-permissions.md) for each.

### Ange företagets administratörslösenord före första inloggningen

1. Företagsadministratören hittar ett välkomstmeddelande från butiken.

   ![Exempel på välkomstmeddelande](./assets/company-admin-welcome-email.png){width="500"}

   >[!NOTE]
   >
   >E-postadressmålen och innehållet i e-postmeddelandet bestäms av alternativen som anges i [e-postalternativ för företag](email-company-configuration.md) konfiguration.

1. Följer instruktionerna och klickar [!UICONTROL **link**] för att ange sitt lösenord.

1. Skriver in a [!UICONTROL **Nytt lösenord**] för sitt konto och på nytt för att bekräfta.

   Lösenordet måste innehålla minst tre av följande teckentyper:

   - Gemener (abc...)
   - Versaler (ABC...)
   - Nummer (1234567890)
   - Specialtecken (!@#$...)

1. Klickningar [!UICONTROL **Ange ett nytt lösenord**].

   ![Kundinloggning - företagsadministratör](./assets/company-admin-account-login.png){width="700" zoomable="yes"}

1. När [!UICONTROL Customer Login] visas, kunderna anger [!UICONTROL **E-post**] och [!UICONTROL **Lösenord**].

1. Klickningar [!UICONTROL **Logga in**] för att få åtkomst till deras kontokontrollpanel.

   ![Konto Dashboard - företag](./assets/account-dashboard-company.png){width="700" zoomable="yes"}

## Företagsstruktur

Ett företagskonto kan skapas för att återspegla affärsstrukturen. Till att börja med innehåller företagsstrukturen bara företagsadministratören, men kan utvidgas till att omfatta användargrupper. Användarna kan associeras med team eller vara organiserade i en hierarki av divisioner och indelningar inom företaget. Strukturen är utformad för att stödja användning av [regler för godkännande](account-dashboard-approval-rules.md) for [inköpsorder](purchase-order-flow.md) (PO) som är kopplade till företagskontot.

![Företagsstruktur med divisioner](./assets/company-structure-diagram.svg){width="450"}

I företagsadministratörens kontouppsättningspanel representeras företagsstrukturen som ett träd och består inledningsvis av endast företagsadministratören.

![Företagsstruktur med företagsadministratör](./assets/company-structure-tree-admin.png){width="600"}

När kontot skapas kan företagsadministratören använda företagets e-postadress eller tilldelas en annan e-postadress.

I följande exempel innehåller den inledande företagsstrukturen företagsadministratören plus ett individuellt användarkonto i namnet på företagsadministratören. Företagsadministratörsfunktioner (t.ex. företagsstruktur och godkännanderegler) är bara tillgängliga när de är inloggade på det användarkonto som har angetts som företagsadministratör.

![Företagsstruktur med administratör och användarkonto](./assets/company-structure-tree-admin-user.png){width="600"}
