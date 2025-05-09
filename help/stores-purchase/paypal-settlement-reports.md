---
title: Rapport över PayPal-kvittning
description: Läs mer om PayPal-kvittningsrapporten som ett verktyg för att hantera PayPal-transaktioner.
exl-id: cd087e15-e6ad-4472-9038-8c64fde316f9
feature: Payments
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Rapport över PayPal-kvittning

PayPal-kvittningsrapporten förser handlarna med information om varje transaktion som påverkar kvittningen av medel.

>[!NOTE]
>
>Innan kvittningsrapporter genereras måste butiksadministratören begära att PayPal Merchant Technical Services skapar ett SFTP-användarkonto, aktiverar generering av kvittningsrapporter och aktivera SFTP i PayPals affärskonto.

När du har konfigurerat och aktiverat avvecklingsrapporter på PayPal-handelskontot kommer Adobe Commerce och Magento Open Source att börja generera rapporter under de följande 24 timmarna. Listan med tillgängliga kvittningsrapporter kan visas från administratören.

**_Så här visar du kvittningsrapporter:_**

1. Gå till **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**&#x200B;på sidofältet_ Admin _.

   ![PayPal-kvittningsrapporter](../getting-started/assets/reports-sales-paypal-settlement.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Fetch Updates]** i det övre högra hörnet för de senaste uppdateringarna.

   Systemet ansluter till PayPal SFTP-servern för att hämta rapporterna. När processen är klar visas ett meddelande med antalet rapporter som har hämtats. Rapporten innehåller följande information för varje transaktion:

   | Rapportkolumn | Beskrivning |
   | ------------ | ----------- |
   | [!UICONTROL PayPal Reference ID Type] | En av följande referenskoder:<br/>- Order-IDT<br/>- Transaction ID<br/>- Subscription ID |
   | [!UICONTROL Preapproved Payment ID] | **[!UICONTROL Custom]** - Den text som handlaren anger i transaktionen på PayPal.<br/>**[!UICONTROL Transaction Debit or Credit]**- Riktningen för penningförflyttning av bruttobelopp.<br/>**[!UICONTROL Fee Debit or Credit]** - Riktningen för penningförflyttning mot avgift. |

   {style="table-layout:auto"}
