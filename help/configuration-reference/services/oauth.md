---
title: '[!UICONTROL Services] &gt; [!UICONTROL OAuth]'
description: Granska konfigurationsinställningarna på [!UICONTROL Services] &gt; [!UICONTROL OAuth] sidan för Commerce Admin.
exl-id: 984793e0-6ac9-443b-b234-e0cea717dada
feature: Configuration, Security
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# [!UICONTROL Services] > [!UICONTROL OAuth]

{{config}}

## [!UICONTROL Access Token Expiration]

![Åtkomsttokenets förfallodatum](./assets/oauth-token-expire.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Customer Token Lifetime (hours]) | Global | Fastställer tiden i timmar innan en kund-API-token upphör att gälla. Kundtoken upphör aldrig att gälla om fältet är tomt. Standardvärde: `1` |
| [!UICONTROL Admin Token Lifetime (hours)] | Global | Fastställer hur lång tid i timmar som en API-token för administratörer ska förfalla. Admin-token upphör aldrig att gälla om fältet är tomt. Standardvärde: `4` |

{:style=&quot;table-layout:auto&quot;}

>[!NOTE]
>
>Livstid och krypteringsalgoritmer för Bearer-kund och Admin API-token styrs av [JWT-autentisering](magento-web-api.md#jwt-authentication) konfigurationsinställningar.

## [!UICONTROL Cleanup Settings]

![Rensningsinställningar](./assets/oauth-cleanup.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Cleanup Probability] | Global | Anger antalet OAuth-begäranden innan rensning startas. Ange inte `0` för att inaktivera rensning. |
| [!UICONTROL Enable WSDL Cache] | Global | Fastställer posernas ålder i minuter, innan de rensas. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Consumer Settings]

![Konsumentinställningar](./assets/oauth-consumer-settings.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL OAuth consumer credentials HTTP Post timeout] | Global | Anger hur många sekunder det tar för systemet att timeout inträffar när kunderna skickar sina inloggningsuppgifter. |
| [!UICONTROL OAuth consumer credentials HTTP Post maxredirects] | Global | Anger det maximala antalet omdirigeringar som är relaterade till en publicering av konsumentreferenser. |
| [!UICONTROL Expiration Period] | Global | Anger antalet sekunder innan en oanvänd nyckel/hemlighet upphör att gälla efter att OAuth-tokenutbytet börjar. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Authentication Locks]

![Autentiseringslås](./assets/oauth-locks.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Maximum Login Failures to Lock Out Account] | Global | Anger maximalt antal autentiseringsfel som ska låsa ut kontot. |
| [!UICONTROL Lockout Time (seconds)] | Global | Anger den tidsperiod i sekunder efter vilken kontot låses upp. |

{:style=&quot;table-layout:auto&quot;}
