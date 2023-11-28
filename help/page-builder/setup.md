---
title: '''[!DNL Page Builder] konfiguration'
description: Läs mer om [!DNL Page Builder] funktionskonfiguration i Admin för Adobe Commerce och Magento Open Source.
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# [!DNL Page Builder] konfiguration

När det är aktiverat i konfigurationen [!DNL Page Builder] är standardverktyget för att skapa innehåll för CMS-sidor, block och dynamiska block. Dessutom är _[!UICONTROL Enable Advanced CMS]_knapperbjudanden [!DNL Page Builder] som ett alternativ för Kategorier och Produkter. Du kan också välja standardinställningen [sidlayout](../content-design/page-layout.md) som du vill använda för produkter, kategorier och CMS-sidor. [!DNL Page Builder] är inte tillgängligt för nyhetsbrevinnehåll som använder WYSIWYG [redigerare](../content-design/editor.md).

>[!NOTE]
>
>Vid installation [!DNL Page Builder] åsidosätter standardinställningen för [!UICONTROL Mask for Meta Description] konfigurationsfält. Värdet ändras från `{{name}} {{description}}` till `{{name}}`.
><br>
>Du kan komma åt den här inställningen när du går till [!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration], expandera [!UICONTROL Catalog]och väljer [!UICONTROL Catalog] under. The [!UICONTROL Mask for Meta Description] fältet finns i [!UICONTROL Product Fields Auto-generation] -avsnitt.

>[!NOTE]
>
>En administratör måste ha [!UICONTROL Content] behörigheter för sina [rollomfång](../systems/permissions-user-roles.md) för att se [!UICONTROL Edit with Page Builder] och kan använda Page Builder.

Mer information om konfigurationsalternativen för det avancerade verktyget för innehållshantering finns i [_Referenshandbok för konfiguration_](../configuration-reference/general/content-management.md).

## Konfigurera [!DNL Page Builder]

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I den vänstra panelen under _[!UICONTROL General]_, välja **[!UICONTROL Content Management]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** och verifiera att **[!UICONTROL Enable Page Builder]** är inställd på `Yes`.

   ![Avancerade innehållsverktyg](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. Om du är redo att konfigurera [!DNL Google Maps]gör du följande:

   - Om nödvändigt följer du [Hämta API-nyckel][1] och sedan kopiera och klistra in **[!UICONTROL Google Maps API Key]**.

   - Ändra **[!UICONTROL Google Maps Style]**, klistra in JSON-koden som genereras av [[!DNL Google Maps] API:er Styling Wizard][2].

   >[!NOTE]
   >
   >Se [Media - Karta](map.md) för mer information om hur du använder [!DNL Google Maps] i [!DNL Page Builder] innehåll.

1. Konfigurera antalet riktlinjer i [!DNL Page Builder] kolumnstödraster gör du följande:

   - För **[!UICONTROL Default Column Grid Size]** anger du standardantalet kolumner som du vill ska visas i stödrastret.

   - För **[!UICONTROL Maximum Column Grid Size]** anger du det största antalet kolumner som du vill ska vara tillgängliga i stödrastret.

   >[!NOTE]
   >
   >Se [Layout - kolumn](column.md) för mer information om hur du använder kolumnstödrastret när du arbetar med [!DNL Page Builder] innehåll.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Konfigurera standardlayouter

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I den vänstra panelen under _[!UICONTROL General]_, välja **[!UICONTROL Web]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]** och gör följande:

   ![Standardlayouter](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   Mer information om webbkonfigurationsalternativen finns i [_Referenshandbok för konfiguration_](../configuration-reference/general/web.md#default-layouts).

   - Välj **[!UICONTROL Default Product Layout]** som du vill använda för produktsidor.

   - Välj **[!UICONTROL Default Category Layout]** som du vill använda för kategorisidor.

   - Välj **[!UICONTROL Default Page Layout]** som du vill använda för CMS-sidor.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Inaktivera [!DNL Page Builder]

>[!NOTE]
>
>Inaktiverar [!DNL Page Builder] ersätter de avancerade innehållsverktygen med WYSIWYG [redigerare](../content-design/editor.md)och kan orsaka visningsfel i butiken. Innehåll som du tidigare skapat med [!DNL Page Builder] går kanske inte att redigera från administratören.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I den vänstra panelen under _[!UICONTROL General]_, välja **[!UICONTROL Content Management]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** och ange **[!UICONTROL Enable Page Builder]** till `No`.

1. När du uppmanas att bekräfta klickar du på **[!UICONTROL Turn Off]**.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

1. När du uppmanas att göra det [uppdatera](../systems/cache-management.md) eventuell ogiltig cache.

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
[2]: https://mapstyle.withgoogle.com/
