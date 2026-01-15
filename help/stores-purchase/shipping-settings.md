---
title: Leveransinställningar
description: Lär dig hur du konfigurerar leveransinställningar som definierar ursprung och leveransregler för din butik.
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
source-git-commit: 528e57df775b53b6137e1542ad0583c60d2f47ff
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 0%

---

# Leveransinställningar

Leveranskonfigurationen fastställer referenspunkten för alla leveranser, din leveranspolicy och hanteringen av leveranser till flera adresser.

## Ursprungsplats

Ursprungspunkten används för att beräkna avgiften för försändelser som görs från din butik eller lagerställe, och fastställer även skattesatsen för sålda produkter. När du beräknar [EU-skatt](international-tax-guidelines.md#eu-tax-configuration) måste du se till att [Standardberäkning för skattemål](../configuration-reference/sales/tax.md) för varje butiksvy motsvarar ursprungspunkten för leveransinställningar.

![Ursprung](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_&#x200B;Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Shipping Settings]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Origin]** och fyll i följande:

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] (och rad 2, om det behövs)

1. Klicka på **[!UICONTROL Save Config]**.

## Leveranspolicy

En fraktpolicy bör förklara företagets affärsregler och riktlinjer för leveranser. Om du till exempel har prisregler som utlöser fri frakt kan du förklara villkoren i din fraktpolicy.

![Leveransprincip vid utcheckning](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

Om du vill visa din leveranspolicy under utcheckning fyller du i parametrarna för leveranspolicy i konfigurationen. Texten visas när kunderna klickar på _Se vår leveranspolicy_ under utcheckningen.

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_&#x200B;Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Shipping Settings]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Shipping Policy Parameters]**.

1. Ange **[!UICONTROL Apply Custom Shipping Policy]** till `Yes`.

1. Klistra in eller ange **[!UICONTROL Shipping Policy]** i textrutan.

   >[!NOTE]
   >
   >Om du använder en ordbehandlare för att komponera texten måste du spara dokumentet som en TXT-fil för att ta bort alla kontrolltecken från texten. Kopiera och klistra sedan in texten i textrutan Leveransregler.

   ![Parametrar för leveransprincip](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]**.

## Flera adresser

Med alternativen för leverans av flera adresser kan kunderna skicka en order till flera adresser under utcheckningen och bestämma det högsta antalet adresser som en order kan skickas till.

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_&#x200B;Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Multishipping Settings]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Options]**.

   ![Leveransalternativ för flera adresser](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Allow Shipping to Multiple Addresses]** till `Yes`.

1. Ange **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]**.

1. Klicka på **[!UICONTROL Save Config]**.

>[!NOTE]
>
>![Adobe Commerce B2B](../assets/b2b.svg) (Adobe Commerce B2B) Betalningsmetoden [Betalning på konto](../b2b/enable-basic-features.md#configure-payment-on-account) är inte tillgänglig under utcheckningen för order med flera leveransadresser, även om den är aktiverad.

## URL:er för e-postleveransspårning

[!BADGE Endast SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce as a Cloud Service-projekt (SaaS-infrastruktur som hanteras av Adobe)."}

[!BADGE Sandbox]{type=Caution tooltip="Objekten i listan är för närvarande bara tillgängliga i sandlådemiljöer. Adobe gör nya releaser tillgängliga i sandlådemiljöer först för att ge dig tid att testa kommande ändringar innan releasen är tillgänglig i produktionsmiljöer."}

Som standard är leveransspårningsnummer som skickas i e-postmeddelanden från kunder oformaterad text. Du kan konvertera spårningsnumren till klickbara länkar genom att aktivera den anpassade spårnings-URL-funktionen. Med den här funktionen kan du definiera en mall för att spåra URL:er för olika fraktfirmor. Varje mall innehåller den fullständiga URL:en till spårningswebbplatsen och en platshållare för spårningsnumret. Commerce ersätter platshållaren med det faktiska spårningsnumret i e-postmeddelandet.

Följande fraktföretag stöds:

- United States Postal Service (USPS)
- United Parcel Service (UPS)
- Federal Express (FedEx)
- DHL Express (DHL)

Så här aktiverar eller redigerar du anpassade spårnings-URL:er:

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_&#x200B;Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Shipping Settings]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Shipment Tracking URLs]**.

1. Ange **[!UICONTROL Enable Custom Tracking URLs]** till `Yes`.

1. Standardmallar för URL:er anges för varje bärare som stöds. Om du behöver ändra något av dessa värden anger du en ny URL-mall i motsvarande fält. Använd `{{tracking_number}}` som platshållare för det faktiska spårningsnumret. Om UPS till exempel ändrar sin URL till `https://www.ups.com/newtracker?tracknumber` kan den nya URL-spårningsmallen se ut så här:

   ```text
   https://www.ups.com/newtracker?tracknumber={{tracking_number}}
   ```

1. Klicka på **[!UICONTROL Save Config]**.
