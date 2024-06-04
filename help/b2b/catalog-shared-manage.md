---
title: Hantera dina delade kataloger
description: Läs mer om den information och de verktyg som finns på sidan Delade kataloger.
exl-id: a01ac292-240d-42e7-b4c9-2982f293c521
feature: B2B, Companies, Catalog Management
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 0%

---

# Hantera dina delade kataloger

The _[!UICONTROL Shared Catalogs]_-sidan ger tillgång till de verktyg som behövs för att hantera dina delade kataloger. Sidan liknar standardarbetsytan för administratörer med filter och åtgärdskontroller. I rutnätet visas alla delade kataloger, inklusive den gemensamma standardkatalogen och eventuella egna kataloger som du har konfigurerat.

## Uppdatera produktvalet

Urvalet av produkter i en delad katalog kan enkelt uppdateras via _[!UICONTROL Action]_-kolumnen i stödrastret för delade kataloger. De ändringar du gör är synliga för medlemmar i associerade företagskonton. Processen är i stort sett densamma som att välja produkter för en ny [katalogstruktur](catalog-shared-pricing-structure.md), förutom att konfigurationens omfattning inte kan ändras.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. För den delade katalogen i rutnätet går du till **[!UICONTROL Action]** kolumn och markera **[!UICONTROL Set Pricing and Structure]**.

   ![Stödraster och åtgärdsmeny för delad katalog](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. Följ instruktionerna i [Steg 2: Välj produkter](catalog-shared-pricing-structure.md#step-2-choose-the-products).

   Du kan hoppa över det första objektet eftersom omfånget för en delad katalog inte kan ändras när den har sparats för första gången.

Om du arbetar med en viss produkt _[!UICONTROL Products In Shared Catalog]_finns en lista över alla delade kataloger där produkten är tillgänglig. Mer information finns på [Lägga till produkter i en delad katalog](catalog-shared-product-add.md).

![Produkt i delade kataloger](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

## Uppdatera anpassade priser

De anpassade priserna för produkter i alla delade kataloger kan enkelt uppdateras från åtgärdskolumnen i rutnätet för delade kataloger. De ändringar du gör är synliga i butiken för medlemmar i det associerade företaget eller kundgruppen. Processen är i stort sett densamma som att ange anpassade priser för en ny [delad katalog](catalog-shared-pricing-structure.md), förutom att konfigurationens omfattning inte kan ändras.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. För den delade katalogen i rutnätet som du vill uppdatera går du till **[!UICONTROL Action]** kolumn och markera **[!UICONTROL Set Pricing and Structure]**.

1. På _[!UICONTROL Catalog Structure]_sida, klicka **[!UICONTROL Configure]**och gör något av följande:

   - Klicka på förloppsindikatorn längst upp på sidan **[!UICONTROL Pricing]**.
   - Klicka på i det övre högra hörnet **[!UICONTROL Next]**.

1. Följ instruktionerna i [Steg 3: Ange anpassade priser](catalog-shared-pricing-structure.md#step-3-set-custom-prices).

## Uppdatera kategoribehörigheter

[Kategoribehörigheter](../catalog/category-permissions.md) ställs in automatiskt på `Allow` för produkter som läggs till från kategoriträdet till en delad katalog. Du kan senare justera behörigheterna eller skapa ytterligare regler efter behov.

>[!NOTE]
>
>**[B2B version 1.3.0](release-notes.md#b2b-v130) och senare** - När du skapar en delad katalog [kategoribehörighet](../catalog/category-permissions.md) för katalogen är inställd på `Allow` för _[!UICONTROL Display Product Prices]_och_[!UICONTROL Add to Cart]_ för kundgrupper som har tilldelats den här åtkomsten i katalogens behörighetsinställningar. Tidigare var dessa inställningar automatiskt inställda på `Deny` även när katalogbehörigheter har angetts till `Allow`.

>[!IMPORTANT]
>
>Alla befintliga [gruppbehörighetsinställningar](../configuration-reference/catalog/catalog.md#category-permissions) ignoreras av **_alla_** i katalogen när **_[!UICONTROL Shared Catalog]_** funktionen är aktiverad. [!UICONTROL Shared Catalog] har fullständig kontroll över alla kategoribehörigheter i katalogen när den är aktiverad.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Välj kategorin för de produkter som du vill uppdatera i kategoriträdet.

   Om du vill inkludera alla produkter väljer du den översta kategorin i trädet.

1. Rulla ned och expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Category Permissions]** -avsnitt.

1. Klicka **[!UICONTROL New Permission]** och gör följande:

   ![Ny behörighet](./assets/category-permissions-new.png){width="600" zoomable="yes"}

   - Välj **[!UICONTROL Customer Group]** som motsvarar den delade katalogen och ändrar behörighetsinställningarna efter behov.

     ![Regel för kategoribehörigheter](./assets/shared-catalog-category-permissions.png){width="600" zoomable="yes"}

   - Om du vill skapa en behörighetsregel för en annan kundgrupp klickar du på **[!UICONTROL New Permissions]** och upprepa processen.

   - Om du vill ta bort en behörighetsregel klickar du på _Ta bort_ ![Papperskorgen](../assets/icon-delete-trashcan-solid.png) -ikon.

1. När du är klar klickar du på **[!UICONTROL Save]**.

## Uppdatera kataloginformationen

Detaljinformationen i alla delade kataloger kan enkelt uppdateras från åtgärdskolumnen i rutnätet för delade kataloger. De ändringar du gör återspeglas i alla associerade företagskonton.

![Allmänna inställningar](./assets/shared-catalog-grid-general-settings.png){width="700" zoomable="yes"}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. För den delade katalogen som du vill uppdatera går du till **[!UICONTROL Action]** kolumn och markera **[!UICONTROL General Settings]**.

   ![Kataloginformation](./assets/shared-catalog-update-details.png){width="600" zoomable="yes"}

1. Uppdatera kataloginformationen efter behov.

   - Om du ändrar namnet på en delad katalog ändras även namnet på motsvarande kundgrupp.
   - Ändra katalogtypen från `Custom` till `Public` konverterar den befintliga offentliga katalogen till en anpassad katalog. Alla företag som är associerade med den ursprungliga offentliga katalogen tilldelas om till ersättningen. En offentlig katalog kan inte konverteras till en anpassad katalog.

1. När du är klar klickar du på **[!UICONTROL Save]**.

## Referens för sida med delad katalog

### Knappfält

| Knapp | Beskrivning |
|--- |--- |
| [!UICONTROL Back] | Återgår till sidan Delade kataloger utan att spara den nya delade katalogen. |
| [!UICONTROL Delete] | Tar bort katalogen och tilldelar eventuella associerade företag och deras medlemmar till den offentliga delade katalogen. |
| [!UICONTROL Reset] | Rensar formen på ändringar som inte har sparats och återställer den ursprungliga katalogdetaljinformationen. |
| [!UICONTROL Duplicate] | Skapar en [duplicerad kopia av katalogen](catalog-shared-create.md). För en anpassad katalog är prismodellen och strukturen för originalet, men utan företagsorganisationerna. Om en offentlig delad katalog dupliceras, ändras typen för den duplicerade katalogen till `custom`. En motsvarande kundgrupp skapas också med samma namn som den duplicerade katalogen. Som standard har en duplicerad katalog samma namn _Duplicera_ den ursprungliga katalogen. |
| [!UICONTROL Save and Continue Edit] | Sparar alla ändringar och låter formuläret vara öppet i redigeringsläge. |
| [!UICONTROL Save] | Sparar ändringar, stänger formuläret och återgår till sidan Delade kataloger. |

{style="table-layout:auto"}

### Kataloginformation

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Name] | Identifierar den delade katalogen i hela administratören och i kundkontona där den är tillgänglig. Katalognamnet ska vara beskrivande och högst 32 tecken långt. Du kan inte ha två delade kataloger med samma namn. Maximalt antal tecken: 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** - Identifierar en katalog med anpassade priser som bara är tillgänglig för de specifika företag som den är tilldelad till.<br/>**[!UICONTROL Public]**- Identifierar den delade katalogen som är tillgänglig för alla gästbesökare och inloggade kunder som inte är associerade med ett företag. En offentlig standardkatalog skapas när Adobe Commerce B2B installeras, men måste konfigureras av administratören. Det får bara finnas en offentlig delad katalog åt gången. |
| [!UICONTROL Customer Tax Class] | Bestämmer den momsklass som används för inköp som görs från katalogen. Alternativen omfattar alla tillgängliga momsklasser. |
| [!UICONTROL Description] | En kort förklaring av hur katalogen ska användas. |

{style="table-layout:auto"}
