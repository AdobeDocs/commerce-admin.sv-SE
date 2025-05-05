---
title: Fragment
description: Återanvända anteckningar och visuella element för att anteckna en funktion eller sida som gäller en viss utgåva
source-git-commit: e82b979ee2c5f51caba6a2aa416c5f20dbce110a
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%

---

# Fragment

## Endast EE-funktion {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Funktionen Adobe Commerce" src="../assets/adobe-logo.svg" width="20" height="20" /> Endast exklusiv funktion i Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=sv-SE#product-editions">Läs mer</a>)</td></tr>
</table>

## Endast B2B-funktion {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Adobe Commerce B2B-funktion" src="../assets/b2b.svg" width="20" height="20" /> Exklusiv funktion endast tillgänglig med <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=sv-SE">Adobe Commerce B2B</a></td></tr>
</table>

## Endast CE-funktion {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Funktionen Magento Open Source" src="../assets/open-source.svg" width="20" height="20" /> Alternativ metod krävs för Magento Open Source (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=sv-SE#product-editions">Läs mer</a>)</td></tr>
</table>

## Autentiseringsanteckning för IMS-administratör {#ims-admin-note}

>[!NOTE]
>
>Adobe Commerce-handlare som har en Adobe ID och vill ha en smidig inloggning på Adobe Commerce- och Adobe Business-produkter kan integrera Commerce Admin-autentisering med Adobe IMS-autentiseringsarbetsflödet. När integreringen har aktiverats för din Commerce Store måste varje Admin-användare använda sina Adobe-inloggningsuppgifter - inte sina Commerce-kontouppgifter - för att kunna logga in. Se [Integrera Adobe Commerce med Adobe IMS - översikt](/help/getting-started/adobe-ims-integration-overview.md).

## Information om GTag API:er {#gtag-api-note}

>[!NOTE]
>
>Från och med version 2.4.5 uppdateras integreringen av Google-tjänster så att den stöder användningen av GTag-API:erna. GTag är en enhetlig mekanism för integrering med Google-funktioner för webbsidor och har stöd för de senaste funktionerna och möjligheterna att spåra och hantera innehåll via Google Services. Mer information finns i [dokumentationen för Google Analytics-utvecklare](https://developers.google.com/analytics/devguides/collection/gtagjs).

## Skriv om automatisk överhoppningsanteckning för URL {#url-rewrite-skip}

>[!NOTE]
>
>När automatiska omdirigeringar är aktiverade och du sparar en kategori, genereras alla produkt- och kategoriomskrivningar i realtid och lagras som standard i omskrivningstabeller. Denna process kan leda till betydande prestandaproblem för kategorier med många tilldelade produkter. Lösningen är att ändra den här standardinställningen och hoppa över generering av kategori-/produkt-URL-omskrivningar av produkter för att spara kategorier. I det här fallet genereras produktomskrivningar endast för den kanoniska produkt-URL:en. Mer information finns i [Automatiska produktomdirigeringar](/help/merchandising-promotions/url-redirect-product-automatic.md).

## Anteckning av parametrar för URL-omskrivning {#url-rewrite-params}

>[!IMPORTANT]
>
>Under omdirigeringen tas alla GET-parametrar som anges i URL-adressen bort av säkerhetsskäl.

## Ny prisregel {#new-price-rule}

>[!NOTE]
>
>Prisreglerna bearbetas automatiskt med andra systemregler. Bearbetningsfrekvensen beror på [cron-konfigurationen](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html?lang=sv-SE). När du skapar en prisregel måste du ge den tillräckligt med tid för att komma in i systemet. Testa regeln när du är säker på att den finns i systemet.

## Konfigurationsinställningar {#config}

Om du vill komma åt lagringskonfigurationsinställningarna väljer du **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;i sidofältet_ Admin _.

## UPS API-borttagning {#ups-api}

>[!IMPORTANT]
>
>Från och med juni 2024 kan Adobe Commerce handlare inte längre interagera med den nuvarande UPS-integreringen. Detta beror på att de UPS-API:er (United Parcel Service) som används av den inbyggda Adobe Commerce-integreringen för närvarande inte stöder den OAuth 2.0-säkerhetsmodell som krävs. Om du vill aktivera integreringen [skapar du ett program på UPS-utvecklingsplattformen](https://developer.ups.com/get-started) för att hämta de autentiseringsuppgifter som krävs för OAuth 2.0. Använd de nya inloggningsuppgifterna som `username` och `password` i Commerce UPS-leveranskonfiguration. Mer information om ändringen av säkerhetsmodellen finns i [Migreringsguide för nyckel för utvecklarportal_](https://developer.ups.com/oauth-developer-guide). <br/>
>
>Merchants ska [tillämpa en kvalitetsuppdatering](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html?lang=sv-SE) i sina butiker för att migrera från SOAP API till RESTful API, som har stöd för OAuth 2.0-autentiseringsprotokoll.


## Tillgänglig dokumentation {#docs-links}

| Dokumentationsresurs | Beskrivning |
|----------------------- | ----------- |
| [Användarhandböcker för administratörer i Adobe Commerce 2.4](../landing/home.md) | Dokumentation och resurser för handlare som arbetar i administratören. |
| [Tjänster för Adobe Commerce-dokumentation](https://experienceleague.adobe.com/docs/commerce/user-guides/home.html?lang=sv-SE) | Dokumentation till stöd för en samling marknadsföringstjänster som hjälper handlare att integrera viktiga komponenter i sin verksamhet med sin butik. |
| [Commerce on Cloud Infrastructure Guide](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html?lang=sv-SE) | Stegvisa procedurer för att driftsätta Adobe Commerce på en hanterad, automatiserad värdmolnplattform. |
| [Handböcker för Adobe Commerce 2.4](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html?lang=sv-SE) | Systemdokumentation om koncept, processer, verktyg och bästa metoder för att utveckla, driftsätta och underhålla Adobe Commerce i molnprojekt och lokala projekt. |
| [Adobe Commerce 2.4 Developer Documentation](https://developer.adobe.com/commerce/docs) | Dokumentation för utvecklare som används för att anpassa Adobe Commerce och integrera med tredjepartssystem. |

{style="table-layout:auto"}

## B2B-kompatibilitet {#b2b-compatibility}

>[!IMPORTANT]
>
>Adobe Commerce B2B version 1.4.2+ är kompatibel med PHP 8.2. Om du uppgraderar Commerce-instansen till version 2.4.7+ måste du se till att instansen använder PHP version 8.2 för att bibehålla kompatibiliteten med Adobe Commerce B2B-versionen. Dessutom stöder inte B2B 1.4.2+-versionen [GraphQL Application Server](https://experienceleague.adobe.com/sv/docs/commerce-operations/performance-best-practices/concepts/application-server).
