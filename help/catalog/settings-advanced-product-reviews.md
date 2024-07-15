---
title: Produktinställningar - [!UICONTROL Product Reviews]
description: För en produkt ger inställningarna för [!UICONTROL Product Reviews] åtkomst till inskickade granskningar för produkten och redigerar statusen för väntande granskningar.
exl-id: 9328c9f5-dcd4-4837-8902-39dc48cb8151
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Produktinställningar - [!UICONTROL Product Reviews]

I avsnittet _[!UICONTROL Product Reviews]_visas alla recensioner som kunder har skickat in om produkten. Det här avsnittet visas med den andra produktinformationen först när en ny produkt har sparats för första gången. Mer information finns i [Produktrecensioner](../merchandising-promotions/product-reviews.md).

![Produktrecensioner](./assets/product-review.png){width="600" zoomable="yes"}

## Fältreferens

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL ID] | Unikt, numeriskt ID genererat för produktgranskningsposten |
| [!UICONTROL Created] | Datum för offentliggörande av översynen |
| [!UICONTROL Status] | Granskningsstatus (`Pending`, `Approved` eller `Not Approved`) |
| [!UICONTROL Title] | Granskningsrubrik |
| [!UICONTROL Nickname] | Smeknamnet på användaren som lämnade granskningen |
| [!UICONTROL Review] | Kundrecension av den aktuella produkten |
| [!UICONTROL Visibility] | Synlighet i butiksgranskningar |
| [!UICONTROL Type] | Typ av användare som lämnade granskningen (`Guest` eller `Customer`) |
| [!UICONTROL Product] | Granskat produktnamn |
| [!UICONTROL SKU] | Den unika Stock Keeping-enheten som är tilldelad produkten |
| [!UICONTROL Action] | Öppnar produkten i redigeringsläge |

{style="table-layout:auto"}

## Moderera recensioner för en viss produkt

1. Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]** på sidofältet _Admin_.

1. Leta reda på produkten och öppna den i redigeringsläge.

1. Bläddra till avsnittet _[!UICONTROL Product Reviews]_.

1. Klicka på **[!UICONTROL Edit]** för en produktgranskning med statusen `Pending` om du vill visa och redigera informationen.

1. Ange status för granskning:

   - Om du vill godkänna en väntande granskning väljer du `Approved`.
   - Om du vill avvisa en granskning väljer du `Not Approved`.
   - Du kan när som helst ändra granskningsstatusen tillbaka till `Pending`.

1. Klicka på **[!UICONTROL Save Review]** när du är klar.

Granskningar med statusvärdena `Pending` och `Not Approved` visas inte i butiken.
