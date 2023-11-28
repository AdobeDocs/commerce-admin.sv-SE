---
title: '[!DNL Google Tag Manager]'
description: Lär dig använda [!DNL Google Tag Manager] för att hantera många taggar (kodavsnitt) som är relaterade till era marknadsföringskampanjer på era Adobe Commerce-webbplatser.
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '1161'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] hjälper er att hantera de många taggar (kodavsnitt) som hör till era marknadsföringskampanjer. [!DNL Google Tag Manager] ger er möjlighet att lägga till spårningstaggar på er webbplats för att mäta målgruppen eller för att personalisera, återmarknadsföra eller genomföra marknadsföringssatsningar i sökmotorer.

[!DNL Google Tag Manager] direkt överför data och händelser till [!DNL Google Analytics], Enhanced Ecommerce och andra analyslösningar från tredje part som ger en tydlig bild av hur bra er webbplats, produkter och kampanjer fungerar.

Du borde ha en [!DNL Google Analytics] och [!DNL Tag Manager] för att fortsätta processen. Följande instruktioner hjälper dig genom processen att konfigurera dina Google-konton, konfigurera din Commerce Store och skapa en tagg.

>[!NOTE]
>
>Om ditt företag omfattas av sekretessbestämmelser som [Allmän dataskyddsförordning](../getting-started/compliance-gdpr.md) och/eller [California Consumer Privacy Act](../getting-started/compliance-ccpa.md), se [Sekretessinställningar för Google](google-tools.md#google-privacy-settings).

## Steg 1. Konfigurera [!DNL Google Analytics] konto

Se [Konfigurera webbplatssökning](https://support.google.com/analytics/answer/1012264) i Google-hjälpen för att få information om grunderna för hur du kommer igång. Se även Google-guiderna för [Google Analytics](https://support.google.com/analytics/answer/9304153) och [Google Tag Manager](https://support.google.com/tagmanager/answer/6102821).

1. Logga in på [!DNL Google Analytics] konto.

1. Aktivera **[!UICONTROL Internal Site Search Tracking]** gör du följande:

   - Navigera till **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - Ange **[!UICONTROL Site Search Tracking]** till `On`.

   - Ange **[!UICONTROL Query]** parameter till `q`.

   - När det är klart **[!UICONTROL Save]** inställningarna.

1. Så här aktiverar du visningsfunktioner:

   - Välj **[!UICONTROL Property Settings]**.

   - Under _[!UICONTROL Advertising Features]_, ange **[!UICONTROL Enable Demographics and Interest Reports]**till `On`.

   - **[!UICONTROL Save]** inställningarna.

1. Så här aktiverar du e-handelsspårning:

   - Navigera till **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

   - Ange **[!UICONTROL Enable Ecommerce]** till `On`.

   - Ange **[!UICONTROL Enable Enhanced Ecommerce Reporting]** till `On`.

   - **[!UICONTROL Save]** inställningarna.

1. Läs in sidan igen och verifiera att alla inställningar finns kvar `On`.

   >[!NOTE]
   >
   >Om inte alla inställningar `On`, upprepa föregående steg, spara och läsa in sidan igen. Upprepa den här processen tills alla inställningar är inställda på `On`.

## Steg 2. Konfigurera [!DNL Google Tag Manager] konto

Följande instruktioner visar hur du konfigurerar en ny behållare med de grundläggande inställningarna. Ett exempel [Disposition](https://developer.adobe.com/commerce/php/development/composer/) konfigurationsfilen (.json) används för att förenkla processen och import för att generera en tagg i en ny behållare. I det här exemplet rekommenderas att du skapar en behållare i stället för att ändra en befintlig behållare.

>[!NOTE]
>
>Mer information finns i Google [Exportera och importera behållare](https://support.google.com/tagmanager/answer/6106997). De här instruktionerna innehåller en genomgång för att importera ett JSON-prov i en ny behållare.

1. Hämta den länkade filen [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt), öppna filen i en redigerare och spara den som `GTM_M2_Config.json`.

   JSON-filen överförs direkt till [!DNL Google Tag Manager].

1. Navigera till **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**.

1. Klicka **[!UICONTROL Choose container file]** och väljer json-filen.

1. Under **[!UICONTROL Choose workspace]**, klicka **[!UICONTROL New]**.

1. Ange en titel och beskrivning och klicka sedan på **[!UICONTROL Save]**.

1. Om du vill importera filen väljer du en av följande åtgärder:

   - The **[!UICONTROL Overwrite]** ska vara markerat för en ny behållare.

   - The **[!UICONTROL Merge]** bör vara markerat om du använder en befintlig behållare.

1. Klicka **[!UICONTROL Preview]** för att granska taggar, utlösare och variabler.

1. Redigera **[!UICONTROL Google Analytics ID]** som refereras i variabler gör du följande:

   - Navigera till **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**.

   - Välj **[!UICONTROL Google Analytics]** och uppdatera platshållaren (`UA-xxxxxx-x`) med egen **[!UICONTROL GA ID]**.

1. Följ Google instruktioner för hur du lägger till taggar, utlösare och variabler i den nya behållaren.

   Om du har inställningar i en annan behållare som du vill använda kan de flyttas till den nya behållaren.

1. Klicka **[!UICONTROL Confirm]** när det är klart.

1. Följ Google anvisningar för hur du publicerar den nya behållaren.

## Steg 3. Konfigurera din butik

{{gtag-api-note}}

1. Logga in i administratören för din Commerce Store.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Google API]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Google Analytics]** och konfigurera följande:

   ![Försäljningskonfiguration - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL Enable]** till `Yes`.

   - Ange **[!UICONTROL Account type]** till `Google Tag Manager`.

   - I **[!UICONTROL Container ID]** anger du ditt GTM-ID (`GTM-xxxxxx`).

   - Om du även använder Google Analytics för att experimentera med innehåll anger du **Aktivera innehållsexperiment** till `Yes`.

   - Använd standardvärdena för de återstående fälten.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

1. Testa [!DNL Google Tag Manager] och verifiera att allt fungerar som det ska.

>[!NOTE]
>
>Varje behållare är kopplad till en webbplats och du behöver bara en behållare per konto. Om du har en Commerce-instans för flera webbplatser behöver du separata behållare.

## Steg 4. Lägg till GTM-koden i din Adobe Commerce Store

1. Om du vill kopiera GTM-koden går du till **[!UICONTROL Admin]** > **[!UICONTROL Install Google Tag Manager]**.

   Det finns två GTM-kodfragment att lägga till på din Commerce-webbplats: det första för den `<head>` -taggen och den andra för `<body>` -tagg.

1. Gå till Commerce Admin **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**och öppna butiksvyn i redigeringsläge.

1. Under _[!UICONTROL Other Settings]_, expandera **[!UICONTROL HTML Head]**och klistra in koden du kopierade från GTM för `<head>` i **[!UICONTROL Scripts and Style Sheets]**fält.

   ![Infoga kod i HTML Head](./assets/head-tag.png){width="600" zoomable="yes"}

1. Expandera **[!UICONTROL Footer]** och klistra in GTM-koden för `<body>` i **[!UICONTROL Miscellaneous HTML]** fält.

   ![Infoga kod i sidfoten](./assets/footer-tag-section.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Configuration]**.

## Fältbeskrivningar

| Fält | Omfång | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable] | Butiksvy | Avgör om Google Analytics Enhanced Ecommerce kan användas för att analysera aktiviteter i din butik. Alternativ: `Yes` / `No` |
| [!UICONTROL Account type] | Butiksvy | Anger den spårningskod för Google som används för att övervaka butiksaktivitet och trafik. Alternativ: `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | Butiksvy | Avgör om identifieringsinformation tas bort från IP-adresser som visas i Google Analytics-resultat. |
| [!UICONTROL Enable Content Experiments] | Butiksvy | Aktiverar Google Content Experiments, som kan användas för att testa upp till tio olika versioner av samma sida. Alternativ: `Yes` / `No` |
| [!UICONTROL Container Id] | Butiksvy | If [!DNL Google Tag Manager] redan är installerat och konfigurerat för din butik visas behållar-ID automatiskt i det här fältet. |
| [!UICONTROL List property for the catalog page] | Butiksvy | Identifierar tagghanterarens egenskap som är associerad med katalogsidan. Standardvärde: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Butiksvy | Identifierar tagghanterarens egenskap som är associerad med korsförsäljningsblocket. Standardvärde: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Butiksvy | Identifierar tagghanterarens egenskap som är associerad med merförsäljningsblocket. Standardvärde: `Up-sell` |
| [!UICONTROL List property for the related products block] | Butiksvy | Identifierar tagghanterarens egenskap som är associerad med det relaterade produktblocket. Standardvärde: `Related Products` |
| [!UICONTROL List property for the search results page] | Butiksvy | Identifierar tagghanterarens egenskap som är associerad med sökresultatsidan. Standardvärde: `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | Butiksvy | Identifierar tagghanterarens egenskap som är associerad med etiketterna för interna kampanjer. Standardvärde: `Label` |

{style="table-layout:auto"}

## Skapa en tagg för att spåra konverteringar

Om du har ett Google AdWords-konto kan du skapa en tagg som spårar konverteringar. I följande exempel visas hur du använder båda [!DNL Google Tag Manager] och [!DNL Google Analytics] för att skapa en tagg som påverkar din butiks konvertering _Lyckades_ sida.

### Steg 1. Skapa en tagg

1. Logga in på [!DNL Google Tag Manager] och klicka på länken för den behållare som du skapade för butiken.

1. I **[!UICONTROL New Tag]** ruta, klicka **[!UICONTROL Add a new tag]**.

1. Hämta följande information från ditt AdWords-konto:

   - Konverterings-ID
   - Konverteringsetikett

   Om du behöver hjälp kan du besöka Google [supportwebbplats](https://support.google.com/tagmanager/answer/6105160).

1. Från [!DNL Google Tag Manager] kontrollpanel, klicka **[!UICONTROL Google AdWords]** och gör följande:

   - Klicka på titelplatshållaren och ange ett namn för den nya taggen.

   - Under **[!UICONTROL Choose Product]** väljer du **[!UICONTROL Google AdWords]**.

   - Under _[!UICONTROL Choose a Tag Type]_, markera **[!UICONTROL AdWords Conversion Tracking]**och klicka **[!UICONTROL Continue]**.

1. Ange **[!UICONTROL Conversion ID]** och **[!UICONTROL Conversion Label]** från ditt AdWords-konto och klicka **[!UICONTROL Continue]**.

### Steg 2. Skapa en regel

Fortsätta från [!DNL Google Tag Manager] dashboard är nästa steg att skapa en regel som aktiverar taggen på konverteringssidan.

1. Under **[!UICONTROL Fire On]**, klicka **[!UICONTROL Some Pages]**.

1. I _[!UICONTROL Choose Pages]_fyller du i följande inställningar:

   - **[!UICONTROL Name]** - Ange ett namn för sidbeskrivningen.

   - **[!UICONTROL Variable]** `url`

   - **Åtgärd** - `matches RegEx`

     Mer information finns på [Operatorer för Regex- och CSS-väljare](https://support.google.com/tagmanager/answer/7679109) i Google Tag Manager Help.

   - **[!UICONTROL Value]** - `checkout/success.*`

1. Markera den gröna kryssrutan och klicka på **[!UICONTROL Save]**.

   Utlösaren som du ställer in visas som en blå knapp i avsnittet Elden på.

1. När du är klar klickar du på **[!UICONTROL Save Tag]**.

### Steg 3. Förhandsgranska och publicera

Nästa steg i processen är att förhandsgranska taggen. Varje gång taggen förhandsgranskas sparas en ögonblicksbild av versionen. När du är nöjd med resultatet går du till den version du vill använda och klickar på **[!UICONTROL Publish]**.
