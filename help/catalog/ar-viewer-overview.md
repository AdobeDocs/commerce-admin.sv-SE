---
title: '[!DNL AR Viewer] för Adobe Commerce'
description: Se hur [!DNL AR Viewer] kan vara till fördel för din Adobe Commerce-instans och för hur du kan ta med och konfigurera tillägget.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# [!DNL AR Viewer] för Adobe Commerce

Den förbättrade verkligheten (AR) beskriver användarupplevelser som lägger till 2D- eller 3D-element i livevyn från en enhets kamera på ett sätt som gör att dessa element ser ut att befinna sig i verkligheten.

The [!DNL AR Viewer] för Adobe Commerce-tillägg ger en smidig upplevelse som utformats för att visa återgiven 3D-grafik för användaren.

Informationen i den här guiden ger en översikt över startupplevelsen för [!DNL AR Viewer] i Adobe Commerce och hur [!DNL AR Viewer] är till nytta för användaren och de bästa sätten att följa under resan.

Utvecklad av Pixar, [Universal Scene Description (USD)](https://www.pixar.com/usd){target=_blank} är den första programvaran med öppen källkod som på ett robust och skalbart sätt kan utbyta 3D-scener som kan bestå av många olika resurser, källor och animeringar, samtidigt som de främjar arbetsflöden med starkt samarbete. Denna USD används inom `.USDZ` filer. Detta `.USDZ` filen levererar AR- och 3D-innehåll till användarens enheter.

>[!NOTE]
>
> The [!DNL AR Viewer] endast stöder `.USDZ` filer.

## [!DNL AR Viewer] krav

The [!DNL AR Viewer] är kompatibelt med båda [!DNL Magento Open Source] och Adobe Commerce. Se [Livscykelprincip](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank} om du vill ha mer information om vilka versioner som stöds.

Se [Installera [!DNL AR Viewer] extension](../catalog/ar-viewer-setup.md) för mer information.

För att kunna använda [!DNL AR Viewer]måste du ha följande tillgängliga för din instans:

* PHP 8.1.0
* Adobe Commerce version 2.4.4 och senare
* Magento Open Source (CE) version 2.4.x

## Kompatibilitetsbegränsningar

[!DNL AR Viewer] befintliga kompatibilitetsbegränsningar:

* `.USDZ` endast: Den här funktionen stöder endast `.USDZ` filer.
* `qr-code`: Kräver `endroid/qr-code` version 4.5.
* `Catalog module`: Kräver `magento/module-catalog` version 104.0.0.
