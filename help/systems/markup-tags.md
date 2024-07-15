---
title: Markeringstaggar
description: Lär dig mer om taggar som innehåller kodfragment som refererar till ett objekt i din butik.
exl-id: 0d6f5a9b-983d-473e-b641-0dceba40974f
feature: Page Content, Communications, Variables
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# Markeringstaggar

En märkordstagg är ett direktiv som innehåller kodfragment med en relativ referens till ett objekt i din butik, t.ex. en variabel, URL, bild eller block. Markeringstaggar kan användas var som helst där redigeraren är tillgänglig och ingår i HTML i mallarna [email](email-templates.md) och [newsletter](../merchandising-promotions/newsletter-template.md) samt andra typer av [innehåll](../content-design/introduction.md#content).

Markeringstaggar omges av dubbla klammerparenteser och kan antingen genereras med widgetverktyget eller skrivas direkt i HTML. I stället för att hårdkoda hela sökvägen till en sida kan du använda en tagg som representerar butikens URL. De märkordstaggar som beskrivs i följande exempel är:

{{$include /help/_includes/directives-caution.md}}

## Anpassad variabel

Du kan använda taggen Variable-kod för att infoga en [anpassad variabel](variables-custom.md) i en e-postmall, block, nyhetsbrev och innehållssidor.

\{\{CustomVar code= &quot;my_custom_variable&quot;}}

## Lagra URL

Markeringstaggen Butiks-URL representerar webbplatsens bas-URL och används som ersättning för den första delen av en fullständig URL, inklusive domännamnet. Det finns två versioner av den här märkordstaggen: en som kommer direkt till din butik och den andra med ett snedstreck (`/`) i slutet som används när en sökväg läggs till.

\{\{store url=&#39;kläder/skor/kvinnor&#39;}}

## Media-URL

URL-taggen för dynamiska medier representerar platsen och filnamnet för en bild som lagras i ett CDN-nätverk. Taggen kan användas för att placera en bild på en sida, ett block, en banner eller en e-postmall.

\{\{media url=&#39;shoe-sales.jpg&#39;}}

## Blockera ID

Kodtaggen för block-ID är en av de enklaste att använda och kan användas för att placera ett block direkt på en CMS-sida, eller till och med kapslas i ett annat block. Du kan använda den här tekniken för att ändra ett block för olika erbjudanden eller språk. Kodtaggen Block ID refererar till ett block med hjälp av dess identifierare.

\{\{block id=&#39;block-id&#39;}}

## Malltagg

En malltagg refererar till en PHTML-mallfil och kan användas för att visa blocket på en CMS-sida eller ett statiskt block. Koden i följande exempel kan läggas till på en sida eller i ett block för att visa formuläret Kontakta oss.

\{\{block class=&quot;Magento\Contact\Block\ContactForm&quot; name=&quot;contactForm&quot; template=&quot;Magento_Contact::form.phtml&quot;}}

Koden i nästa exempel kan läggas till på en sida eller i ett block för att visa en lista med produkter i en viss kategori, per kategori-ID.

\{\{block type=&quot;catalog/product_list&quot; category_id=&quot;22&quot; template=&quot;catalog/product/list.phtml&quot;}}

## Widget-kod

Widgetverktyget kan användas för att visa produktlistor eller för att infoga komplexa länkar, till exempel en som går till en viss produktsida, baserat på produkt-ID. Koden som genereras omfattar blockreferensen, platsen för kodmodulen och motsvarande PHTML-mall. När koden har skapats kan du kopiera och klistra in den från ett ställe till ett annat.

Koden i följande exempel kan läggas till på en sida eller i ett block för att visa listan över nya produkter.

\{\{widget type=&quot;catalog/product_widget_new&quot; display_type=&quot;new_products&quot; products_count=&quot;10&quot; template=&quot;catalog/product/widget/new/content/new_grid.phtml&quot;}}

Koden i nästa exempel kan läggas till på en sida eller i ett block för att visa en länk till en viss produkt per produkt-ID.

\{\{widget type=&quot;catalog/product_widget_link&quot; anchor_text=&quot;My Product Link&quot; title=&quot;My Product Link&quot; template=&quot;catalog/product/widgetlink/link_block.phtml&quot; id_path=&quot;product/31&quot;}}

## Använda taggar i länkar

Du kan använda märkordstaggar med ankarpunktstaggar i HTML och länka direkt till en sida i din butik. Länken kan läggas in i innehållssidor, block eller mallar för e-post och nyhetsbrev. Du kan också använda den här tekniken för att länka en bild till en viss sida.

### Steg 1. Identifiera mål-URL

Navigera om möjligt till sidan som du vill länka till och kopiera den fullständiga URL:en från webbläsarens adressfält. Den del av URL:en som du behöver kommer efter `.com/`. Annars kopierar du URL-nyckeln från CMS-sidan som du vill använda som länkmål.

#### Hel URL till kategorisida

`https://mystore.com/apparel/shoes/womens`
`https://mystore.com/apparel/shoes/womens.html`

#### Fullständig URL till produktsida

`https://mystore.com/apparel/shoes/womens/nine-west-pump`
`https://mystore.com/apparel/shoes/womens/nine-west-pump.html`

#### Fullständig URL till CMS-sida

`https://mystore.com/about-us`

### Steg 2. Lägg till markeringen i URL:en

URL-taggen för butik representerar bas-URL:en för din webbplats och används som ersättning för HTTP-adressdelen i butikens URL, inklusive domännamnet och `.com`. Det finns två versioner av taggen som du kan använda, beroende på vilket resultat du vill uppnå.

`store direct_url` - länkar direkt till en sida.

`store url` - Placerar ett snedstreck i slutet så att ytterligare referenser kan läggas till som en sökväg.

I följande exempel omges URL-tangenten med enkla citattecken och hela taggen omges med dubbla klammerparenteser. När märkordet används med en ankartagg placeras det inuti ankarpunktens dubbla citattecken. För att undvika missförstånd kan du växla med enkla och dubbla citattecken för varje kapslad uppsättning med citattecken.

Om du börjar med en fullständig URL-adress tar du bort HTTP-adressen (`http://` eller `https://`) från URL-adressen, till och med `.com/`. I stället för detta anger du taggen Store URL markup, upp till det inledande enkla citattecknet.

#### Lagra URL-märkordstagg

`https://mystore.com/apparel/shoes/womens`

`{{store url='apparel/shoes/womens'}}`

I annat fall anger du den första delen av taggen för butikens URL-kod och klistrar in URL-nyckeln eller sökvägen som du kopierade tidigare.

### Lagra URL-tagg med URL-nyckel

`{{store url=`

Slutför taggen genom att ange avslutande citattecken och dubbla klammerparenteser.

`{{store url='apparel/shoes/womens'}}`

### Steg 3. Slutför ankartaggen

Lägg in den färdiga taggen i en ankartagg med taggen markup i stället för mål-URL:en. Lägg sedan till länktexten och den avslutande ankartaggen.

#### Markering i ankarpunktstagg

\&lt;a href=&quot;\{\{markup tag goes here}}&quot;>Länktext\&lt;/a>

Klistra in den färdiga ankartaggen i koden för en CMS-sida, -block, -banderoll eller -e-postmall där du vill att länken ska visas.

### Fullständig länk med markering

\&lt;a href=&quot;\{\{store url=&#39;kläm/skor&#39;}}&quot;>Skådeförsäljning\&lt;/a>
