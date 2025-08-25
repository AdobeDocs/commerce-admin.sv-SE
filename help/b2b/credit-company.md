---
title: Hantera företagskrediter
description: Lär dig mer om företagskreditrader, ställa in parametrar och hantera förskottsbetalningar.
exl-id: 62ff2a36-053d-4ba0-9969-0f05701afbff
feature: B2B, Companies, Payments
role: Admin
source-git-commit: 1fc1e07f20e2c22ac430f384e9e2b278edae405c
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# Hantera företagskrediter

Med företagskrediter kan B2B-företag göra inköp mot en på förhand godkänd kreditlinje i stället för att kräva omedelbar betalning. När [Betalning på konto](../b2b/enable-basic-features.md#configure-payment-on-account) är aktiverat kan företag köpa upp till sin kreditgräns och visa sin kreditstatus från kontouppsättningen.

![Företagskrediter](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

Med företagskrediter kan du

* **Utöka kreditvillkoren** - Tillåt betrodda företagskunder att handla a conto med fördröjd betalning
* **Ange kreditgränser** - Kontrollera finansiell exponering genom att ange kreditgränser för varje företag
* **Spåra kreditaktivitet** - Övervaka alla kredittransaktioner, betalningar och utestående saldon i realtid
* **Effektivisera B2B-transaktioner** - Förenkla inköpsprocessen för företag med etablerade kreditrelationer
* **Stöd för komplexa arbetsflöden** - Integrera med inköpsorder, offerter och godkännandeprocesser

## Förutsättningar

Innan du skapar företagskrediter måste du se till att:

* B2B-funktioner aktiveras i din Adobe Commerce-installation
* [Betalning på konto](../b2b/enable-basic-features.md#configure-payment-on-account) har konfigurerats och aktiverats
* Företagskonton är korrekt konfigurerade med nödvändig affärsinformation
* Du har administratörsbehörighet för att hantera företagskreditinställningar
* Valutainställningar konfigureras om de används i flera valutor

## Användningsexempel

Företagskrediten är perfekt för:

* **Fasta B2B-relationer** - Långfristiga företagskunder med beprövad betalningshistorik
* **Stora företagskunder** - Företag som gör betydande, regelbundna inköp som kräver utökade betalningsvillkor
* **Säsongsföretag** - Företag med cykliskt kassaflöde som behöver flexibel betalningstiming
* **Företagsinköp** - Organisationer med centraliserade inköp men distribuerad betalningshantering
* **Leverantörskedjor** - Distributörer, återförsäljare och kanalpartners som behöver kreditmöjligheter

## Förstå företagskreditinställningar

Du kan konfigurera följande kreditrelaterade parametrar för varje företagsprofil:

* **Kreditvaluta** - Valuta för alla kredittransaktioner och saldon
* **Kreditgräns**- Högsta belopp som företaget kan vara skyldig när som helst
* **Tillåt att kreditgränsen överskrids** - Om företag kan göra beställningar som överskrider den tillgängliga kreditgränsen
* **Orsak till ändring** - Dokumentationsfält för registrering av ändringar i kreditinställning

Mer information om de här inställningarna och hur du konfigurerar företagsprofilen finns i [Skapa ett företagskonto](account-company-create.md).

>[!NOTE]
>
>Om ett företag har ett utestående saldo visas ett meddelande för butiksadministratören längst upp på försäljningsorder när den visas från administratören. Detta bidrar till att säkerställa att kunderna är medvetna om kreditstatusen vid orderbehandlingen.

## Företagskreditaktivitet

Avsnittet [!UICONTROL Company Credit] i företagsprofilen visar en fullständig historik över alla kredittransaktioner, saldoändringar och betalningsaktiviteter i ett rutnätsformat.

![Företagskreditaktivitet](./assets/company-credit-reimbursements-grid.png){width="700" zoomable="yes"}

I rutnätet visas följande information för varje transaktion:

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Date] | Datum för transaktionen. Håll markören över datumet om du vill visa datum och tid. |
| [!UICONTROL Operation] | Den typ av aktivitet som är associerad med transaktionen. Värden: <br/>**[!UICONTROL Allocated]**- kredit tilldelad företaget.<br/>**[!UICONTROL Updated]** - En ändring tillämpades på ett av följande fält: [!UICONTROL Credit limit] / [!UICONTROL Credit currency] / [!UICONTROL Allow to exceed credit limit] <br/>**[!UICONTROL Purchased]**- en ordning placerades.<br/>**[!UICONTROL Reimbursed]** - Det utestående saldot har återbetalats. <br/>**[!UICONTROL Refunded]**- Ett kreditfakturabelopp har återbetalats.<br/>**[!UICONTROL Reverted]** - Ordern annullerades och beloppet returnerades till kreditsaldot. |
| [!UICONTROL Amount] | Beloppet för transaktionen som är associerad med följande transaktionstyper: `Purchased` / `Reimbursed` / `Refunded` / `Reverted` <br/>För inköpsbelopp visas beloppet i butikens visningsvaluta och i formatet för kreditvalutainställningen, följt av aktuell konverteringsgrad (om tillämpligt). Exempel: <br/>20 000,00 EUR ($22 400,00) <br/>USD/0,8928 EUR |
| [!UICONTROL Outstanding Balance] | Det återbetalda beloppet minus det totala beloppet som ska betalas från alla order som lagts med metoden Betalning på konto. Beloppet kan visas som ett positivt eller negativt värde. <br/>**[!UICONTROL Positive value]**- En förskottsbetalning representeras som ett positivt värde.<br/>**[!UICONTROL Negative value]** - Ett förfallobelopp representeras som ett negativt värde. |
| [!UICONTROL Available Credit] | Summan av _[!UICONTROL Credit Limit]_och_[!UICONTROL Outstanding Balance]_. Om företaget har överskridit kreditgränsen visas beloppet som ett negativt värde. |
| [!UICONTROL Credit Limit] | Det kreditbelopp som har beviljats företaget. |
| [!UICONTROL Updated By] | Namnet på den person som initierade åtgärden. |
| [!UICONTROL Custom Reference Number] | Det anpassade referensnummer som är associerat med transaktionen. |
| [!UICONTROL Comment] | En kompilering av värdena från fältet `Reason for Change`, enligt åtgärdstyp. <br/>**[!UICONTROL Purchased]**- Inkluderar kommentarer från inköpet samt ordernumret och länken till ordern.<br/>**[!UICONTROL Reimbursed]** - Inkluderar kommentarer från den återbetalda transaktionen. |
| [!UICONTROL Action] | Endast för `Reimbursed`-åtgärder. **[!UICONTROL Edit]** - Tillåter att ersättningsbeloppet uppdateras. |

{style="table-layout:auto"}

## Uppdatera kreditinformationen

När kunderna gör betalningar uppdaterar administratörerna kreditinformationen i Admin.

1. Gå till _Kunder > Företag_ på sidofältet **Admin**.

1. Hitta företaget i rutnätet och öppna i _redigeringsläget_.

1. Expandera avsnittet **Företagskrediter**.

1. Ange det nya värdet för **Kreditgräns**.

1. Ändra de andra värdena efter behov.

1. När uppdateringarna är klara klickar du på **[!UICONTROL Save]**.

## Ta emot betalningar

Ett återbetalt saldo är en offlinebetalning som ett företag gör mot saldot på sitt konto. Butiksadministratören anger beloppet manuellt i företagsprofilen med knappen _Återbetalningssaldo_ . När beloppet skickas beräknar systemet om det utestående saldot och tillgängliga företagskrediter och registrerar åtgärden i företagets kredithistorik. Det återbetalda beloppet anges i kreditvalutan enligt inställningarna i konfigurationen.

### Använda en betalning på ett företagskonto

1. Gå till _>_ på sidofältet **[!UICONTROL Customers]** Admin **[!UICONTROL Companies]**.

1. Hitta företagsposten i listan och öppna i **[!UICONTROL Edit]**-läge.

1. Klicka på **Återbetalningssaldo** överst på sidan.

1. Lägg till betalningsinformationen i dialogrutan:

   ![Återbetalningssaldo](./assets/company-reimburse-balance.png){width="500"}

   * Ange **Belopp** för betalningen.

     Beloppet kan anges som ett positivt eller negativt värde.

   * Ange **Eget referensnummer** som referens, om tillämpligt.

     Endast ett anpassat referensnummer kan anges per återbetalning. Om du vill använda betalningen för flera inköpsordrar skapar du en separat återbetalning för varje.

   * Ange en **kommentar** som beskriver ersättningen efter behov.

1. Klicka på **Återbetalning**.

   Systemet uppdaterar saldon och kredithistorik automatiskt för att återspegla ersättningen.

### Redigera en återbetalning

1. Öppna företagsprofilen i läget **[!UICONTROL Edit]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **Företagskrediter**.

1. Hitta ersättningstransaktionen i rutnätet och klicka på **[!UICONTROL Edit]**.

1. Gör nödvändiga ändringar i **Anpassat referensnummer** och **Kommentar**.

   Återbetalningsbeloppet kan inte ändras.

1. Klicka på **[!UICONTROL Save]**.

## Kreditinformation för butiksexponeringar

Företagsadministratörer kan visa sin kreditinformation på kontouppsättningen, inklusive utestående saldo, tillgänglig kredit, kreditgräns och utestående fakturor. När order annulleras återgår beloppen till företagssaldot och visas i fältet Kreditallokeringshistorik.

![Företagskrediter](./assets/company-credit.png){width="700" zoomable="yes"}

## Företagskreditdemo

Läs mer om hur du hanterar företagskrediter i den här filmen:

>[!VIDEO](https://video.tv.adobe.com/v/344445?quality=12&learn=on)

## Säkerhetsaspekter

När man hanterar företagskrediter ska man vidta kraftfulla säkerhetsåtgärder för att skydda känslig finansiell information:

* **Åtkomstkontroll** - Begränsa kredithanteringsbehörigheter till endast behörig personal
* **Granskningsspår** - Bibehåll omfattande loggar över alla kredittransaktioner och ändringar
* **Dataskydd** - Kryptera känslig ekonomisk information både under överföring och i vila
* **Arbetsflöden för godkännande** - Implementera godkännandeprocesser på flera nivåer för betydande kreditjusteringar
* **Regelbundna granskningar** - Utför periodiska granskningar av användaråtkomst och kreditrelationer

## God praxis

* 
   * **Hantering av kreditpolicyer** - När du hanterar företagskrediter måste du skapa tydliga policyer för att ange kreditgränser baserat på kundbetalningshistorik och affärsrelationer. Granska regelbundet utestående saldon och betalningsmönster för att bedöma risker och dokumentera alltid ändringar av kreditinställningar med detaljerade skäl för revision.

Bearbeta betalningar snabbt för att upprätthålla korrekta saldon och se till att kreditvalutainställningarna är anpassade efter respektive företags huvudsakliga verksamhet.

* **Efterlevnad och säkerhet** - Begränsa kredithanteringsbehörigheter till endast auktoriserad personal, implementera arbetsflöden för godkännande för betydande kreditjusteringar och skydda känslig ekonomisk information enligt organisationens säkerhetsprofiler. Regelbunden granskning av användaråtkomst och kreditförhållanden bidrar till att upprätthålla korrekt tillsyn och regelefterlevnad.

>[!MORELIKETHIS]
>
>* [Aktivera B2B-funktioner](enable-basic-features.md) * Konfigurera kontobetalning och andra B2B-funktioner
>* [Skapa ett företagskonto](account-company-create.md) * Konfigurera företagskonton med kreditmöjligheter
>* [Hantera företag](manage-companies.md) * Översikt över funktioner för företagshantering
>* [Företagsroller och behörigheter](account-company-roles-permissions.md) * Konfigurera användaråtkomst för kredithantering
>* [Arbetsflöde för inköpsorder](purchase-order-flow.md) * Förstå hur krediter integreras med inköpsorder
>* [B2B-konfigurationsreferens](../configuration-reference/general/b2b-features.md) - Detaljerade konfigurationsinställningar för B2B-funktioner
