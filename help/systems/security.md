---
title: Säkerhet
description: Lär dig mer om de verktyg som finns för att skydda era butiker och data, och riktlinjer för en säkerhetsåtgärdsplan om du upptäcker en kompromiss.
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
source-git-commit: 671ec7015c37b24ca0acc615ae3715b8b870a453
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Säkerhet

Det finns flera sätt att skydda din butik och upprätthålla din datasäkerhet:

- Konfigurera [tvåfaktorsautentisering](security-two-factor-authentication.md)
- Implementera [CAPTCHA](security-captcha.md) eller [reCAPTCHA](security-google-recaptcha.md)
- Konfigurera en [Säkerhetsgenomsökning](security-scan.md) för varje domän i Adobe Commerce- eller Magento Open Source-installationen.

Besök [Security Center](https://helpx.adobe.com/security.html){:target=&quot;_blank&quot;} och gå med i säkerhetsvarningsregistret för de senaste nyheterna om potentiella sårbarheter. Mer information om bästa säkerhetsmetoder finns i [Skydda din Commerce Site och Infrastructure](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html) i _Implementera spelningsbok_.

>[!NOTE]
>
>Lager som har aktiverats [!DNL Adobe Identity Management Services] (IMS)-autentisering har inbyggda Adobe Commerce och Magento Open Source 2FA inaktiverat. Administratörsanvändare som är inloggade på sin Commerce-instans med sina inloggningsuppgifter för Adobe behöver inte autentisera igen för många administratörsuppgifter. Autentisering hanteras av Adobe IMS när administratörsanvändaren loggar in på sin aktuella session. Se [[!DNL Adobe Identity Management Service] (IMS) Integreringsöversikt](../getting-started/adobe-ims-integration-overview.md).

![Security Center](./assets/product-security-home.png){width="700" zoomable="yes"}

## Åtgärdsplan för säkerhet

Om du misstänker att din Adobe Commerce- eller Magento Open Source-webbplats är komprometterad ska du följa den här åtgärdsplanen utan dröjsmål.

1. **Diagnostisera**: Kör en sökning för att fastställa säkerhetsstatusen för din Commerce Store. Handel [Säkerhetsgenomsökning](security-scan.md) är en kostnadsfri tjänst från Adobe som gör att du kan övervaka dina Commerce-sajter med avseende på kända säkerhetsrisker och skadlig kod samt ta emot säkerhetsmeddelanden.

1. **Ren**: Anställ en [kvalificerad konsult](https://solutionpartners.adobe.com/s/directory/?partner_type=1) eller onlinetjänst för att rensa din webbplats från all skadlig kod. Vissa medlemmar i Commerce Community rekommenderar [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). Kontrollera `/media` mapp för överbliven körbar kod. Ta bort alla okända administratörsanvändare och återställ alla administratörslösenord.

1. **Protect**: Håll din Commerce-installation uppdaterad med den senaste versionen. Om du använder en äldre version bör du tillämpa alla säkerhetsuppdateringar när de blir tillgängliga. Granska och följ [Bästa praxis för affärssäkerhet](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). Prenumerera på [Säkerhetsvarningar för Commerce](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **Rapport**: Om du tror att du har hittat en specifik säkerhetslucka i Commerce, [öppna ett problem med Adobe](https://hackerone.com/adobe?type=team) och innehåller teknisk information.

1. **Uppgradera**: Om du vill känna dig extra trygg med support dygnet runt kan du planera din uppgradering till [Adobe Commerce på vår molnarkitektur](https://business.adobe.com/products/magento/cloud-delivery.html) nu.
