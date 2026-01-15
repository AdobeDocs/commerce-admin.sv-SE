---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Admin Panel]'
description: Granska konfigurationsinställningarna på sidan [!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Admin Panel] i Commerce Admin.
exl-id: e4e6771a-487a-43ee-8b98-6acee4599aaf
feature: Configuration, Security
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 6fe5ffb6f529f95e32bb12a55ae16100f4d1bbbb
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Admin Panel]

>[!IMPORTANT]
>
>Innan du kan konfigurera Google reCAPTCHA måste du se till att filen `PHP.ini` innehåller följande inställning: `allow_url_fopen = 1`. Detta kan kräva hjälp av utvecklare. Se [Nödvändiga PHP-inställningar](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) i _installationshandboken_.

{{config}}

Mer information om hur du ändrar de här inställningarna finns i [Google reCAPTCHA](../../systems/security-google-recaptcha.md) i _handboken för administratörssystem_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 (&quot;Jag är inte en robot&quot;)](./assets/recaptcha-admin-v2-not-robot.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--|--|--|
| [!UICONTROL Google API Website Key] | Global | Den webbplatsnyckel som skapas när du registrerar ditt Google reCAPTCHA-konto. |
| [!UICONTROL Google API Secret Key] | Global | Den hemliga nyckel som är kopplad till ditt Google reCAPTCHA-konto. |
| [!UICONTROL Size] | Global | Storleken på rutan Google reCAPTCHA som visas vid inloggning. Alternativ: `Normal` (standard) / `Compact` |
| [!UICONTROL Theme] | Global | Anger formatet för rutan Google reCAPTCHA. Alternativ: `Light Theme` (standard) / `Dark Theme` |
| [!UICONTROL Language Code] | Global | En [kod med två tecken](https://developers.google.com/recaptcha/docs/language) som anger vilket språk som används för Google reCAPTCHA-text och -meddelanden. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 Osynlig](./assets/recaptcha-admin-v2-invisible.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--|--|--|
| [!UICONTROL Google API Website Key] | Global | Den webbplatsnyckel som skapas när du registrerar ditt Google reCAPTCHA-konto. |
| [!UICONTROL Google API Secret Key] | Global | Den hemliga nyckel som är kopplad till ditt Google reCAPTCHA-konto. |
| [!UICONTROL Invisible Badge Position] | Global | Positionen för det osynliga reCAPTCHA-märket på varje sida. Alternativ: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Global | Anger formatet för rutan Google reCAPTCHA. Alternativ: `Light Theme` (standard) / `Dark Theme` |
| [!UICONTROL Language Code] | Global | En [kod med två tecken](https://developers.google.com/recaptcha/docs/language) som anger vilket språk som används för Google reCAPTCHA-text och -meddelanden. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 osynlig](./assets/recaptcha-admin-v3-invisible.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--|--|--|
| [!UICONTROL Google API Website Key] | Global | Den webbplatsnyckel som skapas när du registrerar ditt Google reCAPTCHA-konto. |
| [!UICONTROL Google API Secret Key] | Global | Den hemliga nyckel som är kopplad till ditt Google reCAPTCHA-konto. |
| [!UICONTROL Minimum Score Threshold] | Global | Det lägsta poängvärde som identifierar en användarinteraktion som en potentiell risk, där 1.0 är en typisk användarinteraktion och 0.0 är troligtvis en robot. Standard: `0.5` |
| [!UICONTROL Invisible Badge Position] | Global | Positionen för det osynliga reCAPTCHA-märket på varje sida. Alternativ: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Global | Anger formatet för rutan Google reCAPTCHA. Alternativ: `Light Theme` (standard) / `Dark Theme` |
| [!UICONTROL Language Code] | Global | En [kod med två tecken](https://developers.google.com/recaptcha/docs/language) som anger vilket språk som används för Google reCAPTCHA-text och -meddelanden. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![Felmeddelanden](./assets/recaptcha-admin-failure-messages.png)<!-- zoom -->

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | Global | Meddelandet som visas i Admin om verifieringen misslyckas. Standardtext: `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | Global | Meddelandet som visas i Admin om reCAPTCHA inte returnerar ett verifieringsresultat. Standardtext: `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Admin Panel]

![Admin Panel](./assets/recaptcha-admin-panel.png)<!-- zoom -->

>[!NOTE]
>
>Typen reCAPTCHA som du väljer måste matcha den typ som är associerad med API-nyckeln från ditt Google reCAPTCHA-konto.

>[!WARNING]
>
>När du använder reCAPTCHA version 3 kan en äkta användare med låg poäng inte fortsätta. För version 2 får en äkta användare med låg poäng en utmaning. Tänk efter noga om äkta användare med låg poäng ska kunna lösa ett problem (version 2) eller blockeras (version 3).

| Fält | [Omfång](../../getting-started/websites-stores-views.md#scope-settings) | Beskrivning |
|--|--|--|
| [!UICONTROL Enable for Login] | Global | Bestämmer vilken typ av reCAPTCHA som är aktiverad för [administratörsinloggningen](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html). Alternativ:<br/>**`No`**- (standard) Verifierar inte administratörsinloggningen.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Kräver att användaren markerar kryssrutan _Jag är inte en robot_.<br />**`Invisible reCAPTCHA v2`**- Validerar användarbeteende i bakgrunden utan att det krävs interaktioner baserat på poäng.<br/>**`Invisible reCAPTCHA v3`** - (Rekommenderas) Validerar användarbeteende i bakgrunden baserat på interaktionspoäng. |
| [!UICONTROL Enable for Forgot Password] | Global | Bestämmer vilken typ av reCAPTCHA som är aktiverad för att begära en [återställning av administratörslösenord](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html#reset-your-password). Alternativ:<br/>**`No`**- (standard) Verifierar inte begäran om återställning av lösenord.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Kräver att användaren markerar kryssrutan _Jag är inte en robot_.<br />**`Invisible reCAPTCHA v2`**- Validerar användarbeteende i bakgrunden utan att det krävs interaktioner baserat på poäng.<br/>**`Invisible reCaptcha v3`** - (Rekommenderas) Validerar användarbeteende i bakgrunden baserat på interaktionspoäng. |

{style="table-layout:auto"}
