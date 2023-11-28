---
title: Aktivera B2B-funktioner
description: Läs om hur du aktiverar B2B-funktioner för din Adobe Commerce-butik, inklusive företagskonton, standardbetalningsmetoder och leveransmetoder, inköpsorder och ordergodkännanden.
exl-id: aed203ef-f39b-4f7e-b32f-ded53eca09a8
feature: B2B, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '1629'
ht-degree: 0%

---

# Aktivera B2B-funktioner

Som standard är alla B2B-funktioner inaktiverade från början. En butiksadministratör kan aktivera eller inaktivera B2B-funktionerna efter behov för Commerce Store. En fullständig lista över B2B-konfigurationsinställningar finns i [B2B Funktioner, konfigurationsreferens](../configuration-reference/general/b2b-features.md).

När du aktiverar stöd för kundföretag aktiveras ytterligare B2B-funktioner automatiskt:

- [!DNL Shared Catalog]

  Stöder anpassad priskonfiguration för olika företag och aktiverar även kategoribehörigheter för alla butiker.

- [!DNL Enable Shared Catalog direct products price assigning]

  Förbättrar webbplatsens prestanda genom att endast produkter som har tilldelats en delad katalog lagras i prisindexet. Att aktivera den här funktionen är en bra metod för Merchants som har många delade kataloger att hantera anpassade priser för olika företag.

- [!DNL B2B Quotes]

  Ger säljare och företagsköpare möjlighet att förhandla om priser.

- [!DNL B2B default payment and shipping methods]

  Fastställer valet av betalnings- och leveransalternativ som är tillgängliga för B2B-köpare i butiken.

Konfigurationsinställningar för dessa funktioner visas bara när [!DNL Enable Company] är inställd på `Yes`.

B2B [!DNL Quick Order] och [!DNL Requisition List] funktioner kan aktiveras och inaktiveras oberoende av varandra.

## Konfigurera B2B-funktioner

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   Om du har en installation med flera platser anger du **[!UICONTROL Store View]** i det övre vänstra hörnet på webbplatsen där konfigurationen gäller.

1. I den vänstra panelen under _[!UICONTROL General]_, välja **[!UICONTROL B2B Features]**:

   ![B2B-konfiguration - allmän](./assets/b2b-features.png){width="600"}

   - Ge kunderna möjlighet att hantera sina egna företagskonton och aktivera stöd för ytterligare B2B-funktioner genom att ange **[!UICONTROL Enable Company]**  till `Yes`.

     När du aktiverar företagsstöd aktiveras automatiskt metoderna för delad katalog, B2B-offert, B2B-betalning och B2B-leverans.

   - Om du vill att kunder och gäster snabbt ska kunna göra beställningar baserat på SKU eller produktnamn anger du **[!UICONTROL Enable Quick Order]** till `Yes`.

   - Om du vill att kunderna ska kunna skapa och hantera rekvisitionslistor från sin kontokontrollpanel anger du **[!UICONTROL Enable Requisition List]** till `Yes`.

     Du kan också [konfigurera maximalt antal listor](configure-requisition-lists.md) en kund kan ha för sitt konto.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Konfigurera standardmetoder för B2B-betalning och -leverans

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Default B2B Payment Methods]** -avsnitt.

1. Ange standardbetalningsmetoder för B2B-order **[!UICONTROL Applicable Payment Methods]** till något av följande:

   - `All Payment Methods`

   - `Selected Payment Methods`

     För det specifika alternativet väljer du **[!UICONTROL Payment Methods]** som du vill göra tillgängliga för dina kunder genom att hålla ned Ctrl-tangenten (PC) eller Kommando-tangenten (Mac) när du klickar på varje alternativ.

   Listan med [betalningsmetoder](../configuration-reference/sales/payment-methods.md) visar vilka alternativ som är aktiverade eller inaktiverade i din butik. Förutom standardbetalningsmetoderna innehåller listan även följande:

   - Ingen betalningsinformation krävs
   - [Betalning à conto](#configure-payment-on-account)
   - Lagrade konton
   - Lagrade kort

   ![B2B-konfiguration - standardinställningar för betalningsmetod](./assets/b2b-features-default-payment-methods.png){width="600"}

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Default B2B Shipping Methods]** -avsnitt.

1. Ange standardleveransmetoder för B2B-beställningar **[!UICONTROL Applicable Shipping Methods]** till något av följande:

   - `All Shipping Methods`
   - `Selected Shipping Methods`

     För det specifika alternativet väljer du **[!UICONTROL Shipping Methods]** som du vill göra tillgängliga för dina kunder genom att hålla ned Ctrl-tangenten (PC) eller Kommando-tangenten (Mac) när du klickar på varje alternativ.

     Listan över leveransmetoder visar vilka som för närvarande är [aktiverad eller inaktiverad](../configuration-reference/sales/delivery-methods.md).

   ![B2B-konfiguration - standardleveransmetoder](./assets/b2b-features-shipping-methods.png){width="600"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Konfigurera e-postalternativ för företag

The [säljare](account-company-manage.md#assign-a-sales-representative) som har tilldelats som primär kontakt för ett företag konfigureras som standard som avsändare av många automatiska e-postmeddelanden som skickas till företaget.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Customers]** och välja **[!UICONTROL Company Configuration]**.

1. Ange vid behov **[!UICONTROL Store View]** till butiksvyn för att definiera [omfång](../getting-started/websites-stores-views.md#scope-settings) av konfigurationen.

1. Slutför **[!UICONTROL Company Registration]** avsnitt:

   >[!NOTE]
   >
   >Rensa **[!UICONTROL Use system value]** för att göra fältet redigerbart.

   - Ange **[!UICONTROL Company Registration Email Recipient]** till [butikskontakt](../getting-started/store-details.md#store-email-addresses) som ska meddelas när en ny registreringsbegäran tas emot.

   - För **[!UICONTROL Send Company Registration Email Copy To]** Ange e-postadressen till varje person som ska få en kopia av registreringsmeddelandet. Avgränsa flera e-postadresser med komma.

   - Ange hur kopian av meddelandet ska skickas **Skicka e-postkopieringsmetod** till något av följande:

      - `Bcc` - Skickar en _blankt text_ genom att inkludera mottagaren i rubriken för samma e-postmeddelande som skickas till kunden. Mottagaren av hemlig kopia är inte synlig för kunden.
      - `Separate Email` - Skickar kopian som ett separat e-postmeddelande.

   - Om du har förberett en e-postmall som ska användas i stället för standardmallen anger du **[!UICONTROL Default Company Registration Email]** till mallens namn. Som standard är `Company Registration Request` -mallen används.

     ![Kundkonfiguration - företagsregistrering](./assets/company-email-options-company-registration.png){width="600"}

1. Slutför **[!UICONTROL Customer-Related Emails]** avsnitt:

   Om du har förberett alternativa e-postmallar som ska användas i stället för standardvärdena, väljer du den mall som du vill använda för följande:

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![Kundkonfiguration - kundrelaterade e-postmeddelanden](./assets/company-email-options-customer-related-emails.png){width="600"}

1. Slutför **[!UICONTROL Company Status Change]** avsnitt:

   - För **[!UICONTROL Send Company Status Change Email Copy To]** Ange e-postadressen till varje person som ska få en kopia av meddelandet om statusändring. Avgränsa flera e-postadresser med komma.

   - Ange hur kopian av meddelandet ska skickas **Skicka e-postkopieringsmetod** till något av följande:

      - `Bcc` - Skickar en _blankt text_ genom att inkludera mottagaren i rubriken för samma e-postmeddelande som skickas till kunden. Mottagaren av hemlig kopia är inte synlig för kunden.
      - `Separate Email` - Skickar kopian som ett separat e-postmeddelande.

   - Om du har förberett en e-postmall som ska användas när företagsstatusen ändras från `Pending Approval` till `Active`, ange **[!UICONTROL Default 'Company Status Change to Active 1' Email]** till mallens namn. Som standard är `Company Status Active 1` -mallen används.

   - Om du har förberett en e-postmall som ska användas när företagsstatusen ändras från `Rejected` eller `Blocked` till `Active`, ange **[!UICONTROL Default 'Company Status Change to Active 2' Email]** till mallens namn. Som standard är `Company Status Active 2` -mallen används.

   - Om du har förberett en e-postmall som ska användas när företagsstatusen ändras till `Rejected`, ange **[!UICONTROL Default 'Company Status Change to Rejected' Email]** till mallens namn. Som standard är `Company Status Rejected` -mallen används.

   - Om du har förberett en e-postmall som ska användas när företagsstatusen ändras till `Blocked`, ange **[!UICONTROL Default 'Company Status Change to Blocked' Email]** till mallens namn. Som standard är `Company Status Blocked` -mallen används.

   - Om du har förberett en e-postmall som ska användas när företagsstatusen ändras till `Pending Approval`, ange **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** till mallens namn. Som standard är `Company Status Pending Approval` -mallen används.

   ![Kundkonfiguration - ändring av företagsstatus](./assets/company-email-options-company-status-change.png){width="600"}

1. Slutför **[!UICONTROL Company Credit Emails]** avsnitt:

   - Ange **[!UICONTROL Company Credit Change Email Sender]** till [butikskontakt](../getting-started/store-details.md#store-email-addresses) som ska meddelas när en ändring görs av kreditgränsen som tilldelas ett företag. Som standard skickas meddelandet till _Säljare_.

   - För **[!UICONTROL Send Company Credit Change Email Copy To]** Ange e-postadressen till varje person som ska få en kopia av meddelandet om kreditändring. Avgränsa flera e-postadresser med komma.

   - Ange hur kopian av meddelandet ska skickas **Skicka e-postkopieringsmetod** till något av följande:

      - `Bcc` - Skickar en _blankt text_ genom att inkludera mottagaren i rubriken för samma e-postmeddelande som skickas till kunden. Mottagaren av hemlig kopia är inte synlig för kunden.
      - `Separate Email` - Skickar kopian som ett separat e-postmeddelande.

   - Om du har förberett e-postmallar som ska användas i stället för standardvärdena, väljer du mallen för vart och ett av följande meddelanden som skickas till företagsadministratören.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![Kundkonfiguration - företagskreditmeddelanden](./assets/company-email-options-company-credit.png){width="600"}

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Konfigurera ordergodkännande

Möjligheten att spåra orderbehandling och inköpsorder ger företagsadministratörer kontroll över hur företagets köpare agerar. Funktionen för ordergodkännande är tillgänglig när funktionen för inköpsorder aktiveras av en butiksadministratör.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL General]** och välja **[!UICONTROL B2B Features]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Order Approval Configuration]** -avsnitt.

   ![Konfiguration för ordergodkännande](./assets/b2b-features-order-approval.png){width="600"}

1. Om du vill att företag ska kunna skapa egna inköpsorder anger du **[!UICONTROL Enable Purchase Orders]** till `Yes`.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

   Funktionen för inköpsorder är aktiverad på webbplatsnivå. Om du vill aktivera den här typen av beställning för ett företag gör du samma sak med lämpliga inställningar i varje [företagsprofil](account-company-manage.md).

## Konfigurera inköpsorder

1. På _Administratör_ sidebar, gå till **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Hitta företaget i listan och klicka på **[!UICONTROL Edit]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Advanced Settings]** -avsnitt.

1. Ange **[!UICONTROL Enable Purchase Orders]** till `Yes`.

1. När du är klar klickar du på **[!UICONTROL Save]**.

Efter aktiveringen **[!UICONTROL Approval Rules]** -avsnittet visas i butiken [Kontrollpanel för konto](../customers/account-dashboard.md) för en företagsadministratör.

>[!NOTE]
>
>Åtkomst till inköpsorder i butiken måste beviljas av företagsadministratören baserat på [behörigheter för företagsanvändarroll](account-company-roles-permissions.md).

## Konfigurera betalning a conto

Betalning på konto är en offlinebetalningsmetod som gör att företag kan göra köp upp till den kreditgräns som anges i deras profil. Betalning på konto kan aktiveras globalt, eller per företag, och visas endast vid utcheckning om det är aktiverat. När _Betalning à conto_ används som betalningsmetod visas ett meddelande högst upp i ordern som anger kontots status. Information om hur du konfigurerar den här betalningsmetoden för ett visst företag finns i [Hantera företagskonton](account-company-manage.md).

>[!NOTE]
>
>Betalning på konto stöds inte för order med [flera leveransadresser](../stores-purchase/shipping-settings.md#multiple-addresses) och visas inte bland betalningsalternativen för dessa order.

Så här aktiverar du Betalning på konto för din butik:

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Payment Methods]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Payment on Account]** -avsnitt.

   ![Betalning à conto](./assets/payment-methods-payment-on-account.png){width="600"}

   >[!NOTE]
   >
   >Om det behövs avmarkerar du **[!UICONTROL Use system value]** om du vill ändra inställningarna.

1. Om du vill tillåta kontobetalning anger du **[!UICONTROL Enabled]** till `Yes`.

1. Ange en **[!UICONTROL Title]** som identifierar betalningsmetoden under utcheckningen eller så kan du godkänna `Payment on Account` standardtitel.

1. Om beställningarna vanligtvis väntar på godkännande, acceptera standardinställningen **[!UICONTROL New Order Status]** as `Pending` tills det har godkänts.

   Om du vill kan du använda `Processing` eller `Suspected Fraud` status för nya order med denna betalningsmetod.

1. Ange **[!UICONTROL Payment from Applicable Countries]** till något av följande:

   - `All Allowed Countries` - Kunder från alla [länder](../getting-started/store-details.md#country-options) som anges i din butikskonfiguration kan använda den här betalningsmetoden.
   - `Specific Countries` - När du har valt det här alternativet visas _[!UICONTROL Payment from Specific Countries]_visas. Om du vill markera flera länder håller du ned Ctrl (PC) eller Kommando (Mac) och klickar på varje alternativ.

1. Ange **[!UICONTROL Minimum Order Total]** och **[!UICONTROL Maximum Order Total]** till de orderbelopp som krävs för att få utnyttja denna betalningsmetod.

   >[!NOTE]
   >
   >En order kvalificerar om summan faller mellan, eller exakt matchar, minimi- eller maximivärdena för totalvärdet.

1. Ange en **[!UICONTROL Sort Order]** tal som anger positionen för det här objektet i listan över betalningsmetoder som visas vid utcheckning.

   Värdet är relativt till de andra betalningsmetoderna. (`0` = first, `1` = sekund, `2` = tredje och så vidare.)

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
