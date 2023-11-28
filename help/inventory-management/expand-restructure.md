---
title: Expandera och strukturera om lager
description: Lär er hur ni kan utöka till en handlare med flera olika källor eller reducera er till en handlare med endast en källkod.
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# Expandera och strukturera om lager

När verksamheten växer och förändras [!DNL Inventory Management] har stöd för dina behov. Ni kan enkelt utöka er till en flerkanalshandlare eller minska er till en enda återförsäljare.

## Expandera till flera källor

Försäljare med en enda källa kan lägga till nya butiker, lagerställen, avsändare och mycket annat. Expandering kräver endast några få tillägg och arkivuppdateringar för att kunna användas med flera olika källor:

1. Lägg till [anpassade källor](sources-add.md) för varje ny plats.

   Du använder bara standardkällan för paketprodukter.

1. Lägg till [anpassade stockar](stocks-add.md) efter behov för era nya källor.

   Du kan till exempel skapa aktier per webbplats, land, språkområde eller andra metoder. Du kan tilldela källor till dina anpassade lager. Du använder bara standardpaketet Stock för programpaket.

1. Uppdatera [källtilldelningar och kvantiteter](quantities-manage.md) för dina produkter.

   Du kan också använda [Verktyget Massåtgärder](bulk-assignment.md) och [Import-export](inventory-import-export.md) för att snabbt lägga till källor och produktdata.

## Strukturera om till en enda källa

För handlare med flera källor som vill minska onlineförsäljningen till en enda plats för leverans kan du ändra källor, lager och kvantiteter som ska uppdateras:

1. Inaktivera [anpassade källor](sources-disable.md).

1. Överför produktlager till standardkällan.

   Vi rekommenderar att du använder massåtgärder. Se [Överför lager till källa](inventory-transfer.md).

1. Tilldela alla webbplatser till [Standardlager](stocks-manage.md).
