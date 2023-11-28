---
title: Sidor
description: Läs mer om de sidor med huvudinnehåll som ingår i [!DNL Commerce] demobutik och ändring av konfigurationen för standardsidor.
exl-id: 4be7d3d6-ce36-42bc-9224-4804c3211f16
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 0%

---

# Sidor

Innehållet kan ses i termer av hållbarhet, precis som alla produkter i en butik. Visste du att hållbarheten för innehåll i sociala medier är mindre än 24 timmar? Den potentiella hållbarheten för det innehåll du skapar kan hjälpa dig att bestämma var du ska investera dina resurser.

Innehåll med lång livslängd kallas ibland för _vintergrönt_. Exempel på grönt innehåll är nöjda kunder, _hur_ och Frågor och svar. Innehåll som till sin natur är lättfördärvligt inkluderar händelser, branschnyheter och pressmeddelanden.

![Sidan Om oss som ingår i exempelarkivet för luma ](./assets/storefront-about-us.png){width="700" zoomable="yes"}

## Kärninnehållssidor

The [!DNL Commerce] demobutik innehåller exempel på sidor med kärninnehåll som hjälper dig att komma igång. Alla dessa sidor kan ändras efter dina behov. Titta på följande sidor i din butik och se till att innehållet förmedlar ditt budskap, din röst och ditt varumärke.

### Startsida

Demon [Startsida](../getting-started/storefront.md#home-page) sidan innehåller en banderoll, en bildkarusell, flera statiska block med länkar samt en lista med nya produkter.

### Integritetspolicy

Butiken [Integritetspolicy](../getting-started/privacy-policy.md) sidan ska uppdateras med din egen information. Som en god praxis bör er integritetspolicy förklara för kunderna vilken typ av information ditt företag samlar in och hur den används.

### 404 Hittades inte

Sidan med 404 sidor hittades inte namnges för den svarskod som returneras när det inte går att hitta en sida. URL-omdirigeringar minskar antalet gånger som den här sidan visas. Men när det är nödvändigt kan du lika gärna utnyttja möjligheten att erbjuda länkar till produkter som kunden kanske tycker är intressanta.

### Åtkomst nekad

{{b2b-feature}}

The [Åtkomst nekad](../b2b/account-company-roles-permissions.md) visas när behörigheter som tilldelats en företagsanvändare förhindrar åtkomst till sidan.

### Aktivera cookies

The [Aktivera cookies](../getting-started/compliance-cookie-law.md) visas när besökarna på webbplatsen inte har cookies aktiverade i webbläsarna. Sidan innehåller stegvisa, illustrerade instruktioner för att aktivera cookies för de vanligaste webbläsarna.

### Tjänsten är inte tillgänglig

The [503 Tjänsten är inte tillgänglig](../configuration-reference/general/general.md) sidan namnges för den svarskod som returneras när servern inte är tillgänglig.

### Om oss

Sidan Om oss är länkad från butikens sidfot. Du kan inkludera bilder, video, länkar till pressmeddelanden och meddelanden. Exempelsidan har en bild till höger och en dekorativ bild som anger slutet på sidan.

### Kundtjänst

Kundtjänstsidan är en annan nod i sidhierarkin. De två rubrikerna på sidan har innehåll som bara syns när kunden klickar på rubriken.

![Kundtjänst på butiken](./assets/storefront-customer-service.png){width="700" zoomable="yes"}

## Konfigurera standardsidor

The _Standardsidor_ konfiguration bestämmer vilken landningssida som är kopplad till [bas-URL](../stores-purchase/store-urls.md) och motsvarande hemsida. Den avgör också vilken sida som visas när en _Sidan hittades inte_ fel inträffar och om ett [spårbarhet](../catalog/navigation-breadcrumb-trail.md) visas högst upp på varje sida.

1. På _Administratör_ sidebar, gå till  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I den vänstra panelen under _[!UICONTROL General]_, välja **[!UICONTROL Web]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Default Pages]** -avsnitt.

   ![Standardsidor](./assets/web-default-pages.png){width="500" zoomable="yes"}

   | Fält | [Omfång](../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
   |--- |--- |--- |
   | [!UICONTROL Default Web URL] | Butiksvy | Anger landningssidan som är associerad med bas-URL:en. Som standard är det här fältet inställt på `cms` för att ange en sida på [!DNL Commerce] innehållshanteringssystem. Du kan också använda en annan typ av landningssida, till exempel en blogg. Om till exempel en blogg är installerad på servern på `magento/blog`kan du ange mappnamnet `blog` som en relativ sökväg till sidmarkeringen. |
   | [!UICONTROL CMS Home Page] | Butiksvy | Om du vill välja butikens hemsida väljer du bara CMS-sidan i listan. Som standard visas hela urvalet av CMS-sidor som är tillgängliga för din butik på CMS-startsidan. |
   | [!UICONTROL Default No-route URL] | Butiksvy | Innehåller URL-adressen till den standardsida som du vill ska visas när en `404 Page not Found` ett fel inträffar. Standardvärdet är `cms/noroute/index`. |
   | [!UICONTROL CMS No Route Page] | Butiksvy | Identifierar en specifik CMS-sida som du vill ska visas när ett fel av typen 404 Sidan hittades inte inträffar. Standardsidan är `404 Not Found`. |
   | [!UICONTROL CMS No Cookies Page] | Butiksvy | Identifierar en specifik CMS-sida som visas när cookies inte är aktiverade för webbläsaren. På sidan förklaras varför cookies används och hur du aktiverar dem för varje webbläsare. Standardsidan är `Enable Cookies`. |
   | [!UICONTROL Show Breadcrumbs for CMS Pages] | Butiksvy | Avgör om ett spårningsspår visas på alla CMS-sidor i katalogen. Alternativ: `Yes` / `No` |

   {style="table-layout:auto"}

1. För **[!UICONTROL Default Web URL]** anger du den relativa sökvägen till mappen i [!DNL Commerce] installation som innehåller landningssidan.

   Standardinställningen, `cms`, anger en sida från [!DNL Commerce] innehållshanteringssystem.

   >[!NOTE]
   >
   >Om du vill visa en viss butiksvy rensar du **[!UICONTROL Use Default]** kryssruta intill _[!UICONTROL Default Web URL]_och andra standardinställningar som ska ändras.

1. Ange **[!UICONTROL CMS Home Page]** till CMS-sidan som ska användas som startsida. Andra skapade sidor kan användas som startsida, till exempel:

   - Välkommen till den exklusiva onlinebutiken
   - Belöningspoäng
   - Om oss
   - Kundtjänst
   - Aktivera cookies
   - Integritetspolicy
   - Företag: Åtkomst nekad

1. För **[!UICONTROL Default No-route URL]** anger du den relativa sökvägen till mappen i [!DNL Commerce] installation där sidan omdirigeras när en _404 Sidan hittades inte_ ett fel inträffar.

   Standardvärdet är `cms/index/noRoute`.

1. Ange **[!UICONTROL CMS No Route Page]** till CMS-sidan som visas när en _404 Sidan hittades inte_ ett fel inträffar.

1. Ange **[!UICONTROL CMS No Cookies Page]** till CMS-sidan som visas när cookies är inaktiverade i webbläsaren. På sidan förklaras varför cookies används och hur du aktiverar dem för varje webbläsare. Standardsidan är `Enable Cookies`.

1. Om du vill att ett vägbeskrivande spår ska visas högst upp på alla CMS-sidor anger du **[!UICONTROL Show Breadcrumbs for CMS Pages]** till `Yes`.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
