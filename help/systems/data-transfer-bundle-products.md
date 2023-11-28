---
title: Importera paketprodukter
description: Granska ett exempel på hur du importerar produktdata för en paketprodukt.
exl-id: 52146979-9911-449b-9f14-54377e2ae9f4
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%

---

# Importera paketprodukter

En paketprodukt innehåller ett urval av artiklar och ger kunderna möjlighet att välja vilka de vill köpa. Alla objekt som utgör ett paket finns i katalogen som antingen [Enkla produkter](../catalog/product-create-simple.md) eller [Virtuella produkter](../catalog/product-create-virtual.md). Vanligtvis skapas och uppdateras paketprodukter från administratören. Du kan dock även importera data för att skapa en paketprodukt eller exportera befintliga paketprodukter, redigera data och importera dem tillbaka till katalogen. Sprite Yoga Companion Kit är en paketprodukt i exempeldata som används i följande exempel.

![Paketprodukt](../catalog/assets/product-bundle.png){width="700" zoomable="yes"}

## Ändra ordningen på paketobjekt

Det finns två sätt att ändra ordning på objekten i en paketprodukt.

### Metod 1: Dra och släpp

När du arbetar med en [Paket](../catalog/product-create-bundle.md) från administratören kan du dra och släppa objekt och avsnitt på plats.

![Paketera objekt](../catalog/assets/product-bundle-items-move.png){width="600" zoomable="yes"}

### Metod 2: Redigera produktdata

Det bästa sättet att förstå strukturen hos en paketprodukt är att exportera produkten och undersöka data i ett kalkylblad. Du kan ändra ordningen på paketobjekt genom att exportera produkten och lägga till en positionsparameter till data för varje objekt. Objektdata finns i `bundle_values` den exporterade produktens kolumn. När de öppnas i ett kalkylblad finns alla objekt som är kopplade till produkten i en enda cell som en lång textsträng. The `bundle_values` kolumnen innehåller följande element för varje objekt:

- Namn på artikelavsnittet
- Indatakontroll
- Indikator för obligatorisk artikel
- SKU
- Färg
- Pris
- Indikator för standardalternativ
- Standardkvantitet
- Pristyp
- Redigerbar kvantitetsindikator

#### Steg 1: Exportera paketprodukten

I det här steget exporteras Sprite Yoga Companion Kit som en ([CSV](data-csv.md) -fil. Du kan använda vilken paketprodukt som helst som finns i katalogen.

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Under _Exportinställningar_, ange **[!UICONTROL Entity Type]** till `Products`.

1. I listan över produktattribut bläddrar du nedåt till **[!UICONTROL SKU]** och ange SKU:n för den paketprodukt som du vill exportera.

   SKU:n `24-WG080` för produkten i detta exempel.

1. Rulla ned till avsnittets nederkant och klicka **[!UICONTROL Continue]**.

1. I _[!UICONTROL Action]_kolumn i_[!UICONTROL File name]_ stödraster, klicka **[!UICONTROL Select]** och välja `Download`.

   Filen visas på den hämtningsplats som används i webbläsaren.

#### Steg 2: Redigera data

1. Öppna den hämtade CSV-filen i ett kalkylblad.

1. Rulla längst till höger tills du ser `bundle_values` kolumn.

   I `bundle_values` data avgränsas varje element med kommatecken, och varje källobjekt separeras från nästa med ett lodrätt streck. (Det sista objektet avslutas inte med ett lodrätt streck.) Dina exporterade paketdata ska se ut som i följande exempel:

   ![Paketvärden](./assets/product-bundle-values-export-data.png){width="600" zoomable="yes"}

1. Om du vill göra det enklare att redigera kan du kopiera `bundle_values` data och klistra in dem i en textredigerare. Lägg sedan till en radbrytning efter varje objekt så att varje objekt finns på en separat rad.

1. Ta bort radbrytningarna och klistra in redigerade data i `bundle_values` kolumn.

   På följande bild är `position=[number]` parametern läggs till i varje yogastam för att ändra ordningen på objekten i butikslistan.

   ![Positionsparameter](./assets/product-bundle-values-position-parameter.png){width="500" zoomable="yes"}

1. När du har redigerat data **[!UICONTROL Save]** CSV-filen.

#### Steg 3: Importera den uppdaterade produkten

1. På _Administratör_ sidebar, gå till **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Under _[!UICONTROL Import Settings]_, ange **[!UICONTROL Entity Type]**till `Products`.

1. Ange **[!UICONTROL Import Behavior]** till `Replace`.

   Det här alternativet skriver över tidigare data för paketprodukten, i stället för att lägga till ändringarna som ytterligare objekt.

1. Bläddra nedåt till _Fil att importera_ och klicka **[!UICONTROL Choose File]**.

1. Markera CSV-filen som du redigerade.

1. Klicka **[!UICONTROL Check Data]** och vänta en stund på att data ska kontrolleras.

1. Om filen är giltig klickar du på **[!UICONTROL Import]**.

1. När processen är klar går du till **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**och klicka **[!UICONTROL Flush Cache Storage]**.

   Detta garanterar att den uppdaterade produkten finns omedelbart tillgänglig i butiken.
