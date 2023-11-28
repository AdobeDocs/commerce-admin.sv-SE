---
title: Konfigurera returer
description: Lär dig hur du aktiverar returer för din butik och konfigurerar de leveransmetoder som stöds.
exl-id: a1b508fc-7e42-4d37-bf7e-dea17a40d39b
feature: Returns, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# Konfigurera returer

{{ee-feature}}

När det här alternativet är aktiverat kan RMA-begäranden skickas in av kunder från butiken. Ett RMA-nummer kan bara genereras om det finns ett objekt i ordningen som kan returneras. Begäranden att returnera enskilda objekt hanteras av _Aktivera RMA_ i varje produktpost. Som standard används konfigurationsinställningarna på produkten (_[!UICONTROL Use Config Settings]_är markerat). If_[!UICONTROL Enable RMA]_ är inställd på `No`, visas produkten inte i listan med artiklar som kan returneras. Om du ändrar _Aktivera RMA_ gäller det både nya och befintliga order.

## Aktivera RMA för din butik

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Sales]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL RMA Settings]** -avsnitt.

   ![RMA-inställningar](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enable RMA on Storefront]** till `Yes`.

   Den här inställningen avgör om kunderna kan skapa och visa RMA-begäranden från butiken. RMA-nummer kan tillämpas på både nya och befintliga order.

1. Ange **[!UICONTROL Enable RMA on Product Level]** till `Yes`.

   Den här inställningen avgör beteendet för _Aktivera RMA_ attribut för enskilda produkter i butiken:

   - När [!UICONTROL Enable RMA on Product Level] är inställd på `Yes`kan kunderna i butiken returnera alla enskilda produkter. Den innehåller båda _[!UICONTROL Enable RMA]_= `Yes` och_[!UICONTROL Enable RMA]_ = `No` produktattributvärden.
   - När [!UICONTROL Enable RMA on Product Level] är inställd på `No`kan kunder i butiken bara returnera produkter med _[!UICONTROL Enable RMA]_= `Yes` produktattributvärde.

1. Ange **[!UICONTROL Use Store Address]** till något av följande värden:

   - `Yes` - Skicka returnerade produkter till butiksadressen.
   - `No` - Ange en alternativ adress för produktreturer.

   ![RMA-inställningar med alternativ adress](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]**.

## Konfigurera leveransmetoder för returer

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Delivery Methods]**.

1. Expandera avsnittet för transportören som du vill använda för returtjänsten, till exempel **[!UICONTROL UPS]**.

   ![Aktivera RMA-tjänst för transportföretag](./assets/rma-delivery-method.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enabled for RMA]** till `Yes`.

1. Klicka på **[!UICONTROL Save Config]**.

## Ändra tillåtna RMA-nummer på produktnivå

Om du aktiverar RMA-nummer för din butik och katalogen innehåller produkter som inte ska kunna returneras, kan du ändra inställningen på produktnivå,

1. Öppna produkten i redigeringsläge.

1. Rulla ned och expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Autosettings]** -avsnitt.

1. Rensa **[!UICONTROL Use Config Setting]** vid behov.

1. Växla **[!UICONTROL Enable RMA]** ange till `No`.

   ![Inaktivera RMA för en produkt](./assets/product-advanced-autosettings-enable-rma.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]**.
