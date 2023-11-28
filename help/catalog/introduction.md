---
title: Introduktion till kataloghantering
description: Lär dig hur katalog och produktomfång fungerar inom kataloghantering.
exl-id: 3c58fc1c-d7a3-4f51-8a78-6bf2fd0dbeee
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# Introduktion till kataloghantering

Adobe Commerce och Magento Open Source använder termen _katalog_ för att hänvisa till produktdatabasen som helhet.

Ett av de viktigaste områdena när det gäller att skapa och hantera din butik är att skapa produkter och kategorier. Admin innehåller flera verktyg som du använder för den första konfigurationen av din butik, för att underhålla din butik och optimera din verksamhet.

>[!TIP]
>
>Inventory management för Adobe Commerce och Magento Open Source ger er de verktyg ni behöver för att hantera ert produktlager. Handlare med en enda butik till flera lager, butiker, upphämtningsplatser, avsändare med mera kan använda dessa funktioner för att behålla kvantiteter för försäljning och hantera leveranser för att slutföra beställningar. Mer information om de här funktionerna och hur du kan använda dem för att hantera Stock på flera platser finns i [Inventory management Användarhandbok](../inventory-management/introduction.md).

## Katalogomfång

Åtkomsten till katalogdata bestäms av flera faktorer, bland annat [omfång](../getting-started/websites-stores-views.md#scope-settings) inställning, katalogkonfiguration och [rotkategori](category-root.md) som har tilldelats arkivet. Katalogen innehåller produkter som är aktiverade och tillgängliga för försäljning samt produkter som inte är till salu.

I försäljning, termen _katalog_ avser vanligtvis ett urval av produkter som är tillgängliga för försäljning. En butik kan till exempel ha en &quot;vårkatalog&quot; och en &quot;hög katalog&quot;.

Precis som innehållsförteckningen i en tryckt katalog, är butikens huvudmeny - eller _navigering överst_ - organiserar produkter efter kategori så att kunderna enkelt kan hitta det de vill ha. Huvudmenyn är baserad på en _rotkategori_, som är en behållare för den meny som tilldelas arkivet. Eftersom de specifika menyalternativen definieras på visningsnivå kan varje vy ha en egen huvudmeny som baseras på samma rotkategori. På varje meny kan du erbjuda ett välstrukturerat urval produkter som passar butiken.

![Kataloghierarkidiagram](./assets/catalog-hierarchy-scope.svg){width="550"}

## Produktomfång

För installationer med flera webbplatser, butiker och vyer finns [omfång](../getting-started/websites-stores-views.md#scope-settings) -inställningen avgör var produkter finns tillgängliga för försäljning och vilken produktinformation som är tillgänglig för varje butiksvy. Till att börja med publiceras alla produkter du skapar på standardwebbplatsen, butiken och butiksvyn.

![lagringsdiagram för flera platser](./assets/scope-multisite.svg){width="550"}

Om du bara har en butik med standardvyn kan du köra din butik i [single store mode](../getting-started/websites-stores-views.md#single-store-mode) om du vill dölja scopeinställningarna. Om din butik har flera vyer visas en omfångsindikator under namnet på varje fält.

- Använd _Butiksvy_ i det övre vänstra hörnet för att välja vyn. Ytterligare kontroller blir tillgängliga för alla fält som kan redigeras i butiksvyn.

- Om du vill definiera omfattningen för en produkt i en installation på flera platser går du till [Produkt på webbplatser](settings-basic-websites.md) produktinformation.

Att redigera en produkt för en butiksvy är som att lägga till ett lager med produktinformation som är specifik för vyn.

Du kan bara redigera eller tilldela produkter för den plats du har behörighet för, inte för alla platser där produkten har tilldelats.

Även om _Spanska_ butiksvyn är markerad i följande exempel. Produktinformationen visas fortfarande på det ursprungliga språket i standardbutiksvyn. Om du vill översätta produktinformationen måste du växla till _Spanska_ lagra vy och översätta textfälten, t.ex. produkttitel, beskrivning och metadata. Mer information finns i [Lokalisera produkter](../stores-purchase/store-localize.md#localize-products).

## Redigera en produkt för en annan vy

>[!NOTE]
>
>The _Alla butiksvyer_ omfånget är inaktiverat för Admin-användare som är begränsade till ett visst omfång när produkten också publiceras utanför det tillåtna omfånget. Det första omfånget som är tillgängligt för redigering är markerat som standard eftersom begränsade användare inte kan utföra _global_ åtgärder som påverkar omfattningar där de inte har tillgång till dem.

1. I det övre vänstra hörnet anger du **[!UICONTROL Store View]** till den specifika vy som ska redigeras.

1. Bekräfta ändringen av omfattningen genom att klicka på **[!UICONTROL OK]**.

1. Uppdatera fältet med det nya värdet för butiksvyn.

   En kryssruta visas under alla fält som kan redigeras för butiksvyn. Om du vill åsidosätta standardvärdet avmarkerar du **Använd standardvärde** kryssrutan.

   ![Översätter produktnamn för den spanska butiksvyn](./assets/product-translate-field-french.png){width="600" zoomable="yes"}

1. När du är klar klickar du på **[!UICONTROL Save]**.

1. I det övre vänstra hörnet anger du **[!UICONTROL Store View]** Välj tillbaka till standardinställningen.

1. Så här verifierar du ändringen i din butik:

   - Klicka i det övre högra hörnet på _Administratör_ menypil och välj **[!UICONTROL Customer View]**.

     ![Kundvy](./assets/product-admin-menu-customer-view.png){width="600" zoomable="yes"}

   - I butikens övre högra hörn anger du **[!UICONTROL Language Chooser]** till butiksvyn för den produkt du redigerade och hitta den produkt du redigerade för vyn.

     ![Språkväljaren](./assets/storefront-language-chooser.png){width="700" zoomable="yes"}
