---
title: Dynamiska block
description: Använd dynamiska block för att skapa interaktivt multimediematerial som bygger på logik från prisregler och kundsegment.
exl-id: 0c842ad9-2e46-48aa-9a12-2f74a54c352e
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# Dynamiska block

{{ee-feature}}

Skapa avancerat interaktivt innehåll som styrs av logik från [prisregler](../merchandising-promotions/introduction.md#price-rules) och [kundsegment](../customers/customer-segments.md). Befintliga [dynamiska block](../page-builder/dynamic-block.md) kan läggas till direkt på [!DNL Page Builder] [scenen](../page-builder/workspace.md). Ett detaljerat steg-för-steg-exempel på hur du använder dynamiska block finns i [Självstudiekurs 2: Block](../page-builder/2-blocks.md).

>[!NOTE]
>
>Alternativet _[!UICONTROL Banner]_&#x200B;i [[!UICONTROL Content] menu ](content-menu.md) togs bort i 2.3.1 och togs bort i 2.4.0. Funktionen ersätts av Dynamic Blocks.

![[!DNL Page Builder] - dynamiskt block med prisregel och kundsegment ](../page-builder/assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

## Steg 1: Skapa ett dynamiskt block

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**&#x200B;på sidofältet_ Admin _.

   ![Lista med dynamiska block](../page-builder/assets/pb-tutorial2-block-dynamic-add.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Add Dynamic Block]** i det övre högra hörnet.

   ![Nytt dynamiskt block](../page-builder/assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. Om det är tillämpligt anger du **[!UICONTROL Store View]** till en specifik butiksvy där det dynamiska blocket ska visas.

1. Om du vill aktivera det dynamiska blocket anger du **[!UICONTROL Enable Dynamic Block]** till `Yes`.

1. Ange en beskrivande **[!UICONTROL Dynamic Block Name]** för intern referens.

1. Ange **[!UICONTROL Dynamic Block Type]** till det område på sidan där du vill att det dynamiska blocket ska visas och klicka på **[!UICONTROL Done]**.

   ![Anger den dynamiska blocktypen](../page-builder/assets/pb-dynamic-block-type.png){width="500" zoomable="yes"}

1. Markera kryssrutan för varje segment som du vill se det dynamiska blocket i listan **[!UICONTROL Customer Segment]** och klicka på **[!UICONTROL Done]** för att spara inställningen.

   ![Välja ett kundsegment](../page-builder/assets/pb-dynamic-block-customer-segment.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >- Om inget segment skapas är det dynamiska blocket synligt för alla.
   >- Om kunden inte tillhör något segment och det dynamiska blocket skapas för alla segment visas fortfarande innehållet i det dynamiska blocket.
   >- Om alla kundsegment som är tilldelade ett dynamiskt block tas bort, visas innehållet för alla.

### Använda Real-Time CDP-målgrupper i dynamiska block

Om du [installerade](../customers/audience-activation.md#install-the-extension) och [konfigurerade](../customers/audience-activation.md#configure-the-extension) tillägget [!DNL Audience Activation] visas ett avsnitt med namnet **[!UICONTROL Audiences]**.

![Välj en Real-Time CDP-publik](./assets/dynamic-block-rtcdp.png){width="600" zoomable="yes"}

I listan **[!UICONTROL Real-Time CDP Audience]** markerar du kryssrutan för varje publik som du vill se det dynamiska blocket och klickar på **[!UICONTROL Done]** för att spara inställningen.

## Steg 2: Slutför innehållet

Använd [!DNL Page Builder] [arbetsytan](../page-builder/workspace.md) för att slutföra innehållet.

![[!DNL Page Builder] - arbetsytan för dynamiskt block](../page-builder/assets/pb-dynamic-block-workspace.png){width="600" zoomable="yes"}

## Steg 3: Välj en relaterad kampanj

1. Bläddra nedåt och expandera ![Expansionsväljaren](../assets/icon-display-expand.png) **[!UICONTROL Related Promotions]**.

1. Klicka på den typ av befordran som du vill associera med det dynamiska blocket:

   - **[!UICONTROL Add Cart Price Rules]** (se [Kundprisregler](../merchandising-promotions/price-rules-cart.md))

   - **[!UICONTROL Add Catalog Price Rules]** (se [Katalogprisregler](../merchandising-promotions/price-rules-catalog.md))

   >[!NOTE]
   >
   >Katalogprisregler stöds inte för Real-Time CDP-målgrupper.

1. I listan med tillgängliga regler markerar du kryssrutan för varje regel som du vill använda och klickar på **[!UICONTROL Add Selected]**.

1. När det dynamiska blocket är klart klickar du på **[!UICONTROL Save]**.

## Steg 4: Lägg till det dynamiska blocket på en sida

1. Öppna sidan där du vill att det dynamiska blocket ska visas.

1. Använd innehållstypen [[!UICONTROL Add Dynamic Block]](../page-builder/dynamic-block.md) för att lägga till det dynamiska blocket på scenen.

## Fält- och verktygsbeskrivningar

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Store View] | Anger de butiksvyer där det dynamiska blocket ska vara tillgängligt. |
| [!UICONTROL Enable Dynamic Block] | Aktiverar eller inaktiverar det dynamiska blocket. Alternativ: Ja/Nej |
| [!UICONTROL Dynamic Block Name] | Ett beskrivande namn som identifierar det dynamiska blocket i Admin. |
| [!UICONTROL Dynamic Block Type] | Identifierar platsen i [standardsidlayouten](layout-updates.md) där det dynamiska blocket placeras. Alternativ: <br/>**[!UICONTROL Content Area]**- Placerar det dynamiska blocket i sidans [innehållsområde](layout-updates.md).<br/>**[!UICONTROL Footer]** - Placerar det dynamiska blocket på sidan [footer](page-setup.md#footer). <br/>**[!UICONTROL Header]**- Placerar det dynamiska blocket på sidan [header](page-setup.md#header).<br/>**[!UICONTROL Left Column]** - Placerar det dynamiska blocket i [vänster sidofält](page-layout.md#standard-page-layouts) i en layout med två eller tre kolumner. <br/>**[!UICONTROL Right Column]**- Placerar det dynamiska blocket i [höger sidofält](page-layout.md#standard-page-layouts) i en layout med två eller tre kolumner. |
| Kundsegment | Associerar ett kundsegment med det dynamiska blocket för att avgöra vilka kunder som kan se det. |
| Real-Time CDP Audience | Associerar en [Real-Time CDP-målgrupp](../customers/audience-activation.md) med det dynamiska blocket för att avgöra vilka kunder som kan se det. |

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
| [!UICONTROL Related Cart Price Rule] | **[!UICONTROL Add Cart Price Rules]** - Associera en befintlig [kundvagnsprisregel](../merchandising-promotions/price-rules-cart.md) med det dynamiska blocket som en befordran. |
| [!UICONTROL Related Catalog Price Rule] | **[!UICONTROL Add Catalog Price Rules]** - Associera en befintlig [katalogprisregel](../merchandising-promotions/price-rules-catalog.md) med det dynamiska blocket som en befordran. |

{style="table-layout:auto"}
