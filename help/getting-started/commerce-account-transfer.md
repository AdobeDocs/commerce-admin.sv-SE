---
title: Överföra ett Commerce-konto
description: Lär dig hur du överför ditt Commerce-konto till en annan ägare eller e-postadress.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: b66fd3fad065f78726eb368b5ba06f0f61174356
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 1%

---

# Överföra ett Commerce-konto

När ditt ansvar förändras kan du behöva överföra ditt Commerce-konto till en ny ägare eller till en annan e-postadress. Den här överföringen kräver en ändring av den primära användarens e-postadress som är kopplad till kontot.

Följande information beskriver processen för överföring av ett Commerce-konto (MAGEID). Det innehåller inga ändringar av ägarskapet för molnkontot (molnprojektet eller New Relic). Mer information om åtkomst till molnprojekt finns i [Hantera användaråtkomst](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html?lang=sv-SE) i _Commerce on Cloud Infrastructure Guide_.

>[!IMPORTANT]
>
>Om den nya kontoägaren har köpt tillägg med delad åtkomst, kommer åtkomsten till tilläggen att förloras så snart kontoöverföringsprocessen har initierats. Innan du begär kontoöverföringen kontrollerar du att den nya ägaren hämtar order-ID:n för köp från [deras Marketplace-konto](https://commercemarketplace.adobe.com/sales/order/history/) och begär en återbetalning för dessa tillägg från [Marketplace-teamet](https://experienceleague.adobe.com/sv/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case). Det går inte att överföra tilläggsköp till ett annat konto.

## Identifiera din överföringstyp

Vilken typ av kontoöverföring som Commerce har beror på vilka inloggningsuppgifter för Commerce-kontot som är tillgängliga för den aktuella ägaren och den nya ägaren. I följande scenarier beskrivs de olika överföringstyperna baserat på dessa autentiseringsuppgifter.

| Överföringstyp | Aktuell ägare | Ny ägare |
| ------------- | ------------- | --------- |
| [Ny ändring av Adobe ID och e-post](#new-adobe-id-and-email-change) | Har ett MAGEID som **_inte är anslutet_** med ett Adobe-inloggningskonto. | Har inget MAGEID och är inte anslutet till ett Adobe-inloggningskonto. |
| [E-poständring](#email-change) | Har ett MAGEID som är **_anslutet_** med ett Adobe-inloggningskonto. | Har inget MAGEID och är inte anslutet till ett Adobe-inloggningskonto. |
| [Adobe ID-växel](#adobe-id-account-switch) | Har ett MAGEID som är **_anslutet_** med ett Adobe-inloggningskonto. | Har ett MAGEID och är anslutet till ett Adobe-inloggningskonto. |

{style="table-layout:auto"}

>[!NOTE]
>
>När Adobe Commerce fortsätter att integrera med andra Adobe-lösningar kräver nu ett Commerce-konto (MAGEID) en koppling till en Adobe-inloggning. Den här Adobe ID använder samma e-postadress som är kopplad till ditt Commerce-konto.

## Ny ändring av Adobe ID och e-post

>[!IMPORTANT]
>
>Granska [överföringstyperna](#identify-your-transfer-type) och kontrollera att du uppfyller villkoren för den här stegsekvensen.

Den här överföringstypen kräver att du först skapar en associerad Adobe ID och sedan ändrar kontot till den nya ägarens e-postadress.

1. Gå till ditt [Commerce-konto](https://account.magento.com/customer/account/login/).

1. Klicka på **[!UICONTROL Sign in with Adobe ID]**.

1. Klicka på **[!UICONTROL Create an account]**.

1. Ange den aktuella ägarens e-postadress och ett lösenord.

1. Klicka på **[!UICONTROL Continue]**.

   I det här steget skapas en Adobe ID och den länkas till det aktuella Commerce-kontot (MAGEID). Med den här kontolänken blockeras fältet _[!UICONTROL Email]_&#x200B;från ändringar. Konfigurationen av den associerade e-postadressen hanteras från Adobe ID-kontot.

1. Navigera till [account.adobe.com](https://account.adobe.com/).

1. Klicka på **[!UICONTROL Change Email]**.

1. Ange den nya ägarens e-postadress.

   Om den nya e-postadressen redan är länkad till ett annat konto i systemet kan den inte användas direkt för överföringen. Processen kräver i stället att du använder en [tillfällig e-postadress](#change-to-a-temporary-account) för att underlätta ändringen.

1. Klicka på **[!UICONTROL Change]**.

   I det här steget skapas ett bekräftelsemeddelande som skickas till den nya e-postadressen. E-postmeddelandet innehåller en bekräftelsekod som krävs för att slutföra ändringen av e-postadressen.

1. Ange bekräftelsekoden som skickas till den nya e-postadressen.

1. Klicka på **[!UICONTROL Verify]**.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## E-poständring

>[!IMPORTANT]
>
>Granska [överföringstyperna](#identify-your-transfer-type) och kontrollera att du uppfyller villkoren för den här stegsekvensen.

1. Gå till [account.adobe.com](https://account.adobe.com/) och fyll i Adobe-inloggningen.

1. Klicka på **[!UICONTROL Change Email]** under ditt kontonamn och din avatar.

1. Ange den nya ägarens e-postadress i dialogrutan.

   Om den nya e-postadressen redan är länkad till ett annat konto i systemet kan den inte användas direkt för överföringen. Processen kräver i stället att du använder en [tillfällig e-postadress](#change-to-a-temporary-account) för att underlätta ändringen.

1. Klicka på **[!UICONTROL Change]**.

   I det här steget skapas ett bekräftelsemeddelande som skickas till den nya e-postadressen. E-postmeddelandet innehåller en bekräftelsekod som krävs för att slutföra ändringen av e-postadressen.

1. Ange bekräftelsekoden som skickas till den nya e-postadressen.

1. Klicka på **[!UICONTROL Verify]**.

## Adobe ID-kontoväxel

>[!IMPORTANT]
>
>Granska [överföringstyperna](#identify-your-transfer-type) och kontrollera att du uppfyller villkoren för den här stegsekvensen.

Om den nuvarande ägaren och den nya ägaren har ett befintligt Adobe-ID bör båda kontona finnas kvar, men e-postadresserna måste växlas mellan dem. Detta kräver att en giltig _tillfällig_-e-postadress används, men den är inte associerad med en Adobe ID.

### Ändra till ett tillfälligt konto

Den aktuella ägaren slutför dessa steg för att associera sin Adobe ID med en annan tillfällig e-postadress.

1. Gå till [account.adobe.com](https://account.adobe.com/) och fyll i Adobe-inloggningen.

1. Klicka på **[!UICONTROL Change Email]** under ditt kontonamn och din avatar.

1. I dialogrutan anger du en giltig tillfällig e-postadress som inte används av en Adobe ID.

   Du måste ha tillgång till e-postadressen så att du kan hämta e-postmeddelandet med bekräftelsekoden.

1. Klicka på **[!UICONTROL Change]**.

   Det här steget genererar ett bekräftelsemeddelande som skickas till den temporära e-postadressen. E-postmeddelandet innehåller en bekräftelsekod som krävs för att slutföra ändringen av e-postadressen.

1. Ange bekräftelsekoden som skickas till den temporära e-postadressen.

1. Klicka på **[!UICONTROL Verify]**.

1. Logga ut från Adobe-kontot.

### Nya ägarsteg

När den aktuella ägaren har slutfört överföringen till en temporär e-postadress måste den nya ägaren utföra de här stegen för att ändra kontokonfigurationen så att den pekar på den aktuella ägarens ursprungliga e-postadress.

1. Gå till [account.adobe.com](https://account.adobe.com/) och fyll i Adobe-inloggningen.

1. Klicka på **[!UICONTROL Change Email]** under ditt kontonamn och din avatar.

1. Ange den aktuella ägarens ursprungliga e-postadress i dialogrutan.

1. Klicka på **[!UICONTROL Change]**.

   I det här steget skapas ett bekräftelsemeddelande som skickas till den aktuella ägarens ursprungliga e-postadress. E-postmeddelandet innehåller en bekräftelsekod som krävs för att slutföra ändringen av e-postadressen.

1. Ange bekräftelsekoden som skickas till den aktuella ägarens ursprungliga e-postadress.

1. Klicka på **[!UICONTROL Verify]**.

1. Logga ut från Adobe-kontot.

### Följ upp steg

När den nya ägaren har konfigurerat sitt Adobe-konto med den ursprungliga e-postadressen till den aktuella (nu tidigare) ägaren följer du de här stegen för att överföra ägarskap.

1. Gå till [account.adobe.com](https://account.adobe.com/) och fyll i Adobe-inloggningen med e-postadressen för det [tillfälliga kontot](#change-to-a-temporary-account).

1. Klicka på **[!UICONTROL Change Email]** under kontonamnet och avataren.

1. Ange den nya ägarens e-postadress i dialogrutan.

1. Klicka på **[!UICONTROL Change]**.

   I det här steget skapas ett bekräftelsemeddelande som skickas till den nya ägarens e-postadress. E-postmeddelandet innehåller en bekräftelsekod som krävs för att slutföra ändringen av e-postadressen.

1. Ange bekräftelsekoden som skickas till den nya ägarens e-postadress.

1. Klicka på **[!UICONTROL Verify]**.

>[!IMPORTANT]
>
>Skicka en supportförfrågan för att informera supportteamet om att du har uppdaterat kontoägarens e-postadress. Teamet måste utföra ytterligare steg för att slutföra uppdateringen, till exempel uppdatera e-postadressen för din [Commerce Marketplace](https://commercemarketplace.adobe.com/) -profil. Inkludera föregående kontoägares e-postadress i din begäran.
