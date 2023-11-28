---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Google API]'
description: Granska konfigurationsinställningarna på [!UICONTROL Sales] &gt; [!UICONTROL Google API] sidan för Commerce Admin.
exl-id: 5031ad3d-1c9a-4bc6-9bfa-683414dca979
feature: Configuration, Marketing Tools
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Google API]

{{config}}

## [!UICONTROL Google Analytics]

![Google Analytics](./assets/google-api-analytics-ee.png)<!-- zoom -->

<!-- [Google Analytics](https://docs.magento.com/user-guide/marketing/google-universal-analytics.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Butiksvy | Aktiverar [!DNL Google Analytics] för er butik. Alternativ: `Yes` / `No` |
| [!UICONTROL Account Type] | Butiksvy | ![Adobe Commerce](../../assets/adobe-logo.svg) (Endast Adobe Commerce) Anger konfigurationsalternativen enligt din kontotyp för Google Analytics. Alternativ: Universal Analytics (standard)/Google Tag Manager |
| [!UICONTROL Account Number] | Butiksvy | Kontonumret, eller spårningskoden, som tilldelades när du skapade [!DNL Google Analytics] konto. |
| [!UICONTROL Anonymize IP] | Butiksvy | Avgör om identifieringsinformation tas bort från IP-adresser som visas i [!DNL Google Analytics] resultat. |
| [!UICONTROL Enable Content Experiments] | Butiksvy | Aktiverar [Google Content Experiments](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207), som kan användas för att testa upp till tio olika versioner av samma sida. Alternativ: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Google Analytics - Google Tag Manager]

{{ee-feature}}

![Google Analytics - kontotypen Google Tag Manager](./assets/google-api-analytics-tag-manager.png)<!-- zoom -->

När **[!UICONTROL Account Type]** är inställd på `Google Tag Manager`visas ytterligare fält.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container ID] | Butiksvy | Unikt ID för [!DNL Google Tag Manager] behållare. Det här värdet börjar vanligtvis med `GTM-`. Detta ID finns i din [!DNL Google Tag Manager] konto. If [!DNL Google Tag Manager] redan är installerat och konfigurerat för din butik visas behållar-ID automatiskt i det här fältet. |
| [!UICONTROL List property for the catalog page] | Butiksvy | Anger [!DNL Google Tag Manager] egenskap som är associerad med katalogsidan. Standardvärde: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Butiksvy | Anger [!DNL Google Tag Manager] egenskap som är associerad med korsförsäljningsblocket. Standardvärde: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Butiksvy | Anger [!DNL Google Tag Manager] egenskap som är associerad med merförsäljningsblocket. Standardvärde: `Up-sell` |
| [!UICONTROL List property for the related products block] | Butiksvy | Anger [!DNL Google Tag Manager] egenskap som är associerad med det relaterade produktblocket. Standardvärde: `Related Products` |
| [!UICONTROL List property for the search results page] | Butiksvy | Anger [!DNL Google Tag Manager] egenskap som är associerad med sökresultatsidan. Standardvärde: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Butiksvy | Anger [!DNL Google Tag Manager] egenskap som är associerad med etiketterna för interna kampanjer. Standardvärde: `Label` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Google AdWords]

![Google AdWord](./assets/google-api-google-adwords.png)<!-- zoom -->

<!-- [Google AdWords](https://docs.magento.com/user-guide/marketing/google-adwords.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Butiksvy | Aktiverar Google AdWords för butiken. Alternativ: `Yes` / `No` |
| [!UICONTROL Conversion ID] | Butiksvy | ID från ditt Google AdWords-konto. |
| [!UICONTROL Conversion Language] | Butiksvy | Språket som används för AdWords-konverteringar. Alternativ: `All available languages` |
| [!UICONTROL Conversion Format] | Butiksvy | Bestämmer formatet för [!DNL Google Site Stats] meddelande som visas på konverteringssidan. Meddelandet länkar till en sida som informerar besökarna om de cookies som används för att spåra deras besök. Det här numeriska värdet tilldelas `google_conversion_format` i ditt AdWords-skript. Mer information finns på [Om konverteringsspårning](https://support.google.com/google-ads/answer/1722022?hl=en) på Google webbplats. Alternativ: <br/>**`1`**- Visar en enradig avisering.<br/>**`2`** - (Standard) Visar ett tvåradsmeddelande. <br/>**`3`**- Visar inget kundmeddelande. |
| [!UICONTROL Conversion Color] | Butiksvy | Bestämmer färgen på konverteringsetiketten. Använd en [färgväljare](https://www.w3schools.com/colors/colors_picker.asp) för att välja det hexadecimala värdet. Detta hexadecimala värde tilldelas `google_conversion_color` i ditt AdWords-skript. Till exempel: ffffff  `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Butiksvy | En textetikett som visas med [!DNL Google Site Stats] meddelande. Den här textsträngen tilldelas `~` i ditt AdWords-skript. Till exempel:&quot;Tack för att du handlar!&quot; |
| [!UICONTROL Conversion Value Type] | Butiksvy | Anger vilken typ av värde som används för att avgöra när en konvertering sker. Alternativ: <br/>**`Dynamic`**- Avgör att en konvertering har skett baserat på det dynamiska orderbeloppet.<br/>**`Constant`** - Anger att en konvertering har skett baserat på det angivna värdet. |
| [!UICONTROL Conversion Value] | Butiksvy | Anger värdet som används för en _[!UICONTROL Constant]_konverteringsvärdetyp. |
| [!UICONTROL Send Order Currency] | Butiksvy | Aktiverar transaktionsspecifika valutakonverteringsvärden i AdWords (för webbplatser med olika basvalutor). |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Google GTag]

{{gtag-api-note}}

### [!UICONTROL Google Analytics4]

![Google Analytics4](./assets/google-api-gtag-google-analytics4.png)<!-- zoom -->

<!-- [Google Analytics4](https://docs.magento.com/user-guide/marketing/google-universal-analytics.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Butiksvy | Aktiverar Google Analytics 4 för din butik. Alternativ: `Yes` / `No` |
| [!UICONTROL Account Type] | Butiksvy | ![Adobe Commerce](../../assets/adobe-logo.svg) (Endast Adobe Commerce) Anger konfigurationsalternativen enligt din kontotyp för Google Analytics. Alternativ: `Google Analytics4` (standard) / `Google Tag Manager` |
| [!UICONTROL Measurement ID] | Butiksvy | Kontonumret, eller spårningskoden, som tilldelades när du skapade ditt Google Analytics-konto. |
| [!UICONTROL Anonymize IP] | Butiksvy | Avgör om identifieringsinformation tas bort från IP-adresser som visas i Google Analytics-resultat. |
| [!UICONTROL Enable Content Experiments] | Butiksvy | Aktiverar [Google Content Experiments](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207), som kan användas för att testa upp till tio olika versioner av samma sida. Alternativ: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Google Analytics4 - Google Tag Manager]

{{ee-feature}}

![Google Analytics 4 - kontotypen Google Tag Manager](./assets/google-api-gtag-google-analytics4-gtm.png)<!-- zoom -->

När **[!UICONTROL Account Type]** är inställd på `Google Tag Manager`visas ytterligare fält.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container Id] | Butiksvy | Unikt ID för [!DNL Google Tag Manager] behållare. Det här värdet börjar vanligtvis med `GTM-`. Detta ID finns i ditt Google Tab Manager-konto. If [!DNL Google Tag Manager] redan är installerat och konfigurerat för din butik visas behållar-ID automatiskt i det här fältet. |
| [!UICONTROL List property for the catalog page] | Butiksvy | Anger [!DNL Google Tag Manager] egenskap som är associerad med katalogsidan. Standardvärde: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Butiksvy | Anger [!DNL Google Tag Manager] egenskap som är associerad med korsförsäljningsblocket. Standardvärde: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Butiksvy | Anger [!DNL Google Tag Manager] egenskap som är associerad med merförsäljningsblocket. Standardvärde: `Up-sell` |
| [!UICONTROL List property for the related products block] | Butiksvy | Anger [!DNL Google Tag Manager] egenskap som är associerad med det relaterade produktblocket. Standardvärde: `Related Products` |
| [!UICONTROL List property for the search results page] | Butiksvy | Anger [!DNL Google Tag Manager] egenskap som är associerad med sökresultatsidan. Standardvärde: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Butiksvy | Anger [!DNL Google Tag Manager] egenskap som är associerad med etiketterna för interna kampanjer. Standardvärde: `Label` |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Google AdWords]

![Google AdWord](./assets/google-api-gtag-google-adwords.png)<!-- zoom -->

<!-- -- Google AdWords](https://docs.magento.com/user-guide/marketing/google-adwords.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Butiksvy | Aktiverar Google AdWords för butiken. Alternativ: `Yes` / `No` |
| [!UICONTROL Conversion ID] | Butiksvy | ID från ditt Google AdWords-konto. |
| [!UICONTROL Conversion Language] | Butiksvy | Språket som används för AdWords-konverteringar. Alternativ: Alla tillgängliga språk |
| [!UICONTROL Conversion Format] | Butiksvy | Anger formatet för det Google Site Stats-meddelande som visas på konverteringssidan. Meddelandet länkar till en sida som informerar besökarna om de cookies som används för att spåra deras besök. Det här numeriska värdet tilldelas `google_conversion_format` i ditt AdWords-skript. Mer information finns på [Om konverteringsspårning](https://support.google.com/google-ads/answer/1722022?hl=en) på Google webbplats. Alternativ: <br/>**`1`**- Visar en enradig avisering.<br/>**`2`** - (Standard) Visar ett tvåradsmeddelande. <br/>**`3`**- Visar inget kundmeddelande. |
| [!UICONTROL Conversion Color] | Butiksvy | Bestämmer färgen på konverteringsetiketten. Använd en [färgväljare](https://www.w3schools.com/colors/colors_picker.asp) för att välja det hexadecimala värdet. Detta hexadecimala värde tilldelas `google_conversion_color` i ditt AdWords-skript. Till exempel: ffffff  `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Butiksvy | En textetikett som visas med meddelandet Google Site Stats. Den här textsträngen tilldelas `~` i ditt AdWords-skript. Till exempel:&quot;Tack för att du handlar!&quot; |
| [!UICONTROL Conversion Value Type] | Butiksvy | Anger vilken typ av värde som används för att avgöra när en konvertering sker. Alternativ: <br/>**`Dynamic`**- Avgör att en konvertering har skett baserat på det dynamiska orderbeloppet.<br/>**`Constant`** - Anger att en konvertering har skett baserat på det angivna värdet. |
| [!UICONTROL Conversion Value] | Butiksvy | Anger värdet som används för en _[!UICONTROL Constant]_konverteringsvärdetyp. |
| [!UICONTROL Send Order Currency] | Butiksvy | Aktiverar transaktionsspecifika valutakonverteringsvärden i AdWords (för webbplatser med olika basvalutor). |

{:style=&quot;table-layout:auto&quot;}
