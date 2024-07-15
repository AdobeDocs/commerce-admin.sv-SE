---
title: Transaktioner
description: Lär dig mer om sidan Transaktioner och hur du använder den för att spåra aktiviteter mellan din butik och ett betalningssystem.
exl-id: 5970db88-146d-4caf-aab4-d9315357a4fe
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Transaktioner

På sidan _Transaktioner_ visas alla betalningsaktiviteter som har utförts mellan din butik och ett betalningssystem, och du får tillgång till mer detaljerad information.

## Visa transaktioner

Gå till **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Transactions]**på sidofältet_ Admin _.

![Transaktionsrutnät](./assets/transactions.png){width="600" zoomable="yes"}

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL ID] | En unik numerisk identifierare som tilldelas varje transaktion. |
| [!UICONTROL Order ID] | En unik identifierare som tilldelas när en kund gör en beställning. |
| [!UICONTROL Transaction ID] | En unik numerisk identifierare som tilldelas när en transaktion inträffar efter att en kund har gjort en beställning. |
| [!UICONTROL Parent Transaction ID] | ID-numret för den överordnade transaktionen. |
| [!UICONTROL Payment Method] | Betalningsmetoden som är associerad med en transaktion. |
| [!UICONTROL Transaction Type] | Typ av transaktion, som kan vara Order, Authorization, Capture, Void eller Refund. |
| [!UICONTROL Closed] | Anger om en transaktion är stängd eller inte. |
| [!UICONTROL Created] | Tid och datum då transaktionen skapades. |

{style="table-layout:auto"}

## Visa transaktionsinformation

Klicka på den post som du vill visa.

På sidan med transaktionsinformation kan du se rutnätet med transaktionsdetaljer och underordnade transaktioner.

### Transaktionsdata

Det här avsnittet innehåller information om transaktionen och en länk till ordersidan i kolumnen **Order ID** .

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Transaction ID] | Transaktions-ID-numret. |
| [!UICONTROL Parent Transaction ID] | Ett motsvarande ID-nummer för den överordnade transaktionen, om tillämpligt. |
| [!UICONTROL Transaction Type] | Typ av transaktion, som kan vara Order, Authorization, Capture, Void eller Refund. |
| [!UICONTROL Is Closed] | Anger om en transaktion är stängd eller inte. |
| [!UICONTROL Created At] | Tid och datum då transaktionen skapades. |

{style="table-layout:auto"}

### Underordnade transaktioner

Underordnade transaktioner visas i rutnätet efter att fakturor för [order](orders.md) har skapats. Med det här formatet kan du spåra transaktionshistorik efter en transaktionshierarki.

### [!UICONTROL Transaction Details]

Det här avsnittet innehåller ytterligare information för en viss transaktion. Informationen visas i form av nycklar och värden. De tillgängliga nycklarna är:

- authAmount
- authCode
- VSResponse
- BillTo
- cardCodeResponse
- kund
- customerIP
- lineItems
- marketType
- beställa
- betalning
- produkt
- återkommandeFakturering
- responseCode
- responseReasonCode
- responseReasonDescription
- settAmount
- lösning
- submitTimeLocal
- submitTimeUTC
- taxExclut
- transactionStatus

>[!NOTE]
>
>Om transaktionsinformationen inte är tillgänglig eller är inaktuell kan du uppdatera den genom att klicka på **[!UICONTROL Fetch]** i knappfältet.
