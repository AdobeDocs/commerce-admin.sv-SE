---
title: Hantera företagskrediter
description: Lär dig mer om företagskreditrader, ställa in parametrar och hantera förskottsbetalningar.
exl-id: 62ff2a36-053d-4ba0-9969-0f05701afbff
feature: B2B, Companies, Payments
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---

# Hantera företagskrediter

If [Betalning à conto](../getting-started/../b2b/enable-basic-features.md#configure-payment-on-account) är aktiverat i konfigurationen, kan företag göra köp på sitt konto upp till kreditgränsen som beviljas företaget. När det här alternativet är aktiverat kan kunderna kontrollera status för sina företagskrediter från sin kontokontrollpanel.

![Företagskrediter](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

Du kan ange följande kreditrelaterade parametrar för varje företagsprofil:

- Kreditvaluta
- Kreditgräns
- Tillåt att kreditgränsen överskrids
- Orsak till ändring

Om företaget har ett utestående saldo visas ett meddelande till butiksadministratören högst upp i försäljningsordern när den visas från administratören. Mer information finns på [Skapa ett företagskonto](account-company-create.md).

## Företagskreditaktivitet

The [!UICONTROL Company Credit] i företagsprofilen visas en sammanfattning av kundens kreditaktivitet, med ett rutnät för företagets kredithistorik.

![Företagskreditaktivitet](./assets/company-credit-reimbursements-grid.png){width="700" zoomable="yes"}

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Date] | Datum för transaktionen. Håll markören över datumet om du vill visa datum och tid. |
| [!UICONTROL Operation] | Den typ av aktivitet som är associerad med transaktionen. Värden: <br/>**[!UICONTROL Allocated]**- Tilldelad kredit till företaget.<br/>**[!UICONTROL Updated]** - En ändring gjordes i något av följande fält: [!UICONTROL Credit limit] / [!UICONTROL Credit currency] / [!UICONTROL Allow to exceed credit limit] <br/>**[!UICONTROL Purchased]**- En beställning gjordes.<br/>**[!UICONTROL Reimbursed]** - Det utestående saldot återbetalas. <br/>**[!UICONTROL Refunded]**- Ett kreditfakturabelopp har återbetalats.<br/>**[!UICONTROL Reverted]** - Ordern annullerades och beloppet returnerades till kreditsaldot. |
| [!UICONTROL Amount] | Beloppet för transaktionen som är associerad med följande transaktionstyper: `Purchased` / `Reimbursed` / `Refunded` / `Reverted` <br/>För inköpsbelopp visas beloppet i butikens visningsvaluta och i formatet för kreditvalutainställningen följt av aktuell konverteringsgrad (om tillämpligt). Till exempel: <br/>20 000,00 EUR ($22 400,00) <br/>USD/EUR 0,8928 |
| [!UICONTROL Outstanding Balance] | Det återbetalda beloppet minus det totala beloppet som ska betalas från alla order som lagts med metoden Betalning på konto. Beloppet kan visas som ett positivt eller negativt värde. <br/>**[!UICONTROL Positive value]**- En förskottsbetalning representeras som ett positivt värde.<br/>**[!UICONTROL Negative value]** - Ett förfallobelopp representeras som ett negativt värde. |
| [!UICONTROL Available Credit] | Summan av _[!UICONTROL Credit Limit]_och_[!UICONTROL Outstanding Balance]_. Om företaget har överskridit kreditgränsen visas beloppet som ett negativt värde. |
| [!UICONTROL Credit Limit] | Det kreditbelopp som har beviljats företaget. |
| [!UICONTROL Updated By] | Namnet på den person som initierade åtgärden. |
| [!UICONTROL Custom Reference Number] | Det anpassade referensnummer som är associerat med transaktionen. |
| [!UICONTROL Comment] | En kompilering av värdena från `Reason for Change` -fält, enligt åtgärdstyp. <br/>**[!UICONTROL Purchased]**- Innehåller kommentarer från köpet samt ordernumret och länken till ordern.<br/>**[!UICONTROL Reimbursed]** - Innehåller kommentarer från den återbetalda transaktionen. |
| [!UICONTROL Action] | För `Reimbursed` endast åtgärder. **[!UICONTROL Edit]** - Tillåter att ersättningsbeloppet uppdateras. |

{style="table-layout:auto"}

## Uppdatera kreditinformationen

När kunden betalar för sin utestående kredit till handlaren måste en butiksadministratör sedan uppdatera kundens kreditinformation i Admin.

1. På _Administratör_ sidebar, gå till **Kunder > Företag**.

1. Hitta företaget i rutnätet och öppna i _Redigera_ läge.

1. Expandera **Företagskrediter** -avsnitt.

1. För **Kreditgräns** anger du det nya värdet.

1. Ändra de andra värdena efter behov.

1. När uppdateringarna är klara klickar du på **[!UICONTROL Save]**.

## Ta emot betalningar

Ett återbetalt saldo är en offlinebetalning som ett företag gör mot saldot på sitt konto. Butiksadministratören anger beloppet manuellt i företagsprofilen med hjälp av _Återbetalningssaldo_ -knappen. När beloppet skickas beräknar systemet om det utestående saldot och tillgängliga företagskrediter och registrerar åtgärden i företagets kredithistorik. Det återbetalda beloppet anges i kreditvalutan enligt inställningarna i konfigurationen.

### Använda en betalning på ett företagskonto

1. På _Administratör_ sidebar, gå till **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Hitta företagsposten i listan och öppna i **[!UICONTROL Edit]** läge.

1. Klicka på längst upp på sidan **Återbetalningssaldo**.

1. Lägg till betalningsinformationen i dialogrutan:

   ![Återbetalningssaldo](./assets/company-reimburse-balance.png){width="500"}

   - Ange **Belopp** av betalningen.

     Beloppet kan anges som ett positivt eller negativt värde.

   - Ange **Anpassat referensnummer** för referens.

     Endast ett anpassat referensnummer kan anges per återbetalning. Om du vill använda betalningen för flera inköpsordrar skapar du en separat återbetalning för varje.

   - Ange **Kommentar** för att beskriva ersättningen.

1. Klicka **Återbetalning**.

   Företagets utestående saldo och tillgängliga krediter räknas om och företagets kredithistorik uppdateras för att återspegla återbetalningen.

### Redigera en återbetalning

1. Öppna företagsprofilen i **[!UICONTROL Edit]** läge.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **Företagskrediter** -avsnitt.

1. Hitta ersättningstransaktionen i rutnätet och klicka på **[!UICONTROL Edit]**.

1. Gör de ändringar som behövs för att **Anpassat referensnummer** och **Kommentar**.

   Återbetalningsbeloppet kan inte ändras.

1. Klicka på **[!UICONTROL Save]**.

## Kreditinformation för butiksexponeringar

För företagsadministratören visas på kontouppsättningen _Företagskrediter_ -avsnitt. Här anges aktuellt utestående saldo, tillgänglig kredit och kreditgränsen som tilldelas deras företagskonto följt av en lista över utestående fakturor.

Om handlaren annullerar en order som debiterats företagskrediter, returneras orderbeloppet till företagssaldot och _Kreditallokeringshistorik_ innehåller en post för åtgärden.

![Företagskrediter](./assets/company-credit.png){width="700" zoomable="yes"}

## Företagskreditdemo

Läs mer om hur du hanterar företagskrediter i den här filmen:

>[!VIDEO](https://video.tv.adobe.com/v/344445?quality=12)
