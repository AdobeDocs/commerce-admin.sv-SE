---
title: Initiera offert för en köpare
description: Lär dig hur en säljare kan skapa en offert för en viss köpare för att starta förhandlingsprocessen. Säljaren kan endast skicka offerter till kunder som är kopplade till ett företagskonto på den valda webbplatsen.
exl-id: 7bbb281f-7b6a-45fa-b906-da314d159bc8
feature: B2B, Quotes
role: Admin, User
source-git-commit: 69396421bae610ff02b12054bdea2278a8c0efe5
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Initiera en offert för en köpare

Om offerter är aktiverade i [konfigurationen för försäljningsfunktioner](configure-quotes.md) kan en säljare initiera förhandlingsprocessen med en företagsköpare genom att skapa en offert från administratören.

- Utkastcitattecken visas bara för säljaren.
- Det går inte att skicka offerter förrän säljaren lägger till artiklar, relevanta rabatter och anteckningar för att skapa det ursprungliga erbjudandet för köparen.
- En säljare kan skapa en offert från citattecknen eller kundstödrastret.

Säljaren skickar offerten till köparen för att inleda förhandlingsprocessen. Se [Förhandla en offert](quote-price-negotiation.md).

## Erfarenhet av att skapa offerter för säljare

En säljare kan skapa en offert från offerterna eller kundstödrastret.

>[!NOTE]
>
>En videodemo av en säljare som skapar en offert för en köpare finns i [Säljare initierar offerten](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/b2b/b2b-quote/sales-rep-initiates-quote.html?lang=sv-SE) i _Commerce Videos och Tutorials_.

### Skapa en offert från offertstödrastret

1. Säljaren loggar in på administratören som administratör med [försäljningsbehörighet](../systems/permissions.md) för att hantera offerter.

1. Gå till rutnätet [!UICONTROL Quotes] i Admin genom att markera **[!UICONTROL Sales]** och sedan välja **[!UICONTROL Quotes]**.

1. Skapa en offert för en köpare.

   - Välj **[!UICONTROL Create New Quote]** i rastret för citattecken.

     ![Säljaren initierar en köpoffert från administratören](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}

   - På sidan [!UICONTROL Create New Quote] väljer du kunden (företagsköparen) för att skapa offerten.

     ![Välj kund för ny offert](./assets/quote-draft-from-admin-select-buyer.png){width="700" zoomable="yes"}

     En ny offert visas med statusen `Draft`.

     ![Nytt utkast till offert skapad av säljaren](./assets/quote-create-by-seller.png){width="700" zoomable="yes"}

   - Uppdatera offertnamnet och ändra utgångsdatumet efter behov.

   - Spara offerten som ett utkast.

## Förbered offerten för köparen

När du har skapat offertutkastet lägger du till produktartiklar, lägger till rabatter och kommunicerar med köparen genom att lägga till kommentarer och relaterade filer i offerten. Skicka sedan offerten till köparen för granskning eller spara den som ett utkast.

1. Lägg till objekt i offerten genom att välja **[!UICONTROL Add Product By SKU]**. Ange SKU-numret och kvantiteten och välj sedan **[!UICONTROL Add Product]**.

   ![Säljaren lägger till objekt i offertutkast för köparen](./assets/quote-draft-add-items.png){width="675" zoomable="yes"}

1. Använd radartikelrabatter på produkter efter behov.

   - Välj **[!UICONTROL Discount Item]** på åtgärdsmenyn [!UICONTROL Select].

   - Markera **[!UICONTROL Discount Type]** i formuläret [!UICONTROL Discount Line item].

     ![Använd radobjektrabatt på offert](./assets/quote-discount-line-item.png){width="675" zoomable="yes"}

   - I fältet [!UICONTROL Discount] anger du värdet för rabattypen. Om du till exempel har valt en rabatt i procent anger du 10 för att tillämpa en rabatt på 10 % på radobjektet.

   - Du kan även låsa radartikelns rabattvärde så att produktpriset inte sänks ytterligare med eventuella rabatter som tillämpas på offertnivån.

     När ändringen har bekräftats uppdateras radobjektattributen i produktrutnätet så att rabattbeloppet visas. Om rabatten är låst visas en låsikon.

   En säljare kan begära en rabatt från en viss radobjekt i en offert.

   >[!NOTE]
   >
   >En demonstrationsvideo om hur rabatterna på radobjektet fungerar finns i [Säljare tillämpar rabatt på ett offertradobjekt](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/b2b/b2b-quote/quote-line-item-discount.html?lang=sv-SE) i _Commerce Videos och Tutorials_.

1. Använd rabatt på offertnivå efter behov:

   - I avsnittet [!UICONTROL Quote Totals - Negotiated Price] väljer du rabattypen och anger sedan det värde som ska användas.

     ![Säljaren lägger till rabatt på offertnivå](./assets/quote-draft-total-discount.png){width="700" zoomable="yes"}

   Rutnätet uppdateras för att visa rabatten.

1. Lägg till ytterligare information för köparen.

   Lägg till en anteckning på fliken **[!UICONTROL Negotiation - Comments]** och bifoga eventuella stödfiler som krävs för köparen.

   ![Försäljaren lägger till information för köparen](./assets/quote-draft-add-info-for-buyer.png){width="700" zoomable="yes"}

   Som standard kan en [bifogad fil](configure-quotes.md) vara upp till 2 MB i något av följande filformat: DOC, DOCX, XLS, XLSX, PDF, TXT, JPG eller JPEG, PNG.

1. Lägg till leveransadress under förhandlingar.

   En säljare kan göra ett leverans- och leveransval när köparen har lagt till en leveransadress i offerten.

   Leveransalternativen är låsta vid utcheckning.

   Mer information finns i [Mina citattecken](account-dashboard-my-quotes.md#adding-a-shipping-address).

1. Bearbeta offerten.

   Spara offerten som ett utkast eller skicka den till köparen.

   - Om du sparar offerten som ett utkast uppdateras statusen till `Draft` och ett bekräftelsemeddelande visas.

   - Om du skickar offerten till köparen ändras statusen till `Submitted`. Köparen får ett e-postmeddelande för att granska offerten. Offerten är låst tills köparen returnerar den för vidare förhandling. Säljaren kan visa offerten från offertrutnätet eller kundrutnätet.

## Visa och skapa offerter från kundstödrastret

1. Gå till rutnätet [!UICONTROL Customer] i Admin genom att markera **[!UICONTROL Customers]** och sedan välja **[!UICONTROL All Customers]**.

1. Välj kund-ID för en företagsköpare.

   ![Bekräftelseutkast till offert har skickats till köparen](./assets/quote-view-customer-quotes.png){width="700" zoomable="yes"}

1. Välj **[!UICONTROL Edit]** om du vill visa kundinformationen.

1. Skapa en offert för kunden genom att välja **[!UICONTROL Create Quote]** och följa processen för att uppdatera offerten och skicka den till kunden.

1. Visa kundernas befintliga offerter genom att välja **[!UICONTROL Quotes]**.

   ![Bekräftelseutkast till offert har skickats till köparen](./assets/quote-list-from-customer-information.png){width="700" zoomable="yes"}

1. Öppna en offert genom att välja **[!UICONTROL View]**.

Mer information om hur du hanterar offertförhandlingen finns i [Förhandla en offert](quote-price-negotiation.md)
