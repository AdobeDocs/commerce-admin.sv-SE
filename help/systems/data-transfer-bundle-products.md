---
title: Importera paketprodukter
description: Granska ett exempel på hur du importerar produktdata för en paketprodukt.
exl-id: 52146979-9911-449b-9f14-54377e2ae9f4
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 0%

---

# Importera paketprodukter

En paketprodukt innehåller ett urval av artiklar och ger kunderna möjlighet att välja vilka de vill köpa. Alla objekt som utgör ett paket finns i katalogen som antingen [Enkla produkter](../catalog/product-create-simple.md) eller [Virtuella produkter](../catalog/product-create-virtual.md). Vanligtvis skapas och uppdateras paketprodukter från administratören. Du kan dock även importera data för att skapa en paketprodukt eller exportera befintliga paketprodukter, redigera data och importera dem tillbaka till katalogen. Sprite Yoga Companion Kit är en paketprodukt i exempeldata som används i följande exempel.

![Paketprodukt](../catalog/assets/product-bundle.png){width="700" zoomable="yes"}

## Ändra ordningen på paketobjekt

Det finns två sätt att ändra ordning på objekten i en paketprodukt.

### Metod 1: Dra och släpp

När du arbetar med en [paketprodukt](../catalog/product-create-bundle.md) från administratören kan du dra och släppa objekt och avsnitt på plats.

![Paketobjekt](../catalog/assets/product-bundle-items-move.png){width="600" zoomable="yes"}

### Metod 2: Redigera produktdata

Det bästa sättet att förstå strukturen hos en paketprodukt är att exportera produkten och undersöka data i ett kalkylblad. Du kan ändra ordningen på paketobjekt genom att exportera produkten och lägga till en positionsparameter till data för varje objekt. Objektdata finns i kolumnen `bundle_values` för den exporterade produkten. När de öppnas i ett kalkylblad finns alla objekt som är kopplade till produkten i en enda cell som en lång textsträng. Kolumnen `bundle_values` innehåller följande element för varje objekt:

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

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**&#x200B;på sidofältet_ Admin _.

1. Under _Exportinställningar_ anger du **[!UICONTROL Entity Type]** till `Products`.

1. Bläddra nedåt till **[!UICONTROL SKU]** i listan över produktattribut och ange SKU:n för den paketprodukt som du vill exportera.

   SKU är `24-WG080` för produkten i det här exemplet.

1. Bläddra nedåt till avsnittets nederkant och klicka på **[!UICONTROL Continue]**.

1. Klicka på **[!UICONTROL Select]** i kolumnen _[!UICONTROL Action]_&#x200B;i rutnätet&#x200B;_[!UICONTROL File name]_ och välj `Download`.

   Filen visas på den hämtningsplats som används i webbläsaren.

#### Steg 2: Redigera data

1. Öppna den hämtade CSV-filen i ett kalkylblad.

1. Rulla längst till höger tills du ser kolumnen `bundle_values`.

   I `bundle_values`-data avgränsas varje element med kommatecken, och varje paketobjekt separeras från nästa med ett lodrätt streck. (Det sista objektet avslutas inte med ett lodrätt streck.) Dina exporterade paketdata ska se ut som i följande exempel:

   ![Paketvärden](./assets/product-bundle-values-export-data.png){width="600" zoomable="yes"}

1. Om du vill göra det enklare att redigera kan du kopiera `bundle_values`-data och klistra in dem i en textredigerare och sedan lägga till en radbrytning efter varje objekt, så att varje objekt finns på en separat rad.

1. När du har redigerat data tar du bort radbrytningarna och klistrar in redigerade data i kolumnen `bundle_values`.

   På följande bild läggs en `position=[number]`-parameter till i varje yogaband för att ändra ordningen på objekten i butikslistan.

   ![Positionsparameter](./assets/product-bundle-values-position-parameter.png){width="500" zoomable="yes"}

1. **[!UICONTROL Save]** CSV-filen när du har redigerat data.

#### Steg 3: Importera den uppdaterade produkten

1. Gå till **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**&#x200B;på sidofältet_ Admin _.

1. Under _[!UICONTROL Import Settings]_&#x200B;anger du **[!UICONTROL Entity Type]**&#x200B;till `Products`.

1. Ange **[!UICONTROL Import Behavior]** till `Replace`.

   Det här alternativet skriver över tidigare data för paketprodukten, i stället för att lägga till ändringarna som ytterligare objekt.

1. Bläddra ned till avsnittet _Fil att importera_ och klicka på **[!UICONTROL Choose File]**.

1. Markera CSV-filen som du redigerade.

1. Klicka på **[!UICONTROL Check Data]** och vänta en stund på att data ska kontrolleras.

1. Om filen är giltig klickar du på **[!UICONTROL Import]**.

1. När processen är klar går du till **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**&#x200B;och klickar på&#x200B;**[!UICONTROL Flush Cache Storage]**.

   Detta garanterar att den uppdaterade produkten finns omedelbart tillgänglig i butiken.
