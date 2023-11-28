---
title: Översikt över produktattribut
description: Lär dig mer om produktattribut och hur de används för att beskriva specifika egenskaper hos en produkt.
exl-id: e15770ee-fb71-43f0-8c26-e8029935799a
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Översikt över produktattribut

Attribut är byggstenarna i produktkatalogen och beskriver specifika egenskaper hos en produkt. Produktattribut kan ordnas i [attributuppsättningar](attribute-sets.md), som sedan används som mallar för att skapa produkter.

Attribut avgör vilken typ av indatakontroll som används för produktalternativ och ger ytterligare information för produktsidor. De används också som sökparametrar och sökvillkor för lagerstyrd navigering, produktjämförelserapporter och kampanjer. Du kan skapa så många attribut och attributuppsättningar som behövs för att beskriva produkterna i katalogen. Förutom de attribut du kan skapa är systemattribut, som pris, inbyggda i den centrala Commerce-plattformen och kan inte ändras.

![Skapa ett nytt attribut när du redigerar en produkt](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

Använd de bästa metoderna som beskrivs i följande avsnitt när du planerar och skapar produktattribut.

## Attributnamn

Upprätta konsekventa konventioner för attributnamngivning, inklusive bokstavsskiftningar och interpunktion. Till exempel: `Color:Green` och `Color:green` kan betraktas som två olika attributvärden i olika system. Sådana brus i data kan påverka affärsregler, sökresultat och datafilter för program som matchar produkter.

## Attributanvändning

Tänk på hur attribut ska användas när du tilldelar egenskaper och värden. Identifiera de attribut som används som etiketter för presentation, till exempel produktnamn, bild, pris och beskrivning, och vilka attribut som används för datainmatning. Tänk på hur attributen visas på olika sidor på webbplatsen och hur de visas på kategorisidor, produktinformationssidor, kategoristödraster och miniatyrskjutreglage.

## Färg

Ad-hoc-färgbeskrivningar kan utgöra en utmaning när det gäller databasåtgärder. Färgnamn som &quot;Azure Skies&quot; eller &quot;Robin Egg Blue&quot; är mycket tilltalande, men returnerar kanske inte det bästa resultatet när de används som sökvillkor, eller om du måste ange för att kunna sälja produkten `Color_Family:Blue`. Fundera över hur färger visas i sökresultat och lagerstyrd navigering, och ta fram riktlinjer för ditt företags behov. Var sedan konsekvent när du tilldelar färgattributvärden i hela katalogen.

## Varianthantering

Använd produkt [konfigurationsalternativ](product-configurations.md) och [konfigurerbara produkter](product-create-configurable.md) för att hantera olika varianter av produkterna. De här funktionerna gör det enklare att kategorisera produkter, att skapa kundvagnsregler och dynamiska kategoriregler samt att erbjuda ett urval av alternativ med olika typer av text, urval och datuminmatning.

## Viktad sökning

Produktattribut som är aktiverade för [katalogsökning](search.md) kan tilldelas en vikt som ger dem ett högre värde i sökresultaten. Attribut med större vikt returneras före attribut med lägre vikt. Ta till exempel två attribut i systemet, _färg_ med en sökvikt på 3 och _description_ med sökvikten 1. En sökning efter ordet _röd_ returnerar en lista med produkter med färgattributvärdet `red`, men returnerar inte produkter med beskrivningar som innehåller ordet _röd_. I det här exemplet `color` har en större definierad vikt än `description` -attribut.

## Oanvända egenskaper

Ta bort oanvända produktegenskaper för bättre strukturering och snabbare indexering.
