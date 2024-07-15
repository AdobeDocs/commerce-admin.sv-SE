---
title: Nya alternativ för kundkonton
description: Läs mer om konfigurationsalternativen för nya kundkonton i din butik.
exl-id: aa19f0e2-ffbe-433d-8bd5-c14700b67b37
feature: Customers, Configuration
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Nya alternativ för kundkonton

I avsnittet _[!UICONTROL Create New Account Options]_i konfigurationen kombineras de grundläggande kontoalternativen med mer avancerade alternativ som relaterar till moms-ID-validering och anpassade integreringar. Följande instruktioner täcker endast de vanligaste alternativen. Mer information om automatiska kundgrupptilldelningar finns i [momsvalidering](../stores-purchase/vat.md).

![Skapa nya kontoalternativ](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## Ange grundläggande alternativ för kundkonton

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Customers]** i den vänstra panelen och välj **[!UICONTROL Customer Configuration]**.

1. Expandera avsnittet **[!UICONTROL Create New Account Options]**:

   ![Skapa standardinställningar för nya kontoalternativ](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. Ställ in vart och ett av alternativen efter den kundupplevelse ni behöver för att få support i er butik:

   - Ange **[!UICONTROL Default Group]** till kundgruppen som tilldelas nya kunder när ett konto skapas.

   - Om du har ett _Value Added Tax_-nummer och vill att det ska vara synligt för kunderna anger du **[!UICONTROL Show VAT Number on Storefront]** till `Yes`.

   - Om du vill att en kunds e-postadress ska krävas när administratörsordern skapas för en kund anger du **[!UICONTROL Email is required field for Admin order creation]** till `Yes`.

   - Ange **[!UICONTROL Default Email Domain]** för butiken, till exempel `mystore.com`

   - Ange **[!UICONTROL Default Welcome Email]** till mallen som används för välkomstmeddelandet som skickas till nya kunder.

   - Om du vill att kunderna ska bekräfta sin begäran om att öppna ett konto hos din butik anger du **[!UICONTROL Require Emails Confirmation]** till `Yes`. Ange sedan **[!UICONTROL Confirmation Link Email]** till mallen som används för bekräftelsemeddelandet.

     >[!NOTE]
     >
     >Från och med version 2.4.7 måste kunderna ange sin e-postadress och sitt lösenord på nytt för att logga in på sina konton efter e-postbekräftelse, oavsett webbläsare.

   - Ange **[!UICONTROL Welcome Email]** till mallen som används för välkomstmeddelandet som skickas när kontot har bekräftats.

   - Ange **[!UICONTROL Default Welcome Email without Password]** till mallen som används när ett kundkonto som ännu inte har något lösenord skapas. Ett kundkonto som skapats från administratören har till exempel ännu inte tilldelats något lösenord.

   - Ange **[!UICONTROL Email Sender]** till butikskontakten som visas som avsändare av välkomstmeddelandet.

   - Om du vill att kunderna ska bekräfta sin begäran om att öppna ett konto hos din butik anger du **[!UICONTROL Require Emails Confirmation]** till `Yes`. Ange sedan **[!UICONTROL Confirmation Link Email]** till mallen som används för bekräftelsemeddelandet.

   ![Skapa nya kontoalternativ med moms aktiverat](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

   Mer information om de olika alternativen i den här konfigurationsalternativsuppsättningen finns i _Skapa nya kontoalternativ_ [konfigurationsreferensen](../configuration-reference/customers/customer-configuration.md).

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
