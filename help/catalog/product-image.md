---
title: Hantera produktbilder och videor
description: Lär dig hur du hanterar bild- och videomaterial för produktlistor.
exl-id: 3cb4ab8a-8966-400f-be94-a517634d1334
feature: Catalog Management, Products, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# Hantera produktbilder och videor

För varje produkt kan du överföra flera bilder och videoklipp, ändra ordningen på dem och styra hur de används. Om du har ett stort antal bilder att hantera kan du föredra att importera dem som en grupp i stället för att överföra dem separat. Mer information finns i [Importera produktbilder](../systems/data-import-product-images.md).

Om du planerar att överföra stora bilder för visning på sidan _[!UICONTROL Product Details]_kan det vara bra att ange en maximal pixelstorlek (bredd och höjd) och automatiskt ändra storlek på filerna vid överföringen. Det finns ett alternativ för att aktivera automatisk storleksändring av större bildfiler när du överför dem. Mer information finns i [Ändra storlek på produktbilder](product-image-config.md#product-image-resizing).

## Uppdatera produktbilderna

1. Öppna produkten i redigeringsläge.

1. Om du vill arbeta med en viss butiksvy ska du ställa in **[!UICONTROL Store View]**-väljaren i det övre vänstra hörnet på den aktuella vyn.

   >[!NOTE]
   >
   >Nya produktbilder överförs **_alltid_** och visas i **_alla_** butiksvyer, även om `All Store Views`-omfånget inte används för överföring. <br/><br/>Om du vill dölja en produktbild från en viss butiksvy måste du växla till den butiksvyn, markera kryssrutan **[!UICONTROL Hide from Product Page]** för bilden och klicka på **[!UICONTROL Save]**.

1. Bläddra nedåt och expandera avsnittet _[!UICONTROL Images and Videos]_.

### Överföra en bild

För bästa kompatibilitet rekommenderar vi att du överför alla produktbilder med färgprofilen `sRGB`. Alla andra färgprofiler konverteras automatiskt till färgprofilen `sRGB` under överföringen av produktbilden, vilket kan orsaka färginkonsekvenser i den överförda bilden.

Bildfilens namnlängd, inklusive filnamnstillägg, får inte överstiga 90 tecken.

Gör något av följande om du vill överföra en bild:

- Dra en bild från skrivbordet och släpp den på plattan _Kamera_ ( ![Kameraikon](../assets/icon-camera.png) ) i rutan _[!UICONTROL Images And Videos]_.

- Klicka på rutan _Kamera_ ( ![Kameraikon](../assets/icon-camera.png) ) i rutan _[!UICONTROL Images And Videos]_, markera bildfilen på datorn och klicka på&#x200B;**[!UICONTROL Open]**.

  ![Överför eller dra och släpp](./assets/product-images-and-video-jewel-tee.png){width="600" zoomable="yes"}

### Ordna om bilder

Om du vill ändra ordning på bilderna i galleriet klickar du på ikonen _[!UICONTROL Sort]_( ![Sorteringsikonen ](./assets/inventory-icon-sort.png) ) längst ned i bildrutan och drar bilden till en annan plats i rutan_[!UICONTROL Images And Videos]_.

![Ändra ordning](./assets/product-images-and-videos-drag.png){width="600" zoomable="yes"}

### Ta bort en bild

Om du vill ta bort en bild från galleriet klickar du på ikonen **[!UICONTROL Delete]** ( ![papperskorgen ](../assets/icon-delete-trashcan.png) ) i det övre högra hörnet av bildpanelen och klickar på **[!UICONTROL Save]**.

### Ange bildinformation

Klicka på bilden som du vill öppna i detaljvyn och gör något av följande:

![Detaljvy för bild](./assets/product-image-detail-jewel-tee.png){width="600" zoomable="yes"}

Om du vill stänga detaljvyn klickar du på ikonen _Stäng_ ( ![Stäng ikon](../assets/icon-close-x.png) ) i det övre högra hörnet.

Klicka på **[!UICONTROL Save]** när du är klar.

#### Ange alternativ text

Bild-Alt-text refereras av skärmläsare för att förbättra webbtillgängligheten och av sökmotorer när webbplatsen indexeras. I vissa webbläsare visas Alt-texten när du för muspekaren. Alt-text kan vara flera ord lång och innehålla noggrant markerade nyckelord.

Ange en kort beskrivning av bilden i rutan _[!UICONTROL Alt Text]_.

#### Tilldela roller

Som standard tilldelas alla roller till den första bilden som överförs till produkten. Så här tilldelar du en roll till en annan bild:

I rutan _[!UICONTROL Role]_väljer du den roll du vill tilldela bilden.

När du återgår till avsnittet _Bilder och videoklipp_ visas de för närvarande tilldelade rollerna under varje bild.

![Tilldelade roller](./assets/product-images-video-swatch.png){width="600" zoomable="yes"}

#### Dölja en bild

Om du vill utesluta en bild från miniatyrgalleriet markerar du kryssrutan **[!UICONTROL Hidden]** och klickar på **[!UICONTROL Save]**.

![Dolda bilder](./assets/product-images-and-videos-hidden.png){width="600" zoomable="yes"}

## Bildroller

| Bildroll | Beskrivning |
|--- |--- |
| [!UICONTROL Thumbnail] | Miniatyrbilder visas i miniatyrgalleriet, i kundvagnen och i vissa block, t.ex. Relaterade objekt. Exempelstorlek: 50 x 50 pixlar |
| [!UICONTROL Small Image] | Den lilla bilden används för produktbilder i listor på kategori- och sökresultatsidor och för att visa de produktbilder som behövs för avsnitt som Up-sells, Cross-sells och New Products List. Exempelstorlek: 470 x 470 pixlar |
| [!UICONTROL Base Image] | Basbilden är huvudbilden på produktinformationssidan. Bildzoomning aktiveras om du överför en bild som är större än bildbehållaren. Basbilden bör vara två eller tre gånger så stor som behållaren, beroende på vilken zoomnivå du vill uppnå. Exempelstorlekar: 470 x 470 pixlar (utan zoom), 1 100 x 1 100 pixlar (med zoom) |
| [!UICONTROL Swatch] | En [färgruta](swatches.md) kan användas för att illustrera färg, mönster eller struktur. Exempelstorlek: 50 x 50 pixlar |

{style="table-layout:auto"}

## Vattenstämplar

Om du går på bekostnad av att skapa egna originalproduktbilder finns det inte mycket du kan göra för att hindra oseriösa konkurrenter från att stjäla dem med en musklickning. Du kan dock göra dem mindre attraktiva genom att placera en vattenstämpel på varje bild för att identifiera dem som din egenskap. En vattenstämpelfil kan vara antingen en JPG (JPEG), GIF eller PNG-bild. Både filtyperna GIF och PNG har stöd för genomskinliga lager som kan användas för att ge vattenstämpeln en genomskinlig bakgrund.

Den vattenstämpel som används för bilden _small_ i följande exempel är en svart logotyp med genomskinlig bakgrund och sparad som en PNG-fil med följande inställningar:

- Storlek: 50x50
- Opacitet: 5
- Position: Sida vid sida

![Vattenstämpel sida vid sida](./assets/storefront-watermark-tiled.png){width="700" zoomable="yes"}

### Lägga till vattenstämplar i produktbilder

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

   Mer information om designkonfigurationer finns i [Designkonfiguration](../content-design/configuration.md).

1. Leta reda på den butiksvy som du vill konfigurera och klicka på **[!UICONTROL Edit]** i kolumnen _[!UICONTROL Action]_.

1. Under _[!UICONTROL Other Settings]_expanderar du ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Product Image Watermarks]**.

   ![Vattenstämplar för produktbilder - bas](./assets/config-design-product-image-watermarks-base.png){width="600" zoomable="yes"}

   Bildinställningarna **[!UICONTROL Base]**, **[!UICONTROL Thumbnail]**, **[!UICONTROL Small]** och **[!UICONTROL Swatch Image]** är desamma.

1. Använd någon av följande metoder för att lägga till resursen med vattenstämpelbild:

   - Klicka på **[!UICONTROL Upload]** och välj den bildfil på datorn som du vill överföra för användning som vattenstämpel.
   - Klicka på **[!UICONTROL Select from Gallery]** och välj en bildresurs i [Mediegalleriet](../content-design/media-gallery.md).

1. Slutför inställningarna för vattenstämpelvisning:

   - Ange **[!UICONTROL Image Opacity]** som en procentandel. Till exempel: `40`

   - Ange **[!UICONTROL Image Size]** i pixlar. Till exempel: `200 x 200`

   - Ange **[!UICONTROL Image Position]** för att bestämma var vattenstämpeln visas.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

1. När du uppmanas att uppdatera cachen klickar du på **[!UICONTROL Cache Management]** i systemmeddelandet och uppdaterar den ogiltiga cachen.

   ![Uppdatera cache](./assets/msg-cache-management.png){width="600" zoomable="yes"}

>[!TIP]
>
>Du kan klicka på **[!UICONTROL Use Default Value]** ![Pilretur](../assets/icon-arrow-return.png) om du vill återställa standardvärdet.

### Ta bort en vattenstämpel

1. Klicka på ikonen **[!UICONTROL Delete]** ( ![papperskorgen ](../assets/icon-delete-trashcan-solid.png) ) i bildens nedre vänstra hörn.

   ![Ta bort vattenstämpel](./assets/product-image-watermark-delete.png){width="300"}

1. Klicka på **[!UICONTROL Save Config]**.

1. När du uppmanas att uppdatera cachen klickar du på **[!UICONTROL Cache Management]** i systemmeddelandet och uppdaterar den ogiltiga cachen.

   Om vattenstämpelbilden finns kvar i butiken går du tillbaka till cachehantering och klickar på **[!UICONTROL Flush Magento Cache]**.
