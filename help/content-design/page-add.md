---
title: Lägga till och ta bort sidor
description: Lär dig hur du lägger till och tar bort innehållssidor som används i [!DNL Commerce] butik.
exl-id: a7a503ea-3631-4be2-81e4-aed2ae9419dc
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 0%

---

# Lägga till och ta bort sidor

Processen att lägga till en innehållssida i din butik är i stort sett densamma för alla typer av sidor som du kanske vill skapa. Du kan inkludera text, bilder, innehållsblock, variabler och widgetar. De flesta innehållssidor är utformade för att läsas av sökmotorer först och av andra. Tänk på behoven för var och en av dessa två olika målgrupper när du väljer sidrubrik, URL-adress och när du komponerar metadata och innehåll. När sidan är klar kan den läggas till i din butiksnavigering, länkas till andra sidor, länkas från butikens sidfot eller användas som en ny [hemsida](page-home-new.md).

![Sidstödraster](./assets/pages-grid.png){width="700" zoomable="yes"}

## Lägga till en sida

I följande instruktioner får du hjälp med varje steg för att skapa en enkel sida. Vissa avancerade funktioner hoppas över, men beskrivs i andra ämnen.

### Steg 1: Skapa sidan

1. På _Administratör_ sidebar, gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Klicka på **[!UICONTROL Add New Page]**.

   ![Ny sida](./assets/pages-new-page.png){width="600" zoomable="yes"}

1. Om du inte vill publicera sidan direkt anger du **[!UICONTROL Enable Page]** till `No`.

1. Ange **[!UICONTROL Page Title]**.

   Sidans rubrik visas på sidan [breadcrumb](../catalog/navigation-breadcrumb-trail.md) navigering.

### Steg 2: Slutför innehållet

Beroende på din [Konfiguration av avancerade verktyg för innehåll](../configuration-reference/general/content-management.md), lägger till sidinnehållet.

#### Använda innehållsverktygen i Page Builder

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![Innehåll med Page Builder](../page-builder/assets/pb-page-content.png){width="600" zoomable="yes"}

1. I **[!UICONTROL Content Heading]** anger du den rubrik som du vill ska visas överst på sidan.

   Om den är aktiverad visas [Page Builder](../page-builder/introduction.md) -scenen och -panelen visas under innehållsrubriken. Mer information finns i [Arbetsyta](../page-builder/workspace.md). If _Page Builder_ är inte aktiverat öppnas redigeraren i WYSIWYG-läge med verktygsfältet överst.

1. Fyll i innehållet och formatera texten efter behov.

#### Använda redigeringsverktygsfältet

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![Innehåll](./assets/page-content-editor.png){width="600" zoomable="yes"}

1. I **[!UICONTROL Content Heading]** anger du den rubrik som du vill ska visas överst på sidan.

1. Fyll i innehållet och formatera texten efter behov.

   Du kan lägga till [bilder](media-storage.md), [variabler](../systems/variables-predefined.md)och [widgetar](widgets.md) efter behov. Mer information finns i [Använda redigeraren](editor.md).

### Steg 3: Fyll i SEO-informationen

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]**.

   ![Sökmotoroptimering](./assets/page-search-engine-optimization.png){width="600" zoomable="yes"}

1. Acceptera standardinställningen eller ange en annan **[!UICONTROL URL Key]** som består av alla gemener, med bindestreck i stället för mellanslag.

   Standardnyckeln för URL skapades när sidan sparades och baseras på rubriken Innehåll.

1. Ange en **[!UICONTROL Meta Title]** för sidan.

   Meta-title får inte innehålla fler än 70 tecken och visas i webbläsarens namnlist och på fliken.

1. Ange det värde du vill ha **[!UICONTROL Meta Keywords]** som sökmotorer kan använda för att indexera sidan.

   Avgränsa flera ord med komma. Meta-nyckelord ignoreras av vissa sökmotorer, men används av andra.

1. För **[!UICONTROL Meta Description]**, anger du en kort beskrivning av sidan för sökresultatlistor.

   I idealfallet bör beskrivningen vara 150-160 tecken lång, med en maxgräns på 255.

1. Klicka på **[!UICONTROL Save]**.

### Steg 4: Ange sidans omfattning

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Page in Websites]**.

   ![Sidor på webbplatser](./assets/page-in-websites.png){width="600" zoomable="yes"}

1. I **[!UICONTROL Store View]** väljer du varje vy där sidan ska vara tillgänglig.

   Om installationen har flera webbplatser väljer du varje webbplats och butiksvy där sidan ska vara tillgänglig.

### Steg 5: Identifiera den överordnade sidan (om tillämpligt)

{{ee-feature}}

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Hierarchy]**.

   ![Hierarki](./assets/page-hierarchy.png){width="600" zoomable="yes"}

1. Om den här sidan är underordnad en annan sida markerar du kryssrutan för **[!UICONTROL Parent page]**.

### Steg 6: Ange designändringar (valfritt)

1. Om du vill ändra sidans layout expanderar du ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Design]**.

   ![Design](./assets/page-design.png){width="600" zoomable="yes"}

1. Om du vill ändra sidans kolumnlayout anger du **[!UICONTROL Layout]** till något av följande:

   - `Empty`
   - `1 column`
   - `2 columns with left bar`
   - `2 columns with right bar`
   - `3 columns`
   - `Page -- Full Width` (Kräver [Page Builder](../page-builder/introduction.md))
   - `Category -- Full Width` (Kräver Page Builder)
   - `Product -- Full Width` (Kräver Page Builder)

1. Använda en **[!UICONTROL Custom Layout Update]** väljer du namnet på filen i listan.

   Mer information finns i [Layoutuppdateringar](layout-updates.md).

1. Om du vill ändra sidans tema anger du **[!UICONTROL New Theme]** till något av följande:

   - `Magento Black`
   - `Magento Luma`

1. ![Magento Open Source](../assets/open-source.svg) (Endast Magento Open Source) Om du vill schemalägga en designändring expanderar du ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Custom Design Update]** och gör följande:

   ![Anpassad designuppdatering](./assets/page-custom-design-update.png){width="600" zoomable="yes"}

   - Använd kalendern (![Kalenderikon](../assets/icon-calendar.png)) för att välja **[!UICONTROL From]** och **[!UICONTROL To]** datum för när ändringen ska träda i kraft.

   - Om du vill använda ett annat tema på sidan väljer du namnet på **[!UICONTROL New Theme]**.

   - Välj knappen **[!UICONTROL Layout]** som du vill använda.

### Steg 7: Förhandsgranska sidan

1. Klicka på **[!UICONTROL Save]** pil och välj **[!UICONTROL Save & Close]** för att återgå till sidstödrastret.

1. Hitta sidan i rutnätet och markera **[!UICONTROL View]** i _[!UICONTROL Action]_kolumn.

1. Om du vill gå tillbaka till rutnätet klickar du på **[!UICONTROL Back]** i det övre vänstra hörnet i webbläsarfönstret.

### Steg 8: Publicera sidan

1. Välj **[!UICONTROL Edit]** i _[!UICONTROL Action]_stödrastrets kolumn.

1. Ange **[!UICONTROL Enable Page]** till `Yes`.

1. Klicka på **[!UICONTROL Save]** pil och välj **[!UICONTROL Save & Close]**.

## Duplicera en sida

Alla innehållssidor kan användas som mallar och sparas som dubbletter. Du kan använda den här tidsbesparande tekniken för att skapa en enhetlig design för innehållssidor på hela webbplatsen. Den duplicerade sidan behåller den ursprungliga sidans titel, men fälten URL-nyckel och Status måste uppdateras.

![Spara och duplicera](./assets/page-duplicate-save-menu.png){width="600" zoomable="yes"}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Leta reda på sidan som du vill duplicera i rutnätet och klicka på **[!UICONTROL Edit]** i _[!UICONTROL Action]_kolumn.

1. Klicka på **[!UICONTROL Save]** pil och välj **[!UICONTROL Save & Duplicate]**.

1. När du ser meddelanden om att sidan har sparats och duplicerats klickar du **[!UICONTROL Back]** i det övre knappfältet för att gå tillbaka till rutnätet.

1. Hitta den duplicerade sidan i rutnätet och notera följande:

   - Sidrubriken är densamma som originalet.
   - En unik, men tillfällig URL-nyckel tilldelas.
   - Sidans status är `Disabled`.

1. Öppna den duplicerade sidan i _Redigera_ och gör följande:

   - Om du vill publicera sidan direkt anger du **[!UICONTROL Enable Page]** till `Yes`.

   - Uppdatera **[!UICONTROL Page Title]**, efter behov.

   - Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Search Engine Optimization]** och ange det unika **[!UICONTROL URL Key]** som du vill använda för den duplicerade sidan.

     ![Tillfällig URL-nyckel](./assets/page-search-engine-optimization-url-key-duplicate.png){width="600" zoomable="yes"}

   - Uppdatera det återstående sidinnehållet efter behov.

1. Klicka på **[!UICONTROL Save]** pil och välj **[!UICONTROL Save & Close]**.

   Den duplicerade sidan i rutnätet återspeglar dina ändringar.

## Spara-menyn

| Kommando | Beskrivning |
|--- |--- |
| [!UICONTROL Save] | Spara den aktuella sidan och fortsätt arbeta. |
| [!UICONTROL Save & New] | Spara och stäng den aktuella sidan och påbörja en ny sida. |
| [!UICONTROL Save & Duplicate] | Spara och stäng den aktuella sidan och öppna en ny kopia. |
| [!UICONTROL Save & Close] | Spara och stäng den aktuella sidan och gå tillbaka till sidstödrastret. |

{style="table-layout:auto"}

## Ta bort en sida

Det finns två sätt att ta bort en skapad sida. Du kan ta bort den från _[!UICONTROL Pages]_stödraster eller från_[!UICONTROL Edit]_ sida.

### Metod 1: Ta bort en sida från sidstödrastret

1. På _Administratör_ sidebar, gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Leta upp sidorna med hjälp av filter ovanför stödrastret och markera kryssrutan för en eller flera sidor som ska tas bort.

1. I listans övre vänstra hörn anger du **[!UICONTROL Actions]** till `Delete`.

1. Bekräfta åtgärden genom att klicka **[!UICONTROL OK]**.

### Metod 2: Ta bort en sida från redigeringssidan

1. På _Administratör_ sidebar, gå till **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Hitta sidan som ska tas bort.

1. I _[!UICONTROL Actions]_kolumn för sidenheten klickar du på&#x200B;**[!UICONTROL Select]**och välja **[!UICONTROL Edit]**.

1. Klicka på i knappfältet **[!UICONTROL Delete Page]**.

1. Bekräfta åtgärden genom att klicka **[!UICONTROL OK]**.
