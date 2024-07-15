---
title: '[!UICONTROL General] &gt; [!UICONTROL Currency Setup]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL General] &gt; [!UICONTROL Currency Setup] i Commerce Admin.
exl-id: a84be30f-f2eb-4c86-942c-2d49e5cf23af
role: Admin
feature: Currency, Configuration, Data Import/Export
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Currency Setup]

{{config}}

>[!NOTE]
>
>Mer information om de här konfigurationerna finns i [Valutakonfiguration](../../stores-purchase/currency-configuration.md).

## [!UICONTROL Currency Options]

![Valutainställningar > Valutaalternativ](./assets/currency-setup-currency-options.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Base Currency] | Webbplats | Den primära valutan som används för alla onlinebetalningstransaktioner. För flera butiksvyer måste prisets omfång anges i konfigurationen [Katalog](../catalog/catalog.md). |
| [!UICONTROL Default Display Currency] | Butiksvy | Den primära valuta som används för att visa priser. |
| [!UICONTROL Allowed Currencies] | Butiksvy | Valutorna som är godkända av din butik för betalning. |

{style="table-layout:auto"}

## [!UICONTROL Fixer.io (legacy)]

>[!IMPORTANT]
>
>Från och med version 2.4.6 är tjänsten [[!DNL Fixer.io]](https://fixer.io/) inaktuell och ersatt med tjänsten [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api). Vi rekommenderar att du använder ett APILayer-konto i stället för ett inaktuellt [!DNL Fixer.io]-konto.

![Valutainställningar > Fixer.io](./assets/currency-setup-fixer.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL API key] | Global | Nyckeln som används för att komma åt konverteringstjänsten via ditt [!DNL fixer.io]-konto. Mer information finns i [[!DNL fixer.io]](https://fixer.io/). |
| [!UICONTROL Connection Timeout in Seconds] | Global | Avgör antalet sekunder av inaktivitet innan en Fixer.io-session tar slut. Standardvärde: `100` |

{style="table-layout:auto"}

## [!UICONTROL Fixer Api (APILayer)]

![Valutainställning > Fast API (APILayer)](./assets/currency-setup-fixer-api.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL API key] | Global | Nyckeln som används för att komma åt konverteringstjänsten via ditt [!DNL APILayer]-konto. Mer information finns i [[!DNL APILayer]](https://apilayer.com/). |
| [!UICONTROL Connection Timeout in Seconds] | Global | Fastställer antalet sekunder av inaktivitet innan en [!DNL APILayer]-session-timeout inträffar. Standardvärdet är `100`. |

{style="table-layout:auto"}

## [!UICONTROL Currency Converter API]

![Valutainställning > Valutakonverterar-API](./assets/currency-setup-converter.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL API key] | Global | Nyckeln som används för att komma åt konverteringstjänsten. Mer information finns i [[!DNL Currency Convertor] API](https://free.currencyconverterapi.com/). |
| [!UICONTROL Connection Timeout in Seconds] | Global | Fastställer antalet sekunder av inaktivitet innan en [!DNL Currency Converter]-session-timeout inträffar. Standardvärde:`100` |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Import Settings]

![Valutainställningar > Schemalagda importinställningar](./assets/currency-setup-scheduled-import-settings.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled] | Butiksvy | Avgör om schemalagd import är aktiverad för valutakurser. Alternativ: `Yes` / `No` |
| [!UICONTROL Service] | Butiksvy | Anger den tjänst som tillhandahåller data för den schemalagda importen. Standardvärdet är `fixer.io` |
| [!UICONTROL Start Time] | Butiksvy | Anger starttiden per timme, minut och sekund, baserat på en 24-timmarsklocka. |
| [!UICONTROL Frequency] | Butiksvy | Anger hur ofta den schemalagda importen sker. Alternativ: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | Butiksvy | Identifierar e-postadressen till varje person som får ett e-postmeddelande om schemalagda importfel. För flera mottagare avgränsar du varje post med ett komma. |
| [!UICONTROL Error Email Sender] | Webbplats | Identifierar den butikskontakt som visas som avsändare av felmeddelandet. Standardavsändare: `General Contact` |
| [!UICONTROL Error Email Template] | Webbplats | Anger mallen som används som bas för felmeddelandet. Standardmall: `Currency Update Warnings` |

{style="table-layout:auto"}
