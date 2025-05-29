---
title: Inloggningsuppgifter och URL:er
description: Läs mer om Commerce URL:er och kontoinloggningsuppgifter som används för att få åtkomst till din administratör och till din butik.
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 77e7eb00e9f8d5af6361059c287707993180c4c4
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Inloggningsuppgifter och URL:er

Innan du fortsätter med konfiguration och konfiguration bör du kontrollera att du har den information som krävs för att få åtkomst till administratören för din butik och ditt Commerce-konto.

## Lagringsplats-URL

Adressen till din [storefront](storefront.md) är vanligtvis den domän som är tilldelad din IP-adress. Vissa butiker installeras i rotkatalogen eller den översta katalogen. Andra installeras i en katalog under roten. Butiken kan ligga i en underdomän som är associerad med en primär domän. URL:en för din butik kan se ut så här:

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`

Om du ännu inte har någon domän innehåller din butiks-URL en en serie med fyra siffror, där vart och ett avgränsas med en punkt i _prickad quad_-notation.

## Admin-URL

Adressen för din butik [Admin](admin.md) ställs in under installationen. Standardadressen är samma som din butik, men med `/admin` i slutet. Även om exemplen i den här handboken använder standardkatalogen är det bäst att köra din administratör från en plats som är unik för din butik.

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## [!DNL Commerce]-konto

Ditt [Commerce-konto](commerce-account-create.md) ger dig tillgång till information om dina produkter och tjänster, kontoinställningar, faktureringshistorik och supportresurser. Gå till Commerce huvudwebbplats och klicka på **[!UICONTROL My Account]** i det övre högra hörnet om du vill komma åt ditt konto.

## Kundkonto

Se till att du konfigurerar ett [kundkonto](../customers/account-dashboard.md) när du lär dig mer om butiken, så att du kan uppleva processen och utcheckningen ur kundens perspektiv.

## Exempeldata

[!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."}

Adobe tillhandahåller en exempeldatauppsättning som innehåller en exempelbutik med mer än 250 produkter (cirka 200 av dem är konfigurerbara produkter), kategorier, kampanjprisregler, CMS-sidor, banners osv. Exempeldata använder _Luma_-temat på butiken. [Det är valfritt att installera exempeldata](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html), men det kan vara användbart för att testa och utveckla anpassningar för din e-handelsverksamhet.
