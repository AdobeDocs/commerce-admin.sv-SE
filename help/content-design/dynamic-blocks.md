---
title: Dynamiska block
description: Använd dynamiska block för att skapa interaktivt multimediematerial som bygger på logik från prisregler och kundsegment.
exl-id: 0c842ad9-2e46-48aa-9a12-2f74a54c352e
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# Dynamiska block

{{ee-feature}}

Skapa avancerat interaktivt material som bygger på logik från [prisregler](../merchandising-promotions/introduction.md#price-rules) och [kundsegment](../customers/customer-segments.md). Befintlig [dynamiska block](../page-builder/dynamic-block.md) kan läggas till direkt i [!DNL Page Builder] [stage](../page-builder/workspace.md). Ett detaljerat steg-för-steg-exempel på hur du använder dynamiska block finns i [Självstudiekurs 2: Block](../page-builder/2-blocks.md).

>[!NOTE]
>
>The _[!UICONTROL Banner]_i [[!UICONTROL Content] meny](content-menu.md) togs bort i 2.3.1 och togs bort i 2.4.0. Funktionen ersätts av Dynamic Blocks.

![[!DNL Page Builder] - dynamiskt block med prisregel och kundsegment](../page-builder/assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

## Steg 1: Skapa ett dynamiskt block

1. På _Administratör_ sidebar, gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

   ![Dynamisk blocklista](../page-builder/assets/pb-tutorial2-block-dynamic-add.png){width="600" zoomable="yes"}

1. Klicka på i det övre högra hörnet **[!UICONTROL Add Dynamic Block]**.

   ![Nytt dynamiskt block](../page-builder/assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. Ange om tillämpligt **[!UICONTROL Store View]** till en viss butiksvy där det dynamiska blocket ska visas.

1. Aktivera det dynamiska blocket genom att ange **[!UICONTROL Enable Dynamic Block]** till `Yes`.

1. Ange en beskrivning för intern referens **[!UICONTROL Dynamic Block Name]**.

1. Ange **[!UICONTROL Dynamic Block Type]** till det område på sidan där du vill att det dynamiska blocket ska visas och klicka på **[!UICONTROL Done]**.

   ![Ställa in den dynamiska blocktypen](../page-builder/assets/pb-dynamic-block-type.png){width="500" zoomable="yes"}

1. I **[!UICONTROL Customer Segment]** markerar du kryssrutan för varje segment som du vill se det dynamiska blocket och klickar på **[!UICONTROL Done]** för att spara inställningen.

   ![Välja ett kundsegment](../page-builder/assets/pb-dynamic-block-customer-segment.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >- Om inget segment skapas är det dynamiska blocket synligt för alla.
   >- Om kunden inte tillhör något segment och det dynamiska blocket skapas för alla segment visas fortfarande innehållet i det dynamiska blocket.
   >- Om alla kundsegment som är tilldelade ett dynamiskt block tas bort, visas innehållet för alla.

### Använda Real-Time CDP-målgrupper i dynamiska block

Om du [installerat](../customers/audience-activation.md#install-the-extension) och [konfigurerad](../customers/audience-activation.md#configure-the-extension) den [!DNL Audience Activation] tillägg visas ett avsnitt som kallas **[!UICONTROL Audiences]**.

![Välj en Real-Time CDP-publik](./assets/dynamic-block-rtcdp.png){width="600" zoomable="yes"}

I **[!UICONTROL Real-Time CDP Audience]** markerar du kryssrutan för varje publik som du vill se det dynamiska blocket och klickar på **[!UICONTROL Done]** för att spara inställningen.

## Steg 2: Slutför innehållet

Använd [!DNL Page Builder] [arbetsyta](../page-builder/workspace.md) för att slutföra innehållet.

![[!DNL Page Builder] - arbetsytan för dynamiska block](../page-builder/assets/pb-dynamic-block-workspace.png){width="600" zoomable="yes"}

## Steg 3: Välj en relaterad kampanj

1. Rulla ned och expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Related Promotions]**.

1. Klicka på den typ av befordran som du vill associera med det dynamiska blocket:

   - **[!UICONTROL Add Cart Price Rules]** (se [Kundprisregler](../merchandising-promotions/price-rules-cart.md))

   - **[!UICONTROL Add Catalog Price Rules]** (se [Katalogprisregler](../merchandising-promotions/price-rules-catalog.md))

   >[!NOTE]
   >
   >Katalogprisregler stöds inte för Real-Time CDP-målgrupper.

1. I listan med tillgängliga regler markerar du kryssrutan för varje regel som du vill använda och klickar på **[!UICONTROL Add Selected]**.

1. När det dynamiska blocket är klart klickar du **[!UICONTROL Save]**.

## Steg 4: Lägg till det dynamiska blocket på en sida

1. Öppna sidan där du vill att det dynamiska blocket ska visas.

1. Använd [[!UICONTROL Add Dynamic Block]](../page-builder/dynamic-block.md) innehållstyp för att lägga till det dynamiska blocket på scenen.

## Fält- och verktygsbeskrivningar

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Store View] | Anger de butiksvyer där det dynamiska blocket ska vara tillgängligt. |
| [!UICONTROL Enable Dynamic Block] | Aktiverar eller inaktiverar det dynamiska blocket. Alternativ: Ja/Nej |
| [!UICONTROL Dynamic Block Name] | Ett beskrivande namn som identifierar det dynamiska blocket i Admin. |
| [!UICONTROL Dynamic Block Type] | Identifierar platsen i [standardsidlayout](layout-updates.md) där det dynamiska blocket placeras. Alternativ: <br/>**[!UICONTROL Content Area]**- Placerar det dynamiska blocket i huvudblocket [innehållsområde](layout-updates.md) på sidan.<br/>**[!UICONTROL Footer]** - Placerar det dynamiska blocket på sidan [sidfot](page-setup.md#footer). <br/>**[!UICONTROL Header]**- Placerar det dynamiska blocket på sidan [header](page-setup.md#header).<br/>**[!UICONTROL Left Column]** - Placerar det dynamiska blocket i [vänster sidospalt](page-layout.md#standard-page-layouts) i en layout med två eller tre kolumner. <br/>**[!UICONTROL Right Column]**- Placerar det dynamiska blocket i [höger sidospalt](page-layout.md#standard-page-layouts) i en layout med två eller tre kolumner. |
| Kundsegment | Associerar ett kundsegment med det dynamiska blocket för att avgöra vilka kunder som kan se det. |
| Real-Time CDP Audience | Associerar en [Real-Time CDP](../customers/audience-activation.md) med det dynamiska blocket för att avgöra vilka kunder som kan se det. |

{style="table-layout:auto"}

### Innehåll

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Layout] | Lägg till rader, kolumner eller tabbar på scenen. |
| [!UICONTROL Elements] | Lägg till text, rubriker, knappar, avgränsare och HTML-kod i alla layoutbehållare på scenen. |
| [!UICONTROL Media] | Lägg till bilder, video, banners, reglage och Google Maps i alla befintliga layoutbehållare på scenen. |
| [!UICONTROL Add Content] | Lägg till befintliga block, dynamiska block och produkter på scenen. |

{style="table-layout:auto"}

### Relaterade kampanjer

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Related Cart Price Rule] | **[!UICONTROL Add Cart Price Rules]** - Associera en befintlig [kundprisregel](../merchandising-promotions/price-rules-cart.md) med det dynamiska blocket som en befordran. |
| [!UICONTROL Related Catalog Price Rule] | **[!UICONTROL Add Catalog Price Rules]** - Associera en befintlig [katalogprisregel](../merchandising-promotions/price-rules-catalog.md) med det dynamiska blocket som en befordran. |

{style="table-layout:auto"}
