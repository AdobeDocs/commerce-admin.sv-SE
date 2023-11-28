---
title: Inloggningsuppgifter och URL:er
description: Lär dig mer om Commerce-URL:er och kontoautentiseringsuppgifter som används för att få åtkomst till din administratör och till din butik.
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---

# Inloggningsuppgifter och URL:er

Innan du fortsätter med konfiguration och konfiguration bör du kontrollera att du har den information som krävs för att få åtkomst till administratören för din butik och ditt Commerce-konto.

## Lagringsplats-URL

Adressen till [storefront](storefront.md) är vanligtvis den domän som är tilldelad din IP-adress. Vissa butiker installeras i rotkatalogen eller den översta katalogen. Andra installeras i en katalog under roten. Butiken kan ligga i en underdomän som är associerad med en primär domän. URL:en för din butik kan se ut så här:

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`s

Om du ännu inte har någon domän innehåller din butiks-URL en en serie med fyra siffror, där vart och ett avgränsas med en punkt i _prickad quad_ notation.

## Admin-URL

Butikens adress [Administratör](admin.md) konfigureras under installationen. Standardadressen är densamma som din butik, men med `/admin` i slutet. Även om exemplen i den här handboken använder standardkatalogen är det bäst att köra din administratör från en plats som är unik för din butik.

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## [!DNL Commerce] konto

Dina [Handelskonto](commerce-account-create.md) ger tillgång till information om produkter och tjänster, kontoinställningar, faktureringshistorik och supportresurser. Gå till Commerce-webbplatsen och klicka på **[!UICONTROL My Account]** längst upp till höger.

## Kundkonto

Se till att du konfigurerar ett test medan du lär dig mer om butiken [kundkonto](../customers/account-dashboard.md)så att ni kan uppleva butiks- och utcheckningsprocessen ur kundens perspektiv.

## Exempeldata

Adobe tillhandahåller en exempeldatauppsättning som innehåller en exempelbutik med mer än 250 produkter (cirka 200 av dem är konfigurerbara produkter), kategorier, kampanjprisregler, CMS-sidor, banners osv. Exempeldata använder _Luma_ temat på butiken. [Installerar exempeldata](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html) är valfritt, men kan vara användbart för att testa och utveckla anpassningar för din e-handelsverksamhet.
