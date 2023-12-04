---
title: Belönings- och förmånsprogram
description: Läs om belöningspoängsystemet som ni kan använda för att öka kundengagemanget och främja kundlojaliteten.
exl-id: 2bccdcce-7936-4449-9634-d463ad29e5cc
feature: Rewards, Promotions/Events, Customers, Configuration
source-git-commit: 9d775e8e8521032dc58f6cd1ed7796595db745a0
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 0%

---

# Belönings- och förmånsprogram

{{ee-feature}}

The _belöningspoäng_ i Adobe Commerce ger er möjlighet att implementera unika program som ökar kundengagemanget och främjar kundlojaliteten. Poäng kan tilldelas för ett stort antal transaktioner- och kundaktiviteter och konfigurationen kan ställas in för att styra poängallokering, balans och utgångsdatum. Kunderna kan lösa in poäng mot inköp baserat på den konverteringsgrad som ni fastställer mellan belöningspoäng och valuta.

## Prisregler för kundvagn

Poängen kan belönas för kunder baserat på en [kundvagnsregel](price-rules-cart.md). De kan belönas som den enda åtgärden i prisregeln, eller tillsammans med en rabatt.

## Kundsaldo

Belöningspunktsaldon kan hanteras av administratörsanvändare per kund. Om det är aktiverat i butiken kan kunderna även se information om sina poäng.

## Lösa in punkter

>[!NOTE]
>
>[Belöningsbaserade växelkurser](reward-exchange-rates.md) konfiguration krävs för att kunder och administratörsanvändare ska kunna lösa in belöningspoäng vid utcheckning.

Poängen kan lösas in av administratörsanvändare och -kunder (om de är aktiverade) under utcheckningen. I avsnittet Betalningsmetod visas kryssrutan Använd mina belöningspunkter ovanför de aktiverade betalningsmetoderna. Tillgängliga poäng och valutakurs inkluderas. Om det tillgängliga saldot är större än orderns totalsumma krävs ingen ytterligare betalningsmetod. Antalet belöningspoäng som tillämpas på ordern visas med ordersummorna, subtraherade från totalsumman, som liknar ett butikskreditkort eller presentkort. Om belöningspoäng används tillsammans med butikskrediter eller presentkort dras belöningspoängen av först. Butikskrediten eller presentkortet dras sedan av om ordersumman är större än det inlösta antalet belöningspoäng.

>[!NOTE]
>
>Belöningspoäng rekommenderas inte för postförskott eftersom det inte går att bekräfta inleveransen förrän ordern har fakturerats.

## Återbetala till belöningspoäng

Order som lagts med belöningspoäng kan återbetalas till belöningspoängen upp till det belopp som inlösts i ordern. På [_Ny kreditnota_ page](../stores-purchase/credit-memo-create.md), kan antalet poäng som ska tillämpas på kundens saldo anges. Som standard innehåller fältet det fullständiga antalet punkter som användes i ordningen.

## Aktivera belöningspunktsåtgärder för din butik

Konfiguration av belöningspunkter avgör hur belöningspunkter presenteras i butiken och definierar de grundläggande driftparametrarna.

![Kundkonfiguration - belöningspoäng](../configuration-reference/customers/assets/reward-points-reward-points.png){width="600" zoomable="yes"}

### Steg 1. Konfigurera belöningspoäng

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Customers]** och välja **[!UICONTROL Reward Points]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Reward Points]** och gör följande:

   - Aktivera belöningspunkter genom att ange **[!UICONTROL Enable Reward Points Functionality]** till `Yes`.

   - Om du vill att kunderna ska kunna tjäna sina egna belöningspoäng anger du **[!UICONTROL Enable Reward Points Functionality on Storefront]** till `Yes`.

   - Om du vill att kunderna ska kunna se en detaljerad historik över sina belöningar anger du **[!UICONTROL Customers May See Reward Point History]** till `Yes`.

1. För **[!UICONTROL Reward Points Balance Redemption Threshold]** anger du antalet poäng som måste uppstå innan de kan lösas in (tomt utan minimalt).

1. För **[!UICONTROL Cap Reward Points Balance At]** anger du det maximala antalet poäng en kund kan få (tomt utan gräns).

1. För **[!UICONTROL Reward Points Expire in (days)]** anger du antalet dagar innan belöningspoängen förfaller (tomt om du inte vill förfalla).

1. Ange **[!UICONTROL Reward Points Expiry Calculation]** till något av följande:

   - `Static` - Bestämmer den återstående livslängden för belöningspoäng baserat på antalet dagar som anges i konfigurationen. Om utgångsgränsen i konfigurationen ändras ändras inte utgångsdatumet för befintliga punkter.

   - `Dynamic` - Beräknar det återstående antalet dagar när belöningspunktssaldot ökar. Om förfallogränsen i konfigurationen ändras uppdateras förfallotiden för alla befintliga punkter därefter.

1. Om du vill återbetala tillgängliga belöningspoäng automatiskt anger du **[!UICONTROL Refund Reward Points Automatically]** till `Yes`.

1. Ange om du vill annullera belöningspoäng som erhållits genom inköp när ordern som fått poäng helt eller delvis återbetalas **[!UICONTROL Deduct Reward Points from Refund Amount Automatically]** till `Yes`.

   >[!NOTE]
   >
   >Endast poäng som intjänas i den order som återbetalas påverkas.

1. Ange **[!UICONTROL Landing Page]** till innehållssidan som förklarar belöningspoängprogrammet.

   Se till att uppdatera standardsidan för belöningspunkter med din egen information.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

### Steg 2. Konfigurera poäng som tjänats in för kundaktiviteter

I det här steget anges antalet belöningspoäng som kan intjänas för olika kundaktiviteter. När kunderna utför en åtgärd som har tilldelats poäng visas ett meddelande som anger hur många poäng de har tjänat in.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Actions for Acquiring Reward Points by Customer]** -avsnitt.

   ![Kundkonfiguration - åtgärder för att erhålla belöningspoäng per kund](../configuration-reference/customers/assets/reward-points-actions-for-acquiring.png){width="600" zoomable="yes"}

1. Om du vill visa ett meddelande i kundvagnen som innehåller belöningspoäng som intjänats för köpet och kundens aktuella belöningspoäng anger du **[!UICONTROL Purchase]** till `Yes`.

   >[!NOTE]
   >
   >För att få belöningspoäng för sina _först_ beställning måste kunden registreras _före_ transaktionen hämtas med betalningsmetoden. De flesta betalningsmetoder kunde konfigureras för att hämta transaktioner _automatiskt_ när ordern placeras, men _före_ kundkontoregistreringen är klar.

1. För **[!UICONTROL Registration]** anger du antalet poäng som tjänats in för att öppna ett kundkonto.

1. För **[!UICONTROL Newsletter Signup]** anger du antalet poäng som registreras av kunder som prenumererar på ett nyhetsbrev.

1. För **[!UICONTROL Converting Invitation to Customer]** anger du antalet poäng som en kund får när han eller hon skickar en inbjudan och sedan öppnar ett kundkonto.

   Du kan begränsa antalet inbjudningskonverteringar som kan användas för att tjäna poäng för den kund som skickar inbjudan (tomt utan gräns). Om du vill göra det anger du en siffra i **[!UICONTROL Invitation to Customer Conversions Quantity Limit]** fält.

1. För **[!UICONTROL Converting Invitation to Order]** anger du antalet poäng som en kund får när han eller hon skickar en inbjudan till mottagaren som sedan lägger en order och gör följande:

   - För **Kvantitetsgräns för inbjudan till orderkonvertering** anger du antalet poäng som kunden tjänat in när mottagaren skickar inbjudan när mottagaren gör en första beställning (tom för ingen begränsning).

   - För **[!UICONTROL Invitation Conversion to Order Reward]** väljer du `Each` för att få poäng för varje mottagarorder, eller välj `First` om du bara vill få poäng för den första beställningen från mottagaren.

1. För **[!UICONTROL Review Submission]** anger du antalet poäng som en kund får när han/hon skickar in en recension som godkänts för publicering.

1. Om du sedan vill begränsa antalet recensioner som kan användas för att få poäng per kund anger du numret i dialogrutan **[!UICONTROL Rewarded Reviews Submission Quantity Limit]** fält (tomt för ingen gräns).

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

### Steg 3. Slutför inställningarna för e-postmeddelanden

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Email Notification Settings]** -avsnitt.

   ![Kundkonfiguration - belöningspoäng för e-postmeddelanden](../configuration-reference/customers/assets/reward-points-email-notification-settings.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Email Sender]** till butikskontakten som visas som avsändare av saldouppdateringar och förfallomeddelanden.

1. Om du som standard vill prenumerera på kunder för att få meddelanden om saldouppdateringar och kommande förfallodatum anger du **[!UICONTROL Subscribe Customers by Default]** till `Yes`.

1. Ange **[!UICONTROL Balance Update Email]** till den mall som används för det meddelande som skickas till kunderna när deras punktbalans uppdateras.

1. Ange **[!UICONTROL Reward Points Expiry Warning Email]** till den mall som används för det meddelande som skickas till kunderna när utgångsgränsen för ett batchantal poäng nås.

1. För **[!UICONTROL Expiry Warning Before (days)]** anger du antalet dagar innan det här meddelandet upphör att gälla.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Uppdatera belöningspoängsaldot

Saldot för belöningspoäng kan uppdateras från administratören.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Hitta kunden i rutnätet och klicka **[!UICONTROL Edit]** i _[!UICONTROL Action]_kolumn.

1. Under _Kundinformation_ väljer du **[!UICONTROL Reward Points]** -avsnitt.

1. Ange antalet **[!UICONTROL Update Points]**:

   - Om du vill uppdatera belöningspoängens belopp anger du talet för att öka det totala poängsaldot.
   - Om du vill subtrahera belöningspoängen anger du det negativa tal som du vill minska det totala poängsaldot.

1. Retur **[!UICONTROL Comments]** relaterat till justeringen av belöningspunkter, om det behövs.

   ![Saldo för belöningspoäng](./assets/reward-points-balance.png){width="700" zoomable="yes"}

1. Om du vill kan du prenumerera kunden på _Belöningsmeddelanden_:

   - **[!UICONTROL Subscribe for Balance Updates]**
   - **[!UICONTROL Subscribe for Points Expiration Notifications]**

1. Klicka på **[!UICONTROL Save Customer]**.

Alla åtgärder som rör belöningspoäng visas i kundens _[!UICONTROL Reward Points History]_blockera deras konto i butiken.

## Fältbeskrivningar

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Balance] | Aktuell saldo för belöningspoäng för kund |
| [!UICONTROL Amount Balance] | Beloppet för det aktuella saldot |
| [!UICONTROL Points] | Antalet tillagda eller subtraherade punkter |
| [!UICONTROL Amount] | Mängd tillförda eller subtraherade pengar |
| [!UICONTROL Rate] | The [avkastningskurs](reward-exchange-rates.md) |
| [!UICONTROL Website] | Webbplats som belöningspoänghistoriken tilldelas till |
| [!UICONTROL Reason] | Orsaker till att poäng tilldelas:<br>**[!UICONTROL Making purchases]**- Varje gång kunden gör ett köp kan de få poäng.<br>**[!UICONTROL Registering on the site]** - Uppträder vid registrering (en gång).<br>**[!UICONTROL Subscribing to a newsletter]**- Upplupen för förstagångsprenumeration (en gång).<br>**[!UICONTROL Sending Invitations]** — Få poäng genom att bjuda in kompisar till webbplatsen.<br>**[!UICONTROL Converting Invitations to Customer]**— Få poäng för varje inbjudan de skickar ut, ledande vänner som registrerar sig på webbplatsen.<br>**[!UICONTROL Converting Invitations to Order]** — Få poäng för varje försäljning som är resultatet av en skickad inbjudan.<br>**[!UICONTROL Review Submission]**- Få poäng för produktrecensioner. |
| [!UICONTROL Created] | Datum och tid för uppdatering av belöningspoäng |
| [!UICONTROL Expired] | Antal förfallna belöningspoäng |
| [!UICONTROL Comment] | Kommentarer när punkter läggs till eller tas bort |

{style="table-layout:auto"}

## Felsökningsresurser

Hjälp om felsökning av belöningspoängproblem finns i följande artiklar i kunskapsbasen med Commerce Support:

- [Förmånspoäng för partiella order](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31295-magento-patch-loyalty-points-on-partial-orders.html)
- [404-fel - ta bort belöningspoäng vid utcheckning av flera leveranser](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/magento-2.4.0-404-error-removing-rewards-points-on-multi-shipping-checkout.html)
