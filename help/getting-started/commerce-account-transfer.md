---
title: Överföra ett Commerce-konto
description: Lär dig hur du överför ditt Commerce-konto till en annan ägare eller e-postadress.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: 03a16730eebe3979157bc9eb847ac2b232d938bf
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 1%

---

# Överföra ett Commerce-konto

När ditt ansvar förändras kan du behöva överföra ägarskapet för ditt befintliga Commerce-konto till en ny ägare eller till en annan e-postadress. Den här överföringen kräver en ändring av den primära användarens e-postadress som är kopplad till kontot.

Följande information beskriver processen för överföring av ett Commerce-konto (MAGEID). Det innehåller inga ändringar av ägarskapet för molnkontot (molnprojektet eller New Relic). Mer information om åtkomst till molnprojekt finns i [Hantera användaråtkomst](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) i _Commerce on Cloud Infrastructure Guide_.

## Identifiera din överföringstyp

Hur du slutför den här överföringen beror på vilket av följande scenarier som beskriver din situation som den nuvarande ägaren av kontot och den nya ägaren (e-postadress) till vilken du vill överföra kontot:

| Överföringstyp | Aktuell ägare | Ny ägare |
| ------------- | ------------- | --------- |
| [Ny ändring av Adobe ID och e-post](#new-adobe-id-and-email-change) | Har ett MAGEID som **_inte är anslutet_** med ett Adobe-inloggningskonto. | Har inget MAGEID och är inte anslutet till ett Adobe-inloggningskonto. |
| [E-poständring](#email-change) | Har ett MAGEID som är **_anslutet_** med ett Adobe-inloggningskonto utan andra associerade Adobe-produkter/tjänster. | Har inget MAGEID och är inte anslutet till ett Adobe-inloggningskonto. |
| [Adobe ID-växel](#adobe-id-account-switch) | Har ett MAGEID som är **_anslutet_** med ett Adobe-inloggningskonto utan andra associerade Adobe-produkter/tjänster. | Har ett MAGEID och är anslutet till ett Adobe-inloggningskonto utan andra associerade Adobe-produkter/tjänster. |

{style="table-layout:auto"}

>[!NOTE]
>
>I takt med att Adobe Commerce fortsätter att integrera med andra Adobe-lösningar kräver nu ett Commerce-konto (MAGEID) en koppling till en Adobe-inloggning. Den här Adobe ID använder samma e-postadress som är kopplad till ditt Commerce-konto.

>[!NOTE]
>
>Om den aktuella eller nya ägaren har ett Adobe-inloggningskonto som är kopplat till andra Adobe-produkter/tjänster kan du öppna en [supportbiljett](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket) för hjälp med att överföra ett Commerce-konto till en annan Adobe ID.

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

   Detta skapar en Adobe ID och länkar den till det aktuella Commerce-kontot (MAGEID). Med den här kontolänken blockeras fältet _[!UICONTROL Email]_från ändringar. Den associerade e-postadressen hanteras av Adobe ID-kontot.

1. Navigera till [account.adobe.com](https://account.adobe.com/).

1. Klicka på **[!UICONTROL Change Email]**.

1. Ange den nya ägarens e-postadress.

1. Klicka på **[!UICONTROL Change]**.

   Detta genererar ett bekräftelsemeddelande som skickas till den nya e-postadressen. E-postmeddelandet innehåller en bekräftelsekod som krävs för att slutföra ändringen av e-postadressen.

1. Ange bekräftelsekoden som skickas till den nya e-postadressen.

1. Klicka på **[!UICONTROL Verify]**.

## E-poständring

>[!IMPORTANT]
>
>Granska [överföringstyperna](#identify-your-transfer-type) och kontrollera att du uppfyller villkoren för den här stegsekvensen.

1. Gå till [account.adobe.com](https://account.adobe.com/) och fyll i inloggningen till Adobe.

1. Klicka på **[!UICONTROL Change Email]** under ditt kontonamn och din avatar.

1. Ange den nya ägarens e-postadress i dialogrutan.

1. Klicka på **[!UICONTROL Change]**.

   Detta genererar ett bekräftelsemeddelande som skickas till den nya e-postadressen. E-postmeddelandet innehåller en bekräftelsekod som krävs för att slutföra ändringen av e-postadressen.

1. Ange bekräftelsekoden som skickas till den nya e-postadressen.

1. Klicka på **[!UICONTROL Verify]**.

## Adobe ID-kontoväxel

>[!IMPORTANT]
>
>Granska [överföringstyperna](#identify-your-transfer-type) och kontrollera att du uppfyller villkoren för den här stegsekvensen.

Om den nuvarande ägaren och den nya ägaren har ett befintligt Adobe-ID bör båda kontona finnas kvar, men e-postadresserna måste växlas mellan dem. Detta kräver att du använder en giltig _tillfällig_-e-postadress som inte är associerad med och Adobe ID.

### Ändra till ett tillfälligt konto

Den aktuella ägaren slutför dessa steg för att associera sin Adobe ID med en annan tillfällig e-postadress.

1. Gå till [account.adobe.com](https://account.adobe.com/) och fyll i inloggningen till Adobe.

1. Klicka på **[!UICONTROL Change Email]** under ditt kontonamn och din avatar.

1. I dialogrutan anger du en giltig tillfällig e-postadress som inte används av en Adobe ID.

   Du måste ha tillgång till e-postadressen så att du kan hämta e-postmeddelandet med bekräftelsekoden.

1. Klicka på **[!UICONTROL Change]**.

   Detta genererar ett bekräftelsemeddelande som skickas till den temporära e-postadressen. E-postmeddelandet innehåller en bekräftelsekod som krävs för att slutföra ändringen av e-postadressen.

1. Ange bekräftelsekoden som skickas till den temporära e-postadressen.

1. Klicka på **[!UICONTROL Verify]**.

1. Logga ut från Adobe.

### Nya ägarsteg

När den aktuella ägaren har slutfört överföringen till en temporär e-postadress utför du de här stegen för att ändra kontot till den aktuella ägaren.

1. Gå till [account.adobe.com](https://account.adobe.com/) och fyll i inloggningen till Adobe.

1. Klicka på **[!UICONTROL Change Email]** under ditt kontonamn och din avatar.

1. Ange den aktuella ägarens ursprungliga e-postadress i dialogrutan.

1. Klicka på **[!UICONTROL Change]**.

   Detta genererar ett bekräftelsemeddelande som skickas till den e-postadressen. E-postmeddelandet innehåller en bekräftelsekod som krävs för att slutföra ändringen av e-postadressen.

1. Ange bekräftelsekoden som skickas till den aktuella ägaren.

1. Klicka på **[!UICONTROL Verify]**.

1. Logga ut från Adobe.

### Följ upp steg

När den nya ägaren har överfört sitt Adobe-konto till den aktuella (nu tidigare) ägaren, utför du dessa steg för att överföra ägarskapet.

1. Navigera till [account.adobe.com](https://account.adobe.com/) (det första kontot som används i serien med steg) och slutför inloggningen till Adobe.

   Den här inloggningen kräver att den tillfälliga e-postadressen används.

1. Klicka på **[!UICONTROL Change Email]** under kontonamnet och avataren.

1. Ange den nya ägarens e-postadress i dialogrutan.

1. Klicka på **[!UICONTROL Change]**.

   Detta genererar ett bekräftelsemeddelande som skickas till den e-postadressen. E-postmeddelandet innehåller en bekräftelsekod som krävs för att slutföra ändringen av e-postadressen.

1. Ange bekräftelsekoden som skickas till den nya ägaren.

1. Klicka på **[!UICONTROL Verify]**.

1. **Skicka en supportförfrågan** för att informera supportteamet om att du har uppdaterat kontoägarens e-postadress. Inkludera föregående kontoägares e-postadress i din begäran.

Supporten måste utföra ytterligare steg, till exempel uppdatera e-postadressen i din [Commerce Marketplace](https://commercemarketplace.adobe.com/) -profil.
