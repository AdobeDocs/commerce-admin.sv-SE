---
title: Skydda ditt [!DNL Commerce] konto
description: Lär dig hur du använder tvåfaktorsautentisering för att skydda ditt [!DNL Commerce] konto.
exl-id: 4847b5cb-a93a-40d0-8c31-c30afa27c0ce
feature: User Account
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1677'
ht-degree: 0%

---

# Skydda ditt [!DNL Commerce]-konto

Tvåfaktorautentisering (TFA eller 2FA) är ett extra säkerhetslager som bättre skyddar ditt [!DNL Commerce]-konto från obehörig åtkomst. För att slutföra inloggningsprocessen krävs en _andra faktor_, förutom standardautentiseringsuppgifterna för användarnamn och lösenord, för TFA. Den andra faktorn har formen av tillfälliga verifieringskoder som kontinuerligt genereras av ett TFA-program som är installerat på din mobila enhet och som är kopplade till ditt [!DNL Commerce]-konto.

Om TFA är aktiverat är ditt konto säkrare. En obehörig användare kan inte logga in om de inte har både ditt användarnamn och lösenord (första faktorn) och en giltig verifieringskod från TFA-programmet på din personliga enhet (andra faktor).

>[!NOTE]
>
>Den tvåfaktorsautentisering som skyddar _Admin_ i din butik har en separat inställning. Mer information finns i [Tvåfaktorautentisering](../systems/security-two-factor-authentication.md).

## Innan du börjar

Om du vill använda TFA måste du ha ett TFA-program installerat på din personliga enhet (till exempel din smarttelefon, surfplatta eller dator). Det finns många tillgängliga alternativ, men några populära och kostnadsfria alternativ är:

- Google Authenticator (iOS, Android™, BlackBerry®)

- Authy (iOS, Android™)

- Microsoft® Authenticator (iOS, Android™, Windows Phone)

## Aktivera tvåfaktorsautentisering

1. Logga in på ditt [[!DNL Commerce] konto](https://account.magento.com/customer/account/login){:target="_blank"}.

1. I den vänstra navigeringsrutan väljer du **[!UICONTROL Account Settings]** och sedan **[!UICONTROL Two-factor Authentication]**.

   ![Aktivera TFA](./assets/2fa-enable.png){width="600" zoomable="yes"}

1. Välj **[!UICONTROL Enable]** om du vill påbörja konfigurationen av tvåfaktorsautentisering.

1. Ange **[!UICONTROL Verification Code]** som skickats till ditt e-postmeddelande och välj **[!UICONTROL Verify Code]** för att fortsätta.

   ![Ange verifieringskoden](./assets/2fA-verification-code-prompt.png){width="400"}

1. Öppna det tvåfaktorsautentiseringsprogram som du har laddat ned och installerat på din personliga enhet.

1. Använd [!UICONTROL SETUP TWO-FACTOR AUTHENTICATION] i formuläret **[!UICONTROL Setup Code]** för att lägga till Adobe Commerce i ditt TFA-program.

   ![Lägg till Adobe Commerce i TFA-appen](./assets/commerce-account-2fa-setup-app.png){width="400"}

   Du kan lägga till koden genom att skanna QR-koden med TFA-programmet eller genom att ange den manuellt. Den här koden parar ihop ditt TFA-program med ditt [!DNL Commerce]-konto och aktiverar behörigheten att generera TFA-appen för att generera verifieringskoder för säker kontoåtkomst.

1. Slutför installationen.

   - I formuläret [!UICONTROL SETUP TWO FACTOR-AUTHENTICATION] anger du verifieringskoden från ditt tvåfaktorautentiseringsprogram.

   - Välj **[!UICONTROL Verify Code]**.

   >[!NOTE]
   >
   >Av säkerhetsskäl upphör verifieringskoderna i TFA-programmet att gälla och genereras om kontinuerligt. **_Använd alltid_** koden som visas.

1. Spara **[!UICONTROL Recovery Codes]** som visas på en säker och tillgänglig plats.

   ![Lagra återställningskoder](./assets/commerce-account-2fa-store-recovery-codes.png){width="400"}

   Om du inte kan ange en verifieringskod när du loggar in på ditt [!DNL Commerce]-konto måste du använda en återställningskod för att återfå kontoåtkomst.

   Varje återställningskod kan bara användas en gång, men du kan [generera](#generate-new-recovery-codes) nya. Återställningskoderna är skiftlägeskänsliga.

1. Markera bekräftelsekryssrutan och välj **[!UICONTROL Submit]** för att fortsätta.

1. Ange en **[!UICONTROL Recovery Email]** om du vill försäkra dig om att du kan återställa åtkomsten till ditt konto.

   Den här e-postadressen behövs om du inte kan generera en verifieringskod från ditt tvåfaktorautentiseringsprogram och du inte har tillgång till en oanvänd förgenererad återställningskod.

   Var 24:e timme kan du generera och skicka en tillfällig återställningskod till den angivna e-postadressen för återställning. Använd den här koden för att återta kontoåtkomst.

   >[!IMPORTANT]
   >
   >Behåll åtkomst till ditt e-postkonto för återställning. Annars kan du inte använda tillfälliga återställningskoder som skickas till det kontot.

   ![Ange e-post för återställning](./assets/commerce-account-2fa-set-recovery-email.png){width="400"}

1. Markera bekräftelsekryssrutan och välj **[!UICONTROL Submit]** för att slutföra konfigureringsprocessen för tvåfaktorsautentisering.

   - Ett meddelande skickas till den e-postadress som är kopplad till ditt [!DNL Commerce]-konto för att bekräfta att du har aktiverat tvåfaktorautentisering.

   - Ett meddelande skickas till ditt e-postkonto för återställning för att bekräfta konfigurationen.

>[!TIP]
>
>Om du förlorar din personliga enhet eller skaffar en ny kan du [ändra din tvåfaktorautentiseringsapp](#change-your-two-factor-authentication-application) och generera nya återställningskoder.

## Logga in med en verifieringskod

1. Gå till [!DNL Commerce] [kontoinloggningen](https://account.magento.com/customer/account/login){:target="_blank"}.

1. Ange ditt användarnamn och lösenord och välj sedan **[!UICONTROL Login]**.

1. Ange **[!UICONTROL Verification Code]** som visas i ditt tvåfaktorautentiseringsprogram när du uppmanas till det.

   ![Ange verifieringskod](./assets/commerce-account-2fa-login-verification-code.png){width="600"}

1. Välj **[!UICONTROL Submit]** för att slutföra inloggningsprocessen.

## Logga in med en återställningskod

1. Gå till [!DNL Commerce] [kontoinloggningen](https://account.magento.com/customer/account/login){:target="_blank"}.

1. Ange ditt användarnamn och lösenord och välj sedan **[!UICONTROL Login]**.

1. Välj **[!UICONTROL Use recovery code]** om du vill kringgå uppmaningen om verifieringskod.

1. Ange en oanvänd **[!UICONTROL Recovery Code]** när du uppmanas till det.

   ![Ange återställningskod](./assets/2fa-recovery-code.png){width="600"}

1. Välj **[!UICONTROL Submit]** för att slutföra inloggningsprocessen.

## Logga in med ditt återställningsmejl

1. Logga in på ditt [[!DNL Commerce] konto](https://account.magento.com/customer/account/login){:target="_blank"}.

1. Ange ditt användarnamn och lösenord och välj sedan **[!UICONTROL Login]**.

1. Välj **[!UICONTROL Use recovery code]** om du vill kringgå uppmaningen om verifieringskod.

1. Om du vill hämta en tillfällig återställningskod via e-post väljer du länken **[!UICONTROL recovery email]**.

   ![Använd e-post för återställning](./assets/2fa-recovery-email.png){width="600"}

1. Öppna ditt e-postkonto för återställning för att hämta den tillfälliga koden och ange sedan koden i de angivna fälten.

1. Välj **[!UICONTROL Submit]** för att slutföra inloggningsprocessen.

När du har använt en tillfällig återställningskod för att komma åt ditt konto, [genererar nya återställningskoder](#generate-new-recovery-codes) och sparar dem för att förhindra ytterligare problem med kontoåtkomst.

## Visa dina återställningskoder

1. Gå till [!DNL Commerce] [kontoinloggningen](https://account.magento.com/customer/account/login){:target="_blank"}.

1. Ange ditt användarnamn och lösenord och välj sedan **[!UICONTROL Login]**.

1. Slutför inloggningsprocessen med en av de två autentiseringsmetoder som beskrivs ovan.

1. I den vänstra navigeringsrutan väljer du **[!UICONTROL Account Settings]** och sedan **[!UICONTROL Two-factor Authentication]**.

   ![2FA-inställningar](./assets/commerce-account-2fa-manage.png){width="600" zoomable="yes"}

1. Om du vill visa dina förgenererade återställningskoder väljer du **Visa återställningskoder**.

1. Ange **[!UICONTROL Verification Code]** som skickats till ditt e-postmeddelande och välj **[!UICONTROL Verify Code]** för att fortsätta.

   ![Ange verifieringskod](./assets/2fA-verification-code-prompt.png){width="400"}

1. Spara **återställningskoderna** som visas på en säker och tillgänglig plats.

   Om du inte kan ange en verifieringskod för att logga in på ditt [!DNL Commerce]-konto är det enda sättet att återta kontoåtkomst att använda en återställningskod.

   Varje återställningskod används endast en gång, men du kan alltid [generera](#generate-new-recovery-codes) nya. Återställningskoderna är skiftlägeskänsliga.

   ![Visa återställningskoder](./assets/2fa-view-recovery.png){width="400"}

1. Markera bekräftelsekryssrutan och välj **[!UICONTROL Submit]** för att stänga dialogrutan.

## Generera nya återställningskoder

1. Gå till [!DNL Commerce] [kontoinloggningen](https://account.magento.com/customer/account/login){:target="_blank"}.

1. Ange ditt användarnamn och lösenord och välj sedan **[!UICONTROL Login]**.

1. Slutför inloggningsprocessen med en av de två autentiseringsmetoder som beskrivs ovan.

1. I den vänstra navigeringsrutan väljer du **[!UICONTROL Account Settings]** och sedan **[!UICONTROL Two-factor Authentication]**.

1. Om du vill generera nya förgenererade återställningskoder väljer du **Skapa nya återställningskoder**.

1. Ange **[!UICONTROL Verification Code]** som skickats till ditt e-postmeddelande och välj **[!UICONTROL Verify Code]** för att fortsätta.

1. Spara **återställningskoderna** som visas på en säker och tillgänglig plats.

   Om du inte kan ange en verifieringskod när du loggar in på ditt [!DNL Commerce]-konto är det enda sättet att återfå kontoåtkomst att använda en återställningskod.

   Alla tidigare genererade återställningskoder renderas nu som ogiltiga och bör ignoreras (endast den aktuella uppsättningen genererade återställningskoder fungerar). Återställningskoderna är skiftlägeskänsliga.

1. Markera bekräftelsekryssrutan och välj **[!UICONTROL Submit]** för att stänga dialogrutan.

## Ändra ditt återställningsmejl

1. Gå till [!DNL Commerce] [kontoinloggningen](https://account.magento.com/customer/account/login){:target="_blank"}.

1. Ange ditt användarnamn och lösenord och välj sedan **[!UICONTROL Login]**.

1. Slutför inloggningsprocessen med en av de två autentiseringsmetoder som beskrivs ovan.

1. I den vänstra navigeringsrutan väljer du **[!UICONTROL Account Settings]** och sedan **[!UICONTROL Two-factor Authentication]**.

1. Välj **Ändra återställningens e-postadress** om du vill ändra återställningens e-postadress för ditt konto.

1. Ange **[!UICONTROL Verification Code]** som skickats till ditt e-postmeddelande och välj **[!UICONTROL Verify Code]** för att fortsätta.

1. Ange ett **återställningsmeddelande** om du vill försäkra dig om att du kan återställa åtkomsten till ditt konto.

   Den här e-postadressen behövs om du inte kan generera en verifieringskod från ditt tvåfaktorautentiseringsprogram och du inte har tillgång till en oanvänd förgenererad återställningskod.

   Var 24:e timme kan du generera och skicka en tillfällig återställningskod till den angivna e-postadressen för återställning. Du kan använda den här koden för att återfå kontoåtkomst.

   >[!IMPORTANT]
   >
   >Behåll åtkomst till ditt e-postkonto för återställning. Annars kan du inte använda tillfälliga återställningskoder som skickas till det kontot.

1. Markera bekräftelsekryssrutan och välj **[!UICONTROL Submit]** för att stänga dialogrutan.

   Systemet skickar ett e-postmeddelande till det återställningsmeddelande som du har angett för att bekräfta att en viss e-postadress finns i filen som ditt återställningsmeddelande för att ta emot tillfälliga återställningskoder.

## Ändra ditt tvåfaktorautentiseringsprogram

1. Gå till [!DNL Commerce] [kontoinloggningen](https://account.magento.com/customer/account/login){:target="_blank"}.

1. Ange ditt användarnamn och lösenord och välj sedan **[!UICONTROL Login]**.

1. Slutför inloggningsprocessen med en av de två autentiseringsmetoder som beskrivs ovan.

1. I den vänstra navigeringsrutan väljer du **[!UICONTROL Account Settings]** och sedan **[!UICONTROL Two-factor Authentication]**.

1. Välj **Ändra TFA-program** om du vill använda ett annat TFA-program med ditt magento.com.

1. Ange **[!UICONTROL Verification Code]** som skickats till ditt e-postmeddelande och välj **[!UICONTROL Verify Code]** för att fortsätta.

1. Öppna tvåfaktorsautentiseringsprogrammet på din personliga enhet.

1. Ange **inställningskod** i ditt tvåfaktorautentiseringsprogram.

   Du kan lägga till koden genom att skanna QR-koden med TFA-programmet eller genom att ange den manuellt. Den här koden parar ihop ditt TFA-program med ditt [!DNL Commerce]-konto och aktiverar behörigheterna för TFA-appen för att generera verifieringskoder för säker kontoåtkomst.

   >[!NOTE]
   >
   >Av säkerhetsskäl upphör verifieringskoderna i TFA-programmet att gälla och genereras om kontinuerligt. **_Använd alltid_** koden som visas.

1. När ditt TFA-program nu har parats ihop med ditt [!DNL Commerce]-konto anger du **[!UICONTROL Verification Code]** som visas i ditt TFA-program och väljer **[!UICONTROL Verify Code]** för att fortsätta.

1. Spara **återställningskoderna** som visas på en säker och tillgänglig plats.

   Om du inte kan ange en verifieringskod när du loggar in på ditt [!DNL Commerce]-konto kan du bara återfå kontoåtkomst genom att använda en återställningskod.

   Varje återställningskod används endast en gång, men du kan alltid [generera](#generate-new-recovery-codes) nya. Återställningskoderna är skiftlägeskänsliga. Återställningskoderna är skiftlägeskänsliga.

1. Markera kryssrutan för att bekräfta och välj **[!UICONTROL Submit]** för att fortsätta.

1. Ange ett **återställningsmeddelande** om du vill försäkra dig om att du kan återställa åtkomsten till ditt konto.

   Den här e-postadressen behövs om du inte kan generera en verifieringskod från ditt tvåfaktorautentiseringsprogram och du inte har tillgång till en oanvänd förgenererad återställningskod.

   Var 24:e timme kan du generera och skicka en tillfällig återställningskod till den angivna e-postadressen för återställning. Använd den här koden för att återta kontoåtkomst.

   >[!IMPORTANT]
   >
   >Behåll åtkomst till ditt e-postkonto för återställning. Annars kan du inte använda tillfälliga återställningskoder som skickas till det kontot.

1. Markera bekräftelsekryssrutan och välj **[!UICONTROL Submit]** för att slutföra konfigureringsprocessen för tvåfaktorsautentisering.

   Ett e-postmeddelande skickas till det återställningsmejl som du har angett för att bekräfta att en viss e-postadress finns i filen som återställningsmejl för att du ska få en tillfällig återställningskod.

## Inaktivera tvåfaktorsautentisering

>[!IMPORTANT]
>
>Om din organisationssäkerhetsprincip kräver multifaktorautentisering på Adobe Commerce-konton kan du inte inaktivera tvåfaktorsautentisering.

1. Gå till [!DNL Commerce] [kontoinloggningen](https://account.magento.com/customer/account/login){:target="_blank"}.

1. Ange ditt användarnamn och lösenord och välj sedan **[!UICONTROL Login]**.

1. Slutför inloggningsprocessen med en av de två autentiseringsmetoder som beskrivs ovan.

1. I den vänstra navigeringsrutan väljer du **[!UICONTROL Account Settings]** och sedan **[!UICONTROL Two-factor Authentication]** under.

1. Välj **[!UICONTROL Disable]** för att påbörja inaktiveringsprocessen för TFA.

1. Ange **[!UICONTROL Verification Code]** som skickats till ditt e-postmeddelande och välj **[!UICONTROL Verify Code]** för att fortsätta.

1. Markera bekräftelsekryssrutan och välj **[!UICONTROL Submit]** för att slutföra inaktiveringen för tvåfaktorsautentisering.

   Systemet skickar en e-postbekräftelse som anger att TFA har inaktiverats på ditt [!DNL Commerce]-konto.

   ![Inaktivera TFA](./assets/2fa-disable.png){width="400"}
