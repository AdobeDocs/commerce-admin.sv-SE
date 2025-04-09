---
title: Användningsexempel och arbetsflöden för offertmallar
description: Skapa en offertmall från en befintlig offert för att effektivisera offertförhandling för återkommande order.
feature: B2B, Quotes
exl-id: 7d1e7a3d-6c50-416a-b490-0a083e1c06b4
source-git-commit: 6fe8a356ab517fc5dd169c4a6f7ef52937f705c4
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 0%

---

# Offertmallar använder skiftläge och arbetsflöden

Tack vare funktionen för offertmallar kan köpare och säljare effektivisera offertprocessen genom att skapa återanvändbara och anpassningsbara offertmallar.

- **Anpassningsbara offerter** - Köpare kan generera länkade offerter från en förgodkänd mall, vilket möjliggör anpassning inom angivna parametrar som antal radartiklar och val.
- **Beställningströsklar** - Säljarna kan ange minsta och högsta orderåtaganden och se till att köparna följer avtalade inköpsvolymer. När köparen har godkänt offertmallen ökas ordertröskelvärdet varje gång en länkad offert skapas. Om den länkade offerten stängs utan att konverteras till en order subtraheras ordern från tröskelvärdet. När det högsta ordertröskelvärdet har uppnåtts upphör offertmallen att gälla.
- **Förfallodatum** - Mallar kan ha giltighetsperioder (*[!UICONTROL Valid Until]*), vilket säkerställer att villkoren bara är tillämpliga inom en angiven tidsram. Mallen stängs och alla kopplade offerter stängs.
- **Rabatter och priser**- Säljarna kan använda samma radobjekt, offertnivå och fraktprisrabatt som finns tillgängliga med offerter för att ange rabatter för återkommande order, vilket förenklar förhandlingsprocessen.
- **Spårning och rapportering** - Systemet spårar antalet länkade offerter som genererats från mallen och slutfört order för att ge insikter om hur avtalade orderkvoter uppfylls.
- **Referera till dokumentlänkar** - Både köpare och säljare kan lägga till, redigera och hantera externa dokumentlänkar (som DocuSign, Adobe Sign eller andra onlinetjänster) i offertmallen. Detta gör det enkelt att komma åt relaterade kontrakt och avtal under offertmallsprocessen.

## Användningsfall

En företagsköpare kan använda en offertmall för att beställa en viss uppsättning produkter under en tidsperiod. Köparen konfigurerar följande alternativ för offertmallar för att göra offertprocessen mer effektiv, konsekvent och anpassad till strategiska inköpsavtal.

- Beställningströskelvärde för att ange minsta och högsta antal order som är berättigade till förhandlat pris. Detta kan användas för att tillämpa och spåra beställningskvoter som anges i avtalsavtal.

- Kvantitetströsklar (minimi-/maximikvantiteter) I mallen anges ett tröskelvärde för kvantitet för att fastställa den minsta och högsta kvantitet som kan köpas för varje order, vilket säkerställer att säljaren kan hantera lagernivåerna effektivt samtidigt som köparen har möjlighet att justera kvantiteterna efter behov.

- Länkar till referensdokument för att upprätthålla anslutningar till externa kontrakt och avtal, vilket gör det enklare att komma åt relaterad dokumentation under offertprocessen.

## Arbetsflöde för offertmall

Offertmallar kan initieras av köparen eller säljaren.

**Steg 1: Skapa offertmall (ny)**

- **Köparen skapar offertmallen**

  När en befintlig offert granskas bestämmer köparen att företaget måste skicka in flera order under det kommande året och vill begära ytterligare rabatter baserat på upprepad verksamhet. De skapar en offertmall genom att använda åtgärden *[!UICONTROL Create quote template]* för offerten. Köparen kan lägga till referensdokumentlänkar till externa kontrakt eller avtal med kontrollen *[!UICONTROL Add]* i avsnittet med referensdokument. Sedan initierar de förhandlingen genom att skicka offertmallen till säljaren för granskning.

  Köpare kan också beställa en offertmall genom att lägga produkter de vill köpa regelbundet i kundvagnen. Begär sedan en offert och ange i kommentarerna hur ofta de vill upprepa köpet.

- **Försäljningsrepresentant** - En säljare kan skapa en offertmall från administratören för en specifik företagsköpare. Säljaren kan skapa offertmallen i administratören från en befintlig offert eller från rutnätet [!UICONTROL Quote Templates] och spara den som en `draft` eller skicka den till köparen för att starta förhandlingen. I utkastläge är offerten bara synlig för säljaren. När offerten har skickats är statusen `Submitted`. Den kan inte ändras av säljaren förrän köparen skickar tillbaka den.

  ![Säljare som initierar en inköpsoffert från rastret Offerter i administratören](./assets/quote-template-create-from-grid.png){width="700" zoomable="yes"}

  När säljaren skapar offertmallen är förfallodatumet ([!UICONTROL Valid until] datumfält) som standard 180 dagar. Om köparen skapade mallen är förfallodatumet tomt.  Köparen måste ange förfallodatumet innan mallen skickas tillbaka till köparen för granskning.

  När säljaren skapar offertmallen är förfallodatumet (*[!UICONTROL Valid until]* datumfält) som standard 180 dagar. Om köparen skapade mallen är förfallodatumet tomt.  Köparen måste ange förfallodatumet innan mallen skickas tillbaka till köparen för granskning.

**Steg 2: Offertgranskning och förhandling (granskning)**

Att granska eller förhandla om en offertmall kan inkludera ändrade kvantiteter, borttagna artiklar, lägga till radartikelkommentarer, tillämpa radobjekt- eller offertrabatter (säljare), lägga till en leveransadress (köpare) och hantera länkar till referensdokument.

- **Säljaren visar förfrågan och skickar svar** - I administratören visar säljaren offertmallen från rutnätet *[!UICONTROL Quote Templates]** eller öppnar den från länken i e-postmeddelandet. I butiken ändras offertens status till `Pending` och köparen kan inte göra några ändringar. Efter samma process för [offertförhandling](quote-price-negotiation.md) svarar säljaren genom att erbjuda prisrabatter och justera kvantiteter och artiklar efter behov, anger en kommentar och skickar offertmallen tillbaka till köparen. Säljaren kan också lägga till, redigera eller ta bort referensdokumentlänkar under den här processen. Köparen och säljaren meddelas via e-post att säljaren har svarat.

- **Köparen visar offertmallen från säljaren och skickar svar** - Köparen klickar på länken i e-postmeddelandet för att öppna offertmallen eller öppnar den från sidan _Mina offertmallar_ på kontonamallen. Köparen kan lämna noteringar till säljaren på radobjekt- eller offertnivå, ändra kvantiteter, ta bort artiklar och hantera referensdokumentlänkar.

Köparen och säljaren fortsätter att förhandla tills ett avtal nås eller säljaren avvisar offertmallen. Om köparen gör ändringar i offertmallen - lägger till eller tar bort produkter, ändrar produktkvantiteter eller ändrar referensdokumentlänkar - måste den returneras till säljaren för granskning.

- **Köparen lägger till en leveransadress** - Köparen måste lägga till en leveransadress i offertmallen om den inte har någon. När köparen har lagt till adressen kan säljaren tillhandahålla alternativ för frakt och leverans. Vilka leveransmetoder som visas beror på konfigurationen för Storefront.

Om köparen lägger till en leveransadress, måste förhandlingsavtalet granskas och säljaren kan fortsätta förhandlingsprocessen tills ett avtal nås eller säljaren avvisar offertmallen.

**Steg 3: Köparen accepterar offertmall**

Köparen accepterar de förhandlade villkoren i mallen. När offertmallen har godkänts kan köparen använda den för att [generera förgodkända, länkade offerter](account-dashboard-my-quote-templates.md#generate-a-linked-quote) som kan användas för att skicka order utan att ytterligare förhandling krävs.

Leveransalternativen är låsta vid utcheckning.

Offertmallar är aktiva tills de går ut, annulleras eller stängs, eller så är det inte längre en giltig köpare som har nått det högsta ordertröskelvärdet.

### Visa en offertmall

1. Klicka på **[!UICONTROL View]** i kolumnen **[!UICONTROL Actions]** för en post.

1. Om du vill besvara kundens begäran följer du instruktionerna och påbörjar samma [prisförhandlingsprocess](quote-price-negotiation.md) som används för att förhandla offerter.

### Visa mallaktivitet för offerter

Visa tidslinjen för förhandlingen, kommunikation och annan offertmallsaktivitet från [!UICONTROL Comments] och [!UICONTROL History Log] - informationen innehåller statusändringar, uppdateringar av kund- och leveransinformation, artikel- och prisuppdateringar och annan viktig information.

1. Öppna en offertmall.

1. Visa kommentarer och historik för offertförhandling genom att bläddra till **[!UICONTROL Negotiation]** och välja **[!UICONTROL Comments]** och **[!UICONTROL History Log]**.

   ![Visa historik](./assets/quote-view-history.png){width="400" zoomable="yes"}

1. Händelser spåras också på radobjektnivå.

   ![Visa historik för radobjekt](./assets/quote-view-line-item-history.png){width="400" zoomable="yes"}

### Avvisa en offertmall

Endast offertmallar med statusen `In Review` kan avvisas.

1. Öppna offertmallen som du vill avvisa från rutnätet *[!UICONTROL Quote Templates]*.

1. Klicka på **[!UICONTROL Decline]** i offertmallen.

1. Ange anledningen till att offerten avvisades när du uppmanas till detta och klicka på **[!UICONTROL Confirm]**.
