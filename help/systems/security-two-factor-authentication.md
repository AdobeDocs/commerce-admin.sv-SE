---
title: Tvåfaktorautentisering (2FA)
description: Lär dig mer om stöd för tvåfaktorsautentisering för att säkerställa säkerheten i ditt system och dina data.
exl-id: d9eb3dd6-4a7b-411a-ac08-0441803cd59a
role: Admin
feature: Configuration, Security, User Account
source-git-commit: 4997c4c01f11d6e0355eb8e02f8f099db685b400
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 0%

---

# Tvåfaktorautentisering (2FA)

Commerce _Admin_ för din Adobe Commerce- eller Magento Open Source-installation ger åtkomst till din butik, dina beställningar och dina kunddata. För att förhindra obehörig åtkomst till dina data måste alla användare som försöker logga in på _Admin_ slutföra en autentiseringsprocess för att verifiera sin identitet.

>[!NOTE]
>
>Den här implementeringen av tvåfaktorsautentisering (2FA) gäller endast _Admin_ och är inte tillgänglig för kundkonton. Den tvåfaktorsautentisering som skyddar ditt Commerce-konto har en separat konfiguration. Gå till [Skydda ditt Commerce-konto](../getting-started/commerce-account-secure.md) om du vill veta mer.

Tvåfaktorsautentisering används ofta och det är vanligt att generera åtkomstkoder för olika webbplatser i samma app. Denna extra autentisering säkerställer att bara du kan logga in på ditt användarkonto. Om du tappar bort ditt lösenord eller om någon gissar det lägger tvåfaktorsautentisering till ett skyddslager. Du kan till exempel använda Google Authenticator för att generera koder för administratören av din butik, ditt Commerce-konto och Google-konto.

![Iphone för säkerhetskonfiguration - 2FA](./assets/google-authenticator-iphone.png){width="300"}

Adobe Commerce stöder 2FA-metoder från flera leverantörer. Vissa kräver installation av en app som genererar ett engångslösenord som användare anger vid inloggning för att verifiera sin identitet. U2F-enheter (Universal Second Factor) liknar nyckelfob och genererar en unik nyckel för att verifiera identitet. Andra enheter kontrollerar identiteten när de sätts in i en USB-port. Som butiksadministratör kan du behöva en eller flera av de tillgängliga 2FA-metoderna för att verifiera användaridentiteten. Din 2FA-konfiguration gäller för alla webbplatser och butiker som är kopplade till Adobe Commerce-installationen.

Första gången en användare loggar in på _Admin_ måste de ställa in varje [2FA](../configuration-reference/security/2fa.md) -metod som du behöver och verifiera sin identitet med den associerade appen eller enheten. Efter den första konfigurationen måste användaren autentisera med en av de konfigurerade metoderna varje gång han/hon loggar in. Varje användares 2FA-information registreras i användarens _Admin_-konto och kan vid behov [återställas](security-two-factor-authentication-manage.md). Om du vill veta mer om inloggningsprocessen går du till [_Admin_ Logga in](../getting-started/admin-signin.md).

>[!NOTE]
>
>Lager som har aktiverat autentisering med Adobe Identity Management Services (IMS) har inbyggt Adobe Commerce och Magento Open Source 2FA inaktiverat. Administratörsanvändare som är inloggade på sin Commerce-instans med sina Adobe-inloggningsuppgifter behöver inte autentisera igen för många administratörsuppgifter. Autentisering hanteras av Adobe IMS när administratörsanvändaren loggar in på sin aktuella session. Se [Integreringsöversikt för Adobe Identity Management-tjänst (IMS)](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

Du kan titta på den här [videodemonstrationen](https://video.tv.adobe.com/v/339104?quality=12&learn=on) om du vill se en översikt över tvåfaktorsautentisering i Admin.

## Konfigurera dina 2FA-leverantörer

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Security]** i den vänstra panelen och välj **[!UICONTROL 2FA]**.

1. I avsnittet _[!UICONTROL General]_väljer du de providers som ska användas.

   | Provider | Funktion |
   |--- |--- |
   | [!UICONTROL Google Authenticator] | Skapar ett engångslösenord i programmet för användarautentisering. |
   | [!UICONTROL Duo Security] | Tillhandahåller SMS och push-meddelanden. |
   | [!UICONTROL Authy] | Genererar en tidsberoende sexsiffrig kod och levererar SMS- eller Voice Call 2FA-skydd eller -token. |
   | [!UICONTROL U2F Devices (Yubikey and others)] | Använder en fysisk enhet för autentisering, till exempel [[!DNL YubiKey]](https://www.yubico.com/). |

   Om du vill välja flera metoder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje objekt.

1. Slutför [inställningarna](../configuration-reference/security/2fa.md) för varje nödvändig 2FA-metod.

   ![Säkerhetskonfiguration - 2FA](../configuration-reference/security/assets/2fa-general.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

   Första gången användare loggar in på _Admin_ måste de konfigurera varje 2FA-metod som krävs. Efter den första konfigurationen måste de autentisera med en av de konfigurerade metoderna varje gång de loggar in.

## 2FA-providerinställningar

Slutför inställningarna för varje 2FA-metod som du behöver.

### Google

Om du vill ändra hur länge engångslösenordet är tillgängligt under inloggningen avmarkerar du kryssrutan **[!UICONTROL Use system value]**. Ange sedan det antal sekunder som du vill att **[!UICONTROL OTP Window]** ska vara giltig.

![Säkerhetskonfiguration - Google](../configuration-reference/security/assets/2fa-google.png){width="600" zoomable="yes"}

>[!NOTE]
>
>I Adobe Commerce 2.4.7 och senare styr konfigurationsinställningen för fönstret för engångslösenord hur lång tid (i sekunder) som systemet accepterar en administratörs engångslösenord efter att det har gått ut. Värdet måste vara mindre än 30 sekunder. Systemets standardinställning är `29`.<br><br> I version 2.4.6 bestämmer fönsterinställningen för engångslösenord antalet tidigare och framtida koder för engångslösenord som förblir giltiga. Värdet `1` anger att den aktuella engångskoden plus en tidigare och en framtida kod förblir giltig vid en given tidpunkt.

### [!DNL Duo Security]

Ange följande autentiseringsuppgifter från ditt Duo-säkerhetskonto:

- Klient-ID
- Klienthemlighet
- Integrationsnyckel
- Hemlig nyckel
- API-värdnamn

![Säkerhetskonfiguration - Duo](../configuration-reference/security/assets/2fa-duo-security.png){width="600" zoomable="yes"}

### [!DNL Authy]

1. Ange API-nyckeln från ditt [!DNL Authy]-konto.

1. Om du vill ändra standardmeddelandet som visas under autentiseringen avmarkerar du kryssrutan **[!UICONTROL Use system value]**. Ange sedan **[!UICONTROL OneTouch Message]** som du vill ska visas.

   ![Säkerhetskonfiguration - autentisering](../configuration-reference/security/assets/2fa-authy.png){width="600" zoomable="yes"}

### U2F-enheter ([!DNL Yubikey] med flera)

Butiksdomänen används som standard under autentiseringsprocessen. Om du vill använda en anpassad domän för autentiseringsutmaningar avmarkerar du kryssrutan **[!UICONTROL Use system value]**. Ange sedan **[!UICONTROL WebAPi Challenge Domain]**.

![Säkerhetskonfiguration - U2F-enheter](../configuration-reference/security/assets/2fa-u2f-key.png){width="600" zoomable="yes"}
