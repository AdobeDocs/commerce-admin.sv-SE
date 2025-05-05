---
title: Omfång för webbplats, lagring och visning
description: Lär dig mer om hierarkin med webbplatser, butiker och butiksvyer som ni kan använda för att leverera shoppingupplevelser till era kunder.
exl-id: 80fc1b73-c869-4f1c-b1a1-d61823b91d83
feature: System, Site Management
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Omfång för webbplats, lagring och visning

Alla Adobe Commerce- och Magento Open Source-installationer har en [hierarki](../stores-purchase/stores.md) med webbplatser, butiker och butiksvyer. Termen _scope_ avgör var i hierarkin en databasentitet - t.ex. en produkt, ett attribut eller en kategori - innehållselementet eller konfigurationsinställningen gäller. Webbplatser, butiker och butiksvyer har en-till-många-relation mellan överordnade och underordnade. En installation kan ha flera webbplatser, och varje webbplats kan ha flera butiker och butiksvyer.

>[!NOTE]
>
>Mer information finns i [Flera webbplatser eller butiker](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) i utvecklardokumentationen för [!DNL Commerce].

## Webbplatser

Installationer börjar med en enda [webbplats](../stores-purchase/stores.md#add-websites), som kallas _huvudwebbplats_ som standard. Du kan också konfigurera flera webbplatser för en enskild installation, var och en med sin egen IP-adress och domän.

## Lager

En enskild webbplats kan ha flera [butiker](../stores-purchase/stores.md#add-stores) med en egen huvudmeny. Butikerna delar produktkatalogen men kan ha ett annat urval av produkter och design. Alla butiker på samma webbplats delar administratören och kassan.

## Butiksvyer

Varje butik som är tillgänglig för kunder presenteras enligt en specifik _[vy](../stores-purchase/store-views.md)_. Inledningsvis har en butik en enda standardvy. Ytterligare butiksvyer kan läggas till för olika språk eller andra syften. Kunder kan använda språkväljaren i rubriken för att ändra butiksvyn.

Tänk på följande när du arbetar med webbplatser, butiker och butiksvyer:

- Commerce-instanser har en överlappande modell: global → webbplats → lagra → butiksvy.
- Varje webbplats har minst en standardvy för butik och butik.
- Varje butiksvy kan ha en egen bas-URL.
- Den primära funktionen för en webbplats är den högsta funktionskonfigurationen.
- Den primära funktionen i ett arkiv är rotkategorikonfiguration.
- Den primära funktionen i en butiksvy är konverteringsinformation och valutasymbolkonfiguration.

## Omfångsinställningar

Om din Adobe Commerce- eller Magento Open Source-installation har en hierarki med webbplatser, butiker eller vyer kan du ange kontexten, eller _omfattningen_, för en konfigurationsinställning. Kontexten för många databasentiteter kan också tilldelas ett specifikt omfång för att avgöra hur den används i butikshierarkin. Mer information finns i [Produktomfång](../catalog/introduction.md#product-scope) och [Prisomfång](../catalog/catalog-price-scope.md).

Vissa konfigurationsinställningar, till exempel postnummer, har ett globalt omfång eftersom samma värde används i hela systemet. Omfånget [webbplats](../stores-purchase/stores.md#add-websites) gäller alla butiker under den nivån i hierarkin, inklusive alla butiker och deras vyer. Alla objekt med omfånget [butiksvy](../stores-purchase/store-views.md) kan anges på olika sätt för varje butiksvy, vilket vanligtvis används för flera språk. Mer information om hur du åsidosätter standardvärdena för konfigurationsinställningarna finns i [Ange omfånget](../configuration-reference/scope-change.md#set-the-scope).

Såvida inte butiken körs i [single store-läge](#single-store-mode) visas omfånget för varje konfigurationsinställning i liten text under fältetiketten. Om din installation innehåller flera webbplatser, butiker eller vyer väljer du [butiksvyn](../stores-purchase/store-views.md) där inställningarna ska gälla innan du gör några ändringar.

![Hierarki med webbplatser, butiker och butiksvyer](./assets/scope-multisite.svg){width="550"}

| Omfång | Beskrivning |
|--- |--- |
| [!UICONTROL Global] | Systemomfattande inställningar och resurser som är tillgängliga under hela installationen. |
| [!UICONTROL Website] | Inställningar och resurser som är begränsade till den aktuella webbplatsen. Varje webbplats har en standardbutik. |
| [!UICONTROL Store] | Inställningar och resurser som är begränsade till den aktuella butiken. Varje butik har en standardrotkategori (huvudmeny) och standardbutiksvy. |
| [!UICONTROL Store View] | Inställning och resurser som är begränsade till den aktuella butiksvyn. |

{style="table-layout:auto"}

## Enskilt butiksläge

Om din Commerce-installation bara har en enda butiksvy kan du förenkla visningen genom att stänga av alla visningsalternativ och omfångsindikatorer för butiken. Läget för en butik åsidosätts om du [lägger till fler butiksvyer](../stores-purchase/store-views.md) senare.

![Omfång - enkel vy](./assets/scope-single-view.svg){width="550"}

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Under **[!UICONTROL General]** bläddrar du nedåt till sidan och expanderar avsnittet **[!UICONTROL Single-Store Mode]**.

1. Ange **[!UICONTROL Enable Single-Store Mode]** till `Yes`.

   ![Allmän konfiguration - Aktivera Single-Store-läge](./assets/general-single-store-mode.png){width="400"}

1. Klicka på **[!UICONTROL Save Config]**.

1. Gör följande när du uppmanas att uppdatera cachen:

   - Klicka på länken **[!UICONTROL Cache Management]** i systemmeddelandet längst upp på sidan.

     ![Systemmeddelande - cachehantering](../catalog/assets/msg-cache-management.png){width="600" zoomable="yes"}

   - Markera kryssrutan **[!UICONTROL Page Cache]**.

   - Med **[!UICONTROL Actions]** inställd på `Refresh` klickar du på **[!UICONTROL Submit]**
