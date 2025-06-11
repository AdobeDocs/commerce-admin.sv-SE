---
title: Sidor
description: Lär dig mer om de sidor med huvudinnehåll som ingår i  [!DNL Commerce] demoarkivet och ändra konfigurationen för standardsidor.
exl-id: 4be7d3d6-ce36-42bc-9224-4804c3211f16
feature: Page Content, Configuration
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '932'
ht-degree: 0%

---

# Sidor

Innehållet kan ses i termer av hållbarhet, precis som alla produkter i en butik. Visste du att hållbarheten för innehåll i sociala medier är mindre än 24 timmar? Den potentiella hållbarheten för det innehåll du skapar kan hjälpa dig att bestämma var du ska investera dina resurser.

Innehåll med lång hållbarhetstid kallas ibland _evergreen content_. Exempel på flergrönt innehåll är framgångsberättelser från kunder, _hur man_ får instruktioner och Vanliga frågor och svar. Innehåll som till sin natur är lättfördärvligt inkluderar händelser, branschnyheter och pressmeddelanden.

![Sidan Om oss som ingår i Luma-exempelarkivet ](./assets/storefront-about-us.png){width="700" zoomable="yes"}

## Kärninnehållssidor

Demoversionen [!DNL Commerce] innehåller exempel på sidor med kärninnehåll som hjälper dig att komma igång. Alla dessa sidor kan ändras efter dina behov. Titta på följande sidor i din butik och se till att innehållet förmedlar ditt budskap, din röst och ditt varumärke.

### Startsida

Demonsidan [Hem](../getting-started/storefront.md#home-page) innehåller en banderoll, en bildkarusell, flera statiska block med länkar och en lista med nya produkter.

### Integritetspolicy

Butikens [sekretesspolicy](../getting-started/privacy-policy.md)-sida ska uppdateras med din egen information. Som en god praxis bör er integritetspolicy förklara för kunderna vilken typ av information ditt företag samlar in och hur den används.

### 404 Hittades inte

Sidan med 404 sidor hittades inte namnges för den svarskod som returneras när det inte går att hitta en sida. URL-omdirigeringar minskar antalet gånger som den här sidan visas. Men när det är nödvändigt kan du lika gärna utnyttja möjligheten att erbjuda länkar till produkter som kunden kanske tycker är intressanta.

### Åtkomst nekad

{{b2b-feature}}

Sidan [Åtkomst nekad](../b2b/account-company-roles-permissions.md) visas när behörigheter som tilldelats en företagsanvändare förhindrar åtkomst till sidan.

### Aktivera cookies

Sidan [Aktivera cookies](../getting-started/compliance-cookie-law.md) visas när besökare på webbplatsen inte har cookies aktiverade i sina webbläsare. Sidan innehåller stegvisa, illustrerade instruktioner för att aktivera cookies för de vanligaste webbläsarna.

### Tjänsten är inte tillgänglig

Sidan [503 Tjänst ej tillgänglig](../configuration-reference/general/general.md) namnges för den svarskod som returneras när servern inte är tillgänglig.

### Om oss

Sidan Om oss är länkad från butikens sidfot. Du kan inkludera bilder, video, länkar till pressmeddelanden och meddelanden. Exempelsidan har en bild till höger och en dekorativ bild som anger slutet på sidan.

### Kundtjänst

Kundtjänstsidan är en annan nod i sidhierarkin. De två rubrikerna på sidan har innehåll som bara syns när kunden klickar på rubriken.

![Kundtjänstsidan i butiken](./assets/storefront-customer-service.png){width="700" zoomable="yes"}

## Konfigurera standardsidor

Konfigurationen _Standardsidor_ avgör vilken landningssida som är associerad med [bas-URL:en](../stores-purchase/store-urls.md) och motsvarande startsida. Den avgör också vilken sida som visas när ett _Sidan hittades inte_-fel inträffar och om ett [flödeslänk ](../catalog/navigation-breadcrumb-trail.md) visas högst upp på varje sida.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Välj **[!UICONTROL Web]** i den vänstra panelen under _[!UICONTROL General]_.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Default Pages]**.

   ![Standardsidor](./assets/web-default-pages.png){width="500" zoomable="yes"}

   | Fält | [Omfång](../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
   |--- |--- |--- |
   | [!UICONTROL Default Web URL] | Butiksvy | Anger landningssidan som är associerad med bas-URL:en. Som standard är det här fältet inställt på `cms` för att ange en sida från innehållshanteringssystemet [!DNL Commerce]. Du kan också använda en annan typ av landningssida, till exempel en blogg. Om till exempel en blogg är installerad på servern på `magento/blog` kan du ange mappnamnet `blog` som en relativ sökväg till urvalet av sidor. |
   | [!UICONTROL CMS Home Page] | Butiksvy | Om du vill välja butikens hemsida väljer du CMS-sidan i listan. Som standard visas hela urvalet av CMS-sidor som är tillgängliga för din butik på CMS hemsida. |
   | [!UICONTROL Default No-route URL] | Butiksvy | Innehåller URL-adressen till den standardsida som du vill ska visas när ett `404 Page not Found`-fel inträffar. Standardvärdet är `cms/noroute/index`. |
   | [!UICONTROL CMS No Route Page] | Butiksvy | Identifierar en specifik CMS-sida som du vill ska visas när ett fel av typen 404 Sidan hittades inte inträffar. Standardsidan är `404 Not Found`. |
   | [!UICONTROL CMS No Cookies Page] | Butiksvy | Identifierar en specifik CMS-sida som visas när cookies inte är aktiverade för webbläsaren. På sidan förklaras varför cookies används och hur du aktiverar dem för varje webbläsare. Standardsidan är `Enable Cookies`. |
   | [!UICONTROL Show Breadcrumbs for CMS Pages] | Butiksvy | Avgör om ett spårningsspår visas på alla CMS-sidor i katalogen. Alternativ: `Yes` / `No` |

   {style="table-layout:auto"}

1. För **[!UICONTROL Default Web URL]** anger du den relativa sökvägen till mappen i [!DNL Commerce]-installationen som innehåller landningssidan.

   Standardinställningen, `cms`, anger en sida från innehållshanteringssystemet [!DNL Commerce].

   >[!NOTE]
   >
   >Om du vill visa en viss butiksvy avmarkerar du kryssrutan **[!UICONTROL Use Default]** bredvid _[!UICONTROL Default Web URL]_&#x200B;och alla andra standardinställningar som ska ändras.

1. Ange **[!UICONTROL CMS Home Page]** på CMS-sidan som ska användas som startsida. Andra skapade sidor kan användas som startsida, till exempel:

   - Välkommen till den exklusiva onlinebutiken
   - Belöningspoäng
   - Om oss
   - Kundtjänst
   - Aktivera cookies
   - Integritetspolicy
   - Företag: Åtkomst nekad

1. För **[!UICONTROL Default No-route URL]** anger du den relativa sökvägen till mappen i installationen av [!DNL Commerce] där sidan omdirigeras när ett _404-sidfel inte hittades_ inträffar.

   Standardvärdet är `cms/index/noRoute`.

1. Ange **[!UICONTROL CMS No Route Page]** till den CMS-sida som visas när ett _404-sidfel inte hittades_ inträffar.

1. Ange **[!UICONTROL CMS No Cookies Page]** till den CMS-sida som visas när cookies är inaktiverade i webbläsaren. På sidan förklaras varför cookies används och hur du aktiverar dem för varje webbläsare. Standardsidan är `Enable Cookies`.

1. Om du vill att ett spårningsspår ska visas högst upp på alla CMS-sidor anger du **[!UICONTROL Show Breadcrumbs for CMS Pages]** till `Yes`.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
