---
title: Introduktion till Inventory management
description: Lär dig använda [!DNL Inventory Management] funktioner för att hantera stockbilder på flera platser så att [!DNL Commerce] lagret korrekt återspeglar det fysiska lagret.
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Introduktion till Inventory management

[!DNL Inventory Management] for [!DNL Commerce] ger dig verktygen du behöver för att hantera produktinventeringen. Handlare med en enda butik till flera lager, butiker, upphämtningsplatser, avsändare med mera kan använda dessa funktioner för att behålla kvantiteter för försäljning och hantera leveranser för att slutföra beställningar. Ni kan spåra era lagerkvantiteter, tillhandahålla korrekta försäljningsbara lagerbelopp till kunder för alla era webbplatser och leverera enligt rekommendationer baserat på avstånd eller prioritet. Du kan också konfigurera dina önskade produktkonfigurationer globalt (för alla butiker och produkter), per källa och per produkt. De här funktionerna växer i takt med din verksamhet, så att du kan arbeta från ett enda lagerställe eller ett komplext leveransnätverk med några ytterligare inställningar.

[!DNL Inventory Management] funktioner:

- Olika konfigurationer för handlare vars lager kommer från en enda källa och från flera källor
- Lager för att spåra tillgängliga aggregerade kvantiteter via tilldelade källor
- Samtidiga utcheckningsskydd
- Leveransmatchningsalgoritmer

>[!NOTE]
>
>Dessa funktioner utvecklades som en del av [Inventory management](https://github.com/magento/inventory) (tidigare MSI-projekt) genom gemenskapens tekniska program.<br/>
>
>The [!DNL Inventory Management] -modulen installeras med Magento Open Source och Adobe Commerce, med alla funktioner aktiverade som standard. Information om ändringar i modulreleaser finns i [Versionsinformation](release-notes.md).

## Grundläggande terminologi

Det är viktigt att du förstår följande termer när du arbetar med [!DNL Inventory Management]:

[!UICONTROL **Källor**] representerar fysiska platser som lagrar och levererar tillgängliga produkter. De här platserna kan vara lagerlokaler, butiker, distributionscentraler och lossningsplatser. (Alla platser kan anges som en källa för virtuella produkter.)

[!UICONTROL **Lager**] mappa en försäljningskanal (för närvarande begränsad till webbplatser) till källplatser och lagerbehållning. En aktie kan mappas till flera försäljningskanaler, men en försäljningskanal kan bara tilldelas en aktie.

[!UICONTROL **Sammanställd säljbar kvantitet**] är det totala virtuella lagret som kan säljas via en försäljningskanal. Beloppet beräknas för alla källor som är tilldelade till ett lager.

[!UICONTROL **Reservationer**] spåra avdrag från den säljbara kvantiteten när kunderna lägger till produkter i varukorgar och slutför utcheckning. När en order levereras rensas och dras de levererade beloppen från specifika lagerkvantiteter av reservationen.
