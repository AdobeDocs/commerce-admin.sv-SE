---
title: Återskrivningar av kategori-URL
description: Lär dig hur du använder omskrivningar av kategori-URL:er för att omdirigera länkar till URL:en för en annan kategori i din Commerce Store.
exl-id: fc18f472-4aa8-4203-ade9-7ca576689d61
feature: Categories, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# Återskrivningar av kategori-URL

Om en kategori tas bort från katalogen kan du använda en kategoriomskrivning för att omdirigera länkar till URL:en för en annan kategori i din butik. Tänk i termer av _target_ / _ursprunglig begäran_  eller _omdirigera till_ / _omdirigera från_. Även om användare fortfarande kan navigera till den förra sidan från sökmotorer eller inaktuella länkar, leder omdirigeringen till att din butik växlar till det nya målet.

If [automatiska omdirigeringar](url-redirect-product-automatic.md) är aktiverade för din butik, du behöver inte skapa en omskrivning när en kategori [URL-nyckel](../catalog/catalog-urls.md) ändras.

{{url-rewrite-skip}}

## Steg 1. Planera omskrivningen

För att undvika misstag skriver du ned _omdirigera till_ bana och _omdirigera från_ sökväg och ange URL-nyckel och suffix (om tillämpligt).

Om du är osäker öppnar du varje kategorisida i butiken och kopierar sökvägen från webbläsarens adressfält.

**Exempel:**

Omdirigera till: `gear/backpacks-and-bags.html`

Omdirigera från: `gear/bags.html`

## Steg 2. Skapa omskrivning

{{url-rewrite-params}}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Innan du fortsätter gör du följande för att verifiera att sökvägen till begäran är tillgänglig:

   - I sökfiltret högst upp i **[!UICONTROL Request Path]** anger du URL-nyckeln för den kategori som ska omdirigeras och klickar på **[!UICONTROL Search]**.

   - Om det finns flera omdirigeringsposter för sidan, söker du efter den som matchar rätt butiksvy och öppnar omdirigeringsposten i redigeringsläge.

   - Klicka på i det övre högra hörnet **[!UICONTROL Delete]**. Klicka på **[!UICONTROL OK]** för att bekräfta.

1. När du återgår till _[!UICONTROL URL Rewrites]_sida, klicka **[!UICONTROL Add URL Rewrite]**.

1. Ange **[!UICONTROL Create URL Rewrite]** till `For category` och välj målkategorin i trädet som är målet för omdirigeringen.

   ![Skriv om URL - välj kategori](./assets/url-rewrite-category-choose.png){width="700" zoomable="yes"}

1. I _URL-omskrivning_ gör du följande:

   - Om du har flera butiker väljer du **[!UICONTROL Store]** där omskrivningen gäller.

   - För **[!UICONTROL Request Path]** anger du URL-nyckeln för den kategori som kunden begär. Det här är _omdirigera från_ kategori.

     >[!NOTE]
     >
     >Sökvägen till begäran måste vara unik för det angivna arkivet. Om det redan finns en omdirigering som använder samma sökväg visas ett fel när du försöker spara omdirigeringen. Den tidigare omdirigeringen måste tas bort innan du kan skapa en.

   - Ange **[!UICONTROL Redirect]** till något av följande:

      - `Temporary (302)`
      - `Permanent (301)`

   - Ange en kort beskrivning av omskrivningen som referens.

   ![Lägg till URL-omskrivning för kategori](./assets/url-rewrite-for-category.png){width="700" zoomable="yes"}

1. Läs följande innan du sparar omdirigeringen:

   - Länken i det övre vänstra hörnet visar namnet på målkategorin.
   - Sökvägen till begäran innehåller sökvägen till originalet _omdirigera från_ kategori.

1. När du är klar klickar du på **[!UICONTROL Save]** -knappen.

   Den nya kategoriomskrivningen visas högst upp i rutnätet för URL-omskrivning.

## Steg 3. Testa resultatet

1. Gå till butikens hemsida.

1. Gör något av följande:

   - Navigera till originalet _omdirigera från_ kategori.
   - Ange sökvägen till originalet i webbläsarens adressfält _omdirigera från_ -kategorin omedelbart efter butikens URL och tryck på **[!UICONTROL Enter]**.

   Den nya målkategorin visas i stället för den ursprungliga kategoriförfrågan.

## Fältbeskrivningar

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Anger typ av omskrivning. Det går inte att ändra typen efter att omskrivningen har skapats. Alternativ: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | Kategorin som ska omdirigeras. Beroende på din konfiguration kan sökvägen till begäran innehålla suffixet .html eller .htm samt den överordnade kategorin. Sökvägen till begäran måste vara unik och kan inte användas av en annan omdirigering. Om du får ett felmeddelande om att sökvägen till begäran finns tar du bort den befintliga omdirigeringen och försöker igen. |
| [!UICONTROL Target Path] | Den interna sökväg som används av systemet för att peka mot omdirigeringens mål. Målbanan är nedtonad och kan inte redigeras. |
| [!UICONTROL Redirect] | Anger typen av omdirigering. Alternativ: <br/>**[!UICONTROL No]**- Ingen omdirigering har angetts. Många åtgärder skapar omdirigeringsbegäranden av den här typen. Varje gång du t.ex. lägger till produkter i en kategori omdirigeras `No` typen skapas för varje butiksvy.<br/>**[!UICONTROL Temporary (302)]** - Anger för sökmotorer att omskrivningen pågår under en begränsad tid. Sökmotorer behåller vanligtvis inte sidrankningsinformation för temporära omskrivningar. <br/>**[!UICONTROL Permanent (301)]**- Anger för sökmotorer att omskrivningen är permanent. Sökmotorer behåller vanligtvis sidrankningsinformation för permanent omskrivning. |
| [!UICONTROL Description] | Beskriver syftet med omskrivningen för intern referens. |

{style="table-layout:auto"}
