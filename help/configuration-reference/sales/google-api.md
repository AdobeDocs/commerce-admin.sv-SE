---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Google API]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Sales] &gt; [!UICONTROL Google API] i Commerce Admin.
exl-id: 5031ad3d-1c9a-4bc6-9bfa-683414dca979
feature: Configuration, Marketing Tools
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Google API]

{{config}}

## [!UICONTROL Google Analytics]

![Google Analytics](./assets/google-api-analytics-ee.png)<!-- zoom -->

<!-- [Google Analytics](https://docs.magento.com/user-guide/marketing/google-universal-analytics.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Butiksvy | Aktiverar [!DNL Google Analytics] för din butik. Alternativ: `Yes` / `No` |
| [!UICONTROL Account Type] | Butiksvy | ![Adobe Commerce](../../assets/adobe-logo.svg) (endast Adobe Commerce) Anger konfigurationsalternativen enligt din kontotyp för Google Analytics. Alternativ: Universal Analytics (standard)/Google Tag Manager |
| [!UICONTROL Account Number] | Butiksvy | Kontonumret, eller spårningskoden, som tilldelades när du skapade ditt [!DNL Google Analytics]-konto. |
| [!UICONTROL Anonymize IP] | Butiksvy | Avgör om identifieringsinformation tas bort från IP-adresser som visas i [!DNL Google Analytics]-resultat. |
| [!UICONTROL Enable Content Experiments] | Butiksvy | Aktiverar [Google Content Experiments](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207) som kan användas för att testa upp till tio olika versioner av samma sida. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Google Analytics - Google Tag Manager]

{{ee-feature}}

![Google Analytics - Google Tag Manager-kontotyp](./assets/google-api-analytics-tag-manager.png)<!-- zoom -->

När **[!UICONTROL Account Type]** är inställt på `Google Tag Manager` visas ytterligare fält.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container ID] | Butiksvy | Unikt ID för behållaren [!DNL Google Tag Manager]. Det här värdet börjar vanligtvis med `GTM-`. Detta ID finns i ditt [!DNL Google Tag Manager]-konto. Om [!DNL Google Tag Manager] redan är installerat och konfigurerat för din butik visas behållar-ID:t automatiskt i det här fältet. |
| [!UICONTROL List property for the catalog page] | Butiksvy | Identifierar egenskapen [!DNL Google Tag Manager] som är associerad med katalogsidan. Standardvärde: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Butiksvy | Identifierar egenskapen [!DNL Google Tag Manager] som är associerad med korsförsäljningsblocket. Standardvärde: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Butiksvy | Identifierar egenskapen [!DNL Google Tag Manager] som är associerad med merförsäljningsblocket. Standardvärde: `Up-sell` |
| [!UICONTROL List property for the related products block] | Butiksvy | Identifierar egenskapen [!DNL Google Tag Manager] som är associerad med det relaterade produktblocket. Standardvärde: `Related Products` |
| [!UICONTROL List property for the search results page] | Butiksvy | Identifierar egenskapen [!DNL Google Tag Manager] som är associerad med sökresultatsidan. Standardvärde: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Butiksvy | Identifierar egenskapen [!DNL Google Tag Manager] som är associerad med etiketterna för interna kampanjer. Standardvärde: `Label` |

{style="table-layout:auto"}

## [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-google-adwords.png)<!-- zoom -->

<!-- [Google AdWords](https://docs.magento.com/user-guide/marketing/google-adwords.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Butiksvy | Aktiverar Google AdWords för butiken. Alternativ: `Yes` / `No` |
| [!UICONTROL Conversion ID] | Butiksvy | ID från ditt Google AdWords-konto. |
| [!UICONTROL Conversion Language] | Butiksvy | Språket som används för AdWords-konverteringar. Alternativ: `All available languages` |
| [!UICONTROL Conversion Format] | Butiksvy | Bestämmer formatet för det [!DNL Google Site Stats]-meddelande som visas på konverteringssidan. Meddelandet länkar till en sida som informerar besökarna om de cookies som används för att spåra deras besök. Det här numeriska värdet tilldelas variabeln `google_conversion_format` i ditt AdWords-skript. Mer information finns i [Om konverteringsspårning](https://support.google.com/google-ads/answer/1722022?hl=en) på Google webbplats. Alternativ: <br/>**`1`**- Visar ett enradsmeddelande.<br/>**`2`** - (Standard) Visar ett tvåradsmeddelande. <br/>**`3`**- Visar inget kundmeddelande. |
| [!UICONTROL Conversion Color] | Butiksvy | Bestämmer färgen på konverteringsetiketten. Använd en [färgväljare](https://www.w3schools.com/colors/colors_picker.asp) för att välja det hexadecimala värdet. Detta hexadecimala värde tilldelas variabeln `google_conversion_color` i ditt AdWords-skript. Till exempel: ffffff `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Butiksvy | En textetikett som visas med meddelandet [!DNL Google Site Stats]. Den här textsträngen tilldelas variabeln `~` i ditt AdWords-skript. Till exempel:&quot;Tack för att du handlar!&quot; |
| [!UICONTROL Conversion Value Type] | Butiksvy | Anger vilken typ av värde som används för att avgöra när en konvertering sker. Alternativ: <br/>**`Dynamic`**- Avgör att en konvertering har skett baserat på det dynamiska orderbeloppet.<br/>**`Constant`** - Avgör att en konvertering har skett baserat på det angivna värdet. |
| [!UICONTROL Conversion Value] | Butiksvy | Anger värdet som används för konverteringsvärdetypen _[!UICONTROL Constant]_. |
| [!UICONTROL Send Order Currency] | Butiksvy | Aktiverar transaktionsspecifika valutakonverteringsvärden i AdWords (för webbplatser med olika basvalutor). |

{style="table-layout:auto"}

## [!UICONTROL Google GTag]

{{gtag-api-note}}

### [!UICONTROL Google Analytics4]

![Google Analytics4](./assets/google-api-gtag-google-analytics4.png)<!-- zoom -->

<!-- [Google Analytics4](https://docs.magento.com/user-guide/marketing/google-universal-analytics.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Butiksvy | Aktiverar Google Analytics 4 för din butik. Alternativ: `Yes` / `No` |
| [!UICONTROL Account Type] | Butiksvy | ![Adobe Commerce](../../assets/adobe-logo.svg) (endast Adobe Commerce) Anger konfigurationsalternativen enligt din kontotyp för Google Analytics. Alternativ: `Google Analytics4` (standard) / `Google Tag Manager` |
| [!UICONTROL Measurement ID] | Butiksvy | Kontonumret, eller spårningskoden, som tilldelades när du skapade ditt Google Analytics-konto. |
| [!UICONTROL Anonymize IP] | Butiksvy | Avgör om identifieringsinformation tas bort från IP-adresser som visas i Google Analytics-resultat. |
| [!UICONTROL Enable Content Experiments] | Butiksvy | Aktiverar [Google Content Experiments](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207) som kan användas för att testa upp till tio olika versioner av samma sida. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Google Analytics4 - Google Tag Manager]

{{ee-feature}}

![Google Analytics4 - Google Tag Manager-kontotyp](./assets/google-api-gtag-google-analytics4-gtm.png)<!-- zoom -->

När **[!UICONTROL Account Type]** är inställt på `Google Tag Manager` visas ytterligare fält.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container Id] | Butiksvy | Unikt ID för behållaren [!DNL Google Tag Manager]. Det här värdet börjar vanligtvis med `GTM-`. Detta ID finns i ditt Google Tab Manager-konto. Om [!DNL Google Tag Manager] redan är installerat och konfigurerat för din butik visas behållar-ID:t automatiskt i det här fältet. |
| [!UICONTROL List property for the catalog page] | Butiksvy | Identifierar egenskapen [!DNL Google Tag Manager] som är associerad med katalogsidan. Standardvärde: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Butiksvy | Identifierar egenskapen [!DNL Google Tag Manager] som är associerad med korsförsäljningsblocket. Standardvärde: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Butiksvy | Identifierar egenskapen [!DNL Google Tag Manager] som är associerad med merförsäljningsblocket. Standardvärde: `Up-sell` |
| [!UICONTROL List property for the related products block] | Butiksvy | Identifierar egenskapen [!DNL Google Tag Manager] som är associerad med det relaterade produktblocket. Standardvärde: `Related Products` |
| [!UICONTROL List property for the search results page] | Butiksvy | Identifierar egenskapen [!DNL Google Tag Manager] som är associerad med sökresultatsidan. Standardvärde: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Butiksvy | Identifierar egenskapen [!DNL Google Tag Manager] som är associerad med etiketterna för interna kampanjer. Standardvärde: `Label` |

{style="table-layout:auto"}

### [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-gtag-google-adwords.png)<!-- zoom -->

<!-- -- Google AdWords](https://docs.magento.com/user-guide/marketing/google-adwords.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Butiksvy | Aktiverar Google AdWords för butiken. Alternativ: `Yes` / `No` |
| [!UICONTROL Conversion ID] | Butiksvy | ID från ditt Google AdWords-konto. |
| [!UICONTROL Conversion Language] | Butiksvy | Språket som används för AdWords-konverteringar. Alternativ: Alla tillgängliga språk |
| [!UICONTROL Conversion Format] | Butiksvy | Anger formatet för det Google Site Stats-meddelande som visas på konverteringssidan. Meddelandet länkar till en sida som informerar besökarna om de cookies som används för att spåra deras besök. Det här numeriska värdet tilldelas variabeln `google_conversion_format` i ditt AdWords-skript. Mer information finns i [Om konverteringsspårning](https://support.google.com/google-ads/answer/1722022?hl=en) på Google webbplats. Alternativ: <br/>**`1`**- Visar ett enradsmeddelande.<br/>**`2`** - (Standard) Visar ett tvåradsmeddelande. <br/>**`3`**- Visar inget kundmeddelande. |
| [!UICONTROL Conversion Color] | Butiksvy | Bestämmer färgen på konverteringsetiketten. Använd en [färgväljare](https://www.w3schools.com/colors/colors_picker.asp) för att välja det hexadecimala värdet. Detta hexadecimala värde tilldelas variabeln `google_conversion_color` i ditt AdWords-skript. Till exempel: ffffff `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Butiksvy | En textetikett som visas med meddelandet Google Site Stats. Den här textsträngen tilldelas variabeln `~` i ditt AdWords-skript. Till exempel:&quot;Tack för att du handlar!&quot; |
| [!UICONTROL Conversion Value Type] | Butiksvy | Anger vilken typ av värde som används för att avgöra när en konvertering sker. Alternativ: <br/>**`Dynamic`**- Avgör att en konvertering har skett baserat på det dynamiska orderbeloppet.<br/>**`Constant`** - Avgör att en konvertering har skett baserat på det angivna värdet. |
| [!UICONTROL Conversion Value] | Butiksvy | Anger värdet som används för konverteringsvärdetypen _[!UICONTROL Constant]_. |
| [!UICONTROL Send Order Currency] | Butiksvy | Aktiverar transaktionsspecifika valutakonverteringsvärden i AdWords (för webbplatser med olika basvalutor). |

{style="table-layout:auto"}
