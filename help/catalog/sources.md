---
title: Produktinställningar - [!UICONTROL Sources]
description: För en produkt är [!UICONTROL Sources] inställningar ger åtkomst till [!DNL Inventory Management] källor som produkten kan distribueras från.
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Produktinställningar - [!UICONTROL Sources]

The _[!UICONTROL Sources]_i produktinställningarna listas de källor som produkten kan distribueras från. Den används för att tilldela och ta bort tilldelningar samt för att hantera kvantitet och tillgänglighet för produkten. Det här avsnittet visas bara om mer än en källa har definierats för din butik. Mer information om källor finns i [Hantera källor](../inventory-management/sources-manage.md).

## Tilldela en källa för en produkt

1. Klicka på **[!UICONTROL Assign Source]**.

1. Markera kryssrutan för de önskade källorna.

1. Klicka på **[!UICONTROL Done]**.

1. Välj **[!UICONTROL Source Item Status]** och anger **[!UICONTROL Qty]** och **[!UICONTROL Notify Qty]** värden efter behov.

1. Klicka **[!UICONTROL Save]** för att spara ändringarna.

![Källvy](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## Fältreferens

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Name] | Det unika namnet för en källa. |
| [!UICONTROL Source Status] | Avgör om produkten är aktiverad eller inaktiverad i katalogen. |
| [!UICONTROL Source Item Status] | Bestämmer produktens aktuella tillgänglighet. Alternativ:<br />**[!UICONTROL In Stock]**- Gör produkten tillgänglig att köpa.<br />**[!UICONTROL Out of Stock]** - Såvida inte restorder aktiveras förhindrar du att produkten kan köpas och tar bort listan från katalogen. |
| [!UICONTROL Qty] | Lagringsbelopp för varje källa. |
| [!UICONTROL Notify Qty] | Ett belopp för _Meddela om kvantitet_ för denna specifika källa om `Notify Quantity Use Default` är inte markerat. |
| [!UICONTROL Notify Qty Use Default] | Anger att standardinställningen för _Meddela om kvantitet_ i produktinställningen Avancerat lager eller global i butikskonfigurationen. Mer information om avancerade lagerinställningar för produkten finns i [Konfigurera avancerade produktalternativ](../inventory-management/product-options.md). |
| [!UICONTROL Actions] | Klicka på för en tilldelad källa **[!UICONTROL Unassign]** för att göra källan inte tillgänglig för produkten. För en ej tilldelad källa klickar du på **[!UICONTROL Assign Sources]** för att göra en källa tillgänglig för produkten. Mer information om [!UICONTROL Assign Sources] alternativ, se [Tilldela källor per produkt](../inventory-management/sources-assign-per-product.md). |

{style="table-layout:auto"}
