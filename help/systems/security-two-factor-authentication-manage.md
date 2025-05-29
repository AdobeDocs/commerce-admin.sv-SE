---
title: Hantera tvåfaktorsautentisering
description: Lär dig hur du hanterar tvåfaktorsautentisering och återställer autentiserarna för administratörsanvändare.
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# Hantera tvåfaktorsautentisering

Användare som inte kan logga in på _Admin_ med tvåfaktorsautentisering (2FA) kan försöka synkronisera eller felsöka problemet. Du kan också återställa autentiserarna som är kopplade till kontot. Vid återställning måste användaren logga in igen och konfigurera om de nödvändiga autentiserarna.

Om du har problem med att logga in med 2FA bör du tänka på följande:

- Vissa mobilappar innehåller synkroniseringsalternativ. Det här alternativet återansluter programmet och servern och synkroniserar tidsinställningarna på enheten och servern.
- Genom att återkalla en enhet eller återställa en autentiserare kan användarna ansluta.
- Att rensa webbcachen och cookies för Adobe Commerce- eller Magento Open Source-installationen kan också vara till hjälp. Autentiserare, som Google, använder genererade cookies för att spara åtkomst och varaktighet. Rensa cookies för din specifika webbläsare och butiksdomän.
- Genom att blockera cookies förhindras vissa autentiserare, som [!DNL Google Authenticator], från att slutföra verifieringsprocessen. Lägg till en regel i webbläsaren som tillåter cookies för din Adobe Commerce-installation.

Information om hur du återställer autentiserare från kommandoraden och mer avancerad felsökningsinformation finns i [Tvåfaktorautentisering](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/) i utvecklardokumentationen.

**_Så här återställer du autentiserare för ett användarkonto:_**

>[!NOTE]
>
>Om du vill återställa 2FA-providers för andra användare måste du vara _administratör_ med `All` behörigheter eller ha `Custom` behörigheter för din roll med [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth] och [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users] markerat. Mer information finns i [Användarroller](permissions-user-roles.md).

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**på sidofältet_ Admin _.

1. Markera användaren och öppna kontot i redigeringsläge.

1. Bläddra ned till avsnittet _[!UICONTROL Current User Identity Verification]_och ange ditt lösenord.

1. Klicka på **[!UICONTROL 2FA]** i den vänstra panelen.

1. Klicka på **[!UICONTROL Reset]** och **[!UICONTROL OK]** i avsnittet _[!UICONTROL Configuration reset]_för att bekräfta.

   ![Användarkonto - aktivera 2FA](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   Om användaren vill återställa de 2FA-metoder som krävs till sitt konto måste de konfigurera om varje metod från sidan _Logga in_.

1. Klicka på **[!UICONTROL Save User]** när du är klar.
