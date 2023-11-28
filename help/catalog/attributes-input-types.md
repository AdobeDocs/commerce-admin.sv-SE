---
title: Attributindatatyper
description: Lär dig mer om de indatatyper som är tillgängliga för produktattribut, som bestämmer vilken typ av data som kan anges och formatet för fältet eller indatakontrollen.
exl-id: c35b3b9d-57b0-4c33-abdb-662ac6d0260e
feature: Catalog Management, Products
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Attributindatatyper

När attribut visas från administratören är de fält som du fyller i när du skapar en produkt. Indatatypen som tilldelas till ett attribut avgör vilken typ av data som kan anges och formatet för fältet eller indatakontrollen. Ur kundens synvinkel ger attribut information om produkten och är de alternativ och datainmatningsfält som måste fyllas i för att man ska kunna köpa en produkt.

## Indatatyper

| Egenskap | Beskrivning |
|--- |--- |
| [!UICONTROL Text Field] | Ett enradigt inmatningsfält för text. |
| [!UICONTROL Text Area] | Ett inmatningsfält med flera rader för att skriva textstycken, som en produktbeskrivning. Du kan använda WYSIWYG-redigeraren för att formatera texten med HTML-taggar, eller ange taggarna direkt i texten. |
| [!UICONTROL Text Editor] | En fullt fungerande textredigerare på attributplatsen. |
| [!UICONTROL Date] | Visar ett datumvärde i [format](#date-and-time-options) och [tidszon](../getting-started/store-details.md#locale-options). Datumvärden kan väljas från en lista eller en kalender ( ![Kalenderikon](../assets/icon-calendar.png) ). <br/><br/>**_Obs!_**Beroende på systemkonfigurationen,_Administratör _-användare kan ange datum direkt i ett fält eller välja ett datum i kalendern eller listan. Mer information om hur du anger datum- och tidsvärden finns i [Alternativ för datum och tid](#date-and-time-options). |
| [!UICONTROL Date and Time] | Visar ett datum- och tidsvärde i dialogrutan [format](#date-and-time-options) och [tidszon](../getting-started/store-details.md#locale-options). Datum och tid kan anges manuellt eller väljas från en kalender. Exempelformat: MM/DD/ÅÅÅÅ HH:MM |
| [!UICONTROL Yes/No] | Visar en nedrullningsbar lista med fördefinierade alternativ för `Yes` och `No`. |
| Listruta | Visar en nedrullningsbar lista med värden som endast accepterar ett val. Indatatypen för listrutan är en nyckelkomponent i [konfigurerbara produkter](../catalog/product-create-configurable.md). |
| [!UICONTROL Multiple Select] | Visar en nedrullningsbar lista med värden som accepterar flera val. |
| [!UICONTROL Price] | Den här indatatypen används för att skapa prisfält utöver de fördefinierade attributen: `Price`, `Special Price`, `Tier Price`och `Cost`. Valutan som används avgörs av systemkonfigurationen. |
| [!UICONTROL Media Image] | Kopplar en extra bild till en produkt, t.ex. en produktlogotyp, anvisningar för omvårdnad eller ingredienser från en livsmedelsetikett. När du lägger till ett mediabildsattribut i en produkts attributuppsättning blir det en extra bildtyp tillsammans med Base, Small och Thumbnail. Mediebildattributet kan uteslutas från [storefront media browser](catalog-images-video.md#storefront-media-browser). |
| [!UICONTROL Fixed Product Tax] | Här kan du definiera [FPT-räntor](../stores-purchase/fixed-product-tax.md) baserat på kraven för ditt språkområde. |
| [!UICONTROL Visual Swatch] | Visar en färgruta som visar färg, struktur eller mönster för en konfigurerbar produkt. A [visuell färgruta](swatches.md) kan fyllas med ett hexadecimalt färgvärde eller visas en överförd bild som representerar färg, material, struktur eller mönster för alternativet. |
| [!UICONTROL Text Swatch] | En textbaserad representation av ett konfigurerbart produktalternativ som ofta används för storlek. [Textfärgrutor](swatches.md) kan även innehålla hexadecimala färgvärden. |
| [!UICONTROL Page Builder] | A [[!DNL Page Builder]](../page-builder/workspace.md) på den plats där attributet är placerat, vilket gör det enkelt att lägga till engagerande innehåll på produktsidan. |

{style="table-layout:auto"}

## Alternativ för datum och tid

Du kan anpassa formatet för datum- och tidsfält och välja den indatakontroll som används för datainmatning. Datumvärden kan väljas från en nedrullningsbar lista eller popup-kalender.

![Exempel - popup-kalender för butiker](./assets/storefront-popup-calendar.png){width="700" zoomable="yes"}

**_Så här formaterar du datum/tid-fält:_**

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Utöka på panelen till vänster **[!UICONTROL Catalog]** och klicka på **[!UICONTROL Catalog]** underobjekt.

1. Expandera avsnittet **[!UICONTROL Date & Time Custom Options]**.

   ![Katalogkonfiguration - datum- och tidsalternativ](../configuration-reference/catalog/assets/catalog-date-time-custom-options.png){width="600" zoomable="yes"}

   En detaljerad lista över dessa alternativ finns på [_Anpassade alternativ för datum och tid_](../configuration-reference/catalog/catalog.md) i _Konfigurationsreferens_.

1. Ange en popup-kalender som indatakontroll för datumfält **[!UICONTROL Use JavaScript Calendar]** till `Yes`.

1. För att fastställa **[!UICONTROL Date Fields Order]**, ställ in ordningen för varje del av datumfältet efter behov:

   - Månad
   - Dag
   - År

1. Ange önskat tidsformat **Tidsformat** till något av följande:

   - `12h AM/PM`
   - `24h`

1. För att fastställa **[!UICONTROL Year Range]** för värdena i listrutan anger du år (ÅÅÅÅ) för att ange **[!UICONTROL from]** och **[!UICONTROL to]** datum.

   Om fältet är tomt används det aktuella året som standard.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.
