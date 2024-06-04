---
title: CAPTCHA
description: Lär dig hur du konfigurerar CAPTCHA för administratörsåtkomst och olika butiksåtgärder som initierats av registrerade kunder.
exl-id: b2867ad5-7d48-4e9f-b84e-3cf0a14ec16f
role: Admin
feature: Configuration, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# CAPTCHA

En CAPTCHA är en visuell enhet som ser till att en människa i stället för en dator (eller robot) interagerar med webbplatsen. CAPTCHA är en förkortning av _Helt automatiserat offentligt kurstest för att skilja datorer och människor åt_. Den kan användas både för administratörsåtkomst och för olika butiksåtgärder som initierats av registrerade kunder. Adobe Commerce och Magento Open Source stöder CAPTCHA-standarden som beskrivs i det här avsnittet och [Google reCAPTCHA](security-google-recaptcha.md).

Du kan läsa in CAPTCHA igen så många gånger som behövs genom att klicka på ikonen Läs in igen i bildens övre högra hörn. CAPTCHA är helt konfigurerbart och kan anges varje gång, eller endast efter ett definierat antal misslyckade inloggningsförsök.

![Logga in med CAPTCHA](./assets/customer-account-login-captcha.png){width="700" zoomable="yes"}

## Konfigurera CAPTCHA för administratören

För en extra säkerhetsnivå kan du lägga till en CAPTCHA på sidan Administrera inloggning och Glömt lösenord. Administratörsanvändare kan läsa in CAPTCHA-filen igen genom att klicka på _Läs in igen_ ![ikonen läs in igen](./assets/CAPTCHA-icon-reload.png) i bildens övre högra hörn. Antalet omladdningar är obegränsat.

![Administratör - Logga in med CAPTCHA](./assets/security-captcha-admin.png){width="300"}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Advanced]** och välja **[!UICONTROL Admin]**.

1. I det övre högra hörnet anger du **[!UICONTROL Store View]** till `Default`.

   Om [omfång](../getting-started/websites-stores-views.md#scope-settings) Om din Commerce-installation innehåller flera webbplatser väljer du de webbplatser där du vill att CAPTCHA-konfigurationen ska användas.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL CAPTCHA]** -avsnitt.

1. Ange **[!UICONTROL Enable CAPTCHA in Admin]** till `Yes`. Fyll sedan i de återstående alternativen enligt följande:

   ![Admin - CAPTCHA-konfiguration](../configuration-reference/advanced/assets/admin-captcha.png){width="600" zoomable="yes"}

   - Ange namnet på **[!UICONTROL Font]** ska användas för CAPTCHA-symboler (standard: `LinLibertine`).

     Om du vill lägga till ett eget teckensnitt måste teckensnittsfilen finnas i samma katalog som din Commerce-installation och måste deklareras i `config.xml` fil för Captcha-modulen på `app/code/Magento/Captcha/etc`.

   - Välj något av följande **[!UICONTROL Forms]** där CAPTCHA ska användas. Om du vill välja flera formulär håller du ned Ctrl (PC) eller Kommando (Mac).

      - `Admin Login`
      - `Admin Forgot Password`

   - Ange **[!UICONTROL Displaying Modes]** till något av följande:

      - `Always` — CAPTCHA krävs alltid för att logga in på Admin.
      - `After number of attempts to login` — Det här alternativet gäller endast för formuläret Administratörsinloggning. När du väljer det här alternativet visas _[!UICONTROL Number of Unsuccessful Attempts to Login]_visas. Ange antalet inloggningsförsök som du vill tillåta. Värdet 0 (noll) påminner om inställningen för visningsläge `Always`.

     För att spåra antalet misslyckade inloggningsförsök räknas varje försök att logga in under en e-postadress och från en IP-adress. Det maximala antalet inloggningsförsök från samma IP-adress är 1 000. Den här begränsningen gäller bara när CAPTCHA är aktiverat.

   - För **[!UICONTROL Number of Unsuccessful Attempts to Login]** anger du antalet gånger som administratören kan försöka logga in innan CAPTCHA visas. Om inställt på noll (`0`) krävs alltid CAPTCHA.

   - För **[!UICONTROL CAPTCHA Timeout (minutes)]** anger du antalet minuter innan CAPTCHA förfaller. När CAPTCHA förfaller måste administratören läsa in sidan igen.

   - Ange **[!UICONTROL Number of Symbols]** visas i CAPTCHA. Upp till åtta (`8`) kan användas. Ange ett intervall (t.ex. `5-8`).

   - För **[!UICONTROL Symbols Used in CAPTCHA]** anger du de bokstäver (a-z och A-Z) och siffror (0-9) som du vill ska visas slumpmässigt i CAPTCHA. Symboler som är svåra att skilja från andra symboler, till exempel `i`, `l`, eller `1`, ingår inte i standarduppsättningen med CAPTCHA-symboler.

   - Ange **[!UICONTROL Case Sensitive]** till `Yes` om du vill att administratörer ska ange tecknen med versaler eller gemener exakt som i CAPTCHA.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Konfigurera CAPTCHA för butiken

Kunder kan behöva ange en CAPTCHA varje gång de loggar in på sina konton, eller efter flera misslyckade inloggningsförsök. Dessutom kan många formulär som används i hela butiken konfigureras så att CAPTCHA måste verifiera dem.

![CAPTCHA vid utcheckning](./assets/storefront-checkout-payment-captcha.png){width="700" zoomable="yes"}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Customers]** och välja **[!UICONTROL Customer Configuration]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL CAPTCHA]** -avsnitt.

![CAPTCHA-konfiguration för kund](../configuration-reference/customers/assets/customer-configuration-captcha.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Enable CAPTCHA on Storefront]** till `Yes`. Fyll sedan i de återstående alternativen enligt följande:

   - Ange namnet på **[!UICONTROL Font]** ska användas för CAPTCHA-symboler (standard: `LinLibertine`).

     Om du vill lägga till ett eget teckensnitt måste teckensnittsfilen finnas i samma katalog som din Commerce-installation och måste deklareras i `config.xml` CAPTCHA-modulens fil.

   - Välj något av följande **[!UICONTROL Forms]** där CAPTCHA ska användas. Om du vill välja flera formulär håller du ned Ctrl (PC) eller Kommando (Mac).

      - `Applying coupon code`
      - `Checkout/Placing Order`
      - `Create user`
      - `Login`
      - `Forgot password`
      - `Contact Us`
      - `Change password`
      - `Share Wishlist Form`
      - `Payflow Pro` (se [säkerhetsuppdatering](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html) _Knowledge Base_ artikel)
      - `Send to Friend Form` ![Magento Open Source](../assets/open-source.svg) (endast Magento Open Source)
      - `Add Gift Card Code` ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)
      - `Create company` ![Adobe Commerce B2B](../assets/b2b.svg) (Endast för Adobe Commerce B2B)

   - Ange **[!UICONTROL Displaying Mode]** till något av följande:

      - `Always` — CAPTCHA krävs alltid för att komma åt de valda formulären.
      - `After number of attempts to login` — Ange antalet inloggningsförsök innan CAPTCHA visas. Värdet 0 (noll) liknar Alltid. När du väljer det här alternativet visas antalet misslyckade inloggningsförsök. Det här alternativet gäller inte för formuläret Glömt lösenord, som om det är aktiverat alltid visar CAPTCHA.

   - För **[!UICONTROL Number of Unsuccessful Attempts to Login]** anger du antalet gånger som en kund inte kan logga in innan CAPTCHA visas. Om inställt på noll (`0`) används alltid CAPTCHA.

   - För **[!UICONTROL CAPTCHA Timeout (minutes)]** anger du antalet minuter innan CAPTCHA förfaller. När CAPTCHA förfaller måste kunden läsa in sidan igen för att generera en ny CAPTCHA.

   - Ange **[!UICONTROL Number of Symbols]** visas i CAPTCHA. Upp till åtta (`8`) kan användas. Ange ett intervall (t.ex. `5-8`).

   - För **[!UICONTROL Symbols Used in CAPTCHA]** anger du de bokstäver (a-z och A-Z) och siffror (0-9) som du vill ska visas slumpmässigt i CAPTCHA. Standarduppsättningen med tecken innehåller inte liknande symboler som `I` eller `1`. För bästa resultat bör du använda symboler som användarna lätt kan identifiera.

   - Ange **[!UICONTROL Case Sensitive]** till `Yes` om du vill att kunderna ska ange tecknen med versaler eller gemener exakt som de visas i CAPTCHA.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
