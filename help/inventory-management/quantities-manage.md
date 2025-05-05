---
title: Hantera lagerkvantiteter
description: Lär dig hur du tilldelar källor och kvantiteter för nya produkter eller ändrar befintliga produkter.
exl-id: b3d4a4c0-725a-4e62-854f-efb6a5709f73
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Hantera lagerkvantiteter

Följande information beskriver hur du tilldelar källor och kvantiteter för nya produkter eller ändrar befintliga produkter.

Tilldela källor och kvantiteter när du skapar produkter. Mer information finns i [Skapa en produkt](../catalog/product-create.md). Dessa sidor innehåller information om källor och kvantiteter per källa, både från en och flera källor.

När du först får åtkomst till en uppgraderad [!DNL Commerce] med [!DNL Inventory Management] tilldelas alla produkter och kvantiteter till standardversionen av Source. När du importerar nya produkter via en CSV-fil tilldelas de även till standardversionen av Source.

Försäljare med en eller flera källor kan uppdatera källor, lagerkvantiteter och tröskelvärden per produkt eller grupp.

- Försäljare med en enda källa kan uppdatera produktkvantiteter för standardversionen av Source. Denna kvantitet är det totala antalet produkter som är tillgängliga för försäljning.

- Handlare med flera källor kan tilldela flera källor och kvantiteter per produkt för varje plats (lagerställen, butiker, avsändare osv.). Du bör lägga till källor innan du anger produktlagerbelopp.

När du lägger till källor och kvantiteter till dina produkter kan du visa beloppen via produktstödrastret. Om du har ett stort antal källor håller du pekaren över _[!UICONTROL Quantity per Source]_&#x200B;för att se den fullständiga, rullningsbara listan över källor med aktuella kvantiteter.

![Produktkvantiteter per källa](assets/inventory-product-quantity.png){width="600" zoomable="yes"}

Du har följande alternativ för att tilldela lager till produkter:

- [Tilldela källor per produkt](sources-assign-per-product.md) - Tilldela källor manuellt per produkt i katalogen.

- [Tilldela kvantiteter per produkt](quantities-assign-per-product.md) - Lägg till lagerbehållningsbelopp till dina produkter per källa. Den här informationen är specifik för handlare med flera källor.

- [Tilldela och ta bort tilldelning av källor gruppvis](bulk-assignment.md) - Tilldela källor till valda produkter som en massåtgärd. Använd alternativet [Överför lager till Source](inventory-transfer.md) om du vill överföra lager och ta bort källan.

- [Överför lager till Source](inventory-transfer.md) - Massöverföra allt lager från en ursprungskälla till en målkälla.

- [Importera och exportera kvantiteter](inventory-import-export.md) - Använd import- och exportfunktioner för att uppdatera flera produkt-SKU:er med källor och lagerkvantiteter.
