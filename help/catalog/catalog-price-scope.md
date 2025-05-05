---
title: Prisområde
description: Läs mer om vilket omfång som används för produktpriser, som kan konfigureras för att gälla både globalt och på webbplatsnivå.
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---

# Prisområde

Omfånget för den [basvaluta](../stores-purchase/currency-configuration.md) som används för produktpriser kan konfigureras för att användas på global nivå eller på webbplatsnivå. Om det används på global nivå används samma pris i hela butikshierarkin. Om den används på webbplatsnivå kan samma produkt finnas till olika priser från butiker som är kopplade till olika webbplatser. Som standard är produktprissättningen global.

Olika faktorer kan påverka priset på samma produkt på en plats och inte på en annan. Det kan till exempel finnas ytterligare distributionskostnader för produkten och andra överväganden som påverkar priset på produkter som säljs i en viss butik. I följande diagram visas en multisiteinstallation med basvalutan inställd på webbplatsnivån. De butiker och butiksvyer som är kopplade till varje webbplats återspeglar de produktpriser som anges på webbplatsnivå.

![Adobe Commerce B2B](../assets/b2b.svg) Om du använder delade kataloger, se även [Ange priser och struktur för delade kataloger](../b2b/catalog-shared-pricing-structure.md) i _Adobe Commerce B2B-guiden_.

![Prisomfångsdiagram](./assets/catalog-price-scope.svg){width="550"}

## Konfigurera prisomfång

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på menyn_ Admin _.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Catalog]** under.

1. Rulla ned till avsnittet **[!UICONTROL Price]** och ange **[!UICONTROL Catalog Price Scope]** till något av följande:

   - `Global`
   - `Website`

   Omfångsinställningen som du väljer visas under prisfält i katalogen.

   ![Katalogprisomfång](./assets/catalog-price.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Använd omfång för att ställa in produktpriser

Commerce tillåter inte att ett produktpris fastställs för varje butik. Men du kan ändra priset per webbplats:

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på menyn_ Admin _.

1. Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Catalog]** under.

1. På fliken **[!UICONTROL Price]** anger du prisomfånget till `Website` i stället för globalt.

1. Ställ in priset genom att öppna produktredigeringssidan, markera omfånget uppe till vänster och sedan ange ett nytt pris per webbplats.
