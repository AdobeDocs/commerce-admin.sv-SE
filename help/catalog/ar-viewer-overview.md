---
title: '[!DNL AR Viewer] för Adobe Commerce'
description: Lär dig hur  [!DNL AR Viewer] kan hjälpa din Adobe Commerce-instans och hur du kan ta in och konfigurera tillägget.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# [!DNL AR Viewer] för Adobe Commerce

Den förbättrade verkligheten (AR) beskriver användarupplevelser som lägger till 2D- eller 3D-element i livevyn från en enhets kamera på ett sätt som gör att dessa element ser ut att befinna sig i verkligheten.

Tillägget [!DNL AR Viewer] för Adobe Commerce ger en smidig upplevelse som utformats för att visa återgiven 3D-grafik för användaren.

Informationen i den här handboken ger en översikt över introduktionsupplevelsen för [!DNL AR Viewer] i Adobe Commerce och hur [!DNL AR Viewer] är till nytta för användaren samt de bästa metoderna att följa under den resan.

[Universal Scene Description (USD)](https://openusd.org/release/index.html){target=_blank} har utvecklats av Pixar och är den första programvaran med öppen källkod som på ett robust och skalbart sätt kan utbyta 3D-scener som kan bestå av många olika resurser, källor och animeringar, samtidigt som de främjar arbetsflöden med mycket goda samarbetsformer. Den här USD används i `.USDZ` filer. Den här `.USDZ`-filen levererar AIR- och 3D-innehåll till användarens enheter.

>[!NOTE]
>
> [!DNL AR Viewer] stöder bara `.USDZ` filer.

## Krav för [!DNL AR Viewer]

[!DNL AR Viewer] är kompatibel med både [!DNL Magento Open Source] och Adobe Commerce. Mer information om vilka versioner som stöds finns i [Livscykelprincip](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html?lang=sv-SE){target=_blank}.

Mer information finns i [Installera  [!DNL AR Viewer] tillägget](../catalog/ar-viewer-setup.md).

För att kunna använda [!DNL AR Viewer] måste du ha följande tillgängliga för din instans:

* PHP 8.1.0
* Adobe Commerce version 2.4.4 och senare
* Magento Open Source (CE) version 2.4.x

## Kompatibilitetsbegränsningar

[!DNL AR Viewer] befintliga kompatibilitetsbegränsningar:

* Endast `.USDZ`: Den här funktionen har bara stöd för `.USDZ` filer.
* `qr-code`: `endroid/qr-code` version 4.5 krävs.
* `Catalog module`: kräver `magento/module-catalog` version 104.0.0.
