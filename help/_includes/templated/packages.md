---
source-git-commit: a37e67c332140fbba7609db8cc5e22a3625a1c9d
workflow-type: tm+mt
source-wordcount: '2387'
ht-degree: 0%

---
# Adobe Commerce med B2B-paket

<!-- The 'packages' variable contains the 'packages' node of the '_data/codebase/b2b/composer_lock.json' file
 -->

<!-- The 'packages-dev' variable contains the 'packages-dev' node of the '_data/codebase/b2b/composer_lock.json' file
 -->

<!-- The 'product' variable contains data of the 'magento/product-enterprise-edition' package
 -->

<!-- The edition variable contains `commerce-b2b` value from the _data/names.yml file
 -->

Adobe Commerce B2B använder Composer för att hantera PHP-paket.

Filen `composer.json` deklarerar paketlistan medan filen `composer.lock` lagrar en fullständig lista över de paket (en fullständig version av varje paket och dess beroenden) som används för att skapa en installation av Adobe Commerce B2B.

Följande referensdokumentation genereras från filen `composer.lock` och omfattar obligatoriska paket som ingår i Adobe Commerce B2B 1.5.2.

## Beroenden

`magento/extension-b2b 1.5.2` har följande beroenden:

- magento/framework: >=103.0.6 &lt;103.0.9
- magento/magento2-b2b-base: 1.5.2
- [magento/module-b2b](https://developer.adobe.com/commerce/php/module-reference/module-b2b/): 100.5.2
- [magento/module-bundle-runable-quote](https://developer.adobe.com/commerce/php/module-reference/module-bundle-negotiable-quote/): 100.5.1
- [magento/module-bundle-reksition-list](https://developer.adobe.com/commerce/php/module-reference/module-bundle-requisition-list/): 100.5.1
- [magento/module-bundle-reksition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-bundle-requisition-list-graph-ql/): 1.5.1
- [magento/module-bundle-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-bundle-shared-catalog/): 100.5.1
- [magento/module-checkout-address-search-förhandlable-quote](https://developer.adobe.com/commerce/php/module-reference/module-checkout-address-search-negotiable-quote/): 100.5.1
- [magento/module-checkout-agreements-runable-quote](https://developer.adobe.com/commerce/php/module-reference/module-checkout-agreements-negotiable-quote/): 100.5.1
- [magento/module-checkout-agreements-purchase-order](https://developer.adobe.com/commerce/php/module-reference/module-checkout-agreements-purchase-order/): 1.5.1
- [magento/module-company](https://developer.adobe.com/commerce/php/module-reference/module-company/): 102.0.2
- [magento/module-company-asynchronous-operations](https://developer.adobe.com/commerce/php/module-reference/module-company-asynchronous-operations/): 1.5.1
- [magento/module-company-credit](https://developer.adobe.com/commerce/php/module-reference/module-company-credit/): 100.5.2
- [magento/module-company-credit-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-company-credit-graph-ql/): 1.5.1
- [magento/module-company-customer-import-export](https://developer.adobe.com/commerce/php/module-reference/module-company-customer-import-export/): 1.5.0
- [magento/module-company-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-company-graph-ql/): 1.5.2
- [magento/module-company-runable-quote](https://developer.adobe.com/commerce/php/module-reference/module-company-negotiable-quote/): 1.5.1
- [magento/module-company-runable-quote-template](https://developer.adobe.com/commerce/php/module-reference/module-company-negotiable-quote-template/): 1.5.1
- [magento/module-company-payment](https://developer.adobe.com/commerce/php/module-reference/module-company-payment/): 100.5.1
- [magento/module-company-quote](https://developer.adobe.com/commerce/php/module-reference/module-company-quote/): 1.5.2
- [magento/module-company-quote-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-company-quote-graph-ql/): 1.5.2
- [magento/module-company-relation](https://developer.adobe.com/commerce/php/module-reference/module-company-relation/): 1.5.2
- [magento/module-company-relation-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-company-relation-shared-catalog/): 1.5.1
- [magento/module-company-shipping](https://developer.adobe.com/commerce/php/module-reference/module-company-shipping/): 1.5.1
- [magento/module-configurable-runable-quote](https://developer.adobe.com/commerce/php/module-reference/module-configurable-negotiable-quote/): 100.5.1
- [magento/module-configurable-rekvisisition-list](https://developer.adobe.com/commerce/php/module-reference/module-configurable-requisition-list/): 100.5.1
- [magento/module-configurable-reksition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-configurable-requisition-list-graph-ql/): 1.5.1
- [magento/module-configurable-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-configurable-shared-catalog/): 100.5.1
- [magento/module-downloadable-company](https://developer.adobe.com/commerce/php/module-reference/module-downloadable-company/): 1.5.1
- [magento/module-downloadable-reksition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-downloadable-requisition-list-graph-ql/): 1.5.1
- [magento/module-present-card-runable-quote](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-negotiable-quote/): 100.5.1
- [magento/module-present-card-rekvisisition-list](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-requisition-list/): 100.5.1
- [magento/module-present-card-reksition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-requisition-list-graph-ql/): 1.5.1
- [magento/module-present-card-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-shared-catalog/): 100.5.1
- [magento/module-grouped-reksition-list](https://developer.adobe.com/commerce/php/module-reference/module-grouped-requisition-list/): 100.5.1
- [magento/module-grouped-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-grouped-shared-catalog/): 100.5.1
- [magento/module-runable-quote](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote/): 101.0.2
- [magento/module-runable-quote-async-order](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-async-order/): 1.5.1
- [magento/module-runable-quote-duplicate](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-duplicate/): 1.5.2
- [magento/module-runable-quote-duplicate-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-duplicate-graph-ql/): 1.5.1
- [magento/module-runable-quote-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-graph-ql/): 1.5.1
- [magento/module-runable-quote-rekvisisition-list](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-requisition-list/): 1.5.1
- [magento/module-runable-quote-rekvisisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-requisition-list-graph-ql/): 1.5.1
- [magento/module-runable-quote-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-shared-catalog/): 100.5.1
- [magento/module-runable-quote-template](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template/): 1.5.2
- [magento/module-runable-quote-template-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template-graph-ql/): 1.5.2
- [magento/module-runable-quote-template-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template-shared-catalog/): 1.5.1
- [magento/module-runable-quote-weee](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-weee/): 100.5.1
- [magento/module-order-history-search](https://developer.adobe.com/commerce/php/module-reference/module-order-history-search/): 100.5.2
- [magento/module-paypal-runable-quote](https://developer.adobe.com/commerce/php/module-reference/module-paypal-negotiable-quote/): 1.5.1
- [magento/module-paypal-purchase-order](https://developer.adobe.com/commerce/php/module-reference/module-paypal-purchase-order/): 1.5.1
- [magento/module-purchase-order](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order/): 100.5.2
- [magento/module-purchase-order-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-graph-ql/): 1.5.1
- [magento/module-purchase-order-rule](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-rule/): 100.5.2
- [magento/module-purchase-order-rule-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-rule-graph-ql/): 1.5.1
- [magento/module-quick-order](https://developer.adobe.com/commerce/php/module-reference/module-quick-order/): 100.5.1
- [magento/module-quick-order-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-quick-order-graph-ql/): 1.5.1
- [magento/module-rekvisisition-list](https://developer.adobe.com/commerce/php/module-reference/module-requisition-list/): 100.5.2
- [magento/module-rekvisisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-requisition-list-graph-ql/): 1.5.1
- [magento/module-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-shared-catalog/): 100.5.2
- [magento/module-shared-catalog-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-shared-catalog-graph-ql/): 1.5.1
- magento/security-package-b2b: 1.0.6

## Tredjepartslicenser

### Apache-2.0, LGPL-2.1-only

<table>
  <thead>
    <tr>
      <th>Namn</th>
      <th>Typ</th>
      <th>Beskrivning</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/opensearch-project/opensearch-php">opensearch-project/opensearch-php</a>
    </td>
    <td>Bibliotek</td>
    <td>PHP-klient för OpenSearch</td>
  </tr>
  </tbody>
</table>

### Apache-2.0

<table>
  <thead>
    <tr>
      <th>Namn</th>
      <th>Typ</th>
      <th>Beskrivning</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/adobe/stock-api-libphp">astock/stock-api-libphp</a>
    </td>
    <td>Bibliotek</td>
    <td>Adobe Stock API-bibliotek</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/awslabs/aws-crt-php">aws/aws-crt-php</a>
    </td>
    <td>Bibliotek</td>
    <td>AWS Common Runtime for PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/aws/aws-sdk-php">aws/aws-sdk-php</a>
    </td>
    <td>Bibliotek</td>
    <td>AWS SDK for PHP - Använd Amazon Web Services i PHP-projekt</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/opentelemetry-php/api">open-telemetry/api</a>
    </td>
    <td>Bibliotek</td>
    <td>API för OpenTelemetry PHP.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/opentelemetry-php/context">open-telemetry/context</a>
    </td>
    <td>Bibliotek</td>
    <td>Context implementation for OpenTelemetry PHP.</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree
    </td>
    <td>Metapackage</td>
    <td>Braintree Magento</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/wikimedia/less.php">wikimedia/less.php</a>
    </td>
    <td>Bibliotek</td>
    <td>PHP-port för LESS-processor</td>
  </tr>
  </tbody>
</table>

### BSD-2-klausul

<table>
  <thead>
    <tr>
      <th>Namn</th>
      <th>Typ</th>
      <th>Beskrivning</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/Bacon/BaconQrCode">bacon/bacon-qr-code</a>
    </td>
    <td>Bibliotek</td>
    <td>BaconQrCode är en QR-kodgenerator för PHP.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/DASPRiD/Enum">dasprid/enum</a>
    </td>
    <td>Bibliotek</td>
    <td>PHP 7.1 enum implementation</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/webimpress/safe-writer">webimpress/safe-writer</a>
    </td>
    <td>Bibliotek</td>
    <td>Verktyg för att skriva filer på ett säkert sätt, för att undvika konkurrensförhållanden</td>
  </tr>
  </tbody>
</table>

### BSD-3-klausul

<table>
  <thead>
    <tr>
      <th>Namn</th>
      <th>Typ</th>
      <th>Beskrivning</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/Cm_Cache_Backend_File">colinMovie/cache-backend-file</a>
    </td>
    <td>Magento-modul</td>
    <td>Zend_Cache_Backend_File-serverdelen har mycket dålig prestanda för att rensa med taggar, vilket gör den oanvändbar när antalet cachelagrade objekt ökar. Den här serverdelen gör många ändringar, vilket ger en rejäl prestandaökning, särskilt för tagghantering.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/php-redis-session-abstract">colinblöenhour/php-redis-session-abstract</a>
    </td>
    <td>Bibliotek</td>
    <td>En Redis-baserad sessionshanterare med optimistisk låsning</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/duosecurity/duo_universal_php">duosecurity/duo_universal_php</a>
    </td>
    <td>Bibliotek</td>
    <td>En PHP-implementering av Duo Universal SDK.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/firebase/php-jwt">firebase/php-jwt</a>
    </td>
    <td>Bibliotek</td>
    <td>Ett enkelt bibliotek för kodning och avkodning av JSON Web Tokens (JWT) i PHP. Ska överensstämma med den aktuella specifikationen.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-captcha">laminas/laminas-captcha</a>
    </td>
    <td>Bibliotek</td>
    <td>Generera och validera CAPTCHA med Figlets, images, ReCaptcha med flera</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-code">laminas/laminas-code</a>
    </td>
    <td>Bibliotek</td>
    <td>Tillägg till API:t för PHP-reflektion, statisk kodskanning och kodgenerering</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-config">laminas/laminas-config</a>
    </td>
    <td>Bibliotek</td>
    <td>innehåller ett kapslat objektegenskapsbaserat användargränssnitt för åtkomst av konfigurationsdata i programkoden</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-di">laminas/laminas-di</a>
    </td>
    <td>Bibliotek</td>
    <td>Automatisk beroendeinjektion för PSR-11-behållare</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-escaper">laminas/laminas-escape</a>
    </td>
    <td>Bibliotek</td>
    <td>Undvik säkert HTML, HTML-attribut, JavaScript, CSS och URL:er</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-eventmanager">laminas/laminas-eventManager</a>
    </td>
    <td>Bibliotek</td>
    <td>Utlös och lyssna på händelser i ett PHP-program</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-feed">laminas/laminas-feed</a>
    </td>
    <td>Bibliotek</td>
    <td>innehåller funktioner för att skapa och använda RSS- och Atom-flöden</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-filter">laminas/laminas-filter</a>
    </td>
    <td>Bibliotek</td>
    <td>Filtrera och normalisera data och filer programmatiskt</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-http">laminas/laminas-http</a>
    </td>
    <td>Bibliotek</td>
    <td>Ger ett enkelt gränssnitt för att utföra HTTP-begäranden (Hyper-Text Transfer Protocol)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-i18n">laminas/laminas-i18n</a>
    </td>
    <td>Bibliotek</td>
    <td>Ange översättningar för programmet och filtrera och validera internationella värden</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-json">laminas/laminas-json</a>
    </td>
    <td>Bibliotek</td>
    <td>erbjuder bekväma metoder för att serialisera inbyggda PHP till JSON och avkoda JSON till inbyggda PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-loader">laminas/laminas-loader</a>
    </td>
    <td>Bibliotek</td>
    <td>Inläsningsstrategier för automatisk inläsning och plugin-program</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-modulemanager">laminas/laminas-modulemanager</a>
    </td>
    <td>Bibliotek</td>
    <td>Modulärt programsystem för laminas-mvc-program</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-mvc">laminas/laminas-mvc</a>
    </td>
    <td>Bibliotek</td>
    <td>Laminas händelsestyrda MVC-lager, inklusive MVC-program, styrenheter och plugin-program</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-permissions-acl">laminas/laminas-permissions-acl</a>
    </td>
    <td>Bibliotek</td>
    <td>Tillhandahåller en enkel och flexibel ACL-implementering (access control list) för behörighetshantering</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-recaptcha">laminas/laminas-recaptcha</a>
    </td>
    <td>Bibliotek</td>
    <td>OOP-wrapper för ReCaptcha-webbtjänsten</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-router">laminas/laminas-router</a>
    </td>
    <td>Bibliotek</td>
    <td>Flexibelt routningssystem för HTTP- och konsolapplikationer</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-server">laminas/laminas-server</a>
    </td>
    <td>Bibliotek</td>
    <td>Skapa reflektionsbaserade RPC-servrar</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-servicemanager">laminas/laminas-servicemanager</a>
    </td>
    <td>Bibliotek</td>
    <td>Behållare för fabriksstyrd beroendeinjektion</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-session">laminas/laminas-session</a>
    </td>
    <td>Bibliotek</td>
    <td>Objektorienterat gränssnitt för PHP-sessioner och -lagring</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-soap">laminas/laminas-soap</a>
    </td>
    <td>Bibliotek</td>
    <td></td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-stdlib">laminas/laminas-stdlib</a>
    </td>
    <td>Bibliotek</td>
    <td>SPL-tillägg, matrisverktyg, felhanterare med mera</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-text">laminas/laminas-text</a>
    </td>
    <td>Bibliotek</td>
    <td>Skapa FIGlets och textbaserade tabeller</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-translator">laminas/laminas-translator</a>
    </td>
    <td>Bibliotek</td>
    <td>Gränssnitt för Translator-komponenten av laminas-i18n</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-uri">laminas/laminas-uri</a>
    </td>
    <td>Bibliotek</td>
    <td>En komponent som underlättar manipulering och validering av URI (Uniform Resource Identifiers)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-validator">laminas/laminas-validator</a>
    </td>
    <td>Bibliotek</td>
    <td>Valideringsklasser för ett stort antal domäner och möjlighet att kedja validerare för att skapa komplexa valideringskriterier</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-view">laminas/laminas-view</a>
    </td>
    <td>Bibliotek</td>
    <td>Flexibla visningslager med stöd för flera visningslager, stödfunktioner med mera</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/marc-mabe/php-enum">marc-mabe/php-enum</a>
    </td>
    <td>Bibliotek</td>
    <td>Enkel och snabb implementering av uppräkningar med inbyggd PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/nikic/PHP-Parser">nikic/php-parser</a>
    </td>
    <td>Bibliotek</td>
    <td>En PHP-parser skriven i PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpfui/recaptcha">phpfui/recaptcha</a>
    </td>
    <td>Bibliotek</td>
    <td>Klientbibliotek för Google reCAPTCHA för PHP 8.4 och senare</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/tedious/JShrink">tedivm/jkrink</a>
    </td>
    <td>Bibliotek</td>
    <td>Javascript-minifier inbyggd i PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/tubalmartin/YUI-CSS-compressor-PHP-port">tubalmartin/cssmin</a>
    </td>
    <td>Bibliotek</td>
    <td>En PHP-port för YUI CSS-komprimeraren</td>
  </tr>
  </tbody>
</table>

### BSD-3-Clause-Modification

<table>
  <thead>
    <tr>
      <th>Namn</th>
      <th>Typ</th>
      <th>Beskrivning</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/Cm_Cache_Backend_Redis">colinkvart/hour/cache-backend-redis</a>
    </td>
    <td>Magento-modul</td>
    <td>Zend_Cache backend använder Redis med fullständigt stöd för taggar.</td>
  </tr>
  </tbody>
</table>

### ISC

<table>
  <thead>
    <tr>
      <th>Namn</th>
      <th>Typ</th>
      <th>Beskrivning</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/paragonie/sodium_compat">paragonie/natrium_compat</a>
    </td>
    <td>Bibliotek</td>
    <td>Ren PHP-implementering av libnatrium; använder PHP-tillägget om det finns</td>
  </tr>
  </tbody>
</table>

### LGPL-2.1-eller-senare

<table>
  <thead>
    <tr>
      <th>Namn</th>
      <th>Typ</th>
      <th>Beskrivning</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/ezyang/htmlpurifier">ezyang/htmlpurifier</a>
    </td>
    <td>Bibliotek</td>
    <td>Standardkompatibelt HTML-filter som skrivits i PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-amqplib/php-amqplib">php-amqplib/php-amqplib</a>
    </td>
    <td>Bibliotek</td>
    <td>Tidigare videlalvaro/php-amqplib.  Det här biblioteket är en ren PHP-implementering av AMQP-protokollet. Den har testats mot RabbitMQ.</td>
  </tr>
  </tbody>
</table>

### MIT

<table>
  <thead>
    <tr>
      <th>Namn</th>
      <th>Typ</th>
      <th>Beskrivning</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/braintree/braintree_php">braintree/braintree_php</a>
    </td>
    <td>Bibliotek</td>
    <td>Braintree PHP Client Library</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/brick/math">brick/math</a>
    </td>
    <td>Bibliotek</td>
    <td>Arbitrary-precision aritmetic library</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/brick/varexporter">brick/varexporter</a>
    </td>
    <td>Bibliotek</td>
    <td>Ett kraftfullt alternativ till var_export(), som kan exportera stängningar och objekt utan __set_state()</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ChristianRiesen/base32">Christian-riesen/base32</a>
    </td>
    <td>Bibliotek</td>
    <td>Base32-kodare/avkodare enligt RFC 4648</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/credis">colinblöenhour/credis</a>
    </td>
    <td>Bibliotek</td>
    <td>Credis är ett lättviktsgränssnitt för Redis nyckelvärdenhet som omsluter phpredis-biblioteket när det är tillgängligt för bättre prestanda.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/ca-bundle">disposition/ca-bundle</a>
    </td>
    <td>Bibliotek</td>
    <td>Gör att du kan hitta en sökväg till systemets CA-paket och inkluderar en reservanslutning till Mozilla CA-paketet.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/class-map-generator">dispositör/klass-map-generator</a>
    </td>
    <td>Bibliotek</td>
    <td>Verktyg för att skanna PHP-kod och generera klasskartor.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/composer">disposition/disposition</a>
    </td>
    <td>Bibliotek</td>
    <td>Composer hjälper dig att deklarera, hantera och installera beroenden av PHP-projekt. Det ser till att du har rätt hög överallt.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/metadata-minifier">disposition/metadata-minifier</a>
    </td>
    <td>Bibliotek</td>
    <td>Liten verktygsbibliotek som hanterar miniatyrbilder och utbyggnad av metadata.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/pcre">disposition/pcre</a>
    </td>
    <td>Bibliotek</td>
    <td>PCRE-paketeringsbibliotek som erbjuder typsäkra preg_*-ersättningar.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/semver">disposition/server</a>
    </td>
    <td>Bibliotek</td>
    <td>Semversionsbibliotek som erbjuder verktyg, versionskontrollerad tolkning och validering.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/spdx-licenses">Composer/spdx-licenses</a>
    </td>
    <td>Bibliotek</td>
    <td>SPDX-licenslista och valideringsbibliotek.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/xdebug-handler">dispositör/xdebug-handler</a>
    </td>
    <td>Bibliotek</td>
    <td>Startar om en process utan Xdebug.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/doctrine/lexer">doctrine/lexer</a>
    </td>
    <td>Bibliotek</td>
    <td>PHP Doctrine Lexer-parserbibliotek som kan användas i uppifrån och ned, rekursiva fallparametrar.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/egulias/EmailValidator">egulias/email-validator</a>
    </td>
    <td>Bibliotek</td>
    <td>Ett bibliotek för validering av e-post mot flera RFC:er</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/elastic/elastic-transport-php">elastisk/transport</a>
    </td>
    <td>Bibliotek</td>
    <td>PHP-bibliotek för HTTP-transport för elastiska produkter</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/elastic/elasticsearch-php">elasticsearch/elasticsearch</a>
    </td>
    <td>Bibliotek</td>
    <td>PHP-klient för Elasticsearch</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/endroid/qr-code">endroid/qr-code</a>
    </td>
    <td>Bibliotek</td>
    <td>Endroid QR-kod</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ezimuel/guzzlestreams">ezimuel/guzzlestreams</a>
    </td>
    <td>Bibliotek</td>
    <td>Gbit guzzle/streams (övergiven) som ska användas med elasticsearch-php</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ezimuel/ringphp">ezimuel/ringphp</a>
    </td>
    <td>Bibliotek</td>
    <td>Gummigaffel/RingPHP (övergiven) som ska användas med elasticsearch-php</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/guzzle">guzzlehttp/guzzle</a>
    </td>
    <td>Bibliotek</td>
    <td>Guzzle är ett PHP HTTP-klientbibliotek</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/promises">guzzlehttp/promise</a>
    </td>
    <td>Bibliotek</td>
    <td>Bibliotek med löften om pussel</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/psr7">guzzlehttp/psr7</a>
    </td>
    <td>Bibliotek</td>
    <td>Implementering av PSR-7-meddelanden som även innehåller vanliga verktygsmetoder</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/jsonrainbow/json-schema">justinrainbow/json-schema</a>
    </td>
    <td>Bibliotek</td>
    <td>Ett bibliotek som validerar ett json-schema.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem">Lag/flygsystem</a>
    </td>
    <td>Bibliotek</td>
    <td>Filarkiveringssammanfattning för PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem-aws-s3-v3">leag/flysystem-aws-s3-v3</a>
    </td>
    <td>Bibliotek</td>
    <td>AWS S3-filsystemadapter för flygsystem.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem-local">Lag/flysystem-local</a>
    </td>
    <td>Bibliotek</td>
    <td>Lokal filsystemadapter för flygsystemet.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/mime-type-detection">Identifiering av ligg/mime-typ</a>
    </td>
    <td>Bibliotek</td>
    <td>Mime-type detection for Flysystem</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/monolog">monolog/monolog</a>
    </td>
    <td>Bibliotek</td>
    <td>Skickar loggarna till filer, socketar, inkorgar, databaser och olika webbtjänster</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/jmespath/jmespath.php">mtdowling/jmespath.php</a>
    </td>
    <td>Bibliotek</td>
    <td>Ange deklarativt hur element ska extraheras från ett JSON-dokument</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/paragonie/constant_time_encoding">paragonie/constant_time_encoding</a>
    </td>
    <td>Bibliotek</td>
    <td>Konstanta implementeringar av RFC 4648-kodning (Base-64, Base-32, Base-16)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/paragonie/random_compat">paragonie/random_compat</a>
    </td>
    <td>Bibliotek</td>
    <td>PHP 5.x-polyfill för random_bytes() och random_int() från PHP 7</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/MyIntervals/emogrifier">pelago/emogrifier</a>
    </td>
    <td>Bibliotek</td>
    <td>Konverterar CSS-format till infogade formatattribut i din HTML-kod</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/discovery">php-http/discovery</a>
    </td>
    <td>Composer-plugin</td>
    <td>Söker efter och installerar implementeringar av PSR-7, PSR-17, PSR-18 och HTTPlug</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/httplug">php-http/httplug</a>
    </td>
    <td>Bibliotek</td>
    <td>HTTPlug, HTTP-klientabstraktion för PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/promise">php-http/promise</a>
    </td>
    <td>Bibliotek</td>
    <td>Löfte som används för asynkrona HTTP-begäranden</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/CssXPath">phpgt/cssxpath</a>
    </td>
    <td>Bibliotek</td>
    <td>Konvertera CSS-väljare till XPath-frågor.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/Dom">phpgt/dom</a>
    </td>
    <td>Bibliotek</td>
    <td>Modern DOM API.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/PropFunc">phpgt/propfunc</a>
    </td>
    <td>Bibliotek</td>
    <td>Egenskapsåtkomst och mutatorfunktioner.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpseclib/mcrypt_compat">phpseclib/mcrypt_compat</a>
    </td>
    <td>Bibliotek</td>
    <td>PHP 5.x-8.x-polyfill för kryptering</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpseclib/phpseclib">phpseclib/phpseclib</a>
    </td>
    <td>Bibliotek</td>
    <td>PHP Secure Communications Library - Pure-PHP-implementeringar av RSA, AES, SSH2, SFTP, X.509 osv.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/cache">psr/cache</a>
    </td>
    <td>Bibliotek</td>
    <td>Gemensamt gränssnitt för att cacha bibliotek</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/clock">psr/clock</a>
    </td>
    <td>Bibliotek</td>
    <td>Gemensamt gränssnitt för att läsa klockan.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/container">psr/container</a>
    </td>
    <td>Bibliotek</td>
    <td>Gränssnitt för gemensam behållare (PHP FIG PSR-11)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/event-dispatcher">psr/event-dispatcher</a>
    </td>
    <td>Bibliotek</td>
    <td>Standardgränssnitt för händelsehantering.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-client">psr/http-client</a>
    </td>
    <td>Bibliotek</td>
    <td>Gemensamt gränssnitt för HTTP-klienter</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-factory">psr/http-factory</a>
    </td>
    <td>Bibliotek</td>
    <td>PSR-17: Vanliga gränssnitt för PSR-7 HTTP-meddelandefabriker</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-message">psr/http-message</a>
    </td>
    <td>Bibliotek</td>
    <td>Gemensamt gränssnitt för HTTP-meddelanden</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/log">psr/log</a>
    </td>
    <td>Bibliotek</td>
    <td>Gemensamt gränssnitt för loggning av bibliotek</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ralouphie/getallheaders">ralouphie/getallheaders</a>
    </td>
    <td>Bibliotek</td>
    <td>En polyfyllning för getallheaders.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ramsey/collection">ramsey/collection</a>
    </td>
    <td>Bibliotek</td>
    <td>Ett PHP-bibliotek för att representera och ändra samlingar.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ramsey/uuid">ramsey/uuid</a>
    </td>
    <td>Bibliotek</td>
    <td>Ett PHP-bibliotek för generering och arbete med UUID (Universally Unique Identiters).</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/reactphp/promise">reagerar/utlovar</a>
    </td>
    <td>Bibliotek</td>
    <td>En lätt implementering av CommonJS Promises/A för PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/MyIntervals/PHP-CSS-Parser">sabberworm/php-css-parser</a>
    </td>
    <td>Bibliotek</td>
    <td>Parser for CSS Files written in PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/jsonlint">seld/jsonlint</a>
    </td>
    <td>Bibliotek</td>
    <td>JSON Linter</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/phar-utils">seld/phar-utils</a>
    </td>
    <td>Bibliotek</td>
    <td>Verktyg för PHAR-filformat, t.ex. när PHP hjälper dig</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/signal-handler">seld/signal-handler</a>
    </td>
    <td>Bibliotek</td>
    <td>Enkel, enkel signalhanterare som tyst misslyckas där signaler inte stöds för enkel plattformsoberoende utveckling</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/aes-key-wrap">spomky-labs/aes-key-wrap</a>
    </td>
    <td>Bibliotek</td>
    <td>AES Key Wrap for PHP.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/otphp">spomky-labs/otphp</a>
    </td>
    <td>Bibliotek</td>
    <td>Ett PHP-bibliotek för generering av engångslösenord enligt RFC 4226 (HOTP-algoritm) och RFC 6238 (TOTP-algoritm) som är kompatibelt med Google Authenticator</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/pki-framework">spomky-labs/pki-framework</a>
    </td>
    <td>Bibliotek</td>
    <td>Ett PHP-ramverk för hantering av infrastrukturer med publik nyckel. Det omfattar X.509-certifikat för offentlig nyckel, attributcertifikat, certifieringsbegäranden och validering av certifieringssökväg.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/config">symfony/config</a>
    </td>
    <td>Bibliotek</td>
    <td>Hjälper dig att hitta, ladda, kombinera, autofylla och validera konfigurationsvärden av alla slag</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/console">symbol/konsol</a>
    </td>
    <td>Bibliotek</td>
    <td>Förenklar skapandet av snygga och testbara kommandoradsgränssnitt</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/css-selector">symfony/css-selector</a>
    </td>
    <td>Bibliotek</td>
    <td>Konverterar CSS-väljare till XPath-uttryck</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/dependency-injection">symbol/beroendeinjicering</a>
    </td>
    <td>Bibliotek</td>
    <td>Används för att standardisera och centralisera det sätt på vilket objekt skapas i programmet</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/deprecation-contracts">symfony/deprecation-agreements</a>
    </td>
    <td>Bibliotek</td>
    <td>En allmän funktion och konvention som utlöser meddelanden om borttagning</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/error-handler">symfony/error-handler</a>
    </td>
    <td>Bibliotek</td>
    <td>Tillhandahåller verktyg för att hantera fel och underlätta felsökning av PHP-kod</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/event-dispatcher">symfony/event-dispatcher</a>
    </td>
    <td>Bibliotek</td>
    <td>Tillhandahåller verktyg som gör att programkomponenterna kan kommunicera med varandra genom att skicka händelser och lyssna på dem</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/event-dispatcher-contracts">symfony/event-dispatcher-agreements</a>
    </td>
    <td>Bibliotek</td>
    <td>Allmänna abstraktioner relaterade till skicka-händelse</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/filesystem">symfony/filesystem</a>
    </td>
    <td>Bibliotek</td>
    <td>Tillhandahåller grundläggande verktyg för filsystemet</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/finder">symfony/finder</a>
    </td>
    <td>Bibliotek</td>
    <td>Söker efter filer och kataloger via ett intuitivt flytande gränssnitt</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-client">symfony/http-client</a>
    </td>
    <td>Bibliotek</td>
    <td>Tillhandahåller kraftfulla metoder för att hämta HTTP-resurser synkront eller asynkront</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-client-contracts">symfony/http-client-agreements</a>
    </td>
    <td>Bibliotek</td>
    <td>Allmänna abstraktioner relaterade till HTTP-klienter</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-foundation">symfony/http-foundation</a>
    </td>
    <td>Bibliotek</td>
    <td>Definierar ett objektorienterat lager för HTTP-specifikationen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-kernel">symfony/http-kernel</a>
    </td>
    <td>Bibliotek</td>
    <td>Tillhandahåller en strukturerad process för konvertering av en begäran till ett svar</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/intl">symfony/intl</a>
    </td>
    <td>Bibliotek</td>
    <td>Ger åtkomst till ICU-bibliotekets lokaliseringsdata</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/mailer">symfony/mailer</a>
    </td>
    <td>Bibliotek</td>
    <td>Hjälper dig att skicka e-post</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/mime">symfony/mime</a>
    </td>
    <td>Bibliotek</td>
    <td>Tillåter manipulering av MIME-meddelanden</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-ctype">symfony/polyfill-type</a>
    </td>
    <td>Bibliotek</td>
    <td>Symfonisk polyfyllning för typfunktioner</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-grapheme">symfony/polyfill-intl-grapteme</a>
    </td>
    <td>Bibliotek</td>
    <td>Symfony polyfill for intl's grapheme_* functions</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-idn">symfony/polyfill-intl-idn</a>
    </td>
    <td>Bibliotek</td>
    <td>Symfony polyfill for intl's id_to_ascii and id_to_utf8 functions</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-normalizer">symfony/polyfill-intl-normalizer</a>
    </td>
    <td>Bibliotek</td>
    <td>Symfonisk polyfyllning för klassen Normalizer i AIR och relaterade funktioner</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-mbstring">symfony/polyfill-mbstring</a>
    </td>
    <td>Bibliotek</td>
    <td>Symfonisk polyfyllning för MbitString-tillägget</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php73">symfony/polyfill-php73</a>
    </td>
    <td>Bibliotek</td>
    <td>Symfonisk polyfill backporting vissa PHP 7.3+-funktioner ger lägre PHP-versioner</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php80">symfony/polyfill-php80</a>
    </td>
    <td>Bibliotek</td>
    <td>Symfonisk polyfill backporting vissa PHP 8.0+-funktioner till lägre PHP-versioner</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php81">symfony/polyfill-php81</a>
    </td>
    <td>Bibliotek</td>
    <td>Symfonisk polyfill backporterar vissa PHP 8.1+-funktioner till lägre PHP-versioner</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php82">symfony/polyfill-php82</a>
    </td>
    <td>Bibliotek</td>
    <td>Symfonisk polyfill backporting vissa PHP 8.2+-funktioner till lägre PHP-versioner</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php83">symfony/polyfill-php83</a>
    </td>
    <td>Bibliotek</td>
    <td>Symfonisk polyfill backporterar vissa PHP 8.3+-funktioner till lägre PHP-versioner</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/process">symfony/process</a>
    </td>
    <td>Bibliotek</td>
    <td>Kör kommandon i underprocesser</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/service-contracts">symfony/service-contract</a>
    </td>
    <td>Bibliotek</td>
    <td>Allmänna abstraktioner relaterade till skrivande tjänster</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/string">symbol/sträng</a>
    </td>
    <td>Bibliotek</td>
    <td>Ger ett objektorienterat API för strängar och hanterar byte, UTF-8-kodpunkter och grafemkluster på ett enhetligt sätt</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/var-dumper">symfony/var-dumper</a>
    </td>
    <td>Bibliotek</td>
    <td>Tillhandahåller mekanismer för att gå igenom valfri PHP-variabel</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/var-exporter">symfony/var-exporting</a>
    </td>
    <td>Bibliotek</td>
    <td>Tillåter export av serialiserbara PHP-datastrukturer till vanlig PHP-kod</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/yaml">symfony/yaml</a>
    </td>
    <td>Bibliotek</td>
    <td>Läser in och dumpar YAML-filer</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/web-token/jwt-framework">web-token/jwt-framework</a>
    </td>
    <td>Symfony-bundle</td>
    <td>JSON Object Signing and Encryption library for PHP and Symfony Bundle.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/webonyx/graphql-php">webonyx/graphql-php</a>
    </td>
    <td>Bibliotek</td>
    <td>En PHP-port för GraphQL referensimplementering</td>
  </tr>
  </tbody>
</table>

### OSL-3.0, AFL-3.0

<table>
  <thead>
    <tr>
      <th>Namn</th>
      <th>Typ</th>
      <th>Beskrivning</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      paypal/module-braintree-customer-balance
    </td>
    <td>Magento2-modul</td>
    <td>Ej tillämpligt</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-present-card
    </td>
    <td>Magento2-modul</td>
    <td>Ej tillämpligt</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-present-card-account
    </td>
    <td>Magento2-modul</td>
    <td>Ej tillämpligt</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-present-wrapping
    </td>
    <td>Magento2-modul</td>
    <td>Ej tillämpligt</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-graph-ql
    </td>
    <td>Magento2-modul</td>
    <td>Ej tillämpligt</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-gain
    </td>
    <td>Magento2-modul</td>
    <td>Ej tillämpligt</td>
  </tr>
  </tbody>
</table>

### OSL-3.0

<table>
  <thead>
    <tr>
      <th>Namn</th>
      <th>Typ</th>
      <th>Beskrivning</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>

### PHP

<table>
  <thead>
    <tr>
      <th>Namn</th>
      <th>Typ</th>
      <th>Beskrivning</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/2tvenom/CBOREncode">2tvenom/cborencode</a>
    </td>
    <td>Bibliotek</td>
    <td>CBOR encoder for PHP</td>
  </tr>
  </tbody>
</table>

### Egendom

<table>
  <thead>
    <tr>
      <th>Namn</th>
      <th>Typ</th>
      <th>Beskrivning</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>

### egen

<table>
  <thead>
    <tr>
      <th>Namn</th>
      <th>Typ</th>
      <th>Beskrivning</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      paypal/module-braintree-core
    </td>
    <td>Magento2-modul</td>
    <td>Fork från modulen Magento Braintree 2.2.0 av Gene Commerce for PayPal.</td>
  </tr>
  </tbody>
</table>
