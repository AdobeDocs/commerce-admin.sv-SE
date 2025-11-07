---
title: Belönings- och förmånsprogram
description: Läs om belöningspoängsystemet som ni kan använda för att öka kundengagemanget och främja kundlojaliteten.
exl-id: 2bccdcce-7936-4449-9634-d463ad29e5cc
feature: Rewards, Promotions/Events, Customers, Configuration
source-git-commit: 7a505b1dc953286aa9879e77bd322d9681513096
workflow-type: tm+mt
source-wordcount: '1363'
ht-degree: 0%

---

# Belönings- och förmånsprogram

{{ee-feature}}

_belöningspoängsystemet_ i Adobe Commerce ger dig möjlighet att implementera unika program som ökar kundengagemanget och främjar kundlojaliteten. Poäng kan tilldelas för ett stort antal transaktioner- och kundaktiviteter och konfigurationen kan ställas in för att styra poängallokering, balans och utgångsdatum. Kunderna kan lösa in poäng mot inköp baserat på den konverteringsgrad som ni fastställer mellan belöningspoäng och valuta.

## Prisregler för kundvagn

Poäng kan belönas för kunder baserat på en [kundvagnsregel](price-rules-cart.md). De kan belönas som den enda åtgärden i prisregeln, eller tillsammans med en rabatt.

## Kundsaldo

Belöningspunktsaldon kan hanteras av administratörsanvändare per kund. Om det är aktiverat i butiken kan kunderna även se information om sina poäng.

## Lösa in punkter

>[!NOTE]
>
>[Konfiguration av belöningsvalutakurser](reward-exchange-rates.md) krävs för inlösen av belöningspunkter av kunder och administratörsanvändare vid utcheckning.

Poängen kan lösas in av administratörsanvändare och -kunder (om de är aktiverade) under utcheckningen. I avsnittet Betalningsmetod visas kryssrutan Använd mina belöningspunkter ovanför de aktiverade betalningsmetoderna. Tillgängliga poäng och valutakurs inkluderas. Om det tillgängliga saldot är större än orderns totalsumma krävs ingen ytterligare betalningsmetod. Antalet belöningspoäng som tillämpas på ordern visas med ordersummorna, subtraherade från totalsumman, som liknar ett butikskreditkort eller presentkort. Om belöningspoäng används tillsammans med butikskrediter eller presentkort dras belöningspoängen av först. Butikskrediten eller presentkortet dras sedan av om ordersumman är större än det inlösta antalet belöningspoäng.

>[!NOTE]
>
>Belöningspoäng rekommenderas inte för postförskott eftersom det inte går att bekräfta inleveransen förrän ordern har fakturerats.

## Återbetala till belöningspoäng

Order som lagts med belöningspoäng kan återbetalas till belöningspoängen upp till det belopp som inlösts i ordern. På sidan [_Ny kreditnota_](../stores-purchase/credit-memo-create.md) kan antalet poäng som ska tillämpas på kundens saldo anges. Som standard innehåller fältet det fullständiga antalet punkter som användes i ordningen.

## Aktivera belöningspunktsåtgärder för din butik

Konfiguration av belöningspunkter avgör hur belöningspunkter presenteras i butiken och definierar de grundläggande driftparametrarna.

![Kundkonfiguration - belöningspoäng](../configuration-reference/customers/assets/reward-points-reward-points.png){width="600" zoomable="yes"}

### Steg 1. Konfigurera belöningspoäng

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_&#x200B;Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Customers]** i den vänstra panelen och välj **[!UICONTROL Reward Points]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Reward Points]** och gör följande:

   - Om du vill aktivera belöningspunkter anger du **[!UICONTROL Enable Reward Points Functionality]** till `Yes`.

   - Ange **[!UICONTROL Enable Reward Points Functionality on Storefront]** till `Yes` om du vill att kunderna ska kunna få sina egna belöningspoäng.

   - Om du vill att kunderna ska kunna se en detaljerad historik över sina belöningar anger du **[!UICONTROL Customers May See Reward Point History]** till `Yes`.

1. För **[!UICONTROL Reward Points Balance Redemption Threshold]** anger du det antal poäng som måste uppstå innan de kan lösas in (tomt utan minimalt).

1. För **[!UICONTROL Cap Reward Points Balance At]** anger du det maximala antalet poäng en kund kan få (tomt för ingen gräns).

1. För **[!UICONTROL Reward Points Expire in (days)]** anger du antalet dagar innan belöningspoängen förfaller (tomt om du inte vill förfalla).

1. Ange **[!UICONTROL Reward Points Expiry Calculation]** till något av följande:

   - `Static` - Fastställer den återstående livstiden för belöningspunkter baserat på antalet dagar som angetts i konfigurationen. Om utgångsgränsen i konfigurationen ändras ändras inte utgångsdatumet för befintliga punkter.

   - `Dynamic` - Beräknar det återstående antalet dagar när belöningspunktssaldot ökar. Om förfallogränsen i konfigurationen ändras uppdateras förfallotiden för alla befintliga punkter därefter.

1. Om du vill återbetala tillgängliga belöningspoäng automatiskt anger du **[!UICONTROL Refund Reward Points Automatically]** till `Yes`.

1. Ange **[!UICONTROL Deduct Reward Points from Refund Amount Automatically]** till `Yes` om du vill annullera belöningspoäng som erhållits genom inköp när ordern som fick poäng helt eller delvis återbetalas.

   >[!NOTE]
   >
   >Endast poäng som intjänas i den order som återbetalas påverkas.

1. Ange **[!UICONTROL Landing Page]** på innehållssidan som förklarar belöningspoängprogrammet.

   Se till att uppdatera standardsidan för belöningspunkter med din egen information.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

### Steg 2. Konfigurera poäng som tjänats in för kundaktiviteter

I det här steget anges antalet belöningspoäng som kan intjänas för olika kundaktiviteter. När kunderna utför en åtgärd som har tilldelats poäng visas ett meddelande som anger hur många poäng de har tjänat in.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Actions for Acquiring Reward Points by Customer]**.

   ![Kundkonfiguration - åtgärder för att erhålla belöningspoäng per kund](../configuration-reference/customers/assets/reward-points-actions-for-acquiring.png){width="600" zoomable="yes"}

1. Ange [&#x200B; till &#x200B;](reward-exchange-rates.md) om du vill tillåta belöningspoäng att intjänas för inköp baserat på de konfigurerade **[!UICONTROL Purchase]** belöningspriserna`Yes`.

   >[!NOTE]
   >
   >För att tjäna belöningspoäng för sin _första_-order måste kunden vara registrerad _innan_ transaktionen hämtas med betalningsmetoden. De flesta betalningsmetoder kunde konfigureras så att transaktioner _hämtas automatiskt_ när ordern läggs, men _före_ har kundkontoregistreringen slutförts.

1. För **[!UICONTROL Registration]** anger du antalet poäng som tjänats in för att öppna ett kundkonto.

1. För **[!UICONTROL Newsletter Signup]** anger du antalet poäng som tjänats in av registrerade kunder som prenumererar på ett nyhetsbrev.

1. För **[!UICONTROL Converting Invitation to Customer]** anger du antalet poäng som en kund tjänat in och mottagaren öppnar sedan ett kundkonto.

   Du kan begränsa antalet inbjudningskonverteringar som kan användas för att tjäna poäng för den kund som skickar inbjudan (tomt utan gräns). Om du vill göra det anger du ett nummer i fältet **[!UICONTROL Invitation to Customer Conversions Quantity Limit]**.

1. För **[!UICONTROL Converting Invitation to Order]** anger du antalet poäng som en kund tjänat in och som skickar en inbjudan till mottagaren som sedan lägger en order och gör följande:

   - För **Kvantitetsgräns för inbjudan till orderkonverteringar** anger du antalet poäng som kunden har tjänat in när mottagaren skickar en inledande order (tom för ingen begränsning).

   - För **[!UICONTROL Invitation Conversion to Order Reward]** väljer du alternativet `Each` för att få poäng för varje placering av mottagarordern, eller välj alternativet `First` för att få poäng enbart för den första placerade ordern från mottagaren.

1. För **[!UICONTROL Review Submission]** anger du antalet poäng som en kund som skickar in en granskning som godkänts för publicering får.

1. Om du sedan vill begränsa antalet granskningar som kan användas för att få poäng per kund anger du numret i fältet **[!UICONTROL Rewarded Reviews Submission Quantity Limit]** (tomt om du inte vill ha någon gräns).

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

### Steg 3. Slutför inställningarna för e-postmeddelanden

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Email Notification Settings]**.

   ![Kundkonfiguration - belöningspoäng - e-postmeddelanden](../configuration-reference/customers/assets/reward-points-email-notification-settings.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Email Sender]** till butikskontakten som visas som avsändare av saldouppdateringar och förfallomeddelanden.

1. Om du som standard vill prenumerera på kunder för att få meddelanden om balansuppdateringar och kommande förfallodatum anger du **[!UICONTROL Subscribe Customers by Default]** till `Yes`.

1. Ange **[!UICONTROL Balance Update Email]** till mallen som används för meddelandet som skickas till kunder när deras punktbalans uppdateras.

1. Ange **[!UICONTROL Reward Points Expiry Warning Email]** till mallen som används för meddelandet som skickas till kunder när förfallogränsen för en grupp punkter nås.

1. För **[!UICONTROL Expiry Warning Before (days)]** anger du antalet dagar innan det meddelandet skickas ut.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Uppdatera belöningspoängsaldot

Saldot för belöningspoäng kan uppdateras från administratören.

1. Gå till _>_ på sidofältet **[!UICONTROL Customers]** Admin **[!UICONTROL All Customers]**.

1. Hitta kunden i rutnätet och klicka på **[!UICONTROL Edit]** i kolumnen _[!UICONTROL Action]_.

1. Välj avsnittet _under_ Kundinformation **[!UICONTROL Reward Points]**.

1. Ange antalet **[!UICONTROL Update Points]**:

   - Om du vill uppdatera belöningspoängens belopp anger du talet för att öka det totala poängsaldot.
   - Om du vill subtrahera belöningspoängen anger du det negativa tal som du vill minska det totala poängsaldot.

1. Ange **[!UICONTROL Comments]** som är relaterad till justeringen av belöningspunkter, om det behövs.

   ![Balans för belöningspunkter](./assets/reward-points-balance.png){width="700" zoomable="yes"}

1. Om du vill kan du prenumerera på _meddelanden om belöningspunkter_:

   - **[!UICONTROL Subscribe for Balance Updates]**
   - **[!UICONTROL Subscribe for Points Expiration Notifications]**

1. Klicka på **[!UICONTROL Save Customer]**.

Alla åtgärder som är relaterade till belöningspunkter visas i kundens _[!UICONTROL Reward Points History]_-block i deras konto i butiken.

## Fältbeskrivningar

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Balance] | Aktuell saldo för belöningspoäng för kund |
| [!UICONTROL Amount Balance] | Beloppet för det aktuella saldot |
| [!UICONTROL Points] | Antalet tillagda eller subtraherade punkter |
| [!UICONTROL Amount] | Mängd tillförda eller subtraherade pengar |
| [!UICONTROL Rate] | [belöningens valutakurs](reward-exchange-rates.md) |
| [!UICONTROL Website] | Webbplats som belöningspoänghistoriken tilldelas till |
| [!UICONTROL Reason] | Orsaker till att poäng tilldelas:<br>**[!UICONTROL Making purchases]**- Varje gång kunden gör ett köp kan de få poäng.<br>**[!UICONTROL Registering on the site]** - Uppträder vid registrering (en gång).<br>**[!UICONTROL Subscribing to a newsletter]**- Upplupen för första prenumerationen (en gång).<br>**[!UICONTROL Sending Invitations]** - Tjäna poäng genom att bjuda in kompisar till webbplatsen.<br>**[!UICONTROL Converting Invitations to Customer]**- Få poäng för varje inbjudan de skickar ut, ledande vänner som registrerar sig på webbplatsen.<br>**[!UICONTROL Converting Invitations to Order]** - Få poäng för varje försäljning som är resultatet av en skickad inbjudan.<br>**[!UICONTROL Review Submission]**- Få poäng för att skicka produktrecensioner. |
| [!UICONTROL Created] | Datum och tid för uppdatering av belöningspoäng |
| [!UICONTROL Expired] | Antal förfallna belöningspoäng |
| [!UICONTROL Comment] | Kommentarer när punkter läggs till eller tas bort |

{style="table-layout:auto"}

