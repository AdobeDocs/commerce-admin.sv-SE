---
title: Lager och källor
description: Lär dig mer om förhållandet mellan produkter, källor och lager.
exl-id: 01bbbd82-898b-4757-ab40-0d8b89ec59bc
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Lager och källor

Hantera ert lager oavsett lagerställe, typ av produkt eller tjänst eller försäljningskanal. Fyll i order och leverera produkter från olika lagerställen, butiker, distributionscentra och droppleveransställen och slutför beställningar med fokus på balanserat lager, fraktkostnader med mera.

Dessa beskrivningar omfattar produkter, källor och lager för ett cykelföretag med flera leveransställen och webbplatser i USA och Europa.

## Källor

[Källor](sources-manage.md) är de fysiska platser där produktlager hanteras och skickas för orderleverans eller där tjänster är tillgängliga. De här platserna kan vara lagerlokaler, butiker, distributionscentraler och lossningsplatser. [!DNL Commerce] använder kvantiteter och försäljningsbara kvantiteter per lager och hanterar lagerbelopp automatiskt för hanterade produkter och order. Om du har en källa kan du använda läget _En källa_. Om du har flera källor beaktas du i läget _flera källor_.

En källa kan ha prioritet i lagrets omfattning, men inte nödvändigtvis i alla lager, eftersom källan kan återanvändas i olika lager. Antalet lager och källor ökar komplexiteten när det gäller att fastställa det bästa lagret eller den bästa butiken för att utföra en beställning. Du kan t.ex. ha ett begränsat antal produkter som finns att tillgå på din plats för tegelstenar och murbruk med omfattande lager och tjänster på viktiga platser med begränsad tillgänglighet.

I det här exemplet har handlaren en bergscykel tillgänglig för leverans från butiker, lagerlokaler och en droppare.

![Exempel på källdiagram](assets/diagram-sources.png){width="600" zoomable="yes"}

## Lager

[Stock](stocks-manage.md) representerar en virtuell, aggregerad inventering av produkter som är tillgängliga för försäljning till dina försäljningskanaler (webbplatser). Varje aktie mappar dina försäljningskanaler med källor för tillgängliga lager och säljbara kvantiteter. Beroende på webbplatskonfigurationen kan aktien tilldelas en eller flera försäljningskanaler och källor.

Sales Channeler representerar enheter som säljer ert lager, inklusive webbplatser, butiker, kundgrupper inom B2B och så vidare. Försäljningskanaler kan bara associeras med en Stock. Varje försäljningskanal kan endast ha en enda aktie tilldelad och en enda aktie kan tilldelas till flera webbplatser. Genom Adobe Stock kan du ändra prioriteringen av källor som används vid leveransorder och med [Source Selection Algorithm](selection-reservations.md).

Du börjar med ett standardlager som är tilldelat till standardversionen av Source och din webbplats, som används bäst av handlare med en enda källa. Det är bara standardversionen av Source som kan tilldelas den här versionen. Handlare med flera källor kan skapa anpassade stockar för anpassade källor och webbplatser efter behov.

![Diagram över exempelvis lager för en butik](assets/diagram-stock.png){width="600" zoomable="yes"}

## Produktkvantiteter

Kvantitet är antalet produkter i ditt aktiva lager som är tillgängliga för inköp. Kvantiteten produkter ökar och minskar när du slutför leveranser eller justerar lager. Detta belopp påverkas inte om du lägger till produkter i en kundvagn. Salable Quantity spårar tillgängligheten för produkten för en försäljningskanal och använder även det här värdet för att fastställa tillgängligt lager för inköp. Beroende på antalet källor kan du se och hantera produktkvantiteten för något av följande:

- **Kvantitet** - För handlare med en enda källa spårar kolumnen och värdet _[!UICONTROL Quantity]_mängden tillgängligt lagerutrymme.
- **Kvantitet per Source** - För handlare med flera källor spårar kolumnen och värdena _[!UICONTROL Quantity per Source]_lagerbehållningen som är tillgänglig per plats. Om du lägger till flera källor ersätter det här värdet Kvantitet och visar alla källor och tilldelade kvantiteter.

Reservationer spårar lagerbegäranden för hela shoppingprocessen - lägga till produkter i kundvagnen, slutföra utcheckningen och hantera återbetalningar. För tillgängligt lager och lager reserverar du lagerbelopp per order via utcheckningsprocessen, subtraherat från den försäljningsbara kvantiteten. Reservationer konverteras till kvantitetsavdrag vid fakturering och leverans av produkter.

Försäljningsbar kvantitet beräknar det virtuella lagret för produkter (eller tillgänglighet) med hjälp av konfigurerade tröskelvärden, reserverade eller sålda belopp och kvantiteter per källa. För varje lager har [!DNL Commerce] åtkomst till alla tilldelade källor och aggregerar associerade produktkvantiteter. Med det här basvärdet subtraheras sedan alla reservationsbelopp och tröskelvärdet _[!UICONTROL Notify for Quantity Below]_.

![Beräknar den försäljningsbara kvantiteten för ett lager](assets/diagram-salable-quantity.png){width="600" zoomable="yes"}

## Lagerkonfigurationer

Varje produkt, källa och lager innehåller flera alternativ för att konfigurera för din butik på global nivå, på källnivå, på lager- och produktnivå. En fullständig lista över dessa alternativ finns i [Konfigurera Inventory management](configuration.md).

Följande är viktiga alternativ att förstå för [!DNL Inventory Management]:

- **[!UICONTROL Out-of-Stock Threshold]** - Anger ett belopp som ska subtraheras från ditt försäljningsvärde. Om du aktiverar Restorder dras detta värde inte av från Salable Quantity.
- **[!UICONTROL Backorders]** - Avgör om produkter kan säljas utöver ett nolllager, vilket sparar order tills de återställs. När backorder är aktiverade bör du konfigurera [!UICONTROL Out-of-Stock Threshold].

>[!NOTE]
>
>Tröskelvärdet utanför lagret har stöd för negativa och positiva belopp. Om du aktiverar Restorder anger du det här värdet till ett negativt belopp för det maximala antalet produkter som kan restordnas innan produkten verkligen anses vara utanför lagret.

## Inventory management demo

I den här videon får du lära dig mer om Inventory management källor och resurser:

>[!VIDEO](https://video.tv.adobe.com/v/343748?quality=12&learn=on)
