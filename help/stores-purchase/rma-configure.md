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

När det här alternativet är aktiverat kan RMA-begäranden skickas in av kunder från butiken. Ett RMA-nummer kan bara genereras om det finns ett objekt i ordningen som kan returneras. Begäranden att returnera enskilda objekt hanteras av attributet _Enable RMA_ i varje produktpost. Som standard används konfigurationsinställningarna för produkten (_[!UICONTROL Use Config Settings]_är valt). Om_[!UICONTROL Enable RMA]_ är inställt på `No` visas produkten inte i listan med objekt som är tillgängliga för retur. Om du ändrar inställningen _Aktivera RMA_ gäller den både nya och befintliga order.

## Aktivera RMA för din butik

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Sales]** under.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL RMA Settings]**.

   ![RMA-inställningar](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enable RMA on Storefront]** till `Yes`.

   Den här inställningen avgör om kunderna kan skapa och visa RMA-begäranden från butiken. RMA-nummer kan tillämpas på både nya och befintliga order.

1. Ange **[!UICONTROL Enable RMA on Product Level]** till `Yes`.

   Den här inställningen avgör beteendet för attributet _Aktivera RMA_ för enskilda produkter i butiken:

   - När [!UICONTROL Enable RMA on Product Level] är inställt på `Yes` kan kunder i butiken returnera alla enskilda produkter. Den innehåller både _[!UICONTROL Enable RMA]_= `Yes` och_[!UICONTROL Enable RMA]_ = `No` produktattributsvärden.
   - När [!UICONTROL Enable RMA on Product Level] är inställt på `No` kan kunder på butiken bara returnera produkter med ett _[!UICONTROL Enable RMA]_= `Yes` produktattributvärde.

1. Ange **[!UICONTROL Use Store Address]** till ett av följande värden:

   - `Yes` - Skicka returnerade produkter till butiksadressen.
   - `No` - Ange en alternativ adress för produktreturer.

   ![RMA-inställningar med alternativ adress](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]**.

## Konfigurera leveransmetoder för returer

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Delivery Methods]**.

1. Expandera avsnittet för transportören som du vill använda för returtjänsten, till exempel **[!UICONTROL UPS]**.

   ![Aktivera RMA-tjänsten för transportföretaget](./assets/rma-delivery-method.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enabled for RMA]** till `Yes`.

1. Klicka på **[!UICONTROL Save Config]**.

## Ändra tillåtna RMA-nummer på produktnivå

Om du aktiverar RMA-nummer för din butik och katalogen innehåller produkter som inte ska kunna returneras, kan du ändra inställningen på produktnivå,

1. Öppna produkten i redigeringsläge.

1. Bläddra nedåt och utöka ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Autosettings]**.

1. Avmarkera kryssrutan **[!UICONTROL Use Config Setting]** om det behövs.

1. Växla inställningen **[!UICONTROL Enable RMA]** till `No`.

   ![Inaktivera RMA för en produkt](./assets/product-advanced-autosettings-enable-rma.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]**.
