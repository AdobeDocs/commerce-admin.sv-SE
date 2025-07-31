---
title: Hantera en kundvagn
description: Lär dig hur du kan hjälpa en kund med kundvagnen direkt från administratören.
exl-id: beb41dfa-ef87-4065-96fd-0649a5c4c21c
feature: Customer Service, Shopping Cart
source-git-commit: 69cd571b66a81159c2c99e6652907f22142568cb
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 1%

---

# Hantera en kundvagn

{{ee-feature}}

För att kunna starta en assisterad shoppingsession måste kunden vara inloggad på sitt konto från butiken för att göra informationen tillgänglig. Om kunden inte har något konto kan du [skapa ett](../customers/account-create.md).

![Kundvagn i kundkontot](./assets/customer-account-manage-cart-items.png){width="600" zoomable="yes"}

## Åtgärdskontroll

| Alternativ | Beskrivning |
|--- |--- |
| [!UICONTROL Remove] | Tar bort artiklar från den aktuella kundvagnen |
| [!UICONTROL Move to Wish List] | Flyttar objekt till den valda kundens önskelista |

{style="table-layout:auto"}

## Kontrollknappar

| Knapp | Beskrivning |
|--- |--- |
| [!UICONTROL Clear my shopping cart] | Tar bort alla objekt från kundvagnen. |
| [!UICONTROL Update Items and Quantities|]Ange önskad kvantitet i fältet **[!UICONTROL Qty]** och uppdatera antalet artiklar i kundvagnen. |
| [!UICONTROL Add selections to my cart] | Lägger till produkter från alla avsnitt i kundvagnen. |

{style="table-layout:auto"}

## Verifiera att kunden är inloggad

1. Gå till _>_ på sidofältet **[!UICONTROL Customers]** Admin **[!UICONTROL Now Online]**.

   Alla besökare i butiken och inloggade kunder visas i listan.

   ![Kunder som är online](./assets/customers-now-online.png){width="700" zoomable="yes"}

## Erbjud assisterad butik

1. Gå till _>_ på sidofältet **[!UICONTROL Customers]** Admin **[!UICONTROL All Customers]**.

1. Öppna kundposten i redigeringsläge i listan.

   >[!TIP]
   >
   >Använd kontrollen [Filter](../getting-started/admin-grid-controls.md) om du vill hitta kundposten snabbt.

   I kundprofilen under _[!UICONTROL Personal Information]_visar datumet och tiden_[!UICONTROL Last Logged In]_ att kunden är online.

   ![Kundprofil för en onlinekund](./assets/customer-account-manage-cart.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Manage Shopping Cart]** i det övre knappfältet om du vill gå till det assisterade shoppingläget.

   ![Assisterat shoppingläge](./assets/customer-manage-shopping-cart.png){width="600" zoomable="yes"}

## Lägg produkter i kundvagn efter attribut

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Products]**.

1. Hitta en produkt med hjälp av något av filtren längst upp i varje kolumn.

1. Klicka på **[!UICONTROL Search]**.

1. Använd någon av följande stegserier beroende på produkttyp:

### Lägg till en enkel produkt

1. Klicka på den produkt du vill beställa.

   Den här åtgärden markerar posten och ställer in **[!UICONTROL Quantity]** till standardvärdet `1`.

1. Uppdatera beställd kvantitet om det behövs.

1. Klicka på **[!UICONTROL Add selections to my cart]** till vänster ovanför stödrastret.

   ![Lägg till produkt i kundvagn](./assets/customer-account-manage-cart-order-products.png){width="600" zoomable="yes"}

   Radartikeln läggs till i kundvagnen högst upp på sidan.

   ![Kundvagnen har uppdaterats](./assets/customer-account-manage-cart-update-cart.png){width="600" zoomable="yes"}

### Lägg till en produkt med konfiguration

Det finns tre typer av produkter som måste konfigureras innan de läggs till i kundvagnen: `Bundle Product`, `Configurable Product` och `Grouped Product`.

1. Klicka på **[!UICONTROL Configure]** bredvid produktnamnet i rutnätet.

   ![Konfigurera produkten](./assets/customer-account-manage-cart-order-configurable-product.png){width="600" zoomable="yes"}

1. I dialogrutan _Associerade produkter_ väljer du varje produktalternativ för att beskriva artikeln som ska beställas, anger **[!UICONTROL Quantity]** och klickar på **[!UICONTROL OK]**.

   Produkten markeras med en bock och den beställda kvantiteten visas i rutnätet.

1. Klicka på **[!UICONTROL Add selections to my cart]** om du vill lägga produkten i kundvagnen.

   ![Konfigurerbar produkt i kundvagnen](./assets/customer-account-manage-cart-order-configurable-product-cart.png){width="600" zoomable="yes"}

1. Uppdatera produktalternativ i kundvagnen om det behövs:

   - Klicka på **[!UICONTROL Configure]**.

   - Uppdatera alternativen och klicka sedan på **[!UICONTROL OK]**.

## Lägg till produkt efter SKU

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Add to Shopping Cart by SKU]**.

1. Lägg till produkter individuellt av **[!UICONTROL SKU]** eller lägg till produkter genom att överföra en CSV-fil.

### Lägg till artiklar individuellt efter SKU

1. Ange **[!UICONTROL SKU]** och **[!UICONTROL Qty]** för objektet som ska beställas.

1. Om du vill beställa en annan produkt klickar du på **[!UICONTROL Add another]**.

   ![Lägg till produkter efter SKU](./assets/customer-account-manage-cart-order-product-by-sku.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Add selections to my cart]**.

1. Om objektet är en konfigurerbar produkt väljer du produktalternativen när du uppmanas till det och klickar sedan på **[!UICONTROL Add to Shopping Cart]**.

### Lägga till produkter genom att överföra en CSV-fil

1. Förbered en [csv-fil](../systems/data-csv.md) med objekten som ska läggas till i kundvagnen.

   Filen får bara innehålla två kolumner, med `sku` och `qty` i sidhuvudet.

1. Överför den förberedda filen:

   - Klicka på **[!UICONTROL Choose File]**.

   - Välj den fil som ska överföras från din katalog.

## Överför en artikel

Du kan överföra artiklar till kundvagnen från kundens önskelista och nyligen visade, jämförda eller beställda artiklar. Antalet objekt i varje avsnitt visas inom parentes efter avsnittshuvudet.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i något av följande avsnitt:

   - [!UICONTROL Wish List]
   - [!UICONTROL Products in the Comparison List]
   - [!UICONTROL Recently Compared Products]
   - [!UICONTROL Recently Viewed Products]
   - [!UICONTROL Last Ordered Items]

1. I rutnätet väljer du varje produkt som ska beställas och anger **[!UICONTROL Quantity]**.

1. Om du vill ange alternativ för en konfigurerbar produkt klickar du på **[!UICONTROL Configure]** och anger produktalternativen efter behov.

1. Klicka på **[!UICONTROL Add selections to my cart]**.

1. Använd en eller flera kupongkoder om sådana finns:

   - Ange en giltig kupongkod för **[!UICONTROL Apply Coupon Code]**.

   - Klicka på pilen _Använd_ ( ![pilikon](../assets/icon-apply-arrow.png) ).

1. Justera beställd kvantitet efter behov:

   - Ange rätt belopp i kolumnen **[!UICONTROL Qty]** för den produkt som ska justeras.

   - Klicka på **[!UICONTROL Update Items and Quantities]**.

## Skapa ordern

1. Klicka på **[!UICONTROL Create Order]**.

   På sidan _[!UICONTROL Create New Order]_visas artiklarna i kundvagnen följt av leverans- och betalningsinformation.

1. Fyll i information om frakt och betalning.

1. Klicka på **[!UICONTROL Submit Order]**.

Mer information finns i [Skapa en beställning](customer-account-create-order.md).

## Ta bort alla objekt från en kundvagn

Att ta bort alla artiklar från kundvagnen i assisterat shoppingläge är användbart om kunden vill börja om, har lagt till felaktiga artiklar eller behöver rensa kundvagnen innan en ny order läggs. Detta säkerställer att kundvagnen endast innehåller de produkter kunden faktiskt vill köpa.

1. Gå till _>_ på sidofältet **[!UICONTROL Customers]** Admin **[!UICONTROL All Customers]**.

1. Öppna kundposten i redigeringsläge i listan.

1. Klicka på **[!UICONTROL Manage Shopping Cart]** i det övre knappfältet.

1. Klicka på **[!UICONTROL Clear my shopping cart]**.

   ![Rensa min kundvagn](./assets/customer-manage-shopping-cart-clear.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL OK]** när du uppmanas att bekräfta åtgärden.
