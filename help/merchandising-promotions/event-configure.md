---
title: Konfigurera händelser
description: Lär dig hur du slutför den grundläggande konfigurationen för att aktivera händelser och ställer in händelseblocket i butikens sidofält.
exl-id: 620b2d60-ce6f-4f31-93bb-18d3dd9cdce6
feature: Marketing Tools, Promotions/Events
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Konfigurera händelser

{{ee-feature}}

Innan du kan skapa en händelse måste du slutföra den grundläggande konfigurationen för att aktivera händelser och konfigurera händelseblocket i sidofältet.

## Aktivera och konfigurera händelser

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Catalog Events]** och gör följande:

   ![Katalogkonfiguration - kataloghändelser](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL Enable Catalog Events Functionality]** till `Yes`.

   - Ange **[!UICONTROL Enable Catalog Event Widget on Storefront]** till `Yes`.

   - Ange **[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]**. Som standard är det här värdet inställt på `5`. Om du bara vill visa en händelse i skjutreglaget åt gången anger du `1`.

   - Ange antalet **[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]**. Som standard är det här värdet inställt på `2`. Om du vill att reglaget ska visa nästa händelse i sekvensen när du klickar på den anger du `1`.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Åtkomstbegränsningar

Åtkomsten till en privat försäljning, ett evenemang eller en webbplats kan begränsas till registrerade kunder som loggar in eller utökas till icke-registrerade kunder som måste registrera sig innan de får åtkomst.

![Allmän konfiguration - webbplatsbegränsningar](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### Begränsa åtkomst

Åtkomsten till en privat försäljning, ett evenemang eller en webbplats kan begränsas till registrerade kunder som loggar in eller utökas till icke-registrerade kunder som måste registrera sig innan de får åtkomst.

![Allmän konfiguration - webbplatsbegränsningar](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL General]** i den vänstra panelen och välj **[!UICONTROL General]** under.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Website Restrictions]**.

1. Ange **[!UICONTROL Access Restriction]** till `Yes`.

1. Ange **[!UICONTROL Restriction Mode]** till något av följande:

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. Ange **[!UICONTROL Startup Page]** till något av följande:

   - `To login form (302 Found)` - Användare omdirigeras till inloggningsformuläret innan de får åtkomst till webbplatsen.

   - `To landing page (302 Found)` - Användare omdirigeras till den angivna landningssidan tills de loggar in.

     >[!IMPORTANT]
     >
     >Se till att du inkluderar en länk till inloggningssidan från landningssidan så att kunderna kan logga in för att komma åt webbplatsen.

1. Välj den **[!UICONTROL Landing Page]** som visas innan kunderna loggar in på den privata försäljningswebbplatsen.

1. Om du vill att sökmotorstart och spindlar ska veta att landningssidan är korrekt och att det inte finns några andra sidor att indexera på webbplatsen anger du **[!UICONTROL HTTP Response]** till `200 OK`.

   I alla andra fall inställda på `503 Service Unavailable`.

   >[!NOTE]
   >
   >Gäller endast om begränsningsläget är inställt på _Webbplatsen stängd_. Landningssidan återges som rå HTML.

1. Om du vill att fälten i kundinloggningen och formulären för glömt lösenord ska fyllas i automatiskt från tidigare poster anger du **[!UICONTROL Enable Autocomplete on login/forgot password forms]** till `Yes`.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

### Begränsa försäljningen

Som standard är produkter som visas i kommande eller stängda händelser inte tillgängliga för allmän försäljning och knappen _[!UICONTROL Add to Cart]_visas inte i produktlistan eller produktsidan.

Om du vill återställa knappen _[!UICONTROL Add to Cart]_för en stängd händelse måste händelsen tas bort (se [Uppdatera händelser](event-create.md#update-events)). Om en produkt är kopplad till en annan kategori som inte har några försäljningsbegränsningar är knappen tillgänglig på produktsidan. På samma sätt visas inte börskursblocket på produktsidan om produkten är kopplad till en annan kategori som inte har några försäljningsbegränsningar.
