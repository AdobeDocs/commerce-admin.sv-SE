---
title: Spårspår
description: Lär dig mer om de olika mönstren för vägbeskrivningar och hur du konfigurerar dem så att de visas på innehålls- och katalogsidor.
exl-id: 2f60d48e-960f-437c-8f8f-a3d06cc0840a
feature: Catalog Management, Categories, Site Navigation, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Spårspår

En _flödeslänk_ är en uppsättning länkar som visar kunden var de befinner sig i relation till andra sidor i butiken. De kan klicka på en länk i det synliga spåret för att gå tillbaka till föregående sida.

Det synliga spåret kan konfigureras så att det visas på innehållssidor och på katalogsidor. Formatet och positionen för det synliga spåret varierar beroende på temat, men är vanligtvis placerad precis nedanför rubriken. Som standard visas den synliga sökvägen på CMS-sidor.

![Breadcrumb-spår visas i storefront](./assets/storefront-breadcrumb-trail.png){width="700" zoomable="yes"}

## Allmänna typer av brödsmulor

Brödkrummar kan delas in i tre huvudtyper, som skiljer sig åt när det gäller syfte. Nedan beskrivs grunderna och huvudprinciperna för genomförandet av varje typ av brödsmulor.

### Hierarkibaserade vägbeskrivningar

Den här typen av vägbeskrivningar baseras på den kategorihierarki som är inställd på platsen. De angivna kedjorna talar om för användaren var i strukturen de är. I det här fallet är varje textlänk avsedd för en sida som är en nivå högre än den föregående.

Exempel: `Men > Tops > Hoodies & Sweatshirts`

Fördelen med den här typen är att användarna enkelt kan se vilken kategorinivå de befinner sig i och enkelt få tillgång till navigering mellan katalogsidor.

### Historikbaserade vägbeskrivningar

Historikbaserad (eller sökväg) navigering liknar bakåtknappen i en webbläsare. Den här typen av navigering gör att användarna snabbt kan gå tillbaka till de tidigare sidorna de besökt utan att göra några ändringar.

Fördelen med den här typen är att den är mest användbar när kunderna vill gå tillbaka till en tidigare sida efter att ha valt flera filter på en kategorisida.

Exempel: `Home > What's New > Gear > Bags`

### Attributbaserade vägbeskrivningar

Den här typen av vägbeskrivningar visar de attribut som är markerade på kategorisidan. Den största skillnaden jämfört med de andra typerna är att de attributbaserade vägbeskrivningarna representerar de filter och alternativ som kunden har valt i navigeringslagret för vissa produkter (till exempel pris, kvalitet och färg).

Exempel: `Home > Suits > All Suits > Refined by > Slim Fit`

## Lägg till/ta bort vägbeskrivningar från CMS-sidor

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Välj **[!UICONTROL Web]** i den vänstra panelen under _[!UICONTROL General]_.

   ![Visa vägbeskrivningar för CMS-sidor](../configuration-reference/general/assets/web-default-pages.png){width="600" zoomable="yes"}

1. Expandera avsnittet _[!UICONTROL Default Pages]_.

1. Avmarkera kryssrutan **[!UICONTROL Use system value]**.

1. Ange **[!UICONTROL Show Breadcrumbs for CMS Pages]** till `No` eller `Yes`.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

>[!NOTE]
>
>Överordnad kategori visas inte på spårningsraden på den underordnade kategorisidan när den har `Browsing Category`= `Deny` [kategoribehörighetsinställningar](category-permissions.md).
