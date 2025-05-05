---
title: Inaktivera Commerce Admin-integrering med Adobe ID
description: Följ den här valfria proceduren för att inaktivera integreringen av Adobe Commerce Admin med Adobe IMS.
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Inaktivera Commerce Admin-integrering med Adobe ID

{{ee-feature}}

Handlare som har integrerat sin Commerce-instans med Adobe IMS-autentiseringsarbetsflödet kan behöva inaktivera den här valfria integreringen.

Commerce-distributioner återgår till standardarbetsflödet för Commerce-autentisering och lösenordsprinciper när IMS-integreringen har inaktiverats. Endast arbetsflöden för administrationsanvändare påverkas när den här integreringen är aktiverad eller inaktiverad.

Se [Ditt administratörskonto](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html) för en översikt över inloggningen med Commerce Admin.

## Steg 1: Inaktivera integreringen

Du kan inte inaktivera den här integreringen från administratören. Om du vill inaktivera Adobe IMS-integrationen med Commerce och återställa Commerce-autentiseringen till standardläget måste du inaktivera integreringen från kommandoradsgränssnittet.

Så här inaktiverar du integreringen:

```bash
bin/magento admin:adobe-ims:disable
```

Adobe Commerce visar följande meddelande när det är klart:

```
Admin Adobe IMS integration is disabled.
```

## Steg 2: Skapa eller hämta ditt Commerce-lösenord

När integreringen har inaktiverats måste administratörsanvändare använda ett Commerce-lösenord för att logga in på administratören.

* Användare av Commerce-administratörer som kommer ihåg sitt befintliga Commerce-lösenord (det vill säga ett Commerce-lösenord som skapades innan IMS-integreringen) kan använda det för att logga in i administratören.

* Användare av Commerce-administratörer som inte har något befintligt Commerce-lösenord eller som har glömt det måste skapa ett nytt lösenord. Om du vill skapa ett nytt lösenord kan administratörsanvändare använda funktionen [!UICONTROL Forgot your password?] på inloggningssidan för Commerce för att skapa ett nytt lösenord. Se [Återställ kundlösenord](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html). Commerce godkänner inte ett tomt lösenordsfält.

## När integreringen har inaktiverats

Commerce standardautentiseringsarbetsflöde återupptas när IMS-integrering har inaktiverats och administratörsanvändare uppmanas att ange sitt lösenord igen.

Om du inaktiverar IMS-integreringen tas de inloggningsuppgifter som angavs när integreringen aktiverades (`Organization ID`, `Client ID` och `Client Secret` värden) bort från Commerce konfigurationsfiler.
