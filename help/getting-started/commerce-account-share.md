---
title: Dela ett [!DNL Commerce] konto
description: Lär dig hur du ger begränsad åtkomst till ditt [!DNL Commerce] konto för andra [!DNL Commerce] kontoinnehavare.
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
source-git-commit: e7d76a7fa9ba8d8b8ee1ce122f7ca61e2aa317c6
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 0%

---

# Dela ett [!DNL Commerce]-konto

Ditt [!DNL Commerce]-konto innehåller information som du kan göra tillgänglig för betrodda medarbetare och tjänsteleverantörer som hjälper till att hantera din webbplats. Som primär kontoinnehavare har du behörighet att bevilja begränsad åtkomst till andra [!DNL Commerce]-kontoinnehavare. Delad åtkomst kan återkallas, men kan inte överföras från en användare till en annan.

[!DNL Commerce]-supportteamet har inte åtkomst till kontot och kan inte konfigurera delad åtkomst för dig. Det är bara den primära kontoinnehavaren med rätt behörigheter som kan konfigurera delad åtkomst. När du delar kontoåtkomst förblir all känslig information, som faktureringshistorik eller kreditkortsinformation, skyddad och är aldrig tillgänglig för andra användare.

>[!NOTE]
>
>Den primära kontoinnehavaren ansvarar själv för alla åtgärder som vidtas av användare med delad åtkomst. Adobe ansvarar inte för några åtgärder som vidtas av användare som har delad åtkomst till ditt konto.

![Inställningar för delad åtkomst](./assets/shared-access.png){width="600" zoomable="yes"}

## Konfigurera ett delat konto

1. Innan du börjar får du följande information från [!DNL Commerce]-kontot för den **nya delade åtkomstbehörigheten**:

   - Användaren måste ha registrerat sig för ett konto på account.adobe.com och loggas in via account.magento.com. Mer information finns i [Skapa ett Commerce-konto](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create#create-a-commerce-account).
   - `MAGE ID/Account ID (MAG00XXXXXXX)` visas i det övre vänstra hörnet på fliken _[!UICONTROL Magento]_, precis ovanför länken **Logga ut**.
   - Den `Email`-adress som är associerad med kontot.

1. Logga in på ditt [[!DNL Commerce] konto](commerce-account-create.md).

1. Klicka på **[!UICONTROL Shared Access]** i den vänstra navigeringspanelen.

1. Klicka på **[!UICONTROL Add New User]**.

   ![Lägg till en ny användare](./assets/shared-access-add.png){width="600" zoomable="yes"}

1. Gör följande under [!UICONTROL _New User Information]_:

   - Ange **[!UICONTROL Account ID]** från den nya användarens [!DNL Commerce]-konto.
   - Ange den **[!UICONTROL Email]**-adress som är associerad med den nya användarens [!DNL Commerce]-konto.

   ![Ny användarinformation](./assets/shared-new-user.png){width="600"}

1. Gör följande under _[!UICONTROL Shared Information]_:

   - Om du vill identifiera det delade kontot anger du **[!UICONTROL Share Name]**. Det här namnet används som intern referens och är bara synligt för dig och den person som du delar ditt konto med.

     Ett tips är att använda ditt organisationsnamn som [!UICONTROL Share Name]. Använd inte ett namn som börjar med `CLOUD SHARED ACCESS FROM MAG XYX`.
   - Om du vill dela din personliga kontaktinformation med den nya användaren anger du **[!UICONTROL Your Email]** och **[!UICONTROL Your Phone]**.

1. Under _[!UICONTROL Grant Account Permissions]_markerar du kryssrutan för varje [!DNL Commerce]-produkt och tjänst som du vill dela.

   ![Bevilja kontobehörigheterna](./assets/shared-permissions.png){width="600"}

1. Klicka på **[!UICONTROL Create Shared Access]**.

   Den nya användarinformationen visas i avsnittet _[!UICONTROL Manage Permissions]_på sidan Delad åtkomst och en e-postinbjudan med instruktioner om hur du får åtkomst till det delade kontot skickas till den nya användaren.

   ![Hantera behörigheter för delad åtkomst](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Det är inte nödvändigt att dela åtkomst till _[!UICONTROL Security Tool]_- Alla användare med ett MAGE ID kan konfigurera verktyget för säkerhetsgenomsökning med ett eget konto. De behöver bara de nödvändiga behörigheterna för att göra ändringar på webbplatsen och för att verifiera domänens ägarskap med någon av de [obligatoriska metoderna](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-scan)).

## Åtkomst till ett delat konto

Följande instruktioner är skrivna ur ett delat användarperspektiv som tar emot en inbjudan till ett delat konto.

1. När du får en inbjudan till ett delat konto följer du instruktionerna i e-postmeddelandet för att logga in på ditt eget [!DNL Commerce]-konto.

   Den vänstra navigeringspanelen för ditt konto har en ny _[!UICONTROL Shared with me]_-flik. Kontrollen_[!UICONTROL Switch Accounts]_ i det övre högra hörnet har alternativ för `My Account` och namnet på det delade kontot.

   ![Delad med mig](./assets/shared-with-me.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >   Om du inte ser kontrollen _[!UICONTROL Switch Accounts]_kontaktar du den primära kontoinnehavaren och bekräftar att de har angett rätt [kontoinformation](#set-up-a-shared-account).


1. Om du vill få åtkomst till det delade kontot anger du **[!UICONTROL Switch Accounts]** till namnet på det delade kontot.

   ![Växla till det delade kontot](./assets/shared-switch.png){width="600" zoomable="yes"}

   Det delade kontot visar ett välkomstmeddelande och kontaktinformation. Den vänstra navigeringspanelen innehåller endast de objekt som du har behörighet att använda.

1. Om du vill ansluta det delade kontot till hjälpcentret klickar du på **[!UICONTROL Support]** i den vänstra navigeringspanelen för det delade kontot.

   ![Support](./assets/shared-support.png){width="600" zoomable="yes"}

   Du kan använda [Adobe Commerce Help Center](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview) från det delade kontot för att söka efter artiklar och felsökningsinformation, hitta korrigeringsfiler för kända problem och skapa supportärenden.

   >[!NOTE]
   >
   >När användaren har fått delad åtkomst måste han/hon logga in på sitt [[!DNL Commerce] konto](https://account.magento.com/customer/account/login), navigera till _Delad åtkomst_ och klicka på fliken **[!UICONTROL Support]**. Den här åtgärden krävs första gången bara för att säkerställa att [Adobe Commerce Support Knowledge Base](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview) har konfigurerats korrekt via `SSO`-anropet.

1. Om du vill återgå till ditt eget konto klickar du på **Bakåt** i webbläsarkontrollerna och anger **[!UICONTROL Switch Accounts]** till `My Account`.

## Återkalla delad åtkomst

1. Logga in på ditt Commerce-konto.

1. Klicka på **[!UICONTROL Shared Access]** i den vänstra navigeringspanelen.

1. Hitta kontot som ska återkallas under _[!UICONTROL Managing Users & Permissions]_och klicka på&#x200B;**[!UICONTROL Delete]**.

   >[!NOTE]
   >
   > Om **[!UICONTROL Delete]** inte visas kontrollerar du om **[!UICONTROL Share Name]** börjar med `Cloud Shared Access from MAG XYZ`. Du kan inte ta bort konton med det [namnmönstret](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users).
   > 
   > Be i så fall kontoägaren att ändra kontot för delad åtkomst för att rensa kontobehörigheterna. Efter den uppdateringen kan användaren inte komma åt några kontoresurser.
   >
   > Se dessutom till att användarna tas bort från projektet så att de inte längre får e-postmeddelanden: [Tidigare teammedlemmar får Adobe Commerce molnmeddelanden](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails)


1. När du uppmanas att bekräfta klickar du på **[!UICONTROL Delete User]**.

>[!NOTE]
>
>Du kan inte ta bort användare med resursnamnet _Cloud Shared Access från MAG[XYZ]_ i det här gränssnittet. Se [Så här tar du bort användare som har beviljats delad åtkomst via ett molnprojekt?](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/shared-access-troubleshooting).
