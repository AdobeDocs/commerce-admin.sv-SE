---
title: Introduktion till [!DNL B2B for Adobe Commerce]
description: Lär dig hur ni kan använda de integrerade B2B-funktionerna för att tillgodose era behov hos kunder som är företag.
exl-id: fc7e8147-5fd5-4e4b-b16e-0b0d54c415da
feature: B2B
source-git-commit: fb075822e318073053cdf8cdd5cd9bb3a6343904
workflow-type: tm+mt
source-wordcount: '841'
ht-degree: 0%

---

# Introduktion till [!DNL B2B for Adobe Commerce]

Till skillnad från standardmodellen företag-till-kund är de integrerade B2B-funktionerna (Business to Business) utformade för att uppfylla behoven hos säljare (Adobe Commerce handlare) som har kunder som är företag. Det passar företag med komplexa organisationsstrukturer och flera användare med olika roller och nivåer av inköpsbehörighet. En typisk B2B-kund kan vara chef för en butik eller en köpare som handlar för ett företags räkning. I båda fallen sker transaktionen mellan ert företag och deras företag. Du kan också sälja produkter direkt till konsumenten. [!DNL B2B for Adobe Commerce] är en integrerad lösning som har stöd för både B2B- och B2C-modeller.

Med [installation](install.md) och [aktivering](enable-basic-features.md) av B2B-tillägget i din Adobe Commerce-butik kan köpupplevelsen anpassas med kundspecifika kataloger och priser samt riktat innehåll och riktade kampanjer.

## Företagskonton

Företagskontokomponenten är en nyckelenhet inom B2B som alla andra funktioner på något sätt är beroende av. Det gör det möjligt att gå samman flera köpare som tillhör ett enda företag till ett enda företagskonto (eller företagskonto). Företagsadministratören kan skapa en företagsstruktur (divisioner, delsektioner och användare) som återspeglar företagets operativa modell och ger olika användarroller och behörigheter för företagsmedlemmar. Med den här strukturen kan företagsadministratören styra användaraktiviteten för företagskontot: beställning, offert, inköp, åtkomst till företagets kreditinformation eller profil osv.

Från administratören kan administratören för Commerce-webbplatsen konfigurera hur företaget arbetar på webbplatsen. Konfiguration avgör vilka B2B-funktioner som är tillgängliga för företagsanvändare, inklusive betalningsmetoder, prisnivåer, möjligheten att förhandla priser med hjälp av offerter, möjligheten att skapa rekvisitionslistor med mera.

Mer information finns i [Företagskonton](account-companies.md).

>[!NOTE]
>
>När den är aktiverad kan din butik ge företagen möjlighet att _Betala på konto_, vilket innebär att göra inköp på en företagskreditrad. Som handlare kan du allokera kredit för ett företagskonto och hantera kreditinställningar för ett företag samt återbetala kredit.

## Företagsledning

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Endast tillgängligt för betaprogramdeltagare"}

Med företagsledning kan handlaradministratörer effektivisera administration och hantering av B2B-organisationer med komplexa operativa modeller.

Användare med rätt behörighet från administratören kan skapa en **[!UICONTROL Company Hierarchy]** som återspeglar organisationsstrukturen i ett affärsföretag som består av flera företag. Med den här hierarkin kan de visa och hantera företag som en grupp. Administratören kan till exempel utse ett moderföretag och tilldela alla företag som är verksamma som dotterföretag till moderbolaget. Därefter kan administratören för det överordnade företaget visa och hantera företagskonton för alla tilldelade företag.

Mer information finns i [Företagshantering](manage-companies.md).

## Tjänster för Adobe Commerce

Tjänster för Adobe Commerce är värdtjänster som ger utökade möjligheter för Adobe Commerce och Magento Open Source. Tjänster som stöder B2B-arbetsflöden är:

* [Katalogtjänst](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html)
* [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html)
* [Recommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html)

## Delade kataloger

Delade kataloger är de prisnivåer som gör det möjligt att ange anpassade priser per produkt för olika företag på en eller flera webbplatser. Genom att använda delade kataloger kan ni sälja produkter genom att tillämpa olika prisnivåer för olika kundgrupper. Stöd för delade kataloger är bara tillgängligt för Commerce-butiker som har konfigurerats för att stödja företagskonton.

Mer information finns i [Arbeta med delade kataloger](catalog-shared.md).

## Snabbordning

Konfigurera Snabbordning för att reducera orderprocessen till flera klick för inloggade kunder när de känner till produktnamnet eller SKU:n för de produkter de vill beställa.

Mer information finns i [Snabborder](quick-order.md).

## Förhandlingsbara offerter

Använd funktionen Offerter för att initiera prisförhandlingar mellan en företagsköpare och en säljare.

* En auktoriserad köpare kan initiera en offert från kundvagnen.

* En säljare kan initiera en offert för en köpare från Admin.

Köpare och säljare använder offerten för att hantera förhandlingsprocessen - till exempel lägga till artiklar, uppdatera kvantiteter, begära och tillämpa rabatter - tills de når ett avtal. The _Citat_ rutnätet i Admin visar varje mottagen offert och underhåller en historik över kommunikationen mellan köpare och säljare.

Stöd för Negotiable Quotes är endast tillgängligt för Commerce-butiker som har konfigurerats för att stödja företagskonton.

Mer information finns i [Förhandlingsbara offerter](quotes.md).

## Godkännanden av inköpsorder

När inköpsorder aktiveras för ett företagskonto skapas alla order automatiskt som inköpsorder (PO). Företagsanvändare med nödvändig behörighet kan skapa, redigera och ta bort inköpsordrar som de skapar och inköpsordrar som skapas av underordnade användare. Beroende på deras roll och beställning kan företagsanvändare omfattas av flera godkännanderegler.

Mer information finns i [Inköpsorder för företag](purchase-order-flow.md).

## Rekvisitionslistor

Kunder kan använda rekvisitionslistan för att spara tid när de köper ofta beställda produkter, eftersom de kan lägga till artiklar i kundvagnen direkt från listan. De kan ha flera listor som fokuserar på produkter från olika leverantörer, köpare, team, kampanjer eller annat som effektiviserar arbetsflödet.

Mer information finns i [Rekvisitionslistor](requisition-lists.md).
