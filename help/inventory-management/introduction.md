---
title: Introduktion till Inventory management
description: Lär dig hur du använder  [!DNL Inventory Management] funktioner för att hantera lager på flera platser så att  [!DNL Commerce] butiken korrekt återspeglar det fysiska lagret.
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# Introduktion till Inventory management

[!DNL Inventory Management] för [!DNL Commerce] ger dig verktygen för att hantera produktlagret. Handlare med en enda butik till flera lager, butiker, upphämtningsplatser, avsändare med mera kan använda dessa funktioner för att behålla kvantiteter för försäljning och hantera leveranser för att slutföra beställningar. Ni kan spåra era lagerkvantiteter, tillhandahålla korrekta försäljningsbara lagerbelopp till kunder för alla era webbplatser och leverera enligt rekommendationer baserat på avstånd eller prioritet. Du kan också konfigurera dina önskade produktkonfigurationer globalt (för alla butiker och produkter), per källa och per produkt. De här funktionerna växer i takt med din verksamhet, så att du kan arbeta från ett enda lagerställe eller ett komplext leveransnätverk med några ytterligare inställningar.

[!DNL Inventory Management] funktioner:

- Olika konfigurationer för handlare vars lager kommer från en enda källa och från flera källor
- Lager för att spåra tillgängliga aggregerade kvantiteter via tilldelade källor
- Samtidiga utcheckningsskydd
- Leveransmatchningsalgoritmer

>[!NOTE]
>
>Dessa funktioner utvecklades som en del av [Inventory management](https://github.com/magento/inventory)-projektet (tidigare MSI) via Community Engineering-programmet.<br/>
>
>Modulen [!DNL Inventory Management] installeras med Magento Open Source och Adobe Commerce, med alla funktioner aktiverade som standard. Mer information om ändringar i modulreleaser finns i [Versionsinformation](release-notes.md).

## Grundläggande terminologi

Det är viktigt att du förstår följande termer när du arbetar med [!DNL Inventory Management]:

[!UICONTROL **Källor**] representerar fysiska platser där tillgängliga produkter lagras och levereras. De här platserna kan vara lagerlokaler, butiker, distributionscentraler och lossningsplatser. (Alla platser kan anges som en källa för virtuella produkter.)

[!UICONTROL **Lager**] mappar en försäljningskanal (som för närvarande är begränsad till webbplatser) till källplatser och lagerbehållning. En aktie kan mappas till flera försäljningskanaler, men en försäljningskanal kan bara tilldelas en aktie.

[!UICONTROL **Aggregerad försäljningsbar kvantitet**] är det totala virtuella lagret som kan säljas via en försäljningskanal. Beloppet beräknas för alla källor som är tilldelade till ett lager.

[!UICONTROL **Reservationer**] spårar avdrag från den försäljningsbara kvantiteten när kunder lägger till produkter i kundvagnen och slutför utcheckningen. När en order levereras rensas och dras de levererade beloppen från specifika lagerkvantiteter av reservationen.
