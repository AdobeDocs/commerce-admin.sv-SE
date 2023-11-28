---
title: Sociala medier och RSS-flöden
description: Lär dig hur du lägger till sociala medier och annan integrering med RSS-flöden för att skapa varumärkes- och produktmedvetenhet.
exl-id: e4a48870-f53e-4848-8faa-8f2aedaf53b7
feature: Merchandising, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 0%

---

# Sociala medier och RSS-flöden

Många handlare använder sociala medier och andra digitala verktyg för att skapa varumärkes- och produktmedvetenhet. Du kan integrera din butik med dina sociala nätverk genom att installera ett Marketplace-tillägg eller lägga till ett plugin-program på dina innehållssidor. Använd RSS-flöden för att publicera din produktinformation på shoppingaggregeringssajter och till och med inkludera dem i dina nyhetsbrev. Kunder kan prenumerera på dina RSS-flöden för att lära sig mer om nya produkter och kampanjer.

## Sociala nätverk

Din butik kan anslutas till sociala nätverk genom att installera en [Marketplace-tillägg](../getting-started/commerce-marketplace.md). Dessutom kan du enkelt lägga till sociala plugin-program som _Gilla_ till CMS-block som kan läggas in på hela butiken.

Sociala nätverksplatser har ett antal plugin-program som enkelt kan läggas till i din butik. Dessutom finns det många tillägg på Commerce Marketplace som kan användas för att integrera din butik med sociala medier. I följande exempel visas hur du lägger till en Facebook _Gilla_ till din butik.

>[!NOTE]
>
>Adobe Commerce har tagit bort det inbyggda _Magento Social_ Facebook-integrering och stöder inte längre tillägget. Gå till [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=Facebook){:target=&quot;_blank&quot;} för att hitta alternativa tillägg för Facebook-integrering.

### Steg 1. Hämta knappkoden

1. På Meta Developers webbplats går du till [knappkonfiguration](https://developers.facebook.com/docs/plugins/like-button) sida.

1. För **[!UICONTROL URL to Like]** anger du URL-adressen till den sida i din butik som du vill att andra ska _Gilla_.

   Du kan till exempel ange URL-adressen till butikens hemsida.

1. Välj **[!UICONTROL Layout]** för knappen.

1. Ange **[!UICONTROL Width]** i pixlar som är tillgängliga på din webbplats för knappen och tillhörande textmeddelanden.

1. Ange **[!UICONTROL Action Type]** till något av följande:

   - `Like`
   - `Recommend`

1. Klicka **[!UICONTROL Get Code]** om du vill kopiera den genererade koden till Urklipp.

### Steg 2. Skapa ett innehållsblock

1. Återvänd till din butiksadministratör.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Klicka på i det övre högra hörnet **[!UICONTROL Add New Block]**.

1. Ange en beskrivning **[!UICONTROL Block Title]** för intern referens.

   Exempel: `Facebook Like Button`.

1. Tilldela en unik **[!UICONTROL Identifier]** till blocket med alla gemener och understreck i stället för mellanslag.

   Exempel: `facebook_like_button`.

1. Om din Commerce-instans har flera butiksvyer väljer du varje **[!UICONTROL Store View]** där blocket ska vara tillgängligt.

1. Lägg till kodfragmentet i blockinnehållet, beroende på vilket innehållsverktyg du använder:

   - När du använder [!DNL Page Builder], lägga till [HTML Code](../page-builder/html-code.md) blockera till scenen och klistra in kodfragmentet som du kopierade från Facebook-platsen. Annars klistrar du in kodfragmentet i **[!UICONTROL Content]** box.

   - Klistra in kodfragmentet som du kopierade från Facebook-webbplatsen i **[!UICONTROL Content]** box.

1. Om blocket inte är klart att publiceras anger du **[!UICONTROL Enable Block]** till `No`.

1. När du är klar klickar du på **[!UICONTROL Save Block]**.

### Steg 3. Placera blocket

1. Lägg till blocket, beroende på vilket innehållsverktyg du använder:

   - När du använder [!UICONTROL Page Builder]följer du instruktionerna för att [lägg till blocket](../page-builder/block.md) till scenen.

   - På _Administratör_ sidebar, gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicka på i det övre högra hörnet **[!UICONTROL Add Widget]** och gör följande:

   - ![B2B för Adobe Commerce](../assets/b2b.svg) (Endast tillgängligt med B2B för Adobe Commerce) I _Inställningar_ avsnitt, ange **[!UICONTROL Type]** till `CMS Static Block` och klicka **[!UICONTROL Continue]**.

   - Verifiera att **[!UICONTROL Design Theme]** är inställt på det aktuella temat.

   - Klicka på **[!UICONTROL Continue]**.

1. I **[!UICONTROL Storefront Properties]** gör du följande:

   - För **[!UICONTROL Widget Title]**, anger du en rubrik för intern referens.

   - Ange **[!UICONTROL Assign to Store Views]** till `All Store Views`eller till den vy där du vill att appen ska vara tillgänglig. Om du vill markera flera vyer håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

   - Ange ett tal i dialogrutan **[!UICONTROL Sort Order]** -fält för att bestämma blockets ordning om det tilldelas att visas på samma plats på sidan som andra innehållselement. Den översta positionen är noll.

1. I _[!UICONTROL Layout Updates]_avsnitt, klicka **[!UICONTROL Add Layout Update]**och ange **[!UICONTROL Display On]**till den kategori, produkt eller sida där du vill att blocket ska visas.

   Om du till exempel väljer `All Pages` och placera blocket i antingen sidhuvudet eller sidfoten, visas blocket på samma plats på alla sidor i butiken.

   Så här placerar du blocket på en viss sida:

   - Ange **[!UICONTROL Display On]** till `Specified Page` och väljer **[!UICONTROL Page]** där du vill att blocket ska visas.

   - Välj **[!UICONTROL Block Reference]** för att identifiera den plats på sidan där blocket ska placeras.

   - Acceptera standardinställningen för **[!UICONTROL Template]**, som är inställd på `CMS Static Block Default Template`.

   - Klicka på **[!UICONTROL Save and Continue Edit]**.

1. Välj **[!UICONTROL Widget Options]**.

1. Klicka **[!UICONTROL Select Block…]** och välj det block som du vill montera.

1. När du är klar klickar du på **[!UICONTROL Save]**.

1. Följ instruktionerna högst upp på arbetsytan för att uppdatera indexet och sidcachen när du uppmanas till detta.

   Widgeten visas nu i _[!UICONTROL Widgets]_lista.

### Steg 4. Verifiera platsen i butiken

Gå tillbaka till butiken för att bekräfta att blocket finns på rätt plats. Om du vill flytta blocket kan du öppna widgeten igen och försöka med en annan sida eller blockreferens.

## RSS-flöden

RSS (Really Simple Syndication) är ett XML-baserat dataformat som används för att distribuera information online. Dina kunder kan prenumerera på dina RSS-flöden för att lära sig mer om nya produkter och kampanjer. RSS-flöden kan också användas för att publicera produktinformation på shoppingaggregeringswebbplatser och kan inkluderas i nyhetsbrev.

När RSS-flöden är aktiverade skickas automatiskt alla tillägg till produkter, erbjudanden, kategorier och kuponger till prenumeranterna på varje flöde. En länk till alla RSS-flöden som du publicerar finns i sidfoten på din butik.

![RSS-matningsikon](./assets/icon-rss.png){width="100"}<br/>

Den programvara som krävs för att läsa ett RSS-flöde kallas flödesläsare och gör att man kan abonnera på rubriker, bloggar, poddsändningar och mycket annat. Google Reader är en av många flödesläsare som är tillgängliga online gratis.

![Exempel på storefront - RSS-feed](./assets/storefront-rss-feeds.png){width="700" zoomable="yes"}

### Fördelar med att konfigurera en RSS-feed

- Hämta den senaste uppdateringen från din butik eller blogg
- Ljusa annonser
- Vanliga aktier
- Öka SEO
- Öka försäljningen

### Typer av RSS-flöden

| RSS-feed | Beskrivning |
|--- |--- |
| [!UICONTROL Wish List] | När det här alternativet är aktiverat visas en RSS-matningslänk högst upp i kundens önskelista. Dessutom innehåller sidan för delning av önskelistor en kryssruta som gör att du kan lägga till en länk till flödet från delade önskelistor. |
| [!UICONTROL New Products] | Publicerar meddelanden om nya produkter som lagts till i katalogen. |
| [!UICONTROL Special Products] | Publicerar meddelanden om produkter med specialpriser. |
| [!UICONTROL Coupons / Discounts] | Publicerar meddelanden om specialkuponger eller rabatter som finns i butiken. |
| [!UICONTROL Top Level Category] | Publicerar meddelanden om ändringar i katalogstrukturen på den översta nivån, vilket återspeglas i huvudmenyn. |
| [!UICONTROL Customer Order Status] | Ger kunderna möjlighet att spåra deras beställningsstatus via RSS-flöden. När det här alternativet är aktiverat visas en RSS-matningslänk i ordningen. |

{style="table-layout:auto"}

### Konfigurera RSS-flöden för din butik

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I det övre högra hörnet anger du **[!UICONTROL Store View]** till de vyer där flödena ska vara tillgängliga.

   Om du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL RSS Feeds]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Rss Config]** avsnitt och ange **[!UICONTROL Enable RSS]** till `Enable`.

   ![Katalogkonfiguration - RSS-flöden](../configuration-reference/catalog/assets/rss-feeds-rss-config.png){width="600" zoomable="yes"}

   Rensa **[!UICONTROL Use Default]** om du vill ändra standardvärdet.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Wish List]** avsnitt och ange **[!UICONTROL Enable RSS]** till `Enable`.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Catalog]** och ange andra feeds till `Enable` efter behov.

   - **[!UICONTROL New Products]**
   - **[!UICONTROL Special Products]**
   - **[!UICONTROL Coupons/Discounts]**
   - **[!UICONTROL Top Level Category]**

   ![Katalog - inställningar för RSS-flöden](../configuration-reference/catalog/assets/rss-feeds-catalog.png){width="600" zoomable="yes"}

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Order]** avsnitt och ange **[!UICONTROL Customer Order Status Notification]** till `Enable`.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

1. Se resultatet i butiken med `/rss` i slutet av sidans URL.

