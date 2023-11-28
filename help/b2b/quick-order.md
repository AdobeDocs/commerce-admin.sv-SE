---
title: Snabborder
description: Läs mer om funktioner för snabb beställning och hur ni gör det möjligt för era kunder.
exl-id: 7007e1b4-a64f-46fe-a235-3ca9f64e77e4
feature: B2B, Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# Snabborder

The _Snabbordning_ funktionen minskar beställningsprocessen till flera klick för kunder som känner till produktnamnet eller SKU:n för de produkter de vill beställa. Beställningar med flera SKU:er kan anges manuellt eller importeras till formuläret Snabbordning. Snabbbeställning kan användas av kunder som är inloggade på sina konton och av gäster. När det är aktiverat visas _Snabbordning_ visas högst upp på sidan bredvid kundnamnet.

![Länk till snabbbeställning](./assets/quick-order-link.png){width="700" zoomable="yes"}

## Aktivera snabbbeställningar för din butik

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I _[!UICONTROL General]_väljer du **[!UICONTROL B2B Features]**.

1. Ange **[!UICONTROL Enable Quick Order]** till `Yes`.

   ![Aktivera snabbordning](./assets/quick-orders-config.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]**.

1. Klicka på [Cachehantering](../systems/cache-management.md) och uppdatera ogiltiga cacheminnen.

## Snabborderarbetsflöden

Kunder kan ange produkter för snabbbeställningar på något av följande sätt.

### Metod 1: Ange enskilda produkter

1. Kunden klickar på **[!UICONTROL Quick Order]** länk.

1. Väljer produkt efter SKU eller produktnamn:

   Placera en **snabbbeställning från SKU** och kunden gör följande:

   - Anger **[!UICONTROL SKU]**.

   - Klickningar **[!UICONTROL Add to List]**.

     SKU:n visas på inmatningsraden med produktinformationen nedan.

     ![Snabbeställningsinformation](./assets/quick-order-product-detail.png){width="600" zoomable="yes"}

   Placera en **snabbbeställ efter produktnamn** och kunden gör följande:

   - Anger de första tecknen i **[!UICONTROL Product Name]**.

     >[!NOTE]
     >
     >Använd inte _Retur_ för att välja namnet på produkten.

   - När listan över möjliga matchningar visas klickar kunden på produkten som de vill beställa.

     ![Klicka för att välja produktnamn](./assets/quick-order-product-name.png){width="700" zoomable="yes"}

1. Anger **[!UICONTROL Qty]**.

1. Om du använder nästa inmatningsrad upprepas processen så många gånger som behövs.

1. Klickningar **[!UICONTROL Add to Cart]**.

### Metod 2: Ange flera produkter

1. I **[!UICONTROL Enter Multiple SKUs]** gör kunden något av följande:

   - Ange en SKU per rad

   - Anger alla SKU:er på samma rad, avgränsade med kommatecken och utan mellanslag.

     ![Ange flera SKU:er](./assets/quick-order-skus.png){width="600" zoomable="yes"}

1. Om du vill lägga till produkterna i listan klickar du på **[!UICONTROL Add to List]**.

1. Anger **[!UICONTROL Qty]** som ska beställas för varje artikel i listan.

   ![Snabbeställningslista](./assets/quick-order-skus-detail.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Om produkten har de alternativ som krävs uppmanas kunden att välja alternativen. De kan vänta tills de når kundvagnen och lägga till produktalternativ.

   ![Välj alternativ](./assets/quick-order-skus-product-options.png){width="600" zoomable="yes"}

### Metod 3: Överför en lista över produkter

1. I _[!UICONTROL Add from File]_avsnitt, klicka **[!UICONTROL Download Sample]**om du vill hämta en ordermall.

   ![Lägg till från fil](./assets/quick-order-skus-add-from-file.png){width="600" zoomable="yes"}

1. Öppnar den hämtade filen.

1. Använder mallen för att lägga till SKU:er för produkten som ska överföras för snabborderlistan.

1. När det är klart klickar du **[!UICONTROL Save]**.

   ![SKU:er att överföra](./assets/quick-order-skus-add-from-file-sample.png){width="400" zoomable="yes"}

1. Klicka för att överföra filen **[!UICONTROL Choose]** och markerar filen i systemet.

   Objekten läggs till i listan Snabbordning.

1. När det är klart klickar du **[!UICONTROL Add to Cart]**.

När kunden har skapat den snabba beställningen kan de fortsätta till kassan som vanligt.

![Snabbordning](./assets/quick-order-add-to-cart.png){width="700" zoomable="yes"}
