---
title: Ditt administratörsanvändarkonto
description: Lär dig mer om ditt Admin-konto och hur du använder tvåfaktorsautentisering för att logga in på Admin.
exl-id: ad576533-5914-49d1-8e73-3f59c55543a5
feature: Admin Workspace, User Account
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 0%

---

# Ditt administratörskonto

Det primära administratörskontot konfigurerades ursprungligen under installationen och kan innehålla inledande platshållarinformation eller exempeldatainformation. Den angivna ägaren av kontot kan anpassa användarnamnet och lösenordet och uppdatera förnamnet, efternamnet och e-postadressen när som helst. Det här kontot, som är en _superanvändare_ med alla behörigheter som standard, skapar vanligtvis de administratörsanvändarkonton som behövs för företaget.

- Mer information om hur du lägger till eller redigerar användare finns i [Skapa en användare](../systems/permissions-users-all.md#create-a-user).

- Mer information om administratörer och användarroller finns i [Behörigheter](../systems/permissions.md) och [Användarroller](../systems/permissions-user-roles.md).

{{ims-admin-note}}

## Administratörsinloggning

[!DNL Commerce] _Admin_ skyddas av flera lager med säkerhetsåtgärder för att förhindra obehörig åtkomst till din butik, beställning och kunddata. Första gången du loggar in på _Admin_ måste du ange ditt användarnamn och lösenord och ställa in [tvåfaktorautentisering](../systems/security-two-factor-authentication.md) (2FA).

Beroende på hur din butik är konfigurerad kan det finnas en [CAPTCHA](../systems/security-google-recaptcha.md) -utmaning att lösa, som att ange en serie tangentbordstecken, lösa ett pussel eller klicka på en serie bilder med ett gemensamt tema. Dessa tester är utformade för att identifiera dig som människa, snarare än som en automatiserad robot.

För ytterligare säkerhet kan du avgöra vilka delar av _Admin_ som varje användare har [behörighet](../systems/permissions.md) att komma åt och även begränsa antalet [inloggningsförsök](../configuration-reference/advanced/admin.md). Som standard är kontot låst efter sex försök och användaren måste vänta några minuter innan han/hon försöker igen. [Låsta konton](../systems/permissions-users-all.md#locked-users) kan också återställas från _administratören_.

>[!NOTE]
>
>Första gången du loggar in på _Admin_ uppmanas du att _Tillåt insamling av administratörsanvändningsdata_. Mer information finns i [Insamling av användningsdata](admin.md#usage-data-collection).

![Administratörsinloggning](./assets/admin-login.png){width="400"}

### Steg 1: Konfigurera tvåfaktorsautentisering

Innan du kan logga in på _Admin_ i din butik måste du ha en autentiseringslösning med två faktorer konfigurerad och klar att använda. Mer information om autentiseringsprocessen som används av varje lösning finns i [Använda Tvåfaktorautentisering](../systems/security-two-factor-authentication-use.md). Som standard har [!DNL Commerce] stöd för [Google Authenticator](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&hl=en_US).

Fråga din [!DNL Commerce]-systemadministratör vilka 2FA-lösningar som stöds för butiken. Slutför sedan konfigurationen av den 2FA-lösning du föredrar enligt leverantörens instruktioner.

### Steg 2: Logga in på administratören

1. Ange den _Admin_-URL som angavs under installationen av [!DNL Commerce].

   _Admin_-standardwebbadressen ser ut ungefär som `https://www.yourdomain.com/your-custom-admin-domain`.

   >[!NOTE]
   >
   >Även om den här dokumentationen använder `admin` som bas-URL i de flesta exempel rekommenderar vi att du väljer en unik och svårgissad [anpassad URL](../stores-purchase/store-urls.md) för _Admin_ i din butik.

   Du kan lägga till ett bokmärke för sidan eller spara ett kortkommando på skrivbordet för enkel åtkomst.

1. Ange din _administratör_ **[!UICONTROL Username]** och **[!UICONTROL Password]**.

1. (Valfritt) Om en CAPTCHA är aktiverad för din butik följer du instruktionerna på skärmen för att lösa problemet.

   Mer information finns i [CAPTCHA](../systems/security-captcha.md) och [reCAPTCHA](../systems/security-google-recaptcha.md).

1. Klicka på **[!UICONTROL Sign in]**.

   Om det är första gången du loggar in på _Admin_ från kontot bör du få ett e-postmeddelande med en länk till konfigurationsinstruktionerna.

### Steg 3: Slutför 2FA-konfigurationen

I följande exempel visas hur du parar ditt _Admin_-konto med Google Authenticator.

1. När QR-koden visas kan du använda någon av följande metoder för att hämta koden och koppla Google Authenticator till ditt _Admin_-konto.

   ![Konfigurera Google Authenticator](./assets/admin-login-google-auth-setup.png){width="400"}

   - Hämta QR-kod med en smartphone

     Starta Google Authenticator på smarttelefonen. Tryck på _plustecknet_ (+) i appens övre högra hörn. Tryck sedan på **[!UICONTROL Scan Barcode]** längst ned på skärmen och ta en bild av QR-koden.

   - Hämta QR-kod från webbläsare

     Om Google Authenticator är installerat som ett tillägg i webbläsaren klickar du på ikonen **Autentiserare** i verktygsfältet och hämtar sidan.

   - Ange QR-kod manuellt

     Kopiera textsträngen nedanför QR-koden. Starta Google Authenticator med antingen din smartphone eller webbläsare och klicka på plustecknet (+). Välj sedan **[!UICONTROL Manual Entry]**. Under **[!UICONTROL Account]** anger du den e-postadress som är associerad med ditt _Admin_-konto och klistrar in QR-kodsträngen i fältet **[!UICONTROL Key]**.

1. Om du vill logga in på _Admin_ med tvåfaktorsautentisering anger du den sexsiffriga kod som genererats av Google Authenticator i fältet **[!UICONTROL Authenticator code]** och klickar sedan på **[!UICONTROL Confirm]**.

   ![Ange autentiseringskoden](./assets/admin-login-2fa-google.png){width="400"}

## Återställ lösenordet

Det är inte tillåtet att återanvända de fyra senaste lösenorden som tilldelats kontot.

1. Ange **[!UICONTROL Email Address]** som är associerad med _Admin_-kontot.

   ![Har du glömt lösenordet](./assets/admin-sign-in-forgot-password.png){width="400"}

1. Klicka på **[!UICONTROL Retrieve Password]**.

   Om ett konto är kopplat till e-postadressen skickas ett e-postmeddelande för att återställa lösenordet.

   >[!NOTE]
   >
   >Ett _Admin_-lösenord måste innehålla minst sju tecken och innehålla både bokstäver och siffror. Mer information om lösenordsalternativ finns i [Konfigurera _Admin_ Security](../systems/security-admin.md) .

## Logga ut från administratören

1. Klicka på ikonen _Konto_ (![Konto](../assets/icon-admin-user.png)) i det övre högra hörnet.

1. Klicka på **[!UICONTROL Sign Out]**.

   ![Logga ut](./assets/admin-sign-out.png){width="700" zoomable="yes"}

Sidan _[!UICONTROL Sign In]_&#x200B;visar ett meddelande om att du är utloggad. Logga ut från_ Admin _när du lämnar datorn obevakad.

## Redigera kontoinformation

1. Klicka på ikonen _Konto_ (![Konto](../assets/icon-admin-user.png)).

1. Klicka på **[!UICONTROL Account Setting]**.

   ![Kontoinformation](./assets/admin-account-information.png){width="700" zoomable="yes"}

1. Gör nödvändiga ändringar i din kontoinformation.

   Om du ändrar dina inloggningsuppgifter måste du lagra dem på en säker plats.

1. Ange ditt aktuella kontolösenord.

1. Klicka på **[!UICONTROL Save Account]**.

## Tillåt flera administratörsinloggningar

Administratören ger åtkomst till funktionerna för att hantera order, kunder, produkter, frakt och betalningar. Standardkonfigurationen är inställd på att inte tillåta flera inloggningar för ett administratörskonto som en god säkerhetsrutin. Du kan dock ändra den här inställningen så att administratörsanvändare kan logga in från flera enheter för att få plats med dina arbetsflöden.

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_&#x200B;Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Advanced]** i den vänstra navigeringspanelen och välj **[!UICONTROL Admin]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Security]**.

1. Välj **för** Admin Account Sharing`Yes`.

   ![Tillåt delning av administratörskonton](./assets/multiple-admin-login.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]**.

## Ange administratörens inloggningsnamn som skiftlägeskänsliga

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_&#x200B;Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Advanced]** i den vänstra navigeringspanelen och välj **[!UICONTROL Admin]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Security]**.

1. Ställ in fältet **[!UICONTROL Login is Case Sensitive]** på `Yes`.

1. Klicka på **[!UICONTROL Save Config]**.


## Upprätthåll säker åtkomst till administratören

För att försäkra dig om att din administratör är säker bör du regelbundet kontrollera användare och roller med administratörsåtkomst.

Överväg också att [uppdatera Admin Base URL-konfigurationen](https://experienceleague.adobe.com/en/docs/commerce-admin/config/advanced/admin#admin-base-url) om du vill ändra standardslutpunkten `/admin` till en anpassad sökväg. Att konfigurera en anpassad sökväg ger följande säkerhetsfördelar:

**Förbättrat skydd**: Standardsökvägen för admin är allmänt känd och är ofta riktad till illasinnade aktörer som försöker attackera med styrkan. Genom att ändra det till ett unikt, anpassat värde minskar du avsevärt risken för obehöriga åtkomstförsök.

**Reducerad sårbarhet**: Automatiserade botar söker ofta efter vanliga sökvägar som &quot;admin&quot; för att utnyttja sårbarheter. En anpassad sökväg gör det svårare för dessa robotar att hitta din administratörsinloggningssida, vilket minskar risken för attacker.

**Förbättrad sekretess**: En anpassad administratörssökväg lägger till ett extra lager av osäkerhet, vilket gör det svårare för potentiella angripare att identifiera och rikta in sig på din administratörsinloggningssida.

**Efterlevnad av bästa praxis**: Följande bästa säkerhetspraxis, till exempel att anpassa din administratörssökväg, visar en proaktiv metod för att skydda din e-handelsplats och dina kunddata.

>[!NOTE]
>
>Om det finns misstanke om en överträdelse ska du ta bort alla okända administratörsanvändare och återställa alla administratörslösenord. Mer information finns i [säkerhetsplanen](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security).
