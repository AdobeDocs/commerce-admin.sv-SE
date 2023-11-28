---
title: WYSIWYG Editor
description: Lär dig hur du använder redigeraren och arbetar med innehåll i vyn _What You See Is What You Get_ (WYSIWYG).
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# WYSIWYG Editor

Med redigeraren kan du ange och formatera medan du arbetar i en _Vad du ser är vad du får_ (WYSIWYG) vy över innehållet. Om du föredrar att arbeta direkt med den underliggande HTML-koden kan du enkelt ändra läge. Redigeraren kan användas för att skapa innehåll för [sidor](pages.md), [block](blocks.md)och [produktbeskrivningar](../catalog/product-content.md). Gå till redigeraren genom att klicka **[!UICONTROL Show / Hide Editor]**.

>[!NOTE]
>
>TinyMCE 5 är WYSIWYG-standardredigerare. En uppdatering av TinyMCE 5.10-biblioteket i Adobe Commerce och Magento Open Source 2.4.5 åtgärdar en sårbarhet som tillåter godtycklig JavaScript-körning vid uppdatering av en bild eller länk med vissa typer av URL:er. TinyMCE 3 togs bort i version 2.4.0 och togs bort i version 2.4.3. TinyMCE 4 togs bort i version 2.4.4.

![Verktygsfältet Redigerare](./assets/editor-toolbar.png){width="700" zoomable="yes"}

Följande avsnitt innehåller detaljerad information om hur du använder redigeraren:

- [Infoga en länk](editor-insert-link.md)
- [Infoga en bild](editor-insert-image.md)
- [Infoga en widget](editor-widget.md)
- [Infoga en variabel](editor-insert-variable.md)

## Konfigurera redigeraren

WYSIWYG-redigeraren är aktiverad som standard och kan användas för att redigera innehåll på CMS-sidor och -block samt i produkter och kategorier. I konfigurationen kan du aktivera eller inaktivera redigeraren och välja att använda statiskt, i stället för att [dynamisk](../catalog/catalog-urls.md#dynamic-url), URL:er för medieinnehåll i beskrivningar av produkter och kategorier.

![WYSIWYG-alternativ](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

En detaljerad beskrivning av alla WYSIWYG-alternativ finns i [Innehållshantering](../configuration-reference/general/content-management.md) i _Konfigurationsreferens_.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I den vänstra panelen under _[!UICONTROL General]_, välja **[!UICONTROL Content Management]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**.

1. Ange **[!UICONTROL Enable WYSIWYG Editor]** efter dina önskemål.

   Redigeraren är aktiverad som standard.

1. Ange **[!UICONTROL Static URLs for Media Content in WYSIWYG]** efter dina önskemål om [mediainnehåll](../catalog/catalog-urls.md#static-url) som anges med WYSIWYG-redigeraren.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
