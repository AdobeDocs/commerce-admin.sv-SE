---
title: Kategorier - Innehållsinställningar
description: Läs mer om hur du använder [!UICONTROL Content] inställningar för att definiera eventuellt ytterligare innehåll som visas på kategorisidan.
exl-id: 988083e1-0993-4e08-b5e6-8b0855e56467
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Kategorier - Innehållsinställningar

The _[!UICONTROL Content]_inställningarna avgör om ytterligare innehåll visas på kategorisidan. Förutom listan med kategoriprodukter kan sidan innehålla en bild, beskrivning och CMS-block. Du kan använda [[!DNL Page Builder]](../page-builder/introduction.md) innehållsverktyg för att definiera kategoribeskrivningen.

## Lägg till kategoribeskrivningen i [!DNL Page Builder]

1. Öppna kategorin i redigeringsläge.

1. Rulla ned och expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Content]** -avsnitt.

   ![Kategoriinnehåll](./assets/category-content.png){width="600" zoomable="yes"}

1. Överst till höger på sidan **[!UICONTROL Description]** område, klicka **[!UICONTROL Edit with Page Builder]**.

1. Använd [[!DNL Page Builder]](../page-builder/introduction.md) innehållsverktyg till [redigera befintlig text](../page-builder/text.md) och lägga till annat innehåll (om det behövs).

## [!DNL Page Builder] förhandsgranska

När du expanderar _Innehåll_ för en befintlig kategori där innehåll har skapats med [!DNL Page Builder]visas en förhandsgranskning av **[!UICONTROL Description]** innehåll så som det skulle visas på kategorisidan. När du klickar på innehållsområdet öppnas [!DNL Page Builder] arbetsyta där du kan göra nödvändiga uppdateringar.

![Förhandsgranska beskrivning](../page-builder/assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

Den här innehållsförhandsgranskningen är som standard aktiverad för produkt- och kategoriformulären. Om prestandan försämras på grund av inläsning av förhandsvisningen kan du inaktivera förhandsvisningen i [Konfiguration för innehållshantering](../configuration-reference/general/content-management.md#advanced-content-tools) inställningar.

## Lägg till kategoribeskrivningen i redigeraren

Ange endast vanliga ASCII-tecken i textrutan. Om du klistrar in text från en ordbehandlare bör du först spara den som en vanlig TXT-fil för att ta bort osynliga kontrolltecken.

Mer information finns i [WYSIWYG-redigerare](../content-design/editor.md).

1. Öppna kategorin i redigeringsläge.

1. Rulla ned och expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Content]** -avsnitt.

   ![Kategoriinnehåll](./assets/category-content-ce.png){width="500" zoomable="yes"}

1. Ange kategorin **[!UICONTROL Description]** och använder [redigeringsverktygsfältet](../content-design/editor.md) för att formatera efter behov.

   Du kan dra i det nedre högra hörnet om du vill ändra textrutans höjd.

## Lägg till ett CMS-block på kategorisidan

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Välj den kategori som du vill redigera i kategoriträdet.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Content]** -avsnitt.

1. För **[!UICONTROL Add the CMS block]** markerar du det block som du vill lägga till.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Display Settings]** -avsnitt.

1. Ange **[!UICONTROL Display Mode]** till något av följande:

   - `Static block only`
   - `Static block and products`

1. När du är klar klickar du på **[!UICONTROL Save]** och granska blockvisningen i butiken (kräver uppdatering av cachen).

## Referens för innehållsinställningar

| Inställning | [Omfång](../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Category Image] | Butiksvy | Anger en bild för kategorisidans överkant. Metoder: <br/><br/>**[!UICONTROL Upload]**- Överför en bildfil från den lokala datorn till galleriet och använder den som kategoribild.<br/><br/>**[!UICONTROL Select from Gallery]** - Uppmanar dig att välja en befintlig bild från galleriet. <br/><br/>![Page Builder-kameraikon](../assets/icon-camera.png) - Dra en bildfil till kamerapanelen eller bläddra till bilden och välj den i det lokala filsystemet. |
| [!UICONTROL Description] | Butiksvy | Anger en beskrivning som visas på kategorisidan. <br/><br/>**[!UICONTROL Edit with Page Builder]**- Öppnar [[!DNL Page Builder] arbetsyta](../page-builder/workspace.md), där du kan redigera beskrivningen.<br/><br/>**[!UICONTROL Show / Hide Editor]** - Växlar visningen mellan WYSIWYG-redigeringsläget och HTML. |
| [!UICONTROL Add CMS Block] | Butiksvy | Lägger till en befintlig [CMS-block](../content-design/blocks.md) till kategorisidan. |

{style="table-layout:auto"}
