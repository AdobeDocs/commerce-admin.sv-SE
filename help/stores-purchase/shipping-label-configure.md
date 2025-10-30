---
title: Konfigurera etiketter för leverans
description: Lär dig hur du konfigurerar butik för att generera fraktetiketter.
exl-id: 0693d74b-8b36-4a36-8739-c9fe5a934ff0
feature: Shipping/Delivery, Orders
source-git-commit: d5beff4d450dab21f74e5baec6b718b844963858
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 0%

---

# Konfigurera etiketter för leverans

Följande inställningar måste göras på produktnivå och i konfigurationen för varje bärare som används för att skriva ut etiketter. Om du vill skriva ut etiketter måste du öppna ett konto för alla transportföretag. Slutför sedan konfigurationen i din butik för varje operatör som du tänker använda.

## Krav för transportföretag

| [!UICONTROL Carrier] | Krav |
|-------|--------|
| [USPS](usps.md) | Kräver ett USPS-konto för fraktsetikettposten. |
| [UPS](ups.md) | Kräver ett UPS-konto. Leveransetiketter är bara tillgängliga för leveranser som har sitt ursprung i USA-specifika autentiseringsuppgifter krävs för butiker utanför USA. |
| [FedEx](fedex.md) | Kräver ett FedEx-konto. För butiker utanför USA stöds etiketter endast för internationella leveranser. FedEx tillåter inte inhemska leveranser som kommer utanför USA |
| [DHL](dhl.md) | Kräver ett DHL-konto. Leveransetiketter stöds endast för leveranser som har sitt ursprung i USA. |

{style="table-layout:auto"}

## Steg 1: Verifiera tillverkningslandet

Tillverkningslandet krävs för alla produkter som levereras internationellt av USPS och FedEx. Om du har många produkter som ska uppdateras kan du antingen [importera](../systems/data-import.md) uppdateringarna eller använda lagerrutnätet för att uppdatera flera poster.

1. Gå till _>_ på sidofältet **[!UICONTROL Catalog]** Admin **[!UICONTROL Products]**.

1. Uppdatera etikettposten för frakt på något av följande sätt.

### Metod 1: Uppdatera en enskild post

1. Leta reda på produkten som ska uppdateras i rutnätet och öppna den i redigeringsläge.

1. Uppdatera **tillverkningslandet** efter behov.

   ![Tillverkningsland](./assets/product-country-of-manufacture.png){width="700" zoomable="yes"}

1. Klicka på **[!UICONTROL Save]**.

### Metod 2: Uppdatera flera poster

1. Markera kryssrutan för varje produkt som ska uppdateras i rutnätet.

   Till exempel alla produkter som tillverkas i Kina.

1. Ställ in kontrollen **[!UICONTROL Actions]** på `Update Attributes` och klicka på **[!UICONTROL Submit]**.

1. I formuläret _Uppdatera attribut_ letar du reda på fältet **Tillverkningsland** och markerar kryssrutan **Ändra**.

1. Välj land.

1. Klicka på **[!UICONTROL Save]**.

## Steg 2 Verifiera butiksinformationen

1. Gå till _>_ > **[!UICONTROL Stores]** på sidofältet _[!UICONTROL Settings]_&#x200B;Admin **[!UICONTROL Configuration]**.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Shipping Settings]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Origin]** och kontrollera att följande fält är fullständiga:

   - **[!UICONTROL Street Address]** - Gatuadressen till den plats varifrån försändelser skickas. Till exempel var ditt företag eller lagerställe finns. Det här fältet är obligatoriskt för fraktsetiketter.
   - **[!UICONTROL Street Address Line 2]** - All ytterligare adressinformation, till exempel golvet eller ingången. Vi rekommenderar att du använder det här fältet.

   ![Ursprung](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. Välj _i avsnittet_ Försäljning **[!UICONTROL Delivery Methods]** i den vänstra panelen.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL USPS]** och kontrollera att följande fält är fullständiga:

   - **[!UICONTROL Secure Gateway URL]** - Systemet anger automatiskt gateway-URL:en.
   - **[!UICONTROL Password]** - Lösenordet tillhandahålls av USPS och ger dig åtkomst till deras system via webbtjänster.
   - **Längd, Bredd, Höjd, Tjocklek** - Paketets standardmått. Om du vill att de här fälten ska visas anger du **[!UICONTROL Size]** till `Large`.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **FedEx** och kontrollera att följande fält är fullständiga:

   - Mätarnummer
   - Nyckel
   - Lösenord

   Den här informationen tillhandahålls av leverantören och krävs för att få åtkomst till systemet via webbtjänster.

1. Expandera **[!UICONTROL General]** i den vänstra panelen och välj **[!UICONTROL General]** under.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Store Information]** och kontrollera att följande fält är fullständiga:

   - **[!UICONTROL Store Name]** - Namnet på butiken eller butiksvyn.
   - **[!UICONTROL Store Contact Telephone]** - Telefonnumret till den primära kontakten för butiks- eller butiksvyn.
   - **[!UICONTROL Country]** - Det land där din butik är baserad.
   - **[!UICONTROL VAT Number]** - Om tillämpligt, momsregistreringsnumret för moms för din butik. (Krävs inte för butiker i USA.)
   - **[!UICONTROL Store Contact Address]** - Gatuadressen till den primära kontakten för butiks- eller butiksvyn.

1. Om du har flera arkiv och kontaktinformationen skiljer sig från standardinställningen anger du **[!UICONTROL Store View]** för varje och kontrollerar att informationen är fullständig.

   Om informationen saknas visas ett fel när du försöker skriva ut etiketterna.

   ![Lagra information](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Save Config]**.
