---
title: Google webbplatsverktyg
description: Läs mer om de Google-verktyg som ni kan använda för att optimera ert innehåll, analysera trafiken och koppla samman er katalog med shoppingaggregatorer och marknadsplatser.
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Google webbplatsverktyg

Din butikskonfiguration är integrerad med följande Google-verktyg för att optimera ditt innehåll, analysera trafiken och koppla din katalog till shoppingaggregatorer och marknadsplatser.

- [Google Analytics](google-analytics.md) - Användning _Google Universal Analytics_ för att definiera ytterligare anpassade mått och mätvärden för spårning, med stöd för interaktioner offline och i mobilappar samt tillgång till pågående uppdateringar.

- [Google Content Experiments](google-content-experiments.md) - Konfigurera ett A/B-test för produkter, kategorier eller innehållssidor med hjälp av Google Analytics Content Experiments.

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Använd Google Tag Manager för att hantera de många taggar som är kopplade till marknadsföringskampanjer.

- [Google AdWord](google-adwords.md) - Skapa en Google AdWords-kampanj och spåra konverteringar för din butik.

{{gtag-api-note}}

## Google sekretessinställningar

Om ditt företag måste följa sekretessregler som [GDPR](../getting-started/compliance-gdpr.md) eller [CCPA](../getting-started/compliance-ccpa.md)ändrar du standardinställningarna för Google-verktygen så att de uppfyller sekretesskraven. Följ de här stegen för att se till att din användning av kunddata fortsätter att uppfylla kraven.

### Steg 1: Uppdatera Google-inställningar

1. [Logga in][1]{: target=&quot;_blank&quot;} till ditt företags Google Analytics-konto.

1. Längst ned på vänster sidofält väljer du **[!UICONTROL Admin]** och navigera sedan till kontot som du vill redigera (om tillämpligt).

1. I **[!UICONTROL Account]** kolumn, klicka **[!UICONTROL Account Settings]**.

1. Inaktivera datadelning för att uppfylla kraven på sekretesslagstiftning.

   Standardinställningarna för Google Analytics delar dina företagsdata med Google och andra parter. Om du vill inaktivera datadelning avmarkerar du kryssrutan för följande inställningar:

   - Google produkter och tjänster
   - Benchmarking
   - Teknisk support
   - Kontospecialister

1. Acceptera _Ändring av databehandling_.

   Google Ads Data Processing Terms beskriver hur Google behandlar data och vilka åtgärder som vidtas för att säkerställa datasäkerheten för företag som omfattas av den allmänna dataskyddsförordningen. En förteckning över era juridiska personer och kontaktuppgifter bevaras också i samband med ändringen. Till [läs mer][2]{: target=&quot;_blank&quot;}, klicka på länken i meddelandet överst på sidan.

   - Bläddra nedåt på sidan till **[!UICONTROL Data Processing Amendment]**.
   - Klicka **[!UICONTROL Review Amendment]** för att läsa _Google Ads Data Processing Terms_.
   - Klicka på **[!UICONTROL Accept]**.
   - Klicka på **[!UICONTROL Save]**.

1. Slutför _DPA-administration_ information.

   - Klicka **[!UICONTROL Manage DPA Details]** för att öppna en DPA-administrationssida där du kan redigera kontakter och organisationens juridiska personer.

   - I **[!UICONTROL Legal Entities]** klickar du på _Redigera_ ( ![Google redigeringsikon](./assets/google-icon-edit.png) ) och lägg till ett eller flera registrerade namn för din organisation. När du är klar klickar du på **[!UICONTROL Save]**.

   - I **Kontakter** klickar du på _Lägg till_ ( ![Google-ikon](./assets/google-icon-add.png) ) och ange information för den första kontakten. Markera sedan kryssrutan för varje roll och klicka på **[!UICONTROL Add]**.

      - Primär kontakt - (e-postadress för meddelande) Den kontakt som meddelanden skickas till.
      - Uppgiftsskyddsombud - (om tillämpligt) Den person som har utsetts för att underlätta efterlevnaden av reglerna för integritetsskydd.
      - Företrädare för Europeiska ekonomiska samarbetsområdet (EES) - (om tillämpligt) den person som företräder kunder utanför EU när det gäller deras skyldigheter i den allmänna dataskyddsförordningen.

     Upprepa om du vill lägga till ytterligare en kontakt, om tillämpligt.

### Steg 2: Ändra dina Google JS-bibliotek

Google har stöd för tre JavaScript-bibliotek för att mäta webbplatsanvändningen, beroende på Google-produkt: `gtag.js`, `analytics.js`och `ga.js`. För att uppfylla integritetskraven kan standardkoden ändras på följande sätt:

#### Anonymisera IP-adresser

För att anonymisera IP-adresserna som används av **_Google Universal Analytics_**, lägger du till följande utdrag i `analytics.js` bibliotek på webbservern:

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

Mer information finns i [Fältreferens för Analytics.js][3]{: target=&quot;_blank&quot;} i hjälpen för Google.

Om du använder äldre `ga.js` lägg till följande kodfragment i biblioteket:

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

För att anonymisera IP-adresserna som används av **_Google Tag Manager_**, ange `anonymize_ip` parameter till `true` i `gtag.js` på webbservern.

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

Mer information finns på [IP-analys i Analytics][4] i Google Help.

#### Tvinga SSL

Om du vill tvinga alla Google-data att överföras via ett säkert socketlager (SSL) lägger du till följande utdrag i `analytics.js` på webbservern.

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### Steg 3: Uppdatera din sekretesspolicy

Uppdatera dina [integritetspolicy](../getting-started/privacy-policy.md) för att ange att ditt företag

- Använder Google Analytics
- Maskerar IP-adresser för att dölja personlig information
- Har inaktiverat Google-datadelning
- Använder inte andra Google-tjänster med Google Analytics cookies

[1]: https://www.google.com/analytics/
[2]: https://support.google.com/analytics/answer/3379636
[3]: https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference
[4]: https://support.google.com/analytics/answer/2763052
