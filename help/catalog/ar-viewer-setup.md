---
title: '''[!DNL AR Viewer] för Adobe Commerce'
description: Läs om hur du hanterar 3D-modellresurser med [!DNL AR Viewer] tillägg för dina produktlistor.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Hantera 3D-produktmodeller med [!DNL AR Viewer] för Adobe Commerce

Du kan överföra en `.USDZ` som gör det möjligt att använda AR- och 3D-modeller i produktlistan.

The [!DNL AR Viewer] endast stöder `.USDZ` filer.

## Installera tillägget

[!DNL AR Viewer] installeras som ett tillägg från [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}.

Se [_Installationshandbok_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) om du vill ha mer information om installationsprocessen för tillägget.

Efter [!DNL AR Viewer] tillägg är installerat och konfigurerat kan administratörsanvändare konfigurera, anpassa och hantera produktlistor som inkluderar 3D-modeller.

## Lägga till en 3D-modell

1. Öppna produkten i redigeringsläge.

1. Om du vill arbeta med en viss butiksvy anger du **[!UICONTROL Store View]** Välj till lämplig vy.

   >[!NOTE]
   >
   >Nya 3D-modeller för produkter är _alltid_ överförd och synlig i _alla_ lagra vyer, även om `All Store Views` omfånget används inte för överföring. <br/><br/>Om du vill dölja 3D-modeller för produkter från en viss butiksvy måste du växla till den butiksvyn, välja **[!UICONTROL Hide from Product Page]** kryssrutan för 3D-modellen och klicka **[!UICONTROL Save]**.

1. Bläddra nedåt och expandera _[!UICONTROL Product 3D Model]_-avsnitt.

   ![Popup-meny](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. Lägg till 3D-modellen (`.USDZ` -fil) för produkten.

1. Klicka på **[!UICONTROL Save]**.

### Ta bort en 3D-modell

Så här tar du bort en 3D-modell från produktinformationen:

1. Klicka på **[!UICONTROL Delete]**.

1. Klicka på **[!UICONTROL Save]**.

## Visa 3D-produktmodeller

När produktinformationen uppdateras med 3D-modellen:

1. The [!DNL AR Viewer] genererar en QR-kod i produktbeskrivningen som kodar AR AR-filen.

1. Kunden kan se den här QR-koden på produktsidan.

1. När kunderna skannar QR-koden med sina mobila enheter återges en AR-upplevelse på den mobila enheten.

>[!NOTE]
>
> En serie demonstrationsvideor om hur en användare lägger till en 3D-modell till en produkt finns i [AR Viewer för Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) sida in _Commerce Videos och Tutorials_.
