---
title: Kupongkoder
description: Lär dig hur du använder kupongkoder med kundprisregler för att tillämpa en rabatt när en uppsättning villkor uppfylls.
exl-id: 4f2e6203-0de2-44eb-a5f7-edd7b5f714d1
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: fdc14758788fa5cd0391371ebfafb478dadec8a4
workflow-type: tm+mt
source-wordcount: '1912'
ht-degree: 0%

---

# Kupongkoder

Kupongkoder används med [kundvagnsprisregler](price-rules-cart.md) för att tillämpa en rabatt när en uppsättning villkor uppfylls. En kupongkod kan till exempel skapas för en viss kundgrupp eller för alla som gör ett köp över ett visst belopp. Om du vill tillämpa kupongen på ett inköp kan kunden ange kupongkoden i kundvagnen eller eventuellt i kassaregistret för din _tegelbutik_. Här är några sätt att använda kuponger i din butik:

- E-postkuponger till kunder
- Skapa tryckta kuponger
- Skapa butikskuponger för mobilanvändare

Kupongkoder kan skickas via e-post eller inkluderas i nyhetsbrev, kataloger och annonser. Listan med kupongkoder kan exporteras och skickas till ett tryckeri. Ni kan också skapa butikskuponger med en snabb svarskod som kunderna kan skanna med sina smarttelefoner. QR-koden kan länka till en sida på webbplatsen med mer information om kampanjen.

Från och med Commerce 2.4.7 kan man få flera kuponger i en kundvagn. Handlarna kan också lägga på flera kuponger med hjälp av shoppingassistenten.

>[!NOTE]
>
>Kundprisregler som har samma prioritet ger ingen kombinerad rabatt. Varje regel (kupong) tillämpas på matchande produkter separat, en i taget, enligt kundprisregelns ID i databasen. Adobe rekommenderar att du anger olika prioriteter för varje tillagd kundprisregel för att styra i vilken ordning rabatterna ska tillämpas.

## Konfigurera kupongkoder

Längden på och formatet för automatiskt genererade kupongkoder styrs av konfigurationen. Tecknen kan anges till alla siffror, alla bokstäver eller en kombination. Du kan infoga ett bindestreck med angivna intervall för att göra det enkelt att läsa, och lägga till ett prefix och suffix för att associera koden med en viss kampanj eller ett visst initiativ.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Customers]** i den vänstra panelen och välj **[!UICONTROL Promotions]**.

   ![Kundkonfiguration - autogenererade specifika kupongkoder](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Expandera avsnittet **[!UICONTROL Auto Generated Specific Coupon Codes]**.

   ![Kundkonfiguration - autogenererade specifika kupongkoder](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Code Length]**, inklusive prefix, suffix och avgränsare.

1. Ange **[!UICONTROL Code Format]** till något av följande:

   - `Alphanumeric`
   - `Alphabetical`
   - `Numeric`

1. För **[!UICONTROL Code Prefix]** anger du det värde som du vill ska visas i början av alla kupongkoder.

1. För **[!UICONTROL Code Suffix]** anger du det värde som du vill ska visas i slutet av alla kupongkoder.

1. Ange antalet tecken mellan varje streck för **[!UICONTROL Dash Every X Characters]**.

   Kupongkoder med olika streckmönster anses vara olika koder, även om siffrorna är desamma.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Skapa kuponger

>[!NOTE]
>
>[!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."} Använd kommandot `bin/magento cron:run` för att verifiera att kron körs innan du skapar kuponger. Mer information finns i [Kör cron från kommandoraden](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html#run-cron-from-the-command-line) i _konfigurationshandboken_.

### Metod 1: Skapa en specifik kupong

1. Följ instruktionerna för att skapa en [kundvagnsprisregel](price-rules-cart.md).

1. I avsnittet **[!UICONTROL Rule Information]** anger du **[!UICONTROL Coupon]** till `Specific Coupon`.

1. Ange en **[!UICONTROL Coupon Code]** som ska användas med kampanjen.

   Kodformatet (numeriskt, alfanumeriskt eller alfabetiskt) bestäms av [konfigurationen](#configure-coupon-codes).

1. Så här begränsar du antalet gånger kupongen kan användas:

   - Ange antalet **[!UICONTROL Uses per Coupon]**.
   - Ange antalet **[!UICONTROL Uses per Customer]**.

   Lämna dessa fält tomma för obegränsad användning.

   ![Kundprisregel - kuponginformation](./assets/coupon-info.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Om flera kunder samtidigt använder samma kupong är det möjligt att den angivna gränsen kan överskridas på grund av försenad kupongbearbetning.

1. Så här gör du för att kupongen ska vara giltig under en tidsperiod:

   - ![Magento Open Source](../assets/open-source.svg) (endast Magento Open Source) Fyll i datumen **Från** och **Till**. Klicka på ikonen **Kalender** (![Kalender-ikon](../assets/icon-calendar.png)) bredvid varje fält för att välja datum. Om du låter datumintervallet vara tomt upphör regeln inte att gälla.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Gör något av följande:

     **Alternativ 1:** Schemalägg en ny uppdatering

      - Klicka på **[!UICONTROL Schedule New Update]** i det övre högra hörnet på sidan.

        ![Schemauppdatering](./assets/coupon-schedule-new-update.png){width="600" zoomable="yes"}

      - Ange **[!UICONTROL Update Name]** och **[!UICONTROL Description]**.

      - Välj **Startdatum** och **[!UICONTROL End Date]** i kalendern ( ![kalenderikon](../assets/icon-calendar.png) ). Om du låter datumintervallet vara tomt upphör regeln inte att gälla.

      - Klicka på **[!UICONTROL Save]** när du är klar.

        ![Kundprisregel - schemalagd ändring](./assets/coupon-scheduled-change.png){width="600" zoomable="yes"}

     **Alternativ 2:** Tilldela till en befintlig uppdatering:

      - Välj **[!UICONTROL Assign to Another Update]**.

      - Sök efter uppdateringen i listan och klicka på **[!UICONTROL Select]**.

1. Slutför kundprisregeln [kundvagnen](price-rules-cart.md) efter behov.

### Metod 2: Generera en grupp kuponger

Genereringen av rabattkuponger är en asynkron åtgärd som körs i bakgrunden så att du kan fortsätta arbeta i administratören utan att vänta på att åtgärden ska slutföras. Ett meddelande visas när uppgiften är slutförd.

1. Följ instruktionerna för att skapa en [kundvagnsprisregel](price-rules-cart.md).

1. Markera kryssrutan **[!UICONTROL Use Auto Generation]** under **[!UICONTROL Coupon Code]**.

1. Om du vill begränsa antalet gånger som varje kund kan använda kupongen anger du antalet **[!UICONTROL Uses per Customer]**.

   ![Kundprisregel - generera automatiskt numrerade kuponger](./assets/coupon-auto.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Om flera kunder samtidigt använder samma kupong är det möjligt att den angivna gränsen kan överskridas på grund av försenad kupongbearbetning.

1. Bläddra nedåt och expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Manage Coupon Codes]** och gör följande:

   ![Kundprisregel - hantera kupongkoder](./assets/manage-coupon-codes.png){width="600" zoomable="yes"}

   - Ange antalet kuponger som du vill generera för **[!UICONTROL Coupons Qty]**.

   - Ange **[!UICONTROL Code Length]**, utan prefix, suffix eller avgränsare.

   - Ange **[!UICONTROL Code Format]** till något av följande:

      - `Alphanumeric`
      - `Alphabetical`
      - `Numeric`

   - (Valfritt) Ange en **[!UICONTROL Code Prefix]** som ska läggas till i början av koden.

   - (Valfritt) Ange en **[!UICONTROL Code Suffix]** som ska läggas till i slutet av koden.

   - (Valfritt) Ange antalet tecken mellan varje streck för **[!UICONTROL Dash Every X Characters]**. Om koden till exempel är 12 tecken lång och det finns ett streck var fjärde tecken ser den ut som `xxxx-xxxx-xxxx`. Med streck blir det enklare att läsa och ange koder.

1. Klicka på **[!UICONTROL Generate]** när du är klar.

   Systemet visar `Message is added to queue, wait to get your coupons soon`.

   När cron-jobbet är klart visas listan med genererade koder.

   | Fält | Beskrivning |
   |-------------|-------------|
   | [!UICONTROL Coupon Code] | En unik kupongkod som har skapats och kan användas för att ta emot särskilda villkor. |
   | [!UICONTROL Created] | Datumet då kupongkoden skapades. |
   | [!UICONTROL Used] | Anger om kupongen användes. |
   | [!UICONTROL Times Used] | Anger hur många gånger kupongkoden användes. |

   {style="table-layout:auto"}

Du kan exportera kupongkoder till en CSV- eller Excel XML-fil genom att markera filformatet och klicka på **[!UICONTROL Export]**.

Om du vill ta bort kupongkoder väljer du en eller flera koder i listan. Välj `Delete` i **[!UICONTROL Actions]**-väljaren och klicka sedan på **[!UICONTROL Submit]**.

>[!NOTE]
>
>Även om Commerce tillåter konfigurering av flera kupongkoder, kan kunden bara använda en kupongkod i kundvagnen. Om du vill tillåta användning av mer än en kupongkod i kundvagnen samtidigt kan du använda ett motsvarande tillägg från [Commerce Marketplace](https://marketplace.magento.com/).

## Kupongrapport

Rapporten _Kuponger_ samlar in data från varje kupong som används under ett visst datumintervall. Eftersom kuponger används från kundvagnen innehåller rapporten data från alla inlösta kuponger, oavsett [orderstatus](../stores-purchase/order-status.md). Därför kan rapporten innehålla både beräknade och faktiska summor. Rapporten kan filtreras efter en viss butiksvy, tidsperiod, orderstatus och kundprisregel.

I följande exempel användes kupongkoden&quot;H20&quot; av två kunder. En av beställningarna faktureras, men den andra är fortfarande _väntande_. Kolumnerna Prognoserad förs.delsumma, Försäljningsrabatt och Försäljningssumma visar aggregerade belopp från båda orderna, men endast den faktiska fakturerade ordern visas i kolumnerna Delsumma, Rabatt och Totalt. Varje rad i rapporten representerar en kupongkampanj.

![Kupongrapport](./assets/reports-coupons.png){width="600" zoomable="yes"}

### Kör rapporten

1. Gå till **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Coupons]**&#x200B;på sidofältet_ Admin _.

1. Om du har flera butiksvyer anger du **[!DNL Store View]** i det övre vänstra hörnet för att fastställa rapportens omfång.

1. Om du vill uppdatera [försäljningsstatistiken](../getting-started/sales-reports.md#refresh-statistics) för dagen klickar du på meddelandet _Senast uppdaterad_ längst upp på arbetsytan.

   Klicka sedan för att markera kryssrutan **[!UICONTROL Coupons]** och klicka på **[!UICONTROL Refresh]**.

   ![Kupongrapport - uppdatera statistik](./assets/reports-coupons-refresh-statistics.png){width="600" zoomable="yes"}

1. Så här filtrerar du data:

   ![Kupongrapport - filter](./assets/reports-coupons-filters.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL Date Used]** till något av följande:

      - `Order Created`
      - `Order Updated`

     Rapporten _Order Updated_ skapas i realtid och kräver ingen uppdatering.

   - Ange **[!UICONTROL Period]** till något av följande för att definiera tidsperioden som omfattas av rapporten:

      - `Day`
      - `Month`
      - `Year`

   - Om du vill definiera datumintervallet för rapporten anger du datumen **Från** och **Till** i formatet M/D/YY.

   - Om du vill skriva ut en rapport för en viss [orderstatus](../stores-purchase/order-status.md) anger du **[!UICONTROL Order Status]** till `Specified` och väljer orderstatus i listan.

   - Om du vill utesluta rader utan data från rapporten anger du **[!UICONTROL Empty Rows]** till `No`.

   - Gör något av följande om du vill definiera kupongaktivitet som ingår i rapporten:

      - Om du vill inkludera all kupongaktivitet från alla prisregler anger du **[!UICONTROL Cart Price Rule]** till `Any`.
      - Om du bara vill ta med aktiviteter som är relaterade till en viss prisregel anger du **[!UICONTROL Cart Price Rule]** till `Specified` och väljer kundprisregeln i listan.

1. När du är klar att köra rapporten klickar du på **[!UICONTROL Show Report]**.

   Rapporten visas längst ned på sidan.

### Filteralternativ

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Date Used] | Identifierar datumfältet som används som grund för rapporten. Alternativ:<br/>**[!UICONTROL Order Created]**: Genererar rapporten baserat på det datum då ordern lades av kunden. Klicka på länken i meddelandet för att uppdatera statistiken för att se till att de senaste data finns med.<br/>**[!UICONTROL Order Updated]**: Skapar rapporten baserat på det datum då beställningarna senast uppdaterades. Den här rapporten använder realtidsdata och behöver inte uppdateras. |
| [!UICONTROL Period] | Bestämmer vilken typ av datumintervall som används för rapporten. Alternativ: `Day` / `Month` / `Year` |
| [!UICONTROL From] | Anger det första datumet i intervallet med orderdata som ingår i rapporten. |
| [!UICONTROL To] | Anger det sista datumet i intervallet med orderdata som ingår i rapporten. |
| [!UICONTROL Order Status] | Filtrerar rapporten efter orderstatus. Rapporten kan genereras för alla order eller kan begränsas till en viss orderstatus. Alternativ: <br/>**[!UICONTROL Any]**: Inkluderar alla order oavsett status.<br/>**[!UICONTROL Specified]**: Inkluderar endast order med den angivna statusen. Annullerade order ingår inte i rapporten. |
| [!UICONTROL Empty Rows] | Avgör om rapporten innehåller rader med tomma data som kan hämtas. Alternativ: `Yes` / `No` |
| [!UICONTROL Cart Price Rules] | Avgör vilka kupongkampanjer som ingår i rapporten. Alternativ:<br/>**[!UICONTROL Any]**: Inkluderar orderinformation för alla kupongkampanjer som användes under det angivna datumintervallet.<br/>**[!UICONTROL Specified]**: Inkluderar endast orderinformation för den valda kupongkampanjen under det angivna datumintervallet. |

{style="table-layout:auto"}

### Rapportkolumner

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Interval] | Anger datumintervallet för kuponganvändning som ska inkluderas i rapporten. Intervallet kan vara en viss dag, månad eller år eller ett visst datumintervall. Intervalldatumet formateras som i följande exempel, enligt värdet som angetts i inställningen **[!UICONTROL Period]**: <br/>`Day`: 6/21/19<br/>`Month`: 6/2019 <br/>`Year`: 2019 |
| [!UICONTROL Coupon Code] | Rabattkoden som kunderna anger i kundvagnen för att få rabatten. |
| [!UICONTROL Price Rule] | Namnet på prisregeln som är associerad med kupongen. |
| [!UICONTROL Uses] | Antalet gånger som kupongen har använts under det datumintervall som har angetts för rapporten. |
| [!UICONTROL Sales Subtotal] | Prognostiserad delsumma från alla order som placerats med kupongen. <br/>Delsumman för försäljning representerar den aggregerade delsumman från alla kvalificerande order och inkluderar `Pending` försäljningsorder som ännu inte har fakturerats. |
| [!UICONTROL Sales Discount] | Det planerade rabattbeloppet från alla order som placerats med kupongen. <br/>Rabatten representerar det aggregerade rabattbeloppet från alla kvalificerande order och inkluderar `Pending` försäljningsorder som ännu inte har fakturerats. |
| [!UICONTROL Sales Total] | Prognosen Summa av alla order som placerats med kupongen. Försäljningssumman inkluderar frakt- och expeditionsavgifter minus rabattbeloppet. <br/>Försäljningssumman representerar det aggregerade totalbeloppet från alla kvalificerande order och inkluderar `Pending` försäljningsorder som ännu inte har fakturerats. Värdet inkluderar delsumman plus frakt och hantering minus rabatt plus moms. <br/> Beräknat av: `((Subtotal + Shipping & Handling) - Discount) + Tax` |
| [!UICONTROL Subtotal] | Den aggregerade delsumman från alla fakturerade order som använde kupongen. |
| [!UICONTROL Discount] | Den aggregerade rabatten från alla fakturerade order som använde kupongen. |
| [!UICONTROL Total] | Den aggregerade ordersumman från alla fakturerade order som använde kupongen. |

{style="table-layout:auto"}
