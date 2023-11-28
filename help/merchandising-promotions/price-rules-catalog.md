---
title: Katalogprisregler
description: Lär dig mer om katalogprisregler som kan användas för att erbjuda produkter till köpare till ett rabatterat pris baserat på en uppsättning definierade villkor.
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# Katalogprisregler

Katalogprisregler kan användas för att erbjuda produkter till köpare till rabatterat pris, baserat på en uppsättning definierade villkor. Katalogprisreglerna använder inte [kupongkoder](price-rules-cart-coupon.md), eftersom de aktiveras innan en produkt placeras i kundvagnen.

Du kan till exempel definiera och ange villkoren för en prisregel som när den är uppfylld automatiskt visar produkter med ett särskilt eller kampanjpris. Definierade regelegenskaper kan omfatta kundgrupper, produktkategorier, ett rabattbelopp eller en procentandel, produktfärg, produktstorlek eller så gott som alla produktattribut som finns i din butik. Du kan ange start- och slutdatum för en prisregel som automatiskt startar och stoppar en kampanj på de datum som du definierar i regeln. Egenskaperna för en sparad regel kan uppdateras eller ändras efter behov.

- ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Du kan även länka en definierad regel till en [dynamiskt block](../content-design/dynamic-blocks.md) för att marknadsföra evenemanget eller produkten i din butik.

- ![Magento Open Source](../assets/open-source.svg) (Endast Magento Open Source) För återkommande kampanjer kan du manuellt ange en sparad regel till _Aktiv_ eller _Inaktiv_ status varje gång du vill köra kampanjen.

## Få tillgång till prisregler för kataloger

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

   ![Katalogprisregler](./assets/price-rule-catalog.png){width="700" zoomable="yes"}

1. Uppdatera egenskaper för en regel:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Klicka på **[!UICONTROL Edit]** för att visa _Regelinformation_ sida.

   - ![Magento Open Source](../assets/open-source.svg) (Endast Magento Open Source) Klicka på regeln i listan för att visa sidan Regelinformation.

   Här kan du ändra inställningarna för linjen (liknande [skapa en regel](price-rules-catalog-create.md)).

## Filteralternativ

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL ID] | Ange text för att filtrera listan efter ett visst regel-ID-nummer. |
| [!UICONTROL Rule] | Ange text för att filtrera listan baserat på det regelnamn som definierades när regeln skapades. |
| [!UICONTROL Priority] | ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Ange text i det här fältet för att filtrera listan baserat på den prioritet som har definierats för en regel. |
| [!UICONTROL Web Site] | ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Använd det här alternativet om du vill filtrera listan baserat på webbplatser som definierats för en regel. |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) (Endast Adobe Commerce) Klicka på **[!UICONTROL Edit]** om du vill visa regelinformationen och uppdatera regelinställningarna (ungefär som att skapa en regel). |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) (Endast Magento Open Source) Använd de dynamiska kalenderfälten (Till: och Från:) för att filtrera listan baserat på regelns startdatum som det definierades när regeln skapades. |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) (Endast Magento Open Source) Använd de dynamiska kalenderfälten (Till: och Från:) för att filtrera listan baserat på slutdatumet för regeln som den definierades när regeln skapades. |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (Endast Magento Open Source) Använd det här alternativet om du vill filtrera listan baserat på regelstatus (`Active` eller `Inactive`). |

{style="table-layout:auto"}

## Felsökningsresurser

Hjälp om hur du felsöker problem med katalogprisregler finns i följande artiklar i kunskapsbasen med Commerce Support:

- [404 Fel i butiksleverans när uppdatering av katalogiffegler har utförts](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/404-error-on-store-front-once-catalog-price-rule-schedules-update-is-performed.html)
- [Förbättrade prestanda för produktsidor med relaterade produkter och målregler](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-31791-magento-patch-improvement-for-product-page-with-related-products-and-target-rules.html)
- [Katalogens prisregler fungerar inte](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-24201-magento-patch-catalog-price-rules-don-t-work.html)
- [GraphQL prisberäkningar](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33975-magento-patch-graphql-price-calculations.html)
