---
title: Nivåpriser
description: Lär dig hur du använder nivåpriser för att erbjuda en mängdrabatt från en produktlista eller produktsida.
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 8d73a3a635c20e636c4b8bde41a4f807d3fd9f2e
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 0%

---

# Nivåpriser

Med nivåpriser kan ni erbjuda mängdrabatt från en produktlista eller en produktsida i butiken. Rabatten kan tillämpas på en viss butiksvy, kundgrupp eller delad katalog.

Om du har många produkter att uppdatera är det mest effektivt att importera nivåprisändringarna i stället för att ange dem individuellt. Mer information finns i [Importera nivåpriser](../systems/data-import-price-tier.md).

![Nivåpris på en butiksproduktsida](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

På produktsidan beräknas kvantitetsrabatten och ett meddelande visas, till exempel:

`Buy 6 for $5.95 each and save 15%`

Priserna i butiken har företräde från högsta till lägsta kvantitet. Om du har ett nivåpris för kvantiteten `5` och en för `10`, och en kund lägger till fem, sex, sju, åtta eller nio artiklar i kundvagnen, får kunden det rabatterade priset för kvantitetsnivån `5`. När kunden lägger till den tionde artikeln ersätter det rabatterade priset som anges för nivån `10` skiktet skiktet för kvantiteten `5`, och det rabatterade priset för `10` gäller.

## Lägg till en prisnivå för en produkt

1. Öppna produkten i redigeringsläge.

1. Klicka _[!UICONTROL Price]_nedanför fältet **[!UICONTROL Advanced Pricing]**.

1. Klicka på _[!UICONTROL Tier Price]_i avsnittet **[!UICONTROL Add]**.

   Om du skapar en nivå med flera priser klickar du på **[!UICONTROL Add]** för varje ytterligare nivå så att du kan arbeta med alla nivåer samtidigt. Varje nivå i gruppen har samma webbplats och kundgrupp eller delad katalogtilldelning, men olika kvantitet och pris.

## Konfigurera prisnivån

1. Om din butik har flera webbplatser väljer du den **[!UICONTROL Website]** som nivåpriset gäller för.

1. Om det behövs kan du begränsa tillgängligheten för prisnivån genom att välja **[!UICONTROL Customer Group]** eller **[!UICONTROL Shared Catalog]** (![Adobe Commerce B2B](../assets/b2b.svg) endast tillgänglig med [Adobe Commerce B2B](./b2b/../introduction.md)).

1. För **[!UICONTROL Qty]** anger du den kvantitet som måste beställas för att få rabatten.

   - **Metod 1:** Ange priset som ett fast belopp

     Ange **[!UICONTROL Price]** till `Fixed` och ange det justerade priset för en enhet på den nivån.

     ![Pris i nivå som fast belopp](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **Metod 2:** Ange pris i procent

     Ange **[!UICONTROL Price]** till `Discount` och ange det rabatterade priset som en procentandel av produktens baspris.

     Ange till exempel talet `15` för en rabatt på 15 procent. (Priset sparas med två decimaler, till exempel `15.00`.)

     >[!NOTE]
     >
     >För att få det rabatterade priset beräknas den definierade procentandelen mot det värde som definieras i fältet _[!UICONTROL Price]_, inte i fältet_[!UICONTROL Special Price]_.

     ![Pris i procent](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## Slutför priskonfigurationen

1. Om du vill lägga till en annan uppsättning nivåpriser för en annan webbplats eller kundgrupp upprepar du de föregående stegen.

1. När du är klar klickar du på **[!UICONTROL Done]** och sedan på **[!UICONTROL Save]**.

>[!NOTE]
>
>Det **_slutliga_**-produktpriset beräknas som det **_lägsta_** relevanta priset, med följande formel: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Fast pris_** anpassningsbara produktalternativ _påverkas_ inte av reglerna för grupppris, pris, specialpris eller katalogpris.

## Aktivera nivåpriser för katalogprisregler

[!BADGE Endast SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce as a Cloud Service-projekt (SaaS-infrastruktur som hanteras av Adobe)."}

I tidigare versioner av Commerce gick det inte att använda nivåpriser tillsammans med katalogprisreglerna. Katalogreglerna ignorerade nivåpriskonfigurationen och beräknade rabatter från det ursprungliga baspriset. Med Adobe Commerce as a Cloud Service kan du nu välja att inkludera nivåpriser i beräkningen av katalogprisregler.

Så här aktiverar du den här funktionen:

1. Navigera till **[!UICONTROL Stores]** > *[!UICONTROL Settings]* > **[!UICONTROL Configuration]** > **[!UICONTROL Sales]** > **[!UICONTROL Sales]** > **[!UICONTROL Promotions]** och ställ in fältet **[!UICONTROL Apply Catalog Price Rule on Grouped Price]** på **[!UICONTROL Yes]**.

   ![Aktivera nivåprissättning för katalogprisregler](../configuration-reference/sales/assets/sales-promotions-settings.png){width="700" zoomable="yes"}

1. Definiera ett skiktpris med kvantiteten `1` för varje specifik kundgrupp eller delad katalog (till exempel `Wholesale`, `Retail` eller handlardefinierad grupp) som du vill ha som mål med katalogprisregler. Det går inte att använda kundgruppen `ALL GROUPS` och den delade katalogen `Default` för detta ändamål. Nivåprissättning har inte aktiverats för någon grupp som inte har ett nivåpris definierat med kvantiteten `1`.

1. Definiera ytterligare nivåpriser med kvantiteter som är större än `1` efter behov. Dessa ytterligare nivåpriser kommer att tillämpas som vanligt när kunden lägger till ytterligare kvantiteter av produkten i kundvagnen. Katalogprisreglerna gäller inte för dessa ytterligare nivåpriser.

Titta på följande exempel för att illustrera hur nivåpriser fungerar med katalogprisregler när du köper en enskild produkt:

- Standardbaspriset för en produkt är 100 USD.
- Ett nivåpris definieras för kundgruppen `Wholesale` med en kvantitet på `1` och ett fast pris på 90 USD.
- En katalogprisregel ger 10 % rabatt för kundgruppen `Wholesale`.

När nivåprissättning är aktiverat för katalogprisregler använder systemet följande flöde för att beräkna det slutliga priset:

1. Innan kunden loggar in visas produktpriset som 100 USD (standardbaspriset).

1. När kunden har loggat in som medlem i gruppen `Wholesale` justeras produktpriset till 90 USD (skiktpriset för gruppen `Wholesale`).

1. Katalogprisregeln tillämpas, vilket ger 10 % rabatt på priset på skiktet 90 USD, vilket resulterar i ett slutpris på 81 USD.

I följande tabell sammanfattas prisberäkningar när nivåprissättning är aktiverat för katalogprisregler och en katalogprisregel ger 10 % rabatt för alla kundgrupper:

Produkt: standardpris $100 (inköp av enstaka artikel)

| Kundgrupp | Pris (ant=1) | Nytt baspris | Slutpris |
|---|---|---|---|
| ALLA GRUPPER | Inte konfigurerad | 100 dollar | $100 - 10% = $90 |
| Grossist | Fast: $85 | $85 | $85 - 10% = $76.50 |
| Återförsäljare | 20 % rabatt | $80 | $80 - 10% = $72.00 |
| VIP | 15 % rabatt | $85 | $85 - 10% = $76.50 |
