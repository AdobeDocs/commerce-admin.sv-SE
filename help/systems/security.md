---
title: Säkerhet
description: Lär dig mer om de verktyg som finns för att skydda era butiker och data, och riktlinjer för en säkerhetsåtgärdsplan om du upptäcker en kompromiss.
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
source-git-commit: fede05a413428520eec89d46f41a1cdd9c9c3a2e
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Säkerhet

Det finns flera sätt att skydda din butik och upprätthålla din datasäkerhet:

- Konfigurera [tvåfaktorsautentisering](security-two-factor-authentication.md)
- Implementera [CAPTCHA](security-captcha.md) eller [reCAPTCHA](security-google-recaptcha.md)
- Konfigurera en [säkerhetsgenomsökning](security-scan.md) för varje domän i Adobe Commerce- eller Magento Open Source-installationen.

>[!NOTE]
>
>Lager som har aktiverat [!DNL Adobe Identity Management Services] (IMS)-autentisering har inbyggda Adobe Commerce och Magento Open Source 2FA inaktiverade. Administratörsanvändare som är inloggade på sin Commerce-instans med sina inloggningsuppgifter för Adobe behöver inte autentisera igen för många administratörsuppgifter. Autentisering hanteras av Adobe IMS när administratörsanvändaren loggar in på sin aktuella session. Se [[!DNL Adobe Identity Management Service] (IMS)-integreringsöversikt](../getting-started/adobe-ims-integration-overview.md).

Besök [Säkerhetscenter](https://helpx.adobe.com/se/security.html){:target=&quot;_blank&quot;} för att få de senaste nyheterna om potentiella sårbarheter, registrera dig för säkerhetsmeddelanden från Adobe och få tillgång till Adobe Trust Center.

![Säkerhetscenter](./assets/product-security-home.png){width="700" zoomable="yes"}

Information om bästa säkerhetsmetoder finns i [Skydda din Commerce-webbplats och infrastruktur](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html?lang=sv-SE) i _Implementeringspellistan_.

## Åtgärdsplan för säkerhet

Om du misstänker att din Adobe Commerce- eller Magento Open Source-webbplats är komprometterad ska du följa den här åtgärdsplanen utan dröjsmål.

1. **Diagnostisera**: Kör en sökning för att fastställa säkerhetsstatusen för din Commerce-butik. Commerce [Security Scan](security-scan.md) är en kostnadsfri tjänst från Adobe som gör att du kan övervaka Commerce webbplatser för att upptäcka kända säkerhetsrisker och skadlig kod samt ta emot säkerhetsmeddelanden.

1. **Rensa**: Anställ en [kvalificerad konsult](https://solutionpartners.adobe.com/s/directory/?partner_type=1) eller onlinetjänst för att rensa din webbplats från all skadlig kod. Vissa Commerce-communitymedlemmar rekommenderar [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). Kontrollera om mappen `/media` innehåller körbar kod kvar. Ta bort alla okända administratörsanvändare och återställ alla administratörslösenord.

1. **Protect**: Håll din Commerce-installation uppdaterad med den senaste versionen. Om du använder en äldre version bör du tillämpa alla säkerhetsuppdateringar när de blir tillgängliga. Granska och följ [Commerce bästa säkerhetspraxis](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). Prenumerera på [Commerce säkerhetsvarningar](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **Rapport**: Om du tror att du har hittat en specifik säkerhetslucka i Commerce [öppnar du ett problem med Adobe](https://hackerone.com/adobe?type=team) och inkluderar teknisk information.

1. **Uppgradera**: Om du vill känna dig extra trygg som supporten dygnet runt kan du planera din uppgradering till [Adobe Commerce på vår molnarkitektur](https://business.adobe.com/se/products/magento/cloud-delivery.html) nu.
