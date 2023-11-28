---
title: Prisområde
description: Läs mer om vilket omfång som används för produktpriser, som kan konfigureras för att gälla både globalt och på webbplatsnivå.
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 0%

---

# Prisområde

Omfattningen av [basvaluta](../stores-purchase/currency-configuration.md) som används för produktpriser kan konfigureras så att de gäller både globalt och på webbplatsnivå. Om det används på global nivå används samma pris i hela butikshierarkin. Om den används på webbplatsnivå kan samma produkt finnas till olika priser från butiker som är kopplade till olika webbplatser. Som standard är produktprissättningen global.

Olika faktorer kan påverka priset på samma produkt på en plats och inte på en annan. Det kan till exempel finnas ytterligare distributionskostnader för produkten och andra överväganden som påverkar priset på produkter som säljs i en viss butik. I följande diagram visas en multisiteinstallation med basvalutan inställd på webbplatsnivån. De butiker och butiksvyer som är kopplade till varje webbplats återspeglar de produktpriser som anges på webbplatsnivå.

![B2B för Adobe Commerce](../assets/b2b.svg) Om du använder delade kataloger, se även [Ange priser och struktur för delade kataloger](../b2b/catalog-shared-pricing-structure.md) i _Handbok för B2B for Adobe Commerce_.

![Diagram över prisomfång](./assets/catalog-price-scope.svg){width="550"}

## Konfigurera prisomfång

1. På _Administratör_ meny, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL Catalog]** under.

1. Bläddra nedåt till **[!UICONTROL Price]** avsnitt och ange **[!UICONTROL Catalog Price Scope]** till något av följande:

   - `Global`
   - `Website`

   Omfångsinställningen som du väljer visas under prisfält i katalogen.

   ![Katalogprisomfång](./assets/catalog-price.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Använd omfång för att ställa in produktpriser

Handel tillåter inte att ett produktpris anges för varje butik. Men du kan ändra priset per webbplats:

1. På _Administratör_ meny, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL Catalog]** under.

1. I **[!UICONTROL Price]** flik, ange prisomfång till `Website` i stället för globalt.

1. Ställ in priset genom att öppna produktredigeringssidan, markera omfånget uppe till vänster och sedan ange ett nytt pris per webbplats.
