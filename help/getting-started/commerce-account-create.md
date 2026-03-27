---
title: Skapa och få åtkomst till ditt [!DNL Commerce] konto
description: Lär dig mer om  [!DNL Commerce] konton, som hanterar de produkter och tjänster som du har köpt.
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
exl-id: 45f938c8-9bd9-4bd3-ac12-cce722a61e03
feature: User Account
source-git-commit: 96acaff3e614a5758fdc51bc5de70ce0507a970a
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 0%

---


# Åtkomst till ditt [!DNL Commerce]-konto

Ett [!DNL Commerce]-konto är din centrala åtkomstpunkt för hantering av Adobe Commerce-tjänster för Adobe Commerce-projekt som distribueras i molninfrastruktur eller lokalt. På kontokontrollpanelen kan du visa prenumerationer, hantera API-nycklar för Commerce Services, granska tidigare faktureringsinformation och samarbeta med andra användare i organisationen.

Om du behöver [skicka in din första biljett](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) eller hantera din Adobe Commerce-relation, i stället för att arbeta i en viss butik, börjar du med att skapa eller komma åt ditt [!DNL Commerce]-konto.

Du kan komma åt ditt [!DNL Commerce]-konto från webbplatsen [!DNL Commerce]. På kontokontrollpanelen kan du visa information om de produkter och tjänster du har köpt och tillhandahålla [delad åtkomst](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-help-center-user-guide#provide-shared-access) till andra användare. Viss information, t.ex. API-nycklar för Commerce Services, visas endast för licensägare.

>[!NOTE]
>
>Avsnittet **[!UICONTROL Billing History]** på kontosidan [!DNL Commerce] visar endast fakturor som skapats före uppdateringen av faktureringssystemet.
>
>Om nyare fakturor inte finns med i listan har de överförts till det nya systemet och är inte tillgängliga från den här sidan.

![Ditt [!DNL Commerce]-konto](./assets/home-acct.png){width="700"}

Inloggningen för ditt [!DNL Commerce]-konto är skild från inloggningen för din administratör för butik. Du använder vanligtvis olika autentiseringsuppgifter för varje, och åtkomsten till varje system hanteras separat.

En användare som vill effektivisera sin inloggning på Adobe Commerce och Adobe Business-produkter kan dock konfigurera sin Adobe ID att logga in på butiksadministratören: [Konfigurera Commerce Admin Integration med Adobe ID](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-config) i *IMS Integration Guide for Commerce*.

>[!NOTE]
>
>När du har skapat ditt konto rekommenderar vi att du använder Tvåfaktorautentisering (TFA) för att [skydda ditt konto](commerce-account-secure.md).

## Logga in på ditt [!DNL Commerce]-konto

Du måste ha en Adobe ID för att få tillgång till ditt [!DNL Commerce]-konto. Om du har ett befintligt [!DNL Commerce]-konto men inte har loggat in sedan augusti 2022 måste du skapa en Adobe ID under inloggningsprocessen. Du måste slutföra det här steget innan du kan logga in på ditt konto.

>[!WARNING]
>
>Om du inte hittar Commerce-organisationen när du skickar in ett [supportärende](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-help-center-user-guide#support-case) från Adobe Commerce betyder det vanligtvis något av följande: Kontoägaren har inte skapat någon Adobe ID, eller så finns en Adobe ID men är inte länkad till Commerce-kontot.

1. Gå till webbplatsen [[!DNL Commerce]](https://account.magento.com/customer/account/login/).

1. Klicka på **[!UICONTROL Sign in with Adobe ID]**.

   ![Logga in med inloggningsskärmen för Adobe](./assets/sign-in-with-adobe.png){width="700"}

1. Ange din e-postadress och klicka på **[!UICONTROL Continue]**.

   >[!TIP]
   >
   >Om du använde en e-postadress som är kopplad till ett befintligt Commerce-konto-MAGEID, länkar inloggningsprocessen automatiskt till din Adobe ID.

## Skapa ett [!DNL Commerce]-konto

Alla kan skapa ett kostnadsfritt [!DNL Commerce]-konto. Den e-postadress du använder kan bara kopplas till ett Commerce-konto.

>[!NOTE]
>
>Använd en Adobe ID för att skapa och få tillgång till ett Commerce-konto.
>- Om du inte har något Commerce-konto kan du skapa ett under registreringsprocessen.
>- Om du redan har ett Commerce-konto men inte har någon Adobe ID kan du läsa [logga in på ett Commerce-konto](#log-in-to-your-dnl-commerce-account).

1. Gå till [[!DNL Commerce] platsen](https://account.magento.com/customer/account/login/).

1. Klicka på **[!UICONTROL Sign in with Adobe ID]**.

1. Klicka **[!UICONTROL Create an account]** om du inte har någon Adobe ID. Annars går du vidare till steg 7.

   ![Skapa en kontolänk](./assets/account-create-link.png){width="700"}

1. Fyll i anmälningsformuläret.

   ![Kontoinformation](./assets/account-create.png){width="700"}

1. Klicka på **[!UICONTROL Create account]**.

1. Ange den verifieringskod som skickas till din e-postadress.

   ![Ange verifieringskod](./assets/verification-code.png){width="700"}

1. När din Adobe ID har skapats och verifierats går du tillbaka till https://account.magento.com/. Ett MAGE-ID genereras och länkas automatiskt till din Adobe ID.

## Återställ lösenordet

1. Gå till [[!DNL Commerce] platsen](https://account.magento.com/customer/account/login/).

1. Klicka på **[!UICONTROL Sign in with Adobe ID]**.

1. Klicka på **[!UICONTROL Get help signing in]**.

   ![Få hjälp med att logga in](./assets/sign-in-get-help.png){width="700"}

1. Klicka på **[!UICONTROL Reset your password]**.

   ![Ändra ditt lösenord](./assets/change-password.png){width="700"}

1. Ange din e-postadress.

1. Klicka på **[!UICONTROL Continue]**.

## Ger delad åtkomst till ditt Commerce-konto

Med delad åtkomst kan du ge betrodda användare - t.ex. kollegor, partners och administratörer - behörighet att hantera din Adobe Commerce-relation åt dig utan att använda din personliga inloggning. Detta inkluderar att andra kan öppna och spåra supportärenden.

I avsnittet [Dela ett Commerce-konto](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-share?lang=en) i Adobe Commerce Starthandbok finns mer information om hur du konfigurerar ett delat konto.

Detaljerade instruktioner om hur du skickar in ett supportärende från Commerce finns i [användarhandboken för Adobe Commerce Help Center](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-help-center-user-guide#support-case).

## Sammanfattning

| Scenario | Vad händer? | Så här gör du med Adobe ID | Vad du ska göra för MAGE ID/Commerce-konto | Resultat |
| --- | --- | --- | --- | --- |
| Nyheter i Adobe och Commerce | Ingen Adobe ID, inget MAGE-ID | Skapa en Adobe ID när du uppmanas att göra det under inloggning på https://account.magento.com | När Adobe ID har skapats loggar du in igen på https://account.magento.com | Ett Commerce-konto skapas och ett MAGE-ID skapas och länkas till Adobe ID |
| Har Adobe ID, men ännu inget MAGE-ID | Använder endast andra Adobe-produkter | Logga in med Adobe ID på https://account.magento.com | Första lyckade inloggningen skapar Commerce-kontot och MAGE-ID:t | MAGE ID skapas och länkas automatiskt |
| Äldre Commerce-kund med gammalt MAGE-ID | Har ett historiskt MAGE-ID, men inte Adobe ID | Skapa en Adobe ID på https://account.adobe.com med samma e-postadress som det befintliga MAGE-ID:t | Logga in på https://account.magento.com med&quot;Logga in med Adobe ID&quot; | Befintligt MAGE-ID är länkat till nya Adobe ID |
| Adobe ID och MAGE ID finns men är inte länkade | E-post för Adobe ID och Commerce skiljer sig åt | Justera e-postmeddelandet från Adobe ID så att det matchar e-postadressen för Commerce-kontot (eller vice versa, beroende på ägarskap) | När e-postmeddelandena matchar loggar du in via&quot;Logga in med Adobe ID&quot; på https://account.magento.com | Adobe ID blir inloggningsnamn; MAGE-ID:t är fortfarande berättigandeidentifieraren |
| Har Adobe ID men inget MAGE-ID | Aldrig inloggad på https://account.magento.com | Använda befintlig Adobe ID | Logga in på https://account.magento.com för första gången | Den första inloggningen genererar och länkar ett MAGE-ID |
| Använder endast inloggning för molnprojekt (accounts.magento.cloud) | Kan komma åt molnprojekt men inte klassiskt Commerce-konto | Fortsätt använda Adobe ID för molnprojekt | Om Marketplace/licensvillkoren behövs kan du även logga in på https://account.magento.com med samma Adobe ID | Ett klassiskt Commerce-konto (med MAGE-ID) skapas och länkas |

Om en användare anser att de bör ha Commerce-berättiganden men inte ser ett MAGE-ID är nästa steg att logga in på https://account.magento.com med hjälp av sin Adobe ID så att ett Commerce-konto och ett MAGE-ID kan skapas eller länkas på rätt sätt.
