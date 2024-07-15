---
title: Google webbplatsverktyg
description: Läs mer om de Google-verktyg som ni kan använda för att optimera ert innehåll, analysera trafiken och koppla samman er katalog med shoppingaggregatorer och marknadsplatser.
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Google webbplatsverktyg

Din butikskonfiguration är integrerad med följande Google-verktyg för att optimera ditt innehåll, analysera trafiken och koppla din katalog till shoppingaggregatorer och marknadsplatser.

- [Google Analytics](google-analytics.md) - Använd _Google Universal Analytics_ för att definiera ytterligare anpassade mått och mätvärden för spårning, med stöd för interaktioner offline och i mobilappar samt tillgång till pågående uppdateringar.

- [Google Content Experiments](google-content-experiments.md) - Konfigurera ett A/B-test för produkter, kategorier eller innehållssidor med hjälp av Google Analytics Content Experiments.

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Använd Google Tag Manager för att hantera många taggar som hör till marknadsföringskampanjhändelser.

- [Google AdWords](google-adwords.md) - Skapa en Google AdWords-kampanj och spåra konverteringar för din butik.

{{gtag-api-note}}

## Google sekretessinställningar

Om ditt företag måste följa sekretessregler som [GDPR](../getting-started/compliance-gdpr.md) eller [CCPA](../getting-started/compliance-ccpa.md) ändrar du standardinställningarna för Google-verktygen så att de uppfyller sekretesskraven. Följ de här stegen för att se till att din användning av kunddata fortsätter att uppfylla kraven.

### Steg 1: Uppdatera Google-inställningar

1. [Logga in][1]{: target=&quot;_blank&quot;} på ditt företags Google Analytics-konto.

1. Välj **[!UICONTROL Admin]** längst ned i det vänstra sidfältet och navigera sedan till det konto som du vill redigera (om tillämpligt).

1. Klicka på **[!UICONTROL Account Settings]** i kolumnen **[!UICONTROL Account]**.

1. Inaktivera datadelning för att uppfylla kraven på sekretesslagstiftning.

   Standardinställningarna för Google Analytics delar dina företagsdata med Google och andra parter. Om du vill inaktivera datadelning avmarkerar du kryssrutan för följande inställningar:

   - Google produkter och tjänster
   - Benchmarking
   - Teknisk support
   - Kontospecialister

1. Acceptera _databearbetningstillägget_.

   Google Ads Data Processing Terms beskriver hur Google behandlar data och vilka åtgärder som vidtas för att säkerställa datasäkerheten för företag som omfattas av den allmänna dataskyddsförordningen. En förteckning över era juridiska personer och kontaktuppgifter bevaras också i samband med ändringen. Om du vill [lära dig mer][2]{: target=&quot;_blank&quot;} klickar du på länken i meddelandet överst på sidan.

   - Bläddra ned sidan till **[!UICONTROL Data Processing Amendment]**.
   - Klicka på **[!UICONTROL Review Amendment]** för att läsa _Google Ads Data Processing Terms_.
   - Klicka på **[!UICONTROL Accept]**.
   - Klicka på **[!UICONTROL Save]**.

1. Fyll i informationen om _DPA-administration_.

   - Klicka på **[!UICONTROL Manage DPA Details]** för att öppna en DPA-administrationssida där du kan redigera kontakter och organisationens juridiska personer.

   - Klicka på ikonen _Redigera_ ( ![Google-redigeringsikonen](./assets/google-icon-edit.png) ) i avsnittet **[!UICONTROL Legal Entities]** och lägg till ett eller flera registrerade namn för din organisation. Klicka på **[!UICONTROL Save]** när du är klar.

   - I avsnittet **Kontakter** klickar du på ikonen _Lägg till_ ( ![Lägg till Google-ikon](./assets/google-icon-add.png) ) och anger information för den första kontakten. Markera sedan kryssrutan för varje tillämplig roll och klicka på **[!UICONTROL Add]**.

      - Primär kontakt - (e-postadress för meddelande) Den kontakt som meddelanden skickas till.
      - Uppgiftsskyddsombud - (om tillämpligt) Den person som har utsetts för att underlätta efterlevnaden av reglerna för integritetsskydd.
      - Företrädare för Europeiska ekonomiska samarbetsområdet (EES) - (om tillämpligt) den person som företräder kunder utanför EU när det gäller deras skyldigheter i den allmänna dataskyddsförordningen.

     Upprepa om du vill lägga till ytterligare en kontakt, om tillämpligt.

### Steg 2: Ändra dina Google JS-bibliotek

Google stöder tre JavaScript-bibliotek för att mäta webbplatsanvändningen, beroende på Google-produkten: `gtag.js`, `analytics.js` och `ga.js`. För att uppfylla integritetskraven kan standardkoden ändras på följande sätt:

#### Anonymisera IP-adresser

Om du vill anonymisera IP-adresserna som används av **_Google Universal Analytics_** lägger du till följande kodutdrag i `analytics.js`-biblioteket på webbservern:

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

Mer information finns i [Fältreferens för Analytics.js][3]{: target=&quot;_blank&quot;} i Google-hjälpen.

Om du använder det gamla `ga.js`-biblioteket lägger du till följande kodutdrag:

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

Om du vill anonymisera IP-adresserna som används av **_Google Tag Manager_** anger du parametern `anonymize_ip` till `true` i biblioteket `gtag.js` på webbservern.

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

Mer information finns i [IP-analys i Analytics][4] i Google-hjälpen.

#### Tvinga SSL

Om du vill tvinga alla Google-data att överföras via ett säkert socketlager (SSL) lägger du till följande utdrag i biblioteket `analytics.js` på webbservern.

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### Steg 3: Uppdatera din sekretesspolicy

Uppdatera din [sekretesspolicy](../getting-started/privacy-policy.md) för att ange att ditt företag:

- Använder Google Analytics
- Maskerar IP-adresser för att dölja personlig information
- Har inaktiverat Google-datadelning
- Använder inte andra Google-tjänster med Google Analytics cookies

[1]: https://www.google.com/analytics/
[2]: https://support.google.com/analytics/answer/3379636
[3]: https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference
[4]: https://support.google.com/analytics/answer/2763052
