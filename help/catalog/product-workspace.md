---
title: Produktarbetsyta
description: Lär dig mer om de inställningar och kontroller som finns på produktarbetsytan.
exl-id: 8258b117-56d2-4d5f-9413-80d51fd5eae6
feature: Catalog Management, Products, Admin Workspace
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---

# Produktarbetsyta

Produktarbetsytan är i stort sett densamma för alla produkttyper, även om urvalet av fält ändras beroende på vilken attributuppsättning som används. Produktattributen är överst i formuläret, följt av expanderbara avsnitt av produktinformationen. När en ny produkt sparas för första gången _[!UICONTROL Store View]_En väljare visas längst upp till vänster i formuläret.

![Produktarbetsyta](./assets/product-workspace-ee.png){width="700" zoomable="yes"}

## [!UICONTROL Enable Product] inställning

Produktens onlinestatus anges av väljaren högst upp i formuläret. Om du vill ändra onlinestatus anger du **[!UICONTROL Enable Product]** växla till `Yes` eller `No`.

| Kontroll | Beskrivning |
|-------- | ----------- |
| ![Växla ja](../assets/toggle-yes.png) | Anger att produkten är online. |
| ![Växla inte](../assets/toggle-no.png) | Anger att produkten är offline. |

{style="table-layout:auto"}

## Attributuppsättning

Namnet på [attributuppsättning](attribute-sets.md) visas i det övre vänstra hörnet och avgör vilka fält som visas i produktposten. Om du vill välja en annan attributuppsättning klickar du på nedpilen bredvid standardnamnet för attributuppsättningen.

![Attributuppsättning](./assets/product-attribute-set.png){width="600" zoomable="yes"}

## Expandera/komprimera

Om du vill expandera eller komprimera ett avsnitt klickar du på antingen Expandera ![Expansionsväljare](../assets/icon-display-expand.png) eller komprimera ![Komprimera väljare](../assets/icon-display-collapse.png) -ikon.

## [!UICONTROL Save] meny

The _[!UICONTROL Save]_-menyn innehåller flera alternativ som du kan använda för att spara och fortsätta, spara och skapa en produkt, spara och duplicera produkten eller spara och stänga.

![Spara-menyn](./assets/product-save-menu.png){width="600" zoomable="yes"}

| Kommando | Beskrivning |
|--- |--- |
| [!UICONTROL Save] | Spara den aktuella produkten och fortsätt arbeta. |
| [!UICONTROL Save & New] | Spara och stäng den aktuella produkten och påbörja en ny produkt som baseras på samma produkttyp och mall. |
| [!UICONTROL Save & Duplicate] | Spara och stäng den aktuella produkten och öppna en ny kopia. |
| [!UICONTROL Save & Close] | Spara den aktuella produkten och gå tillbaka till _[!UICONTROL Products]_arbetsyta. |

{style="table-layout:auto"}

## Standardfältvärden

Om du vill spara tid när du skapar produkter refererar standardvärdet för flera produktfält till värden från ett annat fält. Du kan antingen acceptera standardvärdet eller ange ett annat. Följande fält har automatiskt genererat standardvärden:

| Fält | Standard |
|----- |------- |
| [!UICONTROL SKU] | Baserat på produktnamn. |
| [!UICONTROL Meta Title] | Baserat på produktnamn. |
| [!UICONTROL Meta Keywords] | Baserat på produktnamn. |
| [!UICONTROL Meta Description] | Baserat på produktnamn och beskrivning. |

{style="table-layout:auto"}

Platshållare som representerar värdet för ett annat fält omges av klammerparenteser. All attributkod som ingår i produkten [attributuppsättning](attribute-sets.md) kan användas som platshållare.

![Automatisk generering av produktfält](../configuration-reference/catalog/assets/catalog-product-fields-auto-generation.png){width="600" zoomable="yes"}

En detaljerad lista över de här inställningarna finns i [Automatisk generering av produktfält](../configuration-reference/catalog/catalog.md#product-fields-auto-generation) i _Konfigurationsreferens_.

### Redigera platshållarvärdet

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Product Fields Auto-Generation]** och gör eventuella ändringar av platshållarvärdena.

   Om det till exempel finns ett specifikt nyckelord som du vill ta med för varje produkt eller en fras som du vill ta med i varje metabeskrivning, anger du värdet direkt i rätt fält.

   >[!NOTE]
   >
   >Om du vill behålla de befintliga platshållarvärdena ska du bevara de dubbla klammerparenteserna som omger varje tagg.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

### Vanliga platshållare

- `{{color}}`
- `{{country_of_manufacture}}`
- `{{description}}`
- `{{gender}}`
- `{{material}}`
- `{{name}}`
- `{{short_description}}`
- `{{size}}`
- `{{sku}}`
