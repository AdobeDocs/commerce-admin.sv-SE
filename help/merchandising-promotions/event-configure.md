---
title: Konfigurera händelser
description: Lär dig hur du slutför den grundläggande konfigurationen för att aktivera händelser och ställer in händelseblocket i butikens sidofält.
exl-id: 620b2d60-ce6f-4f31-93bb-18d3dd9cdce6
feature: Marketing Tools, Promotions/Events
source-git-commit: 084d2c3381f57a8a4c7e8ffde9da1abd4d8af670
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Konfigurera händelser

{{ee-feature}}

Innan du kan skapa en händelse måste du slutföra den grundläggande konfigurationen för att aktivera händelser och konfigurera händelseblocket i sidofältet.

## Aktivera och konfigurera händelser

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Catalog Events]** och gör följande:

   ![Katalogkonfiguration - kataloghändelser](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL Enable Catalog Events Functionality]** till `Yes`.

   - Ange **[!UICONTROL Enable Catalog Event Widget on Storefront]** till `Yes`.

   - Ange **[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]**. Som standard är det här värdet inställt på `5`. Om du bara vill visa en händelse i skjutreglaget åt gången anger du `1`.

   - Ange antalet **[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]**. Som standard är det här värdet inställt på `2`. Om du vill att reglaget ska visa nästa händelse i sekvensen när du klickar på den, anger du `1`.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Åtkomstbegränsningar

Åtkomsten till en privat försäljning, ett evenemang eller en webbplats kan begränsas till registrerade kunder som loggar in eller utökas till icke-registrerade kunder som måste registrera sig innan de får åtkomst.

![Allmän konfiguration - webbplatsbegränsningar](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### Begränsa åtkomst

Åtkomsten till en privat försäljning, ett evenemang eller en webbplats kan begränsas till registrerade kunder som loggar in eller utökas till icke-registrerade kunder som måste registrera sig innan de får åtkomst.

![Allmän konfiguration - webbplatsbegränsningar](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL General]** och välja **[!UICONTROL General]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Website Restrictions]** -avsnitt.

1. Ange **[!UICONTROL Access Restriction]** till `Yes`.

1. Ange **[!UICONTROL Restriction Mode]** till något av följande:

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. Ange **[!UICONTROL Startup Page]** till något av följande:

   - `To login form (302 Found)` - Användarna dirigeras om till inloggningsformuläret innan de får åtkomst till webbplatsen.

   - `To landing page (302 Found)` - Användare dirigeras om till den angivna landningssidan tills de loggar in.

     >[!IMPORTANT]
     >
     >Se till att du inkluderar en länk till inloggningssidan från landningssidan så att kunderna kan logga in för att komma åt webbplatsen.

1. Välj **[!UICONTROL Landing Page]** som visas innan kunderna loggar in på den privata försäljningswebbplatsen.

1. Om du vill att sökmotorstart och spindlar ska veta att landningssidan är korrekt och att det inte finns några andra sidor att indexera på webbplatsen anger du **[!UICONTROL HTTP Response]** till `200 OK`.

   I alla andra fall inställda på `503 Service Unavailable`.

   >[!NOTE]
   >
   >Gäller endast om begränsningsläget är inställt på _Webbplatsen stängd_. Landningssidan återges som rå HTML.

1. Om du vill att fälten i kundinloggningen och i formulären för glömt lösenord ska fyllas i automatiskt från tidigare poster anger du **[!UICONTROL Enable Autocomplete on login/forgot password forms]** till `Yes`.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

### Begränsa försäljningen

Som standard är produkter som visas i kommande eller stängda evenemang inte tillgängliga för allmän försäljning och _[!UICONTROL Add to Cart]_visas inte på produktlistan eller produktsidan.

Återställ _[!UICONTROL Add to Cart]_för en stängd händelse måste händelsen tas bort (se [Uppdatera händelser](event-create.md#update-events)). Om en produkt är kopplad till en annan kategori som inte har några försäljningsbegränsningar är knappen tillgänglig på produktsidan. På samma sätt visas inte börskursblocket på produktsidan om produkten är kopplad till en annan kategori som inte har några försäljningsbegränsningar.
