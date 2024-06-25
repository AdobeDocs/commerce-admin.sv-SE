---
title: "Konfigurera [!DNL Inventory Management]"
description: Läs mer om konfigurationen av [!DNL Inventory Management] alternativ som bestämmer källans tillgänglighet, butiksprodukter och orderleverans.
exl-id: 1696999e-77b1-45c7-9b0b-dd1512427cff
feature: Inventory, Configuration
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 0%

---

# Konfigurera [!DNL Inventory Management]

The [!DNL Inventory Management] modulen har stöd för lagerkonfigurationsinställningar på produkt- och global nivå och innehåller även ytterligare inställningar som påverkar källans tillgänglighet, butiksprodukter och orderleverans. Konfigurationsinställningarna gäller för:

- Hela katalogen: Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**. Expandera sedan **[!UICONTROL Catalog]**i den vänstra panelen och väljer **[!UICONTROL Inventory]**.

- Specifika produkter: Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**. Öppna sedan produkten i redigeringsläge och klicka på **[!UICONTROL Advanced Inventory]** i _[!UICONTROL Sources]_-avsnitt.

Katalogen kan konfigureras för att visa lagerdata i din butik, hantera aktiva kundvagnar och mycket annat. Visa tillgängligheten för varje objekt som _I Stock_ eller _Slut på lager_ och det tillgängliga lagret när lagret är lågt.

Gränsen för lagerutfall anger när en produkt ska sorteras om, subtraherar från säljbara kvantiteter för ett lager och kan ställas in på att stödja aktiverade eller inaktiverade efterbeställningar. Tillåt restorder för din butik genom att ange ett maximalt antal order för alla eller specifika produkter.

Ett annat sätt att använda tröskelvärdet för lagertillgänglighet är att hantera produkter som efterfrågas mycket. Om du vill hämta nya kunder, i stället för att sälja till köpare med stora kvantiteter, kan du ange en maximal kvantitet för att hindra en enskild köpare från att ta ut hela lagret.

![Exempel i Stock, endast 1 vänster](assets/storefront-stock-options-1-left.png)

## Konfigurationsalternativ

[!DNL Commerce] butiker och produkter stöder följande konfigurationer för att hantera produkter, inventering, meddelanden med mera. [!DNL Commerce] innehåller ytterligare konfigurationsinställningar för massåtgärder och algoritmen Avståndsprioritet.

| Alternativ | Beskrivning |
|--|--|
| [!UICONTROL Manage Stock] | Aktiverar [!DNL Commerce] för att hantera allt lager. Ange om lagerkontroll används för den här produkten eller alla produkter i [!DNL Commerce]. Visar fler alternativ när inställningen är `Yes`. |
| [!UICONTROL Only X left Threshold] | Anger en kvantitet som ska meddelas när ett visst belopp finns tillgängligt för inköp. Detta belopp spåras på lagernivå. |
| [!UICONTROL Out-of-Stock Threshold] | Ditt säkerhetslager, antal för att utlösa ett meddelande om att produkten ligger utanför lagret och för att minska risken för utlagring. Det här värdet påverkar bakgrunder. Alternativ:<br />**[!UICONTROL No Backorders]**: Tar inte emot restorder när produkten inte finns i lager.<br />**[!UICONTROL Allow Qty Below 0]**: Accepterar restorder när kvantiteten är under noll.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: Accepterar restorder när kvantiteten är under noll, men meddelar kunderna om att beställningar fortfarande kan göras.<br /><br />**[!UICONTROL Backorders disabled]**: Du bör ange ett positivt värde över 0, till exempel 5 eller 25. <br/>**[!UICONTROL Backorders enabled]**: Ange ett negativt tröskelvärde för högsta tillåtna antal restorder, till exempel -5 eller -25. Värdet 0 fungerar som oändligt lager. Ett positivt värde ignoreras och behandlas som 0. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Anger den minsta kvantiteten av produkten som kan köpas i en enda order. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Anger den maximala kvantiteten av produkten som kan köpas i en enda order. |
| [!UICONTROL Qty Uses Decimals] | Tillåter decimalbelopp i stället för heltal för en produkts kvantitet. Den här inställningen är användbar för produkter som säljs efter vikt, volym eller längd. Anges på källnivå, beräknad på lagernivå baserad på tilldelade källor. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Avgör om delar av en produkt kan levereras separat. Det här alternativet visas när **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Anger om restorder är tillåtna. Anges på källnivå, beräknad på lagernivå baserad på tilldelade källor. Om det här alternativet är aktiverat för att tillåta restorder anger du ett negativt värde för tröskelvärdet för Ej lagrad (se [Konfigurera backorders](backorders.md)) rekommenderas. Alternativ:<br />**[!UICONTROL No Backorders]**: Tar inte emot restorder när produkten inte finns i lager.<br />**[!UICONTROL Allow Qty Below 0]**: Accepterar restorder när kvantiteten är under noll.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: Accepterar restorder när kvantiteten är under noll, men meddelar kunderna om att beställningar fortfarande kan göras. |
| [!UICONTROL Notify for Quantity Below] | Anger den kvantitet som utlöser ett meddelande för Kvantitet under, varningar för lågt lager. Detta belopp dras av från den säljbara kvantiteten, inte från lagerkvantiteten. |
| [!UICONTROL Enable Qty Increments] | Avgör om produkten kan säljas i kvantitetssteg. Om det här alternativet är aktiverat anger du den kvantitet produkter som måste köpas i ett steg. Ökningar anger hur många produktartiklar som måste köpas som en enda produkt och som underordnade till konfigurerbara, grupperade och paketerade produkter. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | [!DNL Inventory Management] använder inte det här värdet. När du slutför en retur eller en kreditnota returneras produktkvantiteten automatiskt till den berörda källkvantiteten. Se [Konfigurerar produktalternativ](product-options.md). |

## Återgång och arv för konfigurationsfall

Konfigurationer åsidosätter eller används i följande arvssökväg: Produkt _[!UICONTROL Sources]_avsnittsåsidosättningar Produkt_[!UICONTROL Advanced Options]_ åsidosätter globalt _[!UICONTROL Inventory]_lagringskonfiguration.

När [!DNL Commerce] söker efter anpassade inställningar som ska användas, följer den här ordningen:

1. Söker efter anpassade inställningar på produktnivå i dialogrutan _[!UICONTROL Sources]_-avsnitt. Det finns några tillgängliga inställningar.

1. Kontrollerar produkten _[!UICONTROL Advanced Inventory]_inställningar.

1. If `Use Config Settings` väljs för produktinställningarna och söker efter ett värde från den globala _Lager_ konfigurationssida för butik.

Du kan t.ex. konfigurera backorder på olika sätt i din butik med en konfiguration som liknar följande:

- _Globalt:_ Aktivera restorder för butiken, ange värdet för Ej lagrad `-50`

- _Produkt:_ Inaktivera restorder för en viss produkt, ange värdet för Ej lagrad till `10`
