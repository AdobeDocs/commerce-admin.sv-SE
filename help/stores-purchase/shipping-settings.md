---
title: Leveransinställningar
description: Lär dig hur du konfigurerar leveransinställningar som definierar ursprung och leveransregler för din butik.
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# Leveransinställningar

Leveranskonfigurationen fastställer referenspunkten för alla leveranser, din leveranspolicy och hanteringen av leveranser till flera adresser.

## Ursprungsplats

Ursprungspunkten används för att beräkna avgiften för försändelser som görs från din butik eller lagerställe, och fastställer även skattesatsen för sålda produkter. Vid beräkning [EU-skatt](international-tax-guidelines.md#eu-tax-configuration)måste du se till att [Beräkning av standardskattedestination](../configuration-reference/sales/tax.md) för varje butiksvy motsvarar ursprungspunkten för leveransinställningarna.

![Ursprung](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Shipping Settings]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Origin]** och fylla i följande:

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] (och rad 2, om det behövs)

1. Klicka på **[!UICONTROL Save Config]**.

## Leveranspolicy

En fraktpolicy bör förklara företagets affärsregler och riktlinjer för leveranser. Om du till exempel har prisregler som utlöser fri frakt kan du förklara villkoren i din fraktpolicy.

![Leveranspolicy vid utcheckning](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

Om du vill visa din leveranspolicy under utcheckning fyller du i parametrarna för leveranspolicy i konfigurationen. Texten visas när kunderna klickar _Se vår fraktpolicy_ vid utcheckning.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Shipping Settings]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Shipping Policy Parameters]** -avsnitt.

1. Ange **[!UICONTROL Apply Custom Shipping Policy]** till `Yes`.

1. Klistra in eller ange **[!UICONTROL Shipping Policy]** i textrutan.

   >[!NOTE]
   >
   >Om du använder en ordbehandlare för att komponera texten måste du spara dokumentet som en TXT-fil för att ta bort alla kontrolltecken från texten. Kopiera och klistra sedan in texten i textrutan Leveransregler.

   ![Parametrar för leveranspolicy](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]**.

## Flera adresser

Med alternativen för leverans av flera adresser kan kunderna skicka en order till flera adresser under utcheckningen och bestämma det högsta antalet adresser som en order kan skickas till.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Multishipping Settings]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Options]** -avsnitt.

   ![Leveransalternativ för flera adresser](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Allow Shipping to Multiple Addresses]** till `Yes`.

1. Ange **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]**.

1. Klicka på **[!UICONTROL Save Config]**.

>[!NOTE]
>
>![B2B för Adobe Commerce](../assets/b2b.svg) (B2B för Adobe Commerce) För beställningar med flera leveransadresser: [Betalning à conto](../b2b/enable-basic-features.md#configure-payment-on-account) betalningsmetoden är inte tillgänglig under utcheckningen, även om den är aktiverad.
