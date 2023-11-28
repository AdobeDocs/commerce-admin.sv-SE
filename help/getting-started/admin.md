---
title: Vad är administratören?
description: Läs mer om [!DNL Commerce] Admin, den plats där handlare ställer in produkter och kampanjer, hanterar beställningar och utför andra administrativa uppgifter.
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
source-git-commit: b657db7e486fec591d5a6239d554376f00707e8c
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Vad är administratören?

Din butik _Administratör_ är det lösenordsskyddade kontoret där du som handlare kan ställa in produkter och kampanjer, hantera beställningar och utföra andra administrativa uppgifter. Alla grundläggande konfigurationsuppgifter och lagringshanteringsåtgärder utförs från _Administratör_.

Om du vill ha ytterligare säkerhet kan du _Administratör_ inloggningen skyddas av [tvåfaktorsautentisering](../systems/security-two-factor-authentication.md)och kan konfigureras att kräva en [CAPTCHA](../systems/security-captcha.md). Om du vill veta mer går du till [Konfigurera administratörssäkerhet](../systems/security-admin.md).

![Administratörens sidopanel och kontrollpanel](./assets/admin-dashboard.png){width="700" zoomable="yes"}

Din initiala [inloggning](admin-signin.md) autentiseringsuppgifter konfigurerades under installationen av Adobe Commerce eller Magento Open Source. Om du glömmer lösenordet kan du skicka ett tillfälligt lösenord till den e-postadress som är kopplad till kontot. Om du vill öka säkerheten konfigurerar du din butik så att den kräver ett skiftlägeskänsligt användarnamn och starkt lösenord.

Förutom det förvalda administratörskontot kan ditt företag skapa så många [ytterligare konton](../systems/permissions-users-all.md) som ni behöver för att hantera butiken och ge support för kundkonton. Varje konto kan kopplas till ett specifikt [roll](../systems/permissions-user-roles.md) och åtkomstnivå, baserat på affärsverksamhet _behöver veta_. E-postadressen som är kopplad till varje administratörskonto måste vara unik.

{{ims-admin-note}}

## Insamling av användningsdata

Första gången du loggar in på _Administratör_ blir du ombedd att ge Adobe tillstånd att samla in användningsdata för alla Admin-användare. Genom att tillåta datainsamling med administratörsinformation kan du hjälpa Adobe att förbättra upplevelsen av att använda Adobe Commerce Admin, och relaterade produkter och tjänster.

![Tillåt datainsamling för administratörsanvändning](./assets/admin-usage-data.png){width="600"}

Enskilda användare identifieras inte i användningsdata. Inställningen för datainsamling kan ändras när som helst från [Administratörsanvändning](../configuration-reference/advanced/admin.md#admin-usage) konfiguration.

För Adobe Commerce innebär datainsamling även att _Produktvägledning_, som är utformat för att ge interaktivt innehåll till _Administratör_. Här finns hjälp, tips, guider, introduktionsinformation, funktionsmeddelanden med mera.
