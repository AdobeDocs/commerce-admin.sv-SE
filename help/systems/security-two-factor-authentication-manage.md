---
title: Hantera tvåfaktorsautentisering
description: Lär dig hur du hanterar tvåfaktorsautentisering och återställer autentiserarna för administratörsanvändare.
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# Hantera tvåfaktorsautentisering

Användare som inte kan logga in på _Administratör_ med tvåfaktorsautentisering (2FA) kan försöka synkronisera eller felsöka problemet. Du kan också återställa autentiserarna som är kopplade till kontot. Vid återställning måste användaren logga in igen och konfigurera om de nödvändiga autentiserarna.

Om du har problem med att logga in med 2FA bör du tänka på följande:

- Vissa mobilappar innehåller synkroniseringsalternativ. Det här alternativet återansluter programmet och servern och synkroniserar tidsinställningarna på enheten och servern.
- Genom att återkalla en enhet eller återställa en autentiserare kan användarna ansluta.
- Att rensa webbcachen och cookies för installationen av Adobe Commerce eller Magento Open Source kan också vara till hjälp. Autentiserare, som Google, använder genererade cookies för att spara åtkomst och varaktighet. Rensa cookies för din specifika webbläsare och butiksdomän.
- Spärra cookies förhindrar vissa autentiserare, som [!DNL Google Authenticator]från det att verifieringsprocessen har slutförts. Lägg till en regel i webbläsaren som tillåter cookies för din Adobe Commerce-installation.

Information om hur du återställer autentiserare från kommandoraden och mer avancerad felsökningsinformation finns i [Autentisering med två faktorer](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/) i utvecklardokumentationen.

**_Så här återställer du autentiserare för ett användarkonto:_**

>[!NOTE]
>
>Om du vill återställa 2FA-providers för andra användare måste du vara en _administratör_ med `All` behörigheter, eller har `Custom` behörigheter för din roll med [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth] och [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users] markerat. Mer information finns på [Användarroller](permissions-user-roles.md).

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Markera användaren och öppna kontot i redigeringsläge.

1. Bläddra nedåt till _[!UICONTROL Current User Identity Verification]_och ange ditt lösenord.

1. Klicka på i den vänstra panelen **[!UICONTROL 2FA]**.

1. I _[!UICONTROL Configuration reset]_avsnitt, klicka **[!UICONTROL Reset]**och **[!UICONTROL OK]**för att bekräfta.

   ![Användarkonto - aktivera 2FA](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   Om användaren vill återställa de 2FA-metoder som krävs till sitt konto måste de konfigurera om var och en av dem från _Logga in_ sida.

1. När du är klar klickar du på **[!UICONTROL Save User]**.
