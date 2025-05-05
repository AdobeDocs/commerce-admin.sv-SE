---
title: Sociala medier och RSS-flöden
description: Lär dig hur du lägger till sociala medier och annan integrering med RSS-flöden för att skapa varumärkes- och produktmedvetenhet.
exl-id: e4a48870-f53e-4848-8faa-8f2aedaf53b7
feature: Merchandising, Communications
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 0%

---

# Sociala medier och RSS-flöden

Många handlare använder sociala medier och andra digitala verktyg för att skapa varumärkes- och produktmedvetenhet. Du kan integrera din butik med dina sociala nätverk genom att installera ett Marketplace-tillägg eller lägga till ett plugin-program på dina innehållssidor. Använd RSS-flöden för att publicera din produktinformation på shoppingaggregeringssajter och till och med inkludera dem i dina nyhetsbrev. Kunder kan prenumerera på dina RSS-flöden för att lära sig mer om nya produkter och kampanjer.

## Sociala nätverk

Din butik kan anslutas till sociala nätverk genom att installera ett [Marketplace-tillägg](../getting-started/commerce-marketplace.md). Dessutom kan du enkelt lägga till sociala plugin-program som knappen _Gilla_ i CMS-block som kan läggas in på sidor i hela din butik.

Sociala nätverksplatser har ett antal plugin-program som enkelt kan läggas till i din butik. Dessutom finns det många tillägg på Commerce Marketplace som kan användas för att integrera din butik med sociala medier. I följande exempel visas hur du lägger till en _Gilla_-knapp från Facebook i din butik.

>[!NOTE]
>
>Adobe Commerce har tagit bort den inbyggda Facebook-integreringen _Magento Social_ och stöder inte längre tillägget. Gå till [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=Facebook){:target=&quot;_blank&quot;} om du vill hitta alternativa tillägg för Facebook-integrering.

### Steg 1. Hämta knappkoden

1. Gå till sidan [knappkonfiguration](https://developers.facebook.com/docs/plugins/like-button) på Meta-utvecklarwebbplatsen.

1. För **[!UICONTROL URL to Like]** anger du URL-adressen till sidan i din butik som du vill att personer ska _Gilla_.

   Du kan till exempel ange URL-adressen till butikens hemsida.

1. Välj **[!UICONTROL Layout]** för knappen.

1. Ange **[!UICONTROL Width]** i pixlar som är tillgängliga på din webbplats för knappen och eventuella associerade textmeddelanden.

1. Ange **[!UICONTROL Action Type]** till något av följande:

   - `Like`
   - `Recommend`

1. Klicka på **[!UICONTROL Get Code]** om du vill kopiera den genererade koden till Urklipp.

### Steg 2. Skapa ett innehållsblock

1. Återvänd till din butiksadministratör.

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add New Block]** i det övre högra hörnet.

1. Ange en beskrivande **[!UICONTROL Block Title]** för intern referens.

   Till exempel: `Facebook Like Button`.

1. Tilldela ett unikt **[!UICONTROL Identifier]** till blocket med alla gemener och understreck i stället för mellanslag.

   Till exempel: `facebook_like_button`.

1. Om din Commerce-instans har flera butiksvyer väljer du var **[!UICONTROL Store View]** där blocket ska vara tillgängligt.

1. Lägg till kodfragmentet i blockinnehållet, beroende på vilket innehållsverktyg du använder:

   - När du använder [!DNL Page Builder] lägger du till ett [HTML-kodblock](../page-builder/html-code.md) på scenen och klistrar in kodfragmentet som du kopierade från Facebook-webbplatsen. Annars klistrar du in kodfragmentet i rutan **[!UICONTROL Content]**.

   - Klistra in kodfragmentet som du kopierade från Facebook-webbplatsen i rutan **[!UICONTROL Content]** med redigeraren.

1. Om blocket inte är klart att publiceras anger du **[!UICONTROL Enable Block]** till `No`.

1. Klicka på **[!UICONTROL Save Block]** när du är klar.

### Steg 3. Placera blocket

1. Lägg till blocket, beroende på vilket innehållsverktyg du använder:

   - När du använder [!UICONTROL Page Builder] följer du instruktionerna för att [lägga till blocket](../page-builder/block.md) på scenen.

   - Gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add Widget]** i det övre högra hörnet och gör följande:

   - ![Adobe Commerce B2B](../assets/b2b.svg) (endast tillgängligt med Adobe Commerce B2B) I avsnittet _Inställningar_ anger du **[!UICONTROL Type]** till `CMS Static Block` och klickar på **[!UICONTROL Continue]**.

   - Kontrollera att **[!UICONTROL Design Theme]** är inställt på det aktuella temat.

   - Klicka på **[!UICONTROL Continue]**.

1. Gör följande i avsnittet **[!UICONTROL Storefront Properties]**:

   - Ange en rubrik för intern referens för **[!UICONTROL Widget Title]**.

   - Ange **[!UICONTROL Assign to Store Views]** till `All Store Views` eller till den vy där du vill att appen ska vara tillgänglig. Om du vill markera flera vyer håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

   - Ange ett nummer i fältet **[!UICONTROL Sort Order]** för att bestämma ordningen på blocket om det tilldelats att visas på samma plats på sidan som andra innehållselement. Den översta positionen är noll.

1. I avsnittet _[!UICONTROL Layout Updates]_&#x200B;klickar du på&#x200B;**[!UICONTROL Add Layout Update]**&#x200B;och anger **[!UICONTROL Display On]**&#x200B;till den kategori, produkt eller sida där du vill att blocket ska visas.

   Om du till exempel väljer `All Pages` och placerar blocket i antingen sidhuvudet eller sidfoten, visas blocket på samma plats på alla sidor i butiken.

   Så här placerar du blocket på en viss sida:

   - Ange **[!UICONTROL Display On]** till `Specified Page` och markera **[!UICONTROL Page]** där du vill att blocket ska visas.

   - Välj **[!UICONTROL Block Reference]** för att identifiera den plats på sidan där blocket ska placeras.

   - Acceptera standardinställningen för **[!UICONTROL Template]**, som är inställd på `CMS Static Block Default Template`.

   - Klicka på **[!UICONTROL Save and Continue Edit]**.

1. Välj **[!UICONTROL Widget Options]** i panelen till vänster.

1. Klicka på **[!UICONTROL Select Block…]** och välj det block som du vill montera.

1. Klicka på **[!UICONTROL Save]** när du är klar.

1. Följ instruktionerna högst upp på arbetsytan för att uppdatera indexet och sidcachen när du uppmanas till detta.

   Widgeten visas nu i listan _[!UICONTROL Widgets]_.

### Steg 4. Verifiera platsen i butiken

Gå tillbaka till butiken för att bekräfta att blocket finns på rätt plats. Om du vill flytta blocket kan du öppna widgeten igen och försöka med en annan sida eller blockreferens.

## RSS-flöden

RSS (Really Simple Syndication) är ett XML-baserat dataformat som används för att distribuera information online. Dina kunder kan prenumerera på dina RSS-flöden för att lära sig mer om nya produkter och kampanjer. RSS-flöden kan också användas för att publicera produktinformation på shoppingaggregeringswebbplatser och kan inkluderas i nyhetsbrev.

När RSS-flöden är aktiverade skickas automatiskt alla tillägg till produkter, erbjudanden, kategorier och kuponger till prenumeranterna på varje flöde. En länk till alla RSS-flöden som du publicerar finns i sidfoten på din butik.

![Ikon för RSS-feed](./assets/icon-rss.png){width="100"}<br/>

Den programvara som krävs för att läsa ett RSS-flöde kallas flödesläsare och gör att man kan abonnera på rubriker, bloggar, poddsändningar och mycket annat. Google Reader är en av många flödesläsare som är tillgängliga online gratis.

![Exempelarkiv - RSS-feed](./assets/storefront-rss-feeds.png){width="700" zoomable="yes"}

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

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. I det övre högra hörnet anger du **[!UICONTROL Store View]** till de vyer där flödena ska vara tillgängliga.

   Om du uppmanas att bekräfta klickar du på **[!UICONTROL OK]**.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL RSS Feeds]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Rss Config]** och ange **[!UICONTROL Enable RSS]** till `Enable`.

   ![Katalogkonfiguration - RSS-flöden](../configuration-reference/catalog/assets/rss-feeds-rss-config.png){width="600" zoomable="yes"}

   Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use Default]** för att ändra standardvärdet.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Wish List]** och ange **[!UICONTROL Enable RSS]** till `Enable`.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Catalog]** och ange andra feeds till `Enable` efter behov.

   - **[!UICONTROL New Products]**
   - **[!UICONTROL Special Products]**
   - **[!UICONTROL Coupons/Discounts]**
   - **[!UICONTROL Top Level Category]**

   ![Katalog - Inställningar för RSS-flöden](../configuration-reference/catalog/assets/rss-feeds-catalog.png){width="600" zoomable="yes"}

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Order]** och ange **[!UICONTROL Customer Order Status Notification]** till `Enable`.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

1. Se resultatet i butiken med `/rss` i slutet av sidans URL.

