---
title: "Konfigurera [!DNL Inventory Management]"
description: Lär dig mer om konfigurationen av  [!DNL Inventory Management] alternativ som bestämmer källtillgänglighet, butiksprodukter och orderleverans.
exl-id: 1696999e-77b1-45c7-9b0b-dd1512427cff
feature: Inventory, Configuration
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 0%

---

# Konfigurera [!DNL Inventory Management]

Modulen [!DNL Inventory Management] har stöd för lagerkonfigurationsinställningar på produkt- och global nivå och innehåller även ytterligare inställningar som påverkar källans tillgänglighet, butiksprodukter och orderleverans. Konfigurationsinställningarna gäller för:

- Hela katalogen: Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**. Expandera sedan **[!UICONTROL Catalog]**&#x200B;i den vänstra panelen och välj **[!UICONTROL Inventory]**.

- Särskilda produkter: Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**. Öppna sedan produkten i redigeringsläge och klicka på **[!UICONTROL Advanced Inventory]** i avsnittet _[!UICONTROL Sources]_.

Katalogen kan konfigureras för att visa lagerdata i din butik, hantera aktiva kundvagnar och mycket annat. Visa tillgängligheten för varje artikel som _I Stock_ eller _Utanför lager_ och tillgängligt lager när lagret är lågt.

Gränsen för lagerutfall anger när en produkt ska sorteras om, subtraherar från säljbara kvantiteter för ett lager och kan ställas in på att stödja aktiverade eller inaktiverade efterbeställningar. Tillåt restorder för din butik genom att ange ett maximalt antal order för alla eller specifika produkter.

Ett annat sätt att använda tröskelvärdet för lagertillgänglighet är att hantera produkter som efterfrågas mycket. Om du vill hämta nya kunder, i stället för att sälja till köpare med stora kvantiteter, kan du ange en maximal kvantitet för att hindra en enskild köpare från att ta ut hela lagret.

![Exempel på i Stock, endast 1 vänster](assets/storefront-stock-options-1-left.png)

## Konfigurationsalternativ

[!DNL Commerce] butiker och produkter stöder följande konfigurationer för att hantera produkter, lager, meddelanden med mera. [!DNL Commerce] innehåller ytterligare konfigurationsinställningar för massåtgärder och algoritmen Avståndsprioritet.

| Alternativ | Beskrivning |
|--|--|
| [!UICONTROL Manage Stock] | Gör att [!DNL Commerce] kan hantera allt lager. Ange om lagerkontroll används för den här produkten eller för alla produkter i [!DNL Commerce]. Visar fler alternativ när värdet är `Yes`. |
| [!UICONTROL Only X left Threshold] | Anger en kvantitet som ska meddelas när ett visst belopp finns tillgängligt för inköp. Detta belopp spåras på lagernivå. |
| [!UICONTROL Out-of-Stock Threshold] | Ditt säkerhetslager, antal för att utlösa ett meddelande om att produkten ligger utanför lagret och för att minska risken för utlagring. Det här värdet påverkar bakgrunder. Alternativ:<br />**[!UICONTROL No Backorders]**: Tar inte emot restorder när produkten inte finns i lager.<br />**[!UICONTROL Allow Qty Below 0]**: Accepterar restorder när kvantiteten är under noll.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: Accepterar restorder när kvantiteten är under noll, men meddelar kunderna om att beställningar fortfarande kan göras.<br /><br />**[!UICONTROL Backorders disabled]**: Du bör ange ett positivt värde över 0, till exempel 5 eller 25. <br/>**[!UICONTROL Backorders enabled]**: Ange ett negativt tröskelvärde för den högsta tillåtna kvantiteten för restorder, till exempel -5 eller -25. Värdet 0 fungerar som oändligt lager. Ett positivt värde ignoreras och behandlas som 0. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Anger den minsta kvantiteten av produkten som kan köpas i en enda order. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Anger den maximala kvantiteten av produkten som kan köpas i en enda order. |
| [!UICONTROL Qty Uses Decimals] | Tillåter decimalbelopp i stället för heltal för en produkts kvantitet. Den här inställningen är användbar för produkter som säljs efter vikt, volym eller längd. Anges på Source-nivå, beräknat på Stock-nivå baserat på tilldelade källor. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Avgör om delar av en produkt kan levereras separat. Det här alternativet är synligt när **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Anger om restorder är tillåtna. Anges på Source-nivå, beräknat på Stock-nivå baserat på tilldelade källor. Om det här alternativet är aktiverat för att tillåta restorder rekommenderar vi att du anger ett negativt värde för tröskelvärdet för Ej lagrad (se [Konfigurera restorder](backorders.md)). Alternativ:<br />**[!UICONTROL No Backorders]**: Tar inte emot restorder när produkten inte finns i lager.<br />**[!UICONTROL Allow Qty Below 0]**: Accepterar restorder när kvantiteten är under noll.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: Accepterar restorder när kvantiteten är under noll, men meddelar kunderna om att beställningar fortfarande kan göras. |
| [!UICONTROL Notify for Quantity Below] | Anger den kvantitet som utlöser ett meddelande för Kvantitet under, varningar för lågt lager. Detta belopp dras av från den säljbara kvantiteten, inte från lagerkvantiteten. |
| [!UICONTROL Enable Qty Increments] | Avgör om produkten kan säljas i kvantitetssteg. Om det här alternativet är aktiverat anger du den kvantitet produkter som måste köpas i ett steg. Ökningar anger hur många produktartiklar som måste köpas som en enda produkt och som underordnade till konfigurerbara, grupperade och paketerade produkter. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | [!DNL Inventory Management] använder inte det här värdet. När du slutför en retur eller en kreditnota returneras produktkvantiteten automatiskt till den berörda källkvantiteten. Se [Konfigurera produktalternativ](product-options.md). |

## Återgång och arv för konfigurationsfall

Konfigurationer åsidosätter eller används i följande arvssökväg: Avsnittet Product _[!UICONTROL Sources]_&#x200B;åsidosätter Product&#x200B;_[!UICONTROL Advanced Options]_ global _[!UICONTROL Inventory]_-butikskonfiguration.

När [!DNL Commerce] söker efter anpassade inställningar som ska användas följer den ordningen:

1. Söker efter anpassade inställningar på produktnivå i avsnittet _[!UICONTROL Sources]_. Det finns några tillgängliga inställningar.

1. Kontrollerar inställningarna för produkten _[!UICONTROL Advanced Inventory]_.

1. Om `Use Config Settings` har valts för produktinställningarna söker programmet efter ett värde från den globala konfigurationssidan för _Inventory_.

Du kan t.ex. konfigurera backorder på olika sätt i din butik med en konfiguration som liknar följande:

- _Globalt:_ Aktivera efterbeställningar för butiken, ange Inaktuellt tröskelvärde till `-50`

- _Produkt:_ Inaktivera efterbeställningar för en viss produkt, ange Inaktiverat tröskelvärde till `10`
