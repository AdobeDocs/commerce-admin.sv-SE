---
title: Inaktivera Commerce Admin-integrering med Adobe ID
description: Följ den här valfria proceduren för att inaktivera integreringen av Adobe Commerce Admin med Adobe IMS.
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# Inaktivera Commerce Admin-integrering med Adobe ID

{{ee-feature}}

Handlare som har integrerat sin Commerce-instans med Adobe IMS-autentiseringsarbetsflödet kan behöva inaktivera den här valfria integreringen.

Commerce-distributioner återgår till standardarbetsflödet för Commerce-autentisering och lösenordsprinciper när IMS-integreringen har inaktiverats. Endast arbetsflöden för administrationsanvändare påverkas när den här integreringen är aktiverad eller inaktiverad.

Se [Ditt administratörskonto](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html) om du vill ha en översikt över Commerce Admin-inloggningen.

## Steg 1: Inaktivera integreringen

Du kan inte inaktivera den här integreringen från administratören. Om du vill inaktivera Adobe IMS-integreringen med Commerce och återställa Commerce-autentiseringen till standardläget måste du inaktivera integreringen från kommandoradsgränssnittet.

Så här inaktiverar du integreringen:

```bash
bin/magento admin:adobe-ims:disable
```

Adobe Commerce visar följande meddelande när det är klart:

```terminal
Admin Adobe IMS integration is disabled.
```

## Steg 2: Skapa eller hämta ditt handelslösenord

När integreringen har inaktiverats måste administratörsanvändare använda ett Commerce-lösenord för att logga in på administratören.

* Commerce-administratörsanvändare som kommer ihåg sitt befintliga Commerce-lösenord (det vill säga ett Commerce-lösenord som skapades innan IMS-integreringen) kan använda det för att logga in i administratören.

* Användare av Commerce-administratörer som inte har något befintligt Commerce-lösenord eller som har glömt det måste skapa ett nytt lösenord. Administratörsanvändare kan använda [!UICONTROL Forgot your password?] på inloggningssidan för Commerce för att skapa ett nytt lösenord. Se [Återställ kundlösenord](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html). Handeln accepterar inte ett tomt lösenordsfält.

## När integreringen har inaktiverats

Standardarbetsflödet för Commerce-autentisering återupptas när IMS-integrering har inaktiverats och administratörsanvändare uppmanas att ange sitt lösenord igen.

Om du inaktiverar IMS-integreringen tas de inloggningsuppgifter som angavs när integreringen aktiverades bort (`Organization ID`, `Client ID`och `Client Secret` värden) från Commerce-konfigurationsfilerna.
