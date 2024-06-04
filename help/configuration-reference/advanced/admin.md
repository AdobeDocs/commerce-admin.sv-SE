---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL Admin]'
description: Granska konfigurationsinställningarna på [!UICONTROL Advanced] &gt; [!UICONTROL Admin] sidan för Commerce Admin.
exl-id: 546b8d01-9611-4415-ab2b-29be560316f5
role: Admin
feature: Configuration, Admin Workspace
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 0%

---

# Avancerat > Admin

{{config}}

## [!UICONTROL Admin User Emails]

![Admin - e-post för användare](./assets/admin-admin-user-emails.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Glömt lösenord och återställ e-post](../../systems/permissions-users-all.md#forgotten-password-and-reset-emails).

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|---------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Forgot Password Email Template] | Global | Identifierar e-postmallen som används för meddelandet som skickas när en Admin-användare glömmer sitt lösenord. Standardmall: `Forgot Admin Password` |
| [!UICONTROL Forgot and Reset Email Sender] | Global | Identifierar butikskontakten som visas som avsändare av _Glömt lösenordet_ e-post. Standardavsändare: `General Contact`<br/>Andra avsändaralternativ: `Sales Representative`, `Customer Support`, `Custom Email` |
| [!UICONTROL User Notification Template] | Global | Bestämmer e-postmallen som används som standard för administratörsmeddelanden. Standardmall: `User Notification` |

{style="table-layout:auto"}

## [!UICONTROL Startup Page]

![Startsida](./assets/admin-startup-page.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Ändra startsidan](../../getting-started/admin-dashboard.md#change-the-startup-page) i _Starthandbok_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|---------------------------|------------------------------------------------------------------------|------------------------------------------------------------------|
| [!UICONTROL Startup Page] | Global | Bestämmer startsidan för administratören som visas när du har loggat in. |

{style="table-layout:auto"}

### [!UICONTROL Startup Page] alternativ

| Område |                                                                                                                                                                                                                                                                                                                                                                           | Alternativ |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`Dashboard`](../../getting-started/admin-dashboard.md) |                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `Sales` | `Operations` | [`Quotes`](../../b2b/quotes.md) ![Adobe Commerce B2B](../../assets/b2b.svg) <br/>[`Orders`](../../stores-purchase/orders.md)<br/>[`Invoices`](../../stores-purchase/invoices.md)<br/>[`Shipments`](../../stores-purchase/shipments.md)<br/>[`Credit Memos`](../../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../../stores-purchase/returns.md) ![Adobe Commerce](../../assets/adobe-logo.svg) </span><br/>[`Transactions`](../../stores-purchase/transactions.md)<br/>`Braintree Virtual Terminal` |
| `Catalog` | [`Inventory`](../../inventory-management/introduction.md) | [`Products`](../../catalog/products-list.md)<br/>[`Categories`](../../catalog/categories.md)<br/>[`Shared Catalog`](../../b2b/catalog-shared-create.md) ![Adobe Commerce B2B](../../assets/b2b.svg) |
| `Customers` | [`All Customers`](../../customers/customers-all.md)<br/>[`Now Online`](../../customers/now-online.md)<br/>[`Customer Groups`](../../customers/customer-groups.md)<br/>[`Segments`](../../customers/customer-segments.md) ![Adobe Commerce](../../assets/adobe-logo.svg) <br/>[`Companies`](../../b2b/account-companies.md)![Adobe Commerce B2B](../../assets/b2b.svg) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `Marketing` | `Promotions` | [`Catalog Price Rule`](../../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../../merchandising-promotions/price-rules-cart.md)) <br/>[`Related Products Rules`](../../merchandising-promotions/product-related-rules.md) ![Adobe Commerce](../../assets/adobe-logo.svg) <br/>[`Gift Card Accounts`](../../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | [`Private Sales`](../../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../../assets/adobe-logo.svg) | [`Events`](../../merchandising-promotions/event-configure.md) <br/>[`Invitations`](../../merchandising-promotions/invitations.md) |
|                                                         | `Communications` | [`Email Templates`](../../systems/email-templates.md) <br/>[`Newsletter Template`](../../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../../merchandising-promotions/email-reminder-rules.md) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | `SEO & Search` | [`Search Terms`](../../catalog/search-terms.md) <br/>[`Search Synonyms`](../../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../../merchandising-promotions/url-rewrite.md) <br/>[`Site Map`](../../merchandising-promotions/sitemap-xml.md) |
|                                                         | [`User Content`](../../catalog/settings-advanced-product-reviews.md) | [`All Reviews`](../../catalog/settings-advanced-product-reviews.md) <br/>[`Pending Reviews`](../../merchandising-promotions/product-reviews-moderate.md) <br/> |
| `Content` | `Elements` | [`Pages`](../../content-design/pages.md)<br/>[`Hierarchy`](../../content-design/page-hierarchy.md) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`Blocks`](../../content-design/blocks.md)<br/>[`Dynamic Blocks`](../../content-design/dynamic-blocks.md) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`Widgets`](../../content-design/widgets.md)<br/>[`Media Gallery`](../../content-design/media-storage.md) |
|                                                         | `Design` | [`Configuration`](../../content-design/configuration.md)<br/>[`Themes`](../../content-design/themes.md)<br/>[`Schedule`](../../content-design/schedule.md) |
|                                                         | `Content Staging` ![Adobe Commerce](../../assets/adobe-logo.svg)<br /> | [Kontrollpanel](../../content-design/content-staging.md) |
| `Reports` | [`Marketing`](../../getting-started/marketing-reports.md) | `Products in Cart`<br />`Search Terms`<br />`Abandoned Carts`<br />`Newsletter Problem Reports` |
|                                                         | [`Reviews`](../../getting-started/review-reports.md) | `By Customer`<br/> `By Products`<br/> |
|                                                         | [`Sales`](../../getting-started/sales-reports.md) | `Orders`<br/>`Tax`<br/>`Invoiced`<br/>`Shipping`<br/>`Refunds`<br/>`Coupons`<br/>`PayPal Settlement`<br/>`Braintree Settlement` |
|                                                         | `System Insights` | [`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | [`Customers`](../../getting-started/customer-reports.md) | `Order Total`<br/>`Order Count`<br/>`New`<br/>`Wish Lists`<br/>`Segments`<br/> |
|                                                         | [`Products`](../../getting-started/product-reports.md) | `Views`<br/>`Bestsellers`<br/>`Low Stock`<br/>`Ordered`<br/>`Downloads` |
|                                                         | [`Private Sales`](../../getting-started/private-sales-reports.md) ![Adobe Commerce](../../assets/adobe-logo.svg) | `Invitations`<br/>`Invited Customers`<br/>`Conversions` |
|                                                         | `Statistics` | [`Refresh Statistics`](../../getting-started/sales-reports.md#refresh-statistics) |
|                                                         | [`Business Intelligence`](../../getting-started/business-intelligence.md) | `Advanced Reporting`<br/>`BI Essentials`<br/> |
|                                                         | `Customer Engagement` | `Dashboard`<br/>`Importer Status`<br/>`Automation Enrollment`<br/>`Campaign Sends`<br/>`SMS Sends`<br/>`Cron Tasks`<br/>`Log Viewer`<br/>`Abandoned Carts` |
| `Stores` | `Settings` | [`All Stores`](../../stores-purchase/stores.md)<br/>[`Configuration`](../../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../../stores-purchase/order-status.md) |
|                                                         | [`Inventory`](../../inventory-management/introduction.md) | [`Sources`](../../inventory-management/sources-stocks.md#sources)<br/>[`Stocks`](../../inventory-management/sources-stocks.md#stocks) |
|                                                         | [`Taxes`](../../stores-purchase/taxes.md) | [`Tax Rules`](../../stores-purchase/tax-rules.md)<br/>[`Tax Zones and Rates`](../../stores-purchase/tax-zones-rates.md) |
|                                                         | [`Currency`](../../stores-purchase/currency.md) | [`Currency Rates`](../../stores-purchase/currency-configuration.md)<br/>[`Currency Symbols`](../../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) |
|                                                         | `Attributes` | [`Customer`](../../systems/data-attributes-customer.md)<br/>[`Customer Address`](../../systems/data-attributes-customer.md#customer-addresses)<br/>[`Product`](../../systems/data-attributes-product.md)<br/>[`Attribute Set`](../../catalog/attribute-sets.md)<br/>[`Returns`](../../stores-purchase/attributes-returns.md)<br/>[`Ratings`](../../merchandising-promotions/product-reviews.md#create-custom-ratings) |
|                                                         | `Other Settings` | [`Reward Exchange Rates`](../../merchandising-promotions/reward-exchange-rates.md)<br/>[`Gift Wrapping`](../../stores-purchase/cart-configuration.md#gift-wrap)<br/>[`Gift Registry`](../../merchandising-promotions/gift-registry-create.md) |
| `System` | [`Data Transfer`](../../systems/data-transfer.md) | [`Import`](../../systems/data-import.md)<br/>[`Export`](../../systems/data-export.md)<br/>[`Import/Export Tax Rates`](../../systems/data-transfer-tax-rates.md)<br/>[`Import History`](../../systems/data-import.md#import-history)<br/>[`Scheduled Import/Export`](../../systems/data-scheduled-import-export.md) |
|                                                         | `Extensions` | [`Integrations`](../../systems/integrations.md) |
|                                                         | `Tools` | [`Cache Management`](../../systems/cache-management.md)<br/>[`Index Management`](../../systems/index-management.md) |
|                                                         | `Support` | [`Data Collector`](../../systems/support.md#data-collector)<br/>[`System Report`](../../systems/support.md#system-reports) |
|                                                         | `Permissions` | [`All Users`](../../systems/permissions-users-all.md)<br/>[`Locked Users`](../../systems/permissions-users-all.md#locked-users)<br/>[`User Roles`](../../systems/permissions-user-roles.md) |
|                                                         | `Action Log` ![Adobe Commerce](../../assets/adobe-logo.svg) | [`Report`](../../systems/action-log.md)<br/>[`Archive`](../../systems/action-log-archive.md)<br/>[`Bulk Actions`](../../systems/action-log-bulk-actions.md) |
|                                                         | `Other Settings` | [`Notifications`](../../systems/notifications.md)<br/>[`Custom Variables`](../../systems/variables-custom.md)<br/>[`Manage Encryption Key`](../../systems/encryption-key.md) |
| `Find Partners & Extensions` |                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

{style="table-layout:auto"}

<!-- Feature still in development 
## [!UICONTROL Unified Experience]

![Store Configuration for Unified Experience](./assets/admin-uex-configuration.png)

The [!UICONTROL Unified Experience] option is available in Adobe Commerce deployments that have the Commerce Admin Unified Experience extension loaded. This extension enables integration with Experience Cloud to streamline cross-application workflows between Commerce and other Experience Cloud solutions. See [Adobe Experience Cloud Integration for Commerce Admin](../../getting-started/admin-unified-experience-integration-overview.md).

| Field        | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Description                                                                                                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Enable       | Global                                                                 | Determines if the Commerce instance uses the Experience Cloud integration. Before enabling this feature, review the [requirements and configuration instructions](../../getting-started/admin-unified-experience-integration-overview.md). Options: Yes/No.                                                                                                                    |
| Project Name | Global                                                                 | Identifies the instance in the Experience Cloud Commerce Projects workspace when the Unified Experience is enabled. The name can contain only alphanumeric characters and spaces. Defaults to the [cloud environment name](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-architecture.html?lang=en#pro-environment-architecture). |

{style="table-layout:auto"}

-->

## [!UICONTROL Admin Base URL]

![Admin - bas-URL](./assets/admin-admin-base-url.png)<!-- zoom -->

Mer information om hur du anger dessa alternativ finns i [Konfigurera bas-URL:en](../../stores-purchase/store-urls.md#configure-the-base-url) i _Butiks and Purchase Experience Guide_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|------------------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Use Custom Admin URL] | Global | Avgör om en anpassad URL används för att komma åt administratören. Alternativ: `Yes` / `No` |
| [!UICONTROL Custom Admin URL] | Global | Anger en anpassad URL för att komma åt administratören. Som standard är Admin-URL samma som bas-URL:en.<br/>**Viktigt:** Admin-URL:en måste finnas i samma Commerce-installation och ha samma dokumentrot som butiken. |
| [!UICONTROL Use Custom Admin Path] | Global | Avgör om en anpassad sökväg används för att komma åt administratören. Standardsökvägen är `admin`. Alternativ: `Yes` / `No` |
| [!UICONTROL Custom Admin Path] | Global | Ändrar namnet på administratörens standardsökväg till något svårt att gissa sig till. Ange namnet på den anpassade sökvägen med gemener. Till exempel: `aardvark` |

{style="table-layout:auto"}

## [!UICONTROL Security]

![Säkerhet](./assets/admin-security.png)<!-- zoom -->

Mer information om hur du anger dessa alternativ finns i [Konfigurera administratörssäkerhet](../../systems/security-admin.md) i _Handbok för adminsystem_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Admin Account Sharing] | Butiksvy | Avgör om en Admin-användare kan logga in på samma konto samtidigt från olika enheter. Alternativ: <br/>**`Yes`**- Tillåter flera aktiva sessioner från samma administratörskonto.<br/>**`No`** - Endast en aktiv session per administratörskonto tillåts. |
| [!UICONTROL Password Reset Protection Type] | Butiksvy | Bestämmer vilken metod som används för att hantera begäranden om återställning av lösenord. Alternativ: <br/>**`By IP and Email`**- Lösenordet kan återställas online när ett svar har tagits emot från meddelandet skickas till den e-postadress som är kopplad till administratörskontot.<br/>**`By IP`** - Lösenordet kan återställas online utan ytterligare bekräftelse. <br/>**`By Email`**- Lösenordet kan bara återställas genom att svara via e-post på meddelandet som skickas till den e-postadress som är kopplad till administratörskontot.<br/>**`None`** - Lösenordet kan bara återställas av butiksadministratören. |
| [!UICONTROL Recovery Link Expiration Period (hours)] | Global | Anger hur många timmar en länk för lösenordsåterställning ska vara giltig. |
| [!UICONTROL Max Number of Password Reset Requests] | Butiksvy | Anger det maximala antalet lösenordsbegäranden som kan skickas per timme. |
| [!UICONTROL Min Time Between Password Reset Requests] | Butiksvy | Anger det minsta antalet minuter mellan begäranden om återställning av lösenord. |
| [!UICONTROL Add Secret Key to URLs] | Global | När det här alternativet är aktiverat läggs en hemlig nyckel till i Admin-URL:en som en försiktighetsåtgärd mot att den utnyttjas. Alternativ: `Yes` / `No` |
| [!UICONTROL Login Is Case Sensitive] | Global | Avgör om inloggningsuppgifter som anges av en användare måste matcha de lagrade. Alternativ: `Yes` / `No` |
| [!UICONTROL Admin Session Lifetime (seconds)] | Global | Anger längden på en Admin-session i sekunder. |
| [!UICONTROL Maximum Login Failures to Lockout Account] | Global | Anger hur många gånger administratörsanvändare kan försöka logga in innan deras konton är låsta. Om fältet är tomt ställs ingen miniminivå in. Standardvärde: `6` |
| [!UICONTROL Lockout Time (minutes)] | Global | Anger hur många minuter ett administratörskonto är låst innan användaren kan försöka logga in igen. Standardvärde: `30` |
| [!UICONTROL Password Lifetime (days)] | Global | Anger antalet dagar innan ett administratörslösenord upphör att gälla. Om fältet är tomt ställs ingen livstid in. Standardvärde: `90` |
| [!UICONTROL Password Change] | Global | Avgör om administratörsanvändare måste ändra sina lösenord. Alternativ: <br/>**`Forced`**- Kräver att administratörsanvändare ändrar sina lösenord efter att kontot har konfigurerats.<br/>**`Recommended`** - Rekommenderar att administratörsanvändare ändrar sina lösenord efter att kontot har konfigurerats. |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![Kontrollpanel](./assets/admin-dashboard.png)<!-- zoom -->

Mer information om hur du anger dessa alternativ finns i [Kontrollpanel för administratörer](../../getting-started/admin-dashboard.md) i _Starthandbok_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|----------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Charts] | Global | Avgör om instrumentpanelen innehåller ett diagram som genererats från aktuella försäljningsdata. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Grids]

![Administratörsstödraster](./assets/admin-admin-grids.png)<!-- zoom -->

Mer information om hur du anger dessa alternativ finns i [Begränsa produktvisning](../../catalog/products-list.md#limit-product-display) i _Kataloghanteringsguide_.

>[!NOTE]
>
>För att förbättra prestanda för stora kataloger rekommenderar vi att du begränsar antalet produkter som visas i rutnätet.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|-----------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Limit Number of Products in Grid] | Global | Anger om antalet produkter som visas i rutnätet är begränsat till _[!UICONTROL Records Limit]_värde. Alternativ: `Yes` / `No` |
| [!UICONTROL Records Limit] | Global | Anger antalet produkter i produktrutnätet. Standardminimivärdet är `20000`. |

## [!UICONTROL CAPTCHA]

![CAPTCHA](./assets/admin-captcha.png)<!-- zoom -->

Mer information om hur du anger dessa alternativ finns i [CAPTCHA](../../systems/security-captcha.md) i _Handbok för adminsystem_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|-------------------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable CAPTCHA in Admin] | Global | Aktiverar CAPTCHA för administratörsinloggning. Alternativ: `Yes` / `No` |
| [!UICONTROL Font] | Global | Anger vilket teckensnitt som används för att visa CAPTCHA. Om du vill lägga till ett eget teckensnitt placerar du teckensnittsfilen i samma katalog som din Commerce-instans och lägger till deklarationen i filen config.xml på `app/code/Magento/Captcha/etc` Standardteckensnitt:` LinLibertine` |
| [!UICONTROL Forms] | Global | Bestämmer vilka formulär som CAPTCHA används i. Alternativ: `Admin Login` / `Admin Forgot Password` |
| [!UICONTROL Displaying Mode] | Global | Avgör när CAPTCHA visas. Alternativ: <br/>**`Always`**- CAPTCHA krävs alltid för att logga in.<br/>**`After number of attempts to login`** - Visar [!UICONTROL Number of Unsuccessful Attempts to Login] fält. Ange antalet tillåtna inloggningsförsök. Värdet 0 (noll) liknar inställningen för visningsläge till Alltid. Det här alternativet täcker inte formulären Glömt lösenord och Skapa användare. Om CAPTCHA är aktiverat och inställt på att visas, inkluderas det alltid i formuläret.<br />**Anteckning**: För att spåra antalet misslyckade inloggningsförsök räknas varje försök att logga in under en e-postadress och från en IP-adress. Det maximala antalet inloggningsförsök från samma IP-adress är 1 000. Den här begränsningen gäller bara när CAPTCHA är aktiverat. |
| [!UICONTROL Number of Unsuccessful Attempts to Login] | Global | Anger hur många gånger en person kan försöka logga in innan kontot är låst. För att spåra antalet misslyckade inloggningsförsök spåras försöken från en e-postadress från en enda IP-adress. Det maximala antalet försök från samma IP-adress är 1 000. Den här begränsningen gäller bara om CAPTCHA är aktiverat. |
| [!UICONTROL CAPTCHA Timeout (minutes)] | Global | Anger livslängden för aktuell CAPTCHA. När CAPTCHA förfaller måste användaren läsa in sidan igen. |
| [!UICONTROL Number of Symbols] | Global | Anger antalet symboler som används i CAPTCHA. Högsta tillåtna värde är `8`. Du kan också ange ett intervall, till exempel `5-8`. |
| [!UICONTROL Symbols Used in CAPTCHA] | Global | Avgör vilka symboler som används i CAPTCHA. Endast bokstäver (a-z och A-Z) och siffror (0-9) tillåts. Standarduppsättningen symboler som föreslås i fältet utesluter symboler som liknar varandra, som i, l eller 1. Om du visar dessa symboler i CAPTCHA minskar risken för att en användare känner igen CAPTCHA korrekt. |
| [!UICONTROL Case Sensitive] | Global | Avgör om tecknen som används i CAPTCHA är skiftlägeskänsliga. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Actions Logging]

{{ee-feature}}

![Loggning av administratörsåtgärder](./assets/admin-actions-logging.png)<!-- zoom -->

Mer information om hur du anger dessa alternativ finns i [Åtgärdsloggarkiv](../../systems/action-log-archive.md) i _Handbok för adminsystem_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|-----------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Actions] | Global | Aktiverar åtgärdsloggning för var och en av de valda åtgärderna: <br/>`Admin My Account` <br/>`Admin Permission Roles` <br/>`Admin Permission Users` <br/>`Admin Sign In` <br/>`CMS Blocks` <br/>`CMS Hierarchy` <br/>`CMS Pages` <br/>`Cache Management` <br/>`Cart Price Rules` <br/>`Catalog Attributes` <br/>`Catalog Categories` <br/>`Catalog Events` <br/>`Catalog Price Rules` <br/>`Catalog Product Tax Classes` <br/>`Catalog Product Templates` <br/>`Catalog Products` <br/>`Catalog Ratings` <br/>`Catalog Reviews` <br/>`Catalog Search` <br/>`Checkout Terms and Conditions` <br/>`Companies` <br/>`Company Credit` <br/>`Custom Variables` <br/>`Customer Groups` <br/>`Customer Invitations` <br/>`Customer Tax Classes` <br/>`Customers` <br/>`Design Configuration` <br/>`Gift Card Accounts` <br/>`Gift Registry Entity` <br/>`Gift Registry Type` <br/>`Index Management` <br/>`Login as a Customer` <br/>`Manage Currency Rates` <br/>`Manage Customer Address Attributes` <br/>`Manage Customer Attributes` <br/>`Manage Design` <br/>`Manage Dynamic Blocks` <br/>`Manage Segments` <br/>`Manage Store Views` <br/>`Manage Stores` <br/>`Manage Websites` <br/>`Negotiable Quotes` <br/>`Newsletter Queue` <br/>`Newsletter Subscribers` <br/>`Newsletter Templates` <br/>`PayPal Settlement Reports` <br/>`Reports` <br/> `Reward Points Rates` <br/>`Rule-Based Product Relations` <br/>`Sales Archive` <br/>`Sales Credit Memos` <br/>`Sales Invoices` <br/>`Sales Order Status` <br/>`Sales Orders` <br/>`Sales Shipments` <br/>`Shared Catalog` <br/>`Shopping Cart Management` <br/>`Store Credit` <br/>`System Backups` <br/>`System Configuration` <br/>`Tax Rates` <br/>`Tax Rules` <br/>`Transactional Emails` <br/>`URL Rewrites` <br/>`Widget` <br/>`XML Sitemap` |

{style="table-layout:auto"}

## [!UICONTROL Admin Usage]

![Administratörsanvändning](./assets/admin-usage.png)<!-- zoom -->

Mer information om hur du anger dessa alternativ finns i [Insamling av användningsdata](../../getting-started/admin.md#usage-data-collection) i _Starthandbok_.

| Fält | Omfång | Beskrivning |
|------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Admin Usage Tracking] | Global | Ger Adobe tillstånd att samla in administratörsinformation för att förbättra upplevelsen av att använda _Administratör_ och tillhörande produkter och tjänster. Genom att datainsamlingen tillåts kan du även _Produktvägledning_ som är utformat för att ge interaktivt innehåll som hjälp, funktionsbeskrivningar, guider, introduktionsinformation, funktionsmeddelanden med mera till _Administratör_. Enskilda administratörer identifieras inte i användningsdata. Alternativ:<br />**`Yes`**- Tillåter datainsamling och aktiverar _Produktvägledning_.<br />**`No`** - Tillåter inte datainsamling och aktiverar inte _Produktvägledning_. |

{style="table-layout:auto"}
