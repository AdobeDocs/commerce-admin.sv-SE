---
title: Belöningsbaserade växelkurser
description: Lär dig hur du ställer in belöningsvalutakurserna som bestämmer antalet belöningspoäng som intjänas.
exl-id: 4850d853-fb86-4f64-bfee-47915ea028e2
feature: Rewards, Promotions/Events, Customers
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Belöningsbaserade växelkurser

{{ee-feature}}

Belöningsbaserade valutakurser bestämmer antalet poäng som intjänas baserat på orderbeloppet och värdet av de intjänade poängen. Olika valutakurser kan tillämpas på olika webbplatser och olika kundgrupper. Om flera valutakurser från olika webbplatser och kundgrupper gäller för samma kund gäller följande prioriteringsregler:

## Valutakursprioritet

**1**: Gäller en viss webbplats och en viss kundgrupp.

**2**: Gäller alla webbplatser och en viss kundgrupp.

**3**: Gäller en viss webbplats och alla kundgrupper.

**4**: Gäller alla webbplatser och alla kundgrupper.

När du konverterar valuta till punkter kan antalet punkter inte delas upp. Valutaresten avrundas nedåt. Om till exempel $2.00 konverteras till tio poäng, genereras poäng i grupper om $2.00. Därför skulle en beställning på 7,00 USD ge 30 poäng och de återstående 1,00 USD avrundas nedåt. Orderns penningbelopp definieras som det belopp som handlaren erhåller eller totalsumman minus frakt, moms, rabatter, butikskrediter och presentkort. Poängen intjänas så fort det inte finns några icke fakturerade artiklar i ordern (alla artiklar är antingen betalda eller annullerade). Om en Admin-användare inte vill att kunderna ska kunna få belöningspoäng för annullerade order, kan dessa poäng dras av manuellt från sidan Hantera kunder.

## Ställ in valutakurser

![Belöningsbaserade växelkurser](./assets/reward-exchange-rates.png){width="700" zoomable="yes"}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Reward Exchange Rates]**.

1. Klicka på i det övre högra hörnet **[!UICONTROL Add New Rate]**.

1. I **[!UICONTROL Reward Exchange Rate Information]** gör du följande:

   ![Belöningsvalutakurser - information](./assets/reward-exchange-rate-new.png){width="600" zoomable="yes"}

   - Ange **[!UICONTROL Website]** på de webbplatser där den extra växelkursen tillämpas.

   - Ange **[!UICONTROL Customer Group]** till de grupper där belöningskursen tillämpas.

   - Ange **[!UICONTROL Direction]** till något av följande:

      - `Points to Currency`
      - `Currency to Points`

   För båda riktningsinställningarna representeras beloppet i webbplatsens basvaluta.

1. Ange **[!UICONTROL Rate]** värden enligt _[!UICONTROL Direction]_inställning.

   | Riktning | Kursinställningar |
   |---------|-------------|
   | [!UICONTROL Points to Currency] | I den första _[!UICONTROL Rate]_anger du antalet punkter. I den andra_[!UICONTROL Rate]_ anger du det monetära värdet för poängen. |
   | [!UICONTROL Currency to Points] | I den första  _[!UICONTROL Rate]_anger du det monetära värdet. I den andra_[!UICONTROL Rate]_ anger du antalet punkter som representeras av det monetära värdet. |

   När du konverterar punkter till valuta kan antalet punkter inte delas. Om tio punkter till exempel konverteras till $2.00 måste poäng lösas in i grupper om tio. Därför skulle 25 poäng återbetalas för 4,00 USD, med 5 poäng kvar i kundens saldo.

   Vi rekommenderar att du skapar en konvertering för båda `Points to Currency` och `Currency to Points`.

1. När du är klar klickar du på **[!UICONTROL Save]**.

## Ta bort en belöningsvalutakurs

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Reward Exchange Rates]**.

1. Hitta den belöningsvalutakurs som ska tas bort och öppna den i redigeringsläge.

1. Klicka på **[!UICONTROL Delete]**.

1. Bekräfta åtgärden genom att klicka **[!UICONTROL OK]**.

## Fältbeskrivningar

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Website] | Webbplatserna där belöningspriserna gäller. |
| [!UICONTROL Customer Group] | Kundgrupperna som belöningssatserna gäller för. |
| [!UICONTROL Direction] | Avgör vilken typ av transaktion valutakursen definierar. Alternativ: <br/>**[!UICONTROL Points to Currency]**- Definierar antalet poäng som kan användas som kredit i förhållande till orderbeloppet. I den första _[!UICONTROL Rate]_anger du antalet punkter. I den andra_[!UICONTROL Rate]_ anger du det monetära värdet för poängen.<br/>**[!UICONTROL Currency to Points]** - Definierar beloppet för en order som kan tjäna kundpoäng. I den första  _[!UICONTROL Rate]_anger du det monetära värdet. I den andra_[!UICONTROL Rate]_ anger du antalet punkter som representeras av det monetära värdet. |
