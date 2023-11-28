---
title: Avancerade priser
description: Läs mer om de avancerade prissättningsfunktionerna i Adobe Commerce.
exl-id: 0f353341-1b6b-4093-bba9-4a1b88323f8a
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 0%

---

# Avancerade priser

Adobe Commerce och Magento Open Source har stöd för olika prisalternativ som du kan använda för kampanjer eller för att uppfylla tillverkarens minimikrav på annonserad prissättning. Ändringar av produktpriserna kan göras enligt schema eller efter prisregel som tillämpas på produktnivå eller i kundvagnen.

Hantera priser för era produkter med avancerade priser för att erbjuda kunderna bättre priser som uppmuntrar kunderna att spendera mer, driva trafiken till er webbplats och rensa gamla bördor.

The _[!UICONTROL Advanced Pricing]_-inställningarna definierar villkoren för specialpriser som är tillgängliga för en viss kundgrupp eller delad katalog. Avancerade priser kan tillämpas på enkla, virtuella, nedladdningsbara och paketbaserade produkter. Använd en [katalogprisregel](../merchandising-promotions/price-rules-catalog.md). Mer information finns i [Prisomfång](catalog-price-scope.md).

Avancerade prisuppgifter synkroniseras med produktsidor. Om du till exempel uppdaterar en nivåpriskvantitet uppdateras värdet på produktsidan.

![B2B för Adobe Commerce](../assets/b2b.svg) (Tillgängligt med [B2B för Adobe Commerce](./b2b/../introduction.md) endast) Om du använder delade kataloger synkroniseras avancerade prisdata med både produktsidor och delade kataloger. Om du till exempel uppdaterar en nivåpriskvantitet uppdateras värdet i den delade katalogen och på produktsidan. Alla anpassade priser som anges i den delade katalogen har prioritet framför kundgruppspriserna. Se även [Ange priser och struktur för delade kataloger](https://experienceleague.adobe.com/docs/commerce-admin/b2b/shared-catalogs/define/catalog-shared-pricing-structure.html) i _Handbok för B2B for Adobe Commerce_.

![Avancerade priser](./assets/product-pricing-advanced-link.png){width="600" zoomable="yes"}

## Få tillgång till de avancerade prisalternativen

1. Öppna produkten i redigeringsläge.

1. Under **[!UICONTROL Price]**, klicka **[!UICONTROL Advanced Pricing]**.

1. Följ instruktionerna för den typ av avancerad prissättning som behövs.

   - [Grupppris](product-price-group.md)

   - [Specialpris](product-price-special.md)

   - [Pris](product-price-tier.md)

   - [Lägsta kampanjpris](product-price-minimum-advertised.md)

## Sidreferens

### [!UICONTROL Special Price]

Om du vill erbjuda ett rabatterat pris under en viss tidsperiod eller en schemalagd kampanj anger du specialpriset. När ett specialpris finns tillgängligt stryks detaljhandelspriset över och specialpriset visas nedan i stor, fetstil.

#### [!UICONTROL Special Price From] datum

{{ce-feature}}

| Fält | Beskrivning |
| ---- | ----------- |
| [!UICONTROL From] | Anger det första datum då specialpriset är tillgängligt. Du kan antingen ange datumet eller välja det i kalendern. |
| [!UICONTROL To] | Anger det sista datum då specialpriset är tillgängligt. Du kan antingen ange datumet eller välja det i kalendern. |

{style="table-layout:auto"}

### [!UICONTROL Cost]

Ange den faktiska kostnaden för artikeln.

### [!UICONTROL Customer Group Price]

![Avancerade priser](./assets/product-pricing-advanced-group-price.png){width="600" zoomable="yes"}

Ställ in kampanjpriser och nivåpriser för specifika kundgrupper.

| Objekt | Beskrivning |
| ---- | ----------- |
| [!UICONTROL Website] | Identifierar webbplatsen där gruppprisregeln gäller. Det här alternativet visas bara om installationen har flera webbplatser. |
| [!UICONTROL Customer Group] | (Obligatoriskt) Identifierar kundgruppen som är berättigad att ta emot rabattpriset. När ett värde i ett grupp- eller katalogfält ändras tas motsvarande anpassade prisrad som matchar den tidigare inställningen bort från den delade katalogen. <br/>**[!UICONTROL ALL GROUPS]**- Tillämpar regeln på alla kundgrupper.<br/>**[!UICONTROL NOT LOGGED IN]** - Använder regelgäster och kunder som inte är inloggade på sina konton. |
| [!UICONTROL Quantity] | Anger den kvantitet som krävs för att ta emot ett nivåpris. |
| [!UICONTROL Price] | (Obligatoriskt) Anger ett fast eller rabatterat produktpris för medlemmar i kundgruppen inom den specifika webbplatsen. Alternativ: <br/>**[!UICONTROL Fixed]**- (Standard) Rabattpriset anges som ett fast decimalvärde. Skriv till exempel `9.99` som rabattpris.<br/>**[!UICONTROL Discount]** - Rabattpriset anges som en procentandel (%) av basproduktpriset. Skriv till exempel `10` till 10 % rabatt. |
| ![Papperskorgsikon](../assets/icon-delete-trashcan-solid.png) | Tar bort den aktuella regeln. |
| **[!UICONTROL Add]** | Infogar en ny rad för en ny regel. |

{style="table-layout:auto"}

### [!UICONTROL Catalog and Tier Price]

Ställ in kampanjpriser och nivåpriser för specifika delade kataloger och kundgrupper.

{{b2b-feature}}

![Avancerade priser för B2B-butiker med delade kataloger](./assets/product-pricing-advanced.png){width="600" zoomable="yes"}

| Objekt | Beskrivning |
|----|-----------|
| [!UICONTROL Website] | Identifierar webbplatsen där gruppprisregeln gäller. Det här alternativet visas bara om installationen har flera webbplatser. <br>**_Viktigt:_**ALso välj_Webbplats _i [Katalogprisomfång](catalog-price-scope.md) konfiguration, annars visas de angivna avancerade priserna för**alla **webbplatser. |
| [!UICONTROL Group or Catalog] | (Obligatoriskt) Identifierar den kundgrupp eller delade katalog som berättigar till rabatt. När ett värde i ett grupp- eller katalogfält ändras tas motsvarande anpassade prisrad som matchar den tidigare inställningen bort från den delade katalogen. <br/>**[!UICONTROL ALL GROUPS]**- Tillämpar regeln på alla kundgrupper. Värdet används inte i den delade katalogen och ändringar i avancerade prisdata synkroniseras inte med den delade katalogen.<br/>**[!UICONTROL NOT LOGGED IN]** - Använder regelgäster och kunder som inte är inloggade på sina konton.<br/>**[!UICONTROL Shared Catalogs]**- Tillämpar regeln på en viss delad katalog. |
| Kvantitet | Anger den kvantitet som krävs för att ta emot ett nivåpris. |
| [!UICONTROL Price] | (Obligatoriskt) Anger ett fast eller rabatterat produktpris för medlemmar i kundgruppen inom den specifika webbplatsen. Alternativ: <br/>**[!UICONTROL Fixed]**- (Standard) Rabattpriset anges som ett fast decimalvärde. Skriv till exempel `9.99` som rabattpris.<br/>**[!UICONTROL Discount]** - Rabattpriset anges som en procentandel (%) av basproduktpriset. Skriv till exempel `10` till 10 % rabatt. |
| ![Papperskorgsikon](../assets/icon-delete-trashcan-solid.png) | Tar bort den aktuella regeln. |
| **[!UICONTROL Add]** | Infogar en ny rad för en ny regel. |

{style="table-layout:auto"}

### [!UICONTROL Minimum Advertised Price]

Det lägsta annonspriset (MAP) för produkten.

### [!UICONTROL Display Actual Price]

Avgör var det faktiska priset på produkten är synligt för kunden.

| Objekt | Beskrivning |
|----|-----------|
| [!UICONTROL Use Config] | Använder den aktuella konfigurationsinställningen för prisvisningen. |
| [!UICONTROL On Gesture] | Visar det faktiska produktpriset i ett popup-fönster som svar på _Klicka för pris_ eller _Vad är det här?_ länk. |
| [!UICONTROL In Cart] | Visar det faktiska produktpriset i kundvagnen. |
| [!UICONTROL Before Order Confirmation] | Visar det faktiska produktpriset i slutet av utcheckningsprocessen, precis innan ordern skickas. |

{style="table-layout:auto"}
