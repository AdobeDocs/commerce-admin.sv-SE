---
title: Skapa en katalogprisregel
description: Lär dig hur du skapar en katalogprisregel som tillämpar en rabatt på vissa produkter när en uppsättning villkor uppfylls.
exl-id: 53c5745b-f1c4-4ee8-b995-d2c70f639c7d
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '1662'
ht-degree: 0%

---

# Skapa en katalogprisregel

Följ dessa anvisningar för att tillämpa en rabatt på vissa produkter när en uppsättning villkor uppfylls. Rabatterna för katalogprisregel börjar gälla innan produkten läggs i kundvagnen.

## Steg 1: Lägg till en regel

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rule]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add New Rule]** i det övre högra hörnet.

   Avsnittet _[!UICONTROL Rule Information]_&#x200B;innehåller utökningsbara avsnitt för **[!UICONTROL Conditions]**&#x200B;och **[!UICONTROL Actions]**.

   ![Katalogprisregel - information](./assets/price-rule-catalog-new-ee.png){width="700" zoomable="yes"}

1. Fyll i fälten **[!UICONTROL Rule Name]** och **[!UICONTROL Description]**.

   Dessa fält är endast till för intern referens.

1. Ange **[!UICONTROL Status]** för prisregeln efter behov.

   Som standard är statusen `Inactive`.

   >[!NOTE]
   >
   >När regeln har skapats kan dess status uppdateras genom att statusen ändras till `Active` eller `Inactive` efter behov.

1. Välj **[!UICONTROL Websites]** där regeln ska vara tillgänglig.

1. Markera **[!UICONTROL Customer Groups]** som den här regeln gäller för.

   Om du vill välja flera grupper håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

   >[!NOTE]
   >
   >Alternativen i den här listan beror på vilka kundgrupper som har skapats och hanterats i _Kunder_ > _Kundgrupper_.

1. ![Magento Open Source](../assets/open-source.svg) (endast Magento Open Source) Ange datumen **[!UICONTROL From]** och **[!UICONTROL To]** för att avgöra när prisregeln gäller.

   Du kan ange datum eller använda **[!UICONTROL Calendar]** (![kalenderikonen](../assets/icon-calendar.png)) för att välja datum. Om du lämnar datumen tomma aktiveras regeln när prisregeln sparas.

1. Ange ett nummer för att etablera **[!UICONTROL Priority]** för den här regeln i förhållande till andra regler.

   >[!NOTE]
   >
   >Inställningen _[!UICONTROL Priority]_&#x200B;är viktig när samma katalogprodukt uppfyller villkoren som angetts för mer än en prisregel. Regeln med högsta prioritet (prioriteter från högst upp till lägst är 0,1,2,3...) blir aktiv för produkten.

## Steg 2: Definiera villkoren

De flesta tillgängliga villkor baseras på befintliga attributvärden. Om du vill tillämpa regeln på alla produkter lämnar du villkoren tomma.

>[!NOTE]
>
>Om minst ett villkorligt produktattribut har ett tomt värde används inte katalogprisregeln för produkten.

>[!NOTE]
>
>Om du vill tillämpa ett `Category`-produktattributvillkor på en [bundle](../catalog/product-create-bundle.md)- eller [grouped](../catalog/product-create-grouped.md)-produkt måste alla underordnade produkter tilldelas till samma kategori för att regeln ska gälla korrekt. Annars kan du använda en [kundvagnsprisregel](price-rules-cart-create.md) istället.

1. Bläddra nedåt och utöka ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Conditions]**.

   Det första villkoret visas som standard och lägen:

   `If **ALL** of these conditions are **TRUE**:`

   ![Katalogprisregel - villkorsrad 1](./assets/catalog-condition1.png){width="400"}

   Programsatsen har två feta länkar som du kan klicka på för att visa urvalet av alternativ för den delen av programsatsen. Du kan skapa olika villkor genom att ändra kombinationen av dessa värden.

1. Ändra programsatsen på något av följande sätt:

   - Klicka på **[!UICONTROL ALL]** och välj `ALL` eller `ANY`.
   - Klicka på **[!UICONTROL TRUE]** och välj `TRUE` eller `FALSE`.
   - Låt villkoret vara oförändrat om du vill tillämpa regeln på alla produkter.

   Du kan skapa olika villkor genom att ändra kombinationen av dessa värden. I det här exemplet används standardvillkoret.

1. Klicka på ikonen _Lägg till_ (![Lägg till ikon](../assets/icon-add-green-circle.png)) i början av nästa rad och välj ett alternativ för villkoret, till exempel ett produktattribut eller en kombination.

1. I listan under **[!UICONTROL Product Attribute]** väljer du det attribut som du vill använda som grund för villkoret.

   I detta exempel är villkoret `Attribute Set`.

   ![Katalogprisregel - villkorsrad 2](./assets/catalog-condition2.png){width="400"}

   >[!NOTE]
   >
   >För att ett attribut ska visas i listan måste det konfigureras för användning i kampanjregelvillkor. Mer information finns i [Produktattribut](../catalog/product-attributes.md).

   >[!NOTE]
   >
   >När du använder villkoret `is not one of` med produktattributet _SKU_ och den konfigurerbara produkten måste både den överordnade och den underordnade produktens SKU:er väljas. För att undvika att lista alla underordnade SKU:er i regeln kan du använda villkoret `does not contain` med vanliga SKU-delar för en konfigurerbar produkt och dess underordnade produkter.

   Det markerade villkoret visas i programsatsen, följt av ytterligare två feta länkar. Alternativen varierar beroende på vilket villkorsattribut du väljer. Det står nu:

   `If **ALL** of these conditions are **TRUE**: <br/>Attribute Set **is** …`

1. Klicka på **[!UICONTROL is]** och välj den jämförelseoperator som beskriver villkoret som ska uppfyllas.

   Dessa alternativ kan innehålla ett alternativ för olika jämförelser. I det här exemplet är alternativen `is` och `is not`.

1. Välj eller ange värden för villkoret.

   Beroende på villkoret kan du välja produkter från ett rutnät eller en lista, ange ett numeriskt värde och så vidare.

   ![Katalogprisregel - villkorsrad 2](./assets/catalog-condition3.png){width="400"}

   Det markerade objektet visas i satsen för att slutföra villkoret.

   `If **ALL** of these conditions are **TRUE**: <br/> Attribute Set **is Default**`

1. Om du vill lägga till ytterligare en villkorslinje i satsen klickar du på ikonen _Lägg till_ (![Lägg till ikon](../assets/icon-add-green-circle.png)) och väljer något av följande:

   - `Conditions Combination`
   - `Product Attribute`

   Upprepa processen tills alla önskade villkor är klara.

   Om du vill ta bort en del av villkorssatsen klickar du på ikonen **[!UICONTROL Delete]** (![Ta bort ](../assets/icon-delete-red-circle.png) i slutet av raden.

## Steg 3: Definiera åtgärderna

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png)i avsnittet **[!UICONTROL Actions]** och gör följande:

   ![Katalogprisregel - åtgärder](./assets/price-rule-catalog-actions.png){width="600" zoomable="yes"}

1. Under **[!UICONTROL Pricing Structure Rules]** anger du **[!UICONTROL Apply]** till något av följande:

   - `Apply as percentage of original` - Rabattartikel genom att subtrahera en procentandel av normalpriset. Exempel: Ange 10 i Rabattbelopp för ett slutgiltigt pris som markeras med 10 % nedåt från det normala priset.
   - `Apply as fixed amount` - Rabattartikel genom att subtrahera ett fast belopp från normalpriset. Exempel: Ange 10 i Rabattbelopp för ett slutligt pris som är 10 USD mindre än det vanliga priset.
   - `Adjust final price to this percentage` - Justerar det slutliga priset med en procentandel av det normala priset. Ange t.ex. 25 i Rabattbelopp för ett slutpris som markeras med 75 % nedåt från normalpriset.
   - `Adjust final price to discount value` - Anger slutpriset till ett fast, diskonterat belopp. Exempel: Ange 20 i Rabattbelopp för det slutliga priset 20,00 USD.

   >[!NOTE]
   >
   >_Ordinarie pris_ avser basproduktpriset utan några avancerade priser (special/tier/group) eller kampanjrabatter. _Slutligt pris_ refererar till det rabatterade priset som visas i kundvagnen. <br/>Det **_slutliga_** produktpriset beräknas som det **_lägsta_** relevanta priset, med följande formel: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

   >[!NOTE]
   >
   >**_Fast pris_** anpassningsbara produktalternativ _påverkas_ inte av reglerna för grupppris, pris, specialpris eller katalogpris.

1. Ange **[!UICONTROL Discount Amount]**.

1. Om du vill sluta bearbeta andra regler efter att den här regeln har tillämpats anger du **[!UICONTROL Discard Subsequent Rules]** till `Yes`.

   >[!NOTE]
   >
   >Om du anger det här till `Yes` är det en säkerhetsåtgärd som förhindrar att systemet tillämpar flera rabatter (regler) på samma produkt.

## Steg 4: Lägg till relaterade dynamiska block

{{ee-feature}}

[Dynamiska block](../content-design/dynamic-blocks.md) som är associerade med en katalogprisregel visas i butiken när villkoren uppfylls. Detta är ett valfritt steg.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png)i avsnittet **[!UICONTROL Related Dynamic Blocks]**.

1. Använd [sökfiltren](../getting-started/admin-workspace.md) för att hitta de dynamiska block som du vill associera med regeln.

1. Markera kryssrutan i den första kolumnen om du vill koppla det dynamiska blocket till regeln.

   ![Katalogprisregel - relaterade dynamiska block](./assets/price-rule-catalog-related-dynamic-blocks.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save and Continue Edit]**.

## Steg 5: Schemalägg regeln

{{ee-feature}}

>[!NOTE]
>
>Du måste lägga till en schemalagd uppdatering för att aktivera regeln. Mer information finns i [Schemalagda ändringar](price-rule-catalog-scheduled-changes.md).

1. Klicka **[!UICONTROL Schedule New Update]** högst upp i rutan _Schemalagda ändringar_).

   Om regeln har en befintlig schemalagd uppdatering kan du klicka på **[!UICONTROL View/Edit]** till höger om den listade ändringen.

   Du kan antingen redigera den befintliga uppdateringen eller tilldela katalogprisregeln till en annan kampanj. Alternativet **Redigera befintlig uppdatering** är markerat som standard.

1. Om du vill schemalägga regeln anger du **[!UICONTROL Start Date]** och **[!UICONTROL End Date]** att prisregeln ska vara aktiv.

   Du kan antingen ange datum eller välja datum från _kalendern_ (![kalenderikonen](../assets/icon-calendar.png)).

   ![Katalogprisregel - uppdateringsschema](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]**.

1. I avsnittet _Regelinformation_ anger du **[!UICONTROL Status]** till `active`.

## Steg 6: Spara och testa regeln

1. När du är klar sparar du regeln.

   - ![Magento Open Source](../assets/open-source.svg) (endast Magento Open Source) Klicka på **[!UICONTROL Save and Apply]**.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Klicka på **[!UICONTROL Save]**.

     På sidan Regelinformation visas en uppdaterad tidslinje i Regelns schemalagda ändringar.

     ![Katalogprisregler - schemalagda ändringar](./assets/price-rule-scheduled-changes-updated.png){width="600" zoomable="yes"}

1. Uppdatera egenskaper för en regel:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Klicka på **[!UICONTROL Edit]** för att visa sidan _[!UICONTROL Rule Information]_.

   - ![Magento Open Source](../assets/open-source.svg) (endast Magento Open Source) Klicka på regeln i listan för att visa sidan _[!UICONTROL Rule Information]_.

1. Testa regeln för att kontrollera att den fungerar som den ska.

   Prisreglerna bearbetas automatiskt med andra systemregler varje kväll. När du skapar en prisregel bör du ge den tillräckligt med tid för att komma in i systemet innan du testar regeln för att se till att den fungerar som den ska. I takt med att nya regler läggs till beräknar Commerce om priserna och prioriteterna utifrån detta.

## Film om katalogprisregel

I den här videon får du lära dig mer om hur du skapar katalogprisregler:

>[!VIDEO](https://video.tv.adobe.com/v/343834?quality=12&learn=on)

## Fältbeskrivningar

### [!UICONTROL Rule Information]

| Fält | Beskrivning |
|-----|-----------|
| [!UICONTROL Rule name] | (Obligatoriskt) Namnet på regeln används som intern referens. |
| [!UICONTROL Description] | En beskrivning av regeln ska innehålla regelns syfte och förklara hur den används. |
| [!UICONTROL Websites] | (Obligatoriskt) Identifierar de webbplatser där regeln kan användas. |
| [!UICONTROL Customer Groups] | (Obligatoriskt) Identifierar de kundgrupper som regeln gäller. |
| [!UICONTROL Priority] | Ett tal som anger den här regelns prioritet i förhållande till andra. Prioriteringarna från högsta till lägsta är `0,1,2,3...` |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (endast Magento Open Source) Anger om regeln är aktiv i butiken. Alternativ: `Yes` / `No` |
| [!UICONTROL From] | ![Magento Open Source](../assets/open-source.svg) (endast Magento Open Source) Anger den första dagen som prisregeln gäller. Om den lämnas tom träder prisregeln i kraft när den sparas. |
| [!UICONTROL To] | ![Magento Open Source](../assets/open-source.svg) (endast Magento Open Source) Anger den sista dagen som prisregeln gäller. Om inget anges fortsätter prisregeln oavbrutet. |

{style="table-layout:auto"}

### [!UICONTROL Conditions]

Anger villkoren som måste uppfyllas innan katalogprisregeln verkställs. Om inget anges gäller regeln alla produkter.

### [!UICONTROL Actions]

| Fält | Beskrivning |
|-----|-----------|
| [!UICONTROL Apply] | Bestämmer vilken typ av beräkning som ska tillämpas på inköpet. Alternativ: <br/>**[!UICONTROL Apply as percentage of original]**- Rabattartikel genom att subtrahera en procentandel av normalpriset.<br/>**[!UICONTROL Apply as fixed amount]** - Rabattartikel genom att subtrahera ett fast belopp från normalpriset. <br/>**[!UICONTROL Adjust final price to this percentage]**- Justerar det slutliga priset med en procentandel av det normala priset.<br/>**[!UICONTROL Adjust final price to discount value]** - Anger slutpriset till ett fast, diskonterat belopp. <br/><br/>**_Obs!_**&#x200B;Ordinarie pris avser basproduktpriset utan några avancerade priser (special/tier/group) eller kampanjrabatter. Slutpris avser det rabatterade pris som visas i kundvagnen. <br/>Det&#x200B;**_slutliga _**&#x200B;produktpriset beräknas som det&#x200B;**_lägsta _**&#x200B;relevanta priset, med följande formel: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)` |
| [!UICONTROL Discount Amount] | (Obligatoriskt) Erbjudandet om rabatt. |
| [!UICONTROL Discard Subsequent Rules] | Avgör om ytterligare regler kan tillämpas på det här köpet. Välj `Yes` om du vill förhindra att flera rabatter tillämpas på samma inköp. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Related Dynamic Blocks]

{{ee-feature}}

Identifierar alla [dynamiska block](../content-design/dynamic-blocks.md) som är associerade med regeln.
