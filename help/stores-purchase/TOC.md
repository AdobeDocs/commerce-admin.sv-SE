---
user-guide-title: Butiks and Purchase Experience Guide
user-guide-description: Omfattande information för webbadministratörer, kundtjänstpersonal och säljchefer som arbetar i Adobe Commerce och Magento Open Source.
breadcrumb-title: Butiks- och inköpsupplevelser
role: Admin, User
feature: Storefront
recommendations: noDisplay
source-git-commit: 736cf0404983dbaee76bb46aa2d88a2becdc5f14
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---


# Butiks and Purchase Experience Guide {#stores-sales}

+ [Butiks and Purchase Experience Guide](guide-overview.md)
+ [Introduktion till butiker och inköpsupplevelser](introduction.md)
+ Hantering av webbplatser och butiker {#site-store}
   + [Menyn Lager](stores-menu.md)
   + [Lagring och webbplatsstruktur](stores.md)
   + [Butiksvyer](store-views.md)
   + [Lagringsplats](store-localize.md)
   + [Lagra URL:er](store-urls.md)
   + Skatter {#taxes}
      + [Ökning](taxes.md)
      + [Inställningar för momskonfiguration](tax-settings-general.md)
      + [Prisvisningsinställningar](display-settings.md)
      + [Skatteregler](tax-rules.md)
      + [Skatteklasser](tax-class.md)
      + [Fast produktskatt](fixed-product-tax.md)
      + [Dold momsberäkning](hidden-tax-calculation.md)
      + [Skattezoner och skattesatser](tax-zones-rates.md)
      + [Moms (moms)](vat.md)
      + [Skatteriktlinjer per land](international-tax-guidelines.md)
   + Valuta {#currency}
      + [Ökning](currency.md)
      + [Valutakonfiguration](currency-configuration.md)
      + [Uppdatera valutakurser](currency-update.md)
   + [E-post](sales-email.md)
   + [Försäljningsdokument](sales-documents.md)
+ Inköpsplats {#point-of-purchase}
   + [Omedelbart köp](checkout-instant-purchase.md)
   + Kundvagn {#cart}
      + [Ökning](cart.md)
      + [Kundkonfiguration](cart-configuration.md)
      + [Kartbeständighet](cart-persistent.md)
      + [Beställa efter SKU](order-by-sku.md)
   + Shoppingassistans {#assist}
      + [Hantera en kundvagn](shopping-assisted-cart-manage.md)
      + [Skapa en order](customer-account-create-order.md)
      + [Uppdatera en kundorder](order-update.md)
   + Utcheckning {#checkout}
      + [Ökning](checkout-process.md)
      + [Ensidig utcheckning](checkout-one-page.md)
      + [Kassa på gäst](checkout-guest.md)
      + [Villkor](terms-and-conditions.md)
      + [Adresssökning](checkout-address-search.md)
      + [Meddelande om misslyckade betalningar](checkout-payment-failed-emails.md)
      + [Sorteringsordning för utcheckningssummor](checkout-totals-sort-order.md)
   + Presentkort {#gift-cards}
      + [Köp och inlösen av presentkort](product-gift-card-workflow.md)
      + [Presentkortskonton](product-gift-card-accounts.md)
+ Shopparverktyg {#shopper-tools}
   + [Skicka e-post till en vän](email-a-friend.md)
   + Önsklistorna {#wish-lists}
      + [Ökning](wishlists.md)
      + [Konfigurera önskelistor](wishlist-configuration.md)
      + [Önska butiksupplevelsen](wishlist-storefront.md)
   + [Jämför produkter](product-compare.md)
   + [Nyligen visade eller jämförda](products-viewed-compared.md)
   + [Tillåt ombeställningar](reorders-allow.md)
   + [Tillåt annulleringsorder](cancel-allow.md)
+ Betalningar {#payments}
   + [Ökning](payments.md)
   + Betalningslösningar för PayPal {#paypal}
      + [Översikt över PayPal-lösningar](paypal.md)
      + [PayPal Express-kassan](paypal-express-checkout.md)
      + [Avancerade PayPal-betalningar](paypal-payments-advanced.md)
      + [PayPal Payments Pro](paypal-payments-pro.md)
      + [PayPal Payments Standard](paypal-payments-standard.md)
      + [PayPal Payflow Pro](paypal-payflow-pro.md)
      + [Länk till PayPal-betalningsflöde](paypal-payflow-link.md)
      + [PayPal-faktureringsavtal](paypal-billing-agreements.md)
      + [PayPal-kvittningsrapporter](paypal-settlement-reports.md)
   + [Braintree](braintree.md)
   + [Lagrade betalningsmetoder](stored-payment-methods.md)
   + Offlinebetalningsmetoder {#offline}
      + [Checkar och betalningsorder](check-money-order.md)
      + [Kontant vid leverans](cash-on-delivery.md)
      + [Banköverföringar](bank-transfer.md)
      + [Inköpsorder](purchase-order.md)
      + [Ingen deltotal utcheckning](zero-subtotal-checkout.md)
+ Hantera orderflöde {#order-management}
   + [Försäljningsmeny](sales-menu.md)
   + Beställningar {#orders}
      + [Ökning](orders.md)
      + [Arbetsflöde och bearbetning](order-processing.md)
      + [Leverera en beställning](order-ship.md)
      + [Orderstatus](order-status.md)
      + [Schemalagda orderåtgärder](order-scheduled-operations.md)
      + [Arkivera order](order-archive.md)
      + [Beställningshantering i lager](orders-storefront.md)
   + [Fakturor](invoices.md)
   + [Leveranser](shipments.md)
   + Kreditnotor {#credit-memos}
      + [Ökning](credit-memos.md)
      + [Utfärda en kreditnota](credit-memo-create.md)
   + Returnerar {#returns}
      + [Ökning](returns.md)
      + [Konfigurera returer](rma-configure.md)
      + [Returnera attribut](attributes-returns.md)
      + [Returnerar butiksupplevelsen](rma-customer-experience.md)
   + [Transaktioner](transactions.md)
+ Leverans {#delivery}
   + [Ökning](delivery.md)
   + [Leveransinställningar](shipping-settings.md)
   + Grundläggande leveransmetoder {#basic-methods}
      + [Fri frakt](shipping-free.md)
      + [Schablonbelopp](shipping-flat-rate.md)
      + [Registersatser](shipping-table-rate.md)
      + [Leverans i butik](shipping-in-store-delivery.md)
   + Transportföretag {#shipping-carriers}
      + [Inställningar för fraktfirma](carriers.md)
      + [UPS](ups.md)
      + [USPS](usps.md)
      + [FedEx](fedex.md)
      + [DHL](dhl.md)
   + Leveransetiketter {#shipping-labels}
      + [Översikt över leveransetikett](shipping-labels.md)
      + [Konfigurera etiketter för leverans](shipping-label-configure.md)
      + [Skapa leveransetiketter](shipping-label-create.md)
+ [Återgå till administratörens användarhandböcker](https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=sv-SE)
