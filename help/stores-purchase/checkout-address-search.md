---
title: Adresssökning vid utcheckning
description: Lär dig hur du inkluderar adresssökning i kassan på din butik.
exl-id: 8153c456-0848-4bb4-8deb-8219323344ed
feature: Checkout
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# Adresssökning vid utcheckning

{{ee-feature}}

Dina kunder kan ha många sparade adresser och information i adressboken, särskilt regelbundet, som returnerar kunder eller företag som gör flera beställningar och leveransställen. Att visa många adresser kan göra att det går långsammare att läsa in checkar ut och att processerna utförs avsevärt, vilket ger en negativ shoppingupplevelse. Vi rekommenderar att du aktiverar och konfigurerar adresssökningen för din webbplats för att öka svarstiden för utcheckning.

>[!NOTE]
>
>Adresssökning är inte aktiverat som standard. Du kan konfigurera den här funktionen så att den inkluderar funktionerna på din webbplats.

När den här funktionen är aktiverad och kundens antal sparade adresser uppfyller eller överskrider den konfigurerade gränsen, är _Leverans_ och _Granska och betala_ visas endast en adress (standard). Kunden kan ändra den valda adressen genom att klicka på **Ändra adress** och söker sedan efter rätt adress efter ort, stat, gata eller postnummer. Den här funktionen stöder även adressval för utcheckning av presentregister.

![Utcheckning med sparade leveransadresser visas](./assets/storefront-checkout-address-search.png){width="700" zoomable="yes"}

Om kunden inte har någon standardleveransadress _Leverans_ sidvisning _Ingen adress har valts_. I så fall måste kunden klicka **Ändra adress** för att välja en sparad adress eller klicka på **Ny adress** för att lägga till och markera en adress innan du fortsätter med utcheckningen. Om kunden inte har någon standardfaktureringsadress visas _Granska och betala_ visas den adress som valts för leverans tillsammans med _Ändra adress_ alternativ.

![Utcheckning utan vald adress](./assets/storefront-checkout-address-search-no-default.png){width="600" zoomable="yes"}

## Låst adresssökning efter citattecken

![Adobe Commerce B2B](../assets/b2b.svg) (Endast för Adobe Commerce B2B)

Om du aktiverar adresssökning påverkas även utcheckningen av order som skapas från offerter där kundens antal sparade adresser uppfyller eller överskrider den konfigurerade gränsen. När offerten är klar och kunden går vidare till kassan visas endast den valda leveransadressen. På sidan visas också ett meddelande om att leveransadressen är låst och endast kan ändras i offerten.

![Leveransadress låst för en offert](./assets/quote-checkout-shipping-address-locked.png){width="600" zoomable="yes"}

## Aktivera adresssökning

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Checkout]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Checkout Options]** -avsnitt.

   ![Konfiguration - Utcheckningsalternativ](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

   En detaljerad beskrivning av de här konfigurationsinställningarna finns i [Utcheckningsalternativ](../configuration-reference/sales/checkout.md#checkout-options) i _Referenshandbok för konfiguration_.

1. Ange **[!UICONTROL Enable Address Search]** till `Yes`.

1. Om du vill ange tröskelvärdet för att ta med adresssökningsfunktionen anger du **[!UICONTROL Number of Customer Addresses Limit]** alternativ.

   Rensa **[!UICONTROL Use system value]** om du vill göra den här ändringen.

   När kundens antal sparade adresser uppfyller eller överskrider denna gräns visas antingen standardadressen (om kunden har en) eller _Ingen adress har valts_ med _Ändra adress_ alternativ. Standardgränsen är `10`.

1. Klicka på **[!UICONTROL Save Config]**.
