---
title: Inställningar för [!DNL Page Builder]
description: Lär dig mer om  [!DNL Page Builder] funktionskonfigurationen i Admin for Adobe Commerce och Magento Open Source.
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Inställningar för [!DNL Page Builder]

När det är aktiverat i konfigurationen är [!DNL Page Builder] standardverktyget för att skapa innehåll för CMS-sidor, block och dynamiska block. Dessutom erbjuder knappen _[!UICONTROL Enable Advanced CMS]_[!DNL Page Builder] som ett alternativ för Kategorier och Produkter. Du kan också välja standardsidlayouten [som du vill använda för produkter, kategorier och CMS-sidor.](../content-design/page-layout.md) [!DNL Page Builder] är inte tillgängligt för nyhetsbrevinnehåll som använder WYSIWYG [editor](../content-design/editor.md).

>[!NOTE]
>
>När det är installerat åsidosätter [!DNL Page Builder] standardinställningen för konfigurationsfältet [!UICONTROL Mask for Meta Description]. Värdet har ändrats från `{{name}} {{description}}` till `{{name}}`.
><br>
>Du kan komma åt den här inställningen när du går till [!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration], expanderar [!UICONTROL Catalog] och väljer [!UICONTROL Catalog] under. Fältet [!UICONTROL Mask for Meta Description] finns i avsnittet [!UICONTROL Product Fields Auto-generation].

>[!NOTE]
>
>En Admin-användare måste ha [!UICONTROL Content] behörigheter för [rollomfånget](../systems/permissions-user-roles.md) för att kunna se [!UICONTROL Edit with Page Builder]-knappar och kunna använda Page Builder.

Mer information om konfigurationsalternativen för det avancerade verktyget för innehållshantering finns i [_referenshandboken för konfiguration_](../configuration-reference/general/content-management.md).

## Konfigurera [!DNL Page Builder]

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_Admin **[!UICONTROL Configuration]**.

1. Välj _[!UICONTROL General]_i den vänstra panelen under **[!UICONTROL Content Management]**.

1. Expandera ![Expansionsväljaren ](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** och verifiera att **[!UICONTROL Enable Page Builder]** är inställd på `Yes`.

   ![Avancerade innehållsverktyg](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. Om du är redo att konfigurera [!DNL Google Maps] gör du följande:

   - Om det behövs följer du instruktionerna för [Hämta API-nyckel](https://developers.google.com/maps/documentation/javascript/get-api-key) och kopierar och klistrar sedan in **[!UICONTROL Google Maps API Key]**.

   - Om du vill ändra **[!UICONTROL Google Maps Style]** klistrar du in JSON-koden som genereras av [[!DNL Google Maps] API:ernas formateringsguide](https://mapstyle.withgoogle.com/).

   >[!NOTE]
   >
   >Mer information om hur du använder [ i ditt ](map.md)-innehåll finns i [!DNL Google Maps]Media - karta[!DNL Page Builder].

1. Så här konfigurerar du antalet stödlinjer i kolumnstödrastret [!DNL Page Builder]:

   - För **[!UICONTROL Default Column Grid Size]** anger du standardantalet kolumner som du vill ska visas i rutnätet.

   - För **[!UICONTROL Maximum Column Grid Size]** anger du det största antalet kolumner som du vill ska vara tillgängliga i rutnätet.

   >[!NOTE]
   >
   >Mer information om hur du använder kolumnstödrastret när du arbetar med ditt [-innehåll finns i ](column.md)Layout - kolumn[!DNL Page Builder].

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Konfigurera standardlayouter

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_Admin **[!UICONTROL Configuration]**.

1. Välj _[!UICONTROL General]_i den vänstra panelen under **[!UICONTROL Web]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]** och gör följande:

   ![Standardlayouter](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   Mer information om webbkonfigurationsalternativen finns i [_referenshandboken för konfiguration_](../configuration-reference/general/web.md#default-layouts).

   - Välj den **[!UICONTROL Default Product Layout]** som du vill använda för produktsidor.

   - Välj den **[!UICONTROL Default Category Layout]** som du vill använda för kategorisidor.

   - Välj den **[!UICONTROL Default Page Layout]** som du vill använda för CMS-sidor.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Inaktivera [!DNL Page Builder]

>[!NOTE]
>
>Om du inaktiverar [!DNL Page Builder] ersätts de avancerade innehållsverktygen med WYSIWYG [editor](../content-design/editor.md). Det kan orsaka visningsfel i butiken. Innehåll som du tidigare skapat med [!DNL Page Builder] kanske inte kan redigeras från administratören.

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_Admin **[!UICONTROL Configuration]**.

1. Välj _[!UICONTROL General]_i den vänstra panelen under **[!UICONTROL Content Management]**.

1. Expandera ![Expansionsväljaren ](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** och ange **[!UICONTROL Enable Page Builder]** till `No`.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL Turn Off]**.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

1. [Uppdatera](../systems/cache-management.md) om du uppmanas till det.
