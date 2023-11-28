---
title: Leverans i butik
description: Lär dig hur du ställer in ett leveransalternativ för din butik.
exl-id: bd64b110-5c39-41c6-8a0c-38561b2a5bf4
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Leverans i butik

Med leveransmetoden i butik kan kunden välja en källa som ska användas som hämtningsplats under utcheckningen.

![Leveranssätt i butik vid utcheckning](./assets/luma-in-store-example.png){width="700" zoomable="yes"}

Vid utcheckning av butiken:

1. Kunden klickar **[!UICONTROL Pick In Store]** eller markerar _[!UICONTROL In-Store Pickup Delivery]_leveranssätt.
1. The _[!UICONTROL Pick In Store]_utcheckningsfliken öppnas.

När kunden har en adress eller tidigare fyllt i leveransadressformuläret innan han/hon byter till _[!UICONTROL Pick In Store]_tab:

- Den närmaste källan till kundadressen inom den konfigurerade radien väljs automatiskt som hämtningsbutik.
- När kunden klickar **[!UICONTROL Select Other]**, _[!UICONTROL Select Store]_sökformuläret öppnas. Endast butiker inom det konfigurerade avståndet (radien) till det förvalda arkivet visas i listan. Alla butiker i listan sorteras efter avståndet till den förvalda butiken.
- När kunden anger ett postnummer eller stadsnamn i sökfältet visas endast butiker inom det konfigurerade avståndet (radien) till den sökta platsen i listan. Alla butiker i listan sorteras efter avståndet till den sökta platsen.
- När kunden rensar postnumret eller stadsnamnet från sökfältet visas alla upphämtningsbutiker som är tilldelade produkterna i kundvagnen för kunden. Alla butiker i listan sorteras i stigande ordning efter källkoderna utan någon begränsning av avståndet (radien).

Om kunden inte har någon adress eller tidigare har fyllt i leveransadressen innan han/hon går till _[!UICONTROL Pick In Store]_tab:

- Sidan visar _Det gick inte att förmarkera hämtningsplatsen baserat på tillgänglig information_ meddelande.
- När kunden klickar **[!UICONTROL Select Store]**, _[!UICONTROL Select Store]_sökformuläret öppnas.
- Alla upphämtningsbutiker som är tilldelade produkterna i kundvagnen visas i stigande ordning med källkoderna utan någon distans (radie) begränsning.
- När kunden anger ett postnummer eller stadsnamn i sökfältet visas endast butiker inom det konfigurerade avståndet (radien) till den sökta platsen i listan. Alla butiker i listan sorteras efter avståndet till den sökta platsen.

## Före konfiguration

- Se till att du har ett lager och en källa som inte är standard. Mer information om hur du konfigurerar en källa som en hämtningsplats finns i [Lägg till en källa](../inventory-management/sources-add.md).
- Kontrollera att du har konfigurerat en algoritm för avståndsprioritet. Mer information finns i [Konfigurera algoritmen för avståndsprioritet](../inventory-management/distance-priority-algorithm.md).
- Se till att du har [hämtat och importerat](../inventory-management/cli.md#import-geocodes) alla nödvändiga geokoder för offlineberäkning.
- Kontrollera att du har konfigurerat [Beräkning av standardskattedestination](../configuration-reference/sales/tax.md#default-tax-destination-calculation) inställningar.

>[!IMPORTANT]
>
>**I butiken filtreras sökresultaten efter avstånd (radie) för att visa relevanta resultat:**<br><br>
>Om kunden har en leveransadress hämtas basplatsen för beräkning av avståndet (radien) från leveransadressen.<br><br>
>Om kunden inte har någon leveransadress hämtas basplatsen för beräkning av avståndet från [Beräkning av standardskattedestination](../configuration-reference/sales/tax.md#default-tax-destination-calculation) inställningar. De här inställningarna anges per butiksvy och du måste konfigurera standardinställningarna för beräkning av skattemål för att se till att hämtningsarkivsökningen fungerar som den ska.

## Ställ in butiksleverans

Kontrollera först att leverans i butik är aktiverat.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Delivery Methods]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL In-Store Delivery]** -avsnitt.

   ![Butiksleverans](../configuration-reference/sales/assets/delivery-methods-in-store-delivery.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enabled]** till `Yes`.

   >[!NOTE]
   >
   >Rensa **[!UICONTROL Use system value]** om du vill ändra standardinställningen för ett fält.

1. Ange **[!UICONTROL Method Name]** som beskriver den beräkningsmetod som används för att göra en leveransuppskattning.

   Metodnamnet visas bredvid den beräknade tariffen i kundvagnen.

1. Ange **[!UICONTROL Title]** som du vill söka efter _Butiksleverans_ under utcheckning.

   Standardtiteln är `In-Store Pickup Delivery`.

1. Om du vill debitera kunder för hämtningstjänsten i butik anger du avgiften i dialogrutan **[!UICONTROL Price]** fält.

1. Ange **[!UICONTROL Search Radius]** i kilometer för butiksupphämtningsplats vid butiksutcheckning.

1. För **[!UICONTROL Displayed Error Message]** anger du det meddelande som visas om leveransen inte är tillgänglig i butiken.

   Standardmeddelandet är `In-Store Delivery is not available. To use this delivery method, please contact us.`

1. Klicka på **[!UICONTROL Save Config]**.
