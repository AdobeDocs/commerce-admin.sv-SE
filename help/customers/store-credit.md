---
title: Butikskredit
description: Butikskrediter är ett belopp som återställs till ett kundkonto och som kan användas för att betala för inköp eller för kontantåterbetalning.
exl-id: 1fe627dd-5c49-4ff8-85e0-3c987285726d
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Butikskredit

{{ee-feature}}

Butikskrediter är ett belopp som återställs till ett kundkonto. Kunder kan använda sina butikskrediter för att betala inköp, och administratörer kan använda butikskrediter för kontantåterbetalning. Presentkortssaldon kan krediteras kundens konto i stället för att använda presentkortskoden för framtida inköp.

När en order har betalats och fakturerats kan ordern, eller en del av den, återbetalas av [utfärda en kreditnota](../stores-purchase/credit-memo-create.md). En kreditnota skiljer sig från en återbetalning eftersom kreditbeloppet återställs till kundens konto där den kan användas för framtida inköp. Ibland kan en återbetalning ges samtidigt som en kreditnota utfärdas och tillämpas på kundens saldo för butikskrediter. Mängden butikskrediter som är tillgänglig på kundens konto anges i konfigurationen.

>[!NOTE]
>
>The [_Noll delsumma, utcheckning_](../stores-purchase/zero-subtotal-checkout.md) Betalningsmetod måste aktiveras om butikskrediten täcker ordersumman.

## Arbetsflöde för butikskrediter

1. **Kundinloggning** - Kunden loggar in på kontot innan utcheckningsprocessen påbörjas.

1. **Använd butik** - kredit under [!UICONTROL _Granska och betala_] i kassan väljer kunden [!UICONTROL _Använd butikskrediter_] som betalningsalternativ. Det tillgängliga saldot visas inom parentes. Om det tillgängliga saldot är större än totalsumman visas inte längre de andra betalningsmetoderna.

1. **Krediterat** - Beloppet för butikskrediten som tillämpas på ordern visas tillsammans med ordersummorna och dras av från totalsumman.

1. **Kundsaldo justerad** - Kundens tillgängliga saldo justeras när ordern läggs.
