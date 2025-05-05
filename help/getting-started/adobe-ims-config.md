---
title: Konfigurera Commerce Admin-integrering med ID
description: Följ den här valfria proceduren för att integrera inloggningar för användarkonton i Adobe Commerce Admin med Adobe ID.
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---

# Konfigurera Commerce Admin Integration med Adobe ID

{{ee-feature}}

Integrationen stöder Commerce handlare med admin-användare som har en Adobe ID och som vill effektivisera inloggningen på Adobe Commerce- och Adobe Business-produkter. Den är valfri och aktiveras per instans. Endast arbetsflöden för administratörer påverkas när de är aktiverade. 

>[!IMPORTANT]
>
>Administratörsanvändare bör spara sina inloggningsuppgifter för Commerce Admin (användarnamn och lösenord) och 2FA-inloggningsuppgifter innan de aktiverar integreringen. Dessa autentiseringsuppgifter krävs om IMS-integreringen är inaktiverad.

## Förutsättningar

* Adobe Commerce 2.4.5 eller senare
* Ett Adobe.com med åtkomst till [Adobe Admin Console](https://adminconsole.adobe.com/).

Administratören som konfigurerar den här integreringen behöver följande autentiseringsuppgifter när modulen aktiveras:

* Organisations-ID (hämtas från [Adobe Admin Console](https://adminconsole.adobe.com/)), som måste innehålla minst 24 tecken. Den autentiserade användaren måste tillhöra den här IMS-organisationen. Mer information om hur du hittar ditt företags-ID finns i [Organisationer i Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=sv-SE).
* 2FA ska tillämpas på organisationsnivå i Adobe Admin Console för att aktivera modulen. Kontrollera [autentiseringsinställningar](https://helpx.adobe.com/se/enterprise/using/authentication-settings.html#two-step-verification).
* Klient-ID
* Klienthemlighet
* Klient-ID och klienthemlighet är tillgängliga efter hämtning av API-nycklar från [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/credentials/).

Commerce Admin-användare måste skapa ett konto hos en Adobe ID för att kunna logga in.

## Allmänna steg

* Hämta Adobe Org ID från [Adobe Admin Console](https://adminconsole.adobe.com/)
* Generera ett nytt projekt, IMS API-nycklar och hemlighet från [Adobe Developer Console](https://developer.adobe.com/)
* Konfigurera Adobe Commerce-användare i Adobe Admin Console
* Aktivera modulen `AdminAdobeIms`.

För en lyckad integrering krävs att alla Adobe Commerce-användare har administratörskonton med samma namn och primära e-postadress. Om det inte finns något matchande administratörskonto måste en användare med nödvändig behörighet (vanligtvis tilldelad administratörsrollen) manuellt [skapa administratörsanvändarkontot](../systems/permissions-users-all.md#create-a-user) med samma namn och e-postadress.

## Konfigurera integreringen

När följande steg har slutförts av en administratör eller utvecklare med systemåtkomst visas knappen _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_&#x200B;på inloggningssidan för Commerce Admin för alla Admin-användare.

### Steg 1: Hämta Adobe Org ID

Det krävs medlemskap i minst en IMS-organisation för att den här funktionen ska kunna aktiveras. Om du har en Adobe ID tillhör du som standard minst en Adobe-organisation. Logga in på [Adobe Admin Console](https://adminconsole.adobe.com/) för att hämta ditt företags-ID.

### Steg 2: Generera ett nytt projekt, IMS API-nycklar och hemlig

Om du vill skapa projekt för en organisation måste organisationens Adobe Admin-konto ha rollen systemadministratör eller utvecklare. Se [Developer Console Guide](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. Logga in på [Adobe Developer Console](https://developer.adobe.com/).
1. Gå till fliken **[!UICONTROL Projects]** (adobe.io/projects) och klicka på **[!UICONTROL Create a new project]**.
1. Klicka på **[!UICONTROL Add API]** på den nyligen skapade projektsidan.
1. Välj **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**.
1. Välj **[!UICONTROL Oauth 2.0 Web]**.
1. Ange **[!UICONTROL Redirect URI]**: `https://<commerce_base_url>/`
1. Ange **[!UICONTROL Redirect URI pattern]**: `https://<commerce_base_url>/.*`

   Undvik alla punkter i värdnamnet genom att föregå punkterna med `\\`. Om du lägger till ett jokertecken i slutet av URL:en stöds hemlig nyckel för Adobe Commerce Admin.

1. Klicka på **[!UICONTROL Save configured API]**.
1. Kopiera nycklarna [!UICONTROL Client ID] och [!UICONTROL Client Secret] från det skapade projektet.

### Steg 3: Konfigurera Adobe Commerce-användare i Adobe Admin Console

Innan du aktiverar integreringen bör du kontrollera att alla Adobe Commerce Admin-användarkonton har ett motsvarande Adobe IMS-konto. Adobe Commerce-användare måste tillhöra en viss Adobe-organisation för att kunna logga in med en Adobe ID.

>[!TIP]
>
>Du kan skapa flera användarkonton genom att överföra användarinformationen från en CSV-fil. Se [Hantera flera användare](https://helpx.adobe.com/se/enterprise/using/bulk-upload-users.html).

1. Gå till **[!UICONTROL Users]** > **[!UICONTROL Users]** i [Adobe Admin Console](https://helpx.adobe.com/se/enterprise/using/admin-console.html).

1. Klicka på **[!UICONTROL Add User]**.

1. Ange användarens e-postadress.

   Om det är tillämpligt fylls den rekommenderade ID-typen i automatiskt. Du kan ändra den här inställningen till ett produkt-ID i listan, som baseras på din organisations inköpsplan.

   Du kan lägga till upp till tio användare samtidigt. Om du vill lägga till fler upprepar du de föregående stegen när du har sparat ändringarna.

1. Klicka på **[!UICONTROL Save]**.

Användaren läggs till och visas i listan [!UICONTROL Users].

### Steg 4: Aktivera AdminAdobeIms-modulen

Modulen `AdminAdobeIms` ansvarar för integreringen av Adobe Commerce/Adobe IMS. När du har konfigurerat det nya projektet och kopierat ditt organisations-ID, klient-ID och klienthemlighet kan du aktivera modulen `AdminAdobeIms`.

Ange `bin/magento admin:adobe-ims:enable`. Du uppmanas att ange följande parametrar. Använd de värden som genererades när projektet skapades.

* Organisations-ID
* Klient-ID
* Klienthemlighet
* 2FA aktiverat

Adobe Commerce visar ett meddelande som anger om aktiveringen lyckades eller misslyckades.

När du har aktiverat den här funktionen kan du överföra andra Adobe Commerce-användarkonton till Adobe IMS-konton. Adobe Commerce-användare måste tillhöra den konfigurerade Adobe-organisationen för att kunna logga in med en Adobe ID.
