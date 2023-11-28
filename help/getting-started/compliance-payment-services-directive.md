---
title: PSD2-kompatibilitet
description: Läs mer om kraven i direktivet om betaltjänster (PSD2) som kan påverka din butik.
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 0%

---

# PSD2-kompatibilitet

Från och med den 14 september 2019 kräver EU att alla handlare i EU och Storbritannien uppfyller kraven i [Stark kundautentisering](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) (SCA) kraven i direktivet om betaltjänster (PSD2). Handelsföretag i alla andra länder uppmuntras att följa PSD2 som en god praxis.

>[!NOTE]
>
>Detta ämne är avsett endast i informationssyfte och ska inte tolkas som juridisk rådgivning. Om du vill ta reda på om och hur ditt företag ska uppfylla några juridiska skyldigheter kontaktar du ditt juridiska ombud.

Stark kundautentisering är en nyckelkomponent i PSD2 och kräver två av följande:

- Något som bara kunden har (lösenord eller PIN-kod)
- Något som bara kunden känner till (unik säkerhetstoken som genereras via telefon eller nyckelfob)
- Något som bara kunden är (biometrisk autentisering som fingeravtryck eller ansiktsigenkänning)

Europeiska banker får neka betalningar som inte uppfyller kraven. Lågrisk- och lågvärdestransaktioner kan dock fortfarande accepteras, och efterföljande betalningar i en återkommande prenumeration.

På grund av denna stora förändring och för att säkerställa att kundbetalningarna inte minskar har Adobe infört följande ändringar och rekommendationer för [!DNL Commerce] betalningsintegrationer.

| Betalningssätt | Efterlevnadskrav |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | För de flesta PayPal-lösningar krävs ingen åtgärd för att uppfylla PSD 2, eftersom kraven hanteras av PayPal. Information om specifika lösningar finns i anteckningen överst i varje PayPal-avsnitt. |
| [Braintree](../stores-purchase/braintree.md) | Från och med övergången till det installerade tillägget i 2.4.0 hanteras kraven i den medföljande betalningsmodulen Braintree och inga åtgärder krävs för att uppfylla PSD 2. <br /><br />**_Obs!_**Gör något av följande om du vill följa PSD 2 med integreringen i tidigare versioner:<br/>- (Rekommenderas) Installera det officiella Braintree-tillägget för betalningsintegration från [[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&amp;idx=m2_cloud_prod_default_products&amp;p=0&amp;nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1){:target=&quot;_blank&quot;}.<br/>- Aktivera och konfigurera betalningsmetoden Braintree i [!DNL Commerce] konfiguration.<br/><br/>Dessa tidigare kärnintegreringar stöder 3D Secure 2.0-verifiering. Implementeringar av Braintree som körs på JavaScript SDK v2 har dock inte stöd för 3D Secure 2.0. |
| Övriga | För alla andra betalningsintegreringar ska du kontrollera tillgängliga tillägg för [[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target=&quot;_blank&quot;}. Be din betalningsleverantör att rekommendera en lösning som stöder kraven för PSD2. |

{style="table-layout:auto"}
