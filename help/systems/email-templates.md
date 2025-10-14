---
title: E-postmallar
description: Lär dig mer om e-postmallar och hur du kan använda dem för att stödja kommunikation med dina kunder och förstärka ert varumärke.
exl-id: dfe28c77-607e-41e4-b872-3a07bcd67962
feature: Communications, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1151'
ht-degree: 0%

---

# E-postmallar

E-postmallar definierar layout, innehåll och formatering för automatiserade meddelanden som skickas från din butik. De kallas transaktionsbaserade e-postmeddelanden eftersom var och en är kopplad till en viss typ av transaktion eller händelse.

Commerce innehåller en uppsättning responsiva e-postmallar som aktiveras av olika händelser som inträffar när din butik används. Varje mall är optimerad för alla skärmstorlekar och kan visas både från skrivbordet och på surfplattor och mobila enheter. Det finns olika förberedda e-postmallar för kundaktiviteter, försäljning, produktvarningar, administratörsåtgärder och systemmeddelanden som du kan [anpassa](email-template-custom.md) efter ditt varumärke.

Commerce e-postmeddelanden kan återges av HTML och e-postklienter med oformaterad text. Det kan finnas vissa skillnader mellan klienterna när det gäller hur e-postmeddelanden återges.

## Förbered din e-postlogotyp

Logotyper kan sparas som någon av följande filtyper. Logotyper med genomskinliga bakgrunder kan sparas som GIF eller PNG-filer.

- JPG/JPEG
- GIF
- PNG

Det finns dimensioner angivna i rubrikmallen. För att logotypen ska kunna återges korrekt på enheter med hög upplösning bör den överförda bilden vara tre gånger så stor. Vanligtvis skapas den ursprungliga logotypen som en vektorbild, så att du kan skala upp den utan att förlora upplösningen. Bilden kan sedan sparas i ett av de bitmappsbildformat som stöds.

<!-- ![Logo 3X display size](./assets/email-logo-third-size.png)-->

Om du vill utnyttja det begränsade lodräta utrymmet i sidhuvudet måste du beskära bilden för att ta bort allt utrymme som går förlorat upptill eller nedtill. När du redigerar bilden bör du vara noga med att bevara logotypens proportioner, så att höjd och bredd ändras proportionellt.

Som regel kan du göra en bild mindre än originalet, men inte större utan att förlora upplösningen. Om du tar en liten bild och skalar upp den i en fotoredigerare sänks upplösningen i bilden. Om till exempel logotypens visningsdimensioner är 168 pixlar breda och 48 pixlar höga i rubrikmallen ska den överförda bilden vara 504 pixlar bred och 144 pixlar hög.

| Dimensioner för logotyp | 1 x (visningsstorlek) | 3 x (bildstorlek) |
|----------|----|----|
| Bredd: | 168 px | 504 px |
| Höjd | 48 px | 144 px |

{style="table-layout:auto"}

## Konfigurera e-postmallar

Konfigurationen avgör vilken logotyp som visas i standardsidhuvudsmallen och eventuella anpassade [sidhuvud](email-template-custom.md#header-template) - och [sidfot](email-template-custom.md#footer-template) -mallar som du vill använda för transaktionsmeddelanden som skickas från dina butiker.

![Transaktionell e-postdesign](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

En detaljerad lista över konfigurationsinställningarna finns i [_Transaktionsmeddelanden_](../content-design/configuration.md) i _Content and Design Guide_.

## Steg 1. Ladda upp din logotyp

1. Gå till **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**&#x200B;på sidofältet_ Admin _.

1. Leta reda på den butiksvy som du vill konfigurera och klicka på **[!UICONTROL Edit]** i kolumnen _[!UICONTROL Action]_.

1. Under _[!UICONTROL Other Settings]_&#x200B;expanderar du ![Expansionsväljaren](../assets/icon-display-expand.png) i avsnittet **[!UICONTROL Transactional Emails]**.

1. Om du vill överföra den förberedda **[!UICONTROL Logo Image]** klickar du på **[!UICONTROL Upload]** och väljer filen från datorn.

1. För **[!UICONTROL Logo Image Alt]** anger du alternativ text för att identifiera bilden.

1. Ange **[!UICONTROL Logo Width]** och **[!UICONTROL Logo Height]** i pixlar.

   Ange varje värde som ett tal, utan förkortningen `px`. Dessa värden avser visningsdimensionerna för logotypen i sidhuvudet och inte bildens verkliga storlek.

## Steg 2. Välj sidhuvud- och sidfotsmallar

Om du har anpassade sidhuvuds- och sidfotsmallar för din butik, eller för olika butiker, kan du ange vilka mallar som ska användas för varje, enligt [omfånget](../getting-started/websites-stores-views.md#scope-settings) för konfigurationen. I annat fall används standardmallarna. Mer information finns i [Anpassa e-postmallar](email-template-custom.md).

1. Välj **[!UICONTROL Header Template]** som ska användas för alla transaktionsmeddelanden.

1. Välj **[!UICONTROL Footer Template]** som ska användas för alla transaktionsmeddelanden.

1. Klicka på **[!UICONTROL Save Config]** när du är klar.

## E-postmallslista

Listan med e-postmallar ordnas i bokstavsordning efter modul.

### [!DNL Amazon_Payment]

| Mall | Konfigurationssökväg |
|--- |--- |
| `Hard-declined Authorization` | n/a |
| `Soft-declined Authorization` | n/a |

{style="table-layout:auto"}

### [!DNL Magento_Checkout]

| Mall | Konfigurationssökväg |
|--- |--- |
| `Payment Failed` | **Sida:** [!UICONTROL Sales] > [[!UICONTROL Checkout]](../configuration-reference/sales/checkout.md)<br/>**Avsnitt:** [!UICONTROL Payment Failed Emails]<br/>**Fält:** [!UICONTROL Payment Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_Company]

![Adobe Commerce B2B](../assets/b2b.svg) (endast tillgängligt med Adobe Commerce B2B)

| Mall | Konfigurationssökväg |
|--- |--- |
| `Assign Company Admin` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Avsnitt:** [!UICONTROL Customer-Related Emails]<br/>**Fält:** [!UICONTROL Default 'Assign Company Admin' Email] |
| `Assign Company to Customer` | **Sida:** [!UICONTROL Customers] > [Företagskonfiguration &#x200B;](../configuration-reference/customers/company-configuration.md)<br/>**Avsnitt:** [!UICONTROL Customer-Related Emails] <br/>**Fält:** [!UICONTROL Default 'Assign Company to Customer' Email] |
| `Company Admin Changed to Member` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Avsnitt:** [!UICONTROL Customer-Related Emails]<br/>**Fält:** [!UICONTROL Default 'Company Admin Changed To Member' Email] |
| `Company Admin Set Inactive` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Avsnitt:** [!UICONTROL Customer-Related Emails]<br/>**Fält:** [!UICONTROL Default 'Customer Status Inactive' Email] |
| `Company Invite` | n/a |
| `Company Registration Request` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Avsnitt:** [!UICONTROL Email Options - Company Registration]<br/>**Fält:** [!UICONTROL Default Company Registration Email] |
| `Company Status Active1` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Avsnitt:** [!UICONTROL Company Status Change]<br/>**Fält:** [!UICONTROL Default 'Company Status Change To Active 1" Email] |
| `Company Status Active2` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Avsnitt:** [!UICONTROL Company Status Change]<br/>**Fält:** [!UICONTROL Default 'Company Status Change To Active 2" Email] |
| `Company Status Blocked` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Avsnitt:** [!UICONTROL Company Status Change]<br/>**Fält:** [!UICONTROL Default 'Company Status Change To Blocked" Email] |
| `Company Status Pending Approval` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Avsnitt:** [!UICONTROL Company Status Change]<br/>**Fält:** [!UICONTROL Default 'Company Status Change To Pending Approval" Email] |
| `Company Status Rejected` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Avsnitt:** [!UICONTROL Company Status Change]<br/>**Fält:** [!UICONTROL Default 'Company Status Change To Rejected" Email] |
| `Customer Status Active` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Avsnitt:** [!UICONTROL Customer-Related Emails]<br/>**Fält:** [!UICONTROL Default 'Customer Status Active' Email] |
| `Customer Status Inactive` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Avsnitt:** [!UICONTROL Customer-Related Emails]<br/>**Fält:** [!UICONTROL Default 'Company Admin Inactive' Email] |
| `Sales Representative Assigned to Company` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Avsnitt:** [!UICONTROL Customer-Related Emails]<br/>**Fält:** [!UICONTROL Default 'Sales Rep Assigned' Email] |

{style="table-layout:auto"}

### [!DNL Magento_CompanyCredit]

![Adobe Commerce B2B](../assets/b2b.svg) (endast tillgängligt med Adobe Commerce B2B)

| Mall | Konfigurationssökväg |
|--- |--- |
| `Credit Limit Allocated` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Avsnitt:** [!UICONTROL Company Credit]<br/>**Fält:** [!UICONTROL Allocated Email Template] |
| `Credit Limit Updated` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Avsnitt:** [!UICONTROL Company Credit]<br/>**Fält:** [!UICONTROL Updated Email Template] |
| `Credit Reimbursed` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Avsnitt:** [!UICONTROL Company Credit]<br/>**Fält:** [!UICONTROL Reimbursed Email Template] |
| `Order Refunded to Company Credit` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Avsnitt:** [!UICONTROL Company Credit]<br/>**Fält:** [!UICONTROL Refunded Email Template] |
| `Order Reverted to Company Credit` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Avsnitt:** [!UICONTROL Company Credit]<br/>**Fält:** [!UICONTROL Reverted Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Contact]

| Mall | Konfigurationssökväg |
|--- |--- |
| `Contact Form` | **Sida:** [!UICONTROL General] > [[!UICONTROL Contacts]](../configuration-reference/general/contacts.md)<br/>**Avsnitt:** [!UICONTROL Email Options]<br/>**Fält:** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Customer]

| Mall | Konfigurationssökväg |
|--- |--- |
| `Change Email` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Avsnitt:** [!UICONTROL Account Information Options]<br/>**Fält:** [!UICONTROL Change Email Template] |
| Ändra e-post och lösenord | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Avsnitt:** [!UICONTROL Account Information Options]<br/>**Fält:** [!UICONTROL Change Email and Password Template] |
| `Forgot Password` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Avsnitt:** [!UICONTROL Password Options]<br/>**Fält:** Mall för glömd e-post |
| `New Account` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Avsnitt:** [!UICONTROL Create New Account Options]<br/>**Fält:** Standardvälkomstmeddelande |
| `New Account (Magento/luma)` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Avsnitt:** [!UICONTROL Create New Account Options]<br/>**Fält:** Standardvälkomstmeddelande |
| `New Account Confirmation Key` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Avsnitt:** [!UICONTROL Create New Account Options]<br/>**Fält:** Bekräftelselänkens e-postadress |
| `New Account Confirmed` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Avsnitt:** [!UICONTROL Create New Account Options]<br/>**Fält:** Välkomstmeddelande |
| `New Account Without Password` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Avsnitt:** [!UICONTROL Create New Account Options]<br/>**Fält:** Standardvälkomstmeddelande utan lösenord |
| `Remind Password` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Avsnitt:** [!UICONTROL Password Options]<br/>**Fält:** Påminn e-postmall |
| `Reset Password` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Avsnitt:** [!UICONTROL Password Options] <br/>**Fält:** Återställ lösenordsmall |

{style="table-layout:auto"}

### [!DNL Magento_CustomerBalance]

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)

| Mall | Konfigurationssökväg |
|--- |--- |
| `Store Credit Update` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Avsnitt:** [!UICONTROL Store Credit Options]<br/>**Fält:** [!UICONTROL Store Credit Update Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Directory]

| Mall | Konfigurationssökväg |
|--- |--- |
| `Currency Update Warnings` | **Sida:** [!UICONTROL General] > [[!UICONTROL Currency Setup]](../configuration-reference/general/currency-setup.md)<br/>**Avsnitt:** [!UICONTROL Scheduled Import Settings]<br/>**Fält:** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Email]

| Mall | Konfigurationssökväg |
|--- |--- |
| `Footer` | n/a |
| `Footer (Magento/luma)` | n/a |
| `Header` | n/a |

{style="table-layout:auto"}

### [!UICONTROL Magento_GiftCard]

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)

| Mall | Konfigurationssökväg |
|--- |--- |
| `Gift Card(s) Purchase` | **Sida:** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**Avsnitt:** [!UICONTROL Gift Card Email Settings]<br/>**Fält:** [!UICONTROL Gift Card Notification Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftCardAccount]

| Mall | Konfigurationssökväg |
|--- |--- |
| `Gift Card Code/Balance` | **Sida:** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**Avsnitt:** [!UICONTROL Email Sent from Gift Card Account Management]<br/>**Fält:** [!UICONTROL Gift Card Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftRegistry]

| Mall | Konfigurationssökväg |
|--- |--- |
| `New Registry` | **Sida:** [!UICONTROL &#x200B; Customers] > [[!UICONTROL &#x200B; Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**Avsnitt:** [!UICONTROL Owner Notification]<br/>**Fält:** [!UICONTROL Email Template] |
| `Registry Sharing` | **Sida:** [!UICONTROL &#x200B; Customers] > [[!UICONTROL &#x200B; Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**Avsnitt:** [!UICONTROL Gift Registry Sharing]<br/>**Fält:** [!UICONTROL Email Template] |
| `Registry Update` | **Sida:** [!UICONTROL &#x200B; Customers] > [[!UICONTROL &#x200B; Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**Avsnitt:** [!UICONTROL Gift Registry Update]<br/>**Fält:** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_InventoryInStorePickupSales]

| Mall | Konfigurationssökväg |
|--- |--- |
| `Order is Ready for Pickup` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL Order Ready For Pickup in Store]<br/>**Fält:** [!UICONTROL Order Ready For Pickup Email Template] |
| `Order is Ready for Pickup For Guest` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL Order Ready For Pickup in Store]<br/>**Fält:** [!UICONTROL Order Ready For Pickup Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_Invitation]

| Mall | Konfigurationssökväg |
|--- |--- |
| `Customer Invitation` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Invitation]](../configuration-reference/customers/invitations.md)<br/>**Avsnitt:** [!UICONTROL Email]<br/>**Fält:** [!UICONTROL Customer Invitation Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_NegotiableQuote]

![Adobe Commerce B2B](../assets/b2b.svg) (endast tillgängligt med Adobe Commerce B2B)

| Mall | Konfigurationssökväg |
|--- |--- |
| `Declined Quote` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL Quote]<br/>**Fält:** [!UICONTROL Declined Quote Template (to Buyer)] |
| `Expiration Date Reset` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL Quote]<br/>**Fält:** [!UICONTROL Expiration Date Reset] | **Sida:** [!UICONTROL Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL Quote]<br/>**Fält:** [!UICONTROL Order Ready For Pickup Email Template] |
| `Expiration Warning` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL Quote]<br/>**Fält:** [!UICONTROL Quote Expiration (in 48 hrs)] |
| `Expiration Warning1` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL Quote]<br/>**Fält:** [!UICONTROL Quote Expiration (in 24 hrs)] |
| `New Quote` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL Quote]<br/>**Fält:** [!UICONTROL New Quote Template (to Seller)] |
| `Updated Quote` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL Quote]<br/>**Fält:** [!UICONTROL Updated Quote Template (to Seller)] |

{style="table-layout:auto"}

### [!DNL Magento_Newsletter]

| Mall | Konfigurationssökväg |
|--- |--- |
| `Subscription Confirmation` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**Avsnitt:** [!UICONTROL &#x200B; Subscription Options]<br/>**Fält:** [!UICONTROL Confirmation Email Template] |
| `Subscription Success` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**Avsnitt:** [!UICONTROL &#x200B; Subscription Options]<br/>**Fält:** [!UICONTROL Success Email Template] |
| `Unsubscription Success` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**Avsnitt:** [!UICONTROL &#x200B; Subscription Options]<br/>**Fält:** [!UICONTROL Unsubscription Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_ProductAlert]

| Mall | Konfigurationssökväg |
|--- |--- |
| `Cron Error Warning` | **Sida:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**Avsnitt:** [!UICONTROL Product Alerts Run Settings]<br/>**Fält:** [!UICONTROL Error Email Template] |
| `Price Alert` | **Sida:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**Avsnitt:** [!UICONTROL Product Alerts]<br/>**Fält:** [!UICONTROL Price Alert Email Template] |
| `Stock Alert` | **Sida:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**Avsnitt:** [!UICONTROL Product Alerts]<br/>**Fält:** [!UICONTROL Stock Alert Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_PurchaseOrder]

| Mall | Konfigurationssökväg |
|--- |--- |
| `Approved Purchase Order` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL Purchase Order Approval]<br/>**Fält:** [!UICONTROL Approved Purchase Order] |
| `Approved, requires payment` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL Purchase Order Approval]<br/>**Fält:** [!UICONTROL Approved, requires payment details (to Buyer)] |
| `Comment added to Purchase Order` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL Purchase Order Approval]<br/>**Fält:** [!UICONTROL Comment added to Purchase Order] |
| `Created and Auto-approved Purchase Order` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL Purchase Order Approval]<br/>**Fält:** [!UICONTROL Created and Automatically approved Purchase Order (to Buyer)] |
| `Created and automatically approved, requires payment details` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL Purchase Order Approval]<br/>**Fält:** [!UICONTROL Created and automatically approved, requires payment details (to Buyer)] |
| `Created and requires Approval Purchase Order` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL Purchase Order Approval]<br/>**Fält:** [!UICONTROL Created and requires Approval Purchase Order (to Buyer)] |
| `Error creating Order from Purchase Order` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL Purchase Order Approval]<br/>**Fält:** [!UICONTROL Error creating Order from Purchase Order (to Buyer)] |
| `Purchase Order requires Approval` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL Purchase Order Approval]<br/>**Fält:** [!UICONTROL Purchase Order requires Approval (to Approver)] |
| `Rejected Purchase Order` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL Purchase Order Approval]<br/>**Fält:** [!UICONTROL Rejected Purchase Order (to Buyer)] |

{style="table-layout:auto"}

### [!DNL Magento_Reminder]

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)

| Mall | Konfigurationssökväg |
|--- |--- |
| `Promotion Notification/Reminder` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Promotions]](../configuration-reference/customers/promotions.md)<br/>**Avsnitt:** [!UICONTROL Automated Email Reminder Rules]<br/>**Fält:** [!UICONTROL Reminder Email Sender] |

{style="table-layout:auto"}

### [!DNL Magento_Reward]

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)

| Mall | Konfigurationssökväg |
|--- |--- |
| `Balance Update` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**Avsnitt:** [!UICONTROL Email Notification Settings]<br/>**Fält:** [!UICONTROL Balance Update Email] |
| `Points Expiry Warning` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**Avsnitt:** [!UICONTROL Email Notification Settings]<br/>**Fält:** [!UICONTROL Reward Points Expiry Warning Email] |

{style="table-layout:auto"}

### [!DNL Magento_Rma]

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)

| Mall | Konfigurationssökväg |
|--- |--- |
| `New RMA` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL &#x200B; RMA]<br/>**Fält:** [!UICONTROL RMA Email Template] |
| `New RMA for Guest` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL &#x200B; RMA]<br/>**Fält:** [!UICONTROL RMA Email Template for Guest] |
| `RMA Admin Comments` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL &#x200B; RMA Admin Comments]<br/>**Fält:** [!UICONTROL RMA Comment Email Template] |
| `RMA Admin Comments for Guest` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL &#x200B; RMA Admin Comments]<br/>**Fält:** [!UICONTROL RMA Comment Email Template for Guest] |
| `RMA Authorization` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL &#x200B; RMA Authorization]<br/>**Fält:** [!UICONTROL RMA Authorization Email Template] |
| `RMA Authorization for Guest` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL &#x200B; RMA Authorization]<br/>**Fält:** [!UICONTROL RMA Authorization Email Template for Guest] |
| `RMA Customer Comments` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Avsnitt:** [!UICONTROL RMA Customer Comments]<br/>**Fält:** [!DNL RMA Comment Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sales]

| Mall | Konfigurationssökväg |
|--- |--- |
| `Credit Memo Update` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Credit Memo Contents]<br/>**Fält:** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update (Magento/luma)` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Credit Memo Comments]<br/>**Fält:** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update for Guest` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Credit Memo Comments]<br/>**Fält:** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Credit Memo Update for Guest (Magento/luma)` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Credit Memo Comments]<br/>**Fält:** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Invoice Update` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Invoice Comments]<br/>**Fält:** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update (Magento/luma)` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Invoice Comments]<br/>**Fält:** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update for Guest` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Invoice Comments]<br/>**Fält:** [!UICONTROL Invoice Comment Email Template for Guest] |
| `Invoice Update for Guest (Magento/luma)` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Invoice Comments]<br/>**Fält:** [!UICONTROL Invoice Comment Email Template for Guest] |
| `New Credit Memo` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Credit Memo]<br/>**Fält:** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo (Magento/luma)` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]]../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Credit Memo]<br/>**Fält:** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo for Guest` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Credit Memo]<br/>**Fält:** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Credit Memo for Guest (Magento/luma)` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Credit Memo]<br/>**Fält:** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Invoice` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Invoice]<br/>**Fält:** [!UICONTROL Invoice Email Template] |
| `New Invoice (Magento/luma)` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Invoice]<br/>**Fält:** [!UICONTROL Invoice Email Template] |
| `New Invoice for Guest` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Invoice]<br/>**Fält:** [!UICONTROL Invoice Email Template for Guest] |
| `New Invoice for Guest (Magento/luma)` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Invoice]<br/>**Fält:** [!UICONTROL Invoice Email Template for Guest] |
| `New Order` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Order]<br/>**Fält:** [!UICONTROL New Order Confirmation Template] |
| `New Order (Magento/luma)` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Order]<br/>**Fält:** [!UICONTROL New Order Confirmation Template] |
| `New Order for Guest` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Order]<br/>**Fält:** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Order for Guest (Magento/luma)` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Order]<br/>**Fält:** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Shipment` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Shipment]<br/>**Fält:** [!UICONTROL Shipment Email Template] |
| `New Shipment (Magento/luma)` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Shipment]<br/>**Fält:** [!UICONTROL Shipment Email Template] |
| `New Shipment for Guest` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Shipment]<br/>**Fält:** [!UICONTROL Shipment Email Template for Guest] |
| `New Shipment for Guest (Magento/luma)` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Shipment]<br/>**Fält:** [!UICONTROL Shipment Email Template for Guest] |
| `Order Update` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Order Comments]<br/>**Fält:** [!UICONTROL Order Comment Email Template] |
| `Order Update (Magento/luma)` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Order Comments]<br/>**Fält:** [!UICONTROL Order Comment Email Template] |
| `Order Update for Guest` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Order Comments]<br/>**Fält:** [!UICONTROL Order Comment Email Template for Guest] |
| `Order Update for Guest (Magento/luma)` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Order Comments]<br/>**Fält:** [!UICONTROL Order Comment Email Template for Guest] |
| `Shipment Update` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Shipment Comments]<br/>**Fält:** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update (Magento/luma)` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Shipment Comments]<br/>**Fält:** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update for Guest` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Shipment Comments]<br/>**Fält:** [!UICONTROL Shipment Comment Email Template for Guest] |
| `Shipment Update for Guest (Magento/luma)` | **Sida:** [!UICONTROL &#x200B; Sales] > [[!UICONTROL &#x200B; Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Avsnitt:** [!UICONTROL Shipment Comments]<br/>**Fält:** [!UICONTROL Shipment Comment Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_ScheduledImportExport]

![Adobe Commerce](../assets/adobe-logo.svg) (endast Adobe Commerce)

| Mall | Konfigurationssökväg |
|--- |--- |
| `Export Failed` | **Sida:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**Avsnitt:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**Fält:** [!UICONTROL Export Failed Template] |
| `File History Clean Failed` | **Sida:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**Avsnitt:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**Fält:** [!UICONTROL Error Email Template] |
| `Import Failed` | **Sida:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**Avsnitt:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**Fält:** [!UICONTROL Import Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_SendFriend]

| Mall | Konfigurationssökväg |
|--- |--- |
| `Send Product Link to Friend` | **Sida:** [!UICONTROL Catalog] > [[!UICONTROL Email to a Friend]](../configuration-reference/catalog/email-to-a-friend.md)<br/>**Avsnitt:** [!UICONTROL Email Templates]<br/>**Fält:** [!UICONTROL Select Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sitemap]

| Mall | Konfigurationssökväg |
|--- |--- |
| `Sitemap Generation Settings` | **Sida:** [!UICONTROL Catalog] > [[!UICONTROL XML Sitemap]](../configuration-reference/catalog/xml-sitemap.md)<br/>**Avsnitt:** [!UICONTROL Generation Settings]<br/>**Fält:** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_TwoFactorAuth]

| Mall | Konfigurationssökväg |
|--- |--- |
| `2FA Configuration Required by User` | n/a |
| `2FA Configuration Required for the Application` | n/a |

{style="table-layout:auto"}

### [!DNL Magento_User]

| Mall | Konfigurationssökväg |
|--- |--- |
| `Forgot Admin Password` | **Sida:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**Avsnitt:** [!UICONTROL Admin User Emails]<br/>**Fält:** E-postmall för glömt lösenord |
| `User Notification` | **Sida:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**Avsnitt:** [!UICONTROL Admin User Emails]<br/>**Fält:** Användarmeddelandemall |
| `New User Notification` | **Sida:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**Avsnitt:** [!UICONTROL Admin User Emails]<br/>**Fält:** [!UICONTROL New User Notification Template] |

{style="table-layout:auto"}

### [!DNL Magento_Wishlist]

| Mall | Konfigurationssökväg |
|--- |--- |
| `Magento Wish List Sharing` | **Sida:** [!UICONTROL Customers] > [[!UICONTROL Wish List]](../configuration-reference/customers/wishlist.md)<br/>**Avsnitt:** [!UICONTROL Share Options]<br/>**Fält:** [!UICONTROL Email Template] |

{style="table-layout:auto"}
