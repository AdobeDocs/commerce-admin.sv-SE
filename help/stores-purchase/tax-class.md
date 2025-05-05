---
title: Skatteklasser
description: Lär dig hur du konfigurerar de momsklasser som används för momsregler.
exl-id: dd867eba-3f1e-45a8-9332-9e668a2092e1
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# Skatteklasser

Skatteklasser kan tilldelas kunder, produkter och frakt. Commerce analyserar kundvagnen och beräknar lämplig moms utifrån kundens klass, produktklass i kundvagnen och region. Regionen bestäms av kundens leveransadress, faktureringsadress eller leveransadress. Nya momsklasser kan skapas när en [momsregel](tax-rules.md) definieras.

- **Kund** - Du kan skapa så många kundmomsklasser som du behöver och tilldela dem till [kundgrupper](../customers/customer-groups.md). I vissa jurisdiktioner beskattas till exempel inte partihandelstransaktioner, men detaljhandelstransaktioner beskattas. Du kan associera medlemmar i kundgruppen för grossister med momsklassen för grossistledet.

- **Produkt** - Produktklasser används i beräkningar för att fastställa att rätt momssats tillämpas i kundvagnen. När du skapar en produkt tilldelas den till en viss momsklass. Till exempel kanske inte maten beskattas eller beskattas i en annan omfattning.

- **Leverans** - Om din butik debiterar en extra avgift vid frakt bör du ange en specifik produktskatteklass för frakt. I konfigurationen anger du den sedan som den momsklass som används för leverans.

## Konfigurera momsklasser

Den momsklass som används för leverans och standardmomsklasserna för [produkter och kunder](#add-a-product-tax-class) anges i konfigurationen _[!UICONTROL Sales]_.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Tax]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Tax Classes]**.

   ![Konfiguration - momsklasser](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. Välj momsklass för följande:

   - **[!UICONTROL Set Tax Class for Shipping]**
   - **[!UICONTROL Tax Class for Gift Options]**
   - **[!UICONTROL Default Tax Class for Product]**
   - **[!UICONTROL Default Tax Class for Customer]**

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## Lägg till momsklasser

Skatteklasser för kunder och produkter kan enkelt läggas till och sedan tilldelas enskilda kunder och produkter, och användas i skatteregler.

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**&#x200B;på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Add New Tax Rule]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Additional Settings]**.

   ![Lägg till ny momsklass](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. Klicka på **[!UICONTROL Add New Tax Class]** under _Kundskatteklass_.

1. Ange **[!UICONTROL Name]** för den nya skatteklassen i textrutan.

   ![Lägg till ny momsklass](./assets/tax-class-customer-add-new.png){width="600" zoomable="yes"}

1. Om du vill lägga till den nya klassen i listan över tillgängliga kundmomsklasser klickar du på bockmarkeringen.

   ![Nya momsklasser](./assets/tax-classes-updated.png){width="600" zoomable="yes"}

## Lägg till en produktskatteklass

1. Klicka på **[!UICONTROL Add New Tax Class]** under _Produktskatteklass_.

1. Ange **[!UICONTROL Name]** för den nya skatteklassen i textrutan.

1. Om du vill lägga till den nya klassen i listan över tillgängliga produktskatteklasser klickar du på bockmarkeringen.

1. När du är klar klickar du på **[!UICONTROL Back]** i knappfältet för att gå tillbaka till rutnätet _Skatteregler_.

## Standardmomsmål

Standardinställningarna för skattedestination avgör vilket land, delstat och postnummer som används som underlag för momsberäkningar.

**_Så här konfigurerar du standardmålet för skatt för beräkningar:_**

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales]** i den vänstra panelen och välj **[!UICONTROL Tax]**.

1. Expandera ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Default Tax Destination Calculation]**.

   ![Beräkning av standardmomsmål](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. Ange **[!UICONTROL Default Country]** till landet som momsberäkningar baseras på.

1. Ange **[!UICONTROL Default State]** till den delstat eller provins som används som underlag för momsberäkningar.

1. Ange **[!UICONTROL Default Post Code]** till det postnummer eller postnummer som används som bas för lokala momsberäkningar.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.
