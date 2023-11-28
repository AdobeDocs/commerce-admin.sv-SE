---
title: Uppdatera valutakurser
description: Lär dig hur du ställer in valutakurser manuellt eller importerar dem till din butik.
exl-id: 316a7bc8-1118-46e7-82ff-891ada04cd13
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Uppdatera valutakurser

Valutakurser kan ställas in manuellt eller importeras till butiken. För att vara säker på att din butik har de senaste kurserna kan du konfigurera valutakurserna så att de uppdateras automatiskt enligt schema.

Innan du importerar valutakurser ska du slutföra [inställning av valutakurs](currency-configuration.md) för att ange vilka valutor du godkänner och för att upprätta importanslutningen och tidsplanen.

![Valutakurser](./assets/stores-currency-rate-update.png){width="600" zoomable="yes"}

## Uppdatera en valutakurs manuellt

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Klicka på den kurs som du vill ändra och ange det nya värdet för varje valuta som stöds.

1. När du är klar klickar du på **[!UICONTROL Save Currency Rates]**.

## Importera valutakurser

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Ange **[!UICONTROL Import Service]** till valutaprovidern.

   Standardprovidern är `fixer.io (legacy)`.

   >[!IMPORTANT]
   >
   >Från och med version 2.4.6 av [[!DNL Fixer.io]](https://fixer.io/) är ersatt med [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api) service. Vi rekommenderar att du använder ett APILayer-konto i stället för ett inaktuellt [!DNL Fixer.io] konto.

1. Klicka på **[!UICONTROL Import]**.

   De uppdaterade priserna visas i _[!UICONTROL Currency Rates]_lista. Om priserna har ändrats sedan den senaste uppdateringen visas den gamla tariffen nedan som referens.

1. När du är klar klickar du på **[!UICONTROL Save Currency Rates]**.

1. När du uppmanas att uppdatera cachen klickar du på **[!UICONTROL Cache Management]** länka och uppdatera den ogiltiga cachen.

   ![Systemmeddelande - uppdatera den ogiltiga cachen](./assets/currency-cache-update.png){width="600" zoomable="yes"}

## Importera valutakurser enligt schema

1. Se till att [Cron](../systems/cron.md) har aktiverats för din butik.

1. Om du vill ange vilka valutor du godkänner och upprätta en importanslutning och ett schema fyller du i [Inställningar för valutakurs](currency-configuration.md).

1. Om du vill verifiera att priserna importeras enligt schema kontrollerar du _[!UICONTROL Currency Rates]_lista.

1. Vänta på tidsperioden för den frekvensinställning som har fastställts för schemat och kontrollera hastigheterna igen.
