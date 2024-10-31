---
title: Användningsexempel och arbetsflöden för offertmallar
description: Skapa en offertmall från en befintlig offert för att effektivisera offertförhandling för återkommande order.
feature: B2B, Quotes
source-git-commit: 3000d9abab467a86e37c7eca6e7db16b39c763ab
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---


# Offertmallar använder skiftläge och arbetsflöden

Tack vare funktionen för offertmallar kan köpare och säljare effektivisera offertprocessen genom att skapa återanvändbara och anpassningsbara offertmallar.

- **Anpassningsbara offerter** - Köpare kan generera länkade offerter från en förgodkänd mall, vilket möjliggör anpassning inom angivna parametrar som antal radartiklar och val.
- **Beställningströsklar** - Säljarna kan ange minsta och högsta orderåtaganden och se till att köparna följer avtalade inköpsvolymer.
- **Förfallodatum** - Mallar kan ha giltighetsperioder och säkerställer att villkoren bara är tillämpliga inom en angiven tidsram.
- **Rabatter och priser**- Säljarna kan använda samma radobjekt, offertnivå och fraktprisrabatt som finns tillgängliga med offerter för att ange rabatter för återkommande order, vilket förenklar förhandlingsprocessen.
- **Spårning och rapportering** - Systemet spårar antalet länkade offerter som genererats från mallen och slutfört order för att ge insikter om hur avtalade orderkvoter uppfylls.

## Användningsfall

En företagsköpare kan använda en offertmall för att beställa en viss uppsättning produkter under en tidsperiod. Köparen konfigurerar följande alternativ för offertmallar för att göra offertprocessen mer effektiv, konsekvent och anpassad till strategiska inköpsavtal.

- Beställningströskelvärde för att ange minsta och högsta antal order som är berättigade till förhandlat pris. Detta kan användas för att tillämpa och spåra beställningskvoter som anges i avtalsavtal.

- Kvantitetströsklar (minimi-/maximikvantiteter) I mallen anges ett tröskelvärde för kvantitet för att fastställa den minsta och högsta kvantitet som kan köpas för varje order, vilket säkerställer att säljaren kan hantera lagernivåerna effektivt samtidigt som köparen har möjlighet att justera kvantiteterna efter behov.

## Arbetsflöde för offertmall

Offertmallar kan initieras av köparen eller säljaren.

**Steg 1: Skapa offertmall (ny)**

- **Köparen skapar offertmallen**

  När man granskar en befintlig offertmall bestämmer sig köparen för att företaget måste skicka in flera order under det kommande året och vill begära ytterligare rabatter baserat på den upprepade verksamheten. De skapar en offertmall genom att använda åtgärden *[!UICONTROL Create quote template]* för offerten. Sedan initierar de förhandlingen genom att skicka den nya mallen till säljaren för granskning.

  Köpare kan också skapa en offertmall direkt från sidan *[!UICONTROL My Quote Templates]** i butiken.

- **Försäljningsrepresentant** - En säljare kan skapa en offertmall från administratören för en specifik företagsköpare. Säljaren kan skapa offertmallen i administratören från en befintlig offert eller från rutnätet [!UICONTROL Quote Templates] och spara den som en `draft` eller skicka den till köparen för att starta förhandlingen. I utkastläge är offerten bara synlig för säljaren. När offerten har skickats är statusen `Submitted`. Den kan inte ändras av säljaren förrän köparen skickar tillbaka den.

  ![Säljare som initierar en inköpsoffert från rastret Offerter i administratören](./assets/quote-template-create-from-grid.png){width="700" zoomable="yes"}

**Steg 2: Offertgranskning och förhandling (granskning)**

Granskning eller förhandling av en offertmall kan omfatta ändrade kvantiteter, borttagning av artiklar, tillägg av radartikelkommentarer, användning av radobjekt- eller offertrabatter (säljare) och tillägg av en leveransadress (köpare).

- **Säljaren visar förfrågan och skickar svar** - I administratören visar säljaren offertmallen från rutnätet *[!UICONTROL Quote Templates]** eller öppnar den från länken i e-postmeddelandet. I butiken ändras offertens status till `Pending` och köparen kan inte göra några ändringar. Efter samma process för [offertförhandling](quote-price-negotiation.md) svarar säljaren genom att erbjuda prisrabatter och justera kvantiteter och artiklar efter behov, ange en kommentar och skicka offerten tillbaka till köparen. Köparen och säljaren meddelas via e-post att säljaren har svarat.

- **Köparen visar offertmallen från säljaren och skickar svar** - Köparen klickar på länken i e-postmeddelandet för att öppna offertmallen eller öppnar offerten från sidan _Mina offertmallar_ på kontouppsättningen. Köparen kan lämna noteringar till säljaren på rad- eller offertnivå, ändra kvantiteter och ta bort artiklar.

Köparen och säljaren fortsätter att förhandla tills ett avtal nås eller säljaren avvisar offertmallen. Om köparen gör ändringar i offerten - lägger till eller tar bort produkter eller ändrar produktkvantiteter - måste offerten skickas tillbaka till säljaren för granskning.

- **Köparen lägger till en leveransadress** - Köparen måste lägga till en leveransadress i offertmallen om den inte har någon. När köparen har lagt till adressen kan säljaren tillhandahålla alternativ för frakt och leverans. Vilka leveransmetoder som visas beror på konfigurationen för Storefront.

Om köparen lägger till en leveransadress, måste förhandlingsavtalet granskas och säljaren kan fortsätta förhandlingsprocessen tills ett avtal nås eller säljaren avvisar offertmallen.

**Steg 3: Köparen accepterar offertmall**

Köparen accepterar de förhandlade villkoren i mallen. När offertmallen har godkänts kan köparen använda den för att generera förgodkända, länkade offerter som kan användas för att skicka order utan att ytterligare förhandling krävs.

Leveransalternativen är låsta vid utcheckning.

### Visa en offertmall

1. Klicka på **[!UICONTROL View]** i kolumnen **[!UICONTROL Actions]** för en post.

1. Om du vill besvara kundens begäran följer du instruktionerna och påbörjar samma [prisförhandlingsprocess](quote-price-negotiation.md) som används för att förhandla offerter.

### Visa mallaktivitet för offerter

Visa förhandlingens tidslinje, kommunikation och annan offertaktivitet från [!UICONTROL Comments] och [!UICONTROL History Log] - informationen innehåller statusändringar, uppdateringar av kund- och leveransinformation, artikel- och prisuppdateringar och annan viktig information.

1. Öppna en offertmall.

1. Visa kommentarer och historik för offertförhandling genom att bläddra till **[!UICONTROL Negotiation]** och välja **[!UICONTROL Comments]** och **[!UICONTROL History Log]**.

   ![Visa historik](./assets/quote-view-history.png){width="400"}

1. Händelser spåras också på radobjektnivå.

   ![Visa historik för radobjekt](./assets/quote-view-line-item-history.png){width="400"}


### Avvisa en offertmall

Endast offertmallar med statusen `In Review` kan avvisas.

1. Öppna offertmallen som du vill avvisa från rutnätet *[!UICONTROL Quote Templates]*.

1. Klicka på **[!UICONTROL Decline]** i offertmallen.

1. Ange anledningen till att offerten avvisades när du uppmanas till detta och klicka på **[!UICONTROL Confirm]**.