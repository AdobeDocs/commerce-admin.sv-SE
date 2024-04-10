---
title: Kundgrupper
description: Använd kundgrupper för att avgöra vilka rabatter som är tillgängliga för kunder som är tilldelade till en grupp och den skatteklass som är associerad med gruppen.
exl-id: 6b785c4a-a5dc-480c-8182-2a940784218d
feature: Customers, Configuration
source-git-commit: 805ceef0fe67c1ed2a4fbd06e6f02d9ad252ecef
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Kundgrupper

Kundgrupper avgör vilka rabatter som är tillgängliga och vilken skatteklass som är associerad med gruppen. Standardkundgrupperna är `General`, `Not Logged In`och `Wholesale`.

![Kundgrupper](assets/customer-groups.png){width="700" zoomable="yes"}

## Filtrera [!UICONTROL Customer Groups] list

1. På _Administratör_ sidebar, gå till **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Klicka på **[!UICONTROL Filters]**.

1. Ange sökvillkor för grupper, inklusive ett intervall med ID:n, grupper eller momsklass.

   ![Filtreringsalternativ](assets/groups-filters.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Apply Filters]**.

## Skapa en kundgrupp

>[!NOTE]
>
>Administratörsanvändare som inte har tillgång till alla webbplatser (tilldelas en roll med en Custom) [!UICONTROL Role Scope]) kan inte skapa, ändra eller ta bort kundgrupper.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Klicka på **[!UICONTROL Add New Customer Group]**.

1. För [!DNL **Group Name]** anger du ett unikt namn med högst 32 tecken för att identifiera gruppen.

1. Välj **[!UICONTROL Tax Class]** som gäller för gruppen.

   ![Gruppinformation](assets/group-information.png){width="600" zoomable="yes"}

1. Välj **[!UICONTROL Excluded Website(s)]** som du vill utesluta från gruppen.

   >[!IMPORTANT]
   >
   >Om du utesluter webbplatser kan du minska produktpriset och indexeringstiden för katalogregler, eftersom uteslutna webbplatser inte indexeras. När en kundgrupp sparas med ett tillagt undantag för en webbplats blir produktpriset, katalogregeln och katalogens sökindex ogiltiga. Om du har många produkter, webbplatser och kundgrupper rekommenderar vi att du gör en paus i indexeringsprocessen tills du har uteslutit webbplatser från kundgrupperna.

   Inga webbplatser utesluts som standard. Om du vill markera flera värden håller du ned _Ctrl_ tangent (PC) eller _Kommando_ (Mac) och klicka på varje alternativ.

1. När du är klar klickar du på **[!UICONTROL Save Customer Group]**.

## Redigera en kundgrupp

1. På _Administratör_ sidebar, gå till **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Öppna posten i redigeringsläge.

1. Gör de ändringar som behövs.

1. När du är klar klickar du på **[!UICONTROL Save Customer Group]**.

## Tilldela en kund till en annan grupp

1. På _Administratör_ sidebar, gå till **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Hitta kunden i listan och markera kryssrutan i den första kolumnen.

1. Ange **Åtgärder** styra till `Assign a Customer Group` och väljer gruppen på menyn.

   ![Tilldela en kundgrupp](assets/group-assign.png){width="600" zoomable="yes"}

1. När du uppmanas att bekräfta klickar du på **OK**.

## Associera en grupp kunder med specifika rabatter

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _Erbjudanden_ > **[!UICONTROL Cart Price Rules]**.

1. Välj den kundprisregel där du vill associera en grupp för rabatten, eller [skapa en prisregel](../merchandising-promotions/price-rules-catalog.md).

1. Välj de kundgrupper som regeln gäller för.

   ![Kundgrupp till specifika rabatter](assets/group-discount.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]**.

>[!NOTE]
>
> Du kan också använda avancerad prissättning för att tillämpa produktrabatter på kundgrupper. Se [Avancerade priser](../catalog/product-price-group.md).

## Ta bort en kundgrupp

1. På _Administratör_ sidebar, gå till **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**.

1. Öppna posten i redigeringsläge.

1. Klicka på i knappfältet **[!UICONTROL Delete Customer Group]**.

1. När du uppmanas att bekräfta klickar du på **OK**.

## Demo av kundgrupper

Läs om hur du skapar kundgrupper i den här demon:

>[!VIDEO](https://video.tv.adobe.com/v/343660/?quality=12)
