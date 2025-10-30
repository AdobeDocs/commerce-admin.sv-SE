---
title: Anteckning om val av USPS API-typ
description: Återanvänd anteckning om säkerhetskopiering
source-git-commit: 556b8d5556e3351eaee827c6b32fe09a247f5395
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Konfigurationsalternativ för USPS API-typ

>[!NOTE]
>
>Dessa instruktioner innehåller steg för att välja USPS API-typ för integrering: Web Tools API eller REST API:er. Konfigurationsalternativen för API-typ är bara tillgängliga om du har tillämpat kvalitetskorrigeringen [USPS REST API Migration](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/usps-rest-api-migration-patch.html) (AC-1520) på ditt Commerce-program. Om du inte har tillämpat korrigeringen är API-typväljaren inte tillgänglig och API:t för USPS Web Tools används som standard.<br>USPS-API:erna är den rekommenderade metoden för integrering med USPS. USPS Web Tools API är föråldrat och kan tas bort i framtida versioner.
