---
title: Specialpriser
description: Lär dig hur du kan erbjuda specialpriser för en viss tidsperiod.
exl-id: 4a1e2045-f0a8-4bae-a5a3-8ce8b258b217
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 0%

---

# Specialpriser

Ett särskilt pris kan erbjudas för en bestämd tidsperiod. Under den angivna tidsperioden visas specialpriset i stället för normalpriset, följt av en notering som visar det reguljära priset.

![Specialpris på en produktsida](./assets/storefront-price-special.png){width="700" zoomable="yes"}

## Använd specialpris på en enskild produkt

Du kan enkelt ange ett specialpris för en enskild produkt i katalogen.

### Använd en schemalagd uppdatering

{{ee-feature}}

Adobe Commerce har stöd för [schemalagda uppdateringar](../content-design/content-staging-scheduled-update.md). Använd de här kampanjverktygen för att tillämpa ett särskilt pris på en viss produkt under en viss tidsperiod.

1. Öppna produkten i redigeringsläge.

1. Klicka på **[!UICONTROL Scheduled Update]**.

   ![Lägg till schemalagd uppdatering för produkten](./assets/product-schedule-new-update.png){width="600" zoomable="yes"}

1. För **Uppdateringsnamn**, anger du ett namn för specialpriskampanjen.

1. Ange en kort beskrivning **[!UICONTROL Description]**.

1. Använd _Kalender_ ( ![kalenderikon](../assets/icon-calendar.png) ) för att välja **[!UICONTROL Start Date]** och **[!UICONTROL End Date]** för specialpriskampanjen.

   Du kan använda **[!UICONTROL Hour]** och **[!UICONTROL Minute]** med skjutreglagen kan du även välja start- och sluttid. Klicka **[!UICONTROL Close]** när start och slut är inställda.

   ![Spara som ny uppdatering](./assets/product-price-special-scheduled-update.png){width="600" zoomable="yes"}

1. Bläddra nedåt till _Pris_ fält, klicka **[!UICONTROL Advanced Pricing]** och ange beloppet för **[!UICONTROL Special Price]** som ska tillämpas enligt den schemalagda uppdateringen.

   ![Specialprisinställningar](./assets/product-price-special.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Done]** och sedan **[!DNL Save]**.

   I butiken ska specialpriset visas både i kataloglistan och på produktsidan.

   The _[!UICONTROL Scheduled Change]_visas högst upp på sidan.

   ![Schemalagd ändring](./assets/product-price-special-scheduled-change.png){width="600" zoomable="yes"}

### Använd ett enkelt start- och slutdatum

{{ce-feature}}

Magento Open Source har alternativ för enkla start- och slutdatum i Avancerade priser.

1. Öppna produkten i redigeringsläge.

1. Bläddra nedåt till _[!UICONTROL Price]_fält, klicka **[!UICONTROL Advanced Pricing]**och anger **[!UICONTROL Special Price]**belopp.

1. Använd _Kalender_ ( ![Kalenderikon](../assets/icon-calendar.png) ) för att välja **[!UICONTROL Start Date]** och **[!UICONTROL End Date]** för specialpriskampanjen.

   Det särskilda priset gäller omedelbart efter midnatt i början av startdatumet (00:01) och fortsätter till och med strax före midnatt (23:59) dagen före slutdatumet.

   ![Schemalagd ändring](./assets/product-special-price-from-ce.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Done]** och sedan **[!UICONTROL Save]**.

   I butiken ska specialpriset visas både i kataloglistan och på produktsidan.

## Tillämpa ett specialpris på flera produkter

Du kan också tilldela ett specialpris till flera produkter, t.ex. flera varianter av en [konfigurerbar produkt](product-create-configurable.md).

### Ange ett specialpris för valda produkter

{{ee-feature}}

I följande exempel visas hur du tilldelar samma specialpris till flera produktvarianter av en konfigurerbar produkt i Adobe Commerce.

1. På _[!UICONTROL Products]_sida, klicka **[!UICONTROL Filters]**och anger **[!UICONTROL Name]**av den konfigurerbara produkten.

1. Ange **[!UICONTROL Type]** till `Configurable Product` och klicka **[!UICONTROL Apply Filters]**.

1. Om du vill tilldela alla produkter samma specialpris anger du kontrollen i den första kolumnrubriken till `Select All`.

   Du kan också markera kryssrutan för varje produkt som du vill inkludera.

1. Ange **[!UICONTROL Actions]** styra till `Update attributes`.

1. Bläddra nedåt till _[!UICONTROL Special Price]_och välj **[!UICONTROL Change]**kryssrutan nedanför_[!UICONTROL Special Price]_ och ange det specialpris som du vill erbjuda.

   ![Specialprisfält](./assets/product-price-special-commerce.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save]**.

Specialpriset i butiken visas i kataloger och på produktsidan. För en konfigurerbar produkt visas det ordinarie priset även på produktsidan när du väljer alternativ.

### Ange ett särskilt pris och datumintervall för valda produkter

{{ce-feature}}

I följande exempel visas hur du tilldelar samma specialpris till flera produktvarianter av en konfigurerbar produkt i Magento Open Source.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Klicka på **[!UICONTROL Filters]**.

1. Ange **[!UICONTROL Name]** av den konfigurerbara produkten.

1. Ange **[!UICONTROL Type]** till `Simple Product`.

   ![Filter](./assets/product-price-special-filter.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Apply Filters]**.

   I rutnätet visas alla enkla produkter som är associerade som varianter av den konfigurerbara produkten.

1. Om du vill tilldela alla produkter samma specialpris anger du kontrollen i den första kolumnrubriken till `Select All`.

   Du kan också markera kryssrutan för varje produkt som du vill inkludera.

1. Ange **[!UICONTROL Actions]** styra till `Update attributes`.

   ![Uppdatera attribut](./assets/product-price-special-action-update-attributes-ce.png){width="600" zoomable="yes"}

1. Bläddra nedåt till _[!UICONTROL Special Price]** och gör följande:

   - Välj **[!UICONTROL Change]** kryssrutan under _[!UICONTROL Special Price]** och ange specialpriset.

   - Välj **[!UICONTROL Change]** kryssrutan nedanför _Specialpris från datum_ klickar du på _Kalender_ ( ![Kalenderikon](../assets/icon-calendar.png) ) och välj det första datumet för specialpriskampanjen.

     Det särskilda priset gäller omedelbart efter midnatt i början av startdatumet (00:01) och fortsätter till och med strax före midnatt (23:59) dagen före slutdatumet.

   - Välj **[!UICONTROL Change]** kryssrutan nedanför _Pris till dagens datum_ klickar du på _Kalender_ ( ![Kalenderikon](../assets/icon-calendar.png) ) och välj det sista datumet för specialpriserbjudandet.

   ![Specialprisfält](./assets/product-price-special-action-update-attributes-fields-ce.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save]**.

   Ett meddelande visar hur många poster som uppdaterades med specialpriset.

   Specialpriset blir tillgängligt i butiken det angivna datumet och visas i kataloglistor och på produktsidan. För en konfigurerbar produkt visas det ordinarie priset även på produktsidan när du väljer alternativ.

   ![Specialpris för konfigurerbar produkt](./assets/storefront-special-price-configurable-product-detail.png){width="600" zoomable="yes"}

## Testning

Om specialpriset inte visas korrekt i butiken både på kataloglistan och på produktsidorna rensar du webbläsarens cache:

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > **[!UICONTROL Cache Management]**.

1. Klicka på **[!UICONTROL Flush Magento Cache]**.

>[!NOTE]
>
>The **_final_** produktpriset beräknas som **_minimum_** relevant pris, med följande formel: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Fast pris_** de anpassningsbara alternativen är _not_ påverkas av reglerna för grupppris, pris, specialpris eller katalogpris.
