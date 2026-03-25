---
title: Hjälp till kunderna
description: När du använder inloggningen som kundfunktion kan du se vad kunderna ser och göra uppdateringar för deras räkning.
exl-id: 6842ae7a-6440-45f1-af18-e6427088d29d
feature: Customers, Customer Service
source-git-commit: 29f3a8bb019d464e6d7646e0ebc7a4fa2ed0dd74
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 0%

---

# Hjälp till kunderna

Ibland behöver kunderna hjälp med beställningen. Butiksadministratörer kan använda _inloggning som kund_, vilket gör att de kan se vad kunden ser och göra uppdateringar för att hjälpa dem.

Alla åtgärder som vidtas när kunden är inloggad tillämpas på den faktiska kundens konto.

>[!BEGINTABS]

>[!TAB Adobe Commerce]

[!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."}

När det är aktiverat för en _Admin_ -användare visas knappen _[!UICONTROL Login as Customer]_&#x200B;på flera sidor:

* [Kundredigeringssida](../customers/update-account.md)
* [Sidan Ordervy](../stores-purchase/order-processing.md)
* [Fakturavy page](../stores-purchase/invoices.md)
* [Sidan Leveransvy](../stores-purchase/shipments.md)
* [Visa kreditnota](../stores-purchase/credit-memo-create.md)

![Logga in som kund](assets/login-as-customer.png){width="600" zoomable="yes"}

>[!TAB Adobe Commerce as a Cloud Service]

[!BADGE Endast SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce as a Cloud Service- och Adobe Commerce Optimizer-projekt (SaaS-infrastruktur som hanteras av Adobe)."}

I Adobe Commerce as a Cloud Service använder funktionen Logga in som kund ett **OTC**-arbetsflöde i stället för en direkt inloggning. Administratörer genererar en kortvarig engångskod för en kund. Den här koden kan sedan bytas ut mot en kundåtkomsttoken via GraphQL, vilket möjliggör lösenordslös inloggning som kundarbetsflöden för shoppingscenarier som stöds av säljare.

Funktionen består av följande komponenter:

* **Administratörsgränssnitt** - På kundredigeringssidan kan administratörer begära en engångskod (OTC) i stället för att logga in direkt som kund.
* **[REST API](https://developer.adobe.com/commerce/webapi/rest/saas-integrations/login-as-customer/)** - En programmatisk slutpunkt för OTC-generering, användbar för administratörsskript och tredjepartsintegreringar.
* **GraphQL API** - Mutationer som byter ut en OTC-fil mot en kundåtkomsttoken för butiks- eller headless-handelsflöden.

>[!ENDTABS]

## Aktivera inloggning som kund

Om du vill aktivera _inloggningen som kund_ måste du aktivera funktionen i din Commerce-instans och sedan aktivera åtkomst för administratörsanvändare med användarrollbehörigheter.

### Aktivera funktionen

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidlisten Admin.

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

1. Gå till _>_ Behörigheter **[!UICONTROL System]** > _på sidofältet_ Admin **[!UICONTROL User Roles]**.

1. Klicka på rollen i listan.

1. Klicka på [!UICONTROL _i den vänstra panelen_] Rollinformation **[!UICONTROL Role Resources]**.

1. Ändra **[!UICONTROL Role Resources]** på sidan till `Custom`.

   >[!INFO]
   >
   > När det här alternativet är markerat visas resurshierarkin på sidan.

1. Bläddra till det **[!UICONTROL Customers]** överordnade objektet och **[!UICONTROL Login as Customer]**-objektet under. Välj sedan de resurser som du vill aktivera för rollen:

   * **[!UICONTROL Allow Login as Customer]** - Tillåter administratörsanvändaren att använda funktionen _Logga in som kund_.
   * **[!UICONTROL View Login as Customer Log]** - Gör att administratörsanvändaren kan se loggen _Logga in som kund_.

   ![Rollresurser - Logga in som kund](assets/customers-login-as-customer-role-resources.png){width="400" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Role]**.

## Kundkontobehörighet för fjärrshoppingassistans

Om du vill aktivera kontoåtkomst för butiksupporten från administratören måste kunden aktivera funktionen för sitt konto:

>[!BEGINTABS]

>[!TAB Adobe Commerce]

[!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."}

1. Kunden går till sidan **[!UICONTROL Account Information]**.

1. Markerar kryssrutan **[!UICONTROL Allow remote shopping assistance]**.

1. Kunden klickar på **[!UICONTROL Save]**.

![Sidan med kontoinformation](assets/permission.png){width="700" zoomable="yes"}

>[!TAB Adobe Commerce as a Cloud Service]

[!BADGE Endast SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce as a Cloud Service- och Adobe Commerce Optimizer-projekt (SaaS-infrastruktur som hanteras av Adobe)."}

Kunden måste ha tilläggsattributet `login_as_customer_assistance_allowed` inställt på **2**. Detta kan konfigureras på sidan **Redigera kund** i Admin eller via GraphQL när en kund skapas eller redigeras.

>[!WARNING]
>
>Utan den här behörigheten kan en Admin-användare inte logga in som den här kunden.

![Konfiguration av tilläggsattribut för kundgodkännande på sidan Redigera kund](assets/customer-consent-attribute.png){width="600" zoomable="yes"}

Om du vill ange den här behörigheten med GraphQL för ett befintligt kundkonto anger du `allow_remote_shopping_assistance`-indata till `true` med hjälp av [`updateCustomerV2`](https://developer.adobe.com/commerce/webapi/graphql/schema/customer/mutations/update-v2/)- eller [`createCustomerV2`](https://developer.adobe.com/commerce/webapi/graphql/schema/customer/mutations/create-v2/)-mutationerna.

>[!ENDTABS]

## Logga in som kund från administratören

>[!BEGINTABS]

>[!TAB Adobe Commerce]

[!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."}

1. Gå till _>_ Alla kunder **[!UICONTROL Customers]** på sidofältet [!UICONTROL _Admin_].

1. Öppna en användare i redigeringsläge.

1. Välj avsnittet **[!UICONTROL Customer Information]** på panelen **[!UICONTROL Account Information]**.

1. Ange **[!UICONTROL Allow remote shopping assistance]** som `Yes`.

   >[!INFO]
   >
   >Administratören kan nu logga in som en användare utan tillstånd från butiken.

>[!TAB Adobe Commerce as a Cloud Service]

[!BADGE Endast SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce as a Cloud Service- och Adobe Commerce Optimizer-projekt (SaaS-infrastruktur som hanteras av Adobe)."}

>[!NOTE]
>
>Mer information om hur du implementerar den här funktionen med REST finns i dokumentationen för [inloggningen som kund](https://developer.adobe.com/commerce/webapi/rest/saas-integrations/login-as-customer/) REST API.

### Begär en engångskod (OTC) från administratören

1. Navigera till **[!UICONTROL Customers]** och välj en kund för att öppna redigeringssidan.

1. Klicka på **[!UICONTROL Get Customer Login OTC]** på sidan Redigera kund.

   ![Knappen Hämta OTC för kundinloggning på sidan Redigera kund](assets/get-customer-login-otc-button.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Reason]** (obligatoriskt) och klicka på **[!UICONTROL Request]**.

   ![OTC-begäran modal med orsaksfältet](assets/otc-reason-modal.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Fältet **Orsak** är obligatoriskt. Den skickas till genereringsflödet för engångslösenord och är reserverad för kommande gransknings- och händelseloggningsfunktioner.

1. Den genererade OTC-koden visas i modalfilen. Använd den här koden med mutationen `generateCustomerToken` eller `exchangeOtpForCustomerToken` för GraphQL för kundauktorisering.

   ![Genererad OTC visas i modal](assets/otc-generated-code.png){width="300" zoomable="yes"}

>[!IMPORTANT]
>
>Den genererade OTC-koden är som standard giltig i 30 sekunder och ogiltigförklaras efter en engångsanvändning. TTL-värdet kan konfigureras genom att skicka en [supportanmälan](https://experienceleague.adobe.com/home?support-tab=home#support).

När du har skapat engångskoden kan du använda den genom att navigera till butiken och logga in med följande inloggningsuppgifter:

* **E-post**: Kundens e-postadress
* **Lösenord**: Den genererade engångskoden (OTC)

>[!ENDTABS]

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
