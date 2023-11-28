---
title: Alternativ för kundlösenord
description: Kundlösenordsalternativen avgör säkerhetsnivån för olika kundmotstående funktioner i din butik.
exl-id: 84dec8e8-3363-4133-bbcc-9e58467749c4
feature: Customers, Configuration, Security
source-git-commit: ea9eeea0fc5213de2787e0b7ea2aed825ca3a9de
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Alternativ för kundlösenord

Kundlösenordsalternativen avgör säkerhetsnivån som används för begäranden om lösenordsåterställning, e-postmallar som används för kundmeddelanden och livslängden för länken för lösenordsåterställning. Du kan tillåta kunderna att ändra sina egna lösenord eller kräva att bara butiksadministratörer kan göra det.

## Konfigurera alternativ för kundlösenord

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Customers]** och välja **[!UICONTROL Customer Configuration]**.

1. Expandera avsnittet **[!UICONTROL Password Options]**.

   ![Alternativ för lösenord](../configuration-reference/customers/assets/customer-configuration-password-options.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Password Reset Protection Type]** till den metod som du vill använda för att kontrollera begäranden om återställning av lösenord:

   - `By IP and Email` - Sök efter tidigare försök att återställa lösenordet för en viss e-postadress eller från en viss IP-adress.
   - `By IP` - Sök efter tidigare försök att återställa lösenordet från en viss IP-adress.
   - `By Email` - Sök efter tidigare försök att återställa lösenordet för en viss e-postadress.
   - `None` - Skydd inaktiverat (inga begränsningar för återställning av lösenord).

   The **[!UICONTROL Max Number of Password Reset Requests]** och **[!UICONTROL Min Time Between Password Reset Requests]** beräknas baserat på den här konfigurationen.

1. Så här begränsar du antalet begäranden om återställning av lösenord som skickas per timme:

   - För **[!UICONTROL Max Number of Password Reset Requests]** anger du det maximala antalet begäranden om återställning av lösenord som kan skickas per timme.

   - För **[!UICONTROL Min Time Between Password Reset Requests]** anger du det minsta antal minuter som ska förflyta mellan begäranden.

1. Så här konfigurerar du e-postmeddelanden om återställning av lösenord:

   - Ange **[!UICONTROL Forgot Email Template]** till mallen som används för e-postmeddelandet som skickas till kunder som har glömt sina lösenord.

   - Ange **[!UICONTROL Remind Email Template]** till mallen som används när ett kundlösenord återställs av en Admin-användare.

   - Ange **[!UICONTROL Reset Password Template]** till mallen som används när kunderna ändrar sina lösenord.

   - Ange **[!UICONTROL Password Template Email Sender]** till [butikskontakt](../getting-started/store-details.md) som visas som avsändare av lösenordsrelaterade meddelanden.

1. Fyll i följande säkerhetsalternativ för återställning av lösenord:

   - För **[!UICONTROL Recovery Link Expiration Period (hours)]** anger du antalet timmar innan länken för återställning av lösenord upphör att gälla.

   - Om du vill att fälten i kundinloggningen och i formulären för glömt lösenord ska fyllas i automatiskt från tidigare poster anger du **[!UICONTROL Enable Autocomplete on login/forgot password forms]** till `Yes`.

   - För **[!UICONTROL Number of Required Character Classes]** anger du antalet olika teckentyper som måste ingå i ett lösenord baserat på följande teckenklasser:

      - `Lowercase`
      - `Uppercase`
      - `Numeric`
      - `Special Characters`

   - För **[!UICONTROL Maximum Login Failures to Lockout Account]** anger du antalet misslyckade inloggningsförsök tills kundkontot är låst. För obegränsat antal försök anger du noll (`0`).

   - För **[!UICONTROL Minimum Password Length]** anger du det minsta antalet tecken som kan användas i ett lösenord. Talet måste vara större än noll.

   - För **[!UICONTROL Lockout Time (minutes)]** anger du antalet minuter som ett kundkonto är låst efter för många misslyckade inloggningsförsök.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
