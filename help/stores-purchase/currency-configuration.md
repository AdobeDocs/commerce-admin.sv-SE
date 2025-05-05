---
title: Valutakonfiguration
description: Lär dig hur du anger omfånget för basvalutan och hur du anger vilka valutor du godkänner och vilken valuta du vill använda för prisvisning.
exl-id: ba78095f-36eb-4e38-a6e8-72d85e0cf980
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---

# Valutakonfiguration

Innan du ställer in enskilda valutakurser måste du först ställa in omfånget för [basvalutan](../configuration-reference/general/currency-setup.md). Den är inställd på global som standard, vilket tillämpar basvalutainställningen på hela [butikshierarkin](../getting-started/websites-stores-views.md). Om du har en Adobe Commerce- eller Magento Open Source-installation för flera webbplatser kan du hantera flera basvalutor genom att ange omfånget till webbplatsnivån.

Du anger också vilka valutor du godkänner och vilken valuta du vill använda för att visa [priser](../catalog/catalog-price-scope.md) i din butik. I följande diagram anges basvalutans omfång på webbplatsnivå så att varje webbplats kan ha olika basvaluta.

![Valutaomfångsdiagram](./assets/scope-currency-config.svg){width="600" zoomable="yes"}

## Steg 1: Välj godkända valutor

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. I det övre vänstra hörnet anger du **[!UICONTROL Scope]** till den butiksvy där konfigurationen gäller.

1. Välj **[!UICONTROL Currency Setup]** på den vänstra panelen under _Allmänt_.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Currency Options]** och ange följande alternativ:

   - **[!UICONTROL Base Currency]** - Ange den primära valutan som du använder för onlinetransaktioner.

   - **[!UICONTROL Default Display Currency]** - Ange den valuta som du använder för att visa priser i butiksvyn.

   - **[!UICONTROL Allowed Currencies]** - Välj alla valutor som du godkänner som betalning i butiksvyn. Se även till att välja din primära valuta.

     Om du har flera valutor håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på respektive alternativ.

   ![Allmän konfiguration - valutaalternativ](../configuration-reference/general/assets/currency-setup-currency-options.png){width="600" zoomable="yes"}

   En detaljerad beskrivning av de här konfigurationsinställningarna finns i [Valutaalternativ](../configuration-reference/general/currency-setup.md) i _referenshandboken för konfiguration_.

1. När du uppmanas att uppdatera cachen klickar du på _Close_ ( ![Close box](../assets/icon-close-x.png) ) i det övre högra hörnet av systemmeddelandet.

   Du kan [uppdatera cachen](../systems/cache-management.md) senare.

1. Definiera omfattningen för basvalutan:

   - Expandera **[!UICONTROL Catalog]** i den vänstra panelen och välj **[!UICONTROL Catalog]** under.

   - Bläddra nedåt och utöka ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Price]**. (Det här avsnittet visas bara om omfånget är inställt på **[!UICONTROL Store View:]** _Standardkonfiguration_.)

   - Ange **[!UICONTROL Catalog Price Scope]** till antingen `Global` eller `Website`.

   ![Katalogkonfiguration - prisalternativ](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

## Steg 2: Konfigurera importanslutningen

1. Bläddra överst på sidan.

1. Expandera **[!UICONTROL General]** i den vänstra panelen och välj **[!UICONTROL Currency Setup]**.

1. Konfigurera anslutningen för valutatjänsten:

   Det finns tre tjänstalternativ: _[!UICONTROL Fixer.io (legacy)]_,_[!UICONTROL Fixer Api (APILayer)]_ och _[!UICONTROL Currency Converter API]_

   >[!IMPORTANT]
   >
   >Från och med version 2.4.6 är tjänsten [[!DNL Fixer.io]](https://fixer.io/) inaktuell och ersatt med tjänsten [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api). Vi rekommenderar att du använder ett APILayer-konto i stället för ett inaktuellt [!DNL Fixer.io]-konto.

   - _Ansluta till tjänsten [fixer.io](https://fixer.io/):_

      - Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Fixer.io]**.

      - Ange din fixer.io **[!UICONTROL API key]**.

      - För **[!UICONTROL Connection Timeout in Seconds]** anger du antalet sekunder av inaktivitet som ska tillåtas innan anslutningens timeout inträffar.

     ![Allmän konfiguration - valutainställning - Fixer.io-alternativ](../configuration-reference/general/assets/currency-setup-fixer.png){width="600" zoomable="yes"}

   - _Ansluta till [[!DNL Fixer Api (APILayer)] tjänsten](https://apilayer.com/):_

      - Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Fixer Api (APILayer)]**.

      - Ange din [!DNL APILayer] **[!UICONTROL API key]**.

      - För **[!UICONTROL Connection Timeout in Seconds]** anger du antalet sekunder av inaktivitet som ska tillåtas innan anslutningens timeout inträffar.

     ![Allmän konfiguration - valutainställning - alternativ för Fast API (APILayer)](../configuration-reference/general/assets/currency-setup-fixer-api.png){width="600" zoomable="yes"}

   - _Ansluta till [[!DNL Currency Convertor API] tjänsten](https://free.currencyconverterapi.com/):_

      - Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Currency Convertor API]**.

      - Ange valutakonverteraren **[!UICONTROL API key]**.

      - För **[!UICONTROL Connection Timeout in Seconds]** anger du antalet sekunder av inaktivitet som ska tillåtas innan anslutningens timeout inträffar.

     ![Allmän konfiguration - valutainställning - API-alternativ för valutakonverterare](../configuration-reference/general/assets/currency-setup-converter.png){width="600" zoomable="yes"}

## Steg 3: Konfigurera inställningar för schemalagd import

1. Utöka ![Expanderingsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Scheduled Import Settings]** när du fortsätter med valutainställningarna.

   ![Allmän konfiguration - schemalagda importinställningar för valuta](../configuration-reference/general/assets/currency-setup-scheduled-import-settings.png){width="600" zoomable="yes"}

1. Om du vill uppdatera valutakurser automatiskt anger du **[!UICONTROL Enabled]** till `Yes`.

1. Ange uppdateringsalternativ:

   - **[!UICONTROL Service]** - Ange till tariffprovidern. Standardvärdet är `Fixer.io (legacy)`.

   - **[!UICONTROL Start Time]** - Ange timma, minut och sekund att hastigheterna uppdateras enligt schemat.

   - **[!UICONTROL Frequency]** - Ange något av följande för att avgöra hur ofta tarifferna uppdateras:

      - `Daily`
      - `Weekly`
      - `Monthly`

   - **[!UICONTROL Error Email Recipient]** - Ange e-postadressen till den person som ska få e-postmeddelanden om ett fel inträffar under importen.

     Om du vill ange flera e-postadresser avgränsar du dem med kommatecken.

   - **[!UICONTROL Error Email Sender]** - Ange som [butikskontakt](../getting-started/store-details.md#store-email-addresses) som visas som avsändare av felmeddelandet.

   - **[!UICONTROL Error Email Template]** - Ange till den e-postmall som används för felmeddelandet.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

1. När du uppmanas att uppdatera cachen klickar du på länken **[!UICONTROL Cache Management]** och uppdaterar det ogiltiga cacheminnet.

   ![Systemmeddelande - uppdatera den ogiltiga cachen](./assets/msg-cache-management.png){width="600" zoomable="yes"}

## Steg 4: Uppdatera valutakurserna

Valutakurserna måste uppdateras med aktuella värden innan de träder i kraft. [Uppdatera frekvenserna](currency-update.md) manuellt eller importera dem automatiskt.

## Steg 5: Anpassa valutasymboler (valfritt)

Med Hantering av valutasymboler kan du anpassa symbolen som är kopplad till varje valuta som accepteras som betalning i din butik.

![Valutasymboler](./assets/stores-currency-symbols.png){width="600" zoomable="yes"}

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Symbols]**&#x200B;på sidofältet_ Admin _.

   Varje valuta som är aktiverad för din butik visas i listan _[!UICONTROL Currency]_.

1. Ändra inställningarna i listan efter behov:

   - Ange en anpassad symbol för varje valuta som du vill använda, eller markera kryssrutan **[!UICONTROL Use Standard]** för varje valuta.

   - Om du vill åsidosätta standardsymbolen avmarkerar du kryssrutan _[!UICONTROL Use Standard]_&#x200B;och anger den symbol som du vill använda.

   >[!NOTE]
   >
   >Det går inte att ändra justeringen av valutasymbolen från vänster till höger.

1. Klicka på **[!UICONTROL Save Currency Symbols]** när du är klar.

1. När du uppmanas att uppdatera cachen klickar du på länken **[!UICONTROL Cache Management]** och uppdaterar eventuell ogiltig cache.
