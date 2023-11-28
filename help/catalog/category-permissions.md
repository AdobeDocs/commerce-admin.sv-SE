---
title: Kategoribehörigheter
description: Lär dig hur du använder kategorier för att styra visningen av produktpriser, avgöra vilka kundgrupper som kan lägga till produkter i kundvagnen och specificera landningssidan.
exl-id: d80a0545-918e-4c08-9f37-4aa3cd7771f4
feature: Catalog Management, Categories, Customers, Configuration
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# Kategoribehörigheter

{{ee-feature}}

Kategoriåtkomsten kan begränsas till specifika kundgrupper eller helt och hållet begränsas. Du kan styra visningen av produktpriser, avgöra vilka kundgrupper som kan lägga till produkter i kundvagnen och specificera landningssidan.

>[!NOTE]
>
>Kategoribehörigheter har ett globalt omfång och när de är aktiverade begränsas åtkomsten till varje kategori enligt dess individuella behörigheter. Kategoribehörigheter är inte aktiverade som standard.

Om du till exempel bara säljer till kunder i grossistledet kan du låta vem som helst bläddra i katalogen, men visa priser och endast tillåta köp för kunder i _Grossist_ kundgrupp. I följande exempel har bara inloggade användare åtkomst till kategorin Samlingar. För gäster visas inte alternativet Samlingar på huvudmenyn.

![Inloggade användare ser kategorin Samlingar](./assets/storefront-category-permissions-logged-in.png){width="600" zoomable="yes"}

När den är aktiverad visas en ny _[!UICONTROL Category Permissions]_visas på kategorisidan där du kan använda den åtkomst som krävs för varje kategori. Du kan lägga till flera behörighetsregler i varje kategori för olika webbplatser och kundgrupper.

## Steg 1: Konfigurera kategoribehörigheter

>[!IMPORTANT]
>
>Alla befintliga [gruppbehörighetsinställningar](../configuration-reference/catalog/catalog.md#category-permissions) ignoreras av **_alla_** i katalogen när **_[!UICONTROL Shared Catalog]_** funktionen är aktiverad. [!UICONTROL Shared Catalog] har fullständig kontroll över alla kategoribehörigheter i katalogen när den är aktiverad.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Category Permissions]** -avsnitt.

   ![Kategoribehörigheter](../configuration-reference/catalog/assets/catalog-category-permissions.png){width="600" zoomable="yes"}

   En detaljerad lista över dessa alternativ finns på [Kategoribehörigheter](../configuration-reference/catalog/catalog.md#category-permissions) i _Konfigurationsreferens_.

1. Ange **[!UICONTROL Enable]** till `Yes`.

1. Fyll i de andra alternativen enligt vad du vill tillåta eller begränsa i din butik (se följande avsnitt).

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

1. När du uppmanas att uppdatera cachen klickar du på **[!UICONTROL Cache Management]** i systemmeddelandet och följ instruktionerna för att uppdatera cachen.

### [!UICONTROL Allow Browsing Category]

Det här alternativet gäller för alla kategorier i [webbplats](../getting-started/websites-stores-views.md).

Tillåta medlemmar i en **_specifik kundgrupp_** Gör så här om du vill bläddra bland kategoriprodukter:

1. Ange **[!UICONTROL Allow Browsing Category]** till `Specified Customer Groups`.

1. I **[!UICONTROL Customer Groups]** markerar du varje grupp som får bläddra bland produkterna i kategorin.

   Om du vill markera flera grupper håller du ned Ctrl-tangenten (PC) eller Kommando-tangenten (Mac) när du klickar på varje grupp.

   ![Tillåt surfning efter kundgrupp i grossistledet](./assets/category-permissions-allow-browsing-customer-groups.png){width="600" zoomable="yes"}

Till **_begränsa åtkomst och omdirigering till en landningssida_** gör du följande:

1. Ange **[!UICONTROL Allow Browsing Category]** till `No, Redirect to Landing Page`.

1. Välj **[!UICONTROL Landing Page]** där besökarna omdirigeras.

   ![Omdirigera till startsidan](./assets/category-permissions-browse-category-landing-page.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Även om _[!UICONTROL Allow Browsing Category]_inställningen gäller för alla kategorier på webbplatsen, du kan konfigurera olika landningssidor för varje butiksvy.

### [!UICONTROL Display Product Prices]

Det här alternativet gäller för alla kategorier i [webbplats](../getting-started/websites-stores-views.md).

Tillåt endast medlemmar i **_specifika kundgrupper_** Så här ser du priset på produkterna i kategorin:

1. Ange **[!UICONTROL Display Product Prices]** till `Yes, for Specified Customer Groups`.

1. I **[!UICONTROL Customer Groups]** markerar du varje grupp som får se priset på produkterna i kategorin.

   Om du vill markera flera grupper håller du ned Ctrl-tangenten (PC) eller Kommando-tangenten (Mac) när du klickar på varje grupp.)

   ![Endast grossister kan se priser](./assets/category-permissions-price-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Allow Adding to Cart]

Det här alternativet gäller för alla kategorier i [webbplats](../getting-started/websites-stores-views.md).

Tillåt endast medlemmar i **_specifika kundgrupper_** Så här placerar du kategoriprodukter i kundvagnen:

1. Ange **[!UICONTROL Allow Adding to Cart]** till `Yes, for Specified Customer Groups`.

1. I **[!UICONTROL Customer Groups]** markerar du varje grupp som har rätt att lägga till produkter från kategorin i kundvagnen.

   Om du vill markera flera grupper håller du ned Ctrl-tangenten (PC) eller Kommando-tangenten (Mac) när du klickar på varje grupp.

   ![Endast grossister kan placera produkten i varukorgen](./assets/category-permissions-cart-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Disallow Catalog Search]

Ange det här alternativet om du inte vill att medlemmar i en viss kundgrupp ska kunna använda katalogsökning. Den gäller för alla kategorier i [webbplats](../getting-started/websites-stores-views.md).

- Tillåt **_endast inloggade kunder_** om du vill använda katalogsökning väljer du `NOT LOGGED IN`.

- Tillåt **_endast specifika kundgrupper_** Om du vill använda katalogsökning markerar du varje grupp som ska uteslutas från användning av kategorisökning.

  Om du vill markera flera grupper håller du ned Ctrl-tangenten (PC) eller Kommando-tangenten (Mac) när du klickar på varje grupp.

  ![Katalogsökning tillåts inte för allmän kundgrupp](./assets/category-permissions-disallow-category-search.png){width="600" zoomable="yes"}

## Steg 2: Använd kategoribehörigheter

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Välj målkategori i kategoriträdet.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) **[!UICONTROL Category Permissions]** på sidan och gör följande:

   - Om du vill skapa en behörighetsregel klickar du **[!UICONTROL New Permission]**.

     ![Avsnitt för kategoribehörigheter](./assets/category-permissions-section-admin.png){width="600" zoomable="yes"}

   - Välj lämplig **[!UICONTROL Website]** och **[!UICONTROL Customer Group]**.

   - Ange de enskilda behörigheterna efter behov.

   >[!NOTE]
   >
   >När `Browsing Category` = `Deny` behörighet har angetts för en överordnad kategori, den visas inte på [Breadcrumb-spår](navigation-breadcrumb-trail.md) på sidan med underordnade kategorier.

1. När du är klar klickar du på **[!UICONTROL Save]**.

>[!NOTE]
>
>Om någon **_Tillåt_** behörigheter anges för `Root Category`, tillämpas dessa behörigheter automatiskt på alla underkategorier och alla produkter i `Catalog`. Om någon produkt har tilldelats flera kategorier, och den har **_Tillåt_** behörigheter för minst en kategori, har automatiskt samma **_Tillåt_** behörigheter för alla tilldelade kategorier.
