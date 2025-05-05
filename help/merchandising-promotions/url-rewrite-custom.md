---
title: Anpassade URL-omskrivningar
description: Lär dig hur du använder anpassade URL-omskrivningar för att hantera olika omdirigeringar i din Commerce Store.
exl-id: b15054be-e463-48e6-b6c1-0a8a2141cc01
feature: Search, Configuration
badgePaas: label="Endast PaaS" type="Informative" url="https://experienceleague.adobe.com/sv/docs/commerce/user-guides/product-solutions" tooltip="Gäller endast Adobe Commerce i molnprojekt (Adobe-hanterad PaaS-infrastruktur) och lokala projekt."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 0%

---

# Anpassade URL-omskrivningar

En anpassad omskrivning kan användas för att hantera olika omdirigeringar, som att omdirigera en sida från din butik till en extern webbplats. Du kan till exempel ha två Commerce-webbplatser, var och en med sin egen domän. Du kan använda en anpassad omdirigering för att dirigera om begäranden för en produkt, kategori eller sida till den andra webbplatsen. Till skillnad från andra omdirigeringstyper väljs inte målet för en anpassad omdirigering från en lista över befintliga sidor i din butik.

Innan du börjar ser du till att du förstår exakt vad omdirigeringen ska åstadkomma. Tänk i termer av _target_ / _source_ eller _omdirigera till_ / _omdirigera från_. Även om användare fortfarande kan navigera till den förra sidan från sökmotorer eller inaktuella länkar, leder omdirigeringen till att din butik växlar till det nya målet.

## Steg 1. Planera omskrivningen

Du undviker misstag genom att skriva ned URL:en för sidan _omdirigering till_ och URL-nyckeln för sidan _omdirigering från_.

Om du är osäker öppnar du varje sida och kopierar URL-adressen från webbläsarens adressfält.

**Exempel**

Omdirigera till:

    http://www.different-website.com/page.html

Omdirigera från:

    cms-page
    category.html
    category/subcategory.html
    product.html
    category/product.html

## Steg 2. Skapa omskrivning

{{url-rewrite-params}}

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**&#x200B;på sidofältet_ Admin _.

1. Innan du fortsätter gör du följande för att verifiera att sökvägen till begäran är tillgänglig:

   - I sökfiltret högst upp i kolumnen **[!UICONTROL Request Path]** anger du URL-nyckeln för sidan som ska omdirigeras och klickar på **[!UICONTROL Search]**.

   - Om det finns flera omdirigeringsposter för sidan, söker du efter den som matchar rätt butiksvy och öppnar den i redigeringsläge.

   - Klicka på **[!UICONTROL Delete]** i det övre högra hörnet. Klicka på **[!UICONTROL OK]** när du uppmanas att bekräfta.

1. När du kommer tillbaka till sidan URL-omskrivning klickar du på **[!UICONTROL Add URL Rewrite]**.

1. Ange **[!UICONTROL Create URL Rewrite]** till `Custom`.

   ![URL-omskrivningar - anpassad](./assets/url-rewrite-custom.png){width="600" zoomable="yes"}

1. Gör följande under URL-omskrivningsinformation:

   - Om du har flera butiksvyer väljer du **[!UICONTROL Store]** där omskrivningen gäller.

   - För **[!UICONTROL Request Path]** anger du URL-nyckeln och sökvägen (om tillämpligt) för den produkt, kategori eller CMS-sida som ska omdirigeras.

     >[!NOTE]
     >
     >Sökvägen till begäran måste vara unik för det angivna arkivet. Om det redan finns en omdirigering som använder samma sökväg visas ett fel när du försöker spara omdirigeringen. Den tidigare omdirigeringen måste tas bort innan du kan skapa en.

   - Ange målets URL för **[!UICONTROL Target Path]**. Om målet finns på en annan webbplats anger du den fullständiga URL:en.

   - Ange **Omdirigering** till något av följande:

      - `Temporary (302)`
      - `Permanent (301)`

   - Ange en kort beskrivning av omskrivningen som referens.

1. Läs följande innan du sparar omdirigeringen:

   - [!UICONTROL Request Path] innehåller URL-nyckeln eller sökvägen för den ursprungliga sidan _omdirigera från_.
   - [!UICONTROL Target Path] innehåller URL:en för sidan _omdirigering till_.

1. Klicka på **[!UICONTROL Save]** när du är klar.

   Den nya omskrivningen visas i rutnätet högst upp i listan.

## Steg 3. Testa resultatet

1. Gå till butikens hemsida.

1. Gör något av följande:

   - Navigera till den ursprungliga _omdirigeringen från_-sidan.
   - I webbläsarens adressfält anger du namnet på den ursprungliga _omdirigeringssidan_ omedelbart efter butikens URL och trycker på **Retur**.

   Den nya målsidan visas i stället för den ursprungliga sidförfrågan.

## Fältbeskrivningar

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Anger typ av omskrivning. Det går inte att ändra typen efter att omskrivningen har skapats. Alternativ: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | Den sida som ska omdirigeras. Sökvägen till begäran måste vara unik och kan inte användas av en annan omdirigering. Om du får ett felmeddelande om att sökvägen till begäran finns tar du bort den befintliga omdirigeringen och försöker igen. |
| [!UICONTROL Target Path] | Den interna sökväg som används av systemet för att peka mot målet. Målbanan är nedtonad och kan inte redigeras. |
| [!UICONTROL Redirect] | Anger typen av omdirigering. Alternativ: <br/>**Nej** - Ingen omdirigering har angetts. <br/>**[!UICONTROL Temporary (302)]**- Anger för sökmotorer att omskrivningen är för en begränsad tid. Sökmotorer behåller vanligtvis inte sidrankningsinformation för temporära omskrivningar.<br/>**[!UICONTROL Permanent (301)]** - Anger för sökmotorer att omskrivningen är permanent. Sökmotorer behåller vanligtvis sidrankningsinformation för permanent omskrivning. |
| [!UICONTROL Description] | Beskriver syftet med omskrivningen för intern referens. |

{style="table-layout:auto"}
