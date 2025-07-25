---
title: '[!UICONTROL Content]-menyn'
description: Använd menyn [!UICONTROL Content] för att få tillgång till flera funktioner för att hantera innehållet i din butik.
exl-id: 4e149836-f13c-4240-8700-882f2fc1619a
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# [!UICONTROL Content]-menyn

>[!NOTE]
>
>När den nya [[!DNL Media Gallery]](media-gallery.md) är aktiverad visas avsnittet _[!UICONTROL Media]_&#x200B;med ett alternativ för åtkomst till [!DNL Media Gallery]. Du kan ange alternativet **[!UICONTROL Enable Old Media Gallery]**&#x200B;till `No` genom att gå till **[!UICONTROL Stores]**>_[!UICONTROL Settings]_ > **[!UICONTROL Configuration]** och välja **[!UICONTROL Advanced]** > **[!UICONTROL System]** i den vänstra panelen.

>[!BEGINTABS]

>[!TAB Adobe Commerce]

[!BADGE Endast PaaS]{type=Informative url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."}

![Menyn [!UICONTROL Content] som visas i Admin](./assets/admin-menu-content.png){width="400" zoomable="yes"}

>[!TAB Adobe Commerce as a Cloud Service]

[!BADGE Endast SaaS]{type=Positive url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce as a Cloud Service- och Adobe Commerce Optimizer-projekt (SaaS-infrastruktur som hanteras av Adobe)."}

![Menyn [!UICONTROL Content] som visas i Admin](./assets/admin-menu-content-accs.png){width="400" zoomable="yes"}

>[!ENDTABS]

## Visa menyn [!UICONTROL Content]

Välj **[!UICONTROL Content]** på sidofältet _Admin_.

## [!UICONTROL Elements]

- Skapa [sidor](pages.md) med text, bilder, block, variabler och widgetar. Dina sidor kan integreras i navigeringen i din butik och länkas till andra sidor.
- ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Ordna sidorna i en [hierarki](page-hierarchy.md) med navigering.
- Skapa [block](blocks.md) med innehåll utan att skriva kod. Block kan innehålla text, bilder och till och med video och kan tilldelas valfri del av sidlayouten.
- ![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce) Skapa [dynamiska block](dynamic-blocks.md) för att införliva interaktivt innehåll som styrs av logik från [prisregler](../merchandising-promotions/introduction.md#promotions) och [kundsegment](../customers/customer-segments.md).
- Skapa [widgetar](widgets.md) som visar dynamiska data och lägger till block, länkar och interaktiva element nästan var som helst i din butik.
- Skapa [mallar](../page-builder/templates.md) från ditt Page Builder-innehåll och spara tid och arbete när du lägger till nytt innehåll (eller ersätter äldre innehåll).

>[!NOTE]
>
>Alternativet _[!UICONTROL Banners]_&#x200B;på den här menyn har tagits bort från 2.3.1 och har nu tagits bort. Funktionen ersätts av Dynamic Blocks.

## [!UICONTROL Design] {#design-features}

Hantera butikens visuella presentation:

- Ange [designkonfigurationen](configuration.md) om du vill behålla olika inställningar för varje webbplats, butik och vy i din [!DNL Commerce]-installation.

- Använd [teman](themes.md), som är samlingar av layoutfiler, mallfiler, översättningsfiler och skal, för att fastställa butikens visuella presentation.

- Använd [Schedule](schedule.md) för att planera temaändringar i förväg för en säsong eller befordran.

## [!UICONTROL Content Staging]

{{ee-feature}}

[Mellanlagring av innehåll](content-staging.md) ger ditt affärsteam möjlighet att enkelt skapa, förhandsgranska och schemalägga ett brett urval av innehållsuppdateringar direkt från administratören för din butik.
