---
title: Teman
description: Lär dig mer om  [!DNL Commerce] teman, som innehåller layoutfiler, mallfiler, översättningsfiler och skal som definierar utseendet på din butik.
exl-id: d2ccff51-5019-4f80-8eaa-3fe50d5cd6cc
feature: Page Content, Themes
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Teman

Ett tema är en samling filer som avgör den visuella presentationen av din butik. När du installerar [!DNL Commerce] första gången baseras butikens designelement på _Default_ -temat. Förutom det ursprungliga standardtemat som medföljer din [!DNL Commerce]-installation finns det en mängd tillgängliga teman som du kan använda _som_ eller ändra efter behov.

Ett responsivt tema justerar sidlayouten så att den passar enhetens visningsport. Exempeltemat _Luma_ har en flexibel, responsiv layout som kan visas från skrivbordet, surfplattan eller den mobila enheten.

[!DNL Commerce] teman innehåller layoutfiler, mallfiler, översättningsfiler och skal. Ett skal är en samling CSS-, bild- och JavaScript-filer som tillsammans utgör den visuella presentation och de interaktioner som kunderna upplever när de besöker er butik. Teman och skal kan ändras och anpassas av utvecklare eller designproffs som förstår Commerce temadedesign och har tillgång till din server. Mer information finns i [_Utvecklarhandbok för Adobe Premiere_](https://developer.adobe.com/commerce/frontend-core/guide/themes/).

![Lumatema](./assets/design-responsive.png){width="600" zoomable="yes"}

## Standardtemat

Det responsiva `Magento Blank`-temat återger visningen av ditt butiksområde för olika enheter och innehåller metodtips för datorer, tabeller och mobila enheter. Vissa teman är utformade för att endast användas med vissa enheter. När [!DNL Commerce] upptäcker ett specifikt webbläsar-ID, eller en användaragent, används det tema som är konfigurerat för den specifika webbläsaren. Söksträngen kan även innehålla Perl-Compatible Regular Expressions (PCRE).

![Teman](./assets/themes.png){width="700" zoomable="yes"}

### Filtrera temarutnätet

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Filters]**.

1. Ange ett ID-intervall, temanamn (eller titel), mappsökväg eller överordnat tema.

1. Klicka på **[!UICONTROL Apply Filters]** för att uppdatera listan med teman.

## Visa aktuella temainställningar

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**&#x200B;på sidofältet_ Admin _.

1. I listan med installerade teman letar du reda på det tema som du vill granska och klickar på raden för att visa inställningarna.

1. Om du vill visa en exempelsida klickar du på **[!UICONTROL Theme Preview Image]**.

![Förhandsgranska tema](./assets/theme-settings.png){width="600" zoomable="yes"}

## Använd ett standardtema

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Leta reda på den butiksvy som du vill konfigurera och klicka på **[!UICONTROL Edit]** i kolumnen _[!UICONTROL Action]_.

1. Under _[!UICONTROL Default Theme]_&#x200B;anger du **[!UICONTROL Applied Theme]**&#x200B;till den som du vill använda för den aktuella vyn.

   ![Använt tema](./assets/theme-default-apply.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Configuration]** när du är klar.

## Lägg till en användaragentregel

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add New User Agent Rule]** under _[!UICONTROL Design Rule]_.

   ![Designregel](./assets/theme-design-rule.png){width="600" zoomable="yes"}

1. Ange webbläsar-ID för den specifika enheten för **[!UICONTROL Search String]**.

   Söksträngar matchas i den ordning de anges. För Firefox anger du till exempel:

   `/^mozilla/i`

1. Om du vill ange ytterligare enheter upprepar du processen.

1. Klicka på **[!UICONTROL Save Configuration]** när du är klar.
