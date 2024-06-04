---
title: Kundkonfiguration
description: Läs mer om de kundvagnsfunktioner som du kan konfigurera för att stödja köpupplevelsen i din butik.
exl-id: b98ec7ce-9354-4f03-b67e-dd1587f0c866
feature: Shopping Cart, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '2449'
ht-degree: 0%

---

# Kundkonfiguration

Kundvagnskonfigurationen avgör hur kundvagnen fungerar för dina butikskunder, inklusive när kunden omdirigeras till kundvagnssidan och vilka bilder som används för produktminiatyrbilder. Du kan också begära att en order ska nå ett minimibelopp innan utcheckningsprocessen börjar, ange hur många dagar offertpriserna ska vara giltiga och ange ordningen för artiklarna i _Ordersummor_ -avsnitt.

[**Mini cart**](#mini-cart) - Konfigurera det här alternativet för att bestämma om kundvagnens länk/ikon visar antalet olika produkter (eller SKU:er) i kundvagnen eller det totala antalet artiklar.

[**Mini cart-länk**](#configure-the-cart-link) - Konfigurera det här alternativet för att avgöra om minivagnen visas när en kund klickar på antalet artiklar i kundvagnen högst upp på en butikssida.

[**Omdirigering till kundvagn**](#redirect-to-cart)- Konfigurera det här alternativet för att bestämma om kundvagnssidan ska visas när en artikel läggs till i kundvagnen eller endast när en kund väljer att gå till sidan.

[**Offertlivstid**](#quote-lifetime) - Konfigurera det här alternativet för att ange hur länge ett pris är giltigt.

[**Minsta orderbelopp**](#minimum-order-amount) - Konfigurera dessa alternativ för att ange ett minimibelopp, efter att rabatter har tillämpats, som delsummor för order måste uppfylla och meddelandet visas i kundvagnen.

[**Minsta orderkvantitet**](#minimum-order-quantity) - Konfigurera dessa alternativ för att ange ett minsta antal objekt som krävs för att göra en beställning.

[**Miniatyrbilder**](#cart-thumbnails)  - Konfigurera alternativen för vagnsminiatyrbilder för att bestämma vilka miniatyrbilder som visas i vagnen för grupperade eller konfigurerbara produkter.

[**Presentalternativ**](#gift-options) - Konfigurera presentalternativ för att avgöra om kunderna kan lägga till ett presentmeddelande eller gratulationskort och om det finns presentalternativ.

>[!NOTE]
>
>Information om hur du konfigurerar utcheckningsprocessen finns i [Utcheckningsalternativ](checkout-process.md).

## Mini cart

The _mini cart_ visar en sammanfattning av artiklarna i kundvagnen. Den är aktiverad som standard och visas när du klickar på länken Cart överst på sidan.
Länken kan konfigureras för att visa antalet olika produkter (eller SKU:er) i kundvagnen, eller det totala antalet artiklar.

![Köparen visar sidofältet i kundvagnen på en produktsida](./assets/storefront-mini-cart-watch.png){width="700" zoomable="yes"}

>[!NOTE]
>
>För _registrerad_ -kunder kan det finnas tillfällen då Mini Cart inte kan synkroniseras mellan flera enheter och webbläsare automatiskt. Om du vill synkronisera miniatyrbilden i sådana fall kan kunden bara öppna [Kundvagn](cart.md) på den enheten eller webbläsaren.

### Konfigurera mini-vagnen

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Checkout]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den _[!UICONTROL Mini Cart]_-avsnitt.

   ![Konfigurera mini-vagnen](../configuration-reference/sales/assets/checkout-mini-cart.png){width="600" zoomable="yes"}

1. Om inställningen gäller en viss butiksvy, [välj butiksvyn](../configuration-reference/scope-change.md#set-the-scope) där konfigurationen gäller.

   Klicka på **[!UICONTROL OK]** för att fortsätta.

1. Ange **[!UICONTROL Display Mini Cart]** till något av följande:

   - `Yes` - Visar minivagnen på butikssidorna. Utseendet på sidofältet beror på temat.
   - `No` - Inaktiverar visning av minikundvagnen på butikssidor.

1. Om visningen är aktiverad uppdaterar du de andra alternativen för att konfigurera visningen:

   - För **[!UICONTROL Number of Items to Display Scrollbar]** anger du antalet objekt som kan visas i sidofältet innan rullningslisten aktiveras.
   - För **[!UICONTROL Maximum Display Recently Added Item(s)]** anger du det maximala antalet nyligen tillagda objekt som du vill ska visas i minivagnen.

1. Klicka på **[!UICONTROL Save Config]**.

### Konfigurera kundvagnslänken

1. På _Administratör_ sidebar **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Checkout]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL My Cart Link]** -avsnitt.

1. Ange **[!UICONTROL Display Cart Summary]** till någon av följande inställningar:

   - `Display item quantities` - Den här inställningen visar det totala antalet produkter i varukorgen, med tillägg av kvantiteterna för varje produkt.
   - `Display number of items in cart` - Den här inställningen visar antalet produktartiklar i kundvagnen, oavsett kvantitet.

   ![Konfigurationsalternativ för Min kundvagnslänk](../configuration-reference/sales/assets/checkout-my-cart-link.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]**.

## Omdirigering till kundvagn

Kundvagnssidan kan konfigureras så att den visas när en artikel läggs till i kundvagnen, eller bara när kunderna väljer att gå till sidan. Den grundläggande informationen om artiklarna som finns i kundvagnen finns alltid i [mini cart](#mini-cart). Beslutet handlar om att balansera fördelarna med att låta kunderna fortsätta handla, och fördelarna med att uppmuntra kunderna att gå vidare till kassan. Det kan vara en enkel fråga om personliga preferenser. Om du vill säkerhetskopiera den med siffror kan du köra ett A/B-test för att se vilket tillvägagångssätt som ger en högre konverteringsgrad.

**_Så här konfigurerar du när kundvagnen visas:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Checkout]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Shopping Cart]** -avsnitt.

   ![Konfigurationsinställningarna för kundvagnen har utökats på sidan](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. Om inställningen gäller en viss butiksvy, [välj butiksvyn](../configuration-reference/scope-change.md#set-the-scope) där konfigurationen gäller.

   Klicka på **[!UICONTROL OK]** för att fortsätta.

1. Ange **[!UICONTROL After Adding a Product Redirect to Shopping Cart]** till något av följande:

   - `Yes` - Visar kundvagnssidan omedelbart efter att en produkt har lagts till i kundvagnen.
   - `No` - Inaktiverar omdirigering till kundvagnen efter att en produkt lagts till i kundvagnen.

1. Klicka på **[!UICONTROL Save Config]**.

## Offertlivstid

Med installation och aktivering av Adobe Commerce B2B kan du lägga till stöd för _Citat_ -funktion. Med den här funktionen kan auktoriserade köpare initiera prisförhandlingsprocessen genom att skicka en begäran från kundvagnen. The _Citat_ rutnätet visar varje mottagen offert och upprätthåller en historik över kommunikationen mellan köpare och säljare. Mer information om B2B-funktionerna finns i [Förhandlade offerter](../b2b/quotes.md) i _Användarhandbok för Adobe Commerce B2B_.

Du kan bestämma hur länge ett pris är giltigt genom att ställa in livslängden för varukorgsofferten i konfigurationen. Om en kund t.ex. lämnar en kundvagn utan tillsyn efter flera dagar kanske priset för vissa artiklar inte längre är detsamma. Som standard är offertens livstid 30 dagar.

**_Så här konfigurerar du offertens livstid:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Checkout]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Shopping Cart]** -avsnitt.

   ![Konfigurationsinställningarna för kundvagnen har utökats på sidan](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. Om inställningen gäller en viss butiksvy, [välj butiksvyn](../configuration-reference/scope-change.md#set-the-scope) där konfigurationen gäller.

   Klicka på **[!UICONTROL OK]** för att fortsätta.

1. För **[!UICONTROL Quote Lifetime (days)]** anger du det antal dagar som ett offertpris fortfarande gäller.

1. Klicka på **[!UICONTROL Save Config]**.

## Minsta orderbelopp

Med konfigurationen kan du ange ett minimibelopp, efter att rabatter har tillämpats, som delsummor för order måste uppnå. Beställningar som skickas till flera adresser kan krävas för att det minsta orderbeloppet per adress ska uppfyllas. Knappen Checka ut blir tillgänglig först när minimiorderbeloppet har uppnåtts.

![Kundvagnen visar ett meddelande om minimiorder](./assets/storefront-cart-minimum-order-amount.png){width="700" zoomable="yes"}

**_Så här konfigurerar du ett minimiorderbelopp:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Sales]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Minimum Order Amount]** -avsnitt.

   ![Alternativen för minimiorderkonfiguration har utökats på sidan](../configuration-reference/sales/assets/sales-minimum-order-amount.png){width="600" zoomable="yes"}

1. Ange ett minimiorderbelopp **[!UICONTROL Enable]** till `Yes`.

1. Om minimibeställningen är aktiverad anger du följande alternativ för att konfigurera kravet:

   - Ange **[!UICONTROL Minimum Amount]** som krävs för delsumman, efter att rabatter har tillämpats.

   - Ange **[!UICONTROL Include Discount Amount]** till något av följande:

      - `Yes` - Kräver att delsumman motsvarar minimibeloppet med eventuella rabatter. Om du använder ett exempel på minst $50 och kundvagnen innehåller en övre kr på $60 med en rabatt på 25 %, blir den resulterande delsumman 45 kr och kundvagnen uppfyller inte minimikravet.
      - `No` - Kräver att delsumman motsvarar minimibeloppet utan några rabatter.

   - Ange **[!UICONTROL Include Tax to Amount]** till något av följande:

      - `Yes` - Kräver att delsumman uppfyller minimibeloppet inklusive moms.
      - `No` - Kräver att delsumman uppfyller minimibeloppet utan moms.

1. Du kan också anpassa meddelandeinställningar för minimiorderbelopp:

   - För **[!UICONTROL Description Message]** anger du den text som du vill använda för att anpassa meddelandet som visas högst upp i kundvagnen när delsumman inte uppfyller minimibeloppet.

   - För **[!UICONTROL Error to Show in Shopping Cart]** anger du den text som du vill använda för att anpassa felmeddelandet i kundvagnen.

   Lämna meddelandebeskrivningsfälten tomma om du vill använda standardmeddelandena.

1. Konfigurera vid behov minimiorderbeloppsinställning för fleradressorder:

   - Om du vill kräva att varje adress i en fleradressorder uppfyller minimiorderbeloppet anger du **[!UICONTROL Validate Each Address Separately in Multi-address Checkout]** till `Yes`.

   - Du kan också anpassa meddelandeinställningar för minimiorderbelopp:

      - **[!UICONTROL Multi-address Description Message]** - Ange den text som du vill använda för att anpassa meddelandet som visas högst upp i kundvagnen för order med flera adresser som inte uppfyller minimikraven.

      - **[!UICONTROL Multi-address Error to Show in Shopping Cart]** - Ange den text som du vill använda för att anpassa felmeddelandet i kundvagnen för beställningar med flera adresser som inte uppfyller minimikraven. Skriv texten i rutan.

     Lämna meddelandebeskrivningsfälten tomma om du vill använda standardmeddelandena.

1. Klicka på **[!UICONTROL Save Config]**.

## Minsta orderkvantitet

Du kan ange den minsta tillåtna kvantiteten för en order. Den minsta kvantiteten kan också konfigureras för varje kundgrupp.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL Inventory]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Product Stock Options]** -avsnitt.

   ![ProduktStock-alternativ](../configuration-reference/catalog/assets/catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

1. För **[!UICONTROL Minimum Qty Allowed in Shopping Cart]**, anger minimikvantiteten för produkten för en order.

   Rensa **[!UICONTROL Use system value]** om du vill ändra inställningarna.

   - Ändra **[!UICONTROL Customer Group]** ange till en viss grupp och ange **[!UICONTROL Minimum Qty]** för den gruppen. Om du vill lägga till ytterligare en grupp och kvantitetsbegränsning klickar du på **[!UICONTROL Add Minimum Qty]**.

   - Om du vill ange samma minimikvantitet för alla kunder ska du behålla `ALL GROUPS` och ange **[!UICONTROL Minimum Qty]**.

1. Klicka på **[!UICONTROL Save Config]**.

   ![Minsta kvantitetskrav i kundvagn](./assets/minimum-qty-allowed-in-shopping-cart.png){width="700" zoomable="yes"}

## Miniatyrbilder

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)

Miniatyrbilderna som visas i kundvagnen ger kunderna en snabb översikt över de artiklar de håller på att köpa. För produkter med flera alternativ kanske bilden inte matchar variationen i produkten som finns i kundvagnen. Om kunden köper ett objekt i en viss färg, helst, bör miniatyrbilden i kundvagnen matcha.

Miniatyrbilden för både grupperade och konfigurerbara produkter kan ställas in så att den visas antingen från den överordnade produkten eller från produktvariationen.

![I kundvagnen visas miniatyrbilder för varje produkt](./assets/storefront-cart.png){width="700" zoomable="yes"}

**_Så här konfigurerar du kundvagnsminiatyrer:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Checkout]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Shopping Cart]** -avsnitt.

   ![Konfigurationsinställningarna för kundvagnen har utökats på sidan](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Grouped Product Image]** för att fastställa miniatyrbilden som används i vagnen för [grupperade produkter](../catalog/product-create-grouped.md):

   - `Product Thumbnail Itself` - Använder den miniatyrbild som är kopplad till produktvariationen som läggs till i kundvagnen.
   - `Parent Product Thumbnail` - Använder den miniatyrbild som tilldelats den överordnade produkten.

1. Ange **[!UICONTROL Configurable Product Image]** för att fastställa miniatyrbilden som används i vagnen för [konfigurerbara produkter](../catalog/product-create-configurable.md):

   - `Product Thumbnail Itself` - Använder den miniatyrbild som är kopplad till produktvariationen som läggs till i kundvagnen.
   - `Parent Product Thumbnail` - Använder den miniatyrbild som tilldelats den överordnade produkten.

1. Klicka på **[!UICONTROL Save Config]**.

## Presentalternativ

Valet av tillgängliga presentalternativ visas i kundvagnen innan utcheckningsprocessen börjar. Presentalternativinställningens konfiguration avgör om kunderna kan lägga till ett presentmeddelande eller gratulationskort och om det finns presentalternativ tillgängliga. Varje artikel i beställningen kan ha ett separat meddelande och en separat presentförpackning. När det gäller hela beställningen kan kunden även lägga till ett presentkort och ett presentkort.

![Exempel på butiksskylt - Presentalternativ i kundvagn](./assets/storefront-cart-gift-options-for-products-or-order.png){width="700" zoomable="yes"}

Presentationsalternativskonfigurationen gäller hela webbplatsen, men kan åsidosättas på produktnivå.

### Aktivera presentalternativ

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Sales]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Gift Options]** på sidan.

   ![Försäljningskonfiguration - Inställningar för presentalternativ](../configuration-reference/sales/assets/sales-gift-options.png){width="600" zoomable="yes"}

1. Ange alternativ för presentmeddelanden enligt dina önskemål:

   - För **[!UICONTROL Allow Gift Messages on Order Level]**, markera `Yes` för att aktivera ett enda presentmeddelande för hela beställningen.
   - För **[!UICONTROL Allow Gift Messages for Order Items]**, markera `Yes` för att kunna lägga till separata presentmeddelanden för enskilda artiklar i kundvagnen.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Ange önskade alternativ för presentationer:

   - För **[!UICONTROL Allow Gift Wrapping on Order Level]**, markera `Yes` om du vill ha en enda presentförpackning för hela beställningen.
   - För **[!UICONTROL Allow Gift Wrapping for Order Items]**, markera `Yes` för att göra det möjligt att lägga till en enskild present till varje artikel i kundvagnen.

   Du kan också definiera olika [presentationer](#gift-wrap) så att kunderna kan välja själva förpackningen.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Om du vill ge kunderna möjlighet att inkludera ett presentkvitto anger du **[!UICONTROL Allow Gift Receipt]** till `Yes`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Om du vill ge kunderna möjlighet att inkludera ett utskrivet kort anger du **[!UICONTROL Allow Printed Card]** till `Yes`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Ange **[!UICONTROL Default Price for Printed Card]**.

1. Klicka på **[!UICONTROL Save Config]**.

### Presentbrytning

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)

Presentomslutning är tillgängligt för alla produkter som kan levereras och kan erbjudas för enskilda artiklar eller för hela beställningen. Du kan debitera ett separat pris för varje presentationsdesign och överföra en miniatyrbild för varje design som visas som ett alternativ för en produkt i kundvagnen. När en kund klickar på miniatyrbilden av presentationen visas en bild i full storlek. Under utcheckningsgranskningen visas kostnaden för presentfigursättningen med den andra [kassasummor](checkout-totals-sort-order.md) i _Ordersammanfattning_ -avsnitt.

Presentfigursättningsbilden ska vara en färgruta som visar det upprepade mönstret och kan även innehålla ett exempel på det band som ska användas. Du kan antingen skanna papperet eller ta ett foto av ett emballage. Den överförda bilden kan vara en GIF-, JPG- eller PNG-bild och ska vara fyrkantig. I följande exempel är den överförda figursättningsbilden 230 x 230 pixlar.

![Presentalternativ i kundvagn](./assets/storefront-cart-gift-options-gift-wrap.png){width="700" zoomable="yes"}

#### Lägg till en figursatt design

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Wrapping]**.

   ![Presentomslutningsrutnät](./assets/gift-wrapping.png){width="700" zoomable="yes"}

1. Klicka på i det övre högra hörnet **[!UICONTROL Add Gift Wrapping]**.

1. Ange namnet på **[!UICONTROL Gift Wrapping Design]** visas vid utcheckning.

   Om det behövs kan du ändra **[!UICONTROL Scope]** och konfigurera olika namn för varje butiksvy.

1. Välj **[!UICONTROL Websites]** där presentationen finns tillgänglig.

1. Ange **[!UICONTROL Status]** till `Enabled`.

   Om du har ett säsongsbundet radbrytningsalternativ kan du ange det till `Disabled` om du inte vill att alternativet ska vara tillgängligt.

1. Ange **[!UICONTROL Price]** av presentdesignen.

   Den här inställningen kan åsidosättas av presentpriset som anges på produktnivån.

   ![Ny figursättning](./assets/gift-wrapping-new.png){width="600" zoomable="yes"}

1. Så här överför du en miniatyr **[!UICONTROL Image]** av presentpaketet, klicka **[!UICONTROL Choose File]** och välj den fil som ska överföras från din katalog.

   En miniatyrbild av bilden visas i _[!UICONTROL Gift Wrapping Information]_när posten har sparats.

1. Klicka på **[!UICONTROL Save]**.

#### Redigera en figursatt design

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Wrapping]**.

1. Hitta presentradsposten i listan.

1. I _Åtgärd_ kolumn, klicka **[!UICONTROL Edit]**.

   ![Redigera information om presentomslutning](./assets/gift-wrapping-edit.png){width="600" zoomable="yes"}

1. Gör de ändringar som behövs.

1. Klicka på **[!UICONTROL Save]**.

#### Ta bort presentfigursättning

Med _Presentfigursättning_ om du vill öppna stödrastret använder du någon av dessa metoder för att ta bort figursatta designer.

**_Metod 1: Ta bort en enstaka figursatt design_**

1. Öppna presentationsdesignen i redigeringsläge.

1. Klicka på längst upp på arbetsytan **[!UICONTROL Delete]**.

1. Klicka på **[!UICONTROL OK]** för att bekräfta.

**_Metod 2: Ta bort flera presentfigursättningar_**

1. I _Presentfigursättning_ markerar du kryssrutan för varje figursättningsdesign som du vill ta bort.

1. Ange **[!UICONTROL Actions]** styra till `Delete`.

1. Klicka på **[!UICONTROL Submit]**.

### Moms för presentalternativ

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)

Priserna för presentkort och presentkort kan konfigureras så att de inkluderar eller exkluderar moms, eller så att båda alternativen visas. Du kan också ange en momsklass för dessa objekt, antingen på global nivå eller på webbplatsnivå.

**_Så här konfigurerar du moms för presentalternativ:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Tax]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Tax Classes]** -avsnitt.

   ![Konfiguration av momsklass](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Tax Class for Gift Options]** till den tillämpliga skatteklassen.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** -avsnitt.

   ![Visningsinställningar för order, fakturor, kreditnotor](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Display Gift Wrapping Prices]** till något av följande:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Ange **[!UICONTROL Display Printed Card Prices]** till något av följande:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Klicka på **[!UICONTROL Save Config]**.
