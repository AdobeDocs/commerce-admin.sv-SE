---
title: '[!DNL Google Content Experiments]'
description: Lär dig hur du använder  [!DNL Google Content Experiments] för att ställa in ett A/B-test av Commerce produkter, kategorier eller innehållssidor.
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

I följande exempel visas hur du ställer in ett A/B-test av produkter, kategorier eller innehållssidor med hjälp av Google Analytics Content Experiments. Vi rekommenderar att du har två webbläsarflikar öppna när du arbetar med instruktionerna eftersom du måste hoppa fram och tillbaka mellan Commerce Admin och ditt [!DNL Google Analytics]-konto.

>[!NOTE]
>
>[!DNL Google Content Experiments] har tagits bort och är schemalagd för ersättning av [Google Optimize](https://support.google.com/optimize/answer/7084762?hl=en).

## Steg 1. Aktivera innehållsexperiment (Commerce)

1. Logga in på administratören för din Commerce-installation.

1. Följ instruktionerna för att aktivera [Google Analytics](google-analytics.md) med innehållsexperiment i Commerce-konfigurationen.

   ![Försäljningskonfiguration - Google API - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## Steg 2. Konfigurera variationerna (Commerce)

Skapa flera varianter av samma produkt, kategori eller sida.

- Varje variation måste ha en unik [URL-nyckel](../catalog/catalog-urls.md).
- Alla variationer måste ha samma [butiksvy](../getting-started/websites-stores-views.md#scope-settings) markerad.

Du kan skapa upp till tio varianter av varje enhet som du vill testa. Spara tid med [Spara och duplicera](../catalog/product-workspace.md) för produkter.

## Steg 3. Konfigurera experimentet (Google)

>[!NOTE]
>
>Du måste ha rätt behörighet för Google-kontot för att kunna skapa ett experiment.

1. Öppna en annan webbläsarflik och logga in på ditt [Google Analytics][2]-konto.

   Om det behövs går du till **[!UICONTROL Account]** och **[!UICONTROL Property]**.

1. Välj **[!UICONTROL Admin]** i sidofältet till vänster och använd någon av följande metoder:

   **Metod 1:** Välj en befintlig vy

   Klicka på nedpilen i kolumnrubriken _[!UICONTROL View]_&#x200B;och välj den vy som ska tillhandahålla data för experimentet.

   **Metod 2:** Skapa en ny rapportvy

   - Klicka på **[!UICONTROL Create View]** i rubriken för kolumnen _Visa_ och gör följande:

      - Identifiera experimentplatsen som antingen `Website` eller `Mobile app`.

      - Ange en beskrivande **[!UICONTROL Reporting View Name]**.

      - Ange **[!UICONTROL Reporting Time Zone]**.

   - När du är klar klickar du på **[!UICONTROL Create View]** och sedan på bakåtpilen för att gå tillbaka till föregående sida.

1. Välj **[!UICONTROL Behavior]** > **[!UICONTROL Experiments]** i den vänstra panelen under _[!UICONTROL Reports]_.

1. Klicka på **[!UICONTROL Create experiment]** och gör följande:

   - Ange den procentandel av trafiken som ska omdirigeras.

   - Ange **[!UICONTROL Original Page URL]** och URL:erna för varje **[!UICONTROL page variation]** som du vill testa.

   - Fyll i övriga alternativ.

1. När du har konfigurerat experimentet klickar du på **[!UICONTROL Manually Insert the Code]** och kopierar kodfragmentet.

## Steg 4. Klistra in kodfragment (Commerce)

1. Gå tillbaka till administratören för din Commerce-installation och öppna den ursprungliga versionen av produkten, kategorin eller sidan i redigeringsläge.

1. Expandera avsnittet **[!UICONTROL View Optimization]** för produkten, kategorin eller sidan.

1. Klistra in kodfragmentet som du kopierade från Google Analytics i textrutan **[!UICONTROL Experiment Code]**.

   >[!NOTE]
   >
   >Klistra inte in kodfragmentet i någon av varianterna.

   ![Optimering av produktvyn](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]** när du är klar.

## Steg 5: Granska och påbörja experimentet (Google)

1. Gå tillbaka till ditt [Google Analytics][2]-konto.

1. Granska inställningarna för experimentet.

1. Klicka på **[!UICONTROL Start Experiment]** om du är redo att börja.

   Annars klickar du på **[!UICONTROL Save for Later]**.


[2]: https://analytics.google.com/
