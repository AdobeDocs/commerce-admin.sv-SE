---
title: Hantera administratörsanvändarkonton
description: Lär dig hur du skapar administratörskonton och tilldelar roller för att ge administratörsfunktioner behörigheter.
exl-id: 65cca7a8-3d44-4c8c-a758-c0de03d53e11
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
source-git-commit: ad75c77ada34c4d66b1a58a666edadd44d054e17
workflow-type: tm+mt
source-wordcount: '1012'
ht-degree: 0%

---

# Hantera administratörsanvändarkonton

När din butik installeras första gången skapas ett administratörskonto med inloggningsuppgifter som ger dig fullständig administrativ åtkomst. Det är en god vana att skapa ett annat användarkonto med fullständig administratörsåtkomst. På så sätt kan du använda ett konto för dina dagliga administrativa aktiviteter och reservera det andra som ett superadministratörskonto. Detta kan vara praktiskt om du glömmer dina vanliga inloggningsuppgifter eller om de på något sätt blir oanvändbara.

Om andra teammedlemmar eller tjänsteleverantörer behöver åtkomst kan du skapa enskilda användarkonton för dem och tilldela begränsad åtkomst baserat på deras specifika affärsbehov. Om du vill begränsa vilka webbplatser eller arkiv som användare kan få åtkomst till i Admin måste du först [skapa en roll](permissions-user-roles.md) med begränsad omfattning och endast de resurser som krävs är valda. Sedan kan du tilldela rollen till ett specifikt användarkonto. Administratörsanvändare som har tilldelats en begränsad roll kan endast visa och ändra data för webbplatser eller butiker som är associerade med rollen, men kan inte ändra några globala inställningar eller data.

>[!NOTE]
>
>Adobe Commerce-handlare som har en Adobe ID och vill ha en smidig inloggning på Adobe Commerce- och Adobe Business-produkter kan integrera Commerce-autentisering med Adobe IMS-autentiseringsarbetsflödet. När integreringen har aktiverats för din Commerce Store måste varje Admin-användare använda sina Adobe-inloggningsuppgifter - inte Commerce-inloggningsuppgifter - för att logga in. Se [Integreringsöversikt för Adobe Identity Management-tjänst (IMS)](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html?lang=sv-SE).

För användare och roller som är tillfälliga kan du även ange ett förfallodatum för användarkontot.

<!--  update this to a better info-graphic ![User types for your Admin](./assets/merchant-admin-users.png) -->

## Skapa en användare

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add New User]** i det övre högra hörnet.

   Om du vill redigera en befintlig användare klickar du på ett användarnamn i rutnätet. Du kan ändra avsnitten _[!UICONTROL User Info]_&#x200B;och&#x200B;_[!UICONTROL User Role]_ efter behov.

1. Gör följande i avsnittet _[!UICONTROL Account Information]_:

   ![Information om användarkonto](./assets/permissions-user-new.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL User Name]** för kontot.

     Användarnamnet ska vara lätt att komma ihåg. Den är inte skiftlägeskänslig. Om användarnamnet till exempel är `John` kan de även logga in som `john`.

   - Fyll i följande information:

      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**
      - **[!UICONTROL Email address]**

     Varje användarkonto måste ha en unik e-postadress.

   - Ange en **[!UICONTROL Password]** för kontot.

     >[!NOTE]
     >
     >Ett administratörslösenord måste innehålla minst sju tecken och innehålla både bokstäver och siffror. Fler lösenordsalternativ finns i [Konfigurera administratörsskydd](security-admin.md).

   - Ange lösenordet igen för **[!UICONTROL Password Confirmation]** för att kontrollera att det angavs korrekt.

   - Om din butik har flera språk anger du **[!UICONTROL Interface Locale]** till det språk som ska användas för administratörsgränssnittet.

1. Ange **[!UICONTROL This Account is]** till `Active`.

1. Klicka på kalenderikonen för att ange **[!UICONTROL Expiration Date]** för användarkontot.

   Det är praktiskt att definiera ett förfallodatum när en användare eller roll är tillfällig. Efter förfallodatumet ändras användarkontots status till `Inactive` och kan uppdateras vid behov.

1. Ange ditt lösenord för användarkontot under _[!UICONTROL Current User Identity Verification]_.

>[!IMPORTANT]
>
>När avsnittet _[!UICONTROL Account Information]_&#x200B;är klart kan du spara användaren. Den nya användaren visas i rutnätet&#x200B;_[!UICONTROL Users]_, men användarnamnet kan inte logga in förrän en roll har tilldelats.

## Tilldela en användarroll

1. Klicka på **[!UICONTROL User Role]** i den vänstra panelen.

   I rutnätet visas alla befintliga användarroller. _[!UICONTROL Administrators]_&#x200B;är den enda tillgängliga rollen för en ny butik.

   ![Admin - lägg till ny användarroll](./assets/permissions-user-roles.png){width="600" zoomable="yes"}

1. Välj en användarroll i kolumnen _[!UICONTROL Assigned]_.

   Du kan [visa befintliga eller definiera ytterligare användarroller](permissions-user-roles.md). När en roll har definierats måste du redigera användarkontot för att tilldela den nya rollen.

## Verifiera eller återställa 2FA-leverantörer

1. Öppna administratörens användarkonto.

1. Klicka på **[!UICONTROL 2FA]** i den vänstra panelen.

   ![Admin - lägg till ny användarroll](./assets/permissions-user-2fa.png){width="600" zoomable="yes"}

1. Verifiera de 2FA-lösningar som är tillgängliga för _Admin_ -användare och råda alla användare att installera de lösningar de vill använda innan de loggar in.

   Autentisering med endast en 2FA-lösning krävs för att logga in på _administratören_.

1. Om användaren behöver installera om 2FA-lösningen kan du återställa den aktuella 2FA-konfigurationen.

   Detta kräver att användaren upprepar installationsprocessen innan han/hon kan logga in igen. Användaren kan till exempel ha en ny smartphone och måste installera om Google Authenticator. Om du vill rensa användarens nuvarande 2FA-konfiguration klickar du på **[!UICONTROL Reset (Provider)]** för varje lösning som du vill rensa. Klicka på **[!UICONTROL OK]** när du uppmanas att bekräfta.

   Användaren får ett e-postmeddelande med en länk för att [konfigurera 2FA](security-two-factor-authentication.md). Länken kan bara användas en gång. Om användaren försöker logga in flera gånger skickas en ny länk efter varje försök.

1. Klicka på **[!UICONTROL Save User]**.

1. Ange ditt lösenord för att bekräfta din identitet när du uppmanas till detta och klicka sedan på **[!UICONTROL Save User]** igen.

   Rutnätet _[!UICONTROL Users]_&#x200B;öppnas och alla användare visas.

## Ta bort en administratörsanvändare

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**&#x200B;på sidofältet_ Admin _.

1. Leta upp användarkontot med hjälp av filter ovanför rutnätet och klicka på användarnamnet.

1. Ange ditt lösenord för att bekräfta din identitet när du uppmanas till detta.

1. Klicka på **[!UICONTROL Delete User]** i det övre högra hörnet.

1. Bekräfta åtgärden genom att klicka på **[!UICONTROL OK]**.

## Glömt lösenord och återställ e-post

Konfigurationen av administratörens e-postmall avgör vilka e-postmeddelanden som skickas när användarna glömmer bort och återställer sina lösenord. Den här konfigurationen anger den butikskontakt som visas som meddelandets avsändare och hur länge länken för lösenordsåterställning är giltig.

**_Så här konfigurerar du administratörens e-postmallar:_**

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Setting]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Advanced]** på den vänstra panelen och välj **[!UICONTROL Admin]**.

1. Expandera ![expansionsväxlingen](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Admin User Emails]**.

   ![Avancerad konfiguration - Inställningar för e-postmall för administratör](../configuration-reference/advanced/assets/admin-admin-user-emails.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Forgot Password Email Template]** till mallen som skickas när en Admin-användare glömmer sina lösenord.

1. Ange **[!UICONTROL Forgot and Reset Email Sender]** till den butikskontakt som visas som meddelandets avsändare.

1. Ange **[!UICONTROL User Notification Template]** till den e-postmall som används som standard för administratörsmeddelanden.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Låsta användare

Av säkerhetsskäl låses användarkonton som standard efter sex misslyckade försök att [logga in](../getting-started/admin-signin.md) i administratören. Alla användarkonton som är låsta visas i rutnätet Låsta användare. Ett konto kan låsas upp av andra användare med fullständig administratörsbehörighet.

Ytterligare säkerhetsmätningar för lösenord kan implementeras i konfigurationen [Avancerad administratör](../configuration-reference/advanced/admin.md#security). Se [Administratörssäkerhet](security-admin.md).

![Varning på inloggningsskärmen - kontot är tillfälligt inaktiverat](./assets/admin-login-locked-out-message.png){width="300"}

**_Så här låser du upp ett administratörskonto:_**

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL Locked Users]**&#x200B;på sidofältet_ Admin _.

1. Markera kryssrutan för det låsta kontot i rutnätet.

   ![Behörigheter - låsta användarkonton](./assets/permissions-locked-users-grid.png){width="600" zoomable="yes"}

1. I det övre vänstra hörnet anger du **[!UICONTROL Actions]** till `Unlock`.

1. Klicka på **[!UICONTROL Submit]** för att låsa upp kontot.
