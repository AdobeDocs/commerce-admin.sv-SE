---
title: Kunder som nu är online
description: Alternativet _Now Online_ på menyn [!UICONTROL Customers ]visar alla kunder och besökare som för närvarande är online i din butik.
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# Kunder som nu är online

Alternativet **[!UICONTROL Now Online]** på menyn [!DNL Customers] visar alla kunder och besökare som för närvarande är online i din butik. Det tidsintervall som kunder visas som online anges i konfigurationen och avgör hur lång tid [!DNL Customer's]-aktiviteten är synlig från administratören. Som standard är intervallet 15 minuter. Sessionen avslutas om tangentbordet inte används under tiden och kunderna måste logga in på sina konton igen för att kunna fortsätta handla. Det är viktigt att notera att innehållet i kundvagnen sparas för senare åtkomst.

![Onlinekunder](assets/customers-now-online.png){width="700" zoomable="yes"}

Kundernas onlinestatus uppdateras endast vid kundinloggning, registrering eller andra händelser som förändras i det aktuella läget. Det innehåller kundvagnsrelaterade händelser, som att lägga till, ta bort och ändra produkter.

>[!NOTE]
>
>Enbart sidbesök uppdaterar inte kundens onlinestatus. Om du vill samla in sådan information bör du [konfigurera Google Analytics](../merchandising-promotions/google-analytics.md) (fristående eller med [Google Tag Manager](../merchandising-promotions/google-tag-manager.md)) eller använda andra analysprogram med Adobe Commerce.

## Se alla kunder online

Gå till **[!UICONTROL Customers]** > **[!UICONTROL Online Now]** på sidofältet _Admin_.

>[!TIP]
>
>Mer information om hur du kan hjälpa en onlinekund att slutföra ett köp finns i [Shoppinghjälp](../stores-purchase/introduction.md#shopping-assistance).

## Konfigurera tidsintervallet

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Customers]** i den vänstra panelen och välj **[!UICONTROL Customer Configuration]**.

1. Expandera avsnittet **[!UICONTROL Online Customers Options]** och gör följande:

   ![Alternativ för onlinekunder](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - För **[!UICONTROL Online Minutes Interval]** anger du antalet minuter som kundsessionen ska vara synlig från administratören. Lämna fältet tomt om du vill acceptera standardintervallet på 15 minuter.

   - För **[!UICONTROL Customer Data Lifetime]** anger du antalet minuter innan osparade data som anges av kunden förfaller.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

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
