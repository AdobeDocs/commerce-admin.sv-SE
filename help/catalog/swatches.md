---
title: Färgrutor för produkt
description: Lär dig hur du definierar färgrutor för dina konfigurerbara produktlistor.
exl-id: 6163cec4-5d84-4e2c-ba5c-3c22ac4e3f28
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1164'
ht-degree: 0%

---

# Färgrutor för produkt

Kunderna har höga förväntningar på att välja en färg, och det är viktigt att produktbeskrivningarna återger varje tillgänglig färg, mönster eller textur. byxorna i följande exempel är till exempel inte tillgängliga i rött, grönt och blått. De finns bara i vissa nyanser av rött, grönt och blått, som troligen är unika för den här produkten.

![Färgrutor på en produktsida](./assets/storefront-color-swatches.png){width="700" zoomable="yes"}

För [konfigurerbara produkter](product-create-configurable.md) kan färgen indikeras av en visuell färgruta, en textfärgruta eller en indatakontroll. Färgrutor kan användas på produktsidan, i produktlistor och i [lageruppbyggd navigering](navigation-layered.md). På produktsidan synkroniseras färgrutorna så att motsvarande produktbild visas när du väljer färgrutan. När kunden väljer färgrutan visas motsvarande värde i inmatningsfältet och färgrutan markeras som aktuell markering.

>[!NOTE]
>
>Du kan konfigurera färgruteattribut så att de inte visar motsvarande enkla produktbilder när du väljer färgrutan genom att ange alternativvärdet _[!UICONTROL Update Product Preview Image]_&#x200B;till `No` på sidan [!UICONTROL Attribute Edit] i Admin.

## Textbaserade färgrutor

Om en bild inte är tillgänglig för en färgruta visas attributvärdet som text. En textbaserad färgruta fungerar som en knapp med en textetikett och fungerar på samma sätt som en färgruta med en bild. När textbaserade färgrutor används för att visa tillgängliga storlekar stryks alla storlekar som inte är tillgängliga över.

![Textbaserad färgrutemarkering visar storlek som inte finns i lager](./assets/storefront-swatch-size-out-of-stock.png){width="700" zoomable="yes"}

## Färgrutor i navigering i lager

Färgrutor kan också användas i lagerstyrd navigering om egenskapen _[!UICONTROL Use in Layered Navigation]_&#x200B;för färgattributet är inställd på `Yes`. I följande exempel visas både textbaserade färgrutor och färgrutor i lageruppbyggd navigering.

![Färgrutor visas i lagernavigering](./assets/storefront-swatches-layered-navigation.png){width="700" zoomable="yes"}

## Skapa färgrutor för produkter

Färgrutor kan definieras som en komponent i attributet `color` eller konfigureras lokalt för en viss produkt och överföras som [produktbilder](product-image.md#upload-an-image).

I de tidigare exemplen är &quot;Sylvia Capri&quot;-byxorna tillgängliga i specifika värden för `red`, `green` och `blue`. Eftersom färgrutorna togs från produktbilden är varje färg en riktig representation av färgen. Attributet `color` används för att hantera informationen för alla produktfärger och färgrutor.

### Steg 1: Skapa färgrutorna

Använd någon av följande metoder för att skapa färgrutor för dina produkter.

#### Metod 1: Lägga till en färgruta

1. Om du vill fånga en produkts verkliga färg öppnar du bilden i en fotoredigerare och använder pipettverktyget för att identifiera den exakta färgen och noterar det motsvarande hexadecimala värdet.

   ![Hexadecimala färgvärden](./assets/swatch-hex-values.png){width="400"}

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**&#x200B;på sidofältet_ Admin _.

1. Öppna attributet _color_ i redigeringsläget i rutnätet.

1. Kontrollera att **[!UICONTROL Catalog Input Type for Store Owner]** är inställd på `Visual Swatch`.

1. Om du inte vill visa motsvarande enkla produktbilder när färgrutan väljs på produktvisningssidan anger du **[!UICONTROL Update Product Preview Image]** till `No`.

1. Klicka på **[!UICONTROL Add Swatch]** under _[!UICONTROL Manage Swatch (Values of Your Attribute)]_&#x200B;och gör följande:

   ![Hantera värden för färgrutor](./assets/attribute-color-manage-swatch-values.png){width="600" zoomable="yes"}

   - Klicka på den nya färgrutan i kolumnen _Färgruta_ och välj **[!UICONTROL Choose a color]** på menyn.

     ![Välj en färgrutefärg](./assets/attribute-color-swatch-menu.png){width="500" zoomable="yes"}

   - Placera markören i fältet **#** i färgväljaren, ta bort det aktuella värdet och ange det hexadecimala värdet på sex tecken för den nya färgen.

     ![Ange det hexadecimala värdet](./assets/attribute-swatch-color-picker-hex-value.png){width="500" zoomable="yes"}

   - Om du vill spara färgrutan klickar du på ikonen _Färghjul_ ( ![Färg-ikon](../assets/icon-color-wheel.png) ) i det nedre högra hörnet av färgväljaren.

   - I kolumnen _Admin_ anger du en etikett som beskriver färgen för lagringsadministratören.

     Om det är tillämpligt kan du även ange översättningen av färgen för varje språk som stöds. I följande exempel inkluderas SKU:n som referens i etiketten _Admin_ eftersom färgerna bara används för en viss produkt. Du kan inkludera ett mellanslag eller ett understreck i etiketten, men inte ett bindestreck.

   - I kolumnen _Är standard_ väljer du den färgruta som ska vara standardalternativ.

   - Om du vill ändra ordningen på färgrutorna klickar du på ikonen _[!UICONTROL Order]_![Sorteringsordning](../assets/icon-sort-order.png) och drar objektet till en ny plats i listan.

     ![Färgruteetiketter](./assets/attribute-swatch-labels.png){width="400"}

1. När du är klar klickar du på **[!UICONTROL Save Attribute]** och uppdaterar cachen när du uppmanas till det.

1. Öppna varje produkt i redigeringsläge och uppdatera attributet **Color** med rätt färgruta.

   Följ stegen nedan om du vill uppdatera flera produkter samtidigt.

#### Metod 2: Överför en färgrutebild

1. Om du vill hämta en bild för en färgruta öppnar du produktbilden i en fotoredigerare och sparar ett fyrkantigt område av bilden som avbildar färgen, mönstret eller texturen.

   Om det behövs kan du upprepa den här åtgärden för varje produktvariant.

   Färgrutans storlek och mått bestäms av temat. Om du sparar en bild som en fyrkant bevaras vanligtvis ett mönsters proportioner.

   ![Färgrutebilder](./assets/swatch-samples.png){width="400"}

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**&#x200B;på sidofältet_ Admin _.

1. Öppna attributet **[!UICONTROL color]** i redigeringsläge i rutnätet.

1. Kontrollera att **[!UICONTROL Catalog Input Type for Store Owner]** är inställd på `Visual Swatch`.

1. Om du inte vill visa motsvarande enkla produktbilder när färgrutan väljs på produktvisningssidan anger du **[!UICONTROL Update Product Preview Image]** till `No`.

1. Under _[!UICONTROL Manage Swatch]_(värden för ditt attribut) klickar du på&#x200B;**[!UICONTROL Add Swatch]**&#x200B;och gör följande:

   - I kolumnen _[!UICONTROL Swatch]_&#x200B;klickar du på den nya färgrutan för att visa menyn och väljer **[!UICONTROL Upload a file]**.

   - Navigera till den färgrutefil som du har förberett och välj den fil som ska överföras.

   - Upprepa dessa steg för varje färgrutebild.

   - Ange etiketterna för Admin och storefront.

     I det här exemplet inkluderas SKU:n i Admin-etiketten som referens eftersom dessa färger endast används för en viss produkt. Du kan inkludera ett mellanslag eller ett understreck i etiketten, men det får inte innehålla ett bindestreck.

     ![Ange etiketter](./assets/swatch-upload.png){width="500" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Attribute]** och uppdaterar cachen när du uppmanas till det.

1. Öppna varje produkt i redigeringsläge och uppdatera attributet **[!UICONTROL Color]** med rätt färgruta.

   Följ stegen nedan om du vill uppdatera flera produkter samtidigt.

### Steg 2: Uppdatera produkterna

1. Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]** på sidofältet _Admin_.

1. Använd **[!UICONTROL Filter]** för att visa listan efter namn eller SKU och endast inkludera de tillämpliga produkterna.

1. Markera kryssrutan för varje produkt som färgrutan gäller för i rutnätet.

1. Ange **[!UICONTROL Actions]** till `Update Attributes`.

   I det här exemplet väljs alla blå konfigurationer av byxorna.

   ![Uppdatera attribut för produktfärgruta](./assets/swatch-apply-update-attributes.png){width="600" zoomable="yes"}

1. Bläddra ned till attributet **[!UICONTROL Color]** och markera kryssrutan **[!UICONTROL Change]**.

   ![Ändra kryssruta](./assets/swatch-update-attributes-choose-color.png){width="400"}

1. Välj den färgruta som gäller för de valda produkterna och klicka på **[!UICONTROL Save]**.

1. Uppdatera cacheminnet när du uppmanas till detta.

   ![Färgrutan visas i butiken](./assets/swatch-blue-schmear.png){width="200"}

## Lägga till färgrutor i en enkel produkt

1. Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]** på sidofältet _Admin_.

1. Öppna en produkt i redigeringsläge, kontrollera produktstatus (bör vara aktiverad).

1. Klicka på knappen **[!UICONTROL Create Configurations]** (under fliken `Configurations`).

1. I popup-fönstret väljer du färgattributet och **[!UICONTROL Next]**.

1. Välj färgrutor från attributet som du vill inkludera i den här produkten.

1. Klicka på **[!UICONTROL Next]** i förloppsindikatorn.

1. [Konfigurera bilder, pris och kvantitet](product-create-configurable.md#step-3-configure-the-images-price-and-quantity).

   I det här steget anger du bilder, priser och kvantitet för varje konfiguration. De tillgängliga alternativen är desamma för alla, och du kan bara välja ett. Du kan använda samma inställning för alla SKU:er, använda en unik inställning för varje SKU:er eller hoppa över inställningarna för tillfället.

1. När konfigurationen för bilder, pris och kvantitet är klar klickar du på **[!UICONTROL Next]** i det övre högra hörnet.

   De aktuella produktvariationerna visas längst ned i avsnittet Konfiguration. Om du är nöjd med konfigurationerna klickar du på **[!UICONTROL Generate Products]**.
