---
title: '[!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings] i Commerce Admin.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

De här inställningarna är tillgängliga när [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html?lang=sv-SE) installeras.

![Inställningar för Sales Channel](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| Fält | [Omfång](../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|-----|---------|------|
| [!UICONTROL Clear Log History] | Global | Alternativ:<br/><br/>**`Once Daily`**: Välj det här alternativet om du vill rensa butikens aktivitetshistorik en gång om dagen.<br/><br/>**`Once Weekly`**: Välj det här alternativet om du vill rensa butikens aktivitetshistorik en gång i veckan.<br/><br/>**`Once Monthly`**: (Standard) Välj det här alternativet om du vill ta bort butikens aktivitetshistorik en gång i månaden. |
| [!UICONTROL Background Tasks (CRON) Source] | Global | Välj `Magento CRON` om du vill ange att [!DNL Amazon Sales Channel] använder dina Commerce kron-inställningar för att fastställa kommunikations- och datasynkroniseringsintervall med Amazon Seller Central. |
| [!UICONTROL Enable Debug Logging] | Global | Välj `Enabled` om du vill samla in ytterligare synkroniseringsdata när felsökning behövs.<br/><br/>Det här alternativet är inaktiverat som standard och bör endast aktiveras när det behövs för felsökning, eftersom fortsatt loggning påverkar prestandan negativt. Om den är aktiverad för felsökning bör den vara inaktiverad när den är klar.<br/><br/>**_Obs!_**&#x200B;Amazon Sales Channel-loggning skrivs till filen `/var/log/channel_amazon.log` och kan visas i [utvecklarläge](../systems/developer-tools.md#operation-modes). |
| [!UICONTROL Read-Only Mode] | Global | Välj `Enabled` om du vill blockera alla utgående API-begäranden som ändrar tillståndet. Möjliga ändringar sparas, men skickas inte, förrän skrivskyddat läge har inaktiverats. Om du vill starta dataöverföringar igen väljer du `Disabled`.<br/><br/>När en databas migreras till en ny kopia av instansen (identifieras när arkivets URL ändras i konfigurationen) aktiveras skrivskyddat läge automatiskt.<br/><br/>Detta är utformat för att användas på kopior av produktionsinstansen, som _Förproduktion_ eller _QA_, och bör inte användas på produktionsinstansen.<br/><br/>**_Obs!_**: Konfigurationscachen måste rensas för att [!UICONTROL Read-Only Mode] ska kunna aktiveras. |

{style="table-layout:auto"}
