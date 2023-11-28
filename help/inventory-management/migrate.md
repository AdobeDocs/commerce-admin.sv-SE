---
title: '''[!DNL Commerce] uppgraderingar'
description: Se hur uppgraderingar av Adobe Commerce och Magento Open Source påverkar katalogen och [!DNL Inventory Management] konfigurationer.
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# [!DNL Commerce] uppgraderingar

Om du använde lager med en enda källa i en tidigare version innehåller den här informationen information om nya funktioner och ändringar i din befintliga katalog- och lagerkonfigurationer.

[!DNL Inventory Management] för Adobe Commerce och Magento Open Source innehåller funktioner, förbättringar och utvecklarsupport som förbättrar och uppdaterar all produkthantering och lägger till nya funktioner. Alla funktioner är färdiga att användas, inklusive algoritmen för källval och Concurrent Checkout, för att matcha orderkvantiteter mot källor och orderhantering. Beroende på webbplatser, butiker och handelstyp kan du skapa ytterligare lager och källor, tilldela lagerbelopp och mycket annat. Fullständig information finns i [Inventory management](introduction.md).

När du installerar Magento Open Source 2.4.x eller Adobe Commerce 2.4.x sker följande initiala ändringar:

- [Inventory management](enable.md) på global butiks- eller produktnivå. Alternativet Hantera lager aktiverar eller inaktiverar spårning av lagerkvantiteter, beräkningar av aggregerade säljbara kvantiteter och reservationshantering för att spåra inköp till faktura och leverans. Du kan inaktivera det här alternativet om du vill använda en ERP och andra tredjepartstjänster för att hantera lager, order och leveranser. Mer information finns i [!DNL Inventory Management] Moduler nedan.

- A [Standardkälla](sources-manage.md) och [Standardlager](stocks-manage.md) läggs till i systemet. Inaktivera eller ta inte bort dessa standardinställningar. [!DNL Commerce] tilldelar befintliga och nyligen importerade produkter till dessa standardvärden.

  >[!IMPORTANT]
  >
  >Användning av standardlagret och standardkällan rekommenderas inte eftersom de är en del av `CatalogInventory` som nu är inaktuellt. Vi rekommenderar att du skapar och använder anpassade lager och källor i stället.

   - Stock ger en aggregerad virtuell säljbar kvantitet med reservationer för att spåra kundvagnar och order, vilket säkerställer samtidig utcheckning.

   - Alla befintliga produkter i din katalog tilldelas standardkällan. Produktgränssnittet ändras inte förrän du lägger till nya källor. Om du bara levererar produkter från ett ställe finns det inga andra skillnader mellan källorna. Du kan skapa egna [källor](sources-add.md) och [tilldela kvantiteter](quantities-manage.md) per leveransplatse.

   - Du kan konfigurera en källa som hämtningsplats och [tilldela kvantiteter](quantities-manage.md) för den källan.

   - Din webbplats tilldelar till standardbutiken. Du kan skapa egna [lager](stocks-add.md) koppla samman försäljningskanaler (webbplatser) och källor (platser).

- Ytterligare [konfigurationsalternativ](configuration.md) till produkterna och till den globala butiken. Vissa befintliga konfigurationsalternativ får uppdaterade alternativ och beteenden:

   - Anmäl om kvantitet nedan skickar meddelanden och avdrag från den säljbara kvantiteten.

   - Tröskelvärdet för lagerbrist har stöd för positiva belopp, noll och negativa belopp. När du har aktiverat Restorder ignoreras positiva belopp, som betraktas som noll (eller oändligt).

   - Restorder har stöd för noll (oändligt) och negativa belopp. När alternativet är aktiverat dras inte meddelandet för kvantitet nedan från den säljbara kvantiteten.

- Nya reservationer spårar potentiell försäljning och konverterar till kvantitetsavdrag när ordern levereras. Du får aldrig direkt tillgång till eller kan skapa reservationer. [!DNL Commerce] skapar och hanterar reservationer bakom kulisserna genom order, leveranser och kreditnotor.

- [Beställningar och leveranser](shipments.md) innehåller nya funktioner för att rekommendera leveranser med hjälp av algoritmen för källval och stöder partiella leveranser från flera källor för att utföra en beställning.

- Nytt [import-/exportfunktioner](inventory-import-export.md) gör att du kan lägga till flera källor, uppdatera lagerkvantiteter och ange lagerstatus (in/ut ur lager) för alla SKU:er i din katalog. Med dessa funktioner kan du ändra för en, vald eller alla källor.

- Nya gruppalternativ via produktrutnätssidan har stöd för massvis [tilldela och ta bort tilldelning av källor](bulk-assignment.md)och [överföra lager till källa](inventory-transfer.md).

- [!DNL Inventory Management] stöder B2B-kataloger. För närvarande måste alla B2B-produkter tilldelas standardkällan och standardlagret.

## [!DNL Commerce Order Management] och [!DNL Inventory Management]

[Hantering av handelsorder (MCOM)][1] är inte kompatibelt med [!DNL Inventory Management]. MCOM-moduler innehåller alla funktioner för lagerhantering när de är installerade. [!DNL Commerce], inklusive single- och multi-source-hantering, aktier, reservationer med mera. The [!DNL Inventory Management] moduler är inaktiverade som standard.

MCOM erbjuder omfattande funktioner och tjänster för avancerad flerkanalsbeställningshantering, global lagerhantering och flerleverantörshantering, leverans från butik till lagerställe samt centraliserad kundservice. En fullständig lista över funktioner finns i [MCOM - funktionslista][2].

[!DNL Inventory Management] utökar befintlig [!DNL Commerce] funktioner med ytterligare alternativ för att spåra beställningar som är under bearbetning, lagerbehållning, tillgängligt lager för ett lager och API:er för tilläggsutveckling.

## [!DNL Inventory Management] moduler

Du kanske vill inaktivera [!DNL Inventory Management] moduler till:

- Snabba upp uppgraderingen av handlare som för närvarande använder Adobe Commerce eller Magento Open Source 2.0/2.1/2.2/2.3 och gå över till 2.4.x.

- Använd anpassade eller externa lagerhanterings- och orderhanteringsmoduler.

- Använd [!DNL Order Management System] för lagerhantering. Den aktuella kopplingen stöder inte [!DNL Inventory Management] gränssnitt. För OMS-handlare som uppgraderar till Adobe Commerce 2.4.0 måste de inaktivera dessa moduler.

Fullständig information finns på [Installera och uppdatera](install-update.md).

[1]: https://omsdocs.magento.com/
[2]: https://omsdocs.magento.com/en/getting-started/feature-list/
