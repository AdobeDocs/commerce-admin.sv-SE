---
title: Introduktion till butiker och inköpsupplevelser
description: Lär dig mer om de funktioner som används för att skapa och hantera onlinebutiker och hur kunderna upplever sina inköp.
exl-id: 7ced9cbc-49b4-48f7-aae2-fcb48fdb888f
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Introduktion till butiker och inköpsupplevelser

Adobe Commerce och Magento Open Source har en omfattande uppsättning funktioner för att skapa och hantera onlinebutiker och kundupplevelsen. I din Commerce-instans kan du hantera butikshierarkin för webbplatser, butiker och vyer. Du kan också konfigurera de skatter och valutakurser som krävs för att köra butiker för flera språkområden, inklusive momsklasser för produkter och kundgrupper.

## Butiksstruktur

En instans av Adobe Commerce eller Magento Open Source kan ha stöd för flera webbplatser, butiker eller butiksvyer som använder olika attribut och innehåll. Ett vanligt scenario är att konfigurera butiker med olika alternativ i olika domäner. Du kanske vill ha en uppsättning kategorier och produkter på en domän och en annan uppsättning kategorier och produkter på en annan domän på ett annat språk. Marknadsförare kan konfigurera webbplatser, butiker och butiksvyer i Admin.

När [hierarki](stores.md) är definierat kan du använda konfigurationsinställningar enligt [omfång](../getting-started/websites-stores-views.md#scope-settings) så att varje webbplats-, butiks- och butiksvy tillhandahåller den produktkatalog och butiksupplevelse du vill ha.

## Inköpsplats

Adobe Commerce och Magento Open Source minskar antalet beställningsfel genom att automatiskt verifiera SKU:n och tillgängligheten för alla artiklar innan en beställning skickas. Du kan konfigurera [kundvagn](cart.md) och [utcheckningsalternativ](checkout-process.md) för att ge en optimal köpupplevelse, från transaktionen till leveransen. Kunder som är inloggade på sina konton kan slutföra utcheckningen snabbt eftersom mycket av informationen redan finns på deras konton. The _Utcheckning_ leder sidan kunden genom varje steg i processen för att slutföra ordertransaktionen. Om du aktiverar [Omedelbart köp](checkout-instant-purchase.md), kan kunderna snabba upp utcheckningsprocessen med hjälp av information som sparas på deras konto.

>[!TIP]
>
>![Adobe Commerce B2B](../assets/b2b.svg) Med installation och aktivering av Adobe Commerce B2B kan du konfigurera _Snabbordning_ för kunder som är kopplade till ett företagskonto. Den här funktionen minskar orderprocessen till flera klick när de vet namnet eller SKU:n på de produkter de vill beställa. Du kan också konfigurera stöd för Negotiable Quotes för dina företagskonton. Mer information om B2B-funktionerna finns i [Användarhandbok för Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

## Shoppingassistans

Kunderna behöver ibland hjälp med att slutföra ett köp. Vissa kunder gillar att handla online, men föredrar att beställa via telefon. Du kan erbjuda omedelbar hjälp till både gäster och kunder som har registrerat sig för ett konto hos din butik.

- [Hantera kundvagnen](shopping-assisted-cart-manage.md)
- [Skapa order](customer-account-create-order.md) för registrerade kunder
- [Uppdatera order](order-update.md)

![Kundvagn](./assets/storefront-cart-price-group-discount.png){width="700" zoomable="yes"}

Läs mer om säljarassisterad butik i den här videon:

>[!VIDEO](https://video.tv.adobe.com/v/343662/?quality=12)

## Beställningshantering och -åtgärder

I Admin har handlarna åtkomst till information i varje steg i orderarbetsflödet och processorder:

- The [Beställningar](orders.md) sidan ger säljarna en lättillgänglig lista över alla aktuella order och innehåller verktyg för att redigera och bearbeta befintliga order samt skapa order för kundernas räkning.

- The [Fakturor](invoices.md) sidlistor En faktura baseras på en tillfällig försäljningsorder och ger en permanent post för ordern.

- The [Leveranser](shipments.md) På sidan visas försändelseposten för varje faktura som är klar att skickas.

- The [Kreditnotor](credit-memos.md) kan handlare bearbeta och hantera en kreditnota, vilket är ett dokument som visar det belopp som kunden är skyldig. Beloppet kan tillämpas på ett köp eller återbetalas till kunden.

- ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) [Returnerar](returns.md) På sidan visas de artiklar som returneras (RMA) och som används för att ange nya returbegäranden.

- The [Transaktioner](transactions.md) På sidan visas alla betalningsaktiviteter som har utförts mellan din butik och ett betalningssystem. Där finns även mer detaljerad information.

## Leverans

Studier visar att butiker erbjuder kunderna flera [leveransmetoder](delivery.md) har högre konverteringsgrader än butiker som använder en enda metod. Admin innehåller olika verktyg som handlare kan använda för att ställa in flera leveransmetoder och [rederier](carriers.md)och skriva ut [fraktsedlar](shipping-labels.md).
