---
title: '[!DNL Audience Activation]'
description: Lär dig hur du aktiverar Real-Time CDP-målgrupper i Adobe Commerce för att utveckla personaliseringen i din butik.
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 5929a2ff26dadda40ecfa9e435a73343caef3cde
workflow-type: tm+mt
source-wordcount: '1683'
ht-degree: 0%

---

# [!DNL Audience Activation]

Med tillägget [!DNL Audience Activation] kan du aktivera Real-Time CDP-målgrupper i Adobe Commerce för att skapa unika erbjudanden i kundvagnen. Erbjudandena och incitamenten omfattar vanliga tekniker för e-handel, som _köp 2 få 1 kostnadsfritt_, hjältebanners som är inriktade på den kunden och ändrade produktpriser genom olika erbjudanden. De målgrupper som byggs inom Real-Time CDP bygger på data från olika affärssystem, t.ex. ERP (Enterprise Resource Planning), CRM (Customer Relationship Management), försäljningsställen och marknadsföringssystem. Eftersom kundsegmentsinformationen uppdateras kontinuerligt kan kunderna associeras och kopplas bort från ett segment när de handlar i din butik.

Du kan aktivera målgrupper i en Luma storefront eller [headless](#headless-support) store. I en Lumabutik lagras målgruppsinformation (segmentmedlemskap) i en cookie på Commerce-sidan. I ett headless-lager skickas målgruppsinformation i GraphQL API-huvudet som en parameter med namnet: `aep-segments-membership`.

## Versionsinformation

Det här avsnittet innehåller information om uppdateringar av Audience Activation-tillägget och innehåller:

![Nytt](../assets/new.svg) - Nya funktioner
![Korrigera ](../assets/fix.svg) - Korrigeringar och förbättringar
![Fel](../assets/bug.svg) - Kända fel

Läs [Kommande releaser](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) om du vill veta mer om releasescheman och support.

Läs utvecklardokumentationen för att [lära dig mer om produktkompatibilitet](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html).

## Uppdateringar av tjänster som stöds

I versionsinformationen beskrivs funktionsändringar och korrigeringar för tillägg som används av Audience Activation.

+++Uppdateringar av tjänster som stöds

_15 augusti 2023_

![Korrigera](../assets/fix.svg) - Kontrollpanelen [Real-Time CDP Audiences](#real-time-cdp-audiences-dashboard) har uppdaterats för att förenkla filtreringen.

_27 juni 2023_

![Korrigera](../assets/fix.svg) - Stöd för PHP 8.2 har lagts till i paketet `magento/module-data-services-graphql`.

_30 maj 2023_

![Nytt](../assets/new.svg) - Kontrollpanelen [Real-Time CDP Audiences](#real-time-cdp-audiences-dashboard) har uppdaterats så att den kan sortera, söka efter och filtrera de aktiva målgrupperna i din Adobe Commerce-instans.

+++

### 2.4.0

[!BADGE Kompatibilitet]{type=Informative tooltip="Kompatibilitet"} Adobe Commerce version 2.4.4 och senare

_24 mars 2025_

![Nytt](../assets/new.svg) - Stöd för PHP 8.4 har lagts till.

### 2.3.1

[!BADGE Kompatibilitet]{type=Informative tooltip="Kompatibilitet"} Adobe Commerce version 2.4.4 och senare

_12 november 2024_

![Korrigera](../assets/fix.svg) - Ett fel har korrigerats vid filtrering av tillgängliga Real-Time CDP-målgrupper att välja bland.

### 2.3.0

[!BADGE Kompatibilitet]{type=Informative tooltip="Kompatibilitet"} Adobe Commerce version 2.4.4 och senare

_29 juli 2024_

![Nytt](../assets/new.svg) - Kommandoradssyntax har lagts till så att du kan [testa autentiseringsuppgifter](#validate-the-connection) för att avgöra om de behöver uppdateras för att hämta målgruppsdata från Adobe Experience Platform.

### 2.2.0

[!BADGE Kompatibilitet]{type=Informative tooltip="Kompatibilitet"} Adobe Commerce version 2.4.4 och senare

_12 juni 2024_

![Nytt](../assets/new.svg) - GA-version för [relaterade produktregler](../merchandising-promotions/product-related-rule-create.md) informerad av målgrupper.

### 2.1.1

[!BADGE Kompatibilitet]{type=Informative tooltip="Kompatibilitet"} Adobe Commerce version 2.4.4 och senare

_4 april 2024_

![Nytt](../assets/new.svg) - Stöd för PHP 8.3 har lagts till.

### 2.2.0-beta1

[!BADGE Kompatibilitet]{type=Informative tooltip="Kompatibilitet"} Adobe Commerce version 2.4.4 och senare

_16 februari 2024_

![Nytt](../assets/new.svg) - Om du deltar i betaversionen kontrollerar du att `composer.json`-filen har följande på rotnivån: ` "minimum-stability": "beta"`.
![Nytt](../assets/new.svg) - (**Beta**) Lagt till möjlighet att skapa [relaterade produktregler](../merchandising-promotions/product-related-rule-create.md) som har informerats av målgrupper.

### 2.1.0

[!BADGE Kompatibilitet]{type=Informative tooltip="Kompatibilitet"} Adobe Commerce version 2.4.4 och senare

_24 januari 2024_

![Nytt](../assets/new.svg) - Kontrollpanelen [Real-Time CDP Audiences](#real-time-cdp-audiences-dashboard) har uppdaterats för att inkludera de webbplatser som innehåller målgrupperna och ange vilka dynamiska block och kundprisregler som har konfigurerats för att använda dessa målgrupper.

### 2.0.1

[!BADGE Kompatibilitet]{type=Informative tooltip="Kompatibilitet"} Adobe Commerce version 2.4.4 och senare

_16 november 2023_

![Korrigera](../assets/fix.svg) - Förbättrad stabilitet.

### 2.0.0

[!BADGE Kompatibilitet]{type=Informative tooltip="Kompatibilitet"} Adobe Commerce version 2.4.4 och senare

_10 oktober 2023_

![Nytt](../assets/new.svg) - Stöd för OAuth 2.0 har lagts till när du [konfigurerar](#configure-the-extension) Audience Activation-tillägget.
![Korrigera](../assets/fix.svg) - Förbättrad stabilitet.

### 1.2.0

[!BADGE Kompatibilitet]{type=Informative tooltip="Kompatibilitet"} Adobe Commerce version 2.4.4 och senare

_15 augusti 2023_

![Korrigera](../assets/fix.svg) - Uppdaterade UI-komponentens version.

### 1.1.0

_30 maj 2023_

[!BADGE Kompatibilitet]{type=Informative tooltip="Kompatibilitet"} Adobe Commerce version 2.4.4 och senare

![Nytt](../assets/new.svg) - Stöd för [dynamiska block](#headless-support) har lagts till i en headless-butik.

### 1.0.1

_11 maj 2023_

[!BADGE Kompatibilitet]{type=Informative tooltip="Kompatibilitet"} Adobe Commerce version 2.4.4 och senare

![Korrigera](../assets/fix.svg) - Ett problem har korrigerats där en dynamisk spärr- eller kundvagnsprisregel inte tillämpades på butiken.
![Korrigera](../assets/fix.svg) - Ett problem har korrigerats där en okonfigurerad installation av Audience Activation-tillägget orsakade ett fel när en handlare försökte skapa eller uppdatera ett dynamiskt block.

### 1.0.0

_31 mars 2023_

[!BADGE Kompatibilitet]{type=Informative tooltip="Kompatibilitet"} Adobe Commerce version 2.4.4 och senare

![Nytt](../assets/new.svg) - allmän tillgänglighetsrelease

## Implementering

Följande uppgifter gäller både Luma-implementeringar och implementeringar utan headless storefront. Om du vill aktivera målgrupper i Adobe Commerce måste du:

- Installera Adobe Commerce version 2.4.4 eller senare
- [Aktivera](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Adobe Commerce som mål i Real-Time CDP
- [Installera](#install-the-extension) tillägget [!DNL Audience Activation] i Admin
- [Konfigurera](#configure-the-extension) tillägget [!DNL Audience Activation] i Admin

### Installera tillägget

Installera tillägget [!DNL Audience Activation] från [Marketplace](https://commercemarketplace.adobe.com/magento-audiences.html) eller kör följande kommando:

```bash
composer require magento/audiences
```

### Konfigurera tillägget

När du har installerat tillägget [!DNL Audience Activation] måste du logga in i Commerce Admin och slutföra följande:

1. Gå till _>_ > **[!UICONTROL System]** på sidofältet _[!UICONTROL Services]_Admin **[!UICONTROL Commerce Services Connector]**.

1. [Logga in](https://experienceleague.adobe.com/docs/commerce/user-guides/integration-services/saas.html#organizationid) på ditt Adobe-konto och välj ditt företags-ID.

1. Gå till _>_ > **[!UICONTROL System]** på sidofältet _[!UICONTROL Services]_Admin **[!UICONTROL [!DNL Data Connection]]**.

1. I fältet **[!UICONTROL Datastream ID]** klistrar du in ID:t för den datastream som du skapade när du [aktiverade](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html#parameters) Adobe Commerce som mål i Real-Time CDP.

   Denna datastream skickar data från din Commerce webbplats till Real-Time CDP för att avgöra om en kund tillhör en viss målgrupp. Om du ännu inte har skapat ett datastream [skapar](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#create) i Experience Platform, [lägger till](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) det i Commerce-målet i Real-Time CDP och i tillägget [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/connect-data.html#data-collection) i Admin.

   >[!NOTE]
   >
   >När du anger ett datastream-ID [kopplar du det till en specifik webbplats](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/connect-data.html#data-collection) i tillägget [!DNL Data Connection]. Om din Commerce-butik har flera webbplatser kan du [skapa ett mål](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) för varje webbplats i Real-Time CDP och använda olika data-ID för varje.

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Services]** och välj **[!UICONTROL [!DNL Data Connection]]**.

1. [Lägg till ](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/connect-data.html#add-service-account-and-credential-details) tjänstkonto och autentiseringsuppgifter.

## Var kan man använda Real-Time CDP målgrupper i Commerce?

När tillägget [!DNL Audience Activation] är aktiverat kan du:

- [Skapa en kundprisregel](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) som har informerats av målgrupper
- [Skapa ett dynamiskt block](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) som stöds av målgrupper
- [Skapa en relaterad produktregel](../merchandising-promotions/product-related-rule-create.md) som har informerats av målgrupper

>[!TIP]
>
>Ett komplett slutanvändarexempel med information om hur du exporterar [!DNL Commerce]-data till Real-Time CDP finns i [!DNL Commerce]Skapa en målgrupp och aktivera den målgruppen till [Real-Time CDP med  [!DNL Commerce] .](https://experienceleague.adobe.com/en/docs/commerce/data-connection/use-cases/create-audience)

## Real-Time CDP målgruppspanel

Du kan visa alla [aktiva](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html) målgrupper som är tillgängliga för anpassning i din Adobe Commerce-instans med kontrollpanelen **Real-Time CDP-målgrupper**.

Gå till sidofältet **Admin** och gå till _>_ för att komma åt kontrollpanelen **[!UICONTROL Customers]** Real-Time CDP Audiences **[!UICONTROL Real-time CDP Audience]**.

![Real-Time CDP Audiences Dashboard](./assets/real-time-cdp-dashboard.png){width="700" zoomable="yes"}

Kontrollpanelen innehåller följande fält:

| Kolumn | Beskrivning |
|--- |--- |
| `Hide filters` | Gör att du kan visa eller dölja alla filter som du kan använda på kontrollpanelen. Det enda filter som du kan använda är `Last updated`. Med det här filtret kan du välja ett datumintervall för målgrupper baserat på när de senast uppdaterades. |
| `Search` | Gör att du kan söka efter aktiva målgrupper i din Commerce-instans. |
| `Name` | Namn som ges till målgruppen i Real-Time CDP. |
| `Origin` | Anger varifrån målgruppen kom, till exempel `Experience Platform`. |
| `Websites` | Anger vilka webbplatser som är konfigurerade att använda målgrupperna. |
| `Dynamic Blocks` | Anger vilka dynamiska block som är konfigurerade att använda målgrupperna. |
| `Cart Price Rules` | Anger vilka kundprisregler som har konfigurerats för att använda målgrupperna. |
| `Related Product Rules` | Anger vilka relaterade produktregler som har konfigurerats för att använda målgrupperna. |
| `Last updated` | Anger när målgruppen ändrades i Real-Time CDP. |
| `Sync now` | Hämtar nya eller uppdaterade målgrupper från Real-Time CDP. |
| `Customize table` | Gör att du kan visa eller dölja kolumnerna `Origin`, `Websites`, `Dynamic Blocks`, `Cart Price Rules` och `Last updated`. |

{style="table-layout:auto"}

## Headless-support

Du kan aktivera målgrupper i en headless Adobe Commerce-instans, som AEM och PWA, för att visa kundprisregler, relaterade produktregler eller dynamiska block baserade på målgrupperna.

### Kundprisregler och relaterade produktregler

För kundvagnsprisregler och relaterade produktregler kommunicerar en headless Store till Experience Platform via [Commerce integration framework (CIF)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html). Ramverket innehåller ett API på serversidan som implementeras med GraphQL. Målgruppsinformation, till exempel en kunds segment, skickas till Commerce via en GraphQL-huvudparameter med namnet `aep-segments-membership`.

Den övergripande arkitekturen är följande:

![Skicka data från Headless StoreFront till Backend](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

När du har [installerat](#install-the-extension) och [konfigurerat](#configure-the-extension) tillägget innehåller Experience Platform Web SDK målgruppsinformation i form av segmentmedlemskap.

Information om hur du fångar dessa segmentmedlemskap från SDK finns i det här [kodfragmentet](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes).

När segmenten har hämtats kan du skicka dem till Commerce i GraphQL sidhuvud. Exempel:

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```

### Dynamiska block

För dynamiska block kan GraphQL `dynamicBlocks`-frågor innehålla indataattributet `audience_id`. Om du anger ett eller flera `audience_id`-värden i en `dynamicBlocks`-fråga returneras en lista med dynamiska block som tilldelats dessa målgrupper.

#### Exempel på användning

Följande fråga returnerar alla dynamiska block som är associerade med flera målgrupps-ID:n.

**Begäran:**

```graphql
{
  dynamicBlocks(input:
  {
    type: SPECIFIED
    audience_id: {
      in: [
        "cd29a789-9be8-40ad-a1ef-640c33b3742e"
        "92c3e14d-c72b-40d0-96b7-b96801dcc135"
      ]
    }
  })
  {
    items {
      uid
      audience_id
      content {
        html
      }
    }
    page_info {
      current_page
      page_size
      total_pages
    }
    total_count
  }
}
```

**Svar:**

```json
{
  "data": {
    "dynamicBlocks": {
      "items": [
        {
          "uid": "MQ==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e"
          ],
          "content": {
            "html": "<h2><strong>SAVE 20%</strong></h2>\r\n<p>(some restrictions apply)</p>\r\n<p>&nbsp;</p>"
          }
        },
        {
          "uid": "Mg==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e",
            "92c3e14d-c72b-40d0-96b7-b96801dcc135"
          ],
          "content": {
            "html": "<p><img src=\"{{media url=&quot;wysiwyg/save20.png&quot;}}\" alt=\"save 20% red\"></p>"
          }
        }
      ],
      "page_info": {
        "current_page": 1,
        "page_size": 20,
        "total_pages": 1
      },
      "total_count": 2
    }
  }
}
```

Läs mer om GraphQL-frågan `dynamicBlocks` i [utvecklardokumentationen](https://developer.adobe.com/commerce/webapi/graphql/schema/store/queries/dynamic-blocks/).

## Hämta målgrupper med Adobe Experience Platform Mobile SDK

Du kan hämta Real-Time CDP-målgrupper med Adobe Experience Platform Mobile SDK.

1. [Installera](#install-the-extension) Audience Activation-tillägget.
1. [installera och konfigurera SDK för din mobila Commerce-webbplats](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/mobile-sdk-epc.html).

>[!IMPORTANT]
>
>Adobe Experience Platform Mobile SDK för iOS har stöd för iOS 11 eller senare.

När du är klar med konfigurationen kan du använda SDK-mobilåtgärder för att hämta målgruppsdata. Exempel:

```swift
Edge.sendEvent(experienceEvent: experienceEvent) { (handles: [EdgeEventHandle]) in
    for handle in handles {
        if handle.type == "activation:pull" {
        let payloadItems = handle.payload ?? []
            for payloadItem in payloadItems {
                if let segments = payloadItem["segments"] as? any Sequence {
                    var segmentsArr = [Any]()
                    for segment in segments {
                        let response = segment as AnyObject?
                        segmentsArr.append(response?.object(forKey: "id")! ?? "")
                    }
                    print("Saving segments ->  \(segments)")
                    storage.set(segmentsArr, forKey: "segments")
                    print("End saving segments")
                }
         
                // Show segments
                let rSegments = storage.object(forKey: "segments") ?? nil;
                print("Retrieving segments -> \(rSegments)")
            }
        }
    }
}
```

När data har hämtats kan du använda den för att skapa kundorienterade [kundprisregler](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences), [dynamiska block](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) och [relaterade produktregler](../merchandising-promotions/product-related-rule-create.md) i Commerce-appen.

## Målgrupper visas inte i Commerce

Om Real-Time CDP-målgrupper inte visas i Commerce kan det bero på:

- Ogiltig anslutning
- Felaktig autentiseringstyp har valts på konfigurationssidan **Dataanslutning**
- Otillräckliga privilegier för genererad token

I följande avsnitt beskrivs hur du felsöker dessa problem.

### Validera anslutningen

Kör följande kommando för att validera inloggningsuppgifterna och svaret från Adobe Experience Platform:

```bash
bin/magento audiences:config:status
```

Det här kommandot returnerar anslutningsstatusen. Lägg till flaggan `-v` om du vill ha mer utförlig information:

```
./bin/magento audiences:config:status -v  
```

Exempel:

```
+----------------------------------+---------------+---------------------------------------------+---------------------------------------------------------+--------------+
| Client ID                        | Client secret | Technical account ID                        | Technical account email                                 | Sandbox name |
+----------------------------------+---------------+---------------------------------------------+---------------------------------------------------------+--------------+
| 1234bd57fac8497d8933327c535347d8 | *****         | 12341E116638D6B00A495C80@techacct.adobe.com | 12345-b95b-4894-a41c-a4130d26bd80@techacct.adobe.com | dev          |
```

### Felaktig autentiseringstyp har valts i konfigurationen

1. Öppna din Commerce-instans.
1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_Admin **[!UICONTROL Configuration]**.
1. Expandera **[!UICONTROL Services]** och välj **[!UICONTROL [!DNL Data Connection]]**.
1. Kontrollera att auktoriseringsmetoden server-till-server som du angav i fältet **[!UICONTROL Authentication Type]** är korrekt. Adobe rekommenderar att du använder **OAuth**. JWT har tagits bort. [Läs mer](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/).

### Otillräckliga privilegier för genererad token

Problemet kan bero på otillräcklig API-behörighet för den genererade token. Så här ser du till att din token har rätt behörigheter:

1. Identifiera systemadministratören för Adobe Experience Platform i din organisation.
1. Hitta projektet och autentiseringsuppgifterna som du kommer att använda.
1. Identifiera e-postadressen till det tekniska kontot, till exempel: `fe3c9476-1234-1234-abcd-2a51a785009a@techacct.adobe.com`.
1. Låt systemadministratören starta Adobe Experience Platform och gå till **[!UICONTROL Permissions]** -> **[!UICONTROL Users]** -> **[!UICONTROL API credentials]**.
1. Använd det tekniska kontots e-postadress ovan för att söka efter de autentiseringsuppgifter som ska ändras.
1. Öppna autentiseringsuppgifterna och välj sedan **[!UICONTROL Roles]** -> **[!UICONTROL Add roles]**.
1. Lägg till rollen som innehåller behörigheten **[!UICONTROL Manage destinations]**.
1. Klicka på **[!UICONTROL Save]**.
1. [Återskapa](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html#generate-access-token) åtkomsttoken i konsolen.
1. Kontrollera att token ger ett giltigt svar med [Target Connections API](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/getTargetConnections).
