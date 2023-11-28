---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL System]'
description: Granska konfigurationsinställningarna på [!UICONTROL Advanced] &gt; [!UICONTROL System] sidan för Commerce Admin.
exl-id: ffdaf7b5-c508-4fab-93ec-21f28cff6d3d
role: Admin, Developer
feature: Configuration, System
source-git-commit: 1f84bf9ab20aeccacf56eab396b2778140964d17
workflow-type: tm+mt
source-wordcount: '1592'
ht-degree: 0%

---

# [!UICONTROL Advanced] > [!UICONTROL System]

{{config}}

## [!UICONTROL Cron (Scheduled Tasks)]

![Avancerad konfiguration - Kron (schemalagda aktiviteter)](./assets/system-cron.png)<!-- zoom -->

Mer information om hur du ändrar dessa konfigurationsinställningar finns i [Cron (schemalagda aktiviteter)](../../systems/cron.md).

### [!UICONTROL index]

![Avancerad konfiguration - cron Group: Index](./assets/system-cron-group-index.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Generate Schedules Every] | Global | Anger frekvensen i minuter som scheman genereras. |
| [!UICONTROL Schedule Ahead for] | Global | Anger antalet minuter i förväg som scheman genereras. |
| [!UICONTROL Missed if Not Run Within] | Global | Fastställer antalet minuter innan ett cron-jobb som ännu inte har körts markeras som missat. |
| [!UICONTROL History Cleanup Every] | Global | Anger antalet minuter som förflyter innan kron-historiken rensas. |
| [!UICONTROL Success History Lifetime] | Global | Anger det antal minuter som posten för slutförda kronijobb sparas i databasen. |
| [!UICONTROL Failure History Lifetime] | Global | Anger det antal minuter som posten med misslyckade kronijobb sparas i databasen. |
| [!UICONTROL Use Separate Process] | Global | Avgör om cron-jobb utförs parallellt som separata processer. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL default]

![Kronsgrupp: Standard](./assets/system-cron-group-default.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Generate Schedules Every] | Global | Anger frekvensen i minuter som scheman genereras. |
| [!UICONTROL Schedule Ahead for] | Global | Anger antalet minuter i förväg som scheman genereras. |
| [!UICONTROL Missed if Not Run Within] | Global | Fastställer antalet minuter innan ett cron-jobb som ännu inte har körts markeras som missat. |
| [!UICONTROL History Cleanup Every] | Global | Anger antalet minuter som förflyter innan kron-historiken rensas. |
| [!UICONTROL Success History Lifetime] | Global | Anger det antal minuter som posten för slutförda kronijobb sparas i databasen. |
| [!UICONTROL Failure History Lifetime] | Global | Anger det antal minuter som posten med misslyckade kronijobb sparas i databasen. |
| [!UICONTROL Use Separate Process] | Global | Avgör om cron-jobb utförs parallellt som separata processer. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL MySQL Message Queue Cleanup]

{{ee-feature}}

![Avancerad konfiguration - rensning av MySQL-meddelandekö](./assets/system-mysql-message-queue-cleanup.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Successful Messages Lifetime] | Global | Anger livslängden för slutförda meddelanden i minuter. Ange noll om du vill hoppa över rensningen. Standard: `10080` (7 dagar) |
| [!UICONTROL New Messages Lifetime] | Global | Anger livslängden för nya meddelanden i minuter. Ange noll om du vill hoppa över rensningen. Standard: `10080` (7 dagar) |
| [!UICONTROL Failed Messages Lifetime] | Global | Anger livslängden för misslyckade meddelanden i minuter. Ange noll om du vill hoppa över rensningen. Standard: `10080` (7 dagar) |
| [!UICONTROL Retry Messages in Progress After] | Global | Avgör hur länge systemet väntar på ett meddelande innan det försöker igen. Standard: `1440` (24 timmar) |

{style="table-layout:auto"}

## [!UICONTROL Mail Sending Settings]

![Avancerad konfiguration - Inställningar för e-postsändning](./assets/system-mail-sending-settings.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Konfigurera e-postkommunikation](../../systems/email-communications.md) i _Handbok för adminsystem_.

>[!IMPORTANT]
>
>**Säkerhetsmeddelande** Vi rekommenderar att alla handlare omedelbart ställer in sin konfiguration för att skicka e-post för att skydda mot en nyligen identifierad potentiell fjärrexekvering av kod. Du bör undvika att använda [!DNL Sendmail] för e-postkommunikation. I [!UICONTROL Mail Sending Settings]måste du se till att [!UICONTROL Set Return Path] är inställd på `No`.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Disable Email Communications] | Butiksvy | Avgör om e-postkommunikation är aktiverad för butiken. Alternativ: `Yes` / `No` |
| [!UICONTROL Transport] | Butiksvy | Bestämmer transporttypen för e-postkommunikation från butiken. Alternativ: `Sendmail` / `SMTP` |
| [!UICONTROL Host] | Butiksvy | (Endast för SMTP- och Windows-servrar) Anger namnet som används för att referera till värden. Standardvärde: `localhost` |
| [!UICONTROL Port (25)] | Butiksvy | (Endast för SMTP- och Windows-servrar) Identifierar porten som används för e-postkommunikation. Standardvärde: `25` |
| [!UICONTROL Set Return-Path] | Butiksvy | Avgör om en routningsadress används för returnerade e-postmeddelanden. Alternativ: `No` / `Yes` / `Specified` |

{style="table-layout:auto"}

### SMTP-alternativ

När du väljer SMTP vid transporttypen finns det ytterligare alternativ för att konfigurera SMTP-serveranslutningen.

![Avancerad konfiguration - Inställningar för e-postsändning med SMTP](./assets/system-mail-sending-settings-smtp.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Username] | Butiksvy | Inloggningsanvändarnamn för SMTP-servern. |
| [!UICONTROL Password] | Butiksvy | Lösenord för inloggning på SMTP-servern. |
| [!UICONTROL Auth] | Butiksvy | Bestämmer autentiseringstypen för SMTP-serveranslutningen. Alternativ: `NONE` / `PLAIN` / `LOGIN` |
| [!UICONTROL SSL] | Butiksvy | Bestämmer verifieringstyp för värdsäkerhetscertifikatet. Alternativ: `SSL` / `TLS` |

{style="table-layout:auto"}

## [!UICONTROL Currency]

![Avancerad konfiguration - Valuta](./assets/system-currency.png)<!-- zoom -->

Mer information om hur du ändrar den här inställningen finns i [Valutakonfiguration](../../stores-purchase/currency-configuration.md) i _Butiks and Purchase Experience Guide_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Installed Currencies] | Global | Anger de valutor som för närvarande är tillgängliga för Commerce-installationen. Alternativen omfattar alla tillgängliga valutor, med installerade valutor valda. |

{style="table-layout:auto"}

## [!UICONTROL Security]

![Avancerad konfiguration - säkerhet](./assets/system-security.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Sessionshantering](../../systems/security-session-management.md) i _Handbok för adminsystem_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Max Session Size in Admin] | Global | Begränsa den maximala sessionsstorleken i byte. Använd `0` för att inaktivera. |
| [!UICONTROL Max Session Size in Storefront] | Global | Begränsa den maximala sessionsstorleken i byte. Använd `0` för att inaktivera. |

{style="table-layout:auto"}

## [!UICONTROL Notifications]

![Avancerad konfiguration - meddelanden](./assets/system-notifications.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Systemmeddelanden](../../systems/notifications.md) i _Handbok för adminsystem_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Use HTTPS to Get Feed] | Global | Avgör om administratörsmeddelanden levereras via en säker kanal. Alternativ: `Yes` / `No` |
| Uppdateringsfrekvens | Global | Anger frekvensen för uppdateringar av administratörsmeddelanden. Alternativ: `1 Hour` / `2 Hours` / `6 Hours` / `12 Hours` / `24 Hours` |
| [!UICONTROL Last Update] | Global | Anger datum och tid för den senaste meddelandeuppdateringen. |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Backup Settings]

![Avancerad konfiguration - Inställningar för schemalagd säkerhetskopiering](./assets/system-scheduled-backup-settings.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Säkerhetskopiering av system](../../systems/backups.md) i _Handbok för adminsystem_.

{{$include /help/_includes/backups-note.md}}

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Scheduled Backup] | Global | Avgör om Commerce-instansen automatiskt säkerhetskopieras enligt ett regelbundet schema. Alternativ: `Yes` / `No` |
| [!UICONTROL Backup Type] | Global | Anger vilka element i Commerce-instansen som ingår i säkerhetskopian. Alternativ: `Database` / `Database and Media` / `System` / `System (excluding Media)` |
| [!UICONTROL Start Time] | Global | Anger timmen, minuten och sekunden då den schemalagda säkerhetskopieringen börjar. |
| [!UICONTROL Frequency] | Global | Avgör hur ofta den schemalagda säkerhetskopieringen sker. Alternativ: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Maintenance Mode] | Global | Anger om butiken är i underhållsläge under den schemalagda säkerhetskopieringen. Alternativ: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Actions Log Archiving]

{{ee-feature}}

![Avancerad konfiguration - Loggarkivering för administratörsåtgärder](./assets/system-admin-actions-log-archiving.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Åtgärdsloggarkiv](../../systems/action-log-archive.md) i _Handbok för adminsystem_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Log Entry Lifetime, Days] | Butiksvy | Anger antalet dagar som administratörsåtgärder sparas i arkivet med administratörsåtgärder. Standard: `60` |
| [!UICONTROL Log Archiving Frequency] | Butiksvy | Anger hur ofta administratörsåtgärdsloggarna arkiveras. Alternativ: `Daily` / `Weekly` / `Monthly` |

{style="table-layout:auto"}

## [!UICONTROL Full Page Cache]

{{beta2-patches-updates}}

![Avancerad konfiguration - helsidescache](./assets/system-full-page-cache.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Cachelagring](../../systems/cache-management.md#full-page-caching) i _Handbok för adminsystem_.

![Avancerad konfiguration - Slutgiltig konfiguration](./assets/system-full-page-cache-varnish.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Caching Application] | Global | Bestämmer vilket program som används för att hantera helsidescachen. Alternativ: <br/>**`Built-in Application`**- Rekommenderas inte för produktionsmiljön.<br/>**`Varnish Caching`** - Rekommenderas för produktionsmiljön. |
| [!UICONTROL TTL for public content] | Global | Anger livslängden för cacheminnet för offentligt innehåll i sekunder. Standardvärde: `120` |
| **[!UICONTROL Varnish Configuration]** |  |  |
| [!UICONTROL Access list] | Global | Anger de IP-adresser som kan tömma konfigurationen för lack för att generera en konfigurationsfil. Avgränsa flera poster med komma. Standardvärde: `localhost` |
| [!UICONTROL Backend host] | Global | Anger den serverdelsvärd som genererar konfigurationsfiler. Standardvärde: `localhost` |
| [!UICONTROL Backend port] | Global | Anger den serverdelsport som används för att generera konfigurationsfiler. Standardvärde: `8080` |
| [!UICONTROL Grace period] | Global | Anger respitperioden i sekunder för generering av en konfigurationsfil. Standardvärde: `300` |
| **[!UICONTROL Export Configuration]** |  |  |
| [!UICONTROL Export VCL for Varnish 4] | Global | Exporterar `varnish.vcl` för version 4. |
| [!UICONTROL Export VCL for Varnish 5] | Global | Exporterar `varnish.vcl` för version 5. |
| [!UICONTROL Export VCL for Varnish 6] | Global | Exporterar `varnish.vcl` för version 6. |

{style="table-layout:auto"}

## [!UICONTROL Storage Configuration for Media]

![Avancerad konfiguration - lagringskonfiguration för media - filsystem](./assets/system-storage-config-media.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Använda en mediedatabas](../../content-design/media-storage-database.md) i _Content and Design Guide_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Media Storage] | Global | Bestämmer vilken metod som ska användas för att lagra mediefiler. Standardinställning: `File System` |
| [!UICONTROL Environment Update Time] | Global | Anger hur ofta mediefilens miljö uppdateras i sekunder. Standardvärde: `3600` |

{style="table-layout:auto"}

![Avancerad konfiguration - lagringskonfiguration för media - databas](./assets/database-storage-deprecated.png)<!-- zoom -->

>[!IMPORTANT]
>
>Databasmedielagringsmetoden används inte i Adobe Commerce och Magento Open Source 2.4.3.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Media Storage] | Global | Anger databasen som den metod som används för att lagra mediefiler. |
| [!UICONTROL Select Media Database] | Global | Identifierar namnet på databasen som används för medielagring. Standardinställning: `default_setup` |
| [!UICONTROL Synchronize] |  | Synkroniserar överföringen av alla media till den angivna databasplatsen. |
| Uppdateringstid för miljö | Global | Anger hur ofta mediefilens miljö uppdateras i sekunder. Standardvärde: `3600` |

{style="table-layout:auto"}

## [!UICONTROL Bulk Actions]

{{ee-feature}}

![Avancerad konfiguration - Massåtgärder](./assets/system-bulk-actions.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Massåtgärder](../../systems/action-log-bulk-actions.md) i _Handbok för adminsystem_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Days Saved in Log] | Global | Anger antalet dagar som massåtgärder sparas i _Logg för gruppåtgärd_ arkiv. Standard: `60` |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Import/Export File History Cleaning]

{{ee-feature}}

![Avancerad konfiguration - rensning av schemalagd import/export av filhistorik](./assets/system-schedule-history-cleaning.png)<!-- zoom -->

Mer information om hur du ändrar de här inställningarna finns i [Schemalagd import och export](../../systems/data-scheduled-import-export.md) i _Handbok för adminsystem_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Save File, Days] | Global | Anger hur många dagar som historikfiler för import/export sparas. |
| [!UICONTROL Enable Scheduled File History Cleaning] | Global | Aktiverar schemalagd rensning av import-/exportfiler. Alternativ: `Yes` / `No` |
| [!UICONTROL Clean Now] |  | Åsidosätter den schemalagda rensningen och rensar omedelbart import-/exporthistorikfilerna. |
| [!UICONTROL Start Time] | Global | Anger timme, minut och sekund för rensning av import-/exporthistorikfilen. |
| [!UICONTROL Frequency] | Global | Anger hur ofta import-/exporthistorikfilerna rensas. Alternativ: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | Global | E-postadressen till den person som ska få ett meddelande om ett fel inträffar när import-/exportfilhistoriken rensas. Avgränsa flera adresser med komma. |
| [!UICONTROL Error Email Sender] | Global | Identifierar den butikskontakt som visas som meddelandets avsändare. Standardavsändare: `General Contact` |
| [!UICONTROL Error Email Template] | Global | Identifierar den e-postmall som används för rensningsfelmeddelanden för import/export av filer. Standardmall: `File History Clean Failed` |

{style="table-layout:auto"}

## [!UICONTROL Image Upload Configuration]

![Avancerad konfiguration - konfiguration för bildöverföring](./assets/system-image-upload-configuration.png)<!-- zoom -->

<!-- [Image Upload Configuration](https://docs.magento.com/user-guide/system/action-log-bulk-actions.html) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Quality] | Global | Anger JPG-kvaliteten för den storleksändrade bilden. Lägre kvalitet minskar filstorleken. Använd 80-90 % för att minska filstorleken med hög kvalitet. Standard: `80` |
| [!UICONTROL Enable Frontend Resize] | Global | Aktivera den här inställningen för att tillåta Commerce att ändra storlek på stora, stora bilder som du kan överföra för _Produktinformation_ sida. I Commerce ändras bildfilernas storlek med JavaScript innan filen överförs. När bildens storlek ändras behålls de exakta proportionerna och den största storleken för Maximal bredd och Maximal höjd får inte överskridas. Standard: `Yes` |
| [!UICONTROL Maximum Width] | Global | Anger bildens maximala pixelbredd. När bildens storlek ändras överskrider den inte denna bredd. Standard: `1920` |
| [!UICONTROL Maximum Height] | Global | Anger bildens maximala pixelhöjd. När bildens storlek ändras överskrider den inte den här höjden. Standard: `1200` |

{style="table-layout:auto"}

## [!UICONTROL Media Gallery]

![Avancerad konfiguration - Mediegalleri](./assets/system-media-gallery.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Old Media Gallery] | Global | Aktiverar eller inaktiverar det gamla mediegalleriet. |

{style="table-layout:auto"}

## [!UICONTROL Media Gallery Image Optimization]

![Avancerad konfiguration - Bildoptimering i Mediegalleriet](./assets/system-media-image-optimization.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Image Optimization] | Global | Avgör om bildens storlek ändras för att minska filstorleken på de bilder som infogas i innehållet. Originalbilder bevaras i Mediegalleriet. |
| [!UICONTROL Maximum Width] | Global | Den maximala bredden (i pixlar) för bilder som infogats från Mediegalleriet i innehållet. |
| [!UICONTROL Maximum Height] | Global | Den maximala höjden (i pixlar) för bilder som infogats från Mediegalleriet i innehållet. |

{style="table-layout:auto"}

## [!UICONTROL Adobe Stock Integration]

![Avancerad konfiguration - integrering med Adobe Stock](./assets/system-adobe-stock-integration.png)<!-- zoom -->

Mer information om hur du konfigurerar de här inställningarna finns i [Adobe Stock Integration](../../content-design/adobe-stock.md) i _Content and Design Guide_.

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enabled Adobe Stock] | Global | Aktiverar eller inaktiverar Adobe Stock Integration. |
| [!UICONTROL API Key (Client ID)] | Global | Det krävs en API-nyckel för att ansluta butiken till Adobe Stock-tjänsten. |
| [!UICONTROL Client Secret] | Global | Klienthemlighet för Adobe Stock-integrering krävs. |
| [!UICONTROL Test Connection] |  | Kör ett test för att verifiera att API-nyckeln är giltig för användning med Adobe Stock-tjänsten. |

{style="table-layout:auto"}
