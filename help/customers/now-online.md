---
title: Kunder som nu är online
description: Alternativet _Now Online_ på [!UICONTROL Customers ]listar alla kunder och besökare som för närvarande är online i din butik.
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# Kunder som nu är online

The **[!UICONTROL Now Online]** på [!DNL Customers] listar alla kunder och besökare som för närvarande är online i din butik. Det tidsintervall som kunderna visas som online anges i konfigurationen och avgör hur länge [!DNL Customer's] aktiviteten visas från Admin. Som standard är intervallet 15 minuter. Sessionen avslutas om tangentbordet inte används under tiden och kunderna måste logga in på sina konton igen för att kunna fortsätta handla. Det är viktigt att notera att innehållet i kundvagnen sparas för senare åtkomst.

![Onlinekunder](assets/customers-now-online.png){width="700" zoomable="yes"}

Kundernas onlinestatus uppdateras endast vid kundinloggning, registrering eller andra händelser som förändras i det aktuella läget. Det innehåller kundvagnsrelaterade händelser, som att lägga till, ta bort och ändra produkter.

>[!NOTE]
>
>Enbart sidbesök uppdaterar inte kundens onlinestatus. För att samla in sådan information rekommenderas [konfigurera Google Analytics](../merchandising-promotions/google-analytics.md) (ensam eller med [Google Tag Manager](../merchandising-promotions/google-tag-manager.md)) eller använda andra analysprogram med Adobe Commerce.

## Se alla kunder online

På _Administratör_ sidebar, gå till **[!UICONTROL Customers]** > **[!UICONTROL Online Now]**.

>[!TIP]
>
>Mer information om hur du hjälper en onlinekund att slutföra ett köp finns på [Shoppingassistans](../stores-purchase/introduction.md#shopping-assistance).

## Konfigurera tidsintervallet

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Customers]** och välja **[!UICONTROL Customer Configuration]**.

1. Expandera **[!UICONTROL Online Customers Options]** och gör följande:

   ![Kundalternativ online](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - För **[!UICONTROL Online Minutes Interval]** anger du antalet minuter som kundsessionen ska visas från administratören. Lämna fältet tomt om du vill acceptera standardintervallet på 15 minuter.

   - För **[!UICONTROL Customer Data Lifetime]** anger du antalet minuter innan osparade data som anges av kunden förfaller.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Kolumnbeskrivningar

| Kolumn | Beskrivning |
| --- | --- |
| **[!UICONTROL ID]** | Kund-ID för en registrerad kund. |
| **[!UICONTROL First Name]** | Förnamnet på en registrerad kund. |
| **[!UICONTROL Last Name]** | Efternamnet på en registrerad kund. |
| **[!UICONTROL Email]** | E-postadressen till en registrerad kund. |
| **[!UICONTROL Last Activity]** | Datum och tid för kundens senaste aktivitet i din butik. |
| **[!UICONTROL Type]** | Alternativ: `Customer` / `Visitor` |
| **[!UICONTROL Last URL]** | Den sista URL som kunden besökte. |
| **[!UICONTROL Company]** | Namnet på det företag som användaren tillhör. |

{style="table-layout:auto"}
