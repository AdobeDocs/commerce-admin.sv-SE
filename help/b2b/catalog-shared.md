---
title: Översikt över delad katalog
description: Lär dig mer om de delade kataloger som tillhandahålls av Adobe Commerce B2B och hur du kan använda dem för att underhålla kataloger med anpassade priser för olika företagskonton.
exl-id: cf7c9099-9b7d-407b-adb9-06a4815624ee
feature: B2B, Companies, Catalog Management
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# Översikt över delad katalog

Adobe Commerce B2B ger dig möjlighet att underhålla delade _delade_-kataloger med anpassade priser för olika företag. Förutom standardproduktkatalogen, _primär_, ger den kundåtkomst till två typer av delade kataloger med olika prisstrukturer.

Om funktionen [Delad katalog](enable-basic-features.md) är aktiverad i konfigurationen är den ursprungliga primära katalogen fortfarande synlig från Admin, men endast den gemensamma standardkatalogen (Allmänt) visas från arkivet. Dessutom kan egna kataloger skapas som bara är synliga för medlemmar i specifika [företag](account-companies.md)-konton.

För den `Default (General)` offentliga delade katalogen måste du tilldela produkter för att visa katalogen på butiken. Som standard är den tom och innehåller inga produkter.

>[!NOTE]
>
>**[B2B version 1.3.0](release-notes.md#b2b-v130) och senare** - När du skapar en delad katalog anges varje [kategoribehörighet](../catalog/category-permissions.md) för katalogen till _[!UICONTROL Allow for the Display Product Prices]_och_[!UICONTROL Add to Cart]_ för kundgrupper som tilldelas den här åtkomsten i katalogens behörighetsinställningar. Tidigare var de här inställningarna automatiskt inställda på `Deny` även när katalogbehörigheter var inställda på `Allow`.

>[!IMPORTANT]
>
>Alla befintliga [gruppbehörighetsinställningar](../configuration-reference/catalog/catalog.md#category-permissions) ignoreras av **_alla_** kategorier i katalogen när funktionen **_[!UICONTROL Shared Catalog]_** är aktiverad. [!UICONTROL Shared Catalog] styr alla kategoribehörigheter i katalogen när den är aktiverad.

Sidan _[!UICONTROL Shared Catalogs]_ger åtkomst till de verktyg som används för att hantera dina delade kataloger. Sidan liknar standardarbetsytan [för administratörer](../getting-started/admin-workspace.md) med filter och åtgärdskontroller. I rutnätet visas alla delade kataloger, inklusive den gemensamma standardkatalogen och eventuella egna kataloger som du har konfigurerat.

![Delade kataloger](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

## Öppna sidan [!UICONTROL Shared Catalogs]

Gå till **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]** på sidofältet _Admin_.

## Åtgärder

[åtgärdskontrollerna](../getting-started/admin-actions-control.md) i det övre vänstra hörnet kan användas med kontrollen för massåtgärder för att ta bort markerade delade kataloger som inte längre behövs. I stödrastret innehåller kolumnen _[!UICONTROL Actions]_det fullständiga urvalet av verktyg för att hantera dina delade kataloger.

![Åtgärder för delad katalog](./assets/shared-catalog-grid-action-column-controls.png){width="350"}

| Kontroll | Beskrivning |
|------|-----------|
| [[!UICONTROL Set Pricing and Structure]](catalog-shared-pricing-structure.md) | Bestämmer produkturval och anpassade priser som är tillgängliga i den delade katalogen. |
| [[!UICONTROL Assign Companies]](catalog-shared-assign-companies.md) | Avgör vilka företag som kan komma åt en delad katalog. |
| [[!UICONTROL General Settings]](catalog-shared-manage.md) | Anger katalogdetaljinformationen, inklusive namn, katalogtyp, kundskatteklass och beskrivning. |
| [!UICONTROL Delete] | Tar bort de markerade delade katalogerna. |

{style="table-layout:auto"}

## Kolumnbeskrivningar

| Rubrik | Beskrivning |
|--- |--- |
| [!UICONTROL Select] | Väljer delade katalogposter för att tillämpa en åtgärd. Kontrollen i sidhuvudet kan användas för att markera alla eller avmarkera alla delade katalogposter i rutnätet. Markera kryssrutan om du vill välja en enskild delad katalog. |
| [!UICONTROL ID] | En unik numerisk identifierare som tilldelas i sekvens när katalogen skapas. |
| [!UICONTROL Name] | Namnet på den delade katalogen. Som standard är den delade standardkatalogen (Allmänt) tillgänglig. |
| [!UICONTROL Type] | Identifierar typen av delad katalog som antingen: <br/>**[!UICONTROL Public]**- Den gemensamma standardkatalogen skapas automatiskt när Adobe Commerce B2B installeras. Den är ursprungligen tilldelad kundgrupperna `General` och `Not Logged In` och är synlig för gäster och enskilda inloggade kunder som inte är associerade med ett företag. Systemet stöder endast en offentlig delad katalog åt gången.<br/>**[!UICONTROL Custom]** - En anpassad delad katalog innehåller prissättning som bara är synlig för inloggade associationer till de tilldelade företagskontona. Du kan skapa så många anpassade delade kataloger du behöver. |
| [!UICONTROL Customer Tax Class] | Den momsklass som tilldelas motsvarande kundgrupp. Den här kolumnen visas inte i standardstödrastret, men du kan lägga till den genom att ändra kolumnlayouten. |
| [!UICONTROL Created At] | Det datum och den tidpunkt då den delade katalogen skapades. |
| [!UICONTROL Created By] | Förnamn och efternamn för den lagringsadministratör som skapade den delade katalogen. |
| [!UICONTROL Action] | Visar åtgärder som ska tillämpas på valda kataloger. Alternativ: `Set Pricing and Structure` / `Assign Companies` / `General Settings` / `Delete` |

{style="table-layout:auto"}
