---
title: Nya alternativ för kundkonton
description: Läs mer om konfigurationsalternativen för nya kundkonton i din butik.
exl-id: aa19f0e2-ffbe-433d-8bd5-c14700b67b37
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# Nya alternativ för kundkonton

I _[!UICONTROL Create New Account Options]_i konfigurationen kombineras de grundläggande kontoalternativen med mer avancerade alternativ som relaterar till moms-ID-validering och anpassade integreringar. Följande instruktioner täcker endast de vanligaste alternativen. Mer information om automatiska kundgrupptilldelningar finns i [momsvalidering](../stores-purchase/vat.md).

{{beta-updates}}

![Skapa nya kontoalternativ](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## Ange grundläggande alternativ för kundkonton

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Customers]** och välja **[!UICONTROL Customer Configuration]**.

1. Expandera **[!UICONTROL Create New Account Options]** avsnitt:

   ![Skapa standardinställningar för nya kontoalternativ](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. Ställ in vart och ett av alternativen efter den kundupplevelse ni behöver för att få support i er butik:

   - Ange **[!UICONTROL Default Group]** till kundgruppen som tilldelas nya kunder när ett konto skapas.

   - Om du har en _Mervärdesskatt_ och vill att den ska vara synlig för kunderna, ange **[!UICONTROL Show VAT Number on Storefront]** till `Yes`.

   - Om du vill att en kunds e-post ska krävas när en kund skapas i en administratörsorder anger du **[!UICONTROL Email is required field for Admin order creation]** till `Yes`.

   - Ange **[!UICONTROL Default Email Domain]** för butiken, till exempel `mystore.com`

   - Ange **[!UICONTROL Default Welcome Email]** till mallen som används för välkomstmeddelandet som skickas till nya kunder.

   - Ange **[!UICONTROL Default Welcome Email without Password]** till mallen som används när ett kundkonto skapas som ännu inte har något lösenord. Ett kundkonto som skapats från administratören har till exempel ännu inte tilldelats något lösenord.

   - Ange **[!UICONTROL Email Sender]** till butikskontakten som visas som avsändare av välkomstmeddelandet.

   - Om du vill att kunderna ska bekräfta sin begäran om att öppna ett konto hos din butik anger du **[!UICONTROL Require Emails Confirmation]** till `Yes`. Sedan anger du **[!UICONTROL Confirmation Link Email]** till mallen som används för bekräftelsemeddelandet.

   - Ange **[!UICONTROL Welcome Email]** till mallen som används för välkomstmeddelandet som skickas när kontot har bekräftats.

     ![Skapa nya kontoalternativ med moms aktiverat](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

     Mer information om de olika alternativen som finns i den här uppsättningen konfigurationsalternativ finns i _Skapa nya kontoalternativ_ [konfigurationsreferens](../configuration-reference/customers/customer-configuration.md).

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
