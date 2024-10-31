---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Gift Registry]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Customers] &gt; [!UICONTROL Gift Registry] i Commerce Admin.
exl-id: c5153c4e-897a-41d2-bde1-8483855d1a37
feature: Configuration, Gift
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Gift Registry]

{{ee-feature}}

{{config}}

Mer information om hur du använder dessa inställningar för att aktivera presentregister för dina butikskunder finns i [Konfigurera presentregister](../../merchandising-promotions/gift-registry-configure.md). Mer information om hur du inkluderar sökning i presentregistret i butiken finns i [Lägg till sökning i presentregistret](../../merchandising-promotions/gift-registry-search.md).

## [!UICONTROL General Options]

![Allmänna alternativ](./assets/gift-registry-general-options.png)<!-- zoom -->

<!-- [General Options](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Enable Gift Registry] | Butiksvy | Avgör om presentregister är tillgängliga. Alternativ: <br/>**`Yes`**- Aktiverar presentregister för den valda butiksvyn. Fliken Presentregister visas på kontouppsättningen med registrerade kunder.<br/>**`No`** - Presentregister är inte tillgängliga för butiksvyn. |
| [!UICONTROL Maximum Registrants] | Butiksvy | Anger antalet personer som en kund kan lägga till i ett presentregister. Kunden delar presentregistret med varje registrant. I butiken är knappen _Lägg till registrant_ tillgänglig för kunder tills maximalt antal nås. |

{style="table-layout:auto"}

## [!UICONTROL Owner Notification]

![Ägarmeddelande](./assets/gift-registry-owner-notification.png)<!-- zoom -->

<!-- [Owner Notification](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Email Template] | Butiksvy | Bestämmer vilken mall som används för e-postadressen för ägarmeddelanden som skickas när ett presentregister skapas. Standardmall: Meddelande om ägare av presentregister |
| [!UICONTROL Email Sender] | Butiksvy | Identifierar [butikskontakten](../../getting-started/store-details.md#store-email-addresses) som visas som avsändare av presentatörens meddelandemeddelande. Standardvärde: `General Contact` |

{style="table-layout:auto"}

## Presentregisterdelning

![Presentregisterdelning](./assets/gift-registry-gift-registry-sharing.png)<!-- zoom -->

<!-- Gift Registry Sharing](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Email Template] | Butiksvy | Bestämmer vilken mall som används för e-postmeddelandet om gift-registerdelning som skickas när ett presentregister skapas. När ägaren klickar på _Dela presentregister_ skickas e-postmeddelandet till varje mottagare. Standardmall: `Gift Registry Sharing` |
| [!UICONTROL Email Sender] | Butiksvy | Identifierar den [butikskontakt](../../getting-started/store-details.md#store-email-addresses) som visas som avsändare av e-postmeddelandet om gift-registerdelning. Standardvärde: `General Contact` |
| [!UICONTROL Maximum Sent Emails Threshold] | Butiksvy | Maximalt antal e-postmeddelanden om gift-registerdelning som kan skickas samtidigt. |

{style="table-layout:auto"}

## [!UICONTROL Gift Registry Update]

![Presentregisteruppdatering](./assets/gift-registry-gift-registry-update.png)<!-- zoom -->

<!-- [Gift Registry Update](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--- |--- |--- |
| [!UICONTROL Email Template] | Butiksvy | Bestämmer vilken mall som används för e-postmeddelandet om uppdatering av presentregistret som skickas till presentregisterägaren när ett köp görs från presentregistret. Uppdateringen innehåller information om artikeln och kvantiteten som köpts, men inte namnet på den person som beställt. Standardmall: `Gift Registry Update` |
| [!UICONTROL Email Sender] | Butiksvy | Identifierar [butikskontakten](../../getting-started/store-details.md#store-email-addresses) som visas som avsändare av presentatörens registeruppdatering. Standardvärde: `General Contact` |

{style="table-layout:auto"}
