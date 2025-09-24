---
title: Beställningsarbetsflöde och -bearbetning
description: Lär dig mer om orderarbetsflöde, vilken status som gäller i varje steg och hur du flyttar beställningar genom den här processen.
exl-id: 5bc152c8-2adf-4faf-af84-ca65d260c22a
feature: Orders, Customer Service
source-git-commit: 82f040fa34cf96af6f1e9752f8d9f1ddeab9f84c
workflow-type: tm+mt
source-wordcount: '1822'
ht-degree: 0%

---

# Beställningsarbetsflöde och -bearbetning

När en kund gör en beställning skapas en försäljningsorder som en tillfällig post för transaktionen. I orderrutnätet har försäljningsorder till att börja med statusen &quot;Väntande&quot; och kan annulleras när som helst tills betalningen har bearbetats. När betalningen har bekräftats kan ordern faktureras och skickas.

**Steg 1: Beställ** - Utcheckningsprocessen börjar när kunden klickar på **[!UICONTROL Go to Checkout]** på kundvagnssidan eller [beställer ](reorders-allow.md) direkt från kundkontot.

**Steg 2: Väntande beställning** - Den initiala försäljningsorderstatusen är `Pending`. I det här läget har betalningen inte bearbetats och ordern kan fortfarande redigeras eller annulleras. Det här läget inträffar när betalningsmetoden har konfigurerats för auktoriseringsläge.

**Steg 3: Ta emot betalning** - Orderstatusen ändras till `Processing` när betalningen tas emot eller auktoriseras. Beroende på betalningsmetoden kan du få ett meddelande när transaktionen har auktoriserats eller bearbetats. Det här läget inträffar automatiskt när betalningsmetoden är konfigurerad för inspelning eller försäljning av återgivning.

**Steg 4: Fakturaorder** - En order faktureras vanligtvis efter att betalningen har tagits emot. Betalningsmetoden avgör vilka faktureringsalternativ som behövs för ordern. När fakturan har skapats och skickats skickas en kopia till kunden. Om betalningsmetoden har konfigurerats med betalningsåtgärden `capture` eller `intent sale`, genereras en faktura automatiskt när betalningen auktoriseras och hämtas.

>[!NOTE]
>
>Fakturor skapas inte automatiskt för order som har placerats med `Gift Card`, `Store Credit`, `Reward Points` eller andra offlinebetalningsmetoder.

**Steg 5: Bokför en enskild leverans** - Orderstatusen ändras till `Complete` när leveransinformationen är klar, leveransen bokförs och leveransen ställs in. Leveranskravet uppfylls med en utskriven följesedel och leveransetikett eller så har _Notify Ready for Pickup_ valts (leveransmetod i butik). Kunden får ett meddelande och paketet levereras. Om spårningsnummer används kan leveransen spåras från kundens konto.

>[!NOTE]
>
>Mer information om orderstatus och konfigurationsalternativ för betalningsmetoder finns i [Orderstatus](order-status.md) och [Betalningar](payments.md).

## Visa en order

1. Gå till _>_ > **[!UICONTROL Sales]** på sidofältet _[!UICONTROL Operations]_&#x200B;Admin **[!UICONTROL Orders]**.

1. Hitta ordningen i rutnätet.

1. Klicka på _[!UICONTROL Action]_&#x200B;i kolumnen **[!UICONTROL View]**.

1. Kontrollera orderstatus:

   - En `Pending`-order kan ändras, spärras, annulleras eller faktureras och skickas.

   - En `Processing`-beställning kan inte längre redigeras eller annulleras, men fakturerings- och leveransadressen kan redigeras.

   - En `Completed`-order kan ordnas om.

Kundens mejl kan redigeras när som helst i orderarbetsflödet genom att kunden redigeras. E-postmeddelandet kan inte redigeras om ordern har placerats av en gäst.

Den vänstra panelen för en öppen order ger åtkomst till olika typer av information som är relaterad till ordningen.

![Visa ordning](./assets/order-view.png){width="700" zoomable="yes"}

## Bearbeta en order

När en kund gör en beställning skapas en försäljningsorder som en tillfällig post för transaktionen. Försäljningsordern har statusen `Pending` tills betalningen tas emot. När du är i `Pending`-status kan beställningar redigeras eller annulleras tills den tidpunkt då betalningen tas emot och en faktura genereras. Ett enkelt sätt att tänka på det är att beställningar blir fakturor och fakturor blir leveranser. Orderstödrastret visar alla order, oavsett var de finns i arbetsflödet. Mer information om hur du kan hjälpa kunder med en beställning finns i [Uppdatera en beställning](order-update.md).

![Beställningar](./assets/orders-grid.png){width="700" zoomable="yes"}

Om du vill öppna en `Pending`-ordning klickar du på **[!UICONTROL Edit]** i det övre högra hörnet.

>[!NOTE]
>
>Beställningar kan bara redigeras när statusen är `Pending`. Knappen Redigera är inte synlig för order med en annan status eller för order som baseras på ett [förhandlat citattecken](../b2b/quotes.md).

![Redigera försäljningsorder](./assets/order-pending.png){width="600" zoomable="yes"}

Granska följande avsnitt i försäljningsordern med fältbeskrivningarna som referens.

### Beskrivningar av ordervyn

| Tabb | Beskrivning |
|--- |--- |
| [!UICONTROL Information] | Visa detaljerad information om order och konto, inklusive fakturerings- och leveransadresser, betalnings- och leveransmetoder, artikelorder, summor och noteringar. |
| [!UICONTROL Invoices] | Visar varje faktura som är associerad med ordern. |
| [!UICONTROL Credit Memos] | Visar varje kreditnota som är kopplad till ordern. |
| [!UICONTROL Shipments] | Visar varje försändelsepost som är associerad med ordern. |
| [!UICONTROL Comments History] | Visar alla anteckningar som är relaterade till ordern. |

{style="table-layout:auto"}

>[!NOTE]
>
>En administratörsanvändare måste ha **[!UICONTROL Sales / Archive]** [behörigheter](../systems/permissions-user-roles.md) för att rollomfånget ska kunna visa ordningsflikarna _Fakturor_, _Kreditnotor_ och _Leveranser_.

### Knappfält

| Knapp | Beskrivning |
|--- |--- |
| **[!UICONTROL Back]** | Återgår till sidan Beställningar utan att spara ändringarna. |
| **[!UICONTROL Cancel]** | Avbryter försäljningsordern. |
| **[!UICONTROL Send Email]** | Skickar ett e-postmeddelande om ordern till kunden. |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Ändrar försäljningsorderns status till `On Hold`. Välj **[!UICONTROL Unhold]** om du vill släppa spärren på försäljningsordern. |
| **[!UICONTROL Invoice]** | Skapar en faktura från försäljningsordern genom att konvertera ordern till en faktura. |
| **[!UICONTROL Ship]** | Skapar en försändelsepost för ordern. |
| **[!UICONTROL Notify Order is Ready for Pickup]** | Visas bara när en beställning placeras som en leverans i butik. Meddelar kunden att beställningen är klar för hämtning. |
| **[!UICONTROL Reorder]** | Skapar en försäljningsorder baserat på den aktuella ordern. |
| **[!UICONTROL Edit]** | Öppnar en väntande ordning i redigeringsläge. Knappen Redigera visas inte för order med statusen `Processing` eller order som baseras på förhandlade offerter. |

{style="table-layout:auto"}

### Avbryt en beställning

Du kan [avbryta](order-update.md) order som ännu inte har fakturerats. En [kreditnota](credit-memos.md) måste utfärdas om en kund vill annullera en order efter att den har fakturerats (betalningen har hämtats).

Om en order är `Pending` eller `Processing` och betalningen inte har hämtats eller inte har hämtats helt kan du [annullera ordern](#void-an-order) i stället för att avbryta den.

Om du vill återställa en avbruten ordning klickar du på knappen **[!UICONTROL Reorder]** och skapar en ny ordning med statusen `Pending`.

>[!NOTE]
>
>Om du avbryter en order skapas också en void, men om du annullerar en order utlöses ingen annullering.

### Annullera en order

Endast försäljningsorder som inte har fakturerats, har statusen `Processing` och [betalningsintegrationsinställningen `Authorize`](../configuration-reference/sales/payment-methods.md#payment-actions) kan [annulleras](order-update.md#void-a-processing-order). När du har annullerat en order kan du avbryta den.

### [!UICONTROL Order and Account Information]

![Beställnings- och kontoinformation](./assets/order-account-information.png){width="600" zoomable="yes"}

#### Beställningsinformation

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Order Number] | Ordernumret visas högst upp i försäljningsordern, följt av en anteckning som anger om bekräftelsemeddelandet skickades. |
| [!UICONTROL Order Date] | Datum och tid då ordern lades. |
| [!UICONTROL Purchased From] | Anger webbplatsen, butiken och butiksvyn där beställningen placerades. |
| [!UICONTROL Placed from IP] | Anger IP-adressen till datorn som beställningen gjordes från. |
| [!UICONTROL Order Placed from Quote] | ![Adobe Commerce B2B](../assets/b2b.svg) (tillgänglig med Adobe Commerce B2B) Anger [offerten](../b2b/quotes.md) som ordern genererades från, om tillämpligt. Offertnamnet är länkat till offerten. |

{style="table-layout:auto"}

#### Kontoinformation

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Customer Name] | Namnet på den kund eller köpare som lade ordern. Kundnamnet är kopplat till kundprofilen. |
| [!UICONTROL Email] | Kundens eller köparens e-postadress. E-postadressen är länkad för att öppna ett nytt e-postmeddelande. |
| [!UICONTROL Customer Group] | Namnet på den kundgrupp eller delade katalog som kunden är tilldelad till. |
| [!UICONTROL Company Name] | ![Adobe Commerce B2B](../assets/b2b.svg) (Tillgängligt med Adobe Commerce B2B) Namnet på det företag som köparen är associerad med och för vars räkning ordern placeras. Företagsnamnet är länkat till [företagsprofilen](../b2b/account-companies.md). |

{style="table-layout:auto"}

### [!UICONTROL Address Information]

![Adressinformation](./assets/order-address-information.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Billing Address] | Namnet på den kund eller köpare som lade ordern, följt av faktureringsadressen, telefonnumret och [moms](vat.md), om tillämpligt. Telefonnumret är kopplat till automatisk uppringning på en mobil enhet. |
| [!UICONTROL Shipping Address] | Namnet på den person som ordern ska skickas till, följt av leveransadress och telefonnummer. Telefonnumret är kopplat till automatisk uppringning på en mobil enhet. |

{style="table-layout:auto"}

### [!UICONTROL Payment & Shipping Method]

![Betalnings- och leveranssätt](./assets/order-payment-and-shipping-method-braintree.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Payment Information] | Betalningsmetoden som ska användas för ordern och inköpsordernumret, om tillämpligt, följt av valutan som användes för att placera ordern. Om ordern debiteras företagskrediter med hjälp av [Betalning på konto](../b2b/enable-basic-features.md#configure-payment-on-account), anges beloppet som debiteras kontot. |
| [!UICONTROL Shipping & Handling Information] | Den leveransmetod som ska användas och eventuella hanteringsavgifter som är tillämpliga. |

{style="table-layout:auto"}

### Egna orderattribut

[!BADGE Endast SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce as a Cloud Service-projekt (SaaS-infrastruktur som hanteras av Adobe)."}

Med anpassade orderattribut kan du koppla ytterligare information som är specifik för dina affärsbehov till ordern.

![Anpassade ordningsattribut](./assets/custom-order-attributes.png){width="600" zoomable="yes"}

I avsnittet **[!UICONTROL Custom Order Attributes]** visas alla anpassade ordningsattribut och deras aktuella värden.

Om du vill skapa ett nytt attribut för anpassad ordning anger du **[!UICONTROL Attribute Code]** och **[!UICONTROL Value]**

Klicka på **[!UICONTROL Add Attribute]** om du vill skapa ytterligare anpassade ordningsattribut.

Klicka på ikonen **[!UICONTROL X]** om du vill ta bort ett anpassat ordningsattribut.

>[!NOTE]
>
>Anpassade orderattribut kan bara redigeras när ordningen har statusen `Pending`. För order i andra statusar kan du visa attributvärdena, men inte ändra dem.

### Granska beställda artiklar

![Beställda objekt](./assets/order-items-ordered-tee.png){width="600" zoomable="yes"}

Gör följande i avsnittet **[!UICONTROL Order Total]**:

1. Ange en **[!UICONTROL Comment]** som ska inkluderas i ordern.

1. Markera kryssrutan **[!UICONTROL Notify Customer by Email]** om du vill skicka kommentaren till kunden via e-post.

1. Om du vill att kommentaren ska visas på kundkontot markerar du kryssrutan **[!UICONTROL Visible on Storefront]**.

   ![Summa beställningar](./assets/order-total.png){width="600" zoomable="yes"}

1. Om du är redo att fakturera ordern klickar du på **[!UICONTROL Invoice]** och följer instruktionerna för att [skapa en faktura](invoices.md#create-an-invoice).

#### [!UICONTROL Items Ordered]

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Product] | Produktnamn, SKU och alternativ om tillämpligt. |
| [!UICONTROL Item Status] | Anger artikelns status. Värde: `Ordered` |
| [!UICONTROL Original Price] | Artikelns ursprungliga katalogpris före rabatt. |
| [!UICONTROL Price] | Artikelns inköpspris. Detta värde återspeglar eventuell rabatt som tillämpas på objektet från den delade katalogen, om tillämpligt. |
| [!UICONTROL Qty] | Beställd kvantitet. |
| [!UICONTROL Subtotal] | Delsumman är inköpspriset multiplicerat med kvantiteten. |
| [!UICONTROL Tax Amount] | Momsbeloppet som gäller för artikeln som ett decimalvärde. |
| [!UICONTROL Tax Percent] | Procentandel av moms som används för den här artikeln som en procentandel. |
| [!UICONTROL Discount Amount] | Rabatten som gäller för den här artikeln. Rabattvärdet är noll om ordern baseras på en offert. |
| [!UICONTROL Row Total] | Radartikelsumman, inklusive tillämpliga skatter som ska betalas på produktnivå, minus rabatter. |

{style="table-layout:auto"}

#### [!UICONTROL Notes for this Order]

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Status] | Visar försäljningsorderns status. |
| [!UICONTROL Comment] | En textruta som används för att ange en kommentar till kunden som medföljer ordern. <br/>**[!UICONTROL Notify Customer by Email]**- Markera kryssrutan om du vill skicka kommentaren till kunden som ett separat e-postmeddelande.<br/>**[!UICONTROL Visible on Storefront]** - Markera kryssrutan om du vill att kommentaren ska vara synlig från kundens konto. <br/>**[!UICONTROL Update]**- Lägger till kommentaren och skickar ett e-postmeddelande, om tillämpligt. |

{style="table-layout:auto"}

#### [!UICONTROL Order Totals]

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Shipping & Handling] | Det belopp som debiteras för frakt- och expeditionsavgifter. |
| [!UICONTROL Tax] | Momsbelopp som tillämpas på ordern, om tillämpligt. |
| [!UICONTROL Grand Total] | Ordersumman. |
| [!UICONTROL Total Paid] | Det totala belopp som betalats till ordern, om tillämpligt. |
| [!UICONTROL Total Refunded] | Det totala belopp som återbetalas från ordern, om tillämpligt. |
| [!UICONTROL Total Due] | Det totala beloppet som förfaller. |
| [!UICONTROL Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Det tillgängliga kreditbeloppet för butik som tillämpas på ordern, om tillämpligt. |
| [!UICONTROL Catalog Total Price] | ![Adobe Commerce B2B](../assets/b2b.svg) (Tillgängligt med Adobe Commerce B2B) Det totala priset på objekten i offerten utan moms, enligt priset i den delade katalogen eller standardkatalogen som används som bas för offerten. Om visningsvalutan för butiken skiljer sig från basvalutan visas värdet i båda valutorna, med butiken inom hakparenteser. |
| [!UICONTROL Negotiated Discount] | ![Adobe Commerce B2B](../assets/b2b.svg) (tillgänglig med Adobe Commerce B2B) Den rabatt som är resultatet av en offert som förhandlats fram mellan köpare och säljare. Om visningsvalutan för butiken skiljer sig från basvalutan visas värdet i båda valutorna, med butiken inom hakparenteser. |
| [!UICONTROL Subtotal] | ![Adobe Commerce B2B](../assets/b2b.svg) (tillgänglig med Adobe Commerce B2B) Katalogens totalpris minus den förhandlade rabatten. |

{style="table-layout:auto"}

## Film om orderbehandling

Titta på den här videon och läs mer om orderhantering och status:

>[!VIDEO](https://video.tv.adobe.com/v/343935/?quality=12&learn=on)
