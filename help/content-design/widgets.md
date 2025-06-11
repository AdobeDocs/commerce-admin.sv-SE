---
title: Widgetar
description: Lär dig mer om widgetar, som innehåller ett kodfragment som gör det möjligt att visa ett brett innehållsområde och placera det vid särskilda blockreferenser i din butik.
exl-id: 993ba2ca-a8de-4f7e-8cab-7ba7d16eebe7
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 0%

---

# Widgetar

En widget är ett kodfragment som gör det möjligt att visa ett brett innehållsområde och placera det vid särskilda blockreferenser i din butik. Många widgetar visar dynamiska data i realtid och skapar möjligheter för era kunder att interagera med er butik. Med widgetverktyget kan du enkelt placera en widget i befintligt innehåll, till exempel block med bilder och text, och interaktiva element som finns oftast i din butik.

Ni kan använda widgetar för att skapa landningssidor för marknadsföringskampanjer och för att visa kampanjinnehåll på specifika platser i butiken. Du kan också använda widgetar för att lägga till interaktiva element och åtgärdsblock för externa granskningssystem, videochatt, röstformulär och prenumerationsformulär, eller för att tillhandahålla navigeringselement för taggmoln och bildreglage.

{{$include /help/_includes/directives-caution.md}}

![Ny widget för produktlista](./assets/storefront-home-page-new-products.png){width="700" zoomable="yes"}

## Widgettyper

När du [skapar en widget](widget-create.md) måste du ange typen. Den här typen avgör hur widgeten fungerar.

| Typ | Beskrivning |
|--- |--- |
| [!UICONTROL CMS Hierarchy Node Link] | Använd det här alternativet om du vill visa en länk till en viss nod i sidhierarkin som kan införlivas i annat innehåll. |
| [!UICONTROL CMS Page Link] | Använd det här alternativet om du vill ange anpassad text och en rubrik som länkar till en viss CMS-sida. När länken är klar kan den användas på innehållssidor och i block. |
| [!UICONTROL CMS Static Block] | Använd det här alternativet om du vill visa ett innehållsblock på en viss plats på en sida. |
| [!UICONTROL Catalog Category Link] | Använd det här alternativet om du vill visa en textbunden länk eller en blockliknande länk till en vald katalogkategori. När länken är klar kan den användas på innehållssidor och i block. |
| [!UICONTROL Catalog Events Carousel] | Använd det här alternativet om du vill visa en lista över kommande kataloghändelser. |
| [!UICONTROL Catalog New Products List] | Använd det här alternativet om du vill visa ett block med produkter som har utsetts till nya under den tid som anges i produktposten. |
| [!UICONTROL Catalog Product Link] | Använd det här alternativet om du vill visa en textbunden eller blockliknande länk till en vald katalogprodukt. När länken är klar kan den användas på innehållssidor och i block. |
| [!UICONTROL Catalog Products List] | Använd det här alternativet om du vill visa en lista med produkter från katalogen. |
| [!UICONTROL Dynamic Blocks Rotator] | Använd det här alternativet om du vill visa ett enskilt dynamiskt block, eller en uppsättning dynamiska block i en serie, i slumpmässig ordning eller blandad. Det dynamiska blocket kan utlösas av en prisregel och placeras på en viss sida och plats, eller konfigureras att visas på alla sidor. |
| [!UICONTROL Gift Registry Search] | Använd det här alternativet för att ge kunderna möjlighet att söka efter offentliga presentregister efter namn eller register-ID. |
| [!UICONTROL Order by SKU] | Order by SKU kan visas i butiken som en bekvämlighet för alla kunder, eller göras tillgängliga endast för specifika kundgrupper. Köpare kan antingen ange SKU- och kvantitetsinformation direkt i Order by SKU-blocket eller överföra en CSV-fil från sitt kundkonto. |
| [!UICONTROL Orders and Returns] | Använd det här alternativet för att ge gästerna möjlighet att kontrollera status för sina order och skicka in begäranden om att returnera varor. Widgeten visas bara för gäster och kunder som inte är inloggade på sina konton. |
| [!UICONTROL Recently Compared Products] | Visar blocket med nyligen jämförda produkter. Du kan ange antalet produkter som ska inkluderas och formatera dem som en lista eller ett produktrutnät. |
| [!UICONTROL Recently Viewed Products] | Använd det här alternativet om du vill visa blocket med nyligen visade produkter. Du kan ange antalet produkter som ska inkluderas och formatera dem som en lista eller ett produktrutnät. |
| [!UICONTROL Wish List Search] | Använd det här alternativet för att ge en kund möjlighet att söka efter offentligt tillgängliga önskelistor med önskelisteägarens namn eller e-postadress. Butikskunder kan hitta önskelistor som tillhör andra kunder, visa dem och beställa produkter från dem eller lägga till produkterna i sina egna önskelistor. |

{style="table-layout:auto"}
