---
title: Betalningar - översikt
description: Läs om betalningsmetoder och -tjänster som stöds internt i Adobe Commerce och Magento Open Source.
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 0%

---

# Betalningar - översikt

Adobe Commerce och Magento Open Source stöder olika betalningsmetoder och tjänster som du kan erbjuda för enklare utcheckning och bekvämlighet. Denna lista innehåller flera offlinebetalningsmetoder, inklusive betalning med check eller penningorder samt postförskott. Det finns också inbyggda integreringar för flera onlinesödningar och gateways, inklusive Braintree som en paketutvecklad leverantörsutökning.

>[!TIP]
>
>Betalningstjänster för Adobe Commerce och Magento Open Source erbjuder en nyckelfärdig självbetjäningslösning, inklusive sandlådetestning och en enkel konfiguration, för stabil och säker betalningshantering. Om du vill veta mer om den här kraftfulla verktygsuppsättningen och hur den kan ge dig de insikter och den kontroll du behöver för att skapa den bästa upplevelsen för dina köpare kan du läsa [användarhandboken för betaltjänster](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html).

>[!NOTE]
>
>Granska [riktlinjerna för efterlevnad av PCI](../getting-started/compliance-pci.md) som beskriver de krav som ställs av betalkortsbranschen (PCI) för företag som accepterar betalning med kreditkort via internet.

## Ändringar i 2.4

Vissa betalningsintegreringar och programtillägg har tagits bort i version 2.4.x och flyttats till Commerce Marketplace. Du hittar de senaste officiella tilläggen för betalningsintegrering i [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}.

- **Amazon Pay** och **Klarna**: Adobe Commerce och Magento Open Source version 2.4.0 till 2.4.3 innehåller dessa tillägg som utvecklats av återförsäljare. Från och med version 2.4.4 paketeras dessa tillägg inte längre med kärnversionen och måste installeras och uppdateras från Commerce Marketplace. Marketplace ger också tillgång till aktuell dokumentation från tilläggsutvecklaren.

  Om du har aktiverat och konfigurerat något av de här paketerade tilläggen måste du uppdatera filen Composer.json som en del av uppgraderingsprocessen för 2.4.4 och hantera tilläggsuppdateringar framöver. Mer information finns i [Uppgraderingsmoduler](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) i _Uppgraderingshandboken_.

- **Worldplay**, **Eway**, **CyberSource** och **Authorize.Net**: Mer information om hur du gör en säker övergång från dessa betalningsintegreringar finns i [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}.

## Offlinebetalningsmetoder

Adobe Commerce och Magento Open Source innehåller flera inbyggda offlinebetalningsmetoder som inte kräver att ett tredjepartsföretag hanterar betalningar:

- [Noll delsumma, utcheckning](zero-subtotal-checkout.md)
- [Kontant vid leverans](cash-on-delivery.md)
- [Betalning av banköverföring](bank-transfer.md)
- [Check/penningorder](check-money-order.md)
- [Inköpsorder](purchase-order.md)
- [Betalning på konto](../b2b/enable-basic-features.md#configure-payment-on-account) ![Adobe Commerce B2B](../assets/b2b.svg) (tillgänglig med Adobe Commerce B2B)

## Betalningsmetoder online

Adobe Commerce och Magento Open Source har stöd för ett stort antal betallösningar som erbjuder handelstjänster i alla delar av världen. Till skillnad från betalningslösningar som överför kontrollen till en annan plats för att slutföra transaktionen, gör en betalningstjänst det möjligt för dig att acceptera kreditkortsbetalningar direkt från din butik utan att kunden behöver lämna din sajt.

### Rekommenderade lösningar

- [Betalningstjänster](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html)
- [PayPal Express-kassan](paypal-express-checkout.md)
- [Braintree](braintree.md)

### Andra PayPal-betalningslösningar

Mer information om betalningsmetoder för PayPal finns i [PayPal](paypal.md).

#### Allt-i-ett-PayPal-lösningar

- [Avancerade PayPal-betalningar](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal Payments Standard](paypal-payments-standard.md)

#### Betalningsgateways för PayPal

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [Länk till PayPal-betalningsflöde](paypal-payflow-link.md)

## Bedrägeriskydd

Tjänsterna för bedrägeriskydd och -filter undersöker skickade order innan transaktionen behandlas för att upptäcka bedrägliga order och skydda dig mot kostnader för avgiftsåterbetalning. Adobe Commerce och Magento Open Source stöder följande lösningar för skydd mot bedrägerier:

- [Bedrägerihanteringsfilter för PayPal](paypal.md#paypal-fraud-management-filters)

- [Skyddslösningar för bedrägeri på Marketplace][1]

>[!NOTE]
>
>För att ge stöd åt uppdateringar av säkerhetsefterlevnad har spärrskyddet för signerade bedrägerier tagits bort från Commerce från och med version 2.4.0. Om du har använt integreringen Signera i en version 2.3.x eller tidigare rekommenderar vi att du går över till tillägget [Signera bedrägeri och återbetalningsskydd](https://marketplace.magento.com/signifyd-module-connect.html){:target="_blank"}. Se till att du upprätthåller uppdateringar för tillägget enligt leverantörens riktlinjer.

## Felsökningsresurser

Hjälp om felsökning av betalningsproblem finns i [kunskapsbasen med supportfrågor](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html?lang=en).

[1]: https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection
