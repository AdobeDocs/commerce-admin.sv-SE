---
title: Fri frakt
description: Lär dig hur du ställer in ett alternativ för fri frakt för din butik.
exl-id: 3ce69583-0f7f-4c23-b3e3-7d2502bc1bca
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Fri frakt

_Fri frakt_ är en av de mest effektiva erbjudandena. Den kan baseras på ett minimiköp eller konfigureras som en [kundvagnsprisregel](../merchandising-promotions/price-rules-cart.md) som tillämpas när en uppsättning villkor uppfylls. Om båda gäller för samma order har konfigurationsinställningen företräde framför kundvagnsregeln.

>[!NOTE]
>
>Kontrollera din transportföretagskonfiguration för ytterligare inställningar som kan behövas för fri frakt.

## Steg 1: Konfigurera fri frakt

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Delivery Methods]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Free Shipping]**.

   >[!NOTE]
   >
   >Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för att ändra följande inställningar enligt beskrivningen.

1. Ange **[!UICONTROL Enabled]** till `Yes`.

1. För **[!UICONTROL Title]** anger du en titel som identifierar metoden Fri frakt under utcheckningen och en **[!UICONTROL Method Name]** som beskriver den.

1. För **[!UICONTROL Minimum Order Amount]** anger du det minsta totala värdet som berättigar till fri frakt.

   >[!TIP]
   >
   >Om du vill använda fri frakt med [tabellavgifter](shipping-table-rate.md) måste du göra _[!UICONTROL Minimum Order Amount]_så hög att den aldrig uppfylls. Om du använder det här höga värdet hindras fri frakt från att träda i kraft, såvida det inte triggas av en prisregel.

1. Ange **[!UICONTROL Include Tax to Amount]**:

   - `Yes` - Inkluderar moms vid beräkning av minimiorderbelopp (delsumma + moms - rabatt).
   - `No` - Inkluderar inte moms vid beräkning av minimiorderbelopp (delsumma - rabatt).

   ![Fri frakt](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"}

1. För **[!UICONTROL Displayed Error Message]** anger du meddelandet som ska visas om fri frakt inte är tillgänglig.

1. Ange **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda fri frakt.

   - `Specific Countries` - När du har valt det här värdet visas listan _[!UICONTROL Ship to Specific Countries]_. Välj varje land i listan där kostnadsfri frakt kan användas.

1. Ange **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes` - Visar alltid metoden för fri frakt, även om den inte är tillämplig.
   - `No` - Visar metoden för fri frakt endast när det är tillämpligt.

1. För **[!UICONTROL Sort Order]** anger du numret som bestämmer positionen för fri frakt i listan över leveransmetoder vid utcheckning.

   `0` = först, `1` = sekund, `2` = tredje och så vidare.

1. Klicka på **[!UICONTROL Save Config]**.

## Steg 2: Aktivera fri frakt i transportföretagets konfiguration

Se till att du slutför alla konfigurationer som krävs för varje fraktfirma som du tänker använda för fri frakt. Om till exempel din [UPS-konfiguration](ups.md) annars är klar uppdaterar du följande inställningar för att aktivera och konfigurera fri frakt.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL UPS]** i konfigurationen _[!UICONTROL Delivery Methods]_.

1. Ange **[!UICONTROL Free Method]** till `UPS Ground` eller en annan typ som du vill ange för fri frakt.

1. Ange **[!UICONTROL Enable Free Shipping Threshold]** till `Enable` om du vill ha en minimiorder för fri frakt.

   Om du väljer att använda en minimiorder anger du det obligatoriska beloppet för **[!UICONTROL Free Shipping Amount Threshold]**.

1. Klicka på **[!UICONTROL Save Config]**.
