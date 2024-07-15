---
title: Ange priser och struktur för delade kataloger
description: Med Adobe Commerce B2B får du lära dig hur du ställer in priser och struktur för en delad katalog.
exl-id: 67caf56f-1b31-44bb-98dc-ea6ea7d8a4d5
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 0%

---

# Ange priser och struktur för delade kataloger

Att konfigurera priser och struktur för en delad katalog är en tvåstegsprocess. Den aktuella platsen i processen markeras med en siffra i förloppsindikatorn högst upp på sidan. Du kan när som helst visa det andra steget i processen genom att klicka på förloppsindikatorn. Om du till exempel arbetar med anpassade priser kan du behöva gå tillbaka till produktvalssidan för referens. Klicka bara på **[!UICONTROL Products]** i förloppsindikatorn överst på sidan och klicka sedan på **[!UICONTROL Pricing]** för att gå tillbaka till sidan med anpassade priser. Ditt arbete går inte förlorat i den här processen.

![Produkter i katalog](./assets/shared-catalog-products-workspace.png){width="700" zoomable="yes"}

I standardkategoriträdet är rotkategorin den översta behållaren och kallas _standardkategori_ i exempeldata. När delade kataloger är aktiverade har kategoriträdet en yttre behållare med namnet _Rotkatalog_. Rotkatalogen omfattar alla andra kategoristrukturer som finns i systemet. Mer information finns i [Katalogomfång](../catalog/introduction.md#catalog-scope).

## Steg 1: Öppna den delade katalogprissättningen och strukturkonfigurationen

1. Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]** på sidofältet _Admin_

1. För den delade katalogen i rutnätet går du till kolumnen _[!UICONTROL Action]_och klickar på&#x200B;**[!UICONTROL Set Pricing and Structure]**.

   ![Ange priser och struktur för delad katalog](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. Första gången den delade katalogen konfigureras klickar du på **[!UICONTROL Configure]** för att fortsätta med följande steg.

## Steg 2: Välj produkter

Det första steget i processen är att välja de produkter som du vill inkludera i den delade katalogen. Sidan för produktval innehåller [kategoriträdet](../catalog/category-create.md) till vänster och ett synkroniserat produktrutnät till höger. Om du klickar på en kategori i trädet visas produkterna i kategorin i rutnätet.

Endast kategorier med valda produkter visas i den [översta navigeringen](../catalog/navigation-top.md) när den delade katalogen visas från butiken. Som standard inkluderas bara de tre första kategorinivåerna i butiksnavigeringen, inte rotkategorin.

1. Använd **Store**-väljaren för att ange [scopet](../catalog/introduction.md#product-scope) för konfigurationen.

   Konfigurationens omfång kan bara anges innan den delade katalogen sparas för första gången. Om du senare redigerar produktvalet är inte Store-väljaren tillgänglig.

   ![Välj butik](./assets/shared-catalog-products-scope.png){width="600" zoomable="yes"}

1. Gör något av följande i kategoriträdet:

   - Om du vill inkludera alla produkter klickar du på **[!UICONTROL Select all]** eller markerar kryssrutan för den överordnade kategorin.
   - Om du vill ta med specifika produktkategorier markerar du kryssrutan för varje kategori som du vill ta med.
   - Om du vill inkludera eller exkludera en enskild produkt markerar eller avmarkerar du produktkryssrutan.

   Kommentaren under varje kategori i trädet visar antalet produkter i kategorin som för närvarande ingår i den delade katalogen. Kommentaren under rotkategorin [](../catalog/category-root.md) visar det totala antalet produkter från alla kategorier som för närvarande är markerade för den delade katalogen.

1. Om du vill visa kategoriprodukter i rutnätet klickar du på namnet på kategorin i trädet. När en kategori är markerad händer följande:

   - Växlingsknappen i den första kolumnen i rutnätet är inställd på den gröna _On_ -positionen för varje vald produkt.
   - Om en produkt har tilldelats flera kategorier och inte har valts i någon av dem, är den tillgänglig genom de andra kategorierna och även när du använder [katalogsökning](../catalog/search.md).
   - Systemet ställer automatiskt in [kategoribehörigheter](../catalog/category-permissions.md) till `Allow` för de valda produkterna.

1. Om det behövs kan du använda filtren och andra rutnätskontroller för att hitta de produkter som du vill inkludera i den delade katalogen.

   Du kan välja eller utesluta enskilda produkter genom att klicka på växlingsknappen i den första kolumnen.

   Om du väljer en kategori som inte har några produkter, men är länkad till CMS-innehåll eller en extern länk, visas den i den översta navigeringen i butiken.

   De kategoriinställningar du gör registreras inte permanent i databasen förrän konfigurationen sparas. De sparas dock tillfälligt medan du arbetar med strukturen och prissättningen.

1. Klicka på **[!UICONTROL Next]**.

   ![Välj produkter för katalog](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## Steg 3: Ange anpassade priser

Du kan ange anpassade priser för varje enskild produkt eller använda kontrollen _[!UICONTROL Action]_för att ange anpassade priser som ett fast belopp eller en procentsats för flera produktposter.

- **[!UICONTROL Fixed]**: Anger slutproduktspriset. Om du till exempel anger ett fast pris på $10.00, är priset i butiken för motsvarande företag $10.00.

  >[!NOTE]
  >
  >Det minsta värdet mellan baspriset och det angivna fasta värdet används som slutproduktspris.

  >[!NOTE]
  >
  >**_Fast pris_** anpassningsbara produktalternativ _påverkas_ inte av reglerna för grupppris, pris, specialpris eller katalogpris.

- **[!UICONTROL Percentage]**: Fastställer det anpassade priset baserat på rabattprocenten. Om du till exempel vill erbjuda en rabatt på 10 procent anger du den anpassade pristypen till `Percentage` och anger `10`. Det rabatterade anpassade priset är 90 % av det ursprungliga produktpriset.

Använd kolumnen _[!UICONTROL Custom Price]_i rutnätet om du vill ange ett fast belopp eller en procentsats för följande produkttyper:

- [Enkel](../catalog/product-create-simple.md) (inklusive konfigurerbara produktvariationer)
- [Paket](../catalog/product-create-bundle.md)
- [Nedladdningsbar](../catalog/product-create-downloadable.md)
- [Virtuell](../catalog/product-create-virtual.md)

Kolumnen Anpassat pris är tom för [konfigurerbara](../catalog/product-create-configurable.md)- och [grupperade](../catalog/product-create-grouped.md)-produkttyper och för [presentkort](../catalog/product-gift-card-create.md).

Det går inte att ändra valet av produkter i rutnätet från sidan _Anpassade priser_. Du kan dock använda förloppsindikatorn längst upp på sidan för att gå tillbaka till föregående steg och ändra valet av produkter.

![Välj produkter för katalog](./assets/shared-catalog-custome-prices-step-3.png){width="600" zoomable="yes"}

### Använd ett anpassat pris

1. För en installation på flera platser anger du **[!UICONTROL Website]** till webbplatsen där de anpassade priserna gäller.

   ![Välj webbplats](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. Använd någon av följande metoder för att välja de produkter där det anpassade priset ska gälla.

   - Använd kategoriträdet för att välja alla produkter i en viss kategori.
   - Ställ in kontrollen _[!UICONTROL Mass Actions]_i huvudet på `Select All`.
   - Markera kryssrutan för enskilda produkter.

   Rutnätet visar produkterna i de valda kategorierna och du kan använda standardkontrollerna för att hitta produkter och filtrera listan.

   ![Markera alla](./assets/shared-catalog-custom-pricing-mass-actions.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Actions]** till något av följande:

   - `Set Discount` - Tillämpar en rabattprocent på alla valda produkter. Varje berört produktpris visas som ett **_rabatterat_** pris.
   - `Adjust Fixed Price` - Använder en fast prisrabatt i procent på alla valda produkter. Varje berört produktpris visas som ett **_justerat fast_**-pris.

   ![Åtgärdskontroll - Ange rabatt](./assets/shared-catalog-set-custom-prices-discount-action.png){width="600" zoomable="yes"}

1. Ange rabatt eller prisjustering när du uppmanas till det och klicka på **[!UICONTROL Apply]**.

   ![Ange rabatt](./assets/shared-catalog-set-custom-prices-discount.png){width="400"}<br/>

   ![Justera fast pris](./assets/shared-catalog-set-custom-fixed-prices.png){width="400"}

   Rabatten tillämpas på alla valda produkter och kolumnen _Anpassat pris_ visar vilken typ av rabatt och vilket belopp som används.

   ![Kolumn för anpassat pris med rabatt](./assets/shared-catalog-set-custom-prices-discount-applied.png){width="600" zoomable="yes"}

### Använd ett skiktpris

Med [Tier pricing](../catalog/product-price-tier.md) kan du erbjuda en mängdrabatt för produkter i den delade katalogen. Kolumnen _Tier Price_ i rutnätet innehåller en länk till alternativen _Advanced Pricing_ som gäller specifikt för den delade katalogen. Om produkten redan innehåller skiktprissättning visas antalet befintliga skikt inom parentes efter länken.

Följande instruktioner visar hur du tillämpar nivåpriser på en enskild produkt. Om du vill tillämpa nivåpriser på flera produkter, se [Priser för importnivå](../systems/data-import-price-tier.md).

1. Gå till kolumnen _Nivåpris_ för produkten i rutnätet och klicka på **[!UICONTROL Configure]**.

   ![Konfigurera nivåpris](./assets/shared-catalog-tier-price-configure.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Add Price]** på sidan _Avancerade priser_ och gör följande:

   ![Katalog- och nivåpris](./assets/shared-catalog-tier-price-configure-add-price.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL Website]** till webbplatsen där skiktpriset gäller.
   - Ange den kvantitet av produkten som måste köpas för att få rabatten.
   - Ange **[!UICONTROL Price]** till någon av följande rabattyper:
      - `Fixed`
      - `Discount`
   - Ange rabattbeloppet.
   - Om du vill ange ett annat skikt klickar du på **Lägg till pris** och upprepar processen för att definiera nästa skikt.

   ![Flera nivåpriser](./assets/shared-catalog-tier-price-configure-multiple-tiers.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Done]** när du är klar.

   I rutnätet visas antalet lager inom parentes i kolumnen _[!UICONTROL Tier Price]_.

   ![Flera nivåer](./assets/shared-catalog-tier-price-configure-parentheses.png){width="600" zoomable="yes"}

## Spara struktur och prissättning

När de anpassade priserna är klara klickar du på **[!UICONTROL Generate Catalog]** och sedan på **[!UICONTROL Save]**.

Den delade katalogen sparas nu i databasen. Dess namn visas i kolumnen _[!UICONTROL Shared Catalog]_i rutnätet_[!UICONTROL Products]_. Nästa steg är att [tilldela den delade katalogen till ett företag](./catalog-shared-assign-companies.md).
