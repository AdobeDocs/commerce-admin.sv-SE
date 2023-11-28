---
title: Skapa en kundvagnsprisregel
description: Lär dig hur du skapar en kundvagnsprisregel baserat på kundvagn- eller produktattribut.
exl-id: 7260e7c3-3b1e-43e5-9c09-c40538e37378
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: bf52884cb0eccd4d9c7326a95f8600a3ed950918
workflow-type: tm+mt
source-wordcount: '2885'
ht-degree: 0%

---

# Skapa en kundvagnsprisregel

Utför följande steg för att lägga till en regel, beskriva villkoren och definiera åtgärderna. Fyll också i etiketterna och testa regeln. Prisregelvillkoren kan baseras på kundvagn eller [produktattribut](../catalog/product-attributes.md) eller [Real-Time CDP-målgrupper](#use-real-time-cdp-audiences-to-set-a-condition), men inte på [anpassningsbara alternativ](../catalog/settings-advanced-custom-options.md).

## Steg 1: Lägg till en regel

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

1. Klicka **[!UICONTROL Add New Rule]** och gör följande:

   - Under _[!UICONTROL Rule Information]_, slutför **[!UICONTROL Rule Name]**och **[!UICONTROL Description]**.

   - Om du inte vill att regeln ska börja gälla omedelbart anger du **[!UICONTROL Active]** till `No`.

   ![Kundprisregel - regelinformation](./assets/price-rule-cart-new.png){width="600" zoomable="yes"}

1. För att fastställa [omfång](../getting-started/websites-stores-views.md#scope-settings) för regeln gör du så här:

   - Välj **[!UICONTROL Websites]** där kampanjen ska vara tillgänglig.

   - Välj **[!UICONTROL Customer Groups]** som kampanjen gäller.

     Om du vill att kampanjen endast ska vara tillgänglig för registrerade kunder **_inte_** välj `NOT LOGGED IN` alternativ.

1. Ange vilken regel som ska användas med eller utan en [kupong](price-rules-cart-coupon.md) enligt följande:

   - Om du vill att kundvagnsregeln ska användas utan att använda en kupongkod anger du **[!UICONTROL Coupon]** till `No Coupon` och gå vidare till steg 5.

   - Om du vill associera en kupong med en prisregel anger du **[!UICONTROL Coupon]** till `Specific Coupon` och gör följande:

      - Ange fritext **[!UICONTROL Coupon Code]** som kunden måste ange för att få rabatten.

      - Ange en gräns för hur många gånger kupongen får användas genom att fylla i följande alternativ:

     | Alternativ | Beskrivning |
     |------|-----------|
     | `Uses per Coupon` | Avgör hur många gånger kupongkoden kan användas. Om det inte finns någon gräns lämnar du fältet tomt. |
     | `Uses per Customer` | Avgör hur många gånger kundprisregeln kan användas av samma registrerade kund som tillhör någon av de valda kundgrupperna. Inställningen gäller inte gästkunder som är medlemmar i kundgruppen NOT LOGGED IN, eller kunder som handlar utan att logga in på sina konton. Om det inte finns någon gräns lämnar du fältet tomt. |

     {style="table-layout:auto"}

     Mer information finns på [Kupongkoder](price-rules-cart-coupon.md).

     ![Kundprisregel - kuponginställningar](./assets/price-rule-cart-coupon-settings-ee.png){width="600" zoomable="yes"}

   - ![Magento Open Source](../assets/open-source.svg) (Endast Magento Open Source) Använd _Kalender_ (![Kalenderikon](../assets/icon-calendar.png)) för att välja **[!UICONTROL From]** och **[!UICONTROL To]** datumintervall för erbjudandet.

1. Ange ett tal för att definiera **[!UICONTROL Priority]** av den här prisregeln i relation till åtgärdsinställningarna för andra prisregler som är aktiva samtidigt.

   >[!NOTE]
   >
   >Inställningen Prioritet är viktig när två kundvagnsregler/kupongkoder gäller för samma produkt samtidigt. Regeln med inställningen Högsta prioritet (`1` som högst) kontrollerar kundvagnens åtgärd. Se _Ignorera efterföljande prisregler_ i _Definiera funktionsmakron_ steg.

   >[!NOTE]
   >
   >Kundprisregler som har samma prioritet ger ingen kombinerad rabatt. Varje regel tillämpas på matchande produkter separat, en i taget.

1. Tillämpa regeln på publicerad [RSS-flöden](social-rss.md#rss-feeds), ange **Offentlig i RSS-feed** till `Yes`.

1. Klicka på **[!UICONTROL Save and Continue Edit]**.

   - ![Magento Open Source](../assets/open-source.svg) (Endast Magento Open Source) När regeln har sparats visas namnet på kundvagnsprisregeln överst på sidan.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) När regeln har sparats anges namnet på kundprisregeln och [Schemalagda ändringar](price-rule-cart-scheduled-changes.md) visas högst upp på sidan.

     ![Kundprisregel - schemalagda ändringar](./assets/price-rule-cart-scheduled-changes.png){width="600" zoomable="yes"}

## Steg 2: Beskriv villkoren

I det här steget beskrivs de villkor som måste uppfyllas för att en beställning ska vara berättigad till en befordran. Regeln aktiveras när villkorsuppsättningen uppfylls.

Om du använder målgrupper från Real-Time CDP går du vidare till [det här avsnittet](#use-real-time-cdp-audiences-to-set-a-condition).

>[!NOTE]
>
>Kundprisregeln tillämpas på **_var_** produkten i kundvagnen när villkoren i _[!UICONTROL Conditions]_-fliken är uppfylld. Lägg till villkor i_[!UICONTROL Actions]_ för att begränsa antalet produkter som påverkas av kundvagnsprisregeln.

>[!NOTE]
>
>Om minst ett villkorsproduktattribut har ett tomt värde, tillämpas inte kundvagnsprisregeln på produkten.

1. I den vänstra panelen väljer du **[!UICONTROL Conditions]**.

   ![Kundprisregel - villkor](./assets/conditions.png){width="600" zoomable="yes"}

   Det första villkoret visas som standard och lägen:

   `If **ALL** of these conditions are **TRUE**:`

   Programsatsen har två feta länkar som du kan klicka på för att visa urvalet av alternativ för den delen av programsatsen. Du kan skapa olika villkor genom att ändra kombinationen av dessa värden. Gör något av följande:

   - Klicka **[!UICONTROL ALL]** och markera `ALL` eller `ANY`.
   - Klicka **[!UICONTROL TRUE]** och markera `TRUE` eller `FALSE`.
   - Låt villkoret vara oförändrat om du vill tillämpa regeln på alla produkter.

1. Klicka _Lägg till_ (![Ikonen Lägg till](../assets/icon-add-green-circle.png)) i början av nästa rad och välj ett alternativ för villkoret, till exempel kundvagnsattribut, delval av produkt eller kombination.

   I det här exemplet slutför du nästa del av villkoret enligt följande:

   - När du uppmanas till **[!UICONTROL Choose the condition to add]**, välja `Products Subselection`.

     ![Villkor för kundprisregel - delurval av produkter](./assets/price-rule-cart-condition-products-subselection.png){width="600" zoomable="yes"}

   - Klicka på i villkorssatsen **[!UICONTROL total quantity]** och markera `total quantity` eller `total amount`.

   >[!IMPORTANT]
   >
   >[!UICONTROL Total amount] är en radsumma, så moms tas inte med i `total amount` för [!UICONTROL Products Subselection] kundprisregelvillkor. Använd [!UICONTROL Subtotal (Incl. Tax)] villkor för att inkludera skatter.

   - Klicka på i villkorssatsen **[!UICONTROL is]** och markera `greater than`.

1. När nästa del av villkoret visas klickar du på elementen i satsen så att du kan se var varje länk med variabelvärden finns.

1. Klicka på länken &quot;mer&quot; (..) och ange `100`.

   Detta villkor kräver att den totala kvantiteten i vagnen är `101` eller större.

   ![Villkor för kundprisregel - totalkvantitetsvärde](./assets/condition-products-subselection3.png){width="600" zoomable="yes"}

1. Klicka **Lägg till** (![Ikonen Lägg till](../assets/icon-add-green-circle.png)) i början av nästa rad och sedan lägga till ett villkor som baseras på **Kategori**.

   ![Villkor för kundprisregel - produktattributkategori](./assets/condition-products-subselection4.png){width="600" zoomable="yes"}

1. Klicka på i nästa del av villkoret _mer_ (**...**) för att visa inmatningsfältet och sedan öppna _Väljare_ (![Ikonen Lista](../assets/icon-list-chooser.png)) för att visa kategoriträdet.

1. Markera kryssrutan för den kategori som du vill använda som villkor för prisregeln och klicka på ![Ikonen Lägg till](../assets/icon-checkmark-green-circle.png) om du vill acceptera kategorivalen.

   Villkoret kan baseras på vilken kategori som helst som är underordnad butikens [rotkategori](../catalog/category-root.md).

   ![Villkor för kundprisregel - produktkategori](./assets/subselection-category.png){width="600" zoomable="yes"}

1. Om du vill lägga till fler villkor klickar du på _Lägg till_ (![Ikonen Lägg till](../assets/icon-add-green-circle.png)) och definiera ett annat villkor.

   Du kan upprepa processen så många gånger som behövs för att beskriva villkoren som måste uppfyllas för prisregeln. Här är några exempel:

   **Exempel 1:** Regional prisregel

   Om du vill skapa en regional prisregel använder du något av följande kundvagnsattribut:

   - `Shipping Postcode`
   - `Shipping Region`
   - `Shipping State/Province`
   - `Shipping Country`

   **Exempel 2:** Summor i kundvagn

   Om du vill basera villkoret på kundvagnssummor använder du något av följande kundvagnsattribut:

   - `Subtotal`
   - `Total Items Quantity`
   - `Total Weight`

>[!NOTE]
>
>Om det gäller flera parallella kampanjer _Delsumma_ villkoret används i _bas_ kundvagnsdelsumma **_före_** eventuella rabatter.

>[!IMPORTANT]
>
>**Endast för inköpsorder**: När en kundprisregel har ställts in baserat på en eller flera specifika betalningsmetoder, tillämpas rabatten på totalsumman när en inköpsorder skapas. När inköpsordern har skapats tillämpas rabatten på summan om betalningsmetoden ändras till en som inte omfattas av kundvagnsprisregeln.

### Lägg till ett produktattribut i kundprisreglerna

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**och öppna produktattributet.

1. I den vänstra panelen väljer du **[!UICONTROL Storefront Properties]**.

1. Ange **[!UICONTROL Use for Promo Rule Conditions]** till `Yes`.

1. Klicka på **[!UICONTROL Save Attribute]**.

1. Gå till **[!UICONTROL Marketing]** > **[!UICONTROL Cart Price Rules]** och öppna den kundvagnsprisregel som krävs.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Condition]** avsnitt och markera **[!UICONTROL Product attribute combination]**.

1. Ange något av följande värden för det här villkoret:

   - Klicka **[!UICONTROL FOUND]** och markera `FOUND` eller `NOT FOUND`.

   - Klicka **[!UICONTROL ALL]** och markera `ALL` eller `ANY`.

1. Klicka på _Lägg till_ (![Ikonen Lägg till](../assets/icon-add-green-circle.png)) och väljer **[!UICONTROL Product Attribute]** som du ställer in för kampanjregelvillkor.

1. Klicka på **[!UICONTROL Save]**.

>[!NOTE]
>
>När du använder `is not one of` villkor med _SKU_ produktattribut och konfigurerbar produkt, både den överordnade och den underordnade produktens SKU måste väljas. Om du vill undvika att lista alla underordnade SKU:er i regeln kan du använda kommandot `does not contain` villkor med vanliga SKU-delar av en konfigurerbar produkt och dess underordnade produkter.

### Använd Real-Time CDP målgrupper för att ställa in ett villkor

Du kan ange ett villkor för en kundprisregel som baseras på en Real-Time CDP [publik](../customers/audience-activation.md).

1. Expandera **[!UICONTROL Conditions]** klickar du på plusikonen (+) och väljer **[!UICONTROL Real-Time CDP Audience]** från listan.

   ![Välj Real-Time CDP målgruppsvillkor](./assets/rtcdp-conditions.png){width="300"}

1. Välj _Mer_ (**...**) klickar du på **[!UICONTROL Open Chooser]** och se alla tillgängliga Real-Time CDP-målgrupper.

   ![Visa Real-Time CDP-målgrupper](./assets/rtcdp-conditions-chooser.png){width="600" zoomable="yes"}

1. Välj den Real-Time CDP-målgrupp som du vill använda för kundvagnsprisregeln.

   | Alternativ | Beskrivning |
   |------|-----------|
   | `ID` | En intern identifierare för målgruppen som används i administratören |
   | `Real-Time CDP Audience ID` | Unik identifierare för målgruppen när den skapades i Experience Platform |
   | `Name` | Målgruppens namn, till exempel `Orders over $50` |
   | `Description` | Beskrivning av målgruppen, till exempel `People who placed an order over $50 in the last month.`. |
   | `Source` | Anger varifrån målgruppen kommer, till exempel `Experience Platform`. |
   | `Website` | Anger vilken webbplats du har länkat till datastream som innehåller målgrupperna. Du skapar den här länken när du ansluter din Commerce-instans till Experience Platform via [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html) tillägg. |

   {style="table-layout:auto"}

I nästa steg definierar du vilken åtgärd som ska utföras när villkoret är uppfyllt.

## Steg 3: Definiera åtgärderna

Kundvagnsprisregelåtgärderna beskriver hur priserna uppdateras när villkoren uppfylls.

1. Bläddra nedåt till **[!UICONTROL Actions]**, och expandera ![Expansionsväljare](../assets/icon-display-expand.png) avsnittet.

   ![Kundprisregel - åtgärder ](./assets/price-rule-cart-actions.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Apply]** till något av följande rabattalternativ:

   | Alternativ | Beskrivning |
   |------|-----------|
   | `Percent of product price discount` | Rabattartikel genom att subtrahera en procentandel från det ursprungliga priset. Rabatten gäller för varje kvalificerande artikel i kundvagnen. Till exempel: Retur `10` in [!UICONTROL Discount Amount] till ett uppdaterat pris som är 10 % lägre än det ursprungliga priset. |
   | `Fixed amount discount` | Rabattartikel genom att subtrahera ett fast belopp från det ursprungliga priset för varje kvalificerande artikel i kundvagnen. Till exempel: Retur `10` in [!UICONTROL Discount Amount] till ett uppdaterat pris som är 10 USD mindre än det ursprungliga priset. |
   | Fast beloppsrabatt för hela kundvagn | Rabatterar hela kundvagnen genom att subtrahera ett fast belopp från kundvagnssumman. Exempel: Ange 10 i [!UICONTROL Discount Amount] för att ta bort $10 från kundvagnen. Som standard gäller rabatten endast delsumman i kundvagnen. Använd _[!UICONTROL Apply to Shipping Amount]_alternativ. |
   | `Buy X get Y free` | Definierar en kvantitet som kunden måste köpa för att få en kvantitet kostnadsfritt. (Med [!UICONTROL Discount Amount] är Y.) |

   {style="table-layout:auto"}

   - Ange **[!UICONTROL Discount Amount]** som ett tal, utan symboler. Beroende på vilket rabattalternativ du väljer kan talet 10 t.ex. visa en procentsats, ett fast belopp eller en kvantitet artiklar.

   - För _Köp X och få Y utan kostnad_ rabatt, ange kvantiteten i **[!UICONTROL Discount Qty Step (Buy X)]** fält som kunden måste köpa för att få rabatten.

   - I **[!UICONTROL Maximum Qty Discount is Applied To]** anger du den maximala kvantitet av samma produkt som berättigar till rabatt i samma inköp.

   - Ange **[!UICONTROL Apply to Shipping Amount]** (![Växla alternativ](../assets/toggle-yes.png)) enligt följande:

     | Alternativ | Beskrivning |
     |------|-----------|
     | `Yes` | Tillämpar rabattbeloppet separat på delsumman och leveransbeloppen. |
     | `No` | Tillämpar endast rabattbeloppet på delsumman. |

     {style="table-layout:auto"}

   - Om du vill avbryta bearbetningen av andra regler när den här regeln har tillämpats anger du **[!UICONTROL Discard Subsequent Rules]** (![Växla alternativ](../assets/toggle-yes.png)) till `Yes`. Den här inställningen förhindrar att flera rabatter används för samma produkt.

     | Alternativ | Beskrivning |
     |------|-----------|
     | `Yes` | Förhindrar att andra prissättningsregler som kan gälla för en produkt tillämpas. När flera prisregler gäller för samma produkt är det bara prisregeln med den högsta prioriteten (i en regel) [!UICONTROL Priority] fält) tillämpas på den kvalificerande produkten. Detta förhindrar att flera prissättningsregler kan staplas och ger oönskade ytterligare rabatter. |
     | `No` | Tillåter att flera prisregler gäller för samma produkt. Detta kan resultera i en hög rabattnivå och ge flera rabatter på ert listpris. |

     {style="table-layout:auto"}

     >[!IMPORTANT]
     >
     >Om du vill ignorera efterföljande regler måste de definierade prioriteter som anges i fältet Prioritet i varje regel användas i en prisregel, och flera regler ska inte ha samma prioritet definierad. Se **[!UICONTROL Priority]** i _Lägg till en ny regel_ steg.

1. Definiera **_exakt_** produkter i kundvagnen som påverkas av kundvagnsprisregeln lägger du till **_ytterligare_** villkor som krävs för åtgärden.

   Ange om fri frakt ska användas på order som uppfyller villkoren **[!UICONTROL Free Shipping]** till något av följande:

   | Alternativ | Beskrivning |
   |------|-----------|
   | `No` | Fraktfritt är inte tillgängligt. |
   | `For matching items only` | Fri frakt är endast tillgängligt för artiklar som matchar villkoren i regeln. |
   | `For shipment with matching items` | Fri frakt är tillgängligt för alla leveranser som innehåller matchande artiklar. The [Fri frakt](../stores-purchase/shipping-free.md) leveransmetoden måste vara aktiverad för att det här alternativet ska kunna användas. |

   {style="table-layout:auto"}

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) För **[!UICONTROL Add Rewards Points]**, ange det fasta antal poäng kunden får **_en_** per order när kundvagnsprisregeln tillämpas.

   Om belöningspunkter inte är aktiverade lämnar du det här fältet tomt.

1. När du är klar klickar du på **[!UICONTROL Save and Continue Edit]**.

## Steg 4: Fyll i etiketterna

Etiketten visas i orderns summeringsavsnitt för att identifiera rabatten. Etikettexten omges av parenteser, efter ordet `Discount`. Du kan ange en standardetikett för alla butiksvyer eller ange olika etiketter för varje vy.

![Butiksvagn - rabattetiketter](./assets/order-totals-section-discount-special.png){width="600"}

1. Bläddra nedåt till **[!UICONTROL Labels]**, och expandera ![Expansionsväljare](../assets/icon-display-expand.png)avsnittet.

1. Ange texten som du vill använda som **[!UICONTROL Default Rule Label for All Store Views]**.

   ![Kundprisregel - standardetikett](./assets/label-default.png){width="600" zoomable="yes"}

1. Om din butik innehåller flera vyer, eller flera webbplatser med flera vyer, anger du lämplig etikettext för varje.

   Om t.ex. varje butiksvy är på ett annat språk anger du översättningen av etiketten för varje vy.

   ![Lagra specifika etiketter](./assets/label-store-specific.png){width="600" zoomable="yes"}

## Steg 5: Lägg till relaterade dynamiska block (valfritt)

{{ee-feature}}

[Dynamiska block](../content-design/dynamic-blocks.md) som är kopplade till regeln visas i butiken när villkoren är uppfyllda.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Related Dynamic Blocks]** -avsnitt.

1. Använd [sökfilter](../getting-started/admin-workspace.md) för att hitta de block som du vill associera med regeln.

1. Markera kryssrutan i den första kolumnen för att koppla blocket till regeln.

   Mer information finns på [Dynamiska block i prisregler](../content-design/dynamic-blocks-price-rules.md).

## Steg 6: Spara och testa regeln

1. När du är klar klickar du på **[!UICONTROL Save Rule]**.

1. Testa regeln för att kontrollera att den fungerar som den ska.

   Prisreglerna bearbetas automatiskt med andra systemregler varje kväll. När du skapar en prisregel måste du ge den tillräckligt med tid för att komma in i systemet. Testa även regeln för att se till att den fungerar som den ska. I takt med att nya regler läggs till beräknar Commerce om priserna och prioriteringarna i enlighet därmed.

## Demo av kundprisregel

I den här videon får du lära dig att skapa kundvagnsprisregler:

>[!VIDEO](https://video.tv.adobe.com/v/343835?quality=12)

## Fältbeskrivningar

### [!UICONTROL Rule Information]

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Rule Name] | (Obligatoriskt) Namnet på regeln används som intern referens. |
| [!UICONTROL Description] | En beskrivning av regeln ska innehålla regelns syfte och förklara hur den används. |
| [!UICONTROL Active] | (Obligatoriskt) Anger om regeln är aktiv i butiken. Alternativ: `Yes` / `No` |
| [!UICONTROL Websites] | (Obligatoriskt) Identifierar de webbplatser där regeln kan användas. |
| [!UICONTROL Customer Groups] | (Obligatoriskt) Identifierar de kundgrupper som regeln gäller. |
| [!UICONTROL Coupon] | (Obligatoriskt) Anger om en kupong är associerad med regeln. Alternativ: <br/>**[!UICONTROL No Coupon]**- Ingen kupong är associerad med regeln.<br/>**[!UICONTROL Specific Coupon]** - En viss kupong är kopplad till regeln. <br/>**[!UICONTROL Coupon Code]**- Ange den kupongkod som kunden måste ange för att utnyttja erbjudandet.<br/>**[!UICONTROL Use Auto Generation]** - Markera kryssrutan för att automatiskt generera flera kupongkoder som kan användas i kampanjen. <br/>**[!UICONTROL Auto]**- Visar _[!UICONTROL Manage Coupon Codes]_för att definiera formatet för de kupongkoder som ska genereras. |
| [!UICONTROL Uses per Coupon] | Avgör hur många gånger kupongkoden kan användas. Om det inte finns någon gräns lämnar du fältet tomt. |
| [!UICONTROL Uses per Customer] | Avgör hur många gånger kundprisregeln kan användas av samma registrerade kund som tillhör en vald kundgrupp. Gäller inte gästkunder som är medlemmar i kundgruppen NOT LOGGED IN, eller kunder som handlar utan att logga in på sina konton. Utan begränsning lämnas tomt. |
| [!UICONTROL Priority] | Ett tal som anger den här regelns prioritet i förhållande till andra. Den högsta prioriteten är tal `1`. |
| [!UICONTROL Public in RSS Feed] | Avgör om kampanjen ingår i butikens offentliga RSS-feed. Alternativ:  `Yes` / `No` |
| [!UICONTROL From] | ![Magento Open Source](../assets/open-source.svg) (Endast Magento Open Source) Det första datum som kupongen kan användas. |
| [!UICONTROL To] | ![Magento Open Source](../assets/open-source.svg) (Endast Magento Open Source) Det sista datum som kupongen kan användas. |

{style="table-layout:auto"}

### [!UICONTROL Conditions]

Anger villkoren som måste uppfyllas innan kundprisregeln aktiveras. Om inget anges gäller regeln alla produkter i vagnen. Villkoren kan baseras på vilken kombination av kundvagn och produktattribut som helst. Men [anpassningsbara alternativ](../catalog/settings-advanced-custom-options.md) kan inte refereras i kundprisregelvillkor.

### [!UICONTROL Actions]

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Apply] | Bestämmer vilken typ av beräkning som ska tillämpas på inköpet. Alternativ: <br/>**[!UICONTROL Percent of product price discount]**- Rabattartikel genom att subtrahera en procentandel från det ursprungliga priset. Till exempel: Retur `10` in _[!UICONTROL Discount Amount]_till ett uppdaterat pris som är 10 % lägre än det ursprungliga priset.<br/>**[!UICONTROL Fixed amount discount]**- Rabattartikel genom att subtrahera ett fast belopp från det ursprungliga priset för varje kvalificerande artikel i kundvagnen. Till exempel: Retur `10` in_[!UICONTROL Discount Amount]_ till ett uppdaterat pris som är 10 USD mindre än det ursprungliga priset. <br/>**[!UICONTROL Fixed amount discount for whole cart]**- Rabatterar hela kundvagnen genom att subtrahera ett fast belopp från kundvagnens delsumma. Till exempel: Retur `10` in _[!UICONTROL Discount Amount]_för att subtrahera $10 från vagnsdelsumman. Som standard gäller rabatten endast delsumman i kundvagnen. Om du vill tillämpa rabatten på delsumman och skicka separat, se_Tillämpa på leveransbelopp _.<br/>**[!UICONTROL Buy X Get Y Free (discount amount is Y)]**- Definierar en kvantitet som kunden måste köpa för att få en kvantitet utan kostnad. (Med_[!UICONTROL Discount Amount]_ är Y.) |
| [!UICONTROL Discount Amount] | (Obligatoriskt) Erbjudandet om rabatt. |
| [!UICONTROL Maximum Qty Discount is Applied To] | Anger det maximala antalet produkter som rabatten kan tillämpas på i samma inköp. |
| [!UICONTROL Discount Qty Step (Buy X)] | Anger antalet produkter som representeras av `X` i en `Buy X Get Y Free` kampanj. |
| [!UICONTROL Apply to Shipping Amount] | Avgör om rabatten tillämpas separat på delsumman och leveransbeloppen. I annat fall tillämpas den bara på delsumman. Alternativ: `Yes` / `No` |
| [!UICONTROL Discard Subsequent Rules] | Avgör om regler med lägre prioritet (1 är den högsta prioriteten) kan tillämpas på produkten när den här kundprisregeln är en matchning. Aktivera det här alternativet om du vill förhindra att flera rabatter används för samma produkt. Alternativ: `Yes` / `No` |
| [!UICONTROL Free Shipping] | Avgör om fri frakt ingår i kampanjen och, i så fall, för vilka artiklar. Alternativ: <br/>**[!UICONTROL No]**- Fri frakt är inte tillgängligt för den aktuella regeln.<br/>**[!UICONTROL For matching items only]** - Fri frakt endast för specifika artiklar i vagnen som matchar regeln. <br/>**[!UICONTROL For shipment with matching items]**- Fraktfritt för alla artiklar i vagnen. The [Fri frakt](../stores-purchase/shipping-free.md) leveransmetoden måste vara aktiverad för att det här alternativet ska kunna användas. |
| [!UICONTROL Add Reward Points] | ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Anger antalet [belöningspoäng](rewards-loyalty.md) som intjänas av kunden när prisregeln tillämpas. |

{style="table-layout:auto"}

### [!UICONTROL Labels]

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Default Rule Label for All Store Views] | En standardetikett som identifierar rabatten och kan användas för alla butiksvyer. |
| [!UICONTROL Store View Specific Labels] | Om tillämpligt, anger en annan etikett för att identifiera rabatten för varje butiksvy. |

{style="table-layout:auto"}

### [!UICONTROL Related Dynamic Blocks]

{{ee-feature}}

Identifierar alla [dynamiska block](../content-design/dynamic-blocks.md) som är kopplade till regeln.
