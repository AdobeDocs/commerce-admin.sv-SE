---
title: Fragment
description: Återanvända anteckningar och visuella element för att anteckna en funktion eller sida som gäller en viss utgåva
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Fragment

## Endast EE-funktion {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Funktionen Adobe Commerce" src="../assets/adobe-logo.svg" width="20" height="20" /> Endast exklusiva funktioner i Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Läs mer</a>)</td></tr>
</table>

## Endast B2B-funktion {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Funktionen B2B för Adobe Commerce" src="../assets/b2b.svg" width="20" height="20" /> Exklusiv funktion endast tillgänglig med <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=en">B2B för Adobe Commerce</a></td></tr>
</table>

## Endast CE-funktion {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Funktionen Magento Open Source" src="../assets/open-source.svg" width="20" height="20" /> Alternativ metod krävs för Magento Open Source (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Läs mer</a>)</td></tr>
</table>

## Autentiseringsanteckning för IMS-administratör {#ims-admin-note}

>[!NOTE]
>
>Adobe Commerce-handlare som har en Adobe ID och vill ha en smidig inloggning på Adobe Commerce och Adobe Business-produkter kan integrera Commerce Admin-autentisering med Adobe IMS-autentiseringsarbetsflödet. När integreringen har aktiverats för din Commerce Store måste varje Admin-användare använda sina inloggningsuppgifter för Adobe, inte sina autentiseringsuppgifter för Commerce-konton, för att kunna logga in. Se [Integrera Adobe Commerce med Adobe IMS - översikt](/help/getting-started/adobe-ims-integration-overview.md).

## Information om GTag API:er {#gtag-api-note}

>[!NOTE]
>
>Från och med version 2.4.5 uppdateras integreringen av Google-tjänster så att den stöder användningen av GTag-API:erna. GTag är en enhetlig mekanism för integrering med Google-funktioner för webbsidor och har stöd för de senaste funktionerna och möjligheterna att spåra och hantera innehåll via Google Services. Mer information finns i [Google Analytics utvecklardokumentation](https://developers.google.com/analytics/devguides/collection/gtagjs).

## Skriv om automatisk överhoppningsanteckning för URL {#url-rewrite-skip}

>[!NOTE]
>
>När automatiska omdirigeringar är aktiverade och du sparar en kategori, genereras alla produkt- och kategoriomskrivningar i realtid och lagras som standard i omskrivningstabeller. Denna process kan leda till betydande prestandaproblem för kategorier med många tilldelade produkter. Lösningen är att ändra den här standardinställningen och hoppa över generering av kategori-/produkt-URL-omskrivningar av produkter för att spara kategorier. I det här fallet genereras produktomskrivningar endast för den kanoniska produkt-URL:en. Se [Automatiska omdirigeringar av produkter](/help/merchandising-promotions/url-redirect-product-automatic.md) för mer information.

## Anteckning av parametrar för URL-omskrivning {#url-rewrite-params}

>[!IMPORTANT]
>
>Under omdirigeringen tas alla GET-parametrar som anges i URL-adressen bort av säkerhetsskäl.

## Ny prisregel {#new-price-rule}

>[!NOTE]
>
>Prisreglerna bearbetas automatiskt med andra systemregler. Bearbetningsfrekvensen beror på [kundkonfiguration](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html). När du skapar en prisregel måste du ge den tillräckligt med tid för att komma in i systemet. Testa regeln när du är säker på att den finns i systemet.

## Konfigurationsinställningar {#config}

Om du vill komma åt lagringskonfigurationsinställningarna väljer du **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**från_ Administratör _sidofält.

## UPS API-borttagning {#ups-api}

>[!IMPORTANT]
>
>Från och med juni 2024 kan Adobe Commerce handlare inte längre interagera med den nuvarande UPS-integreringen. Detta beror på att de UPS-API:er (United Parcel Service) som används av den inbyggda Adobe Commerce-integreringen för närvarande inte stöder den OAuth 2.0-säkerhetsmodell som krävs. Mer information om den här ändringen finns i [_Guide för migrering av nyckel till Developer Portal Access_](https://developer.ups.com/oauth-developer-guide). <br/>
>
>Merchants should [tillämpa en uppdatering av en kvalitetskorrigering](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html) till sin butik för att migrera från SOAP API till RESTful API, som stöder OAuth 2.0-autentiseringsprotokoll.


## Tillgänglig dokumentation {#docs-links}

| Dokumentationsresurs | Beskrivning |
|----------------------- | ----------- |
| [Adobe Commerce 2.4 Merchant Documentation](../landing/home.md) | Handläggning för både Adobe Commerce och Magento Open Source |
| [Services for Adobe Commerce Documentation](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) | Dokumentation till stöd för en samling tjänster som hjälper handlare att integrera viktiga komponenter i sin verksamhet med sin butik. |
| [Handbok för Commerce on Cloud Infrastructure](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | Stegvisa procedurer för att distribuera Adobe Commerce på en hanterad, automatiserad värdmolnplattform. |
| [Handböcker för Adobe Commerce 2.4](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | Systemdokumentation om koncept, processer, verktyg och bästa metoder för att utveckla, driftsätta och underhålla projekt som körs på Adobe Commerce och Magento Open Source. |
| [Adobe Commerce 2.4 Developer Documentation](https://developer.adobe.com/commerce/docs) | Dokumentation för utvecklare som används för att skapa och anpassa Adobe Commerce eller Magento Open Source |

{style="table-layout:auto"}
