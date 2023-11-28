---
title: Typer av leverantörsförsäljning
description: Lär dig mer om de två källtyperna baserat på antalet platser, eller källor, i ditt företag.
exl-id: ec928929-5826-4504-9fd0-84256b37cb39
feature: Inventory, Products
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Typer av leverantörsförsäljning

[!DNL Commerce] supports [!DNL Inventory Management] för företag av alla storlekar, inklusive en enda butik med en webbplats till ett internationellt nätverk av webbplatser, butiker, lagerställen och avsändare. Alla handlare som använder Adobe Commerce eller Magento Open Source kan indelas i två typer beroende på antalet platser, eller källor, i din verksamhet.

- Försäljare med en enda källa levererar produkter från ett och samma ställe. Du betraktas som en återförsäljare/ett enda källäge tills du börjar lägga till anpassade källor och stockar i installationen.

- Mängdförsäljare levererar produkter från flera källor från mer än en plats, t.ex. tegelhus, lagerlokaler, avsändare och distributionscentraler. När du har lagt till anpassade källor per plats blir du automatiskt en handlare med flera källor.

## Försäljare med en enda källa

Handlare med en enda källa har en enda plats som hanterar lagerbehållning och slutför beställningar. Vanligtvis har du flera webbplatser (eller försäljningskanaler) som säljer produkter från samma katalog, lager och plats.

Du har till exempel en webbplats eller en implementering på flera platser med platser för USA, Tyskland, Frankrike och Brasilien som alla hämtar produkter från ett stort lager. Denna enda källa hanterar alla lagerkvantiteter, leveranser och returer oavsett vilken försäljningskanal som tar emot ordern.

Så här kommer du igång:

- Konfigurera [globala inställningar och produktinställningar](configuration.md) efter behov.

- Uppdatera [Standardkälla](sources-manage.md) med information om din enda lagerplats. Du behöver inte skapa ytterligare källor.

- Uppdatera [Standardlager](stocks-manage.md). Se till att alla dina webbplatser har valts som försäljningskanaler. När du lägger till nya webbplatser [!DNL Commerce] lägger automatiskt till dem i standardlagret. Du behöver inte skapa ytterligare lager.

>[!NOTE]
>
>När verksamheten växer lägger du till ytterligare källor och resurser och uppdaterar [!DNL Inventory Management] för att bli handlare med flera källor. Se [Expandera och strukturera om lager](expand-restructure.md) för all information.

## Handlare med flera källor

Handlare med flera källor har en webbplats eller en implementering av flera platser och hanterar lagerbehållning och orderhantering via flera platser.

Du har till exempel en implementering av flera webbplatser med webbplatser för USA, Tyskland, Frankrike och Brasilien. Ni har flera lagerställen och butiker i dessa länder samt tjänster för leverans av varor som hanterar alla lager- och leveransorder. Dessa platser och webbplatser blir källor och resurser i [!DNL Commerce]. Du kan skapa en stockfil för Amerika och en annan för Europa, och tilldela webbplatser och källor baserat på språkområden och platser. Kunder som köper varje webbplats har endast tillgång till säljbara lager från de tilldelade källorna.

Så här kommer du igång:

- Konfigurera globala inställningar för butikens lager efter behov.

- Lägg till [anpassade källor](sources-add.md) för lagerplatser: lagerställen, butiker, distributionscentraler och avsändare.

- Lägg till [anpassade stockar](stocks-add.md) för varje region för att kartlägga dina webbplatser med flera källor. Sortera om källorna i varje lager i prioritetsordning, vilket är praktiskt när du utför dina beställningar.

- Tilldela källor till produkter och lägg till kvantiteter per plats.

- Slutför eventuella ytterligare konfigurationer per produkt för kvantitetströsklar, restorder osv.
