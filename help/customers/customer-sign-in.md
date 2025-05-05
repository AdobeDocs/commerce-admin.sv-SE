---
title: Kundinloggning
description: Funktionen för kundinloggning i butiken gör det enkelt att få tillgång till kundens konton.
exl-id: eadcc15a-a052-4213-a818-d5b248d974d2
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Kundinloggning

Kunderna har enkelt tillgång till sina konton från alla sidor i din butik. Beroende på [konfigurationen](../customers/account-options-new.md) kan kunderna omdirigeras till sin kontokontrollpanel eller fortsätta handla efter att de har loggat in på sina konton.

Om [CAPTCHA](../systems/security-captcha.md) är aktiverad i konfigurationen måste personen slutföra ett test som verifierar att de är mänskliga innan han eller hon får åtkomst till sina konton.

När kunderna glömmer sina lösenord skickas en återställningslänk till den e-postadress som är kopplad till kontot. Konfigurationen [Lösenordsalternativ](../customers/password-options.md) styr kundupplevelsen för inloggningsförsök:

- Antalet gånger som en kund kan försöka ange ett lösenord
- Antalet minuter mellan försök
- Antal försök innan kontot låses
- Längden på utelåsningen

![Inloggningslänk i butiksrubriken](assets/storefront-sign-in-create-account.png){width="700" zoomable="yes"}

## Logga in på ett kundkonto

1. I butikens huvud klickar kunden på **[!UICONTROL Sign in]**.

   ![Kundinloggning](assets/login.png){width="700" zoomable="yes"}

1. Ange deras **[!UICONTROL Email]**-adress och **[!UICONTROL Password]**.

1. Klicka på **[!UICONTROL Sign in]**.

   >[!IMPORTANT]
   >
   >Om de inte kommer ihåg sitt lösenord kan kunden klicka på **[!UICONTROL Forgot Your Password?]** och följa [instruktionerna](../customers/password-reset.md) för att återställa lösenordet.

## Ange omdirigering till kontokontrollpanelen efter kundinloggning

Du kan konfigurera butiken så att kunderna dirigeras om till sin kontouppsättning när de har loggat in eller låta dem fortsätta handla.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Customers]** i den vänstra panelen och välj **[!UICONTROL Customer Configuration]**.

1. Expandera avsnittet **[!UICONTROL Login Options]**.

1. Ange **[!UICONTROL Redirect Customer to Account Dashboard after Logging in]** till något av följande:

   - `Yes` - Kontoinstrumentpanelen visas när kunderna loggar in på sina konton.
   - `No` - Kunder kan fortsätta att handla efter att ha loggat in på sina konton.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Logga in med Amazon

För butiker med en konfigurerad [!DNL Amazon Pay]- och [!DNL Login with Amazon]-integrering kan kunderna logga in på sina Amazon-köparkonton.

1. I butikens huvud klickar kunden på **[!UICONTROL Sign in]**.

1. Klicka på **[!UICONTROL Login with Amazon]**.

   ![Logga in med Amazon](assets/amazon-pay.png){width="700" zoomable="yes"}

1. När kunden uppmanas att logga in anger han/hon **[!UICONTROL email address]** och **[!UICONTROL password]** för sitt Amazon-köpkonto.

   ![Ange Amazon-autentiseringsuppgifter](assets/amazon-popup1.png){width="700" zoomable="yes"}

1. Klicka på **OK** om du vill ge Amazon behörighet att dela följande information från sitt konto med butiken när du bearbetar köp.

   - Namn
   - E-postadress
   - Leveransadresser

   ![Bevilja behörighet att dela data](assets/amazon-popup2.png){width="700" zoomable="yes"}

## Logga ut från ett kundkonto

1. I det övre högra hörnet bredvid _[!UICONTROL Welcome, Customer Name!]_&#x200B;klickar kunden på menyväljaren **[!UICONTROL v]**.

1. Välj **[!UICONTROL Sign Out]**.

Efter utloggningen omdirigeras kunden till hemsidan.
