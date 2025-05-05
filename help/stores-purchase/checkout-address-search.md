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

När den här funktionen är aktiverad och kundens antal sparade adresser uppfyller eller överskrider den konfigurerade gränsen visas endast en adress i stegen _Leverans_ och _Granska och betalningar_ (standard). Kunden kan ändra den valda adressen genom att klicka på **Ändra adress** och sedan söka efter rätt adress efter ort, stat, gata eller postnummer. Den här funktionen stöder även adressval för utcheckning av presentregister.

![Utcheckning med sparade leveransadresser visas](./assets/storefront-checkout-address-search.png){width="700" zoomable="yes"}

Om kunden inte har någon standardleveransadress visas sidan _Leverans_ _Ingen adress vald_. I så fall måste kunden klicka på **Ändra adress** för att välja en sparad adress eller klicka på **Ny adress** för att lägga till och välja en adress innan utcheckningen fortsätter. Om kunden inte har någon standardfaktureringsadress visar sidan _Granska och betala_ den adress som valts för leverans tillsammans med alternativet _Ändra adress_.

![Utcheckning utan vald adress, meddelande](./assets/storefront-checkout-address-search-no-default.png){width="600" zoomable="yes"}

## Låst adresssökning efter citattecken

![Adobe Commerce B2B](../assets/b2b.svg) (endast tillgängligt med Adobe Commerce B2B)

Om du aktiverar adresssökning påverkas även utcheckningen av order som skapas från offerter där kundens antal sparade adresser uppfyller eller överskrider den konfigurerade gränsen. När offerten är klar och kunden går vidare till kassan visas endast den valda leveransadressen. På sidan visas också ett meddelande om att leveransadressen är låst och endast kan ändras i offerten.

![Leveransadressen är låst för en offert](./assets/quote-checkout-shipping-address-locked.png){width="600" zoomable="yes"}

## Aktivera adresssökning

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Checkout]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Checkout Options]**.

   ![Konfiguration - utcheckningsalternativ](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

   En detaljerad beskrivning av de här konfigurationsinställningarna finns i [Utcheckningsalternativ](../configuration-reference/sales/checkout.md#checkout-options) i _referenshandboken för konfiguration_.

1. Ange **[!UICONTROL Enable Address Search]** till `Yes`.

1. Ange alternativet **[!UICONTROL Number of Customer Addresses Limit]** om du vill ange tröskelvärdet för att inkludera adresssökningsfunktionen.

   Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för att göra den här ändringen.

   När kundens antal sparade adresser uppfyller eller överskrider denna gräns visas antingen standardadressen (om kunden har en) eller _Ingen adress vald_ med alternativet _Ändra adress_. Standardgränsen är `10`.

1. Klicka på **[!UICONTROL Save Config]**.
