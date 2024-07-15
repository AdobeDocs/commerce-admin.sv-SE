---
title: Hjälp till kunderna
description: När du använder inloggningen som kundfunktion kan du se vad kunderna ser och göra uppdateringar för deras räkning.
exl-id: 6842ae7a-6440-45f1-af18-e6427088d29d
feature: Customers, Customer Service
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Hjälp till kunderna

Ibland behöver kunderna hjälp med beställningen. Butiksadministratörer kan använda _inloggning som kund_, vilket gör att de kan se vad kunden ser och göra uppdateringar för att hjälpa dem.

Alla åtgärder som vidtas när kunden är inloggad tillämpas på den faktiska kundens konto.

När det är aktiverat för en _Admin_ -användare visas knappen _[!UICONTROL Login as Customer]_på flera sidor:

* [Kundredigeringssida](../customers/update-account.md)
* [Sidan Ordervy](../stores-purchase/order-processing.md)
* [Fakturavy page](../stores-purchase/invoices.md)
* [Sidan Leveransvy](../stores-purchase/shipments.md)
* [Visa kreditnota](../stores-purchase/credit-memo-create.md)

![Logga in som kund](assets/login-as-customer.png){width="600" zoomable="yes"}

## Aktivera inloggning som kund

Om du vill aktivera _inloggningen som kund_ måste du aktivera funktionen i din Commerce-instans och sedan aktivera åtkomst för administratörsanvändare med användarrollbehörigheter.

### Aktivera funktionen

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidlisten Admin.

1. Expandera **[!UICONTROL Customers]** i den vänstra panelen och välj **[!UICONTROL Login as Customer]**.

   ![Konfigurationsalternativ - Logga in som kund](../configuration-reference/customers/assets/login-as-customer.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enable Login as Customer]** till `Yes`.

1. _(Valfritt)_ Ange **[!UICONTROL Disable Page Cache for Admin User]** till `No` om du vill aktivera sidcachen när Admin-användaren loggar in som kund.

   >[!WARNING]
   >
   > Om du inaktiverar sidcachen (`Yes` - standard) ser du till att användaren loggar in när kunden får nya, ocachelagrade data.

1. _(Valfritt)_ Ange **[!UICONTROL Store View to Log in]** till `Manual Selection` om du har en konfiguration för flera platser och/eller flera butiker och vill att administratörsanvändaren ska välja butiksvyn när han/hon loggar in som kund.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

### Aktivera åtkomst för administratörsanvändare

1. Gå till **[!UICONTROL System]** > _Behörigheter_ > **[!UICONTROL User Roles]** på sidofältet _Admin_.

1. Klicka på rollen i listan.

1. Klicka på **[!UICONTROL Role Resources]** i den vänstra panelen [!UICONTROL _Rollinformation_].

1. Ändra **[!UICONTROL Role Resources]** på sidan till `Custom`.

   >[!INFO]
   >
   > När det här alternativet är markerat visas resurshierarkin på sidan.

1. Bläddra till det **[!UICONTROL Customers]** överordnade objektet och **[!UICONTROL Login as Customer]**-objektet under. Välj sedan de resurser som du vill aktivera för rollen:

   * **[!UICONTROL Allow Login as Customer]** - Tillåter administratörsanvändaren att använda funktionen _Logga in som kund_.
   * **[!UICONTROL View Login as Customer Log]** - Gör att administratörsanvändaren kan se loggen _Logga in som kund_.

   ![Rollresurser - Logga in som kund](assets/customers-login-as-customer-role-resources.png){width="400" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Role]**.

## Logga in som kund från administratören

1. Gå till **[!UICONTROL Customers]** > [!UICONTROL _Alla kunder_] på sidofältet _Admin_.

1. Öppna en användare i redigeringsläge.

1. Välj avsnittet **[!UICONTROL Account Information]** på panelen **[!UICONTROL Customer Information]**.

1. Ange **[!UICONTROL Allow remote shopping assistance]** som `Yes`.

   >[!INFO]
   >
   >Administratören kan nu logga in som en användare utan tillstånd från butiken.

## Kundkontobehörighet för fjärrshoppingassistans

Om du vill aktivera kontoåtkomst för butiksupporten från administratören måste kunden aktivera funktionen för sitt konto:

1. Kunden går till sidan **[!UICONTROL Account Information]**.

1. Markerar kryssrutan **[!UICONTROL Allow remote shopping assistance]**.

1. Kunden klickar på **[!UICONTROL Save]**.

![Sidan med kontoinformation](assets/permission.png){width="700" zoomable="yes"}

>[!WARNING]
>
>Utan den här behörigheten kan en Admin-användare inte logga in som den här kunden.

## Använd inloggning som kund

>[!INFO]
>
>Om du vill använda _inloggning som kund_ kontrollerar du att administratören har konfigurerats enligt beskrivningen ovan.

_Logga in som kund_ gör att du kan se webbplatsen på samma sätt som kunden gör, och du kan felsöka och vidta andra åtgärder för kunden. Om du har en tilldelad användarroll med nödvändig behörighet:

1. Du kan klicka på **[!UICONTROL Login as Customer]** på sidorna i föregående avsnitt.
1. Inloggningen som kund-åtgärder finns i åtgärdsrapporten.

>[!WARNING]
>
>Alla åtgärder som vidtas när [!UICONTROL _loggas in som kund_] (till exempel för att lägga till/ta bort produkter) tillämpas på den faktiska kundens order. På butiken visas en banderoll när du är `logged in as customer_name` för att ge en påminnelse om det speciella läget.

## Logga in som kund

{{ee-feature}}

Adobe Commerce tillhandahåller en loggning för _inloggningen som kund_-åtgärder. Den innehåller alla sessioner där en Admin-användare får åtkomst till funktionen. Gå till [rapporten för administrationsåtgärder](../systems/action-log-report.md) om du vill få åtkomst till de loggade åtgärderna.

Du kan filtrera rapportinställningen **[!UICONTROL Action Group]** till `Login As Customer` överst på sidan och klicka på **[!UICONTROL Search]**.

![Filtrera åtgärdsrapporten](assets/customers-login-as-customer-log-filter.png){width="700" zoomable="yes"}
