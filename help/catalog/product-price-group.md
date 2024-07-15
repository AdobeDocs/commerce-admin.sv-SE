---
title: Grupppriser
description: Lär dig hur du använder grupppriser för att ange priser för rabatterade artiklar baserat på kundgrupper i din butik.
exl-id: bc5be23f-64eb-47c3-beda-01168abfbf96
feature: Catalog Management, Products, Customers
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---

# Grupppriser

Du kan använda produktkonfigurationsinställningarna i Admin för att ange priser för rabatterade artiklar baserat på kundgrupper i din butik. Den här strategiska prismodellen kallas _grupppriser_.

Det rabatterade priset för valfri produkt kan erbjudas medlemmar i en viss kundgrupp när kunden är inloggad på sitt konto. Kundgruppspriset visas på produktsidan tillsammans med det vanliga priset så att en kund enkelt kan jämföra priser och agera därefter. När de har lagt till produkten i kundvagnen ersätts det ordinarie priset av grupppriset baserat på kundgruppen.

Priset för kundgrupper är en komponent i [nivåindelade priser](product-price-tier.md) och har angetts på ett liknande sätt. Den enda skillnaden är att kundgruppspriserna har en kvantitet på 1.

![Kundgrupprabatt](./assets/storefront-price-group.png){width="600" zoomable="yes"}

## Fördelar med att använda grupppriser

- Lämpligt för grossister

- Kundernas incitament att uppgradera sin kundgrupp för att dra nytta av rabatterna

- Målinriktade marknadsföringskampanjer

- Skapa förtroende och trovärdighet genom att belöna lojala kunder

## Ställ in ett grupppris

1. Öppna produkten i redigeringsläge.

1. Klicka **[!UICONTROL Advanced Pricing]** nedanför fältet _[!UICONTROL Price]_.

1. Klicka på **[!UICONTROL Add]** i avsnittet _[!UICONTROL Customer Group Price]_.

   Om din butik innehåller [Adobe Commerce B2B](../b2b/introduction.md) och har [delade kataloger](../b2b/catalog-shared.md) aktiverat får du den här delen etiketten _[!UICONTROL Catalog and Tier Price]_.

   ![Avancerade priser](./assets/product-price-group.png){width="600" zoomable="yes"}

1. Konfigurera grupppriset:

   - För en installation på flera platser väljer du **[!UICONTROL Website]** där grupppriset gäller.

   - Välj den **[!UICONTROL Customer Group]** som ska få rabatten.

   - Ange **[!UICONTROL Quantity]** av `1`.

   - Ange pristyp och belopp för **[!UICONTROL Price]**:

      - `Fixed` - Ange det rabatterade produktpriset.

      - `Discount` - Ange det rabatterade priset som en procentandel av produktpriset.

     ![Priser för kundgrupp](./assets/product-price-group-discount.png){width="600" zoomable="yes"}

1. Om du vill lägga till ett annat grupppris klickar du på **[!UICONTROL Add]** och upprepar föregående steg.

1. När du är klar klickar du på **[!UICONTROL Done]** och sedan på **[!UICONTROL Save]**.

>[!NOTE]
>
>Det **_slutliga_**-produktpriset beräknas som det **_lägsta_** relevanta priset, med följande formel: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Fast pris_** anpassningsbara produktalternativ _påverkas_ inte av reglerna för grupppris, pris, specialpris eller katalogpris.
