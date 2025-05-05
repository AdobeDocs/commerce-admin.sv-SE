---
title: Adobe Experience Cloud Integration for Commerce Admin
description: Läs mer om Admin Unified Experience-tillägget som integrerar Commerce med Experience Cloud så att kunderna kan komma åt Commerce-projekt från Experience Cloud hemsida.
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
source-git-commit: 61874f3dac4f574ad393e8ae258f3d6c56c8f37e
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Adobe Experience Cloud Integration för Commerce

<table style="border:1px solid red">
<tr><td><img alt="Funktionen Adobe Commerce" src="../assets/adobe-logo.svg" width="20" height="20" /> Endast exklusiv funktion i Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=sv-SE#product-editions">Läs mer</a>)</td></tr>
</table>

Integrera Adobe Commerce-projekt med Experience Cloud genom att aktivera Admin Unified Experience-tillägget. När integreringen är aktiv kan administratörer komma åt Commerce-projekt från Adobe Experience Cloud.

![Få åtkomst till Commerce från Experience Cloud hemsida](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## Visa tillgängliga Commerce-projekt

Administratörer kan visa Commerce-projekt som de har behörighet att komma åt genom att välja **[!UICONTROL Commerce]** på Experience Cloud hemsida.

![Commerce Projects-arbetsyta på Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

Administratörer kan öppna Admin och Storefront för varje projekt från arbetsytan [!DNL Commerce Projects] och visa ytterligare information.

- **Ögonblicksbild av Commerce Store-startsida** - ögonblicksbild av butikens startsida. Om ett projekt har flera webbplatser visar ögonblicksbilden startsidan för standardwebbplatsen.

- **[Projektnamn](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html?lang=sv-SE)** - Identifierar instansens molnprojektmiljö. Projektnamnet är som standard [Git-grennamnet](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html?lang=sv-SE) i molnprojektet. Ändra eller uppdatera projektnamnet i konfigurationsinställningarna för [Unified Experience Store](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[Lagringsplats-URL](../stores-purchase/store-urls.md)** - Visar bas-URL:en för standardwebbplatsen.

- **[Miljötyp](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html?lang=sv-SE)** - Commerce-instanser som distribueras till en utvecklings- eller staging-miljö identifieras med en [!UICONTROL Development]- eller [!UICONTROL Staging]-etikett. Instanser som inte har någon etikett distribueras till en produktionsmiljö.

- **Commerce Admin-åtkomst** - Öppna administratören genom att klicka på **[!UICONTROL Open]**.

- **Storefront-åtkomst** - Öppna butiken genom att välja **[!UICONTROL Open storefront]** på Alternativ-menyn.

- **Snabb åtkomst för att välja projekt** - Välj **[!UICONTROL Add to Favorites]** på Alternativ-menyn om du vill lägga till ett projekt på fliken [!UICONTROL Favorites] .

## Autentiseringsflöde

När integreringen av Experience Cloud är aktiverad använder administratörer följande arbetsflöde för att autentisera och komma åt Commerce-projekt.

1. Logga in via inloggningssidan för Experience Cloud.

   ![Experience Cloud - inloggningssida](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   Administratörer måste logga in på Experience Cloud med företagsprofilen Adobe för den organisation som är associerad med Commerce-instansen. Se [Hantera Adobe-profiler](https://helpx.adobe.com/se/enterprise/using/manage-adobe-profiles.html).

1. Öppna [!UICONTROL Commerce Projects workspace] på startsidan för Experience Cloud genom att välja **[!UICONTROL Open]**.

1. Gå till Admin för ett projekt genom att välja **[!UICONTROL Open]**.

1. På Adobe Commerce Sign In-sidan väljer du **[!UICONTROL Sign in with Adobe ID]** för att slutföra autentiseringen och öppna Admin.

   ![Adobe Commerce - inloggningssida](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Mer information om hur autentiseringsarbetsflödet påverkas när integreringen med Experience Cloud är aktiverad eller inaktiverad finns i [Hantera integreringen med Experience Cloud](admin-unified-experience-integration-manage.md).

## Krav

- Adobe Commerce 2.4.5 eller senare
- Adobe Commerce i molninfrastruktur
- Adobe Commerce-tillägg

   - Commerce Admin Unified Experience-tillägg (`magento/module-unified-experience`)

     Om modulen inte är tillgänglig på Commerce-instansen kan den installeras med Composer.

   - [Adobe I/O Events-tjänsten](https://developer.adobe.com/commerce/extensibility/events/) - Krävs för att skicka händelsedata för att hantera administratörsåtkomst till Commerce-projekt från Experience Cloud.

     Integreringen av Adobe I/O Events med Commerce aktiveras av Commerce Event-tillägget (`magento/commerce-eventing`) som är tillgängligt med Adobe Commerce 2.4.4 och senare versioner.

## Aktivera integreringen

Aktivera integreringen genom att följa instruktionerna för att [konfigurera Experience Cloud-integreringen med Commerce Admin](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>Om integreringen av Experience Cloud redan är aktiverad på Commerce-instansen kan du läsa [Hantera integreringen av Experience Cloud](admin-unified-experience-integration-manage.md) för mer information om hur du ändrar eller uppdaterar konfigurationen, hanterar administratörsåtkomst och felsökning.
