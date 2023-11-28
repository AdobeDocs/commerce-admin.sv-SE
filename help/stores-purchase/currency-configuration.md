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

Innan du ställer in individuella valutakurser måste du först ange omfattningen för [basvaluta](../configuration-reference/general/currency-setup.md). Den är som standard global, vilket innebär att basvalutainställningen används för hela [butikshierarki](../getting-started/websites-stores-views.md). Om du har en Adobe Commerce- eller Magento Open Source-installation för flera webbplatser kan du hantera flera basvalutor genom att ange omfånget till webbplatsnivån.

Du kan också ange vilka valutor du godkänner och vilken valuta du vill använda för att visa [priser](../catalog/catalog-price-scope.md) i din butik. I följande diagram anges basvalutans omfång på webbplatsnivå så att varje webbplats kan ha olika basvaluta.

![Diagram över valutaomfång](./assets/scope-currency-config.svg){width="600" zoomable="yes"}

## Steg 1: Välj godkända valutor

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. I det övre vänstra hörnet anger du **[!UICONTROL Scope]** till butiksvyn där konfigurationen gäller.

1. I den vänstra panelen under _Allmänt_, välja **[!UICONTROL Currency Setup]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Currency Options]** och ange följande alternativ:

   - **[!UICONTROL Base Currency]** — Ange den primära valutan som du använder för onlinetransaktioner.

   - **[!UICONTROL Default Display Currency]** - Ange den valuta som du använder för att visa priser i butiksvyn.

   - **[!UICONTROL Allowed Currencies]** — Välj alla valutor som du godkänner som betalning i butiksvyn. Se även till att välja din primära valuta.

     Om du har flera valutor håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på respektive alternativ.

   ![Allmän konfiguration - valutaalternativ](../configuration-reference/general/assets/currency-setup-currency-options.png){width="600" zoomable="yes"}

   En detaljerad beskrivning av de här konfigurationsinställningarna finns i [Valutaalternativ](../configuration-reference/general/currency-setup.md) i _Referenshandbok för konfiguration_.

1. När du uppmanas att uppdatera cachen klickar du på _Stäng_ ( ![Stäng ruta](../assets/icon-close-x.png) ) i det övre högra hörnet av systemmeddelandet.

   Du kan [uppdatera cachen](../systems/cache-management.md) senare.

1. Definiera omfattningen för basvalutan:

   - Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL Catalog]** under.

   - Rulla ned och expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Price]** -avsnitt. (Det här avsnittet visas bara om omfånget är inställt som **[!UICONTROL Store View:]** _Standardkonfiguration_.)

   - Ange **[!UICONTROL Catalog Price Scope]** till antingen `Global` eller `Website`.

   ![Katalogkonfiguration - prisalternativ](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

## Steg 2: Konfigurera importanslutningen

1. Bläddra överst på sidan.

1. Expandera på den vänstra panelen **[!UICONTROL General]** och välja **[!UICONTROL Currency Setup]**.

1. Konfigurera anslutningen för valutatjänsten:

   Det finns tre servicealternativ: _[!UICONTROL Fixer.io (legacy)]_,_[!UICONTROL Fixer Api (APILayer)]_ och _[!UICONTROL Currency Converter API]_

   >[!IMPORTANT]
   >
   >Från och med version 2.4.6 av [[!DNL Fixer.io]](https://fixer.io/) är ersatt med [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api) service. Vi rekommenderar att du använder ett APILayer-konto i stället för ett inaktuellt [!DNL Fixer.io] konto.

   - _Ansluta till [fixer.io-tjänst](https://fixer.io/):_

      - Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Fixer.io]** -avsnitt.

      - Ange fixeraren.io **[!UICONTROL API key]**.

      - För **[!UICONTROL Connection Timeout in Seconds]** anger du antalet sekunder av inaktivitet som ska tillåtas innan anslutningen avbryts.

     ![Allmän konfiguration - valutainställning - alternativ för Fixer.io](../configuration-reference/general/assets/currency-setup-fixer.png){width="600" zoomable="yes"}

   - _Ansluta till [[!DNL Fixer Api (APILayer)] service](https://apilayer.com/):_

      - Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Fixer Api (APILayer)]** -avsnitt.

      - Ange [!DNL APILayer] **[!UICONTROL API key]**.

      - För **[!UICONTROL Connection Timeout in Seconds]** anger du antalet sekunder av inaktivitet som ska tillåtas innan anslutningen avbryts.

     ![Allmän konfiguration - valutainställning - alternativ för fast API (APILayer)](../configuration-reference/general/assets/currency-setup-fixer-api.png){width="600" zoomable="yes"}

   - _Ansluta till [[!DNL Currency Convertor API] service](https://free.currencyconverterapi.com/):_

      - Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Currency Convertor API]** -avsnitt.

      - Ange din valutakonverterare **[!UICONTROL API key]**.

      - För **[!UICONTROL Connection Timeout in Seconds]** anger du antalet sekunder av inaktivitet som ska tillåtas innan anslutningen avbryts.

     ![Allmän konfiguration - valutainställning - Alternativ för valutakonverterarens API](../configuration-reference/general/assets/currency-setup-converter.png){width="600" zoomable="yes"}

## Steg 3: Konfigurera inställningar för schemalagd import

1. Utöka ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Scheduled Import Settings]** -avsnitt.

   ![Allmän konfiguration - Inställningar för schemalagd valutaimport](../configuration-reference/general/assets/currency-setup-scheduled-import-settings.png){width="600" zoomable="yes"}

1. Om du vill uppdatera valutakurser automatiskt anger du **[!UICONTROL Enabled]** till `Yes`.

1. Ange uppdateringsalternativ:

   - **[!UICONTROL Service]** — Ange till tariffprovidern. Standardvärdet är `Fixer.io (legacy)`.

   - **[!UICONTROL Start Time]** - Ange timma, minut och sekund att hastigheterna uppdateras enligt schemat.

   - **[!UICONTROL Frequency]** — För att avgöra hur ofta tarifferna uppdateras ska du ange något av följande:

      - `Daily`
      - `Weekly`
      - `Monthly`

   - **[!UICONTROL Error Email Recipient]** — Ange e-postadressen till den person som ska få e-postmeddelanden om ett fel inträffar under importen.

     Om du vill ange flera e-postadresser avgränsar du dem med kommatecken.

   - **[!UICONTROL Error Email Sender]** — Ange [butikskontakt](../getting-started/store-details.md#store-email-addresses) som visas som avsändaren av felmeddelandet.

   - **[!UICONTROL Error Email Template]** — Ange till den e-postmall som används för felmeddelandet.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

1. När du uppmanas att uppdatera cachen klickar du på **[!UICONTROL Cache Management]** länka och uppdatera den ogiltiga cachen.

   ![Systemmeddelande - uppdatera den ogiltiga cachen](./assets/msg-cache-management.png){width="600" zoomable="yes"}

## Steg 4: Uppdatera valutakurserna

Valutakurserna måste uppdateras med aktuella värden innan de träder i kraft. [Uppdatera tarifferna](currency-update.md) manuellt eller för att importera tarifferna automatiskt.

## Steg 5: Anpassa valutasymboler (valfritt)

Med Hantering av valutasymboler kan du anpassa symbolen som är kopplad till varje valuta som accepteras som betalning i din butik.

![Valutasymboler](./assets/stores-currency-symbols.png){width="600" zoomable="yes"}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Symbols]**.

   Varje valuta som är aktiverad för din butik visas i _[!UICONTROL Currency]_lista.

1. Ändra inställningarna i listan efter behov:

   - Ange en anpassad symbol för varje valuta som du vill använda, eller välj **[!UICONTROL Use Standard]** för varje valuta.

   - Om du vill åsidosätta standardsymbolen avmarkerar du _[!UICONTROL Use Standard]_och ange den symbol som du vill använda.

   >[!NOTE]
   >
   >Det går inte att ändra justeringen av valutasymbolen från vänster till höger.

1. När du är klar klickar du på **[!UICONTROL Save Currency Symbols]**.

1. När du uppmanas att uppdatera cachen klickar du på **[!UICONTROL Cache Management]** länka och uppdatera eventuell ogiltig cache.
