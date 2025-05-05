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
| [!UICONTROL Date] | Visar ett datumvärde i det [önskade formatet](#date-and-time-options) och [tidszonen](../getting-started/store-details.md#locale-options). Datumvärden kan väljas från en lista eller en kalender ( ![kalenderikon](../assets/icon-calendar.png) ). <br/><br/>**_Obs!_**&#x200B;Beroende på systemkonfigurationen kan_Admin _-användare ange datum direkt i ett fält eller välja ett datum i kalendern eller listan. Mer information om att ange datum- och tidsvärden finns i [Datum- och tidsalternativ](#date-and-time-options). |
| [!UICONTROL Date and Time] | Visar ett datum- och tidsvärde i det [önskade formatet](#date-and-time-options) och [tidszonen](../getting-started/store-details.md#locale-options). Datum och tid kan anges manuellt eller väljas från en kalender. Exempelformat: MM/DD/ÅÅÅÅ HH:MM |
| [!UICONTROL Yes/No] | Visar en nedrullningsbar lista med fördefinierade alternativ för `Yes` och `No`. |
| Listruta | Visar en nedrullningsbar lista med värden som endast accepterar ett val. Indatatypen för listrutan är en nyckelkomponent för [konfigurerbara produkter](../catalog/product-create-configurable.md). |
| [!UICONTROL Multiple Select] | Visar en nedrullningsbar lista med värden som accepterar flera val. |
| [!UICONTROL Price] | Den här indatatypen används för att skapa prisfält utöver de fördefinierade attributen: `Price`, `Special Price`, `Tier Price` och `Cost`. Valutan som används avgörs av systemkonfigurationen. |
| [!UICONTROL Media Image] | Kopplar en extra bild till en produkt, t.ex. en produktlogotyp, anvisningar för omvårdnad eller ingredienser från en livsmedelsetikett. När du lägger till ett mediabildsattribut i en produkts attributuppsättning blir det en extra bildtyp tillsammans med Base, Small och Thumbnail. Mediebildattributet kan uteslutas från medieläsaren [storefront](catalog-images-video.md#storefront-media-browser). |
| [!UICONTROL Fixed Product Tax] | Gör att du kan definiera [FPT-frekvenser](../stores-purchase/fixed-product-tax.md) baserat på kraven för din språkinställning. |
| [!UICONTROL Visual Swatch] | Visar en färgruta som visar färg, struktur eller mönster för en konfigurerbar produkt. En [visuell färgruta](swatches.md) kan fyllas med ett hexadecimalt färgvärde, eller så kan en överförd bild som representerar färg, material, struktur eller mönster för alternativet visas. |
| [!UICONTROL Text Swatch] | En textbaserad representation av ett konfigurerbart produktalternativ som ofta används för storlek. [Textfärgrutor](swatches.md) kan även innehålla hexadecimala färgvärden. |
| [!UICONTROL Page Builder] | En [[!DNL Page Builder]](../page-builder/workspace.md)-arbetsyta på attributplatsen som gör det enkelt att lägga till engagerande innehåll på produktsidan. |

{style="table-layout:auto"}

## Alternativ för datum och tid

Du kan anpassa formatet för datum- och tidsfält och välja den indatakontroll som används för datainmatning. Datumvärden kan väljas från en nedrullningsbar lista eller popup-kalender.

![Exempel - popup-kalender för butiker](./assets/storefront-popup-calendar.png){width="700" zoomable="yes"}

**_Så här formaterar du datum/tid-fält:_**

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Catalog]** i panelen till vänster och klicka på underobjektet **[!UICONTROL Catalog]**.

1. Expandera avsnittet **[!UICONTROL Date & Time Custom Options]**.

   ![Katalogkonfiguration - alternativ för datum och tid](../configuration-reference/catalog/assets/catalog-date-time-custom-options.png){width="600" zoomable="yes"}

   En detaljerad lista över dessa alternativ finns i [_Anpassade alternativ för datum och tid_](../configuration-reference/catalog/catalog.md) i _Konfigurationsreferens_.

1. Om du vill använda en popup-kalender som indatakontroll för datumfält anger du **[!UICONTROL Use JavaScript Calendar]** till `Yes`.

1. Om du vill upprätta **[!UICONTROL Date Fields Order]** anger du ordningen för varje del av datumfältet efter behov:

   - Månad
   - Dag
   - År

1. Ställ in **Tidsformat** på något av följande om du vill ange önskat tidsformat:

   - `12h AM/PM`
   - `24h`

1. Ange år (YYY) för att ställa in **[!UICONTROL from]**- och **[!UICONTROL to]**-datumen om du vill fastställa **[!UICONTROL Year Range]** för de nedrullningsbara värdena.

   Om fältet är tomt används det aktuella året som standard.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
