---
title: "[!DNL Audience Activation]"
description: Lär dig hur du aktiverar Real-Time CDP-målgrupper i Adobe Commerce för att utveckla personaliseringen i din butik.
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
source-git-commit: f7b8e47aa5a8113fac768b8086ace3bf673193c5
workflow-type: tm+mt
source-wordcount: '1222'
ht-degree: 0%

---

# [!DNL Audience Activation]

The [!DNL Audience Activation] kan ni aktivera Real-Time CDP-målgrupper i Adobe Commerce för att skapa unika erbjudanden i kundvagnen. Dessa erbjudanden och incitament omfattar bland annat vanliga tekniker för e-handel, som _köp 2 få 1 utan kostnad_, hjältebanners riktade mot den kunden och ändrade produktpriser genom olika erbjudanden. De målgrupper som byggs inom Real-Time CDP bygger på data från olika affärssystem, t.ex. ERP (Enterprise Resource Planning), CRM (Customer Relationship Management), försäljningsställen och marknadsföringssystem. Eftersom kundsegmentsinformationen uppdateras kontinuerligt kan kunderna associeras och kopplas bort från ett segment när de handlar i din butik.

Du kan aktivera målgrupper i en Luma-butik eller [headless](#headless-support) storefront. I en Lumabutik lagras målgruppsinformation (segmentmedlemskap) i en cookie på Commerce-sidan. I ett headless-lager skickas målgruppsinformation i GraphQL API-huvudet som en parameter med namnet: `aep-segments-membership`.

## Versionsinformation

Det här avsnittet innehåller information om uppdateringar av tillägget Audience Activation och innehåller:

![Nytt](../assets/new.svg) - Nya funktioner
![Korrigera](../assets/fix.svg) - Korrigeringar och förbättringar
![Fel](../assets/bug.svg) - Kända fel

Se [Kommande versioner](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) om du vill veta mer om releasescheman och support.

Läs utvecklardokumentationen för att [läs om produktkompatibilitet](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html).

## Uppdateringar av tjänster som stöds

I versionsinformationen beskrivs funktionsändringar och korrigeringar för tillägg som används av Audience Activation.

+++Supported service updates

_15 augusti 2023_

![Korrigera](../assets/new.svg) - Uppdaterade [Real-Time CDP Auditions dashboard](#real-time-cdp-audiences-dashboard) för att förenkla filtreringen.

_27 juni 2023_

![Korrigera](../assets/fix.svg) - Stöd för PHP 8.2 har lagts till i `magento/module-data-services-graphql` paket.

_30 maj 2023_

![Nytt](../assets/new.svg) - Uppdaterade [Real-Time CDP Auditions dashboard](#real-time-cdp-audiences-dashboard) så att du kan sortera, söka efter och filtrera de aktiva målgrupperna i din Adobe Commerce-instans.

+++

### 2.0.0

[!BADGE Kompatibilitet]{type=Informative tooltip="Kompatibilitet"}

_10 oktober 2023_

![Nytt](../assets/new.svg) - Stöd för OAuth 2.0 har lagts till när du [konfigurera](#configure-the-extension) tillägget Audience Activation.
![Korrigera](../assets/fix.svg) - Förbättrad stabilitet.

### 1.2.0

[!BADGE Kompatibilitet]{type=Informative tooltip="Kompatibilitet"}

_15 augusti 2023_

![Korrigera](../assets/fix.svg) - Uppdaterade UI-komponentens version.

### 1.1.0

_30 maj 2023_

[!BADGE Kompatibilitet]{type=Informative tooltip="Kompatibilitet"}

![Nytt](../assets/new.svg) - Stöd för [dynamiska block](#headless-support) i en headless storefront.

### 1.0.1

_11 maj 2023_

[!BADGE Kompatibilitet]{type=Informative tooltip="Kompatibilitet"}

![Korrigera](../assets/fix.svg) - Korrigerade ett problem där en dynamisk spärr- eller kundvagnsprisregel inte tillämpades på butiken.
![Korrigera](../assets/fix.svg) - Korrigerade ett problem där en okonfigurerad installation av tillägget Audience Activation orsakade ett fel när en handlare försökte skapa eller uppdatera ett dynamiskt block.

### 1.0.0

_31 mars 2023_

[!BADGE Kompatibilitet]{type=Informative tooltip="Kompatibilitet"}

![Nytt](../assets/new.svg) - Allmän tillgänglighetsrelease

## Implementering

Följande uppgifter gäller både Luma-implementeringar och implementeringar utan headless storefront. Om du vill aktivera målgrupper i Adobe Commerce måste du:

- Installera Adobe Commerce version 2.4.4 eller senare
- [Aktivera](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Adobe Commerce som mål i Real-Time CDP
- [Installera](#install-the-extension) den [!DNL Audience Activation] i Admin
- [Konfigurera](#configure-the-extension) den [!DNL Audience Activation] i Admin

### Installera tillägget

Installera [!DNL Audience Activation] tillägg från [marknadsplats](https://commercemarketplace.adobe.com/magento-audiences.html)eller kör följande kommando:

```bash
composer require magento/audiences
```

### Konfigurera tillägget

När du har installerat [!DNL Audience Activation] måste du logga in i din Commerce Admin och slutföra följande:

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL Commerce Services Connector]**.

1. [Logga in](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#organizationid) till ditt Adobe-konto och välj ditt företags-ID.

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL [!DNL Data Connection]]**.

1. I **[!UICONTROL Datastream ID]** -fältet, klistra in ID:t för den datastream som du skapade när du [aktiverad](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html#parameters) Adobe Commerce som destination i Real-Time CDP.

   Den här datastreamen skickar data från din Commerce-webbplats till Real-Time CDP för att avgöra om en kund tillhör en målgrupp. Om du ännu inte har skapat en datastream, [skapa](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#create) en i Experience Platform, [lägg till](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) till Commerce-destinationen i Real-Time CDP och till [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) i Admin.

   >[!NOTE]
   >
   >När du anger ett datastream-ID [associera den med en specifik webbplats](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) i [!DNL Data Connection] tillägg. Om din Commerce Store har flera webbplatser, [skapa ett mål](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) för varje webbplats i Real-Time CDP och använd olika datastream-ID för varje.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Services]** och markera **[!UICONTROL [!DNL Data Connection]]**.

1. I [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#send-historical-order-data) följ steg 1: **Skapa ett projekt i Adobe Developer Console** och 2: **Hämta konfigurationsfil**. Resultatet är en fil som du kopierar och klistrar in i **[!UICONTROL [!DNL Data Connection]]** konfigurationssida:

   ![Konfiguration av Real-Time CDP Audience Admin](./assets/epc-admin-config.png){width="700" zoomable="yes"}

1. Klicka **Spara konfiguration**.

Med målgrupper aktiverade för er Adobe Commerce-instans kan ni

- [Skapa en kundvagnsprisregel](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) informerad av målgrupper
- [Skapa ett dynamiskt block](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) informerad av målgrupper

## Real-Time CDP målgruppspanel

Du kan visa alla aktiva målgrupper som är tillgängliga för anpassning i din Adobe Commerce-instans med **Real-Time CDP-målgrupper** kontrollpanel. Alla målgrupper du [aktiverad](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html) i Adobe Commerce-destinationen i Real-Time CDP visas på den här instrumentpanelen.

Så här öppnar du **Real-Time CDP-målgrupper** kontrollpanelen, gå till _Administratör_ sidebar, sedan går du till **[!UICONTROL Customers]** > **[!UICONTROL Real-time CDP Audience]**.

Kontrollpanelen innehåller följande fält:

| Kolumn | Beskrivning |
|--- |--- |
| `Hide filters` | Gör att du kan visa eller dölja alla filter som du kan använda på kontrollpanelen. Det enda filter du kan använda är `Last updated`. Med det här filtret kan du välja ett datumintervall för målgrupper baserat på när de senast uppdaterades. |
| `Search` | Gör att du kan söka efter aktiva målgrupper i din Commerce-instans. |
| `Name` | Namn som ges till målgruppen i Real-Time CDP. |
| `Origin` | Anger varifrån målgruppen kommer, till exempel `Experience Platform`. |
| `Last updated` | Anger när målgruppen ändrades i Real-Time CDP. |
| `Sync now` | Hämtar nya eller uppdaterade målgrupper från Real-Time CDP. |
| `Customize table` | Här kan du visa eller dölja `Origin` och `Last updated` kolumner. |

{style="table-layout:auto"}

## Headless-support

Du kan aktivera målgrupper i en headless Adobe Commerce-instans, som AEM och PWA, för att visa kundvagnsprisregler eller dynamiska block baserade på målgrupperna.

### Kundprisregler

För kundvagnsprisregler kommunicerar en headless store till Experience Platform via [Commerce integration framework (CIF)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html). Ramverket innehåller ett API på serversidan som implementeras med GraphQL. Målgruppsinformation, t.ex. en kunds segment, skickas till Commerce via en GraphQL-huvudparameter med namnet: `aep-segments-membership`.

Den övergripande arkitekturen är följande:

![Skicka data från Headless Store till Backend](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

Efter dig [installera](#install-the-extension) och [konfigurera](#configure-the-extension) Experience Platform Web SDK innehåller även målgruppsinformation i form av medlemskap i segment.

Om du vill hämta segmentmedlemskap från SDK läser du följande [kodfragment](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes).

När segmenten har hämtats kan du skicka dem till Commerce i GraphQL-huvudet. Exempel:

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```

### Dynamiska block

För dynamiska block, GraphQL `dynamicBlocks` frågor kan innehålla `audience_id` input-attribut. Om du anger ett eller flera `audience_id` värden i en `dynamicBlocks` returnerar den en lista med dynamiska block som tilldelats dessa målgrupper.

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

Läs mer om `dynamicBlocks` GraphQL-fråga i [dokumentation för utvecklare](https://developer.adobe.com/commerce/webapi/graphql/schema/store/queries/dynamic-blocks/).

## Hämta målgrupper med Adobe Experience Platform Mobile SDK

Innan du kan hämta Real-Time CDP-målgrupper med Adobe Experience Platform Mobile SDK måste du [installera och konfigurera SDK för din mobila handelsplats](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/mobile-sdk-epc.html).

>[!IMPORTANT]
>
>Adobe Experience Platform Mobile SDK för iOS har stöd för iOS 11 eller senare.

När du är klar med konfigurationen kan du använda SDK-åtgärder för mobilen för att hämta målgruppsdata. Exempel:

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

När data har hämtats kan ni använda dem för att skapa målgruppsinformation [kundprisregler](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) och [dynamiska block](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) i Commerce.
