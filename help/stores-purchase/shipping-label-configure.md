---
title: Konfigurera etiketter för leverans
description: Lär dig hur du konfigurerar butik för att generera fraktetiketter.
exl-id: 0693d74b-8b36-4a36-8739-c9fe5a934ff0
feature: Shipping/Delivery, Orders
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# Konfigurera etiketter för leverans

Följande inställningar måste göras på produktnivå och i konfigurationen för varje bärare som används för att skriva ut etiketter. Om du vill skriva ut etiketter måste du öppna ett konto för alla transportföretag. Slutför sedan konfigurationen i din butik för varje operatör som du tänker använda.

## Krav för transportföretag

| [!UICONTROL Carrier] | Krav |
|-------|--------|
| [USPS](usps.md) | Kräver ett USPS-konto. Från och med den 23 februari 2018 kräver USPS att alla fraktsedlar ska innehålla frakt. |
| [UPS](ups.md) | Kräver ett UPS-konto. Leveransetiketter är bara tillgängliga för leveranser som har sitt ursprung i USA-specifika autentiseringsuppgifter krävs för butiker utanför USA. |
| [FedEx](fedex.md) | Kräver ett FedEx-konto. För butiker utanför USA stöds etiketter endast för internationella leveranser. FedEx tillåter inte inhemska leveranser som kommer utanför USA |
| [DHL](dhl.md) | Kräver ett DHL-konto. Leveransetiketter stöds endast för leveranser som har sitt ursprung i USA. |

{style="table-layout:auto"}

## Steg 1: Verifiera tillverkningslandet

Tillverkningslandet krävs för alla produkter som levereras internationellt av USPS och FedEx. Om du har många produkter som ska uppdateras kan du antingen [import](../systems/data-import.md) uppdateringarna eller använd lagerrutnätet för att uppdatera flera poster.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Uppdatera etikettposten för frakt på något av följande sätt.

### Metod 1: Uppdatera en enskild post

1. Leta reda på produkten som ska uppdateras i rutnätet och öppna den i redigeringsläge.

1. Uppdatera **Tillverkningsland** efter behov.

   ![Tillverkningsland](./assets/product-country-of-manufacture.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]**.

### Metod 2: Uppdatera flera poster

1. Markera kryssrutan för varje produkt som ska uppdateras i rutnätet.

   Till exempel alla produkter som tillverkas i Kina.

1. Ange **[!UICONTROL Actions]** styra till `Update Attributes` och klicka **[!UICONTROL Submit]**.

1. I _Uppdatera attribut_ formulär, hitta **Tillverkningsland** och välj **Ändra** kryssrutan.

1. Välj land.

1. Klicka på **[!UICONTROL Save]**.

## Steg 2 Verifiera butiksinformationen

{{beta2-updates}}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Expandera på den vänstra panelen **[!UICONTROL Sales]** och välja **[!UICONTROL Shipping Settings]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Origin]** och verifiera att följande fält är fullständiga:

   - **[!UICONTROL Street Address]** - Gatuadressen till den plats varifrån försändelsen skickas. Till exempel var ditt företag eller lagerställe finns. Det här fältet är obligatoriskt för fraktsetiketter.
   - **[!UICONTROL Street Address Line 2]** - All ytterligare adressinformation, t.ex. golvet eller ingången. Vi rekommenderar att du använder det här fältet.

   ![Ursprung](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. I _Försäljning_ väljer du **[!UICONTROL Delivery Methods]**.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL USPS]** och verifiera att följande fält är fullständiga:

   - **[!UICONTROL Secure Gateway URL]** - Systemet matar automatiskt in gateway-URL:en.
   - **[!UICONTROL Password]** - Lösenordet tillhandahålls av USPS och ger dig åtkomst till deras system via webbtjänster.
   - **Längd, bredd, höjd, Girth** - Paketets standarddimensioner. Ange att fälten ska visas **[!UICONTROL Size]** till `Large`.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **FedEx** och verifiera att följande fält är fullständiga:

   - Mätarnummer
   - Nyckel
   - Lösenord

   Den här informationen tillhandahålls av leverantören och krävs för att få åtkomst till systemet via webbtjänster.

1. Expandera på den vänstra panelen **[!UICONTROL General]** och välja **[!UICONTROL General]** under.

1. Expandera ![Expansionsväljare](../assets/icon-display-expand.png) den **[!UICONTROL Store Information]** och verifiera att följande fält är fullständiga:

   - **[!UICONTROL Store Name]** - Namnet på butiken eller butiksvyn.
   - **[!UICONTROL Store Contact Telephone]** - Telefonnumret till den primära kontakten för butiks- eller butiksvyn.
   - **[!UICONTROL Country]** - Det land där din butik finns.
   - **[!UICONTROL VAT Number]** - I tillämpliga fall, butikens momsregistreringsnummer. (Krävs inte för butiker i USA.)
   - **[!UICONTROL Store Contact Address]** - Gatuadressen till den primära kontakten för butiken eller butiksvyn.

1. Om du har flera butiker och kontaktinformationen skiljer sig från standardinställningen anger du **[!UICONTROL Store View]** för varje och kontrollera att informationen är fullständig.

   Om informationen saknas visas ett fel när du försöker skriva ut etiketterna.

   ![Butiksinformation](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]**.
