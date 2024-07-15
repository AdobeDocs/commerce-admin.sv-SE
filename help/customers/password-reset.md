---
title: Återställ kundlösenord
description: Kunder återställer vanligtvis sina lösenord från butiken, men en butiksadministratör kan initiera antingen en lösenordsåterställning eller en tvingad inloggning från administratören.
exl-id: bca1ef3e-2bc6-4146-ac86-d6c58c8995e4
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Återställ kundlösenord

Kunder återställer vanligtvis sina lösenord från butiken genom att klicka på _[!UICONTROL Forgot Your Password?]_. Butiksadministratören kan dock initiera en lösenordsåterställning eller en tvingad inloggning från administratören.

| Funktion | Beskrivning |
| --- | --- |
| Återställ lösenord | Ett e-postmeddelande för återställning av lösenord skickas direkt till kundens e-postkonto. Butiksadministratören kan inte få åtkomst till kundens lösenord. |
| Tvinga inloggning | Återkallar OAuth-åtkomsttoken som är associerade med kundkontot. Detta kan bara användas med kundkonton som har tilldelats OAuth-token, som en del av ett webb-API [integration](../systems/integrations.md). Mer information finns i [OAuth-baserad autentisering](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) i utvecklardokumentationen. <br/><br/>Standardkundkonton som skapats från butiken eller från Admin har inte OAuth-tokens. |

{style="table-layout:auto"}

## Återställ ett lösenord från butiken

1. På inloggningssidan klickar kunden på **[!UICONTROL Forgot Your Password?]**.

1. När du uppmanas till det anger du **[!UICONTROL Email Address]** som är associerad med deras konto och klickar på **[!UICONTROL Reset My Password]**.

   ![Har glömt lösenordet](assets/forgot-password.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >Om den angivna e-postadressen matchar den som är kopplad till kontot får kunden ett e-postmeddelande med en länk för att återställa lösenordet.

1. När e-postmeddelandet kommer klickar kunden på länken _reset password_ och anger sin **[!UICONTROL New Password]** när han/hon uppmanas till det.

1. Skriver in den igen för att bekräfta och klickar på **[!UICONTROL Reset Password]**.

   >[!IMPORTANT]
   >
   >Det nya lösenordet måste innehålla minst sex tecken utan blanksteg. När de får en bekräftelse på att lösenordet har uppdaterats kan de använda det nya lösenordet för att logga in på sitt konto. Som standard är länken _reset password_ giltig i 24 timmar.

## Återställ ett lösenord från administratören

1. Gå till **[!UICONTROL Customers]** > **[!UICONTROL All Customers]** på sidofältet _Admin_.

1. Hitta kundkontot i rutnätet och klicka på **[!UICONTROL Edit]** i kolumnen _Åtgärd_.

1. Klicka på **[!UICONTROL Reset Password]** i uppsättningen med alternativ längst upp på sidan.

   Antalet begäranden om återställning av lösenord som tillåts inom en timme anges i avsnittet [configuration](../configuration-reference/customers/customer-configuration.md).

## Återkalla en kunds OAuth-token

>[!IMPORTANT]
>
>Fortsätt inte om du inte har fullständig förståelse för API-autentisering.

1. Gå till **[!UICONTROL Customers]** > **[!UICONTROL All Customers]** på sidofältet _Admin_.

1. Hitta kundkontot i rutnätet och klicka på **[!UICONTROL Edit]** i kolumnen _Åtgärd_.

1. Klicka på **[!UICONTROL Force Sign In]** i uppsättningen med alternativ längst upp på sidan.

1. När du uppmanas att bekräfta klickar du på **OK**.
