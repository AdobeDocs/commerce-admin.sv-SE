---
title: Dela en [!DNL Commerce] konto
description: Lär dig hur du ger begränsad åtkomst till dina [!DNL Commerce] konto för andra [!DNL Commerce] kontoinnehavare.
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
source-git-commit: 8d4c37f512030c907d26b0210ddaad11ce605dfe
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Dela en [!DNL Commerce] konto

Dina [!DNL Commerce] kontot innehåller information som du kan göra tillgänglig för betrodda medarbetare och tjänsteleverantörer som hjälper dig att hantera din webbplats. Som primär kontoinnehavare har du behörighet att bevilja begränsad tillgång till andra [!DNL Commerce] kontoinnehavare. Delad åtkomst kan återkallas, men kan inte överföras från en användare till en annan.

The [!DNL Commerce] Supportteamet har inte åtkomst till kontot och kan inte konfigurera delad åtkomst för dig. Det är bara den primära kontoinnehavaren med rätt behörigheter som kan konfigurera delad åtkomst. När ditt konto delas förblir all känslig information, t.ex. din faktureringshistorik eller kreditkortsinformation, skyddad och delas inte med andra användare.

>[!NOTE]
>
>Den primära kontoinnehavaren ansvarar själv för alla åtgärder som vidtas av användare med delad åtkomst. Adobe ansvarar inte för några åtgärder som vidtas av användare som har delad åtkomst till ditt konto.

![Inställningar för delad åtkomst](./assets/shared-access.png){width="600" zoomable="yes"}

## Konfigurera ett delat konto

1. Hämta följande information från [!DNL Commerce] konto för **nytt delat åtkomstbeviljande**:

   - Användaren måste ha registrerat sig för ett konto på account.adobe.com och loggas in via account.magento.com.
   - The `Account ID` som visas längst upp till vänster i _[!UICONTROL Magento]_-fliken, precis ovanför **Logga ut**länk.
   - The `Email` adress som är associerad med kontot.

1. Logga in på [[!DNL Commerce] konto](commerce-account-create.md).

1. Klicka på i den vänstra navigeringspanelen **[!UICONTROL Shared Access]**.

1. Klicka på **[!UICONTROL Add New User]**.

   ![Lägg till en ny användare](./assets/shared-access-add.png){width="600" zoomable="yes"}

1. Under [!UICONTROL _New User Information]_, gör följande:

   - Ange **[!UICONTROL Account ID]** från den nya användarens [!DNL Commerce] konto.
   - Ange **[!UICONTROL Email]** adress som är associerad med den nya användarens [!DNL Commerce] konto.

   ![Ny användarinformation](./assets/shared-new-user.png){width="600"}

1. Under _[!UICONTROL Shared Information]_gör du följande:

   - Om du vill identifiera det delade kontot anger du en **[!UICONTROL Share Name]**. Det här namnet används som intern referens och är bara synligt för dig och den person som du delar ditt konto med. (Ange inte ett resursnamn som börjar med `CLOUD SHARED ACCESS FROM MAG XYX`.)
   - Om du vill dela din personliga kontaktinformation med den nya användaren anger du **[!UICONTROL Your Email]** och **[!UICONTROL Your Phone]**.

1. Under _[!UICONTROL Grant Account Permissions]_markerar du kryssrutan för varje [!DNL Commerce] produkt och tjänst som du vill dela.

   ![Bevilja kontobehörigheter](./assets/shared-permissions.png){width="600"}

1. När du är klar klickar du på **[!UICONTROL Create Shared Access]**.

   Den nya användarinformationen visas i _[!UICONTROL Manage Permissions]_på sidan Delad åtkomst och en e-postinbjudan med instruktioner om hur du får åtkomst till det delade kontot skickas till den nya användaren.

   ![Hantera behörigheter för delad åtkomst](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

## Åtkomst till ett delat konto

Följande instruktioner är skrivna ur ett delat användarperspektiv som tar emot en inbjudan till ett delat konto.

1. När du får en inbjudan till ett delat konto följer du instruktionerna i e-postmeddelandet för att logga in på ditt eget konto [!DNL Commerce] konto.

   Den vänstra navigeringspanelen för ditt konto har en ny _[!UICONTROL Shared with me]_-fliken. The_[!UICONTROL Switch Accounts]_ i det övre högra hörnet har alternativ för `My Account` och namnet på det delade kontot.

   ![Delas med mig](./assets/shared-with-me.png){width="600" zoomable="yes"}

1. Om du vill få åtkomst till det delade kontot anger du **[!UICONTROL Switch Accounts]** till namnet på det delade kontot.

   ![Växla till det delade kontot](./assets/shared-switch.png){width="600" zoomable="yes"}

   Det delade kontot visar ett välkomstmeddelande och kontaktinformation. Den vänstra navigeringspanelen innehåller endast de objekt som du har behörighet att använda.

1. Om du vill ansluta det delade kontot till hjälpcentret klickar du på **[!UICONTROL Support]** i den vänstra navigeringspanelen för det delade kontot.

   ![Support](./assets/shared-support.png){width="600" zoomable="yes"}

   Du kan använda [Adobe Commerce Help Center](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html) från det delade kontot för att söka efter artiklar och felsökningsinformation, hitta patchar för kända fel och skapa supportärenden.

   >[!NOTE]
   >
   >Efter att ha fått delad åtkomst måste användaren logga in på [[!DNL Commerce] konto](https://account.magento.com/customer/account/login), navigera till _Delad åtkomst_ och klickar på **[!UICONTROL Support]** -fliken. Den här åtgärden krävs endast första gången för att säkerställa att [Adobe Commerce Support Knowledge Base](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html) är korrekt konfigurerad via `SSO` ring.

1. Om du vill återgå till ditt eget konto klickar du på **Bakåt** i webbläsarens reglage **[!UICONTROL Switch Accounts]** till `My Account`.

## Återkalla delad åtkomst

1. Logga in på ditt Commerce-konto.

1. Klicka på i den vänstra navigeringspanelen **[!UICONTROL Shared Access]**.

1. Hitta kontot som ska återkallas under _[!UICONTROL Managing Users & Permissions]_och klicka **[!UICONTROL Delete]**.

   >[!NOTE]
   >
   > If  **[!UICONTROL Delete]** visas inte, kontrollera om **[!UICONTROL Share Name]** börjar med `Cloud Shared Access from MAG XYZ` - [dessa konton](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#remove-cloud-shared-access-users) kan inte tas bort.
   > 
   > Be i så fall kontoägaren att ändra kontot för delad åtkomst och rensa kontobehörigheterna. Efter den uppdateringen är delad åtkomst till någon av resurserna inte tillgänglig för användaren.
   >
   > Se dessutom till att användarna tas bort från projektet så att de inte längre får e-postmeddelanden: [Före detta teammedlemmar får Adobe Commerce molnmeddelanden via e-post](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails.html)


1. När du uppmanas att bekräfta klickar du på **[!UICONTROL Delete User]**.

>[!NOTE]
>
>Du kan inte ta bort användare med resursnamnet _Delad åtkomst i molnet från MAG[XYZ]_ i det här gränssnittet. Mer information finns i [Hur tar jag bort användare som beviljats delad åtkomst via ett Cloud-projekt?](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#remove-cloud-shared-access-users).
