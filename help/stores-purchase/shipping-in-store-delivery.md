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

![Leveransmetod i butik vid utcheckning](./assets/luma-in-store-example.png){width="700" zoomable="yes"}

Vid utcheckning av butiken:

1. Kunden klickar på **[!UICONTROL Pick In Store]** eller väljer leveransmetoden _[!UICONTROL In-Store Pickup Delivery]_.
1. Utcheckningsfliken _[!UICONTROL Pick In Store]_&#x200B;öppnas.

När kunden har en adress eller tidigare fyllt i leveransadressformuläret innan han/hon växlar till fliken _[!UICONTROL Pick In Store]_:

- Den närmaste källan till kundadressen inom den konfigurerade radien väljs automatiskt som hämtningsbutik.
- När kunden klickar på **[!UICONTROL Select Other]** öppnas sökformuläret _[!UICONTROL Select Store]_. Endast butiker inom det konfigurerade avståndet (radien) till det förvalda arkivet visas i listan. Alla butiker i listan sorteras efter avståndet till den förvalda butiken.
- När kunden anger ett postnummer eller stadsnamn i sökfältet visas endast butiker inom det konfigurerade avståndet (radien) till den sökta platsen i listan. Alla butiker i listan sorteras efter avståndet till den sökta platsen.
- När kunden rensar postnumret eller stadsnamnet från sökfältet visas alla upphämtningsbutiker som är tilldelade produkterna i kundvagnen för kunden. Alla butiker i listan sorteras i stigande ordning efter källkoderna utan någon begränsning av avståndet (radien).

Om kunden inte har någon adress eller tidigare har fyllt i leveransadressformuläret innan han/hon växlar till fliken _[!UICONTROL Pick In Store]_:

- Sidan visar _Det gick inte att välja hämtningsplats i förväg baserat på det tillgängliga informationsmeddelandet_.
- När kunden klickar på **[!UICONTROL Select Store]** öppnas sökformuläret _[!UICONTROL Select Store]_.
- Alla upphämtningsbutiker som är tilldelade produkterna i kundvagnen visas i stigande ordning med källkoderna utan någon distans (radie) begränsning.
- När kunden anger ett postnummer eller stadsnamn i sökfältet visas endast butiker inom det konfigurerade avståndet (radien) till den sökta platsen i listan. Alla butiker i listan sorteras efter avståndet till den sökta platsen.

## Före konfiguration

- Se till att du har ett lager och en källa som inte är standard. Mer information om hur du konfigurerar en källa som hämtningsplats finns i [Lägg till en källa](../inventory-management/sources-add.md).
- Kontrollera att du har konfigurerat en algoritm för avståndsprioritet. Mer information finns i [Konfigurera prioritetsalgoritmen för avstånd](../inventory-management/distance-priority-algorithm.md).
- Kontrollera att du har [hämtat och importerat](../inventory-management/cli.md#import-geocodes) alla nödvändiga geokoder för offlineberäkning.
- Kontrollera att du har konfigurerat inställningarna för [Standardberäkning av skattemål](../configuration-reference/sales/tax.md#default-tax-destination-calculation).

>[!IMPORTANT]
>
>**I butiken filtreras sökresultaten efter avstånd (radie) för att visa relevanta resultat:**<br><br>
>Om kunden har en leveransadress hämtas basplatsen för beräkning av avståndet (radien) från leveransadressen.<br><br>
>Om kunden inte har någon leveransadress hämtas basplatsen för att beräkna avståndet från inställningarna för [Standardberäkning av momsmål](../configuration-reference/sales/tax.md#default-tax-destination-calculation). De här inställningarna anges per butiksvy och du måste konfigurera standardinställningarna för beräkning av skattemål för att se till att hämtningsarkivsökningen fungerar som den ska.

## Ställ in butiksleverans

Kontrollera först att leverans i butik är aktiverat.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Delivery Methods]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL In-Store Delivery]**.

   ![Butiksleverans](../configuration-reference/sales/assets/delivery-methods-in-store-delivery.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enabled]** till `Yes`.

   >[!NOTE]
   >
   >Om det behövs avmarkerar du kryssrutan **[!UICONTROL Use system value]** för att ändra standardinställningen för ett fält.

1. Ange **[!UICONTROL Method Name]** som beskriver den beräkningsmetod som används för att skapa en leveransuppskattning.

   Metodnamnet visas bredvid den beräknade tariffen i kundvagnen.

1. Ange den **[!UICONTROL Title]** som du vill ska visas för avsnittet _Butiksleverans_ vid utcheckning.

   Standardtiteln är `In-Store Pickup Delivery`.

1. Om du vill debitera kunder för hämtningstjänsten i butiken anger du avgiften i fältet **[!UICONTROL Price]**.

1. Ange **[!UICONTROL Search Radius]** i kilometer för sökningen efter lagringsplats vid utcheckningen av butiken.

1. För **[!UICONTROL Displayed Error Message]** anger du det meddelande som visas om leveransen i butiken inte är tillgänglig.

   Standardmeddelandet är `In-Store Delivery is not available. To use this delivery method, please contact us.`

1. Klicka på **[!UICONTROL Save Config]**.
