---
title: Användarroller
description: Lär dig hur du skapar användarroller och tillhörande behörigheter för att hantera åtkomst till administratörsfunktioner.
exl-id: a70f74d4-72b4-4639-a67d-9fc13df65924
feature: Admin Workspace, Roles/Permissions, Security
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 0%

---

# Användarroller

För att ge någon begränsad åtkomst till administratören är det första steget att skapa en roll som har rätt behörighetsnivå. När rollen har sparats kan du lägga till nya användare och tilldela den begränsade rollen för att ge dem begränsad åtkomst till administratören.

![Admin - användarroller](./assets/permissions-role-grid.png){width="600" zoomable="yes"}

## Definiera en roll

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add New Role]** i det övre högra hörnet.

1. Slutför stegen för att definiera rollen:

### Steg 1: Lägg till rollnamnet

1. Under _[!UICONTROL Role Information]_anger du en beskrivande **[!UICONTROL Role Name]**.

1. Ange ditt lösenord under _[!UICONTROL Current User Identity Verification]_.

   ![Systembehörigheter - rollinformation](./assets/permissions-role-info.png){width="600" zoomable="yes"}

### Steg 2: Tilldela resurser

>[!IMPORTANT]
>
>När du tilldelar resurser ska du se till att inaktivera åtkomsten till behörighetsverktyget om du begränsar åtkomsten för en viss roll. Annars kan användarna ändra sina egna behörigheter.

1. Ange **[!UICONTROL Role Scopes]** till något av följande:

   - `All`
   - `Custom`

   Om värdet är `Custom` för en installation på flera platser markerar du kryssrutan för webbplatsen och lagret där rollen ska användas.

   ![Resurser för användarroll - anpassat omfång](./assets/permissions-role-scope-custom.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Användare med rollomfånget `Custom` kan inte skapa webbplatser och kategorier, tilldela produkter till kategorier eller redigera produkter i omfattningen _[!UICONTROL All Store Views]_när de tilldelas begränsade butiker. De här användarna kan inte heller utföra andra_ globala _åtgärder som påverkar scope där de inte har åtkomst.

1. Under _[!UICONTROL Roles Resources]_anger du **[!UICONTROL Resource Access]**till `Custom`.

1. Markera kryssrutan för varje administratörsfunktion som rollen har åtkomst till i trädstrukturen **[!UICONTROL Resource]**.

   Om du vill skapa en administratörsroll med tillgång till skatteinställningar väljer du både moms och system/skatt. Om du konfigurerar en webbplats för en region som skiljer sig från din [leveransplats](../stores-purchase/shipping-settings.md#point-of-origin) måste du tillåta åtkomst till system-/leveransresurserna för rollen. Leveransinställningarna bestämmer momssatsen som används för katalogpriser.

   ![Tilldelade användarrollresurser](./assets/permissions-role-resources-product.png){width="600" zoomable="yes"}

   Listan över tillgängliga behörigheter kan innehålla ytterligare alternativ för programpaket och installerade tillägg. Genom att välja den översta behörigheten för varje funktion tilldelar du alla behörigheter som är tillgängliga för användaren.

   >[!NOTE]
   >
   >En Admin-användare måste ha **[!UICONTROL Sales / Archive]** behörigheter för att kunna se flikarna _[!UICONTROL Invoices]_,_[!UICONTROL Credit Memos]_ och _[!UICONTROL Shipments]_order [ ](../stores-purchase/order-processing.md).

1. Klicka på **[!UICONTROL Save Role]** när du är klar.

   Rollen visas nu i rutnätet och kan tilldelas användarkonton.

## Tilldela användare en roll

1. Öppna posten i redigeringsläge från stödrastret _[!UICONTROL Roles]_.

1. Ange ditt lösenord för användarkontot under _[!UICONTROL Current User Identity Verification]_.

1. Välj **[!UICONTROL Role Users]** på den vänstra panelen.

   Alternativet _[!UICONTROL Role Users]_visas bara när en ny roll har sparats.

   ![Användarkonton som tilldelats rollen](./assets/permissions-role-users.png){width="600" zoomable="yes"}

1. Så här söker du efter en viss användarpost:

   - Ange värdet i sökfiltret längst upp i en kolumn och tryck på **Retur**.

   - När du är redo att återgå till den fullständiga listan klickar du på **[!UICONTROL Reset Filter]**.

1. Markera kryssrutan för de användare som ska tilldelas rollen.

1. Klicka på **[!UICONTROL Save Role]**.

## Redigera en roll

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**på sidofältet_ Admin _.

1. Leta reda på rollen med hjälp av filter ovanför stödrastret och klicka på rollnamnet.

1. Gör nödvändiga ändringar.

   Om du vill ha mer information om rollinställningarna läser du stegen för hur du skapar en användarroll.

1. Ange ditt lösenord för att bekräfta din identitet när du uppmanas till detta.

1. Klicka på **[!UICONTROL Save Role]**.

## Ta bort en roll

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**på sidofältet_ Admin _.

1. Leta reda på rollen med hjälp av filter ovanför stödrastret och öppna i redigeringsläge.

1. Klicka på **[!UICONTROL Delete Role]** i det övre högra hörnet.

1. Bekräfta åtgärden genom att klicka på **[!UICONTROL OK]**.

## Demo av användarroller

I den här videon får du lära dig mer om hur du hanterar användarroller:

>[!VIDEO](https://video.tv.adobe.com/v/343654?quality=12&learn=on)

## Rollresurser

En anpassad roll kan tilldelas åtkomst till följande resurser. På den länkade sidan finns mer information om de funktioner som är kopplade till varje resurs.

![Adobe Commerce](../assets/adobe-logo.svg) - endast Adobe Commerce

![Adobe Commerce B2B](../assets/b2b.svg) - endast tillgängligt med Adobe Commerce B2B

| Resurs |   |   |
| --- | --- | --- |
| [`Dashboard`](../getting-started/admin-dashboard.md) |  |  |
| [`Sales`](../stores-purchase/sales-menu.md) | [`Operations`](../stores-purchase/orders.md) |  |
|  | [`Quotes`](../b2b/quotes.md) ![Adobe Commerce B2B](../assets/b2b.svg) <br/>[`Orders`](../stores-purchase/orders.md)<br/>[`Invoices`](../stores-purchase/invoices.md)<br/>[`Shipments`](../stores-purchase/shipments.md)<br/>[`Credit Memos`](../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../stores-purchase/returns.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Transactions`](../stores-purchase/transactions.md) |
|  | [`Archive`](action-log-archive.md)![Adobe Commerce] |  |
|  | [`Shopping Cart Management`](../stores-purchase/cart.md) |  |
| [`Catalog`](../catalog/catalog-menu.md) | [`Category Permissions`](../catalog/categories.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Inventory`](../inventory-management/introduction.md) | [`Products`](../catalog/products-list.md)<br/>[`Categories`](../catalog/categories.md) |
|  | [`Shared Catalog`](../b2b/catalog-shared-create.md) ![Adobe Commerce B2B](../assets/b2b.svg) | [`Manage Shared Catalog`](../b2b/catalog-shared-manage.md) |
| [`Customers`](../customers/guide-overview.md) | [`All Customers`](../customers/customers-all.md)<br/>[`Now Online`](../customers/now-online.md)<br/>[`Customer Groups`](../customers/customer-groups.md)<br/>[`Segments`](../customers/customer-segments.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Login as Customer`](../customers/login-as-customer.md) | `Allow Login as Customer Button`<br/>`View Login as Customer Log` ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Companies`](../b2b/account-companies.md) ![Adobe Commerce B2B](../assets/b2b.svg) | [`Manage Companies`](../b2b/account-company-manage.md) <br/>`Add New Company` <br/>`Delete Company` <br/>`Reimburse Balance` |
| [`Carts`](../stores-purchase/shopping-assisted-cart-manage.md) | [`Manage carts`](../stores-purchase/shopping-assisted-cart-manage.md) |  |
| [`My Account`](../customers/account-dashboard-my-account.md) |  |  |
| [`Marketing`](../merchandising-promotions/marketing-menu.md) | [`Promotions`](../merchandising-promotions/marketing-menu.md#uicontrol-promotions) | [`Catalog Price Rule`](../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../merchandising-promotions/price-rules-cart.md) <br/>[`Related Products Rules`](../merchandising-promotions/product-related-rules.md)![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Gift Card Accounts`](../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Private Sales`](../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../assets/adobe-logo.svg) | [`Events`](../merchandising-promotions/event-create.md) <br/>[`Invitations`](../merchandising-promotions/invitations.md) |
|  | `Communications` | [`Email Templates`](email-templates.md) <br/>[`Newsletter Template`](../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../merchandising-promotions/email-reminder-rules.md) |
|  | `Sales Channel` | [`Amazon Sales Channel`](https://experienceleague.adobe.com/docs/commerce-channels/amazon/overview.html) |
|  | [`SEO & Search`](../merchandising-promotions/marketing-menu.md#uicontrol-seo--search) | [`Search Terms`](../catalog/search-terms.md) <br/>[`Search Synonyms`](../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../merchandising-promotions/url-rewrite-custom.md) <br/>[`Site Map`](../merchandising-promotions/sitemap-xml.md) |
|  | [`User Content`](../merchandising-promotions/product-reviews-moderate.md) | [`All Reviews`](../merchandising-promotions/product-reviews.md) <br/>[`Pending Reviews`](../merchandising-promotions/product-reviews-moderate.md) <br/> |  |
| [`Content`](../content-design/content-menu.md) | [`Elements`](../content-design/content-menu.md#uicontrol-elements)) | [`Pages`](../content-design/pages.md)<br/>[`Hierarchy`](../content-design/page-hierarchy.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Blocks`](../content-design/blocks.md)<br/>[`Dynamic Blocks`](../content-design/dynamic-blocks.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Widgets`](../content-design/widgets.md)<br/>[`Media Gallery`](../content-design/media-gallery.md) |  |
|  | [`Design`](../content-design/introduction.md#design) | [`Themes`](../content-design/themes.md)<br/>[`Schedule`](../content-design/schedule.md) |  |
|  | [Mellanlagring av innehåll](../content-design/content-staging.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br /> |  |
| [`Reports`](../getting-started/reports-menu.md) | [`Marketing`](../getting-started/marketing-reports.md) | `Shopping Cart`<br />[`Search Terms`](../catalog/search-terms.md#search-terms-report)<br />`Newsletter Problem Reports` |  |
|  | [`Reviews`](../getting-started/review-reports.md)<br /> |  |
|  | [`Sales`](../getting-started/sales-reports.md) |  |
|  | `System Insights` ![Adobe Commerce](../assets/adobe-logo.svg) | [`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html) |
|  | [`Customers`](../getting-started/customer-reports.md)<br/>[`Products`](../getting-started/product-reports.md)<br/>[`Private Sales`](../getting-started/private-sales-reports.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br />[`Statistics`](../getting-started/reports-menu.md#uicontrol-statistics)<br />[`Business Intelligence`](../getting-started/business-intelligence.md) |  |
| [`Stores`](../stores-purchase/stores.md) | [`Settings`](../stores-purchase/stores-menu.md) | [`All Stores`](../stores-purchase/stores.md)<br/>[`Configuration`](../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../stores-purchase/order-status.md) |  |
|  | [`Inventory`](../inventory-management/sources-stocks.md) | [`Sources`](../inventory-management/sources-manage.md)<br/>[`Stocks`](../inventory-management/stocks-manage.md) |  |
|  | [`Taxes`](../stores-purchase/taxes.md) |  |  |
|  | [`Currency`](../stores-purchase/currency.md) | [`Currency Rates`](../stores-purchase/currency-update.md)<br/>[`Currency Symbols`](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) |  |
|  | [`Attributes`](../catalog/product-attributes.md) | [`Product`](../catalog/attribute-product-create.md)<br/>[`Update Attributes`](../catalog/attribute-product-create.md)<br/>[`Attribute Set`](../catalog/attribute-sets.md)<br/>[`Ratings`](../merchandising-promotions/product-reviews.md#create-custom-ratings) |
|  | [`Other Settings`](../stores-purchase/stores-menu.md) | [`Customer Groups`](../customers/customer-groups.md) |
| [`System`](system-menu.md) | [`Data Transfer`](data-transfer.md) | [`Import`](data-import.md)<br/>[`Export`](data-export.md)<br/>[`Import/Export Tax Rates`](data-transfer-tax-rates.md)<br/>[`Import History`](data-import.md#import-history) |  |
|  | [`Magento Connect`](../getting-started/commerce-marketplace.md) | `Connect Manager`<br/>`Package Extensions` |  |
|  | [`Tools`](system-menu.md#tools) | [`Cache Management`](cache-management.md)<br/>[`Backups`](backups.md)<br/>[`Index Management`](index-management.md)<br/>[`Change Indexer Mode`](index-management.md) |  |
|  | [`Permissions`](permissions.md) | [`All Users`](permissions-users-all.md)<br/>[`Locked Users`](permissions-users-all.md#locked-users)<br/>[`User Roles`](permissions-user-roles.md) |
| [`Action Log`](action-log.md)![Adobe Commerce](../assets/adobe-logo.svg) | [`Report`](action-log.md)<br/>[`Archive`](action-log-archive.md) |
|  | [`Other Settings`](system-menu.md) | [`Notifications`](notifications.md)<br/>[`Custom Variables`](variables-custom.md)<br/>[`Manage Encryption Key`](encryption-key.md) |  |
| [`Global Search`](../getting-started/admin-workspace.md#workspace-search) |  |  |

{style="table-layout:auto"}
