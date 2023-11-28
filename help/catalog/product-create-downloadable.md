---
title: Nedladdningsbar produkt
description: Lär dig hur du skapar en nedladdningsbar produkt som kan levereras som en digital fil.
exl-id: c3dd4c5f-adc1-4a8f-a9da-7f0dedd1ee34
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1619'
ht-degree: 0%

---

# Nedladdningsbar produkt

En nedladdningsbar produkt kan vara allt du kan leverera som en fil, till exempel en eBook, musik, video, programvara eller uppdatering. Du kan erbjuda ett album att sälja och sälja varje låt separat. Du kan också använda en nedladdningsbar produkt för att leverera en elektronisk version av produktkatalogen.

Eftersom nedladdningen inte är tillgänglig förrän efter köpet kan du ta fram exempel, t.ex. ett utdrag från en bok, ett klipp från en ljudfil eller en trailer från en video. Ett exempel är något som kunden kan prova innan man köper produkten. De filer du gör tillgängliga för hämtning kan antingen överföras till servern eller från en annan server.

![Nedladdningsbar produkt](./assets/storefront-product-downloadable.png){width="700" zoomable="yes"}

Hämtningsbara produkter kan konfigureras så att kunden måste logga in på ett konto för att kunna ta emot länken eller skickas med e-post och dela dem med andra. Status för ordern innan hämtningen blir tillgänglig, standardvärden och andra leveransalternativ anges i konfigurationen. När du planerar dina hämtningsbara katalogtillägg bör du tänka på följande:

- Hämtningsbara produkter kan överföras till servern eller länkas till från en annan server på Internet.

- Du kan bestämma hur många gånger en kund kan hämta en produkt.

- Kunder som köper en nedladdningsbar produkt kan behöva logga in innan de går igenom kassan.

- Leveransen av en nedladdningsbar produkt kan göras när beställningen görs i antingen en `Pending` eller `Invoiced` status.

- Eftersom nedladdningsbara produkter inte levereras kan _Leverans_ steg i utcheckningen hoppas över när vagnen bara innehåller den nedladdningsbara produkten.


## Konfigurera hämtningsalternativ

De hämtningsbara konfigurationsinställningarna avgör standardvärdena och leveransalternativen för hämtningsbara produkter och anger om gästerna kan köpa hämtningar.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Catalog]** och välja **[!UICONTROL Catalog]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den _[!UICONTROL Downloadable Product Options]_-avsnitt.

   ![Nedladdningsbara produktalternativ](../configuration-reference/catalog/assets/catalog-downloadable-product-options.png){width="700" zoomable="yes"}

   En detaljerad lista över dessa konfigurationsalternativ finns i [_Nedladdningsbara produktalternativ_](../configuration-reference/catalog/catalog.md#downloadable-product-options) i _Konfigurationsreferens_.

1. Ange status för orderprocessen när nedladdningen blir tillgänglig **[!UICONTROL Order Item Status to Enable Downloads]** till något av följande:

   - `Pending`
   - `Invoiced`

1. Om du vill ange en standardgräns för hur många hämtningar en enskild kund kan göra anger du numret för **[!UICONTROL Default Maximum Number of Downloads]**.

1. Ange **[!UICONTROL Shareable]** till något av följande:

   - `Yes` - Gör det möjligt för kunder att skicka nedladdningslänken till andra.
   - `No` - Hindrar kunder från att dela nedladdningslänken med andra genom att kräva att kunderna loggar in på sina konton för att få tillgång till nedladdningslänkar.

1. För **[!UICONTROL Default Sample Title]** anger du den rubrik som du vill ska visas ovanför urvalet.

   ![Exempeltitel](./assets/product-downloadable-config-sample-title.png){width="400"}

1. För **[!UICONTROL Default Link Title]** anger du den standardtext som du vill använda för att hämta länkar.

1. Om du vill att nedladdningslänken ska öppnas i ett nytt webbläsarfönster anger du **[!UICONTROL Opens Links in New Window]** till `Yes`.

   Den här inställningen används för att hålla webbläsarfönstret öppet.

1. Ange hur hämtningsbart innehåll ska levereras **[!UICONTROL Use Content Disposition]** till något av följande:

   - `Attachment` - Levererar nedladdningslänken via e-post som en bilaga.
   - `Inline` - Levererar nedladdningslänken som en länk på en webbplats.

1. Om du vill att köpare ska registrera sig för ett kundkonto och logga in innan de köper en nedladdning anger du **[!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items]** till `Yes`.

1. När du är klar klickar du på **[!UICONTROL Save Config]**.

## Skapa en nedladdningsbar produkt

I följande anvisningar visas hur du skapar en nedladdningsbar produkt med hjälp av en [produktmall](attribute-sets.md), obligatoriska fält och grundläggande inställningar. Varje obligatoriskt fält markeras med en röd asterisk (`*`). När du är klar med grunderna kan du slutföra de andra produktinställningarna efter behov.

>[!NOTE]
>
>Filnamn som kan hämtas kan innehålla bokstäver och siffror. Ett streck eller ett understreck kan användas för att representera ett mellanrum mellan ord. Alla ogiltiga tecken i filnamnet ersätts med ett understreck.

### Steg 1: Välj produkttyp

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. På _[!UICONTROL Add Product]_( ![Menypil](../assets/icon-menu-down-arrow-red.png){width="25"} ) i det övre högra hörnet väljer du `Downloadable Product`.

   ![Lägg till hämtningsbar produkt](./assets/product-add-downloadable.png){width="700" zoomable="yes"}

### Steg 2: Välj attributuppsättning

Exempeldata innehåller en [attributuppsättning](attribute-sets.md) anropad _Nedladdningsbar_ som har specialområden för nedladdningsbara produkter. Du kan använda en befintlig mall eller skapa en annan innan produkten sparas.

Gör något av följande om du vill välja den attributuppsättning som används som mall för produkten:

- För **[!UICONTROL Search]** anger du namnet på attributuppsättningen.

- Välj `Downloadable` attributuppsättning.

Formuläret uppdateras för att återspegla ändringen.

![Välj attributuppsättning](./assets/product-create-choose-attribute-set-downloadable.png){width="600" zoomable="yes"}

### Steg 3: Slutför de obligatoriska inställningarna

1. Ange **[!UICONTROL Product Name]**.

1. Acceptera standardinställningen **[!UICONTROL SKU]** som baseras på produktnamnet eller anger ett annat.

1. Ange produkten **[!UICONTROL Price]**.

1. Eftersom produkten ännu inte är klar att publiceras kan du ange **[!UICONTROL Enable Product]** till `No`.

1. klicka **[!UICONTROL Save]** och fortsätta.

   När produkten sparas kan du [Butiksvy](introduction.md#product-scope) Väljaren visas i det övre vänstra hörnet.

1. Välj **[!UICONTROL Store View]** där produkten ska finnas tillgänglig.

   ![Välj butiksvy](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Steg 4: Slutför de grundläggande inställningarna

1. Ange **[!UICONTROL Tax Class]** till något av följande:

   - `None`
   - `Taxable Goods`

1. Ange **[!UICONTROL Quantity]** av den produkt som finns i lager.

   Observera följande:

   - Som standard **[!UICONTROL Stock Status]** är inställd på `Out of Stock`.

   - Eftersom nedladdningsbara produkter inte levereras kan **[!UICONTROL Weight]** fältet används inte. Om du aktiverar den här funktionen blir den [Enkel produkt](product-create-simple.md) och _Är den här nedladdningsbara produkten?_ kan inte användas.

   >[!NOTE]
   >
   >Om du aktiverar [Inventory management](../inventory-management/introduction.md), försäljare med en källa anger kvantiteten i det här avsnittet. Flera källhandlare lägger till källor och kvantiteter i avsnittet Källor. Se följande _Tilldela källor och kvantiteter (Inventory management)_ -avsnitt.

1. Acceptera standardinställningen **[!UICONTROL Visibility]** inställning för `Catalog, Search`.

1. Så här fungerar produkten i [lista över nya produkter](../content-design/widget-new-products-list.md)väljer du **[!UICONTROL Set Product as New]** kryssrutan.

1. Tilldela _[!UICONTROL Categories]_till produkten klickar du på&#x200B;**[!UICONTROL Select…]**och gör något av följande:

   **Välj en befintlig kategori**:

   - Börja skriva i rutan tills du hittar en matchning.

   - Markera kryssrutan för varje kategori som ska tilldelas.

   **Skapa en kategori**:

   - Klicka på **[!UICONTROL New Category]**.

   - Ange **[!UICONTROL Category Name]** och väljer **[!UICONTROL Parent Category]**, som bestämmer dess position i [menystruktur](category-root.md).

   - Klicka på **[!UICONTROL Create Category]**.

1. Ange **[!UICONTROL Format]** till något av följande:

   - `Download`
   - `DVD`

   Om det behövs kan du redigera [attribute](attribute-product-create.md) om du vill lägga till fler värden.

   Det kan finnas ytterligare attribut som beskriver produkten. Markeringen varierar beroende på attributuppsättning och du kan slutföra dem senare.

#### Tilldela källor och kvantiteter ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

### Steg 5: Fyll i den hämtningsbara informationen

Bläddra nedåt, expandera ![Expansionsväljare](../assets/icon-display-expand.png) den _[!UICONTROL Downloadable Information]_och väljer **[!UICONTROL Is this downloadable product?]**kryssrutan.

När det är aktiverat visas _[!UICONTROL Downloadable Information]_-avsnittet har två delar. I den första delen beskrivs varje nedladdningslänk och i den andra delen beskrivs varje exempelfil. Standardvärdet för många av dessa alternativ kan anges i [konfiguration](#configure-the-download-options).

![Nedladdningsbar information](./assets/product-downloadable-information.png){width="600" zoomable="yes"}

#### Fyll i länkarna

1. I _[!UICONTROL Links]_anger du **[!UICONTROL Title]**som du vill använda som rubrik för nedladdningslänkarna.

1. Välj **[!UICONTROL Links can be purchased separately]** kryssrutan.

1. Klicka **[!UICONTROL Add Link]** och gör följande:

   - Ange **[!UICONTROL Title]** och **[!UICONTROL Price]** av nedladdningen.

   - För båda **[!UICONTROL File]** och **[!UICONTROL Sample]** väljer du en av följande distributionsmetoder för nedladdningarna:

      - `Upload File` - Välj den här metoden om du vill överföra distributionsfilen till servern. Bläddra till filen och markera den för överföring.
      - `URL` - Välj den här metoden om du vill komma åt distributionsfilen från en URL. Ange den fullständiga URL:en till den hämtade filen.

   >[!NOTE]
   >
   >Du kan inte använda länkar till externa resurser som hämtningsbara produkter. Giltiga länkdomäner fördefinieras programmatiskt i `env.php` fil (se [env.php reference](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/files/config-reference-envphp.html) i _Konfigurationshandbok_).

   - Ange **[!UICONTROL Shareable]** till något av följande:

      - `No` - Kunder måste logga in på sina konton för att få åtkomst till nedladdningslänken.

      - `Yes` - Skickar länken via e-post, som kunderna kan dela med andra.

      - `Use Config` - Använder metoden som anges i [Nedladdningsbara produktalternativ](../configuration-reference/catalog/catalog.md) konfiguration.

   - Gör något av följande:

      - Om du vill begränsa antalet nedladdningar per kund anger du det maximala antalet för **[!UICONTROL Max. Downloads]**.
      - Om du vill tillåta ett obegränsat antal nedladdningar väljer du **[!UICONTROL Unlimited]** kryssrutan.

   ![Länkdetalj](./assets/product-downloadable-link-detail.png){width="600" zoomable="yes"}

1. Om du vill lägga till en länk klickar du på **[!UICONTROL Add Link]** och upprepa dessa steg.

#### Fyll i exemplen

1. I _[!UICONTROL Samples]_anger du **[!UICONTROL Title]**som du vill använda som rubrik för exemplen.

1. Om du vill fylla i informationen för varje prov klickar du på **[!UICONTROL Add Link]**.

   ![Exempel](./assets/product-downloadable-samples.png){width="600" zoomable="yes"}

1. Fyll i länkinformationen enligt följande:

   - Ange **[!UICONTROL Title]** av det enskilda provet.

   - Välj någon av följande distributionsmetoder:

      - `Upload File` - Välj den här metoden om du vill överföra distributionsfilen till servern. Bläddra till filen och markera den för överföring.
      - `URL` - Välj den här metoden om du vill komma åt distributionsfilen från en URL. Ange den fullständiga URL:en till den hämtade filen.

   - Om du vill lägga till ytterligare ett exempel klickar du **[!UICONTROL Add Link]** och upprepa dessa steg.

   - Om du vill ändra ordningen på proverna tar du _Ändra ordning_ ( ![Positionskontroll](../assets/icon-sort-order.png) ) och dra exemplet till en ny plats.

### Steg 6: Fyll i produktinformationen

Bläddra nedåt och fyll i informationen i följande avsnitt efter behov:

- [Innehåll](product-content.md)
- [Bilder och video](product-images-and-video.md)
- [Sökmotoroptimering](product-search-engine-optimization.md)
- [Samhörande produkter, merförsäljning och korsförsäljning](related-products-up-sells-cross-sells.md)
- [Anpassningsbara alternativ](settings-advanced-custom-options.md)
- [Produkter på webbplatser](settings-basic-websites.md)
- [Design](settings-advanced-design.md)
- [Presentalternativ](product-gift-options.md)

### Steg 7: Publicera produkten

Om du är redo att publicera produkten i katalogen anger du **[!UICONTROL Enable Product]** till `Yes` och gör något av följande:

**Metod 1:** Spara och förhandsgranska

- Klicka på i det övre högra hörnet **[!UICONTROL Save]**.

- Om du vill visa produkten i din butik väljer du **[!UICONTROL Customer View]** på _Administratör_ ( ![Menypil](../assets/icon-menu-down-arrow-black.png) ).

  Butiken öppnas på en ny flik i webbläsaren.

  ![Kundvy](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

**Metod 2:** Spara och stäng

På _[!UICONTROL Save]_( ![Menypil](../assets/icon-menu-down-arrow-red.png){width="25"} ) väljer du **[!UICONTROL Save & Close]**.

## StoreFront

På kontrollpanelen för kundkonton visas _[!UICONTROL My Downloadable Products]_sid-länkar till varje order med nedladdningsbara produkter. Nedladdningarna blir tillgängliga från kundens konto när beställningen är klar.

![Mina nedladdningsbara produkter](./assets/customer-account-my-downloadable-products.png){width="700" zoomable="yes"}

I följande tabell beskrivs _Mina nedladdningsbara produkter_ värden:

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Order#] | The [beställa](../stores-purchase/orders.md) där den nedladdningsbara produkten köptes. Tillhandahåller en länk till orderinformationen. |
| [!UICONTROL Date] | Orderskapandedatum. |
| [!UICONTROL Title] | Namnet på den hämtningsbara produkten som köpts tillsammans med ordern. En länk till den hämtningsbara produkten. |
| [!UICONTROL Status] | Beställningsstatus. |
| [!UICONTROL Remaining Downloads] | Antal tillgängliga hämtningar av den hämtade produkten. |

_**Så här hämtar du en produktfil från kontrollpanelen för konton**_

1. På kontouppsättningen väljer kunden **[!UICONTROL My Downloadable Products]**.

1. Söker efter ordningen i listan och klickar på länken efter titeln.

1. Klicka i det nedre högra hörnet av hämtningsfönstret på _ladda ned_ -ikon.

1. Söker efter filen på hämtningsplatsen och sparar filen på önskad plats.
