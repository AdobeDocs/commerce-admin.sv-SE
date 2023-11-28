---
title: '[!DNL Google Content Experiments]'
description: Lär dig använda [!DNL Google Content Experiments] för att skapa ett A/B-test av Commerce-produkter, kategorier eller innehållssidor.
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

I följande exempel visas hur du ställer in ett A/B-test av produkter, kategorier eller innehållssidor med hjälp av Google Analytics Content Experiments. Vi rekommenderar att du har två webbläsarflikar öppna när du arbetar med instruktionerna, eftersom du måste hoppa fram och tillbaka mellan Commerce Admin och din [!DNL Google Analytics] konto.

>[!NOTE]
>
>[!DNL Google Content Experiments] har tagits bort och är schemalagd att ersättas av [Google Optimize](https://support.google.com/optimize/answer/7084762?hl=en).

## Steg 1. Aktivera innehållsexperiment (Commerce)

1. Logga in på administratören för din Commerce-installation.

1. Följ instruktionerna för att aktivera [Google Analytics](google-analytics.md) med innehållsexperiment i Commerce-konfigurationen.

   ![Säljkonfiguration - Google API - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## Steg 2. Ställ in variationerna (Commerce)

Skapa flera varianter av samma produkt, kategori eller sida.

- Varje variation måste ha ett unikt [URL-nyckel](../catalog/catalog-urls.md).
- Varje variation måste ha samma [butiksvy](../getting-started/websites-stores-views.md#scope-settings) markerat.

Du kan skapa upp till tio varianter av varje enhet som du vill testa. För produkter används [Spara och duplicera](../catalog/product-workspace.md) för att spara tid.

## Steg 3. Konfigurera experimentet (Google)

>[!NOTE]
>
>Du måste ha rätt behörighet för Google-kontot för att kunna skapa ett experiment.

1. Öppna en annan flik i webbläsaren och logga in på [Google Analytics][2] konto.

   Navigera till **[!UICONTROL Account]** och **[!UICONTROL Property]**.

1. Välj **[!UICONTROL Admin]** och använder någon av följande metoder:

   **Metod 1:** Välj en befintlig vy

   I sidhuvudet på _[!UICONTROL View]_klickar du på nedåtpilen och väljer den vy som ska användas för att ange data för experimentet.

   **Metod 2:** Skapa en ny rapportvy

   - I sidhuvudet på _Visa_ kolumn, klicka **[!UICONTROL Create View]** och gör följande:

      - Identifiera experimentplatsen som antingen `Website` eller `Mobile app`.

      - Ange en beskrivning **[!UICONTROL Reporting View Name]**.

      - Ange **[!UICONTROL Reporting Time Zone]**.

   - När du är klar klickar du på **[!UICONTROL Create View]** och klicka sedan på bakåtpilen för att gå tillbaka till föregående sida.

1. I den vänstra panelen under _[!UICONTROL Reports]_, välja **[!UICONTROL Behavior]**>**[!UICONTROL Experiments]**.

1. Klicka **[!UICONTROL Create experiment]** och gör följande:

   - Ange den procentandel av trafiken som ska omdirigeras.

   - Ange **[!UICONTROL Original Page URL]** och URL:er för varje **[!UICONTROL page variation]** som du vill testa.

   - Fyll i övriga alternativ.

1. När du har skapat ett experiment klickar du **[!UICONTROL Manually Insert the Code]** och kopiera kodfragmentet.

## Steg 4. Klistra in kodfragment (Commerce)

1. Gå tillbaka till administratören för din Commerce-installation och öppna den ursprungliga versionen av produkten, kategorin eller sidan i redigeringsläge.

1. Expandera **[!UICONTROL View Optimization]** för produkten, kategorin eller sidan.

1. Klistra in kodfragmentet som du kopierade från Google Analytics i **[!UICONTROL Experiment Code]** textruta.

   >[!NOTE]
   >
   >Klistra inte in kodfragmentet i någon av varianterna.

   ![Optimering av produktvyn](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save]**.

## Steg 5: Granska och påbörja experimentet (Google)

1. Återgå till [Google Analytics][2] konto.

1. Granska inställningarna för experimentet.

1. Klicka på **[!UICONTROL Start Experiment]**.

   Annars klickar du på **[!UICONTROL Save for Later]**.


[2]: https://analytics.google.com/
