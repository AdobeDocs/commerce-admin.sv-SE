---
title: Konfigurera Commerce Admin-integrering med ID
description: Följ den här valfria proceduren för att integrera inloggningar för användarkonton i Adobe Commerce Admin med Adobe ID.
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
source-git-commit: 0c79449ca05056d7a14242bbc859cb1bd4dc526e
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---

# Konfigurera Commerce Admin-integrering med Adobe ID

{{ee-feature}}

Integreringen stöder handlare med administratörsanvändare som har Adobe ID och som vill effektivisera inloggningen på Adobe Commerce och Adobe Business-produkter. Den är valfri och aktiveras per instans. Endast arbetsflöden för administratörer påverkas när de är aktiverade. 

>[!IMPORTANT]
>
>Administratörsanvändare bör spara sina inloggningsuppgifter för Commerce Admin (användarnamn och lösenord) och 2FA-autentiseringsuppgifter innan integreringen aktiveras. Dessa autentiseringsuppgifter krävs om IMS-integreringen är inaktiverad.

## Förutsättningar

* Adobe Commerce 2.4.5 eller senare
* Ett Adobe.com med åtkomst till [Adobe Admin Console](https://adminconsole.adobe.com/).

Administratören som konfigurerar den här integreringen behöver följande autentiseringsuppgifter när modulen aktiveras:

* Organisations-ID (hämtas från [Adobe Admin Console](https://adminconsole.adobe.com/)), som måste innehålla minst 24 tecken. Den autentiserade användaren måste tillhöra den här IMS-organisationen. Mer information om hur du hittar ditt organisations-ID finns i [Organisationer i Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).
* 2FA ska tillämpas på organisationsnivå i Adobe Admin Console för att aktivera modulen. Kontrollera [Autentiseringsinställningar](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification).
* Klient-ID
* Klienthemlighet
* Klient-ID och klienthemlighet är tillgängliga efter att API-nycklar har hämtats från [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/credentials/).

Commerce Admin-användare måste skapa ett konto hos en Adobe ID för att kunna logga in.

## Allmänna steg

* Hämta Adobe Org-ID från [Adobe Admin Console](https://adminconsole.adobe.com/)
* Generera ett nytt projekt, IMS API-nycklar och hemlighet från [Adobe Developer Console](https://developer.adobe.com/)
* Konfigurera Adobe Commerce-användare i Adobe Admin Console
* Aktivera `AdminAdobeIms` -modul.

För en lyckad integrering krävs att alla Adobe Commerce-användare har administratörskonton med samma namn och primära e-postadress. Om det inte finns något matchande administratörskonto måste en användare med nödvändig behörighet (vanligtvis tilldelad administratörsrollen) manuellt [skapa administratörens användarkonto](../systems/permissions-users-all.md#create-a-user) med samma namn och e-postadress.

## Konfigurera integreringen

När följande steg är slutförda av en administratör eller utvecklare med systemåtkomst kan _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_-knappen visas på inloggningssidan för Commerce Admin för alla Admin-användare.

### Steg 1: Hämta Adobe Org ID

Det krävs medlemskap i minst en IMS-organisation för att den här funktionen ska kunna aktiveras. Om du har en Adobe ID-organisation tillhör du som standard minst en Adobe-organisation. Logga in på [Adobe Admin Console](https://adminconsole.adobe.com/) för att hämta ditt organisations-ID.

### Steg 2: Generera ett nytt projekt, IMS API-nycklar och hemlig

Om du vill skapa projekt för en organisation måste Adobe Admin-kontot för organisationen ha systemadministratörs- eller utvecklarrollen. Se [Developer Console Guide](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. Logga in på [Adobe Developer Console](https://developer.adobe.com/).
1. Gå till **[!UICONTROL Projects]** tab (adobe.io/projects) och click **[!UICONTROL Create a new project]**.
1. Klicka **[!UICONTROL Add API]** på den nyligen skapade projektsidan.
1. Välj **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**.
1. Välj **[!UICONTROL Oauth 2.0 Web]**.
1. Ange **[!UICONTROL Redirect URI]**: `https://<hostname>/`
1. Ange **[!UICONTROL Redirect URI pattern]**: `https://<hostname>/.*`

   Undvik alla punkter i värdnamnet genom att föregå punkterna med `\\`. Om du lägger till ett jokertecken i slutet av URL:en stöds hemlig nyckel för Adobe Commerce Admin.

1. Klicka på **[!UICONTROL Save configured API]**.
1. Kopiera [!UICONTROL Client ID] och [!UICONTROL Client Secret] nycklar från det skapade projektet.

### Steg 3: Konfigurera Adobe Commerce-användare i Adobe Admin Console

Innan du aktiverar integreringen bör du kontrollera att alla Adobe Commerce Admin-användarkonton har ett motsvarande Adobe IMS-konto. Adobe Commerce-användare måste tillhöra en viss Adobe-organisation för att kunna logga in med en Adobe ID.

>[!TIP]
>
>Du kan skapa flera användarkonton genom att överföra användarinformationen från en CSV-fil. Se [Hantera flera användare](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html).

1. I [Adobe Admin Console](https://helpx.adobe.com/se/enterprise/using/admin-console.html), navigera till **[!UICONTROL Users]**  > **[!UICONTROL Users]**.

1. Klicka på **[!UICONTROL Add User]**.

1. Ange användarens e-postadress.

   Om det är tillämpligt fylls den rekommenderade ID-typen i automatiskt. Du kan ändra den här inställningen till ett produkt-ID i listan, som baseras på din organisations inköpsplan.

   Du kan lägga till upp till tio användare samtidigt. Om du vill lägga till fler upprepar du de föregående stegen när du har sparat ändringarna.

1. Klicka på **[!UICONTROL Save]**.

Användaren läggs till och visas i [!UICONTROL Users] lista.

### Steg 4: Aktivera AdminAdobeIms-modulen

The `AdminAdobeIms` -modulen ansvarar för integreringen av Adobe Commerce/Adobe IMS. När du har konfigurerat det nya projektet och kopierat ditt företags-ID, klient-ID och klienthemlighet kan du aktivera `AdminAdobeIms` -modul.

Retur `bin/magento admin:adobe-ims:enable`. Du uppmanas att ange följande parametrar. Använd de värden som genererades när projektet skapades.

* Organisations-ID
* Klient-ID
* Klienthemlighet
* 2FA aktiverat

Adobe Commerce visar ett meddelande som anger om aktiveringen lyckades eller misslyckades.

När du har aktiverat den här funktionen kan du överföra andra Adobe Commerce-användarkonton till Adobe IMS-konton. Adobe Commerce-användare måste tillhöra den konfigurerade Adobe-organisationen för att kunna logga in med en Adobe ID.
