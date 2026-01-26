---
title: '[!DNL Commerce] uppgraderingar'
description: Lär dig hur uppgraderingar av Adobe Commerce och Magento Open Source påverkar kataloger och [!DNL Inventory Management] konfigurationer.
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# [!DNL Commerce] uppgraderingar

Om du använde lager med en enda källa i en tidigare version innehåller den här informationen information om nya funktioner och ändringar i din befintliga katalog- och lagerkonfigurationer.

[!DNL Inventory Management] för Adobe Commerce och Magento Open Source innehåller funktioner, förbättringar och utvecklarstöd som förbättrar och uppdaterar all produktarkivhantering och lägger till nya funktioner. Alla funktioner är färdiga, inklusive Source Selection Algorithm och Concurrent Checkout för att matcha orderkvantiteter mot källor och orderleveranser. Beroende på webbplatser, butiker och handelstyp kan du skapa ytterligare lager och källor, tilldela lagerbelopp och mycket annat. Fullständig information finns i [Inventory management](introduction.md).

När du installerar Magento Open Source 2.4.x eller Adobe Commerce 2.4.x sker följande initiala ändringar:

- [Inventory management](enable.md) aktiveras på global butik eller produktnivå. Alternativet Hantera lager aktiverar eller inaktiverar spårning av lagerkvantiteter, beräkningar av aggregerade säljbara kvantiteter och reservationshantering för att spåra inköp till faktura och leverans. Du kan inaktivera det här alternativet om du vill använda en ERP och andra tredjepartstjänster för att hantera lager, order och leveranser. Mer information finns i [!DNL Inventory Management] Moduler nedan.

- Ett [Source](sources-manage.md) och [standardlager](stocks-manage.md) läggs till i systemet. Inaktivera eller ta inte bort dessa standardinställningar. [!DNL Commerce] tilldelar befintliga och nyligen importerade produkter till dessa standardvärden.

  >[!IMPORTANT]
  >
  >Användning av standardlagret och standardversionen av Source rekommenderas inte eftersom de ingår i modulen `CatalogInventory`, som nu är inaktuell. Vi rekommenderar att du skapar och använder anpassade lager och källor i stället.

   - Stock ger en aggregerad virtuell säljbar kvantitet med reservationer för att spåra kundvagnar och order, vilket säkerställer samtidig utcheckning.

   - Alla befintliga produkter i din katalog tilldelas till standardversionen av Source. Produktgränssnittet ändras inte förrän du lägger till nya källor. Om du bara levererar produkter från ett ställe finns det inga andra skillnader mellan källorna. Du kan skapa anpassade [källor](sources-add.md) och [tilldela kvantiteter](quantities-manage.md) per leveransplats.

   - Du kan konfigurera en källa som hämtningsplats och [tilldela kvantiteter](quantities-manage.md) för den källan.

   - Din webbplats tilldelar till standardbutiken. Du kan skapa anpassade [stockar](stocks-add.md) för att ansluta försäljningskanaler (webbplatser) och källor (platser).

- Ytterligare [konfigurationsalternativ](configuration.md) läggs till i dina produkter och den globala butiken. Vissa befintliga konfigurationsalternativ får uppdaterade alternativ och beteenden:

   - Anmäl om kvantitet nedan skickar meddelanden och avdrag från den säljbara kvantiteten.

   - Tröskelvärdet för lagerbrist har stöd för positiva belopp, noll och negativa belopp. När du har aktiverat Restorder ignoreras positiva belopp, som betraktas som noll (eller oändligt).

   - Restorder har stöd för noll (oändligt) och negativa belopp. När alternativet är aktiverat dras inte meddelandet för kvantitet nedan från den säljbara kvantiteten.

- Nya reservationer spårar potentiell försäljning och konverterar till kvantitetsavdrag när ordern levereras. Du får aldrig direkt tillgång till eller kan skapa reservationer. [!DNL Commerce] skapar och hanterar reservationer bakom kulisserna genom order, leveranser och kreditnotor.

- [Beställningar och leveranser](shipments.md) innehåller nya funktioner för att rekommendera leveranser med hjälp av algoritmen Source Selection och stöder partiella leveranser från flera källor för att utföra en beställning.

- Med de nya [import-/exportfunktionerna](inventory-import-export.md) kan du lägga till flera källor, uppdatera lagerkvantiteter och ange lagerstatus (in/ut ur lager) för alla SKU:er i katalogen. Med dessa funktioner kan du ändra för en, vald eller alla källor.

- Nya gruppalternativ på sidan för produktstödraster har stöd för masstilldelning [av och frigör källor](bulk-assignment.md) och [överföring av lager till källa](inventory-transfer.md).

- [!DNL Inventory Management] stöder B2B-kataloger. För närvarande måste alla B2B-produkter tilldelas standardversionen av Source och standardversionen av Stock.

## [!DNL Commerce Order Management] och [!DNL Inventory Management]

[Commerce Order Management (MCOM)](https://commerce-docs.github.io/oms-documentation-archive/) är inte kompatibelt med [!DNL Inventory Management]. När MCOM-modulerna är installerade tillhandahåller de alla lagerhanteringsfunktioner för [!DNL Commerce], inklusive single- och multi-source-hantering, stockar, reservationer med mera. Modulerna [!DNL Inventory Management] är inaktiverade som standard.

MCOM erbjuder omfattande funktioner och tjänster för avancerad flerkanalsbeställningshantering, global lagerhantering och flerleverantörshantering, leverans från butik till lagerställe samt centraliserad kundservice. En fullständig lista över funktioner finns i [MCOM-funktionslistan](https://commerce-docs.github.io/oms-documentation-archive/getting-started/feature-list/).

[!DNL Inventory Management] utökar befintliga [!DNL Commerce]-funktioner med ytterligare alternativ för att spåra pågående order, lagerbehållning, tillgängligt lager för ett lager och API:er för tilläggsutveckling.

## [!DNL Inventory Management] moduler

Du kan inaktivera [!DNL Inventory Management] moduler till:

- Snabba upp uppgraderingen av handlare som för närvarande använder Adobe Commerce eller Magento Open Source 2.0/2.1/2.2/2.3 och gå över till 2.4.x.

- Använd anpassade eller externa lagerhanterings- och orderhanteringsmoduler.

- Använd [!DNL Order Management System] för lagerhantering. Den aktuella kopplingen stöder inte [!DNL Inventory Management]-gränssnitt. För OMS-handlare som uppgraderar till Adobe Commerce 2.4.0 måste de inaktivera dessa moduler.

Fullständig information finns i [Installera och uppdatera](install-update.md).
