---
title: Inköpsorder för företag
description: Lär dig mer om arbetsflöden för inköpsorder som gör det möjligt för företag att spåra och kontrollera utgifter.
exl-id: 4f93ab4c-6bdf-495e-9183-3a18898b377f
feature: B2B, Purchase Orders
source-git-commit: 4b34645377102e890779059e57c61cf23f71f34c
workflow-type: tm+mt
source-wordcount: '924'
ht-degree: 0%

---

# Inköpsorder för företag

Inköpsorder är ett vanligt sätt för företag att spåra och kontrollera utgifter. [Inköpsorder](../stores-purchase/purchase-order.md) är en av de standardmetoder för offlinebetalning som stöds i Adobe Commerce och Magento Open Source. När B2B av Adobe Commerce installeras och [_Aktivera inköpsorder_](account-company-manage.md#advanced-settings) aktiveras för ett företagskonto och alla order skapas automatiskt som inköpsorder (PO). Företagsanvändare med obligatoriska [behörigheter](account-company-roles-permissions.md) kan skapa, redigera och ta bort PO:er som de skapar och PO:er som skapas av underordnade användare.

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
  >Som standard är `Purchase order has been submitted for approval` meddelandet visas alltid för företagsanvändare, även när inga godkännanderegler har angetts. När ingen godkännandeprocess krävs får företagsanvändare automatiskt ett e-postmeddelande som informerar dem om att ordern har skapats och godkänts.

- Om godkännandereglerna definieras av företagsadministratören, går användarna igenom godkännandeprocessen.
- Information om offlinebetalning anges när inköpsordern skapas.
- Betalningsinformation online anges efter att inköpsordern har godkänts.

>[!NOTE]
>
>Inköpsorder skapar en _ögonblicksbild_ av artikelpriser, rabatter och fraktpriser när ordern skapades. Om priset på en artikel ändras efter att inköpsordern har skapats, används det ursprungliga priset.

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

Med de här reglerna på plats för ett företag kan en företagsanvändare slutföra beställningen direkt när beställningen är mindre än 100 USD. Mer information om definition av godkännanderegel finns i [Godkännanderegler](account-dashboard-approval-rules.md)

### Typer av butiksanvändare

Arbetsflödet för inköpsorder kan också vara annorlunda beroende på vem som gör inköpet.

- En fast anställd kan omfattas av alla godkännanderegler
- En chef kan ha större köpkraft och olika godkännanderegler
- Företagsadministratörer kan kringgå alla godkännanderegler och få sina inköpsorder slutförda automatiskt.

Alla dessa faktorer kan påverka den exakta utcheckningsprocessen.

## [!UICONTROL My Purchase Orders]

När inköpsorder är aktiverade för ett företag **[!UICONTROL My Purchase Orders]** objektet visas i den vänstra panelen för kunder som är inloggade på ett företagsanvändarkonto. Det finns tre flikar med olika inköpsorderlistor och funktioner:

- **[!UICONTROL My Purchase Orders]**: PO:er skapade av kunden.
- **[!UICONTROL Company Purchase Orders]**: PO:er som görs av underordnade användare inom företaget (beror på företagets struktur och roller).
- **[!UICONTROL Requires My Approval]**: (Synligt för utsedda godkännare) PO:er som väntar på kundens godkännande. Räknaren visar hur många order som väntar på godkännande.

![Mina inköpsorder](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

Mer information om vilka inköpsorderfunktioner som stöds för företagsanvändare finns i [Mina inköpsorder](account-dashboard-my-purchase-orders.md).

## Betalningsmetoder offline eller online

Arbetsflödena kan variera beroende på betalningsmetoden. Mer information om betalningsmetoder i Adobe Commerce finns i [Betalningsmetoder](../stores-purchase/payments.md) i _Experience Guide för försäljning och inköp_.

>[!IMPORTANT]
>
>Inköpsorder ska använda en _Kontext_ utcheckningsupplevelsen. _Ej kontext_ Utcheckningar stöds inte eftersom de åsidosätter det normala utcheckningsflödet. I allmänhet _Kontext_ innebär att kunden stannar kvar på din e-handelsplats för att slutföra processen. _Ej kontext_ är när kunden besöker en annan webbplats för att slutföra köpet.

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
