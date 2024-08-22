---
title: '[!DNL Google Tag Manager]'
description: Lär dig hur du använder  [!DNL Google Tag Manager] för att hantera många taggar (kodfragment) som är relaterade till marknadsföringskampanjerna på dina Adobe Commerce-webbplatser.
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: be426ca16fb7a72ebeda4a2f92c0f0062a9acc62
workflow-type: tm+mt
source-wordcount: '1050'
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

   - Under _[!UICONTROL Advertising Features]_anger du **[!UICONTROL Enable Demographics and Interest Reports]**till `On`.

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

1. Klicka på **[!UICONTROL New]** under **[!UICONTROL Choose workspace]**.

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

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Google API]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Google Analytics]** och konfigurera följande:

   ![Försäljningskonfiguration - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL Enable]** till `Yes`.

   - Ange **[!UICONTROL Account type]** till `Google Tag Manager`.

   - Ange ditt GTM-ID (`GTM-xxxxxx`) i fältet **[!UICONTROL Container ID]**.

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
| [!UICONTROL Enable Content Experiments] | Butiksvy | Aktiverar Google Content Experiments, som kan användas för att testa upp till tio olika versioner av samma sida. Alternativ: `Yes` / `No` |
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

1. Klicka på **[!UICONTROL Add a new tag]** i rutan **[!UICONTROL New Tag]**.

1. Hämta följande information från ditt AdWords-konto:

   - Konverterings-ID
   - Konverteringsetikett

   Om du behöver hjälp kan du gå till Google [supportwebbplats](https://support.google.com/tagmanager/answer/6105160).

1. Klicka på **[!UICONTROL Google AdWords]** på kontrollpanelen [!DNL Google Tag Manager] och gör följande:

   - Klicka på titelplatshållaren och ange ett namn för den nya taggen.

   - Välj **[!UICONTROL Google AdWords]** under **[!UICONTROL Choose Product]**.

   - Under _[!UICONTROL Choose a Tag Type]_väljer du **[!UICONTROL AdWords Conversion Tracking]**och klickar på&#x200B;**[!UICONTROL Continue]**.

1. Ange **[!UICONTROL Conversion ID]** och **[!UICONTROL Conversion Label]** från ditt AdWords-konto och klicka på **[!UICONTROL Continue]**.

### Steg 2. Skapa en regel

Om du fortsätter från kontrollpanelen [!DNL Google Tag Manager] är nästa steg att skapa en regel som aktiverar taggen på konverteringssidan.

1. Klicka på **[!UICONTROL Some Pages]** under **[!UICONTROL Fire On]**.

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
