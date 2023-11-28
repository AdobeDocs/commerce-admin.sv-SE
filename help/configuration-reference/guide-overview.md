---
title: Referenshandbok för konfiguration
description: Granska beskrivande information för alla konfigurationsinställningar för Commerce Admin Store som är ordnade på konfigurationsflikar, sidor och avsnitt.
exl-id: b0359ba4-3643-4355-9154-adfedb369ec3
source-git-commit: 323ea635286fcb9a2bcc7f4f56b32c1518a7beef
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Referenshandbok för konfiguration

Handboken är avsedd för handlare och systemadministratörer som arbetar i Adobe Commerce eller Magento Open Source. Den innehåller referensinformation för alla butikskonfigurationsinställningar som du kommer åt via _Administratör_ sidebar på **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

Den innehåller inte information om funktionerna i Adobe Commerce och Magento Open Source eller om procedurer för butikskonfiguration.

Den här handboken är organiserad enligt den vänstra navigeringen i konfigurationen:

| Fliken Konfiguration | Underordnade flikar |
| ----------------- | ---------- |
| **[!UICONTROL General]** <br/><br/>The _[!UICONTROL General]_I konfigurationsavsnitten anges butiksparametrar, URL:er, tema, valuta, e-postadresser, butikskontakter, redigerare och instrumentpanelsrapport. | - [[!UICONTROL General]](./general/general.md)<br>- [[!UICONTROL B2B Features]](./general/b2b-features.md)<br>- [[!UICONTROL Web]](./general/web.md)<br>- [[!UICONTROL Currency Setup]](./general/currency-setup.md)<br>- [[!UICONTROL Store Email Addresses]](./general/store-email-addresses.md)<br>- [[!UICONTROL Contacts]](./general/contacts.md)<br>- [[!UICONTROL Reports]](./general/reports.md)<br>- [[!UICONTROL Content Management]](./general/content-management.md)<br>- [[!UICONTROL New Relic Reporting]](./general/new-relic-reporting.md)<br>- [[!UICONTROL Advanced Reporting]](./general/advanced-reporting.md) |
| **[!UICONTROL Catalog]** <br/><br/>The _[!UICONTROL Catalog]_konfigurationsinställningarna bestämmer produkt- och lagerinställningar, styr webbplatskartor och RSS-flöden och anger den e-postmall som används för att dela produkter med vänner. | - [[!UICONTROL Catalog]](./catalog/catalog.md)<br>- [[!UICONTROL Visual Merchandiser]](./catalog/visual-merchandiser.md)<br>- [[!UICONTROL Inventory]](./catalog/inventory.md)<br>- [[!UICONTROL XML Sitemap]](./catalog/xml-sitemap.md)<br>- [[!UICONTROL RSS Feeds]](./catalog/rss-feeds.md)<br>- [[!UICONTROL Email to a Friend]](./catalog/email-to-a-friend.md) |
| **[!UICONTROL Security]** <br/><br/>The _[!UICONTROL Security]_konfigurationsinställningarna styr arkivsäkerhet, tvåfaktorsautentisering och funktionen Google reCAPTCHA. | - [[!UICONTROL 2FA]](./security/2fa.md)<br>- [[!UICONTROL Google reCAPTCHA Admin Panel]](./security/google-recaptcha-admin.md)<br>- [[!UICONTROL Google reCAPTCHA Storefront]](./security/google-recaptcha-storefront.md)<br>- [[!UICONTROL Security.txt]](./security/security-txt.md) |
| **[!UICONTROL Customers]** <br/><br/>The _[!UICONTROL Customers]_konfigurationsinställningarna fastställer grundläggande kundkonto och inloggningsalternativ, nyhetsbrevsinställningar, önskelista och formatet för automatiskt genererade kupongkoder. | - [[!UICONTROL Login as Customer]](./customers/login-as-customer.md)<br>- [[!UICONTROL Newsletter]](./customers/newsletter.md)<br>- [[!UICONTROL Company Configuration]](./customers/company-configuration.md)<br>- [[!UICONTROL Customer Configuration]](./customers/customer-configuration.md)<br>- [[!UICONTROL Requisition Lists]](./customers/requisition-lists.md)<br>- [[!UICONTROL Wish List]](./customers/wishlist.md)<br>- [[!UICONTROL Invitations]](./customers/invitations.md)<br>- [[!UICONTROL Reward Points]](./customers/reward-points.md)<br>- [[!UICONTROL Promotions]](./customers/promotions.md)<br>- [[!UICONTROL Gift Registry]](./customers/gift-registry.md)<br>- [[!UICONTROL Persistent Shopping Cart]](./customers/persistent-shopping-cart.md) |
| **[!UICONTROL Sales]** <br/><br/>The _[!UICONTROL Sales]_konfigurationsinställningarna bestämmer utcheckning och skatteinställningar, betalnings- och leveransalternativ, utskrifter via e-post och PDF samt Google API-inställningar. | - [[!UICONTROL Sales]](./sales/sales.md)<br>- [[!UICONTROL Sales Emails]](./sales/sales-emails.md)<br>- [[!UICONTROL Quotes]](./sales/quotes.md)<br>- [[!UICONTROL PDF Print-outs]](./sales/pdf-print-outs.md)<br>- [[!UICONTROL Tax]](./sales/tax.md)<br>- [[!UICONTROL Checkout]](./sales/checkout.md)<br>- [[!UICONTROL Shipping Settings]](./sales/shipping-settings.md)<br>- [[!UICONTROL Multishipping Settings]](./sales/multishipping-settings.md)<br>- [[!UICONTROL Delivery Methods]](./sales/delivery-methods.md)<br>- [[!UICONTROL Google API]](./sales/google-api.md)<br>- [[!UICONTROL 3D Secure]](./sales/3d-secure.md)<br>- [[!UICONTROL Gift Cards]](./sales/gift-cards.md)<br>- [[!UICONTROL Payment Methods]](./sales/payment-methods.md) |
| **[!UICONTROL Sales Channels]** <br/><br/>När [!DNL Amazon Sales Channel] tillägget är installerat, _[!UICONTROL Sales Channels]_-inställningarna styr automatiserade integreringsåtgärder med din Amazon Store. | - [[!UICONTROL Global Settings]](sales-channels.md) |
| **[!UICONTROL Services]** <br/><br/>The _[!UICONTROL Services]_konfigurationsinställningarna bestämmer integreringsinställningarna för Commerce API, inklusive SOAP och OAuth. | - [[!UICONTROL Web API]](./services/magento-web-api.md)<br>- [[!UICONTROL Commerce Services]](./services/saas.md)<br>- [[!UICONTROL OAuth]](./services/oauth.md) |
| **[!UICONTROL Advanced]** <br/><br/>The _[!UICONTROL Advanced]_konfigurationsinställningarna bestämmer standardinställningar för administratörer, olika systemkonfigurationsinställningar, avancerade modulkontroller och utvecklingsverktyg. | - [[!UICONTROL Admin]](./advanced/admin.md)<br>- [[!UICONTROL System]](./advanced/system.md)<br>- [[!UICONTROL Developer]](./advanced/developer.md) |

{style="table-layout:auto"}

Den innehåller inte information om funktionerna i Adobe Commerce och Magento Open Source eller om procedurer för butikskonfiguration.

## Tillgänglig dokumentation

{{docs-links}}
