---
title: Adobe Experience Cloud Integration for Commerce Admin
description: Läs mer om Admin Unified Experience-tillägget som integrerar handel med Experience Cloud så att kunderna kan komma åt Commerce-projekt från Experience Cloud hemsida.
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Adobe Experience Cloud Integration for Commerce

{{ee-feature}}

{{$include /help/_includes/admin-unified-experience-beta-note.md}}

Integrera Adobe Commerce-projekt med Experience Cloud genom att aktivera Admin Unified Experience-tillägget. När integreringen är aktiv kan administratörer få åtkomst till Commerce-projekt från Adobe Experience Cloud.

![Få tillgång till Commerce från Experience Cloud hemsida](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## Visa tillgängliga handelsprojekt

Administratörer kan visa Commerce-projekt som de har behörighet att komma åt genom att välja **[!UICONTROL Commerce]** från Experience Cloud hemsida.

![Arbetsytan för Commerce Projects på Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

Administratörer kan öppna Admin och Storefront för varje projekt från [!DNL Commerce Projects] och visa ytterligare information.

- **Ögonblicksbild av startsidan för Commerce Store**—Ögonblicksbild av butikens startsida. Om ett projekt har flera webbplatser visar ögonblicksbilden startsidan för standardwebbplatsen.

- **[Projektnamn](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**—Identifierar instansens molnprojektmiljö. Projektnamnet är som standard [Git-grennamn](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html) i molnprojektet. Ändra eller uppdatera projektnamnet i [Konfigurationsinställningar för Unified Experience Store](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[Lagringsplats-URL](../stores-purchase/store-urls.md)**- Visar bas-URL:en för standardwebbplatsen.

- **[Miljötyp](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**—Handelsinstanser som distribueras till en utvecklings- eller mellanlagringsmiljö identifieras med en [!UICONTROL Development] eller [!UICONTROL Staging] etikett. Instanser som inte har någon etikett distribueras till en produktionsmiljö.

- **Åtkomst till Commerce Admin**—Öppna administratören genom att klicka på **[!UICONTROL Open]**.

- **Åtkomst till butiken**—Öppna butiken genom att välja **[!UICONTROL Open storefront]** på Alternativ-menyn.

- **Snabb åtkomst till utvalda projekt**—Select **[!UICONTROL Add to Favorites]** på Alternativ-menyn för att lägga till ett projekt i [!UICONTROL Favorites] -fliken.

## Autentiseringsflöde

När integreringen av Experience Cloud är aktiverad använder administratörer följande arbetsflöde för att autentisera och få åtkomst till Commerce-projekt.

1. Logga in via inloggningssidan för Experience Cloud.

   ![Experience Cloud inloggningssida](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   Administratörer måste logga in på Experience Cloud med affärsprofilen för Adobe för den organisation som är associerad med Commerce-instansen. Se [Hantera Adobe-profiler](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html).

1. På Experience Cloud hemsida öppnar du [!UICONTROL Commerce Projects workspace] genom att välja **[!UICONTROL Open]**.

1. Gå till Admin för ett projekt genom att välja **[!UICONTROL Open]**.

1. På Adobe Commerce Sign In-sidan väljer du **[!UICONTROL Sign in with Adobe ID]** för att slutföra autentiseringen och öppna Admin.

   ![Inloggningssida för Adobe Commerce](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Se [Hantera integreringen med Experience Cloud](admin-unified-experience-integration-manage.md) om du vill ha information om hur autentiseringsarbetsflödet påverkas när integreringen av Experience Cloud är aktiverad eller inaktiverad.

## Krav

- Adobe Commerce 2.4.5 eller senare
- Adobe Commerce i molninfrastruktur
- Adobe Commerce-tillägg

   - Commerce Admin - tillägg för enhetlig upplevelse (`magento/module-unified-experience`)

     Om modulen inte är tillgänglig i Commerce-instansen kan den installeras med Composer.

   - [Tjänsten Adobe I/O Events](https://developer.adobe.com/commerce/extensibility/events/)- Krävs för att skicka händelsedata för att hantera administratörsåtkomst till Commerce-projekt från Experience Cloud.

     Integreringen av Adobe I/O Events med Commerce aktiveras av tillägget Commerce Event (`magento/commerce-eventing`) som finns i Adobe Commerce 2.4.4 och senare.

## Aktivera integreringen

Aktivera integreringen genom att följa instruktionerna för att [Konfigurera integreringen av Experience Cloud med Commerce Admin](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>Om integreringen av Experience Cloud redan är aktiverad i Commerce-instansen finns mer information i [Hantera integreringen med Experience Cloud](admin-unified-experience-integration-manage.md) om du vill ha information om hur du ändrar eller uppdaterar konfigurationen, hanterar administratörsåtkomst och felsökning.
