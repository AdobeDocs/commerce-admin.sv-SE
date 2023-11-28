---
title: Layoutuppdateringar
description: Lär dig hur du använder layoutuppdateringar för att anpassa layouten på en sida.
exl-id: e2d8261f-cae1-4bd4-a047-f861dd7ca14e
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '1007'
ht-degree: 0%

---

# Layoutuppdateringar

Innan du börjar arbeta med anpassade layoutuppdateringar är det viktigt att du förstår hur sidorna i din butik är uppbyggda och skillnaden mellan villkoren *layout* och *layoutuppdatering*. Layout avser sidans visuella och strukturella komposition. Layoutuppdatering är en specifik uppsättning XML-instruktioner som kan åsidosätta eller anpassa hur sidan utformas.

XML-layouten i [!DNL Commerce] store är en hierarkisk struktur med behållare och block. Vissa element visas på varje sida och andra visas bara på specifika sidor. Mer information om layout, behållare och block finns i [Översikt över layouter](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) i _Utvecklarhandbok för Edge_.

The [Widget](widgets.md) är ett enkelt sätt att lägga till ett befintligt [innehållsblock](blocks.md) till en sidas standardlayout. För mer avancerade uppdateringar måste du spara XML-layoutens uppdateringskod på servern och sedan referera filen som en anpassad layoutuppdatering från administratören. En översikt över processen finns i [Använd layousuppdateringar](layout-updates.md#place-a-block-using-layout-updates).

I följande diagram är namnen som refererar till behållare svarta och blocktyperna, eller blockklasssökvägarna, blå.

![Standarddiagram för blocklayout](./assets/page-layout-default.png){width="500" zoomable="yes"}

| Blocktyp | Beskrivning |
|--- |--- |
| `page/html` | Namnet på det här blocket är `root` och det är ett av de få rotblocken i layouten. Du kan också skapa ett eget block och namnge det `root`, som är standardnamnet för block av den här typen. Det får bara finnas ett block av den här typen per sida. |
| `page/html_head` | Blocknamnet är `head` och är underordnad rotblocket. Det kan bara finnas ett block av den här typen per sida och det får inte tas bort. |
| `page/html_notices` | Blocknamnet är `global_notices` och är underordnad rotblocket. Om det här blocket tas bort från layouten visas inte de globala meddelandena på sidan. Det får bara finnas ett block av den här typen per sida. |
| `page/html_header` | Blocknamnet är `header` och är underordnad rotblocket. Det här blocket motsvarar sidhuvudet högst upp på sidan och innehåller flera standardblock. Det kan bara finnas ett block av den här typen per sida och det får inte tas bort. |
| `page/html_wrapper` | Även om det ingår i standardlayouten är det här blocket föråldrat och inkluderas endast för att säkerställa bakåtkompatibilitet. Använd inte block av den här typen. |
| `page/html_breadcrumbs` | Namnet på det här blocket är `breadcrumbs` och är underordnad rubrikblocket. Detta block visar vägbeskrivningar för den aktuella sidan. Det får bara finnas ett block av den här typen per sida. |
| `page/html_footer` | Blocknamnet är `footer` och är underordnad rotblocket. Sidfotsblocket motsvarar den synliga sidfoten längst ned på sidan och innehåller flera standardblock. Det kan bara finnas ett block av den här typen per sida och det får inte tas bort. |
| `page/template_links` | Det finns två block av den här typen i standardlayouten. The `top.links` -blocket är underordnat rubrikblocket och motsvarar den övre navigeringsmenyn. The `footer_links` -blocket är underordnat sidfotsblocket och motsvarar den nedre navigeringsmenyn. <br/><br/>**_Obs!_**Det går att ändra malllänkarna, vilket visas i exemplen. |
| `page/switch` | Det finns två block av den här typen i en standardlayout. The `store_language` -blocket är underordnat rubrikblocket och motsvarar den översta språkväljaren. The `store_switcher` -blocket är underordnat sidfotsblocket och motsvarar väljaren för det nedre arkivet. |
| kärna/meddelanden | Det finns två block av den här typen i en standardlayout. The `global_messages` -block visar globala meddelanden. The `messages` -block används för att visa alla andra meddelanden. Om ni tar bort dessa block ser kunden inga meddelanden. |
| `core/text_list` | Den här typen av block används ofta i hela [!DNL Commerce] som en platshållare för återgivning av underordnade block. |
| `core/profiler` | Det finns bara en instans av den här typen av block per sida. Det används för den interna [!DNL Commerce] profilerare och ska inte användas för något annat ändamål. |

{style="table-layout:auto"}

## Montera ett block med layoutredigeringar

[Layoutuppdateringar](layout-updates.md) gör det möjligt att anpassa sidans layout. Layoutuppdateringar ger större flexibilitet än en [widget](widgets.md), men kräver åtkomst till servern och grundläggande kunskaper i XML.

Följande steg visar hur du använder en layoutuppdatering för att placera ett block på en sida. Specifika exempel och hjälp om syntax finns i [Vanliga layoutanpassningsåtgärder](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) i _Utvecklarhandbok för Edge_.

### Steg 1: Skapa blocket

1. Skapa [block](block-add.md) som du vill montera.

1. Observera `block_id`, eftersom det används i instruktionerna för layoutuppdatering.

### Steg 2: Skapa layoutuppdateringen i XML

1. Skapa layoutinstruktionerna i XML för att [Referera till ett CMS-block](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-manage/).

1. Spara [layoutinstruktioner](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-instructions/) på servern i layoutmappen där XML-filer sparas för temat.

   Exempel:

   `<theme_dir>/<Namespace>_<Module>/layout`

   Layouthandtaget är det filnamn som börjar med `cms_page_view_selectable_`, följt av URL-nyckeln för CMS-sidan, alternativet för layoutuppdatering och `xml` filsuffix. I följande exempel `customer-service` är sidans URL-nyckel, och `ChatTool` är det alternativ som du väljer för att tillämpa layoutredigeringen på sidan.

   `cms_page_view_selectable_`&lt;`customer-service`>`_`&lt;`ChatTool`>`.xml`

   | Element | Beskrivning |
   |--- |--- |
   | CMS-sididentifierare | Sidans URL-nyckel med ett snedstreck (`/`) ersatt med ett understreck (`_`). |
   | Namn på layoutuppdatering | Alternativet som visas för _Anpassad layoutuppdatering_. |

   {style="table-layout:auto"}

### Steg 3: Referera layoutuppdateringen från sidan

1. På _Administratör_ sidebar, gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Leta upp sidan där du vill placera blocket och öppna den i redigeringsläge.

1. Rulla ned och expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Design]** -avsnitt.

1. Om du vill visa alla tillgängliga layoutuppdateringar som är kopplade till sidan klickar du på **[!UICONTROL Custom Layout Update]** -menyn.

   ![Anpassad lista över layoutuppdateringar](./assets/page-design-custom-layout-update.png){width="400" zoomable="yes"}

1. Välj den layoutredigering som du vill använda på sidan.

### Steg 4: Spara och uppdatera cachen

1. När du är klar klickar du på **[!UICONTROL Save & Close]**.

1. Klicka på i meddelandet längst upp på arbetsytan **[!UICONTROL Cache Management]** och uppdatera alla ogiltiga cacheobjekt.
