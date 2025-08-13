---
title: '[!DNL Google Tag Manager]'
description: Lär dig hur du använder  [!DNL Google Tag Manager] för att hantera många taggar (kodfragment) som är relaterade till marknadsföringskampanjerna på dina Adobe Commerce-webbplatser.
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 9c25196367023a44fa76e441d485693493a4c058
workflow-type: tm+mt
source-wordcount: '1437'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] är ett kraftfullt verktyg som hjälper dig att hantera och distribuera olika taggar (kodfragment) som är kopplade till marknadsföringskampanjerna. [!DNL Google Tag Manager] ger dig möjlighet att lägga till spårningstaggar på din webbplats för att mäta målgruppen eller för att anpassa, återannonsera eller genomföra marknadsföringsinitiativ för sökmotorer.

[!DNL Google Tag Manager] överför data och händelser direkt till [!DNL Google Analytics], Enhanced Ecommerce och andra analyslösningar från tredje part för att få en tydlig bild av hur bra din webbplats, produkter och kampanjer fungerar.

Du måste ha ett [!DNL Google Analytics]- och [!DNL Tag Manager]-konto för att kunna fortsätta den här processen. Följande instruktioner hjälper dig genom processen att konfigurera dina Google-konton, konfigurera din Commerce Store och skapa en tagg.

>[!NOTE]
>
>Om ditt företag omfattas av sekretessbestämmelser som [General Data Protection Regulation](../getting-started/compliance-gdpr.md) och/eller [California Consumer Privacy Act](../getting-started/compliance-ccpa.md) kan du läsa [Google Privacy Settings](google-tools.md#google-privacy-settings).

## Steg 1. Konfigurera ditt [!DNL Google Analytics]-konto

Se [Konfigurera webbplatssökning](https://support.google.com/analytics/answer/1012264) i Google-hjälpen för information om grunderna för hur du kommer igång. Se även Google-guiderna för [Google Analytics](https://support.google.com/analytics/answer/9304153) och [Google Tag Manager](https://support.google.com/tagmanager/answer/6102821).

1. Logga in på ditt [!DNL Google Analytics]-konto.

1. Så här aktiverar du **[!UICONTROL Internal Site Search Tracking]**:

   - Navigera till **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - Ange **[!UICONTROL Site Search Tracking]** till `On`.

   - Ange parametern **[!UICONTROL Query]** till `q`.

   - När det är klart **[!UICONTROL Save]** inställningarna.

1. Så här aktiverar du visningsfunktioner:

   - Välj **[!UICONTROL Property Settings]**.

   - Under _[!UICONTROL Advertising Features]_&#x200B;anger du **[!UICONTROL Enable Demographics and Interest Reports]**&#x200B;till `On`.

   - **[!UICONTROL Save]** inställningarna.

1. Så här aktiverar du e-handelsspårning:

   - Navigera till **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

   - Ange **[!UICONTROL Enable Ecommerce]** till `On`.

   - Ange **[!UICONTROL Enable Enhanced Ecommerce Reporting]** till `On`.

   - **[!UICONTROL Save]** inställningarna.

1. Läs in sidan igen och verifiera att alla inställningar är kvar `On`.

   >[!NOTE]
   >
   >Om inte alla inställningar är `On` upprepar du de föregående stegen, sparar och läser in sidan igen. Upprepa den här processen tills alla inställningar är inställda på `On`.

## Steg 2. Konfigurera ditt [!DNL Google Tag Manager]-konto

Följande instruktioner visar hur du konfigurerar en ny behållare med de grundläggande inställningarna. Ett exempel på en [Composer](https://developer.adobe.com/commerce/php/development/composer/)-konfigurationsfil (.json) används för att förenkla processen, och import används för att generera en tagg i en ny behållare. I det här exemplet rekommenderas att du skapar en behållare i stället för att ändra en befintlig behållare.

>[!NOTE]
>
>Mer information finns i Google [Exportera och importera behållare](https://support.google.com/tagmanager/answer/6106997). De här instruktionerna innehåller en genomgång för att importera ett JSON-prov i en ny behållare.

1. Hämta den länkade filen [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt), öppna filen i en redigerare och spara den som `GTM_M2_Config.json`.

   JSON-filen överförs direkt till [!DNL Google Tag Manager].

1. Navigera till **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**.

1. Klicka på **[!UICONTROL Choose container file]** och markera json-filen.

1. Klicka på **[!UICONTROL Choose workspace]** under **[!UICONTROL New]**.

1. Ange en titel och en beskrivning och klicka sedan på **[!UICONTROL Save]**.

1. Om du vill importera filen väljer du en av följande åtgärder:

   - Alternativet **[!UICONTROL Overwrite]** bör väljas för en ny behållare.

   - Alternativet **[!UICONTROL Merge]** bör vara markerat om du använder en befintlig behållare.

1. Klicka på **[!UICONTROL Preview]** om du vill granska taggarna, utlösarna och variablerna.

1. Så här redigerar du **[!UICONTROL Google Analytics ID]** som refereras i variabler:

   - Navigera till **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**.

   - Välj **[!UICONTROL Google Analytics]** och uppdatera platshållaren (`UA-xxxxxx-x`) med din egen **[!UICONTROL GA ID]**.

1. Följ Google instruktioner för hur du lägger till taggar, utlösare och variabler i den nya behållaren.

   Om du har inställningar i en annan behållare som du vill använda kan de flyttas till den nya behållaren.

1. Klicka på **[!UICONTROL Confirm]** när du är klar.

1. Följ Google anvisningar för hur du publicerar den nya behållaren.

## Steg 3. Konfigurera din butik

{{gtag-api-note}}

1. Logga in på administratören för din Commerce-butik.

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_&#x200B;Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Google API]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Google Analytics]** och konfigurera följande:

   ![Försäljningskonfiguration - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL Enable]** till `Yes`.

   - Ange **[!UICONTROL Account type]** till `Google Tag Manager`.

   - Ange ditt GTM-ID (**[!UICONTROL Container ID]**) i fältet `GTM-xxxxxx`.

   - Om du även använder Google Analytics för innehållsexperiment anger du **Aktivera innehållsexperiment** till `Yes`.

   - Använd standardvärdena för de återstående fälten.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

1. Testa dina [!DNL Google Tag Manager]-inställningar och verifiera att allt fungerar som det ska.

>[!NOTE]
>
>Varje behållare är kopplad till en webbplats och du behöver bara en behållare per konto. Om du har en Commerce-instans med flera platser behöver du separata behållare.

## Fältbeskrivningar

| Fält | Omfång | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable] | Butiksvy | Avgör om Google Analytics Enhanced Ecommerce kan användas för att analysera aktiviteter i din butik. Alternativ: `Yes` / `No` |
| [!UICONTROL Account type] | Butiksvy | Anger den spårningskod för Google som används för att övervaka butiksaktivitet och trafik. Alternativ: `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | Butiksvy | Avgör om identifieringsinformation tas bort från IP-adresser som visas i Google Analytics-resultat. |
| [!UICONTROL Container Id] | Butiksvy | Om [!DNL Google Tag Manager] redan är installerat och konfigurerat för din butik visas behållar-ID:t automatiskt i det här fältet. |
| [!UICONTROL List property for the catalog page] | Butiksvy | Identifierar tagghanterarens egenskap som är associerad med katalogsidan. Standardvärde: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Butiksvy | Identifierar tagghanterarens egenskap som är associerad med korsförsäljningsblocket. Standardvärde: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Butiksvy | Identifierar tagghanterarens egenskap som är associerad med merförsäljningsblocket. Standardvärde: `Up-sell` |
| [!UICONTROL List property for the related products block] | Butiksvy | Identifierar tagghanterarens egenskap som är associerad med det relaterade produktblocket. Standardvärde: `Related Products` |
| [!UICONTROL List property for the search results page] | Butiksvy | Identifierar tagghanterarens egenskap som är associerad med sökresultatsidan. Standardvärde: `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | Butiksvy | Identifierar tagghanterarens egenskap som är associerad med etiketterna för interna kampanjer. Standardvärde: `Label` |

{style="table-layout:auto"}

## Skapa en tagg för att spåra konverteringar

Om du har ett Google AdWords-konto kan du skapa en tagg som spårar konverteringar. I följande exempel visas hur du använder både [!DNL Google Tag Manager] och [!DNL Google Analytics] för att skapa en tagg som aktiveras på din butiks konverteringssida _Success_.

### Steg 1. Skapa en tagg

1. Logga in på ditt [!DNL Google Tag Manager]-konto och klicka på länken för den behållare som du skapade för din butik.

1. Klicka på **[!UICONTROL New Tag]** i rutan **[!UICONTROL Add a new tag]**.

1. Hämta följande information från ditt AdWords-konto:

   - Konverterings-ID
   - Konverteringsetikett

   Om du behöver hjälp kan du gå till Google [supportwebbplats](https://support.google.com/tagmanager/answer/6105160).

1. Klicka på [!DNL Google Tag Manager] på kontrollpanelen **[!UICONTROL Google AdWords]** och gör följande:

   - Klicka på titelplatshållaren och ange ett namn för den nya taggen.

   - Välj **[!UICONTROL Choose Product]** under **[!UICONTROL Google AdWords]**.

   - Under _[!UICONTROL Choose a Tag Type]_&#x200B;väljer du **[!UICONTROL AdWords Conversion Tracking]**&#x200B;och klickar på&#x200B;**[!UICONTROL Continue]**.

1. Ange **[!UICONTROL Conversion ID]** och **[!UICONTROL Conversion Label]** från ditt AdWords-konto och klicka på **[!UICONTROL Continue]**.

### Steg 2. Skapa en regel

Om du fortsätter från kontrollpanelen [!DNL Google Tag Manager] är nästa steg att skapa en regel som aktiverar taggen på konverteringssidan.

1. Klicka på **[!UICONTROL Fire On]** under **[!UICONTROL Some Pages]**.

1. Fyll i följande inställningar i avsnittet _[!UICONTROL Choose Pages]_:

   - **[!UICONTROL Name]** - Ange ett namn för sidbeskrivningen.

   - **[!UICONTROL Variable]** `url`

   - **Åtgärd** - `matches RegEx`

     Mer information finns i [Regex- och CSS-väljaroperatorer](https://support.google.com/tagmanager/answer/7679109) i hjälpen för Google Tag Manager.

   - **[!UICONTROL Value]** - `checkout/success.*`

1. Markera den gröna kryssrutan och klicka på **[!UICONTROL Save]**.

   Utlösaren som du ställer in visas som en blå knapp i avsnittet Elden på.

1. Klicka på **[!UICONTROL Save Tag]** när du är klar.

### Steg 3. Förhandsgranska och publicera

Nästa steg i processen är att förhandsgranska taggen. Varje gång taggen förhandsgranskas sparas en ögonblicksbild av versionen. När du är nöjd med resultaten går du till den version som du vill använda och klickar på **[!UICONTROL Publish]**.

## Anpassad HTML-tagg med JavaScript

I det här avsnittet beskrivs hur du lägger till en CSP-notation i JavaScript för anpassade HTML-taggar för körning på utcheckningssidan, och ser till att kraven i Content Security Policy (CSP) uppfylls. Det här tillägget förbättrar webbplatsens säkerhet genom att förhindra att obehöriga skript körs. Mer information finns i dokumentationen till [Content Security Policy](https://developer.adobe.com/commerce/php/development/security/content-security-policies).

>[!NOTE]
>
>Import av den globala variabeln `cspNonce` till Google Tag Manager stöds endast i Adobe Commerce version 2.4.8 och senare.

>[!WARNING]
>
>Om du lägger till okända skript i din butik kan det innebära en risk för att data äventyras. Skript som är auktoriserade på utcheckningssidan kan stjäla känslig kundinformation, inklusive betalningsinformation. Du måste vidta försiktighetsåtgärder för att skydda ditt Google Tag Manager-konto. Lägg bara till betrodda skript, granska och granska taggar regelbundet och implementera kraftfulla säkerhetsåtgärder som tvåfaktorsautentisering (2FA) och åtkomstkontroller.

### Steg 1. Skapa en CSP Nonce-variabel

Du kan skapa en CSP Nonce-variabel som kan användas i din Google Tag Manager genom att importera variabelkonfigurationen eller konfigurera den manuellt.

#### Importera variabelkonfigurationen

CSP Nonce-variabeln ingår i exempelbehållaren [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt). Du kan skapa variabeln genom att importera koden till arbetsytan.

#### Skapa variabeln manuellt

Om du inte kan importera variabelkonfigurationen följer du stegen nedan för att skapa den.

1. Gå till avsnittet **Variabler** i sidlisten på arbetsytan.
1. Klicka på knappen **Ny** längst ned på sidan i avsnittet **Användardefinierade variabler**.
1. Ge variabeln `gtmNonce` ett namn.
1. Klicka på pennikonen för att redigera variabeln.
1. Välj **JavaScript-variabel** i avsnittet **Sidvariabel**.
1. Ange **i fältet** Global variabelnamn`window.cspNonce`.
1. Spara variabeln.

Mer information om [Google Tag Manager-variabler](https://support.google.com/tagmanager/answer/7683056?hl=en) finns i [Användardefinierade variabeltyper för webben](https://support.google.com/tagmanager/answer/7683362?hl=en) i Google-dokumentationen. Den här dokumentationen ger detaljerad vägledning om hur du skapar och hanterar anpassade variabler för att skräddarsy tagghanteringen för specifika marknadsförings- och analysbehov.

### Steg 2. Skapa en anpassad HTML-tagg

1. Gå till avsnittet **Taggar** i sidlisten på arbetsytan.
1. Klicka på knappen **Ny**.
1. I avsnittet **Taggkonfiguration** väljer du **Egen HTML-tagg**.
1. Ange din obligatoriska JavaScript i textområdet och lägg till ett nonce-attribut till den inledande `<script>`-taggen som pekar på variabeln som du skapade i föregående steg. Exempel:

   ```html
   <script nonce="{{gtmNonce}}">
       // Your JavaScript code here
   </script>
   ```

1. Välj **Supportdokument.write**.
1. Välj önskad utlösare i avsnittet **Utlösare**. Till exempel **Samtyckesinitiering - alla sidor**.

Mer information om [taggar](https://support.google.com/tagmanager/answer/3281060) i Google Tag Manager finns i [Anpassade taggar](https://support.google.com/tagmanager/answer/6107167) i Google-dokumentationen.
