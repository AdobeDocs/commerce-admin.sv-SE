---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Inventory]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Catalog] &gt; [!UICONTROL Inventory] i Commerce Admin.
exl-id: 80113a31-3585-4ee1-95af-31efc09389eb
feature: Configuration, Inventory
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Inventory]

{{config}}

>[!NOTE]
>
>[!DNL Inventory Management] för Adobe Commerce och Magento Open Source ger dig verktygen för att hantera produktinventeringen. Handlare med en enda butik till flera lager, butiker, upphämtningsplatser, avsändare med mera kan använda dessa funktioner för att behålla kvantiteter för försäljning och hantera leveranser för att slutföra beställningar. Mer information om de här funktionerna och hur du kan använda dem för att hantera Stock på flera platser finns i [_[!DNL Inventory Management] Användarhandbok _](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html).

## [!UICONTROL Stock Options]

![Alternativ för Stock](./assets/catalog-inventory-stock-options.png)<!-- zoom -->

<!-- [Stock Options](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/global-options) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Decrease Stock When Order is Placed] | Global | Om värdet är `Yes` minskas kvantiteten i lager när ordern placeras. När _Hantera Stock_ är aktiverat anges reservationer för beställda produkter och kvantiteter. Alternativ: `Yes` / `No` |
| [!UICONTROL Set Items' Status to be in Stock When Order is Cancelled] | Butiksvy | Om värdet är `Yes` returneras objekt till lager när ordern annulleras. Med _Hantera lager_ aktiverat rensas reservationen för annullerade produkter och kvantiteter. Alternativ: `Yes` / `No` |
| [!UICONTROL Display Out of Stock Products] | Global | Om värdet är `Yes` visas produkter som inte finns i lager. Om produktvarningar också är aktiverade kan kunderna registrera sig för att få meddelanden när produkten blir tillgänglig. Alternativ: `Yes` / `No` |
| [!UICONTROL Only X left Threshold] | Webbplats | Fastställer tröskelvärdet för meddelandet `Only x left`. Om värdet till exempel är 3 visas meddelandet när det finns tre eller färre objekt i lager. Meddelandet visas inte om värdet är `0`. |
| [!UICONTROL Display products availability in Stock on Storefront] | Butiksvy | Om värdet är `Yes` visas ett `In Stock`- eller `Out of Stock`-meddelande på produktsidan. Alternativ: `Yes` / `No` |
| [!UICONTROL Enable Inventory Check On Cart Load] | Global | Avgör om en lagerkontroll utförs när en produkt läses in i kundvagnen. Om du inaktiverar den här lagerkontrollen kan du förbättra prestanda för utcheckningssteg, särskilt när det finns många artiklar i kundvagnen. Men om du hoppar över förvalidering kan kunderna se _fel som inte finns i lager_ senare i utcheckningsprocessen. Alternativ: `Yes` / `No` |
| [!UICONTROL Synchronize with Catalog] | Global | När värdet är `Yes` justeras lagerdata efter katalogändringarna (t.ex. produktborttagningar, SKU-ändringar för produkter och ändringar av produkttyper) och säkerställer konsekvens mellan lager och katalog. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Stock Options]

![ProduktStock-alternativ](./assets/catalog-inventory-product-stock-options.png)<!-- zoom -->

<!-- [Product Stock Options](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/global-options) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Manage Stock] | Global | Avgör om du använder fullständig lagerkontroll för att hantera artiklarna i din katalog. Alternativ: <br/>**Ja** - Aktiverar fullständig lagerkontroll för att spåra antalet artiklar som för närvarande finns i lager. <br/>**Nej** - spårar inte antalet artiklar som finns i lager. |
| [!UICONTROL Backorders] | Global | Avgör hur din butik hanterar restorder. En restorder ändrar inte orderns bearbetningsstatus. Pengarna godkänns eller hämtas direkt när beställningen görs, oavsett om produkten finns i lager eller inte. När produkten blir tillgänglig skickas den. Alternativ: <br/>**Inga restorder** - Tar inte emot restorder när produkten inte finns i lager. <br/>**Tillåt kvantitet under 0** - Accepterar restorder när kvantiteten är under noll. <br/>**Tillåt kvantitet under 0 och Meddela kund** - Accepterar restorder när kvantiteten är under noll, men meddelar kunderna att beställningar fortfarande kan göras. |
| [!UICONTROL Use deferred Stock update] | Global | ![Adobe Commerce](../../assets/adobe-logo.svg) (endast Adobe Commerce) Avgör om lageruppdatering ska skjutas upp om restorder tillåts (alternativet _Restorder_ är inställt på något annat än standardvärdet `No backorders`). Det fungerar för en enskild produkt eller en hel webbplats och använder mekanismen _Jobbkö_ för att tillåta att indikatorerna för lagerkvantitet uppdateras asynkront efter att beställningarna har placerats ut. Det här alternativet fungerar även med [asynkron orderplacering](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/high-throughput-order-processing.html#asynchronous-order-placement) i kombination med [Inventory management](../../inventory-management/introduction.md). |
| Högsta tillåtna antal i kundvagn | Global | Fastställer det högsta antalet produkter som kan köpas i en enda order. Som standard är den maximala kvantiteten satt till 10 000. |
| [!UICONTROL Out-of-Stock Threshold] | Global | Bestämmer lagernivån där en produkt anses vara ur lager. Alternativ: <br/>**Positivt belopp** - Med _Restorder_ inaktiverat anger du ett positivt belopp. När Restorder är aktiverade ignoreras det här beloppet. <br/>**Noll** - Om _Restorder_ är aktiverat kan du ange `0` för oändliga restorder. <br/>**Negativt belopp** - Med _Restorder_ aktiverat rekommenderar vi att du anger ett negativt belopp. Beloppet läggs till i den säljbara kvantiteten. Ange till exempel -50 om du vill tillåta order upp till detta belopp. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Global | Bestämmer det minsta beloppet för en artikel som är tillgänglig för inköp enligt kundgrupp. Som standard är den minsta kvantiteten satt till 1. Klicka på **[!UICONTROL Add Minimum Qty]** om du vill ange ett annat värde för en viss kundgrupp. |
| [!UICONTROL Notify for Quantity Below] | Global | Fastställer lagernivån där ett meddelande om att lagret har underskridit tröskelvärdet skickas. |
| [!UICONTROL Enable Qty Increments] | Global | Avgör om artiklar kan säljas i kvantitetssteg. Alternativ: `Yes` / `No` |
| [!UICONTROL Qty Increments] | Global | Fastställer antalet produkter som utgör en kvantitetsökning. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | Global | Avgör om artiklar på kreditnotor automatiskt returneras till lagret. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Bulk Operations]

![Admin - gruppåtgärder](./assets/catalog-inventory-admin-bulk-operations.png)<!-- zoom -->

<!-- [Admin Bulk Operations](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/global-options) -->

>[!NOTE]
>
>Om du vill konfigurera och ge stöd för **asynkrona köhanterare** måste du använda kommandoraden. Detta kan kräva hjälp av utvecklare. Se [Starta meddelandekökonsumenter](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) i _Konfigurationshandboken_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Run asynchronously] | Global | Avgör om du kör gruppåtgärder asynkront för massproduktåtgärder, inklusive [bulk](../../inventory-management/bulk-assignment.md), tilldelar källor, tar bort tilldelning av källor och [överför lager till källan](../../inventory-management/inventory-transfer.md). Den samlar in massåtgärder fram till _[!UICONTROL Asynchronous batch size]_och kör sedan dessa åtgärder. Den här funktionen är inaktiverad som standard. Vi rekommenderar att du granskar prestanda med flera åtgärder innan du aktiverar. Alternativ:<br/>**`Yes`**- Kör alla gruppåtgärder för [!DNL Inventory Management] asynkront. Om du vill aktivera måste du konfigurera en asynkron köhanterare.<br/>**`No`**- Standard. Kör inte gruppåtgärder asynkront. |
| [!UICONTROL Asynchronous batch size] | Global | Ange **[!UICONTROL Run asynchronously]** till `Yes` för att ange ett värde för fältet _[!UICONTROL Asynchronous batch size]_. <br/>Standardgruppstorleken är 100. När gruppprocesser når den här mängden körs de. |

{style="table-layout:auto"}

## [!UICONTROL Inventory Indexer Settings]

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Stock/Source reindex strategy] | Global | Bestämmer vilken strategi som används för omindexering av lager/källa. Alternativ: `Synchronous` / `Asynchronous` (en asynkron köhanterare måste konfigureras för asynkront läge) |

{style="table-layout:auto"}

>[!NOTE]
>
> På grund av beroendena av lageruppdateringar för de orderrelaterade aktiviteterna aktiveras också lagerindexeraren när produkten sparas, oavsett inställningen för `Synchronous` eller `Asynchronous`.


## [!UICONTROL Distance Provider for Distance Based SSA]

![Avståndsproviders för avståndsbaserad SSA](./assets/catalog-inventory-distance-provider.png)<!-- zoom -->

<!-- [Distance Providers for Distance Based SSA](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/distance-priority-algorithm) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Provider] | Global | Avgör vilken provider som ska användas för avståndsprioritetsalgoritmen för Source-markering. Den här funktionen är aktiverad som standard. Alternativ: <br/>**`Google MAP`**- Använder Google-tjänster för att beräkna avståndet och tiden mellan leveransdestinationsadressen och källplatserna (adress och GPS-koordinater). Det här alternativet kräver en Google API-nyckel och kan medföra avgifter via Google.<br/>**`Offline Calculation`** - Beräknar avståndet med hjälp av en inbäddad databas för att fastställa närmaste källa till leveransens måladress. Om du vill använda det här alternativet kan du behöva utvecklarhjälp för att initialt hämta databasplatsinnehållet för alla länder som du levererar till via en kommandorad. |

{style="table-layout:auto"}

## [!UICONTROL Google Distance Provider]

![Google Distance Provider](./assets/catalog-inventory-distance-provider-settings.png)<!-- zoom -->

<!-- [Google Distance Provider](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/distance-priority-algorithm) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Google API key] | Global | Ange Google API-nyckeln för Google MAP-providern. Nyckeln är från [!DNL Google Maps Platform] och ska ha [!DNL Geocoding API] och [!DNL Distance Matrix API] aktiverat. Mer information finns i [Konfigurera algoritmen för avståndsprioritet](../../inventory-management/distance-priority-algorithm.md#configure-the-distance-priority-algorithm) i _Inventory management-handboken_. |
| [!UICONTROL Computation mode] | Global | Anger riktningar och sökvägar för att beräkna avståndet från leveransadressen och alla källor som är tilldelade till lagret. Som standard används körläget vid beräkningar. Alternativ: <br/>**`Driving`**- Standardinställning, begär standardvägbeskrivning med vägnätverket.<br/>**`Walking`** - Begär vägbeskrivningar med hjälp av fotgängarbanor och sidewalks (där sådana finns). <br/>**`Bicycling`**- Begär cykelriktningar med hjälp av cykelsökvägar och önskade gator (för närvarande endast tillgängligt i USA och vissa kanadensiska städer). |
| [!UICONTROL Value] | Global | Anger vad som ska beräknas och returneras för avståndet och tiden för källplatserna till leveransdestinationsadressen. Algoritmen Distance Priority (Avståndsprioritet) rekommenderar källan med kortast möjliga avstånd eller tid till leveransadressen, vilket ger snabbare och eventuellt billigare leverans för att leverera försändelser. Alternativ: <br/>**`Distance`**- Returnerar avståndet mellan punkter i mätvärden (kilometer och meter) eller i kors (engelska mil och fot).<br/>**`Time to Destination`** - Returnerar den tid som krävs för att resa från källplatserna till leveransadressen i timmar och minuter. |

{style="table-layout:auto"}
