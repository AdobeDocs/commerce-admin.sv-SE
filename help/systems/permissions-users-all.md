---
title: Hantera administratörsanvändarkonton
description: Lär dig hur du skapar administratörskonton och tilldelar roller för att ge administratörsfunktioner behörigheter.
exl-id: 65cca7a8-3d44-4c8c-a758-c0de03d53e11
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# Hantera administratörsanvändarkonton

När din butik installeras första gången skapas ett administratörskonto med inloggningsuppgifter som ger dig fullständig administrativ åtkomst. Det är en god vana att skapa ett annat användarkonto med fullständig administratörsåtkomst. På så sätt kan du använda ett konto för dina dagliga administrativa aktiviteter och reservera det andra som ett superadministratörskonto. Detta kan vara praktiskt om du glömmer dina vanliga inloggningsuppgifter eller om de på något sätt blir oanvändbara.

Om det finns andra i teamet eller tjänsteleverantörerna som behöver åtkomst, kan du skapa ett separat användarkonto för varje och tilldela begränsad åtkomst baserat på vad de behöver veta. Om du vill begränsa vilka webbplatser och butiker som användare kan komma åt i Admin måste du först [skapa en roll](permissions-user-roles.md) med begränsat omfång och endast de resurser som behövs. Sedan kan du tilldela rollen till ett specifikt användarkonto. Administratörsanvändare som har tilldelats en begränsad roll kan endast visa och ändra data för webbplatser eller butiker som är associerade med rollen, men kan inte ändra några globala inställningar eller data.

>[!NOTE]
>
>Adobe Commerce-handlare som har en Adobe ID och vill ha en smidig inloggning på Adobe Commerce och Adobe Business-produkter kan integrera Commerce-autentisering med Adobe IMS-autentiseringsarbetsflödet. När integreringen har aktiverats för din Commerce Store måste varje Admin-användare använda sina inloggningsuppgifter för Adobe, inte sina Commerce-autentiseringsuppgifter, för att logga in. Se [Integreringsöversikt för Adobe Identity Management-tjänst (IMS)](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

För användare och roller som är tillfälliga kan du även ange ett förfallodatum för användarkontot.

<!--  update this to a better info-graphic ![User types for your Admin](./assets/merchant-admin-users.png) -->

## Skapa en användare

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Klicka på i det övre högra hörnet **[!UICONTROL Add New User]**.

   Om du vill redigera en befintlig användare klickar du på ett användarnamn i rutnätet. Du kan ändra _[!UICONTROL User Info]_och_[!UICONTROL User Role]_ vid behov.

1. I _[!UICONTROL Account Information]_gör du följande:

   ![Användarkontoinformation](./assets/permissions-user-new.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL User Name]** för konto.

     Användarnamnet ska vara lätt att komma ihåg. Den är inte skiftlägeskänslig. Om användarnamnet till exempel är `John`kan de också logga in som `john`.

   - Fyll i följande information:

      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**
      - **[!UICONTROL Email address]**

     Varje användarkonto måste ha en unik e-postadress.

   - Ange en **[!UICONTROL Password]** för kontot.

     >[!NOTE]
     >
     >Ett administratörslösenord måste innehålla minst sju tecken och innehålla både bokstäver och siffror. Ytterligare lösenordsalternativ finns i [Konfigurera administratörssäkerhet](security-admin.md).

   - För **[!UICONTROL Password Confirmation]** anger du lösenordet igen för att vara säker på att det angavs korrekt.

   - Om din butik har flera språk anger du **[!UICONTROL Interface Locale]** till det språk som ska användas för administratörsgränssnittet.

1. Ange **[!UICONTROL This Account is]** till `Active`.

1. Klicka på kalenderikonen för att ange **[!UICONTROL Expiration Date]** för användarkontot.

   Det är praktiskt att definiera ett förfallodatum när en användare eller roll är tillfällig. Efter förfallodatumet ändras användarkontots status till `Inactive` och kan uppdateras vid behov.

1. Under _[!UICONTROL Current User Identity Verification]_anger du lösenordet för ditt användarkonto.

>[!IMPORTANT]
>
>Med _[!UICONTROL Account Information]_-avsnittet är klart kan du spara användaren. Den nya användaren visas i_[!UICONTROL Users]_ rutnät, men användarnamnet kan inte logga in förrän en roll har tilldelats.

## Tilldela en användarroll

1. Klicka på i den vänstra panelen **[!UICONTROL User Role]**.

   I rutnätet visas alla befintliga användarroller. En ny butik _[!UICONTROL Administrators]_är den enda tillgängliga rollen.

   ![Administratör - lägg till ny användarroll](./assets/permissions-user-roles.png){width="600" zoomable="yes"}

1. I _[!UICONTROL Assigned]_väljer du en användarroll.

   Du kan [visa befintliga eller definiera ytterligare användarroller](permissions-user-roles.md). När en roll har definierats måste du redigera användarkontot för att tilldela den nya rollen.

## Verifiera eller återställa 2FA-leverantörer

1. Öppna administratörens användarkonto.

1. Klicka på i den vänstra panelen **[!UICONTROL 2FA]**.

   ![Administratör - lägg till ny användarroll](./assets/permissions-user-2fa.png){width="600" zoomable="yes"}

1. Verifiera de 2FA-lösningar som är tillgängliga för _Administratör_ och råda alla användare att installera de lösningar de vill använda innan de loggar in.

   Endast en 2FA-lösning krävs för att logga in på _Administratör_.

1. Om användaren behöver installera om 2FA-lösningen kan du återställa den aktuella 2FA-konfigurationen.

   Detta kräver att användaren upprepar installationsprocessen innan han/hon kan logga in igen. Användaren kan till exempel ha en ny smartphone och måste installera om Google Authenticator. Om du vill rensa användarens nuvarande 2FA-inställningar klickar du på **[!UICONTROL Reset (Provider)]** för varje lösning som du vill rensa. Klicka på **[!UICONTROL OK]** för att bekräfta.

   Användaren får ett e-postmeddelande med en länk till [konfigurera 2FA](security-two-factor-authentication.md). Länken kan bara användas en gång. Om användaren försöker logga in flera gånger skickas en ny länk efter varje försök.

1. Klicka på **[!UICONTROL Save User]**.

1. Bekräfta din identitet genom att ange ditt lösenord och klicka igen **[!UICONTROL Save User]**.

   The _[!UICONTROL Users]_rutnätet öppnas och alla användare visas.

## Ta bort en administratörsanvändare

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Leta upp användarkontot med hjälp av filter ovanför rutnätet och klicka på användarnamnet.

1. Ange ditt lösenord för att bekräfta din identitet när du uppmanas till detta.

1. Klicka på i det övre högra hörnet **[!UICONTROL Delete User]**.

1. Bekräfta åtgärden genom att klicka **[!UICONTROL OK]**.

## Glömt lösenord och återställ e-post

Konfigurationen av administratörens e-postmall avgör vilka e-postmeddelanden som skickas när användarna glömmer bort och återställer sina lösenord. Den här konfigurationen anger den butikskontakt som visas som meddelandets avsändare och hur länge länken för lösenordsåterställning är giltig.

**_Så här konfigurerar du e-postmallar för administratörer:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Setting]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL Admin]**.

1. Expandera ![expansionskonverterare](../assets/icon-display-expand.png) den **[!UICONTROL Admin User Emails]** -avsnitt.

   ![Avancerad konfiguration - inställningar för administratörens e-postmall](../configuration-reference/advanced/assets/admin-admin-user-emails.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Forgot Password Email Template]** till mallen som skickas när en Admin-användare glömmer sina lösenord.

1. Ange **[!UICONTROL Forgot and Reset Email Sender]** till den butikskontakt som visas som avsändare av meddelandet.

1. Ange **[!UICONTROL User Notification Template]** till e-postmallen som används som standard för administratörsmeddelanden.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Låsta användare

Av säkerhetsskäl låses användarkonton som standard efter sex misslyckade försök att [logga in](../getting-started/admin-signin.md) till administratören. Alla användarkonton som är låsta visas i rutnätet Låsta användare. Ett konto kan låsas upp av andra användare med fullständig administratörsbehörighet.

Ytterligare lösenordssäkerhetsåtgärder kan implementeras i [Avancerad administratör](../configuration-reference/advanced/admin.md#security) konfiguration. Se [Administratörssäkerhet](security-admin.md).

![Varning på inloggningsskärmen - kontot är tillfälligt inaktiverat](./assets/admin-login-locked-out-message.png){width="300"}

**_Så här låser du upp ett administratörskonto:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL Locked Users]**.

1. Markera kryssrutan för det låsta kontot i rutnätet.

   ![Behörigheter - låsta användarkonton](./assets/permissions-locked-users-grid.png){width="600" zoomable="yes"}

1. I det övre vänstra hörnet anger du **[!UICONTROL Actions]** till `Unlock`.

1. Klicka **[!UICONTROL Submit]** för att låsa upp kontot.
