---
title: Initiera offert för en köpare
description: Lär dig hur en säljare kan skapa en offert för en viss köpare för att starta förhandlingsprocessen. Säljaren kan endast skicka offerter till kunder som är kopplade till ett företagskonto på den valda webbplatsen.
exl-id: 7bbb281f-7b6a-45fa-b906-da314d159bc8
feature: B2B, Quotes
role: Admin, User
source-git-commit: 96d592eed0e78234a9ce722f9bf1f904f42eadc1
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---

# Initiera en offert för en köpare

Om citattecken är aktiverade i [Konfiguration av försäljningsfunktioner](configure-quotes.md)kan en säljare initiera förhandlingsprocessen med en företagsköpare genom att skapa en offert från administratören.

- Utkastcitattecken visas bara för säljaren.
- Det går inte att skicka offerter förrän säljaren lägger till artiklar, relevanta rabatter och anteckningar för att skapa det ursprungliga erbjudandet för köparen.
- En säljare kan skapa en offert från citattecknen eller kundstödrastret.

Säljaren skickar offerten till köparen för att inleda förhandlingsprocessen. Se [Förhandla en offert](quote-price-negotiation.md).

## Erfarenhet av att skapa offerter för säljare

En säljare kan skapa en offert från offerterna eller kundstödrastret.

>[!NOTE]
>
>En demonstrationsvideo om hur en säljare skapar en offert för en köpare finns på [Säljaren initierar offerten](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/b2b/b2b-quote/sales-rep-initiates-quote.html) in _Commerce Videos och Tutorials_.

### Skapa en offert från offertstödrastret

1. Säljaren loggar in på administratören med [Behörigheter för försäljningsåtgärder](../systems/permissions.md) för att hantera offerter.

1. Gå till Admin [!UICONTROL Quotes] stödraster genom att markera **[!UICONTROL Sales]** och sedan markera **[!UICONTROL Quotes]**.

1. Skapa en offert för en köpare.

   - I rastret för citattecken väljer du **[!UICONTROL Create New Quote]**.

     ![Säljare som initierar en köpoffert från administratören](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}

   - På [!UICONTROL Create New Quote] väljer du kunden (företagsköparen) för att skapa offerten.

     ![Välj kund för ny offert](./assets/quote-draft-from-admin-select-buyer.png){width="700" zoomable="yes"}

     En ny offert visas i `Draft` status.

     ![Nytt offertutkast som skapats av säljaren](./assets/quote-create-by-seller.png){width="700" zoomable="yes"}

   - Uppdatera offertnamnet och ändra utgångsdatumet efter behov.

   - Spara offerten som ett utkast.

## Förbered offerten för köparen

När du har skapat offertutkastet lägger du till produktartiklar, lägger till rabatter och kommunicerar med köparen genom att lägga till kommentarer och relaterade filer i offerten. Skicka sedan offerten till köparen för granskning eller spara den som ett utkast.

1. Lägg till objekt i offerten genom att välja **[!UICONTROL Add Product By SKU]**. Ange SKU-numret och kvantiteten och välj sedan **[!UICONTROL Add Product]**.

![Säljaren lägger till artiklar i offertutkast för köparen](./assets/quote-draft-add-items.png){width="700" zoomable="yes"}

1. Använd radartikelrabatter på produkter efter behov.

   - Från [!UICONTROL Select] funktionsmakromeny, välja **[!UICONTROL Discount Item]**.

   - På [!UICONTROL Discount Line item] formulär väljer du **[!UICONTROL Discount Type]**.

   ![Använd radobjektrabatt på offert](./assets/quote-draft-add-items.png){width="700" zoomable="yes"}

   - I [!UICONTROL Discount] anger du värdet för rabattypen. Om du till exempel har valt en rabatt i procent anger du 10 för att tillämpa en rabatt på 10 % på radobjektet.

   - [!BADGE Funktioner för 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Endast tillgängligt för betaprogramdeltagare"}

     När ändringen har bekräftats uppdateras radobjektattributen i produktrutnätet så att rabattbeloppet visas. Om rabatten är låst visas en låsikon.

1. Använd rabatt på offertnivå efter behov:

   - I [!UICONTROL Quote Totals - Negotiated Price] väljer du rabattyp och anger sedan det värde som ska gälla.

     ![Säljaren lägger till rabatt på offertnivå](./assets/quote-draft-total-discount.png){width="700" zoomable="yes"}

   Rutnätet uppdateras för att visa rabatten.

1. Lägg till ytterligare information för köparen.

   I [!UICONTROL Negotiation - Comments], lägga till en anteckning och bifoga eventuella stödfiler som köparen behöver i [!UICONTROL Negotiation - Comments]

   ![Säljaren lägger till information för köparen](./assets/quote-draft-add-info-for-buyer.png){width="700" zoomable="yes"}

   Som standard är [bifogad fil](configure-quotes.md) kan vara upp till 2 MB i något av följande filformat: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG eller JPEG, PNG.

1. Bearbeta offerten.

   Spara offerten som ett utkast eller skicka den till köparen.

   - Om du sparar offerten som ett utkast uppdateras statusen till `Draft` och ett bekräftelsemeddelande visas:

     ![Bekräftelseutkast till offert har skickats till köparen](./assets/quote-draft-submitted-confirmation.png){width="700" zoomable="yes"}

   - Om du skickar offerten till köparen ändras statusen till `Submitted`. Köparen får ett e-postmeddelande för att granska offerten. Offerten är låst tills köparen returnerar den för vidare förhandling. Säljaren kan visa offerten från offertrutnätet eller kundrutnätet.

## Visa och skapa offerter från kundstödrastret

1. Gå till Admin [!UICONTROL Customer] stödraster genom att markera **[!UICONTROL Customers]** och sedan markera **[!UICONTROL All Customers]**.

1. Välj kund-ID för en företagsköpare.

   ![Bekräftelseutkast till offert har skickats till köparen](./assets/quote-view-customer-quotes.png){width="700" zoomable="yes"}

1. Välj **[!UICONTROL Edit]** för att visa kundinformationen.

1. Skapa en offert för kunden genom att välja **[!UICONTROL Create Quote]** och följa processen för att uppdatera offerten och skicka den till kunden.

1. Se kundernas befintliga offerter genom att välja **[!UICONTROL Quotes]**.

   ![Bekräftelseutkast till offert har skickats till köparen](./assets/quote-list-from-customer-information.png){width="700" zoomable="yes"}

1. Öppna en offert genom att välja **[!UICONTROL View]**.

Mer information om hur du hanterar offertförhandlingen finns i [Förhandla om en offert](quote-price-negotiation.md)
