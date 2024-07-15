---
title: Presentkortsprodukt
description: Lär dig hur du skapar en presentkortsprodukt som skapar en unik kod som en mottagarkund kan lösa in vid utcheckningen.
exl-id: bc4b60fe-10b3-4d17-85ce-35c2720c90a2
feature: Catalog Management, Products, Gift
source-git-commit: e72977596c4479d2e94b1e066ee166d22cb12405
workflow-type: tm+mt
source-wordcount: '962'
ht-degree: 0%

---

# Presentkortsprodukt

{{ee-feature}}

Varje presentkort har en unik kod som bara en kund kan få tillbaka vid utcheckningen. En [kodpool](../stores-purchase/product-gift-card-accounts.md#step-3-establish-the-gift-card-code-pool) måste upprättas innan presentkort kan säljas. Mer information om hur presentkort löses in i kundvagnen finns i [Presentkortsarbetsflöde](../stores-purchase/product-gift-card-workflow.md).

![Produktsida för presentkort](./assets/storefront-giftcard-product-page.png){width="700" zoomable="yes"}

Det finns tre typer av presentkortsprodukter:

- **Virtuellt** - Ett virtuellt presentkort skickas till mottagarens e-postadress, som krävs när du köper presentkortet. Ingen leveransadress behövs.

- **Fysiskt** - Ett fysiskt presentkort skickas till mottagarens adress, vilket krävs vid köpet av presentkortet.

- **Kombinerad** - Ett kombinerat presentkort skickas och skickas med e-post till mottagaren. Mottagarens e-postadress och leveransadress krävs vid köpet av presentkortet.

## Skapa en presentkortsprodukt

I följande instruktioner visas hur du skapar ett presentkort med hjälp av en [produktmall](attribute-sets.md), obligatoriska fält och grundläggande inställningar. Alla obligatoriska fält är markerade med en röd asterisk (`*`). När du är klar med grunderna kan du slutföra de andra produktinställningarna efter behov.

### Steg 1: Välj produkttyp

1. Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]** på sidofältet _Admin_.

1. I det övre högra hörnet på _[!UICONTROL Add Product]_( ![Menypil](../assets/icon-menu-down-arrow-red.png){width="25"}  ) väljer du **[!UICONTROL Gift Card]**.

   ![Lägg till presentkort](./assets/product-add-gift-card.png){width="700" zoomable="yes"}

### Steg 2: Välj attributuppsättning

Du kan använda standardattributuppsättningen `Gift Card` eller välja en annan. Gör något av följande om du vill välja den attributuppsättning som används som mall för produkten:

- Klicka i fältet **[!UICONTROL Attribute Set]** och ange hela eller en del av attributuppsättningens namn.

- Välj den attributuppsättning som du vill använda i listan som visas.

![Välj attributuppsättning](./assets/product-create-choose-attribute-set-gift-card.png){width="600" zoomable="yes"}

### Steg 3: Slutför de obligatoriska inställningarna

1. Ange **[!UICONTROL Product Name]** som presentkort.

   Du kan också ange typ av presentkort i namnet. Exempel: _Virtuellt presentkort för luma_.

1. Ange en **[!UICONTROL SKU]** för produkten.

   Som standard används produktnamnet som SKU.

1. Ange **[!UICONTROL Card Type]** till något av följande:

   - `Virtual` - Virtuella presentkort levereras via e-post till mottagaren.
   - `Physical` - Fysiska presentkort kan vara masstillverkade i förväg och präglade med unika koder.
   - `Combined` - Ett kombinerat presentkort har samma egenskaper som både ett virtuellt och ett fysiskt presentkort.

   ![Presentkortstyp](./assets/product-create-gift-card-type.png){width="600" zoomable="yes"}

1. Om du vill erbjuda kunden ett val av fasta belopp klickar du på **[!UICONTROL Add Amount]** och anger kortets första fasta värde som ett decimaltal.

   Om du vill ange ett val av fasta belopp upprepar du det här steget för varje.

1. Så här kan du ge kunderna möjlighet att ange värdet på presentkortet:

   - Ange **[!UICONTROL Open Amount]** till `Yes`.

   - Ange värdena **[!UICONTROL Open Amount From]** och **[!UICONTROL To]** för att definiera intervallet för minsta och högsta tillåtna värden.

   Du kan skapa presentkort med fast pris, öppet belopp eller både och.

   >[!NOTE]
   >
   >En presentkortsprodukt har inte ett eget pris i katalogen. Presentkortspriset hämtas från det valda presentkortsbeloppet under köpet.

   ![Presentkortsbelopp](./assets/product-create-gift-card-amounts.png){width="600" zoomable="yes"}

### Steg 4: Slutför de grundläggande inställningarna

1. Ange **[!UICONTROL Quantity]** i lager för ett fysiskt eller kombinerat presentkort.

1. Om presentkortet som ska skickas anger du **[!UICONTROL Weight]** för paketet.

1. Välj `Gift Card` i fältet **[!UICONTROL Categories]**.

Det kan finnas ytterligare enskilda attribut som beskriver produkten. Markeringen varierar attributuppsättningen och du kan slutföra dem senare.

### Steg 5: Fyll i presentkortsinformationen

Avsnittet _[!UICONTROL Gift Card Information]_i produktinställningarna kan användas för att åsidosätta [presentkortskonfigurationen](../configuration-reference/sales/gift-cards.md) som avgör hur kortet hanteras.

1. Bläddra ned till avsnittet _[!UICONTROL Gift Card Information]_.

   Standardinställningarna i det här avsnittet bestäms av systemkonfigurationen.

   ![Presentkortsinformation](./assets/product-gift-card-information.png){width="600" zoomable="yes"}

1. Ändra ytterligare fält efter hur du vill att presentkortet ska fungera:

   - **[!UICONTROL Treat Balance as Store Credit]** - Avgör om presentkortsinnehavaren kan lösa in saldot som butikskrediter.

   - **[!UICONTROL Lifetime (days)]** - Anger antalet dagar efter köpet tills presentkortet går ut. Om du inte vill ange en gräns för kortets livslängd lämnar du det här fältet tomt.

   - **[!UICONTROL Allow Message]** - Avgör om köparen av presentkortet kan ange ett meddelande till mottagaren. Ett presentmeddelande kan inkluderas för både virtuella (e-postade) och fysiska (levererade) presentkort.

   - **[!UICONTROL Email Template]** - Bestämmer e-postmallen som används för meddelandet som skickas till mottagaren av ett presentkort.

### Steg 6: Fyll i produktinformationen

Fyll i informationen i följande avsnitt efter behov:

- [Innehåll](product-content.md)
- [Bilder och video](product-images-and-video.md)
- [Samhörande produkter, merförsäljning och korsförsäljning](related-products-up-sells-cross-sells.md)
- [Sökmotoroptimering](product-search-engine-optimization.md)
- [Anpassningsbara alternativ](settings-advanced-custom-options.md)
- [Produkter på webbplatser](settings-basic-websites.md)
- [Design](settings-advanced-design.md)
- [Presentalternativ](product-gift-options.md)

### Steg 7: Publish produkten

1. Om du är redo att publicera produkten i katalogen anger du **Aktivera produkt** till `Yes`.

1. Gör något av följande:

   **Metod 1:** Spara och förhandsgranska

   - Klicka på **[!UICONTROL Save]** i det övre högra hörnet.

   - Om du vill visa produkten i din butik väljer du **[!UICONTROL Customer View]** på menyn _Admin_ ( ![Menypil](../assets/icon-menu-down-arrow-black.png) ),

   ![Kundvy](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **Metod 2:** Spara och stäng

   Välj **[!UICONTROL Save & Close]** på menyn _[!UICONTROL Save]_( ![Menypil ](../assets/icon-menu-down-arrow-red.png){width="25"} ).

## Saker att komma ihåg

- En _kodpool_ med unika nummer måste genereras innan ett presentkort kan erbjudas för försäljning.

- Presentkort kan anges till `Redeemable` eller `Non-Redeemable`.

- Skatter tillämpas **_inte_** på presentkort under presentkortsköpet. Skatter tillämpas endast på produkter när ett köpt presentkort används för att köpa produkter.

- Presentkortets livslängd kan vara obegränsad eller inställd på ett visst antal dagar.

- Värdet på ett presentkort kan anges till ett fast belopp eller anges till ett öppet belopp med ett lägsta och högsta värde.

- En presentkortsprodukt har inte ett eget pris i katalogen. Presentkortspriset hämtas från det valda presentkortsbeloppet under köpet.

- Ett presentkortskonto för kunden kan skapas när ordern läggs eller när fakturan skickas.
