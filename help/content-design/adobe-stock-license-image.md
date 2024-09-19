---
title: Licensiera en Adobe Stock-bild
description: För att säkerställa att du har laglig åtkomst och för att ta bort Adobe Stock-vattenstämpeln licensierar du dina Adobe Stock-bilder.
exl-id: a2d6b7b8-e9ac-4f3e-bcd1-05e2bb74b6c2
feature: CMS, Media
source-git-commit: ee619d6a46948a714789dfbc275735df8669cdcb
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---

# Licensiera en Adobe Stock-bild

Adobe Stock-mediefiler som du vill använda för din produktion i Adobe Commerce och Magento Open Source butiker bör licensieras. Med den här licensieringen får du laglig åtkomst till bilden och kan ta bort den Adobe Stock-vattenstämpel som finns i alla [bildförhandsvisningar][save-preview]. Om du vill licensiera bilder eller spara redan licensierade bilder måste du vara inloggad på ditt Adobe-konto.

Den nya [[!DNL Media Gallery]](media-gallery.md) har en direkt integrering med Adobe Stock, vilket gör det enkelt att licensiera dina bilder direkt från gallerisidan.

>[!BEGINSHADEBOX]

**Krav**

Licensfunktionen för Adobe Stock är bara tillgänglig om [Adobe Stock Integration][adobe-stock-integration] är installerad och konfigurerad. Licensiering av [Adobe Stock][adobe-stock]-bilder kräver en betald Adobe Stock-plan och ett [Adobe-konto][adobe-signin].

>[!ENDSHADEBOX]

## Licensiera en bild från nya [!DNL Media Gallery]

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**på sidofältet_ Admin _.

1. Följ stegen i [Använda Adobe Stock-bilder][using-adobe-stock] för att logga in och spara förhandsvisningsbilder i [medielagringen][media-storage].

   ![Sparad förhandsvisningsbild](./assets/adobe-stock-gallery-unlicensed.png){width="600" zoomable="yes"}

1. Klicka på de tre punkterna under bilden (![Ikonen Resurs-menyn](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}) och klicka sedan på **[!UICONTROL License]**.

   ![Adobe Stock bildåtgärder](./assets/adobe-stock-gallery-image-actions.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Om du inte är inloggad visas inloggningsformuläret. Mer information om inloggning finns i [Använda Adobe Stock-bilder][using-adobe-stock].

1. I bekräftelsedialogrutan för licensiering klickar du på **[!UICONTROL Confirm]** för att licensiera bilden.

   ![Licensbekräftelse](./assets/adobe-stock-gallery-license-confirm.png){width="350" zoomable="yes"}

   >[!NOTE]
   >
   >Du måste ha [Adobe Stock-krediter][stock-credits] tillgängliga på ditt konto för att licensiera bilden.

## Licensiera en bild från standardmedielagringen

1. [Öppna Adobe Stock Search-rutnätet][access-search].

1. Om du vill [visa bildinformationen][view-details] klickar du på en bild i sökstödrastret.

1. Beroende på den aktuella licensstatusen för bilden gör du något av följande:

   - Om bilden redan är licensierad klickar du på **[!UICONTROL Save]**.

   - Om bilden är _inte_ licensierad klickar du på **[!UICONTROL License and Save]**.

     >[!NOTE]
     >
     >Du måste ha [Adobe Stock-krediter][stock-credits] tillgängliga på ditt konto för att licensiera bilden.

   Den här åtgärden visar en uppmaning om att ange ett filnamn som används för att spara bilden i [medielagringen][media-storage]. Ett standardfilnamn anges, men du kan anpassa namnet efter dina inställningar.

   ![Spara licensierad Adobe Stock-bild](./assets/adobe-stock-save-licensed.png){width="550" zoomable="yes"}

1. Klicka på **[!UICONTROL Confirm]**.

   Sidan dirigeras om till medielagringen och den sparade förhandsvisningen visas.

[adobe-stock-integration]: adobe-stock.md
[media-storage]: media-storage.md
[using-adobe-stock]: adobe-stock-manage.md
[save-preview]: adobe-stock-save-preview.md
[access-search]: adobe-stock-manage.md#access-the-adobe-stock-search-grid
[view-details]: adobe-stock-manage.md#view-image-details
[stock-credits]: https://helpx.adobe.com/stock/help/credit-packs.html
[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
