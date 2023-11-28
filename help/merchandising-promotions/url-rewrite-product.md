---
title: Återskrivningar av produkt-URL
description: Lär dig hur du använder produkt-URL-omskrivningar för att omdirigera länkar till en annan produkts URL i din Commerce Store.
exl-id: 42b28ff7-e148-44f2-b6b4-63a38458e752
feature: Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '877'
ht-degree: 0%

---

# Återskrivningar av produkt-URL

Innan du börjar måste du se till att du förstår exakt vad omdirigeringen ska åstadkomma. Tänk i termer av _target_ / _ursprunglig begäran_ eller _omdirigera till_ / _omdirigera från_. Även om användare fortfarande kan navigera till den förra sidan från sökmotorer eller inaktuella länkar, leder omdirigeringen till att din butik växlar till det nya målet.

If [automatiska omdirigeringar](url-redirect-product-automatic.md) är aktiverade för din butik, du behöver inte skapa en omskrivning när en produkt [URL-nyckel](../catalog/catalog-urls.md) ändras.

{{url-rewrite-skip}}

## Steg 1. Planera omskrivningen

För att undvika misstag skriver du ned _omdirigera till_ bana och _omdirigera från_ sökväg och ange URL-nyckel och suffix (om tillämpligt).

Om du är osäker öppnar du varje produktsida i din butik och kopierar sökvägen från webbläsarens adressfält. När du skapar en produktomdirigering kan du antingen inkludera eller exkludera [kategorisökväg](../catalog/catalog-urls.md). I det här exemplet skapar vi en produktomdirigering utan en kategorisökväg.

### Produkt med kategorisökväg

Omdirigera till: `gear/bags/impulse-duffle.html`

Omdirigera från: `gear/bags/overnight-duffle.html`

### Produkt utan kategorisökväg

Omdirigera till: `impulse-duffle.html`

Omdirigera från: `overnight-duffle.html`

## Steg 2. Skapa omskrivning

{{url-rewrite-params}}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Innan du fortsätter gör du följande för att kontrollera att sökvägen till begäran är tillgänglig.

   - I sökfiltret högst upp i **[!UICONTROL Request Path]** anger du URL-nyckeln för sidan som ska omdirigeras och klickar på **[!UICONTROL Search]**.

   - Om det finns flera omdirigeringsposter för sidan, söker du efter den som matchar rätt butiksvy och öppnar den i redigeringsläge.

   - Klicka på i det övre högra hörnet **[!UICONTROL Delete]**. Klicka på **[!UICONTROL OK]** för att bekräfta.

1. Klicka på i det övre högra hörnet på sidan URL-omskrivning **Lägg till URL-omskrivning**.

1. Ange **[!UICONTROL Create URL Rewrite]** till `For product`.

1. Leta reda på produkten som är målet (målet) för omdirigeringen i rutnätet och klicka på raden.

   ![URL-omskrivningar - produkt](./assets/url-rewrite-product.png){width="700" zoomable="yes"}

1. Klicka under kategoriträdet **[!UICONTROL Skip Category Selection]**.

   I det här exemplet innehåller omdirigeringen ingen kategori.

   ![Skriv om produkt-URL - hoppa över kategorival](./assets/url-rewrite-skip-category-selection.png){width="600" zoomable="yes"}

   På sidan Lägg till URL-omskrivning för en produkt visas en länk till målet i det övre vänstra hörnet och i fältet Målsökväg visas systemversionen av sökvägen, som inte kan ändras. Till att börja med visas målsökvägen även i fältet Omdirigeringssökväg.

   - Om du har flera butiksvyer anger du **[!UICONTROL Store]** till den vy där omskrivningen gäller. I annat fall skapas en omskrivning för varje vy.

   - För **[!UICONTROL Request Path]** ersätter du standardinställningen genom att ange URL-nyckeln och suffixet (om tillämpligt) för den ursprungliga produktbegäran. Det här är _omdirigera från_ produkt som du identifierade i planeringssteget.

     >[!NOTE]
     >
     >Sökvägen till begäran måste vara unik för det angivna arkivet. Om det redan finns en omdirigering som använder samma sökväg visas ett fel när du försöker spara omdirigeringen. Den tidigare omdirigeringen måste tas bort innan du kan skapa en.

   - Ange **[!UICONTROL Redirect Type]** till något av följande:

      - `Temporary (302)`
      - `Permanent (301)`

   - Ange en kort beskrivning **[!UICONTROL Description]** för omskrivningen.

   ![Återskrivning av produkt-URL - information](./assets/url-rewrite-product-permanent-301.png){width="600" zoomable="yes"}

1. Läs följande innan du sparar omdirigeringen:

   - Länken i det övre vänstra hörnet visar namnet på målprodukten.
   - Sökvägen till begäran innehåller sökvägen till originalet _omdirigera från_ produkt.

1. När du är klar klickar du på **[!UICONTROL Save]**.

   Den nya produktomskrivningen visas nu högst upp i rutnätet för URL-omskrivning.

## Steg 3. Testa resultatet

1. Gå till butikens hemsida.

1. Gör något av följande:

   - Navigera till originalet _omdirigera från_ produktförfrågningssida.
   - Ange sökvägen till originalet i webbläsarens adressfält _omdirigera från_ produkten omedelbart efter butikens URL och tryck på **Retur**.

   Den nya målprodukten visas i stället för den ursprungliga produktförfrågan.

## Fältbeskrivningar

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Anger typ av omskrivning. Det går inte att ändra typen efter att omskrivningen har skapats. Alternativ: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | Produkten som ska omdirigeras. Beroende på din konfiguration kan sökvägen till begäran innehålla `.html` eller `.htm` suffix och kategori. Sökvägen till begäran måste vara unik och kan inte användas av en annan omdirigering. Om du får ett felmeddelande om att sökvägen till begäran finns tar du bort den befintliga omdirigeringen och försöker igen. |
| [!UICONTROL Target Path] | Den interna sökväg som används av systemet för att peka mot omdirigeringens mål. Målbanan är nedtonad och kan inte redigeras. |
| [!UICONTROL Redirect] | Anger typen av omdirigering. Alternativ: <br/>**[!UICONTROL No]**- Ingen omdirigering har angetts. Många åtgärder skapar omdirigeringsbegäranden av den här typen. Varje gång du t.ex. lägger till produkter i en kategori omdirigeras `No` typen skapas för varje butiksvy.<br/>**[!UICONTROL Temporary (302)]** - Anger för sökmotorer att omskrivningen pågår under en begränsad tid. Sökmotorer behåller vanligtvis inte sidrankningsinformation för temporära omskrivningar. <br/>**[!UICONTROL Permanent (301)]**- Anger för sökmotorer att omskrivningen är permanent. Sökmotorer behåller vanligtvis sidrankningsinformation för permanent omskrivning. |
| [!UICONTROL Description] | Beskriver syftet med omskrivningen för intern referens. |

{style="table-layout:auto"}

## Flera URL-omskrivningar

Du kan snabbt uppdatera URL-omskrivningar för flera eller alla produkter samtidigt genom att följa de här stegen.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Markera alla produkter som du vill uppdatera URL-omskrivningar för.

1. Under _[!UICONTROL Actions]_, välja **[!UICONTROL Update attributes]**för att uppdatera flera eller alla återskrivningar.

1. Under _[!UICONTROL PRODUCTS INFORMATION]_klickar du på&#x200B;**[!UICONTROL Websites]**-fliken.

1. I _[!UICONTROL Add Product To Websites]_markerar du alla webbplatser som du vill återställa URL-skrivningar för.

1. När du är klar att uppdatera klickar du på **[!UICONTROL Save]**.

>[!NOTE]
>
>Alla valda produkter läses till de valda webbplatserna och URL-omskrivningar genereras om.

![Uppdatera attribut - uppdatera flera URL-omskrivningar](./assets/url-rewrites-update.png){width="600" zoomable="yes"}
