---
title: Orderstatus
description: Lär dig mer om fördefinierade orderstatusar och hur du definierar anpassade orderstatusar som är anpassade efter dina operativa behov.
exl-id: d1153558-a721-4643-a70c-7fc20072983c
feature: Orders
source-git-commit: c2d5e9b41a76ba58d1343a8b3ee5122104d5bfe0
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# Orderstatus

Alla order har en orderstatus som är associerad med en fas i orderbearbetningen [arbetsflöde](order-processing.md).\
Skillnaden mellan orderstatus och orderstatus är att **[!UICONTROL order states]** används programmatiskt. De är inte synliga för kunder eller administratörer. De bestämmer flödet för en order och vilka åtgärder som är möjliga för en order i ett visst läge.\
**[!UICONTROL Order statuses]** används för att förmedla status för en order till kunder och adminanvändare.
Du kan skapa ytterligare orderstatusar som passar dina operativa behov. Beställningsstatus är praktiska om du vill visa förloppet utanför Adobe Commerce, t.ex. beställa plocknings- och leveransstatus. De påverkar inte arbetsflödet för orderbehandling.\
Varje orderstatus är associerad med ett ordertillstånd. Butiken har en uppsättning fördefinierade inställningar för orderstatus och ordertillstånd.

![Ordna lägen och statusvärden](./assets/order-states-and-statuses.png){width="700" zoomable="yes"}

Statusen för varje order visas i _Status_ kolumn i _Beställningar_ rutnät.

![Orderstatus](./assets/stores-order-status-column.png){width="700" zoomable="yes"}

>[!TIP]
>
>En delvis återbetalningsorder finns kvar `Processing` status till **_alla_** beställda artiklar (inklusive återförda artiklar) skickas. Orderstatusen ändras inte till `Complete` tills alla artiklar i ordern har levererats.

## Arbetsflöde för ordertillstånd

![Arbetsflöde för ordertillstånd](./assets/order-state-workflow.png)

## Fördefinierad status

| Orderstatus | Statuskod |                                                                                                                                                                                                                                                                                        |
|--------------------------|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mottaget | `received` | Den här statusen är den initiala statusen för order som placeras när asynkron orderplacering är aktiverad. |
| Misstänkt bedrägeri | `fraud` | Ibland markeras beställningar som betalats via PayPal eller någon annan betalningsgateway som _Misstänkt bedrägeri_. Denna status innebär att ordern inte har någon utskickad faktura och att bekräftelsemeddelandet inte heller skickas. |
| Bearbetar | `processing` | När status för nya order är &#39;Bearbetning&#39;, _Fakturera alla artiklar automatiskt_ blir tillgängligt i konfigurationen. Fakturor skapas inte automatiskt för order som läggs med hjälp av presentkort, butikskrediter, belöningspoäng eller andra offlinebetalningsmetoder. |
| Väntande betalning | `pending_payment` | Den här statusen används om ordern skapas och PayPal eller liknande betalningsmetod används. Det innebär att kunden riktades till betalningstjänstens webbplats, men ingen returinformation har tagits emot ännu. Den här statusen ändras när kunden betalar. |
| Betalningsgranskning | `payment_review` | Den här statusen visas när PayPal-betalningsgranskning är aktiverad. |
| Väntande | `pending` | Den här statusen anger att ingen faktura eller försändelser har skickats. |
| Parkerad | `holded` | Den här statusen kan endast tilldelas manuellt. Du kan spärra alla beställningar. |
| Complete | `complete` | Denna status innebär att ordern skapas, betalas och skickas till kunden. |
| Stängd | `closed` | Den här statusen anger att en order har tilldelats en kreditnota och att kunden har fått en återbetalning. |
| Avbruten | `canceled` | Den här statusen tilldelas manuellt i Admin eller, för vissa betalningslösningar, när kunden inte betalar inom den angivna tiden. |
| Avvisad | `rejected` | Den här statusen innebär att en order avvisades under asynkron orderbearbetning. Detta inträffar när ett fel inträffar under asynkron orderplacering. |
| PayPal avbruten återföring | `paypay_canceled_reversal` | Den här statusen innebär att PayPal avbröt återföringen. |
| Pending PayPal | `pending_paypal` | Denna status innebär att beställningen togs emot av PayPal, men betalningen har ännu inte bearbetats. |
| PayPal omvänd | `paypal_reversed` | Denna status innebär att PayPal återförde transaktionen. |

{style="table-layout:auto"}

## Anpassad orderstatus

Förutom förinställda statusinställningar för ordning kan du skapa egna statusinställningar för beställning, tilldela dem till orderlägen och ange standardstatusvärden för beställningsstatus. Ordertillståndet anger positionen för ordern i orderbearbetningsarbetsflödet och orderstatusen tilldelar en meningsfull, översättningsbar etikett till positionen för ordern. Du kan till exempel behöva en anpassad orderstatus som `packaging"`, `backordered`eller en status som är specifik för dina behov. Du kan skapa ett beskrivande namn för den anpassade statusen och tilldela det till det associerade ordertillståndet i arbetsflödet.

>[!NOTE]
>
>Endast standardvärden för anpassad orderstatus används i orderarbetsflödet. Anpassade statusvärden som inte har angetts som standard kan bara användas i kommentarsavsnittet i ordningen.

![Inställningar för orderstatus](./assets/order-status.png){width="700" zoomable="yes"}

### Skapa en anpassad orderstatus

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Order Status]**.

1. Klicka på i det övre högra hörnet **[!UICONTROL Create New Status]**.

   ![Skapa ny orderstatus](./assets/order-status-new.png){width="600" zoomable="yes"}

1. Uppdatera _[!UICONTROL Order Status Information]_avsnitt:

   - Ange en **[!UICONTROL Status Code]** för intern referens. Det första tecknet måste vara en bokstav (a-z) och det andra kan vara vilken kombination av bokstäver och siffror som helst (0-9). Använd understrecket i stället för ett mellanslag.

   - För **[!UICONTROL Status Label]**, anger du en etikett som identifierar statusinställningen i både Admin och storeFront.

1. I _[!UICONTROL Store View Specific Labels]_anger du de etiketter som behövs för olika butiksvyer.

1. Klicka på **[!UICONTROL Save Status]**.

### Tilldela en orderstatus till ett läge

1. På _Orderstatus_ sida, klicka **[!UICONTROL Assign Status to State]**.

   ![Tilldela status](./assets/store-status-assign-status.png){width="600" zoomable="yes"}

1. Uppdatera **[!UICONTROL Assignment Information]** gör du följande:

   - Välj **[!UICONTROL Order Status]** som du vill tilldela. De listas efter statusetikett.

   - Ange **[!UICONTROL Order State]** till den plats i arbetsflödet där orderstatusen hör.

     >[!NOTE]
     >
     >**_[!UICONTROL Order State]_** listan innehåller standardstatusvärden för tilldelade order. Till exempel `Pending` standardorderstatus visas i stället för `New` orderlägesvärde.

   - Om du vill göra den här statusen till standard för orderläget väljer du **[!UICONTROL Use Order Status as Default]** kryssrutan.

     >[!NOTE]
     >
     >Endast standardorderstatusarna används i orderarbetsflödet. Status som inte är standard kan bara anges i **[!UICONTROL Order Comments]** i Admin.

   - Om du vill att den här statusen ska vara synlig från butiken väljer du **[!UICONTROL Visible On Storefront]** kryssrutan.

   ![Tilldela status till tillstånd](./assets/order-status-assign-state.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Status Assignment]**.

### Redigera en befintlig orderstatus

1. I _[!UICONTROL Order Status]_rutnät, öppna statusposten i redigeringsläge.

1. Uppdatera statusinställningarna efter behov.

1. Klicka på **[!UICONTROL Save Status]**.

### Ta bort en orderstatus från ett tilldelat läge

>[!NOTE]
>
>En statusinställning kan inte tas bort från ett läge om statusen används.

1. I _[!UICONTROL Order Status]_rutnät, sök efter den orderstatuspost som ska tas bort.

1. I _[!UICONTROL Action]_till höger om raden klickar du på&#x200B;**[!UICONTROL Unassign]**länk.

   Ett meddelande visas högst upp på arbetsytan om att orderstatusen inte har tilldelats. Även om orderstatusetiketten fortfarande visas i listan är den inte längre tilldelad till ett läge. Det går inte att ta bort inställningarna för orderstatus.

>[!NOTE]
>
>Om standardorderstatusen inte har tilldelats från ordertillståndet, _**en**_ orderstatus är _**ange automatiskt**_ som standard för det här orderläget.

## Meddelande

Kunderna kan följa orderstatus efter [RSS-feed](../merchandising-promotions/social-rss.md) om RSS-beställningsflödet är aktiverat i konfigurationen. När det här alternativet är aktiverat visas en länk till RSS-flödet på varje order.

### Aktivera meddelande om orderstatus

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL RSS Feeds]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Order]** -avsnitt.

1. Ange **[!UICONTROL Customer Order Status Notification]** till `Enable`.

   ![Meddelande om kundorderstatus](../configuration-reference/catalog/assets/rss-feeds-order.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

### Konfigurera e-postmeddelanden om ny beställning

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Sales Emails]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Order]** -avsnitt.

   ![Konfiguration - orderalternativ](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL New Order Confirmation Email Sender]** till något av följande:

   - `General Contact`
   - `Sales Representative`
   - `Customer Support`
   - `Custom Email 1`
   - `Custom Email 2`

1. Välj de mallar du vill använda för varje kundtyp:

   - **[!UICONTROL New Order Confirmation Template]** - Välj en mall för kunder med ett registrerat butikskonto.
   - **[!UICONTROL New Order Confirmation Template for Guest]** - Välj en mall som ska användas för gästkunder utan ett registrerat butikskonto.

1. Om du vill meddela en annan person (t.ex. en affärschef) om den nya ordern anger du den e-postadress som du vill använda **[!UICONTROL Send Order Email Copy To]**.

   Du kan lägga till flera e-postadresser om fler än en mottagare behövs.

1. Ange **[!UICONTROL Send Order Email Copy Method]** till något av följande:

   - `Bcc` - Endast ett e-postmeddelande om den nya beställningen skickas till både kunden och den andra mottagaren, men kunden ser inte att e-postmeddelandet de fick också skickades till den andra mottagaren.
   - `Separate Email` - Två separata e-postmeddelanden skickas - en till mottagaren och en till kunden.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
