---
title: Skapa en relaterad produktregel
description: Lär dig hur du skapar en relaterad produktregel som kan aktiveras för att visa relaterade produkter, merförsäljning och korsförsäljning.
exl-id: fbc059ec-d3e6-46ca-810a-a979a0631dd8
feature: Merchandising, Products, Storefront
source-git-commit: 8f5a5fb6c277086e5f70221e4a6a5ae1b9e1abfe
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# Skapa en relaterad produktregel

{{ee-feature}}

Processen med att skapa en relaterad produktregel liknar att ställa in en prisregel. Först definierar du villkoren som ska matcha och sedan de produkter som du vill visa. Det kan när som helst finnas flera aktiva regler som kan aktiveras för att visa relaterade produkter, merförsäljning och korsförsäljning. Prioriteten för varje regel avgör i vilken ordning produktblocket visas på sidan.

>[!NOTE]
>
>För ett attribut som ska användas i en målregel är [_[!UICONTROL Use for Promo Rule Conditions]_](../catalog/product-attributes.md) egenskapen måste anges till `Yes`.

>[!NOTE]
>
>The `All Store Views` omfångsvärdet används alltid för båda [!UICONTROL Products to Match] och [!UICONTROL Products to Display] villkor för alla produktattribut. Detta gäller också när produktattributen har olika värden för olika butiksvyer och webbplatser.

## Skapa en relaterad produktregel

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

1. Klicka på i det övre högra hörnet **[!UICONTROL Add Rule]**.

   ![Regel för relaterade produkter - information](./assets/catalog-related-products-rule-information.png){width="600" zoomable="yes"}

1. Slutför **[!UICONTROL Rule Information]** enligt följande:

   - Ange en **[!UICONTROL Rule Name]** för att identifiera regeln när du arbetar i administratören.

   - För **[!UICONTROL Priority]** anger du ett tal som bestämmer i vilken ordning resultaten ska visas på sidan när resultaten från andra regler har samma plats som mål. Nummer `1` har högsta prioritet.

   - Aktivera regeln genom att ange **[!UICONTROL Status]** till `Active`.

   - Ange **[!UICONTROL Apply To]** till något av följande:

      - `Related Products`
      - `Up-sells`
      - `Cross-sells`

   - Om regeln ska vara aktiv under ett visst tidsintervall anger du **[!UICONTROL From]** och **[!UICONTROL To]** datum.

   - För **[!UICONTROL Result Limit]** anger du antalet poster som ska visas i resultatlistan. Det högsta antalet är 20.

   - Om regeln gäller för en viss [kundsegment](../customers/customer-segments.md), ange **[!UICONTROL Customer Segments]** till `Specified` och välj kundsegment i listan.

1. Välj **[!UICONTROL Products to Match]** och bygga upp villkoren på samma sätt som för en [katalogprisregel](price-rules-catalog.md).

   ![Relaterade produkter - produkter att matcha](./assets/catalog-related-products-match.png){width="500"}

1. Välj **[!UICONTROL Products to Display]** och skapa resultatvillkor på samma sätt som för en [katalogprisregel](price-rules-catalog.md).

   ![Relaterad produktregel - produkter som ska visas](./assets/catalog-related-products-to-display.png){width="500"}

   Slutför villkoret för att beskriva de produkter som du vill inkludera i de visade resultaten.

1. När du är klar klickar du på **[!UICONTROL Save]**.

## Ta bort en relaterad produktregel

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

1. Hitta den relaterade produktregel som du vill ta bort.

1. Klicka på regeln för att öppna informationssidan.

1. Klicka på i det övre högra hörnet **[!UICONTROL Delete]**.

1. Bekräfta åtgärden genom att klicka **[!UICONTROL OK]**.

## Demo av relaterade produktregler

I den här videon får du lära dig mer om hur du skapar relaterade produktregler:

>[!VIDEO](https://video.tv.adobe.com/v/343837?quality=12&learn=on)

## Fältbeskrivningar

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Rule Name] | Ett namn som identifierar regeln för internt bruk. |
| [!UICONTROL Priority] | Anger i vilken ordning resultatet av regeln visas när det visas med andra resultatuppsättningar som har samma plats på sidan. Värdet kan anges till vilket heltal som helst, med den högsta prioriteten 1. Om det till exempel finns flera regler för merförsäljning som gäller, visas den som har högst prioritet framför de andra. Sorteringsordningen för produkterna i varje resultatuppsättning är slumpmässig. Eventuell merförsäljning, korsförsäljning och relaterade produkter som konfigurerats manuellt visas alltid på sidan före eventuella regelbaserade produktkampanjer. |
| [!UICONTROL Status] | Kontrollerar regelns aktiva status. Alternativ: `Active` / `Inactive` |
| [!UICONTROL Apply To] | Identifierar den typ av produktrelation som är associerad med regeln. Alternativ: `Related Products` / `Up-sells` / `Cross-sells` |
| [!UICONTROL From Date] | Om regeln är aktiv under ett tidsintervall avgör den här inställningen det första datum då regeln är aktiv. |
| [!UICONTROL To Date] | Om regeln är aktiv under ett tidsintervall avgör den här inställningen vilket datum regeln är aktiv. |
| [!UICONTROL Result Limit] | Anger antalet produkter som visas i resultatet på en gång. Det högsta antalet är 20. Om fler matchande resultat hittas roterar produkterna genom blocket varje gång sidan uppdateras. |
| [!UICONTROL Customer Segments] | Identifierar de kundsegment som regeln gäller för. Alternativ: `All` / `Specified` |

{style="table-layout:auto"}
