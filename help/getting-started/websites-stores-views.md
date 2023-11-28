---
title: Omfång för webbplats, lagring och visning
description: Lär dig mer om hierarkin med webbplatser, butiker och butiksvyer som ni kan använda för att leverera shoppingupplevelser till era kunder.
exl-id: 80fc1b73-c869-4f1c-b1a1-d61823b91d83
feature: System, Site Management
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Omfång för webbplats, lagring och visning

Varje installation av Adobe Commerce och Magento Open Source har en [hierarki](../stores-purchase/stores.md) av webbplatser, butiker och butiksvyer. Termen _omfång_ avgör var i hierarkin en databasenhet - till exempel en produkt, ett attribut eller en kategori - innehållselement eller konfigurationsinställningar gäller. Webbplatser, butiker och butiksvyer har en-till-många-relation mellan överordnade och underordnade. En installation kan ha flera webbplatser, och varje webbplats kan ha flera butiker och butiksvyer.

>[!NOTE]
>
>Mer information finns på [Flera webbplatser eller butiker](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) i [!DNL Commerce] dokumentation för utvecklare.

## Webbplatser

Installationer börjar med en enda [webbplats](../stores-purchase/stores.md#add-websites), som kallas _Huvudwebbplats_ som standard. Du kan också konfigurera flera webbplatser för en enskild installation, var och en med sin egen IP-adress och domän.

## Lager

En och samma webbplats kan ha flera [butiker](../stores-purchase/stores.md#add-stores), var och en med sin egen huvudmeny. Butikerna delar produktkatalogen men kan ha ett annat urval av produkter och design. Alla butiker på samma webbplats delar administratören och kassan.

## Butiksvyer

Varje butik som är tillgänglig för kunder presenteras enligt en specifik _[visa](../stores-purchase/store-views.md)_. Inledningsvis har en butik en enda standardvy. Ytterligare butiksvyer kan läggas till för olika språk eller andra syften. Kunder kan använda språkväljaren i rubriken för att ändra butiksvyn.

Tänk på följande när du arbetar med webbplatser, butiker och butiksvyer:

- Handelsinstanser har en överlappande modell: global → webbplats → lagra → butiksvy.
- Varje webbplats har minst en standardvy för butik och butik.
- Varje butiksvy kan ha en egen bas-URL.
- Den primära funktionen för en webbplats är den högsta funktionskonfigurationen.
- Den primära funktionen i ett arkiv är rotkategorikonfiguration.
- Den primära funktionen i en butiksvy är konverteringsinformation och valutasymbolkonfiguration.

## Omfångsinställningar

Om din Adobe Commerce- eller Magento Open Source-installation har en hierarki med webbplatser, butiker eller vyer kan du ange kontext eller _omfång_ för en konfigurationsinställning. Kontexten för många databasentiteter kan också tilldelas ett specifikt omfång för att avgöra hur den används i butikshierarkin. Mer information finns på [Produktomfång](../catalog/introduction.md#product-scope) och [Prisområde](../catalog/catalog-price-scope.md).

Vissa konfigurationsinställningar, till exempel postnummer, har ett globalt omfång eftersom samma värde används i hela systemet. The [webbplats](../stores-purchase/stores.md#add-websites) omfånget gäller alla butiker under den nivån i hierarkin, inklusive alla butiker och deras vyer. Alla objekt som omfattas av [butiksvy](../stores-purchase/store-views.md) kan ställas in på olika sätt för varje butiksvy, som vanligtvis används för flera språk. Information om hur du åsidosätter standardvärdena för konfigurationsinställningarna finns i [Ange omfånget](../configuration-reference/scope-change.md#set-the-scope).

Såvida inte butiken körs i [single store mode](#single-store-mode)kommer omfattningen för varje konfigurationsinställning att visas i liten text under fältetiketten. Om din installation innehåller flera webbplatser, butiker eller vyer väljer du [butiksvy](../stores-purchase/store-views.md) där inställningarna gäller innan du gör några ändringar.

![Hierarki med webbplatser, butiker och butiksvyer](./assets/scope-multisite.svg){width="550"}

| Omfång | Beskrivning |
|--- |--- |
| [!UICONTROL Global] | Systemomfattande inställningar och resurser som är tillgängliga under hela installationen. |
| [!UICONTROL Website] | Inställningar och resurser som är begränsade till den aktuella webbplatsen. Varje webbplats har en standardbutik. |
| [!UICONTROL Store] | Inställningar och resurser som är begränsade till den aktuella butiken. Varje butik har en standardrotkategori (huvudmeny) och standardbutiksvy. |
| [!UICONTROL Store View] | Inställning och resurser som är begränsade till den aktuella butiksvyn. |

{style="table-layout:auto"}

## Enskilt butiksläge

Om din Commerce-installation bara har en enda butiksvy kan du förenkla visningen genom att inaktivera alla butiksvyalternativ och omfångsindikatorer. Läget för en butik åsidosätts om du [lägga till fler butiksvyer](../stores-purchase/store-views.md) senare.

![Omfång - enkel vy](./assets/scope-single-view.svg){width="550"}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Under **[!UICONTROL General]** rullar du nedåt till sidans nederkant och expanderar **[!UICONTROL Single-Store Mode]** -avsnitt.

1. Ange **[!UICONTROL Enable Single-Store Mode]** till `Yes`.

   ![Allmän konfiguration - Aktivera Single Store-läge](./assets/general-single-store-mode.png){width="400"}

1. Klicka på **[!UICONTROL Save Config]**.

1. Gör följande när du uppmanas att uppdatera cachen:

   - Klicka på **[!UICONTROL Cache Management]** i systemmeddelandet längst upp på sidan.

     ![Systemmeddelande - cachehantering](../catalog/assets/msg-cache-management.png){width="600" zoomable="yes"}

   - Välj **[!UICONTROL Page Cache]** kryssrutan.

   - Med **[!UICONTROL Actions]** ange till `Refresh`, klicka **[!UICONTROL Submit]**
