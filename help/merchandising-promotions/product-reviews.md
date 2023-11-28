---
title: Produktrecensioner
description: Läs om hur produktrecensioner kan förbättra er butik och öka er trovärdighet.
exl-id: 82f96b24-626f-4b2d-be42-3d655d08dfda
feature: Merchandising, Products
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%

---

# Produktrecensioner

Produktrecensioner bidrar till att skapa en känsla av gemenskap och anses vara mer trovärdiga än vad annonsbudgeten kan köpa. Vissa sökmotorer ger sajter med produktrecensioner en högre rankning än de utan. För dem som hittar din webbplats genom att söka efter en viss produkt är en produktrecension i stort sett landningssidan i din butik. Med produktrecensioner kan man hitta en butik, hålla sig engagerad och ofta leda till försäljning.

Handeln innehåller en intern funktion för produktgranskning som du kan hantera från administratören. Du kan också använda ett tillägg från [Commerce Marketplace](../getting-started/commerce-marketplace.md) för att använda ett värdbaserat granskningssystem.

>[!NOTE]
>
>Adobe Commerce och Magento Open Source, version 2.4.0 till 2.4.3, innehåller tillägget som utvecklades av Yotpo-leverantörer. Från och med version 2.4.4 är det här tillägget inte längre paketerat med kärnversionen och måste installeras och uppdateras från Commerce Marketplace. Marketplace ger också tillgång till aktuell dokumentation från tilläggsutvecklaren.
><br><br>
>Om du har det paketerade tillägget aktiverat och konfigurerat måste du uppdatera filen Composer.json som en del av uppgraderingsprocessen för 2.4.4 och hantera tilläggsuppdateringar vidare. Se [Uppgraderingsmoduler](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) i _Uppgraderingshandbok_ för mer information.

## Produktrecensioner i butiken

När den inbyggda produktgranskningsfunktionen är aktiverad kan kunderna skriva recensioner för alla produkter i katalogen. Du kan skriva recensioner på produktsidan genom att klicka på:

- **Lägg till din recension** för produkter med granskningar.

- **Var först med att granska den här produkten** för produkter som saknar recensioner.

The [!UICONTROL Reviews] På -fliken visas alla aktuella granskningar och det formulär som användes för att skicka in en granskning.

Din konfiguration avgör om kunderna måste öppna ett konto i din butik innan de skriver produktrecensioner eller om de kan skicka recensioner som gäster. Att kräva att granskarna öppnar ett konto förhindrar att anonyma dokument skickas in och förbättrar granskningskvaliteten.

![Exempelarkiv - lägg till din recension](./assets/storefront-review-this-product.png){width="700" zoomable="yes"}

Antalet stjärnor anger att produkten är nöjd. Besökarna kan klicka på länken för att läsa granskningarna och skriva sina egna. Som ett incitament kan kunderna få belöningspoäng för att lämna in en recension. När en granskning skickas skickas den till administratören för moderering. När granskningen har godkänts publiceras den i din butik.

![Exempel på storefront - fliken Recensioner](./assets/storefront-reviews-tab.png){width="700" zoomable="yes"}

### [!UICONTROL My Product Reviews]

The _[!UICONTROL My Product Reviews]_i kundkontots kontrollpanel listas alla recensioner som kunden har skickat in och som godkänts för publicering. Varje granskningssammanfattning innehåller det datum då granskningen skickades, länkar till produktsidan och granskningsinformation.

![Mina produktrecensioner](./assets/account-dashboard-my-product-reviews.png){width="700" zoomable="yes"}

1. I sidofältet på deras konto väljer kunden **[!UICONTROL My Product Reviews]**.

1. Om du vill visa hela granskningen klickar du **[!UICONTROL See Details]**.

   ![Granska information](./assets/account-dashboard-my-product-reviews-details.png){width="700" zoomable="yes"}

## Aktivera funktioner för produktgranskning

Funktionen för granskning av Commerce-produkter är aktiverad som standard.

>[!NOTE]
>
>Ange fälten till `No` och inaktivera granskningar av Commerce-produkter måste du rensa **Använd systemvärde** kryssrutor.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och markera **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Product Reviews]** -avsnitt.

   ![Katalogkonfiguration - produktrecensioner för Commerce](../configuration-reference/catalog/assets/catalog-product-reviews.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enabled]** till `Yes`.

   Det här är standardinställningen som möjliggör produktgranskningar.

1. Ange **[!UICONTROL Allow Guests to Write Reviews]** till `Yes`.

   Det här är standardinställningen som avgör om kunderna måste öppna ett konto i din butik för att kunna skriva produktrecensioner.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Skapa egna klassificeringar

Med Commerce Product Reviews kan kunderna tilldela betyg när de skickar in en produktrecension. Standardklassificeringarna är kvalitet, pris och värde. Förutom dessa kan du lägga till egna klassificeringar. De femstjärniga klassificeringar som visas på katalogsidor genereras för varje produkt.

![Exempel på butiker - egna klassificeringar](./assets/attribute-custom-ratings-review.png){width="700" zoomable="yes"}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Rating]**.

1. Klicka på i det övre högra hörnet **[!UICONTROL Add New Rating]**.

   ![Admin - Klassificeringar](./assets/product-reviews-rating.png){width="700" zoomable="yes"}

1. I _[!UICONTROL Rating Title]_anger du **[!UICONTROL Default Value]**för det nya omdömet.

   Ange även översättningen för varje butiksvy, om tillämpligt.

   ![Inställningar för klassificeringsrubrik](./assets/product-rating-title.png){width="600" zoomable="yes"}

1. I _Värderingssynlighet_ avsnitt, ange **[!UICONTROL Visibility In]** till butiksvyn där klassificeringen ska användas.

   Om du vill välja flera butiksvyer håller du ned Ctrl-tangenten (PC) eller Kommando-tangenten (Mac) och klickar på varje objekt.

   >[!NOTE]
   >
   >Klassificeringar visas inte om de inte tilldelats en butiksvy.

1. För **[!UICONTROL Sort Order]** anger du ett nummer som bestämmer ordningen för den här klassificeringen när den anges tillsammans med andra.

1. Om du vill visa din klassificering i butiken väljer du **[!UICONTROL Is Active]** kryssrutan.

   ![Inställningar för klassificeringssynlighet](./assets/product-rating-visibility.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Rating]**.

   Den genomsnittliga klassificeringen för alla recensioner visas för varje produkt på produktstödrastersidan för katalogen.

   ![Katalogsida](./assets/catalog-rating-page.png){width="700" zoomable="yes"}
