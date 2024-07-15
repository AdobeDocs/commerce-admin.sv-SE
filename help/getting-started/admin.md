---
title: Vad är administratören?
description: Lär dig mer om  [!DNL Commerce] Admin, den plats där handlare ställer in produkter och kampanjer, hanterar beställningar och utför andra administrativa uppgifter.
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
source-git-commit: b657db7e486fec591d5a6239d554376f00707e8c
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Vad är administratören?

Din butik _Admin_ är det lösenordsskyddade kontoret där du, som handlare, ställer in produkter och kampanjer, hanterar beställningar och utför andra administrativa uppgifter. Alla grundläggande konfigurationsuppgifter och lagringshanteringsåtgärder utförs från _administratören_.

För ytterligare säkerhet skyddas inloggningen _Admin_ av [tvåfaktorsautentisering](../systems/security-two-factor-authentication.md) och kan konfigureras så att den kräver [CAPTCHA](../systems/security-captcha.md). Mer information finns i [Konfigurera administratörsskydd](../systems/security-admin.md).

![Administratörens sidopanel och kontrollpanel](./assets/admin-dashboard.png){width="700" zoomable="yes"}

De första [inloggningsuppgifterna](admin-signin.md) konfigurerades under Adobe Commerce- eller Magento Open Source-installationen. Om du glömmer lösenordet kan du skicka ett tillfälligt lösenord till den e-postadress som är kopplad till kontot. Om du vill öka säkerheten konfigurerar du din butik så att den kräver ett skiftlägeskänsligt användarnamn och starkt lösenord.

Förutom det förvalda administratörskontot kan ditt företag skapa så många [ytterligare konton](../systems/permissions-users-all.md) som du behöver för att hantera butiken och ge support för kundkonton. Varje konto kan associeras med en specifik [roll](../systems/permissions-user-roles.md) och åtkomstnivå baserat på verksamhetens _behov att känna till_. E-postadressen som är kopplad till varje administratörskonto måste vara unik.

{{ims-admin-note}}

## Insamling av användningsdata

Första gången du loggar in på _Admin_ blir du ombedd att ge Adobe behörighet att samla in användningsdata för alla Admin-användare. Genom att tillåta datainsamling med administratörsinformation kan du hjälpa Adobe att förbättra upplevelsen av att använda Adobe Commerce Admin, och relaterade produkter och tjänster.

![Tillåt datainsamling för administratörsanvändning](./assets/admin-usage-data.png){width="600"}

Enskilda användare identifieras inte i användningsdata. Inställningen för datainsamling kan ändras när som helst från konfigurationen [Administratörsanvändning](../configuration-reference/advanced/admin.md#admin-usage).

Om du tillåter datainsamling för Adobe Commerce aktiveras även _Produktvägledning_, som är utformad för att ge _Admin_ interaktivt innehåll. Här finns hjälp, tips, guider, introduktionsinformation, funktionsmeddelanden med mera.
