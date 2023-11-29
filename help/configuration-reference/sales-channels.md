---
title: '[!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings]'
description: Granska konfigurationsinställningarna på [!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings] sidan för Commerce Admin.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

Dessa inställningar är tillgängliga när [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html) är installerat.

![Inställningar för Sales Channel](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| Fält | [Omfång](../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|-----|---------|------|
| [!UICONTROL Clear Log History] | Global | Alternativ:<br/><br/>**`Once Daily`**: Välj det här alternativet om du vill rensa butikens aktivitetshistorik en gång om dagen.<br/><br/>**`Once Weekly`**: Välj det här alternativet om du vill rensa butikens aktivitetshistorik en gång i veckan.<br/><br/>**`Once Monthly`**: (Standard) Välj det här alternativet om du vill ta bort butikens aktivitetshistorik en gång i månaden. |
| [!UICONTROL Background Tasks (CRON) Source] | Global | Välj `Magento CRON` för att ange att [!DNL Amazon Sales Channel] använder dina Commerce cron-inställningar för att fastställa kommunikations- och datasynkroniseringsintervall med Amazon Seller Central. |
| [!UICONTROL Enable Debug Logging] | Global | Välj `Enabled` för att samla in ytterligare synkroniseringsdata när felsökning behövs.<br/><br/>Det här alternativet är inaktiverat som standard och bör endast aktiveras när det behövs för felsökning, eftersom fortsatt loggning påverkar prestandan negativt. Om den är aktiverad för felsökning bör den vara inaktiverad när den är klar.<br/><br/>**_Anteckning _**: Amazon loggning av Sales Channeler skrivs till `/var/log/channel_amazon.log` och kan visas i [utvecklarläge](../systems/developer-tools.md#operation-modes). |
| [!UICONTROL Read-Only Mode] | Global | Välj `Enabled` för att blockera alla utgående API-begäranden som ändrar tillstånd. Möjliga ändringar sparas, men skickas inte, förrän skrivskyddat läge har inaktiverats. Om du vill starta dataöverföringen igen väljer du `Disabled`.<br/><br/>När en databas migreras till en ny kopia av instansen (identifieras när en butiks URL ändras i konfigurationen) aktiveras skrivskyddat läge automatiskt.<br/><br/>Detta är avsett att användas på kopior av produktionsinstansen, som _Mellanlagring_ eller _QA_ och ska inte användas i produktionsinstansen.<br/><br/>**_Anteckning _**: Konfigurationscachen måste rensas för [!UICONTROL Read-Only Mode] för att aktivera. |

{style="table-layout:auto"}
