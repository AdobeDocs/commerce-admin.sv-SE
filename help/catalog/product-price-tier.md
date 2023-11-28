---
title: Nivåpriser
description: Lär dig hur du använder nivåpriser för att erbjuda en mängdrabatt från en produktlista eller produktsida.
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Nivåpriser

Med nivåpriser kan ni erbjuda mängdrabatt från en produktlista eller en produktsida i butiken. Rabatten kan tillämpas på en viss butiksvy, kundgrupp eller delad katalog.

Om du har många produkter att uppdatera är det mest effektivt att importera nivåprisändringarna i stället för att ange dem individuellt. Mer information finns i [Importera nivåpriser](../systems/data-import-price-tier.md).

![Pris på en butiksproduktsida](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

På produktsidan beräknas kvantitetsrabatten och ett meddelande visas, till exempel:

`Buy 6 for $5.95 each and save 15%`

Priserna i butiken har företräde från högsta till lägsta kvantitet. Om du har ett skiktpris för kvantiteten `5` och en för `10`och en kund lägger till fem, sex, sju, åtta eller nio artiklar i kundvagnen får kunden det rabatterade priset för kvantiteten `5` nivå. När kunden lägger till den tionde artikeln, det rabatterade priset som anges för kvantiteten `10` skiktet ersätter skiktet för en kvantitet `5`och rabatterat pris för `10` gäller.

## Lägg till en prisnivå för en produkt

1. Öppna produkten i redigeringsläge.

1. Under _[!UICONTROL Price]_fält, klicka **[!UICONTROL Advanced Pricing]**.

1. I _[!UICONTROL Tier Price]_avsnitt, klicka **[!UICONTROL Add]**.

   Om du skapar en nivå med flera priser klickar du på **[!UICONTROL Add]** för varje ytterligare nivå, så att du kan arbeta med alla lager samtidigt. Varje nivå i gruppen har samma webbplats och kundgrupp eller delad katalogtilldelning, men olika kvantitet och pris.

## Konfigurera prisnivån

1. Om din butik har flera webbplatser väljer du **[!UICONTROL Website]** för vilket nivåpriset gäller.

1. Om det behövs kan du begränsa tillgången på prisnivån genom att välja **[!UICONTROL Customer Group]** eller **[!UICONTROL Shared Catalog]** (![B2B för Adobe Commerce](../assets/b2b.svg) Finns med [B2B för Adobe Commerce](./b2b/../introduction.md) endast).

1. För **[!UICONTROL Qty]** anger du den kvantitet som måste beställas för att få rabatten.

   - **Metod 1:** Ange pris som ett fast belopp

     Ange **[!UICONTROL Price]** till `Fixed` och ange det justerade priset för en enhet på den nivån.

     ![Pris i nivå som ett fast belopp](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **Metod 2:** Ange pris som en procentandel

     Ange **[!UICONTROL Price]** till `Discount` och ange det rabatterade priset som en procentandel av produktens baspris.

     Om du till exempel vill ha 15 procents rabatt anger du talet `15`. (Priset sparas med två decimaler, till exempel `15.00`.)

     >[!NOTE]
     >
     >För att få det rabatterade priset beräknas den definierade procentandelen mot det värde som definieras i _[!UICONTROL Price]_ fält, inte _[!UICONTROL Special Price]_ fält.

     ![Pris i procent](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## Slutför priskonfigurationen

1. Om du vill lägga till en annan uppsättning nivåpriser för en annan webbplats eller kundgrupp upprepar du de föregående stegen.

1. När du är klar klickar du på **[!UICONTROL Done]** och sedan **[!UICONTROL Save]**.

>[!NOTE]
>
>The **_final_** produktpriset beräknas som **_minimum_** relevant pris, med följande formel: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Fast pris_** de anpassningsbara alternativen är _not_ påverkas av reglerna för grupppris, pris, specialpris eller katalogpris.
