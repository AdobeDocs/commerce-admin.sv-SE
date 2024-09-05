---
title: Inköpsorder för företag
description: Lär dig mer om arbetsflöden för inköpsorder som gör det möjligt för företag att spåra och kontrollera utgifter.
exl-id: 4f93ab4c-6bdf-495e-9183-3a18898b377f
feature: B2B, Purchase Orders
source-git-commit: c1d8bdcd2d09567846ef6819660c57468062ab01
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# Inköpsorder för företag

Inköpsorder är ett vanligt sätt för företag att spåra och kontrollera utgifter. [Inköpsorder](../stores-purchase/purchase-order.md) är en av de standardmetoder för offlinebetalning som stöds i Adobe Commerce och Magento Open Source. När B2B av Adobe Commerce har installerats och [_Aktivera inköpsorder_](account-company-manage.md#advanced-settings) har aktiverats för ett företagskonto skapas alla order automatiskt som inköpsorder (PO). Företagsanvändare med de nödvändiga [behörigheterna](account-company-roles-permissions.md) kan skapa, redigera och ta bort PO:er som de skapar och PO:er som skapas av underordnade användare.

## Inköpsorderflöde

Beroende på deras roll och beställning kan företagsanvändare omfattas av flera godkännanderegler. Och beroende på om du använder online- eller offlinebetalningsmetoder är flödet något annorlunda. Företagsadministratörer kan skapa order automatiskt utan att följa godkännandereglerna. Eftersom det är en säkerhetsrisk att lagra betalningsinformation online under godkännandeprocessen läggs dessa uppgifter till efter godkännandet och sedan konverteras inköpsordern till en verklig order.

![Inköpsorderflöde](./assets/purchase-order-flow.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Det går inte att beställa om en eller flera produkter i inköpsordern är inaktiverade eller inte finns i lager.

Arbetsflödet för inköpsorder för ett företag kan variera på några sätt:

- Om inga godkännanderegler har angetts kan inköpsorder placeras och ordern slutföras direkt.

  >[!NOTE]
  >
  >Som standard visas ett `Purchase order has been submitted for approval`-meddelande alltid för företagsanvändare, även när inga godkännanderegler har angetts. När ingen godkännandeprocess krävs får företagsanvändare automatiskt ett e-postmeddelande som informerar dem om att ordern har skapats och godkänts.

- Om godkännandereglerna definieras av företagsadministratören, går användarna igenom godkännandeprocessen.
- Om flera godkännanderegler gäller för en inköpsorder måste alla unika godkännare godkänna den.
- Information om offlinebetalning anges när inköpsordern skapas.
- Betalningsinformation online anges efter att inköpsordern har godkänts.

>[!NOTE]
>
>Inköpsorder skapar en _ögonblicksbild_ av artikelpriser, rabatter och leveranspriser när ordern skapades. Om priset på en artikel ändras efter att inköpsordern har skapats, används det ursprungliga priset.

### Exempel på grundläggande arbetsflöde

Företagen använder inköpsorder för att styra vad medarbetarna kan köpa för företagets räkning och lägger ofta upp regler för godkännande för att följa företagets riktlinjer. Beroende på godkännandereglerna kan flera personer behöva godkänna ordern.

1. Användaren skapar en inköpsorder för 25 000 dollar för varor.
1. Deras chef måste godkänna.
1. Eftersom beställningen är större än 10 000 USD måste även leverantören godkänna.
1. Beroende på betalningsmetod konverteras inköpsordern automatiskt till en order efter att den godkänts, eller så återgår användaren till att ange betalningsinformation.

### Godkännanderegler

Godkännanderegler används för att kontrollera utgifter baserat på företagets riktlinjer. Exempel på godkännanderegler är:

- Alla order på över 100 USD måste godkännas av din chef.
- Alla order på över 1 000 USD måste godkännas av din chef och företagsadministratören.
- Alla order med fler än 30 unika SKU:er måste godkännas av företagsadministratören.

Med de här reglerna på plats för ett företag kan en företagsanvändare slutföra beställningen direkt när beställningen är mindre än 100 USD. Mer information om definition av godkännanderegel finns i [Godkännanderegler](account-dashboard-approval-rules.md).

### Typer av butiksanvändare

Arbetsflödet för inköpsorder kan också vara annorlunda beroende på vem som gör inköpet.

- En fast anställd kan omfattas av alla godkännanderegler
- En chef kan ha större köpkraft och olika godkännanderegler
- Företagsadministratörer kan kringgå alla godkännanderegler och få sina inköpsorder slutförda automatiskt.

Alla dessa faktorer kan påverka den exakta utcheckningsprocessen.

## [!UICONTROL My Purchase Orders]

När inköpsorder är aktiverade för ett företag visas objektet **[!UICONTROL My Purchase Orders]** på den vänstra panelen för kunder som är inloggade på ett företagsanvändarkonto. Det finns tre flikar med olika inköpsorderlistor och funktioner:

- **[!UICONTROL My Purchase Orders]**: PO:er skapade av kunden.
- **[!UICONTROL Company Purchase Orders]**: PO:er som har gjorts av underordnade användare inom företaget (beroende på företagsstruktur och roller).
- **[!UICONTROL Requires My Approval]**: (Synligt för utsedda godkännare) PO:er som väntar på kundens godkännande. Räknaren visar hur många order som väntar på godkännande.

![Mina inköpsorder](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

Mer information om vilka inköpsorderfunktioner som stöds för företagsanvändare i butiken finns i [Mina inköpsorder](account-dashboard-my-purchase-orders.md).

## Betalningsmetoder offline eller online

Arbetsflödena kan variera beroende på betalningsmetoden. Mer information om betalningsmetoder i Adobe Commerce finns i [Betalningsmetoder](../stores-purchase/payments.md) i _Handboken för försäljning och köp_.

>[!IMPORTANT]
>
>Inköpsorder ska använda en _kontextutcheckning_. _Utcheckningar utan kontext_ stöds inte eftersom de åsidosätter det normala utcheckningsflödet. I allmänhet innebär _Kontext_ att kunden stannar kvar på din e-handelsplats för att slutföra processen. _Kontexten är slut_ när kunden besöker en annan webbplats för att slutföra köpet.

### Onlinebetalningar

Av säkerhetsskäl vill inte onlinebutiker samla in butikens kreditkortsuppgifter i väntan på att godkännandeprocessen ska slutföras. Om du väljer ett onlinebetalningsalternativ återgår därför inköpsorderskaparen till butiken efter godkännandet, anger betalningsinformationen och slutför ordern. Exempel på onlinebetalningar är:

- Kredit-/betalkort
- PayPal
- Braintree

>[!IMPORTANT]
>
>Det går inte att använda presentkort, butikskrediter eller belöningspoäng med onlinebetalningsmetoder för inköpsorder. Om du aktiverar de här funktionerna med onlinebetalningar kan det leda till oväntat beteende. Vi rekommenderar att du inaktiverar presentkort, butikskrediter och belöningspoäng när online-betalningar är aktiverade för inköpsorder.

### Offlinebetalningar

Eftersom offlinebetalningsmetoder, t.ex. en betalningsorder, hanteras utanför webbplatsen är de säkrare. Inköpsorder med offlinebetalningar kan bearbetas automatiskt efter varje godkännandeprocess.

Exempel på offlinebetalningar är:

- Check-/penningbeställning
- Betalning à conto
- Kontant vid leverans
- Banköverföringar
- Butikskrediter
